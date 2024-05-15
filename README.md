# Examen Bases de Datos
### Maria Jose Pinto Aparicio & Samuel Rubiano Orjuela

1. Obtener los nombres de todos los actores y las películas en las que han actuado.
```sql
    SELECT DISTINCT a.nombre, p.titulo
    FROM sakilacampus.actor a
    JOIN sakilacampus.pelicula_actor pa ON a.id_actor =pa.id_actor 
    JOIN sakilacampus.pelicula p ON pa.id_pelicula = p.id_pelicula;
+----------+-----------------------+
| nombre   | titulo                |
+----------+-----------------------+
| PENELOPE | ACADEMY DINOSAUR      |
| PENELOPE | ANACONDA CONFESSIONS  |
| PENELOPE | ANGELS LIFE           |
| PENELOPE | BULWORTH COMMANDMENTS |
| PENELOPE | CHEAPER CLYDE         |
| PENELOPE | COLOR PHILADELPHIA    |
| PENELOPE | ELEPHANT TROJAN       |
| PENELOPE | GLEAMING JAWBREAKER   |
| PENELOPE | HUMAN GRAFFITI        |
| PENELOPE | KING EVOLUTION        |
| PENELOPE | LADY STAGE            |
| PENELOPE | LANGUAGE COWBOY       |
| PENELOPE | MULHOLLAND BEAST      |
| PENELOPE | OKLAHOMA JUMANJI      |
| PENELOPE | RULES HUMAN           |
| PENELOPE | SPLASH GUMP           |
| PENELOPE | VERTIGO NORTHWEST     |
| PENELOPE | WESTWARD SEABISCUIT   |
| PENELOPE | WIZARD COLDBLOODED    |
| NICK     | ADAPTATION HOLES      |
| NICK     | APACHE DIVINE         |
| NICK     | BABY HALL             |
| NICK     | BULL SHAWSHANK        |
| NICK     | CHAINSAW UPTOWN       |
| NICK     | CHISUM BEHAVIOR       |
| NICK     | DESTINY SATURDAY      |
| NICK     | DRACULA CRYSTAL       |
| NICK     | FIGHT JAWBREAKER      |
| NICK     | FLASH WARS            |
| NICK     | GILBERT PELICAN       |
| NICK     | GOODFELLAS SALUTE     |
| NICK     | HAPPINESS UNITED      |
| NICK     | INDIAN LOVE           |
| NICK     | JEKYLL FROGMEN        |
| NICK     | JERSEY SASSY          |
| NICK     | LIAISONS SWEET        |
| NICK     | LUCKY FLYING          |
| NICK     | MAGUIRE APACHE        |
| NICK     | MALLRATS UNITED       |
| NICK     | MASK PEACH            |
| NICK     | ROOF CHAMPION         |
| NICK     | RUSHMORE MERMAID      |
| NICK     | SMILE EARRING         |
| NICK     | WARDROBE PHANTOM      |
| ED       | ALONE TRIP            |
| ED       | ARMY FLINTSTONES      |
| ED       | ARTIST COLDBLOODED    |
| ED       | BOONDOCK BALLROOM     |
| ED       | CADDYSHACK JEDI       |
| ED       | COWBOY DOOM           |
| ED       | EVE RESURRECTION      |
| ED       | FORREST SONS          |
| ED       | FRENCH HOLIDAY        |
| ED       | FROST HEAD            |
| ED       | HALLOWEEN NUTS        |
| ED       | HUNTER ALTER          |
| ED       | IMAGE PRINCESS        |
| ED       | JEEPERS WEDDING       |
| ED       | LUCK OPUS             |
| ED       | NECKLACE OUTBREAK     |
| ED       | PLATOON INSTINCT      |
| ED       | SPICE SORORITY        |
| ED       | WEDDING APOLLO        |
| ED       | WEEKEND PERSONAL      |
| ED       | WHALE BIKINI          |
| ED       | YOUNG LANGUAGE        |
| JENNIFER | ANACONDA CONFESSIONS  |
| JENNIFER | ANGELS LIFE           |
| JENNIFER | BAREFOOT MANCHURIAN   |
| JENNIFER | BED HIGHBALL          |
| JENNIFER | BLADE POLISH          |
| JENNIFER | BOONDOCK BALLROOM     |
| JENNIFER | GHOSTBUSTERS ELF      |
| JENNIFER | GREEDY ROOTS          |
| JENNIFER | HANOVER GALAXY        |
| JENNIFER | INSTINCT AIRPORT      |
| JENNIFER | JUMANJI BLADE         |
| JENNIFER | NATIONAL STORY        |
| JENNIFER | OKLAHOMA JUMANJI      |
| JENNIFER | POSEIDON FOREVER      |
| JENNIFER | RAIDERS ANTITRUST     |
| JENNIFER | RANDOM GO             |
| JENNIFER | REDS POCUS            |
| JENNIFER | SILVERADO GOLDFINGER  |
| JENNIFER | SPLASH GUMP           |
| JENNIFER | SUBMARINE BED         |
| JENNIFER | TREASURE COMMAND      |
| JENNIFER | UNFORGIVEN ZOOLANDER  |
| JOHNNY   | AMADEUS HOLY          |
| JOHNNY   | BANGER PINOCCHIO      |
| JOHNNY   | BONNIE HOLOCAUST      |
| JOHNNY   | CHITTY LOCK           |
| JOHNNY   | COMMANDMENTS EXPRESS  |
| JOHNNY   | CONEHEADS SMOOCHY     |
| JOHNNY   | DADDY PITTSBURGH      |
| JOHNNY   | DAISY MENAGERIE       |
| JOHNNY   | ENOUGH RAGING         |
| JOHNNY   | ESCAPE METROPOLIS     |
| JOHNNY   | FIRE WOLVES           |
| JOHNNY   | FRONTIER CABIN        |
+----------+-----------------------+

```
---
2. Listar todos los clientes y los almacenes donde están registrados.
```sql
    SELECT cl.id_cliente, cl.nombre, cl.apellidos, a.id_almacen, a.id_direccion
    FROM sakilacampus.cliente cl
    JOIN sakilacampus.almacen a ON cl.id_almacen = a.id_almacen;
+------------+-----------+------------+------------+--------------+
| id_cliente | nombre    | apellidos  | id_almacen | id_direccion |
+------------+-----------+------------+------------+--------------+
|          1 | MARY      | SMITH      |          1 |            1 |
|          2 | PATRICIA  | JOHNSON    |          1 |            1 |
|          3 | LINDA     | WILLIAMS   |          1 |            1 |
|          5 | ELIZABETH | BROWN      |          1 |            1 |
|          7 | MARIA     | MILLER     |          1 |            1 |
|         10 | DOROTHY   | TAYLOR     |          1 |            1 |
|         12 | NANCY     | THOMAS     |          1 |            1 |
|         15 | HELEN     | HARRIS     |          1 |            1 |
|         17 | DONNA     | THOMPSON   |          1 |            1 |
|         19 | RUTH      | MARTINEZ   |          1 |            1 |
|         21 | MICHELLE  | CLARK      |          1 |            1 |
|         22 | LAURA     | RODRIGUEZ  |          1 |            1 |
|         25 | DEBORAH   | WALKER     |          1 |            1 |
|         28 | CYNTHIA   | YOUNG      |          1 |            1 |
|         30 | MELISSA   | KING       |          1 |            1 |
|         32 | AMY       | LOPEZ      |          1 |            1 |
|         37 | PAMELA    | BAKER      |          1 |            1 |
|         38 | MARTHA    | GONZALEZ   |          1 |            1 |
|         39 | DEBRA     | NELSON     |          1 |            1 |
|         41 | STEPHANIE | MITCHELL   |          1 |            1 |
|         44 | MARIE     | TURNER     |          1 |            1 |
|         45 | JANET     | PHILLIPS   |          1 |            1 |
|         47 | FRANCES   | PARKER     |          1 |            1 |
|         48 | ANN       | EVANS      |          1 |            1 |
|         50 | DIANE     | COLLINS    |          1 |            1 |
|         51 | ALICE     | STEWART    |          1 |            1 |
|         52 | JULIE     | SANCHEZ    |          1 |            1 |
|         53 | HEATHER   | MORRIS     |          1 |            1 |
|         54 | TERESA    | ROGERS     |          1 |            1 |
|         56 | GLORIA    | COOK       |          1 |            1 |
|         58 | JEAN      | BELL       |          1 |            1 |
|         59 | CHERYL    | MURPHY     |          1 |            1 |
|         60 | MILDRED   | BAILEY     |          1 |            1 |
|         62 | JOAN      | COOPER     |          1 |            1 |
|         63 | ASHLEY    | RICHARDSON |          1 |            1 |
|         67 | KELLY     | TORRES     |          1 |            1 |
|         68 | NICOLE    | PETERSON   |          1 |            1 |
|         71 | KATHY     | JAMES      |          1 |            1 |
|         74 | DENISE    | KELLY      |          1 |            1 |
|         78 | LORI      | WOOD       |          1 |            1 |
|         79 | RACHEL    | BARNES     |          1 |            1 |
|         80 | MARILYN   | ROSS       |          1 |            1 |
|         81 | ANDREA    | HENDERSON  |          1 |            1 |
|         82 | KATHRYN   | COLEMAN    |          1 |            1 |
|         83 | LOUISE    | JENKINS    |          1 |            1 |
|         87 | WANDA     | PATTERSON  |          1 |            1 |
|         89 | JULIA     | FLORES     |          1 |            1 |
|         93 | PHYLLIS   | FOSTER     |          1 |            1 |
|         94 | NORMA     | GONZALES   |          1 |            1 |
|         96 | DIANA     | ALEXANDER  |          1 |            1 |
|         98 | LILLIAN   | GRIFFIN    |          1 |            1 |
|        100 | ROBIN     | HAYES      |          1 |            1 |
|        101 | PEGGY     | MYERS      |          1 |            1 |
|        102 | CRYSTAL   | FORD       |          1 |            1 |
|        103 | GLADYS    | HAMILTON   |          1 |            1 |
|        104 | RITA      | GRAHAM     |          1 |            1 |
|        105 | DAWN      | SULLIVAN   |          1 |            1 |
|        106 | CONNIE    | WALLACE    |          1 |            1 |
|        107 | FLORENCE  | WOODS      |          1 |            1 |
|        108 | TRACY     | COLE       |          1 |            1 |
|        111 | CARMEN    | OWENS      |          1 |            1 |
|        115 | WENDY     | HARRISON   |          1 |            1 |
|        116 | VICTORIA  | GIBSON     |          1 |            1 |
|        117 | EDITH     | MCDONALD   |          1 |            1 |
|        118 | KIM       | CRUZ       |          1 |            1 |
|        119 | SHERRY    | MARSHALL   |          1 |            1 |
|        121 | JOSEPHINE | GOMEZ      |          1 |            1 |
|        122 | THELMA    | MURRAY     |          1 |            1 |
|        124 | SHEILA    | WELLS      |          1 |            1 |
|        125 | ETHEL     | WEBB       |          1 |            1 |
|        126 | ELLEN     | SIMPSON    |          1 |            1 |
|        128 | MARJORIE  | TUCKER     |          1 |            1 |
|        129 | CARRIE    | PORTER     |          1 |            1 |
|        130 | CHARLOTTE | HUNTER     |          1 |            1 |
|        133 | PAULINE   | HENRY      |          1 |            1 |
|        134 | EMMA      | BOYD       |          1 |            1 |
|        138 | HAZEL     | WARREN     |          1 |            1 |
|        139 | AMBER     | DIXON      |          1 |            1 |
|        140 | EVA       | RAMOS      |          1 |            1 |
|        141 | DEBBIE    | REYES      |          1 |            1 |
|        142 | APRIL     | BURNS      |          1 |            1 |
|        143 | LESLIE    | GORDON     |          1 |            1 |
|        144 | CLARA     | SHAW       |          1 |            1 |
|        145 | LUCILLE   | HOLMES     |          1 |            1 |
|        146 | JAMIE     | RICE       |          1 |            1 |
|        148 | ELEANOR   | HUNT       |          1 |            1 |
|        149 | VALERIE   | BLACK      |          1 |            1 |
|        152 | ALICIA    | MILLS      |          1 |            1 |
|        155 | GAIL      | KNIGHT     |          1 |            1 |
|        156 | BERTHA    | FERGUSON   |          1 |            1 |
|        158 | VERONICA  | STONE      |          1 |            1 |
|        159 | JILL      | HAWKINS    |          1 |            1 |
|        161 | GERALDINE | PERKINS    |          1 |            1 |
|        163 | CATHY     | SPENCER    |          1 |            1 |
|        166 | LYNN      | PAYNE      |          1 |            1 |
|        168 | REGINA    | BERRY      |          1 |            1 |
|        170 | BEATRICE  | ARNOLD     |          1 |            1 |
|        172 | BERNICE   | WILLIS     |          1 |            1 |
|        173 | AUDREY    | RAY        |          1 |            1 |
|        175 | ANNETTE   | OLSON      |          1 |            1 |
+------------+-----------+------------+------------+--------------+

```
---
3. Encontrar todas las películas y sus respectivas categorías.
```sql
    SELECT p.id_pelicula, p.titulo, c.nombre AS nombre_categoria
    FROM sakilacampus.pelicula p
    JOIN sakilacampus.pelicula_categoria pc ON p.id_pelicula = pc.id_pelicula
    JOIN sakilacampus.categoria c ON pc.id_categoria = c.id_categoria;

+-------------+-------------------------+------------------+
| id_pelicula | titulo                  | nombre_categoria |
+-------------+-------------------------+------------------+
|          19 | AMADEUS HOLY            | Action           |
|          21 | AMERICAN CIRCUS         | Action           |
|          29 | ANTITRUST TOMATOES      | Action           |
|          38 | ARK RIDGEMONT           | Action           |
|          56 | BAREFOOT MANCHURIAN     | Action           |
|          67 | BERETS AGENT            | Action           |
|          97 | BRIDE INTRIGUE          | Action           |
|         105 | BULL SHAWSHANK          | Action           |
|         111 | CADDYSHACK JEDI         | Action           |
|         115 | CAMPUS REMEMBER         | Action           |
|         126 | CASUALTIES ENCINO       | Action           |
|         130 | CELEBRITY HORN          | Action           |
|         162 | CLUELESS BUCKET         | Action           |
|         194 | CROW GREASE             | Action           |
|         205 | DANCES NONE             | Action           |
|         210 | DARKO DORADO            | Action           |
|         212 | DARN FORRESTER          | Action           |
|         229 | DEVIL DESIRE            | Action           |
|         250 | DRAGON SQUAD            | Action           |
|         252 | DREAM PICKUP            | Action           |
|         253 | DRIFTER COMMANDMENTS    | Action           |
|         271 | EASY GLADIATOR          | Action           |
|         287 | ENTRAPMENT SATISFACTION | Action           |
|         292 | EXCITEMENT EVE          | Action           |
|         303 | FANTASY TROOPERS        | Action           |
|         318 | FIREHOUSE VIETNAM       | Action           |
|         327 | FOOL MOCKINGBIRD        | Action           |
|         329 | FORREST SONS            | Action           |
|         360 | GLASS DYING             | Action           |
|         371 | GOSFORD DONNIE          | Action           |
|         375 | GRAIL FRANKENSTEIN      | Action           |
|         395 | HANDICAP BOONDOCK       | Action           |
|         417 | HILLS NEIGHBORS         | Action           |
|         501 | KISSING DOLLS           | Action           |
|         511 | LAWRENCE LOVE           | Action           |
|         530 | LORD ARIZONA            | Action           |
|         542 | LUST LOCK               | Action           |
|         549 | MAGNOLIA FORRESTER      | Action           |
|         574 | MIDNIGHT WESTWARD       | Action           |
|         579 | MINDS TRUMAN            | Action           |
|         586 | MOCKINGBIRD HOLLYWOOD   | Action           |
|         594 | MONTEZUMA COMMAND       | Action           |
|         659 | PARK CITIZEN            | Action           |
|         664 | PATRIOT ROMAN           | Action           |
|         697 | PRIMARY GLASS           | Action           |
|         707 | QUEST MUSSOLINI         | Action           |
|         717 | REAR TRADING            | Action           |
|         732 | RINGS HEARTBREAKERS     | Action           |
|         748 | RUGRATS SHAKESPEARE     | Action           |
|         793 | SHRUNK DIVINE           | Action           |
|         794 | SIDE ARK                | Action           |
|         802 | SKY MIRACLE             | Action           |
|         823 | SOUTH WAIT              | Action           |
|         825 | SPEAKEASY DATE          | Action           |
|         838 | STAGECOACH ARMAGEDDON   | Action           |
|         850 | STORY SIDE              | Action           |
|         869 | SUSPECTS QUILLS         | Action           |
|         911 | TRIP NEWTON             | Action           |
|         915 | TRUMAN CRAZY            | Action           |
|         927 | UPRISING UPTOWN         | Action           |
|         964 | WATERFRONT DELIVERANCE  | Action           |
|         968 | WEREWOLF LOLA           | Action           |
|         982 | WOMEN DORADO            | Action           |
|         991 | WORST BANGER            | Action           |
|          18 | ALTER VICTORY           | Animation        |
|          23 | ANACONDA CONFESSIONS    | Animation        |
|          36 | ARGONAUTS TOWN          | Animation        |
|          70 | BIKINI BORROWERS        | Animation        |
|          78 | BLACKOUT PRIVATE        | Animation        |
|          89 | BORROWERS BEDAZZLED     | Animation        |
|         118 | CANYON STOCK            | Animation        |
|         121 | CAROL TEXAS             | Animation        |
|         134 | CHAMPION FLATLINERS     | Animation        |
|         154 | CLASH FREDDY            | Animation        |
|         160 | CLUB GRAFFITI           | Animation        |
|         193 | CROSSROADS CASUALTIES   | Animation        |
|         208 | DARES PLUTO             | Animation        |
|         223 | DESIRE ALIEN            | Animation        |
|         239 | DOGMA FAMILY            | Animation        |
|         241 | DONNIE ALLEY            | Animation        |
|         243 | DOORS PRESIDENT         | Animation        |
|         245 | DOUBLE WRATH            | Animation        |
|         259 | DUCK RACER              | Animation        |
|         268 | EARLY HOME              | Animation        |
|         300 | FALCON VOLUME           | Animation        |
|         314 | FIGHT JAWBREAKER        | Animation        |
|         325 | FLOATS GARDEN           | Animation        |
|         326 | FLYING HOOK             | Animation        |
|         330 | FORRESTER COMANCHEROS   | Animation        |
|         349 | GANGS PRIDE             | Animation        |
|         355 | GHOSTBUSTERS ELF        | Animation        |
|         402 | HARPER DYING            | Animation        |
|         430 | HOOK CHARIOTS           | Animation        |
|         433 | HORN WORKING            | Animation        |
|         456 | INCH JET                | Animation        |
|         461 | INSECTS STONE           | Animation        |
|         464 | INTENTIONS EMPIRE       | Animation        |
|         470 | ISHTAR ROCKETEER        | Animation        |
|         489 | JUGGLER HARDLY          | Animation        |
|         510 | LAWLESS VISION          | Animation        |
+-------------+-------------------------+------------------+

```
---
4. Listar los nombres de las ciudades junto con sus países.
```sql
    SELECT c.id_ciudad, c.nombre AS nombre_ciudad, p.id_pais, p.nombre AS nombre_pais 
    FROM sakilacampus.ciudad c
    JOIN sakilacampus.pais p ON c.id_pais = p.id_pais;

+-----------+----------------------+---------+----------------+
| id_ciudad | nombre_ciudad        | id_pais | nombre_pais    |
+-----------+----------------------+---------+----------------+
|       251 | Kabul                |       1 | Afghanistan    |
|        59 | Batna                |       2 | Algeria        |
|        63 | Bchar                |       2 | Algeria        |
|       483 | Skikda               |       2 | Algeria        |
|       516 | Tafuna               |       3 | American Samoa |
|        67 | Benguela             |       4 | Angola         |
|       360 | Namibe               |       4 | Angola         |
|       493 | South Hill           |       5 | Anguilla       |
|        20 | Almirante Brown      |       6 | Argentina      |
|        43 | Avellaneda           |       6 | Argentina      |
|        45 | Baha Blanca          |       6 | Argentina      |
|       128 | Crdoba               |       6 | Argentina      |
|       161 | Escobar              |       6 | Argentina      |
|       165 | Ezeiza               |       6 | Argentina      |
|       289 | La Plata             |       6 | Argentina      |
|       334 | Merlo                |       6 | Argentina      |
|       424 | Quilmes              |       6 | Argentina      |
|       454 | San Miguel de Tucumn |       6 | Argentina      |
|       457 | Santa F              |       6 | Argentina      |
|       524 | Tandil               |       6 | Argentina      |
|       567 | Vicente Lpez         |       6 | Argentina      |
|       586 | Yerevan              |       7 | Armenia        |
|       576 | Woodridge            |       8 | Australia      |
|       186 | Graz                 |       9 | Austria        |
|       307 | Linz                 |       9 | Austria        |
|       447 | Salzburg             |       9 | Austria        |
|        48 | Baku                 |      10 | Azerbaijan     |
|       505 | Sumqayit             |      10 | Azerbaijan     |
|        14 | al-Manama            |      11 | Bahrain        |
|       143 | Dhaka                |      12 | Bangladesh     |
|       234 | Jamalpur             |      12 | Bangladesh     |
|       525 | Tangail              |      12 | Bangladesh     |
|       339 | Mogiljov             |      13 | Belarus        |
|       340 | Molodetno            |      13 | Belarus        |
|       153 | El Alto              |      14 | Bolivia        |
|       501 | Sucre                |      14 | Bolivia        |
|        21 | Alvorada             |      15 | Brazil         |
|        25 | Angra dos Reis       |      15 | Brazil         |
|        26 | Anpolis              |      15 | Brazil         |
|        28 | Aparecida de Goinia  |      15 | Brazil         |
|        30 | Araatuba             |      15 | Brazil         |
|        44 | Bag                  |      15 | Brazil         |
|        66 | Belm                 |      15 | Brazil         |
|        83 | Blumenau             |      15 | Brazil         |
|        84 | Boa Vista            |      15 | Brazil         |
|        89 | Braslia              |      15 | Brazil         |
|       183 | Goinia               |      15 | Brazil         |
|       189 | Guaruj               |      15 | Brazil         |
|       190 | guas Lindas de Gois  |      15 | Brazil         |
|       215 | Ibirit               |      15 | Brazil         |
|       247 | Juazeiro do Norte    |      15 | Brazil         |
|       248 | Juiz de Fora         |      15 | Brazil         |
|       317 | Luzinia              |      15 | Brazil         |
|       328 | Maring               |      15 | Brazil         |
|       410 | Po                   |      15 | Brazil         |
|       413 | Poos de Caldas       |      15 | Brazil         |
|       431 | Rio Claro            |      15 | Brazil         |
|       456 | Santa Brbara dOeste  |      15 | Brazil         |
|       461 | Santo Andr           |      15 | Brazil         |
|       485 | So Bernardo do Campo |      15 | Brazil         |
|       486 | So Leopoldo          |      15 | Brazil         |
|       490 | Sorocaba             |      15 | Brazil         |
|       569 | Vila Velha           |      15 | Brazil         |
|       572 | Vitria de Santo Anto |      15 | Brazil         |
|        53 | Bandar Seri Begawan  |      16 | Brunei         |
|       436 | Ruse                 |      17 | Bulgaria       |
|       498 | Stara Zagora         |      17 | Bulgaria       |
|        60 | Battambang           |      18 | Cambodia       |
|       406 | Phnom Penh           |      18 | Cambodia       |
|        52 | Bamenda              |      19 | Cameroon       |
|       585 | Yaound               |      19 | Cameroon       |
|       179 | Gatineau             |      20 | Canada         |
|       196 | Halifax              |      20 | Canada         |
|       300 | Lethbridge           |      20 | Canada         |
|       313 | London               |      20 | Canada         |
|       383 | Oshawa               |      20 | Canada         |
|       430 | Richmond Hill        |      20 | Canada         |
|       565 | Vancouver            |      20 | Canada         |
|       363 | NDjamna              |      21 | Chad           |
|        27 | Antofagasta          |      22 | Chile          |
|       127 | Coquimbo             |      22 | Chile          |
|       428 | Rancagua             |      22 | Chile          |
|        46 | Baicheng             |      23 | China          |
|        47 | Baiyin               |      23 | China          |
|        80 | Binzhou              |      23 | China          |
|       109 | Changzhou            |      23 | China          |
|       136 | Datong               |      23 | China          |
|       139 | Daxian               |      23 | China          |
|       145 | Dongying             |      23 | China          |
|       157 | Emeishan             |      23 | China          |
|       159 | Enshi                |      23 | China          |
|       166 | Ezhou                |      23 | China          |
|       174 | Fuyu                 |      23 | China          |
|       175 | Fuzhou               |      23 | China          |
|       193 | Haining              |      23 | China          |
|       199 | Hami                 |      23 | China          |
|       207 | Hohhot               |      23 | China          |
|       210 | Huaian               |      23 | China          |
|       240 | Jinchang             |      23 | China          |
|       241 | Jining               |      23 | China          |
+-----------+----------------------+---------+----------------+
```
---
5. Obtener los detalles de los alquileres, incluyendo el cliente y el empleado que gestionó el alquiler.
```sql
    SELECT DISTINCT a.id_alquiler, a.fecha_alquiler, cl.id_cliente, CONCAT(cl.nombre, cl.apellidos) AS nombre_cliente, e.id_empleado, CONCAT(e.nombre, e.apellidos) AS nombre_empleado 
    FROM sakilacampus.alquiler a
    JOIN sakilacampus.cliente cl ON a.id_cliente = cl.id_cliente
    JOIN sakilacampus.empleado e ON a.id_empleado = e.id_empleado;

+-------------+---------------------+------------+-------------------+-------------+-----------------+
| id_alquiler | fecha_alquiler      | id_cliente | nombre_cliente    | id_empleado | nombre_empleado |
+-------------+---------------------+------------+-------------------+-------------+-----------------+
|       16048 | 2005-08-23 22:43:07 |        103 | GLADYSHAMILTON    |           1 | MikeHillyer     |
|       16045 | 2005-08-23 22:25:26 |         14 | BETTYWHITE        |           1 | MikeHillyer     |
|       16044 | 2005-08-23 22:24:39 |        468 | TIMCARY           |           1 | MikeHillyer     |
|       16042 | 2005-08-23 22:20:40 |        131 | MONICAHICKS       |           1 | MikeHillyer     |
|       16038 | 2005-08-23 22:14:31 |        172 | BERNICEWILLIS     |           1 | MikeHillyer     |
|       16035 | 2005-08-23 22:08:04 |         37 | PAMELABAKER       |           1 | MikeHillyer     |
|       16034 | 2005-08-23 22:06:34 |        502 | BRETTCORNWELL     |           1 | MikeHillyer     |
|       16031 | 2005-08-23 21:59:26 |        102 | CRYSTALFORD       |           1 | MikeHillyer     |
|       16029 | 2005-08-23 21:54:02 |        143 | LESLIEGORDON      |           1 | MikeHillyer     |
|       16026 | 2005-08-23 21:49:22 |        484 | ROBERTOVU         |           1 | MikeHillyer     |
|       16024 | 2005-08-23 21:46:47 |        473 | JORGEOLIVARES     |           1 | MikeHillyer     |
|       16023 | 2005-08-23 21:45:02 |        124 | SHEILAWELLS       |           1 | MikeHillyer     |
|       16022 | 2005-08-23 21:44:27 |        504 | NATHANIELADAM     |           1 | MikeHillyer     |
|       16021 | 2005-08-23 21:37:59 |        314 | GEORGELINTON      |           1 | MikeHillyer     |
|       16020 | 2005-08-23 21:34:33 |        311 | PAULTROUT         |           1 | MikeHillyer     |
|       16018 | 2005-08-23 21:27:35 |        439 | ALEXANDERFENNELL  |           1 | MikeHillyer     |
|       16017 | 2005-08-23 21:27:11 |        535 | JAVIERELROD       |           1 | MikeHillyer     |
|       16013 | 2005-08-23 21:17:17 |        462 | WARRENSHERROD     |           1 | MikeHillyer     |
|       16011 | 2005-08-23 21:11:33 |        389 | ALANKAHN          |           1 | MikeHillyer     |
|       16010 | 2005-08-23 21:10:24 |        173 | AUDREYRAY         |           1 | MikeHillyer     |
|       16008 | 2005-08-23 21:04:51 |        189 | LORETTACARPENTER  |           1 | MikeHillyer     |
|       16006 | 2005-08-23 21:01:09 |        533 | JESSIEMILAM       |           1 | MikeHillyer     |
|       16005 | 2005-08-23 21:00:22 |        466 | LEOEBERT          |           1 | MikeHillyer     |
|       16003 | 2005-08-23 20:47:28 |        577 | CLIFTONMALCOLM    |           1 | MikeHillyer     |
|       16002 | 2005-08-23 20:47:12 |         73 | BEVERLYBROOKS     |           1 | MikeHillyer     |
|       16001 | 2005-08-23 20:45:53 |        108 | TRACYCOLE         |           1 | MikeHillyer     |
|       16000 | 2005-08-23 20:44:36 |         71 | KATHYJAMES        |           1 | MikeHillyer     |
|       15998 | 2005-08-23 20:41:09 |        545 | JULIONOLAND       |           1 | MikeHillyer     |
|       15997 | 2005-08-23 20:40:31 |        447 | CLIFFORDBOWENS    |           1 | MikeHillyer     |
|       15996 | 2005-08-23 20:31:38 |        151 | MEGANPALMER       |           1 | MikeHillyer     |
|       15995 | 2005-08-23 20:29:56 |        377 | HOWARDFORTNER     |           1 | MikeHillyer     |
|       15992 | 2005-08-23 20:28:32 |        589 | TRACYHERRMANN     |           1 | MikeHillyer     |
|       15989 | 2005-08-23 20:24:36 |         96 | DIANAALEXANDER    |           1 | MikeHillyer     |
|       15988 | 2005-08-23 20:23:08 |        400 | BRYANHARDISON     |           1 | MikeHillyer     |
|       15986 | 2005-08-23 20:20:37 |        226 | MAUREENLITTLE     |           1 | MikeHillyer     |
|       15985 | 2005-08-23 20:20:23 |        179 | DANAHART          |           1 | MikeHillyer     |
|       15984 | 2005-08-23 20:16:27 |        495 | CHARLIEBESS       |           1 | MikeHillyer     |
|       15983 | 2005-08-23 20:13:38 |        464 | JEROMEKENYON      |           1 | MikeHillyer     |
|       15981 | 2005-08-23 20:12:17 |        489 | RICARDOMEADOR     |           1 | MikeHillyer     |
|       15979 | 2005-08-23 20:08:26 |        536 | FERNANDOCHURCHILL |           1 | MikeHillyer     |
|       15975 | 2005-08-23 20:06:23 |        174 | YVONNEWATKINS     |           1 | MikeHillyer     |
|       15972 | 2005-08-23 20:00:30 |         25 | DEBORAHWALKER     |           1 | MikeHillyer     |
|       15971 | 2005-08-23 19:59:33 |        187 | BRITTANYRILEY     |           1 | MikeHillyer     |
|       15970 | 2005-08-23 19:54:24 |        395 | JOHNNYTURPIN      |           1 | MikeHillyer     |
|       15969 | 2005-08-23 19:51:30 |        327 | LARRYTHRASHER     |           1 | MikeHillyer     |
|       15968 | 2005-08-23 19:51:29 |        257 | MARSHADOUGLAS     |           1 | MikeHillyer     |
|       15967 | 2005-08-23 19:50:06 |        257 | MARSHADOUGLAS     |           1 | MikeHillyer     |
|       15966 | 2006-02-14 15:16:03 |        374 | JEREMYHURTADO     |           1 | MikeHillyer     |
|       15963 | 2005-08-23 19:42:46 |        134 | EMMABOYD          |           1 | MikeHillyer     |
|       15962 | 2005-08-23 19:42:04 |        160 | ERINDUNN          |           1 | MikeHillyer     |
|       15961 | 2005-08-23 19:35:42 |        200 | JEANNELAWSON      |           1 | MikeHillyer     |
|       15959 | 2005-08-23 19:27:04 |        415 | GLENNPULLEN       |           1 | MikeHillyer     |
|       15958 | 2005-08-23 19:22:36 |        492 | LESTERKRAUS       |           1 | MikeHillyer     |
|       15957 | 2005-08-23 19:21:22 |        418 | JEFFEAST          |           1 | MikeHillyer     |
|       15955 | 2005-08-23 19:19:06 |        349 | JOEGILLILAND      |           1 | MikeHillyer     |
|       15954 | 2005-08-23 19:14:07 |        460 | LEONBOSTIC        |           1 | MikeHillyer     |
|       15953 | 2005-08-23 19:13:46 |        540 | TYRONEASHER       |           1 | MikeHillyer     |
|       15952 | 2005-08-23 19:11:29 |        224 | PEARLGARZA        |           1 | MikeHillyer     |
|       15951 | 2005-08-23 19:10:32 |        446 | THEODORECULP      |           1 | MikeHillyer     |
|       15946 | 2005-08-23 18:54:07 |        561 | IANSTILL          |           1 | MikeHillyer     |
|       15945 | 2005-08-23 18:51:41 |         43 | CHRISTINEROBERTS  |           1 | MikeHillyer     |
|       15943 | 2005-08-23 18:49:32 |        462 | WARRENSHERROD     |           1 | MikeHillyer     |
|       15941 | 2005-08-23 18:46:44 |        424 | KYLESPURLOCK      |           1 | MikeHillyer     |
|       15937 | 2005-08-23 18:43:22 |        194 | KRISTENCHAVEZ     |           1 | MikeHillyer     |
|       15936 | 2005-08-23 18:43:11 |        411 | NORMANCURRIER     |           1 | MikeHillyer     |
|       15935 | 2005-08-23 18:41:11 |        361 | LAWRENCELAWTON    |           1 | MikeHillyer     |
|       15931 | 2005-08-23 18:28:09 |        237 | TANYAGILBERT      |           1 | MikeHillyer     |
|       15930 | 2005-08-23 18:26:51 |        379 | CARLOSCOUGHLIN    |           1 | MikeHillyer     |
|       15929 | 2005-08-23 18:23:30 |        477 | DANPAINE          |           1 | MikeHillyer     |
|       15927 | 2005-08-23 18:23:11 |        401 | TONYCARRANZA      |           1 | MikeHillyer     |
|       15922 | 2005-08-23 18:07:31 |        263 | HILDAHOPKINS      |           1 | MikeHillyer     |
|       15920 | 2005-08-23 18:05:10 |        212 | WILMARICHARDS     |           1 | MikeHillyer     |
|       15919 | 2005-08-23 18:01:31 |        497 | GILBERTSLEDGE     |           1 | MikeHillyer     |
|       15917 | 2005-08-23 17:57:28 |        589 | TRACYHERRMANN     |           1 | MikeHillyer     |
|       15914 | 2005-08-23 17:49:26 |        557 | FELIXGAFFNEY      |           1 | MikeHillyer     |
|       15911 | 2005-08-23 17:44:53 |        582 | ANDYVANHORN       |           1 | MikeHillyer     |
|       15909 | 2005-08-23 17:42:42 |        452 | TOMMILNER         |           1 | MikeHillyer     |
|       15908 | 2005-08-23 17:42:00 |        135 | JUANITAMASON      |           1 | MikeHillyer     |
|       15907 | 2005-08-23 17:39:35 |          2 | PATRICIAJOHNSON   |           1 | MikeHillyer     |
|       15903 | 2005-08-23 17:30:40 |        267 | MARGIEWADE        |           1 | MikeHillyer     |
|       15902 | 2005-08-23 17:28:03 |        172 | BERNICEWILLIS     |           1 | MikeHillyer     |
|       15900 | 2005-08-23 17:16:30 |        562 | WALLACESLONE      |           1 | MikeHillyer     |
|       15897 | 2005-08-23 17:12:31 |         15 | HELENHARRIS       |           1 | MikeHillyer     |
|       15895 | 2005-08-23 17:09:31 |        342 | HAROLDMARTINO     |           1 | MikeHillyer     |
|       15894 | 2006-02-14 15:16:03 |        168 | REGINABERRY       |           1 | MikeHillyer     |
|       15892 | 2005-08-23 17:01:00 |        174 | YVONNEWATKINS     |           1 | MikeHillyer     |
|       15891 | 2005-08-23 17:00:12 |         52 | JULIESANCHEZ      |           1 | MikeHillyer     |
|       15890 | 2005-08-23 16:58:12 |         87 | WANDAPATTERSON    |           1 | MikeHillyer     |
|       15889 | 2005-08-23 16:57:43 |        137 | RHONDAKENNEDY     |           1 | MikeHillyer     |
|       15888 | 2005-08-23 16:56:14 |        321 | KEVINSCHULER      |           1 | MikeHillyer     |
|       15885 | 2005-08-23 16:50:43 |        565 | JAIMENETTLES      |           1 | MikeHillyer     |
|       15884 | 2005-08-23 16:45:28 |         81 | ANDREAHENDERSON   |           1 | MikeHillyer     |
|       15883 | 2005-08-23 16:44:56 |        550 | GUYBROWNLEE       |           1 | MikeHillyer     |
|       15881 | 2005-08-23 16:44:25 |        383 | MARTINBALES       |           1 | MikeHillyer     |
|       15876 | 2005-08-23 16:32:10 |         87 | WANDAPATTERSON    |           1 | MikeHillyer     |
|       15875 | 2006-02-14 15:16:03 |         41 | STEPHANIEMITCHELL |           1 | MikeHillyer     |
|       15874 | 2005-08-23 16:30:55 |        132 | ESTHERCRAWFORD    |           1 | MikeHillyer     |
|       15872 | 2005-08-23 16:27:24 |        212 | WILMARICHARDS     |           1 | MikeHillyer     |
|       15869 | 2005-08-23 16:22:20 |        357 | KEITHRICO         |           1 | MikeHillyer     |
|       15862 | 2006-02-14 15:16:03 |        215 | JESSIEBANKS       |           1 | MikeHillyer     |
+-------------+---------------------+------------+-------------------+-------------+-----------------+
```
---
6. Encontrar todas las películas que se encuentran en un almacén específico.
```sql
    SELECT DISTINCT a.id_almacen, p.id_pelicula, p.titulo
    FROM sakilacampus.pelicula p
    JOIN sakilacampus.inventario i ON p.id_pelicula = i.id_pelicula
    JOIN sakilacampus.almacen a ON i.id_almacen = a.id_almacen
    WHERE a.id_almacen = 1;
+------------+-------------+-----------------------------+
| id_almacen | id_pelicula | titulo                      |
+------------+-------------+-----------------------------+
|          1 |           1 | ACADEMY DINOSAUR            |
|          1 |           4 | AFFAIR PREJUDICE            |
|          1 |           6 | AGENT TRUMAN                |
|          1 |           7 | AIRPLANE SIERRA             |
|          1 |           9 | ALABAMA DEVIL               |
|          1 |          10 | ALADDIN CALENDAR            |
|          1 |          11 | ALAMO VIDEOTAPE             |
|          1 |          12 | ALASKA PHANTOM              |
|          1 |          15 | ALIEN CENTER                |
|          1 |          16 | ALLEY EVOLUTION             |
|          1 |          17 | ALONE TRIP                  |
|          1 |          18 | ALTER VICTORY               |
|          1 |          19 | AMADEUS HOLY                |
|          1 |          20 | AMELIE HELLFIGHTERS         |
|          1 |          21 | AMERICAN CIRCUS             |
|          1 |          22 | AMISTAD MIDSUMMER           |
|          1 |          23 | ANACONDA CONFESSIONS        |
|          1 |          24 | ANALYZE HOOSIERS            |
|          1 |          25 | ANGELS LIFE                 |
|          1 |          26 | ANNIE IDENTITY              |
|          1 |          27 | ANONYMOUS HUMAN             |
|          1 |          28 | ANTHEM LUKE                 |
|          1 |          29 | ANTITRUST TOMATOES          |
|          1 |          30 | ANYTHING SAVANNAH           |
|          1 |          31 | APACHE DIVINE               |
|          1 |          35 | ARACHNOPHOBIA ROLLERCOASTER |
|          1 |          37 | ARIZONA BANG                |
|          1 |          39 | ARMAGEDDON LOST             |
|          1 |          43 | ATLANTIS CAUSE              |
|          1 |          44 | ATTACKS HATE                |
|          1 |          45 | ATTRACTION NEWTON           |
|          1 |          48 | BACKLASH UNDEFEATED         |
|          1 |          49 | BADMAN DAWN                 |
|          1 |          50 | BAKED CLEOPATRA             |
|          1 |          51 | BALLOON HOMEWARD            |
|          1 |          53 | BANG KWAI                   |
|          1 |          54 | BANGER PINOCCHIO            |
|          1 |          55 | BARBARELLA STREETCAR        |
|          1 |          56 | BAREFOOT MANCHURIAN         |
|          1 |          57 | BASIC EASY                  |
|          1 |          59 | BEAR GRACELAND              |
|          1 |          60 | BEAST HUNCHBACK             |
|          1 |          61 | BEAUTY GREASE               |
|          1 |          63 | BEDAZZLED MARRIED           |
|          1 |          66 | BENEATH RUSH                |
|          1 |          67 | BERETS AGENT                |
|          1 |          68 | BETRAYED REAR               |
|          1 |          69 | BEVERLY OUTLAW              |
|          1 |          70 | BIKINI BORROWERS            |
|          1 |          72 | BILL OTHERS                 |
|          1 |          73 | BINGO TALENTED              |
|          1 |          74 | BIRCH ANTITRUST             |
|          1 |          76 | BIRDCAGE CASPER             |
|          1 |          77 | BIRDS PERDITION             |
|          1 |          78 | BLACKOUT PRIVATE            |
|          1 |          79 | BLADE POLISH                |
|          1 |          80 | BLANKET BEVERLY             |
|          1 |          81 | BLINDNESS GUN               |
|          1 |          82 | BLOOD ARGONAUTS             |
|          1 |          83 | BLUES INSTINCT              |
|          1 |          84 | BOILED DARES                |
|          1 |          86 | BOOGIE AMELIE               |
|          1 |          89 | BORROWERS BEDAZZLED         |
|          1 |          90 | BOULEVARD MOB               |
|          1 |          91 | BOUND CHEAPER               |
|          1 |          92 | BOWFINGER GABLES            |
|          1 |          94 | BRAVEHEART HUMAN            |
|          1 |          95 | BREAKFAST GOLDFINGER        |
|          1 |          96 | BREAKING HOME               |
|          1 |          97 | BRIDE INTRIGUE              |
|          1 |          98 | BRIGHT ENCOUNTERS           |
|          1 |          99 | BRINGING HYSTERICAL         |
|          1 |         100 | BROOKLYN DESERT             |
|          1 |         101 | BROTHERHOOD BLANKET         |
|          1 |         103 | BUCKET BROTHERHOOD          |
|          1 |         105 | BULL SHAWSHANK              |
|          1 |         106 | BULWORTH COMMANDMENTS       |
|          1 |         109 | BUTTERFLY CHOCOLAT          |
|          1 |         110 | CABIN FLASH                 |
|          1 |         112 | CALENDAR GUNFIGHT           |
|          1 |         114 | CAMELOT VACATION            |
|          1 |         115 | CAMPUS REMEMBER             |
|          1 |         116 | CANDIDATE PERDITION         |
|          1 |         117 | CANDLES GRAPES              |
|          1 |         118 | CANYON STOCK                |
|          1 |         119 | CAPER MOTIONS               |
|          1 |         120 | CARIBBEAN LIBERTY           |
|          1 |         121 | CAROL TEXAS                 |
|          1 |         122 | CARRIE BUNCH                |
|          1 |         123 | CASABLANCA SUPER            |
|          1 |         127 | CAT CONEHEADS               |
|          1 |         129 | CAUSE DATE                  |
|          1 |         130 | CELEBRITY HORN              |
|          1 |         131 | CENTER DINOSAUR             |
|          1 |         132 | CHAINSAW UPTOWN             |
|          1 |         133 | CHAMBER ITALIAN             |
|          1 |         135 | CHANCE RESURRECTION         |
|          1 |         136 | CHAPLIN LICENSE             |
|          1 |         138 | CHARIOTS CONSPIRACY         |
|          1 |         139 | CHASING FIGHT               |
+------------+-------------+-----------------------------+

```
---
7. Listar los nombres y apellidos de los empleados junto con las direcciones de los almacenes en los que trabajan.
```sql
    SELECT DISTINCT CONCAT(e.nombre, e.apellidos) AS nombre_empleado, d.direccion AS direccion_almacen
    FROM sakilacampus.empleado e
    LEFT JOIN sakilacampus.almacen a ON e.id_almacen = a.id_almacen
    LEFT JOIN sakilacampus.direccion d ON a.id_direccion = d.id_direccion;

+-----------------+--------------------+
| nombre_empleado | direccion_almacen  |
+-----------------+--------------------+
| MikeHillyer     | 28 MySQL Boulevard |
| JonStephens     | 28 MySQL Boulevard |
| PepeSpilberg    | 28 MySQL Boulevard |
| AdaByron        | 47 MySakila Drive  |
| RingoRooksby    | 47 MySakila Drive  |
+-----------------+--------------------+
```
---
8. Obtener una lista de pagos realizados, incluyendo el cliente, el empleado que registró el pago y el alquiler correspondiente.
```sql
    SELECT DISTINCT p.id_pago, CONCAT(cl.nombre, cl.apellidos) AS nombre_cliente, CONCAT(e.nombre, e.apellidos) AS nombre_empleado
    FROM sakilacampus.pago p
    JOIN sakilacampus.empleado e ON p.id_empleado = e.id_empleado
    JOIN sakilacampus.almacen a ON e.id_almacen = a.id_almacen
    JOIN sakilacampus.cliente cl ON a.id_almacen = cl.id_almacen;

+---------+-------------------+-----------------+
| id_pago | nombre_cliente    | nombre_empleado |
+---------+-------------------+-----------------+
|   16049 | BARBARAJONES      | JonStephens     |
|   16049 | JENNIFERDAVIS     | JonStephens     |
|   16049 | SUSANWILSON       | JonStephens     |
|   16049 | MARGARETMOORE     | JonStephens     |
|   16049 | LISAANDERSON      | JonStephens     |
|   16049 | KARENJACKSON      | JonStephens     |
|   16049 | BETTYWHITE        | JonStephens     |
|   16049 | SANDRAMARTIN      | JonStephens     |
|   16049 | CAROLGARCIA       | JonStephens     |
|   16049 | SHARONROBINSON    | JonStephens     |
|   16049 | SARAHLEWIS        | JonStephens     |
|   16049 | KIMBERLYLEE       | JonStephens     |
|   16049 | JESSICAHALL       | JonStephens     |
|   16049 | SHIRLEYALLEN      | JonStephens     |
|   16049 | ANGELAHERNANDEZ   | JonStephens     |
|   16049 | BRENDAWRIGHT      | JonStephens     |
|   16049 | ANNAHILL          | JonStephens     |
|   16049 | REBECCASCOTT      | JonStephens     |
|   16049 | VIRGINIAGREEN     | JonStephens     |
|   16049 | KATHLEENADAMS     | JonStephens     |
|   16049 | AMANDACARTER      | JonStephens     |
|   16049 | CAROLYNPEREZ      | JonStephens     |
|   16049 | CHRISTINEROBERTS  | JonStephens     |
|   16049 | CATHERINECAMPBELL | JonStephens     |
|   16049 | JOYCEEDWARDS      | JonStephens     |
|   16049 | DORISREED         | JonStephens     |
|   16049 | EVELYNMORGAN      | JonStephens     |
|   16049 | KATHERINERIVERA   | JonStephens     |
|   16049 | JUDITHCOX         | JonStephens     |
|   16049 | ROSEHOWARD        | JonStephens     |
|   16049 | JANICEWARD        | JonStephens     |
|   16049 | JUDYGRAY          | JonStephens     |
|   16049 | CHRISTINARAMIREZ  | JonStephens     |
|   16049 | THERESAWATSON     | JonStephens     |
|   16049 | BEVERLYBROOKS     | JonStephens     |
|   16049 | TAMMYSANDERS      | JonStephens     |
|   16049 | IRENEPRICE        | JonStephens     |
|   16049 | JANEBENNETT       | JonStephens     |
|   16049 | SARAPERRY         | JonStephens     |
|   16049 | ANNEPOWELL        | JonStephens     |
|   16049 | JACQUELINELONG    | JonStephens     |
|   16049 | BONNIEHUGHES      | JonStephens     |
|   16049 | RUBYWASHINGTON    | JonStephens     |
|   16049 | LOISBUTLER        | JonStephens     |
|   16049 | TINASIMMONS       | JonStephens     |
|   16049 | PAULABRYANT       | JonStephens     |
|   16049 | ANNIERUSSELL      | JonStephens     |
|   16049 | EMILYDIAZ         | JonStephens     |
|   16049 | EDNAWEST          | JonStephens     |
|   16049 | TIFFANYJORDAN     | JonStephens     |
|   16049 | ROSAREYNOLDS      | JonStephens     |
|   16049 | CINDYFISHER       | JonStephens     |
|   16049 | GRACEELLIS        | JonStephens     |
|   16049 | SYLVIAORTIZ       | JonStephens     |
|   16049 | SHANNONFREEMAN    | JonStephens     |
|   16049 | ELAINESTEVENS     | JonStephens     |
|   16049 | MONICAHICKS       | JonStephens     |
|   16049 | ESTHERCRAWFORD    | JonStephens     |
|   16049 | JUANITAMASON      | JonStephens     |
|   16049 | ANITAMORALES      | JonStephens     |
|   16049 | RHONDAKENNEDY     | JonStephens     |
|   16049 | JOANNEROBERTSON   | JonStephens     |
|   16049 | DANIELLEDANIELS   | JonStephens     |
|   16049 | MEGANPALMER       | JonStephens     |
|   16049 | SUZANNENICHOLS    | JonStephens     |
|   16049 | MICHELEGRANT      | JonStephens     |
|   16049 | DARLENEROSE       | JonStephens     |
|   16049 | ERINDUNN          | JonStephens     |
|   16049 | LAURENHUDSON      | JonStephens     |
|   16049 | JOANNGARDNER      | JonStephens     |
|   16049 | LORRAINESTEPHENS  | JonStephens     |
|   16049 | SALLYPIERCE       | JonStephens     |
|   16049 | ERICAMATTHEWS     | JonStephens     |
|   16049 | DOLORESWAGNER     | JonStephens     |
|   16049 | YVONNEWATKINS     | JonStephens     |
|   16049 | SAMANTHADUNCAN    | JonStephens     |
|   16049 | MARIONSNYDER      | JonStephens     |
|   16049 | STACYCUNNINGHAM   | JonStephens     |
|   16049 | ANABRADLEY        | JonStephens     |
|   16049 | IDAANDREWS        | JonStephens     |
|   16049 | HOLLYFOX          | JonStephens     |
|   16049 | BRITTANYRILEY     | JonStephens     |
|   16049 | YOLANDAWEAVER     | JonStephens     |
|   16049 | KATIEELLIOTT      | JonStephens     |
|   16049 | KRISTENCHAVEZ     | JonStephens     |
|   16049 | SUEPETERS         | JonStephens     |
|   16049 | ELSIEKELLEY       | JonStephens     |
|   16049 | BETHFRANKLIN      | JonStephens     |
|   16049 | JEANNELAWSON      | JonStephens     |
|   16049 | CARLAGUTIERREZ    | JonStephens     |
|   16049 | EILEENCARR        | JonStephens     |
|   16049 | TONYACHAPMAN      | JonStephens     |
|   16049 | ELLAOLIVER        | JonStephens     |
|   16049 | WILMARICHARDS     | JonStephens     |
|   16049 | JESSIEBANKS       | JonStephens     |
|   16049 | AGNESBISHOP       | JonStephens     |
|   16049 | WILLIEHOWELL      | JonStephens     |
|   16049 | CHARLENEALVAREZ   | JonStephens     |
|   16049 | DELORESHANSEN     | JonStephens     |
|   16049 | PEARLGARZA        | JonStephens     |
+---------+-------------------+-----------------+

```
---
9. Listar las películas y los idiomas en los que están disponibles.
```sql
    SELECT DISTINCT p.id_pelicula, p.titulo, i.nombre
    FROM sakilacampus.pelicula p
    JOIN sakilacampus.idioma i ON p.id_idioma = i.id_idioma;

+-------------+-----------------------------+---------+
| id_pelicula | titulo                      | nombre  |
+-------------+-----------------------------+---------+
|           1 | ACADEMY DINOSAUR            | English |
|           2 | ACE GOLDFINGER              | English |
|           3 | ADAPTATION HOLES            | English |
|           4 | AFFAIR PREJUDICE            | English |
|           5 | AFRICAN EGG                 | English |
|           6 | AGENT TRUMAN                | English |
|           7 | AIRPLANE SIERRA             | English |
|           8 | AIRPORT POLLOCK             | English |
|           9 | ALABAMA DEVIL               | English |
|          10 | ALADDIN CALENDAR            | English |
|          11 | ALAMO VIDEOTAPE             | English |
|          12 | ALASKA PHANTOM              | English |
|          13 | ALI FOREVER                 | English |
|          14 | ALICE FANTASIA              | English |
|          15 | ALIEN CENTER                | English |
|          16 | ALLEY EVOLUTION             | English |
|          17 | ALONE TRIP                  | English |
|          18 | ALTER VICTORY               | English |
|          19 | AMADEUS HOLY                | English |
|          20 | AMELIE HELLFIGHTERS         | English |
|          21 | AMERICAN CIRCUS             | English |
|          22 | AMISTAD MIDSUMMER           | English |
|          23 | ANACONDA CONFESSIONS        | English |
|          24 | ANALYZE HOOSIERS            | English |
|          25 | ANGELS LIFE                 | English |
|          26 | ANNIE IDENTITY              | English |
|          27 | ANONYMOUS HUMAN             | English |
|          28 | ANTHEM LUKE                 | English |
|          29 | ANTITRUST TOMATOES          | English |
|          30 | ANYTHING SAVANNAH           | English |
|          31 | APACHE DIVINE               | English |
|          32 | APOCALYPSE FLAMINGOS        | English |
|          33 | APOLLO TEEN                 | English |
|          34 | ARABIA DOGMA                | English |
|          35 | ARACHNOPHOBIA ROLLERCOASTER | English |
|          36 | ARGONAUTS TOWN              | English |
|          37 | ARIZONA BANG                | English |
|          38 | ARK RIDGEMONT               | English |
|          39 | ARMAGEDDON LOST             | English |
|          40 | ARMY FLINTSTONES            | English |
|          41 | ARSENIC INDEPENDENCE        | English |
|          42 | ARTIST COLDBLOODED          | English |
|          43 | ATLANTIS CAUSE              | English |
|          44 | ATTACKS HATE                | English |
|          45 | ATTRACTION NEWTON           | English |
|          46 | AUTUMN CROW                 | English |
|          47 | BABY HALL                   | English |
|          48 | BACKLASH UNDEFEATED         | English |
|          49 | BADMAN DAWN                 | English |
|          50 | BAKED CLEOPATRA             | English |
|          51 | BALLOON HOMEWARD            | English |
|          52 | BALLROOM MOCKINGBIRD        | English |
|          53 | BANG KWAI                   | English |
|          54 | BANGER PINOCCHIO            | English |
|          55 | BARBARELLA STREETCAR        | English |
|          56 | BAREFOOT MANCHURIAN         | English |
|          57 | BASIC EASY                  | English |
|          58 | BEACH HEARTBREAKERS         | English |
|          59 | BEAR GRACELAND              | English |
|          60 | BEAST HUNCHBACK             | English |
|          61 | BEAUTY GREASE               | English |
|          62 | BED HIGHBALL                | English |
|          63 | BEDAZZLED MARRIED           | English |
|          64 | BEETHOVEN EXORCIST          | English |
|          65 | BEHAVIOR RUNAWAY            | English |
|          66 | BENEATH RUSH                | English |
|          67 | BERETS AGENT                | English |
|          68 | BETRAYED REAR               | English |
|          69 | BEVERLY OUTLAW              | English |
|          70 | BIKINI BORROWERS            | English |
|          71 | BILKO ANONYMOUS             | English |
|          72 | BILL OTHERS                 | English |
|          73 | BINGO TALENTED              | English |
|          74 | BIRCH ANTITRUST             | English |
|          75 | BIRD INDEPENDENCE           | English |
|          76 | BIRDCAGE CASPER             | English |
|          77 | BIRDS PERDITION             | English |
|          78 | BLACKOUT PRIVATE            | English |
|          79 | BLADE POLISH                | English |
|          80 | BLANKET BEVERLY             | English |
|          81 | BLINDNESS GUN               | English |
|          82 | BLOOD ARGONAUTS             | English |
|          83 | BLUES INSTINCT              | English |
|          84 | BOILED DARES                | English |
|          85 | BONNIE HOLOCAUST            | English |
|          86 | BOOGIE AMELIE               | English |
|          87 | BOONDOCK BALLROOM           | English |
|          88 | BORN SPINAL                 | English |
|          89 | BORROWERS BEDAZZLED         | English |
|          90 | BOULEVARD MOB               | English |
|          91 | BOUND CHEAPER               | English |
|          92 | BOWFINGER GABLES            | English |
|          93 | BRANNIGAN SUNRISE           | English |
|          94 | BRAVEHEART HUMAN            | English |
|          95 | BREAKFAST GOLDFINGER        | English |
|          96 | BREAKING HOME               | English |
|          97 | BRIDE INTRIGUE              | English |
|          98 | BRIGHT ENCOUNTERS           | English |
|          99 | BRINGING HYSTERICAL         | English |
|         100 | BROOKLYN DESERT             | English |
+-------------+-----------------------------+---------+

```
---
10. Encontrar todos los empleados y los almacenes que gestionan.
```sql
    SELECT DISTINCT a.id_almacen, e.id_empleado, CONCAT(e.nombre, ' ', e.apellidos) AS nombre_empleado 
    FROM sakilacampus.empleado e
    JOIN sakilacampus.almacen a ON e.id_almacen = a.id_almacen;

+------------+-------------+-----------------+
| id_almacen | id_empleado | nombre_empleado |
+------------+-------------+-----------------+
|          2 |           1 | Mike Hillyer    |
|          2 |           2 | Jon Stephens    |
|          2 |           3 | Pepe Spilberg   |
|          1 |           4 | Ada Byron       |
|          1 |           5 | Ringo Rooksby   |
+------------+-------------+-----------------+

```
---
11. Obtener los títulos de las películas que nunca han sido alquiladas.
```sql
    SELECT DISTINCT p.id_pelicula, p.titulo
    FROM sakilacampus.pelicula p
    JOIN sakilacampus.inventario i ON p.id_pelicula = i.id_pelicula
    WHERE i.id_inventario NOT IN (
        SELECT a.id_inventario
        FROM sakilacampus.alquiler a
    )

+-------------+------------------+
| id_pelicula | titulo           |
+-------------+------------------+
|           1 | ACADEMY DINOSAUR |
+-------------+------------------+
```
---
12. Listar los empleados que trabajan en el mismo almacén que el empleado con id_empleado = 1.
```sql
    SELECT DISTINCT CONCAT(e.nombre, e.apellidos) AS nombre_empleado
    FROM sakilacampus.empleado e
    WHERE e.id_almacen IN (
        SELECT a.id_almacen
        FROM sakilacampus.almacen a
        JOIN sakilacampus.empleado e ON a.id_almacen = e.id_almacen
        WHERE e.id_empleado = 1 
    );

+-----------------+
| nombre_empleado |
+-----------------+
| MikeHillyer     |
| JonStephens     |
| PepeSpilberg    |
+-----------------+
```
---
13. Encontrar el nombre de las ciudades que no tienen ningún cliente registrado.
```sql
    SELECT DISTINCT c.nombre
    FROM sakilacampus.ciudad c
    JOIN sakilacampus.direccion d ON c.id_ciudad = d.id_ciudad
    JOIN sakilacampus.almacen a ON d.id_direccion = a.id_direccion
    WHERE a.id_almacen NOT IN (
        SELECT cl.id_almacen
        FROM sakilacampus.cliente cl
    );
```
---
14. Obtener los nombres y apellidos de los actores que han participado en más de 10 películas.(having)
```sql

```
---
15. Encontrar los nombres y apellidos de los clientes que han realizado un pago mayor a 100.
```sql

```
---
16. Listar los títulos de las películas lanzadas en el mismo año que la película con id_pelicula = 2.
```sql

```
---