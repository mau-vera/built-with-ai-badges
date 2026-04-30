# AI Disclosure Badges

![ReadMe](https://raw.githubusercontent.com/mau-vera/built-with-ai-badges/main/badges/docs/readme-ai-assisted--claude.svg) ![Site](https://raw.githubusercontent.com/mau-vera/built-with-ai-badges/main/badges/code/ai-coded--claude.svg) 

Open, copy-paste badges for transparently disclosing how AI tools were used in your work: emails, websites, documents, slide decks, and repos.

<p align="center">
  <a href="https://disclosingai.com">
    <img src="https://img.shields.io/badge/Build%20your%20badge%20%E2%86%92-disclosingai.com-212529?style=for-the-badge" alt="Build your badge at disclosingai.com" height="40">
  </a>
</p>

AI use in professional work is widespread but rarely [disclosed](https://www.computerworld.com/article/4120839/always-disclose-how-you-use-ai.html). When you read an email, a piece of code, or a PRD, you can't tell if you're reading someone's thinking or a model's output. The fix is an honor system: just say how you used AI.

---

## How badges work

Each badge is a two-part pill:

```
[ What was done  |  Tool that did it ]
```

The **left pill** describes the state of the artifact using a past participle: a stamp, not a sentence. `AI Written`, not `AI Writes` or `AI has Written`.

The **right pill** names the tool. Use the tool's own capitalization: `Claude`, `ChatGPT`, `Gemini`. If you don't want to name a specific tool, `AI` is a clean and honest fallback.

Human badges have no tool to name. They are a single full pill with no split.

When it's not obvious what the badge covers, add a scope prefix before the label:

```
README: AI Written  |  Claude
Docs: AI Assisted   |  Claude
Logo: AI Generated  |  Midjourney
Code: Human Coded
```

The colon stands in for an implied "was": `README: AI Written` reads as *"the README was AI Written."* See [`pill-copy-guide.md`](pill-copy-guide.md) for the full grammar guide.

---

## Pick a label and color

There is no fixed set of labels. Use any past participle that accurately describes what happened to the thing you're disclosing. The badge system is a vocabulary, not a checklist.

| Color | Meaning | Example labels |
|---|---|---|
| 🟣 Purple `#7B5EA7` | Heavy AI use — AI generated the content | `AI Written`, `AI Coded`, `AI Generated`, `AI Composed`, `AI Designed` |
| 🔵 Blue `#2E71A8` | Partial AI use — AI assisted a human | `AI Assisted`, `AI Edited`, `AI Translated`, `AI Summarized`, `Outline: AI Assisted` |
| ⚫ Gray `#7A8694` | Utility use — AI as a tool, not a creator | `AI Transcribed`, `AI Fact-Checked`, `AI Captioned` |
| 🟢 Green `#3A7D5E` | No AI — human-made | `Human Written`, `Human Coded`, `Human Made`, `Human Photographed` |

Make up whatever label fits. The goal is accuracy, not compliance with a list.

---

## Embed it

The [badge generator at disclosingai.com](https://disclosingai.com) gives you ready-to-paste code for any platform. Pick your label, tool, and color, then copy. The sections below explain how embedding works on each platform.

### Web page

The full pill HTML works in any web page. Inline styles make it self-contained with no external stylesheet required.

**Single badge:**

```html
<span style="display:inline-flex;align-items:stretch;font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',sans-serif;font-size:0.85em;font-weight:500;white-space:nowrap;border-radius:999px;box-shadow:0 1px 3px rgba(0,0,0,0.1);">
  <span style="display:flex;align-items:center;padding:0.45em 0.9em 0.45em 1em;border-radius:999px 0 0 999px;background:#2E71A8;color:#fff;">AI Assisted</span>
  <span style="display:flex;align-items:center;gap:0.5em;padding:0.45em 1em 0.45em 0.9em;border-radius:0 999px 999px 0;background:#212529;color:#fff;">
    <img src="https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/Logos/claude-line.svg" alt="Claude" style="width:16px;height:16px;filter:invert(1);" />
    Claude
  </span>
</span>
```

**Human badge (single pill, no split):**

```html
<span style="display:inline-flex;align-items:center;gap:0.5em;font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',sans-serif;font-size:0.85em;font-weight:500;white-space:nowrap;border-radius:999px;box-shadow:0 1px 3px rgba(0,0,0,0.1);background:#3A7D5E;color:#fff;padding:0.45em 1em;">
      <img src="https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/User%20%26%20Faces/open-arm-line.svg" alt="" style="width:20px;height:20px;filter:invert(1);" />
      Human Written
    </span>
```

**Multi-badge disclosure block** (for a page footer or article byline):

Use scope labels when combining badges so it's clear what each one covers.

```html
<div style="font-size:0.8em;color:#888;margin-top:2rem;padding-top:1rem;border-top:1px solid #e5e5e5;display:flex;flex-wrap:wrap;align-items:center;gap:0.6rem;">
  AI disclosures:

  <!-- Documentation: AI Written · Claude -->
  <span style="display:inline-flex;align-items:stretch;font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',sans-serif;font-size:0.85em;font-weight:500;white-space:nowrap;border-radius:999px;box-shadow:0 1px 3px rgba(0,0,0,0.1);">
    <span style="display:flex;align-items:center;padding:0.45em 0.9em 0.45em 1em;border-radius:999px 0 0 999px;background:#2E71A8;color:#fff;">Documentation: AI Written</span>
    <span style="display:flex;align-items:center;gap:0.5em;padding:0.45em 1em 0.45em 0.9em;border-radius:0 999px 999px 0;background:#212529;color:#fff;">
      <img src="https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/Logos/claude-line.svg" alt="Claude" style="width:16px;height:16px;filter:invert(1);" />
      Claude
    </span>
  </span>

  <!-- Code: Human Coded (single pill) -->
  <span style="display:inline-flex;align-items:center;gap:0.5em;font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',sans-serif;font-size:0.85em;font-weight:500;white-space:nowrap;border-radius:999px;box-shadow:0 1px 3px rgba(0,0,0,0.1);background:#3A7D5E;color:#fff;padding:0.45em 1em;">
      <img src="https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/User%20%26%20Faces/open-arm-line.svg" alt="" style="width:20px;height:20px;filter:invert(1);" />
      Human Coded
    </span>
</div>
```

---

### GitHub README

GitHub's markdown renderer sanitizes inline `style` attributes as a security measure. The pill HTML is valid, but without CSS it renders as unstyled plain text. This is a GitHub limitation, not a problem with the badges themselves.

Use SVG files instead. Browse the [`/badges/`](https://github.com/mau-vera/built-with-ai-badges/tree/main/badges) folder — files are organized by context (`writing/`, `code/`, `docs/`, `comms/`, `research/`, `images/`, `prd/`) with a `neutral/` folder for generic scope-less badges. File names follow the pattern `{scope-label}--{tool}.svg`.

```markdown
![AI Assisted · Claude](https://raw.githubusercontent.com/mau-vera/built-with-ai-badges/main/badges/neutral/ai-assisted--claude.svg)
```

```markdown
![README: AI Written · Claude](https://raw.githubusercontent.com/mau-vera/built-with-ai-badges/main/badges/docs/readme-ai-written--claude.svg)
```

```markdown
![Human Written](https://raw.githubusercontent.com/mau-vera/built-with-ai-badges/main/badges/human/human-written.svg)
```

The full inline HTML works on **GitHub Pages** and any `.html` file in your repo.

---

### Google Doc

Google Docs has no HTML renderer. The only way to add a visual badge is to insert one as an image via **Insert > Image**.

1. Browse the [`/badges/`](https://github.com/mau-vera/built-with-ai-badges/tree/main/badges) folder and open the PNG that matches your disclosure
2. Click **Download raw file** to save it
3. In your Google Doc, go to **Insert > Image > Upload from computer** and select the PNG
4. To place it in the footer, go to **Insert > Headers & footers > Footer** first, then insert the image

A height of around 18px works well inline; 22–24px for a standalone footer line.

---

### Gmail signature

Gmail strips `display:flex` and most modern layout properties from signature HTML. A flexbox pill will render as broken unstyled text.

Use a PNG instead. The `comms/` folder has email-specific badges like `email-ai-assisted--claude.png`.

1. Browse the [`/badges/`](https://github.com/mau-vera/built-with-ai-badges/tree/main/badges) folder and download the PNG that matches your disclosure
2. In Gmail, go to **Settings > See all settings > General > Signature**
3. Click the **Insert image** icon in the signature editor, choose **Upload**, and select the PNG
4. Click the image and use the resize options to set the size — **Small** works best for consistent rendering across devices

---

## Build from scratch

If you want a badge the generator doesn't cover, you only need the HTML template and the right color hex.

```html
<!-- AI badge (two-part pill) -->
<span style="display:inline-flex;align-items:stretch;font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',sans-serif;font-size:0.85em;font-weight:500;white-space:nowrap;border-radius:999px;box-shadow:0 1px 3px rgba(0,0,0,0.1);">
  <span style="display:flex;align-items:center;padding:0.45em 0.9em 0.45em 1em;border-radius:999px 0 0 999px;background:COLOR;color:#fff;">Label</span>
  <span style="display:flex;align-items:center;gap:0.5em;padding:0.45em 1em 0.45em 0.9em;border-radius:0 999px 999px 0;background:#212529;color:#fff;">
    <img src="ICON_URL" alt="TOOL" style="width:16px;height:16px;filter:invert(1);" />
    Tool Name
  </span>
</span>

<!-- Human badge (single pill) -->
<span style="display:inline-flex;align-items:center;gap:0.5em;font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',sans-serif;font-size:0.85em;font-weight:500;white-space:nowrap;border-radius:999px;box-shadow:0 1px 3px rgba(0,0,0,0.1);background:#3A7D5E;color:#fff;padding:0.45em 1em;">
      <img src="https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/User%20%26%20Faces/open-arm-line.svg" alt="" style="width:20px;height:20px;filter:invert(1);" />
      Human Label
    </span>
```

**Tool icons** (from [RemixIcon](https://remixicon.com), free for all use):

| Tool | Icon URL |
|---|---|
| Claude | `https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/Logos/claude-line.svg` |
| ChatGPT | `https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/Logos/openai-fill.svg` |
| Gemini | `https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/Logos/gemini-line.svg` |
| Apple Intelligence | `https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/Logos/apple-line.svg` |
| Perplexity | `https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/Logos/perplexity-fill.svg` |
| Generic AI | `https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/Editor/ai.svg` |

For the full grammar and copy rules, see [`pill-copy-guide.md`](pill-copy-guide.md).

---

## Why disclose

AI has been part of professional work for a few years now. The problem isn't that people use it; it's that most of the time nobody says so. That silence is creating a slow erosion of trust. When you read an email, a report, or a README, you don't know if you're reading someone's thinking or a chatbot's output. That uncertainty is disorienting, and it's getting worse.

The fix isn't a policy or a law. It's a norm: just say what you did.

Mike Elgan framed this clearly in [*Always disclose how you use AI*](https://www.computerworld.com/article/4120839/always-disclose-how-you-use-ai.html):

> *"For the same reason that the foods we buy in the supermarket are augmented with lists of ingredients, we should always list the 'ingredients' of the communications we do and the content we create so the 'consumers' know what they're getting."*

A few concrete reasons to disclose:

**It signals the quality and source of your work.** If you wrote something yourself, a badge gives you credit for it. If AI did the heavy lifting, others deserve to know. Both are honest, and honest is more valuable than impressive.

**It gives colleagues better context.** AI tools can introduce hallucinations, tonal flatness, and confident-sounding errors. When someone knows AI was involved, they know to apply a different kind of scrutiny. That's useful to them.

**It mitigates blame for AI biases you didn't introduce.** If a piece of content turns out to have a subtle bias, disclosing that AI was used opens the door for others to flag it, and protects you from owning a bias that came from the model, not from you.

**It shows respect for data privacy.** Using AI to reply to an email means uploading someone else's words to a third-party model. Disclosing this, or disclosing that you did not, signals that you're thinking about what you're doing with other people's data.

**It builds a useful feedback loop.** When disclosure is normalized, you learn what tools your colleagues are using and why. That's more valuable than any AI tips newsletter.

---

## This works on the honor system

There is no enforcement here. No badge validator. No disclosure police. This project exists purely to make disclosure easy: to give you the vocabulary, the visuals, and the copy-paste code so that when you want to be transparent, the friction is zero.

As Elgan put it: *"Obviously, this idea works on the honor system. But those who lie about how they use AI are doing us a favor when we catch them in the act. Such people are not to be trusted."*

Use these badges because you think transparency is worth something, not because someone told you to.

---

## License

[CC0 1.0 Universal](LICENSE) — Public Domain. Use freely, no attribution required.

---

*Inspired by Mike Elgan's [Always disclose how you use AI](https://www.computerworld.com/article/4120839/always-disclose-how-you-use-ai.html) (Computerworld, Jan 2026).*
