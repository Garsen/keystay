# Keystay: Unit Economics & Financial Model

**Date:** 21 January 2026
**Purpose:** Define the unit economics for Keystay's property investment platform
**Status:** Working model — assumptions to be validated

---

## Executive Summary

This document defines the unit economics for Keystay — what it costs, what we charge, and what we make at different scales. The model is designed for a **joint venture** where Keystay and an operating partner share revenue and costs.

---

## The Unit: One Property

Everything in Keystay's model revolves around **one property under management**. This is our unit of measurement.

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                        THE KEYSTAY UNIT: ONE PROPERTY                            │
├─────────────────────────────────────────────────────────────────────────────────┤
│                                                                                  │
│   REVENUE EVENTS                          RECURRING REVENUE                      │
│   ──────────────                          ─────────────────                      │
│                                                                                  │
│   ┌─────────────────┐                    ┌─────────────────┐                    │
│   │ Property        │                    │ Management Fee  │                    │
│   │ Sourcing        │                    │ (Monthly)       │                    │
│   │ Fee (once)      │                    │                 │                    │
│   └────────┬────────┘                    └────────┬────────┘                    │
│            │                                      │                             │
│            │                                      │                             │
│   ┌────────▼────────┐                    ┌────────▼────────┐                    │
│   │ Tenant          │                    │ Maintenance     │                    │
│   │ Placement       │                    │ Coordination    │                    │
│   │ Fee (per tenant)│                    │ (per job)       │                    │
│   └─────────────────┘                    └─────────────────┘                    │
│                                                                                  │
│                                                                                  │
│   ONCE-OFF              ANNUAL              MONTHLY           PER-EVENT         │
│   ────────              ──────              ───────           ─────────         │
│   Sourcing fee          Placement fee       Management fee    Maintenance       │
│   (at purchase)         (new tenants)       (ongoing)         markup            │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

---

## Property Assumptions

### Reference Property

For modelling purposes, we use a **reference property**:

| Attribute | Value | Notes |
|-----------|-------|-------|
| Purchase Price | R1,000,000 | Entry-level investment property |
| Monthly Rent (Long-term) | R8,000 | ~9.6% gross yield |
| Monthly Revenue (STR) | R12,000 | ~14.4% gross yield (60% occupancy) |
| Location | Gauteng | Pretoria, Centurion, Midrand |
| Type | 2-bed apartment | Sectional title |

### Property Tiers

| Tier | Price Range | Monthly Rent | Typical Yield |
|------|-------------|--------------|---------------|
| Entry | R500k - R800k | R5,000 - R7,000 | 10-12% |
| Mid | R800k - R1.2M | R7,000 - R10,000 | 9-10% |
| Premium | R1.2M - R2M | R10,000 - R15,000 | 8-9% |
| Luxury | R2M+ | R15,000+ | 6-8% |

---

## Fee Structure

### Keystay Fees

| Fee | Amount | When Charged | Who Pays |
|-----|--------|--------------|----------|
| **Sourcing Fee** | 3% of purchase price | At property purchase | Buyer (investor) |
| **Placement Fee** | 1 month rent | Per new tenant | Owner (from rent) |
| **Management Fee** | 8% of rent collected | Monthly | Owner (from rent) |
| **Maintenance Markup** | 15% of job cost | Per maintenance job | Owner |
| **Renewal Fee** | 50% of placement fee | Per lease renewal | Owner |

### Fee Comparison (Market)

| Service | Keystay | IGrow | Traditional Agent |
|---------|---------|-------|-------------------|
| Sourcing | 3% | 5%+ | 0% (no sourcing) |
| Placement | 1 month | 1 month | 1 month |
| Management | 8% | 8-10% | 10-12% |
| Maintenance | 15% markup | Unknown | 10-20% markup |

---

## Unit Economics: Long-Term Rental

