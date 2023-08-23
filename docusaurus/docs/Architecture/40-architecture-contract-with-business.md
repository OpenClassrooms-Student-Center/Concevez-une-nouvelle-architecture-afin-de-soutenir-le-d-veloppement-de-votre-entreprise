# Contrat d’Architecture des utilisateurs Business

| Projet  | Nouvelle Architecture d’Entreprise |
| ------- | ---------------------------------- |
| Client  | Foosus                             |
| Auteurs | Yoann Talon                        |

---

## **Objet de ce document**

Les Contrats d’architecture sont les accords communs entre les partenaires de développement et les sponsors sur les livrables, la qualité, et la correspondance à l’objectif d’une architecture. L’implémentation réussie de ces accords sera livrée grâce à une gouvernance de l’architecture efficace (voir TOGAF Partie VII, Gouvernance de l’architecture). En implémentant une approche dirigée du management de contrats, les éléments suivants seront garantis :

- *Un système de contrôle continu pour vérifier l’intégrité, les changements, les prises de décisions, et l’audit de toutes les activités relatives à l’architecture au sein de l’organisation.*
- *L’adhésion aux principes, standards et conditions requises des architectures existantes ou en développement*
- *L’identification des risques dans tous les aspects du développement et de l’implémentation des/de l’architecture(s), y compris le développement interne en fonction des standards acceptés, des politiques, des technologies et des produits, de même que les	aspects opérationnels des architectures de façon à ce que l’organisation puisse poursuivre son business au sein d’un	environnement résistant.*
- *Un ensemble de process et de pratiques qui garantissent la transparence, la responsabilité et la discipline au regard du développement et de l’utilisation de tous les artefacts architecturaux*
- *Un accord formel sur l’organe de gouvernance responsable du contrat, son degré d’autorité, et le périmètre de l’architecture sous la gouvernance de cet organe*

Ceci est une déclaration d’intention de se conformer à l’architecture d’entreprise, délivrée par les utilisateurs business entreprise. Lorsque l’architecture d’entreprise aura été implémentée (à la fin de la Phase F), un Contrat d’Architecture sera normalement établi entre la fonction architecture (ou la fonction de gouvernance IT, englobant la fonction architecture) et les utilisateurs business qui par la suite construiront et déploieront des applications système dans l’environnement créé par l’architecture.

## **Introduction et Contexte**

La plateforme Foosus actuelle ne peut **plus soutenir la croissance et l’expansion** de l’entreprise avec **son architecture actuelle**. 

Ses **analyses commerciales** ont montré que **les clients souhaitent acheter local** et être **mis en relation** avec des **producteurs près de chez eux**. 

L’entreprise souhaite **créer une nouvelle plateforme** qui **soutiendra sa croissance** et fournira à leurs **clients une nouvelle expérience**.

## **La nature de l’accord**

La nature de cet accord est de partager et valider avec la maîtrise d’ouvrage les objectifs de l’Etat Cible de l’Architecture, suivant les objectifs business que nous nous sommes fixés. Cet accord vaudra comme un des feu verts nécessaire au lancement de la phase 2 du projet de nouvelle architecture.

## **Objectifs et périmètre**

### Objectifs

Les objectifs business de ce travail d’architecture sont les suivants :

| Objectif Business                                                                                                                                                                                        | Notes                                                                                                                                                                                                     |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Tirer partie de la géolocalisation pour relier les fournisseurs locaux et les consommateurs                                                                                                              | Les études de marché et les analyses commerciales montrent que nos clients souhaitent acheter local et soutiennent les producteurs locaux. Proposer des produits disponibles près des lieux de résidence. |
| Proposer une architecture évolutive, soutenant la croissance de l’entreprise.                                                                                                                            | Déployer les services sur diverses régions, dans des villes et des pays donnés. Etre doté de nouvelles fonctionnalités au fil du temps.                                                                   |
| Eviter toute interruption de service nuisant à la disponibilité de la plateforme pour les utilisateurs, impactant le Chiffre d’Affaire.                                                                  | Nous avons constaté des pannes causées par l'incapacité de notre système logiciel d'absorber les pics d'utilisation                                                                                       |
| Prendre en charge divers types d’utilisateur (Consommateurs, Fournisseurs locaux, Personnel Back-Office Foosus) avec fonctionnalités et services spécifiques pour chaque, au sein d’une même plateforme. | Une seule portée d’entrée pour n’importe quel utilisateur.                                                                                                                                                |
| Proposer une solution multi-plateforme (Web et mobile) pour les utilisateurs                                                                                                                             | Responsive Web Design                                                                                                                                                                                     |
| Fournir une alternative automatisée pour mettre à jour l’inventaire des produits alimentaires.                                                                                                           | Concevoir une alternative au traitement manuel de l’inventaire de produits alimentaires                                                                                                                   |
| Réaménager la chaîne de valeur, en optimisant les délais d’approvisionnement et de livraison                                                                                                             | Diminuer le Lead time                                                                                                                                                                                     |

