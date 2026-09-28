# What does one country review cost?

**National uptake of Recommendation Rec(2022)2**  
Budgeting note for Micheal’s / CEDS team  
28 September 2026

---

## Plain answer

**For a Belgium-like desk review, plan on roughly 5 million billed tokens** (mostly input: the agent re-reads a growing context as it searches and writes).

At current Cursor list prices (API rates), **without counting your included allowance**, that is roughly:

| Model band | Approx. cash cost per country | In pounds (at £0.75 / $1) |
|---|---|---|
| Cheap / fast (Composer 2.5, Gemini Flash, GPT Luna) | about **$1–$4** | about **£0.80–£3** |
| Mid (Grok 4.6/4.7, Claude Sonnet 5, GPT Terra) | about **$10–$11** | about **£7.50–£8.50** |
| Strong frontier (Claude Opus 5 / 5.5, GPT-5.6 Sol) | about **$21–$26** | about **£16–£20** |
| Top / expensive (Claude Fable 5.1) | about **$50+** | about **£40+** |

**Inside Cursor:** that usage usually draws your **included monthly allowance first**. You only see a separate invoice line if you go on-demand after the pool is used up. Cloud Agents are billed at the **selected model’s API price**; there is no separate charge for the VM itself.

These numbers are **planning estimates**, not the Cursor invoice. Exact spend is on the Cursor usage dashboard for the run.

---

## How we estimated tokens (Belgium PoC)

This run produced the Belgium desk review (`countries/belgium.md` + `.yaml`) as the first task.

We reconstructed billed tokens from the saved agent transcript (224 messages: 6 user, 141 assistant, 77 tool), using a cumulative-context model:

- each model call is charged for the **context so far** (input) plus the **new assistant message** (output, including tool-call arguments)
- ~8k tokens of system/tool-schema overhead assumed per call

| Slice | Model calls (approx.) | Input tokens | Output tokens | Total |
|---|---|---|---|---|
| **Belgium desk review only** (to first follow-up) | ~80 | **~4.9 million** | ~0.01–0.05 million | **~5 million** |
| Whole session so far (Belgium + method PDFs + Q&A) | ~140 | ~13.6 million | higher | ~14 million |

**Planning figure used below: 5.0M input + 0.05M output** for one country desk review (Belgium-like).

Why input dominates: agents re-send prior tool results (web pages, laws, drafts) on later turns. The written brief is “only” ~50 KB of files; the **search trail** is what costs tokens.

### Planning bands (tokens per country)

| Band | When it happens | Tokens to budget |
|---|---|---|
| **Lean** | English-heavy sources, few instruments, little back-and-forth | ~1.5M input + 0.03M output |
| **Belgium-like (baseline)** | Dedicated statute + decrees, FR/NL/EN mix, full 58 indicators | **~5M input + 0.05M output** |
| **Hard** | Multi-jurisdiction (e.g. Länder), many association rulebooks, several human follow-ups | ~12M input + 0.12M output |

---

## Cost per model — Belgium-like country (~5M in / 0.05M out)

