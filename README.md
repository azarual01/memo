
# memo-sql    Azarual El-Ghazi

Description:
- Le SQL (Structured Query Language) est un langage permettant de communiquer avec une base de données. Ce langage informatique est notamment très utilisé par les développeurs web pour communiquer avec les données d’un site web. SQL.sh recense des cours de SQL et des explications sur les principales commandes pour lire, insérer, modifier et supprimer des données dans une base.

- Système de gestion de base de données (SGBD)
Chaque SGBD possède ses propres spécificités et caractéristiques. Pour présenter ces différences, les logiciels de gestion de bases de données sont cités, tels que : MySQL, PostgreSQL, SQLite, Microsoft SQL Server ou encore Oracle.
Des SGBD de type NoSQL sont également présentés, tel que Cassandra, Redis ou MongoDB.

    
- COMMANDE BASIQUE:
  - SELECT:
  
  	L’utilisation la plus courante de SQL consiste à lire des données issues de la base de données. Cela s’effectue grâce à la commande SELECT, qui retourne des enregistrements dans un tableau de résultat. Cette commande peut sélectionner une ou plusieurs colonnes d’une table.
	
	Exemples:
  
    > 	- SELECT nom_du_champ FROM nom_du_tableau;
    >	- SELECT ville FROM client;
    >	- SELECT prenom, nom FROM client;
    >   - SELECT * FROM client;
    >   - SELECT * FROM table WHERE condition GROUP BY expression HAVING condition { UNION | INTERSECT | EXCEPT } ORDER BY expression LIMIT count OFFSET start;


  - INSERT INTO: 

	L’insertion de données dans une table s’effectue à l’aide de la commande INSERT INTO. Cette commande permet au choix d’inclure une seule ligne à la base existante ou plusieurs lignes d’un coup.
	
	Exemples:
	
    > 	- INSERT INTO table VALUES ('valeur 1', 'valeur 2', ...);
    >	- INSERT INTO table (nom_colonne_1, nom_colonne_2, ...) VALUES ('valeur 1', 'valeur 2', ...);
    >	- INSERT INTO client (prenom, nom, ville, age) VALUES ('Rébecca', 'Armand', 'Saint-Didier-des-Bois', 24),('Aimée', 'Hebert', 'Marigny-le-Châtel', 36),
 ('Marielle', 'Ribeiro', 'Maillères', 27),('Hilaire', 'Savary', 'Conie-Molitard', 58);
 
 
  - UPDATE:
  
  	La commande UPDATE permet d’effectuer des modifications sur des lignes existantes. Très souvent cette commande est utilisée avec WHERE pour spécifier sur quelles lignes doivent porter la ou les modifications.
	
	Exemples:
  
    > 	- UPDATE table SET nom_colonne_1 = 'nouvelle valeur' WHERE condition;
    >	- UPDATE table SET colonne_1 = 'valeur 1', colonne_2 = 'valeur 2', colonne_3 = 'valeur 3' WHERE condition;
    >	- UPDATE client SET rue = '49 Rue Ameline',   ville = 'Saint-Eustache-la-Forêt',   code_postal = '76210' WHERE id = 2;
    >	- UPDATE client SET pays = 'FRANCE';
 

  - DELETE:
  
  	La commande DELETE en SQL permet de supprimer des lignes dans une table. En utilisant cette commande associé à WHERE il est possible de sélectionner les lignes concernées qui seront supprimées.
	
	Exemples:
  
    > 	- DELETE FROM `nom_du_tableau` WHERE condition;
    >	- DELETE FROM `utilisateur` WHERE `id` = 1;
    >	- DELETE FROM `utilisateur` WHERE `date_inscription` < '2012-04-10';
    >	- DELETE FROM `utilisateur`;
    >	- TRUNCATE TABLE `utilisateur`;

  - CREATE DATABASE:
  
	La création d’une base de données en SQL est possible en ligne de commande. Même si les systèmes de gestion de base de données (SGBD) sont souvent utilisés pour créer une base, il convient de connaître la commande à utiliser, qui est très simple.
	
	Exemples:
	
   >    - CREATE DATABASE ma_base;
   >    - CREATE DATABASE IF NOT EXISTS ma_base;


  - DROP DATABASE:

	En SQL, la commande DROP DATABASE permet de supprimer totalement une base de données et tout ce qu’elle contient. Cette commande est à utiliser avec beaucoup d’attention car elle permet de supprimer tout ce qui est inclus dans une base: les tables, les données, les index …
	
	Exemples:
	
  >    - DROP DATABASE ma_base;
  >    - DROP DATABASE IF EXISTS ma_base;
  >    - DROP TABLE nom_table;
  >    - DROP TABLE client_2009;


  - ALTER TABLE:

	La commande ALTER TABLE en SQL permet de modifier une table existante. Idéal pour ajouter une colonne, supprimer une colonne ou modifier une colonne existante, par exemple pour changer le type.
	
	Exemples:
	
  >    - ALTER TABLE nom_table instruction;
  >    - ALTER TABLE nom_table ADD nom_colonne type_donnees;
  >    - ALTER TABLE utilisateur ADD adresse_rue VARCHAR(255);
  >    - ALTER TABLE nom_table DROP nom_colonne;
  >    - ALTER TABLE nom_table DROP COLUMN nom_colonne;
  >    - ALTER TABLE nom_table MODIFY nom_colonne type_donnees;
  >    - ALTER TABLE nom_table CHANGE colonne_ancien_nom colonne_nouveau_nom type_donnees;

