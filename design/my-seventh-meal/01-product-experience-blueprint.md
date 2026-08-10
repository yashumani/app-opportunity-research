# My Seventh Meal — Product Experience Blueprint

**Design date:** August 9, 2026  
**Status:** Provisional product direction for design and validation  
**Working public name:** **My Seventh Meal**  
**Working store descriptor:** **Photo Nutrition & Macros**  
**Primary tagline:** **A clearer picture of what you eat.**  
**Naming status:** Passed preliminary public screening only; final domain, store, and trademark clearance remains required.

---

## 1. Product idea in one sentence

**My Seventh Meal helps people photograph a real meal, confirm the details a camera cannot see, and save an understandable calorie and nutrition estimate without pretending the result is exact.**

The first release is a nutrition-first wellness app. Activity and progress features support consistency, but the main reason to open the app is fast, trustworthy meal logging.

---

## 2. Brand story

The name should feel personal rather than clinical. It should not be explained as a literal instruction to eat seven meals per day.

The visual and messaging story uses the rhythm of a seven-day week:

> **Seven days. Real meals. A clearer pattern.**

The app helps users understand how everyday meals add up over time. The brand is about awareness and consistency rather than perfect eating.

### Brand hierarchy

- **Brand:** My Seventh Meal
- **Store title:** `My Seventh Meal: Food & Macros`
- **Store subtitle:** `Photo nutrition made clearer`
- **Primary tagline:** `A clearer picture of what you eat.`
- **Core feature label:** `Photo Meal Estimate`
- **Friendly action label:** `Scan a meal`
- **Result action:** `Refine estimate`

Avoid calling the feature a “plate calculator” or “dish calculator.” The system estimates, asks questions, and refines uncertainty; it does not perform an exact calculation from a photograph alone.

---

## 3. Experience principles

### 3.1 Show value before asking for commitment

A new user should be able to understand the app, choose a simple goal, and try the meal flow before completing a long profile.

The app asks for:

- Camera access only when the user chooses to take a photograph.
- Photo-library access only when the user chooses an existing image.
- Activity access only after the nutrition experience is understood.
- Notifications only after the user creates a reminder or completes several logs.
- Account creation after the first result if technically and legally practical, so the value is visible before registration.

### 3.2 Honest, not magical

The interface never says:

- “Exact calories from one photo.”
- “Perfectly accurate.”
- “AI knows every ingredient.”

It says:

- “Estimated range.”
- “Help us refine this meal.”
- “The camera cannot see every ingredient.”
- “Main uncertainty: cooking oil and portion size.”

### 3.3 Fast for repeated meals

The first time a meal is logged may require two or three confirmations. The next time should be much faster because the app remembers:

- The user’s usual portion.
- The household recipe.
- Common ingredient choices.
- Preferred units.
- Previous corrections.

### 3.4 Support without judgment

Avoid red failure states for normal eating behavior. Avoid words such as “bad,” “cheat,” “clean,” “guilty,” or “failed.”

Use language such as:

- “You are building a clearer week.”
- “One meal does not define your progress.”
- “You logged four of seven days.”
- “Protein was more consistent this week.”
- “Would you like a reminder tomorrow?”

### 3.5 Every result can be corrected

Users can always:

- Change the detected food.
- Add or remove an item.
- Change the portion.
- Change the cooking method.
- Mark “I’m not sure.”
- Save a household version.
- Report a questionable result.
- Switch to manual entry.

---

## 4. Main navigation

The app uses four destinations plus one central action.

| Navigation item | User purpose |
|---|---|
| **Today** | See the day, recent meals, nutrition progress, and quick suggestions |
| **Recipes** | Reuse household recipes, favorites, and frequent meal combinations |
| **Progress** | Understand weekly patterns across calories, protein, fiber, activity, and weight |
| **Profile** | Goals, preferences, subscription, privacy, export, deletion, and support |
| **Central Scan button** | Start a meal log from any main screen |

The central action is labeled **Scan** with a camera/meal icon. A long press or secondary menu can later expose “Manual entry” and “Repeat recent meal,” but version one should keep the primary action simple.

---

## 5. First-session journey

The ideal first session takes approximately two to four minutes, with the meal scan itself targeted below 45 seconds.

### Screen 1 — Welcome

**Headline:**

> A clearer picture of what you eat.

**Supporting copy:**

> Photograph a meal, confirm what the camera cannot see, and track calories and macros with more confidence.

**Primary action:** `Try it now`  
**Secondary action:** `I already have an account`

Do not lead with a subscription screen.

### Screen 2 — Choose the main goal

**Question:**

> What would you like help with?

