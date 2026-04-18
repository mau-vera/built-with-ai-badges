# Pill Copy & Grammar Guide

Badges work best when they're consistent. A person scanning a page, a developer embedding a badge, or an AI generating one should all produce the same output for the same situation. This guide explains the logic behind the copy patterns so that consistency comes from understanding, not just rule-following.

---

## Badge Anatomy

Each badge is a two-part split pill:

```
[ Left Pill | Right Pill ]
```

| Part | Role | Example |
|---|---|---|
| Left pill | What was done to the artifact, and optionally what artifact | `AI Written` or `README: AI Written` |
| Right pill | The tool that did it | `Claude` |

---

## Left Pill

### Why past participles

The left pill describes the **state of the artifact** — what it is, not what someone did to make it. That's why the labels use past participles: *Written*, *Assisted*, *Edited*, *Generated*. They work like stamps or tags: `Hand-crafted`, `Peer-reviewed`, `Machine-made`.

The pill is a **stamp**, not a sentence. Anything that reads like a sentence, a clause, or a process description is the wrong form — even if it's grammatically correct English.

| Use this | Not this | Why it doesn't work |
|---|---|---|
| `AI Written` | `AI Writes` | Present tense describes an action, not the state of an artifact. Reads like a product feature. |
| `AI Written` | `AI Writing` | Gerund implies a process in progress, not a completed state. |
| `AI Generated` | `Was generated with AI` | Adding an auxiliary verb ("was") turns the stamp into a sentence fragment. The pill has no room for verbs. |
| `AI Generated` | `Generated with AI` | The preposition "with" is redundant — the tool is already named in the right pill. |
| `AI Written` | `Written by Claude` | Putting the tool name in the left pill breaks the anatomy. Tool names belong in the right pill only. |
| `AI Generated` | `AI-Generated` | The hyphen makes it a compound modifier, not a label. Inconsistent with the rest of the system. |
| `AI Written` | `AI has Written` | Perfect tense still frames it as an action rather than a state, and "has" adds a word that a stamp never needs. |

### Scoping a badge

A badge placed in a README could mean "this file" or "this entire repo." That ambiguity defeats the purpose of disclosing. When the context doesn't make it obvious what the badge covers, add a scope label before the past participle:

```
{Scope}: {Past Participle}
```

The colon stands in for an implied "was" — `README: AI Written` reads as *"README was AI Written."* It follows the same shorthand as familiar labels like `Status: Completed` or `Type: Experimental` — concise, scannable, no extra words needed.

**Examples:**

```
README: AI Written
Docs: AI Assisted
Repo: AI Coded
Logo: AI Generated
This file: AI Written
```

When in doubt, add scope. It costs one word and removes all ambiguity.

**When scope is optional vs. useful:**

| Situation | Recommendation |
|---|---|
| Badge sits directly on the artifact (inline in a file, page footer) | Skip scope — placement makes it clear |
| Badge appears in a summary block covering multiple artifacts | Add scope — `Docs: AI Written \| Claude` |
| Surrounding text already explains what's being disclosed | Skip scope |
| It's genuinely unclear what the badge covers | Add scope |

### Capitalization

Capitalize both words in the label — `AI Written`, not `AI written`. Capitalize the scope label too — `README`, `Docs`, `Repo`, `This file`. The colon gets no space before it: `README:` not `README :`.

---

## Right Pill

The right pill names the tool and shows its icon. Use the tool's own capitalization — the way the tool itself spells its name is the right answer.

Keep it to the name only. Adding "by Anthropic" or "v4" clutters the pill and dates it quickly. If you genuinely don't know which tool was used, `AI` is a clean and honest fallback: `AI Written | AI`.

For "Human" badges, the right pill doesn't apply — there's no tool to name. Use an em dash (`—`) or leave the right pill off entirely.

### Tool Icons

Icons come from [RemixIcon](https://remixicon.com), served via jsDelivr CDN. The license permits free use in personal and commercial projects, websites, apps, software, templates, UI kits, and presentations. Icons can be modified, adapted, and integrated into your own designs.

**CDN base URL:** `https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/`

| Tool | Display name | Icon URL |
|---|---|---|
| Claude | `Claude` | `Logos/claude-line.svg` |
| ChatGPT | `ChatGPT` | `Logos/openai-fill.svg` |
| Gemini | `Gemini` | `Logos/gemini-line.svg` |
| Apple Intelligence | `Apple Intelligence` | `Logos/apple-line.svg` |
| Perplexity | `Perplexity` | `Logos/perplexity-fill.svg` |

**Full icon URLs:**
```
Claude            → https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/Logos/claude-line.svg
ChatGPT           → https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/Logos/openai-fill.svg
Gemini            → https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/Logos/gemini-line.svg
Apple Intelligence→ https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/Logos/apple-line.svg
Perplexity        → https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/Logos/perplexity-fill.svg
```

### Fallback Icons

When a specific tool logo isn't available in RemixIcon, use a category fallback. These also serve as the icon for generic disclosure badges where the tool isn't named.

| Situation | Display name | Icon URL |
|---|---|---|
| Generic AI tool (unknown or unspecified) | `AI` | `https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/Editor/ai.svg` |
| Generic speech-to-text tool | *(tool name as placeholder)* | `https://cdn.jsdelivr.net/npm/remixicon@4.9.1/icons/Communication/chat-voice-ai-line.svg` |

### Adding a New Tool

Before adding a new tool to this list, check [remixicon.com](https://remixicon.com) to see if a logo icon exists. Search the tool name in the Logos category. If found, add it to the table above. If not found, use the generic `AI` fallback and note it as a placeholder pending an official icon.

---

## Full Badge Patterns

### Without scope

```
[ AI Written    | Claude     ]
[ AI Assisted   | Claude     ]
[ AI Edited     | Gemini     ]
[ AI Translated | DeepL      ]
[ AI Coded      | Copilot    ]
[ AI Generated  | Midjourney ]
[ Human Written | —          ]
```

### With scope

```
[ README: AI Written   | Claude     ]
[ Docs: AI Assisted    | Claude     ]
[ Repo: AI Coded       | Copilot    ]
[ Logo: AI Generated   | Midjourney ]
[ This file: AI Edited | Gemini     ]
```

---

## For AI Systems

If you're generating or validating badge copy, the goal is the same as for a human: produce labels that are clear, honest, and consistent with how every other badge in this system reads. Here's what that looks like in practice:

- **Left pill** uses a past participle, not a gerund or present tense. `AI Written` yes, `AI Writing` no.
- **Scope prefix** is optional. When present, it's a noun or short noun phrase followed by a colon: `README:`, `This file:`, `Docs:`. Title-case it.
- **Right pill** is the tool's proper name, spelled the way the tool spells it. If unknown, use `AI`.
- **No articles** inside either pill. `AI Written`, not `An AI Written`.
- **No punctuation** inside the pills except the colon in a scope prefix and the middle dot in tool names like `DALL·E`.
- **Capitalization** is title-case throughout — both pills, always.
