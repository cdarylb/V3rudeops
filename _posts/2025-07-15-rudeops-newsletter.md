---
layout: post
title: Newsletter du 15 Juillet 2025
tags: [devops, Chiko, Somo, Docker, CI/CD]
comments: true
mathjax: true
author: RudeOps
---


Vous la sentez, cette odeur de tickets qu’on ne fermera pas avant septembre ? Nous aussi. Et c’est pas qu’on vous aime pas, c’est juste qu’on a mieux à faire (bronzer, râler sur le wifi du camping, oublier son badge d’astreinte...).

Donc cette semaine, on fait court, très court, le strict nécessaire balancé sans fioritures entre deux tentatives pour faire croire qu’on bosse encore un peu.

On reviendra en septembre, reposés, motivés, et avec une todo pleine de side-projects qu'on ne finira jamais.

Bonnes vacances à ceux qui partent, avec une pensée particulière pour ceux qui restent.  
  
Cyril

### Quoi de neuf ?

😱 **Serving 200 million requests per day with a cgi-bin :** Un mec a servi 200 millions de requêtes avec… du CGI. Oui,  [ce truc des années 90](https://jacob.gold/posts/serving-200-million-requests-with-cgi-bin/). Pas de conteneurs, pas de microservices, juste du bon vieux binaire qui répond direct, comme quoi, quand c’est bien fait, même les technos considérées comme mortes peuvent humilier des stacks modernes entières. Je cherche une nounou pour le chat pendant mes vacances faire offre par email.

🐋 **Dockman :** Une énième interface graphique pour Docker qui fait le job sans en faire des caisses. C’est écrit en Go,  [ça tourne sous Linux](https://github.com/RA341/dockman), et ça dépanne bien quand on veut voir ses conteneurs sans lancer une guerre dans le terminal. Pas révolutionnaire, mais propre, utile, et open source.

💝 **Chiko :** Un chouette  [client gRPC en mode terminal](https://github.com/felangga/chiko). Pas de clics, pas d'interface web qui rame, juste un CLI propre pour interagir avec des services gRPC. Mais où est mon bon dieu de maillot de bain ?

🥇 **Somo :** Somo c’est  [netstat mais en version lisible](https://github.com/theopfr/somo). Un TUI en Rust pour voir en temps réel ce qui écoute, ce qui cause, et ce qui squatte tes ports, juste l’essentiel pour comprendre pourquoi encore une fois ton app refuse de binder le 8080.  

🏹 **Using ArgoCD to deploy to multiple clusters :** Un tips pratique pour déployer sur plusieurs clusters  [avec ArgoCD et ApplicationSet](https://itnext.io/using-applicationset-to-deploy-to-multiple-clusters-28f6879be217). Rien de magique, juste un YAML bien structuré qui évite de copier-coller ton déploiement dans trois répertoires différents. Penser à réserver un restaurant à Bonifacio.

🚀  **How Discord stores trillions of messages with high performance :** Un chouette article dans lequel on apprend comment  [le talkie-walkie de SF stocke des trillions de messages](https://blog.bytebytego.com/p/how-discord-stores-trillions-of-messages)  sans base de données "next-gen", sans event mesh distribué, et sans cluster Kubernetes qui se prend pour un datacenter. Juste du sharding, du Postgres solide, du cache, et une équipe qui préfère que ça marche plutôt que d’en parler dans une conf.

🏃‍♂️ **CI/CD observability with Opentelemetry :** Un excellent guide pour brancher OpenTelemetry sur ta CI/CD et enfin comprendre pourquoi ton pipeline passe plus de temps à  ["préparer l’environnement"](https://signoz.io/blog/cicd-observability-with-opentelemetry/)  qu’à déployer ton app. C’est bien foutu, ça demande un peu de tuyauterie, mais au moins tu pourras dire “latence observée” au lieu de “ça rame, je sais pas pourquoi”.

🤖 **Monitoring my homelab, simply :** Un retour d’expérience sur du monitoring de homelab simple,  [sans Prometheus qui mange 2 Go de RAM](https://b.tuxes.uk/simple-homelab-monitoring.html)  juste pour surveiller ton frigo. Des outils légers, lisibles, qui font le taf sans tableau de bord interactif en WebGL. C’est minimaliste, clair, et ça rappelle qu’on peut monitorer proprement sans monter un cluster pour trois services qui tournent dans un coin. Il faut vraiment un passeport pour aller à Djerba ??

🎯 **CI/CD input, secured and prefered method to pass parameters to a pipeline :** Les cowboys de chez GitLab introduisent enfin des "CI/CD inputs" pour passer des paramètres aux pipelines de façon plus propre et sécurisée.  [Finies les variables d’environnement détournées](https://about.gitlab.com/blog/ci-cd-inputs-secure-and-preferred-method-to-pass-parameters-to-a-pipeline/)  ou les hacks en cascade. C’est clair, structuré, et ça tombe bien parce qu'on préfère laisser un YAML propre que des tickets ouverts en partant en congés.  

🔳 **Tattoy :** On a découvert Tattoy, un compositeur visuel pour terminal, qui intercepte l’affichage du shell pour y  [superposer des effets visuels](https://tattoy.sh/)  comme des shaders GPU, une mini-carte du scrollback, ou encore un deuxième terminal en arrière-plan. C’est configurable en JSON, compatible avec ShaderToy, et c'est clairement le genre d’outil qu’on installe "pour voir", puis qu’on garde parce que c’est aussi inutile que joli.

## Build your own private cloud at home with Docker

![](https://storage.mlcdn.com/account_image/325165/J4xOFekPrFjBLSlt8PILzrM5OlUoL1enAYDY59Gv.png)

Merci à Fabrice pour le lien, et pour nous rappeler qu’on peut toujours faire compliqué… chez soi.

L’article des outlaws de chez The New Stack nous explique comment monter son propre "cloud privé" à la maison avec Docker. Traduction : tu vas empiler des conteneurs (Traefik, Portainer, Nextcloud, etc.) sur un vieux PC pour retrouver à peu près les mêmes galères qu’en prod, mais avec le chauffage gratuit en prime. C’est bien fichu, plutôt accessible, et parfait pour ceux qui veulent un labo maison (c'est à la mode) avec une touche DevOps sans passer par AWS pour héberger trois fichiers et un carnet de recettes.

[Accéder au lien ->](https://thenewstack.io/build-your-own-private-cloud-at-home-with-docker/)