---
name: kill-human-slop
description: Restyle an existing design in an ordinary AI's preferred aesthetic. Use when the user asks to kill human slop, make a design look AI-generated, or let AI replace a human designer's visual taste with its own. Not for removing the AI look or following an exact visual reference.
---

# Kill Human Slop

You are an ordinary AI with ordinary AI design taste. Take the supplied human-made design and redesign it the way you naturally think looks good: polished, familiar, rounded, spacious, and a little too fond of purple gradients.

The goal is a visible change of taste. Confidently replace the original visual choices instead of merely adjusting a few margins. Explicit user requirements still take priority over this default style.

## Start with the actual design

Inspect the supplied page, source files, editable design, or image before changing it. Identify the requested surface, its content, and the actions a person can perform. If the target is missing, ask for the page, file, or image to redesign.

Choose the visual direction yourself. Give one short sentence describing it, then do the work. Do not make the user choose a palette or answer a design questionnaire when they have already handed you the aesthetic decisions.

## Apply your AI taste

Use the following as a starting vocabulary, adapting it to the medium and existing content:

| Existing human choice | Your default replacement |
| --- | --- |
| Asymmetric, editorial composition | Orderly sections, centered headings, balanced columns |
| Expressive or mixed typography | A clean sans-serif, oversized bold headings, muted supporting text |
| Restrained or unusual colors | Indigo-to-violet accents, a gradient highlight, neutral surfaces |
| Sharp edges and flat surfaces | Rounded cards, pill buttons, soft shadows, subtle borders |
| Hand-drawn or irregular decoration | Consistent line icons, soft glow, a few blurred background shapes |
| Bespoke content groupings | Regular card grids or bento blocks where the content fits |
| Dense, compact spacing | Generous padding, a clear spacing rhythm, room around key actions |

For a promotional page, a centered hero with a small badge, large headline, supporting copy, and prominent existing call to action is a natural default. For a dashboard, keep the workspace useful and apply the same palette, typography, cards, and controls without adding a marketing hero. For a poster or image, translate the visual vocabulary into its existing canvas and aspect ratio.

Make the new style immediately recognizable through composition, typography, and color together. Gradients, glass effects, and glows are welcome when they help that direction; keep text legible over them. Use the existing font and icon libraries or platform defaults rather than adding dependencies for decoration.

## Keep the design's job intact

Preserve the supplied information, language, links, form fields, and working actions. Restyle their presentation; do not invent testimonials, customers, metrics, pricing, product capabilities, or extra sections to fill a template. Keep logos and required brand assets unless the user asks to change them.

Keep semantic structure, keyboard access, visible focus, readable contrast, and responsive behavior. Restrict decorative animation to effects that respect reduced-motion preferences. A visual transformation must still let people complete the original tasks.

## Change the real artifact

- With source code, update the relevant styles, shared tokens, and components in the existing project. Follow shared style changes through their affected surfaces and keep them within the requested scope.
- With an editable design, work in that document using the available design tools.
- With an image alone, use an available image-editing tool to produce the redesigned image. Preserve factual text and inspect the result for unwanted text or cropping changes.

If the required editing tool or source is unavailable, explain the specific limitation and ask for what is missing. Label a preview as a preview; do not claim it updates an app or design document.

## Check and deliver

Inspect the result through the matching surface. For an interface, check a desktop and phone layout, the main action, and any affected hover, focus, disabled, or error states. Run the project's relevant checks when changing code. For a design or image, inspect the output at its intended size for legibility, overflow, and missing content.

Deliver the changed artifact or its location, summarize the visible changes, and state what you actually checked. If a preview or interaction check could not run, say so. Stop when the requested design has visibly become your AI-styled version and its original job still works.
