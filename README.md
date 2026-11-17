<p align="center">
  <img src="assets/img/photo.jpg" alt="Walid Benchabekh" width="180" style="border-radius:50%;">
</p>

<h3 align="center">Consultant Data & AI Engineer · Ingénieur INSA · Certifié Databricks</h3>

## À propos

Consultant Data & AI Engineer, ingénieur INSA et certifié Databricks. Je conçois et industrialise des pipelines de données fiables (Python, PySpark, SQL) sur le cloud (Azure, AWS, GCP), de l'ingestion jusqu'à la restitution dans Power BI. J'ai de l'expérience en architecture Medallion, en gouvernance des données (Unity Catalog) et en automatisation de processus avec l'IA générative (Power Automate, n8n, LLMs).

**Contact :** [benchabekhwalid@gmail.com](mailto:benchabekhwalid@gmail.com) · 07 57 77 52 03 · Paris, France<br>
**LinkedIn :** [linkedin.com/in/walid-benchabekh](https://www.linkedin.com/in/walid-benchabekh/)<br>
**GitHub :** [github.com/walgt](https://github.com/walgt)

---

## Expériences professionnelles

### Data & AI Engineer — Afpa
*01/2026 – aujourd'hui · Montreuil, Île-de-France*

- **Pipeline de données événementiel sous Power Automate** : ingestion asynchrone de 3 sources, réconciliation par clé métier, transformation et mapping vers un modèle cible de 136 champs, puis génération et diffusion automatisées de documents réglementaires (**gain de 6 à 10 h/semaine**).
- **Fiabilisation du flux de bout en bout** : upsert idempotent (**zéro doublon**), orchestration conditionnelle déclenchée uniquement une fois les 3 sources reçues, contrôles de complétude et de cohérence avant génération, et tableaux de bord Power BI pour le suivi.
- **Enrichissement d'une base de 556 structures** par web scraping et rapprochement multi-sources, avec contrôle qualité et traçabilité des données (**taux de complétude porté de 75 % à 92 %**).

### Data Engineer — CGI
*03/2025 – 09/2025 · Puteaux, Île-de-France*
*Client : Ministère de la Transition écologique, de la Biodiversité et des Négociations internationales sur le climat et la nature*

- Développement et maintenance de pipelines de données en Python sur Azure Databricks (PySpark, SQL) selon une architecture Medallion (Bronze, Silver, Gold).
- Gouvernance des données via Unity Catalog : lineage et gestion des accès.
- Construction de modèles sémantiques et définition de KPIs avec les équipes métier.
- Production de tableaux de bord sur Power BI et orchestration des flux avec Azure Data Factory.

### Data Scientist (LLMs) — Seleniums
*04/2024 – 06/2024 · Puteaux, Île-de-France*

- Conception d'un ATS en Python basé sur des LLM pour analyser et classer les CV selon leur niveau de correspondance avec une offre d'emploi.

### Data Engineer — LITIS
*04/2023 – 06/2023 · Rouen, Normandie*

- Conception d'un ETL en Python pour l'extraction de données via API REST, leur structuration et leur analyse bibliométrique.

---

## Formation

**Master Science des Données** — INSA Rouen
*09/2020 – 09/2025 · Rouen, Normandie*

---

## Compétences

- **Data Engineering** : Databricks, PySpark, Spark SQL, dbt, Airflow, Kafka
- **Bases de données & Modélisation** : SQL avancé, PL/SQL, SQL Server, PostgreSQL, MySQL, Oracle, MongoDB
- **Cloud & Plateformes** : AWS (S3, Glue, Redshift), Azure (Data Factory, Data Lake, Synapse), GCP (GCS, BigQuery)
- **BI & Reporting** : Power BI, DAX, Power Query, Tableau, Excel
- **Programmation & Outils** : Python, Git, CI/CD GitLab, FastAPI, Docker, Kubernetes, Linux, Jira
- **Machine Learning, NLP & Vision** : LLMs, GenAI (LangChain, RAG, Hugging Face), PyTorch, TensorFlow, YOLO
- **IA générative & Automatisation** : Claude, n8n, Microsoft Copilot Studio, Power Automate

---

## Projets

### Pipeline ETL — Apache Airflow, GCP, dbt

Conception et orchestration d'un pipeline ETL avec Apache Airflow, intégration de données vers GCS/BigQuery, transformations modélisées avec dbt et mise en place de tests de qualité des données avec Soda.

**Outils :** Apache Airflow, ETL, Data Pipeline, Google Cloud Platform, GCS, BigQuery, dbt, SQL, Python

### Health Data Hub — Audit qualité d'un pipeline de données de santé
🔗 [github.com/walgt/Health_data_hub_Project](https://github.com/walgt/Health_data_hub_Project)

Audit de qualité de 6 800 fichiers JSON d'une cohorte patients entre une zone SOURCE et une zone DELIVERY. Une démarche hypothético-déductive (profiling, comparaison des FILE_ID, analyse des attributions) a permis d'identifier la cause racine : le script de transformation déduisait le Patient_ID d'un dossier à partir du premier fichier rencontré, ce qui envoyait **1 228 fichiers vers un seul patient** et faisait **disparaître 20 patients** de la delivery.

- Reconstruction possible à 100 % via la correspondance FILE_ID ↔ source, sans aucune perte de fichier.
- Correction du script (contrôle de cohérence du Patient_ID sur tous les fichiers du dossier) et règle de validation à l'ingestion (Patient_ID == dossier parent).

**Outils :** Python, pandas, Jupyter, JSON, Data Quality

### MitoSAM — Segmentation de mitochondries par fine-tuning de SAM
🔗 [github.com/walgt/MitoSAM](https://github.com/walgt/MitoSAM)

<p align="center">
  <img src="https://raw.githubusercontent.com/walgt/MitoSAM/main/Example.png" alt="Prédiction MitoSAM : image, masque prédit et carte de probabilité" width="600">
</p>

Fine-tuning du Segment Anything Model de Meta (sam-vit-base) pour segmenter les mitochondries dans des images de microscopie électronique. Pipeline complet : découpage de 165 images en patchs 256×256 (1 642 paires image/masque après filtrage), prompts par bounding box perturbée, entraînement du seul mask decoder (DiceCELoss, Adam), puis inférence avec carte de probabilité et masque binaire.

**Outils :** Python, PyTorch, Hugging Face Transformers, Segment Anything (SAM), MONAI, Google Colab

### Analyse des Open Data de la SNCF
🔗 [github.com/walgt/Analyse-de-la-SNCF-Open-Data](https://github.com/walgt/Analyse-de-la-SNCF-Open-Data)

<p align="center">
  <img src="https://raw.githubusercontent.com/walgt/Analyse-de-la-SNCF-Open-Data/main/Dashboard.png" alt="Dashboard Tableau SNCF" width="600">
</p>

Analyse et visualisation des données ouvertes de la SNCF : régularité mensuelle des TER, fréquentation des lignes Transilien par tranche horaire et profil démographique des voyageurs par gare. Dashboards Tableau interactifs avec carte de la ponctualité par région et département et analyse des causes de retard. Projet réalisé à l'Université de Rouen Normandie avec Mounir Ahmed Djibaba.

**Outils :** Python, NumPy, pandas, Tableau

---

## Certifications

- **Databricks Certified Data Engineer Associate** (02/2026) — Delta Lake, Unity Catalog, PySpark, SQL, Python
- **ACM ICPC** — 6ᵉ place — Compétition universitaire internationale de programmation en équipe

---

## Langues

Français — Bilingue · Anglais — Bilingue