# National uptake of Recommendation Rec(2022)2

**Start with the [United Kingdom review](countries/united-kingdom.md).** It is the first completed country file. Read it from the top. The topic sections are the findings. The table at the end is the same findings, one line per duty.

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

The codebook is version 1: [`codebook/codebook.md`](codebook/codebook.md), generated from [`codebook/codebook.yaml`](codebook/codebook.yaml). It has 16 clusters and 58 indicators, taken from Annex 1 and Annex 2.

- A **cluster** is a heading in the country brief and in the survey.
- An **indicator** is one duty inside a cluster. Certification, for example, is five indicators: a required certificate, a named authority, a safe capacity, inspection, and enforcement.

Article numbers on each cluster point back to the recommendation. The appendix of criminal offences is illustrative: those indicators are met when the conduct is punishable under national law, including under general criminal law.

A survey question is asked for an indicator when the finding is `partial`, `not_found`, or low confidence. A cluster that is `met` at high confidence is one confirmation.

The first sketch of headings is in [`background/first-topic-list.md`](background/first-topic-list.md). That file is background only. The country table in it is the original sketch and is left unchanged.

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

1. **Codebook v1.** In place. Revise an indicator only when a pilot shows it is too wide to judge or too narrow to be worth a question.
2. **Pilot.** The United Kingdom review is written. England and Wales, Scotland, and Northern Ireland are kept distinct where their regimes differ. The second pilot is a State Party with little of the framework available in English, chosen when the party list is taken from the treaty chart, so an empty search is tested as well.
3. **Desk review.** One country file per remaining State Party, copied from [`countries/_template.yaml`](countries/_template.yaml).
4. **Survey.** Send the pre-filled questions. File the replies against the same indicators.
5. **Overview.** Update the assessments from the replies and write the cross-country map.

The working audience is the people carrying out the review. Country briefs are written so they can be sent on to a country representative. The overview stays in this repository.

A finding based on a text the reviewer cannot read is recorded at low confidence. Country-representative names and emails are not part of the desk review. The survey tool can be chosen when the pilot questions exist. The questions are drafted here either way.

## Rules in force

- **Scope.** States Parties to CETS No. 218. The country list is a dated snapshot of the [treaty chart](https://www.coe.int/en/web/conventions/full-list/-/conventions/treaty/218), taken when the second pilot is chosen. At its meeting of 3–4 June 2025 the Committee welcomed Serbia as the 31st State Party. The snapshot for this review is taken from the chart, not from that meeting note.
- **Cut-off.** 1 September 2022, the date the Committee adopted the recommendation.
- **Scale and instruments.** The status, confidence, and change fields above.
- **Storage.** Citations, links, and short paraphrases. Contact details of officials are left out of the country files.

## Status

Codebook v1 is in [`codebook/`](codebook/). The [United Kingdom review](countries/united-kingdom.md) is the first assessment. The country template for the next file is [`countries/_template.yaml`](countries/_template.yaml).

```
codebook/
  codebook.yaml
  codebook.md
countries/
  united-kingdom.md    the review to read
  united-kingdom.yaml  the same judgements, in the working record
  _template.yaml
sources/
  Rec-2022-2-model-national-legislative-and-regulatory-framework.pdf
background/
  first-topic-list.md
README.md
```
