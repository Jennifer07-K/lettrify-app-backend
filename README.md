📄 Lettrify – Backend (Django REST API)

Plateforme de génération automatisée de lettres administratives togolaises + CV Builder












🧭 Table des matières

Introduction

Fonctionnalités

Technologies

Installation

Cloner

Environnement virtuel

Dépendances

Variables d’environnement

Base PostgreSQL

Migrations

Superuser

Lancement

Structure du Projet

Contribution


✨ Introduction

Lettrify est une plateforme web moderne permettant de créer automatiquement des lettres administratives togolaises grâce à un système de wizard multi-étapes, avec export PDF/DOCX,aperçu de la lettre en tant réel durant les étapes, aide IA .

Le backend fournit une API sécurisée destinée au frontend React.js + Tailwind.

 Fonctionnalités principales
🔐 Authentification (JWT)

Inscription / Connexion / Déconnexion

Mise à jour du profil

Photo, profession, email…

✉️ Lettres administratives

Wizard multi-étapes

Sauvegarde automatique des brouillons

Formules d’introduction & politesse

Gestion du destinataire (option À)

Signature + Nom de la signature

Historique 

📄 Export

Export PDF (ReportLab)

Export DOCX (python-docx)

Format officiel (logo pleine largeur, marges réduites…)

📊 Dashboard

Utilisateur :

statistiques, historique, activités



📑 CV Builder intégré

Upload de CV

Génération de CV simple

Stockage par utilisateur

🤖 Aide rédactionnelle IA

Suggestions

Correction

Amélioration
via Google AI Studio (appelé par le frontend)

🧰 Technologies utilisées

Django

Django REST Framework

PostgreSQL

SimpleJWT

ReportLab

python-docx

Django Storage

Google AI Studio


📦 Installation & Setup
🔽 1. Cloner le dépôt
git clone https://github.com/votre-nom/lettrify-backend.git
cd lettrify-app-backend

🐍 2. Créer un environnement virtuel
Linux / macOS
python3 -m venv venv
source venv/bin/activate

Windows
python -m venv venv
venv\Scripts\activate

📦 3. Installer les dépendances
pip install -r requirements.txt

⚙️ 4. Créer le fichier .env
DEBUG=True
SECRET_KEY=change_me

DATABASE_NAME=lettrify_db
DATABASE_USER=postgres
DATABASE_PASSWORD=your_password
DATABASE_HOST=localhost
DATABASE_PORT=5432

GOOGLE_AI_API_KEY=your_google_api_key

🗄️ 5. Créer la base PostgreSQL
CREATE DATABASE lettrify_db;

🏗️ 6. Appliquer les migrations
python manage.py migrate

👤 7. Créer un superutilisateur
python manage.py createsuperuser

▶️ 8. Lancer le serveur
python manage.py runserver


Backend disponible :
👉 http://127.0.0.1:8000/

📁 Structure du projet
lettrify/
│── users/              # Auth + profil
│── letters/            # Wizard + formules + historique
│── cv/                 # CV builder
│── ai/                 # Google AI proxy
│── exports/            # PDF & DOCX
│── dashboard/          # Stats utilisateur + admin
│── config/             # Settings Django
│── media/              # Fichiers uploadés
│── manage.py
│── requirements.txt

🤝 Contribution

Fork

Créer une branche

Commit & Push

Pull Request ✔

