# Contrat de Conception et de Développement de l’Architecture

| Projet  | Nouvelle Architecture d’Entreprise |
| ------- | ---------------------------------- |
| Client  | Foosus                             |
| Auteurs | Yoann Talon                        |
---

## **Objet de ce document**

Les Contrats d’Architecture sont les accords communs entre les partenaires de développement et les sponsors sur les livrables, la qualité, et la correspondance à l’objectif d’une architecture. L’implémentation réussie de ces accords sera livrée grâce à une gouvernance de l’architecture efficace (voir TOGAF Partie VII, Gouvernance de l’architecture). En implémentant une approche dirigée du management de contrats, les éléments suivants seront garantis :

- Un système de contrôle continu pour vérifier l’intégrité, les changements, les prises de décisions, et l’audit de toutes les activités relatives à l’architecture au sein de l’organisation.
- L’adhésion aux principes, standards et conditions requises des architectures existantes ou en développement
- L’identification des risques dans tous les aspects du développement et de l’implémentation des/de l’architecture(s), y compris le développement interne en fonction des standards acceptés, des politiques, des technologies et des produits, de même que les aspects opérationnels des architectures de façon à ce que l’organisation puisse poursuivre son business au sein d’un environnement résilient.
    - Un ensemble de processus et de pratiques qui garantissent la transparence, la responsabilité et la discipline au regard du développement et de l’utilisation de tous les artefacts architecturaux
    - Un accord formel sur l’organe de gouvernance responsable du contrat, son degré d’autorité, et le périmètre de l’architecture sous la gouvernance de cet organe

Ceci est une déclaration d’intention signée sur la conception et le développement de l’architecture d’entreprise, ou de parties significatives de celles-ci, de la part d’organisations partenaires, y compris les intégrateurs système, fournisseurs d’applications, et fournisseurs de service.

De plus en plus, le développement d’un ou plusieurs domaine(s) d’architecture (business, données, application, technologie) peut être externalisé, avec la fonction d’architecture de l’entreprise fournissant une vue d’ensemble de l’architecture d’entreprise globale, ainsi que la coordination et le contrôle de l’effort total. Dans certains cas, même ce rôle de supervision peut être externalisé, bien que la plupart des entreprises préfèrent conserver cette responsabilité clé en interne.

Quelles que soient les spécificités des dispositions d’externalisation, les dispositions elles-mêmes seront normalement gouvernées par un Contrat d’Architecture qui définit les livrables, la qualité, et la correspondance à l’objectif de l’architecture développée, ainsi que les processus de collaboration pour les partenaires du développement de l’architecture.

## **Introduction et Contexte**

La plateforme Foosus actuelle ne peut **plus soutenir la croissance et l’expansion** de l’entreprise avec **son architecture actuelle**. 

Ses **analyses commerciales** ont montré que **les clients souhaitent acheter local** et être **mis en relation** avec des **producteurs près de chez eux**. 

L’entreprise souhaite **créer une nouvelle plateforme** qui **soutiendra sa croissance** et fournira à leurs **clients une nouvelle expérience**.

## **La Nature de l’accord**

La nature de l'accord avec les équipes techniques est de définir les livrables, la qualité et la correspondance à l'objectif de l'architecture développée, ainsi que les processus de collaboration pour les partenaires du développement de l'architecture.

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

- **La mise en œuvre de l’Etat Cible de l’Architecture**, tel que définit dans les documents dans la vision architecturale, la déclaration de travail d’architecture.

### Parties prenantes, préoccupations et visions

Le tableau suivant montre les parties prenantes qui utilisent ce document, leurs préoccupations, et la façon dont le travail d’architecture répondra à ces préoccupations par l’expression de plusieurs visions, ou perspectives.

| Partie prenante                | Préoccupation                                                                                  | Vision                                                                                  |
| ------------------------------ | ---------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| CEO - Board Members            | La nouvelle architecture doit assurer le développement économique de l’entreprise.             | Faire rayonner Foosus au niveau départemental, régional, national, international.       |
| Engineering Product Team       | Concevoir et intégrer de nouvelles fonctionnalités utilisables et réactives.                   | Offrir une expérience utilisateur de premier plan.                                      |
| Engineering (Development) Team | Concevoir et développer les nouvelles fonctionnalité, en augmentant la vélocité des livraison. | Libérer la créativité et l’expérience de développement. Donner le meilleur d’eux-mêmes. |
| Engineering (Operations) Team  | Déployer et maintenir une plateforme évolutive, résiliente et sécurisée.                       | Assurer la sécurité des services de Foosus                                              |

## **Description de l’architecture, principes stratégiques et conditions requises**

### Description

L'architecture cible de Foosus vise à créer une nouvelle plateforme qui permettra de répondre aux besoins des clients en matière d'achat local en reliant les fournisseurs locaux et les consommateurs grâce à la géolocalisation. 

