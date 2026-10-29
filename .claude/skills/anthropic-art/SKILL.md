---
name: anthropic-art
description: "Directly generate full-background editorial SVG illustrations in Anthropic's signature hand-drawn visual language: warm or muted opaque color fields, irregular ivory carrier shapes, and bold black gestural linework. Emits complete, production-ready SVG files (static or animated) adhering to the 3-layer Anthropic visual grammar across 28 official motifs (hands, nodes, objects), with optional headless browser PNG rendering."
---

# Anthropic Art: Hand-Drawn Editorial SVG System

Directly generate hand-crafted, production-ready SVG illustrations in the authentic Anthropic visual language. The system unites warm, naive, imperfect analog dip-pen linework with structured computational geometry (node graphs, trees, coordinate spaces, and carrier silhouettes).

Instead of relying on external image generation tools, **directly author the complete SVG code and save it as an `.svg` file** (and optionally render to `.png` via headless browser when requested).

---

## Self-Contained Specification (Zero Image Reads Required)

All required visual rules, 28-motif geometries, SVG templates, and verified color palettes are **fully self-contained in this file and [references/style-spec.md](references/style-spec.md)**.

**DO NOT read or load image files into context.** The image files in `images/` or `assets/` are for offline human inspection only. Never attempt to read binary image files during generation—rely entirely on the explicit SVG grammar, coordinates, and rules below to keep generation instant, token-efficient, and error-free.

---

## The 3-Layer SVG Architecture

Every valid Anthropic SVG must be constructed from exactly three spatial layers:

```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000" width="1200" height="1200">
  <defs>
    <!-- Analog Dip-Pen Wobble Filter -->
    <filter id="wobble" x="-10%" y="-10%" width="120%" height="120%">
      <feTurbulence type="fractalNoise" baseFrequency="0.016" numOctaves="2" seed="7" result="noise"/>
      <feDisplacementMap in="SourceGraphic" in2="noise" scale="5" xChannelSelector="R" yChannelSelector="G"/>
    </filter>
  </defs>

  <!-- LAYER 1: Full-Bleed Opaque Field (100% canvas, no transparency, no white border) -->
  <rect width="100%" height="100%" fill="#CBCADB"/>

  <!-- LAYER 2: Irregular Ivory Carrier Shape (#FAF9F5) -->
  <path d="M 260 280 Q 500 220 740 290 Q 790 530 720 740 Q 480 810 260 740 Q 200 510 260 280 Z" fill="#FAF9F5"/>

  <!-- LAYER 3: Bold Near-Black Linework (#141413) & Nodes -->
  <g stroke="#141413" stroke-width="12" stroke-linecap="round" stroke-linejoin="round" fill="none" filter="url(#wobble)">
    <!-- Naive gestural contours with rounded ends and organic joins -->
  </g>
  <!-- Nodes & concentric rings (keep outside or subtle filter so circles stay crisp) -->
  <circle cx="500" cy="500" r="18" fill="#141413"/>
</svg>
```

1. **Layer 1 (Background `<rect>`)**: Full-bleed 100% canvas coverage from corner to corner. Zero transparency. Zero white borders.
2. **Layer 2 (Carrier `<path>`)**: An irregular, soft ivory `#FAF9F5` silhouette occupying 55%–80% of the subject area. Represents the physical object body (scroll, screen, bubble) or a soft organic paper halo bed behind the subject.
3. **Layer 3 (Linework & Nodes)**: Bold `#141413` charcoal ink with rounded terminals (`stroke-linecap="round"`), natural analog wobble filter (`#wobble`), and solid circular node accents. Lines may sparingly spill across the ivory boundary.

---

## Structural Transfer Grammar (Zero-Hallucination Guardrails)

Do not copy literal objects from reference files. Instead, transfer the **underlying stroke behavior, density, and spatial logic** using these strict rules:

