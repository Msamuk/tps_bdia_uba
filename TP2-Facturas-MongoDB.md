## Aggregation Framework en MongoDB 

### 1. Realizar una consulta que devuelva la siguiente información: Región y cantidad total de productos vendidos a clientes de esa Región. 

```json

db.getCollection('facturas').aggregate(
  [
    { $unwind: '$item' },
    {
      $group: {
        _id: '$cliente.region',
        totalProductosVendidos: {
          $sum: '$item.cantidad'
        }
      }
    },
    {
      $project: {
        _id: 0,
        region: '$_id',
        totalProductosVendidos: 1
      }
    }
  ]
);

```

```json
Result sample:
[
  {
      "totalProductosVendidos": 180,
      "region": "CENTRO"
  }
]
```
#### 2. Basado en la consulta del punto 1, mostrar sólo la región que tenga el menor ingreso. 

```json
db.getCollection('facturas').aggregate(
  [
    { $unwind: '$item' },
    {
      $group: {
        _id: '$cliente.region',
        ingresoTotal: {
          $sum: {
            $multiply: [
              '$item.cantidad',
              '$item.precio'
            ]
          }
        }
      }
    },
    { $sort: { ingresoTotal: 1 } },
    { $limit: 1 },
    {
      $project: {
        _id: 0,
        region: '$_id',
        ingresoTotal: 1
      }
    }
  ]);
```
```json
Result sample:
[
  {
      "ingresoTotal": 9800,
      "region": "NOA"
  }
]
```

#### 3. Basado en la consulta del punto 1, mostrar sólo las regiones que tengan una 
cantidad de productos vendidos superior a 10000. 

```json
db.getCollection('facturas').aggregate(
  [
    { $unwind: '$item' },
    {
      $group: {
        _id: '$cliente.region',
        totalCantidad: { $sum: '$item.cantidad' }
      }
    },
    { $match: { totalCantidad: { $gt: 10000 } } },
    {
      $project: {
        _id: 0,
        region: '$_id',
        totalCantidad: 1
      }
    }
  ]
);
```

```json
Result sample: 
[
  {}
]
```

#### 4. Se requiere obtener un reporte que contenga la siguiente información, nro. cuit, apellido y nombre y región y cantidad de facturas, ordenado por apellido. 

```json
db.getCollection('facturas').aggregate(
  [
    {
      $group: {
        _id: {
          cuit: '$cliente.cuit',
          apellido: '$cliente.apellido',
          nombre: '$cliente.nombre',
          region: '$cliente.region'
        },
        cantidadFacturas: { $sum: 1 }
      }
    },
    {
      $project: {
        _id: 0,
        cuit: '$_id.cuit',
        apellido: '$_id.apellido',
        nombre: '$_id.nombre',
        region: '$_id.region',
        cantidadFacturas: 1
      }
    },
    { $sort: { apellido: 1 } }
  ]
);
```

```json
Result:
[
    {
        "cantidadFacturas": 14,
        "cuit": {
          "$numberLong": "2729887543"
        },
        "apellido": "Lavagno",
        "nombre": "Soledad",
        "region": "NOA"
    },
    {
        "cantidadFacturas": 15,
        "cuit": {
          "$numberLong": "2740488484"
        },
        "apellido": "Malinez",
        "nombre": "Marina",
        "region": "CENTRO"
    },
    {
        "cantidadFacturas": 42,
        "cuit": 2029889382,
        "apellido": "Manoni",
        "nombre": "Juan Manuel",
        "region": "NEA"
    },
    {
        "cantidadFacturas": 29,
        "cuit": 2038373771,
        "apellido": "Zavasi",
        "nombre": "Martin",
        "region": "CABA"
    }
]
```


#### 5. Basados en la consulta del punto 4 informar sólo los clientes con número de 
CUIT mayor a 27000000000. 

```json
db.getCollection('facturas').aggregate(
  [
    {
      $match: {
        'cliente.cuit': { $gt: 2700000000 }
      }
    },
    {
      $group: {
        _id: {
          cuit: '$cliente.cuit',
          apellido: '$cliente.apellido',
          nombre: '$cliente.nombre',
          region: '$cliente.region'
        },
        cantidadFacturas: { $sum: 1 }
      }
    },
    {
      $project: {
        _id: 0,
        cuit: '$_id.cuit',
        apellido: '$_id.apellido',
        nombre: '$_id.nombre',
        region: '$_id.region',
        cantidadFacturas: 1
      }
    },
    { $sort: { apellido: 1 } }
  ]
);

```

