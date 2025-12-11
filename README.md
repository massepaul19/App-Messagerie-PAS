#----------------------------------------------------------------
#  --------------------  TRADUCTION BASSA FRANCAIS -----------------------
## --------------- MASSE MASSE PAUL - BASTHYLLE -----------------
#----------------------------------------------------------------


#-----------------------------------------------------------------------------------------------------
#  ---------------- 🎓 BASSA LEARNING - Application d'Apprentissage Intelligente -------------------
#-----------------------------------------------------------------------------------------------------

**Auteur:** PAUL-BASTHYLLE MASSE MASSE  
**Version:** 1.0.0  
**Date:** Octobre 2025

---

## 📋 Table des matières

1. [Description du projet](#description-du-projet)
2. [Fonctionnalités principales](#fonctionnalités-principales)
3. [Architecture technique](#architecture-technique)
4. [Structure de la base de données](#structure-de-la-base-de-données)
5. [Technologies utilisées](#technologies-utilisées)
6. [Installation](#installation)
7. [Utilisation](#utilisation)
8. [Architecture de l'IA conversationnelle](#architecture-de-lia-conversationnelle)
9. [Modules d'apprentissage](#modules-dapprentissage)
10. [API Endpoints](#api-endpoints)
11. [Contribution](#contribution)
12. [Roadmap](#roadmap)

---

## 📖 Description du projet

**Bassa Learning** est une application web interactive pour l'apprentissage de la langue Bassa (langue bantoue du Cameroun). Elle intègre une intelligence artificielle conversationnelle qui permet aux utilisateurs d'apprendre la langue de manière naturelle et progressive.

### 🎯 Objectifs

- Préserver et promouvoir la langue Bassa
- Faciliter l'apprentissage par une approche interactive
- Offrir un dictionnaire complet Bassa-Français
- Permettre des conversations en Bassa grâce à l'IA
- S'améliorer continuellement via l'apprentissage automatique

---

## ✨ Fonctionnalités principales

### 1. 📚 **Dictionnaire intelligent**
- Traduction Bassa ↔ Français
- Singulier et pluriel
- Exemples de phrases contextualisées
- Recherche rapide et intuitive

### 2. 🗣️ **Conjugaison des verbes**
- Conjugaison complète de tous les verbes
- Tous les temps (présent, passé, futur, imparfait)
- Toutes les personnes (je, tu, il, nous, vous, ils)
- Formes affirmatives et négatives

### 3. 📖 **Apprentissage thématique**
- **Vocabulaire par catégories:** cuisine, corps humain, famille, animaux, couleurs, vêtements, nature, maison, transport, métiers
- **Salutations et expressions courantes**
- **Jours, mois et saisons**
- **Relations familiales complètes**

### 4. 🤖 **IA Conversationnelle**
- Chat en temps réel avec l'IA
- Compréhension du contexte
- Réponses personnalisées
- Apprentissage continu des nouvelles expressions

### 5. 📊 **Suivi de progression**
- Statistiques d'apprentissage
- Points et niveaux
- Exercices personnalisés
- Historique des conversations

### 6. 🧠 **Construction dynamique de phrases**
- Analyse grammaticale automatique
- Construction de phrases même non pré-enregistrées
- Suggestions intelligentes

---

## 🏗️ Architecture technique

### Stack technologique

```
┌─────────────────────────────────────────────┐
│              FRONTEND                        │
│  HTML5 + CSS3 + JavaScript (Vanilla)       │
│  - Interface responsive                     │
│  - AJAX pour communication API              │
│  - Design moderne et intuitif               │
└─────────────────────────────────────────────┘
                    ↕️ REST API
┌─────────────────────────────────────────────┐
│              BACKEND                         │
│         Python Flask                         │
│  - Routage API                              │
│  - Logique métier                           │
│  - Traitement IA                            │
│  - Gestion sessions                         │
└─────────────────────────────────────────────┘
                    ↕️ SQL
┌─────────────────────────────────────────────┐
│           BASE DE DONNÉES                    │
│            MySQL 8.0+                        │
│  - 50+ tables organisées                    │
│  - Triggers et procédures stockées          │
│  - Optimisation avec index                  │
└─────────────────────────────────────────────┘
```

---

## 🗄️ Structure de la base de données

La base de données est organisée en **17 modules** interconnectés :

### 📦 Modules principaux

#### **MODULE 1 : PRONOMS**
- `types_pronoms` : Types (sujet, objet, possessif, etc.)
- `pronoms` : Tous les pronoms (je/moi/mon/ma/mes, etc.)

#### **MODULE 2 : VERBES ET CONJUGAISON**
- `verbes` : Liste complète des verbes
- `temps` : Temps de conjugaison
- `conjugaisons` : Formes conjuguées (verbe × pronom × temps)

#### **MODULE 3 : VOCABULAIRE THÉMATIQUE**
- `categories_vocabulaire` : 10 catégories (cuisine, corps, famille...)
- `vocabulaire` : Mots avec singulier/pluriel

#### **MODULE 4 : ÉLÉMENTS TEMPORELS**
- `jours` : Les 7 jours de la semaine
- `mois` : Les 12 mois de l'année
- `saisons` : Saisons en Bassa

#### **MODULE 5 : RELATIONS FAMILIALES**
- `famille` : Termes familiaux (père, mère, frère, sœur, oncle, tante...)

#### **MODULE 6 : SALUTATIONS ET EXPRESSIONS**
- `salutations` : Expressions courantes par contexte

#### **MODULE 7 : GRAMMAIRE**
- `prepositions` : Prépositions (temps, lieu, manière...)
- `adverbes` : Adverbes de temps, lieu, manière...
- `determinants` : Articles, démonstratifs...

#### **MODULE 8 : PHRASES**
- `phrases_validees` : Base de phrases Bassa-Français
- `phrases_liees` : Liens question-réponse
- `phrases_mots_lies` : Liaison phrases ↔ mots

#### **MODULE 9 : DICTIONNAIRE**
- `categories_dictionnaire` : Catégories d'entrées
- `dictionnaire` : Vue consolidée de tous les mots

#### **MODULE 10 : IA CONVERSATIONNELLE**
- `utilisateurs` : Profils utilisateurs
- `conversations` : Sessions de chat
- `messages` : Historique des échanges
- `intentions` : Intentions détectées (saluer, traduire, apprendre...)
- `messages_intentions` : Liaison messages ↔ intentions
- `reponses_types` : Réponses pré-définies par intention

#### **MODULE 11 : APPRENTISSAGE AUTOMATIQUE**
- `messages_non_compris` : Messages nécessitant traduction
- `messages_excuse` : Messages d'excuse de l'IA
- `contexte_conversation` : Contexte et anticipation
- `patterns_conversation` : Patterns récurrents
- `feedback_reponses` : Évaluations utilisateurs
- `stats_apprentissage` : Statistiques quotidiennes

#### **MODULE 12 : CONSTRUCTION DYNAMIQUE**
- `patrons_phrases` : Templates de phrases
- `regles_grammaire` : Règles grammaticales Bassa
- `mots_indexes` : Index pour recherche rapide
- `phrases_construites` : Phrases générées automatiquement

#### **MODULE 13 : PROGRESSION**
- `progression_utilisateur` : Suivi par module
- `exercices` : Exercices d'apprentissage
- `resultats_exercices` : Scores et tentatives

#### **MODULE 14 : ADMINISTRATION**
- `administrateurs` : Gestion admin
- `logs_admin` : Traçabilité des actions

#### **MODULE 15-17 : OPTIMISATION**
- Vues SQL pour requêtes fréquentes
- Triggers pour automatisation
- Procédures stockées pour logique complexe

---

## 💻 Technologies utilisées

### Frontend
- **HTML5** : Structure sémantique
- **CSS3** : Design moderne, animations, responsive
- **JavaScript (Vanilla)** : Interactivité, AJAX, manipulation DOM
- **Fetch API** : Communication avec le backend

### Backend
- **Python 3.9+** : Langage principal
- **Flask 3.0+** : Framework web léger
  - `Flask-CORS` : Gestion CORS
  - `Flask-MySQLdb` ou `PyMySQL` : Connexion MySQL
  - `Flask-Session` : Gestion des sessions
  - `python-dotenv` : Variables d'environnement

### Base de données
- **MySQL 8.0+** : SGBD relationnel
- **UTF-8 (utf8mb4)** : Support caractères spéciaux Bassa

### Outils de développement
- **Git** : Versioning
- **Postman** : Test API
- **MySQL Workbench** : Gestion BDD

---

## 🚀 Installation

### Prérequis

```bash
- Python 3.9+
- MySQL 8.0+
- pip (gestionnaire de paquets Python)
- Navigateur web moderne
```

### Étape 1 : Cloner le projet

```bash
git clone https://github.com/paulmasti/bassa-learning.git
cd bassa-learning
```


```

### Étape 3 : Installer les dépendances Python

```bash
pip install -r requirements.txt
```

**Contenu de `requirements.txt` :**
```
Flask==3.0.0
Flask-CORS==4.0.0
PyMySQL==1.1.0
python-dotenv==1.0.0
cryptography==41.0.0
```

### Étape 4 : Créer la base de données

```bash
# Se connecter à MySQL
mysql -u root -p

# Exécuter le script SQL
SOURCE database/bassa_learning_schema.sql
```

Ou via phpMyAdmin :
1. Créer une base de données `bassa_learning`
2. Importer le fichier `bassa_learning_schema.sql`

### Étape 5 : Configuration

Créer un fichier `.env` à la racine du projet :

```env
# Configuration Flask
FLASK_APP=app.py
FLASK_ENV=development
SECRET_KEY=votre_cle_secrete_tres_longue_et_complexe

# Configuration MySQL
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=votre_mot_de_passe
DB_NAME=bassa_learning
DB_PORT=3306

# Configuration application
DEBUG=True
PORT=5000
```

### Étape 6 : Structure du projet

```
bassa-learning/
│
├── app.py                      # Point d'entrée Flask
├── requirements.txt            # Dépendances Python
├── README.md                   # Documentation
│
├── database/
│   └── bassa_learning_schema.sql  # Schéma de la BDD
│
├── static/                     # Fichiers statiques
│   ├── css/
│   │   ├── style.css          # Styles principaux
│   │   └── responsive.css     # Styles responsive
│   ├── js/
│   │   ├── app.js             # Script principal
│   │   ├── api.js             # Gestion API
│   │   ├── chat.js            # Module chat
│   │   └── dictionary.js      # Module dictionnaire
│   └── images/
│       └── logo.png
│
├── templates/                  # Templates HTML
│   ├── index.html             # Page d'accueil
│   ├── dictionary.html        # Dictionnaire
│   ├── conjugation.html       # Conjugaison
│   ├── vocabulary.html        # Vocabulaire
│   ├── chat.html              # Chat IA
│   └── profile.html           # Profil utilisateur
│
├── routes/                     # Routes API
│   ├── __init__.py
│   ├── dictionary.py          # Routes dictionnaire
│   ├── conjugation.py         # Routes conjugaison
│   ├── vocabulary.py          # Routes vocabulaire
│   ├── chat.py                # Routes chat IA
│   └── users.py               # Routes utilisateurs
│
├── services/                   # Logique métier
│   ├── __init__.py
│   ├── database.py            # Connexion BDD
│   ├── ai_service.py          # IA conversationnelle
│   ├── parser_service.py      # Analyse de phrases
│   └── translation_service.py # Construction dynamique
│
└── utils/                      # Utilitaires
    ├── __init__.py
    ├── helpers.py             # Fonctions utiles
    └── validators.py          # Validation de données
```

### Étape 7 : Lancer l'application

```bash
python app.py
```

L'application sera accessible à : **http://localhost:5000**

---

## 📱 Utilisation

### Interface utilisateur

#### 1. **Page d'accueil**
- Présentation de l'application
- Choix du module d'apprentissage
- Accès rapide au chat

#### 2. **Dictionnaire**
- Recherche Bassa → Français ou Français → Bassa
- Affichage singulier/pluriel
- Exemples de phrases
- Écoute de la prononciation

#### 3. **Conjugaison**
- Sélection d'un verbe
- Choix du temps
- Affichage de la conjugaison complète
- Formes affirmatives et négatives

#### 4. **Vocabulaire**
- Navigation par catégories
- Cartes de vocabulaire avec images
- Quiz interactifs

#### 5. **Chat IA**
- Conversation en temps réel
- Traduction instantanée
- Suggestions de réponses
- Corrections grammaticales

---

## 🤖 Architecture de l'IA conversationnelle

### Flux de traitement d'un message

```
┌─────────────────────────────────────────────┐
│  Utilisateur envoie un message              │
│  "Bonjour, comment vas-tu ?"                │
└─────────────────┬───────────────────────────┘
                  ↓
┌─────────────────────────────────────────────┐
│  1. DÉTECTION D'INTENTION                   │
│  - Analyse des mots-clés                    │
│  - Pattern matching                         │
│  → Intention: "saluer" (score: 95%)         │
└─────────────────┬───────────────────────────┘
                  ↓
┌─────────────────────────────────────────────┐
│  2. RECHERCHE DE RÉPONSE                    │
│  a) Phrases validées exactes ?              │
│  b) Réponses types par intention ?          │
│  c) Construction dynamique ?                │
└─────────────────┬───────────────────────────┘
                  ↓
          ┌───────┴───────┐
          ↓               ↓
    [TROUVÉ]        [NON TROUVÉ]
          ↓               ↓
┌─────────────────┐  ┌──────────────────────┐
│ 3a. RÉPONSE     │  │ 3b. CONSTRUCTION     │
│     DIRECTE     │  │     DYNAMIQUE        │
│                 │  │ - Parser la phrase   │
│ "Mɔ̂ndɛm!        │  │ - Identifier éléments│
│  Ò gɛ̀ŋ ɔ́?"    │  │ - Appliquer règles   │
│                 │  │ - Générer réponse    │
└────────┬────────┘  └─────────┬────────────┘
         │                     ↓
         │           ┌─────────────────────┐
         │           │ Score confiance     │
         │           │ < 50% ?             │
         │           └──────┬──────────────┘
         │                  ↓
         │           ┌─────────────────────┐
         │           │ 3c. MESSAGE EXCUSE  │
         │           │ "Njɔ̀ŋ màp, má gɛ̀ŋ │
         │           │  kɛ́ hɔ̀ŋ..."        │
         │           │                     │
         │           │ + Sauvegarder pour  │
         │           │   traitement admin  │
         │           └─────────┬───────────┘
         └──────────────────────┘
                  ↓
┌─────────────────────────────────────────────┐
│  4. ANTICIPATION                            │
│  - Analyser le contexte                     │
│  - Prédire prochaines questions             │
│  - Pré-charger réponses probables           │
└─────────────────┬───────────────────────────┘
                  ↓
┌─────────────────────────────────────────────┐
│  5. ENVOI DE LA RÉPONSE                     │
│  "Mɔ̂ndɛm! Ò gɛ̀ŋ ɔ́?" / "Bonjour! Comment  │
│   vas-tu?"                                  │
└─────────────────────────────────────────────┘
```

### Système d'apprentissage continu

1. **Collecte** : Messages non compris sauvegardés
2. **Priorisation** : Tri par fréquence et importance
3. **Traduction manuelle** : Admin valide les traductions
4. **Intégration** : Ajout aux phrases validées
5. **Amélioration** : L'IA peut maintenant répondre

---

## 📚 Modules d'apprentissage

### 1. Conjugaison
- Interface de sélection verbe + temps
- Affichage tableau conjugaison
- Exercices de pratique
- Quiz de vérification

### 2. Vocabulaire
- 10 catégories thématiques
- Cartes interactives
- Mode apprentissage et quiz
- Progression sauvegardée

### 3. Salutations
- Contextes variés (matin, soir, formel...)
- Dialogues modèles
- Exercices de conversation

### 4. Famille
- Arbre généalogique interactif
- Relations familiales complètes
- Exercices de reconnaissance

---

## 🔌 API Endpoints

### Dictionnaire

```http
GET /api/dictionary/search?term=bonjour&lang=francais
POST /api/dictionary/add
GET /api/dictionary/word/:id
GET /api/dictionary/examples/:id
```

### Conjugaison

```http
GET /api/conjugation/verbs
GET /api/conjugation/verb/:id
GET /api/conjugation/conjugate?verb_id=1&temps_id=1
POST /api/conjugation/exercise
```

### Vocabulaire

```http
GET /api/vocabulary/categories
GET /api/vocabulary/category/:id
GET /api/vocabulary/random?category_id=1&count=10
POST /api/vocabulary/learn
```

### Chat IA

```http
POST /api/chat/message
POST /api/chat/start
GET /api/chat/history/:conversation_id
POST /api/chat/feedback
```

### Utilisateur

```http
POST /api/user/register
POST /api/user/login
GET /api/user/profile
GET /api/user/progress
POST /api/user/exercise/submit
```

---

## 🤝 Contribution

### Comment contribuer

1. **Traductions** : Aider à traduire plus de phrases
2. **Vérification** : Valider les traductions existantes
3. **Contenu** : Ajouter du vocabulaire, des expressions
4. **Code** : Améliorer les fonctionnalités
5. **Design** : Proposer des améliorations UI/UX

### Workflow Git

```bash
# 1. Fork le projet
# 2. Créer une branche
git checkout -b feature/ma-nouvelle-fonctionnalite

# 3. Commit les changements
git commit -m "Ajout de [fonctionnalité]"

# 4. Push vers votre fork
git push origin feature/ma-nouvelle-fonctionnalite

# 5. Créer une Pull Request
```

---

## 🗺️ Roadmap

### Version 1.0 (Actuelle)
- ✅ Dictionnaire de base
- ✅ Conjugaison des verbes
- ✅ Chat IA basique
- ✅ Modules d'apprentissage

### Version 1.5 (À venir)
- 🔄 Reconnaissance vocale
- 🔄 Synthèse vocale (TTS)
- 🔄 Application mobile (React Native)
- 🔄 Mode hors-ligne

### Version 2.0 (Futur)
- 📱 Application mobile native
- 🎮 Gamification complète
- 👥 Communauté d'apprenants
- 🏆 Certificats d'apprentissage
- 📊 Tableaux de classement

---

## 📄 Licence

Ce projet est sous licence **MIT**. Voir le fichier `LICENSE` pour plus de détails.

---

## 👨‍💻 Auteur

**Massé Paul**  
📧 Email: paolocisse6@gmail.com  
🌐 GitHub: [@massepaul19](https://github.com/massepaul19)

---

## 🙏 Remerciements

- Communauté Bassa pour la préservation de la langue
- Contributeurs et testeurs
- Ressources linguistiques consultées

---

## 📞 Support

Pour toute question ou problème :
- 📧 Email: paolo66@gmail.com
- 💬 Discord: [Serveur Bassa Learning]
- 🐛 Issues GitHub: [github.com/massepaul19/bassa-learning/issues]

---

**Bonne chance dans votre apprentissage du Bassa ! 🎓🇨🇲**
