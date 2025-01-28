---
layout: post
title: Newsletter du 21 Octobre 2024
subtitle: La newsletter de l'austérité			
thumbnail-img: /assets/img/Alain-destruction.png
gh-repo: daattali/beautiful-jekyll
tags: [devops, Servers, Vault, Zendesk, Docker, Git, Talos, Python]
comments: true
mathjax: true
author: RudeOps
---

Certainement le pire jour de la semaine, on espère néanmoins que vous prendrez beaucoup de plaisir à parcourir notre veille techlectique (oui c'est un nouveau mot) qui reflète ce qui nous a le plus marqué durant ces derniers jours. Bonne semaine à tous !  
  
Cyril

### Quoi de neuf ?

**🚩 Sad servers, troubleshoot and make sad servers happy :** Vous êtes un vrai bonhomme comme on dit à Montargis ? Vous allez donc adorer ce site où vous pourrez  [tester vos skills en troubleshooting](https://sadservers.com/) (avec des morceaux de bases de données, Docker, K8s, etc...) en mode Capture the Flag. Vous y trouverez une jolie collection de scénarios avec une description du problème à résoudre et un test pour vérifier si la solution fonctionne. Les serveurs sont créés à la demande, et vous accédez à une session SSH via une fenêtre de votre navigateur.  

☸️ **How to manage secrets with Azure Key Vault in Kubernetes :** Un chouette article écrit par les outlaws de chez Devtron, et qui nous explique  [comment gérer des secrets dans K8s en utilisant Azure Key Vault](https://devtron.ai/blog/how-to-manage-secrets-with-azure-key-vault-in-kubernetes/), la solution cloud de Microsoft pour stocker et protéger des données sensibles, comme des mots de passe, des clés d'API ou les sms de votre ex.  

🐳 **Docker Compose logs - guide to monitoring & debugging :** On a trouvé ce guide qui vous prend par la main et vous explique comment utiliser  [docker compose logs](https://spacelift.io/blog/docker-compose-logs). Idéal si vous débutez.

🛠️ **Git-absorb :** Votre chambre est un foutoir pas possible à l'instar de votre code ?  [Essayez Git-Absorb](https://github.com/tummychow/git-absorb)  qui identifie automatiquement les modifications non validées et les incorpore dans les commits précédents d'une branche Git. Pour votre chambre on n'a hélas encore rien trouvé.

🏆  **How I use Git :** Et on continue sur Git avec ce chouette retour d'expérience qui nous détaille  [une approche personnelle de l'utilisation de Git](https://registerspill.thorstenball.com/p/how-i-use-git), développée au cours de 12 ans d'expérience avec de petites équipes d'ingés. L'auteur y aborde l'importance d'utiliser l'interface en ligne de commande, l'utilisation d'alias, des commits fréquents, et l'importance d'une bonne gestion des pull requests.

**🖥️ Talos Linux :** On pense pas vous avoir déjà parlé de Talos, une distribution Linux conçue [spécifiquement pour les environnements K8s](https://www.talos.dev/). La distrib prend en charge diverses plateformes, y compris dans le cloud, les serveurs physiques et la virtualisation. Le système est entièrement géré via API, supprimant ainsi le besoin d'accès via SSH.

**🐍 SSH scripting with Fabric and Python :** On aime beaucoup Fabric, alors on vous partage ce tuto très sympa qui nous explique comment utiliser le [module Python Fabric](https://www.blog.pythonlibrary.org/2024/10/16/ssh-scripting-with-fabric-and-python/)  pour exécuter des commandes SSH à distance et transférer des fichiers entre machines.

## How Zendesk intentionally left a backdoor in hundreds of Fortune 500

![](https://storage.mlcdn.com/account_image/325165/3YMNSIHlg60k8xuf6PGfU7xj0EXfMc0y4Y5JzfR8.png)

L'histoire du jour nous est partagée par Marc D., sysadmin dans une grosse boîte de retail en France, et elle est passionnante à plus d'un titre : Un gosse de 15 ans a découvert une faille critique dans Zendesk, qui permettait de manipuler les e-mails et de contourner les accès à des tickets de support. Après avoir été initialement rejetée par Zendesk, la faille a été signalée aux entreprises concernées, ce qui a quand même rapporté au chercheur plus de 50 000 dollars de récompenses en bug bounty. Zendesk a finalement corrigé la faille, mais sans offrir de compensation au jeune white hat.  

[Accéder au lien ->](https://gist.github.com/hackermondev/68ec8ed145fcee49d2f5e2b9d2cf2e52)