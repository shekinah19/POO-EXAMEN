# 🍷 Wine Quality Predictor Web Application

Application web Flask pour analyser et prédire la qualité du vin rouge basée sur ses propriétés chimiques.

## 📊 Dataset

- **Source** : `winequality-red.csv`
- **Taille** : 1,599 entrées (1,359 après suppression des doublons)
- **Colonnes** : 11 caractéristiques chimiques + 1 variable cible (qualité)

### Caractéristiques

- Acidité fixe, volatile et citrique
- Sucre résiduel et chlorures
- Dioxyde de soufre libre et total
- Densité, pH, sulfates
- Alcool (%)
- Qualité (3-8)

## 🚀 Installation

### Prérequis
- Python 3.8+
- pip

### Étapes

1. **Cloner le repository**
```bash
git clone https://github.com/shekinah19/POO-EXAMEN.git
cd POO-EXAMEN
```

2. **Créer un environnement virtuel**
```bash
python -m venv venv

# Sur Windows:
venv\Scripts\activate

# Sur Linux/Mac:
source venv/bin/activate
```

3. **Installer les dépendances**
```bash
pip install -r requirements.txt
```

4. **S'assurer que le CSV est disponible**
Placez `winequality-red.csv` dans le répertoire racine du projet.

5. **Lancer l'application**
```bash
python app_complete.py
```

6. **Accéder à l'application**
Ouvrez votre navigateur et allez à : `http://localhost:5000`

## 🎯 Fonctionnalités

### 1. 📈 Page d'Accueil
- Statistiques globales sur le dataset
- Nombre de vins analysés
- Qualité moyenne
- Taux d'alcool moyen
- Plage de qualité

### 2. 🔍 Analyse des Données
- Matrice de corrélation interactive
- Top 5 facteurs influençant la qualité
- Visualisations statistiques
- Corrélations pour chaque variable

### 3. 🎯 Prédiction
- Formulaire interactif avec validation
- Saisie de 11 paramètres chimiques
- Prédiction en temps réel
- Résultats affichés avec clarté

### 4. 📡 API REST
- Endpoint `/api/stats` pour obtenir les statistiques en JSON
- Distribution de la qualité
- Statistiques d'alcool
- Précision du modèle

## 🏗️ Architecture

```
wine-quality-web/
├── app_complete.py           # Application Flask principale
├── requirements.txt          # Dépendances Python
├── winequality-red.csv       # Dataset
├── templates/
│   ├── base.html            # Template de base
│   ├── index.html           # Page d'accueil
│   ├── predict.html         # Formulaire de prédiction
│   └── analysis.html        # Visualisations
└── static/
    └── style.css            # Styles CSS
```

## 🤖 Modèle Machine Learning

- **Algorithme** : RandomForestRegressor
- **Nombre d'arbres** : 100
- **Normalisation** : StandardScaler
- **Validation** : Train/Test split (80/20)

## 📊 Insights des Données

### Corrélation avec la Qualité
1. **Alcool** : 0.480 (positive forte)
2. **Sulfates** : 0.249 (positive faible)
3. **Acide citrique** : 0.228 (positive faible)
4. **Acidité volatile** : -0.395 (négative)
5. **Densité** : -0.184 (négative faible)

## 🎨 Design

- Interface responsive (mobile-friendly)
- Thème brun/or inspiré du vin
- Bootstrap 5 pour la mise en page
- CSS personnalisé pour l'esthétique

## 📝 Endpoints

| Route | Méthode | Description |
|-------|---------|-------------|
| `/` | GET | Page d'accueil |
| `/analysis` | GET | Page d'analyse |
| `/predict` | GET/POST | Page et traitement prédiction |
| `/api/stats` | GET | API des statistiques |

## 🔧 Technologies

- **Backend** : Flask 2.3.2
- **Data Science** : pandas, numpy, scikit-learn
- **Visualisation** : matplotlib, seaborn
- **Frontend** : HTML5, CSS3, Bootstrap 5
- **Normalisation** : StandardScaler

## 👨‍💻 Utilisation

### Faire une prédiction

1. Allez sur la page `/predict`
2. Remplissez tous les champs avec les propriétés du vin
3. Cliquez sur "Prédire la Qualité"
4. La prédiction s'affichera dans une alerte de succès

### Analyser les données

1. Cliquez sur "Analyse" dans le menu
2. Consultez la matrice de corrélation
3. Explorez les facteurs influents

## ⚠️ Notes

- Les prédictions sont arrondies entre 3 et 8
- Les valeurs doivent être dans les plages recommandées
- Le modèle nécessite la normalisation des données
- Les doublons dans le dataset ont été supprimés

## 📄 Licence

MIT License

## 👤 Auteur

Shekinah - POO EXAMEN B3 INFO

## 📞 Support

Pour les issues ou questions, veuillez consulter le repository GitHub.