```json
Result:
[
    {
        "cantidadFacturas": 14,
        "cuit": {
          "$numberLong": "2729887543"
        },
        "apellido": "Lavagno",
        "nombre": "Soledad",
        "region": "NOA"
      },
      {
        "cantidadFacturas": 15,
        "cuit": {
          "$numberLong": "2740488484"
        },
        "apellido": "Malinez",
        "nombre": "Marina",
        "region": "CENTRO"
      }
]

```

#### 6. Basados en la consulta del punto 5 informar solamente la cantidad de clientes que cumplen con esta condición. 

```json
db.getCollection('facturas').aggregate(
  [
    {
      $match: {
        'cliente.cuit': { $gt: 2700000000 }
      }
    },
    {
      $group: {
        _id: {
          cuit: '$cliente.cuit',
          apellido: '$cliente.apellido',
          nombre: '$cliente.nombre',
          region: '$cliente.region'
        }
      }
    },
    { $count: 'cantidadClientes' }
  ],
  { maxTimeMS: 60000, allowDiskUse: true }
);
```
```json
Result:
[
    {
        "cantidadClientes": 2
    }
]
```
#### 7. Se requiere realizar una consulta que devuelva la siguiente información: producto y cantidad de facturas en las que lo compraron, ordenado por cantidad de facturas descendente. 

```json
db.getCollection('facturas').aggregate(
  [
    { $unwind: '$item' },
    {
      $group: {
        _id: '$item.producto',
        cantidadFacturas: { $sum: 1 }
      }
    },
    { $sort: { cantidadFacturas: -1 } },
    {
      $project: {
        _id: 0,
        producto: '$_id',
        cantidadFacturas: 1
      }
    }
  ]
);
```

```json

Result:
[
      {
        "cantidadFacturas": 43,
        "producto": "TALADRO 12mm"
      },
      {
        "cantidadFacturas": 29,
        "producto": "CORREA 10mm"
      },
      {
        "cantidadFacturas": 28,
        "producto": "TUERCA 5mm"
      },
      {
        "cantidadFacturas": 28,
        "producto": "SET HERRAMIENTAS"
      },
      {
        "cantidadFacturas": 28,
        "producto": "TUERCA 2mm"
      },
      {
        "cantidadFacturas": 15,
        "producto": " CORREA 12mm"
      }
]
```

#### 8. Obtener la cantidad total comprada así como también los ingresos totales para cada producto. 

```json
db.getCollection('facturas').aggregate(
  [
    { $unwind: '$item' },
    {
      $group: {
        _id: '$item.producto',
        cantidadTotal: { $sum: '$item.cantidad' },
        ingresosTotales: {
          $sum: {
            $multiply: [
              '$item.cantidad',
              '$item.precio'
            ]
          }
        }
      }
    },
    { $sort: { ingresosTotales: -1 } },
    {
      $project: {
        _id: 0,
        producto: '$_id',
        cantidadTotal: 1,
        ingresosTotales: 1
      }
    }
  ]
);
```
```json

Result:
[
    {
        "cantidadTotal": 350,
        "ingresosTotales": 31500,
        "producto": "TUERCA 5mm"
      },
      {
        "cantidadTotal": 198,
        "ingresosTotales": 26532,
        "producto": "CORREA 10mm"
      },
      {
        "cantidadTotal": 43,
        "ingresosTotales": 21070,
        "producto": "TALADRO 12mm"
      },
      {
        "cantidadTotal": 28,
        "ingresosTotales": 19600,
        "producto": "SET HERRAMIENTAS"
      },
      {
        "cantidadTotal": 112,
        "ingresosTotales": 6720,
        "producto": "TUERCA 2mm"
      },
      {
        "cantidadTotal": 165,
        "ingresosTotales": 2970,
        "producto": " CORREA 12mm"
      }
]
```

#### 9. Idem el punto anterior, ordenar por ingresos en forma ascendente, saltear el 1ro y mostrar 2do y 3ro. 

