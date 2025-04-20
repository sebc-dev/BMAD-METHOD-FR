# {Nom du Projet} PRD

## Statut : { Brouillon | Approuvé }

## Introduction

{ Court paragraphe de 1-2 phrases décrivant le quoi et le pourquoi de ce que le PRD va réaliser, comme indiqué dans le brief du projet ou à travers les questions des utilisateurs }

## Objectifs et Contexte

{
Une courte synthèse du brief du projet, avec des points sur :

- Objectifs clairs du projet
- Résultats mesurables
- Critères de succès
- Indicateurs clés de performance (KPI)
  }

## Fonctionnalités et Exigences

{

- Exigences fonctionnelles
- Exigences non fonctionnelles
- Exigences d'expérience utilisateur
- Exigences d'intégration
- Exigences de test
  }

## Liste des Épopées

{ Nous testerons complètement avant que chaque histoire soit terminée, il n'y aura donc pas d'épopée dédiée et d'histoires à la fin pour les tests }

### Épopée 0 : Configuration manuelle initiale ou provisionnement

- histoires ou tâches que l'utilisateur pourrait avoir besoin d'effectuer, comme s'inscrire ou configurer un compte ou fournir des clés API, configurer manuellement certaines ressources locales comme un LLM, etc...

### Épopée-1 : Épopée PRD actuelle (par exemple, épopée backend)

#### Histoire 1 : Titre

Exigences :

- Faire X
- Créer Y
- Etc...

### Épopée-2 : Deuxième épopée PRD actuelle (par exemple, épopée frontend)

### Épopée-N : Améliorations futures des épopées (au-delà de la portée du PRD actuel)

<exemple>

## Épopée 1 : Mon application peut récupérer des données

#### Histoire 1 : Configuration du projet et de NestJS

Exigences :

- Installer NestJS CLI globalement
- Créer un nouveau projet NestJS avec le générateur CLI nestJS
- Tester les fonctionnalités de démarrage du modèle d'application
- Initialiser le dépôt Git et valider la configuration initiale du projet

#### Histoire 2 : Route API de récupération des actualités

Exigences :

- Créer une route API qui renvoie une liste d'actualités et de commentaires depuis la source d'actualités foo
- Le corps de la requête POST spécifie le nombre de publications, d'articles et de commentaires à renvoyer
- Créer une commande dans package.json que je peux utiliser pour appeler la route API (route configurée dans env.local)

</exemple>

## Pile technologique

{ Tableau répertoriant les choix de langages, bibliothèques, infrastructure, etc... }

<exemple>
  | Technologie | Version | Description |
  | ---------- | ------- | ----------- |
  | Kubernetes | x.y.z | Plateforme d'orchestration de conteneurs pour le déploiement de microservices |
  | Apache Kafka | x.y.z | Plateforme de streaming d'événements pour l'ingestion de données en temps réel |
  | TimescaleDB | x.y.z | Base de données temporelle pour le stockage des données de capteurs |
  | Go | x.y.z | Langage principal pour les services de traitement de données |
  | GoRilla Mux | x.y.z | Framework d'API REST |
  | Python | x.y.z | Utilisé pour l'analyse de données et les services ML |
</exemple>

## Structure du projet

{ Diagramme de l'organisation des dossiers et fichiers avec descriptions }

<exemple>

{ diagramme d'arborescence de dossiers }

</exemple>

### Fonctionnalités POST MVP / PRD

- Idée 1
- Idée 2
- ...
- Idée N

## Journal des modifications

{ Tableau Markdown des changements clés après que le document n'est plus à l'état de brouillon et est mis à jour, le tableau comprend le titre du changement, l'ID de l'histoire pendant laquelle le changement s'est produit, et une description si le titre n'est pas suffisamment clair }

<exemple>
| Changement           | ID Histoire | Description                                                      |
| -------------------- | ----------- | ---------------------------------------------------------------- |
| Brouillon initial    | N/A         | Brouillon initial du PRD                                         |
| Ajout Pipeline ML    | histoire-4  | Intégration de l'histoire du service de prédiction par ML        |
| Mise à jour Kafka    | histoire-6  | Mise à niveau de Kafka 2.0 à Kafka 3.0 pour améliorer les performances |
</exemple>
