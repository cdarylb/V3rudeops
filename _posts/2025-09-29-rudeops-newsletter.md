---
layout: post
title: Newsletter du 29 Septembre 2025
tags: [devops, Kali, Harborguard, Docker]
comments: true
mathjax: true
author: RudeOps
---

On ne sait plus très bien à quel moment on a commencé à écrire des newsletters DevOps sur fond de jazz free et de bières tièdes, mais ce mois-ci, quelque chose a définitivement basculé. Était-ce le froid ? Les projets absurdes aux noms encore plus absurdes ? Le moment où l’on a découvert que “sudo” allait être remplacé par “sudo-rs” et qu’on a ri, un peu trop fort, avant de pleurer dans un coin de l'open space ? Peut-être.

Toujours est-il qu’on continue, parce qu’on croit encore, quelque part, au pouvoir de la veille technique, même noyée sous des PowerPoint multicolores, des VPN qui tombent et des managers qui disent “agilité” comme on dit “synergie”. Et puis, entre deux failles critiques et trois outils en “.sh”, il y a parfois une étincelle : un projet open source qui ne demande rien, un script crado qui sauve la prod, un RSS qui vous fait sourire.

Alors oui, on parle ici de trucs obscurs avec un sérieux très relatif, mais si ça peut vous éviter un apt remove regrettable, un git push --force honteux ou simplement vous faire vous sentir moins seul dans la jungle de YAML, alors ça valait le coup.  

Bonne lecture, camarades.

Cyril

PS : Merci Coni pour le titre de la newsletter.

### Quoi de neuf ?

