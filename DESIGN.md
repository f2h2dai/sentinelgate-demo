# DESIGN.md

## Purpose

This file is the canonical visual design contract for this project.

Every coding agent, designer, or implementation tool must read this file before changing the user interface.

The objective is not to make the interface look "less AI-generated" through cosmetic tricks.

The objective is to make the interface look intentionally designed for this specific product, its users, its workflow, and its information.

AI may build the interface.

AI must not become the visual identity of the interface.

---

# 1. Project Profile

Complete this section before redesigning or building UI.

```
project:
  name: "SentinelGate"
  product_type: "On-prem agent acceptance and assurance workspace"
  primary_user: "AI platform engineer, security reviewer, and Cybersecurity reviewer"
  primary_task: "Determine whether an AI/agent project is ready to cross the enterprise trust boundary and prepare evidence for Cybersecurity review"

  environment:
    "desktop | web | internal | enterprise | public-demo"

  density:
    "high"

  visual_world:
    "Enterprise review workspace centered on acceptance records, evidence, blockers, capability boundaries, and Cybersecurity handoff."

  personality:
    - "measured"
    - "evidence-led"
    - "operational"

  primary_workflow:
    - "inspect project and map boundaries"
    - "review judgment and runtime evidence"
    - "prepare Cybersecurity handoff and track post-deploy effects"

  avoid_visual_associations:
    - "generic AI dashboard"
    - "generic SaaS template"
    - "SOC command-center aesthetic"
```

Bad:

```
Modern
Premium
Clean
Futuristic
AI-powered
Beautiful
```

Better:

```
Records operations workspace for reviewing,
approving, retrieving and auditing documents.
```

Or:

```
Public-source intelligence workspace focused on
signals, evidence, context and decisions.
```

The interface must derive from the product's job, not from adjectives.

---

# 2. Core Principle

Before creating any visual element, answer:

```
What job does this element perform?
```

If there is no functional, informational, navigational, or branding reason for it:

```
do not add it.
```

Prefer:

```
purpose
→ hierarchy
→ structure
→ interaction
→ styling
```

Never:

```
styling
→ decoration
→ invented content
→ product
```

---

# 3. Anti-AI Fingerprint Policy

Do not automatically use patterns commonly produced by generic AI frontend prompts.

These patterns are not forbidden.

They require justification.

## Patterns requiring justification

```
purple / blue gradients
cyan technology accents
neon colors
glow
glassmorphism
blurred floating panels
large rounded cards
pill-shaped controls everywhere
bento grids
three-column feature grids
huge centered hero sections
generic KPI cards
floating badges
sparkle icons
robot icons
brain icons
"AI" decorative imagery
animated blobs
decorative dashboards
fake charts
fake metrics
fake activity feeds
fake testimonials
oversized whitespace
generic dark navy SaaS themes
gradient text
command-center aesthetics
terminal aesthetics
```

Never add these merely because the product uses AI.

---

# 4. Do Not Create Another Template

Anti-AI design must not become another repetitive style.

Do NOT make every project:

```
white
black
red
minimal
editorial
square
```

Do NOT copy a visual metaphor from one project into another simply because it worked previously.

Archive software, intelligence software, developer tools, consumer apps, healthcare systems and financial products should not automatically look alike.

The reusable element is the design discipline.

The visual identity remains project-specific.

---

# 5. Visual Decision Hierarchy

When choosing a design direction, use this priority:

```
1. Product purpose
2. User task
3. Information hierarchy
4. Environment
5. Accessibility
6. Interaction requirements
7. Existing brand
8. Visual style
```

Never reverse this order.

---

# 6. Color System

Color must communicate one of:

```
identity
state
priority
category
interaction
```

Do not use color merely to make the interface look technological.

## Required token structure

```
:root {
  --canvas: ;
  --surface: ;

  --ink: ;
  --text-secondary: ;
  --text-muted: ;

  --border: ;
  --border-strong: ;

  --brand: ;

  --success: ;
  --warning: ;
  --critical: ;
  --info: ;
}
```

Not every project needs every token.

---

## Global Accent Rule

Avoid one bright global `--accent` controlling:

```
links
buttons
tabs
navigation
charts
borders
icons
focus states
status
```

This frequently produces template-like interfaces.

Prefer semantic usage.

Example:

