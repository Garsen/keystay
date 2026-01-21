# Keystay: Short-Term Rental Platform Integrations

**Date:** 21 January 2026
**Purpose:** Technical and commercial requirements for Airbnb, Booking.com, and other OTA integrations

---

## Executive Summary

Short-term rental (STR) is a key revenue stream for Keystay investors. To offer this at scale, we need **connectivity** with major Online Travel Agencies (OTAs). This document covers what's required, how to get it, and the recommended approach.

**Bottom Line:** Direct API access to Airbnb and Booking.com is restricted to approved partners. Keystay should integrate via an established **channel manager** or **property management system (PMS)** rather than building direct integrations.

---

## Platform Overview

| Platform | Market Position | Commission | API Access |
|----------|-----------------|------------|------------|
| **Airbnb** | Dominant in STR | ~3% host fee | Restricted — approved partners only |
| **Booking.com** | Largest OTA globally | 15-20% | Restricted — paused for new partners |
| **Vrbo/Expedia** | Strong in US/EU | 5% + 3% payment | Via Expedia Partner Solutions |
| **LekkeSlaap** | SA-focused | ~15% | Direct integration possible |
| **SafariNow** | SA tourism | ~15% | Direct integration possible |

---

## Airbnb Integration

### API Access Model

Airbnb does **not** offer a public API. Access is restricted to approved "Preferred Software Partners" who must:

1. **Undergo comprehensive security review** — Data security and API quality audit
2. **Meet technical standards** — Integration, foundational, and performance requirements
3. **Demonstrate scale** — Airbnb approaches partners based on supply opportunity
4. **Maintain instant booking** — All API-connected listings must have instant booking enabled

### 2025 Preferred Software Partners

