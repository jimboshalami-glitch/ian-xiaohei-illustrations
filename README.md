# Ian Xiaohei Illustrations

> Turn the judgments, flows, states, and metaphors in your articles into clean, white-background, hand-drawn, delightfully weird inline illustrations.
>
> 16:9 landscape | Xiaohei IP | pure-white hand drawing | a few red/orange/blue handwritten annotations | Codex Skill

---

## What is this repository?

Ian Xiaohei Illustrations is a Codex Skill that guides AI agents to generate inline illustrations for articles, posts, blog entries, Notion docs, and methodology content.

It is not a generic illustration prompt, nor a PPT infographic template. Its core goal: first understand the cognitive anchors in an article, then turn one of its judgments, workflows, structures, states, or metaphors into a memorable 16:9 hand-drawn explanatory illustration.

The default visual IP is "Xiaohei": a small solid-black character with white dot eyes, thin legs, and a blank expression. Xiaohei is not a mascot, not a sticker, and not decoration standing in a corner — it is an absurd worker seriously participating in the operation of the system.

In one sentence: **make the AI do more than "add an image" — draw out one key cognitive move from the article.**

---

## Who is it for

Great fit for:

- People who write articles and need inline illustrations and article imagery
- People making knowledge content, methodology content, or AI workflow content
- People who want to turn abstract judgments into concrete metaphors
- People who want an illustration style lighter, weirder, and more personally recognizable than PPT infographics
- People producing content with Codex who want to reliably reuse one visual language

Not a fit for:

- People who want commercial illustration, brand key visuals, or polished flat illustration
- People who want traditional PPT infographics, complex architecture diagrams, or flowcharts
- People who want children's cartoons, cute IPs, or emoji-sticker styles
- People who want to cram large amounts of body text, long explanations, or entire course pages into one image
- People who need strictly editable vector source files

---

## What it produces

Default output:

- 16:9 landscape inline illustrations
- A 4-8 image shot list per article
- For each image: topic, core meaning, structure type, Xiaohei's action, and suggested annotation labels
- Final PNG images saved to `assets/<article-slug>-illustrations/` in the workspace

Not produced by default:

- PPTX / PDF / Keynote
- SVG / HTML / Canvas editable graphics
- Commercial posters or cover key visuals
- Text-heavy infographics

---

## Visual style

This skill uses Ian's "Xiaohei quirky inline illustration" style by default:

- Pure white background — no paper texture, beige, shadows, or gradients
- Black hand-drawn line art: thin lines with a slight wobble
- Lots of whitespace; the subject takes up only about 40%-60% of the canvas
- A few red, orange, and blue handwritten annotations
- One image expresses only one core action, structure, state, or metaphor
- Xiaohei must carry the core action — it can't be mere decoration
- Weird, creative, and fresh — but never childish or cutesy

---

## Example results

### Two Breakpoints

![Two Breakpoints](examples/images/01-two-breakpoints.png)

### Sort by Purpose

![Sort by Purpose](examples/images/02-sort-by-purpose.png)

### One Fish, Many Uses

![One Fish, Many Uses](examples/images/03-one-fish-many-uses.png)

### Handoff Path

![Handoff Path](examples/images/04-handoff-path.png)

### Information Well

![Information Well](examples/images/05-information-well.png)

### Idea Press

![Idea Press](examples/images/06-idea-press.png)

### Content Fermentation

![Content Fermentation](examples/images/07-content-fermentation.png)

### Trust Bridge

![Trust Bridge](examples/images/08-trust-bridge.png)

These images are style-calibration references, not composition templates. When using the skill, invent fresh metaphors from the current article — don't copy the objects or compositions from these old examples.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/helloianneo/ian-xiaohei-illustrations.git
cd ian-xiaohei-illustrations
```

Copy the skill into the Codex skills directory:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./ian-xiaohei-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

After installation, use it in Codex:

```text
Use $ian-xiaohei-illustrations to design and generate 5 Xiaohei quirky inline illustrations for this article.
```

---

## How to use

### Illustration planning only

```text
Use $ian-xiaohei-illustrations — don't generate images yet.
Analyze where the article below deserves illustrations and output a shot list of about 5 images.
For each image, specify: which paragraph it follows, topic, core meaning, structure type, what Xiaohei is doing, and suggested annotation labels.

