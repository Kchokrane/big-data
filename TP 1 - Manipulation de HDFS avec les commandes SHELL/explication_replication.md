# Role de la replication dans HDFS

La replication dans HDFS consiste a stocker plusieurs copies d'un meme bloc de donnees sur des DataNodes differents.

Pourquoi c'est important:
- Tolerance aux pannes: si un DataNode tombe, les donnees restent lisibles via les autres copies.
- Disponibilite: le fichier reste accessible meme si une machine est indisponible.
- Fiabilite: le risque de perte de donnees diminue.

Dans cet atelier, le facteur de replication est regle a 3. Cela signifie que chaque bloc du fichier est stocke en trois exemplaires dans le cluster.
