# Big Data Labs Repository

Ce depot regroupe 6 travaux pratiques autour de l'ecosysteme Big Data:

- `Tp1 - Manipulation de HDFS avec les commandes SHELL`
- `TP 2 - Stockage Objet avec MinIO`
- `TP 3 - SPARK SQL`
- `TP 4 - Analyse en temps quasi reel des mesures de capteurs avec Spark Structured Streaming et HDFS`
- `TP 5 - Traitement de flux avec Kafka Streams`
- `TP 6 - Atelier Big Data Apache Airflow pour l'orchestration des pipelines Big Data`

## Objectif

Le projet sert de support pedagogique pour pratiquer:

- stockage distribue HDFS
- stockage objet MinIO (S3 compatible)
- traitement batch Spark SQL
- traitement streaming Spark Structured Streaming
- traitement de flux Kafka Streams
- orchestration de pipelines avec Apache Airflow

## Prerequis

- Docker et Docker Compose
- Java 17 (pour les TPs Java)
- Python 3.10+ (pour les TPs Airflow/PySpark)

## Demarrage rapide

Chaque TP contient ses propres fichiers de configuration (`docker-compose`, scripts, DAGs, etc.).

1. Entrer dans le dossier du TP cible
2. Lancer les services necessaires
3. Executer les scripts/commandes du TP

Exemple:

```bash
cd "TP 3 - SPARK SQL"
docker compose up -d
```

## Hygiene du repository

Les artefacts locaux d'execution ne sont pas conserves dans le depot:

- logs runtime
- etat local Kafka Streams
- fichiers IDE
- fichiers temporaires OS/Python/Java

Voir `/.gitignore` pour le detail des exclusions.
