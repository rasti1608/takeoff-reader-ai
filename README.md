# TakeOff Pro AI
## Intelligent Construction Estimating Platform
### Product Vision Document

---

## Executive Summary

**TakeOff Pro AI** is an AI-powered construction estimating platform that automates material takeoffs from PDF blueprints, satellite imagery, and property photos. Built for roofing, siding, stucco, masonry, and exterior contractors who are tired of manual measurements and overpriced per-report services.

**The Problem:** Contractors waste hours with rulers on printed blueprints, or pay $15-87 per property for satellite measurement services like EagleView. Small-to-mid contractors (5-50 employees) are underserved—enterprise tools are too expensive and complex, while manual methods eat into profit margins.

**The Solution:** Upload a PDF or enter an address. AI does the rest. Get accurate material quantities, pitch-adjusted calculations, and professional proposals in minutes—not hours. Flat monthly pricing means you can bid more jobs without per-report costs eating your margins.

---

## The Market Opportunity

### Current Landscape

| Competitor | Approach | Pricing | Limitations |
|------------|----------|---------|-------------|
| **EagleView** | Satellite/aerial imagery | $15-87 per report | Per-report cost adds up fast. No PDF support. New construction not available. |
| **Beam AI** | PDF blueprint automation | Enterprise pricing | 24-72 hour turnaround. QA overhead. Targets large contractors. |
| **HOVER** | Smartphone photos | Subscription | Requires site visit. Limited to existing structures. |
| **PlanSwift/Bluebeam** | Manual digital tracing | $1,500+ license | Still manual. Steep learning curve. |

### The Gap

Small-to-mid contractors—the guy with 10-50 employees doing residential and light commercial—have no good option:
- EagleView at $30/report × 30 jobs/month = $900/month just for measurements
- Enterprise AI tools require demos, contracts, minimums
- Manual takeoffs take 2-4 hours each

**Our Target:** The contractor who does 20-100 jobs per month and needs fast, accurate takeoffs without enterprise complexity or per-report gouging.

---

## Product Vision

### Three Input Methods, One Platform

