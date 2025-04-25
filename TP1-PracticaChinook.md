## Trabajo Practico 1 - Consultas SQL con Postgres

### Selecciona todos los registros de la tabla Albums.

```sql
SELECT * FROM public.album

#################
RESULT:
################# 
"album_id"	"title"	"artist_id"
1	"For Those About To Rock We Salute You"	1
2	"Balls to the Wall"	2
3	"Restless and Wild"	2
4	"Let There Be Rock"	1
5	"Big Ones"	3
6	"Jagged Little Pill"	4
7	"Facelift"	5
8	"Warner 25 Anos"	6
9	"Plays Metallica By Four Cellos"	7
10	"Audioslave"	8
11	"Out Of Exile"	8
12	"BackBeat Soundtrack"	9
13	"The Best Of Billy Cobham"	10
14	"Alcohol Fueled Brewtality Live! [Disc 1]"	11
15	"Alcohol Fueled Brewtality Live! [Disc 2]"	11
16	"Black Sabbath"	12
17	"Black Sabbath Vol. 4 (Remaster)"	12
18	"Body Count"	13
19	"Chemical Wedding"	14
20	"The Best Of Buddy Guy - The Millenium Collection"	15
21	"Prenda Minha"	16
22	"Sozinho Remix Ao Vivo"	16
23	"Minha Historia"	17
24	"Afrociberdelia"	18
25	"Da Lama Ao Caos"	18
26	"Acústico MTV [Live]"	19
27	"Cidade Negra - Hits"	19
28	"Na Pista"	20
29	"Axé Bahia 2001"	21
30	"BBC Sessions [Disc 1] [Live]"	22
31	"Bongo Fury"	23
32	"Carnaval 2001"	21
33	"Chill: Brazil (Disc 1)"	24
34	"Chill: Brazil (Disc 2)"	6
35	"Garage Inc. (Disc 1)"	50
36	"Greatest Hits II"	51
37	"Greatest Kiss"	52
38	"Heart of the Night"	53
39	"International Superhits"	54
40	"Into The Light"	55
41	"Meus Momentos"	56
42	"Minha História"	57
43	"MK III The Final Concerts [Disc 1]"	58
44	"Physical Graffiti [Disc 1]"	22
45	"Sambas De Enredo 2001"	21
46	"Supernatural"	59
47	"The Best of Ed Motta"	37
48	"The Essential Miles Davis [Disc 1]"	68
49	"The Essential Miles Davis [Disc 2]"	68
50	"The Final Concerts (Disc 2)"	58
51	"Up An' Atom"	69
52	"Vinícius De Moraes - Sem Limite"	70
53	"Vozes do MPB"	21
54	"Chronicle, Vol. 1"	76
55	"Chronicle, Vol. 2"	76
56	"Cássia Eller - Coleção Sem Limite [Disc 2]"	77
57	"Cássia Eller - Sem Limite [Disc 1]"	77
58	"Come Taste The Band"	58
59	"Deep Purple In Rock"	58
60	"Fireball"	58
61	"Knocking at Your Back Door: The Best Of Deep Purple in the 80's"	58
62	"Machine Head"	58
63	"Purpendicular"	58
64	"Slaves And Masters"	58
65	"Stormbringer"	58
66	"The Battle Rages On"	58
67	"Vault: Def Leppard's Greatest Hits"	78
68	"Outbreak"	79
69	"Djavan Ao Vivo - Vol. 02"	80
70	"Djavan Ao Vivo - Vol. 1"	80
71	"Elis Regina-Minha História"	41
72	"The Cream Of Clapton"	81
73	"Unplugged"	81
74	"Album Of The Year"	82
75	"Angel Dust"	82
76	"King For A Day Fool For A Lifetime"	82
77	"The Real Thing"	82
78	"Deixa Entrar"	83
79	"In Your Honor [Disc 1]"	84
80	"In Your Honor [Disc 2]"	84
81	"One By One"	84
82	"The Colour And The Shape"	84
83	"My Way: The Best Of Frank Sinatra [Disc 1]"	85
84	"Roda De Funk"	86
85	"As Canções de Eu Tu Eles"	27
86	"Quanta Gente Veio Ver (Live)"	27
87	"Quanta Gente Veio ver--Bônus De Carnaval"	27
88	"Faceless"	87
89	"American Idiot"	54
90	"Appetite for Destruction"	88
91	"Use Your Illusion I"	88
92	"Use Your Illusion II"	88
93	"Blue Moods"	89
94	"A Matter of Life and Death"	90
95	"A Real Dead One"	90
96	"A Real Live One"	90
97	"Brave New World"	90
98	"Dance Of Death"	90
99	"Fear Of The Dark"	90
100	"Iron Maiden"	90
101	"Killers"	90
102	"Live After Death"	90
103	"Live At Donington 1992 (Disc 1)"	90
104	"Live At Donington 1992 (Disc 2)"	90
105	"No Prayer For The Dying"	90
106	"Piece Of Mind"	90
107	"Powerslave"	90
108	"Rock In Rio [CD1]"	90
109	"Rock In Rio [CD2]"	90
110	"Seventh Son of a Seventh Son"	90
111	"Somewhere in Time"	90
112	"The Number of The Beast"	90
113	"The X Factor"	90
114	"Virtual XI"	90
115	"Sex Machine"	91
116	"Emergency On Planet Earth"	92
117	"Synkronized"	92
118	"The Return Of The Space Cowboy"	92
119	"Get Born"	93
120	"Are You Experienced?"	94
121	"Surfing with the Alien (Remastered)"	95
122	"Jorge Ben Jor 25 Anos"	46
123	"Jota Quest-1995"	96
124	"Cafezinho"	97
125	"Living After Midnight"	98
126	"Unplugged [Live]"	52
127	"BBC Sessions [Disc 2] [Live]"	22
128	"Coda"	22
129	"Houses Of The Holy"	22
130	"In Through The Out Door"	22
131	"IV"	22
132	"Led Zeppelin I"	22
133	"Led Zeppelin II"	22
134	"Led Zeppelin III"	22
135	"Physical Graffiti [Disc 2]"	22
136	"Presence"	22
137	"The Song Remains The Same (Disc 1)"	22
138	"The Song Remains The Same (Disc 2)"	22
139	"A TempestadeTempestade Ou O Livro Dos Dias"	99
140	"Mais Do Mesmo"	99
141	"Greatest Hits"	100
142	"Lulu Santos - RCA 100 Anos De Música - Álbum 01"	101
143	"Lulu Santos - RCA 100 Anos De Música - Álbum 02"	101
144	"Misplaced Childhood"	102
145	"Barulhinho Bom"	103
146	"Seek And Shall Find: More Of The Best (1963-1981)"	104
147	"The Best Of Men At Work"	105
148	"Black Album"	50
149	"Garage Inc. (Disc 2)"	50
150	"Kill 'Em All"	50
151	"Load"	50
152	"Master Of Puppets"	50
153	"ReLoad"	50
154	"Ride The Lightning"	50
155	"St. Anger"	50
156	"...And Justice For All"	50
157	"Miles Ahead"	68
158	"Milton Nascimento Ao Vivo"	42
159	"Minas"	42
160	"Ace Of Spades"	106
161	"Demorou..."	108
162	"Motley Crue Greatest Hits"	109
163	"From The Muddy Banks Of The Wishkah [Live]"	110
164	"Nevermind"	110
165	"Compositores"	111
166	"Olodum"	112
167	"Acústico MTV"	113
168	"Arquivo II"	113
169	"Arquivo Os Paralamas Do Sucesso"	113
170	"Bark at the Moon (Remastered)"	114
171	"Blizzard of Ozz"	114
172	"Diary of a Madman (Remastered)"	114
173	"No More Tears (Remastered)"	114
174	"Tribute"	114
175	"Walking Into Clarksdale"	115
176	"Original Soundtracks 1"	116
177	"The Beast Live"	117
178	"Live On Two Legs [Live]"	118
179	"Pearl Jam"	118
180	"Riot Act"	118
181	"Ten"	118
182	"Vs."	118
183	"Dark Side Of The Moon"	120
184	"Os Cães Ladram Mas A Caravana Não Pára"	121
185	"Greatest Hits I"	51
186	"News Of The World"	51
187	"Out Of Time"	122
188	"Green"	124
189	"New Adventures In Hi-Fi"	124
190	"The Best Of R.E.M.: The IRS Years"	124
191	"Cesta Básica"	125
192	"Raul Seixas"	126
193	"Blood Sugar Sex Magik"	127
194	"By The Way"	127
195	"Californication"	127
196	"Retrospective I (1974-1980)"	128
197	"Santana - As Years Go By"	59
198	"Santana Live"	59
199	"Maquinarama"	130
200	"O Samba Poconé"	130
201	"Judas 0: B-Sides and Rarities"	131
202	"Rotten Apples: Greatest Hits"	131
203	"A-Sides"	132
204	"Morning Dance"	53
205	"In Step"	133
206	"Core"	134
207	"Mezmerize"	135
208	"[1997] Black Light Syndrome"	136
209	"Live [Disc 1]"	137
210	"Live [Disc 2]"	137
211	"The Singles"	138
212	"Beyond Good And Evil"	139
213	"Pure Cult: The Best Of The Cult (For Rockers, Ravers, Lovers & Sinners) [UK]"	139
214	"The Doors"	140
215	"The Police Greatest Hits"	141
216	"Hot Rocks, 1964-1971 (Disc 1)"	142
217	"No Security"	142
218	"Voodoo Lounge"	142
219	"Tangents"	143
220	"Transmission"	143
221	"My Generation - The Very Best Of The Who"	144
222	"Serie Sem Limite (Disc 1)"	145
223	"Serie Sem Limite (Disc 2)"	145
224	"Acústico"	146
225	"Volume Dois"	146
226	"Battlestar Galactica: The Story So Far"	147
227	"Battlestar Galactica, Season 3"	147
228	"Heroes, Season 1"	148
229	"Lost, Season 3"	149
230	"Lost, Season 1"	149
231	"Lost, Season 2"	149
232	"Achtung Baby"	150
233	"All That You Can't Leave Behind"	150
234	"B-Sides 1980-1990"	150
235	"How To Dismantle An Atomic Bomb"	150
236	"Pop"	150
237	"Rattle And Hum"	150
238	"The Best Of 1980-1990"	150
239	"War"	150
240	"Zooropa"	150
241	"UB40 The Best Of - Volume Two [UK]"	151
242	"Diver Down"	152
243	"The Best Of Van Halen, Vol. I"	152
244	"Van Halen"	152
245	"Van Halen III"	152
246	"Contraband"	153
247	"Vinicius De Moraes"	72
248	"Ao Vivo [IMPORT]"	155
249	"The Office, Season 1"	156
250	"The Office, Season 2"	156
251	"The Office, Season 3"	156
252	"Un-Led-Ed"	157
253	"Battlestar Galactica (Classic), Season 1"	158
254	"Aquaman"	159
255	"Instant Karma: The Amnesty International Campaign to Save Darfur"	150
256	"Speak of the Devil"	114
257	"20th Century Masters - The Millennium Collection: The Best of Scorpions"	179
258	"House of Pain"	180
259	"Radio Brasil (O Som da Jovem Vanguarda) - Seleccao de Henrique Amaro"	36
260	"Cake: B-Sides and Rarities"	196
261	"LOST, Season 4"	149
262	"Quiet Songs"	197
263	"Muso Ko"	198
264	"Realize"	199
265	"Every Kind of Light"	200
266	"Duos II"	201
267	"Worlds"	202
268	"The Best of Beethoven"	203
269	"Temple of the Dog"	204
270	"Carry On"	205
271	"Revelations"	8
272	"Adorate Deum: Gregorian Chant from the Proper of the Mass"	206
273	"Allegri: Miserere"	207
274	"Pachelbel: Canon & Gigue"	208
275	"Vivaldi: The Four Seasons"	209
276	"Bach: Violin Concertos"	210
277	"Bach: Goldberg Variations"	211
278	"Bach: The Cello Suites"	212
279	"Handel: The Messiah (Highlights)"	213
280	"The World of Classical Favourites"	214
281	"Sir Neville Marriner: A Celebration"	215
282	"Mozart: Wind Concertos"	216
283	"Haydn: Symphonies 99 - 104"	217
284	"Beethoven: Symhonies Nos. 5 & 6"	218
285	"A Soprano Inspired"	219
286	"Great Opera Choruses"	220
287	"Wagner: Favourite Overtures"	221
288	"Fauré: Requiem, Ravel: Pavane & Others"	222
289	"Tchaikovsky: The Nutcracker"	223
290	"The Last Night of the Proms"	224
291	"Puccini: Madama Butterfly - Highlights"	225
292	"Holst: The Planets, Op. 32 & Vaughan Williams: Fantasies"	226
293	"Pavarotti's Opera Made Easy"	227
294	"Great Performances - Barber's Adagio and Other Romantic Favorites for Strings"	228
295	"Carmina Burana"	229
296	"A Copland Celebration, Vol. I"	230
297	"Bach: Toccata & Fugue in D Minor"	231
298	"Prokofiev: Symphony No.1"	232
299	"Scheherazade"	233
300	"Bach: The Brandenburg Concertos"	234
301	"Chopin: Piano Concertos Nos. 1 & 2"	235
302	"Mascagni: Cavalleria Rusticana"	236
303	"Sibelius: Finlandia"	237
304	"Beethoven Piano Sonatas: Moonlight & Pastorale"	238
305	"Great Recordings of the Century - Mahler: Das Lied von der Erde"	240
306	"Elgar: Cello Concerto & Vaughan Williams: Fantasias"	241
307	"Adams, John: The Chairman Dances"	242
308	"Tchaikovsky: 1812 Festival Overture, Op.49, Capriccio Italien & Beethoven: Wellington's Victory"	243
309	"Palestrina: Missa Papae Marcelli & Allegri: Miserere"	244
310	"Prokofiev: Romeo & Juliet"	245
311	"Strauss: Waltzes"	226
312	"Berlioz: Symphonie Fantastique"	245
313	"Bizet: Carmen Highlights"	246
314	"English Renaissance"	247
315	"Handel: Music for the Royal Fireworks (Original Version 1749)"	208
316	"Grieg: Peer Gynt Suites & Sibelius: Pelléas et Mélisande"	248
317	"Mozart Gala: Famous Arias"	249
318	"SCRIABIN: Vers la flamme"	250
319	"Armada: Music from the Courts of England and Spain"	251
320	"Mozart: Symphonies Nos. 40 & 41"	248
321	"Back to Black"	252
322	"Frank"	252
323	"Carried to Dust (Bonus Track Version)"	253
324	"Beethoven: Symphony No. 6 'Pastoral' Etc."	254
325	"Bartok: Violin & Viola Concertos"	255
326	"Mendelssohn: A Midsummer Night's Dream"	256
327	"Bach: Orchestral Suites Nos. 1 - 4"	257
328	"Charpentier: Divertissements, Airs & Concerts"	258
329	"South American Getaway"	259
330	"Górecki: Symphony No. 3"	260
331	"Purcell: The Fairy Queen"	261
332	"The Ultimate Relexation Album"	262
333	"Purcell: Music for the Queen Mary"	263
334	"Weill: The Seven Deadly Sins"	264
335	"J.S. Bach: Chaconne, Suite in E Minor, Partita in E Major & Prelude, Fugue and Allegro"	265
336	"Prokofiev: Symphony No.5 & Stravinksy: Le Sacre Du Printemps"	248
337	"Szymanowski: Piano Works, Vol. 1"	266
338	"Nielsen: The Six Symphonies"	267
339	"Great Recordings of the Century: Paganini's 24 Caprices"	268
340	"Liszt - 12 Études D'Execution Transcendante"	269
341	"Great Recordings of the Century - Shubert: Schwanengesang, 4 Lieder"	270
342	"Locatelli: Concertos for Violin, Strings and Continuo, Vol. 3"	271
343	"Respighi:Pines of Rome"	226
344	"Schubert: The Late String Quartets & String Quintet (3 CD's)"	272
345	"Monteverdi: L'Orfeo"	273
346	"Mozart: Chamber Music"	274
347	"Koyaanisqatsi (Soundtrack from the Motion Picture)"	275


### Selecciona todos los géneros únicos de la tabla Genres.

SELECT DISTINCT * FROM public.genre 

#################
RESULT:
#################

"genre_id"	"name"
21	"Drama"
16	"World"
12	"Easy Listening"
23	"Alternative"
24	"Classical"
8	"Reggae"
13	"Heavy Metal"
11	"Bossa Nova"
25	"Opera"
18	"Science Fiction"
5	"Rock And Roll"
9	"Pop"
19	"TV Shows"
1	"Rock"
3	"Metal"
20	"Sci Fi & Fantasy"
2	"Jazz"
14	"R&B/Soul"
17	"Hip Hop/Rap"
10	"Soundtrack"
22	"Comedy"
4	"Alternative & Punk"
15	"Electronica/Dance"
7	"Latin"
6	"Blues"
```

### Cuenta el número de pistas por género.

```sql
SELECT
    g.name AS genre,
    COUNT(t.track_id) AS track_count
FROM
    genre g
LEFT JOIN
    track t ON g.genre_id = t.genre_id
GROUP BY
    g.name

#################
RESULT:
################# 
"genre"	"track_count"
"Heavy Metal"	28
"TV Shows"	93
"Latin"	579
"Electronica/Dance"	30
"R&B/Soul"	61
"Opera"	1
"Comedy"	17
"Classical"	74
"Pop"	48
"Easy Listening"	24
"Alternative"	40
"Drama"	64
"Sci Fi & Fantasy"	26
"Rock"	1297
"World"	28
"Reggae"	58
"Blues"	81
"Rock And Roll"	12
"Alternative & Punk"	332
"Metal"	374
"Soundtrack"	43
"Bossa Nova"	15
"Science Fiction"	13
"Hip Hop/Rap"	35
"Jazz"	130
```

### Encuentra la longitud total (en milisegundos) de todas las pistas para cada álbum.

