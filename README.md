# perso — Projet hospitalier (base Django)

Dépôt de travail personnel contenant la **pré-configuration Django** du projet de gestion hospitalière (voir aussi `PyreCore/Hosto-v1`). Il sert de socle de code : squelette du projet et de l'application métier, prêt à évoluer.

## Structure

```
gestion_hopital_patient/
├── manage.py                  # Point d'entrée Django
├── gestion_hopital_patient/   # Configuration du projet (settings, urls, wsgi, asgi)
├── patient/                   # Application "patient"
│   ├── models.py              # Modèles (à compléter)
│   ├── views.py               # Vue d'accueil (home)
│   ├── admin.py               # Enregistrement admin
│   └── templates/patient/     # Templates (home.html)
├── requirements.txt           # Dépendances Python
└── db.sqlite3                 # Base SQLite locale (ne pas versionner)
```

## Fonctionnalités actuelles

- Projet Django créé (settings, urls, wsgi/asgi)
- Application `patient` avec une vue d'accueil `home` rendue par `templates/patient/home.html`
- Modèles Django prêts à être définis (placeholder dans `models.py`)

## Démarrage

```bash
cd gestion_hopital_patient

# Créer un environnement virtuel et installer les dépendances
python3 -m venv .env
source .env/bin/activate
pip install -r requirements.txt

# Lancer le serveur de développement
python manage.py migrate
python manage.py runserver
```

Puis ouvrir `http://127.0.0.1:8000/`.

## Notes

- ⚠️ L'environnement virtuel `.env/` et la base `db.sqlite3` ne devraient pas être versionnés (penser à un `.gitignore`).
- Ce dépôt est un brouillon personnel lié au projet hospitalier ; la version aboutie est prévue dans `Hosto-v1`.