Airbnb announced their [2025 Preferred Software Partners](https://news.airbnb.com/announcing-our-2025-preferred-software-partners/) including:

- Guesty
- Hostaway
- Lodgify
- Hostfully
- Uplisting
- Hospitable

### How Keystay Should Connect

```
┌─────────────────────────────────────────────────────────────────┐
│                      RECOMMENDED APPROACH                        │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│   KEYSTAY                    CHANNEL MANAGER              OTAs   │
│   PLATFORM                   (e.g., Guesty)                      │
│                                                                  │
│   ┌─────────┐               ┌─────────────┐          ┌────────┐ │
│   │         │   API/SDK     │             │  Direct  │ Airbnb │ │
│   │ Keystay │──────────────▶│   Guesty    │─────────▶│        │ │
│   │ Backend │               │   Hostaway  │          ├────────┤ │
│   │         │◀──────────────│   Lodgify   │◀─────────│Booking │ │
│   └─────────┘   Webhooks    │             │          │  .com  │ │
│                             └─────────────┘          ├────────┤ │
│                                                      │  Vrbo  │ │
│                                                      └────────┘ │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Alternative: iCal Sync (Not Recommended)

For hosts without API access, Airbnb offers iCal calendar sync:

| Method | Sync Speed | Double-Booking Risk | Features |
|--------|-----------|---------------------|----------|
| **API (via partner)** | Real-time | Very low | Full: pricing, availability, messaging |
| **iCal sync** | 1-24 hours | Higher | Calendar only |

**Recommendation:** iCal is too slow for professional operations. Use a channel manager.

---

## Booking.com Integration

### Connectivity Partner Program

Booking.com offers API access through their [Connectivity Partner Program](https://connectivity.booking.com/s/article/Requirements-for-becoming-a-Booking-com-Connectivity-Partner):

**Current Status (as of 2026):**
> "Booking.com is pausing integrations with new connectivity providers until further notice" while they update terms and conditions.

### API Capabilities

The [Booking.com Connectivity APIs](https://developers.booking.com/connectivity/docs) provide:

| Category | Capabilities |
|----------|--------------|
| **Content** | Create properties, rooms, rates, policies |
| **Rates & Availability** | Load inventory, prices, restrictions |
| **Reservations** | Retrieve bookings, modifications, cancellations |

### Technical Requirements

- **Protocol:** XML (OTA 2003B schema + Booking.com's B.XML extensions)
- **Authentication:** Partner credentials
- **PCI Compliance:** Required for reservation data (card details)
- **PII Compliance:** EU data protection regulations

### Partner Expectations

Booking.com expects connectivity partners to:

1. Load at least **one full year** of rates and availability
2. Provide **user-friendly interface** for property owners
3. **Minimise email fallback** for reservations
4. Keep up with **continuous API changes**

---

## Recommended Approach for Keystay

### Option A: White-Label Channel Manager (Recommended for MVP)

Partner with an established channel manager and white-label their connectivity:

| Provider | Pricing Model | SA Support | Best For |
|----------|---------------|------------|----------|
| **Guesty** | Per-listing/month | Yes | Scale operations (20+ units) |
| **Hostaway** | Per-listing/month | Limited | Mid-market |
| **Lodgify** | Subscription | Limited | Smaller portfolios |
| **NightsBridge** | Per-booking | Yes (SA-based) | SA-focused, LekkeSlaap |

**Pros:**
- Immediate access to Airbnb, Booking.com, Vrbo
- No API partnership required
- Proven, tested integrations
- Ongoing maintenance handled by provider

**Cons:**
- Per-listing fees reduce margins
- Less control over user experience
- Dependency on third party

### Option B: Build via Channel Manager API

Use a channel manager's API to build Keystay-branded experience:

```
Owner Dashboard (Keystay)
         │
         ▼
   Guesty/Hostaway API
         │
         ├──▶ Airbnb
         ├──▶ Booking.com
         └──▶ Vrbo
```

**Pros:**
- Keystay-branded experience
- Single integration point
- Access to all major OTAs

**Cons:**
- Development effort required
- Still paying channel manager fees
- API learning curve

### Option C: Direct Partnership (Long-Term)

Apply for direct Airbnb/Booking.com partnership once Keystay has scale:

**Requirements:**
- Significant property portfolio (1,000+ units typically)
- Dedicated tech team
- PCI/PII compliance infrastructure
- Track record of quality service

**Timeline:** 18-24 months minimum to qualify

---

## South African Platforms

### NightsBridge (SA-Based)

NightsBridge is a local channel manager with strong SA OTA connections:

- **LekkeSlaap** — Direct integration
- **SafariNow** — Direct integration
- **Booking.com** — Connectivity partner
- **Airbnb** — Via iCal (limited)

**Consideration:** Good for SA-focused properties, less suitable for Airbnb-heavy strategy.

### LekkeSlaap Direct

LekkeSlaap offers direct API integration for property managers:

- Lower commission than Airbnb
- Strong in SA leisure market
- Afrikaans-speaking guest base
- Less tech-sophisticated travellers

---

## Cost Analysis

### Channel Manager Costs (Typical)

| Provider | Monthly Cost (per listing) | Setup | Notes |
|----------|---------------------------|-------|-------|
| Guesty | $8-15 | $0 | Volume discounts available |
| Hostaway | $10-20 | $0 | Includes PMS features |
| Lodgify | $5-12 | $0 | Annual billing discount |
| NightsBridge | R150-300 | R500 | SA pricing |

### Impact on Unit Economics

For a R10,000/month rental property:

| Scenario | Gross | Platform Fee | Channel Mgr | Net to Keystay |
|----------|-------|--------------|-------------|----------------|
| Long-term only | R10,000 | R0 | R0 | R10,000 |
| STR via Airbnb | R15,000 | R450 (3%) | R200 | R14,350 |
| STR via Booking | R15,000 | R2,250 (15%) | R200 | R12,550 |

**Key Insight:** Even with platform and channel manager fees, STR can generate 30-50% more gross revenue than long-term rental.

---

## Implementation Roadmap

### Phase 1: MVP (Month 1-3)

1. **Partner with NightsBridge or Guesty** for channel connectivity
2. **Manual listing management** via partner dashboard
3. **Focus on LekkeSlaap + Airbnb** (highest SA demand)

### Phase 2: Integration (Month 4-6)

1. **API integration** with channel manager
2. **Unified dashboard** showing all bookings
3. **Automated pricing** rules

### Phase 3: Scale (Month 7-12)

1. **Direct Booking.com** partnership application
2. **Guest communication** automation
3. **Dynamic pricing** integration (PriceLabs, Wheelhouse)

### Phase 4: Independence (Year 2+)

1. **Airbnb Preferred Partner** application (if scale justifies)
2. **Own booking engine** for direct bookings
3. **Reduced dependency** on OTAs

---

## Key Decisions for Keystay

| Decision | Options | Recommendation |
|----------|---------|----------------|
| Channel manager | Guesty / Hostaway / NightsBridge | **Guesty** (best Airbnb integration) |
| Primary OTA | Airbnb / Booking.com | **Airbnb** (lower commission, higher rates) |
| Secondary OTA | Booking.com / LekkeSlaap | **LekkeSlaap** (SA-focused, lower commission) |
| Build vs Buy | Custom integration / White-label | **White-label first**, build later |

---

## Sources

- [Airbnb API Guide 2026](https://bnbmanagementlondon.co.uk/airbnb-api/)
- [Airbnb 2025 Preferred Software Partners](https://news.airbnb.com/announcing-our-2025-preferred-software-partners/)
- [Booking.com Connectivity APIs](https://developers.booking.com/connectivity/docs)
- [Booking.com Partner Requirements](https://connectivity.booking.com/s/article/Requirements-for-becoming-a-Booking-com-Connectivity-Partner)
- [Elfsight: How to use Airbnb API](https://elfsight.com/blog/how-to-get-and-use-airbnb-api-partnership-and-integration/)
- [Elfsight: How to use Booking.com API](https://elfsight.com/blog/how-to-get-and-use-booking-com-api-partnership-and-integration/)

---

*Document version: 1.0*
*Last updated: 21 January 2026*
