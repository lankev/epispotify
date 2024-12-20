# EpiSpotify

**EpiSpotify** est une application de streaming musical inspirée de Spotify. Ce projet a pour but de recréer une plateforme musicale moderne, interactive et intuitive, avec des fonctionnalités telles que la gestion de playlists, la lecture audio, et les recommandations personnalisées.

---

## 📋 Cahier des charges

### Objectif
Créer une application de streaming musical **EpiSpotify**, fonctionnelle et évolutive, avec une interface inspirée de Spotify et des fonctionnalités clés adaptées aux besoins des utilisateurs.

### Durée totale
**3 mois** avec **2 jours de travail par semaine**, soit 24 jours de développement, répartis en évolutions majeures toutes les deux semaines.

---

## 🛠 Fonctionnalités

### Mois 1 : Fondation technique et interface de base
- **Interface utilisateur** :
  - **Barre latérale** : Accès à Accueil, Recherche, Bibliothèque, Playlists.
  - **Zone principale** : Affichage des playlists sous forme de cartes.
  - **Lecteur audio** : Contrôles de base (Lecture, Pause, Précédent, Suivant).
- **Backend minimal** :
  - Chargement des playlists et chansons depuis des fichiers JSON statiques.
- **Design** :
  - Utilisation de la palette Spotify (noir, gris, vert) et mise en page responsive.

### Mois 2 : Fonctionnalités utilisateur
- **Recherche** :
  - Champ de recherche dynamique pour filtrer les chansons et playlists.
- **Gestion des playlists** :
  - Création, modification et suppression de playlists.
  - Ajout et suppression de chansons dans les playlists.
- **Recommandations dynamiques** :
  - Suggestions basées sur des genres ou chansons populaires.

### Mois 3 : Fonctionnalités avancées
- **Écoute collaborative** :
  - Lecture synchronisée entre plusieurs utilisateurs simulés.
- **Mode hors ligne** :
  - Téléchargement et stockage local des chansons (localStorage).
- **Statistiques utilisateur** :
  - Affichage des chansons les plus écoutées et des playlists favorites.
- **Optimisation UX** :
  - Animations, transitions, et interface finalisée pour mobile et desktop.

---

## 🗓️ Planification

### Semaine par semaine
| **Semaine** | **Objectif**                                                                 |
|-------------|-------------------------------------------------------------------------------|
| Semaine 1   | Création de la structure HTML/CSS (barre latérale, zone principale, lecteur).|
| Semaine 2   | Design : Palette EpiSpotify, mise en page responsive.                        |
| Semaine 3   | Intégration des playlists statiques sous forme de cartes avec JSON.          |
| Semaine 4   | Implémentation du lecteur audio (lecture, pause, suivant, précédent).         |
| Semaine 5   | Création d'un champ de recherche dynamique.                                  |
| Semaine 6   | Fonctionnalité de gestion de playlists (création, modification).             |
| Semaine 7   | Suppression de chansons et de playlists.                                     |
| Semaine 8   | Intégration de recommandations dynamiques.                                   |
| Semaine 9   | Écoute collaborative simulée.                                                |
| Semaine 10  | Ajout d’un mode hors ligne (localStorage).                                   |
| Semaine 11  | Statistiques utilisateur (chansons les plus écoutées, playlists favorites).  |
| Semaine 12  | Finalisation : Animations, responsive, tests et corrections.                 |

---

## ⚙️ Technologies utilisées

### Frontend
- **HTML/CSS/JavaScript** : Construction de l'interface et interactions dynamiques.
- **Responsive Design** : Flexbox et Media Queries.

### Backend
- **Webstrator** : Gestion des workflows backend, API, et base de données.

### Base de données
- Collections dans Webstrator :
  - `users` : Informations des utilisateurs (nom, email, playlists).
  - `songs` : Liste des chansons (titre, artiste, fichier audio).
  - `playlists` : Données des playlists créées par les utilisateurs.

---

## 📂 Structure des fichiers

EpiSpotify/ 
│ 
├── index.html # Fichier principal pour l'interface utilisateur 
├── styles.css # Fichier de styles CSS pour l'application 
├── script.js # Logique principale (JavaScript) 
├── data/ │ 
├── musics.json # Liste des chansons (données statiques) 
│ 
└── playlists.json # Liste des playlists (données statiques) 
└── assets/ 
├── images/ # Couvertures d'albums 
└── songs/ # Fichiers audio

**Cloner le projet** :
   ```bash
   git clone https://github.com/votre-repo/EpiSpotify.git
   cd EpiSpotify
