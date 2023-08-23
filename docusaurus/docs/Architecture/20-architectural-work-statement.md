---
title: Déclaration de travail d'architecture
description: Définit le périmètre et l’approche qui seront utilisés pour mener à bien un projet d’architecture
---

| Projet                             | Nouvelle Architecture d’Entreprise                        |
| ---------------------------------- | --------------------------------------------------------- |
| Client                             | Foosus                                                    |
| Titre                              | Spécification des Conditions requises pour l’Architecture |
| Auteurs                            | Yoann Talon                                               |
| N° de Version du Document          | 0.1                                                       |
| Date de Version du Document        | 06/2023                                                   |
| Préparé par                        | Yoann Talon                                               |
| Revu par                           | Anthony Graignic                                          |
| Date de Révision                   | 19/08/2023                                                |
| Date de rendu :                    | 13/07/2023                                                |
| Types d’action :                   |                                                           |
| Historique de versions du document |                                                           |
| Date de rendu :                    | 13/07/2023                                                |
| Types d’action :                   |                                                           |
| Historique de versions du document |                                                           |

---

## **Objet de ce document**

La Déclaration de travail d’architecture définit le périmètre et l’approche qui seront utilisés pour mener à bien un projet d’architecture. 

La Déclaration de travail d’architecture constitue habituellement le document qui permet de mesurer la réussite de l’exécution du projet d’architecture et peut former la base de l’accord contractuel entre le fournisseur et le consommateur de services d’architecture. 

En général, toutes les informations de ce document doivent se situer à un haut niveau.

## **Déclaration de travail d’architecture**

### Requête du projet et contexte

La plateforme Foosus actuelle ne peut **plus soutenir la croissance et l’expansion** de l’entreprise avec **son architecture actuelle**. 

Ses **analyses commerciales** ont montré que **les clients souhaitent acheter local** et être **mis en relation** avec des **producteurs près de chez eux**. 

L’entreprise souhaite **créer une nouvelle plateforme** qui **soutiendra sa croissance** et fournira à leurs **clients une nouvelle expérience**.

### Description du projet et périmètre

| Quoi     | 1. Analyse et conception d’un nouvelle architecture, 2. Rédaction de livrable et mise à jour d’un référentiel d’architecture                                                                                                                                        |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Qui      | Yoann Talon, Architecte d’entreprise; Daniel Anthony, Directeur Produits, Foosus; Natasha Jarson, Directrice Informatique, Foosus; Jack Harkness, Responsable des opérations, Foosus; Ash Callum, PDG, Foosus; Equipes de développement, Marketing, Produit Foosus. |
| Où       | Travaux et rédaction en distanciel.                                                                                                                                                                                                                                 |
| Quand    | La phase 1 se déroulera sur 2 trimestres                                                                                                                                                                                                                            |
| Comment  | Fourniture de livrables à intervalle régulier.                                                                                                                                                                                                                      |
| Pourquoi | Soutenir la croissance et offrir une expérience utilisateur au plus proche de chez lui.                                                                                                                                                                             |

### Vue d’ensemble

Foosus est une **jeune entreprise** âgée de 3 ans dans le **secteur de l’alimentation durable**. Leur objectif est de **soutenir une alimentation écologique, durable et locale** en mettant en contact les consommateurs avec les producteurs et artisans locaux.

