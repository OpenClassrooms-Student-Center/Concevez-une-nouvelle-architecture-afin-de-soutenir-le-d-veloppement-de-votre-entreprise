---
title: Vision Architecturale
description: Projet Foosus, Platforme d'achat de produits locaux
---

# Vision Architecturale


| Projet  | Nouvelle Architecture d’Entreprise |
| ------- | ---------------------------------- |
| Client  | Foosus                             |
| Auteurs | Yoann Talon                        |


---

  

## **Objectif de ce document**

  

Ce document fournit un résumé partiellement achevé des changements requis de l’entreprise pour un déploiement réussi de l’État Cible de l’Architecture (ECA) pour une plateforme Foosus géoconsciente et éprouvée pour l’avenir.

  

Cette Vision architecturale doit fournir aux parties prenantes clés et à l’équipe de Direction un accord formel sur le résultat attendu. Un accord conclu tôt sur le résultat attendu, en amont de l’expérimentation au sein de l’équipe, permet aux architectes et aux responsables de notre plateforme de se concentrer sur les étapes nécessaires à la validation de la faisabilité et de la concordance de l’ECA avec l’objectif.

  

Ce document est pensé pour fournir une version sommaire de l’architecture à réaliser à travers l’investissement dans la Déclaration architecturale de Travail associée.

  

## **Description du problème**

  

La plateforme historique de Foosus a atteint un stade critique où elle n’est plus adaptée à son objet. Les équipes de développement sont pleinement investies dans l’extinction d’incendies et dans son maintien en état de marche, ce qui a ralenti notre capacité à livrer de nouvelles fonctionnalités et à rester compétitifs au sein d’un marché nouveau et imprévisible.

  

Les analyses de marché indiquent que notre correspondance avec le marché a été éclipsée par l’instabilité de la plateforme et par une image de marque négative causée par des interruptions de service visibles par le public.

  

En réponse à un fort déclin des inscriptions utilisateurs, nous souhaitons conserver la plateforme existante en mode maintenance et restructurer les équipes afin de livrer une plateforme à l’architecture travaillée, qui lui permette de grandir de manière alignée sur notre vision business de soutien aux marchés locaux. Les inscriptions constituent une métrique clé aux yeux de nos investisseurs et ne peuvent être améliorées que par l’agilité nécessaire pour innover rapidement et expérimenter avec des variantes d’offres produit existantes.

  

Notre objectif business est de sortir de manière rapide et itérative un nouveau produit qui pourra coexister dans un premier temps avec la plateforme existante, avant de la remplacer.

  

L’objectif de ce projet est de mettre en place les contraintes et la direction architecturales permettant d’itérer rapidement vers nos objectifs business.

  

Le problème est détaillé davantage dans le brief sur les Conditions fonctionnelles requises de Haut Niveau produit par le CIO et le CPO, qui remplace une requête de travail architectural.

  

## **Contraintes et difficultés**

  

### Taux d’inscription utilisateurs

  

**Parties prenantes : Ash Callum, CEO et Jo Kumar, CFO.**

  

Le consortium d’investisseurs actuels mesure notre valeur en fonction de notre capacité à maintenir un taux positif d’inscriptions de nouveaux utilisateurs.

  

Cette métrique a chuté rapidement au cours des derniers mois et doit être améliorée en priorité. L’expansion au sein des marchés locaux et le fait de fournir du géo ciblage sont vus comme des facteurs critiques pour toucher une gamme plus large d’utilisateurs.

  

Toute architecture doit être conçue pour se mettre à l’échelle en suivant notre base clients.

  

### Innover dans le périmètre d’une Architecture d’Entreprise

  

**Parties prenantes : CIO, CPO, CFO**

  

La plateforme historique de Foosus a naturellement évolué vers la complexité en raison du changement rapide et d’un manque de vision long terme. Tout en préservant un sentiment de possession chez chaque ingénieur et partenaire impliqué dans la création de la nouvelle plateforme, nous avons besoin d’un périmètre clair pour assurer que chaque incrément soit considéré selon son impact sur le fait de fournir les capacités business nécessaires et de soutenir la croissance à venir de Foosus.

  

### Soutenir l’innovation technique rapide et l’expérimentation

  

**Parties prenantes : CMO, CIO, CPO, CFO**

  

