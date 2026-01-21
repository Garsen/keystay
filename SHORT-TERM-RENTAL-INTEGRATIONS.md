# Keystay: Short-Term Rental Platform Integrations

**Date:** 21 January 2026
**Purpose:** Technical and commercial requirements for Airbnb, Booking.com, and other OTA integrations

---

## Executive Summary

Short-term rental (STR) is a key revenue stream for Keystay investors. To offer this at scale, we need **connectivity** with major Online Travel Agencies (OTAs). This document covers what's required, how to get it, and the recommended approach.

**Bottom Line:** Direct API access to Airbnb and Booking.com is restricted to approved partners. Keystay should integrate via an established **channel manager** initially, then build toward **direct partnerships** and a **direct booking engine** as we scale.

---

## The Booking Landscape

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                           GUEST BOOKING CHANNELS                                 │
├─────────────────────────────────────────────────────────────────────────────────┤
│                                                                                  │
│   ┌─────────────────────────────────────────────────────────────────────────┐   │
│   │                        GLOBAL OTAs (Commission-Based)                   │   │
│   ├─────────────────────────────────────────────────────────────────────────┤   │
│   │                                                                         │   │
│   │  Airbnb          Booking.com       Vrbo/Expedia      Agoda             │   │
│   │  3% host fee     15-20%            5% + 3%           15-18%            │   │
│   │  + 14% guest     commission        payment fee       commission        │   │
│   │                                                                         │   │
│   └─────────────────────────────────────────────────────────────────────────┘   │
│                                                                                  │
│   ┌─────────────────────────────────────────────────────────────────────────┐   │
│   │                    SOUTH AFRICAN OTAs (Local Focus)                     │   │
│   ├─────────────────────────────────────────────────────────────────────────┤   │
│   │                                                                         │   │
│   │  LekkeSlaap          SafariNow           TravelGround                   │   │
│   │  15% commission      ~15% commission     15% commission                 │   │
│   │  33,000+ properties  Safari/tourism      English LekkeSlaap             │   │
│   │  Afrikaans market    15+ years           Same backend                   │   │
│   │                                                                         │   │
│   └─────────────────────────────────────────────────────────────────────────┘   │
│                                                                                  │
│   ┌─────────────────────────────────────────────────────────────────────────┐   │
│   │                    LUXURY / NICHE PLATFORMS                             │   │
│   ├─────────────────────────────────────────────────────────────────────────┤   │
│   │                                                                         │   │
│   │  Homes & Villas      Plum Guide          HomeToGo                       │   │
│   │  by Marriott         Ultra-luxury        Metasearch                     │   │
│   │  ~20% commission     ~20% commission     Pay-per-click                  │   │
│   │  High-end only       Curated listings    15M+ listings                  │   │
│   │                                                                         │   │
│   └─────────────────────────────────────────────────────────────────────────┘   │
│                                                                                  │
│   ┌─────────────────────────────────────────────────────────────────────────┐   │
│   │                    DIRECT BOOKING (Commission-Free)                     │   │
│   ├─────────────────────────────────────────────────────────────────────────┤   │
│   │                                                                         │   │
│   │  Own Website              Google Vacation Rentals                       │   │
│   │  0% commission            Commission-free possible                      │   │
│   │  You drive traffic        High search visibility                        │   │
│   │  Own the customer         Requires certified integration                │   │
│   │                                                                         │   │
│   └─────────────────────────────────────────────────────────────────────────┘   │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

---

## Platform Commission Comparison

| Platform | Commission Model | Effective Rate | API Access | Best For |
|----------|------------------|----------------|------------|----------|
| **Airbnb** | 3% host + 14% guest | ~3% to host | Restricted | International guests |
| **Booking.com** | 15-20% commission | 15-20% | Paused | European travellers |
| **Vrbo** | 5% + 3% payment | ~8% | Via Expedia | Families, groups |
| **LekkeSlaap** | 15% commission | 15% | Direct possible | SA domestic |
| **SafariNow** | ~15% commission | 15% | Direct possible | SA tourism |
| **Direct Booking** | 0% | **0%** | N/A | Repeat guests |

---

## Airbnb Partnership

### How to Become an Approved Partner

