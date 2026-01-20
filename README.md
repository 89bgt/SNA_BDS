# Projet d'Analyse de Réseaux Sociaux - Reddit BDS et Boycott Israel

## Description

Ce projet analyse les données des subreddits `r/BDS` et `r/BoycottIsrael` pour comprendre les dynamiques sociales, les thèmes de discussion et les réseaux sémantiques dans ces communautés en ligne.

## Structure du Projet

```
projet/
├── Phase 1 - Nettoyage et Fusion des données.ipynb    # Nettoyage et préparation des données
├── Phase 2 - Analyse Exploratoire des Données.ipynb   # Analyse statistique et visualisations
├── Phase 3 - Analyse de Réseau Sémantique des Subreddits.ipynb  # Analyse de réseau et NLP avancé
├── data/
│   ├── bds_posts_hot.csv                              # Posts hot du subreddit BDS
│   ├── bds_posts_top.csv                              # Posts top du subreddit BDS  
│   ├── boycott_israel_posts_hot.csv                   # Posts hot du subreddit BoycottIsrael
│   ├── boycott_israel_posts_top.csv                   # Posts top du subreddit BoycottIsrael
│   ├── cleaned/                                       # Données nettoyées et traitées
│   └── column_descriptions.txt                        # Description des colonnes
├── results/                                            # Résultats des analyses
├── gephi_viz.gephi                                    # Visualisation réseau pour Gephi
└── README.md                                          # Ce fichier
```

## Phases d'Analyse

### Phase 1: Nettoyage et Fusion des Données
- Chargement et fusion des données CSV des deux subreddits
- Nettoyage des textes et suppression des doublons
- Gestion des valeurs manquantes
- Export des données nettoyées au format pickle

### Phase 2: Analyse Exploratoire des Données
- Statistiques descriptives des posts
- Analyse temporelle des publications
- Distribution des scores et de l'engagement
- Visualisations des tendances et patterns

### Phase 3: Analyse de Réseau Sémantique
- Traitement NLP avancé (tokenisation, lemmatisation)
- Analyse thématique avec LDA et NMF
- Construction de réseaux sémantiques
- Clustering et détection de communautés
- Visualisation avec NetworkX et export vers Gephi

## Données

Les données brutes proviennent de l'API Reddit et contiennent les informations suivantes :

- **id**: Identifiant unique du post
- **subreddit**: r/BDS ou r/BoycottIsrael
- **title**: Titre du post
- **selftext**: Contenu textuel du post
- **created_utc**: Timestamp de création
- **author**: Auteur du post
- **score**: Score Reddit (upvotes - downvotes)
- **num_comments**: Nombre de commentaires
- **upvote_ratio**: Ratio de votes positifs
- **subreddit_subscribers**: Nombre d'abonnés du subreddit
- **total_awards_received**: Nombre d'awards reçus
- **link_flair_text**: Catégorie/thème du post

## Prérequis

```python
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
networkx>=2.6.0
scikit-learn>=1.0.0
nltk>=3.6.0
python-louvain>=0.16
```

## Installation

```bash
pip install pandas numpy matplotlib seaborn networkx scikit-learn nltk python-louvain
```

Pour les ressources NLTK :
```python
import nltk
nltk.download('punkt')
nltk.download('stopwords') 
nltk.download('wordnet')
nltk.download('omw-eng')
```

## Utilisation

1. **Exécuter Phase 1** pour nettoyer et préparer les données
2. **Exécuter Phase 2** pour l'analyse exploratoire
3. **Exécuter Phase 3** pour l'analyse de réseau sémantique

Les notebooks doivent être exécutés dans l'ordre numérique car chaque phase dépend des résultats de la précédente.

## Résultats

Les analyses produisent :
- Visualisations statistiques et temporelles
- Modèles thématiques (topics modeling)
- Graphes de réseaux sémantiques
- Fichiers exportés pour Gephi (`.gephi`)
- Rapports et métriques dans le dossier `results/`

## Auteurs

Projet réalisé dans le cadre du cours de traitement des réseaux sociaux (S5 P2).

## Licence

Ce projet est à usage académique.
