
# Spécification des Conditions requises pour l’Architecture

| Projet                      | Nouvelle architecture                                     |
| --------------------------- | --------------------------------------------------------- |
| Client                      | Foosus                                                    |
| Titre                       | Spécification des Conditions requises pour l’Architecture |
| N° de Version du Document   | 0.1                                                       |
| Date de Version du Document |                                                           |
| Préparé par                 | Yoann Talon                                               |
| Revu par                    | Anthony Graignic                                          |
| Date de Révision            |                                                           |
---

## **Objet de ce document**

> La Spécification des Conditions requises pour l’Architecture fournit un ensemble de déclarations quantitatives qui décrivent ce qu'un projet de mise en œuvre doit faire pour se conformer à l'architecture. Le cahier des charges de l'architecture constitue généralement un élément majeur d'un contrat de mise en œuvre ou d'un contrat de définition plus détaillée de l'architecture.
> 
> 
> Comme indiqué ci-dessus, le document de Spécification des Conditions requises pour l’Architecture accompagne le document de définition de l'architecture, avec un objectif complémentaire : 
> 
> - Le document de définition de l'architecture fournit une vue qualitative de la solution et vise à communiquer l'intention de l'architecte.
> - La spécification des exigences de l'architecture fournit une vue quantitative de la solution, en énonçant des critères mesurables qui doivent être respectés lors de la mise en œuvre de l'architecture.
> 
> ***Source** : [TOGAF](https://pubs.opengroup.org/architecture/togaf90-doc/epf/TOGAF9/workproducts/Architecture%20Requirements%20Specification_FCE52369.html)*
> 

## **Conditions requises pour l’interopérabilité**

L'interopérabilité est une condition essentielle pour l'architecture cible de Foosus. 

Les différents services, API et systèmes internes doivent être capables de communiquer entre eux de manière fluide et transparente. Il est important de mettre en place des normes et des standards pour assurer la compatibilité entre les différents composants de l'architecture.

De plus, les développements doivent être réalisés en gardant à l'esprit l'interopérabilité, ce qui signifie que les équipes doivent travailler en étroite collaboration pour assurer la cohérence de l'ensemble du système.

## **Contraintes**

La vision architecturale de Foosus se concentre sur la création d'une plateforme flexible, stable et extensible, basée sur les technologies actuelles, favorisant le meilleure rapport qualité/coût et offrant une expérience utilisateur exceptionnelle. 

Pour réussir l'Etat Cible d'Architecture (ECA), il est essentiel de respecter les contraintes suivantes :

- Maintenir la plateforme existante en mode "Maintenance" sans ajouter de nouvelles fonctionnalités,
- Permettre la coexistence de deux plateformes pendant la période de transition,
- Favoriser la croissance de l'entreprise en augmentant quotidiennement le nombre d'adhésions utilisateurs et d'adhésions de nouveaux fournisseurs,
- Livrer plus rapidement de petits incréments dans la plateforme, et réduire le taux d'incidents en production à moins de 1/mois.

## **Hypothèses**

| ID  | Hypothèse                                                                                                                                                                                                                                                                         | Impact | Propriétaire |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ | ------------ |
| 1   | Aucune nouvelle fonctionnalité ne sera développée dans la plateforme existante. Elle sera conservée en mode “Maintenance”                                                                                                                                                         | Elevé  | CIO          |
| 2   | La nouvelle architecture sera construite en fonction des technologies actuelles.                                                                                                                                                                                                  | Modéré | CIO          |
| 3   | L’architecture doit permettre d’obtenir le meilleur rapport Qualité-Coût                                                                                                                                                                                                          | Modéré | CIO          |
| 4   | L’architecture peut inclure de nouveaux composants personnalisés ou des composants du commerce pour favoriser la flexibilité, la stabilité et l’extensibilité.                                                                                                                    | Faible | CIO          |
| 5   | Les solutions open-source sont préférables aux solutions payantes                                                                                                                                                                                                                 | Faible | CIO          |
| 6   | L'offre initiale impliquera la coexistence de deux plateformes et la montée en puissance empirique du volume d'utilisateurs qui migreront vers la nouvelle plateforme à mesure que le produit évoluera. Cette augmentation sera proportionnelle à l'évolution des fonctionnalités | Elevé  | CPO          |
| 7   | La géolocalisation, si elle est modélisée suffisamment tôt dans la nouvelle plateforme, permettra d'introduire d'autres innovations en fonction de l'emplacement de l'utilisateur ou du fournisseur alimentaire.                                                                  | Modéré | CPO          |

## **Mesure du succès**

| Métrique                                      | Technique de mesure                                | Valeur cible        | Justification                                                                                                                    |
| --------------------------------------------- | -------------------------------------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| Nombre d'adhésions d'utilisateurs par jour    | Nombre d’inscription journalière à la plateforme   | Augmentation de 10% | La nouvelle architecture doit accompagner la croissance de l’entreprise, notamment en augmentant le nombre d’adhésion quotidien. |
| Adhésion de producteurs alimentaires par mois | Nombre d’inscription à la plateforme               | 4 adhésion / mois   | Actuellement de 1,5/mois, nous souhaitons accélérer l’adhésion de nouveaux fournisseurs                                          |
| Délai moyen de livraison en production        | Temps entre chaque nouveau déploiement             | Moins d’une semaine | Actuellement à 3,5 semaines. Nous souhaitons livrer plus rapidement de petits incréments dans notre plateforme.                  |
| Taux d’incident en production                 | Nombre d’incidents avérés en production sur 1 mois | Inférieur à 1/mois  | Actuellement à plus de 25/mois, le taux d’incidence en production a une conséquence sur notre chiffre d’affaire.                 |

## **Contrats de service (Business & Application)**

### Accords de niveau de service (SLA)

> Le SLA est un contrat de service Business qui précise ce que le fournisseur de service (en l’état Foosus) promet à ses clients/utilisateurs en terme de temps de fonctionnement, de performance du service, réactivité, responsabilité, etc.
> 

### KPI et métriques

| Métrique              | Engagement        | Mesure                       |
| --------------------- | ----------------- | ---------------------------- |
| Disponibilité         | 97%               | Taux de disponibilité annuel |
| Récurrence d’incident |
| en production         | Moins de 1 / mois | Nombre d’incident            |
| en production         |

### Niveau de service, Classification et Priorité

| Niveau de sévérité | Description                                                   | Réponse cible      |
| ------------------ | ------------------------------------------------------------- | ------------------ |
| 1. Interruption    | Serveur SaaS en panne                                         | Immédiat           |
| 2. Critique        | Risque élevé d'indisponibilité du serveur                     | Sous 10 minutes    |
| 3. Urgent          | Impact sur l'utilisateur final initié                         | Sous 20 minutes    |
| 4. Important       | Potentiel d'impact sur les performances s'il n'est pas traité | Sous 30 minutes    |
| 5. Supervision     | Problème traité mais potentiellement impactant à l'avenir     | Sous un jour ouvré |
| 6. Informationnel  | Requête pour information                                      | Sous 48 heures     |

### Réponse de service

| Service           | Description                                                              | Cible SLA        | Métrique de performance                                                   |
| ----------------- | ------------------------------------------------------------------------ | ---------------- | ------------------------------------------------------------------------- |
| 1. Interruption   | L’accès à la plateforme Foosus est impossible                            | Immédiat         | Temps de réponse entre le début du problème et la communication de Foosus |
| 2. Critique       | Risque élevé de temps d’arrêt de la plateforme.                          | En 10 minutes    | Temps de réponse entre le début du problème et la communication de Foosus |
| 3. Urgent         | Impact de l’utilisateur final débuté.                                    | En 20 minutes    | Temps de réponse entre le début du problème et la communication de Foosus |
| 4. Important      | Risque d'impact sur les performances en l'absence de mesures correctives | En 30 minutes    | Temps de réponse entre le début du problème et la communication de Foosus |
| 5. Supervision    | Problème résolu mais potentiellement impactant pour le futur             | En un jour ouvré | Temps de réponse entre le début du problème et la communication de Foosus |
| 6. Informationnel | Demande d’information                                                    | En 48 heures     | Temps de réponse entre le début du problème et la communication de Foosus |

### Disponibilité du support de service

La couverture des services par Foosus, telle qu'elle est décrite dans le présent accord, suit le calendrier spécifié ci-dessous :

- **Support sur l’application** : 9h à 18h, Lundi au Vendredi
- **Support téléphonique** : 12 heures /jour, Lundi au Vendredi
- **Support par mail** : 12 heures /jour, Lundi au Vendredi

## **Tableau des Objectifs et Indicateurs de niveau de service (SLO/SLI)**

> Les SLO définissent les objectifs que se fixe le propriétaire du service (Foosus) pour atteindre les accords de niveau de service (SLA) proposés aux .
> 

| Catégorie               | SLI (Service Level Indicator)                                                                                                                                                                | SLO (Service Level Objectives)                     |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- |
| API (Backends)          |                                                                                                                                                                                              |                                                    |
| Disponibilité           | Proportion de requêtes réussies, telle que mesurées par les métriques des load-balancers Tout statut HTTP autre qu’entre 500-599 est considéré comme succès                                  | 95% de succès                                      |
| Temps de latence        | La proportion de requêtes suffisamment rapides, telle que mesurée par les métriques de l'équilibreur de charge.”Suffisamment rapide” est défini comme inférieur à 600ms ou inférieur à 1s    | 90% des requêtes < 600ms; 99% des requêtes < 1s    |
| HTTP Server (Frontends) |                                                                                                                                                                                              |                                                    |
| Disponibilité           | Proportion de requêtes réussies, telle que mesurées par les métriques des load-balancers Tout statut HTTP autre qu’entre 500-599 est considéré comme succès                                  | 99% de succès                                      |
| Temps de latence        | La proportion de requêtes suffisamment rapides, telle que mesurée par les métriques de l'équilibreur de charge.”Suffisamment rapide” est défini comme inférieur à 500ms ou inférieur à 900ms | 90% des requêtes < 500ms; 99% des requêtes < 900ms |

## **Indicateurs de niveau de service (SLI)**

> Les SLI mesurent la conformité, via des indicateurs quantitatifs, aux objectifs de niveau de service (SLO).
> 

Voir le tableau des SLO/SLI ci-dessus.

## **Implémentation**

### Ligne directrice pour l’implémentation

> Les lignes directrices fixent des bonnes pratiques à suivre pour améliorer l’efficacité des équipes de développement et d’opération.
> 
- **Quarterly and Weekly Planning** : Planifiez vos activités en fonction de la roadmap de l’entreprise ou de vos services, afin d’évaluer sur 3 mois l’évolution et l’atteinte de vos objectifs. Planifiez également vos semaines de travail afin de fournir une transparence sur vos tâches quotidiennes et mesurer les étapes d’avancement semaine par semaine. Ces planifications permettent aussi aux équipes et personnes de mesurer, voir et d’apprécier de la progression au cours du temps.
- **Privilégier des échanges courts mais réguliers** plutôt que des échanges longs mais ponctuels (Ateliers de conceptions, Example Mapping, Pair programming, etc). Cette directive permettra aux équipes de rester alignées dans le temps, et de stimuler l’intelligence collective.
- **Définir, partager et respecter des règles** de développements, de syntaxe, de nommage des fichiers et du code, nomenclatures, qui soient communes afin de renforcer la lisibilité et la clarté.
- **Les processus de conception et développement** doivent adopter une approche agile tel que DDD (Domain-Driven Design), BDD (Behaviour-Driven Design) et TDD (Test-Driven Development), DevOps, Lean, Craftmanship, .
- **Le code métier doit refléter le langage du domaine métier de Foosus**, de ses consommateurs, fournisseurs, et toute autres utilisateurs des services. Un glossaire des termes du domaine devra être tenu, modifié et discuté autant de fois que nécessaire afin d’accroître une compréhension partagée des termes métiers.
- Les travaux ou incréments sur le produits et les services Foosus sont soumis à une revue par des pairs avant leur déploiement.
- **10 minutes Build** : Faire en sorte de Build et tester chaque nouvel incrément dans le code source en moins de 10 minutes, afin d’assurer des retours plus rapides aux équipes de développement. Des builds rapides sont des fondations à une intégration et un déploiement continu efficaces.
- **L' architecture logicielle doit être la plus faiblement couplée**, c'est à dire qu'elle doit séparer au mieux le code fonctionnel du code non fonctionnel,  afin d'être agnostic face aux technologies et d'être plus rapide pour implémenter de nouvelles fonctionnalités



### Spécification pour l’implémentation

> Les spécifications sont des recommandations spécifiques aux projet d’implémentation de l’Etat Cible de l’Architecture Foosus.
> 
- L’accès aux services Foosus pour tous les utilisateurs se fera depuis l’URL [https://foosus.com/](https://foosus.com/) avec une URI différente pour les 3 types.
- Les services (API, IAM, Systèmes internes) assurant le bon fonctionnement de la plateforme principale seront hébergées en tant que sous-domaine du domaine principal [foosus.com](http://foosus.com), en respectant un nommage clair.
- Les stratégies et plans de tests des systèmes Foosus doivent se baser sur une approche par les risques, afin d’identifier les risques produits et ajuster les efforts de test.

### Standards et normes pour l’implémentation

> Les standards sont reconnus comme des solutions appropriées au delà d’une organisation spécifique. De même, les normes sont des cadres internationaux, plus orientés sur le réglementaire.
> 
- Les systèmes d’exploitation utilisés pour toutes nos opérations sont des distributions [GNU/Linux](https://fr.wikipedia.org/wiki/Liste_des_distributions_GNU/Linux), ou leurs images de conteneurs associées.
- Le processus de développement logiciel doivent adopter une approche de **protection des données personnelles** dites “*[Privacy by design](https://donnees-rgpd.fr/definitions/privacy-by-design/)*”
- Les requêtes et réponses de nos serveurs web, applications et API doivent respecter les normes des codes HTTP définis dans la [RFC2616](https://datatracker.ietf.org/doc/html/rfc2616).
- Le développement de nos applications web doivent **se prémunir des risques de sécurité les plus critiques**, partagées internationalement par [OWASP Top 10](https://owasp.org/www-project-top-ten/).
- La qualité de l’entreprise tend à appliquer la norme de management de la qualité [ISO 9001](https://fr.wikipedia.org/wiki/ISO_9001) pour améliorer ses processus.
- La sécurité de nos systèmes d’informations doivent appliquer, du moins tendre vers, les normes internationales [ISO 27001/27002/27005](https://www.ssi.gouv.fr/uploads/2016/05/cyberedu_module_4_cybersecurite_organisation_02_2017.pdf).

## **Conditions requises pour le management du service IT**

- Disponibilité : 97% (MTTR)
- Récurrence d’incident en production : moins de 1 par mois (nombre d’incidents en production)
- API (Applications serveur) :
    - Disponibilité : 95% de succès (proportion de requêtes réussies, telle que mesurées par les métriques des load-balancers. Tout statut HTTP autre qu’entre 500-599 est considéré comme succès)
    - Temps de latence : 90% des requêtes inférieures à 600ms et 99% des requêtes inférieures à 1s (proportion de requêtes suffisamment rapides, telle que mesurée par les métriques de l'équilibreur de charge)
- Serveur HTTP (Applications web) :
    - Disponibilité : 99% de succès (proportion de requêtes réussies, telle que mesurées par les métriques des load-balancers. Toute statut HTTP autre qu’entre 500-599 est considéré comme succès)
    - Temps de latence : 90% des requêtes inférieures à 500ms et 99% des requêtes inférieures à 900ms (proportion de requêtes suffisamment rapides, telle que mesurée par les métriques de l'équilibreur de charge)

Ces métriques de performance devront être mesurées et suivies régulièrement par le comité de direction du projet pour s'assurer que les objectifs sont atteints.