```sql
SELECT
    a.title AS album_title,
    SUM(t.milliseconds) AS total_duration_ms
FROM
    album a
JOIN
    track t ON a.album_id = t.album_id
JOIN
    artist ar ON a.artist_id = ar.artist_id
GROUP BY
    a.album_id, a.title

#################
RESULT:
################# 
"album_title"	"total_duration_ms"
"Os Cães Ladram Mas A Caravana Não Pára"	2967110
"Emergency On Planet Earth"	3327211
"Quanta Gente Veio ver--Bônus De Carnaval"	915904
"Allegri: Miserere"	501503
"Up An' Atom"	4637011
"Adorate Deum: Gregorian Chant from the Proper of the Mass"	245317
"Djavan Ao Vivo - Vol. 1"	3658206
"The Best Of R.E.M.: The IRS Years"	3570407
"English Renaissance"	202962
"Bach: The Cello Suites"	143288
"Scheherazade"	545203
"Original Soundtracks 1"	3489692
"Arquivo Os Paralamas Do Sucesso"	3615574
"Monteverdi: L'Orfeo"	66639
"Palestrina: Missa Papae Marcelli & Allegri: Miserere"	240666
"Use Your Illusion II"	4557211
"Riot Act"	3256468
"Holst: The Planets, Op. 32 & Vaughan Williams: Fantasies"	522099
"Pop"	3612572
"Revelations"	3503638
"Muso Ko"	586442
"Sozinho Remix Ao Vivo"	959711
"...And Justice For All"	3928993
"Santana - As Years Go By"	4303879
"Physical Graffiti [Disc 2]"	2619555
"Battlestar Galactica, Season 3"	52787041
"Mozart: Wind Concertos"	394482
"No More Tears (Remastered)"	695944
"Garage Inc. (Disc 2)"	4251893
"Strauss: Waltzes"	526696
"Temple of the Dog"	3316905
"Unplugged"	8113276
"LOST, Season 4"	39468433
"Live At Donington 1992 (Disc 1)"	3105614
"The World of Classical Favourites"	465201
"Minha História"	3351947
"New Adventures In Hi-Fi"	3933120
"War"	2529903
"Demorou..."	2645702
"Surfing with the Alien (Remastered)"	2259724
"Synkronized"	3180664
"Faceless"	2846138
"Green"	2462010
"20th Century Masters - The Millennium Collection: The Best of Scorpions"	3448442
"Living After Midnight"	3973111
"The X Factor"	4267801
"Into The Light"	3618267
"Zooropa"	3023251
"Charpentier: Divertissements, Airs & Concerts"	110266
"MK III The Final Concerts [Disc 1]"	3484627
"Retrospective I (1974-1980)"	4548694
"Are You Experienced?"	3618056
"Puccini: Madama Butterfly - Highlights"	277639
"Alcohol Fueled Brewtality Live! [Disc 2]"	1447755
"Battlestar Galactica: The Story So Far"	2622250
"Live [Disc 2]"	2966383
"The Essential Miles Davis [Disc 1]"	4597570
"Out Of Time"	2650117
"Prokofiev: Symphony No.1"	254001
"Cássia Eller - Sem Limite [Disc 1]"	3483867
"One By One"	3303622
"Knocking at Your Back Door: The Best Of Deep Purple in the 80's"	3876071
"Chemical Wedding"	3694022
"Van Halen"	2133413
"Ace Of Spades"	2735483
"Diver Down"	1890424
"Purcell: The Fairy Queen"	364296
"The Office, Season 3"	38317095
"Morning Dance"	2476665
"Duos II"	172710
"Live At Donington 1992 (Disc 2)"	3621377
"Big Ones"	4411709
"Blizzard of Ozz"	608940
"Handel: Music for the Royal Fireworks (Original Version 1749)"	120000
"Adams, John: The Chairman Dances"	254930
"Use Your Illusion I"	4567332
"Koyaanisqatsi (Soundtrack from the Motion Picture)"	206005
"Haydn: Symphonies 99 - 104"	306687
"Great Recordings of the Century - Mahler: Das Lied von der Erde"	223583
"Pearl Jam"	2983857
"Chronicle, Vol. 1"	4086691
"Axé Bahia 2001"	2822944
"Let There Be Rock"	2453259
"Bach: Toccata & Fugue in D Minor"	153901
"Ten"	3205871
"Back to Black"	2544050
"A Real Live One"	3537994
"Sibelius: Finlandia"	406000
"Judas 0: B-Sides and Rarities"	4211532
"Audioslave"	3927713
"No Prayer For The Dying"	2652573
"Garage Inc. (Disc 1)"	3946339
"Powerslave"	3036312
"Jagged Little Pill"	3450925
"All That You Can't Leave Behind"	2964604
"Transmission"	2973541
"Quanta Gente Veio Ver (Live)"	3917106
"Blue Moods"	4421323
"American Idiot"	3437890
"Tangents"	4033036
"Un-Led-Ed"	310774
"UB40 The Best Of - Volume Two [UK]"	3523466
"Walking Into Clarksdale"	3649040
"Respighi:Pines of Rome"	286741
"Bongo Fury"	2465929
"A Soprano Inspired"	338243
"Bach: Orchestral Suites Nos. 1 - 4"	225933
"The Final Concerts (Disc 2)"	3728376
"Battlestar Galactica (Classic), Season 1"	70213784
"Alcohol Fueled Brewtality Live! [Disc 1]"	4059919
"Lost, Season 2"	63289631
"The Battle Rages On"	3018129
"Liszt - 12 Études D'Execution Transcendante"	51780
"Rock In Rio [CD2]"	3584753
"St. Anger"	4507057
"The Best Of Billy Cobham"	2680524
"Led Zeppelin II"	2498869
"Californication"	3385461
"Balls to the Wall"	342562
"Maquinarama"	3193621
"Contraband"	3417071
"Angel Dust"	3709719
"Coda"	1981123
"Great Recordings of the Century: Paganini's 24 Caprices"	265541
"The Best Of Van Halen, Vol. I"	4349980
"Olodum"	3019828
"Schubert: The Late String Quartets & String Quintet (3 CD's)"	139200
"Lulu Santos - RCA 100 Anos De Música - Álbum 01"	3153886
"J.S. Bach: Chaconne, Suite in E Minor, Partita in E Major & Prelude, Fugue and Allegro"	285673
"Master Of Puppets"	3286175
"Lost, Season 1"	64854936
"Chopin: Piano Concertos Nos. 1 & 2"	560342
"Facelift"	3249365
"Serie Sem Limite (Disc 1)"	2620336
"Heart of the Night"	3497581
"Blood Sugar Sex Magik"	4437073
"Aquaman"	2484567
"Nevermind"	2557066
"Deixa Entrar"	2842456
"No Security"	4072169
"Minas"	3102844
"The Office, Season 2"	28636206
"News Of The World"	2361438
"The Best of Ed Motta"	3409704
"The Beast Live"	2547615
"The Best Of Buddy Guy - The Millenium Collection"	2636849
"Armada: Music from the Courts of England and Spain"	253281
"Vs."	2777674
"For Those About To Rock We Salute You"	2400415
"King For A Day Fool For A Lifetime"	3589791
"Piece Of Mind"	2752884
"Body Count"	3192389
"Seventh Son of a Seventh Son"	2641785
"Live On Two Legs [Live]"	4278954
"Barulhinho Bom"	3433813
"Houses Of The Holy"	2454435
"Cidade Negra - Hits"	3435043
"Lulu Santos - RCA 100 Anos De Música - Álbum 02"	3314460
"A-Sides"	4752029
"Come Taste The Band"	2236992
"Heroes, Season 1"	59780268
"Warner 25 Anos"	2906926
"Mozart: Chamber Music"	221331
"Great Performances - Barber's Adagio and Other Romantic Favorites for Strings"	596519
"Elis Regina-Minha História"	3095920
"Worlds"	266936
"Lost, Season 3"	70665582
"Outbreak"	3440820
"Beethoven Piano Sonatas: Moonlight & Pastorale"	391000
"Seek And Shall Find: More Of The Best (1963-1981)"	3488122
"In Your Honor [Disc 2]"	2596358
"Vinícius De Moraes - Sem Limite"	3293850
"House of Pain"	3269060
"Motley Crue Greatest Hits"	4435165
"Great Recordings of the Century - Shubert: Schwanengesang, 4 Lieder"	261849
"Led Zeppelin I"	2690399
"Frank"	3035807
"Roda De Funk"	4165844
"Bark at the Moon (Remastered)"	257252
"Raul Seixas"	2833311
"Górecki: Symphony No. 3"	567494
"Bach: Violin Concertos"	193722
"Rattle And Hum"	4348126
"Killers"	2323691
"Djavan Ao Vivo - Vol. 02"	3626756
"Quiet Songs"	553888
"Carried to Dust (Bonus Track Version)"	215386
"Szymanowski: Piano Works, Vol. 1"	333669
"Mozart: Symphonies Nos. 40 & 41"	362933
"Sex Machine"	4211242
"Virtual XI"	3194615
"Fireball"	2359767
"Brave New World"	4021860
"The Best Of 1980-1990"	3935916
"The Number of The Beast"	2413815
"Rock In Rio [CD1]"	3386588
"Deep Purple In Rock"	2535756
"Tchaikovsky: The Nutcracker"	304226
"The Best of Beethoven"	356426
"Stormbringer"	2197077
"BBC Sessions [Disc 2] [Live]"	4699108
"Cafezinho"	3065723
"Dance Of Death"	4083559
"South American Getaway"	289388
"O Samba Poconé"	2694369
"Physical Graffiti [Disc 1]"	2344853
"Out Of Exile"	3224237
"How To Dismantle An Atomic Bomb"	2949351
"The Colour And The Shape"	2815290
"Get Born"	2919830
"Elgar: Cello Concerto & Vaughan Williams: Fantasias"	483133
"Great Opera Choruses"	274504
"ReLoad"	4566304
"Handel: The Messiah (Highlights)"	582029
"The Best Of Men At Work"	2602784
"The Doors"	2669734
"Nielsen: The Six Symphonies"	286998
"Rotten Apples: Greatest Hits"	4450707
"Plays Metallica By Four Cellos"	2671407
"In Your Honor [Disc 1]"	2409295
"Acústico MTV [Live]"	3941268
"As Canções de Eu Tu Eles"	2886236
"The Cream Of Clapton"	4373202
"Sir Neville Marriner: A Celebration"	348971
"A Real Dead One"	3587182
"Radio Brasil (O Som da Jovem Vanguarda) - Seleccao de Henrique Amaro"	4428843
"Achtung Baby"	3328489
"The Real Thing"	3325748
"Mascagni: Cavalleria Rusticana"	243436
"Diary of a Madman (Remastered)"	290851
"BBC Sessions [Disc 1] [Live]"	4489920
"Fauré: Requiem, Ravel: Pavane & Others"	258924
"Prenda Minha"	3819382
"IV"	2557462
"Restless and Wild"	858088
"Beethoven: Symphony No. 6 'Pastoral' Etc."	339567
"Santana Live"	4043543
"Black Sabbath Vol. 4 (Remaster)"	2601921
"Prokofiev: Romeo & Juliet"	275015
"Beyond Good And Evil"	3062903
"Greatest Kiss"	4575025
"Na Pista"	2559734
"The Office, Season 1"	7975164
"Instant Karma: The Amnesty International Campaign to Save Darfur"	5134886
"Compositores"	3594651
"Cássia Eller - Coleção Sem Limite [Disc 2]"	3395232
"Load"	4738605
"A Copland Celebration, Vol. I"	198064
"Live [Disc 1]"	3299705
"Album Of The Year"	2586640
"Volume Dois"	3420285
"The Song Remains The Same (Disc 2)"	3037439
"Chill: Brazil (Disc 2)"	4221459
"Van Halen III"	3923402
"In Step"	2468671
"My Way: The Best Of Frank Sinatra [Disc 1]"	4539941
"Vault: Def Leppard's Greatest Hits"	4401077
"Purcell: Music for the Queen Mary"	142081
"Purpendicular"	3749220
"Bartok: Violin & Viola Concertos"	299350
"Appetite for Destruction"	3230986
"Hot Rocks, 1964-1971 (Disc 1)"	2311283
"Tribute"	4372837
"Sambas De Enredo 2001"	4388174
"Carmina Burana"	156710
"Pure Cult: The Best Of The Cult (For Rockers, Ravers, Lovers & Sinners) [UK]"	4652740
"Led Zeppelin III"	2580189
"Weill: The Seven Deadly Sins"	376510
"Pachelbel: Canon & Gigue"	271788
"Misplaced Childhood"	2477370
"International Superhits"	3645509
"Arquivo II"	2507828
"From The Muddy Banks Of The Wishkah [Live]"	3243381
"Serie Sem Limite (Disc 2)"	2894883
"Greatest Hits II"	4558541
"Wagner: Favourite Overtures"	189008
"My Generation - The Very Best Of The Who"	4580064
"Live After Death"	5827856
"Berlioz: Symphonie Fantastique"	561967
"Acústico MTV"	4523796
"Milton Nascimento Ao Vivo"	2815263
"Bach: Goldberg Variations"	120463
"The Last Night of the Proms"	250031
"Bach: The Brandenburg Concertos"	307244
"The Return Of The Space Cowboy"	3967524
"Mozart Gala: Famous Arias"	174813
"Beethoven: Symhonies Nos. 5 & 6"	392462
"Every Kind of Light"	411967
"Locatelli: Concertos for Violin, Strings and Continuo, Vol. 3"	493573
"Somewhere in Time"	3084379
"Black Sabbath"	2294801
"Mezmerize"	2172650
"Machine Head"	2258595
"Jota Quest-1995"	3016355
"Unplugged [Live]"	3405368
"By The Way"	4129951
"Mendelssohn: A Midsummer Night's Dream"	387826
"Fear Of The Dark"	3517930
"Meus Momentos"	2935452
"Core"	3218749
"Supernatural"	4500551
"Acústico"	4312233
"Miles Ahead"	3134243
"Vozes do MPB"	2858678
"Carnaval 2001"	3926015
"Prokofiev: Symphony No.5 & Stravinksy: Le Sacre Du Printemps"	234746
"SCRIABIN: Vers la flamme"	101293
"Vivaldi: The Four Seasons"	199086
"Vinicius De Moraes"	3254721
"Cake: B-Sides and Rarities"	234013
"Tchaikovsky: 1812 Festival Overture, Op.49, Capriccio Italien & Beethoven: Wellington's Victory"	412000
"Dark Side Of The Moon"	2572638
"Iron Maiden"	2446938
"Bizet: Carmen Highlights"	132932
"Presence"	2668613
"Kill 'Em All"	3080852
"Mais Do Mesmo"	4144347
"A TempestadeTempestade Ou O Livro Dos Dias"	4022509
"BackBeat Soundtrack"	1615722
"Ao Vivo [IMPORT]"	4065140
"The Song Remains The Same (Disc 1)"	2943971
"Pavarotti's Opera Made Easy"	176911
"[1997] Black Light Syndrome"	4030534
"Afrociberdelia"	4238776
"Cesta Básica"	1738470
"Da Lama Ao Caos"	3016667
"Greatest Hits"	15065731
"Jorge Ben Jor 25 Anos"	4571265
"A Matter of Life and Death"	4755239
"Voodoo Lounge"	3730984
"Ride The Lightning"	2850688
"B-Sides 1980-1990"	3594885
"The Essential Miles Davis [Disc 2]"	4398808
"Grieg: Peer Gynt Suites & Sibelius: Pelléas et Mélisande"	253422
"The Singles"	3864679
"Speak of the Devil"	4215305
"The Ultimate Relexation Album"	385506
"Chill: Brazil (Disc 1)"	3701306
"Realize"	693207
"Greatest Hits I"	3508522
"Slaves And Masters"	2815003
"The Police Greatest Hits"	3578900
"Chronicle, Vol. 2"	4499818
"Black Album"	3759224
"In Through The Out Door"	2555478
"Carry On"	3292399
"Minha Historia"	7875643
```

### Lista los 10 álbumes con más pistas.

```sql
SELECT
    a.title AS album_title,
    COUNT(t.track_id) AS total_tracks
FROM
    album a
JOIN
    track t ON a.album_id = t.album_id
JOIN
    artist ar ON a.artist_id = ar.artist_id
GROUP BY
    a.album_id, a.title
ORDER BY total_tracks DESC
LIMIT 10

#################
RESULT:
#################

"album_title"	"total_tracks"
"Greatest Hits"	57
"Minha Historia"	34
"Unplugged"	30
"Lost, Season 3"	26
"Lost, Season 1"	25
"The Office, Season 3"	25
"My Way: The Best Of Frank Sinatra [Disc 1]"	24
"Lost, Season 2"	24
"Battlestar Galactica (Classic), Season 1"	24
"Heroes, Season 1"	23

```

### Encuentra la longitud promedio de la pista para cada género.

```sql
SELECT
    g.name AS genre,
    AVG(t.milliseconds) AS average_duration_ms
FROM
    genre g
JOIN
    track t ON g.genre_id = t.genre_id
GROUP BY
    g.name
ORDER BY
    average_duration_ms

#################
RESULT:
#################

"genre"	"average_duration_ms"
"Rock And Roll"	134643.500000000000
"Opera"	174813.000000000000
"Hip Hop/Rap"	178176.285714285714
"Easy Listening"	189164.208333333333
"Bossa Nova"	219590.000000000000
"R&B/Soul"	220066.852459016393
"World"	224923.821428571429
"Pop"	229034.104166666667
"Latin"	232859.262521588946
"Alternative & Punk"	234353.849397590361
"Soundtrack"	244370.883720930233
"Reggae"	247177.758620689655
"Alternative"	264058.525000000000
"Blues"	270359.777777777778
"Rock"	283910.043176561295
"Jazz"	291755.376923076923
"Classical"	293867.567567567568
"Heavy Metal"	297452.928571428571
"Electronica/Dance"	302985.800000000000
"Metal"	309749.443850267380
"Comedy"	1585263.705882352941
"TV Shows"	2145041.021505376344
"Drama"	2575283.781250000000
"Science Fiction"	2625549.076923076923
"Sci Fi & Fantasy"	2911783.038461538462

```

### Para cada cliente, encuentra la cantidad total que han gastado.

```sql
SELECT
    c.customer_id,
    SUM(i.total) AS total_spent
FROM
    customer c
JOIN
    invoice i ON c.customer_id = i.customer_id
GROUP BY
    c.customer_id
ORDER BY
    total_spent DESC;

#################
RESULT:
#################

"customer_id"	"total_spent"
6	49.62
26	47.62
57	46.62
45	45.62
46	45.62
28	43.62
37	43.62
24	43.62
7	42.62
25	42.62
44	41.62
48	40.62
5	40.62
43	40.62
3	39.62
4	39.62
34	39.62
22	39.62
42	39.62
17	39.62
20	39.62
1	39.62
51	38.62
19	38.62
40	38.62
15	38.62
58	38.62
39	38.62
9	37.62
38	37.62
31	37.62
12	37.62
36	37.62
35	37.62
10	37.62
30	37.62
21	37.62
49	37.62
47	37.62
29	37.62
56	37.62
52	37.62
13	37.62
41	37.62
14	37.62
32	37.62
53	37.62
50	37.62
23	37.62
33	37.62
8	37.62
54	37.62
18	37.62
55	37.62
27	37.62
2	37.62
16	37.62
11	37.62
59	36.64

```

### Para cada país, encuentra la cantidad total gastada por los clientes.

```sql
SELECT
    c.country,
    SUM(i.total) AS total_spent
FROM
    customer c
JOIN
    invoice i ON c.country = i.billing_country
GROUP BY
    c.country
ORDER BY
    total_spent DESC;

#################
RESULT:
#################

"country"	"total_spent"
"USA"	6799.78
"Canada"	2431.68
"France"	975.50
"Brazil"	950.50
"Germany"	625.92
"United Kingdom"	338.58
"Czech Republic"	180.48
"Portugal"	154.48
"India"	150.52
"Chile"	46.62
"Ireland"	45.62
"Hungary"	45.62
"Austria"	42.62
"Finland"	41.62
"Netherlands"	40.62
"Norway"	39.62
"Sweden"	38.62
"Argentina"	37.62
"Belgium"	37.62
"Poland"	37.62
"Australia"	37.62
"Italy"	37.62
"Denmark"	37.62
"Spain"	37.62
```

### Clasifica a los clientes en cada país por la cantidad total que han gastado.

```sql
SELECT
    c.country,
	c.customer_id,
    SUM(i.total) AS total_spent
FROM
    customer c
JOIN
    invoice i ON c.country = i.billing_country
GROUP BY
    c.country, c.customer_id
ORDER BY
    c.country DESC;

#################
RESULT:
#################

"country"	"customer_id"	"total_spent"
"USA"	17	523.06
"USA"	18	523.06
"USA"	22	523.06
"USA"	16	523.06
"USA"	28	523.06
"USA"	21	523.06
"USA"	23	523.06
"USA"	20	523.06
"USA"	19	523.06
"USA"	24	523.06
"USA"	25	523.06
"USA"	26	523.06
"USA"	27	523.06
"United Kingdom"	54	112.86
"United Kingdom"	52	112.86
"United Kingdom"	53	112.86
"Sweden"	51	38.62
"Spain"	50	37.62
"Portugal"	35	77.24
"Portugal"	34	77.24
"Poland"	49	37.62
"Norway"	4	39.62
"Netherlands"	48	40.62
"Italy"	47	37.62
"Ireland"	46	45.62
"India"	58	75.26
"India"	59	75.26
"Hungary"	45	45.62
"Germany"	38	156.48
"Germany"	2	156.48
"Germany"	37	156.48
"Germany"	36	156.48
"France"	41	195.10
"France"	43	195.10
"France"	42	195.10
"France"	39	195.10
"France"	40	195.10
"Finland"	44	41.62
"Denmark"	9	37.62
"Czech Republic"	6	90.24
"Czech Republic"	5	90.24
"Chile"	57	46.62
"Canada"	30	303.96
"Canada"	15	303.96
"Canada"	14	303.96
"Canada"	31	303.96
"Canada"	29	303.96
"Canada"	32	303.96
"Canada"	3	303.96
"Canada"	33	303.96
"Brazil"	1	190.10
"Brazil"	12	190.10
"Brazil"	11	190.10
"Brazil"	13	190.10
"Brazil"	10	190.10
"Belgium"	8	37.62
"Austria"	7	42.62
"Australia"	55	37.62
"Argentina"	56	37.62

```

### Para cada artista, encuentra el álbum con más pistas y clasifica a los artistas por este número.

