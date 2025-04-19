---
title: Bash & Zsh
date: 2022-01-07 08:01:35 +0300
subtitle: Le guide de survie
image: '/images/jongle.png'
---

**Bash** (Bourne Again SHell) est un shell Unix libre et un langage de commande utilisé largement dans les systèmes Linux. Il est simple, stable, et bien documenté.  

**Zsh** (Z Shell) est un shell plus puissant et interactif, compatible avec Bash, mais avec des fonctionnalités supplémentaires comme l'autocomplétion améliorée, les globbing avancés, l'historique partagé, les prompts dynamiques et la correction automatique.

---
[Oh My Zsh](https://ohmyz.sh/) est un framework communautaire pour gérer la configuration de Zsh qui apporte :
- des **thèmes** stylisés pour le prompt,
- une **centaine de plugins** (git, docker, z, autojump, etc.),
- une gestion propre du fichier `.zshrc`.


[Oh My Bash](https://github.com/ohmybash/oh-my-bash) est le pendant d’Oh My Zsh pour Bash. Il fournit également :
- des **thèmes de prompt** variés,
- des **plugins utiles** (git, aliases, etc.),
- une structure de configuration modulaire dans `.bashrc`.

---

## Commandes de base

| Commande             | Description                                |
|----------------------|--------------------------------------------|
| `pwd`                | Affiche le répertoire courant              |
| `ls`                 | Liste les fichiers                         |
| `cd /chemin`         | Change de répertoire                       |
| `touch fichier`      | Crée un fichier vide                       |
| `mkdir dossier`      | Crée un dossier                            |
| `rm fichier`         | Supprime un fichier                        |
| `rm -r dossier`      | Supprime un dossier récursivement          |
| `cp source dest`     | Copie un fichier ou dossier                |
| `mv source dest`     | Déplace ou renomme un fichier              |
| `cat fichier`        | Affiche le contenu d’un fichier            |
| `less fichier`       | Affiche un fichier page par page           |
| `head -n 10 fichier` | Affiche les 10 premières lignes            |
| `tail -n 10 fichier` | Affiche les 10 dernières lignes            |


## Recherche

| Commande                      | Description                                      |
|-------------------------------|--------------------------------------------------|
| `grep 'mot' fichier`          | Recherche un mot dans un fichier                |
| `find . -name "*.txt"`        | Recherche des fichiers avec extension `.txt`    |
| `history`                     | Affiche l’historique des commandes              |
| `ctrl + r`                    | Recherche dans l’historique (reverse-i-search)  |


## Redirection & Pipes

| Commande           | Description                             |
|--------------------|-----------------------------------------|
| `>`                | Redirige la sortie vers un fichier      |
| `>>`               | Ajoute à la fin d’un fichier            |
| `<`                | Lit depuis un fichier                   |
| `|`                | Envoie la sortie d’une commande à une autre |
| `tee fichier`      | Écrit la sortie dans un fichier et à l'écran |


## Variables et Scripts

| Commande                       | Description                                  |
|--------------------------------|----------------------------------------------|
| `VAR="valeur"`                | Déclare une variable                         |
| `echo $VAR`                   | Affiche la valeur de la variable             |
| `export VAR="val"`            | Rend une variable accessible aux sous-processus |
| `$(commande)`                 | Substitution de commande                     |
| ```#!/bin/bash``` ou ```#!/bin/zsh``` | Shebang pour script Bash/Zsh        |
| `source script.sh`            | Exécute un script dans le shell courant      |


## Boucles & Conditions

| Syntaxe                        | Description                         |
|--------------------------------|-------------------------------------|
| `if [[ condition ]]; then ... fi` | Condition                         |
| `for i in liste; do ... done` | Boucle for                          |
| `while condition; do ... done`| Boucle while                        |
| `case $var in ...)`           | Condition switch-like               |


## Tips Zsh spécifiques

| Fonctionnalité             | Description                                |
|----------------------------|--------------------------------------------|
| `autoload -Uz compinit && compinit` | Active la complétion               |
| `setopt autocd`            | Permet de naviguer sans `cd`              |
| `setopt globdots`          | Permet de lister les fichiers cachés avec `*` |
| `alias`                    | Fonctionne comme sous Bash                |
| `~`                        | Expansion du home comme sous Bash         |


## Personnalisation avec Oh My Zsh / Bash

| Élément             | Description                                  |
|---------------------|----------------------------------------------|
| `~/.zshrc` / `~/.bashrc` | Fichier de config du shell                |
| `ZSH_THEME="agnoster"`  | Change le thème Zsh                       |
| `plugins=(git docker z)`| Active des plugins Zsh                    |
| `OSH_THEME="font"`      | Change le thème dans Oh My Bash          |
| `alias gs='git status'` | Déclare un alias                         |


## Raccourcis clavier (Bash & Zsh)

| Raccourci             | Action                                         |
|------------------------|-----------------------------------------------|
| `Ctrl + a`             | Aller au début de la ligne                    |
| `Ctrl + e`             | Aller à la fin de la ligne                    |
| `Ctrl + u`             | Supprime du curseur au début de la ligne     |
| `Ctrl + k`             | Supprime du curseur à la fin de la ligne     |
| `Ctrl + w`             | Supprime le mot précédent                    |
| `Alt + d`              | Supprime le mot suivant                      |
| `Ctrl + l`             | Efface l'écran (comme `clear`)               |
| `Ctrl + r`             | Recherche dans l’historique                  |
| `Ctrl + y`             | Colle le dernier texte supprimé (yank)       |
| `Ctrl + _`             | Annule la dernière action (comme undo)       |
| `Ctrl + t`             | Échange les deux caractères avant le curseur |
| `Alt + .`              | Rappelle le dernier argument de la commande précédente |
| `!!`                   | Réexécute la dernière commande               |
| `!n`                   | Réexécute la commande numéro n de l’historique |
| `!commande`            | Réexécute la dernière commande commençant par `commande` |
| `^old^new`             | Réexécute la dernière commande en remplaçant `old` par `new` |

## Jobs & Processus

| Commande      | Description                                     |
|---------------|-------------------------------------------------|
| `&`           | Lance un processus en arrière-plan              |
| `jobs`        | Liste les processus en arrière-plan             |
| `fg`          | Reprend un job en avant-plan                    |
| `bg`          | Reprend un job en arrière-plan                  |
| `kill PID`    | Tue un processus avec son PID                   |
| `kill %n`     | Tue le job n                                    |


## Nettoyage & sortie

| Commande       | Description                       |
|----------------|-----------------------------------|
| `clear`        | Nettoie l’écran                   |
| `ctrl + l`     | Idem que `clear`                  |
| `exit`         | Quitte le shell                   |
| `ctrl + d`     | Ferme le terminal (EOF)           |