Cette plateforme sera évolutive et résiliente, offrira une expérience utilisateur de premier plan et prendra en charge différents types d'utilisateurs (consommateurs, fournisseurs locaux, personnel back-office Foosus) avec des fonctionnalités et des services spécifiques pour chacun, au sein d'une même plateforme. 

Elle proposera une solution multi-plateforme (Web et mobile) pour les utilisateurs et offrira une alternative automatisée pour mettre à jour l'inventaire des produits alimentaires. 

Enfin, l'architecture cible de Foosus réaménagera la chaîne de valeur en optimisant les délais d'approvisionnement et de livraison afin de diminuer le lead time.

### Principes stratégiques

**Principes généraux :**

- Décisions pilotées par le feed-back et l’apprentissage.
- Faire des choix qui soutiennent les objectifs long terme.
- Accepter le fait que les erreurs se produisent.
- Nous assurer que nous concevons l’architecture pour échouer vite et nous
améliorer.

**Principes Data :** 

- Toujours modéliser comme si vous n’aviez pas encore la vision d’ensemble.
- Toujours protéger les données permettant l’identification personnelle.
- Concevoir pour l’accès aux données ou la mutabilité en fonction du problème.
- Appliquer la cohérence en fonction du scénario pour satisfaire au mieux le
besoin business. (Ne partez pas du principe que toutes les données doivent être cohérentes immédiatement ou même à terme.)
- Refléter le modèle de domaine au sein d’un contexte délimité de façon
appropriée.

**Principes applicatifs :** 

- Responsabilité unique et couplage faible des applications.
- Concevoir des interfaces ouvertes et extensibles en systèmes, sur lesquelles il est facile d’itérer.
- Appliquer une approche pilotée par le contrat client, où les interfaces entre les systèmes reflètent uniquement les données et opérations nécessaires à leur intégration.
- Éviter les dépendances cycliques entre les systèmes.

### Référence aux Conditions requises pour l’architecture

Se référer aux conditions requises pour l’architecture détaillée de le document de spécifications des conditions requises pour l’architecture.

## **Livrables architecturaux**

*Livrables architecturaux qui satisfont aux conditions requises pour le business.*

### Développement de l’architecture

Ci dessous, la vue de haut niveau de l’Etat cible de l’architecture ainsi que de ses applicatifs principaux à développer et mettre en œuvre :

![Container view (C4 Model) of Foosus Target Architecture](https://raw.githubusercontent.com/agent-swyth/oc-p5-new-architecture/master/images/foosus-target-architecture-c4-container-view.png)

Voire la vision architecture pour les schémas de conception (Design Patterns) retenus

### Mesures de l’architecture cible

- Rapports et suivi des incidents dans els environnements d’exploitation
- Rapports de test de niveau Système, Intégration et unitaire.
- Métriques de disponibilité et de temps de réponses HTTP
- Métriques business associés au travail d’architecture.

## **Plan de travail commun priorisé**

Afin de réussir à mettre en œuvre cette architecture, le plan de travail commun priorisé se base sur les activités définies dans la planification du projet, tel que présentée dans la section [Calendrier](https://www.notion.so/Contrat-de-Conception-et-de-D-veloppement-de-l-Architecture-e1fdeb2393544f0baba96948642a5319?pvs=21) du document.

Les différentes équipes et les responsables mèneront des réunions pour prioriser au mieux leurs travaux.

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

En interne : 

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

## **Risques et facteurs de réduction**

### Structure de gouvernance

Le schéma ci-dessous modélise la structure de gouvernance au sein de Foosus.

![Organigramme de la société Foosus](https://raw.githubusercontent.com/agent-swyth/oc-p5-new-architecture/master/images/org-chart.png)

### Analyse des risques

| Risque                                                                                                       | ID  | Gravité /4 | Probabilité /4 | Score (Gr. * Pr.) /16 | Classification | Facteur deRéduction                                                                                | Propriétaire |
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

# **Calendrier**
Le plan et calendrier du projet concerne la phase 1 ainsi que la phase 2, qui aura lieu après la phase de définition de l’architecture cible et du plan de suivi de projet.

Dans l’approche agile adoptée, nous proposons une projection des activités trimestre par trimestre, afin de se fixer des objectifs à moyen terme. De cette manière, nous pourrons rapidement réajuster nos objectifs et fournir une vision à nos équipes. 

Les dates de fin des activités ne sont pas clairement définies, mais seront sujets à réflexions et consensus des équipes.

[Lien notion du calendrier ](https://swyth.notion.site/822c4bd293ea4dfa8af3670187d66669?v=13595747bc7e44a9aa141f716a31d30b&pvs=4) 

![OC P5 - Foosus Project planification Phase 1 & 2 (1)](https://raw.githubusercontent.com/agent-swyth/oc-p5-new-architecture/master/images/architecture-planning.png)

## **Personnes approuvant ce plan**

| Validateur | Domaine de responsabilité | Date |
| ---------- | ------------------------- | ---- |
| x          | x                         | x    |
| x          | x                         | x    |