```sql
WITH track_counts AS (
    SELECT
        ar.artist_id,
        ar.name AS artist_name,
        al.album_id,
        al.title AS album_title,
        COUNT(t.track_id) AS track_count
    FROM
        artist ar
    JOIN
        album al ON ar.artist_id = al.artist_id
    JOIN
        track t ON al.album_id = t.album_id
    GROUP BY
        ar.artist_id, ar.name, al.album_id, al.title
),
max_album_per_artist AS (
    SELECT DISTINCT ON (artist_id)
        artist_id,
        artist_name,
        album_id,
        album_title,
        track_count
    FROM
        track_counts
    ORDER BY
        artist_id, track_count DESC
)
SELECT
    artist_name,
    album_title,
    track_count
FROM
    max_album_per_artist
ORDER BY
    track_count DESC;

#################
RESULT:
#################

"artist_name"	"album_title"	"track_count"
"Lenny Kravitz"	"Greatest Hits"	57
"Chico Buarque"	"Minha Historia"	34
"Eric Clapton"	"Unplugged"	30
"Lost"	"Lost, Season 3"	26
"The Office"	"The Office, Season 3"	25
"Battlestar Galactica (Classic)"	"Battlestar Galactica (Classic), Season 1"	24
"Frank Sinatra"	"My Way: The Best Of Frank Sinatra [Disc 1]"	24
"Heroes"	"Heroes, Season 1"	23
"U2"	"Instant Karma: The Amnesty International Campaign to Save Darfur"	23
"Chico Science & Nação Zumbi"	"Afrociberdelia"	23
"Titãs"	"Acústico"	22
"Gene Krupa"	"Up An' Atom"	22
"Green Day"	"International Superhits"	21
"Os Paralamas Do Sucesso"	"Acústico MTV"	21
"Creedence Clearwater Revival"	"Chronicle, Vol. 1"	20
"James Brown"	"Sex Machine"	20
"The Who"	"My Generation - The Very Best Of The Who"	20
"Kiss"	"Greatest Kiss"	20
"House Of Pain"	"House of Pain"	19
"Battlestar Galactica"	"Battlestar Galactica, Season 3"	19
"Zeca Pagodinho"	"Ao Vivo [IMPORT]"	19
"Iron Maiden"	"Live After Death"	18
"Caetano Veloso"	"Prenda Minha"	18
"Marisa Monte"	"Barulhinho Bom"	18
"The Cult"	"Pure Cult: The Best Of The Cult (For Rockers, Ravers, Lovers & Sinners) [UK]"	18
"The Clash"	"The Singles"	18
"Marvin Gaye"	"Seek And Shall Find: More Of The Best (1963-1981)"	18
"Smashing Pumpkins"	"Rotten Apples: Greatest Hits"	18
"Jimi Hendrix"	"Are You Experienced?"	17
"Van Halen"	"The Best Of Van Halen, Vol. I"	17
"Body Count"	"Body Count"	17
"Cidade Negra"	"Acústico MTV [Live]"	17
"Soundgarden"	"A-Sides"	17
"Marcos Valle"	"Chill: Brazil (Disc 1)"	17
"O Rappa"	"Radio Brasil (O Som da Jovem Vanguarda) - Seleccao de Henrique Amaro"	17
"Red Hot Chili Peppers"	"Blood Sugar Sex Magik"	17
"Queen"	"Greatest Hits II"	17
"Nirvana"	"From The Muddy Banks Of The Wishkah [Live]"	17
"Mötley Crüe"	"Motley Crue Greatest Hits"	17
"Antônio Carlos Jobim"	"Chill: Brazil (Disc 2)"	17
"Legião Urbana"	"Mais Do Mesmo"	16
"Pearl Jam"	"Live On Two Legs [Live]"	16
"Planet Hemp"	"Os Cães Ladram Mas A Caravana Não Pára"	16
"R.E.M."	"The Best Of R.E.M.: The IRS Years"	16
"Funk Como Le Gusta"	"Roda De Funk"	16
"Guns N' Roses"	"Use Your Illusion I"	16
"Def Leppard"	"Vault: Def Leppard's Greatest Hits"	16
"Judas Priest"	"Living After Midnight"	16
"Metallica"	"Garage Inc. (Disc 2)"	16
"Faith No More"	"King For A Day Fool For A Lifetime"	15
"Aerosmith"	"Big Ones"	15
"Gilberto Gil"	"Quanta Gente Veio Ver (Live)"	15
"Toquinho & Vinícius"	"Vinícius De Moraes - Sem Limite"	15
"Vinícius De Moraes"	"Vinicius De Moraes"	15
"Cássia Eller"	"Cássia Eller - Sem Limite [Disc 1]"	15
"Motörhead"	"Ace Of Spades"	15
"O Terço"	"Compositores"	15
"The Rolling Stones"	"Voodoo Lounge"	15
"The Tea Party"	"Tangents"	15
"Tim Maia"	"Serie Sem Limite (Disc 1)"	15
"Falamansa"	"Deixa Entrar"	14
"Elis Regina"	"Elis Regina-Minha História"	14
"Audioslave"	"Audioslave"	14
"Raul Seixas"	"Raul Seixas"	14
"Ed Motta"	"The Best of Ed Motta"	14
"Rush"	"Retrospective I (1974-1980)"	14
"Led Zeppelin"	"BBC Sessions [Disc 1] [Live]"	14
"Gonzaguinha"	"Meus Momentos"	14
"The Police"	"The Police Greatest Hits"	14
"UB40"	"UB40 The Best Of - Volume Two [UK]"	14
"Olodum"	"Olodum"	14
"Os Mutantes"	"Minha História"	14
"Various Artists"	"Axé Bahia 2001"	14
"Ozzy Osbourne"	"Tribute"	14
"Chris Cornell"	"Carry On"	14
"Passengers"	"Original Soundtracks 1"	14
"Miles Davis"	"Miles Ahead"	14
"Jorge Ben"	"Jorge Ben Jor 25 Anos"	14
"Lulu Santos"	"Lulu Santos - RCA 100 Anos De Música - Álbum 02"	14
"João Suplicy"	"Cafezinho"	14
"JET"	"Get Born"	13
"Black Label Society"	"Alcohol Fueled Brewtality Live! [Disc 1]"	13
"Incognito"	"Blue Moods"	13
"Djavan"	"Djavan Ao Vivo - Vol. 1"	13
"Foo Fighters"	"The Colour And The Shape"	13
"Milton Nascimento"	"Minas"	13
"Santana"	"Supernatural"	13
"Alanis Morissette"	"Jagged Little Pill"	13
"Velvet Revolver"	"Contraband"	13
"Godsmack"	"Faceless"	12
"Stone Temple Pilots"	"Core"	12
"Page & Plant"	"Walking Into Clarksdale"	12
"BackBeat"	"BackBeat Soundtrack"	12
"Alice In Chains"	"Facelift"	12
"Spyro Gyra"	"Heart of the Night"	12
"Amy Winehouse"	"Back to Black"	12
"Deep Purple"	"Purpendicular"	12
"David Coverdale"	"Into The Light"	12
"Mônica Marianno"	"Demorou..."	12
"Jota Quest"	"Jota Quest-1995"	12
"Scorpions"	"20th Century Masters - The Millennium Collection: The Best of Scorpions"	12
"Skank"	"Maquinarama"	12
"The Doors"	"The Doors"	11
"R.E.M. Feat. Kate Pearson"	"Out Of Time"	11
"System Of A Down"	"Mezmerize"	11
"Buddy Guy"	"The Best Of Buddy Guy - The Millenium Collection"	11
"Bruce Dickinson"	"Chemical Wedding"	11
"Jamiroquai"	"The Return Of The Space Cowboy"	11
"Black Sabbath"	"Black Sabbath Vol. 4 (Remaster)"	10
"Joe Satriani"	"Surfing with the Alien (Remastered)"	10
"Cláudio Zoli"	"Na Pista"	10
"AC/DC"	"For Those About To Rock We Salute You"	10
"The Black Crowes"	"Live [Disc 1]"	10
"Stevie Ray Vaughan & Double Trouble"	"In Step"	10
"Raimundos"	"Cesta Básica"	10
"Marillion"	"Misplaced Childhood"	10
"Paul D'Ianno"	"The Beast Live"	10
"Men At Work"	"The Best Of Men At Work"	10
"Temple of the Dog"	"Temple of the Dog"	10
"Dennis Chambers"	"Outbreak"	9
"Pink Floyd"	"Dark Side Of The Moon"	9
"Frank Zappa & Captain Beefheart"	"Bongo Fury"	9
"Apocalyptica"	"Plays Metallica By Four Cellos"	8
"Billy Cobham"	"The Best Of Billy Cobham"	8
"Terry Bozzio, Tony Levin & Steve Stevens"	"[1997] Black Light Syndrome"	7
"Accept"	"Restless and Wild"	3
"Habib Koité and Bamada"	"Muso Ko"	2
"The King's Singers"	"English Renaissance"	2
"Academy of St. Martin in the Fields & Sir Neville Marriner"	"The World of Classical Favourites"	2
"Karsh Kale"	"Realize"	2
"Aisha Duo"	"Quiet Songs"	2
"The Posies"	"Every Kind of Light"	2
"Academy of St. Martin in the Fields, Sir Neville Marriner & Thurston Dart"	"Bach: Orchestral Suites Nos. 1 - 4"	1
"Mela Tenenbaum, Pro Musica Prague & Richard Kapp"	"Locatelli: Concertos for Violin, Strings and Continuo, Vol. 3"	1
"Emerson String Quartet"	"Schubert: The Late String Quartets & String Quintet (3 CD's)"	1
"C. Monteverdi, Nigel Rogers - Chiaroscuro; London Baroque; London Cornett & Sackbu"	"Monteverdi: L'Orfeo"	1
"Nash Ensemble"	"Mozart: Chamber Music"	1
"Philip Glass Ensemble"	"Koyaanisqatsi (Soundtrack from the Motion Picture)"	1
"Dread Zeppelin"	"Un-Led-Ed"	1
"Aquaman"	"Aquaman"	1
"Cake"	"Cake: B-Sides and Rarities"	1
"Luciana Souza/Romero Lubambo"	"Duos II"	1
"Aaron Goldberg"	"Worlds"	1
"Nicolaus Esterhazy Sinfonia"	"The Best of Beethoven"	1
"Alberto Turco & Nova Schola Gregoriana"	"Adorate Deum: Gregorian Chant from the Proper of the Mass"	1
"Richard Marlow & The Choir of Trinity College, Cambridge"	"Allegri: Miserere"	1
"English Concert & Trevor Pinnock"	"Handel: Music for the Royal Fireworks (Original Version 1749)"	1
"Anne-Sophie Mutter, Herbert Von Karajan & Wiener Philharmoniker"	"Vivaldi: The Four Seasons"	1
"Hilary Hahn, Jeffrey Kahane, Los Angeles Chamber Orchestra & Margaret Batjer"	"Bach: Violin Concertos"	1
"Wilhelm Kempff"	"Bach: Goldberg Variations"	1
"Yo-Yo Ma"	"Bach: The Cello Suites"	1
"Scholars Baroque Ensemble"	"Handel: The Messiah (Highlights)"	1
"Academy of St. Martin in the Fields Chamber Ensemble & Sir Neville Marriner"	"Sir Neville Marriner: A Celebration"	1
"Berliner Philharmoniker, Claudio Abbado & Sabine Meyer"	"Mozart: Wind Concertos"	1
"Royal Philharmonic Orchestra & Sir Thomas Beecham"	"Haydn: Symphonies 99 - 104"	1
"Orchestre Révolutionnaire et Romantique & John Eliot Gardiner"	"Beethoven: Symhonies Nos. 5 & 6"	1
"Britten Sinfonia, Ivor Bolton & Lesley Garrett"	"A Soprano Inspired"	1
"Chicago Symphony Chorus, Chicago Symphony Orchestra & Sir Georg Solti"	"Great Opera Choruses"	1
"Sir Georg Solti & Wiener Philharmoniker"	"Wagner: Favourite Overtures"	1
"Academy of St. Martin in the Fields, John Birch, Sir Neville Marriner & Sylvia McNair"	"Fauré: Requiem, Ravel: Pavane & Others"	1
"London Symphony Orchestra & Sir Charles Mackerras"	"Tchaikovsky: The Nutcracker"	1
"Barry Wordsworth & BBC Concert Orchestra"	"The Last Night of the Proms"	1
"Herbert Von Karajan, Mirella Freni & Wiener Philharmoniker"	"Puccini: Madama Butterfly - Highlights"	1
"Eugene Ormandy"	"Strauss: Waltzes"	1
"Luciano Pavarotti"	"Pavarotti's Opera Made Easy"	1
"Leonard Bernstein & New York Philharmonic"	"Great Performances - Barber's Adagio and Other Romantic Favorites for Strings"	1
"Boston Symphony Orchestra & Seiji Ozawa"	"Carmina Burana"	1
"Aaron Copland & London Symphony Orchestra"	"A Copland Celebration, Vol. I"	1
"Ton Koopman"	"Bach: Toccata & Fugue in D Minor"	1
"Sergei Prokofiev & Yuri Temirkanov"	"Prokofiev: Symphony No.1"	1
"Chicago Symphony Orchestra & Fritz Reiner"	"Scheherazade"	1
"Orchestra of The Age of Enlightenment"	"Bach: The Brandenburg Concertos"	1
"Emanuel Ax, Eugene Ormandy & Philadelphia Orchestra"	"Chopin: Piano Concertos Nos. 1 & 2"	1
"James Levine"	"Mascagni: Cavalleria Rusticana"	1
"Berliner Philharmoniker & Hans Rosbaud"	"Sibelius: Finlandia"	1
"Maurizio Pollini"	"Beethoven Piano Sonatas: Moonlight & Pastorale"	1
"Gustav Mahler"	"Great Recordings of the Century - Mahler: Das Lied von der Erde"	1
"Felix Schmidt, London Symphony Orchestra & Rafael Frühbeck de Burgos"	"Elgar: Cello Concerto & Vaughan Williams: Fantasias"	1
"Edo de Waart & San Francisco Symphony"	"Adams, John: The Chairman Dances"	1
"Antal Doráti & London Symphony Orchestra"	"Tchaikovsky: 1812 Festival Overture, Op.49, Capriccio Italien & Beethoven: Wellington's Victory"	1
"Choir Of Westminster Abbey & Simon Preston"	"Palestrina: Missa Papae Marcelli & Allegri: Miserere"	1
"Michael Tilson Thomas & San Francisco Symphony"	"Prokofiev: Romeo & Juliet"	1
"Chor der Wiener Staatsoper, Herbert Von Karajan & Wiener Philharmoniker"	"Bizet: Carmen Highlights"	1
"Berliner Philharmoniker & Herbert Von Karajan"	"Prokofiev: Symphony No.5 & Stravinksy: Le Sacre Du Printemps"	1
"Sir Georg Solti, Sumi Jo & Wiener Philharmoniker"	"Mozart Gala: Famous Arias"	1
"Christopher O'Riley"	"SCRIABIN: Vers la flamme"	1
"Fretwork"	"Armada: Music from the Courts of England and Spain"	1
"Calexico"	"Carried to Dust (Bonus Track Version)"	1
"Otto Klemperer & Philharmonia Orchestra"	"Beethoven: Symphony No. 6 'Pastoral' Etc."	1
"Yehudi Menuhin"	"Bartok: Violin & Viola Concertos"	1
"Philharmonia Orchestra & Sir Neville Marriner"	"Mendelssohn: A Midsummer Night's Dream"	1
"Les Arts Florissants & William Christie"	"Charpentier: Divertissements, Airs & Concerts"	1
"The 12 Cellists of The Berlin Philharmonic"	"South American Getaway"	1
"Adrian Leaper & Doreen de Feis"	"Górecki: Symphony No. 3"	1
"Roger Norrington, London Classical Players"	"Purcell: The Fairy Queen"	1
"Charles Dutoit & L'Orchestre Symphonique de Montréal"	"The Ultimate Relexation Album"	1
"Equale Brass Ensemble, John Eliot Gardiner & Munich Monteverdi Orchestra and Choir"	"Purcell: Music for the Queen Mary"	1
"Kent Nagano and Orchestre de l'Opéra de Lyon"	"Weill: The Seven Deadly Sins"	1
"Julian Bream"	"J.S. Bach: Chaconne, Suite in E Minor, Partita in E Major & Prelude, Fugue and Allegro"	1
"Martin Roscoe"	"Szymanowski: Piano Works, Vol. 1"	1
"Göteborgs Symfoniker & Neeme Järvi"	"Nielsen: The Six Symphonies"	1
"Itzhak Perlman"	"Great Recordings of the Century: Paganini's 24 Caprices"	1
"Michele Campanella"	"Liszt - 12 Études D'Execution Transcendante"	1
"Gerald Moore"	"Great Recordings of the Century - Shubert: Schwanengesang, 4 Lieder"	1
```

### Selecciona todas las pistas que tienen la palabra "love" en su título.

```sql
SELECT
    track_id,
    name AS track_title
FROM
    track
WHERE
    name ILIKE '%love%';
#################
RESULT:
#################

"track_id"	"track_title"
24	"Love In An Elevator"
56	"Love, Hate, Love"
195	"Let Me Love You Baby"
335	"My Love"
341	"The Girl I Love She Got Long Black Wavy Hair"
345	"Whole Lotta Love"
413	"Loverman"
440	"Love Gun"
444	"Do You Love Me"
449	"Calling Dr. Love"
493	"Love Is Blind"
495	"Cry For Love"
496	"Living On Love"
571	"Love Of My Life"
589	"Um Love"
593	"Do You Have Other Loves?"
639	"Don't Take Your Love From Me"
749	"I Need Love"
751	"Love Child"
790	"Cascades : I'm Not Your Lover"
803	"Love Conquers All"
808	"Love Don't Mean a Thing"
812	"You Can't Do it Right (With the One You Love)"
819	"Talk About Love"
828	"Love Bites"
834	"When Love & Hate Collide"
836	"Make Love Like A Man"
894	"Sunshine Of Your Love"
921	"Old Love"
930	"She Loves Me Not"
970	"Underwater Love"
1039	"What Now My Love"
1040	"Summer Love"
1042	"Love And Marriage"
1055	"Loves Been Good To Me"
1089	"Is This Love (Live)"
1134	"Jesus Of Suburbia / City Of The Damned / I Don't Care / Dearly Beloved / Tales Of Another Broken Home"
1189	"Love Is The Colour"
1227	"Wasting Love"
1244	"The Thin Line Between Love & Hate"
1261	"Wasting Love"
1310	"Wasting Love"
1468	"Rollover D.J."
1483	"Love Or Confusion"
1485	"May This Be Love"
1554	"Turbo Lover"
1565	"Do You Love Me"
1571	"I Still Love You"
1585	"Whole Lotta Love (Medley)"
1608	"All My Love"
1627	"Whole Lotta Love"
1670	"Whole Lotta Love"
1715	"Let Love Rule"
1765	"Give Me Love"
1777	"When I Had Your Love"
1782	"Gonna Keep On Tryin' Till I Win Your Love"
1783	"Gonna Give Her All The Love I've Got"
1787	"You Sure Love To Ball"
1790	"Heavy Love Affair"
1943	"Love Me Like A Reptile"
1954	"Dirty Love"
1983	"Too Fast For Love"
2123	"House Of Love"
2180	"Love Boat Captain"
2220	"Nothing But Love"
2262	"Crazy Little Thing Called Love"
2263	"Somebody To Love"
2265	"Good Old-Fashioned Lover Boy"
2277	"Get Down, Make Love"
2331	"The One I Love"
2372	"My Lovely Man"
2401	"This Velvet Glove"
2437	"It's Only Love"
2503	"Stand Inside Your Love"
2504	"Real Love"
2508	"Loud Love"
2535	"Let Me Love You Baby"
2540	"Love Me Darlin'"
2628	"Love Removal Machine"
2632	"Love"
2690	"Love Is Strong"
2757	"New Love"
2937	"Love Is Blindness"
2952	"Love Comes Tumbling"
2955	"Everlasting Love"
2958	"Luminous Times (Hold On To Love)"
2967	"Love And Peace Or Else"
2976	"Do You Feel Loved"
2995	"Pride (In The Name Of Love)"
2997	"Love Rescue Me"
2998	"When Love Comes To Town"
3004	"Pride (In The Name Of Love)"
3015	"When Love Comes To Town"
3045	"(I Can't Help) Falling In Love With You"
3065	"Ain't Talkin' 'bout Love"
3072	"Why Can't This Be Love"
3074	"When It's Love"
3084	"Ain't Talkin' 'Bout Love"
3088	"Feel Your Love Tonight"
3134	"Is This Love"
3135	"Love Ain't No Stranger"
3136	"Looking For Love"
3142	"The Deeper The Love"
3261	"Oh, My Love"
3275	"Real Love"
3294	"Believe in Love"
3295	"Rhythm of Love"
3316	"All My Love"
3335	"Freestyle Love"
3355	"Love Comes"
3377	"Arms Around Your Love"
3460	"Love Is a Losing Game"
3470	"I Heard Love Is Blind"
3471	"(There Is) No Greater Love (Teo Licks)"
```

### Selecciona a todos los clientes cuyo primer nombre comienza con 'A'.

```sql
SELECT
	customer_id,
    first_name,
	last_name
FROM
    customer
WHERE
    first_name ILIKE 'a%';

#################
RESULT:
#################
"customer_id"	"first_name"	"last_name"
7	"Astrid"	"Gruber"
11	"Alexandre"	"Rocha"
32	"Aaron"	"Mitchell"s
```

