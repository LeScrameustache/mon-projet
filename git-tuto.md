
### Step 1 : Création du dossier

On crée un dossier de travail nommé `mon-projet` et on initialise Git :
```sh
Thomas@MSI MINGW64 ~
$ mkdir mon-projet

Thomas@MSI MINGW64 ~
$ cd mon-projet

Thomas@MSI MINGW64 ~/mon-projet
$ git init
```
Normalement, `Initialized empty Git repository in C:/Users/tempr/mon-projet/.git/` apparaît dans la console.

**Remarque :*** l'en-tête de ligne dans GitBash devient :`Thomas@MSI MINGW64 ~/mon-projet (master)` . On remarque que la ligne se termine par le nom de la branche sur laquelle on se trouve (ici, master).
### Step 2 : Lier au repo Github
Après avoir crée le repository sur github et récupéré son url `https://github.com/LeScrameustache/mon-projet.git`, on initialise :
```sh
Thomas@MSI MINGW64 ~/mon-projet (master)
$ git remote add origin https://github.com/LeScrameustache/mon-projet.git
```
### Step 3: On sauvegarde son travail
Après avoir travaillé (ici créé un fichier `git-tuto.md`), on met à jour la liste des commits :
```sh
Thomas@MSI MINGW64 ~/mon-projet (master)
$ git add .
```
**Remarque :** il est possible que le message `warning: in the working copy of 'git-tuto.md', LF will be replaced by CRLF the next time Git touches it` apparaisse, il s'agit d'un truc pas grave en lien avec l'encodage des retours à la ligne sous Windows.

On peut vérifier la liste des changements qui seront ajouté au prochain `commit` :
```sh
Thomas@MSI MINGW64 ~/mon-projet (master)
$ git status
```
***Réponse dans la console :***
```sh
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   git-tuto.md
```

On peut effectuer le `commit` , avec le message `premier commit`:
```sh
Thomas@MSI MINGW64 ~/mon-projet (master)
$ git commit -m "premier message"
```
***Réponse dans la console :***
```sh
[master (root-commit) 70654d3] premier message
 1 file changed, 27 insertions(+)
 create mode 100644 git-tuto.md
```
### Step 4 : envoi sur github
On va maintenant envoyer notre commit sur le repository github :
```sh
Thomas@MSI MINGW64 ~/mon-projet (master)
$ git push -u origin master
```
***Réponse dans la console :***
```sh
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 735 bytes | 735.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/LeScrameustache/mon-projet.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.
```
