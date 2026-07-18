---
name: frontend-design
description: >
  Create distinctive, production-grade frontend interfaces with strong product
  interaction design. Use when the user asks to build or refine web components,
  pages, applications, toolbars, settings, navigation, or responsive UI. Also
  trigger when the user mentions UI consistency, icon versus button choices,
  interaction hierarchy, accessibility, or that a feature works but does not
  feel professionally designed.
license: Complete terms in LICENSE.txt
compatibility: Works with existing design systems and new HTML/CSS/React/Vue interfaces.
metadata:
  author: lovstudio
  version: "0.2.0"
  tags: frontend product-design interaction-design accessibility
---

This skill guides creation of distinctive, production-grade frontend interfaces that avoid generic "AI slop" aesthetics. Implement real working code with exceptional attention to aesthetic details and creative choices.

The user provides frontend requirements: a component, page, application, or interface to build. They may include context about the purpose, audience, or technical constraints.

## Product Semantics Before Aesthetics

For an existing product, the current design system and interaction grammar take
priority over novelty. Search for adjacent surfaces and shared primitives before
creating new controls. A visually striking implementation is still a failure if
peer actions use inconsistent control types, states are presented as actions, or
responsive behavior changes the meaning of a control.

Before coding, classify every control by user intent:

| Intent | Default control | Required behavior |
| --- | --- | --- |
| Status or environment | Badge or text | Non-interactive unless it truly opens details |
| Peer actions in a compact toolbar | Uniform icon buttons | Same hit target and visual grammar; Tooltip and accessible name required |
| Low-frequency or ambiguous settings action | Labeled button | Copy states the user goal; icon is supporting information |
| Primary page action | Labeled primary button | Usually one highest-emphasis action per surface |
| Toggle, pin, or selected state | Toggle or `aria-pressed` button | Current state remains visible without relying on a toast |
| Destructive action | Destructive button, or delayed destructive color in a toolbar | Confirmation where data loss is possible |

Rules for action groups:

- Do not mix labeled buttons and icon-only buttons for peer actions just because
  space happens to be available. Either keep the group compact and icon-based,
  or keep the group explicit and labeled.
- Responsive changes apply to the whole group. Never let one peer action switch
  from text to icon independently and leave a mixed control grammar behind.
- Separate status, navigation, ordinary actions, toggles, and destructive actions
  through grouping and state—not arbitrary button variants.
- Reuse a shared toolbar/button primitive when one exists. If the same tooltip,
  sizing, and accessibility wiring appears twice, extract the contract.
- Icon meaning must match the user's mental model. If the icon is not obvious in
  context, use a label instead of hoping the tooltip repairs the design.

Before declaring a UI complete, verify normal, hover, focus, pressed, loading,
disabled, and destructive states; keyboard traversal; localized labels; and the
narrowest supported container. Treat visible affordance and wording as acceptance
criteria, not optional polish.

## Design Thinking

Before coding, understand the context and commit to a BOLD aesthetic direction:
- **Purpose**: What problem does this interface solve? Who uses it?
- **Tone**: Pick an extreme: brutally minimal, maximalist chaos, retro-futuristic, organic/natural, luxury/refined, playful/toy-like, editorial/magazine, brutalist/raw, art deco/geometric, soft/pastel, industrial/utilitarian, etc. There are so many flavors to choose from. Use these for inspiration but design one that is true to the aesthetic direction.
- **Constraints**: Technical requirements (framework, performance, accessibility).
- **Differentiation**: What makes this UNFORGETTABLE? What's the one thing someone will remember?

**CRITICAL**: Choose a clear conceptual direction and execute it with precision. Bold maximalism and refined minimalism both work—the key is intentionality, not intensity. In an established product, express that direction through the existing tokens and primitives rather than replacing its visual language.

Then implement working code (HTML/CSS/JS, React, Vue, etc.) that is:
- Production-grade and functional
- Visually striking and memorable
- Cohesive with a clear aesthetic point-of-view
- Meticulously refined in every detail

## Frontend Aesthetics Guidelines

Focus on:
- **Typography**: Choose fonts that are beautiful, unique, and interesting. Avoid generic fonts like Arial and Inter; opt instead for distinctive choices that elevate the frontend's aesthetics; unexpected, characterful font choices. Pair a distinctive display font with a refined body font.
- **Color & Theme**: Commit to a cohesive aesthetic. Use CSS variables for consistency. Dominant colors with sharp accents outperform timid, evenly-distributed palettes.
- **Motion**: Use animations for effects and micro-interactions. Prioritize CSS-only solutions for HTML. Use Motion library for React when available. Focus on high-impact moments: one well-orchestrated page load with staggered reveals (animation-delay) creates more delight than scattered micro-interactions. Use scroll-triggering and hover states that surprise.
- **Spatial Composition**: Unexpected layouts. Asymmetry. Overlap. Diagonal flow. Grid-breaking elements. Generous negative space OR controlled density.
- **Backgrounds & Visual Details**: Create atmosphere and depth rather than defaulting to solid colors. Add contextual effects and textures that match the overall aesthetic. Apply creative forms like gradient meshes, noise textures, geometric patterns, layered transparencies, dramatic shadows, decorative borders, custom cursors, and grain overlays.

NEVER use generic AI-generated aesthetics like overused font families (Inter, Roboto, Arial, system fonts), cliched color schemes (particularly purple gradients on white backgrounds), predictable layouts and component patterns, and cookie-cutter design that lacks context-specific character.

Interpret creatively and make unexpected choices that feel genuinely designed for the context. No design should be the same. Vary between light and dark themes, different fonts, different aesthetics. NEVER converge on common choices (Space Grotesk, for example) across generations.

**IMPORTANT**: Match implementation complexity to the aesthetic vision. Maximalist designs need elaborate code with extensive animations and effects. Minimalist or refined designs need restraint, precision, and careful attention to spacing, typography, and subtle details. Elegance comes from executing the vision well.

Remember: Claude is capable of extraordinary creative work. Don't hold back, show what can truly be created when thinking outside the box and committing fully to a distinctive vision.
