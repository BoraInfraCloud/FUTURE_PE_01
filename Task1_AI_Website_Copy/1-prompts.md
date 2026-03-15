# 📋 Task 1 — Prompt Engineering System
## AI Website Copy Generator for Local Businesses
**Intern:** Bora Karthik | **CIN:** FIT/MAR26/PE2027 | **Track:** Prompt Engineering (PE)
**Repository:** FUTURE_PE_01 | **Tool Used:** Claude AI + Stitch AI (Website Builder)

---

## 🧠 Prompt Architecture: RCTF-X Framework

All prompts in this project follow the **RCTF-X Framework** — a 5-layer professional prompt engineering structure used in MNC consulting and digital agency workflows:

| Layer | What It Does |
|-------|-------------|
| **R** — Role | Assigns an expert professional persona to the AI |
| **C** — Context | Provides full business, audience, location, and tone details |
| **T** — Task | Defines exactly what to produce with zero ambiguity |
| **F** — Format | Specifies structure, word limits, section labels, output style |
| **X** — eXamples | Sets quality benchmarks and forbidden patterns |

The system uses **5 prompts run in sequence** — each one builds on the previous output, creating a compound, layered content system rather than isolated one-off generations.

---

## 🔷 PROMPT 1 — System Context Prompt
> **Purpose:** Run this FIRST in every Claude/AI session. Sets the expert persona and quality rules before any content is generated.

```
You are CopyBot-Pro, a senior UX copywriter and conversion strategist
with 15+ years of experience at McKinsey Digital, Accenture Interactive,
and Google's Growth team. You specialise in healthcare copywriting for
South Asian markets, with deep expertise in trust-building language,
zero-jargon patient communication, and CRO (conversion rate optimisation).

OPERATING RULES:
1. Never produce filler words, clichés, or placeholder text.
2. Every headline must pass the "5-second test": a visitor must understand
   the core benefit within 5 seconds of reading it.
3. All copy must be structured with clear HTML-ready section labels.
4. Tone is always: Warm > Professional > Trustworthy > Reassuring.
5. Forbidden words: "innovative", "world-class", "solutions", "synergy",
   "cutting-edge", "leverage". These kill credibility in healthcare.
6. Every CTA must contain a verb + benefit + urgency reducer.
7. Output must be directly usable in Stitch AI, Lovable, Framer AI, or Webflow AI.
```

---

## 🟢 PROMPT 2 — Client Discovery Brief
> **Purpose:** Passed as the first user message after the system prompt. Grounds the AI in exact business context before any content is generated.

```
CLIENT PROFILE:
  Business Name   : HealthFirst Clinic
  Type            : Multi-Specialty Outpatient Clinic
  Location        : Vijayawada, Andhra Pradesh, India
  Founded         : 2015 | Doctors: 15+ | Patients Treated: 10,000+
  Target Audience : Families (25-45), Working Professionals (30-55),
                    Senior Citizens (55-75), New Parents

BRAND VOICE PARAMETERS:
  Primary Emotion : Trust (not excitement)
  Language Level  : Class 8 readability (Flesch-Kincaid target: 65+)
  Forbidden Words : disease, diagnose, pathology, regime, prognosis
  Power Words     : care, family, together, here, safe, simple, clear

CONVERSION GOALS (ranked by priority):
  1. Online appointment booking
  2. Phone enquiry calls
  3. Walk-in patient visits

USP MATRIX:
  Rational USP  : Same-day appointments, 15+ specialists, transparent pricing
  Emotional USP : We treat you like family, not a case number
  Local USP     : Serving Vijayawada families for over 10 years

COMPETITOR WEAKNESSES TO EXPLOIT (ethically):
  - Long wait times at other clinics → We offer same-day slots
  - Hidden fees at corporate hospitals → We are transparent
  - Rushed consultations → We take time to listen
```

---

## 🔵 PROMPT 3 — Homepage Copy Master Prompt
> **Purpose:** Generates all 7 homepage sections in one structured output, including A/B test variants and micro-copy.

```
ROLE: Act as CopyBot-Pro [System Prompt loaded above].

CONTEXT: Client Brief — HealthFirst Clinic [Brief loaded above].
Page: Homepage — the single most important page on the website.
Visitor intent: "I or someone I know needs a doctor. Can I trust this place?"
Platform output: Stitch AI / Lovable / Framer AI (structured sections).

TASK — Generate ALL 7 sections below. Do not skip any:

  [SECTION 1] HERO HEADLINE
    - Max 8 words. Emotionally resonant. Patient-benefit-first.
    - Must answer: "What do I get and why should I care?"
    - Avoid: questions, negatives, generic phrases.
    - Generate: 3 headline variants (A/B/C) for split testing.

  [SECTION 2] HERO SUB-HEADLINE
    - Max 25 words. Expands on the headline promise.
    - Must include: location anchor (Vijayawada) + emotional hook.
    - Generate: 2 variants.

  [SECTION 3] TRUST BAR (Social Proof Strip)
    - Exactly 4 trust signals. Format: [NUMBER] + [DESCRIPTOR].
    - One must be time-based (e.g., Same-Day). One must be quantity.

  [SECTION 4] VALUE PROPOSITION BLOCK
    - Section headline (max 10 words) + 3 benefit cards.
    - Each card: Icon label (2-3 words) + 2 sentences (max 30 words each).
    - Cards must address: Expertise, Convenience, Affordability.

  [SECTION 5] ABOUT SECTION
    - 4 sentences exactly. Structure: Story > Mission > Proof > Promise.
    - Must name Vijayawada. Must not use "we are committed to".

  [SECTION 6] DOCTOR TRUST SECTION
    - 2 lines. Humanise the medical team. Avoid listing credentials.
    - Goal: make visitors want to meet the doctors, not fear them.

  [SECTION 7] MICRO-COPY
    - Form placeholder text: 3 examples
    - Error message (gentle): 1 example
    - Success message (after booking): 1 example

FORMAT RULES:
  - Label every section with [SECTION N] header.
  - Show VARIANT A / VARIANT B where requested.
  - After each section add: PLATFORM NOTE: [how to use in Stitch/Lovable/Framer].
  - End with: WORD COUNT AUDIT: [section-by-section word count table].
```

