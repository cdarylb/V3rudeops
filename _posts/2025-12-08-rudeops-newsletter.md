---
layout: post
title: Newsletter du 08 Décembre 2025
tags: [devops, Ghostty, Alpine, RustFS, Sirius]
comments: true
mathjax: true
author: RudeOps
---


Noël arrive dans une quinzaine de jours, et comme chaque année on se demande comment douze mois ont pu disparaître aussi vite. Le monde continue de cavaler, parfois sans logique, souvent sans pause, mais ce n'est pas forcément inquiétant, c'est même plutôt rassurant de voir que malgré le bruit, notre écosystème bouge, invente, et trouve de nouvelles façons de faire mieux que la veille.

C'est un peu ce que montre cette newsletter : un paysage qui évolue en continu, avec des idées, des outils, des modèles qui émergent, disparaissent, reviennent différemment. Rien de linéaire, mais beaucoup d’élan, et tant mieux, c'est ce qui garde nos métiers vivants.

Bref, Noël approche, le monde tourne vite, et nous, on continue d’avancer, un œil sur ce qui change, l'autre sur ce qui vaut encore la peine d’être construit.

Cyril

### Quoi de neuf ?

**👻 Ghostty is now non-profit :** Ghostty, le terminal des gens de bon goût, devient non-profit, et quelque part on sent le parfum d'une époque où l'open source essayait encore d'être un bien commun plutôt qu'un produit d'appel pour un futur rachat.  [Mitchell Hashimoto explique la manœuvre avec gravité](https://mitchellh.com/writing/ghostty-non-profit)  : fiscal sponsorship, transparence totale, impossibilité légale de détourner la mission ou la caisse, et surtout la promesse qu’on ne verra jamais "Ghostty Enterprise Platinum Edition" s'inviter dans nos vies. L'idée est presque touchante : bâtir un terminal moderne qui ne pourra pas se faire capturer par un fonds d'investissement ou finir empaqueté dans un abonnement mensuel, un logiciel qui restera un outil, pas un produit bref, une exception dans un monde où tant de projets libres vieillissent mal, se vendent, mutent, se referment.

🎁 **Advent of sysadmin 2025 :** Un chouette calendrier de l'Avent pour ceux qui préfèrent les logs aux chocolats :  [12 défis Linux/DevOps](https://sadservers.com/advent)  à relever, un par jour du 1er au 12 décembre. Le principe : un scénario réaliste, une machine cassée, 15 minutes pour comprendre, réparer, valider. Le but ? S'entraîner, se muscler techniquement et redécouvrir chaque matin que travailler dans l'informatique c'est une punition consentie.

**🛠️ Domain Locker :** C'est l'outil pour tous ceux qui gèrent un portefeuille de noms de domaine comme je collectionne les mugs : sans méthode, sans souvenir précis, et avec un sentiment diffus de culpabilité. L'idée : vous centralisez  [vos domaines au même endroit](https://github.com/lissy93/domain-locker), Domain Locker fait l'analyse, récupère tout ce qui va avec (DNS, SSL, IPs, sous-domaines, registrar, santé du site, performances…) et surveille tout ça en continu. Simple basique et utile.

☸️ **How to troubleshoot common Kubernetes errors :** Les cowboys de chez Spacelift ont partagé leur guide de "troubleshooting Kubernetes", et comme d'habitude avec ce genre de texte, on oscille entre thérapie de groupe et manuel de survie. L'idée de base est simple : Kubernetes, c'est formidable tant que ça marche, et dès que ça casse, on se retrouve à courir après des Pods en Pending, des Nodes NotReady, des CrashLoopBackOff et des images qui refusent de se laisser puller, tout ça dans un système distribué où absolument tout peut être coupable. Le guide déroule donc  [la méthode idéale du bon petit pompier K8s](https://spacelift.io/blog/kubernetes-troubleshooting)  : identifier, collecter, mitiger, vérifier, pérenniser et documenter, des probes aux events, des exit codes aux port-forward, jusqu'aux assistants "AI-powered" censés vous expliquer en mots doux pourquoi votre cluster brûle.

😱 **What's actually keeping CISOs up at night :** Un article sympa qui nous vient des paranos de chez Security Boulevard, et qui résume assez bien  [pourquoi les CISOs dorment avec un œil ouvert](https://securityboulevard.com/2025/12/sleepless-in-security-whats-actually-keeping-cisos-up-at-night/)  : ce ne sont pas les IA maléfiques ni les hackers quantiques qui les réveillent en sueur, mais deux fléaux autrement plus ordinaires et infiniment plus humiliants, genre les basics qu’on ne fait toujours pas, et le gigantesque tas de Lego open source sur lequel repose toute l’informatique moderne. D’un côté, les fondamentaux : MFA pas déployée partout, IAM en roue libre, segmentation optionnelle… Bref, les mêmes causes, les mêmes conséquences, et les mêmes attaques qui passent parce que personne n'a le courage de s'occuper des 85 % de risques pas sexy mais catastrophiques. De l'autre, le risque existentiel : un écosystème logiciel tellement interconnecté qu'un mainteneur fatigué, un package abandonné ou une librairie générée par une IA que personne ne comprend suffit à faire trembler des milliers de systèmes.

