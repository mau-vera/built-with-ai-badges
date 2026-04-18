# AI Disclosure Badges

Open, copy-paste badges for transparently disclosing how AI tools were used in your work: emails, websites, documents, slide decks, and repos.

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

## How the badges work

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

The colon stands in for an implied "was": `README: AI Written` reads as *"the README was AI Written."* See [`spec/pill-copy-guide.md`](spec/pill-copy-guide.md) for the full grammar guide.

---

## Color coding

| Color | Meaning |
|---|---|
| 🟣 Purple `#7B5EA7` | Heavy AI use: AI generated the content |
| 🔵 Blue `#2E71A8` | Partial AI use: AI assisted a human |
| ⚫ Gray `#7A8694` | Utility use: AI as a tool, not a creator |
| 🟢 Green `#3A7D5E` | No AI: human-made |

---

## Make your own label

There is no fixed set of labels. Use any past participle that accurately describes what happened to the thing you're disclosing. The badge system is a vocabulary, not a checklist.

**If it was heavily AI-generated:** `AI Written`, `AI Coded`, `AI Generated`, `AI Composed`, `AI Designed` (purple)

**If a human did it with AI help:** `AI Assisted`, `AI Edited`, `Copy Proofread`, `AI Translated`, `AI Summarized`, `Outline: AI Assisted` (blue)

**If AI was used as a utility tool:** `AI Transcribed`, `AI Fact-Checked`, `AI Captioned` (gray)

**If no AI was used:** `Human Written`, `Human Coded`, `Human Made`, `Human Photographed` (green)

Make up whatever label fits. The goal is accuracy, not compliance with a list. Browse [`badge-gallery.html`](badge-gallery.html) for visual examples of common badges.

---

## Platform examples

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

Use scope labels when combining badges so it's clear what each one applies to.

```html
<div style="font-size:0.8em;color:#888;margin-top:2rem;padding-top:1rem;border-top:1px solid #e5e5e5;display:flex;flex-wrap:wrap;align-items:center;gap:0.6rem;">
  AI disclosures:

  <!-- Writing: AI Assisted · Claude -->
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

**Left pill color reference:**

| Type | `background` value |
|---|---|
| AI Generated / heavy use | `#7B5EA7` |
| AI Assisted / partial use | `#2E71A8` |
| AI Utility (translate, transcribe) | `#7A8694` |
| Human Made / no AI | `#3A7D5E` |

---

### GitHub README

GitHub's markdown renderer sanitizes inline `style` attributes from HTML elements in `.md` files as a security measure. The pill HTML is valid, but without CSS the pills render as unstyled plain text. This is a GitHub limitation, not a problem with the badges themselves.

**Once SVG badge files are published to this repo** (see [Coming soon](#coming-soon)), you can embed them as images in any markdown file:

```markdown
![Writing: AI Assisted](https://your-host.com/badges/svg/ai-assisted--claude.svg)
![Code: Human Coded](https://your-host.com/badges/svg/human-coded.svg)
```

In the meantime, the full inline HTML works on **GitHub Pages** and any `.html` file in your repo. Use the web page snippet above.

---

### Google Doc footer

Google Docs is a word processor, not an HTML renderer. There is no way to paste or embed HTML or CSS into a document. The only way to add a visual badge is to insert a badge as an image file via **Insert > Image**.

**Once PNG badge files are published to this repo** (see [Coming soon](#coming-soon)), you can:

1. Download the badge PNG for your disclosure
2. In your document, go to **Insert > Image > Upload from computer**
3. Place the image inline at the end of the document or in the footer via **Insert > Headers & footers > Footer**

---

### Gmail signature

Email clients implement their own CSS rendering. Gmail strips `display:flex` and most modern layout properties from signature HTML. A flexbox pill will render as broken unstyled text in most inboxes.

**Once PNG badge files are published to this repo** (see [Coming soon](#coming-soon)), you can embed a badge as an inline image in your Gmail signature:

1. Gmail → Settings (gear icon) → **See all settings**
2. **General** tab → scroll to **Signature**
3. In the signature editor, click the **Insert image** icon
4. Upload your badge PNG or paste its hosted URL

Until then, the signature editor's rich text mode lets you add a styled text disclosure: set a separator line, type your disclosure, and use the formatting toolbar to set a small font size and gray color to keep it unobtrusive.

---

## Coming soon

SVG and PNG badge files will be published to this repo to unlock embedding in GitHub markdown, Google Docs, and email. Track progress here:

- [ ] Publish `/badges/svg/` with pre-built SVG files for all common labels and tools
- [ ] Publish `/badges/png/` with raster versions at 2x resolution
- [ ] Host on GitHub Pages for stable `<img>` URL embedding
- [ ] Build a badge generator page for custom labels and tool combinations
- [ ] Update README with hosted URLs once published

---

## Build your own badge

You only need the HTML template and the right color. All other choices are yours.

**HTML template:**

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

For the full grammar and copy rules, see [`spec/pill-copy-guide.md`](spec/pill-copy-guide.md).

---

## License

[CC0 1.0 Universal](LICENSE) — Public Domain. Use freely, no attribution required.

---

*Inspired by Mike Elgan's [Always disclose how you use AI](https://www.computerworld.com/article/4120839/always-disclose-how-you-use-ai.html) (Computerworld, Jan 2026).*

*AI disclosures: README: AI Assisted · Claude*
