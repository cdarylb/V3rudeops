---
layout: post
title: Newsletter du 30 Juin 2025
tags: [devops, Omarchy, K8s, Arsenal, Git]
comments: true
mathjax: true
author: RudeOps
---

Il y a dans l’open-source quelque chose qu’aucun contrat de licence ne pourra jamais offrir : la possibilité de choisir. De comprendre ce qu’on utilise, d’en modifier les rouages, d’en assumer les défauts autant que les forces. C’est une lente conquête, parfois silencieuse, souvent discrète, mais qui, à mesure qu’elle progresse, redessine les contours d’une souveraineté numérique trop longtemps sacrifiée sur l’autel du confort.

Le Schleswig-Holstein a ouvert la voie. Plutôt que de s’en remettre une énième fois aux GAFAM, ce Land allemand migre ses 30 000 postes vers Linux, LibreOffice, Nextcloud, Mastodon, pas pour le fun ni pour envoyer un signal, mais pour reprendre le contrôle tout simplement.

Et le Danemark lui emboîte le pas. Bruxelles n’a même pas fini de se fâcher sur les traitements de données personnelles par Microsoft 365 que Copenhague, à son tour, décide de claquer la porte. Plus question de négocier des contrats dans le brouillard, ni de stocker des données publiques dans des datacenters étrangers aux juridictions floues. Place à l’open-source, à des outils qu’on peut inspecter, adapter, sécuriser. Pas parce que c’est gratuit, mais parce que c’est maîtrisable.

C’est une voie exigeante, oui. Elle demande des moyens, des compétences, une vision à long terme, mais c’est une voie royale, celle qui fait de l’open-source non pas une rustine de geek barbu, mais un projet d’avenir sérieux, structuré et souverain.

Cyril

### Quoi de neuf ?

