# Product comparison matrix

Tracked by issue #2. Observation date: 2026-10-02.

Canonical data:

- `data/products.csv`: product composition, sodium, origin, storage and evidence state
- `data/offers.csv`: dated seller/price/shipping observations

## Data model rules

1. Product facts and price observations are separated because prices change independently of formulations.
2. "Net/content weight" is not assumed to equal drained/solid ginger weight.
3. A strict solid-weight price ranking may use only rows with verified `solid_g`.
4. A shipping charge shown for another region is not silently reused for Hadano.
5. Unknown additive concentration remains unknown until a manufacturer value, applicable legal maximum, or analytical result is available.
6. Prices are dated observations, not permanent facts.

## Current view

| Product | Form | Salt equivalent | Color / preservative | Observed item cost | Verified Hadano delivered cost | Primary gap |
|---|---|---:|---|---:|---:|---|
| 生姜工房 600g | shredded | 6.1 g/100g | red-radish / sorbate | ¥760 shipped | **¥126.67/100g content basis** | solid weight; high sodium |
| 業務スーパー 1kg | shredded | **2.4 g/100g** | Red 102 / sorbate | unknown locally | unknown | Hadano shelf price; additive exposure |
| 岩下 国産・25%カット 50g | shredded | 3.6 g/100g | vegetable color / no listed sorbate | ¥200 before shipping | unknown | price efficiency; exact additive identities |
| JFDA 平切 1kg | flat slice | unknown | no additives listed | ¥806 before shipping | unknown | sodium; origin; solid weight |
| JFDA 千切り 1kg | shredded | unknown | Red 102 + Yellow 4 / sorbate | ¥522 before shipping | unknown | sodium; origin; additive exposure |
| 紀州ふみこ 600g (solid 500g) | whole pieces | unknown | none | current price unresolved | unknown | sodium; current price |

## Low-sodium view

Among currently verified sodium values:

- 業務スーパー: **2.4 g/100g** — meets the repository preferred threshold of <=3 g/100g.
- 岩下 国産・25%カット: **3.6 g/100g**.
- 生姜工房: **6.1 g/100g**.

The low-sodium leader is therefore not yet the value leader because its Hadano shelf price has not been captured.

## Synthetic-color-free view

Current verified options include:

- 生姜工房 — red-radish color; sodium 6.1 g/100g.
- 岩下 国産・25%カット — vegetable color; sodium 3.6 g/100g.
- JFDA 平切 — no additives listed; sodium unknown.
- 紀州ふみこ — ginger + ume vinegar + red shiso only; no preservative/color additive; sodium unknown.

No current row is yet verified to combine all three:

- <=3 g salt equivalent/100g
- synthetic-color-free
- low delivered cost in Hadano

That is a search gap, not evidence that no such product exists.

## Additive-screen view

Issue #3 adds a dose-based screen rather than a synthetic/natural heuristic.

| Product | Additive status |
|---|---|
| 生姜工房 600g | potassium sorbate conditionally passes the <=10% ADI project rule at the Japanese vinegar-pickle legal maximum; acidulant identity unresolved |
| 業務スーパー 1kg | Red 102 unresolved due unknown concentration; potassium sorbate conditionally passes; stevia unresolved; acidulant identity unresolved |
| 岩下 国産・25%カット | acidulant identity unresolved; no listed sorbate |
| JFDA 平切 1kg | no additive issue identified from the current simple ingredient list |
| JFDA 千切り 1kg | Red 102 and Yellow 4 unresolved due unknown concentrations; potassium sorbate conditionally passes; acidulant identity unresolved |
| 紀州ふみこ 600g | no listed additive requiring this screen |

"Conditionally passes" means the calculation assumes the SKU falls under the Japanese 0.50 g/kg-as-sorbic-acid limit for vinegar-pickled pickles. It is not a claim about the manufacturer's actual concentration.

See `docs/additive-safety-exposure.md` and `data/product-additive-screen.csv`.

## Practical baseline

At the user's initial consumption of about 300 g/month, the 生姜工房 600g mail-order pack represents about two months of consumption and is currently the cleanest verified price baseline for a natural-color product with nationwide free shipping.

The 6.1 g/100g sodium level remains its main disadvantage. At 50 g intake, that is 3.05 g salt equivalent before any rinsing.

## Next dependencies

- #3: quantify additive exposure and uncertainty.
- #4: capture actual Hadano shelf prices.
- #5: quantify DIY and rinsing/soaking alternatives.

Do not declare a final winner until those dependencies are resolved.
