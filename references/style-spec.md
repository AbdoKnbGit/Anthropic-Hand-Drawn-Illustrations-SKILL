# Anthropic Hand-Drawn Editorial Illustration Style Specification

## 1. Overview & Provenance

This specification defines the exact visual system, drawing grammar, color logic, and compositional architecture of Anthropic's hand-drawn editorial illustration language (as featured across anthropic.com, research papers, newsroom announcements, and product interfaces).

The system is built upon a fundamental design philosophy: **Humanism in Ink meets Computational Geometry**. It pairs warm, naive, imperfect analog dip-pen marks with clean, structured computational motifs (nodes, trees, graphs, grids).

---

## 2. The 3-Layer Architectural System

Every valid Anthropic illustration must be constructed from exactly three distinct spatial layers:

```text
┌────────────────────────────────────────────────────────┐
│  LAYER 1: Full-Bleed Opaque Accent Field (Canvas)      │
│  ┌──────────────────────────────────────────────────┐  │
│  │  LAYER 2: Irregular Ivory Carrier Shape (#FAF9F5)│  │
│  │  ┌────────────────────────────────────────────┐  │  │
│  │  │  LAYER 3: Bold Black Gestural Ink (#141413)│  │  │
│  │  │  • Naive analog brush/dip-pen strokes      │  │  │
│  │  │  • Solid circular nodes & connecting lines │  │  │
│  │  └────────────────────────────────────────────┘  │  │
│  └──────────────────────────────────────────────────┘  │
└────────────────────────────────────────────────────────┘
```

### Layer 1: Full-Bleed Opaque Field
- Must cover 100% of the canvas with zero transparency, zero white margins, and zero corner clipping.
- Selected from the 8 verified Anthropic background tokens or the page-native ivory/obsidian environments.
- Acts as the emotional and thematic backdrop.

### Layer 2: Irregular Ivory Carrier Shape (`#FAF9F5`)
The carrier shape is the signature bridge between the background color and the ink drawing. It serves four distinct functions across the 28 reference archetypes:
1. **Artifact Body**: The carrier is the physical object itself (e.g., the parchment sheet in `node-constitution`, the speech bubble in `object-chat`, the monitor screen in `object-desktop`, the glass chamber in `object-hourglass-cosmic`).
2. **Organic Halo / Bed**: A soft, rounded, slightly irregular paper cutout positioned behind a complex network or tool (e.g., behind the abacus in `hand-abacus`, behind the blocks in `hand-buildingbricks`, behind the constellation in `node-head-constellation`).
3. **Drafting Frame**: A rectangular or trapezoidal sheet representing a chart or tablet held by hands (e.g., `hand-nodegraph`, `hand-nodeline`).
4. **Light Spill**: The carrier takes the shape of projected light or an illuminated desk surface (e.g., `object-lamppaper`).

*Rule:* Black ink lines may occasionally cross or spill slightly beyond the ivory carrier boundary to ground the subject in physical space.

### Layer 3: Bold Near-Black Gestural Ink (`#141413`)
- Pure black or charcoal ink with soft warm undertone (`#141413` / `rgb(20, 20, 19)`).
- Line weight: Bold, deliberate, roughly 1.8% to 2.8% of the canvas dimension (e.g., 5px–8px on a 1000×1000 canvas).
- Line quality: Hand-drawn with subtle analog wobble, open joins, rounded terminals (`stroke-linecap: round`), and variable pen pressure. No CAD/vector perfection.

---

## 3. Verified Color Palette System

### Ink & Carrier Tokens
- **Linework Ink**: `#141413` (Deep Charcoal Black)
- **Carrier Silhouette**: `#FAF9F5` (Anthropic Warm Ivory / Bone)
- **Carrier Accent (when canvas is Ivory)**: `#F0EEE6` or `#E8E6DC` (Soft Sand Muted Carrier)

### Full-Bleed Accent Tokens (8 Verified Official Hues)
| Token | Hex | Mood / Thematic Domain | Typical Subject Association |
|---|---:|---|---|
| **cactus** | `#BCD1CA` | Institutional, thoughtful, safety, systems | Governance, model evaluation, safety frameworks |
| **heather** | `#CBCADB` | Research, global, reflective, technical | Foundation models, reasoning, interpretability |
| **oat** | `#E3DACC` | Human, calm, operational, partnership | Enterprise collaboration, developer tooling, docs |
| **clay** | `#D97757` | Energy, milestone, launch, urgency | Major model launches, breakthrough capability |
| **olive** | `#788C5D` | Growth, ecology, resilience, stability | Long-term stewardship, alignment durability |
| **sky** | `#6A9BCC` | Openness, infrastructure, connectivity | API platforms, open weights, global ecosystem |
| **fig** | `#C46686` | Creativity, identity, cultural nuance | Humanistic expression, creative writing, arts |
| **coral** | `#EBCECE` | Care, community, accessibility, warmth | User experience, accessibility, societal impact |