**☸️ What would a Kubernetes 2.0 look like :** Dix ans après ses débuts, Mat Duggan s’interroge :  [et si Kubernetes avait une version 2.0](https://matduggan.com/what-would-a-kubernetes-2-0-look-like/), à quoi ressemblerait-elle pour enfin résoudre la complexité qui nous prend à la gorge ? Il suggère plusieurs remèdes : dire adieu à YAML, remplacer etcd, imaginer un gestionnaire de packages type “KubePkg” inspiré des .deb ou .rpm, et surtout offrir une solution plus simple pour que les ops débutants ne fassent pas exploser leur cluster au premier apply.

💝 **Bighuge BLS Osint Tool (BBOT) :** BBOT, c’est le scanner open-source par excellence : tu donnes une cible (domaine, IP, URL…),  [et il va fouiller partout](https://github.com/blacklanternsecurity/bbot)  : sous-domaines, ports ouverts, certificats SSL, captures web, vulnérabilités via Nuclei… le tout avec plus de 80 modules, sans script artisanal ni phase manuelle. Au cœur de l’engin : un moteur récursif où chaque découverte nourrit les autres modules, jusqu’à saturation, pour ne rien louper dans ta surface d’attaque.

**</> Git Smart Squash :** Terry Pratchett écrivait "Les mages croient à la documentation. Ils aiment la documentation. Ils l’écrivent même parfois". Et si Git avait lu Pratchett, il t’aurait évité cette succession de commits débiles genre : "typo", "fix", "revert revert", "je sais pas ce que je fais", "ça marche enfin", "non en fait". C’est là qu’intervient Git-Smart-Squash, un outil  [qui appelle une IA à la rescousse](https://github.com/edverma/git-smart-squash)  pour te transformer ce magma en une jolie histoire cohérente et bien rangée. Tu balances ta branche, il te pond deux ou trois commits clairs, regroupés logiquement, avec des messages qui ressemblent à quelque chose. En local avec Ollama si t’es responsable, en ligne avec OpenAI si t’as la flemme. Il te montre le plan, te demande confirmation, garde un backup au cas où, et hop, tu passes pour quelqu’un de sérieux.

🐧 **Omarchy, bottling that inspiration before it spoils :** DHH (le papa de Rails), pris d’une soudaine envie de réinventer sa station de travail comme on refait sa cuisine à 3h du mat, a troqué son Ubuntu pour Arch + Hyprland. Pas parce que c’était rationnel, non : parce qu’une bouffée d’inspiration l’a frappé. Et comme souvent avec ce genre d’élan, ça s’est terminé en projet open source.  [Omarchy est donc né](https://world.hey.com/dhh/omarchy-is-out-4666dd31). Une Arch Linux préconfigurée à sa sauce, avec tiling, esthétique soignée et scripts maison. Pas un produit, pas une promesse, juste le reflet d’un moment, celui où on casse tout ce qui marche pour retrouver ce petit frisson du contrôle absolu.

🏹 **Detecting vulnerabilities in public Helm charts :** On parlait plus haut de Kubernetes 2.0, mais en attendant que cette version magique tombe du ciel on reste avec la vraie vie : des charts publics tellement troués qu’on pourrait y faire passer un tunnel VPN. Car pendant que certains rêvent d’un K8s refondu, plus simple, plus humain, d’autres balancent joyeusement des "helm install" sans lire ce qu’ils installent. Et là, c'est le drame :  [des services exposés au monde entier](https://allthingsopen.org/articles/detecting-vulnerabilities-public-helm-charts), des secrets codés en dur, des RBAC en mode open bar, et du Trivy qui hurle en CAPS LOCK. Alors oui, Kubernetes 2.0, c’est peut-être demain. Mais aujourd’hui, le seul garde-fou entre toi et un cluster transformé en hotspot pour script kiddies en reconversion, c’est toi, ton terminal et un peu de paranoïa.

🚀 **ArgoCD, a practical guide to Gitops on Kubernetes :** Un chouette guide pondu par les cowboys de chez SitePoint qui t’expliquent comment apprivoiser ArgoCD sans finir en PLS devant ton cluster. ArgoCD, c’est le collègue qui ne dort jamais, qui relit tes fichiers YAML sans râler et qui remet ton cluster en place dès qu’il s’éloigne un peu trop de ce que Git avait prévu. Fini les “ah mince j’ai patché à la main”, fini les “je crois que c’est à jour”, fini les clusters bipolaires. Branché directement à ton dépôt, il veille, compare, corrige, rollback au besoin, et te donne presque l’illusion que le chaos est maîtrisable.  [C’est pas magique, c’est juste GitOps](https://www.sitepoint.com/power-of-argocd-with-kubernetes/), mais bien fait.

⚡ **Highlights from Git 2.50 :** Git 2.50 est arrivé, et c'est une dinguerie comme on dit à Montargis. Finis les dépôts obèses pleins de blobs oubliés, le moteur de merge ORT devient le nouveau standard, plus rapide et plus simple que l'antique recursive, MIDX s’optimise, les lookups s’accélèrent, et git reflog delete fait son apparition pour nettoyer proprement l’historique.  [En résumé, Git transpire moins](https://github.blog/open-source/git/highlights-from-git-2-50/), pédale plus vite, et te laisse un peu plus de temps pour comprendre pourquoi tu merges encore sur main à 23h00 un dimanche soir.

🎯 **Mitmproxy, an interactive TLS-capable intercepting proxy :** mitmproxy, c’est ton proxy man-in-the-terminal : tu interceptes, modifies et rejoues le trafic HTTP, HTTPS, WebSocket, comme un Retailleau en pleine descente d'acides. Interface terminal ou web, API Python pour tout tordre à la volée, certificats générés à la main ou presque.  [Idéal pour mater ce que ton app envoie vraiment](https://github.com/mitmproxy/mitmproxy)  ou injecter du chaos dans un backend trop confiant.

🥇 **Arsenal :** Arsenal (rien à voir avec le club de foot lol) c'est un peu le Graal du pentester pressé : tu cherches un outil, tu sélectionnes une commande, et hop, elle se tape toute seule dans ton terminal. C’est le rêve  [quand tu ne te souviens plus de la commande exacte de nmap](https://github.com/Orange-Cyberdefense/arsenal)  pour scanner ton réseau ou des arguments de gobuster. Tu peux même définir des variables globales comme ip pour qu’elles s’insèrent dans les bonnes options automatiquement, sans te retaper la doc. Franchement, c’est peut-être l’outil qui nous a le plus bluffés depuis un bon moment, bravo aux outlaws de Orange Cyberdefense pour le taffe !

😱 **Sshx, a secure web-based collaborative terminal :** sshx, c’est du partage de terminal en live, sans VPN ni juron. Tu lances un binaire Rust, tu files un lien,  [et ton collègue voit tout, tape avec toi](https://github.com/ekzhang/sshx), et même te parle via un mini chat. Tout est chiffré, tout marche dans tous les shells, et les commandes vont dans l’historique comme si c’était toi. C’est du pair programming sans Teams, du support sans souffrance, et du cloud sans bullshit.

## Keep calm and respond, a beginner's heuristic to incident response

![](https://storage.mlcdn.com/account_image/325165/hbOBBbeE1ptChGsF38RdxirD2wpn6d2zqs7g8Klr.png)

  

On passe au courrier des lecteurs, et aujourd’hui c’est Sylvain D., SRE sous le soleil de la Côte d’Azur qui nous a partagé un lien bien utile pour garder son sang-froid quand tout brûle. Dans ce billet, on découvre une méthode simple pour structurer sa réponse aux incidents, sans hurler “ROLLBACK” au hasard ni envoyer des gifs paniqués sur Slack. L’approche repose sur six axes à explorer : cause, impact, périmètre, utilisateurs touchés, erreurs observées et temporalité. Pas de magie, juste du bon sens balisé, un pense-bête pour les cerveaux fondus à 3h du mat.

Merci Sylvain, et bon courage si un jour tes alertes tombent un 15 août à midi.

[Accéder au lien ->](https://dzone.com/articles/keep-calm-and-respond-a-beginners-heuristic-to-inc-1)