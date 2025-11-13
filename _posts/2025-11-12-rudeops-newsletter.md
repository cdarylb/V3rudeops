---
layout: post
title: Newsletter du 12 Novembre 2025
tags: [devops, Restic, Nexterm, Talos, Linux]
comments: true
mathjax: true
author: RudeOps
---


Il y a des patchs qui corrigent des failles techniques, et d'autres qui corrigent des failles morales, et la Python Software Foundation en a publié un magistral il y a une dizaine de jours : refuser 1,5 million de dollars de subvention pour ne pas trahir ses valeurs.

Dans un monde où les budgets se signent plus vite que les chartes éthiques, la PSF a choisi la ligne de code la plus coûteuse mais aussi la plus digne. Face à l’administration Trump II, qui conditionnait la subvention à l'abandon de toute action liée à la diversité, l'équité et l'inclusion (DEI), la fondation a dit non.

On pourrait croire qu'il ne s'agit que de politique, mais dans l'open source tout est politique. La liberté du code n’a jamais été séparable de la liberté de celles et ceux qui le produisent, et dire non à la censure idéologique, c’est dire oui à la communauté dans son ensemble, à sa diversité, à sa richesse, à son humanité.

Et pour rappel, la PSF est loin d'être une multinationale avec ses 14 personnes et ses 5 millions de budget annuel. La subvention refusée représentait donc près d'un tiers de leurs moyens, mais ils ont préféré la cohérence à la complaisance.

Ce refus, c'est une (putain de) leçon pour toute l'industrie tech, car pendant que les techs bro de la Silicon Valley jouent les courtisans au bal du pouvoir, la PSF rappelle que l'open source n'a pas de maître, et que le code ouvert, c’est aussi un code moral.  
  
Cyril

### Quoi de neuf ?

