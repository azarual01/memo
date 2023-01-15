
# Mémo-sql    Azarual El-Ghazi

Description :
- Le SQL (Structured Query Language) est un langage permettant de communiquer avec une base de données. Ce langage informatique est notamment très utilisé par les développeurs web pour communiquer avec les données d’un site web. SQL.sh recense des cours de SQL et des explications sur les principales commandes pour lire, insérer, modifier et supprimer des données dans une base.

- Système de gestion de base de données (SGBD)
Chaque SGBD possède ses propres spécificités et caractéristiques. Pour présenter ces différences, les logiciels de gestion de bases de données sont cités, tels que : MySQL, PostgreSQL, SQLite, Microsoft SQL Server ou encore Oracle.
Des SGBD de type NoSQL sont également présentés, tel que Cassandra, Redis ou MongoDB.

    
- COMMANDE BASIQUE :
  - SELECT :
  
  	L’utilisation la plus courante de SQL consiste à lire des données issues de la base de données. Cela s’effectue grâce à la commande SELECT, qui retourne des enregistrements dans un tableau de résultat. Cette commande peut sélectionner une ou plusieurs colonnes d’une table.
	
	Exemples:
  
    > 	- SELECT nom_du_champ FROM nom_du_tableau;
    >	- SELECT ville FROM client;
    >	- SELECT prenom, nom FROM client;
    >   - SELECT * FROM client;
    >   - SELECT * FROM table WHERE condition GROUP BY expression HAVING condition { UNION | INTERSECT | EXCEPT } ORDER BY expression LIMIT count OFFSET start;


  - INSERT INTO : 

	L’insertion de données dans une table s’effectue à l’aide de la commande INSERT INTO. Cette commande permet au choix d’inclure une seule ligne à la base existante ou plusieurs lignes d’un coup.
	
	Exemples :
	
    > 	- INSERT INTO table VALUES ('valeur 1', 'valeur 2', ...);
    >	- INSERT INTO table (nom_colonne_1, nom_colonne_2, ...) VALUES ('valeur 1', 'valeur 2', ...);
    >	- INSERT INTO client (prenom, nom, ville, age) VALUES ('Rébecca', 'Armand', 'Saint-Didier-des-Bois', 24),('Aimée', 'Hebert', 'Marigny-le-Châtel', 36),
 ('Marielle', 'Ribeiro', 'Maillères', 27),('Hilaire', 'Savary', 'Conie-Molitard', 58);
 
 
  - UPDATE :
  
  	La commande UPDATE permet d’effectuer des modifications sur des lignes existantes. Très souvent cette commande est utilisée avec WHERE pour spécifier sur quelles lignes doivent porter la ou les modifications.
	
	Exemples :
  
    > 	- UPDATE table SET nom_colonne_1 = 'nouvelle valeur' WHERE condition;
    >	- UPDATE table SET colonne_1 = 'valeur 1', colonne_2 = 'valeur 2', colonne_3 = 'valeur 3' WHERE condition;
    >	- UPDATE client SET rue = '49 Rue Ameline',   ville = 'Saint-Eustache-la-Forêt',   code_postal = '76210' WHERE id = 2;
    >	- UPDATE client SET pays = 'FRANCE';
 

  - DELETE :
  
  	La commande DELETE en SQL permet de supprimer des lignes dans une table. En utilisant cette commande associé à WHERE il est possible de sélectionner les lignes concernées qui seront supprimées.
	
	Exemples :
  
    > 	- DELETE FROM `nom_du_tableau` WHERE condition;
    >	- DELETE FROM `utilisateur` WHERE `id` = 1;
    >	- DELETE FROM `utilisateur` WHERE `date_inscription` < '2012-04-10';
    >	- DELETE FROM `utilisateur`;
    >	- TRUNCATE TABLE `utilisateur`;

  - CREATE DATABASE :
  
	La création d’une base de données en SQL est possible en ligne de commande. Même si les systèmes de gestion de base de données (SGBD) sont souvent utilisés pour créer une base, il convient de connaître la commande à utiliser, qui est très simple.
	
	Exemples :

   >    - CREATE DATABASE ma_base;
   >    - CREATE DATABASE IF NOT EXISTS ma_base;


  - DROP DATABASE :

	En SQL, la commande DROP DATABASE permet de supprimer totalement une base de données et tout ce qu’elle contient. Cette commande est à utiliser avec beaucoup d’attention car elle permet de supprimer tout ce qui est inclus dans une base : les tables, les données, les index …
	
	Exemples :
	
  >    - DROP DATABASE ma_base;
  >    - DROP DATABASE IF EXISTS ma_base;
  >    - DROP TABLE nom_table;
  >    - DROP TABLE client_2009;


  - ALTER TABLE :

	La commande ALTER TABLE en SQL permet de modifier une table existante. Idéal pour ajouter une colonne, supprimer une colonne ou modifier une colonne existante, par exemple pour changer le type.
	
	Exemples :
	
  >    - ALTER TABLE nom_table instruction;
  >    - ALTER TABLE nom_table ADD nom_colonne type_donnees;
  >    - ALTER TABLE utilisateur ADD adresse_rue VARCHAR(255);
  >    - ALTER TABLE nom_table DROP nom_colonne;
  >    - ALTER TABLE nom_table DROP COLUMN nom_colonne;
  >    - ALTER TABLE nom_table MODIFY nom_colonne type_donnees;
  >    - ALTER TABLE nom_table CHANGE colonne_ancien_nom colonne_nouveau_nom type_donnees;

