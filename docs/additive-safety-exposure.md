# Additive safety and exposure screen

Tracked by issue #3. Evidence reviewed: 2026-10-02.

This document replaces a binary "synthetic = bad / natural = safe" heuristic with dose-based screening where the available data allow it.

## Important interpretation

An ADI is a health-based guidance value for chronic daily intake over a lifetime without appreciable health risk. It is **not** a toxicity threshold at which harm suddenly begins.

This repository additionally uses a deliberately conservative project rule:

> A single red-pickled-ginger product should normally contribute no more than 10% of the selected ADI in the modeled daily intake scenario.

That 10% allocation is a project preference, not a Japanese or international regulatory standard.

For substances with more than one current authoritative ADI, the lower value is used for the project screen. Both values are retained in `data/additives.csv`.

Reference adult: **70 kg**.

Scenarios:

- high intake: **50 g/day**
- stress test: **100 g/day**

## Results summary

| Label / substance | Conservative ADI used | 10% allocation for 70 kg | 50 g/day concentration ceiling | 100 g/day concentration ceiling | Current product-level result |
|---|---:|---:|---:|---:|---|
| Red 102 / Ponceau 4R | 0.7 mg/kg bw/day (EFSA) | 4.9 mg/day | 98 mg/kg food | 49 mg/kg food | concentration unknown |
| Yellow 4 / Tartrazine | 7.5 mg/kg bw/day (EFSA) | 52.5 mg/day | 1050 mg/kg food | 525 mg/kg food | concentration unknown |
| Sorbic acid / potassium sorbate | 11 mg/kg bw/day as sorbic acid (EFSA) | 77 mg/day | — | — | conditionally quantifiable from Japanese legal maximum |
| Steviol glycosides | 4 mg/kg bw/day as steviol (JECFA) | 28 mg/day | 560 mg/kg steviol-equivalent | 280 mg/kg steviol-equivalent | concentration / composition unknown |
| Red 106 / Acid Red | no numeric ADI | — | — | — | project 10% rule cannot be applied |
| "acidulant" / "pH regulator" | not a single chemical | — | — | — | identity required |

## Red No. 102 / Ponceau 4R

EFSA established an ADI of **0.7 mg/kg body weight/day**. Its 2015 refined exposure assessment retained that value, and EFSA's 2026 monitoring report still uses it. JECFA has a less restrictive ADI of **0-4 mg/kg body weight/day**.

For a 70 kg adult:

- EFSA ADI = 49 mg/day
- project 10% allocation = 4.9 mg/day
- at 50 g red ginger/day, the product would need to contain <=98 mg/kg to meet the project target
- at 100 g/day, <=49 mg/kg

The candidate products disclose the presence of Red 102 but not its concentration. The Japanese tar-dye use rules found in this pass define prohibited food categories but do not provide a product-specific numerical concentration that can safely be substituted for the missing concentration in these red-ginger SKUs.

Therefore Red 102 candidates are **unresolved**, not classified as unsafe.

Sources:

- EFSA 2009: https://efsa.onlinelibrary.wiley.com/doi/10.2903/j.efsa.2009.1328
- EFSA 2015: https://efsa.onlinelibrary.wiley.com/doi/10.2903/j.efsa.2015.4073
- EFSA 2026 monitoring: https://efsa.onlinelibrary.wiley.com/doi/10.2903/j.efsa.2026.10070
- JECFA: https://apps.who.int/food-additives-contaminants-jecfa-database/Home/Chemical/4941

## Yellow No. 4 / Tartrazine

EFSA's current food-additive ADI is **7.5 mg/kg body weight/day**; its 2026 monitoring report reports exposure below this ADI. JECFA updated its value in 2016 to **0-10 mg/kg body weight/day**.

For a 70 kg adult using the more conservative EFSA value:

- ADI = 525 mg/day
- project 10% allocation = 52.5 mg/day
- 50 g/day product ceiling = 1050 mg/kg
- 100 g/day product ceiling = 525 mg/kg

The JFDA shredded candidate lists Yellow 4 but does not disclose its concentration, so the product-level screen remains unresolved.

Sources:

- EFSA 2026: https://efsa.onlinelibrary.wiley.com/doi/10.2903/j.efsa.2026.10070
- JECFA: https://apps.who.int/food-additives-contaminants-jecfa-database/Home/Chemical/477

## Potassium sorbate / sorbic acid

EFSA established a group ADI of **11 mg sorbic acid/kg body weight/day** for sorbic acid and potassium sorbate. JECFA retains a group ADI of **0-25 mg/kg body weight/day**, expressed as sorbic acid.

Japan's additive standard sets a maximum of **0.50 g/kg as sorbic acid** for potassium sorbate in **vinegar-pickled pickles (酢漬の漬物)**.

Using the more conservative EFSA ADI and assuming the candidate red ginger is legally in that category:

- 70 kg ADI = 770 mg/day
- project 10% allocation = 77 mg/day
- legal-maximum exposure at 50 g/day = 25 mg/day = **3.25% of ADI**
- legal-maximum exposure at 100 g/day = 50 mg/day = **6.49% of ADI**

