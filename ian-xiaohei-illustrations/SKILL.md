---
name: ian-xiaohei-illustrations
description: Generate Ian-style inline article illustrations with handwritten Chinese-friendly annotations. Use when the user asks to design or generate "quirky", "Xiaohei", "hand-drawn", "inline illustration", "article imagery", "illustration plan", or "shot list" assets for articles, posts, blogs, Notion docs, workflow docs, methodologies, processes, structures, states, metaphors, or viewpoints; also for tasks like "remove title / edit image". Defaults to the Xiaohei IP, pure-white hand-drawn line art, a few red/orange/blue annotations, and a clean, quirky, free-spirited visual style.
---

# Ian Xiaohei Quirky Inline Illustrations

## Core positioning

Design and generate 16:9 landscape inline illustrations for articles. The goal is not commercial illustration, PPT infographics, or cutesy cartoons, but turning the key judgments, workflows, structures, states, or metaphors in an article into crisp, quirky, creative, readable — yet non-instructional — hand-drawn explanatory images.

The default visual IP is "Xiaohei": solid black, white dot eyes, thin legs, blank expression, seriously doing something absurd but plausible. Xiaohei must participate in the core action of the scene — it cannot just stand off to the side as decoration.

## Read these references first

Load them as needed by the task; don't stuff everything into context at once:

- `references/style-dna.md`: style DNA, colors, text rules, taboos.
- `references/xiaohei-ip.md`: Xiaohei's appearance, personality, action library, and taboos.
- `references/composition-patterns.md`: structure types, original-metaphor method, and anti-copy rules.
- `references/prompt-template.md`: single-image generation prompt template.
- `references/qa-checklist.md`: post-generation checks and iteration rules.
- `assets/examples/`: low-frequency visual calibration only — never part of the default generation path. Do not copy these examples' compositions, objects, or labels.

## Workflow

### 1. Digest the article

First read the article, link, Notion page, Markdown file, or screenshot content provided by the user. Extract:

- What the core arguments are
- Which paragraphs carry cognitive turning points
- Which content is well suited to visual explanation
- Which parts work better as text alone and need no image

Don't illustrate evenly. Prioritize "cognitive anchors", e.g.: core judgments, two breakpoints, input-output loops, triage, before/after contrast, one-fish-many-uses, handoff paths, common pitfalls, character state changes.

### 2. Output the illustration strategy first

If the user only says "analyze how to illustrate / think about where images are needed", provide a shot list first. For each image, specify:

- Which paragraph it follows
- The topic of the image
- The core meaning
- The structure type
- What Xiaohei is doing in the image
- Suggested elements
- Suggested annotation labels

Default to 4-8 images. For short articles, 1-3; even for long articles, rarely exceed 9. Enough is enough — avoid turning the article into a picture book.

### 3. Generate one image at a time

If the user explicitly asks to "generate / output / make images / help me generate", don't stop to wait for confirmation; use the built-in `image_gen` to generate each image separately. Never combine multiple images into one.

Each image explains only one core structure. The prompt must include:

- 16:9 landscape inline article illustration
- Pure white background
- Black hand-drawn line art
- A few red/orange/blue handwritten annotations
- Lots of whitespace
- Xiaohei as the core action subject
- Forbidden: PPT look, commercial illustration, childish/cutesy, complex architecture diagrams, type-title labels in the top-left corner

Do not replicate past cases. The examples only calibrate style density and how Xiaohei participates — do not directly reuse existing compositions such as "conveyor belt with two breakpoints / Xiaohei pulling cables / the material fish / the stamping toolbox / the common-pitfall path" unless the user explicitly asks to recreate a specific image. Each time, invent a fresh, strange-but-plausible metaphor from the current article.

### 4. Check and iterate

After generating, check against `references/qa-checklist.md`. If any of these problems appear, prefer regenerating or making local edits:

- Xiaohei is only decoration
- The scene is too crowded
- It looks too much like a flowchart/PPT
- Too much text or serious typos
- A title like "Common Pitfalls / Flowchart / System Architecture" appears in the top-left corner
- The art style is too cutesy, childish, or rigid
- The background isn't a clean white

### 5. Save and deliver

If the user works inside the workspace, copy the final images to:

```text
assets/<article-slug>-illustrations/
```

Name them in order:

```text
01-topic-name.png
02-topic-name.png
```

Keep the original generated files; don't overwrite existing assets unless the user explicitly asks for replacement.

## Delivery voice

Pre-generation strategy output should be short and precise. Post-generation delivery should include:

- How many images were generated
- The purpose of each image
- Save paths
- Which images are most solid and which are optional

Don't write long essays about style theory; let the images speak for themselves.
