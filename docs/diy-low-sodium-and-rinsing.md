# DIY, rinsing, and low-sodium comparison

Tracked by issue #5. Remote evidence review: 2026-10-02.

## Executive result

The remote phase does **not** support a simple claim that DIY is automatically cheaper or lower-sodium.

Three separate strategies behave differently:

1. **Traditional red-ume-vinegar DIY** can remove synthetic additives and may be modestly cheaper on an ingredient-only basis, but purchased red ume vinegar is itself salty and the final solid sodium content is not known from recipe inputs alone.
2. **Rinsing / soaking commercial red ginger** is very likely to remove some sodium, but no ginger-specific reduction factor was found. Published reductions from other foods vary from single digits to large fractions, so no percentage is imported into the product matrix.
3. **A refrigerated, acidified low-sodium DIY prototype** could plausibly be the cheapest and lowest-sodium route, but it must be treated as an experiment: pH must be measured, cold storage maintained, and no long room-temperature shelf-life claim should be made.

Canonical data:

- `data/diy-cost-scenarios.csv`
- `data/rinsing-evidence.csv`

## 1. Traditional red-ume-vinegar DIY

A current home recipe uses approximately:

- 250 g fresh ginger
- 100-150 mL red ume vinegar
- salt for pretreatment

Source:
https://www.sirogohan.com/sp/recipe/benishouga/amp/

A second recipe source uses 1 kg fresh ginger and enough red ume vinegar to keep the ginger submerged, while recommending refrigerated storage and keeping the ginger under the liquid:
https://biomarche.jp/info/9842

### Current ingredient benchmarks

Observed on 2026-10-02:

- Chinese raw ginger: ¥500 / kg item price
  - https://store.shopping.yahoo.co.jp/shougakoubou/seika-china-1.html
- same seller, 4 kg: ¥1850 item price
  - https://store.shopping.yahoo.co.jp/shougakoubou/bfa9cdd1c0.html
- Ishigamimura red ume vinegar: ¥540 / 500 mL
  - https://www.ishigamimura.co.jp/c/ume-products/umezu/17005
- premium 15%-salt red ume vinegar example: ¥1240 / 500 mL
  - https://item.rakuten.co.jp/umeboys/shisoumezu/
- Mizkan grain vinegar official reference price: ¥224 / 500 mL
  - https://www.mizkan.co.jp/product/group/?gid=01001

Shipping is deliberately excluded from these DIY scenarios unless verified for Hadano. Labor, container cost, and energy are also excluded.

### Item-cost model

Using the ¥500/kg raw ginger and ¥540/500mL red ume vinegar:

| Ume-vinegar use | Item cost for 250 g ginger batch | Cost per 100 g ginger input |
|---|---:|---:|
| 100 mL | ¥233 | **¥93.20** |
| 150 mL | ¥287 | **¥114.80** |

Using the 4 kg raw-ginger item price lowers those figures only slightly:

- **¥89.45 / 100 g ginger input** at 100 mL ume vinegar per 250 g
- **¥111.05 / 100 g ginger input** at 150 mL

Using the ¥1240/500mL premium ume vinegar instead raises the input-basis cost to about **¥149-199 / 100 g ginger input**.

### Why this is not yet an apples-to-apples commercial price

These are **per 100 g raw ginger input**, not per 100 g finished drained solids.

Drying, squeezing, trimming, water loss, and retained liquid change the finished mass. Until finished solid yield is measured, the DIY values must not be ranked directly against a commercial "JPY/100 g content" or "JPY/100 g solid" value.

### Break-even observation

Against the current Shoga Kobo mail-order benchmark of ¥126.67/100g content basis, cheap purchased ume vinegar is at least plausible on ingredient cost alone; premium ume vinegar is not.

However, the margin is small enough that:

- shipping,
- yield loss,
- labor,
- and storage losses

can erase the apparent savings.

Traditional DIY becomes much more attractive if red ume vinegar is a **free or low-cost by-product of home umeboshi production**.

## 2. Sodium problem with traditional ume vinegar

Traditional red ume vinegar should not be assumed to be low-sodium.

One current commercial red ume vinegar explicitly reports approximately **15% salt**:
https://item.rakuten.co.jp/umeboys/shisoumezu/

The final sodium concentration of ginger cannot be calculated by simply assigning the brine's 15% salt concentration to the solids. Diffusion, water loss, soaking time, geometry and draining all matter.

Therefore:

- final DIY sodium = **unknown until measured**
- "natural / additive-free" is not equivalent to "low sodium"
- a traditional ume-vinegar DIY batch may fail the project's <=3 g salt-equivalent / 100 g preference

## 3. Rinsing and soaking commercial product

### What the literature supports

Published sodium-removal results vary strongly by food matrix.

Examples:

- canned peas, green beans and corn: about **5-12%** reduction after draining/rinsing
- tuna and cottage cheese: much larger reductions in a 3-minute rinse
- takuan cut into strips: about **40% salt elution after 5 minutes** and **70% after 30 minutes** of water soaking