```
navigation selection → typography / underline
verified state       → success
warning              → warning
critical             → critical
brand moment         → brand
```

---

# 7. Semantic Color

Status must never depend on color alone.

Bad:

```
● green
● yellow
● red
```

Better:

```
Verified
Review required
Critical
```

Color supports the state label.

It does not replace it.

---

# 8. Typography

Typography is part of product identity.

Do not default to:

```
Inter everywhere
```

without considering the product.

However, application interfaces should prioritize readability.

Define:

```
typography:
  display:
  heading:
  body:
  label:
  data:
  mono:
```

Use monospace only for data such as:

```
timestamps
IDs
hashes
scores
logs
commands
machine values
```

Do not use monospace to simulate "technical sophistication."

---

# 9. Information Hierarchy

Use this order:

```
Primary task
↓
Primary information
↓
Context
↓
Metadata
↓
Secondary actions
↓
System details
```

System implementation details should not dominate user-facing product UI.

For AI products, avoid leading with:

```
agents
models
providers
orchestrators
pipelines
workers
embeddings
tokens
LLM routes
```

unless the user is specifically operating those systems.

---

# 10. Layout

Derive layout from workflow.

Do not automatically create:

```
left sidebar
+
top navbar
+
dashboard grid
+
right utility rail
```

Determine whether the product actually requires them.

Questions:

```
What must remain visible?

What requires comparison?

What needs scanning?

What needs sequential reading?

What requires persistent navigation?

What information belongs together?
```

Then derive the layout.

---

# 11. Containers

Default:

```
content does not require a card.
```

Before adding a card ask:

```
Does this content represent a standalone object?
```

If no:

use:

```
spacing
rules
lists
rows
tables
groups
sections
```

instead.

---

# 12. Card Discipline

When cards are justified:

```
Use the minimum visual containment required.
```

Avoid:

```
card inside card
card for every paragraph
large shadows
decorative gradients
large radius
floating surfaces
```

Card styling must come from project tokens.

Never create five different card styles in one product.

---

# 13. Border Radius

Radius is not decoration.

Define a restrained scale:

```
--radius-xs:
--radius-sm:
--radius-md:
--radius-lg:
```

Do not automatically use:

```
16px
20px
24px
999px
```

Pills should be reserved for content that logically behaves like:

```
compact status
filter token
selection token
```

---

# 14. Shadows

Default:

```
no shadow
```

Use shadows when communicating:

```
elevation
overlay
popover
modal
drag state
```

Do not use shadows to make every container appear floating.

---

# 15. Navigation

Navigation must reflect product information architecture.

Do not expose every internal system area equally.

Separate:

```
primary user workflows
```

from:

```
administration
settings
diagnostics
system internals
```

Active state should generally rely on:

```
position
weight
underline
background
border
```

before adding bright color.

---

# 16. Buttons

Button hierarchy:

```
Primary
Secondary
Danger
Quiet / text action
```

Do not create different button styles for every screen.

Primary buttons represent primary actions.

Do not make non-primary actions visually dominant.

---

# 17. Data Interfaces

For products containing substantial information, prefer:

```
tables
rows
lists
timelines
structured metadata
filters
split views
```

over:

```
large cards
illustrative graphics
decorative dashboards
```

Use charts only when the chart communicates something more efficiently than text or numbers.

Never generate a chart merely because the page is called:

```
Dashboard
```

---

# 18. Dashboard Rule

A dashboard must answer:

```
What changed?
What needs attention?
What should the user do?
```

Do not create KPI cards merely to fill the top of a dashboard.

Metrics must come from real data.

Do not display metrics without decision value.

---

# 19. Content Before Decoration

The visual hierarchy should remain understandable if all decorative styling is removed.

Test mentally:

```
Remove:
colors
shadows
images
animation
radius
```

If the page hierarchy collapses, the structure is weak.

Fix structure before styling.

---

# 20. Images

Images must have a reason.

Valid:

```
product evidence
story context
geography
document preview
physical object
person
location
research subject
```

Avoid:

```
AI-generated abstract waves
generic robots
glowing brains
floating cubes
random 3D geometry
technology stock imagery
```

Use imagery to provide information or identity.

---

# 21. Motion

Default:

```
minimal
```

Motion should communicate:

```
state change
navigation
progress
relationship
feedback
```