![Foosus Overview (2).png](https://raw.githubusercontent.com/agent-swyth/oc-p5-new-architecture/master/images/foosus-overview.png)

L’entreprise souhaite construire **une solution géo ciblée** avec une **nouvelle architecture**. Les choix historiques de Foosus ont engendré une **dette technique** et un **manque de cohérence** dans leur architecture initiale, qui impactent déjà le développement de nouvelles fonctionnalités et la qualité de service.

Aujourd’hui, Foosus souhaite investir dans une nouvelle fonction d’architecture. De manière à collaborer avec les équipes dans l’élaboration d’une nouvelle architecture, modulable et résiliente, pour leur solution principale et celles qui suivront.

### Alignement stratégique

L’alignement stratégique est une démarche visant à faire coïncider la stratégie des systèmes d’informations sur la ou les stratégies métiers de l’entreprise.  

Cette démarche a pour finalité de renforcer la **valeur d’usage** du système d’information et de faire de celui-ci un atout pour l’entreprise.

L’alignement de la stratégie d’entreprise et de la stratégie du système d’information repose sur deux conditions préalables : 

- Compréhension et Intégration de la stratégie d’entreprise par la fonction Système d’Information dans son ensemble.
- Prise en compte des contraintes et des opportunités de l’informatique dans la stratégie de l’entreprise

Le projet de nouvelle architecture s’inscrit alors dans l’alignement de la stratégie du SI avec la stratégie Business de Foosus, visant à créer la première plateforme pour l’achat de biens alimentaires locaux.

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

Le périmètre de la phase 1 du projet comprend : 

- L’**analyse de la vision d’entreprise** pour la nouvelle architecture
- **Conception et Définition** de la **nouvelle architecture d’entreprise**
- **Elaboration d’un projet de suivi** pour le développement d’un prototype d’architecture
- **Mise à jour du référentiel d’architecture** avec les choix et compromis décidés, ainsi que tous les documents documentant l’architecture cible.

La **phase 1** du projet a pour objectif de définir une nouvelle architecture soutenant les objectifs Business. Elle ne comprend pas la réalisation, PoC, MVP de la nouvelle architecture.  La mise en œuvre de l’architecture cible sera l’objectif de la phase 2 du projet.

## **Parties prenantes, préoccupations, et visions**

Le tableau suivant montre les parties prenantes qui utilisent ce document, leurs préoccupations, et la façon dont le travail d’architecture répondra à ces préoccupations par l’expression de plusieurs visions.

| Partie prenante                | Préoccupation                                                                                  | Vision                                                                                  |
| ------------------------------ | ---------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| CEO - Board Members            | La nouvelle architecture doit assurer le développement économique de l’entreprise.             | Faire rayonner Foosus au niveau départemental, régional, national, international.       |
| Engineering Product Team       | Concevoir et intégrer de nouvelles fonctionnalités utilisables et réactives.                   | Offrir une expérience utilisateur de premier plan.                                      |
| Engineering (Development) Team | Concevoir et développer les nouvelles fonctionnalité, en augmentant la vélocité des livraison. | Libérer la créativité et l’expérience de développement. Donner le meilleur d’eux-mêmes. |
| Engineering (Operations) Team  | Déployer et maintenir une plateforme évolutive, résiliente et sécurisée.                       | Assurer la sécurité des services de Foosus                                              |
| Marketing Team                 | Déployer et maintenir une architecture évolutive                                               | Faire franchir le million d’utilisateurs inscrits à notre base client.                  |
| Financial Team                 | Augmenter la rentabilité de Foosus                                                             | La nouvelle architecture soutiendra la croissance économique de Foosus                  |

## **Approche managériale**

L’approche managériale du projet s’appuie sur le Lean Management, mettant en avant 5 principes : 

1. **Identifier la valeur** : Offrir un produit et un service pour lequel nos clients sont prêt à payer. Il est nécessaire pour chaque partie, comme pour nos utilisateurs, d’identifier clairement la valeur ajoutées de nos produits.
2. **Cartographier la chaîne de valeur** : En fournissant une visualisation claire des processus liés à la livraison du produit final, nous identifierons rapidement les étapes de nos processus qui ne fournissent pas de valeur ajoutée et de les éliminer. 
3. **Créer un flux de travail continu** : La réalisation de la nouvelle architecture impliquera un travail d’équipes inter fonctionnelles. C’est pourquoi nous devons nous assurer que chaque équipe dispose d’activités et tâches proportionnées ainsi que d’une bonne visualisation des flux de travail à réaliser. L’objectif est d’éviter des goulots d’étranglement, des interruptions ou des mal-être chez nos collaborateurs.
4. **Créer un système de traction** : Pour que nos équipes puissent bénéficier d’un flux de travail continu, livrer rapidement et avec moins d’efforts, il en va aux responsables et architectes de définir la demande. Ainsi, seules les ressources nécessaires sont mobilisées, 
5. **L’amélioration continue** : Notre système n’étant pas infaillibles, Nous devons nous assurer que nos collaborateurs sont impliqués dans l’amélioration continue des processus de réalisation, mais également de leurs savoir-faire.

L’approche managériale s’appuient également sur des valeurs et principes (ainsi que des pratiques) empruntés à **[l’Agile](https://agilemanifesto.org/)**, au **[Craftmanship](https://manifesto.softwarecraftsmanship.org/)**, à l’**[Extreme Programming](https://www.altexsoft.com/blog/business/extreme-programming-values-principles-and-practices/)**, ainsi qu’au **[DevOps](https://sites.google.com/a/jezhumble.net/devops-manifesto/)**.

Notre organisation du travail s’articule autour d’équipes de 4 à 5 personnes dites “Squad” autonomes, effectuant des points de suivis réguliers sur les travaux en cours à délivrer avec les responsables et chefs de projet.

L’approche agile est importante dans nos projets pour itérer rapidement sur des activités à réaliser sans devoir retravailler toutes les exigences du projet, comme dans un cycle de développement en V ou en cascade.

## **Procédures de changement de périmètre**

> Le changement de périmètre implique une démarche globale et systémique en termes de gestion de projet et de gestion du changement.
> 

### Qui demande et/ou décide du changement de périmètre ?

- Demande d’un membre de la direction.
- Demande unilatéral du CTO.
- Demande/suggestion d’un collaborateur approuvé par un membre de la direction.

### Quel sont les questions à se poser avant d’acter le changement de périmètre ?

1. Est-ce que le nouveau périmètre répond aux objectifs stratégiques de l’entreprise ?
2. Est-ce que le budget pour ce changement de périmètre a été calculé ?
3. Est-ce que les objectifs business fournis dans la demande préliminaire (Brief Business) seront toujours atteints avec ce changement de périmètre ? 

### Comment est pris en compte le nouveau périmètre ?

1. Mettre à jour les documents du référentiel d’architecture pour prendre en compte le nouveau périmètre :
    1. Ajouter les éléments liés au nouveau périmètre : Acteurs, exigences, risques, hypothèses.
    2. Supprimer les éléments non pris en compte dans le nouveau périmètre.
    3. Redéfinir le planning du projet.
2. Nouvelle phase de présentation, d’acceptation et de signature des documents.

### Que se passe-t-il après acceptation ?

- Communications aux équipes des changements qui impacteront leurs activités
- Mise à jour des activités, rôles et responsabilités des acteurs pour correspondre au nouveau périmètre
- Mise à jour du planning de projet

## **Structure de gouvernance**

Le schéma ci-dessous modélise la structure de gouvernance au sein de Foosus.

![Diagramme d’organisation de la société Foosus](https://raw.githubusercontent.com/agent-swyth/oc-p5-new-architecture/master/images/org-chart.png)

## **Process du projet**

### Réunions et échanges

- Réunion de lancement, afin d’aligner les équipes sur les buts, objectifs et également les activités les concernant.
- Réunion ponctuelle de suivi de projet (1 à 2 par semaine) avec les différentes squads et leurs activités dans le projet.
- Réunion journalière des squad pour échange autour des activités de la veille, de blocage ou difficultés rencontrées et des tâches de la journée à venir, ainsi que des échanges à prévoir entre eux.
- Réunion hebdomadaire du comité de pilotage (C-Level, Architecture d’entreprise) pour suivre l’évolution du projet et vérifier que les contraintes budgétaires et temporelles sont respectées.
- Des réunions informelles permettront aux différentes équipes de synchroniser leurs travaux , fournir des retours rapides.

### Organisation des informations :

- Progiciel ERP de gestion de projet pour formaliser et suivre au plus près l’avancement du projet. Outil de gestion de projet orienté technique possiblement déjà intégré dans les forges logicielles.
- Outil de documentation commun pour les équipes :
    - Technique : utilisation de la forge logicielle pour versionner la documentation technique
    - Autre : Utilisation de l’ERP (fonctionnalités de documentation) pour formaliser les fonctionnalités, exigences métiers, comptes-rendus de réunion, etc.
- Logiciel de conception d’interface pour formaliser entre les équipes les éléments graphiques et les flows utilisateurs (interactions).
- Forge logicielle où sera versionnée le code source de la nouvelle architecture, et le référentiel d’architecture.
- Cloud partagé pour l’édition/lecture/partage de fichier.
- Partage des secrets et des mots de passes d’administration dans un espace cloud restreint.
- Outil pour le suivi de la qualité / des tests

## **Rôles et responsabilités du projet (RACI)**

La matrice RACI permet d’identifier les rôles et les responsabilités de chacun via 4 responsabilités :

- **R → Responsible** : Celui qui réalise l’activité.
- **A → Accountable** : Celui qui approuve l’activité avant d’être livrée, qui est l’autorité. C’est aussi celui qui doit rendre des comptes une fois l’activité approuvée.
- **C → Consulted** : Celui qui est consulté, donne son avis et ses conseil.
- **I → Informed** : Celui qui doit être informé tout au long de l’activité.

| Activité                                                               | CEO, Ash Calum | CIO, Natacha Jarson | CPO, Daniel Anthony | CFO, Jo Kumar | CMO, Christina Orgega | Architecte d’entreprise, Yoann Talon | Product Team | Frontend Squad | Backend Squad | Ruby Dev Squad | Ops Squad   | IAM Squad   | Marketing Team | Financial Team |
| ---------------------------------------------------------------------- | -------------- | ------------------- | ------------------- | ------------- | --------------------- | ------------------------------------ | ------------ | -------------- | ------------- | -------------- | ----------- | ----------- | -------------- | -------------- |
| Recherche utilisateurs et produit                                      | Informed       | Informed            | Accountable         | Informed      | Informed              | Consulted                            | Responsible  | Consulted      | Informed      | Informed       | Informed    | Informed    | Informed       | Informed       |
| Conception des Maquettes UI/UX                                         | Informed       | Informed            | Accountable         | Informed      | Informed              | Consulted                            | Responsible  | Consulted      | Informed      | Informed       | Informed    | Informed    | Informed       | Informed       |
| Réunions de suivi de projet (comité de pilotage)                       | Accountable    | Responsible         | Responsible         | Responsible   | Responsible           | Responsible                          | Informed     | Informed       | Informed      | Informed       | Informed    | Informed    | Informed       | Informed       |
| Outillage et mise en place des environnements (Dev, Stage, Production) | Informed       | Accountable         | Informed            | Informed      | Informed              | Consulted                            | Informed     | Responsible    | Responsible   | Responsible    | Responsible | Responsible | Informed       | Informed       |
| Développement/Intégration des solutions Frontend                       | Informed       | Accountable         | Consulted           | Informed      | Informed              | Consulted                            | Consulted    | Responsible    | Consulted     | Consulted      | Consulted   | Consulted   | Informed       | Informed       |
| Développement et mise en œuvre des solutions Backend                   | Informed       | Accountable         | Informed            | Informed      | Informed              | Consulted                            | Informed     | Consulted      | Responsible   | Responsible    | Responsible | Responsible | Informed       | Informed       |
| Mise en œuvre de la livraison continue (CI/CD)                         | Informed       | Accountable         | Informed            | Informed      | Informed              | Consulted                            | Informed     | Consulted      | Responsible   | Consulted      | Responsible | Consulted   | Informed       | Informed       |
| Mise en place d’outils de supervision de la plateforme                 | Informed       | Accountable         | Informed            | Informed      | Informed              | Consulted                            | Informed     | Consulted      | Responsible   | Consulted      | Responsible | Consulted   | Informed       | Informed       |
| Mise en place de la gestion d’identité et d’accès (interne et externe) | Informed       | Accountable         | Informed            | Informed      | Informed              | Consulted                            | Informed     | Informed       | Consulted     | Consulted      | Consulted   | Responsible | Informed       | Informed       |
| Développement des tests                                                | Informed       | Accountable         | Informed            | Informed      | Informed              | Consulted                            | Consulted    | Responsible    | Responsible   | Responsible    | Responsible | Responsible | Informed       | Informed       |
| Documentation des systèmes, procédures et du produit                   | Informed       | Accountable         | Consulted           | Informed      | Informed              | Consulted                            | Responsible  | Responsible    | Responsible   | Responsible    | Responsible | Responsible | Informed       | Informed       |
| Production des contenus créatifs et visuels de communication           | Informed       | Informed            | Consulted           | Informed      | Informed              | Consulted                            | Consulted    | Consulted      | Informed      | Informed       | Informed    | Informed    | Responsible    | Informed       |
| Suivi du budget du projet et des KPI                                   | Accountable    | Responsible         | Responsible         | Responsible   | Responsible           | Responsible                          | Informed     | Informed       | Informed      | Informed       | Informed    | Informed    | Informed       | Responsible    |

## **Approche architecturale**

### Process d’architecture

La méthode de développement d’architecture TOGAF (ou ADM pour « Architecture Development Method ») décrit une méthodologie des meilleures pratiques pour le développement architectural.
Néanmoins, toutes les phases ne sont pas également pertinentes pour chaque projet. Le tableau ci-dessous décrit l’utilisation de l’ADM pour ce projet spécifique.

Certaines phases du TOGAF ADM ne concernant pas la phase 1 du projet Foosus, elles ont été supprimées du tableau.

| Phase                                       | Entrée/Sortie                                                                                                                                                                                     |
| ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Préliminaire                                | **Entrée** : Brief Business de Haut Niveau; **Sortie** : Requête de travail d’architecture                                                                                                        |
| A —Vision de l’architecture                 | **Entrée** : Requête de travail d’architecture, Vision architecturale; **Sortie** : Déclaration de travail d’architecture                                                                         |
| B —Architecture business                    | **Entrée** : Requête de travail d’architecture, Vision architecturale; **Sortie** : Contrat d’Architecture des utilisateurs Business                                                              |
| C — Architecture des systèmes d’information | **Entrée** : Requête de travail d’architecture, Vision architecturale; **Sortie** : Contrat de Conception et de Développement de l’Architecture                                                   |
| D — Architecture technologique              | **Entrée** : Requête de travail d’architecture, Vision architecturale; **Sortie** : Contrat de Conception et de Développement de l’Architecture,  Vision architecturale                           |
| E —Opportunités et solutions                | **Entrée** : Requête de travail d’architecture, Vision architecturale; **Sortie** : Contrat d’Architecture des utilisateurs Business, Contrat de Conception et de Développement de l’Architecture |

## **Contenu de l’architecture**

Le cadre de contenu d’architecture TOGAF (ou ACF pour « Architecture Content Framework ») fournit une catégorisation des meilleures pratiques pour le contenu de l’architecture.

Néanmoins, tous les éléments ne sont pas également pertinents pour chaque projet. Le tableau ci-dessous décrit les zones de contenu pertinentes pour ce projet spécifique.

| Zone de contenu                                             | Entrée/Sortie                                                                                                                                                                                                                             |
| ----------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Principes, Vision, et Conditions requises de l’Architecture | **Entrée** : Brief Business de haut niveau, Requête de travail d’architecture, Vision architecturale; **Sortie** : Déclaration de travail d’architecture, Vision architecturale                                                           |
| Architecture Business                                       | **Entrée** : Brief Business de haut niveau, Requête de travail d’architecture, Vision architecturale, **Sortie** : Contrat d’Architecture des utilisateurs Business                                                                       |
| Architecture des systèmes d’information — Données           | **Entrée** : Brief Business de haut niveau, Requête de travail d’architecture, Vision architecturale; **Sortie** : Spécification des Conditions requises pour l’Architecture, Contrat de Conception et de Développement de l’Architecture |
| Architecture des systèmes d’information — Applications      | **Entrée** : Brief Business de haut niveau, Requête de travail d’architecture, Vision architecturale; **Sortie** : Spécification des Conditions requises pour l’Architecture, Contrat de Conception et de Développement de l’Architecture |
| Architecture technologique                                  | **Entrée** : Brief Business de haut niveau, Requête de travail d’architecture, Vision architecturale; **Sortie** : Spécification des Conditions requises pour l’Architecture, Contrat de Conception et de Développement de l’Architecture |

## **Méthodologies pertinentes et normes de l’industrie**

Soutien au Continuum de l’entreprise. Les autres points notables relatifs à l’approche architecturale incluent :

| Type                                                                                                                                 | Commentaire                                                                                                                                                                                                                                                                                                                      |
| ------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Le niveau de détail** (stratégique, segment, capacité)                                                                             | L’approche architecturale assure un niveau de détail stratégique, afin de partager la vision à tous les acteurs du projet. Egalement, elle offre un niveau de détail par segment, en fonction du type de parties prenantes concernée, entre les parties Business et Technique.                                                   |
| **La période de temps** (quelle période de temps l’architecture couvre-t-elle ?)                                                     | L’architecture couvre la période de temps d’Aujourd’hui à plusieurs années. Elle doit être capable d’évoluer au fil des projets sans être remise ne cause dans son entièreté.                                                                                                                                                    |
| **Le niveau d’abstraction** (par exemple une représentation concrète de solutions, ou une architecture de référence plus abstraite). | L’approche architecture fournit un architecture de référence abstraite ainsi qu’une représentation concrète  des solutions à travers des modèles de diagrammes C4                                                                                                                                                                |
| **La ligne de base vs la cible**                                                                                                     | L’accent est mis sur la documentation de l’architecture cible, faisant office de nouvelle architecture. Cependant l’architecture de base est étudiée afin de s’inspirer des compromis architecturaux qui ont fonctionné, mais également pour transférer les savoirs et savoirs faires des équipes dans la nouvelle architecture. |
| **L’itération** — l’itération est-elle utilisée dans l’ADM ?                                                                         | L’itération est utilisée dans l’ADM, de manière à ce que chaque équipe puisse planifier ses travaux, les réaliser, analyser les résultats et agir en conséquence. Le versionnage des documents et blocs architecturaux entrent également dans la démarche d’amélioration continue.                                               |
|                                                                                                                                      |


## **Plan de travail**

Cette section décrit toutes les activités et tous les livrables du travail d’architecture durant la phase 1 du projet.

### Spécification et vision de la nouvelle architecture

**Activités :**

Définition des conditions requises pour la réussite de l’architecture cible, ainsi que des solutions retenues pour y répondre. Mise à jour de la vision architecturale de Foosus, pour que la stratégie business reste alignée avec la stratégie des systèmes d’information.

**Livrables :**

Les produits de travail suivant seront créés en résultat de ce travail d’architecture :

- **Spécification des Conditions requises pour l’Architecture** :
- **Vision Architecturale** : Mise à jour de la vision architecturale, avec notamment un diagramme de haut niveau de l’architecture cible.

### Contrats d’architecture avec les parties prenantes

**Activités :**

Définition des accords communs avec la maîtrise d’ouvrage et la maîtrise d’œuvre du projet de nouvelle architecture.

**Livrables :**

- ****Contrat d’architecture des utilisateurs business :**** Déclaration d’intention de se conformer à l’architecture d’entreprise, délivrée par les utilisateurs business entreprise.
- **Contrat de Conception et de Développement de l’Architecture :**  Déclaration d’intention signée sur la conception et le développement de l’architecture d’entreprise, ou de parties significatives de celles-ci, de la part d’organisations partenaires, y compris les intégrateurs système, fournisseurs d’applications, et fournisseurs de service.

## **Plan de communication**

Afin d’assurer la réussite du projet, et d’élargir la visibilité de Foosus auprès du grand public, nous nous devons de définir un plan de communication qui répondra à ces objectifs.

### Évènements

- Kick-Off, réunion de lancement, durant les début de phases du projet, et des activités.
- Prospection auprès d’utilisateurs finaux, fournisseurs et futurs utilisateurs.
- Campagne de publicité web durant la prochaine phase du projet
- Campagne publicitaire physique
- Evènement physique dans certaines villes afin de promouvoir le produit Foosus, en compagnie de fournisseurs, utilisateurs, ainsi que d’acteurs publics et privés proches du domaine de l’alimentation éco-responsable.

### Canaux

************************Numériques :************************

- LinkedIn, Twitter, Facebook, Instagram, TikTok, Forums locaux, Blogs d’affiliation.

**En interne :** 

- Messagerie et canaux de discussion instantanée, tel que Slack.
- Fils de commentaires depuis l’ERP commun pour les retours rapides
- Documentations des équipes, faisant office de supports de communication plus formels.

**********Physiques :********** 

- Démarchage physique de fournisseurs locaux
- Publicité dans les zones urbaines et péri-urbaines

### Formats

Le format à privilégier pour les documents technique est le markdown (.md). De plus, ces documents devront être versionnés (via Git) afin de suivre l’évolution de ces derniers.

Le format de documents business dépend des choix et contraintes des équipes. Ce peut être du markdown, PDF, ou .docx, du moment qu’ils respectent les formats et structures propres à l’organisation.

Pour les équipes de communication, le format des contenu dépend de la plateforme et  des personnes cibles. Ils peuvent être sous forme vidéo, photo, publication, bannière, courte vidéo, etc. Le format sera adapté au média utilisé.

### Contenu

Le contenu lié à la mise en place de la nouvelle architecture se fera d’abord en interne pour que chaque personne soit au courant et prenne part à l’avancée.

Elle se formalisera ensuite par du contenu sur les réseaux sociaux et du contenu physique dans différentes zones géographiques pour donner un maximum de visibilité au produit. L’objectif est d’augmenter l’engagement et l’adoption de Foosus.

### Durée et effort

La communication autour du produit s’inscrit dans une durée à long terme, ainsi que des efforts soutenus tout au long du projet. 

La durée et l’effort de communication est avant tout en interne pour la première phase, mais sera étendu aux utilisateurs finaux et prospects lors de la deuxième phase et celles qui suivront.

### Collaboration

Les équipes de Foosus seront amenées à collaborer de manière transdisciplinaire afin d’assurer la cohésion et l’alignement des tous les acteurs du projet jusqu’à atteindre l’état final de l’architecture cible.

Les équipes de communication et Produit collaboreront également avec des acteurs externes, soit pour améliorer la connaissance des problèmes utilisateurs, soit pour promouvoir la solution auprès de la population.

### Rythme de communication

La communication autour du produit s’inscrit dans une durée à long terme, ainsi que des efforts soutenus tout au long du projet. 

La durée et l’effort de communication est avant tout en interne pour la première phase, mais sera étendu aux utilisateurs finaux et prospects lors de la deuxième phase et celles qui suivront.

## **Plan et calendrier du projet**

Le plan et calendrier du projet concerne la phase 1 ainsi que la phase 2, qui aura lieu après la phase de définition de l’architecture cible et du plan de suivi de projet.

Dans l’approche agile adoptée, nous proposons une projection des activités trimestre par trimestre, afin de se fixer des objectifs à moyen terme. De cette manière, nous pourrons rapidement réajuster nos objectifs et fournir une vision à nos équipes. 

Les dates de fin des activités sont définies, mais seront sujets à réflexions aux équipes, afin d’organiser au mieux leur temps de travail.

[Lien notion du calendrier ](https://swyth.notion.site/822c4bd293ea4dfa8af3670187d66669?v=13595747bc7e44a9aa141f716a31d30b&pvs=4) 
![Foosus - Planification de laphase 2 du travail d'architecture](https://raw.githubusercontent.com/agent-swyth/oc-p5-new-architecture/master/images/architecture-planning.png)

## **Risques et facteurs de réduction**

### Analyse de risque (Classification)

| Risque                                                                                                       | ID  | Gravité /4 | Probabilité /4 | Score (Gr. * Pr.) /16 | Classification | Facteur de Réduction                                                                               | Propriétaire |
| ------------------------------------------------------------------------------------------------------------ | --- | ---------- | -------------- | --------------------- | -------------- | -------------------------------------------------------------------------------------------------- | ------------ |
| La livraison de l’architecture d’architecture ne respecte pas les délais imposés                             | R1  | 3          | 3              | 9                     | High           | Découpage des tâches et activités en concertation                                                  | CIO          |
| Les équipes internes de Foosus ne se coordonnent pas durant les phases de conception et réalisation          | R2  | 4          | 2              | 8                     | Low            | Meetings et points de suivis réguliers                                                             | CEO          |
| Le nombre d’inscription d’utilisateurs n’augmente pas suite à la mise en place de la nouvelle architecture   | R3  | 4          | 3              | 12                    | Inacceptable   | Campagne de communication agressive, Visibilité Web, Event physique pour créer de l’engagement     | CEO          |
| Les déploiements de la plateforme provoque des interruptions de disponibilité auprès des utilisateurs finaux | R4  | 4          | 2              | 8                     | Low            | Mise en place de déploiement progressif (rolling deployment) pour ne provoquer aucune interruption | CIO          |
| L’architecture cible n’assure pas la mise à l’échelle du produit en cas de fort engagement                   | R5  | 4          | 2              | 8                     | Low            | Mise en place d’une architecture cible résiliente sans limite de capacité                          | CIO          |
| Le nombre d’adhésions fournisseurs n’atteint pas le niveau escompté                                          | R6  | 3          | 3              | 9                     | High           | Démarchage et prospection continues sur les territoires pour engager de nouveaux fournisseurs      | CEO          |

## **Hypothèses**

Le tableau ci-dessous résume les hypothèses formulées et décidée pour cette Déclaration de travail d’architecture :

| ID  | Hypothèse                                                                                                                                                                                                                                                                         | Impact | Propriétaire |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ | ------------ |
| 1   | Aucune nouvelle fonctionnalité ne sera développée dans la plateforme existante. Elle sera conservée en mode “Maintenance”                                                                                                                                                         | Elevé  | CIO          |
| 2   | La nouvelle architecture sera construite en fonction des technologies actuelles.                                                                                                                                                                                                  | Modéré | CIO          |
| 3   | L’architecture doit permettre d’obtenir le meilleur rapport Qualité-Coût                                                                                                                                                                                                          | Modéré | CIO          |
| 4   | L’architecture peut inclure de nouveaux composants personnalisés ou des composants du commerce pour favoriser la flexibilité, la stabilité et l’extensibilité.                                                                                                                    | Faible | CIO          |
| 5   | Les solutions open-source sont préférables aux solutions payantes                                                                                                                                                                                                                 | Faible | CIO          |
| 6   | L'offre initiale impliquera la coexistence de deux plateformes et la montée en puissance empirique du volume d'utilisateurs qui migreront vers la nouvelle plateforme à mesure que le produit évoluera. Cette augmentation sera proportionnelle à l'évolution des fonctionnalités | Elevé  | CPO          |
| 7   | La géolocalisation, si elle est modélisée suffisamment tôt dans la nouvelle plateforme, permettra d'introduire d'autres innovations en fonction de l'emplacement de l'utilisateur ou du fournisseur alimentaire.                                                                  | Modéré | CPO          |

## **Critères d’acceptation et procédures**

### Métriques et KPI de l’État Cible de l’Architecture

Les métriques suivantes seront utilisées pour déterminer le succès de ce travail d’architecture :

| Métrique                                   | Technique de mesure                                | Valeur cible        | Justification                                                                                                                    |
| ------------------------------------------ | -------------------------------------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| Nombre d'adhésions d'utilisateurs par jour | Nombre d’inscription journalière à la plateforme   | Augmentation de 10% | La nouvelle architecture doit accompagner la croissance de l’entreprise, notamment en augmentant le nombre d’adhésion quotidien. |
| Adhésion de producteurs alimentaires       | Nombre d’inscription à la plateforme               | 4 adhésion / mois   | Actuellement de 1,5/mois, nous souhaitons accélérer l’adhésion de nouveaux fournisseurs                                          |
| Délai moyen de livraison en production     | Temps entre chaque nouveau déploiement             | Moins d’une semaine | Actuellement à 3,5 semaines. Nous souhaitons livrer plus rapidement de petits incréments dans notre plateforme.                  |
| Taux d’incident en production              | Nombre d’incidents avérés en production sur 1 mois | Inférieur à 1/mois  | Actuellement à plus de 25/mois, le taux d’incidence en production a une conséquence sur notre chiffre d’affaire.                 |

### Procédure d’acceptation

1. Lorsque la Déclaration de travail d’architecture est terminée et validée par l’architecte référent, le livrable est présentée aux membres de la direction pour acceptation des travaux. 
2. Il est alors possible de formuler des retours & améliorations avant acceptation finale et signature. Si des changements sont demandés, la finalisation du livrable est rallongée le temps nécessaire à la prise en compte des retours, et refait l’objet d’une présentation auprès de la direction pour acceptation.
3. Une fois que tous les membres de la direction ont validé la Déclaration de travail d’architecture, le document est alors transmis et signé par chaque partie.

## **Approbations signées**

| Validateur | Domaine de responsabilité | Date de signature |
| ---------- | ------------------------- | ----------------- |
| x          | x                         | x                 |
| x          | x                         | x                 |