🏃‍♂️  **Kali Linux 2025.3 release :** [La nouvelle update de Kali Linux est là](https://www.kali.org/blog/kali-linux-2025-3-release/), et comme d’habitude, elle arrive en sifflotant avec son sac à outils encore plus affûtés. Au menu : une meilleure intégration du support Nexmon, le framework qui permet d’exploiter les puces Broadcom pour faire du Wi-Fi un terrain de jeu offensif, de nouveaux templates Vagrant et Packer histoire de déployer des VM Kali comme on jette des sorts dans Baldur’s Gate, et, pour les archéologues du binaire, la fin du support ARMel, parce que sa place est dans un musée. Enfin, comme toujours, une fournée de nouveaux outils, dont certains à prononcer uniquement après s’être hydraté correctement : blex, ipsvd, sniffglue... Autant de noms qui sentent bon le terminal brûlé et les ports scannés.

🚀  **7 obsolete security practices that should be terminated immediatly :** Sept pratiques de sécurité obsolètes, qu’on continue pourtant à voir dans la nature, comme des serveurs FTP en prod : le périmètre réseau considéré comme une barrière magique, la sécurité dictée par la conformité (au lieu du bon sens), les VPNs qui datent de Napster, une confiance aveugle dans l’EDR, l’authentification par SMS (coucou les attaques SIM swap), les SIEMs on-prem trop chers pour ingérer tous les logs… et des utilisateurs encore vus comme un problème plutôt qu’une force. Chaque point de l’article rappelle une évidence :  [le monde a changé, mais pas toujours les pratiques](https://www.csoonline.com/article/4022848/7-obsolete-security-practices-that-should-be-terminated-immediately.html).

💝 **How container filesystems works :** Dans le petit monde des conteneurs, on passe beaucoup de temps à empiler des images, tirer des layers, binder des volumes… mais rarement à se demander comment tout ça tient debout. C’est là qu’intervient  [ce super tuto de iximiuz labs](https://labs.iximiuz.com/tutorials/container-filesystem-from-scratch), qui t’embarque dans une exploration du système de fichiers d’un conteneur, depuis zéro. Pas d’images Docker prédigérées ici, mais du unshare, du chroot, du montage à la main, et une lente remontée à la surface de ce qui fait la magie (et parfois le cauchemar) de l’isolation Linux. C’est clair, progressif, presque ludique à condition d’aimer souffrir un peu pour comprendre ce qui se passe vraiment sous les couches d’overlay.

🥇  **Harborguard, a modern image vulnerability scanning :** La sécurité des conteneurs, c’est un peu comme trier tes mails ou ranger tes photos de vacances : tout le monde sait qu’il faut le faire, mais personne n’a envie d’y passer la journée. HarborGuard, lui, t’évite le grand nettoyage à la main. Cette appli web moderne te propose  [une interface unique pour piloter un bataillon d’outils de scan bien connus](https://github.com/HarborGuard/HarborGuard)  (Trivy, Grype, Syft, Dockle, OSV Scanner, Dive…), le tout avec des tableaux interactifs et des graphes qui ne piquent pas les yeux. Tu veux visualiser tes vulnérabilités par couche Docker, explorer ton filesystem, suivre les CVE critiques ou exporter des rapports JSON bien propres ? C’est prévu, et même les API sont là pour brancher tout ça dans ton pipeline.

🐋 **Docker multistage builds, how to optimize your images :** Faire un docker build sans étape intermédiaire, c’est comme souder ton meuble IKEA directement dans le salon : ça tient, mais t’as scié les pieds de la table et la moitié des vis traîne encore sur le tapis. Heureusement, les builds multistage sont là. Le billet des cowboys de chez Spacelift t’explique  [comment construire une image propre](https://spacelift.io/blog/docker-multistage-builds), légère, et sans tout embarquer dedans. Une méthode simple pour que ton conteneur n’emporte pas toute la chaîne de toolchains avec lui, et que docker image ls ne ressemble plus à un listing de partitions Windows 98.

🏹 **Sudo vs sudo-rs, what you need to know :** Ubuntu 25.10 s'apprête à enterrer un monument : la commande sudo telle qu’on la connaît va être remplacée par sudo-rs,  [une réécriture complète en Rust](https://itsfoss.com/sudo-vs-sudo-rs/). Officiellement pour des raisons de sécurité mémoire, de modernisation du code, et d’attrait pour les jeunes développeurs (ceux qui ont peur du C et des pointeurs comme des légumes à la cantine). Dans les faits, pour 99 % des utilisateurs, rien ne change. Vous taperez toujours sudo apt install sans voir la différence, si ce n’est un message d’erreur formulé différemment quand vous tapez n’importe quoi. Mais pour les admins qui aiment farfouiller dans les confs exotiques, attention, adieu certaines fonctionnalités (wildcards, sendmail, configurations non-PAM…), et bonjour les surprises. Bonne nouvelle, l’ancien sudo reste dispo sous le nom sudo-ws, pour les nostalgiques, ou ceux qui gèrent des infrastructures en équilibre sur une pile de scripts hérités de 2011.

**👾 The DevSecOps path :** [On t’a vendu le DevSecOps comme un chemin pavé d’or](https://devops.com/the-devsecops-career-path-what-no-one-tells-you-about-getting-started/), de pipelines sécurisés et de cafés en grain dans l’open-space du bonheur. En vrai, c’est surtout un poste où tu dois convaincre des Devs d’écrire moins de failles, des Ops de ne pas tout exposer sur le net, et des RSSI que "non, ce n’est pas encore audité mais promis, ça va venir". Le billet des punks de chez DevOps.com revient sur ce qu’on oublie souvent de dire : la solitude du poste fourre-tout, la jungle des outils, et la nécessité de savoir parler trois dialectes (dev, sec et ops) tout en gardant le sourire. Tu voulais faire de la sécu, tu finis par gérer des tickets Jira.

[🏗️](https://noted.lol/komodo/) **Komodo, manage docker images & containers :** Comme le disait le regretté Terry Pratchett, "_l__es sorciers n'aiment pas l'inconnu, à moins d'être sûrs de pouvoir le maîtriser à coups de parchemins, de glyphes et de runes dans le bon ordre",_ et c’est un peu la même chose avec nos serveurs.  [Komodo propose de remettre un peu d’ordre dans tout ça](https://noted.lol/komodo/)  : monitoring, gestion des conteneurs, déploiement de stacks Docker, gestion centralisée des secrets, automatisations planifiables, interface claire, API documentée, audit complet. Pas de version pro, pas de limites arbitraires, pas de pièges, mais juste un outil pensé pour reprendre le contrôle sans avoir à inventer une nouvelle CLI tous les matins.

🛡️ **Doxx.net, advanced VPN, parallel internet and delocation platform :** Doxx.net,  [c’est un peu comme un VPN sous stéroïdes](https://github.com/doxx/doxx.net), mais sans les pubs YouTube criardes qui promettent l’anonymat en échange de 3,99 € par mois. On y entre comme dans un VPN classique via WireGuard, HTTPS, TCP ou même HTTPS-over-CDN pour les environnements les plus hostiles, mais c’est à l’intérieur que la magie opère. Une fois connecté, vous basculez dans un réseau maillé chiffré maison, avec ses propres domaines en .doxx, sa topologie fermée, et son ambition de devenir un Internet parallèle où vos appels Signal, vos accès serveurs et vos services web restent bien à l’abri, loin des regards indiscrets et des trackers curieux. Le concept : sortir le moins possible sur l’Internet public, et tout faire à l’intérieur. Moins de fuites, moins de failles, moins de stress. À croire que c’est ce que le VPN aurait dû être depuis le début.  

🔑 **Lazyssh**, Lazyssh, c’est le chaînon manquant entre votre ~/.ssh/config et votre mémoire défaillante. [Tout se fait depuis une interface terminal](https://github.com/Adembc/lazyssh)  propre, rapide et un peu magique façon lazydocker ou k9s mais pour vos connexions SSH. On y retrouve toutes les fonctions utiles : fuzzy search, édition des entrées, ping des serveurs, tags personnalisés, et bientôt le transfert de fichiers sans s’arracher les cheveux. Et le tout en lisant (et respectant religieusement) votre ~/.ssh/config, sans jamais stocker de clés ou faire n’importe quoi avec vos permissions.

## Modèle Zero Trust, les fondamentaux - ANSSI

![](https://storage.mlcdn.com/account_image/325165/mzwVBTkeeM4rJiQcIIFlbpl4Q1qQs18NqjobUwDx.png)

  

Aujourd’hui, un grand merci à Sandrine R. pour ce partage sérieux comme un café sans sucre : un rappel salutaire sur le modèle Zero Trust, ce mot à la mode qu’on balance dans les PowerPoint sans toujours savoir ce qu’il implique.

Face au BYOD, au télétravail généralisé et aux connexions dans tous les sens (cloud, on-prem, via VPN ou avec un bout de ficelle), les solutions estampillées "Zero Trust" promettent de remplacer la bonne vieille sécurité périmétrique. Sauf que, comme le rappelle justement l’ANSSI dans son avis, l’un ne remplace pas l’autre : ils sont complémentaires. Pas de "tout Zero Trust" ou de "VPN c’est mort", mais plutôt une approche progressive, qui consiste à cesser d’accorder une confiance implicite à tout ce qui passe la porte du réseau.

Bref, Zero Trust n’est pas un produit miracle, mais un modèle de pensée, et on vous encourage très fort à lire le document de l’ANSSI mis à jour cet été, surtout si vous prévoyez de glisser le mot dans votre prochaine roadmap sécurité.

[Accéder au lien ->](https://cyber.gouv.fr/publications/zero-trust)