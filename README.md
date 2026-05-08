# Personal Trainer skill for Claude

Turn Claude into a coach. One file. Programs, macros, equipment-aware splits, and a re-prescribe protocol so it acts like an actual PT — not just a one-shot output.

Built by [@builtbyaran](https://www.instagram.com/builtbyaran).

---

## What it does

- Builds **individualised resistance training programmes** (full-body, upper/lower, push/pull/legs) sized to your days, equipment, and experience.
- Calculates **calories + macros** using Mifflin–St Jeor and current sports-nutrition ranges (1.6–2.2 g/kg protein, 0.6–1.0 g/kg fat, etc.).
- Maps your **gym inventory** to exercises — never asks you to use a barbell you don't have.
- Handles **conflicting goals** ("lose 10 kg AND gain 5 kg muscle in 8 weeks") by surfacing the conflict and proposing a phased sequence instead of over-promising.
- Knows the **female-athlete edge cases** (cycle awareness, iron, peri/menopause, postnatal).
- Has a **re-prescribe protocol**: come back after 2–4 weeks with weight delta + adherence + soreness, it adjusts calories ±100–150, swaps volume, schedules deloads.
- Always shows units in **metric and imperial**.

---

## Install

The skill is a single folder (`personal-trainer/`) with a `SKILL.md` inside. Drop it where Claude can find it.

### Option 1 — Claude Code (every project on your machine)

```bash
git clone https://github.com/Builtbyaran/Personal-trainer-skill.git
cp -r Personal-trainer-skill/personal-trainer ~/.claude/skills/
```

Restart Claude Code. Skill is now active everywhere.

### Option 2 — Claude Code (one project only)

```bash
mkdir -p .claude/skills
cp -r personal-trainer .claude/skills/
```

Skill is only active inside that project.

### Option 3 — claude.ai (web / desktop)

Settings → Capabilities → Skills → Upload → pick `personal-trainer/SKILL.md`.

Available in every chat after that.

---

## How to trigger it

Once installed, Claude auto-invokes the skill when you say things like:

- *"Build me a 4-day upper/lower split, 84 kg, dumbbells + bench at home."*
- *"What should I eat to cut to 78 kg in 16 weeks?"*
- *"Give me macros for a lean bulk."*
- *"Plan me a push/pull/legs."*
- *"How often should I train?"*

You can also invoke it manually: *"Use the personal-trainer skill to ..."*.

---

## Example prompt

```
M, 32, 178 cm, 86 kg. Want to cut to 78 kg in ~16 weeks.
4 days/week. Intermediate.
Home gym: barbell + rack, bench, adjustable dumbbells to 40 kg, pull-up bar.
Office job, ~6k steps. Sleep ~6.5h. No allergies.
```

You'll get back:

- Nutrition summary table (BMR / TDEE / target kcal / protein / fat / carbs / hydration / fibre, in both metric and imperial)
- Suggested meal structure for the day
- Full week schedule
- Each session laid out with sets × reps × RIR
- Progression rules
- Equipment swap table for if a lift becomes impossible
- A conditioning slot placement that doesn't trash your leg day

Then check back in 2–4 weeks with weight delta + adherence and it'll re-prescribe.

---

## What it won't do

- Recommend banned compounds, extreme deficits, or "training through" sharp pain.
- Pretend to be a doctor or dietitian. The skill prepends a disclaimer and points you to a clinician for chronic disease, medication interactions, pregnancy, or ED history.
- Invent equipment you don't have.

---

## Updates

This skill is iterated. To pull new versions:

```bash
cd Personal-trainer-skill
git pull
cp -r personal-trainer ~/.claude/skills/
```

Or refresh the upload in claude.ai's Skills panel.

---

## License

MIT — use it, fork it, modify it. Credit appreciated, not required.

---

## Other skills + content

- Instagram: [@builtbyaran](https://www.instagram.com/builtbyaran)
- Free AI starter pack: <https://builtbyaran.gumroad.com/l/ighbb>
- More on the way — agent skills, content pipelines, lead-gen workflows.