Le marché actuel voit nos concurrents directs prendre rapidement l’avantage en pivotant en réponse à de nouvelles informations apprises. L’apprentissage doit être au cœur de notre état cible de l’architecture, étant donné que cela a été verrouillé par des solutions par le passé, d’une manière qui a généré davantage d’instabilité et de dette technique.

  

La plateforme doit être conçue en gardant à l’idée l’extensibilité et la personnalisation des fonctionnalités.

  

### Visibilité de la plateforme

  

**Parties prenantes : CMO, CPO, Directeur des Opérations**

  

Le comportement technique de la plateforme, non plus que sa performance d’un point de vue du business, n’est pas clair. Toutes les connaissances acquises actuellement nécessitent des analyses de registres et de feuilles de calcul, avant de pouvoir rechercher l’intelligence business.

  

Nous avons besoin d’un design d’architecture qui nous offre en temps réel des connaissances et une vision de la santé de la plateforme techniquement et d’un point de vue commercial.

  

### Améliorer la réputation de Foosus sur le marché grâce à la stabilité

  

La marque Foosus doit être renforcée en réduisant les interruptions de service visibles par les utilisateurs. Cela implique :

  

- Des process pour réduire le risque de sortir des solutions qui échouent ou qui soient de mauvaise qualité

- La capacité de sortir de nouvelles versions de notre plateforme sans impacter l’utilisateur par des interruptions de service.

  

Les sorties à 3 h du matin semblaient fonctionner lorsque nos utilisateurs se trouvaient principalement dans la même zone géographique, mais nous ne devons plus dépendre de cela.

  

## **Objectifs détaillés**

  

L’objet de cette section est de décrire les objectifs détaillés qui doivent être atteints par l’état cible de l’architecture Foosus.

  

La section précédente a couvert les problèmes business sous-jacents, tandis que cette section détaille les objectifs de la solution d’architecture, qui permettront de résoudre le problème business.

  

Nous voulons mener des campagnes de marketing Foosus dans de nombreuses grandes villes, avec l’assurance que notre plateforme demeurera utilisable, réactive, et délivrera une expérience client de première classe. Pour parvenir à ce but, nous avons besoin de concevoir une solution d’architecture et un processus de gouvernance qui nous aident à atteindre l’ensemble des objectifs business actuels, ainsi que la vision globale.

  

### Environnement et modèles de processus

  

L’objet de cette section est de tracer les contours de l’environnement et des processus de modèles qui entrent dans le périmètre de l’état cible de l’architecture Foosus.

  

### Processus business entrant dans le périmètre de la vision

  

- Recherche dans l’interface client et commande de produits de consommation.

  

### Environnement business et technologique dans le périmètre de la vision

  

- Application web Foosus et autres atouts logiciel (services)

- Infrastructure Runtime

- Infrastructure et processus de développement

  

### Utilisateurs qui interagissent avec le process business

  

- Les fournisseurs alimentaires soumettront à Foosus un inventaire des produits

alimentaires disponibles

- Les clients des produits de consommation trouveront et commanderont des

produits alimentaires

- Les fournisseurs alimentaires recevront des commandes

- L’équipe finance de Foosus recevra les paiements

  

### Flux d’informations pour les process business