```json
db.getCollection('facturas').aggregate(
  [
    { $unwind: '$item' },
    {
      $group: {
        _id: '$item.producto',
        cantidadTotal: { $sum: '$item.cantidad' },
        ingresosTotales: {
          $sum: {
            $multiply: [
              '$item.cantidad',
              '$item.precio'
            ]
          }
        }
      }
    },
    { $sort: { ingresosTotales: 1 } },
    { $skip: 1 },
    { $limit: 2 },
    {
      $project: {
        _id: 0,
        producto: '$_id',
        cantidadTotal: 1,
        ingresosTotales: 1
      }
    }
  ]
);

```
```json

Result:
[
    {
        "cantidadTotal": 112,
        "ingresosTotales": 6720,
        "producto": "TUERCA 2mm"
      },
      {
        "cantidadTotal": 28,
        "ingresosTotales": 19600,
        "producto": "SET HERRAMIENTAS"
      }
]
```


#### 10. Obtener todos productos junto con un array de las personas que lo compraron. En este array deberá haber solo strings con el nombre completo de la persona. Los documentos entregados como resultado deberán tener la siguiente forma: 
```json
{producto: “<nombre>”, personas:[“…”, …]} 
```

```json
db.getCollection('facturas').aggregate(
  [
    { $unwind: '$item' },
    {
      $group: {
        _id: {
          producto: '$item.producto',
          nombreCompleto: {
            $concat: [
              '$cliente.nombre',
              ' ',
              '$cliente.apellido'
            ]
          }
        }
      }
    },
    {
      $group: {
        _id: '$_id.producto',
        personas: {
          $addToSet: '$_id.nombreCompleto'
        }
      }
    },
    {
      $project: {
        _id: 0,
        producto: '$_id',
        personas: 1
      }
    }
  ]
);
```
```json

Result:
[
    {
        "personas": [
          "Juan Manuel Manoni",
          "Marina Malinez"
        ],
        "producto": "TALADRO 12mm"
      },
      {
        "personas": [
          "Juan Manuel Manoni"
        ],
        "producto": "TUERCA 5mm"
      },
      {
        "personas": [
          "Marina Malinez"
        ],
        "producto": " CORREA 12mm"
      },
      {
        "personas": [
          "Martin Zavasi"
        ],
        "producto": "CORREA 10mm"
      },
      {
        "personas": [
          "Martin Zavasi",
          "Juan Manuel Manoni"
        ],
        "producto": "TUERCA 2mm"
      },
      {
        "personas": [
          "Juan Manuel Manoni",
          "Soledad Lavagno"
        ],
        "producto": "SET HERRAMIENTAS"
      }
]
```

#### 11. Obtener los productos ordenados en forma descendente por la cantidad de diferentes personas que los compraron. 

```json
db.getCollection('facturas').aggregate(
  [
    { $unwind: '$item' },
    {
      $group: {
        _id: {
          producto: '$item.producto',
          nombreCompleto: {
            $concat: [
              '$cliente.nombre',
              ' ',
              '$cliente.apellido'
            ]
          }
        }
      }
    },
    {
      $group: {
        _id: '$_id.producto',
        personas: {
          $addToSet: '$_id.nombreCompleto'
        }
      }
    },
    {
      $project: {
        _id: 0,
        producto: '$_id',
        cantidadPersonas: { $size: '$personas' },
        personas: 1
      }
    },
    { $sort: { cantidadPersonas: -1 } }
  ]
);
```

```json

Result:
[
    {
        "personas": [
          "Martin Zavasi",
          "Juan Manuel Manoni"
        ],
        "producto": "TUERCA 2mm",
        "cantidadPersonas": 2
      },
      {
        "personas": [
          "Juan Manuel Manoni",
          "Soledad Lavagno"
        ],
        "producto": "SET HERRAMIENTAS",
        "cantidadPersonas": 2
      },
      {
        "personas": [
          "Marina Malinez",
          "Juan Manuel Manoni"
        ],
        "producto": "TALADRO 12mm",
        "cantidadPersonas": 2
      },
      {
        "personas": [
          "Martin Zavasi"
        ],
        "producto": "CORREA 10mm",
        "cantidadPersonas": 1
      },
      {
        "personas": [
          "Juan Manuel Manoni"
        ],
        "producto": "TUERCA 5mm",
        "cantidadPersonas": 1
      },
      {
        "personas": [
          "Marina Malinez"
        ],
        "producto": " CORREA 12mm",
        "cantidadPersonas": 1
      }
]
```

