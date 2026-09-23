# Codebook v1

Indicators for the review of Recommendation Rec(2022)2. This file is generated from [`codebook.yaml`](codebook.yaml), which is the list country files use.

An indicator is **met** when a national instrument requires the duty. The appendix offences are met when the conduct is punishable, including under general criminal law.

A survey question is asked for an indicator when the assessment is `partial`, `not_found`, or low confidence. A cluster that is `met` at high confidence is a single confirmation.

## National governance and coordination

Annex 1, articles 5–7. Cluster id `a1.governance`.

| Id | Duty |
|---|---|
| `a1.gov.committee` | A named national body coordinates safety, security and service at football matches and other sports events. |
| `a1.gov.local` | Regional or local multi-agency coordination is required for events. |
| `a1.gov.strategy` | A national strategy covers safety, security and service and is kept under review. |
| `a1.gov.roles` | The framework states the roles of the public authorities, the organiser, and the venue. |

## Venue safety duties

Annex 1, articles 8–10, 30–33. Cluster id `a1.safety`.

| Id | Duty |
|---|---|
| `a1.safety.integrated` | An integrated approach to safety, security and service is required, inside and outside the venue. |
| `a1.safety.operator` | The venue operator or organiser has explicit safety duties. |
| `a1.safety.officer` | A safety officer, or an equivalent post, is responsible for safety at the venue. |
| `a1.safety.regulations` | Venue regulations set spectator behaviour and are a condition of entry. |

## Safety certification and licensing

Annex 1, articles 11–20. Cluster id `a1.certification`.

| Id | Duty |
|---|---|
| `a1.cert.required` | A safety certificate or equivalent licence is required before designated events can be held. |
| `a1.cert.authority` | A public authority issues the certificate and can refuse or withdraw it. |
| `a1.cert.capacity` | The certificate sets a safe capacity. |
| `a1.cert.inspect` | The authority can inspect the venue. |
| `a1.cert.enforce` | Breach of the certificate can be enforced by notice, suspension, or a penalty. |

## Venue infrastructure and operations

Annex 1, articles 21–24, 31–33. Cluster id `a1.venue`.

| Id | Duty |
|---|---|
| `a1.venue.infrastructure` | Physical infrastructure is regulated, including spectator areas, access routes, and parking where the venue has it. |
| `a1.venue.segregation` | Seating and, where used, separation of supporters are regulated. |
| `a1.venue.cctv` | CCTV or an equivalent surveillance system is required at designated venues. |
| `a1.venue.operations` | The operator keeps operational arrangements and can communicate with the police and the emergency services. |

## Emergency and contingency planning

Annex 1, articles 25–29. Cluster id `a1.emergency`.

| Id | Duty |
|---|---|
| `a1.emerg.plan` | An emergency plan is required. |
| `a1.emerg.contingency` | A contingency plan is required for foreseeable disruptions. |
| `a1.emerg.evacuation` | Evacuation arrangements are required. |
| `a1.emerg.exercise` | Emergency and contingency plans are tested in exercises. |

## Venue safety service

Annex 1, articles 34–37. Cluster id `a1.safetyservice`.

Steward qualifications, powers, and training are assessed under Annex 2. These indicators ask only whether the law requires the service.

| Id | Duty |
|---|---|
| `a1.svc.required` | The law requires a venue safety service for designated events. |
| `a1.svc.stewards` | Stewards form part of that service and work under the safety officer. |
| `a1.svc.volunteers` | Any use of volunteers in the safety service is defined and limited. |

## Access, tickets and exclusion from the venue

Annex 1, articles 38–47. Cluster id `a1.access`.

| Id | Duty |
|---|---|
| `a1.access.inclusion` | Access for persons with disabilities is required. |
| `a1.access.tickets` | Ticket issue and sale are regulated, including unauthorised and counterfeit tickets. |
| `a1.access.prohibited` | Prohibited items and behaviour inside the venue are defined. |
| `a1.access.search` | Searches or inspections at entry are authorised. |
| `a1.access.expel` | Staff may refuse entry or expel a spectator, and the consequences of refusing to leave are set out. |

## Policing, risk and exclusion

Annex 1, articles 48–62, 66–68. Cluster id `a1.policing`.

