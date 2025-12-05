# 📄 Lettrify – Backend (Django REST API)

Plateforme de génération automatisée de lettres administratives togolaises + CV Builder

---

## 🧭 Table des matières

- [Introduction](#introduction)
- [Fonctionnalités](#fonctionnalités-principales)
- [Technologies](#technologies-utilisées)
- [Installation](#installation--setup)
- [Structure du Projet](#structure-du-projet)
- [Contribution](#contribution)

---

## ✨ Introduction

**Lettrify** est une plateforme web moderne permettant de créer automatiquement des lettres administratives togolaises grâce à un système de wizard multi-étapes, avec export PDF/DOCX, aperçu de la lettre en temps réel durant les étapes, et aide IA.

Le backend fournit une API sécurisée destinée au frontend React.js + Tailwind.

---

## 🎯 Fonctionnalités principales

### 🔐 Authentification (JWT)

- Inscription / Connexion / Déconnexion
- Mise à jour du profil
- Photo, profession, email…

### ✉️ Lettres administratives

- Wizard multi-étapes
- Sauvegarde automatique des brouillons
- Formules d'introduction & politesse
- Gestion du destinataire (option À)
- Signature + Nom de la signature
- Historique complet

### 📄 Export

- Export PDF (ReportLab)
- Export DOCX (python-docx)
- Format officiel (logo pleine largeur, marges réduites…)

### 📊 Dashboard

- **Utilisateur** : statistiques, historique, activités

### 📑 CV Builder intégré

- Upload de CV
- Génération de CV simple
- Stockage par utilisateur

### 🤖 Aide rédactionnelle IA

- Suggestions
- Correction
- Amélioration via Google AI Studio (appelé par le frontend)

---

## 🧰 Technologies utilisées

- **Django** – Framework backend
- **Django REST Framework** – API REST
- **PostgreSQL** – Base de données
- **SimpleJWT** – Authentification JWT
- **ReportLab** – Génération PDF
- **python-docx** – Génération DOCX
- **Django Storage** – Gestion des fichiers
- **Google AI Studio** – Assistance IA

---

## 📦 Installation & Setup

### 🔽 1. Cloner le dépôt

```bash
git clone https://github.com/votre-nom/lettrify-backend.git
cd lettrify-app-backend
```

### 🐍 2. Créer un environnement virtuel

#### Linux / macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

#### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### 📦 3. Installer les dépendances

```bash
pip install -r requirements.txt
```

### ⚙️ 4. Créer le fichier `.env`

```env
DEBUG=True
SECRET_KEY=change_me

DATABASE_NAME=lettrify_db
DATABASE_USER=postgres
DATABASE_PASSWORD=your_password
DATABASE_HOST=localhost
DATABASE_PORT=5432

GOOGLE_AI_API_KEY=your_google_api_key
```

### 🗄️ 5. Créer la base PostgreSQL

```sql
CREATE DATABASE lettrify_db;
```

### 🏗️ 6. Appliquer les migrations

```bash
python manage.py migrate
```

### 👤 7. Créer un superutilisateur

```bash
python manage.py createsuperuser
```

### ▶️ 8. Lancer le serveur

```bash
python manage.py runserver
```

**Backend disponible :**  
👉 http://127.0.0.1:8000/

---

## 📁 Structure du projet

```
lettrify/
│
├── users/              # Auth + profil
├── letters/            # Wizard + formules + historique
├── cv/                 # CV builder
├── ai/                 # Google AI proxy
├── exports/            # PDF & DOCX
├── dashboard/          # Stats utilisateur + admin
├── core/               # Settings Django
├── media/              # Fichiers uploadés
├── manage.py
└── requirements.txt
```

---

## 🤝 Contribution

1. **Fork** le projet
2. Créer une **branche** pour votre fonctionnalité
3. **Commit** & **Push** vos changements
4. Ouvrir une **Pull Request** ✔

---

**Développé avec ❤️ pour simplifier l'administration au Togo**