# Rendu final - Exercice de synthese 21 (HDFS)

**Module :** Big Data - Atelier Hadoop HDFS  
**Sujet :** Verification de la maitrise des commandes essentielles HDFS

---

## 1) Travail demande (21.2) - Etat d'avancement

Les 10 taches demandees ont ete scriptes dans `run_exercice.sh`:

1. Creer le dossier `/exercice`
2. Creer les sous-dossiers `/exercice/raw`, `/exercice/archive`, `/exercice/export`
3. Creer localement `clients.csv`
4. Envoyer `clients.csv` vers `/exercice/raw`
5. Lire le fichier depuis HDFS
6. Copier le fichier vers `/exercice/archive`
7. Telecharger le fichier depuis HDFS vers le systeme local
8. Afficher la taille du fichier avec `du -h`
9. Verifier les blocs avec `fsck`
10. Modifier le facteur de replication a 3

---

## 2) Commandes utilisees

Execution depuis le conteneur NameNode:

```bash
docker compose exec namenode bash
bash run_exercice.sh
```

Verification de l'arborescence:

```bash
hdfs dfs -ls -R /exercice
```

Verification des blocs:

```bash
hdfs fsck /exercice/raw/clients.csv -files -blocks -locations
```

---

## 3) Livrables (21.4)

### a) Commandes utilisees

- Script: `run_exercice.sh`

### b) Capture de l'interface web NameNode

- Fichier attendu: `capture_namenode.png`
- URL: `http://localhost:9870`

### c) Resultat de `hdfs dfs -ls -R /exercice`

- Fichier fourni: `hdfs dfs -ls -R exercice.txt`

### d) Resultat de `hdfs fsck /exercice/raw/clients.csv -files -blocks -locations`

- Fichier fourni: `fsck_exercice.txt`

### e) Courte explication du role de la replication

- Fichier fourni: `explication_replication.md`

---

## 4) Explication courte - role de la replication

La replication HDFS consiste a stocker plusieurs copies d'un meme bloc sur des DataNodes differents.  
Avec un facteur de replication egal a 3, chaque bloc existe en trois exemplaires.  
Cela augmente la disponibilite des donnees et permet de continuer la lecture des fichiers meme si un DataNode tombe en panne.

---

## 5) Checklist finale avant remise

- [ ] `run_exercice.sh` execute sans erreur dans le conteneur NameNode
- [ ] `hdfs dfs -ls -R /exercice` present dans `hdfs dfs -ls -R exercice.txt`
- [ ] sortie `fsck` reelle presente dans `fsck_exercice.txt`
- [ ] capture NameNode ajoutee (`capture_namenode.png`)
- [ ] dossier de rendu contient tous les fichiers cites
