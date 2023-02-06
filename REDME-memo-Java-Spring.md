# Mémo-java/Spring    Azarual El-Ghazi
Introduction au Spring Boot

Description :
- Spring Framework est un framework Java populaire et largement utilisé pour la création de sites Web
  et applications d'entreprise. Spring, à la base, est un conteneur d'injection de dépendances
  qui offre la flexibilité de configurer les beans de plusieurs manières, telles que XML, les annotations,
  et JavaConfig. Au fil des années, Spring Framework a connu une croissance exponentielle en
  répondant aux besoins des applications métier modernes telles que la sécurité, la prise en charge de NoSQL
  stockage de données, traitement du Big Data, intégration avec d'autres systèmes et
  plus. Parallèlement à ses sous-projets, Spring est devenu une plate-forme viable pour la construction
  applications de l'entreprise.
  Le Spring Framework est très flexible et offre plusieurs façons de configurer des
  composants applicatifs avec des fonctionnalités riches combinées à diverses configurations
  options. La configuration des applications Spring devient complexe et sujette aux erreurs.
  L'équipe Spring a créé Spring Boot pour résoudre la complexité de la configuration grâce à son puissant
  Mécanisme d'autoconfiguration.


- Développement d'applications Web à l'aide de Spring Boot


    - Pour initialise un projet Spring il suffit de se rendre sur le site officiel :
https://start.spring.io/ et de choisir les dépendances qui correspondent aux besoins de l'application.


- @Component : 
    >   L'annotation Spring Component est utilisée pour désigner une classe en tant que composant. Cela signifie que le framework Spring détectera automatiquement ces classes pour l'injection de dépendances lorsque la configuration basée sur les annotations et l'analyse du chemin de classe sont utilisées.

Le framework Spring fournit trois autres annotations spécifiques à utiliser lors du marquage d'une classe en tant que composant.

  > @Service : indique que la classe fournit certains services. Nos classes utilitaires peuvent être marquées comme classes de service.
  
  > @Repository : cette annotation indique que la classe traite des opérations CRUD, généralement elle est utilisée avec les implémentations DAO qui traitent des tables de base de données.
 
  > @Controller : principalement utilisé avec les applications Web ou les services Web REST pour spécifier que la classe est un contrôleur frontal et responsable du traitement de la demande de l'utilisateur et du retour de la réponse appropriée.

- @Autowired :
    > Cela permet à Spring de résoudre et d'injecter des beans collaboratifs dans notre bean.

- @Configuration :
    > L'annotation @Configuration permet de déclarer pour Spring un composant qui ne sert qu'à configurer le contexte de l'application. Normalement ce composant n'est pas destiné à être injecté comme dépendance mais à déclarer des méthodes de fabrique annotées avec @Bean.

- @EnableWebSecurity :
    > Exemple de configuration Java pour activer la sécurité Spring

- @RestController :
    > C'est une annotation pratique qui combine @Controller et @ResponseBody, ce qui élimine le besoin d'annoter chaque méthode de gestion des requêtes de la classe de contrôleur avec l'annotation @ResponseBody.

- @RequestMapping :
    > cet annotation est utilisée pour mapper les requêtes Web aux méthodes Spring Controller.

- @PostMapping :
    > Les méthodes annotées @PostMapping gèrent les requêtes HTTP POST correspondant à l'expression URI donnée.

- @GetMapping :
    > Les méthodes annotées @GetMapping gèrent les requêtes HTTP GET correspondant à l'expression URI donnée.

- @Override :
    > Dans une sous-classe, nous pouvons remplacer ou surcharger les méthodes d'instance. Le remplacement indique que la sous-classe remplace le comportement hérité.

- @value :
    > Cette annotation peut être utilisée pour injecter des valeurs dans des champs dans des beans gérés par Spring, et elle peut être appliquée au niveau du paramètre champ ou constructeur/méthode.

- @PreAuthorize :
    > Le @PreAuthorize peut vérifier l'autorisation avant d'entrer dans la méthode. Le @PreAuthorize autorise sur la base du rôle ou de l'argument qui est passé à la méthode.

- @PostAuthorize :
    > Le @PostAuthorize vérifie l'autorisation après l'exécution de la méthode. Le @PostAuthorize autorise sur la base des rôles connectés, renvoie l'objet par méthode et l'argument passé à la méthode.

- @Secured(“ROLE_VIEWER”) : 
    > L'annotation définit que seuls les utilisateurs qui ont le rôle ROLE_VIEWER peuvent exécuter la méthode getUsername.