```
┌─────────────────────────────────────────────────────────────────┐
│                      TAKEOFF PRO AI                             │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   ┌─────────────┐   ┌─────────────┐   ┌─────────────┐           │
│   │   ADDRESS   │   │  PDF/PLANS  │   │   PHOTOS    │           │
│   │   LOOKUP    │   │   UPLOAD    │   │   UPLOAD    │           │
│   └──────┬──────┘   └──────┬──────┘   └──────┬──────┘           │
│          │                 │                 │                  │
│          ▼                 ▼                 ▼                  │
│   ┌─────────────┐   ┌─────────────┐   ┌─────────────┐           │
│   │  Satellite  │   │  AI Vision  │   │  AI Vision  │           │
│   │  Imagery    │   │  Blueprint  │   │  Photo      │           │
│   │  Analysis   │   │  Analysis   │   │  Analysis   │           │
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

## Input Method Details

### 1. Address Lookup (Satellite/Aerial)

**Use Case:** Existing properties where you need quick measurements without a site visit.

**How It Works:**
- Enter property address
- System pulls satellite/aerial imagery
- AI identifies roof planes, edges, features
- Calculates areas with pitch estimation (from shadow analysis or standard assumptions)
- Outputs material quantities

**Best For:**
- Residential re-roofing
- Insurance estimates
- Quick preliminary bids
- Storm damage assessment

**Limitations:**
- Cannot see under tree cover
- Pitch estimation less precise than blueprints
- New construction not available (no imagery yet)

### 2. PDF Blueprint Upload

**Use Case:** New construction or renovation projects where architectural drawings are available.

**How It Works:**
- Upload PDF blueprint set (can be 1 page or 100+ pages)
- AI scans all pages to find:
  - **Scale notation** (1/4" = 1'-0", 1:50, etc.)
  - **Roof plan** (top-down view showing all planes)
  - **Elevations** (side views showing pitch)
  - **Details** (flashing, drainage, penetrations)
- AI measures dimensions using the detected scale
- Pitch extracted from elevation drawings or explicit notation
- Applies pitch multiplier to convert flat area to actual surface area
- Calculates all material quantities

**Scale Detection:**
The AI looks for scale in common locations:
- Title block (bottom right of each sheet)
- Near the drawing itself
- Cover sheet / index
- Explicit notation like "SCALE: 1/4" = 1'-0""

If scale cannot be found, user is prompted to:
- Manually enter the scale, OR
- Provide a known dimension for calibration

**Pitch Calculation:**
Pitch (roof slope) is critical for accurate material calculation. A 12:12 pitch roof has 41% more surface area than the same footprint measured flat.

The AI finds pitch from:
- Explicit notation on plans (e.g., "6:12 PITCH")
- Roof pitch symbols (triangle with rise/run)
- Calculated from elevation drawings (rise ÷ run)
- Section details showing rafter angles

| Pitch | Multiplier | Common Use |
|-------|------------|------------|
| Flat (0:12) | 1.000 | Commercial flat roofs |
| 2:12 | 1.014 | Low slope |
| 4:12 | 1.054 | Standard residential |
| 6:12 | 1.118 | Common residential |
| 8:12 | 1.202 | Steeper residential |
| 10:12 | 1.302 | Steep |
| 12:12 | 1.414 | Very steep |

**Best For:**
- New construction
- Major renovations
- Commercial projects
- Accurate bidding

### 3. Photo Upload (Future Phase)

**Use Case:** Existing structures where you have site photos but no drawings.

**How It Works:**
- Upload multiple photos of the structure
- AI analyzes geometry from multiple angles
- Estimates dimensions and pitch
- User can add reference measurements for calibration

**Best For:**
- Siding replacement
- Stucco/stone veneer
- Smaller residential jobs
- When blueprints don't exist

---

## Supported Trades

### Phase 1: Roofing (Launch)

**Materials Calculated:**
- Shingles / squares (with waste factor)
- Underlayment / felt (with overlap)
- Drip edge (linear feet)
- Starter strip
- Ridge cap / hip cap
- Flashing (step, counter, valley)
- Ice & water shield
- Vents (ridge, box, turbine)
- Pipe boots / penetration flashings
- Nails / fasteners

**Special Calculations:**
- Pitch-adjusted square footage
- Valley lengths
- Hip lengths
- Ridge lengths
- Rake/gable lengths
- Eave lengths
- Headwall/sidewall flashings

### Phase 2: Siding & Exterior

**Siding Types:**
- Vinyl siding
- Fiber cement (HardiePlank)
- Wood siding
- Metal panels
- Composite

**Materials Calculated:**
- Siding squares
- J-channel
- Starter strip
- Corner posts (inside/outside)
- Window/door trim
- Soffit
- Fascia
- Gutters & downspouts

**Deductions:**
- Windows (automated detection)
- Doors (automated detection)
- Other openings

### Phase 3: Masonry & Stone

**Types:**
- Brick veneer
- Stone veneer
- Thin brick
- Stucco/EIFS
- Concrete block

**Materials Calculated:**
- Square footage of coverage
- Mortar/adhesive quantities
- Lath/scratch coat materials
- Corner pieces
- Trim pieces
- Weep screed
- Control joints

### Future Phases

- Concrete flatwork
- Framing lumber
- Insulation
- Drywall/sheetrock
- Flooring
- Painting
- Fencing

---

## User Experience

### Simple Workflow

```
┌─────────────────────────────────────────────────────────────┐
│  STEP 1: Start New Project                                  │
│  ┌─────────────────────────────────────────────────────┐    │
│  │  Project Name: Smith Residence Re-Roof              │    │
│  │  Address: 123 Main St, Anytown, USA                 │    │
│  │                                                     │    │
│  │  Input Method:                                      │    │
│  │  [Address Lookup] [Upload PDF] [Upload Photos]      │    │
│  └─────────────────────────────────────────────────────┘    │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│  STEP 2: AI Processing                                      │
│  ┌─────────────────────────────────────────────────────┐    │
│  │  ✓ Scale detected: 1/4" = 1'-0"                      │   │
│  │  ✓ Roof plan found on page 4                         │   │
│  │  ✓ Elevations found on pages 7-10                    │   │
│  │  ✓ Pitch identified: 6:12 (main), 4:12 (porch)       │   │
│  │  ⟳ Calculating areas...                             │   │
│  └─────────────────────────────────────────────────────┘   │
└────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌────────────────────────────────────────────────────────────┐
│  STEP 3: Review & Adjust                                   │
│  ┌─────────────────────────────────────────────────────┐   │
│  │  ROOF SUMMARY                                       │   │
│  │  ─────────────────────────────────────────────────  │   │
│  │  Flat Area:        2,450 sq ft                      │   │
│  │  Pitch-Adjusted:   2,739 sq ft (6:12 = 1.118×)      │   │
│  │  Total Squares:    28.5 squares                     │   │
│  │                                                     │   │
│  │  [Edit] if something looks wrong                    │   │
│  └─────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│  STEP 4: Download                                           │
│  ┌─────────────────────────────────────────────────────┐    │
│  │                                                     │    │
│  │  [Download Excel]  [Download PDF Proposal]          │    │
│  │                                                     │    │
│  │  [Save to My Projects]  [Share Link]                │    │
│  └─────────────────────────────────────────────────────┘    │
└─────────────────────────────────────────────────────────────┘
```

### What If Something Is Missing?

**No Scale Found:**
```
┌─────────────────────────────────────────────────────────────┐
│  ⚠️  Scale Not Detected                                      │
│                                                             │
│  We couldn't find a scale notation in your PDF.             │
│                                                             │
│  Options:                                                   │
│  1. Enter scale manually: [1/4" = 1'-0" ▼]                  │
│  2. Enter a known dimension for calibration                 │
│  3. Request clarification from architect                    │
│                                                             │
│  [Continue with Manual Entry]  [Upload Different PDF]       │
└─────────────────────────────────────────────────────────────┘
```

**No Pitch Found:**
```
┌─────────────────────────────────────────────────────────────┐
│  ⚠️  Roof Pitch Not Detected                                 │
│                                                             │
│  We couldn't determine the roof pitch from elevations.      │
│                                                             │
│  Common pitches:                                            │
│  ○ 4:12 (gentle slope)                                      │
│  ○ 6:12 (standard residential)                              │
│  ○ 8:12 (steeper)                                           │
│  ○ Other: [___:12]                                          │
│                                                             │
│  [Apply Selected Pitch]                                     │
└─────────────────────────────────────────────────────────────┘
```

This mirrors exactly what a human estimator would do—if the information isn't on the plans, you either make an assumption, measure on site, or call the architect.

---

## Pricing Tiers

### Starter - $49/month
**For:** Solo contractors, small operations

- 10 takeoffs per month
- PDF uploads only
- Roofing trade only
- Excel export
- Email support

### Professional - $149/month
**For:** Growing contractors, small teams

- 50 takeoffs per month
- PDF + Address lookup
- Roofing + Siding
- Excel + PDF proposal export
- Project history & storage
- Priority support
- 2 team seats

### Business - $299/month
**For:** Established contractors, multiple estimators

- Unlimited takeoffs
- All input methods (PDF, Address, Photos)
- All trades
- All export formats
- Custom proposal templates
- Manufacturer API pricing integration
- Unlimited team seats
- Dedicated support
- API access for integrations

### Enterprise - Custom
**For:** Large contractors, franchises

- Everything in Business
- Custom integrations
- White-label options
- Volume discounts
- SLA guarantees
- On-boarding & training

---

## Competitive Advantages

### vs. EagleView ($15-87/report)

| Feature | EagleView | TakeOff Pro AI |
|---------|-----------|----------------|
| Pricing | Per report | Flat monthly  |
| PDF Support | ❌ | ✅ |
| New Construction | ❌ | ✅ |
| Turnaround | Hours | Minutes |
| Trades | Roofing/Siding | Expanding |
| Team Access | Extra cost | Included |

**At 30 jobs/month:**
- EagleView: $450-900/month
- TakeOff Pro: $149/month (Professional)

### vs. Beam AI (Enterprise)

| Feature | Beam AI | TakeOff Pro AI |
|---------|---------|----------------|
| Target | Large contractors | All sizes |
| Turnaround | 24-72 hours | Minutes |
| Pricing | Per project | Flat monthly |
| Self-service | No (requires QA team) | Yes |
| Sales process | Demo required | Sign up instantly |

### vs. Manual (Ruler & Paper)

| Factor | Manual | TakeOff Pro AI |
|--------|--------|----------------|
| Time per takeoff | 2-4 hours | 5-10 minutes |
| Accuracy | Human error prone | Consistent |
| Scaling | Hire more estimators | Same team, more bids |
| Storage | Filing cabinets | Cloud searchable |

---

## Technical Approach

### AI Vision Processing

Modern AI vision models can:
- Read text from blueprints (OCR)
- Understand drawing conventions
- Measure scaled dimensions
- Identify architectural symbols
- Recognize roof planes, walls, openings

The same technology that lets AI describe a photograph can read a blueprint and extract measurements—it just needs the right instructions.

### Accuracy Commitment

- **95%+ accuracy target** on standard drawings
- Clear indication when confidence is lower
- Always allow manual override
- Feedback loop to improve over time

### When AI Can't Help

We're honest about limitations:
- Severely degraded or hand-drawn plans may need manual assist
- Unusual scales require user input
- Complex multi-building commercial may need enterprise support

But if a competent human estimator could read the plans, so can our AI.

---

## Roadmap

### Phase 1: Foundation (Months 1-3)
- ✅ PDF blueprint processing
- ✅ Roofing takeoffs
- ✅ Excel export
- ✅ User accounts & project storage
- ✅ Basic proposal PDF

### Phase 2: Expand Inputs (Months 4-6)
- Address/satellite lookup integration
- Photo upload processing
- Siding trade support
- Improved proposals with branding

### Phase 3: Scale (Months 7-12)
- Additional trades (stucco, masonry, stone)
- Manufacturer pricing APIs
- Team collaboration features
- Mobile app
- CRM integrations

### Phase 4: Intelligence (Year 2+)
- Historical pricing analytics
- Win rate optimization
- Material cost tracking
- Supplier integrations
- Automated ordering

---

## Why This Will Work

1. **The Technology Exists** - AI vision models are production-ready. Companies like EagleView and Beam AI prove the concept works. We're not inventing new AI—we're applying it better.

2. **The Market Is Underserved** - Small-to-mid contractors are stuck between expensive per-report services and tedious manual work. They need affordable automation.

3. **Simple Beats Complex** - Contractors want to upload and download, not learn complex software. We win by being dead simple.

4. **Flat Pricing Changes Behavior** - When there's no per-report cost, contractors bid more jobs. More bids = more wins = more subscription value.

5. **We Understand The Trade** - This isn't built by tech people guessing what contractors need. It's built with actual roofers, siders, and masons who know what a pitch multiplier is.

---

## The Ask

We're looking for:

1. **Real PDF blueprints** from completed jobs where you know the correct takeoff
2. **Your methodology** - how you read plans, what you look for, your calculations
3. **Feedback** on pricing, features, workflow
4. **Beta testers** when we launch

In return, you'll get:
- Input on exactly how this tool works
- Free access during beta
- Founding member pricing locked in
- A tool built for how YOU actually work

---

## Contact

**Project:** TakeOff Pro AI  
**Status:** In Development  
**Target Launch:** 2025

---

*This document represents our product vision. Features and pricing subject to change based on development and market feedback.*
