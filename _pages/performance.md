---
layout: default
title: "Performance Attribution"
parent: "DeFi Risk & Performance Framework"
nav_order: 3
---

# Performance Attribution & Fee Management
{: .no_toc }

<br>

{: .important }
> Liquidity provision is not about chasing APR. It is about **managing inventory risk** and **extracting fees efficiently**.

---

## Objective
{: .no_toc .text-delta }

Comme expliqué dans la section [Operational Risk]({{ site.baseurl }}/project/risk/), les rendements estimés servent d'aide à la décision, mais seul le rendement réalisé compte pour la mesure de performance.

- **Expected return** → Support à la décision.
- **Realized return** → Mesure de la performance réelle (calculée à la clôture).

---

## Fee Management Process

![Harvested Fees screen]({{ site.baseurl }}/assets/images/performance/harvest_fees.png)
{: .mx-auto }
*Harvested Fees tracking interface*
{: .text-center .text-small }

Ce module permet de suivre l'intégralité des frais récoltés (harvested fees). Il enregistre les revenus des pools actives et inactives par semaine pour obtenir les **frais réalisés**.

### Workflow
* **Cadence** : Récolte hebdomadaire (pour optimiser les coûts de transaction et la pertinence des données).
* **Simplicité** : Saisie rapide (Semaine, Pool, Montant). Les données alimentent automatiquement le tableau de bord global.
* **Contrôle** : Seules les pools actives et les périodes existantes sont sélectionnables pour éviter les erreurs de saisie.

---

## Performance Measurement Framework

![Performance per ended pool]({{ site.baseurl }}/assets/images/performance/performance.png)
{: .mx-auto }
*Net performance analysis for closed positions*
{: .text-center .text-small }

Pour calculer le rendement réalisé global, la position doit être clôturée. Le framework croise alors :
1. Les frais capturés (via la couche *Fees*).
2. Le **drift d'inventaire** (différence de valeur entre l'ouverture et la fermeture).

{: .note }
Le **Daily Return** est notre métrique clé : il permet de comparer la performance de positions ayant des durées de vie différentes.

Ce module répond à la question cruciale : *La prise de risque a-t-elle été suffisamment rémunérée ?*

---

## Why this matters

* **Fees vs Management** : Les frais accumulés ne compensent jamais une mauvaise gestion de "range".
* **Asset Selection** : Le choix des actifs sous-jacents reste primordial (attention à l'excès de volatilité).
* **Time Sensitivity** : Le facteur temps est plus important que l'APR affiché.

<br>

{: .highlight }
**Performance without risk context is noise. This toolkit links both.**
