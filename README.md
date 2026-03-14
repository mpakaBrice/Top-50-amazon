# 📚 Analyse des Best-sellers Amazon (2009-2019) : Stratégie Fiction vs Non-Fiction

## 📌 Présentation du Projet
Ce projet analyse un jeu de données contenant les **50 livres les plus vendus sur Amazon chaque année entre 2009 et 2019**. 

L'objectif est d'identifier les tendances de marché entre les genres **Fiction** et **Non-Fiction** afin de fournir des recommandations stratégiques pour une maison d'édition souhaitant optimiser son catalogue et sa politique de prix.

---

## 🎯 Problématique Business
> **"Dans quel genre et à quel prix une maison d'édition doit-elle investir pour maximiser ses chances d'entrer et de rester dans le Top 50 Amazon ?"**

---

## 🛠️ Stack Technique
* **Nettoyage & Préparation :** Python (Pandas), Power Query (M)
* **Analyse de Données :** SQL (BigQuery), Python (NumPy)
* **Visualisation :** Power BI, Seaborn, Matplotlib

---

## ⚙️ Méthodologie & Transformation des données (ETL)

Une attention particulière a été portée à la qualité des données (**Data Quality**) pour éviter tout biais statistique :

1.  **Gestion des doublons :** Création d'une table de dimension `Dim_Books` pour isoler les caractéristiques uniques des livres (350 titres) et d'une table de faits `Fact_Sales` pour l'analyse temporelle (550 entrées).
2.  **Imputation des prix manquants :** Les prix à 0$ ont été identifiés comme des anomalies. Ils ont été remplacés par la **médiane des prix par genre** pour maintenir la cohérence de l'analyse.
3.  **Normalisation :** Nettoyage des noms d'auteurs (ex: regroupement de "J. K. Rowling" et "J.K. Rowling") via Power Query.
4.  **Segmentation (Binning) :** Création de tranches de prix (0-10$, 10-20$, 20$+) pour une analyse granulaire du comportement d'achat.

---

## 📊 Key Insights (Résultats Clés)

* **Domination du Marché :** La **Non-Fiction** est majoritaire, représentant environ **55%** des titres du Top 50 sur la période. Sa part de marché est en croissance constante depuis 2014.
* **Performance des Prix :** La Fiction performe mieux sur les prix bas (< 10$), tandis que la Non-Fiction parvient à maintenir des volumes élevés même sur des segments Premium (> 20$).
* **Satisfaction Client :** Bien que moins nombreux, les livres de **Fiction** obtiennent en moyenne des notes utilisateurs (`User Rating`) plus élevées (4.62) que la Non-Fiction (4.60), suggérant une plus forte fidélité émotionnelle.
* **Popularité :** Le nombre de commentaires (`Reviews`) a explosé entre 2011 et 2019, signe d'une interactivité accrue sur la plateforme.

---

## 💡 Recommandations Business

1.  **Pour le Volume :** Investir dans la **Non-Fiction** (guides, biographies), car le marché est plus vaste et permet des marges plus élevées (prix moyen supérieur).
2.  **Pour la Notoriété :** Développer des sagas de **Fiction** pour générer des notes élevées et construire une image de marque forte.
3.  **Stratégie de Pricing :** * Viser la tranche **8$ - 12$** pour les nouveaux lancements de Fiction.
    * Appliquer un prix **Premium (> 15$)** pour les ouvrages de Non-Fiction apportant une valeur ajoutée éducative.

---

## 📁 Structure du Repository
* `/data` : Dataset original et dataset nettoyé.
* `/sql` : 
* `/python` :https://colab.research.google.com/drive/1EYd3Kyl_uPBqSn8IxYR79M_oaik7SieQ#scrollTo=O1H_-34zm_t- (EDA et Data Cleaning).
* `/powerbi` : Fichier `.pbix` du dashboard interactif.
* `README.md` : Présentation du projet.

---


## 👤 Contact
**Brice Mpaka** - Junior Data Analyst
* www.linkedin.com/in/bricempaka
* https://resisted-message-95d.notion.site/Mpaka-Brice-30abf06cf80080a0bd10f61492ed6620
