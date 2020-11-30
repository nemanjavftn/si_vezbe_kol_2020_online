# si_vezbe_kol_2020_online

Тип апликације: трослојна архитектура, Web. Potrebno je napraviti aplikaciju ‘GroceryStore’. Koraci:
Kreirati bazu pod nazivom GroceryStoreDB. Potom u bazi kreirati tabelu po sledećem obrascu: 
- Na osnovu početnih slova vašeg imena i prezimena pronaći odgovarajuću numeričku vrednost (prema tabeli i početnim slovima imena i prezimena, bez dijakritika, tj. č,ć=c; š=s, ž=z, đ=d), tako što sabirate numeričke ekvivalente slova, a potom cifre dobijenog rezultata.
Primer: za Nemanja Vićović dobija se N+V=13+21=34 = 7 (3+4).
Slovo:	A	B	C	D	E	F	G	H	I	J	K	L	M
num. ekviv.	0	1	2	3	4	5	6	7	8	9	10	11	12

Slovo:	N	O	P	Q	R	S	T	U	V	W	X	Y	Z
Num. ekviv.	13	14	15	16	17	18	19	20	21	22	23	24	25

- Na osnovu dobijene numeričke vrednosti, iz sledeće liste odabrati naziv tabele (u zagradi su navedeni neki od proizvoda koji spadaju u navedenu kategoriju):
1.	Alcoholdrinks (beer, wine, spirits – whiskey, bourbon, cognac, vodka, etc.)
2.	Beverages (tea, coffee, soda, juice, hot chocolate, water, etc.)
3.	Produce (Fruit and Vegetables – banana, lemon, orange, mandarin, avocado, apple, plum, tomato, broccoli, pepper, squash, onion, garlic, lettuce, potato, etc.)
4.	CookiesSnacksCandies (chocolate, biscuits, mars, marabou, eurocrem, chocko banana, vafles, etc.)
5.	BreadBakery (bread, tortilla, sandwich loaves, dinner rolls, pie, brioche, brownies, croissant, etc.)
6.	DairyEggsCheese (milk, yogurt, cream, butter, cheese, etc.)
7.	GrainsPastaSides (rice, wheat, quinoa, spaghetti, linguine, fettuccine, rigate, etc.)
8.	MeatSeafood (pork, beef, lamb, chicken, poultry, tuna, salmon, trout, swordfish, shrimp, lobster, oyster, squid, caviar, etc.)
9.	Cleaning (detergent, liquid laundry detergent (e.g. Persil Proclean), cleaner spray, cooktop cleaning kit, mops, mopping cloths, foaming cleaner, glass cleaner, dishwashing liquid, wipes, , etc.)
- U tabeli kreirati ID i još 6 atributa/kolona: ProductName (string), ProductDescription (string), ProductQuantity (string), ProductPrice (decimal – na 2 decimale!), ProductDiscount (bit), InStock (int).
Primere proizvoda možete videti npr. kod Wallmart-a: https://www.walmart.com/all-departments
-	Креирати слој који ће вршити конекцију на базу података (Data Layer) и где ће постојати један репозиторијум за комуникацију са креираном табелом у бази података. У оквиру репозиторијума треба да постоје методе: Insert (користи се за унос података у табелу) и GetAll (за довлачење свих редова из табеле).
-	Креирати слој у ком ће се налазити логика апликације и где ће у оквиру посебне business класе за рад са вертикалом креираног ентитета постојати две методе које преко Data слоја врше унос и довлачење података из репозиторијума. Метода која довлачи податке треба да има опцију (опциони аргумент) са називом inStockMin где се довлаче само производи чији InStock je већи од прослеђеног аргументом (ако се не проследи ништа или се проследи 0 довлаче се сви производи).
-	На крају, направити ASP.NET Web Forms апликацију где ће се на почетној форми вршити унос једног ентитета у базу података а у доњем делу форме ће се налазити један ListBox који приказује листу свих редова из табеле (за испис користити минимум 3 атрибута). На сваки унос треба refresh-овати листу. 
Напомене: Користити лабеле поред контрола како би форма “имала смисла”. У моделима користити приватна поља и јавна својства (или аутосвојства).
