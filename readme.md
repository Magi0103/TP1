# TP: introduction à Git

Bienvenu à toi, lecteur ! Ce TP a pour objectif de t'aider à prendre en main Git en mettant les mains dans le cambouis. Mais surtout pas de panique si tu n'as jamais utilisé Git ! Ce TP reprend tout de plus le début, mais a été pensé pour faire suite à une présentation théorique.

## Prérequis

Pour pouvoir faire ce TD, il te faudra le logiciel Git installé sur ton ordinateur :
* Si tu es sous Linux ou Mac, git est normalement déjà installé.
* Si tu es sous Windows, je te conseille d'installer [GitBash](https://github.com/anaszmeafc/TP1).

Ce TP va aussi utiliser l'éditeur de code [VSCode](https://github.com/anaszmeafc/TP1). Je te conseille de l'utiliser aussi pour plus de clarté mais tu peux utiliser un autre éditeur de code.

Maintenant que les prérequis sont installés, il est temps de se lancer !

## Partie 0 : Configuration de Git et du GitHub de Zemmouri 

Avant de pouvoir utiliser Git, il y a quelques configuration à faire.

### Ajout d'un nom et email dans Git

Pour que les modifications que tu feras sur le repository soient identifiables, il faut fournir un nom et une adresse email. Pour faire cette configuration, ouvre GitBash (ou un terminal pour Mac/Linux) et entre les commandes suivantes en remplaçant nom et adresse email :

`git config --global user.name "<votre nom>"`

`git config --global user.email "<votre adresse email>"`

Git sait maintenant qui tu es et le nom choisi sera associé aux modifications que tu feras.

### Paramètre de connexion au serveur GitHub

Lorsque l'on utilise Git, le code est stocké sur un serveur distant, ici :  
👉 **https://github.com/anaszmeafc/TP1**

Dans le cas où le projet n'est pas public, il faudra s'authentifier pour pouvoir synchroniser les fichiers entre le serveur et ton ordinateur.

---

### Paramétrer l'authentification par clé SSH

* Crée une clé SSH en suivant par exemple ce tutoriel : https://github.com/anaszmeafc/TP1
* Ajoute ta clé dans ton profil GitHub.
* Tu pourras maintenant t'authentifier via SSH.

---

Tout est maintenant configuré, on peut entrer dans le vif du sujet !


## Partie 1 : Fork et Repository

La première étape est de créer un repo Git. Au lieu de créer un repo vide, nous allons découvrir une nouvelle opération : **le fork**.

### Fork du projet formation

Rends‑toi ici :  
👉 https://github.com/anaszmeafc/TP1

* Clique sur ***Fork***
* Choisis ton compte
* Une fois créé, ton fork est prêt
* Tu peux maintenant travailler dessus librement

Il ne reste plus qu'à récupérer une copie locale.

### Clone du repo

* Sur ton dépôt forké, clique sur **Code** et copie le lien SSH
* Dans un terminal :

```
git clone <lien SSH>
```

---

## Partie 2 : Versionnage et Premiers commits

Ouvre le dossier dans VSCode.

### Mission 1 : Modifier un fichier

Supprime les lignes indiquées, puis fais :

```
git add .
git commit -m "Suppression des lignes inutiles"
git push
```

### Mission 2 : Ajouter un fichier

Crée `solutions.md` et décris ta démarche.  
Commit + push.

### Mission 3 : Supprimer un fichier (facultatif)

Supprime `fichier_inutile` puis commit + push.

---

## Partie 3 : Collaboration, branches et merge requests

### Mission 1 : Créer une branche

```
git checkout -b nouvelle-branche
```

Crée un `.gitignore` :

```
code/__pycache__/
```

Push :

```
git push --set-upstream origin nouvelle-branche
```

### Merge Requests

Va dans l’onglet **Pull Requests** de GitHub → crée une PR → compare → merge.

---

## Rebase

GitHub permet le rebase via l’interface lorsque ta branche est en retard sur `main`.

---

## Cherry-pick (facultatif)

Récupère le SHA d’un commit dans l’onglet **Commits**, puis :

```
git checkout branche-a-rebase
git cherry-pick <SHA>
```

---

## Conclusion

Tu as découvert les bases essentielles de Git : commit, push, branches, fork, merge, rebase…  
Continue à pratiquer et tout deviendra naturel !
