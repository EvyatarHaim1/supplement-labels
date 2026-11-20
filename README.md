# Supplement label dataset

Label facts of 180 best-selling supplements and 99 protein bar flavors, copied by hand from the Supplement Facts and Nutrition Facts panels: protein per serving, calories, protein per 100 kcal, the doses printed for creatine, magnesium, vitamin D, omega-3 and others, and the third-party certifications printed on the pack.

Maintained by [HealthWorld](https://www.healthworldlabels.com), a site that compares supplements by what their labels say. The live table, with every product's full label, is at [healthworldlabels.com/data/supplement-labels](https://www.healthworldlabels.com/data/supplement-labels).

## Files

| File | What it holds |
|---|---|
| `supplement-labels.csv` | One row per product or bar flavor (279 rows), UTF-8, comma separated |

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

## How the numbers are collected

Every number is read off the label of the product as sold in the United States, from the brand's own page or Open Food Facts. HealthWorld does not run a lab and does not test products; this dataset says what the label prints, nothing more. Formulas and flavors change, so check the pack you buy.

The method is described at [healthworldlabels.com/how-we-pick](https://www.healthworldlabels.com/how-we-pick).

## Licence

[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). Use it, change it and share it, with credit to "HealthWorld, healthworldlabels.com".

## Corrections

Found a number that no longer matches the label? Open an issue with the product name and a photo or link of the current label.
