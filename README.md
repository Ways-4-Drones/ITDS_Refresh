
# ODU Business Analytics & AI — Landing Page Redesign
 
A redesigned program landing page for the proposed **BSBA in Business Analytics & Artificial Intelligence** at Old Dominion University's Strome College of Business, Department of Information Technology & Decision Sciences.
 
Prepared for review at the **Fall 2026 IT&DS faculty meeting**.
 
---
 
## View the site
 
The live page is served via GitHub Pages from `index.html` at the root of this repository. If Pages is enabled on the repo settings, visit:
 
**`https://<your-org>.github.io/<repo-name>/`**
 
To preview locally, no build step is needed — open `index.html` directly, or serve it with any static server:
 
```bash
python -m http.server 8000
# then visit http://localhost:8000
```
 
The page is a single self-contained HTML file with embedded CSS and JavaScript. No dependencies, no build tooling, no framework — chosen so any faculty member can fork it, edit it, and re-deploy without setting up Node or React.
 
---
 
## What's on the page
 
The page is organized as a linear scroll rather than an anchor-driven set of disconnected sections. Structure:
 
1. **Hero** — program name, STEM designation, one-line thesis
2. **At a glance** — 4 headline stats (credits, experiential hours, salary, STEM)
3. **The Curriculum** — an **interactive 5-phase journey** (click each phase to reveal courses)
4. **Featured Courses** — the three new courses that make this a Business Analytics *& AI* degree
5. **Careers** — median salary data for four target roles, two of which are new
6. **Experiential Learning** — internship + community engagement + capstone, each with hour counts
7. **What's Changing** — a **side-by-side diff view** comparing the existing program to the proposal (this is the section written for the faculty audience specifically)
8. **Next Steps** — application, request info, visit, cost estimate
9. **Contact** — department contact card
---
 
## Key changes from the existing site
 
Comparing this design to the current [Business Analytics & Intelligence program page](https://www.odu.edu/academics/programs/undergraduate/business-analytics-intelligence):
 
### Structural changes
 
| Existing site | This redesign |
| :-- | :-- |
| Anchor navigation with disconnected sections | Linear scroll with a section-by-section arc |
| Curriculum shown as a static three-course "Featured Courses" list | Interactive 5-phase Curriculum Journey with all 27+ courses visible on click |
| Program highlights in a bulleted list | Program highlights split across the hero, at-a-glance stats, and featured courses |
| Careers listed with median salary buried in the description | Careers lead with the salary number, with role and description supporting it |
| Experiential learning implied ("internships available") | Experiential learning is its own destination section with hour counts and course codes |
| No section that explains changes from a prior version | Dedicated "What's Changing" diff view for faculty and curriculum committee use |
 
### Content changes (reflect the proposed program)
 
- **Program name:** "Business Analytics & Intelligence" → "Business Analytics & Artificial Intelligence"
- **STEM designation:** promoted from absent to prominent (badge in the hero, callout in stats, dedicated line in the diff view)
- **Course prefix:** BNAL / IT / mixed → unified **BUAN** prefix
- **Tools taught:** Excel / R / Tableau / SAS → **Python / pandas / scikit-learn / TensorFlow** (plus Tableau, Power BI, SQL)
- **New required courses:** BUAN 3301 (AI in Business), BUAN 4381 (Python), BUAN 4383 (Machine Learning for Business Analytics), BUAN 4373 (Data Science for Business Applications), BUAN 4320 (Database Fundamentals for Analytics)
- **Experiential learning:** all three components (internship, community engagement, capstone) are graduation requirements rather than opt-in
### Design & UX changes
 
- **Typography:** Sora (ODU brand web face) + Space Grotesk (Monte Stella stand-in) + JetBrains Mono for data — pulled directly from the ODU FY26 Forward-Focused brand toolkit rather than reusing template defaults
- **Palette:** Monarch Blue, Silver Reign, Hudson Blue, Electric Teal, coastal sand — all from ODU's primary + secondary palette
- **Accessibility:** WCAG AA color pairings, visible focus indicators, keyboard-navigable curriculum journey (arrow keys), reduced-motion respected, semantic landmarks, skip-to-content link
- **Responsive:** single-column at ≤900px, grid at desktop; no dependencies on JavaScript for core content
- **Motion:** deliberate and minimal — a light hover state on cards, a smooth phase transition, nothing gratuitous
---
 
## Benchmarks that shaped the design
 
- **[Indiana Kelley](https://kelley.iu.edu/programs/full-time-mba/academics/experiential-learning/1kelley/undergraduate-students/index.html)** — the way Kelley elevates experiential learning (1Kelley) to a first-class program feature, not a footnote
- **[University of Cincinnati Lindner College](https://www.business.uc.edu/programs-degrees/undergraduate/majors/bs-business-analytics.html)** — how the "Why study" framing sets up the discipline
- **[UT Dallas JSOM Business Analytics](https://infosystems.utdallas.edu/bs-business-analytics/curriculum/)** — clarity of the curriculum-block layout
None of the benchmarks include a diff view for their curriculum revisions. That section is unique to this design and is included specifically for the faculty audience.
 
---
 
## For faculty reviewers
 
The page is deliberately opinionated. If you'd like to see a particular decision reversed (a different section order, different featured courses, different careers), the file is small enough that changes are quick — everything is in `index.html`.
 
Course lists in the interactive Curriculum Journey are driven by a single JavaScript object (`PHASES`) near the bottom of `index.html`. Adding, removing, or renaming a course is a one-line edit.
 
---
 
## Repository layout
 
```
.
├── index.html      # the landing page (self-contained)
└── README.md       # this file
```
 
---
 
## License / attribution
 
Content and course codes reflect the proposed program at ODU Strome College of Business. Program page structure and identifying content adapted from [ODU's existing academic program pages](https://www.odu.edu/academics/programs/undergraduate/business-analytics-intelligence). ODU brand guidelines from the [University Communications brand toolkit](https://www.odu.edu/university-communications/brand-toolkit/palette-fonts).
 
Fonts served via Google Fonts (Sora, Space Grotesk, JetBrains Mono).
