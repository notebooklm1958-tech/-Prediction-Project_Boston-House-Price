# -Prediction-Project_Boston-House-Price
Voici un résumé du contenu de ce fichier (qui est un notebook Jupyter structuré pour un
projet d'apprentissage automatique) :
1. Objectif du projet
● Le projet vise à développer un modèle de bout en bout en utilisant la régression
linéaire pour prédire le prix des maisons à Boston (Boston House Price Prediction
Project).
● Il couvre plusieurs étapes clés : la visualisation approfondie, l'ingénierie des
caractéristiques (feature engineering) et la sélection de variables basée sur leur
corrélation.
2. Importation et préparation des données
● Les bibliothèques standards de la science de données en Python sont chargées
(numpy, pandas, plotly, seaborn, matplotlib).
● Les données sont lues à partir d'un fichier nommé BostonHousing.csv.
● Une variable cible nommée SalePrice est créée en dupliquant la colonne medv (qui
représente la valeur médiane des logements).
● Des vérifications de base sont effectuées pour observer la structure globale
(dimensions avec shape, types de données et valeurs manquantes avec info et
isnull, statistiques descriptives avec describe).
3. Analyse Exploratoire des Données (EDA)
● Visualisations : Le code génère des graphiques de paires (pairplot) pour étudier les
relations entre toutes les variables, ainsi que des diagrammes de dispersion (scatter
plots) ciblés pour analyser l'impact du taux de criminalité (crim) et de l'âge des
logements (age) sur le prix.
● Étude de la distribution : L'asymétrie (skewness) et l'aplatissement (kurtosis) de la
variable cible SalePrice sont analysés. Une courbe normale et un graphique Q-Q
plot sont utilisés pour évaluer sa normalité.
● Transformation : Une transformation logarithmique (np.log1p) est appliquée sur
SalePrice afin de rendre sa distribution plus normale et améliorer l'efficacité du
modèle linéaire.
4. Corrélation et sélection des caractéristiques
● Une carte de chaleur (heatmap) de la matrice de corrélation est tracée.
● Un filtre est appliqué pour sélectionner uniquement les variables explicatives qui ont
une valeur absolue de corrélation supérieure à 0.2 avec le prix de vente (SalePrice).
5. Construction et évaluation du modèle
● Le jeu de données est séparé en fonctionnalités ($X$) et cible ($y$), puis divisé en
données d'entraînement (80 %) et de test (20 %) avec train_test_split.
● Un modèle de Régression Linéaire de scikit-learn est entraîné sur le jeu
d'entraînement.
● Le modèle réalise ensuite des prédictions sur les données de test. Le fichier inclut
une comparaison textuelle entre une valeur réelle et sa prédiction, puis calcule la
performance finale du modèle à l'aide de la racine de l'erreur quadratique moyenne
(RMSE).
