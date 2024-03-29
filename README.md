# Workflow GitHub Actions

Ce dépôt contient un workflow GitHub Actions qui automatise le processus de construction d'un projet Java à l'aide de Gradle.

## Description du workflow

Le workflow est déclenché lors d'un push ou d'une pull request sur la branche `main`. Il s'exécute sur un environnement Ubuntu et comprend les étapes suivantes :

1. **Checkout du code** : Cette étape récupère le code du dépôt à l'aide de l'action `actions/checkout@v2`.

2. **Configuration du JDK** : Cette étape configure le JDK (Java Development Kit) sur la machine d'exécution à l'aide de l'action `actions/setup-java@v2`. Elle est configurée pour utiliser la version 17 du JDK.

3. **Construction avec Gradle** : Cette étape exécute la commande de construction Gradle pour construire le projet Java. La commande par défaut est `./gradlew build`, mais vous pouvez la modifier selon vos besoins dans le fichier du workflow.

## Pour commencer

Pour utiliser ce workflow GitHub Actions dans votre propre projet, suivez ces étapes :

1. Copiez le contenu du fichier `.github/workflows/main.yml` à l'emplacement correspondant dans votre dépôt. Si le répertoire `.github/workflows` n'existe pas, créez-le.

2. Modifiez le fichier du workflow si nécessaire. Vous pouvez mettre à jour la configuration des branches dans la section `on` pour correspondre aux branches déclencheuses souhaitées. De plus, vous pouvez personnaliser la version du JDK, la commande de construction Gradle ou ajouter des étapes supplémentaires selon vos besoins.

3. Validez et poussez le fichier du workflow vers votre dépôt.

## Personnalisation du workflow

Vous pouvez personnaliser le workflow pour répondre aux besoins spécifiques de votre projet. Voici quelques personnalisations possibles :

- Modifier les branches qui déclenchent le workflow en mettant à jour la section `on` dans le fichier du workflow.

- Changer la version du JDK en mettant à jour le paramètre `java-version` dans l'étape `Configuration du JDK`.

- Ajuster la commande de construction Gradle dans l'étape `Construction avec Gradle` pour correspondre à la tâche de construction ou aux arguments supplémentaires spécifiques à votre projet.

## Contribution

Si vous rencontrez des problèmes ou avez des suggestions d'amélioration, n'hésitez pas à ouvrir une issue ou à soumettre une pull request dans ce dépôt.

## Licence

Ce projet est sous licence [MIT License](LICENSE).