Recommended duration:

```
120–220ms
```

Avoid:

```
continuous decorative animation
floating elements
background motion
gradient animation
pulsing glow
```

unless required by the product.

---

# 22. Hover Behavior

Hover may reveal:

```
secondary actions
preview
context
metadata
```

Do not hide primary functionality behind hover.

All hover interactions must also support keyboard focus.

---

# 23. Empty States

Empty states explain:

```
what this area contains
why it is empty
what the user can do next
```

Do not fill empty states with decorative illustrations by default.

---

# 24. Loading States

Loading states must reflect actual system state.

Prefer:

```
skeleton
progress
status text
```

Avoid fake progress values.

Never display:

```
97% complete
```

unless the system knows the actual percentage.

---

# 25. Error States

Errors must state:

```
what failed
what was preserved
what the user can do
```

Do not simply show:

```
Something went wrong.
```

---

# 26. Responsive Design

Design for:

```
large desktop
desktop
tablet
mobile
```

Minimum validation widths:

```
1440
1280
1024
768
390
```

Responsive design is not:

```
shrink everything.
```

It is:

```
preserve task hierarchy
change layout
maintain readable density
keep primary actions reachable
```

---

# 27. RTL / Arabic

If Arabic is supported:

test actual RTL layout.

Verify:

```
navigation
headings
paragraphs
mixed Arabic/English
numbers
dates
timestamps
technical terms
tables
forms
icons
directional arrows
```

Do not reverse English technical strings.

Use bidirectional isolation where required.

---

# 28. Accessibility

Target WCAG 2.2 AA where applicable.

Validate:

```
contrast
keyboard navigation
visible focus
labels
semantic HTML
form errors
heading hierarchy
screen-reader names
status announcements
reduced motion
touch targets
```

Accessibility requirements override decorative preferences.

---

# 29. Product-Specific Components

Before creating a generic component library, identify domain components.

Examples:

Document system:

```
Document row
Review record
Metadata editor
Duplicate comparison
Archive destination
```

Intelligence system:

```
Signal record
Evidence record
Entity
Timeline
Source confidence
```

Infrastructure system:

```
Service state
Incident
Deployment
Change
Log stream
```

The product should visually express its domain.

Not merely:

```
Card
Card
Card
Button
Chart
```

---

# 30. Reuse Rule

Reuse:

```
behavior
tokens
interaction logic
component primitives
```

Do not force visually identical components onto semantically different information.

Consistency does not mean sameness.

---

# 31. Redesign Protocol

Before redesigning an existing product, classify each significant visual element:

```
KEEP
REFINE
REPLACE
REMOVE
```

Definitions:

### KEEP

Correct design and implementation.

### REFINE

Correct concept, weak execution.

### REPLACE

Function is required, visual pattern is wrong.

### REMOVE

Element adds no useful function or information.

Do not redesign everything merely because redesign mode is active.

---

# 32. Redesign Order

Use this sequence:

```
1. Product workflow
2. Information architecture
3. Design tokens
4. Typography
5. Color
6. App shell
7. Navigation
8. Layout
9. Shared components
10. Domain components
11. Individual pages
12. Responsive behavior
13. Accessibility
14. Visual validation
```

Do not begin by changing colors.

---

# 33. Existing Product Rule

Never stack a new design system on top of an old one.

Do not solve redesign through:

```
another CSS override block
```

Instead:

```
identify obsolete styles
remove them
consolidate tokens
replace conflicting rules
remove dead CSS
```

There must be one active design language.

---

# 34. AI Agent Execution Contract

Every coding agent modifying UI must:

```
1. Read DESIGN.md.
2. Inspect the existing implementation.
3. Identify the user workflow affected.
4. Identify reusable existing patterns.
5. Check prohibited/default patterns.
6. Implement.
7. Run the application.
8. Review visually.
9. Test responsive behavior.
10. Test accessibility.
11. Review the diff.
```

The agent must not introduce a new visual system silently.

---

# 35. DESIGN.md Authority

When conflict exists between:

```
agent design preference
generic frontend trend
existing accidental styling
DESIGN.md
```

`DESIGN.md` wins unless:

```
functionality
accessibility
security
explicit product requirement
```

requires otherwise.

Any permanent design change must update `DESIGN.md` in the same change.