### Calcula el porcentaje del total de la factura que representa cada factura.

```sql
WITH total_invoice AS (
    SELECT SUM(total) AS grand_total
    FROM invoice
)
SELECT
    i.invoice_id,
    i.total,
    ROUND((i.total / ti.grand_total) * 100, 2) AS percentage_of_total
FROM
    invoice i,
    total_invoice ti
ORDER BY
    percentage_of_total DESC;

#################
RESULT:
#################

"invoice_id"	"total"	"percentage_of_total"
404	25.86	1.11
299	23.86	1.02
194	21.86	0.94
96	21.86	0.94
89	18.86	0.81
201	18.86	0.81
88	17.91	0.77
313	16.86	0.72
306	16.86	0.72
103	15.86	0.68
208	15.86	0.68
193	14.91	0.64
5	13.86	0.60
26	13.86	0.60
124	13.86	0.60
180	13.86	0.60
173	13.86	0.60
131	13.86	0.60
166	13.86	0.60
159	13.86	0.60
19	13.86	0.60
138	13.86	0.60
152	13.86	0.60
145	13.86	0.60
376	13.86	0.60
369	13.86	0.60
362	13.86	0.60
355	13.86	0.60
33	13.86	0.60
348	13.86	0.60
341	13.86	0.60
40	13.86	0.60
334	13.86	0.60
327	13.86	0.60
47	13.86	0.60
320	13.86	0.60
54	13.86	0.60
397	13.86	0.60
61	13.86	0.60
292	13.86	0.60
411	13.86	0.60
68	13.86	0.60
285	13.86	0.60
278	13.86	0.60
75	13.86	0.60
271	13.86	0.60
264	13.86	0.60
12	13.86	0.60
82	13.86	0.60
257	13.86	0.60
250	13.86	0.60
243	13.86	0.60
236	13.86	0.60
229	13.86	0.60
222	13.86	0.60
390	13.86	0.60
215	13.86	0.60
110	13.86	0.60
383	13.86	0.60
117	13.86	0.60
187	13.86	0.60
311	11.94	0.51
312	10.91	0.47
298	10.91	0.47
102	9.91	0.43
179	8.91	0.38
214	8.91	0.38
284	8.91	0.38
130	8.91	0.38
277	8.91	0.38
11	8.91	0.38
74	8.91	0.38
207	8.91	0.38
389	8.91	0.38
270	8.91	0.38
109	8.91	0.38
263	8.91	0.38
123	8.91	0.38
81	8.91	0.38
206	8.94	0.38
256	8.91	0.38
18	8.91	0.38
249	8.91	0.38
151	8.91	0.38
368	8.91	0.38
137	8.91	0.38
361	8.91	0.38
200	8.91	0.38
410	8.91	0.38
32	8.91	0.38
242	8.91	0.38
354	8.91	0.38
186	8.91	0.38
347	8.91	0.38
235	8.91	0.38
25	8.91	0.38
39	8.91	0.38
396	8.91	0.38
340	8.91	0.38
95	8.91	0.38
333	8.91	0.38
158	8.91	0.38
403	8.91	0.38
46	8.91	0.38
116	8.91	0.38
326	8.91	0.38
228	8.91	0.38
319	8.91	0.38
375	8.91	0.38
172	8.91	0.38
291	8.91	0.38
165	8.91	0.38
67	8.91	0.38
221	8.91	0.38
60	8.91	0.38
144	8.91	0.38
53	8.91	0.38
4	8.91	0.38
382	8.91	0.38
305	8.91	0.38
205	7.96	0.34
310	7.96	0.34
87	6.94	0.30
52	5.94	0.26
3	5.94	0.26
10	5.94	0.26
17	5.94	0.26
24	5.94	0.26
31	5.94	0.26
38	5.94	0.26
45	5.94	0.26
59	5.94	0.26
66	5.94	0.26
73	5.94	0.26
80	5.94	0.26
94	5.94	0.26
101	5.94	0.26
108	5.94	0.26
115	5.94	0.26
122	5.94	0.26
129	5.94	0.26
136	5.94	0.26
143	5.94	0.26
150	5.94	0.26
157	5.94	0.26
164	5.94	0.26
171	5.94	0.26
178	5.94	0.26
185	5.94	0.26
192	5.94	0.26
199	5.94	0.26
213	5.94	0.26
220	5.94	0.26
227	5.94	0.26
234	5.94	0.26
241	5.94	0.26
248	5.94	0.26
255	5.94	0.26
262	5.94	0.26
269	5.94	0.26
276	5.94	0.26
283	5.94	0.26
290	5.94	0.26
297	5.94	0.26
304	5.94	0.26
318	5.94	0.26
325	5.94	0.26
332	5.94	0.26
339	5.94	0.26
346	5.94	0.26
353	5.94	0.26
360	5.94	0.26
367	5.94	0.26
374	5.94	0.26
381	5.94	0.26
388	5.94	0.26
395	5.94	0.26
402	5.94	0.26
409	5.94	0.26
142	3.96	0.17
296	3.96	0.17
9	3.96	0.17
156	3.96	0.17
366	3.96	0.17
198	3.96	0.17
121	3.96	0.17
135	3.96	0.17
303	3.96	0.17
177	3.96	0.17
58	3.96	0.17
261	3.96	0.17
408	3.96	0.17
308	3.98	0.17
309	3.98	0.17
79	3.96	0.17
212	3.96	0.17
387	3.96	0.17
51	3.96	0.17
114	3.96	0.17
93	3.96	0.17
191	3.96	0.17
317	3.96	0.17
268	3.96	0.17
373	3.96	0.17
149	3.96	0.17
163	3.96	0.17
240	3.96	0.17
98	3.98	0.17
324	3.96	0.17
359	3.96	0.17
275	3.96	0.17
44	3.96	0.17
394	3.96	0.17
72	3.96	0.17
184	3.96	0.17
331	3.96	0.17
401	3.96	0.17
254	3.96	0.17
23	3.96	0.17
233	3.96	0.17
282	3.96	0.17
204	3.98	0.17
338	3.96	0.17
2	3.96	0.17
16	3.96	0.17
37	3.96	0.17
219	3.96	0.17
247	3.96	0.17
226	3.96	0.17
345	3.96	0.17
86	3.96	0.17
170	3.96	0.17
289	3.96	0.17
107	3.96	0.17
65	3.96	0.17
380	3.96	0.17
352	3.96	0.17
128	3.96	0.17
100	3.96	0.17
30	3.96	0.17
99	3.98	0.17
203	2.98	0.13
71	1.98	0.09
280	1.98	0.09
281	1.98	0.09
70	1.98	0.09
112	1.98	0.09
120	1.98	0.09
287	1.98	0.09
288	1.98	0.09
64	1.98	0.09
106	1.98	0.09
294	1.98	0.09
295	1.98	0.09
63	1.98	0.09
183	1.98	0.09
210	1.98	0.09
301	1.98	0.09
302	1.98	0.09
211	1.98	0.09
57	1.98	0.09
307	1.99	0.09
56	1.98	0.09
1	1.98	0.09
385	1.98	0.09
315	1.98	0.09
316	1.98	0.09
399	1.98	0.09
50	1.98	0.09
49	1.98	0.09
105	1.98	0.09
322	1.98	0.09
323	1.98	0.09
400	1.98	0.09
189	1.98	0.09
190	1.98	0.09
329	1.98	0.09
330	1.98	0.09
43	1.98	0.09
42	1.98	0.09
217	1.98	0.09
336	1.98	0.09
337	1.98	0.09
218	1.98	0.09
343	1.98	0.09
344	1.98	0.09
8	1.98	0.09
36	1.98	0.09
35	1.98	0.09
386	1.98	0.09
350	1.98	0.09
351	1.98	0.09
7	1.98	0.09
358	1.98	0.09
357	1.98	0.09
29	1.98	0.09
28	1.98	0.09
224	1.98	0.09
364	1.98	0.09
365	1.98	0.09
406	1.98	0.09
225	1.98	0.09
371	1.98	0.09
372	1.98	0.09
407	1.98	0.09
22	1.98	0.09
21	1.98	0.09
141	1.98	0.09
147	1.98	0.09
148	1.98	0.09
140	1.98	0.09
97	1.99	0.09
154	1.98	0.09
155	1.98	0.09
378	1.98	0.09
134	1.98	0.09
231	1.98	0.09
161	1.98	0.09
162	1.98	0.09
379	1.98	0.09
133	1.98	0.09
232	1.98	0.09
168	1.98	0.09
169	1.98	0.09
127	1.98	0.09
412	1.99	0.09
175	1.98	0.09
176	1.98	0.09
126	1.98	0.09
92	1.98	0.09
119	1.98	0.09
238	1.98	0.09
239	1.98	0.09
15	1.98	0.09
91	1.98	0.09
182	1.98	0.09
245	1.98	0.09
246	1.98	0.09
14	1.98	0.09
85	1.98	0.09
196	1.98	0.09
252	1.98	0.09
253	1.98	0.09
197	1.98	0.09
84	1.98	0.09
259	1.98	0.09
260	1.98	0.09
392	1.98	0.09
78	1.98	0.09
266	1.98	0.09
267	1.98	0.09
393	1.98	0.09
77	1.98	0.09
113	1.98	0.09
202	1.99	0.09
273	1.98	0.09
274	1.98	0.09
377	0.99	0.04
181	0.99	0.04
20	0.99	0.04
188	0.99	0.04
118	0.99	0.04
195	0.99	0.04
384	0.99	0.04
111	0.99	0.04
209	0.99	0.04
104	0.99	0.04
216	0.99	0.04
223	0.99	0.04
230	0.99	0.04
237	0.99	0.04
90	0.99	0.04
244	0.99	0.04
251	0.99	0.04
391	0.99	0.04
83	0.99	0.04
258	0.99	0.04
265	0.99	0.04
76	0.99	0.04
272	0.99	0.04
279	0.99	0.04
6	0.99	0.04
69	0.99	0.04
286	0.99	0.04
13	0.99	0.04
293	0.99	0.04
62	0.99	0.04
300	0.99	0.04
398	0.99	0.04
55	0.99	0.04
314	0.99	0.04
321	0.99	0.04
48	0.99	0.04
328	0.99	0.04
335	0.99	0.04
41	0.99	0.04
342	0.99	0.04
349	0.99	0.04
34	0.99	0.04
356	0.99	0.04
405	0.99	0.04
363	0.99	0.04
27	0.99	0.04
370	0.99	0.04
146	0.99	0.04
125	0.99	0.04
139	0.99	0.04
153	0.99	0.04
160	0.99	0.04
132	0.99	0.04
167	0.99	0.04
174	0.99	0.04
```

### Calcula el porcentaje de pistas que representa cada género.

```sql
WITH total_tracks AS (
    SELECT COUNT(track_id) AS grand_total_tracks
    FROM track
)
SELECT
    g.name AS genre,
    COUNT(t.track_id) AS genre_track_count,
    ROUND(
        COUNT(t.track_id) * 100.0 / (SELECT COUNT(track_id) AS grand_total_tracks FROM track),
        2
    ) AS percentage_of_total
FROM
    genre g
JOIN
    track t ON g.genre_id = t.genre_id
GROUP BY
    g.genre_id, g.name
ORDER BY
    percentage_of_total DESC;

#################
RESULT:
#################

"genre"	"genre_track_count"	"percentage_of_total"
"Rock"	1297	37.03
"Latin"	579	16.53
"Metal"	374	10.68
"Alternative & Punk"	332	9.48
"Jazz"	130	3.71
"TV Shows"	93	2.65
"Blues"	81	2.31
"Classical"	74	2.11
"Drama"	64	1.83
"R&B/Soul"	61	1.74
"Reggae"	58	1.66
"Pop"	48	1.37
"Soundtrack"	43	1.23
"Alternative"	40	1.14
"Hip Hop/Rap"	35	1.00
"Electronica/Dance"	30	0.86
"World"	28	0.80
"Heavy Metal"	28	0.80
"Sci Fi & Fantasy"	26	0.74
"Easy Listening"	24	0.69
"Comedy"	17	0.49
"Bossa Nova"	15	0.43
"Science Fiction"	13	0.37
"Rock And Roll"	12	0.34
"Opera"	1	0.03
```

### Para cada cliente, compara su gasto total con el del cliente que gastó más.

```sql
WITH total_por_cliente AS (
    SELECT
        c.customer_id,
        c.first_name,
        c.last_name,
        SUM(i.total) AS total_gastado
    FROM
        customer c
    JOIN
        invoice i ON c.customer_id = i.customer_id
    GROUP BY
        c.customer_id, c.first_name, c.last_name
),
gasto_maximo AS (
    SELECT MAX(total_gastado) AS max_gasto FROM total_por_cliente
)
SELECT
    tpc.customer_id,
    tpc.first_name,
    tpc.last_name,
    tpc.total_gastado,
    gm.max_gasto,
    ROUND((tpc.total_gastado * 100.0 / gm.max_gasto), 2) AS porcentaje_respecto_al_maximo
FROM
    total_por_cliente tpc,
    gasto_maximo gm
ORDER BY
    porcentaje_respecto_al_maximo DESC;

#################
RESULT:
#################
"customer_id"	"first_name"	"last_name"	"total_gastado"	"max_gasto"	"porcentaje_respecto_al_maximo"
6	"Helena"	"Holý"	49.62	49.62	100.00
26	"Richard"	"Cunningham"	47.62	49.62	95.97
57	"Luis"	"Rojas"	46.62	49.62	93.95
45	"Ladislav"	"Kovács"	45.62	49.62	91.94
46	"Hugh"	"O'Reilly"	45.62	49.62	91.94
28	"Julia"	"Barnett"	43.62	49.62	87.91
37	"Fynn"	"Zimmermann"	43.62	49.62	87.91
24	"Frank"	"Ralston"	43.62	49.62	87.91
7	"Astrid"	"Gruber"	42.62	49.62	85.89
25	"Victor"	"Stevens"	42.62	49.62	85.89
44	"Terhi"	"Hämäläinen"	41.62	49.62	83.88
48	"Johannes"	"Van der Berg"	40.62	49.62	81.86
5	"František"	"Wichterlová"	40.62	49.62	81.86
43	"Isabelle"	"Mercier"	40.62	49.62	81.86
3	"François"	"Tremblay"	39.62	49.62	79.85
4	"Bjørn"	"Hansen"	39.62	49.62	79.85
34	"João"	"Fernandes"	39.62	49.62	79.85
22	"Heather"	"Leacock"	39.62	49.62	79.85
42	"Wyatt"	"Girard"	39.62	49.62	79.85
17	"Jack"	"Smith"	39.62	49.62	79.85
20	"Dan"	"Miller"	39.62	49.62	79.85
1	"Luís"	"Gonçalves"	39.62	49.62	79.85
51	"Joakim"	"Johansson"	38.62	49.62	77.83
19	"Tim"	"Goyer"	38.62	49.62	77.83
40	"Dominique"	"Lefebvre"	38.62	49.62	77.83
15	"Jennifer"	"Peterson"	38.62	49.62	77.83
58	"Manoj"	"Pareek"	38.62	49.62	77.83
39	"Camille"	"Bernard"	38.62	49.62	77.83
9	"Kara"	"Nielsen"	37.62	49.62	75.82
38	"Niklas"	"Schröder"	37.62	49.62	75.82
31	"Martha"	"Silk"	37.62	49.62	75.82
12	"Roberto"	"Almeida"	37.62	49.62	75.82
36	"Hannah"	"Schneider"	37.62	49.62	75.82
35	"Madalena"	"Sampaio"	37.62	49.62	75.82
10	"Eduardo"	"Martins"	37.62	49.62	75.82
30	"Edward"	"Francis"	37.62	49.62	75.82
21	"Kathy"	"Chase"	37.62	49.62	75.82
49	"Stanislaw"	"Wójcik"	37.62	49.62	75.82
47	"Lucas"	"Mancini"	37.62	49.62	75.82
29	"Robert"	"Brown"	37.62	49.62	75.82
56	"Diego"	"Gutiérrez"	37.62	49.62	75.82
52	"Emma"	"Jones"	37.62	49.62	75.82
13	"Fernanda"	"Ramos"	37.62	49.62	75.82
41	"Marc"	"Dubois"	37.62	49.62	75.82
14	"Mark"	"Philips"	37.62	49.62	75.82
32	"Aaron"	"Mitchell"	37.62	49.62	75.82
53	"Phil"	"Hughes"	37.62	49.62	75.82
50	"Enrique"	"Muñoz"	37.62	49.62	75.82
23	"John"	"Gordon"	37.62	49.62	75.82
33	"Ellie"	"Sullivan"	37.62	49.62	75.82
8	"Daan"	"Peeters"	37.62	49.62	75.82
54	"Steve"	"Murray"	37.62	49.62	75.82
18	"Michelle"	"Brooks"	37.62	49.62	75.82
55	"Mark"	"Taylor"	37.62	49.62	75.82
27	"Patrick"	"Gray"	37.62	49.62	75.82
2	"Leonie"	"Köhler"	37.62	49.62	75.82
16	"Frank"	"Harris"	37.62	49.62	75.82
11	"Alexandre"	"Rocha"	37.62	49.62	75.82
59	"Puja"	"Srivastava"	36.64	49.62	73.84
```


