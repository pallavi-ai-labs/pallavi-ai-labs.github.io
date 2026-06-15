# Hero Image Prompt for ChatGPT

Use this prompt in ChatGPT image generation (DALL-E or GPT-4o) to create the hero visual for pallavi-ai-labs.github.io.

---

## Context to give ChatGPT first (paste this before the prompt)

The website is a personal brand site for Pallavi Sharma, an AI Product Leader who designed chips at Intel, built cloud infrastructure at AWS, and now ships agentic AI at enterprise scale. The site has a dark editorial aesthetic: near-black navy background (#080c14), warm amber/gold accent color (#f59e0b), clean Inter typography. The hero image sits on the RIGHT side of the split-layout hero section on desktop. It should feel like it belongs on a serious editorial tech publication, not a startup landing page or a LinkedIn post. The person is not in the image — this is an abstract/conceptual visual.

---

## The Prompt

**Create a wide-format abstract editorial illustration (1200×800px, 3:2 ratio) for a dark-themed personal brand website.**

The concept: a single continuous arc — three points connected by a flowing line — representing a career trajectory from silicon chip design through cloud infrastructure to AI agents. The visual language is architectural and precise, not decorative.

**Compositional requirements:**
- The image sits on a near-black navy background (#080c14). The illustration must blend into this background at the edges — no white borders, no bright backgrounds, no drop shadows that presuppose a light page.
- Three visual anchors along the arc: a silicon wafer cross-section or circuit trace at the start (left), a clean server/cloud rack form in the middle, and an abstract node graph or neural mesh at the end (right). These should feel like engineering diagrams, not stock icons.
- A single flowing amber/gold line (#f59e0b) connects the three anchors. The line is thin, precise, and slightly luminous — like a signal path on a circuit board seen from above.
- The overall feel is: printed circuit board meets architectural blueprint meets editorial infographic. Spare. High-contrast. Confident.

**Style:**
- Editorial illustration. Think MIT Technology Review or Wired magazine feature art — intellectual, precise, not decorative.
- Monochromatic base (dark navy, slate, charcoal) with the single amber/gold accent color as the only warm element.
- Flat or very low depth-of-field. No lens flares, no bokeh, no photorealistic lighting.
- No human figures, no hands, no robots, no abstract "brain" imagery, no glowing orbs.
- No text or labels in the image.
- Not cyberpunk. Not neon. Not the generic "blue glowing neural network" cliché.

**Mood:** calm authority. The visual should make a senior engineer or executive think "this person sees the full stack" — not "this person likes AI aesthetics."

**Request 3 versions:**
- Version 1: use the arc-of-three-anchors concept as described above
- Version 2: your own interpretation of "silicon → cloud → AI" as an abstract technical editorial illustration in the same dark palette and editorial style
- Version 3: an alternative that uses architectural grid lines, precision measurement marks, and layered transparency to suggest depth without using any clichéd AI imagery

---

## After you receive the image

1. Save the file as `hero.png` (PNG, at least 1200×800px)
2. Place it at: `C:\Users\samee\Desktop\pallavi-ai-labs.github.io\assets\hero.png`
3. Also copy to: `C:\Users\samee\Desktop\Pallavi AI Labs\Obsidian Vault\InHerVoice\docs\assets\hero.png`
4. Then open InHerVoice and run: `/website add-hero`

Or tell Claude: "I have the hero image ready at assets/hero.png — please add it to the website."

Claude will replace the current CSS orbit visualization in the hero with the real image.

---

## What Claude will do when you provide the image

Replace the hero right panel in `docs/index.html`:

Find `<!-- HERO IMAGE: when you have a custom image, delete this entire div and replace with:` and the surrounding placeholder block.

Replace with:
```html
          <div class="hidden md:flex justify-center items-center">
            <img
              src="assets/hero.png"
              alt="Silicon to Cloud to AI — Pallavi Sharma's career arc from Intel chip design through AWS cloud infrastructure to Amazon AI agents"
              class="rounded-2xl w-full max-w-lg shadow-2xl shadow-black/60 object-cover"
            />
          </div>
```

Then push to both repos.
