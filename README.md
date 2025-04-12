# Mon Premier Projet Vue.js - Gestionnaire de Tâches

Ce projet est mon premier pas dans l'apprentissage de Vue.js. Il s'agit d'un gestionnaire de tâches simple qui me permet de mettre en pratique les concepts fondamentaux de Vue.js.

## Fonctionnalités

- Affichage d'un message si aucune tâche n'est présente
- Ajout de nouvelles tâches via un champ texte et un bouton "Ajouter"
- Marquage des tâches comme terminées via une case à cocher
- Tâches terminées affichées avec un style barré (CSS)
- Tri des tâches : les tâches à faire apparaissent en premier
- Option pour masquer les tâches terminées

## Structure des Tâches

Les tâches sont stockées dans un format JSON avec les propriétés suivantes :
```json
[
    { 
        "title": "Acheter la propriété 'Rue de la Paix'", 
        "completed": false, 
        "date": 20240730 
    },
    { 
        "title": "Construire un hôtel sur 'Avenue Foch'", 
        "completed": false, 
        "date": 20240730 
    },
    { 
        "title": "Éviter la case prison", 
        "completed": false, 
        "date": 20240730 
    }
]
```

## Objectifs d'Apprentissage

Ce projet me permet de découvrir et pratiquer :
- Les composants Vue.js
- La gestion d'état
- La réactivité
- Les directives Vue.js
- Le style conditionnel
- La manipulation du DOM
- Les événements
- Le stockage des données

## Installation et Lancement

### Prérequis
- Node.js (version 14 ou supérieure)
- npm (gestionnaire de paquets Node.js)

### Installation

1. Clonez le projet :
```bash
git clone [https://github.com/MalicknND/todo-with-vuejs]
cd todo-with-vuejs
```

2. Installez les dépendances :
```bash
npm install
```

### Développement

Pour lancer le serveur de développement :
```bash
npm run dev
```

Le projet sera accessible à l'adresse : `http://localhost:5173`

### Production

Pour construire le projet pour la production :
```bash
npm run build
```

Les fichiers de production seront générés dans le dossier `dist/`.