### Para cada factura, calcula la diferencia en el gasto total entre ella y la factura anterior.
```sql
WITH facturas_ordenadas AS (
    SELECT
        invoice_id,
        customer_id,
        invoice_date,
        total,
        ROW_NUMBER() OVER (ORDER BY invoice_date) AS fila
    FROM
        invoice
)
SELECT
    f1.invoice_id,
    f1.customer_id,
    f1.invoice_date,
    f1.total,
    f2.total AS factura_anterior_total,
    f1.total - f2.total AS diferencia_con_anterior
FROM
    facturas_ordenadas f1
LEFT JOIN
    facturas_ordenadas f2
    ON f1.fila = f2.fila + 1
ORDER BY
    f1.invoice_date;

#################
RESULT:
#################

"invoice_id"	"customer_id"	"invoice_date"	"total"	"factura_anterior_total"	"diferencia_con_anterior"
1	2	"2009-01-01 00:00:00"	1.98		
2	4	"2009-01-02 00:00:00"	3.96	1.98	1.98
3	8	"2009-01-03 00:00:00"	5.94	3.96	1.98
4	14	"2009-01-06 00:00:00"	8.91	5.94	2.97
5	23	"2009-01-11 00:00:00"	13.86	8.91	4.95
6	37	"2009-01-19 00:00:00"	0.99	13.86	-12.87
7	38	"2009-02-01 00:00:00"	1.98	0.99	0.99
8	40	"2009-02-01 00:00:00"	1.98	1.98	0.00
9	42	"2009-02-02 00:00:00"	3.96	1.98	1.98
10	46	"2009-02-03 00:00:00"	5.94	3.96	1.98
11	52	"2009-02-06 00:00:00"	8.91	5.94	2.97
12	2	"2009-02-11 00:00:00"	13.86	8.91	4.95
13	16	"2009-02-19 00:00:00"	0.99	13.86	-12.87
14	17	"2009-03-04 00:00:00"	1.98	0.99	0.99
15	19	"2009-03-04 00:00:00"	1.98	1.98	0.00
16	21	"2009-03-05 00:00:00"	3.96	1.98	1.98
17	25	"2009-03-06 00:00:00"	5.94	3.96	1.98
18	31	"2009-03-09 00:00:00"	8.91	5.94	2.97
19	40	"2009-03-14 00:00:00"	13.86	8.91	4.95
20	54	"2009-03-22 00:00:00"	0.99	13.86	-12.87
21	55	"2009-04-04 00:00:00"	1.98	0.99	0.99
22	57	"2009-04-04 00:00:00"	1.98	1.98	0.00
23	59	"2009-04-05 00:00:00"	3.96	1.98	1.98
24	4	"2009-04-06 00:00:00"	5.94	3.96	1.98
25	10	"2009-04-09 00:00:00"	8.91	5.94	2.97
26	19	"2009-04-14 00:00:00"	13.86	8.91	4.95
27	33	"2009-04-22 00:00:00"	0.99	13.86	-12.87
28	34	"2009-05-05 00:00:00"	1.98	0.99	0.99
29	36	"2009-05-05 00:00:00"	1.98	1.98	0.00
30	38	"2009-05-06 00:00:00"	3.96	1.98	1.98
31	42	"2009-05-07 00:00:00"	5.94	3.96	1.98
32	48	"2009-05-10 00:00:00"	8.91	5.94	2.97
33	57	"2009-05-15 00:00:00"	13.86	8.91	4.95
34	12	"2009-05-23 00:00:00"	0.99	13.86	-12.87
35	13	"2009-06-05 00:00:00"	1.98	0.99	0.99
36	15	"2009-06-05 00:00:00"	1.98	1.98	0.00
37	17	"2009-06-06 00:00:00"	3.96	1.98	1.98
38	21	"2009-06-07 00:00:00"	5.94	3.96	1.98
39	27	"2009-06-10 00:00:00"	8.91	5.94	2.97
40	36	"2009-06-15 00:00:00"	13.86	8.91	4.95
41	50	"2009-06-23 00:00:00"	0.99	13.86	-12.87
42	51	"2009-07-06 00:00:00"	1.98	0.99	0.99
43	53	"2009-07-06 00:00:00"	1.98	1.98	0.00
44	55	"2009-07-07 00:00:00"	3.96	1.98	1.98
45	59	"2009-07-08 00:00:00"	5.94	3.96	1.98
46	6	"2009-07-11 00:00:00"	8.91	5.94	2.97
47	15	"2009-07-16 00:00:00"	13.86	8.91	4.95
48	29	"2009-07-24 00:00:00"	0.99	13.86	-12.87
49	30	"2009-08-06 00:00:00"	1.98	0.99	0.99
50	32	"2009-08-06 00:00:00"	1.98	1.98	0.00
51	34	"2009-08-07 00:00:00"	3.96	1.98	1.98
52	38	"2009-08-08 00:00:00"	5.94	3.96	1.98
53	44	"2009-08-11 00:00:00"	8.91	5.94	2.97
54	53	"2009-08-16 00:00:00"	13.86	8.91	4.95
55	8	"2009-08-24 00:00:00"	0.99	13.86	-12.87
56	9	"2009-09-06 00:00:00"	1.98	0.99	0.99
57	11	"2009-09-06 00:00:00"	1.98	1.98	0.00
58	13	"2009-09-07 00:00:00"	3.96	1.98	1.98
59	17	"2009-09-08 00:00:00"	5.94	3.96	1.98
60	23	"2009-09-11 00:00:00"	8.91	5.94	2.97
61	32	"2009-09-16 00:00:00"	13.86	8.91	4.95
62	46	"2009-09-24 00:00:00"	0.99	13.86	-12.87
63	47	"2009-10-07 00:00:00"	1.98	0.99	0.99
64	49	"2009-10-07 00:00:00"	1.98	1.98	0.00
65	51	"2009-10-08 00:00:00"	3.96	1.98	1.98
66	55	"2009-10-09 00:00:00"	5.94	3.96	1.98
67	2	"2009-10-12 00:00:00"	8.91	5.94	2.97
68	11	"2009-10-17 00:00:00"	13.86	8.91	4.95
69	25	"2009-10-25 00:00:00"	0.99	13.86	-12.87
70	26	"2009-11-07 00:00:00"	1.98	0.99	0.99
71	28	"2009-11-07 00:00:00"	1.98	1.98	0.00
72	30	"2009-11-08 00:00:00"	3.96	1.98	1.98
73	34	"2009-11-09 00:00:00"	5.94	3.96	1.98
74	40	"2009-11-12 00:00:00"	8.91	5.94	2.97
75	49	"2009-11-17 00:00:00"	13.86	8.91	4.95
76	4	"2009-11-25 00:00:00"	0.99	13.86	-12.87
77	5	"2009-12-08 00:00:00"	1.98	0.99	0.99
78	7	"2009-12-08 00:00:00"	1.98	1.98	0.00
79	9	"2009-12-09 00:00:00"	3.96	1.98	1.98
80	13	"2009-12-10 00:00:00"	5.94	3.96	1.98
81	19	"2009-12-13 00:00:00"	8.91	5.94	2.97
82	28	"2009-12-18 00:00:00"	13.86	8.91	4.95
83	42	"2009-12-26 00:00:00"	0.99	13.86	-12.87
84	43	"2010-01-08 00:00:00"	1.98	0.99	0.99
85	45	"2010-01-08 00:00:00"	1.98	1.98	0.00
86	47	"2010-01-09 00:00:00"	3.96	1.98	1.98
87	51	"2010-01-10 00:00:00"	6.94	3.96	2.98
88	57	"2010-01-13 00:00:00"	17.91	6.94	10.97
89	7	"2010-01-18 00:00:00"	18.86	17.91	0.95
90	21	"2010-01-26 00:00:00"	0.99	18.86	-17.87
91	22	"2010-02-08 00:00:00"	1.98	0.99	0.99
92	24	"2010-02-08 00:00:00"	1.98	1.98	0.00
93	26	"2010-02-09 00:00:00"	3.96	1.98	1.98
94	30	"2010-02-10 00:00:00"	5.94	3.96	1.98
95	36	"2010-02-13 00:00:00"	8.91	5.94	2.97
96	45	"2010-02-18 00:00:00"	21.86	8.91	12.95
97	59	"2010-02-26 00:00:00"	1.99	21.86	-19.87
98	1	"2010-03-11 00:00:00"	3.98	1.99	1.99
99	3	"2010-03-11 00:00:00"	3.98	3.98	0.00
100	5	"2010-03-12 00:00:00"	3.96	3.98	-0.02
101	9	"2010-03-13 00:00:00"	5.94	3.96	1.98
102	15	"2010-03-16 00:00:00"	9.91	5.94	3.97
103	24	"2010-03-21 00:00:00"	15.86	9.91	5.95
104	38	"2010-03-29 00:00:00"	0.99	15.86	-14.87
105	39	"2010-04-11 00:00:00"	1.98	0.99	0.99
106	41	"2010-04-11 00:00:00"	1.98	1.98	0.00
107	43	"2010-04-12 00:00:00"	3.96	1.98	1.98
108	47	"2010-04-13 00:00:00"	5.94	3.96	1.98
109	53	"2010-04-16 00:00:00"	8.91	5.94	2.97
110	3	"2010-04-21 00:00:00"	13.86	8.91	4.95
111	17	"2010-04-29 00:00:00"	0.99	13.86	-12.87
112	18	"2010-05-12 00:00:00"	1.98	0.99	0.99
113	20	"2010-05-12 00:00:00"	1.98	1.98	0.00
114	22	"2010-05-13 00:00:00"	3.96	1.98	1.98
115	26	"2010-05-14 00:00:00"	5.94	3.96	1.98
116	32	"2010-05-17 00:00:00"	8.91	5.94	2.97
117	41	"2010-05-22 00:00:00"	13.86	8.91	4.95
118	55	"2010-05-30 00:00:00"	0.99	13.86	-12.87
119	56	"2010-06-12 00:00:00"	1.98	0.99	0.99
120	58	"2010-06-12 00:00:00"	1.98	1.98	0.00
121	1	"2010-06-13 00:00:00"	3.96	1.98	1.98
122	5	"2010-06-14 00:00:00"	5.94	3.96	1.98
123	11	"2010-06-17 00:00:00"	8.91	5.94	2.97
124	20	"2010-06-22 00:00:00"	13.86	8.91	4.95
125	34	"2010-06-30 00:00:00"	0.99	13.86	-12.87
126	35	"2010-07-13 00:00:00"	1.98	0.99	0.99
127	37	"2010-07-13 00:00:00"	1.98	1.98	0.00
128	39	"2010-07-14 00:00:00"	3.96	1.98	1.98
129	43	"2010-07-15 00:00:00"	5.94	3.96	1.98
130	49	"2010-07-18 00:00:00"	8.91	5.94	2.97
131	58	"2010-07-23 00:00:00"	13.86	8.91	4.95
132	13	"2010-07-31 00:00:00"	0.99	13.86	-12.87
133	14	"2010-08-13 00:00:00"	1.98	0.99	0.99
134	16	"2010-08-13 00:00:00"	1.98	1.98	0.00
135	18	"2010-08-14 00:00:00"	3.96	1.98	1.98
136	22	"2010-08-15 00:00:00"	5.94	3.96	1.98
137	28	"2010-08-18 00:00:00"	8.91	5.94	2.97
138	37	"2010-08-23 00:00:00"	13.86	8.91	4.95
139	51	"2010-08-31 00:00:00"	0.99	13.86	-12.87
140	52	"2010-09-13 00:00:00"	1.98	0.99	0.99
141	54	"2010-09-13 00:00:00"	1.98	1.98	0.00
142	56	"2010-09-14 00:00:00"	3.96	1.98	1.98
143	1	"2010-09-15 00:00:00"	5.94	3.96	1.98
144	7	"2010-09-18 00:00:00"	8.91	5.94	2.97
145	16	"2010-09-23 00:00:00"	13.86	8.91	4.95
146	30	"2010-10-01 00:00:00"	0.99	13.86	-12.87
147	31	"2010-10-14 00:00:00"	1.98	0.99	0.99
148	33	"2010-10-14 00:00:00"	1.98	1.98	0.00
149	35	"2010-10-15 00:00:00"	3.96	1.98	1.98
150	39	"2010-10-16 00:00:00"	5.94	3.96	1.98
151	45	"2010-10-19 00:00:00"	8.91	5.94	2.97
152	54	"2010-10-24 00:00:00"	13.86	8.91	4.95
153	9	"2010-11-01 00:00:00"	0.99	13.86	-12.87
154	10	"2010-11-14 00:00:00"	1.98	0.99	0.99
155	12	"2010-11-14 00:00:00"	1.98	1.98	0.00
156	14	"2010-11-15 00:00:00"	3.96	1.98	1.98
157	18	"2010-11-16 00:00:00"	5.94	3.96	1.98
158	24	"2010-11-19 00:00:00"	8.91	5.94	2.97
159	33	"2010-11-24 00:00:00"	13.86	8.91	4.95
160	47	"2010-12-02 00:00:00"	0.99	13.86	-12.87
161	48	"2010-12-15 00:00:00"	1.98	0.99	0.99
162	50	"2010-12-15 00:00:00"	1.98	1.98	0.00
163	52	"2010-12-16 00:00:00"	3.96	1.98	1.98
164	56	"2010-12-17 00:00:00"	5.94	3.96	1.98
165	3	"2010-12-20 00:00:00"	8.91	5.94	2.97
166	12	"2010-12-25 00:00:00"	13.86	8.91	4.95
167	26	"2011-01-02 00:00:00"	0.99	13.86	-12.87
168	27	"2011-01-15 00:00:00"	1.98	0.99	0.99
169	29	"2011-01-15 00:00:00"	1.98	1.98	0.00
170	31	"2011-01-16 00:00:00"	3.96	1.98	1.98
171	35	"2011-01-17 00:00:00"	5.94	3.96	1.98
172	41	"2011-01-20 00:00:00"	8.91	5.94	2.97
173	50	"2011-01-25 00:00:00"	13.86	8.91	4.95
174	5	"2011-02-02 00:00:00"	0.99	13.86	-12.87
175	6	"2011-02-15 00:00:00"	1.98	0.99	0.99
176	8	"2011-02-15 00:00:00"	1.98	1.98	0.00
177	10	"2011-02-16 00:00:00"	3.96	1.98	1.98
178	14	"2011-02-17 00:00:00"	5.94	3.96	1.98
179	20	"2011-02-20 00:00:00"	8.91	5.94	2.97
180	29	"2011-02-25 00:00:00"	13.86	8.91	4.95
181	43	"2011-03-05 00:00:00"	0.99	13.86	-12.87
182	44	"2011-03-18 00:00:00"	1.98	0.99	0.99
183	46	"2011-03-18 00:00:00"	1.98	1.98	0.00
184	48	"2011-03-19 00:00:00"	3.96	1.98	1.98
185	52	"2011-03-20 00:00:00"	5.94	3.96	1.98
186	58	"2011-03-23 00:00:00"	8.91	5.94	2.97
187	8	"2011-03-28 00:00:00"	13.86	8.91	4.95
188	22	"2011-04-05 00:00:00"	0.99	13.86	-12.87
189	23	"2011-04-18 00:00:00"	1.98	0.99	0.99
190	25	"2011-04-18 00:00:00"	1.98	1.98	0.00
191	27	"2011-04-19 00:00:00"	3.96	1.98	1.98
192	31	"2011-04-20 00:00:00"	5.94	3.96	1.98
193	37	"2011-04-23 00:00:00"	14.91	5.94	8.97
194	46	"2011-04-28 00:00:00"	21.86	14.91	6.95
195	1	"2011-05-06 00:00:00"	0.99	21.86	-20.87
196	2	"2011-05-19 00:00:00"	1.98	0.99	0.99
197	4	"2011-05-19 00:00:00"	1.98	1.98	0.00
198	6	"2011-05-20 00:00:00"	3.96	1.98	1.98
199	10	"2011-05-21 00:00:00"	5.94	3.96	1.98
200	16	"2011-05-24 00:00:00"	8.91	5.94	2.97
201	25	"2011-05-29 00:00:00"	18.86	8.91	9.95
202	39	"2011-06-06 00:00:00"	1.99	18.86	-16.87
203	40	"2011-06-19 00:00:00"	2.98	1.99	0.99
204	42	"2011-06-19 00:00:00"	3.98	2.98	1.00
205	44	"2011-06-20 00:00:00"	7.96	3.98	3.98
206	48	"2011-06-21 00:00:00"	8.94	7.96	0.98
207	54	"2011-06-24 00:00:00"	8.91	8.94	-0.03
208	4	"2011-06-29 00:00:00"	15.86	8.91	6.95
209	18	"2011-07-07 00:00:00"	0.99	15.86	-14.87
210	19	"2011-07-20 00:00:00"	1.98	0.99	0.99
211	21	"2011-07-20 00:00:00"	1.98	1.98	0.00
212	23	"2011-07-21 00:00:00"	3.96	1.98	1.98
213	27	"2011-07-22 00:00:00"	5.94	3.96	1.98
214	33	"2011-07-25 00:00:00"	8.91	5.94	2.97
215	42	"2011-07-30 00:00:00"	13.86	8.91	4.95
216	56	"2011-08-07 00:00:00"	0.99	13.86	-12.87
217	57	"2011-08-20 00:00:00"	1.98	0.99	0.99
218	59	"2011-08-20 00:00:00"	1.98	1.98	0.00
219	2	"2011-08-21 00:00:00"	3.96	1.98	1.98
220	6	"2011-08-22 00:00:00"	5.94	3.96	1.98
221	12	"2011-08-25 00:00:00"	8.91	5.94	2.97
222	21	"2011-08-30 00:00:00"	13.86	8.91	4.95
223	35	"2011-09-07 00:00:00"	0.99	13.86	-12.87
224	36	"2011-09-20 00:00:00"	1.98	0.99	0.99
225	38	"2011-09-20 00:00:00"	1.98	1.98	0.00
226	40	"2011-09-21 00:00:00"	3.96	1.98	1.98
227	44	"2011-09-22 00:00:00"	5.94	3.96	1.98
228	50	"2011-09-25 00:00:00"	8.91	5.94	2.97
229	59	"2011-09-30 00:00:00"	13.86	8.91	4.95
230	14	"2011-10-08 00:00:00"	0.99	13.86	-12.87
231	15	"2011-10-21 00:00:00"	1.98	0.99	0.99
232	17	"2011-10-21 00:00:00"	1.98	1.98	0.00
233	19	"2011-10-22 00:00:00"	3.96	1.98	1.98
234	23	"2011-10-23 00:00:00"	5.94	3.96	1.98
235	29	"2011-10-26 00:00:00"	8.91	5.94	2.97
236	38	"2011-10-31 00:00:00"	13.86	8.91	4.95
237	52	"2011-11-08 00:00:00"	0.99	13.86	-12.87
238	53	"2011-11-21 00:00:00"	1.98	0.99	0.99
239	55	"2011-11-21 00:00:00"	1.98	1.98	0.00
240	57	"2011-11-22 00:00:00"	3.96	1.98	1.98
241	2	"2011-11-23 00:00:00"	5.94	3.96	1.98
242	8	"2011-11-26 00:00:00"	8.91	5.94	2.97
243	17	"2011-12-01 00:00:00"	13.86	8.91	4.95
244	31	"2011-12-09 00:00:00"	0.99	13.86	-12.87
245	32	"2011-12-22 00:00:00"	1.98	0.99	0.99
246	34	"2011-12-22 00:00:00"	1.98	1.98	0.00
247	36	"2011-12-23 00:00:00"	3.96	1.98	1.98
248	40	"2011-12-24 00:00:00"	5.94	3.96	1.98
249	46	"2011-12-27 00:00:00"	8.91	5.94	2.97
250	55	"2012-01-01 00:00:00"	13.86	8.91	4.95
251	10	"2012-01-09 00:00:00"	0.99	13.86	-12.87
252	11	"2012-01-22 00:00:00"	1.98	0.99	0.99
253	13	"2012-01-22 00:00:00"	1.98	1.98	0.00
254	15	"2012-01-23 00:00:00"	3.96	1.98	1.98
255	19	"2012-01-24 00:00:00"	5.94	3.96	1.98
256	25	"2012-01-27 00:00:00"	8.91	5.94	2.97
257	34	"2012-02-01 00:00:00"	13.86	8.91	4.95
258	48	"2012-02-09 00:00:00"	0.99	13.86	-12.87
259	49	"2012-02-22 00:00:00"	1.98	0.99	0.99
260	51	"2012-02-22 00:00:00"	1.98	1.98	0.00
261	53	"2012-02-23 00:00:00"	3.96	1.98	1.98
262	57	"2012-02-24 00:00:00"	5.94	3.96	1.98
263	4	"2012-02-27 00:00:00"	8.91	5.94	2.97
264	13	"2012-03-03 00:00:00"	13.86	8.91	4.95
265	27	"2012-03-11 00:00:00"	0.99	13.86	-12.87
266	28	"2012-03-24 00:00:00"	1.98	0.99	0.99
267	30	"2012-03-24 00:00:00"	1.98	1.98	0.00
268	32	"2012-03-25 00:00:00"	3.96	1.98	1.98
269	36	"2012-03-26 00:00:00"	5.94	3.96	1.98
270	42	"2012-03-29 00:00:00"	8.91	5.94	2.97
271	51	"2012-04-03 00:00:00"	13.86	8.91	4.95
272	6	"2012-04-11 00:00:00"	0.99	13.86	-12.87
273	7	"2012-04-24 00:00:00"	1.98	0.99	0.99
274	9	"2012-04-24 00:00:00"	1.98	1.98	0.00
275	11	"2012-04-25 00:00:00"	3.96	1.98	1.98
276	15	"2012-04-26 00:00:00"	5.94	3.96	1.98
277	21	"2012-04-29 00:00:00"	8.91	5.94	2.97
278	30	"2012-05-04 00:00:00"	13.86	8.91	4.95
279	44	"2012-05-12 00:00:00"	0.99	13.86	-12.87
280	45	"2012-05-25 00:00:00"	1.98	0.99	0.99
281	47	"2012-05-25 00:00:00"	1.98	1.98	0.00
282	49	"2012-05-26 00:00:00"	3.96	1.98	1.98
283	53	"2012-05-27 00:00:00"	5.94	3.96	1.98
284	59	"2012-05-30 00:00:00"	8.91	5.94	2.97
285	9	"2012-06-04 00:00:00"	13.86	8.91	4.95
286	23	"2012-06-12 00:00:00"	0.99	13.86	-12.87
287	24	"2012-06-25 00:00:00"	1.98	0.99	0.99
288	26	"2012-06-25 00:00:00"	1.98	1.98	0.00
289	28	"2012-06-26 00:00:00"	3.96	1.98	1.98
290	32	"2012-06-27 00:00:00"	5.94	3.96	1.98
291	38	"2012-06-30 00:00:00"	8.91	5.94	2.97
292	47	"2012-07-05 00:00:00"	13.86	8.91	4.95
293	2	"2012-07-13 00:00:00"	0.99	13.86	-12.87
294	3	"2012-07-26 00:00:00"	1.98	0.99	0.99
295	5	"2012-07-26 00:00:00"	1.98	1.98	0.00
296	7	"2012-07-27 00:00:00"	3.96	1.98	1.98
297	11	"2012-07-28 00:00:00"	5.94	3.96	1.98
298	17	"2012-07-31 00:00:00"	10.91	5.94	4.97
299	26	"2012-08-05 00:00:00"	23.86	10.91	12.95
300	40	"2012-08-13 00:00:00"	0.99	23.86	-22.87
301	41	"2012-08-26 00:00:00"	1.98	0.99	0.99
302	43	"2012-08-26 00:00:00"	1.98	1.98	0.00
303	45	"2012-08-27 00:00:00"	3.96	1.98	1.98
304	49	"2012-08-28 00:00:00"	5.94	3.96	1.98
305	55	"2012-08-31 00:00:00"	8.91	5.94	2.97
306	5	"2012-09-05 00:00:00"	16.86	8.91	7.95
307	19	"2012-09-13 00:00:00"	1.99	16.86	-14.87
308	20	"2012-09-26 00:00:00"	3.98	1.99	1.99
309	22	"2012-09-26 00:00:00"	3.98	3.98	0.00
310	24	"2012-09-27 00:00:00"	7.96	3.98	3.98
311	28	"2012-09-28 00:00:00"	11.94	7.96	3.98
312	34	"2012-10-01 00:00:00"	10.91	11.94	-1.03
313	43	"2012-10-06 00:00:00"	16.86	10.91	5.95
314	57	"2012-10-14 00:00:00"	0.99	16.86	-15.87
315	58	"2012-10-27 00:00:00"	1.98	0.99	0.99
316	1	"2012-10-27 00:00:00"	1.98	1.98	0.00
317	3	"2012-10-28 00:00:00"	3.96	1.98	1.98
318	7	"2012-10-29 00:00:00"	5.94	3.96	1.98
319	13	"2012-11-01 00:00:00"	8.91	5.94	2.97
320	22	"2012-11-06 00:00:00"	13.86	8.91	4.95
321	36	"2012-11-14 00:00:00"	0.99	13.86	-12.87
322	37	"2012-11-27 00:00:00"	1.98	0.99	0.99
323	39	"2012-11-27 00:00:00"	1.98	1.98	0.00
324	41	"2012-11-28 00:00:00"	3.96	1.98	1.98
325	45	"2012-11-29 00:00:00"	5.94	3.96	1.98
326	51	"2012-12-02 00:00:00"	8.91	5.94	2.97
327	1	"2012-12-07 00:00:00"	13.86	8.91	4.95
328	15	"2012-12-15 00:00:00"	0.99	13.86	-12.87
329	16	"2012-12-28 00:00:00"	1.98	0.99	0.99
330	18	"2012-12-28 00:00:00"	1.98	1.98	0.00
331	20	"2012-12-29 00:00:00"	3.96	1.98	1.98
332	24	"2012-12-30 00:00:00"	5.94	3.96	1.98
333	30	"2013-01-02 00:00:00"	8.91	5.94	2.97
334	39	"2013-01-07 00:00:00"	13.86	8.91	4.95
335	53	"2013-01-15 00:00:00"	0.99	13.86	-12.87
336	54	"2013-01-28 00:00:00"	1.98	0.99	0.99
337	56	"2013-01-28 00:00:00"	1.98	1.98	0.00
338	58	"2013-01-29 00:00:00"	3.96	1.98	1.98
339	3	"2013-01-30 00:00:00"	5.94	3.96	1.98
340	9	"2013-02-02 00:00:00"	8.91	5.94	2.97
341	18	"2013-02-07 00:00:00"	13.86	8.91	4.95
342	32	"2013-02-15 00:00:00"	0.99	13.86	-12.87
343	33	"2013-02-28 00:00:00"	1.98	0.99	0.99
344	35	"2013-02-28 00:00:00"	1.98	1.98	0.00
345	37	"2013-03-01 00:00:00"	3.96	1.98	1.98
346	41	"2013-03-02 00:00:00"	5.94	3.96	1.98
347	47	"2013-03-05 00:00:00"	8.91	5.94	2.97
348	56	"2013-03-10 00:00:00"	13.86	8.91	4.95
349	11	"2013-03-18 00:00:00"	0.99	13.86	-12.87
350	12	"2013-03-31 00:00:00"	1.98	0.99	0.99
351	14	"2013-03-31 00:00:00"	1.98	1.98	0.00
352	16	"2013-04-01 00:00:00"	3.96	1.98	1.98
353	20	"2013-04-02 00:00:00"	5.94	3.96	1.98
354	26	"2013-04-05 00:00:00"	8.91	5.94	2.97
355	35	"2013-04-10 00:00:00"	13.86	8.91	4.95
356	49	"2013-04-18 00:00:00"	0.99	13.86	-12.87
357	50	"2013-05-01 00:00:00"	1.98	0.99	0.99
358	52	"2013-05-01 00:00:00"	1.98	1.98	0.00
359	54	"2013-05-02 00:00:00"	3.96	1.98	1.98
360	58	"2013-05-03 00:00:00"	5.94	3.96	1.98
361	5	"2013-05-06 00:00:00"	8.91	5.94	2.97
362	14	"2013-05-11 00:00:00"	13.86	8.91	4.95
363	28	"2013-05-19 00:00:00"	0.99	13.86	-12.87
364	29	"2013-06-01 00:00:00"	1.98	0.99	0.99
365	31	"2013-06-01 00:00:00"	1.98	1.98	0.00
366	33	"2013-06-02 00:00:00"	3.96	1.98	1.98
367	37	"2013-06-03 00:00:00"	5.94	3.96	1.98
368	43	"2013-06-06 00:00:00"	8.91	5.94	2.97
369	52	"2013-06-11 00:00:00"	13.86	8.91	4.95
370	7	"2013-06-19 00:00:00"	0.99	13.86	-12.87
371	8	"2013-07-02 00:00:00"	1.98	0.99	0.99
372	10	"2013-07-02 00:00:00"	1.98	1.98	0.00
373	12	"2013-07-03 00:00:00"	3.96	1.98	1.98
374	16	"2013-07-04 00:00:00"	5.94	3.96	1.98
375	22	"2013-07-07 00:00:00"	8.91	5.94	2.97
376	31	"2013-07-12 00:00:00"	13.86	8.91	4.95
377	45	"2013-07-20 00:00:00"	0.99	13.86	-12.87
378	46	"2013-08-02 00:00:00"	1.98	0.99	0.99
379	48	"2013-08-02 00:00:00"	1.98	1.98	0.00
380	50	"2013-08-03 00:00:00"	3.96	1.98	1.98
381	54	"2013-08-04 00:00:00"	5.94	3.96	1.98
382	1	"2013-08-07 00:00:00"	8.91	5.94	2.97
383	10	"2013-08-12 00:00:00"	13.86	8.91	4.95
384	24	"2013-08-20 00:00:00"	0.99	13.86	-12.87
385	25	"2013-09-02 00:00:00"	1.98	0.99	0.99
386	27	"2013-09-02 00:00:00"	1.98	1.98	0.00
387	29	"2013-09-03 00:00:00"	3.96	1.98	1.98
388	33	"2013-09-04 00:00:00"	5.94	3.96	1.98
389	39	"2013-09-07 00:00:00"	8.91	5.94	2.97
390	48	"2013-09-12 00:00:00"	13.86	8.91	4.95
391	3	"2013-09-20 00:00:00"	0.99	13.86	-12.87
392	4	"2013-10-03 00:00:00"	1.98	0.99	0.99
393	6	"2013-10-03 00:00:00"	1.98	1.98	0.00
394	8	"2013-10-04 00:00:00"	3.96	1.98	1.98
395	12	"2013-10-05 00:00:00"	5.94	3.96	1.98
396	18	"2013-10-08 00:00:00"	8.91	5.94	2.97
397	27	"2013-10-13 00:00:00"	13.86	8.91	4.95
398	41	"2013-10-21 00:00:00"	0.99	13.86	-12.87
399	42	"2013-11-03 00:00:00"	1.98	0.99	0.99
400	44	"2013-11-03 00:00:00"	1.98	1.98	0.00
401	46	"2013-11-04 00:00:00"	3.96	1.98	1.98
402	50	"2013-11-05 00:00:00"	5.94	3.96	1.98
403	56	"2013-11-08 00:00:00"	8.91	5.94	2.97
404	6	"2013-11-13 00:00:00"	25.86	8.91	16.95
405	20	"2013-11-21 00:00:00"	0.99	25.86	-24.87
406	21	"2013-12-04 00:00:00"	1.98	0.99	0.99
407	23	"2013-12-04 00:00:00"	1.98	1.98	0.00
408	25	"2013-12-05 00:00:00"	3.96	1.98	1.98
409	29	"2013-12-06 00:00:00"	5.94	3.96	1.98
410	35	"2013-12-09 00:00:00"	8.91	5.94	2.97
411	44	"2013-12-14 00:00:00"	13.86	8.91	4.95
412	58	"2013-12-22 00:00:00"	1.99	13.86	-11.87
```