Single-choice cards:

- Understand my meals
- Manage my weight
- Increase protein
- Build a consistent routine
- Track for fitness

Supporting line:

> You can change this later.

### Screen 3 — Food preferences

Only collect information that improves the first estimate:

- Vegetarian / vegan / pescatarian / no preference
- Common cuisine preferences, using a broad searchable list
- Foods to exclude
- Preferred measurement style: cups and servings / grams and ounces / both

Skip height, weight, goal weight, and activity level until after the first useful result unless the user chooses weight management.

### Screen 4 — First meal action

> Let’s understand one meal.

Actions:

- `Take a photo`
- `Choose a photo`
- `Search or enter manually`

Supporting privacy note:

> Your photo is used to prepare the estimate. You choose whether it remains saved.

### Screen 5 — Processing

Use calm progress messages rather than a technical spinner:

1. “Looking at the meal…”
2. “Finding likely foods…”
3. “Preparing a few quick questions…”

Allow `Cancel` and preserve the selected photo.

### Screen 6 — Meal review

Show the photo at the top, followed by detected components.

Example:

> **We found three items**
>
> Chicken  ·  Rice  ·  Mixed vegetables

Each item has:

- Confidence expressed in words only when helpful: likely / possible
- Portion selector
- Edit action
- Remove action

Then ask no more than two or three high-impact questions, one at a time or in a short sheet:

- How much rice was there?
- Was the chicken grilled, baked, or fried?
- Was oil, butter, or a creamy sauce added?

Provide `I’m not sure` for every uncertainty question.

### Screen 7 — Result

The result prioritizes understanding, not dense nutrient tables.

Example:

> **Estimated meal**
>
> **610–720 calories**
>
> Protein  28–34 g  
> Carbohydrates  76–88 g  
> Fat  19–27 g  
> Fiber  8–11 g

Then explain:

> **Why this is a range**  
> The largest uncertainty is the amount of cooking oil and the rice portion.

Actions:

- `Save meal`
- `Refine estimate`
- `Save as a regular meal`

### Screen 8 — Save and account

After value has been demonstrated:

> Save this meal and make future logging faster.

Options:

- Continue with Apple
- Continue with Google
- Continue with email

If guest mode is not practical for the initial build, move account creation immediately before the first photo while preserving the same short, low-friction tone.

### Screen 9 — Gentle completion

> Your first meal is saved.

Show one useful next step only:

- Add another meal
- Set a daily target
- Save this as a regular meal

Do not present a wall of setup tasks.

---

## 6. Today screen blueprint

### Top area

- Greeting or simple date
- Seven-day consistency indicator: seven small dots or a subtle weekly ring
- Current day summary

Example:

> **Today**
>
> 1,280–1,410 calories  
> of your 2,000-calorie target

Use a range band rather than forcing an exact total when meal estimates remain uncertain.

### Priority nutrient cards

Show only the most useful values by default:

- Protein
- Fiber
- Calories
- Optional carbohydrates/fat based on user goal

Do not show every micronutrient on the home screen.

### Main action

Large, thumb-friendly button:

> `Scan a meal`

Secondary options below:

- Repeat recent meal
- Search manually
- Use a saved recipe

### Recent meals

Each card shows:

- Meal label and time
- Small photo only if the user chose photo retention
- Meal name or components
- Calorie range
- Quick repeat button
- Edit menu

### Helpful insight

One gentle sentence maximum:

> Your lunch estimate will become faster after you save the recipe.

or

> You are 18 g away from today’s protein target.

Avoid generating an insight when the data is incomplete or the message would feel judgmental.

---

## 7. Recipes experience

The Recipes tab is the app’s long-term retention engine.

### Sections

- Frequent meals
- Household recipes
- Favorites
- Recent combinations
- Leftovers

### Recipe card

Show:

- Recipe name
- Typical serving
- Nutrition range or calculated value
- Last used
- One-tap log

### Recipe creation paths

- Save from a corrected photo result
- Build from ingredients
- Copy an existing recipe and customize it
- Convert a frequent meal into a recipe after repeated use

The app should occasionally suggest:

> You have corrected this meal three times. Save it as your regular version?

---

## 8. Progress experience

The Progress area answers:

1. Am I logging consistently?
2. What patterns are changing?
3. What is one reasonable next step?

### Default weekly view

- Seven-day logging consistency
- Average calorie range
- Average protein and fiber
- Activity/steps when connected
- Weight trend when the user chooses to track it

### Insight style

Good:

> You logged dinner on six of seven days.

> Protein was more consistent at breakfast this week.

> Your average meal estimate became narrower as you reused recipes.

