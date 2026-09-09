
![FikaMarket Logo](assets/logo.png)

**FikaMarket** is a data-driven agricultural marketplace connecting small-scale farmers in Zambia directly to produce buyers, cutting out exploitative middlemen.



[For More Information](https://cipherinformationalwebsite.vercel.app/ ){ .md-button target="_blank" rel="noopener" }

## The Problem
Agriculture drives 19% of Zambia's GDP and supports 70% of the rural population, yet small-scale farmers remain cut off from profitable markets. Relying on middlemen kills their bargaining power and market visibility, while post-harvest losses, low digital literacy, poor connectivity, and locked financial services stall any growth. These compounding barriers hit farmers hardest especially women, leaving them heavily excluded from tech, funding, and trade.


## Core Flow

```text
┌─────────────────────┐
│ 1. FARMER REGISTERS │
│      PRODUCE        │
│ Crop • Quantity     │
│ Price • Availability│
└──────────┬──────────┘
           │
           ▼
┌─────────────────────────┐
│ 2. PLATFORM CREATES     │
│       LISTING           │
│                         │
│ Produce becomes visible │
│ to potential buyers     │
└──────────┬──────────────┘
           │
           ▼
┌─────────────────────────┐
│ 3. BUYER BROWSES AND    │
│       PLACES ORDER      │
│                         │
│ Selects produce,        │
│ quantity and collection │
│ date                    │
└──────────┬──────────────┘
           │
           ▼
┌─────────────────────────┐
│ 4. FARMER DELIVERS      │
│    TO COLLECTION POINT  │
│                         │
│ Produce is taken to the │
│ designated collection   │
│ point                   │
└──────────┬──────────────┘
           │
           ▼
┌─────────────────────────┐
│ 5. LEAD FARMER          │
│      VERIFIES           │
│                         │
│ Confirms handover using │
│ Order ID                │
└──────────┬──────────────┘
           │
           ▼
┌─────────────────────────┐
│ 6. BUYER COLLECTS       │
│      PRODUCE            │
│                         │
│ Buyer collects produce  │
│ and payment is released │
│ to the farmer           │
└─────────────────────────┘
```


## Who Uses It

| Role            | What they do                                                                       | How they access FikaMarket         |
| --------------- | ---------------------------------------------------------------------------------- | ---------------------------------- |
| **Farmer**      | Registers and lists available produce, views transactions and receives payments    | USSD / supported digital interface |
| **Lead Farmer** | Manages a designated collection point and verifies produce handovers               | Digital interface                  |
| **Buyer**       | Searches for produce, places orders, selects collection dates and collects produce | Mobile application                 |



## Key Features

### User Onboarding
The platform begins with a role-specific onboarding process where farmers, Lead Farmers, and buyers register to establish verified profiles.

### Produce Listings
Once registered, farmers utilize produce listings to digitally catalog their available crops by type, quantity, price, and location.

### Live Market Prices
Trading decisions are guided by live market prices that provide real-time pricing data to ensure transparency for both sides.

### Buyer Marketplace with Produce Matching
Buyers then navigate a buyer marketplace with produce matching that uses a filterable directory to pair them with ideal listings based on crop type, volume, and date.

### Escrow Checkout via Flutterwave
When a match is found, buyers complete an escrow checkout via Flutterwave which holds their funds securely until delivery terms are met.

### Farmer Transaction History
After a successful trade, the farmer transaction history updates a centralized, permanent ledger tracking all sales, pending escrow funds, and payouts.

### SMS Notifications
Throughout this entire cycle, automated SMS notifications send instant text alerts regarding orders, payments, and handovers to keep users informed.



## System Overview

| Layer | Components and Infrastructure |
| --- | --- |
| **Client Layer** | USSD interface optimized for farmers and a dedicated mobile application for buyers |
| **Backend Services** | Core microservices handling user registration, listings, matching, orders, and escrow |
| **Integrations** | External network bridges including Flutterwave, SMS gateway, and geolocation services |
| **Data Stores** | Persistent relational storage tracking user profiles, listings, orders, and transaction history |