# **🔎 Analyse des crimes à Chicago avec PySpark**

*📌 Description du projet*

Ce projet vise à analyser les incidents criminels signalés dans la ville de Chicago entre 2001 et novembre 2025, à l’aide de PySpark.
L’objectif est d’exploiter un volume important de données publiques pour analyser les tendances criminelles, les taux d’arrestation, et leur évolution dans le temps.

Les données proviennent du système CLEAR (Citizen Law Enforcement Analysis and Reporting) du département de police de Chicago.

*📊 Dataset officiel :*

👉 https://data.cityofchicago.org/Public-Safety/Crimes-2025/t7ek-mgzi/data_preview

*🧠 Objectifs de l’analyse*

Nettoyer et préparer un dataset volumineux avec PySpark

* Analyser :

- le taux global d’arrestation

- l’évolution du taux d’arrestation par année

- les arrestations selon le jour de la semaine

- les incidents par mois, année et type de crime

- la différence entre incidents domestiques et non domestiques

* Mettre en évidence des tendances temporelles et comportementales

*🛠️ Technologies utilisées*

- Python

- PySpark

- Spark SQL

- Pandas

- Matplotlib

- Seaborn

- Google Colab

📂 Structure du projet
📁 Spark/
│
├── PYSPARK.ipynb        # Notebook principal (analyse complète)
├── crimes.csv           # Dataset (à télécharger séparément)
└── README.md            # Documentation du projet

*📥 Chargement des données*

Les données ne sont pas incluses dans le dépôt (taille importante).

Télécharger le fichier depuis le site officiel :

https://data.cityofchicago.org/Public-Safety/Crimes-2025/t7ek-mgzi/data_preview

Renommer le fichier en crimes.csv

Mettre à jour le chemin dans le script si nécessaire :

df = spark.read.csv("crimes.csv", header=True, inferSchema=True)

*🔧 Prétraitement des données*

- Conversion des dates en format timestamp

- Cast des coordonnées géographiques (Latitude, Longitude)

- Harmonisation des catégories de crimes

- Création de nouvelles variables :

- Jour du mois

- Mois (en français)

- Jour de la semaine (en français)

- Indicateur week-end

*📊 Analyses réalisées*

✔️ Taux d’arrestation

- Taux global d’arrestation à Chicago

- Taux d’arrestation par année

- Évolution graphique du taux d’arrestation

✔️ Analyse temporelle

- Nombre d’incidents par année

- Incidents et arrestations par mois

- Arrestations par jour de la semaine

✔️ Analyse comportementale

- Incidents domestiques vs non domestiques

- Arrestations selon le type d’incident

*📈 Visualisations*

- Courbes d’évolution (incidents vs arrestations)

- Barplots par mois et jour

-Comparaisons avec et sans arrestation

- Visualisations claires pour l’aide à la décision

*🚀 Lancer le projet*

- Option 1 : Google Colab (recommandé)

- Ouvrir le notebook PYSPARK.ipynb

Installer les dépendances :

!pip install pyspark
!pip install findspark