### Per Property (R1M property, R8,000/month rent)

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                 UNIT ECONOMICS: LONG-TERM RENTAL (YEAR 1)                        │
├─────────────────────────────────────────────────────────────────────────────────┤
│                                                                                  │
│   ONCE-OFF REVENUE (At Purchase)                                                │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Sourcing Fee (3% of R1,000,000)                              R30,000          │
│                                                                                  │
│   ONCE-OFF REVENUE (Year 1)                                                     │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Placement Fee (1 month rent)                                  R8,000          │
│                                                                                  │
│   RECURRING REVENUE (Monthly)                                                   │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Gross Rent Collected                                          R8,000          │
│   Management Fee (8%)                                             R640          │
│   Average Maintenance Coordination (estimate)                     R150          │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Monthly Recurring Revenue                                       R790          │
│                                                                                  │
│   ANNUAL SUMMARY (YEAR 1)                                                       │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Sourcing Fee                                                 R30,000          │
│   Placement Fee                                                 R8,000          │
│   Management Fees (R640 x 12)                                   R7,680          │
│   Maintenance Coordination (R150 x 12)                          R1,800          │
│   ─────────────────────────────────────────────────────────────────────────     │
│   TOTAL YEAR 1 REVENUE                                        R47,480          │
│                                                                                  │
│   YEAR 2+ (No sourcing fee, assume 1 placement every 2 years)                   │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Management Fees                                               R7,680          │
│   Maintenance Coordination                                      R1,800          │
│   Renewal Fee (every 2 years, so R2,000/year average)           R2,000          │
│   ─────────────────────────────────────────────────────────────────────────     │
│   TOTAL YEAR 2+ REVENUE                                       R11,480          │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

### 5-Year Customer Lifetime Value (Long-Term Rental)

| Year | Sourcing | Placement | Management | Maintenance | Total |
|------|----------|-----------|------------|-------------|-------|
| 1 | R30,000 | R8,000 | R7,680 | R1,800 | R47,480 |
| 2 | - | - | R7,680 | R1,800 | R9,480 |
| 3 | - | R8,000 | R7,680 | R1,800 | R17,480 |
| 4 | - | - | R7,680 | R1,800 | R9,480 |
| 5 | - | R8,000 | R7,680 | R1,800 | R17,480 |
| **Total** | **R30,000** | **R24,000** | **R38,400** | **R9,000** | **R101,400** |

**5-Year LTV: R101,400 per property**

---

## Unit Economics: Short-Term Rental (Airbnb)

### Per Property (R1M property, R12,000/month gross via Airbnb)

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                 UNIT ECONOMICS: SHORT-TERM RENTAL (YEAR 1)                       │
├─────────────────────────────────────────────────────────────────────────────────┤
│                                                                                  │
│   ASSUMPTIONS                                                                   │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Average Daily Rate (ADR):          R800                                       │
│   Occupancy Rate:                    60%                                        │
│   Nights Booked/Month:               18                                         │
│   Gross Monthly Revenue:             R14,400                                    │
│   Booking Channel:                   70% Airbnb, 30% Direct                     │
│                                                                                  │
│   MONTHLY REVENUE CALCULATION                                                   │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Gross Booking Revenue                                        R14,400          │
│                                                                                  │
│   DEDUCTIONS (Before Keystay gets paid)                                         │
│   - Airbnb Host Fee (3% on 70%)                                  (R302)         │
│   - Channel Manager                                              (R200)         │
│   - Cleaning (R400 x 4 turnovers)                              (R1,600)         │
│   - Utilities (higher for STR)                                   (R800)         │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Net Distributable Revenue                                    R11,498          │
│                                                                                  │
│   KEYSTAY FEES                                                                  │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Management Fee (15% for STR)                                  R1,725          │
│   Maintenance Coordination                                        R200          │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Monthly Recurring Revenue                                     R1,925          │
│                                                                                  │
│   TO OWNER                                                                      │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Net to Owner                                                  R9,573          │
│   (vs R7,360 for long-term after management fee)                               │
│                                                                                  │
│   ANNUAL SUMMARY (YEAR 1)                                                       │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Sourcing Fee                                                 R30,000          │
│   Management Fees (R1,725 x 12)                                R20,700          │
│   Maintenance Coordination (R200 x 12)                          R2,400          │
│   ─────────────────────────────────────────────────────────────────────────     │
│   TOTAL YEAR 1 REVENUE                                        R53,100          │
│                                                                                  │
│   YEAR 2+ REVENUE                                              R23,100          │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

