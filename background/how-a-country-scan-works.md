# How a country scan works

**National uptake of Recommendation Rec(2022)2**  
Method note for country experts and review partners  
Version for the Belgium proof of concept — 28 September 2026

---

## Who does what

| Role | Who | What they do |
|---|---|---|
| **Desk reviewer (AI agent)** | Cursor cloud agent working in this repository | Runs the search protocol, opens public sources, drafts judgements against the 58 duties, writes the `.md` / `.yaml` files and survey questions |
| **Review team (humans)** | Project / CEDS team | Sets the codebook and method; reads the draft; challenges weak lines; decides what to send to the country |
| **Country expert (human)** | Micheal’s counterpart / national representative | Confirms, corrects, or supplies missing instruments; answers the survey gaps |

When this note says **“the reviewer”**, it means the **AI desk agent** that produced the draft country file — not a human lawyer signing off the law. The AI draft is the starting map. **Humans check and own the result** before it is treated as settled.

---

## One-sentence summary

A country scan is a checklist-driven desk review of public legal sources against Rec(2022)2’s 58 duties, with every search and judgement written into the repository so a human expert can reproduce, challenge, or correct it. It is not a black-box score.

---

## 1. What we are checking against

Before any country is opened, the project already has a **codebook** (`codebook/codebook.md`). That is the checklist. It was built from Recommendation Rec(2022)2:

| Part of the recommendation | What it covers in the review |
|---|---|
| **Annex 1** | National law topics: governance, venue safety, certification, infrastructure, emergency planning, access/tickets, policing, bans, dialogue, offences |
| **Annex 2** | Stewarding topics: status, qualification, vetting, duties, powers, conduct, visibility, records, training, private-security link |

That gives **16 topic groups (clusters)** and **58 individual duties (indicators)**.

Examples of duties:

- Is there a named national coordinating body?
- Is a safety officer required at the venue?
- Is CCTV required at designated venues?
- Can stewards search at entry?
- Is there a national football information point?
- Must stewards complete approved training before deployment?

Every country is scored against **the same 58**. We do not invent new questions per country.

---

## 2. What “doing a country” involves, step by step

These steps are what the **AI desk agent** does when producing a draft. Humans then check the output (see section 5).

### Step A — Confirm party status

Look up whether the country is a State Party to the Saint-Denis Convention (CETS No. 218), with signature, ratification, and entry-into-force dates.

*Belgium example:* signed 29 November 2016; ratified 9 September 2024; in force 1 November 2024 (Council of Europe country profile + BeSafe ratification notice).

### Step B — Run the fixed search protocol

The project README fixes **six source families** that must be checked for every country:

1. National legislation database or official gazette  
2. Ministry responsible for sport, and the authority responsible for policing sports events  
3. Stadium licensing or safety-certification authority  
4. National football association’s safety and stadium rules  
5. National football information point (NFIP), or the body that carries that function  
6. Direct search for `Rec(2022)2`, the Saint-Denis Convention, and CETS No. 218  

Searches use the indicator wording **and** national-language legal terms (for Belgium: *loi football*, *stewards*, *interdiction de stade*, *responsable de la sécurité*, and so on).

Empty results are logged as carefully as hits. A search that finds nothing is still part of the audit trail.

### Step C — Open the actual instruments

Titles alone are not enough. The AI desk agent opens statutes, royal decrees / regulations, consolidated texts, and official ministry pages, and reads the provisions that speak to each duty.

*Belgium example — main instruments opened:*

- Loi du 21 décembre 1998 (consolidated Football Act)  
- Loi du 19 juin 2023 (amending Act)  
- Arrêté royal du 25 mai 1999 (steward engagement)  
- Arrêté royal du 15 juin 1999 (coordination / safety officer / Cellule football)  
- Arrêté royal du 6 juillet 2013 (stadium safety norms)  
- CCTV, ticketing, and stadium-ban file decrees  
- BeSafe policy pages; CoE country profile; NFIP descriptions  