Sources:

- https://faseb.onlinelibrary.wiley.com/doi/10.1096/fasebj.25.1_supplement.609.3
- https://pubmed.ncbi.nlm.nih.gov/6833685/
- https://www.jstage.jst.go.jp/article/eiyogakuzashi1941/39/6/39_6_267/_article/-char/ja/

### Project rule

**None of these percentages is assigned to red pickled ginger.**

The values demonstrate mechanism and plausible range only. Ginger has a different tissue structure, cut geometry, initial brine chemistry and processing history.

### Recommended red-ginger experiment

Use one lot of a candidate product and split it into equal portions.

Suggested first pass:

| Arm | Treatment |
|---|---|
| R0 | drain only; no rinse |
| R1 | 30-second gentle rinse; drain 2 min |
| R2 | soak 5 min in 10x mass of cold water; drain 2 min |
| R3 | soak 30 min in 10x mass of cold water; drain 2 min |

Record:

- starting mass
- post-treatment mass
- sensory saltiness
- crispness
- acidity
- apparent salinity or analytical sodium if available

A cheap conductivity/salinity meter can be used only as a **relative screening instrument** on identically prepared homogenates. Acid and other ions can interfere, so it must not be reported as laboratory sodium analysis.

For a decision-grade result, use an external food-analysis laboratory or an ion-specific analytical method.

## 4. Low-sodium DIY should use acidification + refrigeration, not low salt alone

Japanese pickle hygiene guidance defines vinegar pickles as products based on vinegar / ume vinegar / organic acid with **pH 4.0 or below**. It also treats low salt and pH as interacting preservation factors.

Source:
https://www.mhlw.go.jp/web/t_doc?dataId=00tc3961&dataType=1

Tokyo's food-safety FAQ separately warns that pathogens can grow even around **4% salt**, and that low-salt home pickles should be refrigerated and eaten promptly:
https://www.hokeniryo.metro.tokyo.lg.jp/anzen/anzen/food_faq/chudoku/chudoku07

MHLW household guidance gives **10°C or below** as a refrigerator target:
https://www.mhlw.go.jp/stf/seisakunitsuite/bunya/kenkou_iryou/shokuhin/syokuchu/01_00006.html

### Experimental low-sodium branch

For research purposes, the promising architecture is:

- fresh ginger
- ordinary brewed vinegar as the main acid source
- red shiso / another acceptable natural coloring source
- salt only for flavor, not as the primary preservation control
- refrigerated storage
- measured equilibrium pH target **<=4.0**

This is **not yet a validated recipe**.

The first prototype should therefore:

1. be a small batch;
2. remain refrigerated;
3. have pH measured with a calibrated meter rather than inferred from vinegar volume;
4. avoid room-temperature storage;
5. use a short experimental consumption window until stability is validated.

### Cost potential

With the current reference prices:

- ginger 250 g from ¥500/kg source = ¥125
- ordinary vinegar 100-150 mL at official ¥224/500mL reference = about ¥44.8-67.2

Before red shiso/color, salt, shipping and yield loss:

- approximately **¥67.92-76.88 per 100 g ginger input**

This is materially below the traditional purchased-ume-vinegar model, which is why the acidified low-sodium branch is worth testing.

But it is not yet a finished-product cost and is not yet a preservation-validated recipe.

## 5. Freezing

Freezing is not the preferred storage method when crisp texture matters.

Iwashita Foods states that freezing pickles may reduce their characteristic crispness, flavor and taste. If freezing is used, it recommends draining liquid, removing air, freezing, and thawing slowly in the refrigerator:
https://iwashita.co.jp/contact/qanda.html

Therefore the repo should treat freezing as:

- useful for preventing waste from bulk purchases;
- acceptable when texture loss is tolerable;
- inferior to refrigerated use for a "crisp" quality target.

## 6. Current decision state

### Traditional DIY

**Potentially cost-competitive, not proven cheaper.**

Best when:

- low-cost ume vinegar is available;
- ume vinegar is already produced at home;
- additive minimization matters more than sodium minimization.

Weakness:

- sodium is unknown and may be high;
- finished yield is unknown;
- purchased ume vinegar can erase the cost advantage.

### Rinsing commercial red ginger

**Very promising low-effort intervention, but ginger-specific reduction must be measured.**

This is likely the highest-value experiment because it can preserve the low purchase price of commercial bulk product while reducing sodium without redesigning the recipe.

### Low-sodium acidified DIY

**Most promising route for simultaneous low sodium + low ingredient cost, but not yet validated.**

It requires pH measurement and refrigerated process control.

## 7. Completion criteria for issue #5

Do not close #5 until at least one of the following is measured on red ginger itself:

1. sodium / apparent salinity before and after a defined rinse or soak protocol; and
2. finished yield, pH and sensory result for a low-sodium DIY prototype.

For a strong final comparison, complete both.

Remote research has reduced the unknowns enough to design these experiments, but it has not replaced them.
