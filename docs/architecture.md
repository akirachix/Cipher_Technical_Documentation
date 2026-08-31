
FikaMarket provides different interfaces for users by role. Farmers use **USSD**, Buyers use a **Mobile Application** and Lead Farmers use a **Dashboard**.

- **Farmer** - registers produce, checks live commodity prices, receives confirmations, via USSD
- **Lead Farmer** - oversees active buys and sells, logs collection point name, verifies produce handovers, via Dashboard
- **Buyer** - browses produce, places orders, pays, via Mobile Application

![FikaMarket System Architecture Diagram](assets/system-architecture.png)

[View full diagram](https://lucid.app/lucidchart/8d420c3a-9293-4261-8156-a244317c230b/edit?viewport_loc=1192%2C-787%2C3464%2C2178%2C0_0&invitationId=inv_23c5b8e0-e9a1-4da1-9094-49b0c22a03d2){ .md-button }

## Backend Architecture

A unified **FikaMarket API** connecting clients to the database and external services, organized into four modules:

| Module | Responsibility |
|---|---|
| **Register Produce** | Produce registration via USSD |
| **Market Management** | Live prices, active buys/sells |
| **Log Location** | Collection point verification |
| **Produce Purchase** | Ordering and payments |

## External Integrations

- **Africa's Talking API** —  live commodity prices, communication
- **LocationIQ API** — location retrieval and verification
- **Flutterwave API** — payments
- **Telecom Service Provider** — USSD communication flow

---

## Data Flow

1. **Registration** - Farmer registers via USSD, system creates Farmer and Location records.
2. **Produce Submission** - Farmer submits crop, quantity, price and collection point. Lead Farmer verifies against past records. Stored as a Produce Listing.
3. **Order Creation** - Buyer browses listings via the mobile application and places an order with a collection date. LocationIQ shows the collection point.
4. **Payment** - Buyer pays via Flutterwave, funds are held in escrow. Telecom provider confirms the mobile money account.
5. **Collection** - Farmer delivers the produce to the collection point. Lead Farmer confirms handover and verifies quantity.
6. **Escrow Release** - Payment releases to the farmer immediately after the buyer confirms pickup, Receipt is issued.
7. **Notifications** - Users get updates on orders, payments, collection,commodity price changes and release.
8. **Transaction History** - Completed transactions feed the farmer's trading history.