#### 12. Obtener el total gastado por persona y mostrar solo los que gastaron más de 3100000. Los documentos devueltos deben tener el nombre completo del cliente y el total gastado: 
```json
{cliente:”<nombreCompleto>”,total:<num>} 
```

```json
db.getCollection('facturas').aggregate(
  [
    { $unwind: '$item' },
    {
      $group: {
        _id: {
          nombreCompleto: {
            $concat: [
              '$cliente.nombre',
              ' ',
              '$cliente.apellido'
            ]
          }
        },
        totalGastado: {
          $sum: {
            $multiply: [
              '$item.precio',
              '$item.cantidad'
            ]
          }
        }
      }
    },
    {
      $match: { totalGastado: { $gt: 3100000 } }
    },
    {
      $project: {
        _id: 0,
        cliente: '$_id.nombreCompleto',
        total: '$totalGastado'
      }
    }
  ]
);
```

```json
Result:
[
  {}
]
```

#### 13. Obtener el promedio de gasto por factura por cada región. 

```json
db.getCollection('facturas').aggregate(
  [
    { $unwind: '$item' },
    {
      $group: {
        _id: '$_id',
        region: { $first: '$cliente.region' },
        totalFactura: {
          $sum: {
            $multiply: [
              '$item.precio',
              '$item.cantidad'
            ]
          }
        }
      }
    },
    {
      $group: {
        _id: '$region',
        promedioGasto: { $avg: '$totalFactura' }
      }
    },
    {
      $project: {
        _id: 0,
        region: '$_id',
        promedioGasto: {
          $round: ['$promedioGasto', 2]
        }
      }
    }
  ]
);
```

```json

Result:
[
    {
        "region": "CABA",
        "promedioGasto": 1088.69
      },
      {
        "region": "CENTRO",
        "promedioGasto": 688
      },
      {
        "region": "NEA",
        "promedioGasto": 1350
      },
      {
        "region": "NOA",
        "promedioGasto": 700
      }
]
```

#### 14. Obtener la factura en la que se haya gastado más. En caso de que sean varias 
obtener la que tenga el número de factura menor.

```json
db.getCollection('facturas').aggregate(
  [
    { $unwind: '$item' },
    {
      $group: {
        _id: '$nroFactura',
        cliente: { $first: '$cliente' },
        fechaEmision: { $first: '$fechaEmision' },
        total: {
          $sum: {
            $multiply: [
              '$item.precio',
              '$item.cantidad'
            ]
          }
        }
      }
    },
    { $sort: { total: -1, _id: 1 } },
    { $limit: 1 }
  ]
);
```

```json
Result:
[
    {
        "_id": 1002,
        "cliente": {
          "apellido": "Zavasi",
          "cuit": 2038373771,
          "nombre": "Martin",
          "region": "CABA"
        },
        "fechaEmision": {
          "$date": "2014-02-20T00:00:00.000Z"
        },
        "total": 1968
      }
]
```

#### 15. Obtener a los clientes indicando cuánto fue lo que más gastó en una única factura. 
```json
db.facturas.aggregate([
    { $unwind: "$item" },
    {
      $group: {
        _id: "$nroFactura",
        cliente: { $first: "$cliente" },
        totalFactura: { $sum: { $multiply: ["$item.precio", "$item.cantidad"] } }
      }
    },
    {
      $group: {
        _id: {
          cuit: "$cliente.cuit",
          nombre: "$cliente.nombre",
          apellido: "$cliente.apellido"
        },
        maxGasto: { $max: "$totalFactura" }
      }
    },
    {
      $project: {
        _id: 0,
        cliente: {
          $concat: ["$_id.nombre", " ", "$_id.apellido"]
        },
        maxGasto: 1
      }
    }
  ])
```

```json
Result:
[
    {
        "maxGasto": 1968,
        "cliente": "Martin Zavasi"
      },
      {
        "maxGasto": 688,
        "cliente": "Marina Malinez"
      },
      {
        "maxGasto": 1960,
        "cliente": "Juan Manuel Manoni"
      },
      {
        "maxGasto": 700,
        "cliente": "Soledad Lavagno"
      }
]
```

