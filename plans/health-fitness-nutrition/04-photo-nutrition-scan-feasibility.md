# Photo-Based Nutrition Scan — Availability, Naming, and Build Decision

**Research date:** August 9, 2026  
**Status:** Feasible now; crowded feature category; proceed with a confirmation-first implementation  
**Product working name:** MealDecode

## Executive decision

Photo-based meal recognition and calorie/macro estimation is available today and can be added to a prototype without training a food-vision model from scratch.

However, the feature itself is no longer unique. Major products and many smaller apps already offer some form of:

> Take a meal photo → identify foods → estimate portions → return calories and macros → allow edits → save to a diary.

Our product should therefore compete on **trust, correction quality, recipe memory, transparent ranges, and speed**, not on the claim that it can analyze a food photograph.

## Name check

### Plate Calculator — reject

The exact name `PlateCalculator` is already used by an active iOS Health & Fitness app for barbell-weight calculations. Many other fitness apps use “plate calculator” to mean choosing weight plates for a barbell.

This phrase would create the wrong expectation, perform poorly in search, and place the nutrition product beside weightlifting calculators.

Examples:

- https://apps.apple.com/us/app/platecalculator/id6755637815
- https://apps.apple.com/us/app/barbell-plate-calculator/id1468808885
- https://www.hevyapp.com/features/weight-plate-calculator/

### Dish Calculator — reject

The exact domain and product `DishCalculator` already exists as a restaurant food-cost, margin, and menu-pricing calculator. Similar products such as DishCost and DishTrack use “dish calculator” language for restaurant economics rather than personal nutrition.

Examples:

- https://dishcalculator.com/en
- https://dishcost.com/
- https://dishtrack.app/tools/food-cost-calculator

### PlateLens — reject

`PlateLens` is already an active iOS/Android AI calorie counter that analyzes meal photographs.

- https://platelens.app/

## Recommended in-app feature labels

Use a friendly feature label rather than making it the company name:

1. **Photo Meal Estimate** — recommended
2. **Meal Breakdown**
3. **Scan a Meal**
4. **Photo Nutrition**
5. **Decode This Meal** — strongest fit if the public brand remains MealDecode

Avoid using `calculator` in the feature label. The system is estimating and refining uncertain information rather than performing a simple exact calculation.

## Current consumer products proving demand

Representative products currently offering photo-first nutrition logging include:

- MyFitnessPal Meal Scan: https://www.myfitnesspal.com/
- Cal AI: https://apps.apple.com/us/app/cal-ai-calorie-tracker/id6480417616
- Foodvisor: https://apps.apple.com/us/app/foodvisor-nutrition-diet/id1064020872
- SnapCalorie: https://apps.apple.com/us/app/snapcalorie-ai-calorie-counter/id1574239307
- SNAQ: https://www.snaq.ai/calorie-counting
- PlateLens: https://platelens.app/
- Bite AI: https://apps.apple.com/us/app/id6736922373
- MealScan AI: https://apps.apple.com/us/app/mealscan-ai-calorie-tracker/id6765870007

This validates user demand but also confirms that “take a picture and get calories” is a crowded promise.

## Can we build it now?

Yes. Three implementation paths are available.

### Option A — Passio Nutrition-AI platform

Passio provides a food-logging SDK and REST API with:

- Single-item and mixed-meal recognition.
- Photo logging.
- Barcode scanning.
- Nutrition-label reading.
- Packaging recognition.
- User confirmation and editing.

Sources:

- https://www.passio.ai/photo-logging
- https://www.passio.ai/platform

**Best use:** Fast cross-platform prototype and commercial evaluation.

### Option B — LogMeal API

LogMeal provides:

- Food and drink detection.
- Multiple-dish recognition.
- Ingredient suggestions.
- Nutrition analysis with macro- and micronutrients.
- Custom recipes and favorites.
- Portion editing.
- Quantity estimation.

Its free trial currently allows up to 30 days or 200 queries for five registered users. More advanced quantity estimation requires several images captured through LogMeal’s iOS or Android depth SDK rather than relying on one ordinary photograph.

