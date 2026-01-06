---
layout: default
title: "DeFi Risk & Performance Framework"
nav_order: 2
# Si "Why this project" est la page d'intro, celle-ci vient logiquement après
---

# DeFi Risk & Performance Framework
{: .no_toc }

{: .warning }
> **Disclaimer**: This project is for educational and personal analytics purposes. It is **not** financial advice.

## Overview
{: .no_toc .text-delta }

The DeFi Risk Monitoring Toolkit is a personal, research-driven framework designed to monitor, analyze, and manage risk across decentralized finance strategies, with a strong focus on capital efficiency, liquidity provision, and market making mechanics.

Built from real-world DeFi usage, this framework aims to bridge the gap between on-chain execution and institutional-style risk monitoring, inspired by practices found in traditional trading, treasury, and market making desks.

The objective is simple: **turn fragmented DeFi positions into a coherent, risk-aware portfolio view.**

---

## Why this toolkit exists

Most DeFi dashboards show *positions*. Few show **risk**. This toolkit is designed to answer, at a glance:

* **What can hurt me today?** (liquidation, out-of-range, leverage drift, concentration)
* **What is working?** (fees vs IL, carry vs price move, real net performance)
* **What should I do next?** (actionable alerts + prioritized checklist)

{: .note }
> **TradFi bridge:** Think of it as a lightweight “risk desk” for DeFi, built for CLMM LPs, lending/borrowing strategies, and on-chain market making.


![Framework flow]({{ site.baseurl }}/assets/images/framework-flow.png)
{: .mx-auto style="max-width: 520px;" }

---

## What it covers

### 1. Position Monitoring (CLMM / LP)
Track the live state of active DeFi positions.
- In-range/out-of-range status
- Inventory composition (token0 / token1) and position value
- Lending/borrowing health: LTV monitoring, liquidation distance

**[Go deeper →]({{ site.baseurl }}/project/positions/)**

### 2. Risk Overview
Aggregates risk indicators for inactive positions.
- Opportunity cost
- Call-to-action indicator

**[Go deeper →]({{ site.baseurl }}/project/risk/)**

### 3. Performance Overview
Measures real LP performance beyond headline APR.
- Net performance over time (position value + fees).
- Daily and cumulative performance tracking

**[Go deeper →]({{ site.baseurl }}/project/performance/)**

---

## Key metrics (the “risk desk” layer)

| Category | Metrics |
| :--- | :--- |
| **Lending / Borrowing** | Current LTV, liquidation LTV |
| **CLMM / LP** | Range status, Inventory drift, Fee velocity, PnL vs IL |
| **Portfolio** | Exposure by token / protocol / chain |

---

## Architecture
- **Storage**: Google Sheets (fast iteration)
- **Logic**: formulas + scripts (Apps Script)
- **Outputs**: dashboards, alerts, and weekly reports

{: .highlight }
> **Design rule:** Every metric must lead to a decision: *hold / rebalance / deleverage / exit / add*.

## Roadmap
- [ ] **V1**: risk overview (LTV + CLMM range monitoring)
- [ ] **V2**: performance attribution (fees/IL/carry)
- [ ] **V3**: alerting system (threshold detection)
- [ ] **V4**: automated report + “playbook” per strategy
