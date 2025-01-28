---
layout: post
title: Newsletter du 16 Décembre 2024
subtitle: All I want for Christmas is tech			
thumbnail-img: /assets/img/sapin de noel.png
gh-repo: daattali/beautiful-jekyll
tags: [devops, Prometheus, Gitlab, Github, Grafana, K8s]
comments: true
mathjax: true
author: RudeOps
---

Voici la dernière newsletter de 2024, on reviendra bien sûr en 2025 car on ne sait pas trop quoi faire de notre temps libre alors il faut bien s'occuper. En tout cas, ceux qui peuvent, on compte sur vous pour déconnecter un max et vous recentrer sur ce qui compte le plus dans une vie : la famille, les amis et le champagne !

Bonnes fêtes de fin d'années à tous, très sincèrement.  
  
Cyril

### Quoi de neuf ?

😱 **Over 300K Prometheus instances exposed, credentials and API keys leaked online :** Des chercheurs en cybersécurité ont révélé que des centaines de milliers de serveurs (?!) utilisant Prometheus sont vulnérables à des leaks et à des attaques par déni de service ou d'exécution de code à distance.  [Selon les mecs de Aqua Security](https://thehackernews.com/2024/12/296000-prometheus-instances-exposed.html), environ 296 000 instances de Prometheus Node Exporter et 40 300 serveurs Prometheus sont accessibles publiquement sur Internet, exposant potentiellement des informations comme des identifiants, des passwords, des tokens d'authentification et des photos de chat.

🦊 **How to deploy a PHP app using Gitlab's cloud run integration :** Les coyotes de chez Gitlab nous partagent un guide en plusieurs étapes détaillant le  [déploiement d'une application PHP sur Google Cloud Run](https://about.gitlab.com/blog/2024/12/10/how-to-deploy-a-php-app-using-gitlabs-cloud-run-integration/)  en utilisant la CI de Gitlab.

**🔌 Stupid network tricks using socat :** Contraction de  _socket_ et de  _cat_,  [socat est le couteau suisse parfait](https://spin.atomicobject.com/socat-stupid-network-tricks/)  pour vous accompagner en randonnée en Corse ou à Koh-Lanta dans l'équipe des jaunes. Bien plus flexible que netcat, c'est socat qu'on privilégie depuis quelques années, et notre décision est irrévocable.

**🛠️ Git revert :** On vous partage un très chouette article des intellos de chez Alchemists.io qui nous expliquent par l'exemple  [la différence entre un git revert et un git rebase](https://alchemists.io/articles/git_revert).

</> **Run database in Github Actions, persisting data to S3, and access it publicly :** On continue avec un article qui nous explique comment utiliser  [GitHub Actions pour lancer une base de données](https://wesql.io/blog/use-github-actions-as-database)  à la demande, en stockant des données de manière persistante sur S3 ou un autre service compatible, et en y accédant via un tunnel sécurisé. Idéal pour tester un prototype ou faire de la QA rapidement.  

🚀  **Grafana and Docker, a simple way to monitor everything :** Un post sympa qui explore comment  [l'utilisation conjointe de Grafana et Docker](https://last9.io/blog/grafana-and-docker/)  facilite la surveillance de nos systèmes. L'article détaille les concepts clés de Docker et fournit des instructions step by step pour installer Grafana dans un conteneur Docker, parfait pour ceux qui débutent.

**☸️ How Kubernetes requests and limits really work :** Imaginez Kubernetes comme un  [chef d'orchestre à moitié dément](https://thenewstack.io/how-kubernetes-requests-and-limits-really-work/), assignant à chaque application (les musicos) une quantité précise de ressources (CPU, mémoire) pour éviter les fausses notes. Les requests elles, garantissent une certaine puissance, tandis que les limits fixent des plafonds à ne pas dépasser. C'est pourtant pas compliqué.

**🐳 Container hardening, securing docker containers :** Un chouette article qui aborde les  [bonnes pratiques de sécurité](https://systemweakness.com/container-hardening-999acb9d2692) comme la prévention des conteneurs avec privilèges, la protection du démon Docker, le contrôle de l'allocation des ressources et l'utilisation d'outils de sécurité comme Seccomp et AppArmor dont on ne pourrait plus se passer.

## Avoid SELECT * even on a single-column table

![](https://storage.mlcdn.com/account_image/325165/ZQnyEP9pdesJ7X8SGo8b0QWZiTXeXxHTpzoVkCAT.png)

Merci à Fabrice L, DBA dans une boîte française liée à l'état, qui nous a envoyé un post un peu provoc mais super intéressant sur un mec traumatisé par une expérience vécue en 2012, où une application côté backend est soudainement devenue aussi lente qu'un parisien en province. Après investigation, il s'est avéré que l'utilisation de  `SELECT *`  sur une table à laquelle des colonnes BLOB avaient été ajoutées entraînait le chargement inutile de données volumineuses, causant une surcharge du réseau et une désérialisation coûteuse.  

[Accéder au lien ->](https://medium.com/@hnasr/avoid-select-even-on-a-single-column-tables-d6deed7b4aee)