- CREATE USERS AND GRANT PERMISSIONS :
	
	exemples :
	
  >   - CREATE USER 'sammy'@'localhost' IDENTIFIED BY 'password';
  >   - GRANT PRIVILEGE ON database.table TO 'username'@'host';
  >   - GRANT CREATE, ALTER, DROP, INSERT, UPDATE, DELETE, SELECT, REFERENCES, RELOAD on *.* TO 'sammy'@'localhost' WITH GRANT OPTION;
  >   - GRANT ALL PRIVILEGES ON *.* TO 'sammy'@'localhost' WITH GRANT OPTION;
  >   - REVOKE type_of_permission ON database_name.table_name FROM 'username'@'host';
  >   - SHOW GRANTS FOR 'username'@'host';
  >   - DROP USER 'username'@'localhost';
	
	#DOCUMENTATION :

  >   - https://www.digitalocean.com/community/tutorials/how-to-create-a-new-user-and-grant-permissions-in-mysql


- FUNCTIONS :

	- AVG():
	
	>  La fonction d’agrégation AVG() dans le langage SQL permet de calculer une valeur moyenne sur un ensemble d’enregistrement de type numérique et non nul.
	
	Exemple :
	
		- SELECT AVG(nom_colonne) FROM nom_table


	- COUNT():
	
	>  En SQL, la fonction d’agrégation COUNT() permet de compter le nombre d’enregistrement dans une table. Connaître le nombre de lignes dans une table est très pratique dans de nombreux cas, par exemple pour savoir combien d’utilisateurs sont présents dans une table ou pour connaître le nombre de commentaires sur un article.
	
	Exemple :
	
	- SELECT COUNT(*) FROM table;
	- SELECT COUNT(nom_colonne) FROM table;


	- MAX():
	
	>  Dans le langage SQL, la fonction d’agrégation MAX() permet de retourner la valeur maximale d’une colonne dans un set d’enregistrement. La fonction peut s’appliquée à des données numériques ou alphanumériques. Il est par exemple possible de rechercher le produit le plus cher dans une table d’une boutique en ligne.
	
	Exemple :
	
	- SELECT MAX(nom_colonne) FROM table;
	- SELECT colonne1, MAX(colonne2) FROM table GROUP BY colonne1;

	- ROUND():
	
	>  Dans le langage SQL la fonction ROUND() permet d’arrondir un résultat numérique. Cette fonction permet soit d’arrondir sans utiliser de décimal pour retourner un nombre entier (c’est-à-dire : aucun chiffre après la virgule), ou de choisir le nombre de chiffre après la virgule.
	
	Exemple :
	
	- SELECT ROUND(nom_colonne) FROM `table`;
	- SELECT ROUND(nom_colonne, 2) FROM `table`;


