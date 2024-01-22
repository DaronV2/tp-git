
## B1-Git - Partie 1 : Création du dépôt et _commits_

- Ouvrir un terminal (terminal _Git Bash_ à privilégier)

- Créer, en ligne de commande, un répertoire `tp-git`

mkdir tp-git

- Se déplacer dans le répertoire

cd tp-git

- Vérifier qu'on est dans le bon répertoire en affichant le chemin du répertoire courant

pwd

- Initialiser un dépôt Git

git init

- Lister tous les fichiers du répertoire (y compris les fichiers cachés) pour s'assurer que le répertoire `.git` à été créé

ls -a

- Ouvrir ce répertoire sous VS Code

- Exécuter `git status` et copier/coller la sortie

'''
PS C:\Users\darke\Music\tp-git> git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        reponses1.md

nothing added to commit but untracked files present (use "git add" to track)
'''

- Créer le fichier `fichier1.md` avec un contenu quelconque et l'enregistrer (vous pouvez utiliser VS Code pour créer et éditer des fichiers)

touch fichier1.md

  - Attention, il s'agit bien de créer un nouveau fichier, et non un répertoire. Il en sera de même tout au long de ce TP.

- Créer le fichier `fichier2.md` avec un contenu quelconque et l'enregistrer

touch fichier2.md, echo "Je suis le fichier deux"> fichier2.md

- Exécuter `git status` et copier/coller la sortie

'''
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        fichier1.md
        fichier2.md
        reponses1.md

nothing added to commit but untracked files present (use "git add" to track)

'''

- Ajouter `fichier1.md` à l'index de Git (zone de _Staging_)

git add fichier1.md

- Exécuter `git status` et copier/coller la sortie

'''
PS C:\Users\darke\Music\tp-git> git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   fichier1.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        fichier2.md
        reponses1.md

'''

- Créer un _commit_ avec pour message : "Ajout de fichier1.md"

git commit -m "Ajout de fichier1.md"

- **_VALIDATION PROF01_**

- Exécuter `git status` et copier/coller la sortie

'''
PS C:\Users\darke\Music\tp-git> git status 
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        fichier2.md
        reponses1.md

nothing added to commit but untracked files present (use "git add" to track)
'''

- Modifier `fichier1.md` et enregistrer

- Exécuter `git status` et copier/coller la sortie

'''
                                git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   fichier1.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        fichier2.md
        reponses1.md

no changes added to commit (use "git add" and/or "git commit -a")
'''

- Ajouter `fichier1.md` et `fichier2.md` à la zone de _Staging_

git add fichier1.md fichier2.md

- Créer un _commit_ "Ajout de fichier2.md et modification de fichier1.md"

git commit -m "Ajout de fichier2.md et modification de fichie1.md

- Exécuter `git status` et copier/coller la sortie

'''
PS C:\Users\darke\Music\tp-git> git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   fichier1.md
        new file:   fichier2.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        reponses1.md

'''

- Copier/coller l'ID des deux premiers _commits_ (utiliser `log`) :

  - ID _commit_ 1 :
    c85515c4b4dbf4cbf2ff8931a28a6c9758930bbc
  - ID _commit_ 2 :
    6263c073703aefdb315e7fdbe19feeec13bbe856

- Que signifie qu'un fichier est "_tracked_" ou "_untracked_" ?

Un fichier "tracked" est un fichier qui est connu et suivi par git, cad que si il est modifié et add a git on connait exactement ses changements par rapport a ses versions précédentes

Un fichier untracked est un fichier qui est connu par git mais pas suivi, on voit juste qu'il existe.

- Pourquoi doit-on passer les fichiers par la zone de _Staging_ (l'index) avant de les committer ?



- **_VALIDATION PROF02_**