### 1. The Hand Law (Anti-Sausage Rule)
- **NEVER** draw realistic multi-jointed fingers, knuckles, wrinkles, or stacked horizontal "sausages".
- If a hand is needed, use only one of two primitive Anthropic patterns:
  - **Pattern A (The Open Cradle / Supporting Hand)**: One continuous outer U-curve for wrist and thumb, with 3 or 4 simple, parallel rounded finger arches (`Q ... Q ...`). Zero interior crease lines.
  - **Pattern B (The Delicate Pinch / Guiding Hand)**: Thumb and index meet in a smooth, continuous teardrop loop; the remaining 3 fingers sweep back in graceful parallel arches.
- *Default Rule:* If an object can stand on its own (e.g. the quill on parchment, a desk lamp, an hourglass, computer monitor), **omit hands entirely**. Standalone symbolic objects are cleaner and more iconic.

### 2. The Text & Writing Law (Anti-Node Rule for Documents)
- When illustrating writing, research, documentation, or code: **NEVER draw branching node trees**.
- Text on paper must be drawn as flowing, calligraphic undulating cursive waves (`u`, `m`, and wavy manuscript lines), as in `object-lamppaper`.
- Code must be drawn as clean curly brackets `{ </ > }` with indented horizontal script strokes.

### 3. The Density & Network Law (Anti-Spiderweb Rule)
- Strictly **one central metaphor** per illustration.
- If drawing a network, tree, or graph: **maximum 4 to 7 nodes total**. Never draw dense spiderwebs, fractal micro-branches, or dotted radiating rays.
- Maintain at least 15% clean, uncluttered breathing room around the outer edges.

### 4. The Analog Wobble Law
- Linework stroke width: 10px to 14px on a 1000×1000 canvas.
- Always use `stroke-linecap="round"` and `stroke-linejoin="round"`.
- Use the `<feDisplacementMap scale="4" to "6">` filter for organic dip-pen tremor. Do not apply heavy displacement to circular nodes so dots stay clean.

---

## Metaphor Mapping Matrix: Topic to Archetype

Distill the user's topic into **one single metaphor** from the 28 verified reference archetypes:

| Topic / Domain | Primary Metaphor | Motif Reference | Carrier Role |
|---|---|---|---|
| **Constitutional AI & Safety** | Curled parchment scroll with quill grounded at decision tree root | `node-constitution` | Artifact body (the scroll itself) |
| **Model Steering & Tuning** | Hands adjusting horizontal sliders or rotary knobs | `hand-knobs` / `hand-nodeslide` | Halo bed behind the controls |
| **Interpretability & Circuits** | Hands untangling an intertwined loose cord or knot | `hand-knot` | Soft circular halo behind knot |
| **Evaluation & Loss Curves** | Hands framing an L-axis chart with steered nodes | `hand-nodegraph` | Chart paper surface inside axis |
| **Deep Reasoning & Cognition** | Head profile contour holding a node constellation | `hand-headnodethink` | Thought aura cloud |
| **Tool Use & Autonomous Agents** | Hand-drawn mouse cursor activating a node cluster | `node-cursor` / `object-desktop` | Display screen or target patch |
| **Cybersecurity & Guardrails** | Hands holding an upright antique key or secure laptop | `hand-key` / `object-laptopsecure` | Key silhouette or laptop screen |
| **Coding & Developer APIs** | Stylized curly brackets `{ </ > }` or hands on keyboard | `object-codechatcode` / `hand-keyboard` | Soft rectangular paper bed |
| **Multimodal Synthesis** | Hands slotting interlocking puzzle pieces together | `hand-puzzle` | Cutout of the puzzle pieces |
| **Human-AI Collaboration** | Two hands reaching toward each other across an ivory bridge | `hand-nodepair` / `hand-reflection` | Connecting bridge shape |
| **Foundations & Architecture** | Hand placing a block on a structured brick course | `hand-buildingbricks` | Silhouette behind the brick wall |
| **Compute Scaling & Latency** | Classical hourglass with particles swirling in both bulbs | `object-hourglass-cosmic` | Glass bulb bodies |
| **Document Analysis & Search** | Gooseneck desk lamp shining a beam onto written paper | `object-lamppaper` | Paper document and light cone |
| **Auditing & Code Review** | Hand-held magnifying glass inspecting code patterns | `object-codemagnifier` | Lens field and illuminated subject |
| **Dialogue & Conversation** | Rounded conversational speech balloon with tail | `object-chat` | Interior fill of the speech bubble |
| **System Architecture & Hubs** | 8-spoke asterism / central hub connecting to outer nodes | `node-box` | Central square/circle hub bed |