- FILTERS AND CONDITIONS :

	- WHERE :
	
	>  La commande WHERE dans une requête SQL permet d’extraire les lignes d’une base de données qui respectent une condition. Cela permet d’obtenir uniquement les informations désirées.

	EXEMPLES :
	
	>  - SELECT nom_colonnes FROM nom_table WHERE condition;
	>  - SELECT * FROM client WHERE ville = 'paris';

	- AND & OR :
	
	>  Une requête SQL peut être restreinte à l’aide de la condition WHERE. Les opérateurs logiques AND et OR peuvent être utilisées au sein de la commande WHERE pour combiner des conditions.

	EXEMPLES :
	
	>  - SELECT nom_colonnes FROM nom_table WHERE condition1 AND condition2;
	>  - SELECT nom_colonnes FROM nom_table  WHERE condition1 OR condition2;
	>  - SELECT nom_colonnes FROM nom_table  WHERE condition1 AND (condition2 OR condition3);
	>  - SELECT * FROM produit WHERE categorie = 'informatique' AND stock < 20;
	>  - SELECT * FROM produit WHERE nom = 'ordinateur' OR nom = 'clavier';
	>  - SELECT * FROM produit WHERE ( categorie = 'informatique' AND stock < 20 ) OR ( categorie = 'fourniture' AND stock < 200 );


	- IN :
	
	>  L’opérateur logique IN dans SQL  s’utilise avec la commande WHERE pour vérifier si une colonne est égale à une des valeurs comprise dans set de valeurs déterminés. C’est une méthode simple pour vérifier si une colonne est égale à une valeur OU une autre valeur OU une autre valeur et ainsi de suite, sans avoir à utiliser de multiple fois l’opérateur OR.

	EXEMPLES :
	
	>  - SELECT nom_colonne FROM table WHERE nom_colonne IN ( valeur1, valeur2, valeur3, ... );
	>  - SELECT prenom FROM utilisateur WHERE prenom = 'Maurice' OR prenom = 'Marie' OR prenom = 'Thimoté';
	>  - SELECT prenom FROM utilisateur WHERE prenom IN ( 'Maurice', 'Marie', 'Thimoté' );
	>  - SELECT * FROM adresse WHERE addr_ville IN ( 'Paris', 'Graimbouville' );


	- BETWEEN :
	
	>  L’opérateur BETWEEN est utilisé dans une requête SQL pour sélectionner un intervalle de données dans une requête utilisant WHERE. L’intervalle peut être constitué de chaînes de caractères, de nombres ou de dates. L’exemple le plus concret consiste par exemple à récupérer uniquement les enregistrements entre 2 dates définies.

	EXEMPLES :
	
	>  - SELECT * FROM table WHERE nom_colonne BETWEEN 'valeur1' AND 'valeur2';
	>  - SELECT * FROM utilisateur WHERE date_inscription BETWEEN ‘2012-04-01’ AND ‘2012-04-20’;
	>  - SELECT * FROM utilisateur WHERE id NOT BETWEEN 4 AND 10;


	- LIKE :
	
	>  L’opérateur LIKE est utilisé dans la clause WHERE des requêtes SQL. Ce mot-clé permet d’effectuer une recherche sur un modèle particulier. Il est par exemple possible de rechercher les enregistrements dont la valeur d’une colonne commence par telle ou telle lettre. Les modèles de recherches sont multiple.

	EXEMPLES :
	
	>  - SELECT * FROM table WHERE colonne LIKE modele;
	>  - SELECT * FROM client WHERE ville LIKE 'N%';
	>  - SELECT * FROM client WHERE ville LIKE '%e';


	- DISTINCT :
	
	>  L’utilisation de la commande SELECT en SQL permet de lire toutes les données d’une ou plusieurs colonnes. Cette commande peut potentiellement afficher des lignes en doubles. Pour éviter des redondances dans les résultats il faut simplement ajouter DISTINCT après le mot SELECT.

	EXEMPLES :
	
	>  - SELECT DISTINCT ma_colonne FROM nom_du_tableau;
	>  - SELECT UNIQUE ma_colonne FROM nom_du_tableau;
	>  - SELECT DISTINCT prenom FROM client;


	- GROUP BY :
	
	>  La commande GROUP BY est utilisée en SQL pour grouper plusieurs résultats et utiliser une fonction de totaux sur un groupe de résultat. Sur une table qui contient toutes les ventes d’un magasin, il est par exemple possible de liste regrouper les ventes par clients identiques et d’obtenir le coût total des achats pour chaque client.

	EXEMPLES :
	
	>  - SELECT colonne1, fonction(colonne2) FROM table GROUP BY colonne1;
	>  - SELECT client, SUM(tarif) FROM achat GROUP BY client;
	>  - SELECT client, SUM(tarif) FROM achat;


	- ORDER BY :
	
	>  La commande ORDER BY permet de trier les lignes dans un résultat d’une requête SQL. Il est possible de trier les données sur une ou plusieurs colonnes, par ordre ascendant ou descendant.

	EXEMPLES :
	
	>  - SELECT colonne1, colonne2 FROM table ORDER BY colonne1;
	>  - SELECT colonne1, colonne2, colonne3 FROM table ORDER BY colonne1 DESC, colonne2 ASC;
	>  - SELECT * FROM utilisateur ORDER BY nom;
	>  - SELECT * FROM utilisateur ORDER BY nom, date_inscription DESC;
	