### Périmètre

Le périmètre de la phase 2 comprend : 

- **La mise en œuvre de l’Etat Cible de l’Architecture**, tel que définit dans les documents dans la vision architecturale, et la déclaration de travail d’architecture.

### Parties prenantes, préoccupations et visions

Le tableau suivant montre les parties prenantes qui utilisent ce document, leurs préoccupations, et la façon dont le travail d’architecture répondra à ces préoccupations par l’expression de plusieurs visions.

| Partie prenante          | Préoccupation                                                                      | Vision                                                                            |
| ------------------------ | ---------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| CEO - Board Members      | La nouvelle architecture doit assurer le développement économique de l’entreprise. | Faire rayonner Foosus au niveau départemental, régional, national, international. |
| Engineering Product Team | Concevoir et intégrer de nouvelles fonctionnalités utilisables et réactives.       | Offrir une expérience utilisateur de premier plan.                                |
| Marketing Team           | Déployer et maintenir une architecture évolutive                                   | Faire franchir le million d’utilisateurs inscrits à notre base client.            |
| Financial Team           | Augmenter la rentabilité de Foosus                                                 | La nouvelle architecture soutiendra la croissance économique de Foosus            |

## **Conditions requises pour la conformité**

L’Etat Cible de l’Architecture devra vérifier les métriques business fixées, et respecter les accords de niveau de service préalablement rédigés. Ces conditions sont requises pour assurer la conformité de l’architecture d’entreprise.

## **Personnes adoptant l’architecture**

- Représentant de l’équipe satisfaction client — face au client
- Membre de l’équipe finance — facturation
- CEO et membre du conseil d’administration
- Membres de l’équipe Produit
- Membres de l’équipe Marketing

## **Fenêtre temporelle**

La fenêtre temporelle de la phase 2 est de 6 mois, et commencera à la suite de la signature des contrats d’architecture.

## **Métriques Business de l’architecture**

| Métrique                                   | Technique de mesure                                | Valeur cible        | Justification                                                                                                                    |
| ------------------------------------------ | -------------------------------------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| Nombre d'adhésions d'utilisateurs par jour | Nombre d’inscription journalière à la plateforme   | Augmentation de 10% | La nouvelle architecture doit accompagner la croissance de l’entreprise, notamment en augmentant le nombre d’adhésion quotidien. |
| Adhésion de producteurs alimentaires       | Nombre d’inscription à la plateforme               | 4 adhésion / mois   | Actuellement de 1,5/mois, nous souhaitons accélérer l’adhésion de nouveaux fournisseurs                                          |
| Délai moyen de livraison en production     | Temps entre chaque nouveau déploiement             | Moins d’une semaine | Actuellement à 3,5 semaines. Nous souhaitons livrer plus rapidement de petits incréments dans notre plateforme.                  |
| Taux d’incident en production              | Nombre d’incidents avérés en production sur 1 mois | Inférieur à 1/mois  | Actuellement à plus de 25/mois, le taux d’incidence en production a une conséquence sur notre chiffre d’affaire.                 |

## **Accords de service pour l’architecture**

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

## **Personnes approuvant ce plan**

| Validateur | Domaine de responsabilité | Date |
| ---------- | ------------------------- | ---- |
| x          | x                         | x    |
| x          | x                         | x    |