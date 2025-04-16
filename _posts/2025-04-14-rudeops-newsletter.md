---
layout: post
title: Newsletter du 14 Avril 2025
tags: [devops, Gitlab, Github, MTTR, DevSecOps]
comments: true
mathjax: true
author: RudeOps
---
La semaine dernière, j’ai vu passer une énième présentation "stratégique" d’un grand groupe sur leur transformation DevOps. Slides léchées, acronymes DevSecWhatever en gras, un schéma en entonnoir pour faire sérieux, et au milieu : zéro trace de réalité opérationnelle. Pas une ligne sur la dette technique. Pas un mot sur les réveils à 3h du mat. Rien sur les 500 tickets Jira non traités parce que personne ne veut toucher à ce microservice zombie.

Le DevOps, le vrai, c’est pas un framework qu’on installe par-dessus des processus foireux. C’est du cambouis, du refacto ingrat, des prises de risque, et parfois des alertes Slack à des heures pas cools. Et surtout, c’est une discipline qui se construit dans la friction, entre équipes, entre métiers, entre couches techniques.

On veut de la résilience ? Alors parlons vrais incidents. Parlons postmortems sans bullshit. Parlons choix techniques pas glamour mais stables. La modernité n’est pas dans les outils qu’on empile, mais dans la lucidité avec laquelle on accepte que nos systèmes sont fragiles, et qu’on les rend un peu moins pires chaque jour.  

Cyril  

### Quoi de neuf ?

🦊 **Gitlab vs Github, key differences in 2025 :** On a pas le même maillot, mais on fait partie de la même équipe. Ou alors c'est l'inverse je sais jamais. Bref, on vous conseille de lire ce chouette article des cowboys de chez Spacelift qui résume fort bien les choses parce qu'à la fin, [ce n’est pas tant une histoire de fonctionnalités qu’un choix de culture](https://spacelift.io/blog/gitlab-vs-github) : modularité ouverte contre intégration verticale, frugalité artisanale contre gouvernance centralisée, c'est vous qui voyez.

👨🏻‍💻 **RedTeam-Tools:** Ce repo est une véritable mine d'or si vous aimez casser des choses. Il regroupe [plus de 130 outils et ressources](https://github.com/A-poc/RedTeam-Tools) couvrant l'ensemble du spectre des opérations de red teaming, de la reco initiale à l'impact final.

🚀 **DnsDiag :** C'est une excellente boîte à outils en ligne de commande pour [auditer, diagnostiquer et mesurer les performances de vos serveurs DNS](https://github.com/farrokhi/dnsdiag). DnsDiag vous permettra donc de tester la latence (dnsping), de tracer le chemin des requêtes DNS (dnstraceroute) et de comparer la fiabilité de plusieurs résolveurs (dnseval). Idéal pour détecter les détournements, les lenteurs ou les anomalies dans vos résolutions DNS, parce que c'est toujours la faute du DNS.

🏃‍♂️ **MTTR is (still) lying you :** Plutôt que de continuer à empiler des chiffres creux, mieux vaut les utiliser comme point d’entrée vers ce qui compte vraiment : les enseignements qualitatifs, les signaux faibles, les frictions organisationnelles... Ce n’est pas une question de data, c’est une question de discernement, et c'est justement ce que met en valeur cet [excellent article des intellos de chez Resilience in Software Foundation](https://resilienceinsoftware.org/news/1157532).

🐧 **Garuda Linux might be the best looking desktop OS on the market:** On vient de découvrir Garuda, [une énième distribution basée sur Arch](https://thenewstack.io/garuda-linux-might-be-the-best-looking-desktop-os-on-the-market/), et qui se distingue par son esthétique soignée et ses performances optimisées d'après les retours de la communauté d'allumés habituels. On a pas testé car on préfère rester sur Slackware, la distribution des vrais bonhommes comme on dit à Montargis. Jetez quand même un coup d'oeil si KDE Plasma et Arch ne vous rebutent pas.

🥇 **DevOps vs DevSecOps, key differences and best fit :** Le DevOps a révolutionné la livraison logicielle en brisant les silos entre devs et opérations, favorisant l'automatisation et la rapidité. Mais dans cette quête insensée de vitesse, [la sécurité est souvent restée en marge](https://roadmap.sh/devops/vs-devsecops), traitée comme une étape finale, voire une contrainte.​ Un bel article d'un des mecs de chez roadmap.sh qui nous explique comment le DevSecOps vient corriger cette lacune en intégrant la sécurité dès le début.

🏹 **Database sharding case study with PostgreSQL :** Une seule instance PG pour servir des millions d’utilisateurs ? Ça marche… jusqu’au jour où VACUUM ne suit plus, les indices pèsent une tonne, et chaque requête devient une roulette russe. Spoiler : [c’est arrivé chez Notion](https://newsletter.francofernando.com/p/database-sharding-case-study-postgresql). Leur plan d’urgence ? Du vrai sharding à l’ancienne : 480 shards logiques, 32 bases physiques, un split par workspace ID pour garder la cohérence et éviter les requêtes croisées.

</> **Git turns 20, a Q&A with Linus Torvalds :** Vingt ans après avoir créé Git, Linus Torvalds reste fidèle à lui-même : pragmatique, direct et peu impressionné par les tendances. Dans une récente interview, [il revient sur la genèse de Git](https://github.blog/open-source/git/git-turns-20-a-qa-with-linus-torvalds/), né de la nécessité de remplacer BitKeeper, et sur sa philosophie du développement logiciel, passionnant comme d'habitude.

☸️ **Even more OpenTelemetry - Kubernetes special :** On vous partage ce [chouette retour d'expérience de Nicolas Frankel](https://blog.frankel.ch/even-more-opentelemetry-kubernetes/), qui nous explique comment il a monté une stack complète de monitoring avec OpenTelemetry dans K8s, Traefik comme Ingress Controller, Jaeger, PostgreSQL, Redis, Mosquitto, le tout orchestré via Helm et isolé proprement avec vCluster. C’est le guide idéal pour apprendre à mettre en place une observabilité sérieuse dans un environnement K8s moderne, modulaire et propre.

🕸 **Trippy :** On a testé et bien aimé Trippy, un énième [outil de diagnostique réseau](https://github.com/fujiapple852/trippy) écrit en Rust, qui toune sur Mac, Linux, et Windows. C'est léger, ça se prend en main en deux secondes, c'est génial pour les premières étapes d'un diag sur une box quelconque.

## OpenTofu becomes the real deal

![](https://storage.mlcdn.com/account_image/325165/v3eToAFLmjvaHMpoXqLeDDzWxpMO3MhJNa0MWAVR.png)

Merci à Julie B, SRE en France dans une grosse boîte tech, qui nous a partagé ce chouette article au sujet de notre chouchou, Opentofu, qui aujourd’hui n’est plus un fork de protestation, mais un projet structuré, sous la bannière de la Linux Foundation avec des poids lourds comme Cloudflare dans le cockpit. Le registre tourne à plein régime, et la roadmap avance vite <3.

[Accéder au lien ->](https://www.infoworld.com/article/3852167/opentofu-becomes-the-real-deal.html)