What was **not** opened is also stated (for Belgium: full RBFA/Pro League licensing books end to end; every OOP circular; non-football sports instruments).

### Step D — Map text to each of the 58 duties

For each duty, the AI desk agent asks: **does a national instrument require this?**

| Judgement | Meaning |
|---|---|
| `met` | A national instrument requires the substance of the duty for football matches or other sports events in scope |
| `partial` | Only part of the duty; only some events; or guidance / practice rather than a hard requirement |
| `not_found` | The search protocol was completed and no such instrument was identified |
| `not_applicable` | The duty cannot apply; the assessment says why |

Also recorded for every duty:

- **Confidence** — high / medium / low  
- **Change since 1 September 2022** — new / amended / unchanged / unknown  
- **Evidence** — which instruments support the line  

*Belgium example:* “safety officer” → Football Act art. 6 + AR 15 June 1999 → `met`, high confidence, unchanged since 2022.

Statute, regulation, and a licensing condition that a venue must meet can all count as `met`. A football-association rule or ministry circular can be `met` when it is the instrument that actually imposes the duty. A strategy or guidance note that only recommends the duty is `partial`.

### Step E — Write two files

| File | Audience | Purpose |
|---|---|---|
| `countries/<country>.md` | Humans (review team + country expert) | Readable brief: short answer, changes since 2022, topic narrative, judgement table, survey questions, sources |
| `countries/<country>.yaml` | Working record / later comparison | Structured searches, evidence list, all 58 judgements with evidence IDs and notes |

### Step F — Generate survey questions

Anything judged `partial`, `not_found`, or low-confidence becomes a pre-filled question for the country expert:

> We found X. It appears to meet / partially meet / not address this duty. Please confirm, correct, or name the instrument that should replace this finding.

One open question also asks what has changed since 1 September 2022 that the brief missed. Replies use the same indicator IDs so they can update the assessment and be compared across countries.

---

## 3. How you know which pages were gone through

Nothing is invisible. There are three audit layers in every country file. These are the first place **humans** look when checking the AI draft.

### A. Search log (`searches:` in the `.yaml`)

Each check records:

- source family (gazette / police / licensing / sport ministry / football association / NFIP / citation)  
- query used  
- date  
- outcome (`hit` or `none`)  
- URL  
- note  

### B. “Where this was looked for” table (in the `.md`)

A plain table: place → what was opened → result.  
It also states what was **not** opened in that pass.

### C. Evidence list + per-indicator sources

Each instrument gets an evidence entry (title, citation, URL, date, language, short paraphrase).  
Each of the 58 judgements points back to those evidence IDs.  
The judgement table at the end of the `.md` has a one-line source per duty.  
Full URLs are repeated under **Sources**.

So if a partner asks “did the AI actually look at the steward decree?”, the answer is in the yaml search entry, the evidence ID, the md search table, and every indicator that cites that decree. A human can open the same URL and re-read the article.

---

## 4. What this is not

Important for expectations:

- **Not a live scrape of every law in the country’s database.** It is targeted search plus reading of opened pages and PDFs.  
- **Not a model that “knows” national law.** The draft only knows what it found and cited in that pass.  
- **Not exhaustive of every circular or association handbook.** If something was not opened, the brief says so and drops confidence or marks `partial` / a survey question.  
- **Association practice is not automatically statute.** Club web pages can support `partial`; they do not get treated as a hard national duty unless a binding instrument requires it.  
- **Language limits are recorded.** A judgement the AI could not fully verify stays at lower confidence until a human reader of that language, or the country representative, confirms it.  
- **Not a final legal opinion.** The AI desk review is a draft map. Human review and country-expert validation close the gaps.

---

## 5. Where humans check the results

This is the non-magic part. Humans do not have to trust the AI’s word; they check the trail.

### For the project / CEDS review team

