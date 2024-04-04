
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


