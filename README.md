# FetchTasks - Gestion Sécurisée des Requêtes API

Ce projet est une implémentation simple d'un script Node.js pour interagir avec une API externe de manière sécurisée. Il utilise Axios pour effectuer des requêtes HTTP et intègre des mécanismes de gestion des erreurs et de sécurité via des variables d'environnement.

---

## Table des matières

- [Introduction](#introduction)
- [Fonctionnalités](#fonctionnalités)
- [Prérequis](#prérequis)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Exemple d'Exécution](#exemple-dexécution)
- [Dépendances](#dépendances)
- [Contributeurs](#contributeurs)
- [Licence](#licence)

---

## Introduction

Ce script permet de :
1. Récupérer des données (tâches) depuis une API externe.
2. Utiliser des en-têtes sécurisés pour authentifier les requêtes.
3. Gérer les erreurs réseau et les réponses inattendues de manière robuste.

Ce projet peut servir de modèle pour intégrer des fonctionnalités similaires dans des applications plus complexes.

---

## Fonctionnalités

- Envoi de requêtes GET sécurisées à une API externe.
- Gestion des clés d'API via des variables d'environnement.
- Vérification explicite du statut HTTP des réponses.
- Gestion des erreurs réseau et API avec des messages clairs.

---

## Prérequis

- [Node.js](https://nodejs.org/) (v14+ recommandé)
- [npm](https://www.npmjs.com/)

---

## Installation

1. Clonez le dépôt :
   ```bash
   git clone https://github.com/votre-repo/fetch-tasks.git
   cd fetch-tasks
   ```

2. Installez les dépendances :
   ```bash
   npm install
   ```

---

## Configuration

Avant d'exécuter le script, configurez les variables d'environnement nécessaires dans un fichier `.env` situé à la racine du projet. Exemple de fichier `.env` :  

```env
API_URL=https://api.example.com/tasks
API_KEY=your_api_key_here
```

- `API_URL` : L'URL de l'API que vous souhaitez interroger.  
- `API_KEY` : La clé d'API ou le jeton d'authentification pour accéder à l'API.

---

## Usage

Pour exécuter le script :
```bash
node index.js
```

Le programme récupérera une liste de tâches depuis l'API spécifiée et les affichera dans la console.

---

## Exemple d'Exécution

Après configuration, une exécution typique pourrait ressembler à ceci :  

### Commande
```bash
node index.js
```

### Sortie
```
Liste des tâches: [
  { id: 1, description: "Tâche 1", status: "done" },
  { id: 2, description: "Tâche 2", status: "pending" }
]
```

En cas d'erreur, des messages clairs seront affichés, par exemple :  
```
Erreur API: 401 - Unauthorized
```

---

## Dépendances

Ce projet utilise les dépendances suivantes :  

- **dotenv** : Chargement des variables d'environnement depuis un fichier `.env`.
- **axios** : Client HTTP pour Node.js.

Installez toutes les dépendances avec :
```bash
npm install
```

---

## Contributeurs

- [Votre Nom](https://github.com/fabioramefiarison) - Développeur principal.

---

