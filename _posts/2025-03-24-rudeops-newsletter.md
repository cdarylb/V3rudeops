---
layout: post
title: Newsletter du 24 Mars 2025
tags: [devops, Linux, Git, K8s, Gitops]
comments: true
mathjax: true
author: RudeOps
---

Le printemps, c’est peut-être le moment idéal pour faire ce qu’on repousse depuis des mois : un peu de jardinage dans les playbooks, du désherbage dans les pipelines, remettre un peu d’air dans l’infra, et surtout, redonner du sens à nos outils. Faire respirer nos stacks. Repenser nos choix.

Pas besoin de tout jeter. On taille, on arrose, on documente. On refait passer la lumière.  

Bon printemps à tous, et bonne lecture de la 38ème édition de notre newsletter.  

Cyril  

### Quoi de neuf ?

**</> How core git developers configure Git :** C'est lors d'un échange à travers une obscure liste de diffusion qu'un core dev de Git, certainement complètement ivre, a lancé un défi :  [supprimer toutes leurs configurations et alias personnalisés pour tester Git en mode vanilla](https://blog.gitbutler.com/how-git-core-devs-configure-git/). L'idée ? Identifier les confs que même les core devs trouvent indispensables. Résultat : une liste resserrée de 9 paramètres et 3 alias, sur laquelle les principaux développeurs de Git sont à peu près tous tombés d’accord, beaucoup pensant même que ces réglages devraient devenir les nouvelles valeurs par défaut de Git. In Vino Veritas...

💝 **No longer my favorite git commit :** On continue avec Git... Il y a six ans, David Thompson partageait son "commit Git préféré", une anecdote sur  [un message de commit exceptionnellement détaillé](https://mtlynch.io/no-longer-my-favorite-git-commit/)  écrit par un collègue. Ce message, long de six paragraphes et comportant cinq extraits de code, expliquait minutieusement la correction d'un simple caractère d'espacement. Ces gens ont beaucoup trop de temps libre, mais ça reste passionnant (et hilarant) à lire.

**☸️ Kubernetes tool, kubectl :** On vous partage cette très jolie série d'articles qui nous propose une  [introduction pratique à K8s](https://rnemet.dev/posts/practical_k8s/k8s_intro_local_and_kubectl/), en se concentrant sur l'installation d'un environnement local à l'aide de Rancher Desktop et sur l'utilisation de kubectl, l'outil forgé dans les entrailles de la Montagne du Destin pour les amener tous et dans les ténèbres les lier. C'est une très bonne base de départ pour s'initier à Kubernetes ou conquérir la Terre du Milieu, c'est vous qui voyez.

😱 **15 Gitops best practices to improve your workflows :** On a comme d'habitude bien aimé ce papier des cowboys de chez Spacelift, qui revient sur  [ce qu'est le Gitops et comment l'implémenter](https://spacelift.io/blog/gitops-best-practices)  à travers différentes approches.

🐧 **My 2025 stack, a modern and optimized setup :** Le post d'un énième linuxien qui nous partage sa transition vers un système "adapté à ses besoins" (notez les guillemets). Le mec a opté pour un dual boot entre Windows 11 et EndeavourOS (une distribution d'extrémistes basée sur Arch Linux), et utilise Hyprland comme tous les radicalisés. A parcourir pour les  [quelques outils essentiels à tout desktop sous Linux](https://medium.com/@a-lebailly/my-2025-stack-a-modern-and-optimized-setup-06533ba67bc9)  que vous ne connaissez peut-être pas et qu'il liste.  

🚀  **Netop :** Un chouette outil qui tourne dans un terminal et qui permet de  [surveiller le trafic réseau en temps réel](https://github.com/ZingerLittleBee/netop)  en utilisant des filtres BPF (Berkeley Packet Filter). Développé en Rust (salut Jojo), on retrouve la possibilité de définir des règles de filtrage personnalisées, de basculer facilement entre plusieurs règles et d'afficher les taux de transfert en temps réel ainsi que le trafic total.

**💻 Sniffnet :** Un  [autre outil de monitoring réseau](https://github.com/GyulyVGC/sniffnet)  qu'on aime particulièrement, écrit en Rust une fois de plus (coucou Jojo), avec une interface graphique sexy (merci à egui), et qui te permet de visualiser en temps réel le trafic entrant et sortant sur ton interface réseau, filtré par protocole, port, IP ou même localisation géographique. Elle est pas belle la vie ?

🏆  **Writeups Noobops :** Un  [site français bien carré](https://writeup.noobops.fr/) comme on dit à Montargis, et dont l'auteur nous partage sa passion du CTF à travers différents writeups (c'est le terme à la mode pour dire comptes-rendus). Idéal pour bosser sa cybersec, tous les exemples sont supers clairs, avec différents niveaux de complexité, on apprécie particulièrement les explications aussi synthétiques que pertinentes.


## Finding my first SQL injection on HackerOne

![](https://storage.mlcdn.com/account_image/325165/YoBtJ253h6ad1AUIV9hdzJb08UMD1uOr1cfqlsWg.png)

Merci à Romain V. pour son post qui nous partage un retour d'expérience de la découverte d'une vulnérabilité d'injection SQL sur une plateforme d'agendas en ligne. En analysant les requêtes backend entre le site principal et son serveur de contenu, le mec a identifié que le paramètre "tag" était vulnérable à une injection SQL basée sur le temps. Très chouette à lire comme d'habitude, merci Romain pour le partage !  

[Accéder au lien ->](https://infosecwriteups.com/finding-my-first-sql-injection-on-hackerone-6a031ab5aa1c)