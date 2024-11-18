TP Github
Partie 1 : Les bases de Git
1.	Initialisation d’un répertoire
    Que fait la commande git init ?
        Réponse :  Elle permet d’initialiser / créer un dépôt.
 
    Quelle est la différence entre git add et git commit ?
        Réponse : La commande git add ajoute le contenu du répertoire de travail dans la zone staging area pour le prochain commit. 
        Quand la commande git commit est lancée, par défaut elle ne regarde que cette zone d'index, donc git add est utilisée pour réaliser le prochain commit exactement comme vous le voulez.
        Et donc git commit emmène le contenu du git add dans la zone localrepo.
 
    Expliquer pourquoi il est important de bien rédiger les messages de commit.
        Réponse : Car elle permet de mieux comprendre le contenu du repository, par exemple le message peut contenir les modifications apportées dans un fichier qui se trouve dans le commit.
 
2.	Historique et modifications
    Quelle est la commande pour ajouter ce fichier au suivi ?
        Réponse : La commande pour ajouter ce fichier au suivi est git add.
 
    Que représente chaque ligne dans le résultat de git log ?
        Réponse : On peut remarquer que dans la capture d’écran ci-dessous, on peut apercevoir la clé d’identification du commit (en jaune), puis l’identification de la personne qui a effectuer le commit, avec le nom d’utilisateur et l’adresse mail lié au compte.
    Puis il y a la date du commit ainsi que le contenu du Commit.
 
    A quoi sert git diff ?
        Réponse : git diff permet d’afficher la différence entre les fichiers qui ont été modifiés qui se trouve directement dans le dépôt, et ce qui seront prochainement ajoutés dans le dépôt et repository .

3.	Utilisation de .gitignore
    Pourquoi est-il utile d’avoir un fichier .gitignore ?
        Réponse : Le fichier .gitignore est utile car elle permet d’ignorer des fichiers ou dossiers en particulier. Comme dans la capture d’écran ci-dessous, on peut voir que j’ai ignoré tous les fichiers qui ont l’extension .py .
 
Partie 2 : Utilisation de GitHub
1.	Création d’un dépôt GitHub
    Quelle est la différence entre un dépôt public et un dépôt privé ?
        Réponse :  La différence entre un dépôt public et un dépôt privé est leur moyen de les voir. 
        En effet, un dépôt public peut être vu par tout le monde, plus précisément ceux qui se connecte ou sont sans être connecté sur GitHub.
        Tandis qu’un dépôt privé peut être vu que par les personnes que le créateur a donné les droits (pour modifier dans le dépôt) ou donné l’accès à le visualiser.
 
2.	Lier le dépôt local à GitHub
    Expliquez à quoi sert la commande git remote add origin ?
        Réponse : La commande sert à créer une branche distante qui se nomme origin dans le repository distant.
 
    Que signifie l’option -u dans la commande git push ?
        Réponse : Elle permet d'associer la branche locale actuelle à une branche distante spécifique, créant ainsi un suivi entre elles.

Partie 3 : Collaboration et Workflows
1.	Créer et gérer des branches
    Pourquoi est-il recommandé de créer une branche pour chaque nouvelle fonctionnalité ? 
        Réponse : Créer une branche pour chaque fonctionnalité permet d'isoler les changements, faciliter la collaboration, et tester ou revoir le code avant de l'intégrer sans perturber la branche principale.

    Quelle commande permet de lister toutes les branches existantes ?
        Réponse : La commande permettant de lister les branches existantes d’un dépôt et git branch.
 

2.	Pull requests (PR) :
    Pourquoi est-il important de bien document une Pull Request ?
        Réponse : Elle permet à un contributeur de notifier les autres personnes d’un projet que ce dernier a effectué des modifications dans une branche différente que la principale. 
        De plus, cela permet que les modifications soient fusionnées dans la branche primaire du dépôt.
3.	Fusion de la PR :
 
Partie 4 : Workflow GitHub Flow vs Git Flow
1.	GitHub Flo
    Dans quel cas est-il préférable d'utiliser GitHub Flow plutôt que Git Flow ?
        Réponse : GitHub Flow est idéal pour :

              -  Déploiements fréquents en production (cycle continu).
              -  Projets avec une seule version active (ex. SaaS).
              -  Petites équipes ou projets simples.
              -  Éviter la complexité inutile de Git Flow.
              -  Git Flow convient mieux aux projets avec plusieurs versions ou cycles complexes.
2.	Git Flow
    Expliquez le rôle des branches hotfix dans Git Flow ?
        Réponse : Les branches hotfix dans Git Flow corrigent des bugs critiques en production. Créées à partir de main, elles permettent :

                    -Correction rapide : Le bug est corrigé et testé.
                    -Fusion : La branche est fusionnée dans main (pour déploiement) et develop (pour le cycle en cours).
                    -Versionnage : Une nouvelle version peut être taguée.
                
                Elles garantissent des corrections sans perturber le développement en cours.

Partie 5 : Travail collaboratif
1. Cloner un projet
    Quelle est la différence entre git clone et git pull ?
            Réponse :
                    - git clone : Clone un dépôt distant sur votre machine locale (création d'une copie complète du projet).
                    - git pull : Récupère les dernières modifications d'un dépôt distant et les fusionne avec votre branche locale.
2. Résoudre des conflits
    Quelles sont les étapes à suivre après avoir résolu un conflit ?
            Réponse : 
            - Résoudre le conflit dans les fichiers.
            - Ajouter les fichiers résolus avec git add.
            - Terminer la fusion avec git commit.
            - Si nécessaire, pousser les changements avec git push.


Partie 6 : Rebase et Cherry-pick
1. Rebase 
    Quelle est la différence entre merge et rebase ?
            Réponse : merge conserve l’historique complet et crée un commit de fusion, tandis que rebase réécrit l’historique pour le rendre plus linéaire.
2. Cherry-pick
Dans quel cas utiliseriez-vous cherry-pick ?
            Réponse : git cherry-pick permet d’appliquer un commit spécifique d’une autre branche à la branche courante, sans fusionner toute la branche. Utilisé pour sélectionner un commit particulier, comme un correctif ou une fonctionnalité.

Partie 7 : Utilisation des Submodules
1. Ajouter un submodule
    Pourquoi utiliser des submodules plutôt que copier directement le code dans votre dépôt ?
           Réponse : Utiliser des submodules Git plutôt que de copier le code directement permet de mieux gérer les dépendances, contrôler les versions, faciliter la maintenance et la collaboration, et améliorer la réutilisabilité et la sécurité du code.
2. Initialiser et mettre à jour les submodules
    Quelle commande permet de mettre à jour les submodules après un pull ?
           Réponse : La commande permettant de mettre à jour les submodules après un pull est la suivante : 
           git submodule update --remote.