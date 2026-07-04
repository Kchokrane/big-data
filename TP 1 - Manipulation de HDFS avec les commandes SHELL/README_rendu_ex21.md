# Rendu - Exercice 21 (HDFS)

Ce dossier contient les elements de rendu de l'exercice de synthese 21.

## 1) Commandes utilisees

Script principal:
- `run_exercice.sh`

Ce script couvre les 10 taches demandees:
1. Creation de `/exercice`
2. Creation de `/exercice/raw`, `/exercice/archive`, `/exercice/export`
3. Creation de `/tmp/clients.csv`
4. Envoi vers `/exercice/raw`
5. Lecture du fichier depuis HDFS
6. Copie vers `/exercice/archive`
7. Telechargement en local
8. Affichage de la taille avec `du -h`
9. Verification des blocs avec `fsck`
10. Changement du facteur de replication a 3

## 2) Resultat `hdfs dfs -ls -R /exercice`

Fichier de preuve:
- `hdfs dfs -ls -R exercice.txt`

## 3) Resultat `hdfs fsck /exercice/raw/clients.csv -files -blocks -locations`

Fichier de preuve:
- `fsck_exercice.txt`

Note:
- Ce fichier doit contenir la sortie reelle de la commande lancee sur ton cluster.

## 4) Capture de l'interface web NameNode

A ajouter:
- `capture_namenode.png` (ou `.jpg`)

URL de reference:
- `http://localhost:9870`

## 5) Explication du role de la replication

Fichier:
- `explication_replication.md`