Voir **[la carte des flux de valeurs organisationnelle pour les flux actuels.](https://s3-eu-west-1.amazonaws.com/course.oc-static.com/projects/Architecte+Logiciel+FR/P5/FLUX_P5.png)**


***À faire : Nouveaux flux à définir par le nouvel architecte.***

  

## **Acteurs, rôles et responsabilités**

Cette section décrit les utilisateurs/acteurs du système dans le périmètre de l’état cible de l’architecture Foosus. Les acteurs/utilisateurs du système sont les utilisateurs qui interagissent avec un système. Ils peuvent être humains ou être un système/ordinateur.

  

### Utilisateurs humains et rôles

  

- Client de produit de consommation — acheteur

- Fournisseur alimentaire — vendeur

- Représentant de l’équipe satisfaction client — face au client

- Développeur — exécutant

- Membre de l’équipe finance — facturation

  

### Acteurs informatiques et rôles

  

- Systèmes d’inventaire

- Systèmes de commande

- Systèmes de recherche

- Systèmes de facturation

- Système d’identité et d’accès

### Responsabilités

- Les systèmes de facturation doivent garantir que les fournisseurs alimentaires soient facturés pour une commission, comme tous les paiements soient effectués directement à la livraison.

  

## **Modèle d’architecture**

  

Cette section décrit les principes et les limites de l’état cible de l’architecture.

  

### Diagramme de haut niveau

  

![Container view (C4 Model) of Foosus Target Architecture](https://raw.githubusercontent.com/agent-swyth/oc-p5-new-architecture/master/images/foosus-target-architecture-c4-container-view.png)

### Design patterns (Schémas de conception)

  

**Le modèle backend pour frontends est supprimé** dans cette architecture cible afin de réduire la complexité technique et la maintenance. Une seule API pour une application multiplateforme suffit car les données envoyées aux applications front-end sont optimisés pour les connexions bas débit

  

D’autres schéma d’architecture frontend et backend ont été retenu :

  

**Micro frontend** :

  

Développer des applications ou plusieurs équipes interviennent pour des périmètres qui concerne la fonction de leur équipe. Exemple : Equipe chargée de la recherche, une autre du paiement. Ce schéma permettra à toutes les équipes de travailler ensemble sur chaque application et leur implémentation.

  

**Single Page Application** :

  

Implémentation d’une application web/Mobile dans un seul document web, mettant à jour le corps du document pour naviguer dans les différentes vues de l’application grâce aux API Javascript.

  

**[Gateway routing](https://learn.microsoft.com/en-us/azure/architecture/patterns/gateway-routing)** :

  

Routage des requêtes de multiple instances de services en utilisant un seul point de terminaison. Utile pour l’équilibrage de charge, la disponibilité des serveurs, la montée en version des environnements de production.

  

**[Retry pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/retry) :**

  

> Permet à une application de gérer les échecs transitoires lorsqu'elle tente de se connecter à un service ou à une ressource réseau, en réessayant de manière transparente une opération qui a échoué. Cela peut améliorer la stabilité de l'application.

*[Cloud Design patterns, Microsoft](https://learn.microsoft.com/en-us/azure/architecture/patterns/retry)*

>

  

## **Conditions requises correspondant à l’architecture cible**

  

Voir **[Brief des Conditions Requises pour le Business Haut Niveau](https://s3-eu-west-1.amazonaws.com/course.oc-static.com/projects/Architecte+Logiciel+FR/P5/V2+Geo-Aware+Food+Sourcing+-+Briefbusiness+haut+niveau_FR+(1).pdf)**

  

## **Contraintes impactant l’architecture cible**

  

Voir les contraintes pour les parties prenantes ci-dessus.

  

## **Principes impactant l’architecture cible**


### Principes généraux

  

- Décisions pilotées par le feed-back et l’apprentissage.

- Faire des choix qui soutiennent les objectifs long terme.

- Accepter le fait que les erreurs se produisent.

- Nous assurer que nous concevons l’architecture pour échouer vite et nous améliorer.

  

### Principes Business

  

- Soutenir l’innovation et l’agilité du business grâce à l’extensibilité

- Soutenir la réputation de la marque grâce à la stabilité

  

### Principes Data

  

- Toujours modéliser comme si vous n’aviez pas encore la vision d’ensemble.

- Toujours protéger les données permettant l’identification personnelle.

- Concevoir pour l’accès aux données ou la mutabilité en fonction du problème.

- Appliquer la cohérence en fonction du scénario pour satisfaire au mieux le besoin business. (Ne partez pas du principe que toutes les données doivent être cohérentes immédiatement ou même à terme.)

- Refléter le modèle de domaine au sein d’un contexte délimité de façon aappropriée.

  

### Principes d’application

  

- Responsabilité unique et couplage faible des applications.

- Concevoir des interfaces ouvertes et extensibles en systèmes, sur lesquelles il est facile d’itérer.

- Appliquer une approche pilotée par le contrat client, où les interfaces entre les systèmes reflètent uniquement les données et opérations nécessaires à leur intégration.

- Éviter les dépendances cycliques entre les systèmes.

  

### Principes technologiques

  

- Faire des choix ouverts et aisés à modifier.

  

# **Vision de l’état cible**

- Plateforme historique décommissionnée

- Une plateforme favorable à l’expérience développeur, qui aide les développeurs à satisfaire de nouvelles nécessités business, en accord avec les feuilles de route business et technique à plus long terme.