**🐧 Alpine 3.23.0 released :** Une news qui me permet de faire de la pige facile avec Alpine Linux 3.23.0 qui est sorti. Pas de drame, pas de polémique, juste une distro qui  [aligne les mises à jour comme si c’était un concours](https://alpinelinux.org/posts/Alpine-3.23.0-released.html)  : kernel 6.18, GCC 15, LLVM 21, Node 24, Rust 1.91, Docker 29, PostgreSQL 18, GNOME 49, KDE 6.5 et tout le reste du zoo habituel.


**🔥 Rustfs :** Une petite douceur pour les amateurs de stockage qui sentent bon la rouille avec RustFS,  [un objet store distribué façon S3](https://github.com/rustfs/rustfs), mais écrit en Rust donc théoriquement rapide, fiable, et moins susceptible de vous exploser au visage qu'un MinIO sous AGPL un lundi matin avec les perfs de Rust, la simplicité d'administration, une licence Apache 2.0 qui ne vous colle pas un avocat dans les pattes, et une compatibilité S3 complète pour ne pas casser vos outils. Le tout pensé pour les data lakes, l'IA, le big data, et toutes les autres raisons "stratégiques" d’acheter plus de disques que nécessaire. Fonctionnellement, l'essentiel est déjà là : uploads, versioning, bitrot protection, notifications, Helm charts. La réplication, le lifecycle et le mode distribué sont encore en chantier, mais ça avance.

🔎 **Sirius Scan :** Pour ceux qui aiment scanner des vulnérabilités plus vite que leur SI ne les produit,  [Sirius est sorti en v0.4.0](https://github.com/SiriusScan/Sirius), et c'est toujours un joli mélange open source entre scanner de sécu, pentest automatisé et tableau de bord qui ressemble à un cockpit d’ISS sous stéroïdes. La nouveauté majeure de cette version tourne autour de l'observabilité. Santé temps réel, logs centralisés, métriques de perf, tableau de bord système… bref, tout ce qu'il faut pour suivre votre cluster pendant qu'il tente héroïquement de résister aux scans que vous lui infligez, plus quelques bonus : builds plus propres, meilleure gestion d’erreurs, SSH moins capricieux, et des tests auto pour éviter les surprises.

🥇 **HoneyQuest :** Pour ceux qui veulent tester leur skills de hacker sans finir au tribunal, Honeyquest propose un jeu où le but est simple : repérer des failles dans des scénarios web réalistes… sauf que certaines sont de faux indices plantés juste pour vous faire passer pour un touriste. On vous montre une requête, une page, un comportement étrange, et à vous de dire ce que vous feriez en vrai, l'objectif n'étant pas de gagner de l'XP, mais d’[observer ce qui attire l’œil des attaquants](https://honeyquest.cns.research.dynatracelabs.com/), ce qu'ils ignorent, et comment ils se font avoir par des pièges grossiers ou subtilement tordus. Honeyquest sert surtout à comprendre quels types de vulnérabilités déclenchent les réflexes des humains et lesquels ne piègent plus que les bots enthousiastes et reste un excellent moyen de mesurer votre paranoïa opérationnelle.

🐋 **Why I like using Docker Compose in production :** Nick Janetakis nous partage son point de vue sur  [Docker Compose en production](https://nickjanetakis.com/blog/why-i-like-using-docker-compose-in-production)  et pour lui, ce n’est ni un aveu de faiblesse ni une hérésie technique, juste du bon sens. Dix ans qu'il déploie ainsi la majorité de ses apps, et ça tourne, ça encaisse, ça facture. Son message, quelque part, c'est que tout le vernis "Compose c'est pour le dev / Kubernetes c'est pour les adultes" relève plus du folklore que du pragmatisme. Si votre app tient sur une machine à 20 balles et répond en moins de 150 ms, à quoi bon monter une cathédrale en YAML pour impressionner LinkedIn ? Compose n'est peut-être pas sexy, mais il est fidèle, prévisible, et ne vous réveille pas la nuit pour un nœud coincé en NotReady.


## Expose localhost to the internet

![](https://storage.mlcdn.com/account_image/325165/8bZ5Iq4Yu86h0OhkYs6OG3Jb8aZW1XHjIasEniyD.png)

  

Merci à Jean-Pierre pour le courrier des lecteurs : après les VPN compliqués, les tunnels bricolés et les ngrok-de-travail, voici tunnl.gg, un service de reverse tunneling qui fait une promesse simple :  _exposer ton serveur local sur Internet avec une seule commande SSH_, sans installer quoi que ce soit.

Le principe ? Un petit  `-R 80:localhost:8080`  qui dit au serveur distant tout ce qui arrive sur ton port 80, tu me le renvoies à la maison, merci bien. Tu remplaces 8080 par ce que tu veux, tu pointes sur  `proxy.tunnl.gg`, et hop, ton app React, ton Flask en dev ou ton bricolage obscur deviennent miraculeusement consultables depuis l’extérieur.

[Accéder au lien ->](https://tunnl.gg/#/)