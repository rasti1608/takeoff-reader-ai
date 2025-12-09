# ![TakeoffReader AI](https://raw.githubusercontent.com/nonamedogai/TakeoffReaderAI/main/TakeoffReaderAI_logo.png)

# TakeoffReader AI
## Intelligent Construction Estimating Platform
### Product Vision Document

---

## Executive Summary

**TakeoffReader AI** is an AI-powered construction estimating platform that automates material takeoffs from aerial imagery, PDF blueprints, and on-site LiDAR scans. Built for roofing, siding, stucco, masonry, and exterior contractors who are tired of manual measurements and overpriced per-report services.

**The Problem:** Contractors waste hours with rulers on printed blueprints, or pay $15-87 per property for aerial measurement services like EagleView. Small-to-mid contractors (5-50 employees) are underserved—enterprise tools are too expensive and complex, while manual methods eat into profit margins.

**The Solution:** Enter an address, upload a PDF, or scan with your phone. AI does the rest. Get accurate material quantities, pitch-adjusted calculations, and professional proposals in minutes—not hours. Flat monthly pricing means you can bid more jobs without per-report costs eating your margins.

---

## Three Products, One Platform

TakeoffReader AI provides **complete exterior takeoff coverage** through three specialized products:

| Product | Input Source | Best For |
|---------|--------------|----------|
| **SkyReader** | Aerial/Satellite Imagery | Existing buildings, quick estimates without site visit |
| **PlanReader** | PDF Blueprints | New construction, renovations with drawings |
| **SiteReader** | iPhone LiDAR Scanning | Existing buildings without drawings, on-site capture |

