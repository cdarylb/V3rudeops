---
layout: post
title: Newsletter du 04 Novembre 2024
subtitle: Donne-moi ton code baby, ton flow baby			
thumbnail-img: /assets/img/Barbara tronconeuse.png
gh-repo: daattali/beautiful-jekyll
tags: [devops, AWS, Uber, eBPF, Docker, Git, Curl]
comments: true
mathjax: true
author: RudeOps
---

Comme les décideurs et les architectes de demain, vous avez le pouvoir d’influencer la stabilité, l’innovation et même l’éthique de vos systèmes. Alors, en explorant les sujets de notre veille techno, pensez à l'impact réel de vos choix, et à cette ambition partagée de créer un monde, numérique ou non, plus robuste et plus durable.  

Cyril

### Quoi de neuf ?

**👨🏻‍🏫 Five lessons from a minor production incident :** On vous partage ce  [chouette retour d'incident](https://lucvandonkersgoed.com/2024/10/17/five-lessons-from-a-minor-production-incident-copy/) où un email quotidien AWS News n’a pas été envoyé à cause d’une surcharge de messages dans le système SQS. Le mec qui écrit ce RETEX en tire cinq leçons : investir tôt dans de l'observabilité, maintenir des tests pertinents et une infra logicielle cohérente, appliquer le principe YAGNI (You Aren't Gonna Need It), et tracer les données, la base quoi.

🚕 **How Uber reduced their log size by 99% :** Joli post dans lequel on apprend que [Uber a réduit la taille de ses journaux de logs de 99 %](https://newsletter.betterstack.com/p/how-uber-reduced-their-log-size-by) en utilisant un outil de traitement compressé de logs (CLP). En divisant le processus de compression en deux phases, Uber a d'abord encodé et compressé les logs avant de les stocker dans HDFS, puis appliqué des étapes de déduplication et d'optimisation (non fiscale cette fois), ce qui leur a permis de passer de 5,38 pétaoctets à seulement 31,4 téraoctets, prolongeant leur rétention de logs de trois jours à un mois.

**🚀 The past, present and future of eBPF and its path to revolutionizing systems :** Un article fourni qui revient  [sur les dix ans d’évolution de eBPF](https://eunomia.dev/en/blogs/ten-years/)  (Extended Berkeley Packet Filter), une technologie initialement conçue pour le filtrage de paquets réseau, qui est devenue incontournable pour la sécurité, l'observabilité et la performance des systèmes. On y explore les avancées comme XDP pour le haut débit, BTF pour la portabilité, et l’introduction de nouvelles fonctionnalités (kfuncs, bpf_arena) qui promettent d’étendre encore ses capacités pour les amener tous et dans les ténèbres les lier.

⚡ **Git branching strategies :** Un zoli [guide qui explore les stratégies](https://newsletter.techworld-with-milan.com/p/git-branching-strategies)  populaires comme le Feature Branching, GitFlow, GitHub Flow, GitLab Flow et le Trunk-Based Development (qui peut nous prendre au sérieux avec des noms pareils ?), et qui détaille les étapes de mise en œuvre, les avantages et les cas d'utilisation optimaux.

💖 **Curl source code age :** Daniel Stenberg, le papa de Curl qu'on vénère, s'ennuyait et a décidé de se transformer en archéologue et d'[explorer l'âge du code de Curl](https://daniel.haxx.se/blog/2024/10/31/curl-source-code-age/). Il a donc créé un script qui utilise Git pour déterminer la date de chaque ligne de code dans le dépôt de Curl puis a visualisé les données avec gnuplot. Ses conclusions : nous ne déchiffrons pas de cartes pour exhumer un trésor, et un X n'a jamais, jamais marqué son emplacement.  

**🐳 Awesome Compose :** Une  [liste d'exemples Docker Compose](https://github.com/docker/awesome-compose)  qui offrent un bon point de départ pour intégrer et gérer différents services sur des envs de dev.

## From YAML chaos to Kubernetes zen

![](https://storage.mlcdn.com/account_image/325165/aemQQ4esXNJm6j8Ur0fXz5FciCNIaubetglVNpu3.png)

Merci à Patrick D. qui nous fait découvrir Pepr, un outil censé simplifier la gestion de Kubernetes avec des modules TypeScript faciles à maintenir, et qui fournit des capacités de journalisation, de surveillance, tout en appliquant les bonnes pratiques de sécurité. Merci Patrick !  

[Accéder au lien ->](https://itnext.io/from-yaml-chaos-to-kubernetes-zen-5b9e8242a5cb)