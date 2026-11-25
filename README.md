# Supplement label dataset

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24506859.svg)](https://doi.org/10.5281/zenodo.24506859)

Label facts of 201 best-selling supplements and 99 protein bar flavors, copied by hand from the Supplement Facts and Nutrition Facts panels: protein per serving, calories, protein per 100 kcal, the doses printed for creatine, magnesium, vitamin D, omega-3 and others, and the third-party certifications printed on the pack.

Since November 25, 2026 it also holds the **full Supplement Facts / Nutrition Facts panel of 112 of them**, line by line, each with the page it was read from and the date (`supplement-panels.csv`).

Maintained by [HealthWorld](https://www.healthworldlabels.com), a site that compares supplements by what their labels say. The live table, with every product's full label, is at [healthworldlabels.com/data/supplement-labels](https://www.healthworldlabels.com/data/supplement-labels).

## What the labels show (November 2026)

We read the labels of 112 popular supplements line by line (November 23–25, 2026): 7 of 12 vitamin D products give 5,000 IU, above the 4,000 IU upper limit the NIH lists for adults; a "1,200 mg" fish oil softgel holds 360 mg of omega-3; and 30 of 111 print a named testing mark.

1. **7 of 12 vitamin D products print more than the adult upper limit.** 7 of the 12 vitamin D labels we read give 125 mcg (5,000 IU) or more per serving, above the 100 mcg (4,000 IU) a day that the NIH lists as the upper limit for adults. The everyday doses on the shelf are 25 mcg (1,000 IU) and 50 mcg (2,000 IU). Taking more than the upper limit is a decision for your doctor.
2. **"Fish oil 1,200 mg" is not 1,200 mg of omega-3.** The number on the front is usually the oil. Nature Made Fish Oil 1200 mg gives 720 mg of omega-3 in 2,400 mg of fish oil (30%); Viva Naturals Triple Strength Omega-3 Fish Oil 2,500 mg gives 2,250 mg in 2,500 mg (90%). Compare the EPA + DHA line, not the oil.
3. **30 of 111 labels print a named testing mark.** NSF Certified for Sport, NSF Contents Certified, USP Verified, Informed Choice / Informed Sport or IFOS appear on 30 of the 111 labels we read line by line. Gluten-free, non-GMO and organic seals don't count here, and neither does "third-party tested" without a named programme. A mark matters most for tested athletes; it is not a measure of how well a product works.
4. **13 of 22 protein powders and shakes list sucralose.** Sucralose is on 13 of the 22 protein labels we read, acesulfame potassium on 10; 5 use only stevia or monk fruit. The 3 with no sweetener at all are all unflavored tubs (Transparent Labs Grass-Fed Whey Protein Isolate (Unflavored), NAKED Nutrition Naked Whey (Unflavored), NOW Sports Whey Protein Isolate, Unflavored).
5. **Magnesium per capsule runs from 48 mg to 150 mg.** Across 9 magnesium capsules and tablets, the elemental magnesium per unit ranges from 48 mg to 150 mg. Double Wood Supplements Magnesium Glycinate 400 mg gives 60 mg per capsule: the "400 mg" in its name is the whole magnesium glycinate compound. The Supplement Facts line "Magnesium … mg" is the number to compare.
6. **Electrolyte mixes range from 55 mg to 1,000 mg of sodium a serving.** Ultima Replenisher Electrolyte Drink Mix lists 55 mg of sodium per serving and LMNT Electrolyte Drink Mix 1,000 mg, about 18 times as much. Sugar runs from 0 g to 11 g. Read the sodium line before choosing one for a long workout or for every day.
7. **Creatine gummies and capsules: 5 g takes more than one serving.** 6 of the 6 creatine powders we read list 5 g per scoop. Optimum Nutrition Micronized Creatine Monohydrate Capsules 2500 mg lists 2.5 g in 2 capsules (1.25 g each), so 5 g takes 4 capsules; Create Creatine Monohydrate Gummies lists 4.5 g in 3 gummies (1.5 g each), so 5 g takes more than 3 gummies. Count the pieces per 5 g before comparing prices.
8. **Pre-workouts: 180–200 mg of caffeine a scoop, up to 400 mg a serving.** All 7 pre-workout labels we read list 180 to 200 mg of caffeine per scoop, and 3 of them also print a two-scoop serving of up to 400 mg. The FDA cites 400 mg a day as an amount not generally linked to negative effects in healthy adults, and that includes coffee and energy drinks.
9. **Whey powders are 67% to 89% protein by scoop weight.** Divide the protein by the scoop's weight in grams. Of 13 whey powders, NOW Sports Whey Protein Isolate, Unflavored is 89% protein (25 g in 28 g) and Body Fortress Super Advanced Whey Protein 67% (30 g in 45 g); the rest is flavor, sweetener, thickeners and, in blends, carbohydrate and fat.
10. **39 of 99 protein bars reach 10 g of protein per 100 calories.** Across 99 bar flavors, protein per 100 calories runs from 5.7 g to 20 g, with a middle of 9.5 g. 39 of them reach 10 g, which means 20 g of protein or more in a 200-calorie bar.
11. **Probiotic counts run from 1 billion to 60 billion CFU.** Align Probiotic 24/7 Digestive Support lists 1 billion CFU "when manufactured" and Physician's Choice 60 Billion Probiotic 60 billion; the labels name 1 to 16 strains. Two things to compare besides the count: the strain names, and whether the count is promised at manufacture or through the expiry date.
12. **A collagen serving is 6 g to 20 g.** Youtheory Collagen Advanced Formula Tablets gives 6 g of collagen in 6 tablets; the scoops we read give 10 g to 20 g. Compare grams of collagen per serving, then servings per container.

Every number above is computed from `supplement-panels.csv` and `supplement-labels.csv`; the live version (it moves when a label changes) is at [healthworldlabels.com/data/supplement-labels](https://www.healthworldlabels.com/data/supplement-labels). These are label facts as printed, not lab tests, and not medical advice.

## Files

| File | What it holds |
|---|---|
| `supplement-labels.csv` | One row per product or bar flavor (300 rows), UTF-8, comma separated |
| `supplement-panels.csv` | The full label panel of 112 supplements in long format: one row per product and label line (1,004 rows), with the variant read, the source page and the date |

## Columns

| Column | Meaning |
|---|---|
| `type` | `product` (a supplement in the catalog) or `bar` (one protein bar flavor) |
| `brand` | Brand name as printed |
| `product` | Product name; for bars, the line and flavor |
| `category` | Protein, Strength & Performance, Sleep & Stress, Vitamins & Minerals, Omega-3 & Heart, Gut Health, Collagen, Greens & Superfoods, High-Protein Pantry, Protein bars |
| `protein_g_per_serving` | Grams of protein per serving, where the label states it |
| `kcal_per_serving` | Calories per serving, where the label states it |
| `protein_g_per_100_kcal` | Protein density, computed from the two columns above |
| `label_facts` | The headline facts as printed, separated by a vertical bar (for example `Creatine: 5 g \| Form: Monohydrate`) |
| `certifications` | Third-party marks printed on the pack (NSF Certified for Sport, USP, USDA Organic), empty when none |
| `url` | The product's page with its full label |
| `source` | Where the numbers come from |

## Columns of `supplement-panels.csv`

| Column | Meaning |
|---|---|
| `product_slug` | Stable id of the product (matches the URL on healthworldlabels.com/products/) |
| `brand`, `product`, `category` | As in `supplement-labels.csv` |
| `variant_read` | The exact flavor, size or count whose label was read |
| `field` | The label line, for example `protein`, `sweeteners`, `caffeine`, `creatinePerServing`, `magnesiumPerUnit`, `epa`, `dha`, `sodium`, `cfu`, `thirdPartyMark` |
| `value` | The value as printed, with its unit (`25 g`, `125 mcg (5,000 IU)`, `none stated`) |
| `source_type` | `brand website` or `NIH DSLD` (the NIH Dietary Supplement Label Database) |
| `source_url` | The page the label was read from |
| `read_date` | The day it was read |

## How the numbers are collected

Every number is read off the label of the product as sold in the United States, from the brand's own page, the NIH Dietary Supplement Label Database (DSLD) or Open Food Facts. HealthWorld does not run a lab and does not test products; this dataset says what the label prints, nothing more. Formulas and flavors change, so check the pack you buy.

The method is described at [healthworldlabels.com/how-we-pick](https://www.healthworldlabels.com/how-we-pick).

## How to cite

HealthWorld (2026). *Supplement label dataset* [Data set]. Zenodo. https://doi.org/10.5281/zenodo.24506859. Licensed CC BY 4.0. A machine-readable citation is in `CITATION.cff`.

## Updates

The file is refreshed from the live table when products are added or a label changes. This version: November 25, 2026 (201 supplements, 99 bar flavors, 112 full panels).

## Licence

[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). Use it, change it and share it, with credit to "HealthWorld, healthworldlabels.com".

## Corrections

Found a number that no longer matches the label? Open an issue with the product name and a photo or link of the current label.
