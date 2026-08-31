# FikaMarket

**FikaMarket** is a data driven agricultural marketplace connecting small scale farmers in Zambia directly to produce buyers, cutting out exploitative middlemen.

## The Problem

Agriculture makes up roughly **19%** of Zambia's GDP and supports around **70%** of the rural population, yet smallscale farmers remain excluded, facing weak bargaining power, post-harvest losses, low digital literacy, and (especially for women) poor access to credit and connectivity.



## Core Flow

1. Farmer registers produce (crop, quantity, price)
2. Platform creates a listing & assigns the nearest collection point
3. Buyer browses, orders, and picks a collection date
4. Farmer delivers to the collection point
5. Lead Farmer verifies the handover using order ID & confirmation ID
6. Buyer collects produce; escrowed payment releases to the farmer

## Who Uses It

| Role | Description |
|---|---|
| **Farmer** | Lists produce, uses USSD (no smartphone needed) |
| **Lead Farmer** | Verifies handovers and manages a collection point no storage/aggregation role |
| **Buyer** | Processors, wholesalers, exporters, retailers, use a mobile app |

## Key Features

- Onboarding
- Produce listings
- Live market prices
- Buyer marketplace with produce matching
- Escrow checkout via Flutterwave
- Farmer transaction history
- SMS notifications

## System Overview

- **Client layer** - USSD (farmers), mobile app (buyers)
- **Backend services** - registration, listings, matching, orders, escrow
- **Integrations** - Flutterwave, SMS gateway, geolocation
- **Data stores** - profiles, listings, orders, transaction history