**🗄️ Database backups, dump files and restic :** Avant, on faisait comme tout le monde : un mysqldump, un petit gzip, et un fichier qui change tous les jours même si la base est aussi vide que le frigo d'un célibataire fin de mois. C’était propre, certes, mais aussi subtil qu’un backup au marteau-piqueur. Résultat : des doublons à la pelle, du stockage qui gonfle comme une grenouille, et l'étrange impression de rejouer  _MacGyver fait de l’IT_. Maintenant,  [on laisse Restic faire le sale boulot](https://strugglers.net/posts/2025/database-backups-dump-files-and-restic/). Il compresse, chiffre, déduplique, trie les fichiers par tags, note dans un petit carnet que "tout va bien" si rien n'a changé… et tout ça sans écrire une seule ligne sur disque. Bref, on est passé de la sauvegarde artisanale à la haute couture du dump, sans couture apparente.

😱 **Déployer un VPN Wireguard sur Proxmox avec Opentofu :** Par votre serviteur. [Trois jours de boulot, du YAML partout](https://www.linkedin.com/pulse/retour-dexp%C3%A9rience-d%C3%A9ployer-un-vpn-wireguard-sur-avec-cyril-beaufrere-di8le/?trackingId=TuxZhatQQ1OfiMMwn%2BQJ2g%3D%3D), OpenTofu qui fait semblant d'être Terraform, Proxmox qui redémarre quand il veut, et WireGuard qui refuse obstinément de causer. Mais au bout : une IP qui ping, une connexion chiffrée et la satisfaction absurde d’avoir refait ce que apt install aurait fait en dix minutes. Ne me jugez pas.

**🐋 Docker monitoring for your terminal :** On vous présente un énième Docker manager, encore un, mais celui-là a une TUI, affiche des métriques en temps réel, et surtout c'est écrit en Rust, donc c'est rapide, sûr, et ça fait transpirer les fans de Python. CPU, mémoire, réseau : tout y passe dans  [une interface qui sent bon le terminal neuf](https://dtop.dev/). Un outil de plus pour surveiller vos conteneurs, et dans les ténèbres les lier.  

🔳 **Nexterm :** On continue avec une app sympa, même si encore en plein chantier, et  [qui permet de faire tout ce qu'on aime](https://docs.nexterm.dev/)  : se connecter en SSH, VNC ou RDP, fouiller des arborescences via SFTP, balancer des containers Docker en prod sans réfléchir, et même gérer vos LXC et QEMU sur Proxmox. Bonus : l'authentification à deux facteurs pour donner l'illusion que tout ça est sécurisé.

🚀  **How tech companies measure the impact of AI on software development :** L'excellent Gergely Orosz s'associe à Laura Tacho (CTO chez DX) pour  [un énorme article qui mérite votre temps](https://newsletter.pragmaticengineer.com/p/how-tech-companies-measure-the-impact-of-ai?ref=dailydev), votre attention, et probablement un petit café corsé. Au menu, comment 18 entreprises tech (dont GitHub, Google, Dropbox, Monzo, Atlassian...) mesurent l'impact réel des outils d'IA sur le développement logiciel. On parle de métriques concrètes : change failure rate, PR throughput, satisfaction dev, maintenabilité du code, ou encore "bad developer days" chez Microsoft (si si). C'est une vraie plongée très documentée dans la réalité des équipes qui veulent autre chose que "Copilot a généré 38% de notre code, tout va bien". C'est dense, c'est sourcé, c'est intelligent, on en redemande.

🏹 **Waveterm, an open-source cross-platform term :** Encore un jouet pour ceux qui trouvent que leur terminal manque de fioritures : Waveterm, un terminal open-source qui mélange bash, navigateur web, éditeur de texte et assistant IA dans une seule interface. Oui, c’est un peu  [comme si tmux avait bu trop de café et décidé de tout faire lui-même](https://github.com/wavetermdev/waveterm). Drag and drop, aperçus de fichiers distants, édition à la volée, chat IA intégré (avec support pour OpenAI, Claude, Ollama & co), et même des blocs de commande isolés pour surveiller vos scripts comme des tamagotchis sous perfusion. Compatible macOS, Linux, Windows, et crises existentielles.

[![](https://storage.mlcdn.com/account_image/325165/m6sU57KyfAKuAxey28vdIk4xSLC3czRXgp4iaNcG.png)](https://capitoledulibre.org/)

# Week-end dédié au logiciel libre à travers plus de 100 conférences et plus de 20 ateliers pour les expertes/experts et le grand public.

  

Au programme ce weekend  :

-   Plus de 100 conférences techniques (retour d'expérience, DevOps, web, jeux…) et plus de 20 ateliers ouverts au public curieux.
    
-   Un village d'associations où les radicalisés du GPL, des licences "à coller sur ton poster" et des hackers bienveillants s'organisent, échangent des stickers, décryptent des licences obscures et expliquent pourquoi "non, Microsoft ne sera jamais ton ami".
    
-   Des moments de détente pour rappeler qu'entre deux patchs Linux, on peut aussi rigoler.
    

Bref, si vous croyiez que le logiciel libre c'était juste un fichier ISO à graver, vous étiez loin. Ici, c'est un rituel, un rassemblement de ceux qui croient que "open" n’est pas un adjectif mais une épiphanie.

L'entrée est gratuite (inscription en ligne obligatoire), ce qui ravira nos lecteurs toulousains qu'on sait nombreux (en fait on en a aucune idée mais ça sonne super bien).


🌐 **It's not always DNS :** Ah, le bon vieux "It's always DNS", le mème préféré des Ops fatigués, des Devs désabusés et des Slackers en panne d'idées. Une punchline universelle, un réflexe pavlovien, un mantra gravé dans les logs de tous les incidents post-mortem depuis 2004. Et si on arrêtait de rigoler deux minutes ? Parce qu'en vrai, c’est  **rarement**  le DNS. C'est souvent l’automatisation bancale, le firewall capricieux, le subnet mal foutu, ou ce script qui fait joyeusement rm sur les enregistrements parce que quelqu’un a oublié un --dry-run, mais sûrement pas cette pauvre pile DNS, qu’on accuse par réflexe parce que c’est la première à tomber quand tout part en sucette.  [Comme le dit Paul Tagliamonte dans son billet](https://notes.pault.ag/its-not-always-dns/), si on peut remplacer "DNS" par "key-value store qui mappe un nom à une IP" et que la phrase reste cohérente, alors non, ce n’était pas DNS. Le vrai danger, ce n’est pas un NXDOMAIN , c’est l’absence totale de pensée critique dès qu’un dig répond lentement, et ça, aucun TTL n’y survivra. On peut donc mieux faire. On  _doit_  mieux faire. Et si on se trompe, bah… on blâmera quand même DNS. Par tradition.

🤖 **OSV-Scanner :** On vous présente aujourd'hui OSV-Scanner, un outil soutenu par une petite startup familiale du nom de Google, qui comme chacun sait, n'a pas du tout pour objectif de scanner tout ce qui bouge dans l'open source, votre infra, et vos rêves. Bref, OSV-Scanner est un frontend officiel  [pour la base de vulnérabilités OSV.dev](https://github.com/google/osv-scanner), qui permet de détecter les failles connues dans vos dépendances, vos conteneurs, vos paquets Linux, et probablement votre grille-pain si vous avez une buildroot un peu exotique. Multi-langage, multi-package manager, avec recommandations de remédiation guidée basées sur la "stratégie de ROI" (c’est écrit, on n'invente rien), c'est un peu le Shazam des CVE : il écoute votre projet et vous crache la liste de ses traumas.

☸️ **Talos Linux, bringing simplicity to Kubernetes :** Aujourd'hui on va vous parler de Talos, un OS minimaliste et open source conçu spécialement pour exécuter Kubernetes… et rien d’autre. Pas d’interface, pas de package manager, pas de SSH. Même le concept d’utilisateur a été mis à la benne. On dirait une distribution faite par un moine du DevSecOps, sous anxiolytiques. C’est développé par Sidero Labs, une boîte qui a décidé que tout ce qui dépassait d’un conteneur était une surface d’attaque. Résultat : Talos ne se gère pas, il se déclare.  [Immutable, sécurisé, sobre](https://thenewstack.io/open-source-talos-linux-bringing-simplicity-to-kubernetes/), on dirait le fantasme mouillé d’un SRE coincé entre une RFC et un audit ANSSI. Talos a séduit des gens tout à fait normaux, comme la SNCF ou la bourse de Singapour, qui ont migré en un clin d’œil depuis OpenShift ou autres artefacts préhistoriques hérités de l’époque où on pensait que "root" c’était une bonne idée. Et pour orchestrer tout ça sans s'arracher les cheveux avec Cluster API ou Terraform, ils ont pondu Omni, une sorte de SaaS centralisateur de vos nodes Talos. Vous pouvez le déployer chez vous, dans le cloud, dans le grenier de votre oncle, tant que ça boote sur PXE. Bref, Talos, c’est Kubernetes sans le gras.  

🐍 **Good bye Python chaos, meet UV :** On pensait que plus rien ne pouvait aggraver l'expérience d’un dev Python.  [Et puis, un jour, on découvre uv](https://shiftmag.dev/tame-python-chaos-with-uv-the-superpower-every-ai-engineer-needs-6051/), un outil écrit en Rust qui remplace tout : pip, poetry, pip-tools, les envs virtuels bordéliques, les installs aléatoires de PyTorch en 47 Go, et même les erreurs cryptiques façon "cannot resolve dependency because of ancient incantation in requirements.in". Uv, c’est un peu le gestionnaire que Python aurait dû avoir dès le départ, si les dieux du langage n'avaient pas décidé de punir l'humanité pour un péché commis avec Perl. Résultat ? Des installs rapides, un cache global partagé entre projets (donc fini les 5 copies de PyTorch), un lockfile universel, la gestion des scripts à la volée, et plus jamais de "ça marche pas sur ma machine".

## 1/3 Hands on Kubernetes with Minikube

![](https://storage.mlcdn.com/account_image/325165/J4xOFekPrFjBLSlt8PILzrM5OlUoL1enAYDY59Gv.png)

  

Un grand merci à Sébastien pour le partage de cette chouette introduction à Kubernetes via Minikube, ce simulateur de cluster qui tourne en solo, un peu comme votre stagiaire en juillet.

On y retrouve tout ce qui fait la beauté de Kubernetes, sans le plaisir de le débugguer à 3h du matin en prod : les namespaces, le control plane, le worker, les services, les IPs qui changent pour aucune raison apparente, etc. Le tout, sur un seul PC, pour apprendre sans se ruiner en nœuds et load balancers.

L'article détaille chaque composant (API server, etcd, CoreDNS…), ce qu'ils font, où ils écoutent, et pourquoi ça a l'air simple alors que ça ne l’est pas. Bonus : le tableau de bord Minikube pour cliquer comme si c'était simple.

Bref, une lecture pédagogique et bien structurée, parfaite pour celles et ceux qui veulent comprendre comment ça marche sous le capot... avant de tout casser pour voir si ça redémarre.

  

[Accéder au lien ->](https://faun.pub/1-3-hands-on-kubernetes-with-minikube-578ecf0351ee)