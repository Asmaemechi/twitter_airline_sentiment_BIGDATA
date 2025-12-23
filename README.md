# twitter_airline_sentiment_BIGDATA

 Analyse Big Data de l’opinion publique à partir des réseaux sociaux avec Apache Spark
## 👩‍💻 Auteur
**Asma Mechi**  
Étudiante en ingénierie – Systèmes embarqués et IoT
---

##  Contexte
Avec l’essor des réseaux sociaux, des millions de messages sont publiés chaque jour et influencent fortement l’opinion publique.  
L’analyse de ces données massives nécessite des outils capables de gérer le **volume**, la **vélocité** et la **variété** des données.

Ce projet exploite l’écosystème **Big Data (Hadoop & Spark)** pour analyser des tweets et étudier l’impact des réseaux sociaux sur l’opinion publique.

---

##  Objectifs du projet
- Mettre en œuvre une architecture Big Data complète
- Stocker des données massives sur **HDFS**
- Effectuer un **traitement batch** avec Apache Spark
- Réaliser des analyses distribuées via **Spark SQL**
- Comparer les performances entre **Batch Processing** et **Streaming Processing**
- Extraire des insights pertinents à partir de données textuelles

---

##  Technologies & Outils
- **Apache Hadoop (HDFS)** : stockage distribué
- **Apache Spark**
  - Spark Core
  - Spark SQL
  - Spark MLlib
  - Spark Streaming
- **Python (PySpark)**
- **Jupyter Notebook**
- **Dataset Twitter (CSV)**

---

##  Structure du projet
SocialPulse-BigData/
│
├── Tweets.csv
│ 
├── final_final_Spark.ipynb
│
├── README.md


---

## 🔄 Architecture du pipeline Big Data

### 1️⃣ Stockage des données sur HDFS
- Importation des tweets bruts dans HDFS
- Stockage distribué pour assurer la tolérance aux pannes et la scalabilité

### 2️⃣ Traitement Batch avec Spark
Les données sont nettoyées et transformées par étapes :
- Suppression des caractères spéciaux
- Mise en minuscules
- Tokenization du texte
- Suppression des stop words
- Vectorisation avec **CountVectorizer**

Ce traitement permet de préparer les données pour l’analyse et le machine learning.

### 3️⃣ Analyse avec Spark SQL
- Création de vues temporaires
- Requêtes SQL distribuées :
  - Nombre total de tweets
  - Fréquence des mots
  - Statistiques globales
- Extraction d’insights sur l’opinion publique

### 4️⃣ Traitement Streaming (comparaison)
- Simulation d’un flux de données
- Mesure du temps d’exécution
- Comparaison avec le traitement batch

---

##  Analyse des performances
| Mode de traitement | Temps d’exécution |
|-------------------|------------------|
| Batch Processing | Plus rapide |
| Streaming Processing | Plus lent (overhead) |

 **Conclusion performance** :  
Le streaming est plus lourd en raison de la gestion continue des flux, des micro-batchs et de la synchronisation, tandis que le batch est plus efficace pour des données statiques.

---

##  Résultats & Observations
- Le traitement batch est mieux adapté aux analyses hors ligne
- Le streaming est utile pour les données en temps réel mais consomme plus de ressources
- Les réseaux sociaux influencent fortement l’opinion publique, notamment lors d’événements majeurs (élections, crises, mouvements sociaux)

---

##  Exécution du projet

### Prérequis
- Hadoop installé et configuré
- Apache Spark
- Python 3
- Jupyter Notebook

### Étapes
1. Lancer HDFS et Spark
2. Importer le dataset dans HDFS
3. Ouvrir le notebook :
   
"jupyter notebook final_final_Spark.ipynb"

4.Exécuter les cellules dans l’ordre
