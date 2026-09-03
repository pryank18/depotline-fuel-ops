# Depotline — Business Requirements Document

## Business objective

Give small and mid-size fuel depot operators a lightweight, single-screen alternative to running stock, pricing, and fleet fuel logs across three disconnected tools (a stock spreadsheet, a pricing sheet, and a paper or WhatsApp log).

## Background

Depot operators typically reconcile inventory, pricing, and fleet consumption manually across separate tools. This creates two recurring costs: pricing decisions made without current stock visibility, and fleet fuel consumption that is only caught after the fact during a manual audit.

## Scope

**In scope:** inventory tracking, pricing and margin calculation, fleet/vehicle fuel logging, and a consolidated dashboard, for a single depot or site.

**Out of scope (v1):** multi-location rollups, POS/ERP integration, invoicing/payments, native mobile app.

## Stakeholders

- **Primary user:** depot operator (one- or two-person team) managing stock and pricing decisions day to day
- **Product owner:** Pryank Wadhera — self-directed project, informed by direct field experience in fuel logistics operations

## Success criteria

- Time to check current margin and stock position drops from a multi-tab spreadsheet lookup (roughly 5–10 minutes) to under 30 seconds via the dashboard
- Zero unreconciled fleet fuel entries per week once logging is in daily use

## Assumptions

- Operator runs a single site/depot (multi-site is out of scope for v1)
- Operator is comfortable using a browser-based tool without formal onboarding

## Constraints

- No backend/database infrastructure assumed — v1 runs as a static, self-contained web app
- No integration with existing POS/ERP systems in v1

## Risks

- Manual data entry is the single point of failure for data accuracy; there's no automated feed from pumps or sensors in v1
- A single-site tool means multi-depot operators would need one instance per site until multi-location support is added

## Status

Live — v1 shipped as a personal/portfolio product project.