### Para cada factura, calcula la diferencia en el gasto total entre ella y la próxima factura.

```sql
WITH facturas_ordenadas AS (
    SELECT
        invoice_id,
        customer_id,
        invoice_date,
        total,
        ROW_NUMBER() OVER (ORDER BY invoice_date) AS fila
    FROM
        invoice
)
SELECT
    f1.invoice_id,
    f1.customer_id,
    f1.invoice_date,
    f1.total,
    f2.total AS proxima_factura_total,
    f1.total - f2.total AS diferencia_con_proxima
FROM
    facturas_ordenadas f1
LEFT JOIN
    facturas_ordenadas f2
    ON f1.fila = f2.fila - 1
ORDER BY
    f1.invoice_date;

#################
RESULT:
#################

"invoice_id"	"customer_id"	"invoice_date"	"total"	"proxima_factura_total"	"diferencia_con_proxima"
1	2	"2009-01-01 00:00:00"	1.98	3.96	-1.98
2	4	"2009-01-02 00:00:00"	3.96	5.94	-1.98
3	8	"2009-01-03 00:00:00"	5.94	8.91	-2.97
4	14	"2009-01-06 00:00:00"	8.91	13.86	-4.95
5	23	"2009-01-11 00:00:00"	13.86	0.99	12.87
6	37	"2009-01-19 00:00:00"	0.99	1.98	-0.99
7	38	"2009-02-01 00:00:00"	1.98	1.98	0.00
8	40	"2009-02-01 00:00:00"	1.98	3.96	-1.98
9	42	"2009-02-02 00:00:00"	3.96	5.94	-1.98
10	46	"2009-02-03 00:00:00"	5.94	8.91	-2.97
11	52	"2009-02-06 00:00:00"	8.91	13.86	-4.95
12	2	"2009-02-11 00:00:00"	13.86	0.99	12.87
13	16	"2009-02-19 00:00:00"	0.99	1.98	-0.99
14	17	"2009-03-04 00:00:00"	1.98	1.98	0.00
15	19	"2009-03-04 00:00:00"	1.98	3.96	-1.98
16	21	"2009-03-05 00:00:00"	3.96	5.94	-1.98
17	25	"2009-03-06 00:00:00"	5.94	8.91	-2.97
18	31	"2009-03-09 00:00:00"	8.91	13.86	-4.95
19	40	"2009-03-14 00:00:00"	13.86	0.99	12.87
20	54	"2009-03-22 00:00:00"	0.99	1.98	-0.99
21	55	"2009-04-04 00:00:00"	1.98	1.98	0.00
22	57	"2009-04-04 00:00:00"	1.98	3.96	-1.98
23	59	"2009-04-05 00:00:00"	3.96	5.94	-1.98
24	4	"2009-04-06 00:00:00"	5.94	8.91	-2.97
25	10	"2009-04-09 00:00:00"	8.91	13.86	-4.95
26	19	"2009-04-14 00:00:00"	13.86	0.99	12.87
27	33	"2009-04-22 00:00:00"	0.99	1.98	-0.99
28	34	"2009-05-05 00:00:00"	1.98	1.98	0.00
29	36	"2009-05-05 00:00:00"	1.98	3.96	-1.98
30	38	"2009-05-06 00:00:00"	3.96	5.94	-1.98
31	42	"2009-05-07 00:00:00"	5.94	8.91	-2.97
32	48	"2009-05-10 00:00:00"	8.91	13.86	-4.95
33	57	"2009-05-15 00:00:00"	13.86	0.99	12.87
34	12	"2009-05-23 00:00:00"	0.99	1.98	-0.99
35	13	"2009-06-05 00:00:00"	1.98	1.98	0.00
36	15	"2009-06-05 00:00:00"	1.98	3.96	-1.98
37	17	"2009-06-06 00:00:00"	3.96	5.94	-1.98
38	21	"2009-06-07 00:00:00"	5.94	8.91	-2.97
39	27	"2009-06-10 00:00:00"	8.91	13.86	-4.95
40	36	"2009-06-15 00:00:00"	13.86	0.99	12.87
41	50	"2009-06-23 00:00:00"	0.99	1.98	-0.99
42	51	"2009-07-06 00:00:00"	1.98	1.98	0.00
43	53	"2009-07-06 00:00:00"	1.98	3.96	-1.98
44	55	"2009-07-07 00:00:00"	3.96	5.94	-1.98
45	59	"2009-07-08 00:00:00"	5.94	8.91	-2.97
46	6	"2009-07-11 00:00:00"	8.91	13.86	-4.95
47	15	"2009-07-16 00:00:00"	13.86	0.99	12.87
48	29	"2009-07-24 00:00:00"	0.99	1.98	-0.99
49	30	"2009-08-06 00:00:00"	1.98	1.98	0.00
50	32	"2009-08-06 00:00:00"	1.98	3.96	-1.98
51	34	"2009-08-07 00:00:00"	3.96	5.94	-1.98
52	38	"2009-08-08 00:00:00"	5.94	8.91	-2.97
53	44	"2009-08-11 00:00:00"	8.91	13.86	-4.95
54	53	"2009-08-16 00:00:00"	13.86	0.99	12.87
55	8	"2009-08-24 00:00:00"	0.99	1.98	-0.99
56	9	"2009-09-06 00:00:00"	1.98	1.98	0.00
57	11	"2009-09-06 00:00:00"	1.98	3.96	-1.98
58	13	"2009-09-07 00:00:00"	3.96	5.94	-1.98
59	17	"2009-09-08 00:00:00"	5.94	8.91	-2.97
60	23	"2009-09-11 00:00:00"	8.91	13.86	-4.95
61	32	"2009-09-16 00:00:00"	13.86	0.99	12.87
62	46	"2009-09-24 00:00:00"	0.99	1.98	-0.99
63	47	"2009-10-07 00:00:00"	1.98	1.98	0.00
64	49	"2009-10-07 00:00:00"	1.98	3.96	-1.98
65	51	"2009-10-08 00:00:00"	3.96	5.94	-1.98
66	55	"2009-10-09 00:00:00"	5.94	8.91	-2.97
67	2	"2009-10-12 00:00:00"	8.91	13.86	-4.95
68	11	"2009-10-17 00:00:00"	13.86	0.99	12.87
69	25	"2009-10-25 00:00:00"	0.99	1.98	-0.99
70	26	"2009-11-07 00:00:00"	1.98	1.98	0.00
71	28	"2009-11-07 00:00:00"	1.98	3.96	-1.98
72	30	"2009-11-08 00:00:00"	3.96	5.94	-1.98
73	34	"2009-11-09 00:00:00"	5.94	8.91	-2.97
74	40	"2009-11-12 00:00:00"	8.91	13.86	-4.95
75	49	"2009-11-17 00:00:00"	13.86	0.99	12.87
76	4	"2009-11-25 00:00:00"	0.99	1.98	-0.99
77	5	"2009-12-08 00:00:00"	1.98	1.98	0.00
78	7	"2009-12-08 00:00:00"	1.98	3.96	-1.98
79	9	"2009-12-09 00:00:00"	3.96	5.94	-1.98
80	13	"2009-12-10 00:00:00"	5.94	8.91	-2.97
81	19	"2009-12-13 00:00:00"	8.91	13.86	-4.95
82	28	"2009-12-18 00:00:00"	13.86	0.99	12.87
83	42	"2009-12-26 00:00:00"	0.99	1.98	-0.99
84	43	"2010-01-08 00:00:00"	1.98	1.98	0.00
85	45	"2010-01-08 00:00:00"	1.98	3.96	-1.98
86	47	"2010-01-09 00:00:00"	3.96	6.94	-2.98
87	51	"2010-01-10 00:00:00"	6.94	17.91	-10.97
88	57	"2010-01-13 00:00:00"	17.91	18.86	-0.95
89	7	"2010-01-18 00:00:00"	18.86	0.99	17.87
90	21	"2010-01-26 00:00:00"	0.99	1.98	-0.99
91	22	"2010-02-08 00:00:00"	1.98	1.98	0.00
92	24	"2010-02-08 00:00:00"	1.98	3.96	-1.98
93	26	"2010-02-09 00:00:00"	3.96	5.94	-1.98
94	30	"2010-02-10 00:00:00"	5.94	8.91	-2.97
95	36	"2010-02-13 00:00:00"	8.91	21.86	-12.95
96	45	"2010-02-18 00:00:00"	21.86	1.99	19.87
97	59	"2010-02-26 00:00:00"	1.99	3.98	-1.99
98	1	"2010-03-11 00:00:00"	3.98	3.98	0.00
99	3	"2010-03-11 00:00:00"	3.98	3.96	0.02
100	5	"2010-03-12 00:00:00"	3.96	5.94	-1.98
101	9	"2010-03-13 00:00:00"	5.94	9.91	-3.97
102	15	"2010-03-16 00:00:00"	9.91	15.86	-5.95
103	24	"2010-03-21 00:00:00"	15.86	0.99	14.87
104	38	"2010-03-29 00:00:00"	0.99	1.98	-0.99
105	39	"2010-04-11 00:00:00"	1.98	1.98	0.00
106	41	"2010-04-11 00:00:00"	1.98	3.96	-1.98
107	43	"2010-04-12 00:00:00"	3.96	5.94	-1.98
108	47	"2010-04-13 00:00:00"	5.94	8.91	-2.97
109	53	"2010-04-16 00:00:00"	8.91	13.86	-4.95
110	3	"2010-04-21 00:00:00"	13.86	0.99	12.87
111	17	"2010-04-29 00:00:00"	0.99	1.98	-0.99
112	18	"2010-05-12 00:00:00"	1.98	1.98	0.00
113	20	"2010-05-12 00:00:00"	1.98	3.96	-1.98
114	22	"2010-05-13 00:00:00"	3.96	5.94	-1.98
115	26	"2010-05-14 00:00:00"	5.94	8.91	-2.97
116	32	"2010-05-17 00:00:00"	8.91	13.86	-4.95
117	41	"2010-05-22 00:00:00"	13.86	0.99	12.87
118	55	"2010-05-30 00:00:00"	0.99	1.98	-0.99
119	56	"2010-06-12 00:00:00"	1.98	1.98	0.00
120	58	"2010-06-12 00:00:00"	1.98	3.96	-1.98
121	1	"2010-06-13 00:00:00"	3.96	5.94	-1.98
122	5	"2010-06-14 00:00:00"	5.94	8.91	-2.97
123	11	"2010-06-17 00:00:00"	8.91	13.86	-4.95
124	20	"2010-06-22 00:00:00"	13.86	0.99	12.87
125	34	"2010-06-30 00:00:00"	0.99	1.98	-0.99
126	35	"2010-07-13 00:00:00"	1.98	1.98	0.00
127	37	"2010-07-13 00:00:00"	1.98	3.96	-1.98
128	39	"2010-07-14 00:00:00"	3.96	5.94	-1.98
129	43	"2010-07-15 00:00:00"	5.94	8.91	-2.97
130	49	"2010-07-18 00:00:00"	8.91	13.86	-4.95
131	58	"2010-07-23 00:00:00"	13.86	0.99	12.87
132	13	"2010-07-31 00:00:00"	0.99	1.98	-0.99
133	14	"2010-08-13 00:00:00"	1.98	1.98	0.00
134	16	"2010-08-13 00:00:00"	1.98	3.96	-1.98
135	18	"2010-08-14 00:00:00"	3.96	5.94	-1.98
136	22	"2010-08-15 00:00:00"	5.94	8.91	-2.97
137	28	"2010-08-18 00:00:00"	8.91	13.86	-4.95
138	37	"2010-08-23 00:00:00"	13.86	0.99	12.87
139	51	"2010-08-31 00:00:00"	0.99	1.98	-0.99
140	52	"2010-09-13 00:00:00"	1.98	1.98	0.00
141	54	"2010-09-13 00:00:00"	1.98	3.96	-1.98
142	56	"2010-09-14 00:00:00"	3.96	5.94	-1.98
143	1	"2010-09-15 00:00:00"	5.94	8.91	-2.97
144	7	"2010-09-18 00:00:00"	8.91	13.86	-4.95
145	16	"2010-09-23 00:00:00"	13.86	0.99	12.87
146	30	"2010-10-01 00:00:00"	0.99	1.98	-0.99
147	31	"2010-10-14 00:00:00"	1.98	1.98	0.00
148	33	"2010-10-14 00:00:00"	1.98	3.96	-1.98
149	35	"2010-10-15 00:00:00"	3.96	5.94	-1.98
150	39	"2010-10-16 00:00:00"	5.94	8.91	-2.97
151	45	"2010-10-19 00:00:00"	8.91	13.86	-4.95
152	54	"2010-10-24 00:00:00"	13.86	0.99	12.87
153	9	"2010-11-01 00:00:00"	0.99	1.98	-0.99
154	10	"2010-11-14 00:00:00"	1.98	1.98	0.00
155	12	"2010-11-14 00:00:00"	1.98	3.96	-1.98
156	14	"2010-11-15 00:00:00"	3.96	5.94	-1.98
157	18	"2010-11-16 00:00:00"	5.94	8.91	-2.97
158	24	"2010-11-19 00:00:00"	8.91	13.86	-4.95
159	33	"2010-11-24 00:00:00"	13.86	0.99	12.87
160	47	"2010-12-02 00:00:00"	0.99	1.98	-0.99
161	48	"2010-12-15 00:00:00"	1.98	1.98	0.00
162	50	"2010-12-15 00:00:00"	1.98	3.96	-1.98
163	52	"2010-12-16 00:00:00"	3.96	5.94	-1.98
164	56	"2010-12-17 00:00:00"	5.94	8.91	-2.97
165	3	"2010-12-20 00:00:00"	8.91	13.86	-4.95
166	12	"2010-12-25 00:00:00"	13.86	0.99	12.87
167	26	"2011-01-02 00:00:00"	0.99	1.98	-0.99
168	27	"2011-01-15 00:00:00"	1.98	1.98	0.00
169	29	"2011-01-15 00:00:00"	1.98	3.96	-1.98
170	31	"2011-01-16 00:00:00"	3.96	5.94	-1.98
171	35	"2011-01-17 00:00:00"	5.94	8.91	-2.97
172	41	"2011-01-20 00:00:00"	8.91	13.86	-4.95
173	50	"2011-01-25 00:00:00"	13.86	0.99	12.87
174	5	"2011-02-02 00:00:00"	0.99	1.98	-0.99
175	6	"2011-02-15 00:00:00"	1.98	1.98	0.00
176	8	"2011-02-15 00:00:00"	1.98	3.96	-1.98
177	10	"2011-02-16 00:00:00"	3.96	5.94	-1.98
178	14	"2011-02-17 00:00:00"	5.94	8.91	-2.97
179	20	"2011-02-20 00:00:00"	8.91	13.86	-4.95
180	29	"2011-02-25 00:00:00"	13.86	0.99	12.87
181	43	"2011-03-05 00:00:00"	0.99	1.98	-0.99
182	44	"2011-03-18 00:00:00"	1.98	1.98	0.00
183	46	"2011-03-18 00:00:00"	1.98	3.96	-1.98
184	48	"2011-03-19 00:00:00"	3.96	5.94	-1.98
185	52	"2011-03-20 00:00:00"	5.94	8.91	-2.97
186	58	"2011-03-23 00:00:00"	8.91	13.86	-4.95
187	8	"2011-03-28 00:00:00"	13.86	0.99	12.87
188	22	"2011-04-05 00:00:00"	0.99	1.98	-0.99
189	23	"2011-04-18 00:00:00"	1.98	1.98	0.00
190	25	"2011-04-18 00:00:00"	1.98	3.96	-1.98
191	27	"2011-04-19 00:00:00"	3.96	5.94	-1.98
192	31	"2011-04-20 00:00:00"	5.94	14.91	-8.97
193	37	"2011-04-23 00:00:00"	14.91	21.86	-6.95
194	46	"2011-04-28 00:00:00"	21.86	0.99	20.87
195	1	"2011-05-06 00:00:00"	0.99	1.98	-0.99
196	2	"2011-05-19 00:00:00"	1.98	1.98	0.00
197	4	"2011-05-19 00:00:00"	1.98	3.96	-1.98
198	6	"2011-05-20 00:00:00"	3.96	5.94	-1.98
199	10	"2011-05-21 00:00:00"	5.94	8.91	-2.97
200	16	"2011-05-24 00:00:00"	8.91	18.86	-9.95
201	25	"2011-05-29 00:00:00"	18.86	1.99	16.87
202	39	"2011-06-06 00:00:00"	1.99	2.98	-0.99
203	40	"2011-06-19 00:00:00"	2.98	3.98	-1.00
204	42	"2011-06-19 00:00:00"	3.98	7.96	-3.98
205	44	"2011-06-20 00:00:00"	7.96	8.94	-0.98
206	48	"2011-06-21 00:00:00"	8.94	8.91	0.03
207	54	"2011-06-24 00:00:00"	8.91	15.86	-6.95
208	4	"2011-06-29 00:00:00"	15.86	0.99	14.87
209	18	"2011-07-07 00:00:00"	0.99	1.98	-0.99
210	19	"2011-07-20 00:00:00"	1.98	1.98	0.00
211	21	"2011-07-20 00:00:00"	1.98	3.96	-1.98
212	23	"2011-07-21 00:00:00"	3.96	5.94	-1.98
213	27	"2011-07-22 00:00:00"	5.94	8.91	-2.97
214	33	"2011-07-25 00:00:00"	8.91	13.86	-4.95
215	42	"2011-07-30 00:00:00"	13.86	0.99	12.87
216	56	"2011-08-07 00:00:00"	0.99	1.98	-0.99
217	57	"2011-08-20 00:00:00"	1.98	1.98	0.00
218	59	"2011-08-20 00:00:00"	1.98	3.96	-1.98
219	2	"2011-08-21 00:00:00"	3.96	5.94	-1.98
220	6	"2011-08-22 00:00:00"	5.94	8.91	-2.97
221	12	"2011-08-25 00:00:00"	8.91	13.86	-4.95
222	21	"2011-08-30 00:00:00"	13.86	0.99	12.87
223	35	"2011-09-07 00:00:00"	0.99	1.98	-0.99
224	36	"2011-09-20 00:00:00"	1.98	1.98	0.00
225	38	"2011-09-20 00:00:00"	1.98	3.96	-1.98
226	40	"2011-09-21 00:00:00"	3.96	5.94	-1.98
227	44	"2011-09-22 00:00:00"	5.94	8.91	-2.97
228	50	"2011-09-25 00:00:00"	8.91	13.86	-4.95
229	59	"2011-09-30 00:00:00"	13.86	0.99	12.87
230	14	"2011-10-08 00:00:00"	0.99	1.98	-0.99
231	15	"2011-10-21 00:00:00"	1.98	1.98	0.00
232	17	"2011-10-21 00:00:00"	1.98	3.96	-1.98
233	19	"2011-10-22 00:00:00"	3.96	5.94	-1.98
234	23	"2011-10-23 00:00:00"	5.94	8.91	-2.97
235	29	"2011-10-26 00:00:00"	8.91	13.86	-4.95
236	38	"2011-10-31 00:00:00"	13.86	0.99	12.87
237	52	"2011-11-08 00:00:00"	0.99	1.98	-0.99
238	53	"2011-11-21 00:00:00"	1.98	1.98	0.00
239	55	"2011-11-21 00:00:00"	1.98	3.96	-1.98
240	57	"2011-11-22 00:00:00"	3.96	5.94	-1.98
241	2	"2011-11-23 00:00:00"	5.94	8.91	-2.97
242	8	"2011-11-26 00:00:00"	8.91	13.86	-4.95
243	17	"2011-12-01 00:00:00"	13.86	0.99	12.87
244	31	"2011-12-09 00:00:00"	0.99	1.98	-0.99
245	32	"2011-12-22 00:00:00"	1.98	1.98	0.00
246	34	"2011-12-22 00:00:00"	1.98	3.96	-1.98
247	36	"2011-12-23 00:00:00"	3.96	5.94	-1.98
248	40	"2011-12-24 00:00:00"	5.94	8.91	-2.97
249	46	"2011-12-27 00:00:00"	8.91	13.86	-4.95
250	55	"2012-01-01 00:00:00"	13.86	0.99	12.87
251	10	"2012-01-09 00:00:00"	0.99	1.98	-0.99
252	11	"2012-01-22 00:00:00"	1.98	1.98	0.00
253	13	"2012-01-22 00:00:00"	1.98	3.96	-1.98
254	15	"2012-01-23 00:00:00"	3.96	5.94	-1.98
255	19	"2012-01-24 00:00:00"	5.94	8.91	-2.97
256	25	"2012-01-27 00:00:00"	8.91	13.86	-4.95
257	34	"2012-02-01 00:00:00"	13.86	0.99	12.87
258	48	"2012-02-09 00:00:00"	0.99	1.98	-0.99
259	49	"2012-02-22 00:00:00"	1.98	1.98	0.00
260	51	"2012-02-22 00:00:00"	1.98	3.96	-1.98
261	53	"2012-02-23 00:00:00"	3.96	5.94	-1.98
262	57	"2012-02-24 00:00:00"	5.94	8.91	-2.97
263	4	"2012-02-27 00:00:00"	8.91	13.86	-4.95
264	13	"2012-03-03 00:00:00"	13.86	0.99	12.87
265	27	"2012-03-11 00:00:00"	0.99	1.98	-0.99
266	28	"2012-03-24 00:00:00"	1.98	1.98	0.00
267	30	"2012-03-24 00:00:00"	1.98	3.96	-1.98
268	32	"2012-03-25 00:00:00"	3.96	5.94	-1.98
269	36	"2012-03-26 00:00:00"	5.94	8.91	-2.97
270	42	"2012-03-29 00:00:00"	8.91	13.86	-4.95
271	51	"2012-04-03 00:00:00"	13.86	0.99	12.87
272	6	"2012-04-11 00:00:00"	0.99	1.98	-0.99
273	7	"2012-04-24 00:00:00"	1.98	1.98	0.00
274	9	"2012-04-24 00:00:00"	1.98	3.96	-1.98
275	11	"2012-04-25 00:00:00"	3.96	5.94	-1.98
276	15	"2012-04-26 00:00:00"	5.94	8.91	-2.97
277	21	"2012-04-29 00:00:00"	8.91	13.86	-4.95
278	30	"2012-05-04 00:00:00"	13.86	0.99	12.87
279	44	"2012-05-12 00:00:00"	0.99	1.98	-0.99
280	45	"2012-05-25 00:00:00"	1.98	1.98	0.00
281	47	"2012-05-25 00:00:00"	1.98	3.96	-1.98
282	49	"2012-05-26 00:00:00"	3.96	5.94	-1.98
283	53	"2012-05-27 00:00:00"	5.94	8.91	-2.97
284	59	"2012-05-30 00:00:00"	8.91	13.86	-4.95
285	9	"2012-06-04 00:00:00"	13.86	0.99	12.87
286	23	"2012-06-12 00:00:00"	0.99	1.98	-0.99
287	24	"2012-06-25 00:00:00"	1.98	1.98	0.00
288	26	"2012-06-25 00:00:00"	1.98	3.96	-1.98
289	28	"2012-06-26 00:00:00"	3.96	5.94	-1.98
290	32	"2012-06-27 00:00:00"	5.94	8.91	-2.97
291	38	"2012-06-30 00:00:00"	8.91	13.86	-4.95
292	47	"2012-07-05 00:00:00"	13.86	0.99	12.87
293	2	"2012-07-13 00:00:00"	0.99	1.98	-0.99
294	3	"2012-07-26 00:00:00"	1.98	1.98	0.00
295	5	"2012-07-26 00:00:00"	1.98	3.96	-1.98
296	7	"2012-07-27 00:00:00"	3.96	5.94	-1.98
297	11	"2012-07-28 00:00:00"	5.94	10.91	-4.97
298	17	"2012-07-31 00:00:00"	10.91	23.86	-12.95
299	26	"2012-08-05 00:00:00"	23.86	0.99	22.87
300	40	"2012-08-13 00:00:00"	0.99	1.98	-0.99
301	41	"2012-08-26 00:00:00"	1.98	1.98	0.00
302	43	"2012-08-26 00:00:00"	1.98	3.96	-1.98
303	45	"2012-08-27 00:00:00"	3.96	5.94	-1.98
304	49	"2012-08-28 00:00:00"	5.94	8.91	-2.97
305	55	"2012-08-31 00:00:00"	8.91	16.86	-7.95
306	5	"2012-09-05 00:00:00"	16.86	1.99	14.87
307	19	"2012-09-13 00:00:00"	1.99	3.98	-1.99
308	20	"2012-09-26 00:00:00"	3.98	3.98	0.00
309	22	"2012-09-26 00:00:00"	3.98	7.96	-3.98
310	24	"2012-09-27 00:00:00"	7.96	11.94	-3.98
311	28	"2012-09-28 00:00:00"	11.94	10.91	1.03
312	34	"2012-10-01 00:00:00"	10.91	16.86	-5.95
313	43	"2012-10-06 00:00:00"	16.86	0.99	15.87
314	57	"2012-10-14 00:00:00"	0.99	1.98	-0.99
315	58	"2012-10-27 00:00:00"	1.98	1.98	0.00
316	1	"2012-10-27 00:00:00"	1.98	3.96	-1.98
317	3	"2012-10-28 00:00:00"	3.96	5.94	-1.98
318	7	"2012-10-29 00:00:00"	5.94	8.91	-2.97
319	13	"2012-11-01 00:00:00"	8.91	13.86	-4.95
320	22	"2012-11-06 00:00:00"	13.86	0.99	12.87
321	36	"2012-11-14 00:00:00"	0.99	1.98	-0.99
322	37	"2012-11-27 00:00:00"	1.98	1.98	0.00
323	39	"2012-11-27 00:00:00"	1.98	3.96	-1.98
324	41	"2012-11-28 00:00:00"	3.96	5.94	-1.98
325	45	"2012-11-29 00:00:00"	5.94	8.91	-2.97
326	51	"2012-12-02 00:00:00"	8.91	13.86	-4.95
327	1	"2012-12-07 00:00:00"	13.86	0.99	12.87
328	15	"2012-12-15 00:00:00"	0.99	1.98	-0.99
329	16	"2012-12-28 00:00:00"	1.98	1.98	0.00
330	18	"2012-12-28 00:00:00"	1.98	3.96	-1.98
331	20	"2012-12-29 00:00:00"	3.96	5.94	-1.98
332	24	"2012-12-30 00:00:00"	5.94	8.91	-2.97
333	30	"2013-01-02 00:00:00"	8.91	13.86	-4.95
334	39	"2013-01-07 00:00:00"	13.86	0.99	12.87
335	53	"2013-01-15 00:00:00"	0.99	1.98	-0.99
336	54	"2013-01-28 00:00:00"	1.98	1.98	0.00
337	56	"2013-01-28 00:00:00"	1.98	3.96	-1.98
338	58	"2013-01-29 00:00:00"	3.96	5.94	-1.98
339	3	"2013-01-30 00:00:00"	5.94	8.91	-2.97
340	9	"2013-02-02 00:00:00"	8.91	13.86	-4.95
341	18	"2013-02-07 00:00:00"	13.86	0.99	12.87
342	32	"2013-02-15 00:00:00"	0.99	1.98	-0.99
343	33	"2013-02-28 00:00:00"	1.98	1.98	0.00
344	35	"2013-02-28 00:00:00"	1.98	3.96	-1.98
345	37	"2013-03-01 00:00:00"	3.96	5.94	-1.98
346	41	"2013-03-02 00:00:00"	5.94	8.91	-2.97
347	47	"2013-03-05 00:00:00"	8.91	13.86	-4.95
348	56	"2013-03-10 00:00:00"	13.86	0.99	12.87
349	11	"2013-03-18 00:00:00"	0.99	1.98	-0.99
350	12	"2013-03-31 00:00:00"	1.98	1.98	0.00
351	14	"2013-03-31 00:00:00"	1.98	3.96	-1.98
352	16	"2013-04-01 00:00:00"	3.96	5.94	-1.98
353	20	"2013-04-02 00:00:00"	5.94	8.91	-2.97
354	26	"2013-04-05 00:00:00"	8.91	13.86	-4.95
355	35	"2013-04-10 00:00:00"	13.86	0.99	12.87
356	49	"2013-04-18 00:00:00"	0.99	1.98	-0.99
357	50	"2013-05-01 00:00:00"	1.98	1.98	0.00
358	52	"2013-05-01 00:00:00"	1.98	3.96	-1.98
359	54	"2013-05-02 00:00:00"	3.96	5.94	-1.98
360	58	"2013-05-03 00:00:00"	5.94	8.91	-2.97
361	5	"2013-05-06 00:00:00"	8.91	13.86	-4.95
362	14	"2013-05-11 00:00:00"	13.86	0.99	12.87
363	28	"2013-05-19 00:00:00"	0.99	1.98	-0.99
364	29	"2013-06-01 00:00:00"	1.98	1.98	0.00
365	31	"2013-06-01 00:00:00"	1.98	3.96	-1.98
366	33	"2013-06-02 00:00:00"	3.96	5.94	-1.98
367	37	"2013-06-03 00:00:00"	5.94	8.91	-2.97
368	43	"2013-06-06 00:00:00"	8.91	13.86	-4.95
369	52	"2013-06-11 00:00:00"	13.86	0.99	12.87
370	7	"2013-06-19 00:00:00"	0.99	1.98	-0.99
371	8	"2013-07-02 00:00:00"	1.98	1.98	0.00
372	10	"2013-07-02 00:00:00"	1.98	3.96	-1.98
373	12	"2013-07-03 00:00:00"	3.96	5.94	-1.98
374	16	"2013-07-04 00:00:00"	5.94	8.91	-2.97
375	22	"2013-07-07 00:00:00"	8.91	13.86	-4.95
376	31	"2013-07-12 00:00:00"	13.86	0.99	12.87
377	45	"2013-07-20 00:00:00"	0.99	1.98	-0.99
378	46	"2013-08-02 00:00:00"	1.98	1.98	0.00
379	48	"2013-08-02 00:00:00"	1.98	3.96	-1.98
380	50	"2013-08-03 00:00:00"	3.96	5.94	-1.98
381	54	"2013-08-04 00:00:00"	5.94	8.91	-2.97
382	1	"2013-08-07 00:00:00"	8.91	13.86	-4.95
383	10	"2013-08-12 00:00:00"	13.86	0.99	12.87
384	24	"2013-08-20 00:00:00"	0.99	1.98	-0.99
385	25	"2013-09-02 00:00:00"	1.98	1.98	0.00
386	27	"2013-09-02 00:00:00"	1.98	3.96	-1.98
387	29	"2013-09-03 00:00:00"	3.96	5.94	-1.98
388	33	"2013-09-04 00:00:00"	5.94	8.91	-2.97
389	39	"2013-09-07 00:00:00"	8.91	13.86	-4.95
390	48	"2013-09-12 00:00:00"	13.86	0.99	12.87
391	3	"2013-09-20 00:00:00"	0.99	1.98	-0.99
392	4	"2013-10-03 00:00:00"	1.98	1.98	0.00
393	6	"2013-10-03 00:00:00"	1.98	3.96	-1.98
394	8	"2013-10-04 00:00:00"	3.96	5.94	-1.98
395	12	"2013-10-05 00:00:00"	5.94	8.91	-2.97
396	18	"2013-10-08 00:00:00"	8.91	13.86	-4.95
397	27	"2013-10-13 00:00:00"	13.86	0.99	12.87
398	41	"2013-10-21 00:00:00"	0.99	1.98	-0.99
399	42	"2013-11-03 00:00:00"	1.98	1.98	0.00
400	44	"2013-11-03 00:00:00"	1.98	3.96	-1.98
401	46	"2013-11-04 00:00:00"	3.96	5.94	-1.98
402	50	"2013-11-05 00:00:00"	5.94	8.91	-2.97
403	56	"2013-11-08 00:00:00"	8.91	25.86	-16.95
404	6	"2013-11-13 00:00:00"	25.86	0.99	24.87
405	20	"2013-11-21 00:00:00"	0.99	1.98	-0.99
406	21	"2013-12-04 00:00:00"	1.98	1.98	0.00
407	23	"2013-12-04 00:00:00"	1.98	3.96	-1.98
408	25	"2013-12-05 00:00:00"	3.96	5.94	-1.98
409	29	"2013-12-06 00:00:00"	5.94	8.91	-2.97
410	35	"2013-12-09 00:00:00"	8.91	13.86	-4.95
411	44	"2013-12-14 00:00:00"	13.86	1.99	11.87
412	58	"2013-12-22 00:00:00"	1.99		
```