---

## Verified Background Palette Tokens

Select exactly one background color:

```text
cactus   #BCD1CA  (Safety, systems, governance, institutional frameworks)
heather  #CBCADB  (Research, technical depth, reflective inquiry, foundational models)
oat      #E3DACC  (Humanistic, operational partnership, developer documentation)
clay     #D97757  (Energy, milestone launch, urgency, major capability leap)
olive    #788C5D  (Growth, durability, ecological stewardship, resilience)
sky      #6A9BCC  (Openness, global ecosystem, connectivity, developer platforms)
fig      #C46686  (Creativity, cultural nuance, human expression, writing)
coral    #EBCECE  (Care, community, accessibility, warmth, societal impact)
```

*Page-Native Neutral:* Outer canvas `#FAF9F5`, carrier shape `#F0EEE6` or `#E8E6DC`.

---

## Direct SVG Generation Workflow

1. **Select One Metaphor**: Map the topic to one archetype from the 28-motif matrix.
2. **Assign Palette Token**: Choose the background color matching the topic's mood.
3. **Draft and Write the SVG**:
   - Write the `.svg` directly to the project directory using your file-writing tool.
   - Use `<filter id="wobble">` with `scale="5"` to `"7"` for authentic pen tremor.
   - Use organic quadratic (`Q`) and cubic (`C`) bezier paths for the carrier and ink lines.
   - Ensure nodes are solid `#141413` circles with clean radii (e.g. `r="14"`, `r="20"`).
4. **When Asked to "Make it Animated"**:
   - Add inline SVG `<style>` with CSS `@keyframes`:
     - Swaying cord or floating hand (`transform: translateY(...) rotate(...)`).
     - Gliding cursor with a click ripple (`stroke-dashoffset`, `transform`, `opacity`).
     - Animated boiling line effect (cycling `seed` in `feTurbulence` or pulsing node radii).
5. **Convert to PNG (Optional / Cross-Platform)**:
   If the user requests a PNG or wants to inspect the visual render, run a headless browser screenshot:
   - **Windows** (Chrome/Edge/Scoop):
     `chrome.exe --headless --disable-gpu --screenshot="out.png" --window-size=1200,1200 "in.svg"`
   - **macOS**:
     `"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless --disable-gpu --screenshot="out.png" --window-size=1200,1200 "in.svg"`
   - **Linux / WSL**:
     `google-chrome --headless --disable-gpu --screenshot="out.png" --window-size=1200,1200 "in.svg"`

---

## SVG Quality Gate

Before finishing, verify:
- [ ] **100% Opaque Corners**: `<rect width="100%" height="100%" fill="[palette]"/>` covers the entire background.
- [ ] **3-Layer Separation**: Background field $\rightarrow$ Irregular ivory carrier (`#FAF9F5`) $\rightarrow$ Bold ink strokes (`#141413`).
- [ ] **Single Clean Metaphor**: One focused concept without competing objects.
- [ ] **Analog Line Character**: Rounded caps (`stroke-linecap="round"`), rounded joins (`stroke-linejoin="round"`), and analog tremor filter.
- [ ] **Crisp Nodes**: Circular nodes remain distinct and legible at thumbnail size.
