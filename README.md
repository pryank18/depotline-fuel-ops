# Depotline

> 📘 **[Read the product case study on Notion](https://fern-appliance-85f.notion.site/3ebefd17b76681089891ed7697810089)** — problem, key decisions, what was cut and how I'd measure it.
>
> **Live demo:** [pryank18.github.io/depotline-fuel-ops](https://pryank18.github.io/depotline-fuel-ops/) · **Docs:** [PRD](https://github.com/pryank18/depotline-fuel-ops/blob/main/docs/PRD.md) · [BRD](https://github.com/pryank18/depotline-fuel-ops/blob/main/docs/BRD.md) · [MRD](https://github.com/pryank18/depotline-fuel-ops/blob/main/docs/MRD.md) · [Spec](https://github.com/pryank18/depotline-fuel-ops/blob/main/docs/product-spec.md) · **More work:** [Notion portfolio](https://fern-appliance-85f.notion.site/Pryank-Wadhera-3eaefd17b76680c88283e85a3217ff52)

Depotline is a single-screen operations dashboard for small and mid-size fuel depots, unifying inventory, pricing, and fleet fuel logs that are normally scattered across a stock spreadsheet, a separate pricing sheet, and a paper or WhatsApp fleet log.

## Live demo

https://pryank18.github.io/depotline-fuel-ops/

## What it does

- **Inventory tracking** — add/adjust stock entries, current level per fuel type (Diesel, Petrol, Gas, Paraffin)
- **Pricing & margin** — set price per fuel type, with margin auto-calculated against last-in stock cost
- **Fleet fuel logs** — log dispensed fuel by vehicle, date, and quantity, kept as a running log with a fleet-average comparison
- **Dashboard** — one screen combining current stock, current price, and today's dispensed total

## Product decisions

- **One screen instead of three tools.** Stock, pricing, and fleet logs share a dashboard because the core failure is pricing set without current stock in view.
- **Running log before trend analytics.** Fleet logs show each vehicle's latest volume against the fleet average. Per-vehicle history is parked for v1.1 until it's clear the target operator needs it.
- **No POS/ERP integration or invoicing in v1.** The target user has neither an ERP nor an ops team; integrations would add setup cost before the core loop is proven.
- **Responsive web, not a native app.** Operators already have a phone and a browser; an app store install is friction with no v1 payoff.

**How I'd measure it:** time to answer "what's my margin right now" drops from a 5–10 minute spreadsheet lookup to under 30 seconds, and unreconciled fleet fuel entries hit zero per week.

## Data

All companies, people, phone numbers, and figures in the demo are fictional sample data.

## Documentation

- [Product spec](docs/product-spec.md)
- [PRD](docs/PRD.md)
- [BRD](docs/BRD.md)
- [MRD](docs/MRD.md)

## How it was built

Built AI-assisted with Claude as coding partner. Product scope, requirements (see `docs/`), and QA are mine.

## Status

Live — v1 is built and deployed as a self-directed product project, informed by direct field experience in fuel logistics operations.
