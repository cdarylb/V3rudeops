---
layout: post
title: Newsletter du 03 Juin 2024
subtitle: Petit ICQ parti trop tard	
thumbnail-img: /assets/img/jonglage.png
gh-repo: daattali/beautiful-jekyll
tags: [devops, DNS, K8s, Linux, Docker, Podman, Memcache]
comments: true
mathjax: true
author: RudeOps
---


Il fait gris dans nos petits coeurs aigris, car le couperet vient de tomber.  [ICQ va rejoindre la tombe qu'il aurait déjà du trouver](https://www.theverge.com/2024/5/25/24164579/icq-shut-down-june)  il y a de nombreuses années, ce qui ne nous rajeunit pas.  
  
Cyril

### Quoi de neuf ?

🏃‍♂️  **Why use DNS ALIAS record instead of CNAME in the cloud :** Un article  [vraiment super didactique](https://adil.medium.com/why-use-dns-alias-record-instead-of-cname-in-the-cloud-ca995b7a364d)  qui vous initie au DNS Flattening. Et n'oubliez pas :  [c'est toujours la faute du DNS.](https://www.cyberciti.biz/humour/a-haiku-about-dns/)

💀 **Why Kubernetes was a mistake for my SaaS business :** Un retour d'expérience qui montre bien qu'utiliser Kubernetes en production  [n'est pas pertinent dans 90% des cas](https://sotergreco.com/why-kubernetes-was-a-mistake-for-my-saas-business).

😱 **How to destroy your OS with tar :** Attention, cette cascade a été réalisée par un professionnel,  [ne reproduisez pas ça chez vous](https://vorakl.com/articles/tar-curdir/).

🔨 **Six Linux commands I use for malware analysis :** C'est écrit par Vlad Ananin, un punk de chez  [any.run](https://any.run/), qui nous partage ses  [outils favoris pour analyser des malwares](https://itsfoss.com/linux-commands-malware-analysis/). On y croisera les incontournables gdb et file, mais aussi quelques outils plus obscurs comme  [objdump](https://stacklima.com/commande-objdump-sous-linux-avec-des-exemples/).

🏹 **Linux crisis tools :** Dans la même veine qu'au dessus, quelques outils essentiels  [d'après un vague barbu linuxien](https://www.brendangregg.com/blog//2024-03-24/linux-crisis-tools.html)  qui permettent d'intervenir rapidement en cas d'incident sur vos systèmes.  

🚀  **Docker vs Podman, a new era in secure orchestration :** Un bel article écrit à travers le prisme de la sécurité qui compare les solutions de containers Podman et Docker.  [A la fin c'est Podman qui gagne](https://levelup.gitconnected.com/docker-vs-podman-a-new-era-in-secure-orchestration-957ea2123098).

🏆  **DNS as Code :** Un chouette post qui décrit dans le détail  [la migration d'une config portée par Cloudflare à travers OpenTofu](https://dev.to/aws-builders/dns-as-code-40ic). On vous le partage parce que ça peut vous donner plein d'idées et que ça fait rudement plaisir de voir  [qu'OpenTofu](https://opentofu.org/), le fork de Terraform, commence à être utilisé.


## How Facebook served billions of requests per seconds using Memcached

![](https://storage.mlcdn.com/account_image/325165/ewE9lyksZXFUd6IsPtO2LnEsAG89mvMcj6nhos2K.png)

Aujourd'hui c'est Clément R. qui nous partage un post grave complet sur l'importance pour Facebook de relever des défis de scalabilité avec la mise en œuvre et l'optimisation de Memcache. Des décisions d'architectures globales aux optimisations spécifiques des serveurs, chaque aspect contribue à la performance, la fiabilité et l'efficacité du système, et tout ça est vraiment bien détaillé ma bonne dame.  

[Accéder au lien ->](https://blog.bytebytego.com/p/how-facebook-served-billions-of-requests)