<paste article>
```

### Generate inline illustrations directly

```text
Use $ian-xiaohei-illustrations to generate 4 Xiaohei quirky inline illustrations for the article below.
Requirements: 16:9 landscape, pure white background, black hand-drawn line art, a few red/orange/blue handwritten annotations.

<paste article>
```

### One image for a single concept

```text
Use $ian-xiaohei-illustrations to create one inline illustration for: "Trust isn't shouted into existence — it's paved, one piece of evidence at a time."
The scene should be weird but clean, and Xiaohei must carry the core action.
```

### Remove a title or fix wrong text in an image

```text
Use $ian-xiaohei-illustrations to edit this image: remove the "flowchart" title in the top-left corner and keep everything else unchanged.
```

More examples in [examples/prompts.md](examples/prompts.md).

---

## Workflow

The skill's workflow:

1. Read the article, Markdown, Notion content, screenshots, or the topic provided by the user
2. Extract the core arguments, cognitive turning points, process structures, and paragraphs suited to visualization
3. Output the shot list first: each image picks only one cognitive anchor
4. Choose a structure type per image: Workflow, system subsystem, before/after contrast, character states, conceptual metaphor, method layering, map route, or mini-comic panels
5. Invent a fresh low-tech, quirky-but-plausible physical metaphor
6. Make Xiaohei carry the core action
7. Generate each image separately with the image model
8. Check against the QA checklist: white background, whitespace, Xiaohei's action, annotations, no PPT feel, no rehashing of old examples
9. Save the final PNGs and report their purpose and paths

---

## Directory structure

```text
.
├── README.md
├── LICENSE
├── NOTICE.md
├── assets/
│   └── ian-wechat-qr.jpg
├── examples/
│   ├── images/
│   │   ├── 01-two-breakpoints.png
│   │   ├── 02-sort-by-purpose.png
│   │   └── ...
│   └── prompts.md
└── ian-xiaohei-illustrations/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    ├── assets/
    │   └── examples/
    └── references/
        ├── style-dna.md
        ├── xiaohei-ip.md
        ├── composition-patterns.md
        ├── prompt-template.md
        └── qa-checklist.md
```

What actually needs to be installed into Codex is the subdirectory:

```text
ian-xiaohei-illustrations/
```

The root-level README, LICENSE, NOTICE, and examples are GitHub sharing docs.

---

## Notes

- The shorter the text inside an image, the more stable the results.
- Each image explains only one core structure — don't turn the article into an instruction manual.
- Xiaohei must carry the core action; if the image still fully works without Xiaohei, then Xiaohei is too decorative.
- The example images are only for calibrating line density, whitespace, color restraint, and how Xiaohei participates — do not replicate their compositions.
- AI image models may produce typos, hallucinated labels, style drift, or extra titles; check the output after generation.
- If there are many text errors, reduce the number of annotation labels and regenerate.

---

## Related projects

- [Ian Handdrawn PPT](https://github.com/helloianneo/ian-handdrawn-ppt) — a skill for generating hand-drawn tech PPT-style page images
- [Awesome Claude Code Skills](https://github.com/helloianneo/awesome-claude-code-skills) — a curated collection of Claude Code Skills / Agents / Plugins
- [Obsidian + Claude AI Second Brain](https://github.com/helloianneo/obsidian-ai-second-brain) — a guide to building a personal knowledge base with Obsidian + Claude AI

---

## About the author

**Ian** — Product designer / solopreneur practitioner / AI builder

Building a one-person company with AI teams.

- GitHub: [helloianneo](https://github.com/helloianneo)
- X/Twitter: [@ianneo_ai](https://x.com/ianneo_ai)
- Website: [www.ianneo.xyz](https://www.ianneo.xyz)
- WeChat: `ianneoxyz`
- Email: hello.neoc@gmail.com

---

## Keep exploring

This Xiaohei illustration skill is just one small tool in the personal production system I've built with AI.

If you're also using AI for content, knowledge bases, workflows, or productization, visit my website: [www.ianneo.xyz](https://www.ianneo.xyz).

If you'd rather observe first, follow me on [X/Twitter](https://x.com/ianneo_ai).

To learn about Indie Builders Club, add me on WeChat: `ianneoxyz` with the note "OPC".

<p>
  <img src="assets/ian-wechat-qr.jpg" alt="Ian WeChat QR code" width="120">
</p>

If scanning the QR code isn't convenient, search WeChat for: `ianneoxyz`.

---

## License

MIT License. See [LICENSE](LICENSE).