Sources:

- https://logmeal.com/api/
- https://logmeal.com/api/pricing/
- https://logmeal.com/api/quantity-estimation/

**Best use:** Vendor comparison and a more structured food-monitoring prototype.

### Option C — General vision model plus structured nutrition data

A general multimodal model can identify likely foods and ask clarification questions. Nutrients can then be calculated from USDA FoodData Central and a curated recipe database.

**Best use:** Cheapest and most flexible early proof-of-concept.

**Important:** The language model should suggest possible foods and questions. It should not directly invent the final calorie and macro totals. Final nutrient math should come from structured ingredients, portions, and a versioned calculation engine.

## Accuracy reality

A meal photograph can show shape, color, visible ingredients, and approximate scale. It usually cannot reliably reveal:

- Oil, butter, ghee, cream, or sugar incorporated during cooking.
- Ingredients hidden inside sauces, soups, casseroles, wraps, and mixed dishes.
- Exact weight or volume from one ordinary two-dimensional photo.
- Recipe substitutions and household preparation differences.
- Density differences between visually similar foods.

Research consistently identifies mixed dishes, hidden ingredients, and portion estimation as the hardest cases. A 2023 systematic review found wide calorie-error ranges across studies and concluded that available tools still require development before use as stand-alone dietary-assessment systems in research or clinical practice.

Sources:

- https://pubmed.ncbi.nlm.nih.gov/38060823/
- https://doi.org/10.3390/s24134089
- https://ajcn.nutrition.org/article/S0002-9165%2825%2900617-3/fulltext

## Recommended user experience

The product should not say, “We calculated your exact meal.”

Use this flow:

1. **Take a photograph.**
2. **Show one to three likely foods or meal components.**
3. **Ask only the highest-impact questions.**
   - Portion or approximate weight.
   - Cooking oil/fat.
   - Main protein or ingredient variant.
   - Sauce, cream, sugar, or cooking method where relevant.
4. **Calculate from structured food and recipe data.**
5. **Display a range when uncertainty remains.**
6. **Let the user edit every item.**
7. **Save the corrected meal or household recipe.**
8. **Reuse the correction the next time.**

### Example result

> **Estimated meal: 610–720 kcal**  
> Protein: 24–29 g  
> Main uncertainty: cooking oil and rice portion  
> `Refine estimate` · `Save meal`

## Product differentiation

The defensible experience is:

- Honest calorie and macro ranges.
- Short, intelligent clarification questions.
- Household-recipe memory.
- Source and assumption visibility.
- Fast repeat logging.
- Strong support for complex home-cooked meals.
- A test set that measures performance across the actual target audience’s meals.

## Immediate proof-of-concept plan

Evaluate three approaches on the same set of 40–60 meals:

- Passio.
- LogMeal.
- General vision model plus USDA/curated recipe matching.

Include:

- Simple single foods.
- Multi-item plates.
- Mixed dishes.
- Soups and sauces.
- Packaged foods.
- Repeated household meals.
- Low-light and imperfect photographs.

Measure:

- Correct food in the top three suggestions.
- Number of edits required.
- Time from photo to saved meal.
- Error after user confirmation.
- Failure rate.
- User trust.
- Cost per analyzed meal.
- Image retention and privacy terms.

## Go criteria

Proceed with the photo feature when the selected approach achieves:

- Correct item/component in the top three for at least 80% of the validation meals.
- Median two or fewer clarification questions.
- Median completed log time of 45 seconds or less.
- Every result is editable.
- Clear fallback to manual entry.
- A credible path to acceptable per-user operating cost.
- No misleading exact-accuracy claim.

## Final conclusion

**Available now:** Yes.  
**Can be prototyped immediately:** Yes, with an existing API/SDK or a general vision model connected to structured nutrition data.  
**Accurate enough to remove user review:** No.  
**Unique as a standalone idea:** No.  
**Worth including in MealDecode:** Yes, when implemented as a confirmation-first, transparent estimate rather than a magic exact calculator.
