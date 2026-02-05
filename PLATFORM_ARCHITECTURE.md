# Platform-First Architecture 🏗️

## Structure

```
~/GumRoad/
├── LemonSqueezy/               ← MASTER PROFILES (complete product DNA)
│   ├── CATEGORY_AI_LLM_TOOLS/
│   │   ├── 01_CLAUDE_INTEGRATION/
│   │   │   └── MASTER_PROFILE.md
│   │   ├── 02_GPT_WRAPPER/
│   │   │   └── MASTER_PROFILE.md
│   │   └── [... up to 8 products per category]
│   ├── CATEGORY_DEVELOPMENT_TOOLS/
│   └── [... 6 total categories]
│
├── Codester/                   ← INDIVIDUAL PRODUCTS (v1 & v2)
│   ├── CATEGORY_AI_LLM_TOOLS/
│   │   ├── 01_CLAUDE_INTEGRATION/
│   │   │   ├── v1.md (original, SEO-optimized)
│   │   │   └── v2.md (keyword variation)
│   │   ├── 02_GPT_WRAPPER/
│   │   │   ├── v1.md
│   │   │   └── v2.md
│   │   └── [... 8 products per category]
│   └── [... 6 total categories]
│
├── Gumroad/                    ← BUNDLES (v1 & v2)
│   ├── CATEGORY_AI_LLM_TOOLS/
│   │   ├── 01_BUNDLE/
│   │   │   ├── v1.md (original, narrative-driven)
│   │   │   └── v2.md (social proof variation)
│   │   └── [1 bundle per category]
│   └── [... 6 total categories]
│
├── Payhip/                     ← DIRECT SALES (v1 & v2)
│   └── [Same structure as Gumroad]
│
├── Sellfy/                     ← SUBSCRIPTIONS (v1 & v2)
│   └── [Same structure as Gumroad]
│
├── Scripts/                    ← SHARED ASSETS
│   ├── AI_LLM_TOOLS/
│   ├── DEVELOPMENT_TOOLS/
│   ├── Shared/ (global utilities)
│   └── [... per category]
│
└── [Strategy docs at root]
    ├── START_HERE.md
    ├── SYSTEM_OVERVIEW.txt
    ├── FEEDBACK_LOOP_SYSTEM.md
    └── [etc.]
```

## How It Works

### Step 1: Create Master Profile (LemonSqueezy)
- Write **ONE complete product definition** in `LemonSqueezy/CATEGORY_X/PRODUCT_N/MASTER_PROFILE.md`
- Includes: Scripts, features, target audiences, pricing logic, use cases, everything
- This is the SOURCE OF TRUTH for all platform variations

### Step 2: Generate Platform Variations
From the master, create platform-specific versions:

**Codester (Individual Products)**:
- `v1.md` = Original, marketplace-optimized (SEO title + feature-focused)
- `v2.md` = Keyword variation (e.g., "API Integration" vs "API Toolkit")

**Gumroad (Bundles)**:
- `v1.md` = Original, narrative-driven (problem → solution)
- `v2.md` = Social proof variation (testimonials + urgency)

**Payhip/Sellfy** (Direct Sales):
- `v1.md` = Payment/discount-focused
- `v2.md` = Scarcity/urgency variation

### Step 3: Deploy & Test
- Week 1: Deploy v1 across all platforms simultaneously
- Week 2-4: Collect metrics (CTR, conversions, email opens)
- Week 4+: Deploy v2 variations as A/B tests
- Track performance via `PERFORMANCE_LOG.csv` per product

## Data Flow

```
Master Profile (LemonSqueezy)
    ↓
    ├→ Codester v1 (marketplace discovery)
    ├→ Codester v2 (keyword test)
    ├→ Gumroad v1 (bundle narrative)
    ├→ Gumroad v2 (social proof test)
    ├→ Payhip v1 (payment focus)
    ├→ Payhip v2 (urgency)
    ├→ Sellfy v1 (subscription benefits)
    └→ Sellfy v2 (recurring messaging)
    
    ↓ All versions pull scripts from:
    
Scripts/ (shared assets)
```

## File Naming Convention

```
LemonSqueezy/CATEGORY_X/01_PRODUCT_NAME/
└── MASTER_PROFILE.md          (complete, source of truth)

Codester/CATEGORY_X/01_PRODUCT_NAME/
├── v1.md                       (original marketplace version)
└── v2.md                       (keyword/feature variation)

Gumroad/CATEGORY_X/01_BUNDLE/
├── v1.md                       (original bundle narrative)
└── v2.md                       (social proof variation)

[Payhip, Sellfy follow same pattern]

Scripts/CATEGORY_X/
└── [Actual tool files]
```

## Workflow

### For Each New Product:

1. **Write Master** (1-2 hours)
   - Create `LemonSqueezy/CATEGORY_X/01_PRODUCT/MASTER_PROFILE.md`
   - Complete product definition (everything)

2. **Generate v1s** (30 min)
   - Extract from master → `Codester/.../v1.md`
   - Extract from master → `Gumroad/.../v1.md`
   - Extract from master → `Payhip/.../v1.md`
   - Extract from master → `Sellfy/.../v1.md`

3. **Create v2s** (30 min)
   - `Codester/.../v2.md` (keyword variation)
   - `Gumroad/.../v2.md` (social proof)
   - `Payhip/.../v2.md` (discount angle)
   - `Sellfy/.../v2.md` (subscription benefits)

4. **Deploy & Track** (ongoing)
   - Launch all v1s Week 1
   - Monitor metrics
   - Deploy v2s Week 2+
   - Track PERFORMANCE_LOG.csv

## Platform Characteristics

| Platform | Role | Version 1 Angle | Version 2 Angle |
|----------|------|-----------------|-----------------|
| **LemonSqueezy** | Master | Complete profile | - |
| **Codester** | Discovery | SEO + features | Keywords |
| **Gumroad** | Bundles | Problem/solution | Social proof |
| **Payhip** | Direct | Simple + payment | Discount/urgency |
| **Sellfy** | Recurring | Subscription benefits | Recurring savings |

## Scaling: From 1 Product to 72

- 1 Master Profile = 1 hour
- Generate 5 platform v1s = 30 min
- Create 5 platform v2s = 30 min
- Total per product = 2 hours
- 72 products = 144 hours = ~4-5 weeks (part-time)

**Deploy sequentially (1 category/week)**:
- Week 1-2: Category 1 (8 products)
- Week 3-4: Category 2 (10 products)
- Week 5-6: Category 3 (9 products)
- Week 7-8: Category 4 (8 products)
- Week 9-10: Category 5 (7 products)
- Week 11-12: Category 6 (11 products)