Avoid:

> You failed to meet your target.

> You ate too much.

> You had a bad week.

---

## 9. Subscription experience

The free experience must prove usefulness before the paywall.

### Suggested free value

- Manual logging
- A limited number of photo estimates each month
- Basic Today view
- A small number of saved recipes
- Seven-day history

### Suggested paid value

- More photo estimates
- Full recipe memory
- Unlimited favorites and recent-meal reuse
- Longer history and progress trends
- Activity connection
- Household recipe features
- Weekly insights

### Paywall timing

Good moments:

- After several successful photo estimates
- When the user attempts to save beyond the free recipe limit
- When opening longer progress history

Bad moments:

- Before the user sees one result
- Immediately after camera permission
- During an error or failed recognition
- While deleting or exporting data

The paywall clearly shows monthly and annual cost, renewal terms, trial length, restore purchase, and cancellation information.

---

## 10. Visual direction

### Overall feeling

- Warm
- Calm
- Trustworthy
- Spacious
- Human
- Modern without looking like a science-fiction scanner

### Logo concept

A simple plate or circular form surrounded by seven subtle marks representing the days of a week. The shape should remain recognizable at small app-icon size.

Avoid:

- A literal number seven sitting on a plate
- Body silhouettes
- Measuring tape imagery
- Medical crosses
- Aggressive flames
- Neon “AI” effects

### Interface style

- Soft neutral background
- Dark readable text
- One fresh primary accent
- A separate gentle accent for estimates and uncertainty
- Rounded but not childish cards
- Food photography treated naturally
- Progress visuals that remain understandable without color

### Typography

Use a highly readable system-friendly typeface. Prioritize:

- Clear number shapes
- Comfortable large text
- Strong contrast
- Support for larger accessibility settings
- No condensed fonts for nutrition values

---

## 11. Phone and accessibility rules

Every core screen must work on:

- Compact iPhones
- Standard and large iPhones
- Common compact Android phones
- Standard and large Android phones
- Tall and narrow screens
- Larger accessibility text
- Light and dark appearance

### Interaction rules

- Important buttons remain reachable near the lower half of the screen.
- Minimum comfortable touch area for every action.
- No essential meaning communicated by color alone.
- Nutrition charts have text summaries.
- Camera guidance includes spoken/screen-reader labels.
- The user can complete meal logging with one hand.
- Keyboard appearance must not hide the main action.
- Loading states, poor connection, image failure, and recognition failure all have clear recovery actions.

---

## 12. Important empty and error states

### No meals yet

> Your day is ready when you are.
>
> Scan, search, or repeat a meal to begin.

### Meal not recognized

> We could not identify this meal confidently.
>
> You can try another photo, choose likely foods, or enter it manually.

Actions:

- Try another photo
- Choose foods
- Enter manually

### Slow connection

> This is taking longer than usual.
>
> You can keep waiting or save the photo and finish later.

### No camera permission

> Camera access is off.
>
> You can choose a photo or log manually without changing your settings.

### Result has high uncertainty

> We need a little more information before showing a useful estimate.

Ask one meaningful question rather than displaying an unreliable number.

---

## 13. First design sprint scope

Design and test these screens first:

1. Welcome
2. Goal selection
3. First meal action
4. Camera/photo selection
5. Processing
6. Meal review and clarification
7. Nutrition result
8. Save/account prompt
9. Today screen after first meal

### Sprint success criteria

- A first-time user understands the app’s purpose within five seconds.
- At least 80% of test users can start a meal scan without help.
- Users understand that the result is an estimate, not an exact measurement.
- Median scan-to-result interaction time is 45 seconds or less, excluding network processing.
- Users can correct a wrong food without restarting.
- Users can identify the largest source of uncertainty.
- Users can complete the flow with larger text enabled.
- The product name is not interpreted primarily as seven meals per day after seeing the subtitle and welcome screen.

---

## 14. Current design decisions

1. Use **My Seventh Meal** as the provisional design name.
2. Use `Photo Nutrition & Macros` as a clear descriptor while the name is tested.
3. Use `A clearer picture of what you eat.` as the lead message.
4. Use **Photo Meal Estimate** as the formal feature name and **Scan a meal** as the main action.
5. Keep the first release nutrition-first; activity and weight remain supportive features.
6. Show value before a paywall and, where practical, before full account setup.
7. Use ranges and explanations whenever uncertainty remains.
8. Make recipe memory central to the experience, not an advanced hidden feature.
9. Design the core flow for compact phones and larger accessibility text first.
10. Continue final name clearance and user comprehension testing in parallel with interface design.