### High-Contrast Accessibility Pairings
- Linework (`#141413`) against Carrier (`#FAF9F5`): **16.86:1** (exceeds WCAG AAA).
- Primary Terracotta (`#A84729` accessible tone): **5.55:1** on Ivory.
- Never use more than ONE accent background family per illustration. Reject multi-color rainbow schemes.

---

## 4. The 28-Motif Visual Taxonomy

Anthropic's official visual library is organized into three distinct symbolic families:

### Family A: Hand Gestures (17 Archetypes)
Hands represent human agency, oversight, steering, craftsmanship, and ethical responsibility:
1. `hand-abacus`: Hands sliding beads on parallel calculation wires — *Symbolizes quantitative control, counting, and parameter adjustment.*
2. `hand-buildingbricks`: Hand lowering a block onto an established brick course — *Symbolizes modular scaffolding, foundations, and system construction.*
3. `hand-headcube`: Profile contour face holding a 3D wireframe cube — *Symbolizes spatial reasoning, mental models, and internal representations.*
4. `hand-headnodethink`: Profile face cradling an emergent node graph — *Symbolizes reflective thought, contemplation, and cognitive alignment.*
5. `hand-key`: Hands presenting an antique key upright — *Symbolizes authorization, credentials, safety unlocking, and privileged access.*
6. `hand-keyboard`: Stylized hands resting on or operating a keyboard — *Symbolizes programming, prompt input, and software creation.*
7. `hand-knobs`: Two hands adjusting rotary or slider knobs on a panel — *Symbolizes model steering, RLHF, and fine-tuning.*
8. `hand-knot`: Hands gently untangling an intertwined cord — *Symbolizes mechanistic interpretability, debugging, and unraveling complexity.*
9. `hand-megaphone`: Hand clutching an angled megaphone emitting projection rays — *Symbolizes broadcasting, user prompts, system announcements.*
10. `hand-nodegraph`: One hand supporting a coordinate frame while another steers the loss/activation curve — *Symbolizes model performance tracking and human oversight.*
11. `hand-nodeline`: Hands operating a pull-down chart scroll with a line curve — *Symbolizes executive reporting, benchmarking, and structured outcomes.*
12. `hand-nodepair`: Two hands extending toward each other across an ivory bridge — *Symbolizes human-AI collaboration, delegation, and partnership.*
13. `hand-nodeslide`: Fingers sliding a circular node along a horizontal boundary rail — *Symbolizes constraint enforcement, guardrails, and bounded steering.*
14. `hand-nodetree`: Hand nurturing a flourishing hierarchical tree with circular leaf nodes — *Symbolizes organic growth, decision trees, and constitutional reasoning.*
15. `hand-puzzle`: Hands slotting together interlocking jigsaw pieces — *Symbolizes multimodal synthesis, integration, and problem solving.*
16. `hand-reflection`: Hands meeting symmetrically across a diagonal waterline/plane — *Symbolizes self-reflection, reciprocal alignment, and RLHF feedback loops.*
17. `hand-shapebuild`: Hands arranging pure primitives (sphere, cone, cube) on a surface — *Symbolizes foundational architectures, priors, and inductive biases.*

### Family B: Computational & Node Networks (4 Archetypes)
Abstract structures representing latent spaces, constitutional frameworks, and decision paths:
18. `node-box`: An 8-spoke asterism / central hub connecting symmetrically to outer circular nodes — *Symbolizes central routing, cross-attention, and hub topology.*
19. `node-constitution`: Classical unrolling parchment scroll with a feather quill resting at the root node of an ascending decision tree — *Symbolizes Constitutional AI, core principles, and transparent ethics.*
20. `node-cursor`: Expressive hand-drawn pointer arrow hovering over or selecting a node cluster — *Symbolizes agentic execution, tool use, and interactive agency.*
21. `node-head-constellation`: Human head silhouette in contour outline with a constellation of linked nodes radiating within the cognitive aura — *Symbolizes latent knowledge, emergent understanding, and intelligence.*

