# Depotline — Product Requirements Document

## Summary

Depotline is a web-based operations tool that gives fuel depot operators a single view of stock, pricing, and fleet fuel consumption, replacing three disconnected tools: a stock spreadsheet, a pricing sheet, and a paper or WhatsApp fleet log.

## Target user

One- or two-person depot or small fuel distribution operations, without an ERP budget or a dedicated ops team.

## Problem

Pricing decisions get made without current stock visibility, and fleet fuel consumption goes unaudited until a manual check catches losses after the fact.

## Goals

- Single view of current stock, pricing, and fleet consumption
- Reduce "what's my margin right now" from a manual spreadsheet pull to a live number
- Make fleet fuel logs auditable — who fueled what, when, and how much

## Non-goals (v1)

- Multi-depot / multi-location rollups
- Integration with POS or ERP systems
- Payment processing or invoicing
- Native mobile app (mobile-responsive web is sufficient)

## Functional requirements

1. **Inventory tracking** — add/adjust stock entries; current stock level shown per fuel type (Diesel, Petrol, Gas, Paraffin)
2. **Pricing & billing** — set price per fuel type; margin auto-calculated against last-in stock cost
3. **Fleet/vehicle fuel logs** — log dispensed fuel by vehicle ID, date, and quantity, kept as a running log
4. **Dashboard** — single screen combining stock level, current price, and today's dispensed total
5. **Fleet comparison** — each vehicle's latest dispensed volume shown against the fleet average

## User stories

- As an operator, I want to log incoming stock so my inventory numbers stay current without a manual recount.
- As an operator, I want to update pricing and see margin against current stock cost in real time.
- As an operator, I want to log fuel dispensed per vehicle so I know exactly what went out and to whom.
- As an operator, I want one dashboard combining stock, price, and today's fleet consumption instead of reconciling three tools.

## Open items for v1.1

- Per-vehicle historical trend / drill-down view beyond the current running log

## Status

Live — v1 is built and deployed at pryank18.github.io/depotline-fuel-ops/.