---

# 36. No Blind Framework Redesign

Do not migrate frontend frameworks merely to improve appearance.

For example:

```
HTML → React
React → Next.js
CSS → Tailwind
```

is not a design solution.

Framework migration requires an independent engineering justification.

---

# 37. No Fake Product Data

Never create:

```
fake metrics
fake alerts
fake users
fake charts
fake activity
fake statuses
fake operational data
```

to improve screenshots.

Use real application state.

Use clearly identified demonstration data only when demo mode exists.

---

# 38. Anti-Template Review

After implementation ask:

```
Could this interface easily belong to an unrelated AI startup?
```

If yes:

investigate why.

Typical causes:

```
generic hero
generic cards
generic palette
generic typography
generic dashboard
generic icons
lack of domain components
lack of real data hierarchy
```

---

# 39. Cross-Project Fingerprint Review

Compare the new project against previous projects.

Ask:

```
Did we reuse the same:
palette?
sidebar?
card system?
hero?
typography?
dashboard layout?
navigation?
```

If yes without product justification:

change it.

The goal is not to create a personal template shared by every project.

---

# 40. Visual Acceptance Gate

Before accepting frontend work verify:

## Product fit

```
Does the interface visibly reflect what this product does?
```

## Information hierarchy

```
Can the user identify the primary information quickly?
```

## Template drift

```
Did generic AI/SaaS patterns appear without justification?
```

## Color

```
Does every non-neutral color have a purpose?
```

## Containers

```
Are cards used only when containment is useful?
```

## Data

```
Is visible data real?
```

## Interaction

```
Do controls work?
```

## Responsive

```
Does the workflow survive narrow layouts?
```

## Accessibility

```
Can keyboard and assistive users operate the interface?
```

## Localization

```
Do RTL and mixed-language content work?
```

---

# 41. Failure Conditions

Do not approve the design if:

```
the interface looks like a generic AI SaaS template
the hierarchy depends primarily on colored cards
decorative AI imagery dominates
fake data was introduced
multiple design systems coexist
desktop is acceptable but mobile is broken
Arabic support is cosmetic only
system internals dominate the user's task
every section becomes a card
visual complexity exceeds informational value
```

---

# 42. Completion Requirements

Before committing UI work:

```
review DESIGN.md
review Git diff
run relevant tests
run application
inspect browser console
verify real data
verify interactions
verify responsive behavior
verify keyboard behavior
verify RTL when supported
compare against project identity
perform anti-template review
```

Never claim an unexecuted check.

---

# 43. Project Override Section

Everything below this point is project-specific.

Do not copy these values from another project.

```
project_design:
  visual_world: "Enterprise review workspace for acceptance evidence, blockers, and handoff."

  canvas: "#F2F4F1"
  surface: "#FFFFFF"
  ink: "#18211D"
  secondary_text: "#53605A"
  border: "#D9DFDB"

  brand_color: "#2F5D50"

  semantic:
    success: "#267451"
    warning: "#9A6519"
    critical: "#AD3D3D"
    info: "#3B5E79"

  typography:
    interface: "Segoe UI / Aptos / Arial"
    editorial: "none"
    data: "Cascadia Mono / Consolas"

  radius:
    xs: "3px"
    sm: "5px"
    md: "8px"

  layout:
    max_width: "1440px"
    navigation: "persistent left review navigation on desktop; compact horizontal workflow navigation on mobile"
    density: "high"

  imagery:
    policy: "No decorative AI imagery. Use only evidence/document previews or product-specific operational imagery when informative."

  domain_components:
    - "Acceptance record"
    - "Judgment case"
    - "Capability boundary"
    - "Decision ledger record"
    - "Effect expectation"
    - "Cyber handoff manifest"
```

---

# 44. Final Rule

The goal is not:

```
Make it look human-designed.
```

The goal is:

```
Make every design decision explainable
by the product, user, workflow, content,
brand, or interaction.
```

If a visual decision cannot be explained by one of those:

remove it.

---

# Design Philosophy

```
Product-specific over fashionable.

Information over decoration.

Hierarchy over effects.

Real data over mock metrics.

Domain components over generic cards.

Semantic color over global accent.

Interaction over animation.

Consistency over repetition.

Accessibility over aesthetics.

Intentional design over AI defaults.
```