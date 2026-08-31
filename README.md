# How AI Learned to Engineer

A talk on the evolution of AI engineering, from chatbot to autonomy. Given at the **Laravel Nagpur Meetup**, 30 minutes, 41 slides.

**▸ [View the deck](https://bhushan.github.io/ai-harness-to-ai-agents-slides/)**

---

## The talk

The model got better. Most of what actually changed is the engineering around the model.

The deck walks that engineering forward one generation at a time: a chatbot with no context, then prompts, then retrieval, then hands, then a loop, then everything you have to build so the loop can be trusted to run unsupervised. Each layer exists because the one before it hit a wall, and every wall in the talk is one the speaker has hit in production.

It ends where the industry currently is: the harness, the workstation, multi-agent systems, and what is left for the engineer once the machine can write the code.

## Contents

| Act | Covers |
| --- | --- |
| 0 · Opening | The question, and the map of the ground |
| 1 · Foundation | Chatbots, LLM APIs, prompt engineering, structured outputs |
| 2 · Context | Embeddings, RAG, and why retrieval quality decides everything |
| 3 · Action | Tool calling, memory, fine-tuning, and the shift to agents |
| 4 · Reliability | Workflow or agent, MCP, evals, guardrails, observability |
| 5 · Autonomy | The environment, the harness, the workstation, multi-agent systems |
| 6 · Close | The complete stack, the engineer's role, and where to start |

## Controls

| Key | Does |
| --- | --- |
| `→` `←` `Space` `PgUp` `PgDn` | Next and previous step |
| `Home` `End` | First and last slide |
| `F` | Full screen |
| `M` | Slide map |
| `N` | Speaker notes drawer |
| `Esc` | Slide overview, or close whatever is open |

Scroll and swipe also advance the deck. The current slide is written to the URL hash, so `#23` opens on slide 23 and reloads keep your place.

> **Presenting?** `N`, `M` and `Esc` render **on the slide**, not on a second screen. Do not press them while sharing.

## Running it locally

The deck is one self-contained `index.html`. Open it directly in a browser, or serve the folder:

```bash
python3 -m http.server 8000   # then open http://localhost:8000
```

No build step, no install, no bundler.

## How it is built

- **One file.** All 41 slides, the animation engine, the typefaces and every image live inside `index.html`. It is 528KB and makes **zero network requests**, so venue wifi cannot break the talk.
- **APPARATUS**, the [Alfred Scholar](https://alfredscholar.com) design system, provides every colour as an `--alfred-*` token. Nearly achromatic: hierarchy comes from type, whitespace and a hairline.
- **Three typefaces, no fourth.** Geist operates the deck, Fraunces is the one line per slide you are meant to sit with, Geist Mono identifies. All vendored as Latin-subset variable fonts.
- **[GSAP](https://gsap.com)** drives the reveals, inlined and pinned to eases named after the design system. Motion resolves onto its mark: no overshoot, no bounce, no spring.
- Pressing forward mid-reveal completes the current animation instead of skipping the step, so the deck never runs ahead of the speaker.

## Speaker material

The spoken script and the rehearsal notes are deliberately **not** in this repository. They are gitignored and stay on the speaker's machine. What is published here is the deck as the room saw it, including the embedded per-slide notes in the `N` drawer.

## Deployment

GitHub Pages serves `main` from the repository root. Pushing to `main` publishes the deck.

## Credits

Deck and talk by [Bhushan](https://github.com/bhushan). GSAP is used under the [GreenSock standard licence](https://gsap.com/standard-license). Geist, Geist Mono and Fraunces are used under the SIL Open Font License.