### Encuentra al artista con el mayor número de pistas para cada género.
```sql
WITH pistas_por_artista_genero AS (
    SELECT
        g.genre_id,
        g.name AS genero,
        a.artist_id,
        ar.name AS artista,
        COUNT(t.track_id) AS cantidad_pistas
    FROM
        track t
    JOIN genre g ON t.genre_id = g.genre_id
    JOIN album a ON t.album_id = a.album_id
    JOIN artist ar ON a.artist_id = ar.artist_id
    GROUP BY
        g.genre_id, g.name, a.artist_id, ar.name
),
max_por_genero AS (
    SELECT
        genre_id,
        MAX(cantidad_pistas) AS max_pistas
    FROM
        pistas_por_artista_genero
    GROUP BY
        genre_id
)
SELECT
    p.genero,
    p.artista,
    p.cantidad_pistas
FROM
    pistas_por_artista_genero p
JOIN
    max_por_genero m ON p.genre_id = m.genre_id AND p.cantidad_pistas = m.max_pistas
ORDER BY
    p.cantidad_pistas DESC;

#################
RESULT:
#################

"genero"	"artista"	"cantidad_pistas"
"Rock"	"Led Zeppelin"	114
"Metal"	"Metallica"	112
"Latin"	"Os Paralamas Do Sucesso"	49
"TV Shows"	"Lost"	48
"Drama"	"Lost"	44
"Alternative & Punk"	"Titãs"	38
"Jazz"	"Miles Davis"	37
"Blues"	"Eric Clapton"	32
"Reggae"	"Cidade Negra"	31
"Heavy Metal"	"Iron Maiden"	28
"Sci Fi & Fantasy"	"Battlestar Galactica (Classic)"	24
"Easy Listening"	"Frank Sinatra"	24
"Pop"	"U2"	23
"R&B/Soul"	"James Brown"	20
"Hip Hop/Rap"	"House Of Pain"	19
"Comedy"	"The Office"	17
"Electronica/Dance"	"O Rappa"	17
"Bossa Nova"	"Toquinho & Vinícius"	15
"Alternative"	"Audioslave"	14
"World"	"João Suplicy"	14
"Soundtrack"	"Gilberto Gil"	14
"Soundtrack"	"Passengers"	14
"Alternative"	"Chris Cornell"	14
"Soundtrack"	"Various Artists"	14
"Science Fiction"	"Battlestar Galactica"	13
"Rock And Roll"	"BackBeat"	12
"Classical"	"Berliner Philharmoniker & Herbert Von Karajan"	3
"Classical"	"Eugene Ormandy"	3
"Opera"	"Sir Georg Solti, Sumi Jo & Wiener Philharmoniker"	1
```

