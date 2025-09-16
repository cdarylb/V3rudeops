---
layout: post
title: Newsletter du 15 Septembre 2025
tags: [devops, Gitops, Git, Docker, Hurl]
comments: true
mathjax: true
author: RudeOps
---

Il y a des semaines où l’actualité tech déborde de nouveautés, de scripts malins, de retours d’expérience bien sentis. Et il y a celles où l’on se dit qu’on ferait mieux d’aller promener son laptop dans un champ, loin des clusters K8s et des pipelines qui refusent de build.

Mais voilà, on est là. On continue de lire, de tester, de partager. Parce que sous les commits mal commités et les conférences trop longues, il y a encore des idées, des outils et des pratiques qui valent le détour.

Cette semaine, on parle d’open source qui gratte, d’automatisation qui pique, et de ces petites trouvailles techniques qui rendent le quotidien un peu moins absurde. Comme toujours, pas de promesse de miracle, juste de quoi nourrir votre veille, et peut-être, vous arracher un sourire en prime.

Bonne lecture.  
  
Cyril

### Quoi de neuf ?

🏃‍♂️  **MLOps vs DevOps, essential differences for tech leaders :** Un choc des titans… du buzzword. D’un côté, DevOps, cette vieille bête fatiguée qui automatise les pipelines, surveille les logs et pousse du YAML jusqu’à ce que mort s’ensuive. De l’autre, MLOps, son cousin sous acide, qui fait la même chose mais en ajoutant du  _"réentraînement automatique de modèle supervisé par CI/CD"_, du  _"monitoring de dérive statistique"_, et une bonne dose de confusion sémantique. [Les cowboys de chez Netguru tentent de clarifier](https://www.netguru.com/blog/mlops-vs-devops)  : les outils se ressemblent, les métiers s’éloignent. Là où DevOps s’occupe de déployer des services stables, MLOps gère des modèles instables. Là où DevOps flique des erreurs humaines, MLOps tente de prévenir les erreurs... mathématiques. Bref, deux mondes, une même promesse : tout casser plus vite, mais proprement.

</> **Never fear git conflict again :** Git, c’est un peu comme la plomberie d’un vieux manoir victorien : tant que personne ne touche à rien, ça tient. Mais dès que deux personnes bricolent la même canalisation en parallèle, tu te retrouves les pieds dans l’eau avec un message de conflit que même Trump n’aurait pas osé écrire. Le billet revient sur ce grand classique :  [pourquoi Git te hurle dessus quand tu merges un pull request](https://apps.theodo.com/article/never-fear-git-conflicts-again-smart-tips-for-smooth-merges)  pourtant validé, comment il découpe tes fichiers en "hunks", pourquoi changer deux lignes différentes peut quand même foutre le feu à ton diff, et comment résoudre tout ça sans te noyer dans les options. Entre les algos de diff façon histogramme, les options qu’on confond tous, et le rerere qui enregistre tes choix comme un stagiaire zélé, il y a de quoi éviter de refaire la même galère trois fois.

🥇  **Supercharge your git workflows :** Imagine un monde où git clone ne dure pas plus longtemps qu’un discours de Bayrou, un monde où cloner Chromium ne nécessite pas une pause déjeuner complète, un massage crânien et une reprise de contexte, un monde sans 95 minutes d’attente, sans disques saturés, sans CI qui tourne dans le vide en brûlant ton budget cloud. [Ce monde, c’est](https://about.gitlab.com/blog/supercharge-your-git-workflows/) _[Git Much Faster](https://about.gitlab.com/blog/supercharge-your-git-workflows/)_. Un script pas très joli, mais diablement efficace, conçu pour benchmarker et optimiser les clones de gros dépôts Git, avec des stratégies comme le ---depth=1, les clones partiels, l'usage de Scalar, et des configurations qui insultent gentiment les réglages par défaut de Git. Résultat : des gains absurdes, des pipelines qui redémarrent, et des devs qui pleurent un peu moins. Alors non, ça ne résout pas tous tes problèmes de monorepo mutant et de JPEG dans Git, mais ça tape fort là où ça fait mal : sur la lenteur. Et pour une fois, ce n’est pas un plugin VS Code qui prétend changer ta vie.

📦 **SafeDep Vet :** Vet, c’est un outil pour ceux qui n’ont plus envie de vivre dans le déni des dépendances.  [Un scanner de packages open source](https://github.com/safedep/vet), qui fouille dans tes projets (Go, npm, PyPI, Maven…) pour identifier les bibliothèques abandonnées, les versions vulnérables, les trucs douteux, les trucs trop vieux, et les trucs que tu n’as jamais compris mais que tu as mergé quand même parce que "ça buildait". Pas de magie, pas de chichi : un tableau de bord brut, des alertes claires, et un petit goût amer quand tu découvres que tout ton backend repose sur une lib maintenue par un certain "g33kman42" plus actif depuis 2017.

🦊 **Getting started with Gitlab CI/CD pipeline :** Il arrive un moment où balancer du code en prod à la main, en SSH à 23h, n’a plus rien d’excitant. Alors tu te penches sur GitLab CI/CD, pas parce que c’est à la mode, mais parce que tu veux que ça tienne debout, même quand tu dors. L’article des cowboys de chez Devtron t’explique  [comment poser les premières briques d’un pipeline](https://devtron.ai/blog/how-to-setup-gitlab-ci-cd-pipeline/)  sans sombrer dans une indigestion de YAML. C’est clair, propre, sans fumée magique, et ça te permet enfin de passer du bricolage fébrile à une mécanique un peu plus digne.

**🐋 Docker approaches to multiple environments :** Configurer plusieurs environnements avec Docker, c’est un peu comme essayer de jouer à Dwarf Fortress sur une TI-83 : théoriquement possible, mais personne ne devrait avoir à vivre ça. Tu penses faire propre avec un docker-compose.override.yml, et tu finis avec des conteneurs qui s’appellent api-test-prod2-bis, des fichiers .env dans .env.local.env, et un volume nommé data_legacy_maybe. [Le billet des mecs de chez SimpleThread essaie de remettre un peu d’ordre dans cette mare de YAML visqueux](https://www.simplethread.com/docker-approaches-to-multiple-environments/). Fichiers de conf, branches Git par environnement, ou scripts dignes d’un rite vaudou à base de sed et de jq : tout y passe. Pas de miracle, mais une bonne piqûre de rappel pour les âmes égarées.

Ⓐ **Hands on automatisation with Ansible :** Écrire des playbooks Ansible, c’est un peu comme tenter de dresser un troupeau de chats en pyjama avec un sifflet à ultrasons : c’est élégant dans l’intention, mais très vite ça miaule dans tous les sens. [Le billet de Faun revient aux bases](https://faun.pub/hands-on-automation-with-ansible-ff724d6bba7a)  : installation, inventaire, modules, état idempotent… Une balade main dans la main avec Ansible, comme si YAML était ton ami et que les erreurs de syntaxe ne te coûtaient pas trois heures de ta vie. Si tu débutes, c’est plutôt bien fichu, si tu es vétéran, ça te rappellera une époque où tu croyais encore qu’un ansible-playbook site.yml allait marcher du premier coup.

💝 **Hurl :** Tester des API avec curl, c’est pratique… jusqu’à ce que ton fichier de commandes ressemble à un grimoire en JSON mal formaté, et que tu te demandes si tu n’aurais pas dû devenir boulanger. Hurl,  [c’est un peu le chaînon manquant entre curl et une vraie syntaxe](https://github.com/Orange-OpenSource/hurl)  lisible. Tu écris tes requêtes HTTP comme des scripts propres, avec des assertions, des variables, des imports, et même un retour chariot de temps en temps. Pas besoin de Node, pas besoin de Swagger, juste du texte bien foutu et une CLI qui va droit au but.

🛠️ **Zizmor :** Zizmor est un chouette outil de  _static analysis_  open source pour GitHub Actions.  [Il scanne tes workflows](https://github.com/zizmorcore/zizmor) pour détecter les failles les plus courantes : actions non “pinées” (utilisation de tags vagues), permissions trop larges, triggers risqués, templates vulnérables ou encore commits imposteurs. Tu l’installes comme un binaire Rust, tu l’ajoutes à ta CI, et il te sort un rapport clair pour que tu puisses corriger ton chantier avant qu’il ne devienne un problème.

😱 **GitOps vs IaC :** GitOps vs IaC, c’est un peu comme demander si tu préfères un tournevis électrique ou un tournevis plat : les deux font le boulot, mais l’un tourne tout seul pendant que l’autre te laisse te visser le poignet. [L’article des outlaws de chez Spacelift](https://spacelift.io/blog/gitops-vs-iac)  remet un peu d’ordre dans la tambouille terminologique : non, GitOps n’est pas juste de l’IaC avec un dépôt Git. C’est un modèle d’exploitation, une philosophie de déploiement, une religion pour certains, un enfer YAML pour d’autres. L’idée ? Tu ne déploies plus, tu  _déclares_ et c’est l’agent qui se tape le sale boulot. L'IaC reste un outil : Terraform, Pulumi, Ansible… c’est ce que tu écris. GitOps, c’est comment tu l’utilises. Si l'IaC est le code de la route, GitOps, c’est l’autopilote qui respecte les limitations (ou pas).


## The origin story of merge queues

![](https://storage.mlcdn.com/account_image/325165/einN7ZhLaqd0K80FTJWNQS49fb8uTD0O82bbnMiy.png)

Cette semaine, merci à Arnaud T. pour son partage d’un article sur l’origine des merge queues.

On y découvre comment une simple idée ("et si on arrêtait de péter la prod à chaque pull request ?") a donné naissance à l’un des outils les plus sous-estimés du CI moderne. L’équipe des intellos de chez Mergify y raconte la genèse de ces files d’attente à merges, conçues pour éviter le chaos quand dix devs décident de merger en même temps le vendredi à 17h.

C’est bien raconté, étonnamment humain, et ça rappellera à certains pourquoi ils ont un bouton pause dans leur CI/CD. Une lecture utile pour quiconque a déjà pleuré devant un rebase, ou tenté d’expliquer à un Product Owner pourquoi “ça marchait sur la branche d’avant”.

[Accéder au lien ->](https://mergify.com/blog/the-origin-story-of-merge-queues)