#### 16. Utilizando MapReduce, indicar la cantidad total comprada de cada ítem. Comparar el resultado con el ejercicio 8. 

```js
var mapFunction = function() {
    this.item.forEach(function(producto) {
      emit(producto.producto, {
        cantidad: producto.cantidad,
        ingresos: producto.cantidad * producto.precio
      });
    });
};

var reduceFunction = function(key, values) {
    var result = { cantidad: 0, ingresos: 0 };
    values.forEach(function(value) {
      result.cantidad += value.cantidad;
      result.ingresos += value.ingresos;
    });
    return result;
};

// Ejecutar mapReduce
var result = db.facturas.mapReduce(
  mapFunction,
  reduceFunction,
  { out: { inline: 1 } }
);

// Acceder a los resultados y recorrerlos
result.results.forEach(function(doc) {
  // Imprimir el resultado con formato legible
  print("Producto: " + doc._id + ", Cantidad Total: " + doc.value.cantidad + ", Ingresos Totales: " + doc.value.ingresos);
});

```



**Resultado del MapReduce:**
```json
[
    { "producto": "CORREA 10mm", "cantidadTotal": 198, "ingresosTotales": 26532 },
    { "producto": "TALADRO 12mm", "cantidadTotal": 43, "ingresosTotales": 21070 },
    { "producto": "SET HERRAMIENTAS", "cantidadTotal": 28, "ingresosTotales": 19600 },
    { "producto": " CORREA 12mm", "cantidadTotal": 165, "ingresosTotales": 2970 },
    { "producto": "TUERCA 2mm", "cantidadTotal": 112, "ingresosTotales": 6720 },
    { "producto": "TUERCA 5mm", "cantidadTotal": 350, "ingresosTotales": 31500 }
]
```
**Resultado del Ejercicio 8:**
```json
[
    { "cantidadTotal": 350, "ingresosTotales": 31500, "producto": "TUERCA 5mm" },
    { "cantidadTotal": 198, "ingresosTotales": 26532, "producto": "CORREA 10mm"},
    { "cantidadTotal": 43, "ingresosTotales": 21070, "producto": "TALADRO 12mm" },
    { "cantidadTotal": 28, "ingresosTotales": 19600, "producto": "SET HERRAMIENTAS" },
    { "cantidadTotal": 112, "ingresosTotales": 6720, "producto": "TUERCA 2mm" },
    { "cantidadTotal": 165, "ingresosTotales": 2970, "producto": " CORREA 12mm" }
]

```


#### 17. Obtener la información de los clientes que hayan gastado 100000 en una orden junto 
con el número de orden. 

```json
db.getCollection('facturas').aggregate(
  [
    { $unwind: '$item' },
    {
      $group: {
        _id: '$nroFactura',
        cliente: { $first: '$cliente' },
        totalFactura: {
          $sum: {
            $multiply: [
              '$item.cantidad',
              '$item.precio'
            ]
          }
        }
      }
    },
    {
      $match: { totalFactura: { $gte: 100000 } }
    },
    {
      $project: {
        _id: 0,
        nroFactura: '$_id',
        cliente: {
          nombre: '$cliente.nombre',
          apellido: '$cliente.apellido',
          cuit: '$cliente.cuit',
          region: '$cliente.region'
        },
        totalFactura: 1
      }
    }
  ]
);
```

```json
Result:
[
  {}
]
```


#### 18. En base a la localidad de los clientes, obtener el total facturado por localidad. 

```json
db.facturas.aggregate([
    { $unwind: "$item" },
    {
      $group: {
        _id: "$cliente.region",
        totalFacturado: {
          $sum: { $multiply: ["$item.cantidad", "$item.precio"] }
        }
      }
    },
    {
      $project: {
        _id: 0,
        localidad: "$_id",
        totalFacturado: 1
      }
    },
    { $sort: { totalFacturado: -1 } }
  ])
```

```json
Result:
[
    {
        "totalFacturado": 56700,
        "localidad": "NEA"
    },
    {
        "totalFacturado": 31572,
        "localidad": "CABA"
    },
    {
        "totalFacturado": 10320,
        "localidad": "CENTRO"
    },
    {
        "totalFacturado": 9800,
        "localidad": "NOA"
    }
]
```