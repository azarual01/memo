
Apache Licence 2.0 (http://www.opensource.org/licenses/apache2.0.php)

○ MIT Licence (https://opensource.org/license/mit/)

○ GPL v2 (https://opensource.org/license/gpl-2-0/)

○ GPL v3 (http://www.opensource.org/licenses/gpl-3.0.html)

○ LGPL v2 (http://www.opensource.org/licenses/lgpl-2.1.php)

○ LGPL v3 (http://www.opensource.org/licenses/lgpl-3.0.html)


Wikipedia : https://fr.wikipedia.org/wiki/Liste_de_licences_libres



Identifier et remplacer dès que possible l’appel à des méthodes dépréciées (deprecated). Les
méthodes sont souvent dépréciées dans la perspective d’être supprimées dans une version
ultérieure de la librairie. Dans ce cas, consulter la documentation dans le code ou le site
officiel de la librairie pour voir si une alternative est proposée et comment modifier l’appel.
● Consulter les notes de version (Release notes) qui accompagnent généralement les
publications de versions, et qui décrivent les changements apportés par la version
(corrections de bugs, évolutions, dépréciation du code, ...)
● Évaluer le risque en fonction du digit impacté et du nombre de “sauts” entre deux versions :
○ Le dernier digit du numéro de version concerne uniquement la correction de bugs ou
des évolutions “mineures” : le passage à une version 0.0.X plus récente est préconisé
et peut normalement se faire sans risque et sans modification de code.
○ Le digit en seconde position du numéro de version concerne uniquement la
corrections de bugs : le passage à une version 0.X.X plus récente nécessite de
vérifier au préalable les changements apportées par cette évolution majeure, et peut
nécessiter des adaptations de code et des tests de bon fonctionnement (cette
modification s’effectue généralement dans une branche à part).

Le digit en première position du numéro de version signifie un changement majeur
de la librairie : le passage à une version X.X.X plus récente nécessite de vérifier et
d’analyser les changements apportés par cette évolution majeure. Elle implique
généralement des adaptations de code et des tests de bon fonctionnement (cette
modification s’effectue systématiquement dans une branche à part).

# org.springframework.boot
    - Licence : 
    - Version :
    - Vulnérabilités : 
    - Remarques : 