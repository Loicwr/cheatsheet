ATTENTION CREER UN REPO DEPUIS MON TERMINAL  : gh repo create NomDeMonRepo --public --source=. --remote=origin
Une Pull Request (PR) est une demande de fusion (merge) d’une branche de travail dans une branche principale (souvent main ou master) dans un dépôt de code

Le rebase réécrit l'historique et peut rendre l'historique plus propre et linéaire. 
Le merge préserve l'historique exact et crée un commit de fusion.
Il est recommandé de rebaser des branches locales avant de les pousser pour garder un historique propre, mais le merge est souvent préféré dans les projets collaboratifs pour préserver la trace des fusions.

Synchroniser votre fork avec l'upstream : Pour récupérer les modifications de l'upstream (le dépôt d'origine), vous pouvez faire :
    git fetch upstream
    git checkout main
    git merge upstream/main
Cela vous permettra de garder votre fork à jour avec les modifications apportées au dépôt d'origine.

La commande git stash permet de mettre de côté temporairement vos modifications locales (non validées) afin de pouvoir travailler sur autre chose sans perdre votre travail en cours.
Vous pouvez aussi utiliser git stash pop, qui applique et supprime le stash en une seule commande.

Les branches dans Git permettent de travailler sur différentes versions d’un projet de manière isolée. Cela permet de développer de nouvelles fonctionnalités, corriger des bugs ou tester sans affecter la branche principale.
Créer une branche :
git checkout -b nouvelle-branche
Cela crée et bascule sur une nouvelle branche.

Fusionner une branche : Lorsque vous avez terminé de travailler sur une branche, vous pouvez la fusionner avec une autre branche (généralement la branche main ou develop) :
git checkout main
git merge nouvelle-branche

La différence entre git switch et git checkout réside principalement dans leur utilisation et leur objectif.
Bien que les deux commandes puissent être utilisées pour changer de branche, git switch a été introduit dans Git 2.23 pour simplifier et clarifier certaines actions courantes liées aux branches. 

Principales différences
Action	                                                        git checkout	                                         git switch
Changer de branche	                              git checkout nom-de-la-branche                                git switch nom-de-la-branche
Créer et changer de branche	                      git checkout -b nouvelle-branche	                            git switch -c nouvelle-branche
Restaurer des fichiers	                              git checkout -- fichier.txt	                            Pas de support pour cette fonction
Simplicité	                                      Plus complexe, plusieurs usages	                            Spécifiquement conçu pour les branches

test 3
Pourquoi utiliser git switch ?

    Simplicité : La commande git switch rend le changement de branche plus explicite et moins confus.
    Clarté : git switch se concentre uniquement sur la gestion des branches, tandis que git checkout gère aussi les fichiers, ce qui peut prêter à confusion.
    Éviter les erreurs : L'introduction de git switch réduit les risques d'erreurs, car elle ne permet pas de manipuler des fichiers de manière imprévue.

Conclusion

    Utilisez git switch pour tout ce qui concerne le changement de branche et la création de nouvelles branches. Cette commande est plus claire et mieux adaptée aux actions liées aux branches.
    Vous pouvez toujours utiliser git checkout pour des tâches plus avancées comme la restauration de fichiers ou pour une compatibilité avec les versions antérieures de Git.

Comprendre le merge dans Git

Le merge dans Git permet de combiner les changements de deux branches distinctes. Lorsque vous effectuez une fusion de branche, Git intègre les commits de la branche source dans la branche cible (souvent la branche principale, comme main ou master).

    Par exemple, pour fusionner une branche de fonctionnalité (feature-branch) dans main :

    git checkout main
    git merge feature-branch

Lorsque vous faites un merge, il peut y avoir deux cas possibles : fast-forward ou merge commit.
2. Comprendre le "fast-forward"

Le "fast-forward" se produit lorsque la branche cible (par exemple, main) n'a pas évolué depuis le point où vous avez créé votre branche de fonctionnalité. Dans ce cas, Git peut avancer directement la tête de la branche cible vers la dernière révision de la branche source sans créer de commit de fusion.

    Exemple : Si main est à jour et que vous avez créé votre branche de fonctionnalité à partir de main, et que vous y avez ajouté des commits, un merge de la branche de fonctionnalité dans main peut simplement avancer le pointeur de main vers la branche de fonctionnalité.

    Cela se produit quand il n'y a pas de divergence entre les deux branches, donc Git peut effectuer un "avancement rapide".

    Commandes :

    git checkout main
    git merge feature-branch  # Git avancera simplement le pointeur de main

    Il n'y a pas de merge commit ici, l'historique reste linéaire.

3. Différence entre un "commit" et un "merge commit"

    Commit : Un commit classique dans Git est un enregistrement des changements dans l'historique du projet. Il contient les modifications apportées à un ou plusieurs fichiers et est associé à un message de commit.

    Exemple de commit :

git commit -m "Ajout de la fonctionnalité X"

Merge commit : Un merge commit est un commit spécial créé lors d'une fusion (merge) entre deux branches. Il a au moins deux parents : l'un correspondant à la branche cible et l'autre à la branche source. Ce commit est nécessaire lorsqu'une fusion n'est pas un fast-forward, c'est-à-dire lorsqu'il y a des changements dans les deux branches qui doivent être combinés.

Exemple de merge commit :

git checkout main
git merge feature-branch

Ici, Git crée un merge commit pour marquer le point où les deux branches sont fusionnées.


4. .gitignore global ou pas ?

Le fichier .gitignore permet de spécifier les fichiers ou répertoires qui ne doivent pas être suivis par Git. Vous pouvez avoir un fichier .gitignore spécifique à un projet, ou un fichier .gitignore global pour ignorer des fichiers générés automatiquement à l’échelle de votre machine, comme les fichiers de configuration d’éditeur ou les fichiers binaires.
.gitignore global :

    Il est utile lorsque vous avez des fichiers qui ne doivent pas être suivis dans tous vos projets, comme les fichiers de configuration d’un éditeur (.vscode/, .idea/), ou des fichiers temporaires (comme *.log).

    Pour configurer un .gitignore global :
        Créez un fichier global .gitignore :

touch ~/.gitignore_global

Ajoutez ce fichier à la configuration Git globale :

git config --global core.excludesfile ~/.gitignore_global


5. Différence entre git pull et git fetch

    git fetch : Récupère les modifications du dépôt distant sans les appliquer à votre branche locale. Cette commande vous permet de voir les mises à jour sans les fusionner immédiatement.

    Exemple :

git fetch origin

git pull : Récupère les modifications du dépôt distant et les fusionne automatiquement dans votre branche locale. Cela est équivalent à faire un git fetch suivi d'un git merge (ou git rebase, selon la configuration).

Exemple :

    git pull origin main

    Différence : git pull modifie immédiatement votre branche locale, tandis que git fetch vous permet de voir les modifications sans affecter votre travail en cours.

6. À quoi sert la commande git fetch --prune ?

La commande git fetch --prune est utilisée pour supprimer les références distantes obsolètes (les branches distantes supprimées) dans votre dépôt local. Lorsqu'une branche est supprimée du dépôt distant, elle persiste encore localement jusqu'à ce que vous fassiez un fetch avec l'option --prune.

Exemple :

git fetch --prune origin

Cela garantit que les branches qui n'existent plus sur le dépôt distant sont supprimées de vos références locales.


7. Comment configurer Git pour que git fetch --prune soit fait automatiquement ?

Pour que Git exécute automatiquement git fetch --prune chaque fois que vous récupérez des modifications d'un dépôt distant, vous pouvez configurer cette option à l'aide de la configuration gc.auto ou fetch.prune dans votre fichier de configuration Git.

Exécutez cette commande pour configurer Git à exécuter --prune par défaut :

git config --global fetch.prune true

Cela garantit que Git supprime automatiquement les branches distantes supprimées chaque fois que vous utilisez git fetch.


Priorité des configurations

Git applique les configurations dans cet ordre de priorité :

    Local (au niveau du dépôt) – a la priorité la plus élevée.
    Global (au niveau de l'utilisateur) – s'applique si aucune configuration locale n'est définie.
    Système (au niveau du système) – a la priorité la plus faible et est utilisée si aucune configuration locale ou globale n'est définie.





    Ajouter un alias :

git config --global alias.[alias] "[commande]"

Vérifier les alias :

git config --get-regexp alias

Supprimer un alias :

git config --global --unset alias.[alias]
