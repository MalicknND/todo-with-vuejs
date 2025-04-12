# 🎯 Mon Premier Projet Vue.js - Gestionnaire de Tâches

Ce projet est mon premier pas dans l'apprentissage de **Vue.js**. Il s'agit d'un gestionnaire de tâches simple qui me permet de mettre en pratique les concepts fondamentaux du framework.

---

## ✅ Fonctionnalités

- Affichage d'un message si aucune tâche n'est présente.
- Ajout de nouvelles tâches via un champ texte et un bouton **"Ajouter"**.
- Marquage des tâches comme terminées via une case à cocher.
- Affichage des tâches terminées avec un style barré (CSS).
- Tri automatique des tâches : les tâches à faire apparaissent en premier.
- Option pour masquer les tâches terminées.

---

## 🗂 Structure des Tâches

Les tâches sont stockées dans un tableau d’objets JSON au format suivant :

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

---

## 🎓 Objectifs d'Apprentissage

Ce projet m’a permis de découvrir et pratiquer :

- Les composants Vue.js
- La gestion d'état (`ref`, `computed`)
- La réactivité de l’interface
- Les directives Vue.js (`v-model`, `v-if`, `v-for`, `@submit`, etc.)
- Le style conditionnel avec `:class`
- La manipulation du DOM
- La gestion des événements
- Le filtrage et tri dynamique des données

---

## ⚙️ Installation et Lancement

### 🔧 Prérequis

- Node.js (version 14 ou supérieure)
- npm (gestionnaire de paquets)

### 📥 Installation

1. Clonez le projet :

   ```bash
   git clone https://github.com/MalicknND/todo-with-vuejs.git
   cd todo-with-vuejs
   ```

2. Installez les dépendances :

   ```bash
   npm install
   ```

### 🚀 Lancement en Développement

Pour démarrer le serveur de développement :

```bash
npm run dev
```

Le projet sera accessible à l’adresse :  
📍 `http://localhost:5173`

### 🏗️ Build de Production

Pour générer la version optimisée :

```bash
npm run build
```

Les fichiers seront disponibles dans le dossier `dist/`.

---

# 📝 To-Do App with Vue.js (English Summary)

This is a simple and functional To-Do application built using **Vue.js**. It allows users to add, mark, and filter tasks, providing a clean and interactive user interface.

---

## Features

- Add new tasks using a simple input form.
- Mark tasks as completed with a checkbox.
- Hide or show completed tasks with a toggle.
- Tasks are automatically sorted with incomplete ones on top.
- Each task includes a timestamp when created.

---

## Technologies Used

- **Vue.js** — JavaScript framework for building UI
- **HTML & CSS** — Structure and design

---

## Getting Started

### 1. Clone the repository:

```bash
git clone https://github.com/MalicknND/todo-with-vuejs.git
```

### 2. Go into the project folder:

```bash
cd todo-with-vuejs
```

### 3. Install dependencies:

```bash
npm install
```

### 4. Start the development server:

```bash
npm run dev
```

### 5. Open in browser:

Go to [http://localhost:5173](http://localhost:5173) to use the app.

---

## 🧑‍💻 Usage

- Type a task in the input field and click **"Ajouter"** to add it.
- Check the box to mark a task as completed.
- Use the **"Masquer les tâches terminées"** option to hide completed tasks.
- Tasks are auto-sorted: incomplete tasks come first.