### Compara el total de la última factura de cada cliente con el total de su factura anterior.
```sql
WITH facturas_ordenadas AS (
    SELECT
        invoice_id,
        customer_id,
        invoice_date,
        total,
        ROW_NUMBER() OVER (PARTITION BY customer_id ORDER BY invoice_date DESC) AS fila_desc
    FROM
        invoice
),
ultimas_facturas AS (
    SELECT * FROM facturas_ordenadas WHERE fila_desc <= 2
),
comparacion AS (
    SELECT
        f1.customer_id,
        f1.total AS total_ultima,
        f2.total AS total_anterior,
        f1.total - f2.total AS diferencia
    FROM
        ultimas_facturas f1
    JOIN
        ultimas_facturas f2
        ON f1.customer_id = f2.customer_id AND f1.fila_desc = 1 AND f2.fila_desc = 2
)
SELECT * FROM comparacion
ORDER BY customer_id;

#################
RESULT:
#################

"customer_id"	"total_ultima"	"total_anterior"	"diferencia"
1	8.91	13.86	-4.95
2	0.99	5.94	-4.95
3	0.99	5.94	-4.95
4	1.98	8.91	-6.93
5	8.91	16.86	-7.95
6	25.86	1.98	23.88
7	0.99	5.94	-4.95
8	3.96	1.98	1.98
9	8.91	13.86	-4.95
10	13.86	1.98	11.88
11	0.99	5.94	-4.95
12	5.94	3.96	1.98
13	8.91	13.86	-4.95
14	13.86	1.98	11.88
15	0.99	5.94	-4.95
16	5.94	3.96	1.98
17	10.91	13.86	-2.95
18	8.91	13.86	-4.95
19	1.99	5.94	-3.95
20	0.99	5.94	-4.95
21	1.98	8.91	-6.93
22	8.91	13.86	-4.95
23	1.98	0.99	0.99
24	0.99	5.94	-4.95
25	3.96	1.98	1.98
26	8.91	23.86	-14.95
27	13.86	1.98	11.88
28	0.99	11.94	-10.95
29	5.94	3.96	1.98
30	8.91	13.86	-4.95
31	13.86	1.98	11.88
32	0.99	5.94	-4.95
33	5.94	3.96	1.98
34	10.91	13.86	-2.95
35	8.91	13.86	-4.95
36	0.99	5.94	-4.95
37	5.94	3.96	1.98
38	8.91	13.86	-4.95
39	8.91	13.86	-4.95
40	0.99	5.94	-4.95
41	0.99	5.94	-4.95
42	1.98	8.91	-6.93
43	8.91	16.86	-7.95
44	13.86	1.98	11.88
45	0.99	5.94	-4.95
46	3.96	1.98	1.98
47	8.91	13.86	-4.95
48	13.86	1.98	11.88
49	0.99	5.94	-4.95
50	5.94	3.96	1.98
51	8.91	13.86	-4.95
52	13.86	1.98	11.88
53	0.99	5.94	-4.95
54	5.94	3.96	1.98
55	8.91	13.86	-4.95
56	8.91	13.86	-4.95
57	0.99	5.94	-4.95
58	1.99	5.94	-3.95
59	8.91	13.86	-4.95
```

### Encuentra cuántas pistas de más de 3 minutos tiene cada álbum.

```sql
SELECT
    a.album_id,
    a.title,
    COUNT(t.track_id) AS pistas_mayores_3min
FROM
    album a
JOIN
    track t ON a.album_id = t.album_id
WHERE
    t.milliseconds > 180000
GROUP BY
    a.album_id, a.title
ORDER BY
    pistas_mayores_3min DESC;

#################
RESULT:
#################

"album_id"	"title"	"pistas_mayores_3min"
141	"Greatest Hits"	57
73	"Unplugged"	30
229	"Lost, Season 3"	26
251	"The Office, Season 3"	25
230	"Lost, Season 1"	25
253	"Battlestar Galactica (Classic), Season 1"	24
231	"Lost, Season 2"	24
228	"Heroes, Season 1"	23
250	"The Office, Season 2"	22
23	"Minha Historia"	22
255	"Instant Karma: The Amnesty International Campaign to Save Darfur"	20
227	"Battlestar Galactica, Season 3"	19
167	"Acústico MTV"	18
51	"Up An' Atom"	18
37	"Greatest Kiss"	18
202	"Rotten Apples: Greatest Hits"	17
203	"A-Sides"	17
102	"Live After Death"	17
36	"Greatest Hits II"	17
213	"Pure Cult: The Best Of The Cult (For Rockers, Ravers, Lovers & Sinners) [UK]"	17
162	"Motley Crue Greatest Hits"	17
259	"Radio Brasil (O Som da Jovem Vanguarda) - Seleccao de Henrique Amaro"	16
224	"Acústico"	16
194	"By The Way"	16
67	"Vault: Def Leppard's Greatest Hits"	16
26	"Acústico MTV [Live]"	16
261	"LOST, Season 4"	16
193	"Blood Sugar Sex Magik"	16
243	"The Best Of Van Halen, Vol. I"	16
5	"Big Ones"	15
190	"The Best Of R.E.M.: The IRS Years"	15
211	"The Singles"	15
149	"Garage Inc. (Disc 2)"	15
72	"The Cream Of Clapton"	15
201	"Judas 0: B-Sides and Rarities"	15
10	"Audioslave"	14
169	"Arquivo Os Paralamas Do Sucesso"	14
271	"Revelations"	14
125	"Living After Midnight"	14
57	"Cássia Eller - Sem Limite [Disc 1]"	14
86	"Quanta Gente Veio Ver (Live)"	14
219	"Tangents"	14
241	"UB40 The Best Of - Volume Two [UK]"	14
75	"Angel Dust"	14
47	"The Best of Ed Motta"	14
84	"Roda De Funk"	14
237	"Rattle And Hum"	14
56	"Cássia Eller - Coleção Sem Limite [Disc 2]"	14
151	"Load"	14
225	"Volume Dois"	14
83	"My Way: The Best Of Frank Sinatra [Disc 1]"	14
45	"Sambas De Enredo 2001"	14
32	"Carnaval 2001"	14
139	"A TempestadeTempestade Ou O Livro Dos Dias"	14
248	"Ao Vivo [IMPORT]"	14
122	"Jorge Ben Jor 25 Anos"	14
215	"The Police Greatest Hits"	14
270	"Carry On"	14
189	"New Adventures In Hi-Fi"	13
218	"Voodoo Lounge"	13
93	"Blue Moods"	13
14	"Alcohol Fueled Brewtality Live! [Disc 1]"	13
34	"Chill: Brazil (Disc 2)"	13
55	"Chronicle, Vol. 2"	13
234	"B-Sides 1980-1990"	13
165	"Compositores"	13
140	"Mais Do Mesmo"	13
46	"Supernatural"	13
69	"Djavan Ao Vivo - Vol. 02"	13
143	"Lulu Santos - RCA 100 Anos De Música - Álbum 02"	13
27	"Cidade Negra - Hits"	13
178	"Live On Two Legs [Live]"	13
238	"The Best Of 1980-1990"	13
124	"Cafezinho"	13
29	"Axé Bahia 2001"	13
91	"Use Your Illusion I"	13
153	"ReLoad"	13
120	"Are You Experienced?"	13
76	"King For A Day Fool For A Lifetime"	13
92	"Use Your Illusion II"	13
217	"No Security"	13
221	"My Generation - The Very Best Of The Who"	13
176	"Original Soundtracks 1"	13
142	"Lulu Santos - RCA 100 Anos De Música - Álbum 01"	13
70	"Djavan Ao Vivo - Vol. 1"	13
24	"Afrociberdelia"	13
33	"Chill: Brazil (Disc 1)"	13
246	"Contraband"	13
232	"Achtung Baby"	12
95	"A Real Dead One"	12
85	"As Canções de Eu Tu Eles"	12
256	"Speak of the Devil"	12
11	"Out Of Exile"	12
115	"Sex Machine"	12
257	"20th Century Masters - The Millennium Collection: The Best of Scorpions"	12
6	"Jagged Little Pill"	12
148	"Black Album"	12
175	"Walking Into Clarksdale"	12
157	"Miles Ahead"	12
41	"Meus Momentos"	12
195	"Californication"	12
99	"Fear Of The Dark"	12
199	"Maquinarama"	12
166	"Olodum"	12
38	"Heart of the Night"	12
48	"The Essential Miles Davis [Disc 1]"	12
174	"Tribute"	12
90	"Appetite for Destruction"	12
63	"Purpendicular"	12
180	"Riot Act"	12
196	"Retrospective I (1974-1980)"	12
236	"Pop"	12
212	"Beyond Good And Evil"	12
30	"BBC Sessions [Disc 1] [Live]"	12
145	"Barulhinho Bom"	11
161	"Demorou..."	11
98	"Dance Of Death"	11
123	"Jota Quest-1995"	11
19	"Chemical Wedding"	11
185	"Greatest Hits I"	11
96	"A Real Live One"	11
235	"How To Dismantle An Atomic Bomb"	11
40	"Into The Light"	11
247	"Vinicius De Moraes"	11
118	"The Return Of The Space Cowboy"	11
126	"Unplugged [Live]"	11
117	"Synkronized"	11
94	"A Matter of Life and Death"	11
187	"Out Of Time"	11
88	"Faceless"	11
61	"Knocking at Your Back Door: The Best Of Deep Purple in the 80's"	11
155	"St. Anger"	11
25	"Da Lama Ao Caos"	11
71	"Elis Regina-Minha História"	11
258	"House of Pain"	11
7	"Facelift"	11
113	"The X Factor"	11
233	"All That You Can't Leave Behind"	11
81	"One By One"	11
150	"Kill 'Em All"	10
220	"Transmission"	10
66	"The Battle Rages On"	10
206	"Core"	10
147	"The Best Of Men At Work"	10
28	"Na Pista"	10
49	"The Essential Miles Davis [Disc 2]"	10
42	"Minha História"	10
179	"Pearl Jam"	10
105	"No Prayer For The Dying"	10
158	"Milton Nascimento Ao Vivo"	10
240	"Zooropa"	10
163	"From The Muddy Banks Of The Wishkah [Live]"	10
104	"Live At Donington 1992 (Disc 2)"	10
159	"Minas"	10
269	"Temple of the Dog"	10
186	"News Of The World"	10
168	"Arquivo II"	10
80	"In Your Honor [Disc 2]"	10
182	"Vs."	10
1	"For Those About To Rock We Salute You"	10
188	"Green"	10
181	"Ten"	10
127	"BBC Sessions [Disc 2] [Live]"	10
97	"Brave New World"	10
77	"The Real Thing"	10
200	"O Samba Poconé"	10
21	"Prenda Minha"	10
245	"Van Halen III"	10
209	"Live [Disc 1]"	10
119	"Get Born"	10
103	"Live At Donington 1992 (Disc 1)"	9
244	"Van Halen"	9
204	"Morning Dance"	9
35	"Garage Inc. (Disc 1)"	9
89	"American Idiot"	9
239	"War"	9
109	"Rock In Rio [CD2]"	9
164	"Nevermind"	9
78	"Deixa Entrar"	9
177	"The Beast Live"	9
106	"Piece Of Mind"	9
18	"Body Count"	9
68	"Outbreak"	9
146	"Seek And Shall Find: More Of The Best (1963-1981)"	9
52	"Vinícius De Moraes - Sem Limite"	9
322	"Frank"	9
192	"Raul Seixas"	9
108	"Rock In Rio [CD1]"	9
65	"Stormbringer"	9
79	"In Your Honor [Disc 1]"	9
156	"...And Justice For All"	9
74	"Album Of The Year"	9
64	"Slaves And Masters"	9
134	"Led Zeppelin III"	9
116	"Emergency On Planet Earth"	9
100	"Iron Maiden"	9
210	"Live [Disc 2]"	9
53	"Vozes do MPB"	8
58	"Come Taste The Band"	8
101	"Killers"	8
129	"Houses Of The Holy"	8
131	"IV"	8
110	"Seventh Son of a Seventh Son"	8
183	"Dark Side Of The Moon"	8
82	"The Colour And The Shape"	8
152	"Master Of Puppets"	8
39	"International Superhits"	8
54	"Chronicle, Vol. 1"	8
112	"The Number of The Beast"	8
111	"Somewhere in Time"	8
197	"Santana - As Years Go By"	8
223	"Serie Sem Limite (Disc 2)"	8
135	"Physical Graffiti [Disc 2]"	8
4	"Let There Be Rock"	8
321	"Back to Black"	8
9	"Plays Metallica By Four Cellos"	8
184	"Os Cães Ladram Mas A Caravana Não Pára"	8
8	"Warner 25 Anos"	8
133	"Led Zeppelin II"	8
13	"The Best Of Billy Cobham"	8
107	"Powerslave"	8
154	"Ride The Lightning"	8
121	"Surfing with the Alien (Remastered)"	8
130	"In Through The Out Door"	7
222	"Serie Sem Limite (Disc 1)"	7
160	"Ace Of Spades"	7
16	"Black Sabbath"	7
207	"Mezmerize"	7
62	"Machine Head"	7
128	"Coda"	7
208	"[1997] Black Light Syndrome"	7
17	"Black Sabbath Vol. 4 (Remaster)"	7
43	"MK III The Final Concerts [Disc 1]"	7
59	"Deep Purple In Rock"	7
60	"Fireball"	7
114	"Virtual XI"	7
205	"In Step"	6
20	"The Best Of Buddy Guy - The Millenium Collection"	6
249	"The Office, Season 1"	6
44	"Physical Graffiti [Disc 1]"	6
132	"Led Zeppelin I"	6
216	"Hot Rocks, 1964-1971 (Disc 1)"	6
242	"Diver Down"	6
136	"Presence"	6
31	"Bongo Fury"	6
214	"The Doors"	5
15	"Alcohol Fueled Brewtality Live! [Disc 2]"	5
137	"The Song Remains The Same (Disc 1)"	5
144	"Misplaced Childhood"	5
198	"Santana Live"	5
191	"Cesta Básica"	4
138	"The Song Remains The Same (Disc 2)"	4
50	"The Final Concerts (Disc 2)"	4
22	"Sozinho Remix Ao Vivo"	3
87	"Quanta Gente Veio ver--Bônus De Carnaval"	3
3	"Restless and Wild"	3
264	"Realize"	2
263	"Muso Ko"	2
265	"Every Kind of Light"	2
173	"No More Tears (Remastered)"	2
280	"The World of Classical Favourites"	2
262	"Quiet Songs"	2
171	"Blizzard of Ozz"	2
329	"South American Getaway"	1
309	"Palestrina: Missa Papae Marcelli & Allegri: Miserere"	1
337	"Szymanowski: Piano Works, Vol. 1"	1
323	"Carried to Dust (Bonus Track Version)"	1
306	"Elgar: Cello Concerto & Vaughan Williams: Fantasias"	1
286	"Great Opera Choruses"	1
279	"Handel: The Messiah (Highlights)"	1
338	"Nielsen: The Six Symphonies"	1
226	"Battlestar Galactica: The Story So Far"	1
276	"Bach: Violin Concertos"	1
281	"Sir Neville Marriner: A Celebration"	1
330	"Górecki: Symphony No. 3"	1
170	"Bark at the Moon (Remastered)"	1
302	"Mascagni: Cavalleria Rusticana"	1
172	"Diary of a Madman (Remastered)"	1
288	"Fauré: Requiem, Ravel: Pavane & Others"	1
341	"Great Recordings of the Century - Shubert: Schwanengesang, 4 Lieder"	1
324	"Beethoven: Symphony No. 6 'Pastoral' Etc."	1
310	"Prokofiev: Romeo & Juliet"	1
304	"Beethoven Piano Sonatas: Moonlight & Pastorale"	1
282	"Mozart: Wind Concertos"	1
292	"Holst: The Planets, Op. 32 & Vaughan Williams: Fantasies"	1
267	"Worlds"	1
332	"The Ultimate Relexation Album"	1
294	"Great Performances - Barber's Adagio and Other Romantic Favorites for Strings"	1
296	"A Copland Celebration, Vol. I"	1
346	"Mozart: Chamber Music"	1
311	"Strauss: Waltzes"	1
325	"Bartok: Violin & Viola Concertos"	1
319	"Armada: Music from the Courts of England and Spain"	1
298	"Prokofiev: Symphony No.1"	1
334	"Weill: The Seven Deadly Sins"	1
274	"Pachelbel: Canon & Gigue"	1
316	"Grieg: Peer Gynt Suites & Sibelius: Pelléas et Mélisande"	1
254	"Aquaman"	1
320	"Mozart: Symphonies Nos. 40 & 41"	1
287	"Wagner: Favourite Overtures"	1
301	"Chopin: Piano Concertos Nos. 1 & 2"	1
312	"Berlioz: Symphonie Fantastique"	1
299	"Scheherazade"	1
290	"The Last Night of the Proms"	1
300	"Bach: The Brandenburg Concertos"	1
284	"Beethoven: Symhonies Nos. 5 & 6"	1
342	"Locatelli: Concertos for Violin, Strings and Continuo, Vol. 3"	1
335	"J.S. Bach: Chaconne, Suite in E Minor, Partita in E Major & Prelude, Fugue and Allegro"	1
339	"Great Recordings of the Century: Paganini's 24 Caprices"	1
326	"Mendelssohn: A Midsummer Night's Dream"	1
2	"Balls to the Wall"	1
272	"Adorate Deum: Gregorian Chant from the Proper of the Mass"	1
327	"Bach: Orchestral Suites Nos. 1 - 4"	1
331	"Purcell: The Fairy Queen"	1
336	"Prokofiev: Symphony No.5 & Stravinksy: Le Sacre Du Printemps"	1
275	"Vivaldi: The Four Seasons"	1
285	"A Soprano Inspired"	1
260	"Cake: B-Sides and Rarities"	1
308	"Tchaikovsky: 1812 Festival Overture, Op.49, Capriccio Italien & Beethoven: Wellington's Victory"	1
343	"Respighi:Pines of Rome"	1
252	"Un-Led-Ed"	1
273	"Allegri: Miserere"	1
303	"Sibelius: Finlandia"	1
305	"Great Recordings of the Century - Mahler: Das Lied von der Erde"	1
283	"Haydn: Symphonies 99 - 104"	1
347	"Koyaanisqatsi (Soundtrack from the Motion Picture)"	1
307	"Adams, John: The Chairman Dances"	1
291	"Puccini: Madama Butterfly - Highlights"	1
289	"Tchaikovsky: The Nutcracker"	1
268	"The Best of Beethoven"	1
```