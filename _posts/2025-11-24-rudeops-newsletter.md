---
layout: post
title: Newsletter du 24 Novembre 2025
tags: [devops, LazyGit, Termix, IaC, ANSSI]
comments: true
mathjax: true
author: RudeOps
---


J'aurais voulu vous pondre un édito brillant, percutant, spirituel, qui dénonce, bref, un truc qui claque, mais malheureusement, l'inspiration a décidé de partir en RTT, probablement pour rejoindre la productivité qui elle aussi a disparu quelque part entre deux contrariétés au boulot.

Alors voilà, pas d'édito. Et honnêtement ? Ce petit vide fera très bien l'affaire, et il a même quelque chose de reposant, comme une pause involontaire et bienvenue dans un monde qui s'agite beaucoup trop.  
  
Cyril

### Quoi de neuf ?

**</> The (lazy) Git UI you didn't know you need :** Bartek nous raconte comment il a accidentellement découvert lazygit pendant un moment de fatigue néovim-esque. Résultat : une semaine plus tard, il avait tout migré dessus, son workflow, sa productivité, sa dignité, probablement ses enfants aussi. Et franchement ? On le comprend. Ça fait combien de fois qu’on vous en parle déjà, de lazygit ? Trois ? Quatre ? On a perdu le compte mais bon, quand quelqu'un tombe dedans par hasard et revient vous dire "wow, c'est génial", ça fait toujours plaisir de voir quelqu'un rejoindre la secte. Lazygit, c’est le Git que vous utilisez déjà,  [mais sans avoir à sacrifier des neurones](https://www.bwplotka.dev/2025/lazygit/)  pour vous souvenir si c'était git switch, checkout ou "tiens, je vais juste ouvrir une bière et reconsidérer ma carrière". Alors oui, si vous ne l'avez toujours pas testé… On ne veut pas dire que vous ratez votre vie, mais vous ratez votre vie.

👨🏻‍💻 **Hackers weaponize Windows Hyper-V to hide Linux VM :** Le groupe Curly COMrades (oui, le nom ressemble à une mascotte de shampooing soviétique) a trouvé une nouvelle manière d'éviter les outils de sécurité :  [lancer leur propre mini-machine virtuelle Hyper-V](https://thehackernews.com/2025/11/hackers-weaponize-windows-hyper-v-to.html)  sur les machines compromises. Dedans, un petit Alpine Linux de 120 Mo, un reverse shell maison (CurlyShell), un reverse proxy, et tout ce qu'il faut pour se balader tranquillement pendant que l'EDR regarde ailleurs en sifflotant. Le gang, déjà connu pour taper sur la Géorgie et la Moldavie, bosse depuis 2023 à base de Mimikatz, implants .NET modulaires, tunnels dans tous les sens et persistance façon "on s'installe, on reste, et on paye pas le loyer". Bref, pendant que vous galérez à faire tourner un cluster K8s de test, eux font tourner un mini-Linux clandestin dans un coin pour piloter leurs attaques tranquillou. On peut être méchant, mais il faut reconnaître que c’est propre et efficace… si on oublie la partie cybercriminalité soutenue par un État.

🥇  **How to write garbage code by Linus Torvalds :** Le créateur de Linux, Git, et accessoirement le chef d'orchestre irritable du plus grand projet collaboratif du monde, a une nouvelle fois expliqué à un ingénieur de Meta que son code était, techniquement parlant,  [de la purée de navet froide](https://read.engineerscodex.com/p/how-to-not-write-garbage-code-by). Derrière la castagne verbale, l'idée est simple : ne cachez pas des opérations triviales derrière des helpers débiles, ça rajoute du bruit, ça fatigue le cerveau, et ça oblige tout le monde à jouer au schmilblick dans les arborescences de fichiers.  

