# **EpiSpotify**

**EpiSpotify** est une application de streaming musical inspirée de Spotify. Ce projet a pour but de recréer le plus loin possible une plateforme musicale moderne, interactive et intuitive, avec des fonctionnalités telles que la gestion de playlists, la lecture audio, et la possibilité de télécharger des playlists au format **.zip**.

---

## 📋 **Cahier des charges**

### **Objectif**
Le projet **EpiSpotify** vise à offrir une plateforme de streaming musicale en ligne avec un lecteur audio complet, permettant de créer des playlists, d’ajouter des morceaux par **Drag and Drop** ou via **URL YouTube**, et de télécharger des playlists sous forme de fichiers **.zip**.

Le challenge principal est de faire fonctionner l'application sans backend complexe tout en utilisant un hébergement **Webstrator**, ce qui impose l'utilisation de **localStorage** pour gérer les données des utilisateurs, leurs playlists et morceaux.

### **Durée totale**
**3 mois**, avec des **évolutions majeures toutes les deux jour par semaine**, soit 24 jours de développement.

---

## 🛠 **Fonctionnalités**

### **Mois 1 : Fondation technique et interface de base**
- **Interface utilisateur** :
  - **Barre latérale** : Accès à Accueil, Recherche, Bibliothèque, Playlists.
  - **Zone principale** : Affichage des playlists sous forme de cartes.
  - **Lecteur audio** : Contrôles de base (Lecture, Pause, Précédent, Suivant).
- **Backend minimal** :
  - **localStorage** utilisé pour gérer les playlists et les morceaux.
- **Design** :
  - Mise en page inspirée de Spotify avec la palette de couleurs **noir**, **gris**, et **vert**.

### **Mois 2 : Fonctionnalités utilisateur**
- **Gestion des playlists** :
  - Création, modification et suppression de playlists dans le **localStorage**.
- **Ajout de morceaux** :
  - Ajout de morceaux via **Drag and Drop** ou **URL YouTube**.
- **Téléchargement de playlists** :
  - Téléchargement des playlists sous forme de fichiers **.zip** avec **JSZip** et **FileSaver.js**.

### **Mois 3 : Fonctionnalités avancées**
- **Mode hors ligne** :
  - Utilisation de **localStorage** pour le stockage local des morceaux et playlists.
- **Optimisation UX** :
  - Animations, transitions fluides, interface finalisée pour mobile et desktop.

---

## 🗓️ **Planification**

### **Semaine par semaine**
| **Semaine** | **Objectif**                                                                 |
|-------------|-------------------------------------------------------------------------------|
| Semaine 1   | Création de la structure HTML/CSS (barre latérale, zone principale, lecteur).|
| Semaine 2   | Design : Palette EpiSpotify, mise en page responsive.                        |
| Semaine 3   | Intégration des playlists statiques et gestion des playlists.                |
| Semaine 4   | Implémentation du lecteur audio (lecture, pause, suivant, précédent).         |
| Semaine 5   | Création d'un champ de recherche dynamique.                                  |
| Semaine 6   | Fonctionnalité de gestion de playlists (création, modification, suppression).|
| Semaine 7   | Suppression de chansons et de playlists.                                     |
| Semaine 8   | Intégration d'un système d'ajout de morceaux par URL YouTube et Drag and Drop.|
| Semaine 9   | Ajout de la fonctionnalité de téléchargement de playlists au format **.zip**.|
| Semaine 10  | Mise en place du mode hors ligne avec **localStorage**.                       |
| Semaine 11  | Test de la gestion des playlists et des morceaux hors ligne.                 |
| Semaine 12  | Finalisation : Animations, responsive, tests et corrections.                 |

---

## ⚙️ **Technologies utilisées**

### **Frontend**
- **HTML5, CSS3, JavaScript** : Construction de l'interface et des interactions dynamiques.
- **Responsive Design** : Utilisation de **Flexbox** et des **Media Queries** pour la compatibilité mobile et desktop.
- **JSZip** et **FileSaver.js** : Pour générer et télécharger les playlists en fichiers **.zip**.

### **Backend**
- **localStorage** : Gestion des utilisateurs, playlists et morceaux sans serveur backend.

### **Base de données**
- Pas de base de données externe. Utilisation de **localStorage** pour stocker les informations suivantes :
  - **Utilisateurs** : nom, email, playlists.
  - **Playlists** : nom, morceaux.
  - **Morceaux** : titre, URL YouTube ou fichier MP3.

---

## 📂 **Structure des fichiers**

**EpiSpotify/**
  
├── **index.html**        # Interface principale du site  
├── **styles.css**        # Styles de l’application  
├── **script.js**         # Logique principale en JavaScript  
├── **assets/**           # Contient les logos et autres assets  
│   ├── **logo.png**      # Logo du site  
│   └── **music.png**     # Image de la musique (exemple)  
├── **js/**               # Fichiers JavaScript externes  
│   ├── **JSZip.min.js**  # Bibliothèque pour créer les fichiers .zip  
│   └── **FileSaver.min.js** # Bibliothèque pour télécharger les fichiers .zip  
├── **data/**             # Contient les fichiers JSON pour la gestion des morceaux  
│   ├── **songs.json**    # Liste des morceaux à ajouter  
│   └── **playlists.json**# Liste des playlists (structure à créer)  

---

## 📝 **Résumé des problèmes rencontrés et solutions**

1. **Problème de gestion des utilisateurs avec la base de données** :
   - **Limitation** : Webstrator ne permet pas d'utiliser une base de données pour gérer les utilisateurs et récupérer des données externes via API.

2. **Ajout des morceaux via URL YouTube** :
   - **Limitation** : Webstrator n'accepte pas les appels externes pour récupérer des données de YouTube.
   - **Solution** : L'utilisateur peut ajouter un morceau via une URL YouTube, mais le titre et les informations doivent être ajoutés manuellement. Un mécanisme de validation est en place pour vérifier l'URL.

3. **Gestion des playlists** :
   - **Limitation** : Les playlists sont créées et gérées localement dans le navigateur via **localStorage**. La gestion d'une base de données côté serveur est impossible.

4. **Téléchargement des playlists** :
   - **Limitation** : Aucun backend pour générer des fichiers **.zip** à partir de morceaux stockés.
   - **Solution** : Utilisation de **JSZip** et **FileSaver.js** pour générer et télécharger les playlists au format **.zip** dans le navigateur.

---

### **Conclusion**

Le projet **EpiSpotify** s'efforce de recréer une plateforme de streaming musicale en utilisant uniquement des technologies front-end et un **stockage local** dans le navigateur. En dépit des limitations imposées par l'hébergeur **Webstrator**, j'ai réussi à développer un prototype presque fonctionnel pour, l'écoute de morceaux, et le téléchargement des playlists en fichiers **.zip**. 

Cette solution permet de contourner les contraintes de la base de données et des API externes, tout en offrant une expérience utilisateur similaire à celle des plateformes de streaming modernes.