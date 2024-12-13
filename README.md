🚀 ALOGIX Data Migration Tool Documentation
📌 1. Vue d'ensemble du projet

ALOGIX est une solution logicielle conçue pour faciliter la migration de bases de données relationnelles (SGBDR) vers des bases NoSQL (Redis, par exemple). Ce projet garantit une compatibilité et une interopérabilité entre ces deux types de SGBD en mettant l'accent sur la facilité, la sécurité et les performances.
Objectifs du projet :

    Permettre la migration de SGBDR vers Redis (et vice versa) en utilisant des commandes personnalisées.
    Garantir l'intégrité et la sécurité des données pendant la migration.
    Fournir une solution rapide et optimisée pour des bases de données de grande taille.

💻 2. Installation
Prérequis :

    Java : Version 11 ou supérieure.
    Maven : Pour la gestion des dépendances et la compilation.
    Redis : Installé et configuré sur votre système ou serveur distant.
    Java Redis Client : Utilisation de la bibliothèque Jedis pour les interactions Redis.
    Java JSON Parser : Intégré via le package com.allom.utils.JsonHandler.

Étape 1 : Récupération du code source

Clonez le dépôt ou téléchargez le package.

git clone https://github.com/Alloma70/

Étape 2 : Configuration du projet

Allez dans le répertoire principal du projet :

cd ALOGIX

Étape 3 : Compilation avec Maven

Utilisez Maven pour compiler le projet :

mvn clean install

Étape 4 : Exécution de la commande principale

Pour migrer une base SGBDR vers Redis avec vos données existantes, utilisez :

mvn exec:java -Dexec.mainClass="com.allom.commands.AllomXpass"

🛠️ 3. Utilisation
Commande principale : AllomXpass

Cette commande extrait des données d'une base source SGBDR et les transfère vers Redis, en utilisant un format JSON intermédiaire pour garantir la cohérence des données.
Exemple d'utilisation :

Pour lancer une migration, configurez les chemins dans le fichier config.properties, puis exécutez :

mvn exec:java -Dexec.mainClass="com.allom.commands.AllomXpass"

⚙️ 4. Sécurité

Pour garantir la sécurité des données, les fonctionnalités suivantes sont intégrées

🏗️ 5. Performances

Pour assurer une migration rapide et efficace, les optimisations suivantes ont été intégrées :

📂 Structure du projet :

src/
  main/
    java/
      com/
        allom/
          commands/
            AllomXpass.java
          utils/
            ConfigLoader.java
            JsonHandler.java
            EncryptionUtils.java
    resources/
      config.properties
      sac.json
      transformed.json
  test/
    com/
      allom/
        tests/
          CommandTests.java
pom.xml

💼 6. Configuration
Exemple de fichier config.properties :

sac.path=/chemin/vers/source.json
redis.host=127.0.0.1
redis.port=6379
redis.password=your_redis_password
batch.size=500
encryption.key=your_encryption_key

🤝 Contribution

Les contributions sont encouragées ! Pour contribuer :

    Forkez le projet sur GitHub.
    Proposez une Pull Request avec une nouvelle fonctionnalité ou une correction.
    Passez vos tests localement avant de soumettre.

📜 Licence

Ce projet est sous Licence Propriétaire d'ALOGIX Startup. Toutes les utilisations de ce package doivent respecter la politique d'utilisation et les termes contractuels définis par la société ALOGIX.

⏩ Pour toute demande, contactez : pycerveau70@gmail.com.

© 2024 ALOGIX - Tous droits réservés.