Prices from [Cursor Models & Pricing](https://cursor.com/docs/models-and-pricing) (per **million** tokens, USD).  
GBP converted at **£0.75 per $1** (planning FX only; check the day’s rate).

Assumes **no prompt-cache discount** and **no Teams “Cursor Token Rate”** (see caveats).

| Model | Provider pool | Input $/MTok | Output $/MTok | Est. USD / country | Est. GBP / country | Pros | Cons |
|---|---|---|---|---|---|---|---|
| **Composer 2.5** | Cursor Models | 0.50 | 2.50 | **~$2.60** | **~£2.00** | Cheapest Cursor-native option; good for drafting; draws Cursor Models pool | Weaker on hard legal nuance / long multilingual research than frontier models |
| **Gemini 3.8 Flash** | Other Models | 0.75 | 3.50 | **~$3.90** | **~£2.90** | Fast and cheap; fine for first pass | May miss subtle statutory distinctions; more human checking needed |
| **GPT-5.6 Luna** | Other Models | 0.20 | 1.20 | **~$1.10** | **~£0.80** | Lowest cash cost in this table | Smallest / least capable GPT-5.6 tier — risky as sole reviewer for legal desk work |
| **Grok 4.6 / 4.7** | Cursor Models | 2.00 | 6.00 | **~$10.30** | **~£7.70** | Strong agent use; Cursor Models pool; no Teams token surcharge on first-party | Still not a specialist legal model; long-context / Fast modes cost more |
| **Claude Sonnet 5** | Other Models | 2.00 | 10.00 | **~$10.50** | **~£7.90** | Best cost/quality balance for this task type; solid long docs | Other Models pool; Teams add Cursor Token Rate |
| **GPT-5.6 Terra** | Other Models | 2.00 | 12.00 | **~$10.60** | **~£8.00** | Mid GPT-5.6; capable agent | More expensive output than Sonnet; Other Models pool |
| **Claude Opus 5.5** | Other Models | 4.00 | 20.00 | **~$21.00** | **~£15.80** | Stronger reasoning / careful reading | ~2× Sonnet cost |
| **GPT-5.6 Sol** | Other Models | 4.00 | 20.00 | **~$21.00** | **~£15.80** | Strong OpenAI frontier (promo pricing noted by OpenAI into Nov 2026) | Same ballpark as Opus 5.5; burns Other Models pool faster |
| **Claude Opus 5** | Other Models | 5.00 | 25.00 | **~$26.30** | **~£19.70** | Very strong for dense legal mapping | Pricey for 30+ countries |
| **Claude Fable 5.1** | Other Models | 10.00 | 50.00 | **~$52.50** | **~£39.40** | Top-tier long-running agent intelligence | ~5× Sonnet; needs retention approval in some setups; usually overkill for routine scans |

### Lean and hard countries (same models, quick view)

| Model | Lean (~1.5M/0.03M) | Belgium-like (~5M/0.05M) | Hard (~12M/0.12M) |
|---|---|---|---|
| Composer 2.5 | ~£0.60 | ~£2.00 | ~£4.70 |
| Gemini 3.8 Flash | ~£0.90 | ~£2.90 | ~£7.10 |
| Grok 4.6/4.7 | ~£2.40 | ~£7.70 | ~£18.50 |
| Claude Sonnet 5 | ~£2.50 | ~£7.90 | ~£18.90 |
| Claude Opus 5.5 / GPT-5.6 Sol | ~£5.00 | ~£15.80 | ~£37.80 |
| Claude Opus 5 | ~£6.20 | ~£19.70 | ~£47.30 |
| Claude Fable 5.1 | ~£12.40 | ~£39.40 | ~£94.50 |

---

## Scale-up sketch (Belgium-like, Claude Sonnet 5)

| Volume | Est. tokens | Est. cash if no allowance | Notes |
|---|---|---|---|
| 1 country | ~5M | ~£8 | PoC |
| 10 countries | ~50M | ~£80 | Still small vs human days |
| 30 States Parties | ~150M | ~£240 | Plus human expert time (the real cost) |
| 30 hard countries | ~360M | ~£570 | Upper planning bound |

Human expert review time is **not** in these figures and will usually dwarf token cost.

---

## What Cursor actually charges (so the allowance point is clear)

1. **Cloud Agents bill tokens at the model’s API list price** (same rates as in the table).  
2. **Included allowance is used first** (Cursor Models pool vs Other Models pool, depending on model).  
3. **On-demand** applies only after included usage is exhausted (must be enabled for Cloud Agents).  
4. **No separate VM fee** for Cloud Agents (as of Cursor’s public docs / forum clarifications).  
5. On **Teams / Enterprise**, third-party models also incur a **Cursor Token Rate of $0.25 per million tokens** on top of API price (~+£0.90 on a 5M-token Sonnet run). First-party Cursor models (Grok, Composer) are exempt.  
6. **Prompt caching** can cut effective input cost a lot when the same law texts are re-read; the table above is the **pessimistic (no-cache)** case.

So: **“How much does a country cost?”**  
→ **~5M tokens** for Belgium-like work.  
→ **~£2 to ~£20** cash-equivalent depending on model, if it were all on-demand.  
→ **Often £0 extra on the invoice** while it still fits inside included allowance — but it still **consumes** that allowance.

---

## Practical recommendation for this project

| Approach | Suggestion |
|---|---|
| **Default for production desk reviews** | **Claude Sonnet 5** or **Grok 4.6/4.7** — about **£8 / country** cash-equivalent, good quality for statute mapping |
| **Budget / volume pass** | Composer 2.5 or Gemini Flash first, then human or Sonnet spot-check of `partial` / `not_found` lines |
| **Hard countries or expert-facing final polish** | Opus 5.5 / GPT-5.6 Sol for a second pass on weak indicators only (not the whole 58 from scratch) |
| **Do not default to Fable** | Reserve for cases where Sonnet/Grok clearly fail long-horizon research |

Always keep the **human check** step (see `how-a-country-scan-works.pdf`): token cost is cheap compared with sending a wrong `met` to a country expert.

---

## Caveats (read before budgeting)

- Token estimate is **reconstructed from this PoC transcript**, not copied from the Cursor billing API. Check **Settings → Usage** for the true number on your account.  
- Output tokens in the transcript look low because much “writing” sits in tool-call payloads; we padded output to **0.05M** for Belgium-like planning.  
- Follow-up chat (method notes, PDFs, Q&A) can **double or triple** a session beyond the pure country file. Budget **desk review** and **partner communication** separately if needed.  
- FX (£0.75/$1) is illustrative.  
- Prices change; re-check [cursor.com/docs/models-and-pricing](https://cursor.com/docs/models-and-pricing) when locking a grant budget.  
- Web search / browsing tool usage may add provider-side costs on some stacks; Cloud Agent public guidance is still “tokens at API rates.”

---

## One-line budget line for a proposal

> *AI desk review: ~5 million tokens per country (~£8 at Claude Sonnet 5 list rates); usually drawn from Cursor included allowance; human expert validation separate.*

---

*Prepared from the Belgium PoC run (bc-066382ea-3141-4635-b3da-bec7d66c6022) and Cursor published model prices as of 28 September 2026.*
