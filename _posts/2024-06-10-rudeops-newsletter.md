---
layout: post
title: Newsletter du 10 Juin 2024
subtitle: La newsletter qui débarque	
thumbnail-img: /assets/img/soldat.png
gh-repo: daattali/beautiful-jekyll
tags: [devops, Omakub, Ubuntu, database, Shell, Gitlab, Sql]
comments: true
mathjax: true
author: RudeOps
---

### Quoi de neuf ?

💊 **An Omakase Developer Setup for Ubuntu 24.04 by DHH :** Quand  [le papa de Ruby on Rails](https://world.hey.com/dhh)  s’ennuie, il lance de nouveaux projets. Le dernier en date s’appelle  [Omakub](https://omakub.org/), et consiste à transformer votre distrib Ubuntu en un système de développement web préconfiguré avec plein d’outils de base (Docker, VSCode, Neovim, etc) en une seule commande.

💝 **What's the difference between SH and BASH :** Vous n’avez jamais osé demander de peur de perdre votre streed cred ?  [Lisez cet article](https://medium.com/@shalinpatel./whats-the-difference-between-sh-and-bash-f8fa6b2cd9f0), vous comprendrez tout.

🥇  **Stop using UUIDs on your database :** On a tous coutume d’utiliser des UUIDs pour identifier de manière unique des lignes dans une base de données, mais ils peuvent vite devenir  [une source de problèmes de performance](https://www.danielfullstack.com/article/stop-using-uuids-in-your-database)  sur les très (très très) grosses infrastructures.

🎁 **Writing .gitlab-ci.yml file with examples :** Tout ce que vous rêviez de savoir sur l’écriture du .gitlab-ci.yml pour configurer proprement vos pipelines de CI/CD dans Gitlab.  [Simple basique](https://spacelift.io/blog/gitlab-ci-yml).

🏹 **SQL injection prevention cheat sheet :** Parce que chaque année, des milliers de serveurs meurent faute de règles de sécurité adéquates, on vous partage  [la cheat sheet de prévention sur les injections SQL](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html)  éditée par  [l’OWASP](https://owasp.org/).  

🚀  **Fastfetch :** Depuis que le célèbre  [Neofetch](https://github.com/dylanaraps/neofetch) n’est plus maintenu, il semblerait que ce soit  [Fastfetch](https://github.com/fastfetch-cli/fastfetch) qui fasse l’unanimité pour le remplacer et afficher plein d'informations sur votre système de manière achi classe. Ça ne sert à rien, donc c’est indispensable !

## BitKeeper, Linux, and licensing disputes: How Linus wrote Git in 14 days

![](https://storage.mlcdn.com/account_image/325165/l6vFXaLqb8oQ8ClgftxN6ZOTduXfp6ERcvEjtv5D.png)

Avant l’utilisation de BitKeeper, le contrôle de version du noyau Linux reposait sur Linus Torvalds himself, qui intégrait avec ses gros doigts potelés les patchs soumis par ses lieutenants. En 1998, Larry McVoy proposa BitKeeper, qui inspira Linus et qui déboucha sur Git qu'il créa en 2005, après des conflits sur l’utilisation de BitKeeper. Tout ça vous est raconté dans un article très complet écrit par les punks de chez graphite.dev. Merci à JMB qui nous a partagé le lien !

[Accéder au lien ->](https://graphite.dev/blog/bitkeeper-linux-story-of-git-creation)