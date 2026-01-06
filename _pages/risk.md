---
layout: default
title: "Operational Risk"
parent: "DeFi Risk & Performance Framework"
nav_order: 2
---

# Operational Risk
{: .no_toc }

<br>

We introduce this module as an operational monitoring layer built to manage idle positions.

{: .note }
> This risk view is intentionally simple and action-oriented.

---

## Purpose
{: .no_toc .text-delta }

-	What is the status of the portfolio?
-	Do I have inactive positions?
-	What is the opportunity cost?
-	What action should I take NOW?

---

![Risk Monitoring Dashboard]({{ site.baseurl }}/assets/images/risk/risk.png)
{: .mx-auto }
*Operational Risk Monitoring*
{: .text-center .text-small }

---

## Scope of the module
As each position works differently (asset, range, volatility), this module aims to create an easy call-to-action (or not).

Thinking as an opportunity cost on out-of-range (OOR) position, restores control on what action perform to reduce non profitable but risky positions.

### Risk Logic: The "OOR Timer"
When talking about fast decision-making, the rules need to be forward: time-based OOR.

-> How much earnings am I losing while OOR?

| OOR duration | Status | Suggested action |
| :--- | :--- | :--- |
| **< 2 Days** | Acceptable | None (noise or volatility spike). |
| **3 to 5 Days** | To monitor | Opportunity cost increases. market structure change? |
| **5 Days+** | Critical | consider adapting strategy : **rebalance** or **exit**. |

---

## Limitations
Ce module exclut délibérément certains risques pour rester focalisé sur l'opérationnel :
- **Impermanent Loss** : Considéré comme inhérent à la structure AMM. Nous comparons ici l'efficacité de la stratégie LP, pas par rapport au HODL.
- **Drawdowns Directionnels** : L'exposition de l'inventaire est gérée séparément.
- **Hedging** : Les stratégies de couverture pour le drift d'inventaire sont identifiées comme une extension future du framework.

This module deliberately excludes some risks such as:
- **Impermanent Loss**: Inherent to AMM structure. We especially focus on LP strategies here, so no need to compare with HODL.
- **Directional drawdowns**: Caused by inventory exposure, it is intentionally outside the current scope.

Hedging strategies for inventory drift are identified as a potential future extension of this risk framework.


### Complementary Risk Monitoring
In addition to LP operational risk, liquidation risk on lending positions is monitored through a dedicated LTV overview and automated alerts.

[Detailled here: Lend & borrow status]({{ site.baseurl }}/testDeFi/project/positions/#lend--borrow-status)
{: .btn .btn-outline }
