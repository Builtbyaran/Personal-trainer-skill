---
name: training-nutrition-planner
description: >-
  Designs resistance-training programmes and nutrition targets from anthropometrics,
  bulk/cut/recomp goals, optional goal weight, and available gym equipment. Use when
  the user asks for a workout plan, training programme, gym routine, meal plan, diet,
  macros, calorie target, bulking, cutting, recomp, or equipment-limited training.
---

# Training & nutrition planner

## Role

Produce **individualised, equipment-aware** training blocks and **calorie/macro targets** from user inputs. This is educational fitness planning, not medical treatment. Keep language clear and actionable.

## Mandatory disclaimer (prepend or footnote once per deliverable)

Output is general fitness information, not medical or dietetic advice. The user should consult a qualified clinician before major diet/training changes if they have chronic disease, take prescription drugs, are pregnant, or have a history of eating disorders.

## Intake checklist (gather before prescribing numbers)

Ask only what is missing. Minimum useful set:

| Field | Why |
|--------|-----|
| Sex (for BMR formula) | Mifflin–St Jeor input |
| Age | BMR |
| Height & weight (and units) | BMR, rate of loss/gain sanity |
| Goal | Bulk / cut / recomp (maintain weight, reshape) |
| Goal weight (if any) & rough timeline | Pace check; optional |
| Training days per week | Split design |
| Experience level | Volume, complexity |
| Injuries / pain patterns | Exercise selection |
| Steps / job activity | NEAT / TDEE adjustment |
| Food constraints (vegan, allergies, halal, etc.) | Meal structure |
| **Gym inventory** | Exercise mapping (see below) |

## Gym equipment → exercise mapping

Build sessions **only** from what they list. Map common kit to patterns:

- **Barbell + rack**: squat, bench, row, deadlift, OHP, hip hinge variants.
- **Dumbbells**: unilateral work, presses, rows, lunges, curls, raises.
- **Cable stack / functional trainer**: flies, pulldowns, pushdowns, face pulls, curls.
- **Pull-up bar**: pull-ups/chin-ups (or band-assisted).
- **Bench (flat/incline)**: pressing, step-ups, supported rows.
- **Smith machine**: stable squat/bench variants if no free rack (note trade-offs briefly).
- **Leg press / hack squat**: quad volume if squatting is limited.
- **Machines (leg curl/extension, chest press, etc.)**: isolation when free weights missing.
- **Resistance bands**: warm-up, assistance, rows and lat-focused pulls, accessory volume.
- **Kettlebells**: swings, goblet squat, unilateral carries (if weight range exists).
- **Cardio only** (treadmill, bike, rower): programme must be honest—strength work is mostly bodyweight + bands or external gym; do not invent racks they do not have.

If equipment is sparse (e.g. dumbbells + bench only), prefer **full-body A/B** alternation, compound-first, moderate frequency.

## Energy & macros (standard practice)

1. **Convert** height/weight to metric if needed (store both for the user).
2. **BMR (Mifflin–St Jeor)**  
   - Men: \(9.99 m + 6.25 h - 4.92 a + 5\)  
   - Women: \(9.99 m + 6.25 h - 4.92 a - 161\)  
   \(m\) = kg, \(h\) = cm, \(a\) = years.
3. **TDEE** = BMR × activity factor: sedentary 1.2; light 1.375; moderate 1.55; active 1.725; very active 1.9+. Adjust with **steps/job**: add ~3–8% TDEE per +2000 steps/day band if they are otherwise sedentary (rough heuristic; state it is approximate).
4. **Target intake**  
   - **Cut**: TDEE − 300 to −500 kcal/day typical; deeper deficits only short-term and not for beginners with ED history. Aim ~0.25–0.75% body weight loss/week as a sanity band.  
   - **Bulk**: TDEE + 200 to +400 kcal/day typical; faster surpluses mostly add fat.  
   - **Recomp / maintenance**: TDEE ±100–200 or match TDEE with progressive training; slower scale change.
5. **Protein** (anchor first): **1.6–2.2 g/kg** body weight for hypertrophy-focused trainees; cutting bias toward **2.0–2.4 g/kg** if sustainable. Cap practical upper ~**2.2–2.4 g/kg** unless coached context.
6. **Fat**: **~0.6–1.0 g/kg** (women often mid–high of range). Never go so low that hormones suffer on sustained cuts—flag if fat would fall below ~0.5 g/kg.
7. **Carbs**: remaining calories. Note fibre (25–40 g) and hydration.

For **goal weight** paired with a date, compute average daily deficit/surplus implied and **sanity-check**: if implied change is roughly above ~1% body-weight loss per week long-term or a reckless surplus, soften the timeline or adjust the goal.

## Training design rules

- **Frequency**: 2–6 days/week based on availability; match split to days and recovery.
- **Splits** (examples): full-body; upper/lower; push/pull/legs; body-part (only if high volume + experience).
- Per session: **1–2 compounds** first, then accessories. **2–4 sets** per exercise for most; **8–15 reps** on many accessories; **main compounds** can use 3–8 rep ranges if experience permits (note technique demands).
- **Progression**: add load when reps hit top of target range with 1–2 reps in reserve (RIR), or add reps, then load. Deload **~every 4–8 weeks** or when joints/mood/strength crash—reduce volume ~40–50% for one week.
- **Conditioning**: optional 1–3×/week if equipment allows and goal isn’t pure strength; keep it **non conflicting** with leg-heavy days where possible.
- **RPE / RIR**: teach briefly (e.g. RIR 1–2 on compounds for most work).

## Output format (always use two sections)

### 1) Nutrition summary

- Estimated BMR, TDEE (show formula inputs).
- Goal calories, protein (g and g/kg), fat (g), carbs (g).
- One short paragraph translating targets into **meal structure** (e.g. 3 meals + snack) without pretend precision.
- If vegan/vegetarian: mention lysine-rich combinations or soy/tempeh/legumes + grains once.

### 2) Training programme

- Week schedule table: **Day | focus | session length estimate**.
- Each session: **Exercise | sets × reps | notes (tempo/RIR optional)**.
- Include **warm-up**: 5–10 min + build sets on first heavy lift.
- **Progression block** (3–4 bullets) specific to their programme.
- **Swap table** if an exercise is impossible (same pattern, different equipment).

## Quality checks before sending

- [ ] Exercises match **declared equipment**; no “use a barbell” if none listed.
- [ ] Calories/macros align mathematically (4/4/9 kcal per g P/C/F).
- [ ] Cut isn’t so aggressive it exceeds sensible weekly BW change for their context.
- [ ] Injuries respected; offer low-impact alternatives.
- [ ] Disclaimer included once.

## Tone

Direct, supportive, no shame. No extreme “hardcore” language. Avoid pseudo-scientific claims.
