---
layout: post
title: Newsletter du 19 Janvier 2026
tags: [devops, Talos, K8s, Tailwind, Memtui]
comments: true
mathjax: true
author: RudeOps
---


Le monde brûle un peu partout. Aux États-Unis, des idées qu'on pensait rangées au rayon des horreurs du 20ème siècle reviennent en costard, badge et algorithmes. Le fascisme ne marche plus au pas de l'oie, il s'optimise, se teste en A/B, se déploie en production.

Et pendant ce temps-là, dans notre petite veille techno, on parle d’open source, d'outils, de pratiques, de gens qui documentent, partagent et construisent à plusieurs. Ce n'est pas hors-sol, c'est même tout l’inverse. Le libre, ce n'est pas juste une licence ou un repo Git, c'est une manière de refuser que tout devienne opaque, propriétaire, verrouillé par défaut.

Cette veille n'a aucune prétention, mais elle rappelle une chose simple : quand tout tend vers le contrôle, la fermeture et la peur, continuer à comprendre, partager et garder la main sur nos outils reste un acte éminemment politique, même quand ça ressemble juste à une newsletter un peu cynique lue entre deux tickets.  
  
Cyril

### Quoi de neuf ?

🖥️ **From pets to cattle, the new mindset for managing VMs :** Un papier des cowboys de chez TheNew Stack qui nous explique, une fois de plus, que les VM ne sont plus des animaux de compagnie mais du bétail, et que la solution consiste évidemment à les faire entrer de force dans Kubernetes via KubeVirt. [L'idée n’est pas tant technique que psychologique](https://thenewstack.io/from-pets-to-cattle-the-new-mindset-for-managing-vms/)  : arrêter de cliquer dans des interfaces pleines de souvenirs, accepter le YAML, Git, la déclaration d'intention et le fait que ça disparaît et ça revient. On y parle surtout de résistance au changement, de perte de contrôle ressentie, et de ce moment gênant où les équipes découvrent que K8s ne fait pas que tourner des conteneurs, mais remet aussi en question leurs habitudes. Rien de révolutionnaire, mais un bon rappel que le plus dur, dans la migration des VM, ce n’est pas la techno, c’est l’ego.

🔥 **Rebuilding my Talos cluster from bare metal :** Un radicalisé a tenté une simple refacto Flux bien propre, et a déclenché l’apocalypse ordinaire du homelab moderne. Rook-Ceph a vu deux manifests bouger, a paniqué sur des disques "déjà vus", et  [le cluster a commencé à faire la grève](https://blog.nerdz.cloud/2025/talos-dr-reset/)  comme un service public un jour de départ en vacances (je plaisante calmez-vous les fonctionnaires). Du coup méthode hygiène maximale, on blkdiscard tout ce qui dépasse, on wipefs les souvenirs, et on relance Talos plus Flux comme si de rien n'était, avec un Taskfile pour éviter de se trahir soi-même en tapant une IP au mauvais endroit. Et quand enfin tout respire, on découvre une feature alpha qui monte un OCI en volume read-only, on l'active évidemment, parce que quitte à tout reconstruire autant ajouter un nouveau point de fragilité, pour l'amour du risque.

**☸️ How to setup kubectl aliases with kuberc :** Bibin Wilson nous apprend une nouveauté qui aurait dû exister avant qu'on invente GitOps et la thérapie de groupe. Depuis kubectl 1.33, les alias peuvent en effet enfin vivre dans un fichier dédié, kuberc,  [au lieu de pourrir votre .zshrc](https://devopscube.com/kubectl-aliases/)  entre deux exports honteux. En pratique, vous passez kubectl en 1.33+, vous activez la feature via une variable d'environnement, vous posez un YAML dans ~/.kube/kuberc, et kubectl lit vos alias nativement. Bonus, vous pouvez aussi y définir des overrides pour imposer des flags par défaut, histoire que "juste un get" finisse systématiquement en "-o yaml", comme la nature l'a voulu.

</> **Two regimes of Git :** Pendant que certains veulent annexer le Groenland, d'autres tentent encore d’annexer Git avec une seule règle universelle, comme si ça avait déjà marché quelque part. Mark Seemann rappelle pourtant un truc simple :  [Git a deux modes de jeu](https://blog.ploeh.dk/2026/01/12/two-regimes-of-git/), et les confondre est un sport de haut niveau. Le premier, collaboratif, où tout ce qui est poussé devient sacré. Tu touches à l’historique et tu déclenches un incident diplomatique. Le second, tactique, en local, sans public. Là, tu rebases, tu réécris, tu nettoies, tu fais disparaître les erreurs comme si elles n'avaient jamais existé parce que personne n’a besoin de voir tes brouillons. Moralité : Git c’est pas compliqué, ce qui l'est, c'est d'accepter que tout le monde ne joue pas dans le même régime, et que hurler "rebase interdit" hors contexte est une forme d'extrémisme modéré.

🏹 **Anubis :** Anubis,  [c'est un pare-feu web](https://github.com/TecharoHQ/anubis)  qui te regarde droit dans les paquets et te demande si tu es un humain ou juste un autre aspirateur à données entraîné au venture capital. C’est pas encore tout à fait sec, mais l'essentiel est là, à suivre pour ceux qui bossent dans de petites structures.

**💾 Plakar :** Une chouette solution de backup qui a décidé que copier des fichiers c'était trop simple et surtout pas suffisant. Plakar sauvegarde les données  [avec leur contexte](https://github.com/PlakarKorp/plakar), histoire de ne pas restaurer un truc inutilisable à 3h du matin en se demandant où est passé le reste. C'est chiffré, immuable, dédupliqué, compressé, scalable dans tous les sens et étonnamment calme sous charge. Tu peux parcourir, comparer, monter un snapshot à la volée, restaurer juste ce qui t'intéresse, et repartir sans avoir à sacrifier un SSD et ta dignité.

![](https://storage.mlcdn.com/account_image/325165/Zup52cvnTcdWNxTUeCyxrJbDOu5vN0KxGLgoAwsU.png)

# Succès technique, échec économique

  

Personne ne conteste le succès de Tailwind, le framework est partout. Ce qui s’effondre, en revanche, ce sont les recettes.  [En deux ans, Tailwind Labs a vu ses revenus chuter brutalement](https://loud-technology.com/blog/tailwind-labs-ia-menace-modele-economique-open-source/), alors même que l'adoption continuait de croître. Résultat mécanique :  [licenciement d’environ 75 % de l’équipe](https://www.leanware.co/insights/tailwind-ai-crisis)  à cause d'une équation économique qui ne tient plus.

Le modèle était pourtant classique pour l'open source moderne : une documentation très fréquentée, notoriété, puis monétisation via des produits premium (UI kits, templates, services). Sauf que la doc n'est plus lue, elle est ingérée. Les agents IA consomment le contenu, génèrent le code, et l'utilisateur n'a plus aucun contact avec le projet ni aucune raison de financer quoi que ce soit. Le trafic baisse, la conversion disparaît, la trésorerie suit.

Le plus dingue, c'est que tout fonctionne techniquement, le projet remplit sa mission, c'est juste que  [la valeur économique est désormais captée en amont](https://devclass.com/2026/01/08/tailwind-labs-lays-off-75-percent-of-its-engineers-thanks-to-brutal-impact-of-ai/), par des intermédiaires qui ne contribuent ni au maintien, ni à l'évolution du logiciel. L'open source continue d’alimenter l’écosystème gratuitement pendant que ceux qui le maintiennent réduisent la voilure.

On reconnaît le scénario. Un contenu devenu indispensable, un modèle fondé sur l'attention, puis une couche intermédiaire qui capte l’usage sans jamais capter la responsabilité. La valeur circule, l'argent s'évapore, le logiciel continue de tourner, mais ceux qui le maintiennent réduisent la voilure. Et la question reste entière :  **comment financer des biens communs quand l’usage n’implique plus aucun lien direct avec ceux qui les produisent ?**

🏃‍♂️  **Open-Bastion :** Open-Bastion c'est l'idée simple qu'on promet depuis vingt ans et qu'on finit rarement par appliquer proprement : reprendre la main sur qui se connecte en SSH, où, et pour faire quoi, sans laisser traîner des clés et des sudoers bricolés à la main. Le principe est simple comme une chanson de Jul :  [un bastion central, branché sur LemonLDAP::NG](https://github.com/linagora/open-bastion) qui décide, accès par token temporaire ou clé SSH vérifiée, règles définies une fois, appliquées partout via PAM/NSS. Pas d’interprétation locale, pas de créativité. Côté hygiène, on est sur du sérieux sans folklore : TLS partout, journaux JSON propres, rate limiting, secrets chiffrés, et même intégration CrowdSec pour ceux qui aiment quand les IP disparaissent toutes seules.

💝 **God's eye :** Pour ceux qui aiment quand la cartographie d'un périmètre ressemble moins à une checklist et  [plus à une autopsie](https://github.com/Vyntral/god-eye), God's Eye arrive avec la délicatesse d'un scanner industriel. Ça énumère les sous-domaines, ça brute-force tout ce qui bouge, ça interroge tout ce qui passe, puis ça enchaîne HTTP probing, détection de technos, cloud guessing, secrets planqués dans le JavaScript, takeover potentiels et CVE servis encore chauds, le tout avec une couche d’analyse avec un LLM local, parce qu'en 2026 même la reco refuse de réfléchir toute seule.

😱 **Histomat of F/OSS, we should reclaim LLMs, not reject them :** Un chouette billet qui défend une idée presque subversive : le problème des LLMs n'est pas qu'ils mangent du code libre, mais qu'ils recrachent du propriétaire.  [La réponse ne serait donc pas la fuite](https://writings.hongminhee.org/2026/01/histomat-foss-llm/)  ou le blocage de bots déjà gavés, mais une bonne vieille arme open source, le copyleft. En gros entraîne-toi si tu veux, mais libère les modèles, poids compris.

🥇 **Memtui :** Pour ceux qui ne savent pas quoi faire de leur week-end et qui trouvent que fouiller un Memcached à coups de telnet manque cruellement de poésie, voilà memtui. [Un TUI moderne en Go](https://github.com/nnnkkk7/memtui)  pour explorer des clés comme on explore une arborescence, lire du JSON sans pleurer, détecter du gzip sans deviner, et éditer des valeurs avec un minimum de garde-fous pour éviter de tout casser. Recherche floue en temps réel, palette de commandes façon VS Code, confirmations avant les actions irréversibles et raccourcis vim pour se sentir chez soi, en clair tout ce qu’il faut pour passer deux jours à "juste regarder" Memcached et finir par comprendre pourquoi personne n’aime y toucher.  

## Easier Than Nano, Fresh is a 'Fresh' New Rust-based Terminal Editor for Linux

![](https://storage.mlcdn.com/account_image/325165/YoBtJ253h6ad1AUIV9hdzJb08UMD1uOr1cfqlsWg.png)

  

Merci à Pascal C, Scrum Master dans une célèbre startup parisienne, qui nous partage cette découverte autour de Fresh, un éditeur de texte TUI qui prend volontairement le contrepied de Vim et Emacs.

Fresh part d'un constat simple : tout le monde n'a ni l'envie ni le temps d'apprendre des keybindings ésotériques ou l'édition modale. Ici, pas de surprise : Ctrl+S pour sauvegarder, Ctrl+F pour chercher, Ctrl+Z pour annuler. Comme un éditeur graphique… mais dans un terminal.

Le projet, écrit en Rust, pousse le concept assez loin : support complet de la souris, palette de commandes (Ctrl+P), explorateur de fichiers intégré (Ctrl+E), panneaux latéraux, thèmes, aperçu Markdown et même un terminal embarqué, le tout sans configuration lourde. À noter aussi un support LSP natif et la capacité de manipuler des fichiers très volumineux ce qui parlera à pas mal d’ops.

Les plugins existent également, développés en TypeScript, exécutés dans un environnement sandboxé, ce qui est plutôt sain côté sécurité.  

[Accéder au lien ->](https://itsfoss.com/fresh-terminal-text-editor/)