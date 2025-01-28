---
layout: post
title: Newsletter du 22 Juillet 2024
subtitle: Merci à Crowdstrike notre nouveau sponsor !		
thumbnail-img: /assets/img/Barbara rigole.png
gh-repo: daattali/beautiful-jekyll
tags: [devops, Starship, Github, API, PostgreSQL, S3]
comments: true
mathjax: true
author: RudeOps
---

Je pense qu'on a tous pris conscience des limites de notre modèle actuel et de la dépendance maladive qu'on a auprès de certains éditeurs logiciels. Comment a-t-on fait pour en arriver là ? Comment corriger le tir et comment trouver un équilibre ? Des questions qui auront un écho, on l'espère, dans les prochaines années, et dont les réponses viendront en partie des acteurs engagés pour un écosystème plus sain que ce qu'on a aujourd'hui.  
  
Cyril

### Quoi de neuf ?

🏃‍♂️  **Starship, a better terminal prompt in 2 minutes :** Un énième terminal qui se veut minimaliste, rapide et personnalisable,  [facile à configurer](https://itnext.io/starship-a-better-terminal-prompt-in-2-minutes-48586aecc1a6)  avec TOML. Il a pas mal de modules intégrés et permet de personnaliser l'affichage selon vos besoins. On a testé, c'est pas mal ouais.

💝 **Using a git commit template :** Un bel article qui explique les bénéfices de  [standardiser les commits](https://blog.scottlowe.org/2024/07/15/using-a-git-commit-template/)  à travers un système de templates, par l'ami Scott Lowe qu'on aime beaucoup.

🥇  **Github Actions tutorial :** Un chouette tuto  [rédigé par les cowboys de chez Spacelift](https://spacelift.io/blog/github-actions-tutorial)  qui couvre la création de workflows, la configuration des jobs, la gestion des secrets et le déploiement d'applications à l'aide d'exemples écrits en Go. Vachement plus simple que la doc publiée sur Github.

😱 **What is an API definition :** Dis donc Jamy, savais-tu que les spécifications d'API fournissent un plan détaillé qui précise leur structure, leurs endpoints, les requêtes, les réponses et les méthodes d'authentification ? Mais oui Fred, et  [en lisant cet article des outlaws de chez Nordic APIS](https://nordicapis.com/what-is-an-api-definition/)  tu apprendras qu'OpenAPI (anciennement Swagger) est la spécification d'API la plus largement utilisée en 2024.

🏹 **Don't query your PostgreSQL anymore, prefer PostgREST :** L'article détaille comment configurer PostgREST, un serveur web autonome  [transformant les bases de données PostgreSQL en API RESTful](https://www.avonture.be/blog/docker-postgrest/) simplifiant les interactions avec votre DB. L'auteur partage son expérience de migration de MySQL vers PG et explique comment PostgREST a simplifié son code PHP en éliminant les requêtes SQL directes. Il y a aussi un tuto sur la configuration et l'utilisation de PG avec Docker sur lequel votre DBA ne crachera pas.  

🚀  **Using S3 as a container registry :** Attention,  [cette cascade a été réalisée par un professionnel](https://ochagavia.nl/blog/using-s3-as-a-container-registry/), n'essayez surtout pas de la reproduire chez vous.

## 8 Strategies for Reducing Latency

![](https://storage.mlcdn.com/account_image/325165/zpSj2EIqMq7ATnfxVwRWGTDQxOEFS3WLCuo1vTtW.png)

Merci à Matthieu D. qui nous partage un article rédigé par les coyotes de chez System Design Codex et qui nous propose quelques bonnes pratiques pour diminuer la latence dans nos environnements. On y parle de l'optimisation des requêtes de base de données, de l'utilisation de caches, de la mise en œuvre de CDNs et d'un tas d'autres trucs que vous devez connaître et mettre en pratique.  

[Accéder au lien ->](https://newsletter.systemdesigncodex.com/p/8-strategies-for-reducing-latency)