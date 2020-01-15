# Utilisation de Git

Voici un tuto pour utiliser Git correctement avec les commandes associées.

## Mise en place

Pour mettre en place le workflow Git, il faut effectuer les étapes suivantes:  
- Créer un `fork` du dépôt git du groupe, c'est à dire une copie personnelle du dépôt
- Cloner ensuite le dépôt _forké_ sur un ordinateur à l'aide de la commande `git clone` pour en obtenir une copie locale
- Créer une branche de développement (`git checkout -b BRANCH`), il est important de ne pas travailler sur la branche `master` du _fork_ 
- Ajouter un lien avec le dépôt du groupe nommé `upstream` afin de pouvoir récupérer les changements (`git remote add upstream REPO_URL`) 


## Utilisation

Cette partie est dédiée à la réalisation d'une `Pull Request` pour intégrer des changements locaux sur le dépôt du groupe.

### 1. Valider les changements
Se positionner sur sa propre branche de développement.
```sh
git checkout BRANCH
```
Faire les modifications souhaitées puis regarder le status de git localement.
```sh
git status
```
Ajouter les modifications et suivre les fichiers créés.
```sh
git add FILES
```
Enregistrer les modifications localement.
```sh
git commit -m "COMMENT"
```


### 2. Mettre à jour la branche `master`

Se mettre sur la branche `master` locale.
```sh
git checkout master
```
Récupérer et appliquer les dernières mises à jour du dépôt du groupe.
```sh
git pull --rebase upstream master
```
Mettre à jour le dépôt _forké_ distant (origin) : 
```sh
git push origin master
```


### 3. Intégrer les changements

On souhaite intégrer les changements effectués avec les dernières mises à jour du dépôt du groupe.  

Dans un premier temps, se positionner sur sa propre branche de développement.
```sh
git checkout BRANCH
```
Intégrer ensuite les `commits` de la branche `master` à nos changements.
```sh
git rebase master
```
Cette étape peut entrainer des conflits, il est nécessaire de les résoudre pour poursuivre.


### 4. Sauvegarde des modifications

Sauvegarder les modifications sur la branche de développement du dépôt _forké_.
```sh
git push origin BRANCH
```


### 5. Créer la `Pull Request`

Aller sur Github et se laisser guider :)