| Id | Duty |
|---|---|
| `a1.police.role` | Police responsibilities at events are defined and coordinated with the organiser. |
| `a1.police.risk` | Supporters may be categorised by risk, with safeguards on how that categorisation is used. |
| `a1.police.ban` | A court or other competent authority may impose a banning order. Record any travel restriction separately in the note. |
| `a1.police.database` | A database of banned persons is kept and used by the relevant authorities. |
| `a1.police.nfip` | A national football information point, or a national sports information point, exists and can exchange police information internationally. |

## Service, dialogue and inclusion

Annex 1, articles 69–80. Cluster id `a1.dialogue`.

| Id | Duty |
|---|---|
| `a1.dial.dialogue` | Supporter dialogue is part of the arrangements, through a strategy, a charter, or an equivalent duty. |
| `a1.dial.slo` | A supporter liaison function is provided. |
| `a1.dial.dao` | A disability access function is provided. |
| `a1.dial.discrimination` | Hate speech and discrimination at events are specifically addressed. |
| `a1.dial.projects` | Fan projects, fan embassies, or community engagement form part of the service approach. |

## Sports-event offences

Annex 1, articles Appendix. Cluster id `a1.offences`.

The appendix is a set of examples. An indicator is met when the conduct is punishable under national law, including through general criminal law. The national text does not have to copy the appendix.

| Id | Duty |
|---|---|
| `a1.off.conduct` | Violence, disorder, throwing objects, and pitch invasion in connection with a sports event are offences. |
| `a1.off.staff` | Offences are aggravated, or separately provided, when committed against players, match officials, stewards, or other event staff. |

## Steward status and authorisation

Annex 2, articles 1, 6, 8, 11, Appendix 2. Cluster id `a2.status`.

| Id | Duty |
|---|---|
| `a2.status.defined` | A steward is defined as qualified safety staff of the organiser or of a contracted provider, and is distinct from the police. |
| `a2.status.qualified` | A person may act as a steward only with a qualification, licence, or professional authorisation. |
| `a2.status.vetting` | Recruitment includes a criminal-record or character check. |
| `a2.status.provider` | An in-house stewarding operation or a private provider must be authorised to recruit, train, and deploy stewards. |

## Steward duties and powers

Annex 2, articles 2–4, 9. Cluster id `a2.duties`.

| Id | Duty |
|---|---|
| `a2.duty.crowd` | Duties include crowd management, entry and exit control, and ticket checks. |
| `a2.duty.powers` | Any power to search, detain, or expel exists only where national law gives it, and is distinguished from police powers. |
| `a2.duty.emergency` | Duties include raising the alarm, basic first aid, and assisting the emergency services. |
| `a2.duty.police` | Where police are deployed, steward and police roles are agreed in advance. |

## Conduct and visibility

Annex 2, articles 5, 12. Cluster id `a2.conduct`.

| Id | Duty |
|---|---|
| `a2.conduct.code` | A written code of conduct covers courtesy, neutrality, and a prohibition on discriminatory behaviour. |
| `a2.conduct.visible` | Stewards wear high-visibility identification carrying a unique number. |

## Records and supervision

Annex 2, articles 13, 15. Cluster id `a2.records`.

| Id | Duty |
|---|---|
| `a2.records.handbook` | Stewards receive their duties in writing, including emergency and contingency arrangements. |
| `a2.records.kept` | Training, vetting, and deployment records are kept and can be inspected by the certifying authority. |

## Training and exercises

Annex 2, articles 8, 10, 14, Appendix 1. Cluster id `a2.training`.

| Id | Duty |
|---|---|
| `a2.train.initial` | Initial training is completed before deployment and covers crowd safety, evacuation, first aid, and fire safety. |
| `a2.train.ct` | Training covers counter-terrorism awareness and discriminatory or anti-social behaviour. |
| `a2.train.exercise` | Exercises of emergency and contingency plans are held and recorded. |

## Spectator service and private-security law

Annex 2, articles 3, 4, 7, 16. Cluster id `a2.service`.

| Id | Duty |
|---|---|
| `a2.svc.welcome` | Stewards have a spectator-welcome role, including support for disabled spectators and a way to report discrimination. |
| `a2.svc.law` | Steward training and deployment sit under the national private-security regime, or under a dedicated stewarding regime that states how the two fit together. |

58 indicators in 16 clusters.
