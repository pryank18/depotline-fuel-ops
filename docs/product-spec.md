# Fuel Management System — Product Spec

## Problem

Small and mid-size fuel operations run on three disconnected tools: a spreadsheet for stock, a separate one for pricing/billing, and a notebook or WhatsApp thread for vehicle/fleet fuel logs. Nobody has one place to see all three together, which means pricing decisions get made without current stock visibility, and fleet consumption goes untracked until someone audits it manually — usually too late to catch losses.

This system puts inventory, pricing, and fleet logs in a single web app so an operator can see the full picture in one screen instead of reconciling three.

## Target user

Depot or small fuel distribution operators — one or two people managing stock and pricing decisions day to day, without an enterprise ERP budget or a dedicated ops team. Built as a personal project, scoped to what a real operator in that position would actually use.

## Goals

- Give a single view of current stock, current pricing, and fleet fuel consumption
- Cut the time it takes to answer "what's my margin right now" from a manual spreadsheet pull to a live number
- Make fleet fuel logs auditable — who fueled what, when, and how much — without a paper trail

## Non-goals (v1)

- Multi-depot / multi-location rollups
- Integration with real POS or ERP systems
- Payment processing or invoicing
- Mobile app (web-first, mobile-responsive is enough)

## User stories

- As an operator, I want to log incoming fuel stock so my inventory numbers stay current without a manual recount.
- As an operator, I want to set and update pricing so I can see margin against my current stock cost in real time.
- As an operator, I want to log fleet/vehicle fuel dispensed so I know exactly how much went out and to which vehicle.
- As an operator, I want a single dashboard view combining stock level, current price, and today's fleet consumption, so I don't have to check three places.

## Core features (v1 scope)

| Feature | Description |
| --- | --- |
| Inventory tracking | Add/adjust stock entries, current stock level per fuel type |
| Pricing & billing | Set price per fuel type, auto-calculate margin against last-in cost |
| Fleet/vehicle logs | Log dispensed fuel by vehicle ID, date, quantity |
| Dashboard | Single-screen summary: stock, price, today's dispensed total |

## Success metrics (hypothesis — no usage data yet)

- Reduce time to check "current margin + stock" from a multi-tab spreadsheet lookup (~5–10 min) to under 30 seconds on the dashboard
- Zero unreconciled fleet fuel entries per week once logging is in daily use

## Open questions — resolved against current build

- **Single vs. multi fuel type:** Resolved as multi-type. The live dashboard already tracks separate stock levels per fuel type (Diesel, Petrol, Gas, and Paraffin observed) per site/terminal, so v1 supports multi-type by default.
- **Fleet log depth (running log vs. historical trends):** Currently a running log — the Fleet → Fuel Logs view shows each vehicle's most recent dispensed volume (derived from its latest completed delivery) plus a comparison against the fleet average. There's no per-vehicle historical trend/drill-down view yet. Decide whether that's worth adding for v1.1, or whether the running log + fleet-average comparison is enough for the target user.

## Status

Live — v1 is built and deployed. Dashboard, multi-fuel-type inventory tracking, pricing, and fleet fuel logs (running-log style) are implemented and running at https://pryank18.github.io/depotline-fuel-ops/. Remaining open item: whether to add per-vehicle historical trend views beyond the current running log.