- CREATE USERS AND GRANT PERMISSIONS:
	
	exemples:
	
  >   - CREATE USER 'sammy'@'localhost' IDENTIFIED BY 'password';
  >   - GRANT PRIVILEGE ON database.table TO 'username'@'host';
  >   - GRANT CREATE, ALTER, DROP, INSERT, UPDATE, DELETE, SELECT, REFERENCES, RELOAD on *.* TO 'sammy'@'localhost' WITH GRANT OPTION;
  >   - GRANT ALL PRIVILEGES ON *.* TO 'sammy'@'localhost' WITH GRANT OPTION;
  >   - REVOKE type_of_permission ON database_name.table_name FROM 'username'@'host';
  >   - SHOW GRANTS FOR 'username'@'host';
  >   - DROP USER 'username'@'localhost';
	
	#DOCUMENTATION:

  >   - https://www.digitalocean.com/community/tutorials/how-to-create-a-new-user-and-grant-permissions-in-mysql


- FUNCTIONS:

	- AVG():
	
	>  La fonction d’agrégation AVG() dans le langage SQL permet de calculer une valeur moyenne sur un ensemble d’enregistrement de type numérique et non nul.
	
	Exemple:
	
		- SELECT AVG(nom_colonne) FROM nom_table


	- COUNT():
	
	>  En SQL, la fonction d’agrégation COUNT() permet de compter le nombre d’enregistrement dans une table. Connaître le nombre de lignes dans une table est très pratique dans de nombreux cas, par exemple pour savoir combien d’utilisateurs sont présents dans une table ou pour connaître le nombre de commentaires sur un article.
	
	Exemple:
	
	- SELECT COUNT(*) FROM table;
	- SELECT COUNT(nom_colonne) FROM table;


	- MAX():
	
	>  Dans le langage SQL, la fonction d’agrégation MAX() permet de retourner la valeur maximale d’une colonne dans un set d’enregistrement. La fonction peut s’appliquée à des données numériques ou alphanumériques. Il est par exemple possible de rechercher le produit le plus cher dans une table d’une boutique en ligne.
	
	Exemple:
	
	- SELECT MAX(nom_colonne) FROM table;
	- SELECT colonne1, MAX(colonne2) FROM table GROUP BY colonne1;

	- ROUND():
	
	>  Dans le langage SQL la fonction ROUND() permet d’arrondir un résultat numérique. Cette fonction permet soit d’arrondir sans utiliser de décimal pour retourner un nombre entier (c’est-à-dire : aucun chiffre après la virgule), ou de choisir le nombre de chiffre après la virgule.
	
	Exemple:
	
	- SELECT ROUND(nom_colonne) FROM `table`;
	- SELECT ROUND(nom_colonne, 2) FROM `table`;


- FILTERS AND CONDITIONS:

	- WHERE:
	
	>  La commande WHERE dans une requête SQL permet d’extraire les lignes d’une base de données qui respectent une condition. Cela permet d’obtenir uniquement les informations désirées.

	EXEMPLES:
	
	>  - SELECT nom_colonnes FROM nom_table WHERE condition;
	>  - SELECT * FROM client WHERE ville = 'paris';

	- AND & OR:
	
	>  Une requête SQL peut être restreinte à l’aide de la condition WHERE. Les opérateurs logiques AND et OR peuvent être utilisées au sein de la commande WHERE pour combiner des conditions.

	EXEMPLES:
	
	>  - SELECT nom_colonnes FROM nom_table WHERE condition1 AND condition2;
	>  - SELECT nom_colonnes FROM nom_table  WHERE condition1 OR condition2;
	>  - SELECT nom_colonnes FROM nom_table  WHERE condition1 AND (condition2 OR condition3);
	>  - SELECT * FROM produit WHERE categorie = 'informatique' AND stock < 20;
	>  - SELECT * FROM produit WHERE nom = 'ordinateur' OR nom = 'clavier';
	>  - SELECT * FROM produit WHERE ( categorie = 'informatique' AND stock < 20 ) OR ( categorie = 'fourniture' AND stock < 200 );

