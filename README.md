# Projet d’analyse Olist

## Objectif
Analyser les ventes, les catégories de produits, les délais de livraison, les avis clients et les moyens de paiement d’Olist. Les cinq questions métier et l’analyse se trouvent dans `notebooks/01_analyse_olist.ipynb`.

## Jeu de données
Brazilian E-Commerce Public Dataset by Olist (Kaggle) : https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce
Licence affichée par Kaggle : CC BY-NC-SA 4.0. Données commerciales anonymisées couvrant 2016–2018.

Placez les CSV extraits dans un dossier `data/` à la racine du projet, ou définissez `DATA_DIR` vers leur emplacement. Le notebook utilise les fichiers commandes, articles, clients, produits, avis, paiements et traduction des catégories. Les CSV ne sont pas copiés dans ce dépôt afin de garder le projet léger; téléchargez-les depuis la source et respectez sa licence.

## Installation et exécution
```bash
python -m venv .venv
source .venv/bin/activate  # Windows : .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```
Ouvrir `notebooks/01_analyse_olist.ipynb`, puis choisir **Restart Kernel and Run All Cells**. Si les données sont ailleurs : `export DATA_DIR="/chemin/vers/archive"` avant de démarrer Jupyter.

## Structure
```text
projet-analyse-olist/
├── notebooks/01_analyse_olist.ipynb
├── requirements.txt
└── README.md
```

## Méthode et limites
Le notebook quantifie les valeurs manquantes, vérifie les doublons et la cardinalité des jointures, convertit les dates, agrège les tables au bon niveau avant de calculer les indicateurs, produit plus de cinq visualisations et formule les limites. Le chiffre d’affaires est ici la somme du prix des articles des commandes livrées; les frais de port et remboursements ne sont pas inclus. Les résultats décrivent 2016–2018 et ne permettent pas d’établir des liens de causalité.

## Historique Git
Initialiser un dépôt dédié, versionner le notebook et le README dès le début, puis faire des commits réguliers au fil des séances. Ne pas ajouter les données brutes volumineuses au dépôt; garder le lien source et les instructions d’accès.
