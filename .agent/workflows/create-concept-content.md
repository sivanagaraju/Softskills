---
description: How to create all 7 content files for a new Softskills concept folder at Deep Practitioner level
---

# Workflow: Create Concept Content (Deep Practitioner Standard)

Use this workflow every time a new concept folder needs its 7 learning files created or rewritten. This applies to ALL concepts across ALL 12 Softskills topics.

---

## Pre-Flight Checks (Do Before Writing Any File)

1. Identify the exact concept folder path:

   ```
   C:\Users\sivan\Learning\Code\Softskills\<Topic>\<Subtopic>\<ConceptFolder>\
   ```

2. Search for 2–3 relevant real images **before** writing any file:
   - Priority 1: `upload.wikimedia.org` — search `site:wikimedia.org <concept keyword> diagram`
   - Priority 2: ResearchGate figures — `site:researchgate.net <concept> diagram`
   - Priority 3: University/research `.png/.jpg` with stable URLs
   - ❌ Never use: Pinterest, social media, hotlink-blocked CDNs
   - Image URLs must end in `.png`, `.jpg`, or `.svg` to embed correctly

3. Read the master task tracker to confirm concept is not already done:
   `C:\Users\sivan\.gemini\antigravity\brain\<conversation-id>\task.md`

---

## Step 1 — Create `01_Theory_and_Concepts.md`

**Target:** 300–500 lines

**Must include:**

- [ ] Quick Reference table at the top (TL;DR — 3–5 key principles)
- [ ] Every concept fully explained with its mechanism (not just named)
- [ ] At least 1 research citation per major section: study name, researcher, year, key finding, and *what it means for the practitioner*
- [ ] Competing theories or nuances acknowledged where they exist
- [ ] "What this means in practice" paragraph after every major section
- [ ] **Minimum 2 embedded images** using `![caption](URL)` syntax with source noted in caption
- [ ] At least 1 Mermaid diagram (`graph TD` or `mindmap`) showing a process or taxonomy
- [ ] Comparison tables for contrasting concepts (e.g., suppression vs regulation)
- [ ] Key Takeaways section at the end (6–8 numbered practitioner insights)

---

## Step 2 — Create `02_Techniques_and_Frameworks.md`

**Target:** 300–450 lines

**Must include:**

- [ ] Overview table at the top: technique name / when to use / time / difficulty
- [ ] For EACH technique:
  - Full step-by-step instructions
  - Rationale for EACH step (not just what to do — why this step works)
  - The scientific/psychological basis for why the technique works
  - What to do when it fails or doesn't produce results (failure modes)
  - Variations by context (introverts, high-stress, remote settings, etc.)
  - A worked/embedded example within the technique section
- [ ] At least 1 Mermaid diagram showing a technique's flow
- [ ] Research citations for at least 2 techniques

---

## Step 3 — Create `03_Practice_Exercises.md`

**Target:** 300–400 lines

**Must include:**

- [ ] Overview table: exercise name / focus / time / difficulty level (🟢🟡🔴)
- [ ] **Minimum 6 exercises**, ordered Beginner → Advanced
- [ ] For EACH exercise:
  - Goal statement
  - Setup instructions
  - Full step-by-step instructions
  - A **worked/filled-in example** showing what a strong response looks like (not blank templates)
  - Reflection prompts
- [ ] "How to Use These Exercises" intro explaining the sequencing logic

---

## Step 4 — Create `04_Real_World_Examples.md`

**Target:** 300–400 lines

**Must include:**

- [ ] **Minimum 6 scenarios**
- [ ] Scenarios must cover diverse contexts: tech/engineering workplace, leadership, personal relationships, cultural dynamics
- [ ] For EACH scenario:
  - Full situational context
  - **Inner monologue** of the character (what they are actually thinking)
  - Trigger/reaction breakdown table (trigger stimulus / body signal / emotion / intensity / situation severity / gap / core wound)
  - What a skilled coach or mentor would say to this person
  - Two contrasting outcomes: **Reactive outcome** vs **Regulated outcome**

---

## Step 5 — Create `05_Common_Mistakes.md`

**Target:** 250–350 lines

**Must include:**

- [ ] Overview table at the top listing all mistakes with a one-line summary
- [ ] **Minimum 8 mistakes**
- [ ] For EACH mistake:
  - Why smart/high-performing people make this mistake (the psychology)
  - What it sounds like in practice (verbatim examples, real language)
  - A diagnostic test to know if you're making this mistake
  - The real cost (what it produces long-term)
  - Exactly how to catch yourself and correct
- [ ] At least 1 Mermaid diagram (comparing the wrong pathway vs correct pathway)
- [ ] Research citations for at least 2 mistakes

---

## Step 6 — Create `06_Tools_and_Resources.md`

**Target:** 200–300 lines

**Must include:**

- [ ] "How to Use This Guide" intro (not just a book list — a recommended reading path)
- [ ] **Minimum 4 books** with full reviews including:
  - Who it's for
  - What it actually covers (not just a blurb)
  - A key quote or insight
  - What the book **won't** do (honest scope)
  - A ⭐ label indicating priority/sequence
- [ ] **Minimum 2 apps** with specific usage instructions for THIS concept (not generic)
- [ ] **Minimum 2 videos/talks** with search terms, what key insight to extract
- [ ] At least 1 therapeutic framework explained (IFS, ACT, Polyvagal, EMDR, etc.) with how it relates to the concept
- [ ] A printable **Quick Reference Card** — formatted as a code block, immediately usable

---

## Step 7 — Create `07_Assessment_and_Reflection.md`

**Target:** 250–350 lines

**Must include:**

- [ ] Section 1: Knowledge Check with **validation questions** (not just "can you explain X?" but a scenario with a **model answer** so the reader knows the expected standard)
- [ ] Section 2: Personal Profile tables — the reader fills in their own data
- [ ] Section 3: Scenario Response Assessment — 2–3 scenarios where the reader writes what they'd do, followed by a **model response for comparison**
- [ ] Section 4: Skill Rating with **behavioural anchors** (what does 1/5 look like vs 3/5 vs 5/5 — must be specific observable behaviours, not just "I don't do it" vs "I always do it")
- [ ] Section 5: Forward-looking commitment section with specific success criteria
- [ ] Section 6: Connecting Forward — Mermaid diagram showing how this concept feeds into the next one
- [ ] Concept Completion Checklist at the end

---

## Post-Creation Checks

After all 7 files are created:

// turbo

1. Run line count verification:

   ```powershell
   (Get-ChildItem "<ConceptFolderPath>\*.md") | ForEach-Object { $lines = (Get-Content $_.FullName).Count; "{0,-50} {1,5} lines" -f $_.Name, $lines }
   ```

2. Confirm all files meet minimums:
   - `01_Theory`: 300+ lines
   - `02_Techniques`: 300+ lines
   - `03_Exercises`: 300+ lines
   - `04_Examples`: 227+ lines
   - `05_Mistakes`: 250+ lines
   - `06_Resources`: 200+ lines
   - `07_Assessment`: 250+ lines

3. Update the task tracker: mark the concept `[x]` in `task.md`

4. State the next concept clearly so the user knows what is ready to proceed