### 5-Year LTV Comparison

| Model | Year 1 | Year 2-5 | 5-Year LTV |
|-------|--------|----------|------------|
| **Long-Term Rental** | R47,480 | R53,920 | R101,400 |
| **Short-Term Rental** | R53,100 | R92,400 | R145,500 |
| **Difference** | +R5,620 | +R38,480 | **+R44,100** |

**STR generates 44% more revenue over 5 years**, but requires more operational effort.

---

## Cost Structure

### Fixed Costs (Monthly)

| Cost Category | Amount | Notes |
|---------------|--------|-------|
| **Platform/Software** | | |
| - Channel Manager (Guesty) | R3,000 | Base subscription |
| - Accounting (Xero) | R500 | |
| - CRM (HubSpot) | R0 | Free tier initially |
| **Operations** | | |
| - Office/Admin | R5,000 | Shared with partner |
| - Insurance | R2,000 | Professional indemnity |
| - Compliance (PPRA) | R500 | Amortised annual |
| **Marketing** | | |
| - Website/SEO | R1,500 | |
| - Paid Ads | R2,500 | Variable |
| **Total Fixed** | **R15,000** | Per month |

### Variable Costs (Per Property)

| Cost Category | Long-Term | Short-Term | Notes |
|---------------|-----------|------------|-------|
| Channel Manager | R0 | R200/mo | Per-listing fee |
| Tenant Screening | R150/placement | N/A | Credit checks |
| Guest Communication | N/A | R100/mo | Automated messaging |
| Photography | R500/once | R1,000/once | Professional photos |
| Listing Setup | 2 hours | 4 hours | Staff time |

---

## Break-Even Analysis

### Monthly Break-Even

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                           BREAK-EVEN ANALYSIS                                    │
├─────────────────────────────────────────────────────────────────────────────────┤
│                                                                                  │
│   FIXED COSTS                                                                   │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Monthly Fixed Costs                                          R15,000          │
│                                                                                  │
│   REVENUE PER PROPERTY (Monthly Recurring Only)                                 │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Long-Term: R640 management + R150 maintenance =                R790          │
│   Short-Term: R1,725 management + R200 maintenance =           R1,925          │
│   Blended (70% LT, 30% STR):                                   R1,131          │
│                                                                                  │
│   BREAK-EVEN (Recurring Revenue Only)                                           │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Properties needed = R15,000 / R1,131 =                    14 properties       │
│                                                                                  │
│   WITH SOURCING FEES (Assuming 2 new properties/month)                          │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Monthly sourcing revenue: 2 x R30,000 =                      R60,000          │
│   Monthly placement revenue: 2 x R8,000 =                      R16,000          │
│   Once-off revenue per month:                                  R76,000          │
│                                                                                  │
│   Break-even with once-off fees:                            From Day 1          │
│   (Once-off fees cover fixed costs during growth phase)                         │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

### Path to Profitability

| Milestone | Properties | Monthly Recurring | Monthly Once-Off | Total | Status |
|-----------|------------|-------------------|------------------|-------|--------|
| Launch | 0 | R0 | R0 | R0 | (R15,000) loss |
| Month 3 | 6 | R6,786 | R76,000 | R82,786 | Profitable |
| Month 6 | 15 | R16,965 | R76,000 | R92,965 | Profitable |
| Month 12 | 30 | R33,930 | R38,000 | R71,930 | Profitable |
| Month 18 | 50 | R56,550 | R38,000 | R94,550 | Profitable |
| Month 24 | 75 | R84,825 | R38,000 | R122,825 | Strong |

