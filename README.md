# National uptake of Recommendation Rec(2022)2

This repository is the review of how far countries have reflected [Recommendation Rec(2022)2](sources/Rec-2022-2-model-national-legislative-and-regulatory-framework.pdf) in national legal, regulatory, and administrative frameworks, and what has changed since it was adopted.

The recommendation was adopted by the Committee on Safety and Security at Sports Events (T-S4, the Saint-Denis Committee) by written procedure on **1 September 2022**. The English text is dated Strasbourg, 5 October 2022. It is addressed to governments of Parties to the Council of Europe Convention on an Integrated Safety, Security and Service Approach at Football Matches and Other Sports Events (CETS No. 218, the Saint-Denis Convention).

It asks those governments to:

1. Adopt or refine a **national law** on safety, security and service at football matches and other sports events, based on the model in **Annex 1**.
2. Adopt or refine a **national regulation on stewarding**, based on the model in **Annex 2**.

The recommendation is a model to adapt. Its introduction says a single statute for every country is neither possible nor desirable. This review therefore maps **equivalent national rules** on the same topics. An explicit citation of Rec(2022)2 is recorded when a source contains one. The result is a sourced map of coverage and of change since 1 September 2022.

Rec(2022)2 is the model law and the stewarding regulation. Rec(2022)1, adopted the same day, is the model structure of a national strategy and is outside this review. Public background is on the [Council of Europe T-S4 recommendations page](https://www.coe.int/en/web/sport/t-s4-recommendations). The authoritative party list is the [treaty chart for CETS No. 218](https://www.coe.int/en/web/conventions/full-list?module=treaty-detail&treatynum=218).

## What the repository holds

The repository is the record. Each claim about a country points at a source, and the git history shows who entered it and when.

| Record | What it is |
|---|---|
| Codebook | The topics every country is checked against. Shared, versioned, and the same for the desk review, the country briefs, and the survey. |
| Search log | The sources checked for a country, including checks that found nothing. |
| Evidence | The instrument: title, citation, link, date, language, and which codebook items it speaks to. A short paraphrase. The text of the instrument stays in the official source. |
| Assessment | For each country and each codebook item: status, confidence, what changed since 1 September 2022, and the evidence used. |
| Country brief | A short narrative for that country: the current framework, and what has changed since 1 September 2022. |
| Survey | Questions generated from the assessment, sent to the country representative, with replies written back into the same assessment. |

Country representatives receive a prepared brief and are asked to confirm it, correct it, or supply a missing instrument. The desk review stays in this repository.

## Codebook

Annex 1 and Annex 2 are the source of the topics. The codebook has two levels.

- A **cluster** is a heading in the country brief and in the survey. Clusters follow the main blocks of the two annexes: governance, safety duties, certification, venue infrastructure, emergency planning, the safety service, access and inclusion, policing and exclusion, supporter dialogue and service, illustrative criminal offences, and the stewarding blocks in Annex 2 (status, duties, conduct, records, training, supporter-facing roles).
- An **indicator** is one distinct duty inside a cluster, small enough that a search can hit it or miss it. Certification, for example, splits into a required certificate, a named authority, inspection powers, and sanctions, rather than one yes-or-no for the whole annex.

Related articles are grouped into one indicator. The article numbers remain on the indicator as a pointer back to the recommendation. The first sketch of cluster headings is in [`background/first-topic-list.md`](background/first-topic-list.md). That file is background only. The country table in it is the original sketch and is left unchanged.

## How a country is judged

Each indicator gets one status:

| Status | Meaning |
|---|---|
| `met` | A national instrument requires the substance of the indicator for football matches or other sports events in scope. |
| `partial` | The instrument covers only part of the indicator, applies only to some events, or recommends the duty without requiring it. |
| `not_found` | The search protocol for that country was completed, and no such instrument was identified. |
| `not_applicable` | The indicator cannot apply. The assessment says why. |

Statute, regulation, and a licensing condition that a venue must meet can all be `met`. A football-association rule, a ministry circular, or another administrative instrument can be `met` when it is the instrument that actually imposes the duty. A strategy, charter, or guidance note that only recommends the duty is `partial`.

Each judgement also records:

- **Confidence:** `high`, `medium`, or `low`. A judgement on a text the reviewer could not read is `low` until a reader of that language, or the country representative, confirms it.
- **Change since 1 September 2022:** `new`, `amended`, `unchanged`, or `unknown`. The country brief states the current rule and what changed. The baseline is the framework that those changes amended.

## Search protocol

The same source families are checked for every country, and each check is written in the search log, including an empty result.

1. The national legislation database or official gazette.
2. The ministry responsible for sport, and the authority responsible for policing sports events.
3. The stadium licensing or safety-certification authority.
4. The national football association’s safety and stadium rules.
5. The national football information point, or the body that carries that function.
6. A direct search for `Rec(2022)2`, the Saint-Denis Convention, and CETS No. 218.

Searches use the indicator wording and the national-language terms for that duty. A citation of the recommendation is logged when it appears. Coverage is judged from the national instrument.

## Country brief and survey

The brief for a country has five parts: party status and the date of the assessment; how safety, security, and service are organised; what has changed since 1 September 2022; the indicator table with sources; and the gaps.

The survey is built from that file. Each question restates the finding (“We found this instrument. It appears to meet / partially meet / not address this indicator.”) and asks the representative to confirm it or to name the instrument that should replace it. One open question asks what has changed since 1 September 2022 that the brief missed. Replies use the same indicator identifiers, so they update the assessment and can be compared across countries.

The cross-country product is a map: by indicator, how many countries are `met`, `partial`, or `not_found`, and where the framework is new or amended since 1 September 2022. It describes the sourced material.

## How the work proceeds

1. **Codebook v1.** Write the clusters and indicators from Annex 1 and Annex 2, with the national-language search terms left blank until a country file needs them.
2. **Pilot.** Run the full protocol, the brief, and a draft survey on two countries. Revise the codebook where an indicator was too wide to judge or too narrow to be worth a question.
3. **Desk review.** One assessment file and one brief per remaining country, using the revised codebook.
4. **Survey.** Send the pre-filled questions. File the replies against the same indicators.
5. **Overview.** Update the assessments from the replies and write the cross-country map.

The pilot is what makes the later survey short. Indicators that cannot be judged from real documents get rewritten before anyone is asked to answer them.

## Rules in force

These are the project rules. Change them before the first country assessment if they should be different.

- **Scope.** States Parties to CETS No. 218. The country list is a dated snapshot of the treaty chart, frozen when the codebook is first used. At its meeting of 3–4 June 2025 the Committee welcomed Serbia as the 31st State Party; the snapshot for this review will be taken from the chart at the time the list is frozen, not from that meeting note.
- **Cut-off.** 1 September 2022, the date the Committee adopted the recommendation.
- **Scale and instruments.** The status, confidence, and change fields above.
- **Storage.** Citations, links, and short paraphrases. Officials’ contact details are stored only if this repository is an acceptable place for them.

## What has to be in place before the first country file

The method can run as soon as the following are settled. Nothing else needs to be installed. This repository is the working system.

1. **Confirm the scope, the cut-off, and the judgement rules**, or say what to change.
2. **Name the audience** for the overview and the country briefs, and say whether those documents can live in this repository.
3. **Name two pilot countries**, and say which languages the people doing the desk review can read. The pilot should include one country whose stadium-safety instruments are already easy to find in a language the reviewer reads, and one where the material is likely to be thinner, so an empty search and the survey questions are tested as well.
4. **Say who may be named.** Country-representative names and emails can wait until the survey. The desk review does not need them.
5. **Choose the survey tool** the organisation is allowed to use, before the survey is sent. The questions are drafted here either way.

## Status

The recommendation text is in [`sources/`](sources/). The codebook, the search log, and the country files are not started. No country has been assessed in this repository.

```
sources/
  Rec-2022-2-model-national-legislative-and-regulatory-framework.pdf
background/
  first-topic-list.md
README.md
```