Airbnb **does not accept open applications**. They identify and approach potential partners based on:

1. **Supply opportunity** — How many listings can you bring?
2. **Technology strength** — Is your platform robust?
3. **Customer support capability** — Can you support shared customers?

### Requirements (If Accepted)

| Requirement | Details |
|-------------|---------|
| Mutual NDA | Sign Airbnb's standard non-disclosure agreement |
| API Terms | Agree to Airbnb's API Terms of Service |
| Data Security Review | Pass comprehensive security audit |
| API Quality Review | Technical integration must meet standards |
| Mandatory Features | Implement all required API features within 6 months |
| Instant Booking | All connected listings must have instant booking enabled |

### Partnership Tiers

| Tier | Meaning | Benefits |
|------|---------|----------|
| **Preferred** | Meets requirements | Marketing exposure, partner support |
| **Preferred+** | Exceeds requirements | Financial incentives, early access, priority support |

### How to Apply

Visit [airbnb.com/d/preferred-software-partner](https://www.airbnb.com/d/preferred-software-partner) — but expect rejection unless you have significant scale (1,000+ units typically).

### Current Approved Partners (2025)

Guesty, Hostaway, Lodgify, Smoobu, Hostify, iGMS, Hospitable, Hostfully, Uplisting, and ~24 others.

---

## Booking.com Partnership

### Current Status

**Applications are PAUSED** — Booking.com stopped accepting new connectivity partners while updating terms and conditions. No ETA on reopening.

### Requirements (When Available)

| Requirement | Details |
|-------------|---------|
| PCI Compliance | Payment Card Industry security standards |
| PII Compliance | EU data protection (GDPR) |
| Integration Project | Present your proposed integration |
| Multi-stage Approval | Technical review before account activation |
| Ongoing Maintenance | Keep up with continuous API changes |
| Full Year Availability | Load 12 months of rates/availability |

### Partnership Tiers

| Tier | Benefits |
|------|----------|
| **Standard** | Basic technical support |
| **Advanced** | Achievement awards, self-certification, event invites |
| **Premier** | Dedicated Business Manager, live chat, innovation fund |

### Application Portal

[connect.booking.com](https://connect.booking.com/) — registration currently closed.

---

## Channel Managers (The Middleware)

Channel managers already have API access to major OTAs. Keystay connects to one channel manager to access all platforms.

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                        CHANNEL MANAGER ARCHITECTURE                              │
├─────────────────────────────────────────────────────────────────────────────────┤
│                                                                                  │
│                              ┌──────────────┐                                   │
│                              │              │                                   │
│                              │   KEYSTAY    │                                   │
│                              │   PLATFORM   │                                   │
│                              │              │                                   │
│                              └──────┬───────┘                                   │
│                                     │                                           │
│                                     │ Single API Integration                    │
│                                     ▼                                           │
│                              ┌──────────────┐                                   │
│                              │              │                                   │
│                              │   CHANNEL    │                                   │
│                              │   MANAGER    │                                   │
│                              │  (Guesty)    │                                   │
│                              │              │                                   │
│                              └──────┬───────┘                                   │
│                                     │                                           │
│           ┌─────────────┬───────────┼───────────┬─────────────┐                │
│           │             │           │           │             │                │
│           ▼             ▼           ▼           ▼             ▼                │
│      ┌────────┐   ┌─────────┐  ┌────────┐  ┌─────────┐  ┌──────────┐          │
│      │ Airbnb │   │Booking  │  │  Vrbo  │  │LekkeSlaap│  │ SafariNow│          │
│      │        │   │  .com   │  │        │  │         │  │          │          │
│      └────────┘   └─────────┘  └────────┘  └─────────┘  └──────────┘          │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

### Top Channel Managers

| Provider | OTA Connections | Pricing | SA Support | Best For |
|----------|-----------------|---------|------------|----------|
| **Guesty** | 200+ channels | $8-15/listing/mo | Yes | Enterprise (50+ units) |
| **Hostaway** | 100+ channels | $10-20/listing/mo | Limited | Mid-market (20-100) |
| **Lodgify** | 50+ channels | $5-12/listing/mo | Limited | Small-mid (5-50) |
| **Rentals United** | 90+ channels | $$$/mo | Yes | Distribution focus |
| **Smoobu** | 30+ channels | $3-8/listing/mo | No | Budget (<20 units) |
| **NightsBridge** | SA-focused | R150-300/mo | Yes (SA-based) | SA properties |
| **Cloudbeds** | 300+ channels | $$$$/mo | Limited | Hotels + vacation |

---

## Direct Booking Engine

### What Is It?

A direct booking engine is **your own website** where guests book directly with you, cutting out OTAs entirely.

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                       OTA vs DIRECT BOOKING COMPARISON                           │
├─────────────────────────────────────────────────────────────────────────────────┤
│                                                                                  │
│   VIA AIRBNB (OTA)                        VIA KEYSTAY.CO.ZA (DIRECT)            │
│   ────────────────                        ──────────────────────────            │
│                                                                                  │
│   Guest                                   Guest                                  │
│     │                                       │                                    │
│     ▼                                       ▼                                    │
│   ┌──────────┐                           ┌──────────────┐                       │
│   │  Airbnb  │                           │ keystay.co.za│                       │
│   │  Website │                           │   Website    │                       │
│   └────┬─────┘                           └──────┬───────┘                       │
│        │                                        │                               │
│        │ Books property                         │ Books property                │
│        ▼                                        ▼                               │
│   ┌──────────┐                           ┌──────────────┐                       │
│   │  Airbnb  │                           │   Keystay    │                       │
│   │ Processes│                           │  Processes   │                       │
│   │ Payment  │                           │   Payment    │                       │
│   └────┬─────┘                           └──────┬───────┘                       │
│        │                                        │                               │
│        │ Takes 3% host fee                      │ Takes 0% commission           │
│        │ + 14% guest fee                        │                               │
│        ▼                                        ▼                               │
│   ┌──────────┐                           ┌──────────────┐                       │
│   │ Keystay  │                           │   Keystay    │                       │
│   │ Receives │                           │   Receives   │                       │
│   │   97%    │                           │    100%      │                       │
│   └──────────┘                           └──────────────┘                       │
│                                                                                  │
│   WHO OWNS THE CUSTOMER?                  WHO OWNS THE CUSTOMER?                │
│   ──────────────────────                  ──────────────────────                │
│   Airbnb owns the                         Keystay owns the                      │
│   relationship. Guest                     relationship. Guest                   │
│   returns via Airbnb.                     returns direct.                       │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

### Commission Comparison

| Booking Method | Commission | Who Owns Customer | Repeat Booking |
|----------------|------------|-------------------|----------------|
| Via Airbnb | 3% host + 14% guest | Airbnb | Goes through Airbnb |
| Via Booking.com | 15-20% | Booking.com | Goes through Booking |
| Via Direct Website | **0%** | **Keystay** | Direct relationship |

### When Direct Booking Makes Sense

| Scenario | Use OTAs | Use Direct |
|----------|----------|------------|
| New property, no reputation | ✅ | ❌ |
| Building initial guest base | ✅ | ❌ |
| International travellers | ✅ | ❌ |
| Repeat guests | ❌ | ✅ |
| Corporate bookings | ❌ | ✅ |
| Local market (SA domestic) | Maybe | ✅ |
| Have marketing budget | Maybe | ✅ |

### The Catch

You need to **drive your own traffic**:

- SEO (takes 6-12 months)
- Paid ads (Google, Facebook)
- Email marketing to past guests
- Social media presence
- Referral programs

OTAs bring customers to you. A direct booking engine requires you to bring customers to it.

### Direct Booking Tools

| Tool | What It Does | Pricing |
|------|--------------|---------|
| **Lodgify** | Website builder + booking engine | $12-32/mo |
| **Hostaway** | Includes direct booking website | Included |
| **Guesty** | Booking widget for your site | Included |
| **Checkfront** | Booking system | $49+/mo |
| **Custom Build** | Your own platform | Dev cost |

---

## Cost Impact Analysis

### For a R15,000/month STR Property

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                    REVENUE BY BOOKING CHANNEL                                    │
├─────────────────────────────────────────────────────────────────────────────────┤
│                                                                                  │
│   GROSS BOOKING VALUE: R15,000                                                  │
│                                                                                  │
│   ┌─────────────────────────────────────────────────────────────────────────┐   │
│   │ VIA AIRBNB                                                              │   │
│   ├─────────────────────────────────────────────────────────────────────────┤   │
│   │ Gross Revenue           R15,000                                         │   │
│   │ - Airbnb Host Fee (3%)    (R450)                                        │   │
│   │ - Channel Manager          (R200)                                        │   │
│   │ ─────────────────────────────────                                        │   │
│   │ Net to Keystay          R14,350     (95.7%)                             │   │
│   └─────────────────────────────────────────────────────────────────────────┘   │
│                                                                                  │
│   ┌─────────────────────────────────────────────────────────────────────────┐   │
│   │ VIA BOOKING.COM                                                         │   │
│   ├─────────────────────────────────────────────────────────────────────────┤   │
│   │ Gross Revenue           R15,000                                         │   │
│   │ - Booking Commission (15%) (R2,250)                                     │   │
│   │ - Channel Manager          (R200)                                        │   │
│   │ ─────────────────────────────────                                        │   │
│   │ Net to Keystay          R12,550     (83.7%)                             │   │
│   └─────────────────────────────────────────────────────────────────────────┘   │
│                                                                                  │
│   ┌─────────────────────────────────────────────────────────────────────────┐   │
│   │ VIA DIRECT BOOKING                                                      │   │
│   ├─────────────────────────────────────────────────────────────────────────┤   │
│   │ Gross Revenue           R15,000                                         │   │
│   │ - OTA Commission             R0                                          │   │
│   │ - Payment Processing (2.5%)  (R375)                                     │   │
│   │ ─────────────────────────────────                                        │   │
│   │ Net to Keystay          R14,625     (97.5%)                             │   │
│   └─────────────────────────────────────────────────────────────────────────┘   │
│                                                                                  │
│   ANNUAL IMPACT (100% occupancy):                                               │
│   • Airbnb:        R172,200/year                                                │
│   • Booking.com:   R150,600/year                                                │
│   • Direct:        R175,500/year  (+R3,300 vs Airbnb, +R24,900 vs Booking)     │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

---

## Keystay Integration Strategy

### Phase 1: MVP (Month 1-6)

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│ PHASE 1: CHANNEL MANAGER DEPENDENCY                                              │
├─────────────────────────────────────────────────────────────────────────────────┤
│                                                                                  │
│   ┌─────────┐        ┌──────────────┐        ┌─────────────────────┐           │
│   │ Keystay │───────▶│  NightsBridge │───────▶│ LekkeSlaap          │           │
│   │ (Manual)│        │  or Guesty   │        │ Airbnb (via iCal)   │           │
│   └─────────┘        └──────────────┘        │ SafariNow           │           │
│                                               └─────────────────────┘           │
│                                                                                  │
│   Focus: Prove the model, get properties, learn operations                      │
│   Scale: 0-20 properties                                                        │
│   Cost: R200-500/property/month for channel manager                             │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

### Phase 2: Integration (Month 7-12)

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│ PHASE 2: API INTEGRATION                                                         │
├─────────────────────────────────────────────────────────────────────────────────┤
│                                                                                  │
│   ┌─────────────┐     ┌──────────────┐     ┌─────────────────────────┐         │
│   │   Keystay   │────▶│   Guesty     │────▶│ Airbnb (full API)       │         │
│   │  Dashboard  │ API │     API      │     │ Booking.com             │         │
│   │             │◀────│              │◀────│ Vrbo                    │         │
│   └─────────────┘     └──────────────┘     │ LekkeSlaap              │         │
│                                             └─────────────────────────┘         │
│                                                                                  │
│   Focus: Unified dashboard, automated sync, dynamic pricing                     │
│   Scale: 20-100 properties                                                      │
│   Cost: R150-300/property/month (volume discounts)                              │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

### Phase 3: Scale (Year 2)

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│ PHASE 3: DIRECT PARTNERSHIPS + DIRECT BOOKING                                    │
├─────────────────────────────────────────────────────────────────────────────────┤
│                                                                                  │
│                         ┌───────────────────┐                                   │
│                         │                   │                                   │
│                         │  KEYSTAY.CO.ZA    │◀──── Direct Bookings (0%)        │
│                         │  (Direct Booking) │                                   │
│                         │                   │                                   │
│                         └─────────┬─────────┘                                   │
│                                   │                                             │
│                    ┌──────────────┴──────────────┐                              │
│                    │                             │                              │
│                    ▼                             ▼                              │
│            ┌──────────────┐             ┌──────────────┐                        │
│            │    Direct    │             │   Channel    │                        │
│            │  Partnerships│             │   Manager    │                        │
│            │  (if approved)│            │  (backup)    │                        │
│            └──────┬───────┘             └──────┬───────┘                        │
│                   │                            │                                │
│           ┌───────┴───────┐            ┌───────┴───────┐                       │
│           ▼               ▼            ▼               ▼                       │
│      ┌────────┐     ┌─────────┐   ┌────────┐    ┌──────────┐                  │
│      │ Airbnb │     │Booking  │   │  Vrbo  │    │LekkeSlaap│                  │
│      │(direct)│     │  .com   │   │        │    │          │                  │
│      │  API   │     │(direct) │   │        │    │          │                  │
│      └────────┘     └─────────┘   └────────┘    └──────────┘                  │
│                                                                                  │
│   Focus: Reduce OTA dependency, own customer relationships                      │
│   Scale: 100-500 properties                                                     │
│   Goal: 30%+ bookings direct                                                    │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

### Phase 4: Independence (Year 3+)

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│ PHASE 4: OTA INDEPENDENCE                                                        │
├─────────────────────────────────────────────────────────────────────────────────┤
│                                                                                  │
│   BOOKING MIX TARGET:                                                           │
│                                                                                  │
│   ┌─────────────────────────────────────────────────────────────────┐           │
│   │                                                                 │           │
│   │   Direct Bookings          50%  ████████████████████            │           │
│   │   (keystay.co.za)                                               │           │
│   │                                                                 │           │
│   │   Airbnb                   30%  ████████████                    │           │
│   │   (for international)                                           │           │
│   │                                                                 │           │
│   │   LekkeSlaap/Other         20%  ████████                        │           │
│   │   (for SA domestic)                                             │           │
│   │                                                                 │           │
│   └─────────────────────────────────────────────────────────────────┘           │
│                                                                                  │
│   At this stage:                                                                │
│   • Keystay is a recognised brand                                               │
│   • Repeat guests book direct                                                   │
│   • Corporate/business accounts book direct                                     │
│   • OTAs used only for discovery                                                │
│   • Significantly improved margins                                              │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

---

## Key Decisions Summary

| Decision | Options | Recommendation |
|----------|---------|----------------|
| Initial channel manager | Guesty / NightsBridge | **NightsBridge** for MVP (SA-focused, affordable) |
| Primary OTA | Airbnb / Booking.com | **Airbnb** (lowest commission, best STR fit) |
| Secondary OTA | Booking.com / LekkeSlaap | **LekkeSlaap** (SA domestic, lower commission) |
| Direct booking | Build / Buy | **Buy** (Lodgify or Guesty widget) initially |
| Partnership applications | Now / Later | **Later** (need scale first: 500+ units) |

---

## Sources

- [Airbnb Preferred Software Partner](https://www.airbnb.com/d/preferred-software-partner)
- [Airbnb 2025 Partners Announcement](https://news.airbnb.com/announcing-our-2025-preferred-software-partners/)
- [Booking.com Connectivity Requirements](https://connectivity.booking.com/s/article/Requirements-for-becoming-a-Booking-com-Connectivity-Partner)
- [Booking.com Connectivity Portal](https://connect.booking.com/)
- [Best Channel Managers 2025 - Hostaway](https://www.hostaway.com/blog/best-vacation-rental-channel-managers/)
- [Hotel Booking Sites SA - RoomRaccoon](https://roomraccoon.co.za/blog/hotel-booking-sites-south-africa/)
- [Airbnb Alternatives - Truvi](https://truvi.com/blog/airbnb-alternatives/)
- [LekkeSlaap](https://www.lekkeslaap.co.za/)
- [SafariNow](https://www.safarinow.com/)

---

*Document version: 2.0*
*Last updated: 21 January 2026*