| Check | Where | What to do |
|---|---|---|
| Read the draft narrative | `countries/<country>.md` — top sections and topic-by-topic text | Does the short answer match what you know of the country? Spot overclaims. |
| Spot-check judgements | Judgement table at the end of the `.md`, or each line in the `.yaml` | Pick high-stakes duties (bans, certification, stewarding). Follow the source column / evidence ID. |
| Re-open the cited law | URLs under **Sources** and in `evidence:` | Confirm the article really says what the draft claims. |
| See what was missed | “Where this was looked for” + notes on what was **not** opened | Decide whether another pass is needed before sending to the country. |
| Challenge weak lines | Any `partial`, `not_found`, or `low` confidence row | Either find better evidence, or leave it for the country survey. |
| Compare countries | Same indicator ID across UK / Austria / Belgium `.yaml` files | Same duty, same scale — useful for consistency checks. |

Practical rule of thumb: **if a line matters for a decision or for sending to a country expert, a human should open the cited source at least once.**

### For Micheal’s team / the country expert

| Check | Where | What to do |
|---|---|---|
| Read the brief as a national reader | `countries/belgium.md` (or the relevant country file) | Confirm the framework description; flag wrong or outdated instruments. |
| Answer the survey block | “What a … reader would be asked” section | Confirm, correct, or name the missing instrument for each gap question. |
| Supply instruments the AI missed | Reply against the same indicator IDs (`a1.cert.required`, `a2.train.ct`, …) | Those replies update the assessment; they become the human-verified record. |
| Challenge a `met` that is too strong | Judgement table + Sources | Point to the real instrument, or say the duty is only guidance / only some events → status becomes `partial`. |
| Challenge a `not_found` | Same | Name the statute, decree, circular, or association rule the desk pass missed. |

The survey is designed so the country expert does **not** re-do all 58 duties from scratch. Clusters that are `met` at high confidence can be one confirmation. Effort goes to gaps and weak lines.

### What “done” means

| Stage | Owner | Meaning |
|---|---|---|
| Draft desk review in the repo | AI desk agent | Sourced map exists; audit trail written |
| Internal human read | Project / CEDS team | Draft is good enough to share |
| Country expert reply | Micheal’s counterpart | Gaps closed or corrected |
| Updated assessment | Project team (from replies) | Human-verified lines replace or confirm AI draft lines |

Until the country expert (or an equivalent human legal reader) has confirmed or corrected it, treat the file as a **desk draft**, not a certified national position.

---

## 6. What has been completed so far

| Country | Role | File |
|---|---|---|
| United Kingdom | First completed review | `countries/united-kingdom.md` |
| Austria | Second review (German-language instruments) | `countries/austria.md` |
| Belgium | Third review / proof of concept for expert feedback | `countries/belgium.md` |

Belgium was chosen as a PoC because it has a dedicated federal Football Act and a dedicated stewarding royal decree — a strong comparator for how far Rec(2022)2’s model already appears in national law for football.

---

## 7. What a partner should open first

| File | What it is |
|---|---|
| `codebook/codebook.md` | The 58 duties being checked |
| `README.md` | Method, judgement rules, search protocol |
| `countries/belgium.md` | Readable Belgium findings + search table + survey questions |
| `countries/belgium.yaml` | Full audit trail: searches, evidence, all 58 lines |
| This note | Process explanation for partners |

Belgium PoC pull request: https://github.com/ds10/council-of-euro-recommendation-2022/pull/6

---

## 8. End-to-end flow (for a single country)

```
Rec(2022)2 Annex 1 + Annex 2
            |
     Codebook (58 duties)
            |
 Fixed search protocol (6 source families)
            |
 AI desk agent opens public instruments
            |
 Draft judgement per duty: status + confidence + change + source
            |
 Country brief (.md) + working record (.yaml)
            |
 Humans check: sources, weak lines, what was not opened
            |
 Survey questions for country expert
            |
 Expert confirms / corrects / supplies missing instruments
            |
 Assessment updated -> later cross-country map
```

---

*Prepared for Micheal’s team from the Rec(2022)2 national uptake review repository. Desk reviews stay in the repository; country-representative contact details do not.*