**Note:** Assumes 2 new properties/month initially, slowing to 1/month after Year 1 as focus shifts to management quality.

---

## Revenue Split (JV)

### Proposed Structure

| Revenue Type | Keystay | Operating Partner | Notes |
|--------------|---------|-------------------|-------|
| Sourcing Fee | 50% | 50% | Both contributed to sale |
| Placement Fee | 30% | 70% | Partner does the work |
| Management Fee | 50% | 50% | Shared ongoing |
| Maintenance Markup | 30% | 70% | Partner coordinates |

### Alternative: Simple 50/50

All revenue split 50/50 after direct costs. Simpler to manage.

---

## Scenario Analysis

### Conservative (Slow Growth)

| Metric | Year 1 | Year 2 | Year 3 |
|--------|--------|--------|--------|
| Properties Added | 15 | 20 | 25 |
| Total Properties | 15 | 35 | 60 |
| Sourcing Revenue | R450k | R600k | R750k |
| Recurring Revenue | R142k | R475k | R814k |
| **Total Revenue** | **R592k** | **R1.08M** | **R1.56M** |
| Fixed Costs | R180k | R240k | R300k |
| Variable Costs | R45k | R105k | R180k |
| **EBITDA** | **R367k** | **R735k** | **R1.08M** |
| EBITDA Margin | 62% | 68% | 69% |

### Base Case (Moderate Growth)

| Metric | Year 1 | Year 2 | Year 3 |
|--------|--------|--------|--------|
| Properties Added | 20 | 35 | 50 |
| Total Properties | 20 | 55 | 105 |
| Sourcing Revenue | R600k | R1.05M | R1.5M |
| Recurring Revenue | R189k | R746k | R1.42M |
| **Total Revenue** | **R789k** | **R1.80M** | **R2.92M** |
| Fixed Costs | R180k | R300k | R420k |
| Variable Costs | R60k | R165k | R315k |
| **EBITDA** | **R549k** | **R1.34M** | **R2.19M** |
| EBITDA Margin | 70% | 74% | 75% |

### Aggressive (Fast Growth)

| Metric | Year 1 | Year 2 | Year 3 |
|--------|--------|--------|--------|
| Properties Added | 30 | 60 | 100 |
| Total Properties | 30 | 90 | 190 |
| Sourcing Revenue | R900k | R1.8M | R3M |
| Recurring Revenue | R284k | R1.22M | R2.57M |
| **Total Revenue** | **R1.18M** | **R3.02M** | **R5.57M** |
| Fixed Costs | R240k | R420k | R600k |
| Variable Costs | R90k | R270k | R570k |
| **EBITDA** | **R850k** | **R2.33M** | **R4.4M** |
| EBITDA Margin | 72% | 77% | 79% |

---

## Key Metrics to Track

### Property Metrics

| Metric | Formula | Target |
|--------|---------|--------|
| Gross Yield | Annual Rent / Purchase Price | >9% |
| Net Yield | (Annual Rent - Costs) / Purchase Price | >7% |
| Occupancy (STR) | Nights Booked / Available Nights | >65% |
| Tenant Retention | Tenants Renewed / Total Tenants | >70% |
| Maintenance Ratio | Maintenance Cost / Rent | <10% |

### Business Metrics

| Metric | Formula | Target |
|--------|---------|--------|
| CAC | Total Acquisition Cost / Properties Added | <R5,000 |
| LTV | 5-Year Revenue per Property | >R100,000 |
| LTV:CAC | LTV / CAC | >20:1 |
| Monthly Recurring Revenue | Management + Maintenance | Track growth |
| Revenue per Property | Total Revenue / Properties | >R3,000/mo (Y1) |
| EBITDA Margin | EBITDA / Revenue | >60% |