🔳 **Termix :** Termix débarque comme une alternative à Termius, open-source, auto-hébergé, [et surtout pour toujours gratuit](https://github.com/Termix-SSH/Termix), ce qui dans ce milieu ressemble presque à une menace. L'idée : unifier la gestion de vos serveurs derrière une interface moderne, propre, et conçue pour vous éviter de jongler entre douze terminaux, trois tunnels SSH, et votre patience en fin de vie. Au programme, un terminal SSH avec panneaux façon "mur Bloomberg du sysadmin fatigué", du tunneling avec reconnexion automatique, un file manager qui ouvre tout, même les images (oui, vraiment), un dashboard qui donne l'illusion que vos serveurs vont bien, de l’OIDC, du TOTP, de l'authent préchauffée, et une UI moderne React/Tailwind/Shadcn pour prouver que même un panneau d'administration peut être sexy en 2025.

🚀  **Why scaling is the funniest game :** Les cowboys de chez The New Stack ont demandé à Adam Jacob (System Initiative)  [pourquoi scaler, c'est la partie la plus fun du game](https://thenewstack.io/adam-jacob-on-why-scaling-is-the-funnest-game/). Sa réponse : parce que tu n'y touches pas tant que ça ne te fait pas mal, et que tant que personne n'utilise ton produit, optimiser revient juste à polir un mirage. Twitter a survécu sans savoir scaler pendant des années, donc relax. Et au final, son message est plutôt rassurant : tu n'as pas besoin d'anticiper l'apocalypse, construis un bon produit, laisse-le vivre, observe quand ça casse, puis renforce là où ça compte vraiment.

🤖 **Infrastructure for AI is finally getting a standard :** Breaking news : après un an où tout le monde a balancé des modèles en prod à la truelle, l'infrastructure IA a enfin un standard. C'est durant la KubeCon d'Atlanta que le CNCF  [a annoncé le Kubernetes AI Conformance Program](https://www.giantswarm.io/blog/infrastructure-for-ai-is-finally-getting-a-standard), un label qui dit en gros que "Votre cluster ne prend pas feu quand vous lancez un modèle de 40 milliards de paramètres." Le standard définit ce qu'un cluster doit réellement savoir faire pour exécuter des workloads IA sans imploser : GPU sharing, scheduling pas trop bête, stockage qui ne pleure pas, gouvernance qui empêche les devs de miner du Dogecoin sur les nœuds, etc.

![](https://storage.mlcdn.com/account_image/325165/oS4P3zdfozuEz2cKDb1fMM735EhcD40ByiszMcQr.jpg)

# Le diagnostic Cyberdépart de l'ANSSI

Vous souhaitez vous protéger contre les cyberattaques mais ne savez absolument pas par où commencer ? Pas de panique : l'ANSSI vous propose de prendre votre cyberdépart, un nom qui sonne un peu comme une course d'orientation, mais en moins fun.

Le principe : un diagnostic gratuit de 1h30 avec un "Aidant cyber", dans vos locaux ou en visio, pour découvrir que vos mots de passe sont nuls, que vos sauvegardes datent d’avant le Covid et que votre Wi-Fi invité est un open bar.

Attention, ce service n’est pas prévu pour les particuliers ni pour les boîtes à un seul salarié. En revanche, 3 300 sociétés ont déjà fait le grand saut, preuve que même les PME commencent à réaliser que le ransomware n'arrive pas qu'aux autres.

Bref, si vous voulez un point de départ simple, rapide, et officiellement sponsorisé, c’est probablement le moment de prendre votre cyberdépart. Après, pour le cyberretour, ça dépendra de vous.

[](https://messervices.cyber.gouv.fr/cyberdepart/)


**🔐 Keepr, an end to end password manager :** Keepr est un gestionnaire de mots de passe pensé pour les devs qui préfèrent vivre en ligne de commande plutôt que d’affronter une interface graphique. Tout est stocké localement  [dans une base SQLCipher chiffrée](https://github.com/bsamarji/Keepr), protégée par un mot de passe maître transformé en clé balaise via PBKDF2-HMAC (SHA256, 1,2 million d'itérations, rien que ça). Pas de cloud, pas de serveur, pas de sync magique, juste du chiffrement et du contrôle total.

🛠️ **Proxmox VE 9.1 available :** Proxmox a dégainé la version 9.1 de sa distro de virtualisation préférée des admins qui aiment souffrir proprement. La grosse nouveauté est une dinguerie comme on dit à Montargis :  [le support des images OCI](https://proxmox.com/en/about/company-details/press-releases/proxmox-virtual-environment-9-1) pour créer des conteneurs LXC. Oui, oui, on peut enfin balancer les mêmes images standardisées que dans nos pipelines. Proxmox les avale, les transforme en conteneurs système ou applicatifs, et pouf, vous déployez votre base de données ou votre API comme si de rien n'était. Le reste est du bonus : vTPM snapshotable en qcow2 (Windows applaudit timidement), contrôle plus fin du nested virtualization (pour ceux qui aiment faire tourner un hyperviseur dans un hyperviseur dans un hyperviseur on vous voit), et une visibilité SDN enfin digne de ce nom, avec un GUI qui arrête de jouer à cache-cache avec vos routes et vos MAC.

⚡ **Loglynx, advanced log analytics for Traefik :** LogLynx, c’est un petit  [moteur d'analytics pour logs Traefik](https://github.com/k0lin/loglynx)  qui tourne avec moins de 50 Mo de RAM, soit à peu près ce que Chrome consomme en clignant des yeux. Ça ingère vos logs en temps réel, fait des cartes, des timelines, de la détection d’appareils, du GeoIP, le tout dans un dashboard dark mode qui ferait presque croire que vous savez ce que vous faites. Ça parle SSE, SQLite, REST API, auto-discovery… bref, tout ce qu'il faut pour jouer au détective réseau sans lâcher un rein dans une licence enterprise.  

🐋 **How Docker hardened images patch cves in 24 hours :** Pour ceux que l'écosystème Docker intéresse, Docker continue de patcher les vulnérabilités à la vitesse d'un admin sous Red Bull. Dès qu’une CVE tombe, Docker Scout l’avale, l'analyse et déclenche la chaîne de rebuild comme si sa vie en dépendait. Résultat :  [images corrigées en moins de 24 heures](https://www.docker.com/blog/how-docker-hardened-images-patch-cves-in-24-hours/), pendant que d'autres en sont encore à rédiger un ticket Jira "à prioriser". Le tout repose sur une surveillance continue, pas sur un scan hebdomadaire qui découvre trois jours trop tard que votre stack est un gruyère. L'IA maison sert de firewall anti-conneries, bloque les patchs douteux, et un humain valide ce qui évite de pousser en prod un fix qui casse tout, joyeux classique de la sécurité pressée. Et comme chaque image embarque un SBOM propre et complet, fini les scanners qui hurlent au faux positif, les débats avec l'audit, ou les heures perdues à prouver que "non, promis juré, c’est bien patché".

## Some Thoughts About Claude Code

![](https://storage.mlcdn.com/account_image/325165/aemQQ4esXNJm6j8Ur0fXz5FciCNIaubetglVNpu3.png)

  

Merci à Arnaud qui nous partage cet article, et qui nous rappelle au passage que Claude Code, c’est un peu le stagiaire surdoué mais imprévisible que tu laisses toucher à ton repo en serrant les dents. Il lit tout, propose un plan, exécute des commandes, lance des tests… et parfois hallucine comme s'il avait compilé en pleine descente d'acide, avec le tout qui part chez Anthropic, avec une politique de rétention qui change plus souvent qu’un sprint mal cadré.

Le conseil phare : ne jamais cliquer sur "always accept". Claude est utile, mais il faut le tenir en laisse. Sur des tâches propres (refacto, boilerplate, tests, etc) il est redoutablement efficace. Sur les demandes floues type "rends ça plus rapide" ou "corrige les bugs", il dérive façon artiste conceptuel.

Et puis il y a le prix. Les tokens fondent vite, surtout quand Claude boucle dans sa petite logique interne. Résultat : tu finis par te demander si cette commande mérite vraiment 4 dollars d’analyse existentielle.

L’auteur résume parfaitement : outil pratique, mais pas magique, à utiliser comme un assistant, pas comme un remplaçant. Relis tout, supervise tout, et garde un œil sur la facture.

  

[Accéder au lien ->](https://hashrocket.com/blog/posts/some-thoughts-about-claude-code)