```
┌─────────────────────────────────────────────────────────────────┐
│                    TAKEOFFREADER AI                             │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   ┌─────────────┐   ┌─────────────┐   ┌─────────────┐           │
│   │  SKYREADER  │   │ PLANREADER  │   │ SITEREADER  │           │
│   │   Address   │   │  PDF/Plans  │   │   iPhone    │           │
│   │   Lookup    │   │   Upload    │   │   LiDAR     │           │
│   └──────┬──────┘   └──────┬──────┘   └──────┬──────┘           │
│          │                 │                 │                  │
│          ▼                 ▼                 ▼                  │
│   ┌─────────────┐   ┌─────────────┐   ┌─────────────┐           │
│   │  EagleView  │   │  AI Vision  │   │   ARKit     │           │
│   │  Aerial     │   │  Blueprint  │   │   3D Scan   │           │
│   │  Imagery    │   │  Analysis   │   │   Analysis  │           │
│   └──────┬──────┘   └──────┬──────┘   └──────┬──────┘           │
│          │                 │                 │                  │
│          └─────────────────┼─────────────────┘                  │
│                            ▼                                    │
│                  ┌─────────────────┐                            │
│                  │  CALCULATION    │                            │
│                  │  ENGINE         │                            │
│                  │  - Pitch adjust │                            │
│                  │  - Materials    │                            │
│                  │  - Waste factor │                            │
│                  └────────┬────────┘                            │
│                           ▼                                     │
│                  ┌─────────────────┐                            │
│                  │  OUTPUT         │                            │
│                  │  - Excel        │                            │
│                  │  - PDF Proposal │                            │
│                  │  - Material List│                            │
│                  └─────────────────┘                            │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

---

## Product Details

### SkyReader — Aerial Takeoffs

**Use Case:** Existing properties where you need quick measurements without a site visit.

**How It Works:**
- Enter property address
- System pulls aerial imagery via EagleView API
- Returns roof measurements, pitch, facets, waste factors
- Wall measurements available (windows, doors, elevations)
- Calculates full material quantities

**Best For:**
- Residential re-roofing
- Siding replacement estimates
- Insurance estimates
- Quick preliminary bids
- Storm damage assessment

**Data Available:**
- Roof: Total area, pitch breakdown, facets, ridges, hips, valleys, eaves, rakes
- Walls: Wall area by elevation, window/door deductions
- Gutters: Eave measurements, downspout count

---

### PlanReader — Blueprint Takeoffs

**Use Case:** New construction or renovation projects where architectural drawings are available.

**How It Works:**
- Upload PDF blueprint set (1 to 500+ pages)
- AI scans all pages to identify relevant sheets
- Detects scale, pitch, dimensions automatically
- Extracts measurements using detected scale
- Applies pitch multiplier to convert flat area to actual surface area
- **4-Way Validation System** ensures <2% variance

**Best For:**
- New construction
- Major renovations
- Commercial projects
- Accurate competitive bidding

**Key Feature — Accuracy Validation System:**
- Phase 1: AI flags estimated vs. verified dimensions
- Phase 2: User confirms uncertain values (30-second interaction)
- Phase 3: 4 parallel calculations validate consistency
- Result: <2% variance, guaranteed

---

### SiteReader — LiDAR Takeoffs

**Use Case:** Existing structures where you have no drawings and need accurate measurements.

**How It Works:**
- Open companion iOS app on iPhone 12 Pro or newer
- Walk around building exterior
- LiDAR captures 3D point cloud
- Upload to TakeoffReader for AI processing
- Receive complete exterior takeoff

**Best For:**
- Older buildings without blueprints
- Additions/renovations to existing structures
- Siding and stucco replacement
- Quick on-site estimates

**Requirements:**
- iPhone 12 Pro or newer (LiDAR equipped)
- iOS companion app (free)
- TakeoffReader subscription

---

## The Market Opportunity

### Current Landscape

| Competitor | Approach | Pricing | Limitations |
|------------|----------|---------|-------------|
| **EagleView** | Aerial imagery | $15-87 per report | Per-report cost adds up. No PDF support. |
| **Beam AI** | PDF automation | Enterprise pricing | 24-72 hour turnaround. QA overhead. |
| **HOVER** | Smartphone photos | Subscription | Requires site visit. Limited accuracy. |
| **PlanSwift/Bluebeam** | Manual digital tracing | $1,500+ license | Still manual. Steep learning curve. |

### The Gap

Small-to-mid contractors—the guy with 10-50 employees doing residential and light commercial—have no good option:
- EagleView at $30/report × 30 jobs/month = $900/month just for measurements
- Enterprise AI tools require demos, contracts, minimums
- Manual takeoffs take 2-4 hours each

**TakeoffReader AI Target:** The contractor who does 20-100 jobs per month and needs fast, accurate takeoffs without enterprise complexity or per-report gouging.

---

## Supported Trades

### All Exterior Building Trades

| Trade Category | Specific Types |
|----------------|----------------|
| **Roofing** | Shingles, metal, tile, flat/membrane, slate |
| **Siding** | Vinyl, fiber cement (Hardie), wood, metal panels, composite |
| **Masonry** | Brick veneer, stone veneer, thin brick, concrete block |
| **Stucco/EIFS** | Traditional stucco, synthetic stucco, EIFS systems |
| **Concrete** | Flatwork, driveways, sidewalks, patios |
| **Gutters** | Seamless, sectional, gutter guards |

---

## Pricing Tiers

### Starter - $49/month
**For:** Solo contractors, small operations

- 10 takeoffs per month
- PlanReader (PDF) only
- Roofing + Siding trades
- Excel export
- Email support

### Professional - $149/month
**For:** Growing contractors, small teams

- 50 takeoffs per month
- PlanReader + SkyReader
- All exterior trades
- Excel + PDF proposal export
- Project history & storage
- Dual-AI verification
- Priority support
- 2 team seats

### Business - $299/month
**For:** Established contractors, multiple estimators

- Unlimited takeoffs
- All products (SkyReader, PlanReader, SiteReader)
- All trades
- All export formats
- Custom proposal templates
- Manufacturer pricing integration
- Unlimited team seats
- Dedicated support
- API access

---

## Competitive Advantages

### vs. EagleView ($15-87/report)

| Feature | EagleView | TakeoffReader AI |
|---------|-----------|------------------|
| Pricing | Per report | Flat monthly |
| PDF Support | ❌ | ✅ PlanReader |
| New Construction | ❌ | ✅ PlanReader |
| Turnaround | Hours | Minutes |
| Trades | Roofing/Siding | All Exterior |
| On-site capture | ❌ | ✅ SiteReader |

**At 30 jobs/month:**
- EagleView: $450-900/month
- TakeoffReader AI: $149/month (Professional)

### vs. Manual (Ruler & Paper)

| Factor | Manual | TakeoffReader AI |
|--------|--------|------------------|
| Time per takeoff | 2-4 hours | 5-10 minutes |
| Accuracy | Human error prone | <2% variance (validated) |
| Scaling | Hire more estimators | Same team, more bids |
| Storage | Filing cabinets | Cloud searchable |

---

## Technical Architecture

### Accuracy Validation System (PlanReader)

The core differentiator. While competitors run single AI calculations or require human QA review, TakeoffReader uses:

1. **Confidence Tracking** — AI explicitly flags estimated vs. verified dimensions
2. **User Confirmation** — Quick 30-second review of uncertain values
3. **4-Way Parallel Validation** — Four independent calculations must agree within 2%
4. **Statistical Verification** — Results averaged and validated before delivery

**Proven Results:**
- Testing showed 79% variance with uncontrolled dimensions
- With locked dimensions: <1% variance achieved
- Methodology documented and proprietary

### AI Engine

- **Primary:** Claude Opus 4.5 (only model that can visually measure from PDFs)
- **Verification:** Claude Sonnet 4.5 for dual-AI cross-check
- **Aerial Data:** EagleView API integration

---

## Domains

- **Primary:** takeoffreader.com
- **Alternative:** takeoffreader.ai

---

## Roadmap

### Phase 1: PlanReader MVP (Current)
- ✅ PDF blueprint processing
- ✅ Roofing + Siding takeoffs
- ✅ 4-Way Validation System
- ✅ Dual-AI verification
- ⬜ User accounts & billing
- ⬜ Report generation

### Phase 2: SkyReader
- ⬜ EagleView API integration (pending pricing confirmation)
- ⬜ Roof + Walls + Gutters from aerial
- ⬜ Address lookup workflow

### Phase 3: SiteReader
- ⬜ iOS companion app
- ⬜ LiDAR capture workflow
- ⬜ 3D scan processing pipeline

### Phase 4: Expansion
- ⬜ Additional trades (masonry, stucco, concrete)
- ⬜ Manufacturer pricing APIs
- ⬜ CRM integrations
- ⬜ Mobile app

---

## Contact

**Project:** TakeoffReader AI  
**Website:** takeoffreader.ai  
**Status:** In Development  
**Target Launch:** Q1 2026

---

*This document represents our product vision. Features and pricing subject to change based on development and market feedback.*