---

## Sensitivity Analysis

### Impact of Fee Changes

| Fee Change | Revenue Impact | Notes |
|------------|----------------|-------|
| Sourcing 3% → 2% | -R10k per property | Lose R200k/year at 20 properties |
| Management 8% → 10% | +R160/property/month | +R38k/year at 20 properties |
| STR Management 15% → 12% | -R432/property/month | -R5k/year per STR property |

### Impact of Mix Changes

| STR Mix | Blended Monthly Revenue | 5-Year LTV |
|---------|------------------------|------------|
| 0% (all LT) | R790 | R101,400 |
| 30% | R1,131 | R114,630 |
| 50% | R1,358 | R123,450 |
| 70% | R1,584 | R132,270 |
| 100% (all STR) | R1,925 | R145,500 |

---

## Startup Costs (Self-Funded)

This is a **bootstrapped venture** — both partners contribute their own capital. No external funding.

### Estimated Startup Costs

| Category | Estimate | Priority | Notes |
|----------|----------|----------|-------|
| Platform MVP | R100k - R150k | P0 | Start lean, iterate based on feedback |
| Legal/Compliance | R30k - R50k | P0 | JV entity, contracts, PPRA alignment |
| Marketing | R50k - R100k | P1 | Website, initial content, campaigns |
| Working Capital | Variable | P1 | Bridge until cash flow positive |

### Why This Works Bootstrapped

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                         CASH FLOW FROM DAY 1                                     │
├─────────────────────────────────────────────────────────────────────────────────┤
│                                                                                  │
│   Property 1 closed:                                                            │
│   • Sourcing fee (3% of R1M)                              R30,000               │
│   • Placement fee (1 month rent)                           R8,000               │
│   ─────────────────────────────────────────────────────────────────────────     │
│   Immediate cash from first property:                     R38,000               │
│                                                                                  │
│   2 properties/month = R76,000/month in once-off fees                           │
│   This covers fixed costs (R15k/month) almost immediately                       │
│                                                                                  │
│   The business is cash-generative from the start.                               │
│   Startup capital is primarily for platform build + legal setup.                │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

---

## Model Assumptions & Risks

### Key Assumptions

| Assumption | Value | Risk if Wrong |
|------------|-------|---------------|
| Average property price | R1,000,000 | Lower = lower sourcing fees |
| Monthly rent (LT) | R8,000 | Lower = lower management fees |
| STR occupancy | 60% | Lower = lower STR revenue |
| Tenant turnover | 2 years | Higher = more placement fees |
| Properties/month | 2 | Lower = slower growth |

### Risk Mitigation

| Risk | Impact | Mitigation |
|------|--------|------------|
| Slow property acquisition | Low revenue | Focus on partner deal flow |
| STR regulation changes | Lose STR revenue | Diversify to LT |
| Partner conflict | Business disruption | Clear JV agreement |
| Market downturn | Lower property prices | Focus on cash flow, not capital gains |

---

## Next Steps

1. **Validate assumptions** with operating partner candidates
2. **Test fee structure** with target customers (property buyers)
3. **Build financial model spreadsheet** for scenario planning
4. **Define MVP scope** based on economics
5. **Set up tracking** for key metrics from Day 1

---

## Related Documents

| Document | Contents |
|----------|----------|
| [venture-plan.md](venture-plan.md) | Business model overview |
| [SHORT-TERM-RENTAL-INTEGRATIONS.md](SHORT-TERM-RENTAL-INTEGRATIONS.md) | STR platform costs and integration |
| [PARTNER-ECOSYSTEM.md](PARTNER-ECOSYSTEM.md) | Partner roles and money flow |

---

*Document version: 1.0*
*Last updated: 21 January 2026*