Thus potassium sorbate passes the project's <=10% ADI target even at 100 g/day **under this conditional legal-maximum model**.

This is a substantially stronger result than simply assuming an unknown manufacturer concentration. The remaining dependency is confirming that each red-ginger SKU is legally classified under the 0.50 g/kg vinegar-pickle category.

Sources:

- EFSA 2019: https://efsa.onlinelibrary.wiley.com/doi/10.2903/j.efsa.2019.5625
- JECFA: https://apps.who.int/food-additives-contaminants-jecfa-database/Home/Chemical/2724
- Japan additive standard: https://www.caa.go.jp/policies/policy/standards_evaluation/food_additives/second_additive_01/assets/cms_standards103_20240507_11.pdf

## Stevia / steviol glycosides

JECFA confirmed in **2026** the ADI of **0-4 mg/kg body weight/day expressed as steviol**.

For a 70 kg adult:

- ADI = 280 mg/day as steviol
- project 10% allocation = 28 mg/day
- 50 g/day product ceiling = 560 mg/kg as steviol equivalents
- 100 g/day product ceiling = 280 mg/kg as steviol equivalents

The Gyomu Super label states "stevia" but does not disclose the concentration, exact glycoside composition, or steviol-equivalent amount. It therefore cannot yet be quantitatively screened.

Source:

- JECFA 2026: https://apps.who.int/food-additives-contaminants-jecfa-database/Home/Chemical/267

## Red No. 106 / Acid Red

This substance is handled differently because a numeric ADI is **not currently established**.

At the Japanese Food Sanitation Standards Council discussions reported in late 2025 / early 2026:

- Red 104, 105 and 106 had no JECFA ADI.
- For Red 106, the FY2023 market-basket "labelled group" estimate was **0.001 mg/kg body weight/day**.
- The FY2022 production-volume estimate was **0.03 mg/kg body weight/day**.
- The Consumer Affairs Agency stated that it would begin information collection and organization with Red 106 and, once information is ready, request a food-health-impact assessment.

A published two-year F344 rat study used 2.5% and 5.0% Red 106 in the diet and reported no treatment-related adverse effects or carcinogenicity. That is useful hazard evidence, but it does **not** provide a regulatory ADI and cannot be converted into this repository's 10%-of-ADI screen without an independent risk assessment.

Project classification:

- not "proven dangerous"
- not quantitatively cleared under the project rule
- **elevated uncertainty / deprioritize when otherwise equivalent alternatives exist**

Sources:

- Consumer Affairs Agency 2025 material: https://www.caa.go.jp/policies/council/fssc/meeting_materials/assets/fssc_cms101_251117_15.pdf
- 2026 meeting minutes: https://www.caa.go.jp/policies/council/fssc/meeting_materials/assets/fssc_cms101_260113_01.pdf
- 2-year rat study: https://www.jstage.jst.go.jp/article/tox1988/5/2/5_2_157/_article/-char/en

## Acidulant and pH-regulator collective labels

"Acidulant" and "pH regulator" are collective labeling names in Japan. They can stand in for multiple permitted substances. The label therefore does not identify one molecule with one ADI.

Project rule:

- do not classify the collective label itself as harmful
- do not assign a numeric ADI to the collective label
- request the actual additive identity from the manufacturer if this variable becomes decision-relevant

Sources:

- Consumer Affairs Agency additive-label guide: https://www.caa.go.jp/policies/policy/food_labeling/food_sanitation/food_additive/assets/food_labeling_cms204_210408_01.pdf
- MHLW definition/range for pH regulator: https://www.mhlw.go.jp/web/t_doc?dataId=00ta5664&dataType=1&pageNo=2

## Candidate implications

### Gyomu Super 1 kg

- Red 102: unresolved due concentration
- potassium sorbate: conditionally passes the 10% ADI rule at the Japanese vinegar-pickle legal maximum
- stevia: unresolved due concentration / steviol-equivalent composition
- acidulant: identity required if detailed assessment becomes necessary

The product therefore should **not** be rejected solely because it contains Red 102, but it also cannot yet be given a fully quantified additive-clearance status.

### Shoga Kobo 600 g

- potassium sorbate: same conditional pass as above
- acidulant: identity unresolved
- natural red-radish color is outside the current quantitative screen

Its dominant known disadvantage remains sodium rather than potassium sorbate.

### JFDA shredded 1 kg

- Red 102: unresolved
- Yellow 4: unresolved
- potassium sorbate: conditional pass if the vinegar-pickle legal category applies
- acidulant: identity unresolved

## Next evidence requests

The highest-value missing data are:

1. Red 102 concentration in Gyomu Super and JFDA shredded products.
2. Yellow 4 concentration in JFDA shredded product.
3. Steviol-equivalent concentration / exact stevia additive in Gyomu Super.
4. Manufacturer or legal-category confirmation that the sorbate-containing SKUs fall under the 0.50 g/kg "vinegar-pickled pickles" limit.

These are suitable manufacturer-inquiry targets; guessing them would weaken the comparison.