### Family C: Objects, Interfaces & Instruments (7 Archetypes)
Physical instruments and digital metaphors stripped down to poetic line art:
22. `object-chat`: Classical dialogue balloon with an ivory fill and clean rounded tail — *Symbolizes natural language interfaces, conversational turn-taking, and chat.*
23. `object-codechatcode`: Stylized curly brackets `{ </ > }` framing software syntax — *Symbolizes programming capability, developer APIs, and software engineering.*
24. `object-codemagnifier`: Angled magnifying glass focusing closely on code or patterns — *Symbolizes code auditing, interpretability research, and security verification.*
25. `object-desktop`: Desktop computer monitor with hand-drawn stand and cursor — *Symbolizes computer use, GUI agents, and human desktop workflows.*
26. `object-hourglass-cosmic`: Classical glass sand-timer with particles swirling in both bulbs — *Symbolizes compute latency, training epochs, inference time, and patience.*
27. `object-lamppaper`: Articulated gooseneck desk lamp casting a focused beam upon a written sheet — *Symbolizes research, close reading, scholarship, and deep document analysis.*
28. `object-laptopsecure`: Portable computer with a prominent keyhole emblem on the display — *Symbolizes confidential compute, data privacy, and secure enterprise deployment.*

---

## 5. Anatomy & Drawing Grammar

### Hand Anatomy Rules
- **Finger Count**: 4 or 5 rounded, tubular fingers with gentle contour bends. No sharp fingernails, no realistic creases, no knuckle wrinkles.
- **Gestural Intent**: The hand must always be *doing* something meaningful: holding, sliding, supporting, nudging, pointing, untangling. Never passive decoration.
- **Wrist / Arm**: Enters from the edge of the frame or carrier, terminating cleanly in an open or rounded contour.

### Line Quality & Wobble
- Hand-drawn using a simulated dip-pen, broad nib, or reed pen.
- Deliberate subtle wobble (frequency of 3–5 waves per major line segment, amplitude ~1–2% of line length).
- Line terminals must be rounded (`stroke-linecap: round`), never squared off or pointed like technical drafting vectors.
- Joints between strokes should have subtle overshoots or imperfect kisses, evoking authentic human sketching.

### Node & Network Grammar
- Nodes are solid filled circles or concentric ring pips.
- Node radii should be hierarchically scaled (e.g., Root node $r=16$, Branch nodes $r=10$, Terminal nodes $r=6$).
- Connecting edges are simple unadorned line segments or smooth quadratic arches.
- No arrows on line ends unless illustrating unidirectional causality or time flow.

---

## 6. Compositional Architecture

### Sizing & Spatial Rhythm
- **Focal Cluster**: Must occupy **65% to 80%** of the frame height and width.
- **Breathing Margin**: Maintain at least **10% to 15%** clean, uncluttered accent field around the entire perimeter.
- **Centering**: Center the primary cluster for square/card compositions; offset slightly to the left/right only for 16:9 banner heroes where headline copy will reside.

### The Single-Metaphor Rule
- Strict adherence to **one central metaphor**. An illustration must never combine a robot, a telescope, a plant, and a rocket simultaneously.
- If the subject is "Code Security", use the single metaphor of `hand-key` or `object-laptopsecure`.
- If the subject is "Constitutional Alignment", use the single metaphor of `node-constitution`.
- If the subject is "Fine-Tuning", use the single metaphor of `hand-knobs` or `hand-nodeslide`.

---

## 7. Generation Quality Gate & Failure Mode Matrix

| Failure Mode | Visual Symptom | Root Cause | Exact Remedy |
|---|---|---|---|
| **Stock Vector Slop** | Razor-sharp bezier curves, perfect circles, corporate tech look | AI defaulting to standard SVG vector clip-art | Enforce `naive analog dip-pen gesture`, `uneven hand wobble`, `rounded stroke terminals`, `deliberate asymmetry`. |
| **Missing Carrier Shape** | Linework sits directly on colored background with no ivory fill | Prompt omitted Layer 2 carrier specification | Add explicit `irregular ivory #FAF9F5 carrier shape behind focal subject covering 60–75% of subject area`. |
| **Transparent / White Canvas** | Outer background is transparent, white, or checkered | Tool defaulted to isolated icon output | Demand `full-bleed opaque [palette token] background covering every corner from edge to edge`. |
| **3D / Photographic Creep** | Shading, gradients, bevels, depth shadows | Model interpreted "illustration" as 3D render | Specify `strictly flat two-dimensional art, zero gradients, zero shadows, zero specular lighting`. |
| **Visual Soup** | Cluttered scene with multiple competing objects | Prompt was too literal or descriptive | Reduce to `one primary metaphor with at most two interacting elements (e.g. one hand + one chart)`. |
| **Overly Detailed Anatomy** | Realistic knuckles, veins, fingernails | Standard human anatomy rendering | Enforce `simplified cartoon-like naive anatomy: tubular rounded fingers, minimal contour strokes`. |