---

## 🟡 PROMPT 4 — Services Page Prompt
> **Purpose:** Generates 6 service cards with patient-friendly descriptions, benefit badges, and internal linking suggestions.

```
ROLE + CONTEXT: [As defined in System + Brief above]

TASK — Services Page Architecture:

  [SECTION 1] SERVICES HERO HEADLINE + INTRO
    - Headline: max 10 words. Patient-benefit led. NOT service-list led.
    - Intro: 2 sentences. Breadth of care + coordination promise.

  [SECTION 2] 6 SERVICE CARDS
    For EACH specialty, generate:
    a. Card Headline: Specialty name + emoji icon
    b. Patient description: 2 sentences, max 40 words total.
       Rule: Write for a worried patient, not a referring doctor.
    c. Benefit badge: 5 words max. Action-oriented.
    d. Platform note: Stitch AI / Lovable / Framer component type suggestion.

    Specialties required (in this order):
    1. General Medicine   2. Cardiology   3. Pediatrics
    4. Orthopedics        5. Gynecology   6. Diagnostics & Lab Tests

  [SECTION 3] REASSURANCE LINE
    - 1 sentence. Guides confused visitors to reception.
    - Must NOT use: "don't hesitate", "feel free to", "please contact".

  [SECTION 4] INTERNAL LINKING SUGGESTIONS
    - List 3 blog posts this page should internally link to.
    - Format: [Blog Title] → [Target keyword] → [Internal link anchor text].

FORMAT: Label all sections. Add platform component notes per card.
```

---

## 🔴 PROMPT 5 — CTA Engineering Prompt
> **Purpose:** Generates 5 strategically placed CTAs using AIDA and PAS psychological frameworks, each with A/B variants.

```
ROLE + CONTEXT: [As defined in System + Brief above]

TASK — Generate 5 strategically placed CTAs:

  [CTA 1] HERO PRIMARY CTA (Above the fold)
    Formula: VERB + BENEFIT + FRICTION REDUCER
    Generate: Primary button + Secondary link text
    Constraint: Primary button max 5 words. No exclamation marks.

  [CTA 2] MID-PAGE URGENCY CTA (After Value Proposition)
    Framework: PAS (Problem > Agitation > Solution)
    Generate: 2-sentence statement + 1 button
    Rule: Create urgency without fear. No "Don't wait until it's too late".

  [CTA 3] SOCIAL PROOF CTA (After Doctor Section)
    Framework: AIDA (Attention > Interest > Desire > Action)
    Generate: Quote-style trust statement + button
    Must include: A number, a local reference, and an action.

  [CTA 4] EXIT-INTENT / STICKY CTA (Mobile bottom bar)
    Generate: Ultra-short 3-word button + phone number format
    Optimised for: Mobile thumb reach, one-tap action.

  [CTA 5] FOOTER CONTACT CTA (Bottom of every page)
    Generate: Warm closing headline + full contact block + 2 buttons
    Contact block: Address, Phone, Email, Hours, Map link.

FORMAT: For each CTA add:
  - Platform placement: [Where in Stitch/Lovable/Framer/Webflow]
  - Psychological trigger: [What cognitive bias it uses]
  - A/B variant: [Alternative version to test against]
```

---

## ✅ BONUS: Copy QA Prompt
> **Purpose:** Run on ALL generated copy before uploading to any platform. Professional 10-point quality audit.

```
TASK: Review the website copy below against these 10 MNC-grade criteria.
Score each 1-10. Flag any score below 7 for revision.

QA CHECKLIST:
  [Q1]  Readability: Flesch-Kincaid grade level 6-8? (Simple language?)
  [Q2]  Trust signals: Does every section build, not break, trust?
  [Q3]  CTA clarity: Does every CTA have verb + benefit + friction reducer?
  [Q4]  Local relevance: Is Vijayawada mentioned naturally 2-3 times?
  [Q5]  Zero jargon: Are ALL medical terms replaced with patient language?
  [Q6]  Mobile scan: Can a user understand each section in 3 seconds?
  [Q7]  Headline power: Does the hero headline pass the 5-second test?
  [Q8]  Emotional arc: Does the page move from problem to solution to CTA?
  [Q9]  SEO basics: Are primary keywords used naturally (not stuffed)?
  [Q10] Uniqueness: Could this copy work for ANY clinic, or ONLY this one?

OUTPUT: Score table + Overall Grade + Sections to revise
```

---

*Intern: Bora Karthik | CIN: FIT/MAR26/PE2027 | Future Interns PE Track*
