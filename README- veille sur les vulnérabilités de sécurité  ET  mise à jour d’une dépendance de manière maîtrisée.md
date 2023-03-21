#       Memo Azarual El-Ghazi  - Bonnes pratiques


# Savoir effectuer une mise à jour d’une dépendance de manière maîtrisée

Pour effectuer une mise à jour d’une dépendance de manière maîtrisée : il faut suivre les notes de version (Release notes)
et de voir les modifications apportées par la nouvelle version (corrections de bugs, évolutions, dépréciation du code, ...)
- voir s'il s'agit d'évolutions mineures ou majeures
- voir s'il s'agit de corrections de bugs 
- si c'est le cas, remplacer les méthodes dépréciées (deprecated)
- dans le cas de changements majeurs nécessitant des vérifications et l'analyse des changements apportés par la nouvelle version.

Dans le cas de notre projet avec une durée de vie de moins d'un mois, il n'y a pas de réelle évolution pour vraiment pratiquer une vraie 
évolution avec des corrections de bugs et le remplacement des méthodes dépréciées ...

Il aurait été préférable si une application avec des dépendances antérieures nous avait été proposé, sur laquelle on peut pratiquer une vraie évolution avec des 
bugs à corriger et des méthodes dépréciées à remplacer ...



# org.springframework.boot:spring-boot-starter-parent : 
    - Licence : Apache Licence 2.0
    - Version : 3.0.4 (latest)
    - Vulnérabilités : Contient des vulnérabilités

# org.springframework.boot:spring-boot-starter-web : 
    - Licence : Apache Licence 2.0
    - Version : 3.0.4 (latest)
    - Vulnérabilités : Pas de vulnérabilités connues


# junit:junit :
    - Licence : EPL 1.0
    - Version : 4.13.2 (latest)
    - Vulnérabilités : Pas de vulnérabilités connues

# org.springframework.boot:spring-boot-starter-test :
    - Licence : Apache Licence 2.0
    - Version : 3.0.4 (latest)
    - Vulnérabilités : Pas de vulnérabilités connues

# fr.le_campus_numerique.square_games:engine :
    - Licence : ?
    - Version : ?
    - Vulnérabilités : ?

# mysql:mysql-connector-java : 
    - Licence : The GNU General Public License, Version 2 
    - Version : 8.0.32 (latest)
    - Vulnérabilités : Pas de vulnérabilités connues



# com.github.ydespreaux.spring.data:spring-data-jpa-criteria :
    - Licence : Apache Licence 2.0
    - Version : 1.2.0 (latest)
    - Vulnérabilités : Vulnérabilités venant des autres dépendances (Vulnerabilities from dependencies)

# org.springframework.boot:spring-boot-starter-security : 
    - Licence : Apache Licence 2.0
    - Version : 3.0.4 (latest)
    - Vulnérabilités : Pas de vulnérabilités connues

# io.jsonwebtoken:jjwt :
    - Licence : Apache Licence 2.0
    - Version : 0.9.1 (latest)
    - Vulnérabilités : Vulnérabilités venant des autres dépendances (Vulnerabilities from dependencies)

# javax.xml.bind:jaxb-api :
    - Licence : CDDL 1.1 / GPL2 w/ CPE
    - Version : 2.4.0-b180830.0359 (latest)
    - Vulnérabilités : Pas de vulnérabilités connues


# com.sun.xml.bind:jaxb-core :
    - Licence : EDL 1.0
    - Version : 4.0.2 (latest)
    - Vulnérabilités : Pas de vulnérabilités connues

# com.sun.xml.bind:jaxb-impl :
    - Licence : EDL 1.0
    - Version : 4.0.2 (latest)
    - Vulnérabilités : Pas de vulnérabilités connues

# org.apache.maven.plugins:maven-checkstyle-plugin :
    - Licence : Apache Licence 2.0
    - Version : 3.2.1 (latest)
    - Vulnérabilités : Vulnérabilités venant des autres dépendances (Vulnerabilities from dependencies)

