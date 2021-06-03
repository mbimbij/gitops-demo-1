# Gitops demo 1

:fr: Sommaire / :gb: Table of Contents
=================

<!--ts-->

- [:fr: Description du projet](#fr-description-du-projet)
- [:gb: Project Description](#gb-project-description)

---

# :fr: Description du projet

Le but de ce projet et de s'essayer à ce que je pensais avoir compris de "gitops" sur le moment, à savoir infra-as-code, repo git comme golden source, et tous les changements sur l'infra se font à partir du code d'infra, via une pipeline de ci/cd dédiée. 

De la même manière que l'application sur les environnements n'est modifié qu'à la suite d'un commit, après toute une série de tests automatisés, et surement pas par intervention manuelle.

J'ai l'impression d'avoir peut-être mal compris ce terme "gitops", mais mettre en place une pipeline de déploiement d'infra sera quand même un side project rigolo.


# :gb: Project Description

The goal of this project is to try out what i thought i understood of so-called "gitops" on the moment, namely infra-as-code, git repo as the golden source, and every change to the infrastructure is being done from the infrastructure code, through a dedicated ci/cd pipeline.

In the same way as applications on environment are modified after a commit, a whole series of automated tests, and definitely no manual intervention.

After some reading, i feel like i am actually missing something about gitops, but setting up a cicd pipeline for infrastructure will style be a fun side project.