- LES JOINTURES :

	- INTERSECT :
	
	>  La commande SQL INTERSECT permet d’obtenir l’intersection des résultats de 2 requêtes. Cette commande permet donc de récupérer les enregistrements communs à 2 requêtes. Cela peut s’avérer utile lorsqu’il faut trouver s’il y a des données similaires sur 2 tables distinctes.
	
	EXEMPLES :
	
	>  - SELECT * FROM `table1`	INTERSECT	SELECT * FROM `table2`;
	>  - SELECT * FROM `magasin1_client`	INTERSECT	SELECT * FROM `magasin2_client`;
	>  - SELECT DISTINCT value FROM `table1` WHERE value IN (  SELECT value   FROM `table2`);


	- UNION :
	
	>  La commande UNION de SQL permet de mettre bout-à-bout les résultats de plusieurs requêtes utilisant elles-même la commande SELECT. C’est donc une commande qui permet de concaténer les résultats de 2 requêtes ou plus. Pour l’utiliser il est nécessaire que chacune des requêtes à concaténer retourne le même nombre de colonnes, avec les mêmes types de données et dans le même ordre.
	
	EXEMPLES :
	
	>  - SELECT * FROM table1 UNION SELECT * FROM table2;
	>  - SELECT * FROM magasin1_client UNION SELECT * FROM magasin2_client;


	- INNER JOIN :
	
	>  Dans le langage SQL la commande INNER JOIN, aussi appelée EQUIJOIN, est un type de jointures très communes pour lier plusieurs tables entre-elles. Cette commande retourne les enregistrements lorsqu’il y a au moins une ligne dans chaque colonne qui correspond à la condition.
	
	EXEMPLES :
	
	>  - SELECT * FROM table1 INNER JOIN table2 ON table1.id = table2.fk_id;
	>  - SELECT * FROM table1 INNER JOIN table2 WHERE table1.id = table2.fk_id;
	>  - SELECT id, prenom, nom, date_achat, num_facture, prix_total FROM utilisateur INNER JOIN commande ON utilisateur.id = commande.utilisateur_id;


	- CROSS JOIN :
	
	>  Dans le langage SQL, la commande CROSS JOIN est un type de jointure sur 2 tables SQL qui permet de retourner le produit cartésien. Autrement dit, cela permet de retourner chaque ligne d’une table avec chaque ligne d’une autre table. Ainsi effectuer le produit cartésien d’une table A qui contient 30 résultats avec une table B de 40 résultats va produire 1200 résultats (30 x 40 = 1200). En général la commande CROSS JOIN est combinée avec la commande WHERE pour filtrer les résultats qui respectent certaines conditions.
	
	EXEMPLES :
	
	>  - SELECT * FROM table1 CROSS JOIN table2;
	>  - SELECT * FROM table1, table2;
	>  - SELECT l_id, l_nom_fr_fr, f_id, f_nom_fr_fr FROM legume CROSS JOIN fruit;
	>  - SELECT l_id, l_nom_fr_fr, f_id, f_nom_fr_fr FROM legume, fruit;


	- LEFT JOIN :
	
	>  Dans le langage SQL, la commande LEFT JOIN (aussi appelée LEFT OUTER JOIN) est un type de jointure entre 2 tables. Cela permet de lister tous les résultats de la table de gauche (left = gauche) même s’il n’y a pas de correspondance dans la deuxième tables.
	
	EXEMPLES :
	
	>  - SELECT * FROM table1 LEFT JOIN table2 ON table1.id = table2.fk_id;
	>  - SELECT * FROM table1 LEFT OUTER JOIN table2 ON table1.id = table2.fk_id;
	>  - SELECT * FROM utilisateur LEFT JOIN commande ON utilisateur.id = commande.utilisateur_id;
	>  - SELECT id, prenom, nom, utilisateur_id FROM utilisateur LEFT JOIN commande ON utilisateur.id = commande.utilisateur_id WHERE utilisateur_id IS NULL;


	- RIGHT JOIN :
	
	>  En SQL, la commande RIGHT JOIN (ou RIGHT OUTER JOIN) est un type de jointure entre 2 tables qui permet de retourner tous les enregistrements de la table de droite (right = droite) même s’il n’y a pas de correspondance avec la table de gauche. S’il y a un enregistrement de la table de droite qui ne trouve pas de correspondance dans la table de gauche, alors les colonnes de la table de gauche auront NULL pour valeur.
	
	EXEMPLES :
	
	>  - SELECT * FROM table1 RIGHT JOIN table2 ON table1.id = table2.fk_id;
	>  - SELECT * FROM table1 RIGHT OUTER JOIN table2 ON table1.id = table2.fk_id;
	>  - SELECT id, prenom, nom, utilisateur_id, date_achat, num_facture  FROM utilisateur  RIGHT JOIN commande ON utilisateur.id = commande.utilisateur_id;


	- FULL JOIN :
	
	>  Dans le langage SQL, la commande FULL JOIN (ou FULL OUTER JOIN) permet de faire une jointure entre 2 tables. L’utilisation de cette commande permet de combiner les résultats des 2 tables, les associer entre eux grâce à une condition et remplir avec des valeurs NULL si la condition n’est pas respectée.
	
	EXEMPLES :
	
	>  - SELECT * FROM table1 FULL JOIN table2 ON table1.id = table2.fk_id;
	>  - SELECT * FROM table1 FULL OUTER JOIN table2 ON table1.id = table2.fk_id;
	>  - SELECT id, prenom, nom, utilisateur_id, date_achat, num_facture FROM utilisateur FULL JOIN commande ON utilisateur.id = commande.utilisateur_id;


	- SELF JOIN :
	
	>  En SQL, un SELF JOIN correspond à une jointure d’une table avec elle-même. Ce type de requête n’est pas si commun mais très pratique dans le cas où une table lie des informations avec des enregistrements de la même table.
	
	EXEMPLES :
	
	>  - SELECT `t1`.`nom_colonne1`, `t1`.`nom_colonne2`, `t2`.`nom_colonne1`, `t2`.`nom_colonne2` FROM `table` as `t1` LEFT OUTER JOIN `table` as `t2` ON `t2`.`fk_id` = `t1`.`id`;
	>  - SELECT `u1`.`u_id`, `u1`.`u_nom`, `u2`.`u_id`, `u2`.`u_nom` FROM `utilisateur` as `u1` LEFT OUTER JOIN `utilisateur` as `u2` ON `u2`.`u_manager_id` = `u1`.`u_id`;


	- NATURAL JOIN :
	
	>  Dans le langage SQL, la commande NATURAL JOIN permet de faire une jointure naturelle entre 2 tables. Cette jointure s’effectue à la condition qu’il y ai des colonnes du même nom et de même type dans les 2 tables. Le résultat d’une jointure naturelle est la création d’un tableau avec autant de lignes qu’il y a de paires correspondant à l’association des colonnes de même nom.
	
	EXEMPLES :
	
	>  - SELECT * FROM table1 NATURAL JOIN table2;
	>  - SELECT * FROM utilisateur NATURAL JOIN pays;

