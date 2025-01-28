---
layout: post
title: Newsletter du 09 Septembre 2024
subtitle: Prenez un chewing gum Emile			
thumbnail-img: /assets/img/chariot.png
gh-repo: daattali/beautiful-jekyll
tags: [devops, CI-CD, CORS, Incus, Curl, Helm, Docker]
comments: true
mathjax: true
author: RudeOps
---

On se rend surtout compte que passer ses applications sous licence open-source est nécessaire pour des raisons business. Dernier exemple en date, avec Elasticsearch qui s'oriente vers une licence AGPL dans les prochaines semaines, tout ça parce que le fork Opensearch (lancé par AWS) commençait à leur faire mal. Même si on aurait préféré un passage sous licence APACHE 2.0, c'est déjà ça de pris. Vous la sentez cette petite pression du fork qui pèse sur les éditeurs ? Est-ce que c'est sain ? Est-ce la solution ? Nous on a tendance à penser que oui, et que l'open-source est de toute façon essentielle pour un business pérenne.  
  
Cyril

### Quoi de neuf ?

🦊 **Introducing CI/CD Steps, a programming language for DevSecOps automation :** On était passé un peu à côté, mais les cowboys de chez Gitlab ont introduit  [un nouveau langage expérimental](https://about.gitlab.com/blog/2024/08/06/introducing-ci-cd-steps-a-programming-language-for-devsecops-automation/)  qui vise à simplifier la création de workflows en permettant la modularité et la réutilisation des jobs CI. Ça a l'air bien foutu, simple, et Gitlab précise qu'ils visent différents ajouts de fonctionnalités dans les mois qui viennent.

💀 **CORS is stupid :** [Grand CORS malade](https://kevincox.ca/2024/08/24/cors/).

🥇  **Linux containers, Incus :** Aujourd'hui on vous parle un peu de  [Incus, un projet libre de gestion de conteneurs](https://linuxcontainers.org/incus/)  encore trop méconnu. En gros c'est un fork de LXD qui propose une solution avancée de virtualisation légère, permettant de gérer des conteneurs système ou applicatifs. Pour les curieux on peut tester quelques fonctionnalités en ligne avant de faire le grand saut.

😱 **Kube-state-metrics, your complete guide to simplifying Kubernetes observability :** Kube-state-metrics est un  [add-on open-source pour K8s qui produit des métriques](https://last9.io/blog/kube-state-metrics/)  (sur vos pods, vos nodes, etc) en allant taper les APIs de votre serveur. Vous êtes grand et responsable, donc vous installez ça comme vous voulez, via Helm, des manifestes YAML, ou en construisant tout depuis les sources comme un vrai bonhomme. Et ouais, il y a bien sûr une intégration avec Prometheus. Le tuto comprend pas mal de bonnes pratiques qui vont de la configuration de permissions RBAC à l'activation de la haute dispo et l'utilisation de métriques personnalisées pour une meilleure observabilité.

👔 **CTO to CTPO, navigating the dual role in tech leadership :** L'article des punks de chez The New Stack aborde  [la transition du rôle de Chief Technology Officer (CTO) vers celui de Chief Technology and Product Officer (CTPO)](https://thenewstack.io/cto-to-ctpo-navigating-the-dual-role-in-tech-leadership/)  à travers un retour d'expérience sympa. Le post détaille les défis et les opportunités à combiner des responsabilités à la fois pour la technologie et le développement produit au sein de la direction technique.  

🚀  **Using CURL to create a telnet connection :** Parce que après tout, pourquoi pas hein.  [Ne jugeons pas](https://nickjanetakis.com/blog/using-curl-to-create-a-telnet-connection), et puis c'est écrit par notre pote Nick Janetakis alors bon, c'est de la pige facile et on ne va pas se priver.

🏆  **Finally, a viable Helm replacement :** Et c'est  [une putain de bonne nouvelle](https://itnext.io/finally-a-viable-helm-replacement-388d538f9e1f)  comme on dit à Montargis, ce post vous explique pourquoi et nous propose enfin une alternative qui a l'air viable, avec Werf qui est depuis quelques mois en version 2.0 stable. On offre une bière à celui qui nous trouve ce que signifie Werf au passage.


## Introducing Docker Build Checks : Optimise dockerfiles with best practices

![](https://storage.mlcdn.com/account_image/325165/tU1DmVmbEeJagaeS9xS6IxFoipD1OvbUG7jvwcii.png)

Merci à Nathalie D. qui nous partage un post tiré du blog de Docker et qui nous apprend la sortie de la première release de Docker Checks, une nouvelle fonctionnalité qui permet d'optimiser nos Dockerfiles en suivant les bonnes pratiques associées. Ces checks identifient et signalent les problèmes potentiels lors des builds Docker, et c'est intégré nativement dans Docker Desktop et ça, ça nous donne envie de chanter la vie !  

[Accéder au lien ->](https://www.docker.com/blog/introducing-docker-build-checks/)