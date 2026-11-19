<p align="center">
  <img src="assets/img/photo.jpg" alt="Walid Benchabekh" width="180" style="border-radius:50%;">
</p>

<h3 align="center">Data Engineer · Ingénieur INSA Rouen · Certifié Databricks Data Engineer Associate</h3>

## Profil

Data Engineer avec près de 2 ans d'expérience dans la conception et l'industrialisation de pipelines de données sur Azure Databricks (Python, PySpark, SQL, architecture Medallion). Habitué à cartographier les sources et les flux, à fiabiliser les traitements par des contrôles qualité et à restituer la donnée dans des tableaux de bord Power BI. Expérience concrète de l'IA générative (LLM, RAG, Microsoft Copilot Studio).

**Contact :** [benchabekhwalid@gmail.com](mailto:benchabekhwalid@gmail.com) · 07 57 77 52 03 · Paris / Île-de-France<br>
**LinkedIn :** [linkedin.com/in/walid-benchabekh](https://www.linkedin.com/in/walid-benchabekh/)<br>
**GitHub :** [github.com/walgt](https://github.com/walgt)

---

## Projets

### Health Data Hub — Audit qualité d'un pipeline de données de santé
🔗 [github.com/walgt/Health_data_hub_Project](https://github.com/walgt/Health_data_hub_Project)

![Health Data Hub – Audit](assets/health_data_hub_banner_audit.png)

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

### Pipeline de données orchestré — Airflow, GCP, dbt, Soda

Conception et orchestration d'un pipeline ETL avec Apache Airflow, intégration de données vers GCS/BigQuery, transformations modélisées avec dbt et mise en place de tests de qualité des données avec Soda.

**Outils :** Apache Airflow, Google Cloud Platform, GCS, BigQuery, dbt, Soda, SQL, Python

---

## Expériences professionnelles

### Data & AI Engineer (Alternance) — Afpa
*01/2026 – aujourd'hui · Montreuil, Île-de-France*

**Projet 1 — Pipeline d'ingestion API pour la prospection alternance 2027 (Île-de-France)**

- Ingestion via les API France Travail (La Bonne Boîte, Offres d'emploi) par code ROME, NAF et département.
- Consolidation multi-sources (entreprises à fort potentiel d'embauche et offres publiées sur les jobboards), agrégation et dédoublonnage par entreprise (SIRET).
- Enrichissement des contacts décideurs (RH, direction) assisté par IA, avec contrôles qualité et traçabilité ; livraison de fichiers de prospection qualifiés aux équipes commerciales.

*Stack : Python (requests, pandas), API REST France Travail (OAuth2), DuckDB, dbt (modèles et tests qualité), pytest, Git, Power Automate, SharePoint, Power BI, Microsoft Copilot*

**Projet 2 — Génération automatisée des CERFA d'alternance (Power Automate)**

- Cartographie et réconciliation de 3 sources par clé métier, mapping vers un modèle de 136 champs.
- Pipeline événementiel industrialisé : génération et diffusion automatisées des CERFA, **gain de 6 à 10 h/semaine**.
- Fiabilisation : upsert idempotent (**zéro doublon**), déclenchement conditionnel, contrôles de complétude.

### Data Engineer (Stage · 6 mois) — CGI
*03/2025 – 09/2025 · Puteaux, Île-de-France*<br>
*Client : Ministère de la Transition écologique*

- Développement et maintenance de pipelines de données en Python sur Azure Databricks (PySpark, SQL) selon une architecture Medallion (Bronze, Silver, Gold).
- Gouvernance des données via Unity Catalog : lineage et gestion des accès.
- Construction de modèles sémantiques et définition de KPIs avec les équipes métier.
- Production de tableaux de bord Power BI et orchestration des flux avec Azure Data Factory.

### Data Scientist – IA générative (Stage · 3 mois) — Seleniums
*04/2024 – 06/2024 · Puteaux, Île-de-France*

- Conception d'un ATS en Python basé sur des LLM classant les CV selon leur adéquation à une offre.

### Data Engineer (Stage · 3 mois) — LITIS
*04/2023 – 06/2023 · Rouen, Normandie*

- Conception d'un ETL en Python : extraction via API REST, structuration des données et analyse bibliométrique.

---

## Compétences

- **Langages** : Python (pandas, PySpark, pytest), SQL (avancé)
- **Plateformes data** : Databricks (Delta Lake, Workflows, Unity Catalog)
- **Data engineering** : pipelines batch et streaming, Apache Spark, ETL/ELT, dbt, Airflow
- **Industrialisation** : Git, CI/CD (GitHub Actions / Azure DevOps), Docker, FastAPI, Linux, tests unitaires et d'intégration
- **Cloud** : Azure (Data Factory, ADLS Gen2), GCP (GCS, BigQuery), AWS (S3, Glue) – notions
- **Visualisation** : Power BI, Tableau
- **Méthodes** : Agile / Scrum, Jira
- **IA générative** : Microsoft Foundry, Microsoft Copilot, API LLM, RAG

---

## Formation

**Master Science des Données** — INSA Rouen<br>
*2023 – 2025 · Rouen, Normandie*

**Licence Science des Données** — Université de Rouen Normandie<br>
*2020 – 2023 · Rouen, Normandie*

---

## Certifications & distinctions

- **Databricks Certified Data Engineer Associate** (02/2026) — Delta Lake, Unity Catalog, PySpark, SQL, Python
- **ACM ICPC** — 6ᵉ place en programmation par équipe

---

## Langues

Français — Bilingue · Anglais — Bilingue
