---
layout: post
title: "Pourquoi Kubernetes mange votre budget (et comment j'ai réduit la facture de 60%)"
description: "Une plongée technique dans l'optimisation des coûts EKS : Spot Instances, VPA et nettoyage des ressources zombies."
date: 2025-11-22 08:00:00 +0100
categories: [DevOps, FinOps, Kubernetes]
image: https://images.unsplash.com/photo-1579621970563-ebec7560ff3e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1351&q=80
# Statistiques Simulées pour la Tuerie
sim_views: "3.4k"
sim_likes: "412"
sim_comments: "28"
---

C'est l'histoire classique : on migre vers le Cloud pour la "flexibilité", et six mois plus tard, le directeur financier débarque dans le bureau des Ops avec une facture AWS qui a doublé.

Kubernetes (K8s) est puissant, mais mal configuré, c'est un trou noir financier. Voici l'analyse post-mortem d'une optimisation que j'ai menée, faisant passer une facture mensuelle de 3 Milloins à 0.9 Milloin de FCFA.

## 1. Le Diagnostic : L'Over-Provisioning

Le premier coupable n'était pas le trafic, mais la **peur**. Par peur que l'application ne crashe, les développeurs avaient défini des `requests` CPU et RAM énormes.

> **Le problème :** Kubernetes réserve les ressources demandées (Requests), qu'elles soient utilisées ou non. Nous payions pour du vide.

### La Solution : Vertical Pod Autoscaler (VPA)
J'ai implémenté le VPA en mode "Recommandation". Après une semaine de collecte de métriques réelles via Prometheus, nous avons ajusté les `requests` au plus près de la consommation réelle (+20% de buffer).

## 2. L'Arme Secrète : Les Spot Instances

Nos environnements de *Staging* et de *Dev* tournaient sur des instances On-Demand (prix fort) 24/7.

**L'Architecture Cible :**
* **Production :** Instances Réservées pour le Control Plane et les bases de données.
* **Stateless Workloads :** Migration vers des **Spot Instances** (jusqu'à -90% du prix).

J'ai utilisé **AWS Node Termination Handler** pour gérer gracieusement les interruptions des Spots. Le cluster est devenu résilient au chaos, et drastiquement moins cher.


<!-- ![Schéma d'architecture Kubernetes optimisé](https://medium.com/@extio/kubernetes-architecture-explained-5e9b406de5d1) -->
<!-- <img src="https://medium.com/@extio/kubernetes-architecture-explained-5e9b406de5d1" alt="Schéma d'architecture Kubernetes" style="max-width: 100%; height: auto; display: block; margin: 20px auto;"> -->

## 3. Le Nettoyage des Zombies 

En scannant le cluster, j'ai trouvé :

* Des volumes EBS orphelins (attachés à des pods morts depuis des mois).
* Des Load Balancers non utilisés.

Un simple script Python programmé dans une CronJob via GitLab CI nous alerte désormais chaque semaine sur les ressources non attachées.

## Conclusion

L'ingénierie ne consiste pas seulement à faire tourner des conteneurs. Elle consiste à délivrer de la valeur. En optimisant ce cluster, j'ai libéré du budget pour recruter un nouveau développeur.

**Et vous, quelle est votre stratégie pour dompter la facture Cloud ? Discutons-en sur GitHub.**