# GDPR Audit Pack - HR tech vendor

AI Act tier - high risk

## Fact pattern

Nordfracht Logistik GmbH is a mid-size logistics and freight company. It has about 1,800 employees and is headquartered in Germany, with warehouses and delivery routes across the EU. The company receives roughly 6,000 job applications per year for warehouse and driver roles, and it wants to speed up the first round of screening. The AI system reads uploaded CVs (name, contact details, work history, keyword matches) and analyzes short video interviews (recorded speech, including tone of voice). It gives each candidate a numeric score and a rank. Candidates below the cut off score get an automated rejection email, with no human involved. Candidates above the cut off go to a recruiter for interview, but in practice recruiters rarely change the AI ranking. The video analysis and scoring engine is licensed from a US based HR tech vendor, which processes the video and audio data on its own cloud infrastructure. The data subjects are job applicants, not employees or customers. Most of them are in Germany or other EU/EEA countries, though some applicants from outside the EU also apply.

**Answers to the required fact pattern questions:**

| Question | Answer |
|---|---|
| Who is the client? | Nordfracht Logistik GmbH, a mid-size logistics and freight company with about 1,800 employees, headquartered in Germany |
| What personal data is processed? | CV and resume data (name, contact info, work history, education, keywords), video interview recordings (voice, speech content, tone of voice), and the score and rank produced for each candidate. Volume is about 6,000 applicants per year. Sensitivity looks moderate at first glance, but voice and tone analysis can risk revealing special category data (see Section B) |
| Who are the data subjects? | Job applicants, not employees and not customers |
| Where are data subjects located? | Mostly in the EU/EEA (Germany and other member states), with some applicants from outside the EU |
| Who are the vendors in the stack? | A US based HR tech vendor that runs the video and audio scoring engine on its own cloud infrastructure, outside the EU |
| What does the AI system do with the data? | It reads CVs and analyzes the audio and tone of video interviews to produce a score and a rank. That rank drives an automatic rejection for candidates below the cut off |
| Is there automated decision making with legal or similarly significant effects? | Effectively yes. Rejection is fully automated for most applicants, and the human review of the shortlist is close to symbolic, since recruiters rarely override it. This still raises Article 22 concerns even though a human is nominally involved for the shortlisted group |

---

## Audit worksheet

*(Phase 2, Sections A, B and C still need to be filled in)*

### Section A - Data map

| Field | Your answer |
|---|---|
| Categories of personal data | CV data (name, contact details, education, employment history, qualifications, skills), video interview recordings, voice recordings, speech content, inferred behavioural characteristics (tone of voice), AI-generated candidate score and ranking, recruitment decisions. |
| Sources (where data comes from) | Job applicants upload CVs and record video interviews during the recruitment process. Recruiters contribute recruitment decisions. The AI system generates scores and rankings from these inputs. |
| Purpose(s), one row per purpose | 1. Recruitment administration: receive and process applications. 2. Candidate assessment: evaluate applicants and rank suitability for warehouse and driver positions. 3. Recruitment decision support: identify candidates progressing to interview and reject unsuitable applicants. 4. Record keeping: maintain recruitment records and demonstrate compliance with employment obligations. |
| Lawful basis per purpose, or `TBD, legal review` | **Recruitment administration**: Article 6(1)(b) – performance of steps prior to entering into an employment contract. **Candidate assessment**: Article 6(1)(f) – legitimate interests (TBD – Legal review/LIA required) **Automated ranking** and rejection: TBD – Legal review, due to Article 22 implications. **Record keeping**: Article 6(1)(c) – compliance with legal obligations relating to employment records and equal treatment. |
| Retention period per purpose | Recruitment records retained only for the period necessary to complete recruitment and meet applicable employment law requirements (typically 6–12 months unless litigation or consent for talent pools applies). Video recordings should be retained for the shortest practical period and deleted after recruitment concludes. |
| Recipients and sub processors | Nordfracht Logistik GmbH (controller), HR department and recruiters, US-based HR technology vendor providing AI screening (processor), cloud infrastructure provider supporting the vendor. |
| International transfers and transfer mechanism | Yes. Applicant data is transferred to a US-based processor. Appropriate safeguards such as the EU Standard Contractual Clauses (SCCs), Transfer Impact Assessment (TIA), and any applicable EU-US Data Privacy Framework participation should be verified before transfers occur. |

---
### Section B - Risk and rights

- Are any special category data present or possible to infer from the outputs (Article 9)?

Although applicants do not intentionally provide special-category data, analysing video interviews and tone of voice may reveal or infer information relating to health, disability, ethnicity, emotional state, or other protected characteristics. This creates a risk that Article 9 special-category data may be indirectly processed and requires careful assessment.

- Is there automated decision making with legal or similarly significant effects (Article 22)? If yes, what safeguard applies?

Yes. Candidates below the cut-off score receive an automatic rejection without meaningful human review. This is likely to constitute automated decision-making with similarly significant effects under Article 22 GDPR. Human review should be genuine, with authority to reconsider and override AI recommendations before rejection decisions are communicated.

- Is a DPIA required? Use the EDPB's nine criteria, explain which apply and why.

Yes. Several EDPB high-risk criteria apply simultaneously, including systematic evaluation and scoring, automated decision-making, processing of sensitive or inferable data, innovative technology (AI-based video analysis), vulnerable data subjects (job applicants), and large-scale recruitment processing (approximately 6,000 applicants annually). A Data Protection Impact Assessment (DPIA) should therefore be completed before deployment.

- What data subject friction points are most likely?

Applicants are likely to exercise the right of access to their assessment, request explanations of AI-generated scores, object to profiling, request deletion of interview recordings, or challenge automated rejection decisions. Transparency around scoring methodology will be particularly important.

- What is the controller and processor split? Name each entity and its role.

Nordfracht Logistik GmbH acts as the data controller, determining the purpose and means of recruitment processing. The US-based HR technology vendor acts as the processor, analysing CVs and video interviews on behalf of Nordfracht. Cloud providers supporting the vendor operate as sub-processors.

- Is a DPA (Data Processing Agreement) needed with any vendor? Which ones?

Yes. A comprehensive Data Processing Agreement (Article 28 GDPR) is required between Nordfracht and the US-based HR technology vendor. Any sub-processors used by the vendor should also be covered contractually.


### Section C - Law stacking (one line each)

- **AI Act cross check:**

The system would likely qualify as a High-Risk AI System under Annex III because it is used for recruitment and employment decisions. The AI Act therefore adds obligations such as risk management, human oversight, technical documentation, logging, and conformity assessment beyond GDPR requirements.

- **ePrivacy check:**

No. The scenario does not involve cookies, tracking technologies, or device-level communications. ePrivacy obligations are therefore not a primary consideration.

- **Data Act check:**

Not applicable. The scenario does not involve connected products, IoT devices, or cloud switching obligations.

---

## Client recommendation memo

To: Head of Human Resources, Nordfracht Logistik GmbH

Subject: GDPR Compliance Assessment of AI-Assisted Recruitment System

Bottom line

Go with conditions. The proposed AI recruitment system may be deployed only after significant GDPR and AI Act compliance measures are implemented. In its current form, the system presents substantial legal risks due to automated rejection decisions, processing of video interview data, and international transfers to a US-based AI provider.

The highest priority is to eliminate fully automated rejection decisions. Candidates who fall below the AI score threshold should receive meaningful human review before any rejection is issued. Recruiters must have sufficient information, authority, and time to challenge or override AI recommendations rather than simply accepting them. This is essential to reduce Article 22 GDPR risks and to meet the AI Act's human oversight expectations.

Second, conduct a Data Protection Impact Assessment (DPIA) before processing begins. The recruitment process combines systematic profiling, AI-based evaluation, video analysis, and international data transfers. The DPIA should assess risks to applicants' rights and define appropriate technical and organisational safeguards.

Third, strengthen governance around third-party processing. A compliant Data Processing Agreement should be established with the US-based HR technology vendor, together with Standard Contractual Clauses (SCCs) and a Transfer Impact Assessment where required. Privacy notices should clearly explain how candidate data is processed, how AI contributes to recruitment decisions, retention periods, and applicants' rights to access, object, or request human review.

Even after these measures are implemented, several residual risks remain. AI scoring may unintentionally disadvantage certain groups because voice analysis can indirectly reveal protected characteristics. International data transfers continue to carry legal uncertainty as transfer mechanisms evolve. Finally, applicants may continue to perceive AI-assisted recruitment as lacking transparency unless clear explanations of the scoring process and meaningful appeal procedures are provided.

This assessment represents a preliminary GDPR compliance review rather than formal legal advice. Before production deployment, the proposed controls should be reviewed by legal counsel and the organisation's Data Protection Officer to confirm compliance with both the GDPR and the EU AI Act.

---

## Reinforce

1. DPIA Outline (Data Protection Impact Assessment)

**Processing Activity**

AI-assisted recruitment involving CV screening, video interview analysis, candidate scoring, ranking, and automated rejection.

**Description of Processing**

The system processes applicants' CVs, personal details, employment history, qualifications, and recorded video interviews. Artificial intelligence analyses both structured and unstructured information, including speech characteristics and tone of voice, to generate a candidate score and ranking. Applicants below a predefined threshold receive an automated rejection, while shortlisted candidates proceed to recruiter review.

**Necessity and Proportionality Assessment**

The processing aims to improve recruitment efficiency by reducing manual review of approximately 6,000 applications per year. While AI-assisted screening may be proportionate for prioritising applications, fully automated rejection without meaningful human intervention is unlikely to satisfy GDPR requirements. The client should demonstrate that the same business objective cannot reasonably be achieved through less intrusive means and that only data necessary for recruitment is collected and processed.

**Risk Identification**

The primary risks include unfair or discriminatory outcomes caused by biased AI models, automated decisions affecting applicants' employment opportunities, indirect inference of special-category data from voice analysis, insufficient transparency regarding AI scoring, and privacy risks arising from international transfers to a US-based vendor. Applicants may also face difficulties exercising their GDPR rights if scoring logic is not sufficiently documented.

**Proposed Mitigation Measures**

Remove fully automated rejection decisions and introduce mandatory human review before rejection.
Conduct fairness and bias testing on AI outputs at regular intervals.
Minimise processing of video and voice data where possible.
Provide applicants with clear privacy information and explanations of AI-assisted decision-making.
Implement Standard Contractual Clauses (SCCs) and complete a Transfer Impact Assessment (TIA) for US data transfers.
Define retention periods and automatically delete recruitment data once it is no longer required.

2. Recommended DPA Clause

**Clause: Restriction on Secondary Use of Personal Data**

The processor shall process personal data solely for the purposes defined by the controller and shall not use applicant data, video recordings, or derived outputs for model training, product improvement, benchmarking, or any other purpose without the controller's prior written authorization.

**Reason**

This is particularly important because the vendor operates an AI-based recruitment platform. Without an explicit contractual restriction, applicant data could potentially be reused to improve AI models or develop future commercial products. Such secondary processing would likely exceed the original recruitment purpose and could violate GDPR's purpose limitation principle.

3. Revised Bottom-Line Recommendation (Including UK Data Subjects)

**Bottom line: Go with conditions.**

The recommendation remains unchanged if the client also recruits applicants in the United Kingdom. However, the organisation must now comply with both the EU GDPR and the UK GDPR, ensuring that privacy notices, applicant rights, and international transfer mechanisms satisfy both regulatory regimes. Data transfers between the UK, EU, and US should be reviewed separately, and any UK-specific guidance issued by the Information Commissioner's Office (ICO) should be incorporated into the compliance programme. Although the overall governance approach remains the same, legal review becomes more important because the organisation must demonstrate compliance under two closely aligned—but legally separate—privacy frameworks.

---

## Stretch

Mini Data Protection by Design Checklist

| Privacy by Design Principle | Current Assessment | Comments                                                                                                                                                                                   |
| --------------------------- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Data minimisation**       | **Fail**           | The system processes full CVs, video recordings, speech, and tone of voice. It is unclear whether all of these data elements are necessary for evaluating warehouse and driver candidates. |
| **Purpose binding**         | **Unknown**        | The scenario does not specify whether applicant data is technically restricted to recruitment purposes or whether the vendor may reuse data for model improvement.                         |
| **Access controls**         | **Unknown**        | No information is provided regarding role-based access controls, audit logs, or restrictions on who may access applicant data.                                                             |
| **Retention enforcement**   | **Fail**           | No automated deletion or anonymisation policy is described. Recruitment records and video interviews may therefore be retained longer than necessary.                                      |
| **Subject rights workflow** | **Unknown**        | The scenario does not describe procedures for responding to access, correction, erasure, or objection requests within the GDPR's one-month deadline.                                       |
| **Incident response**       | **Unknown**        | There is no documented breach response procedure or evidence that personal data incidents can be detected, investigated, and reported within the GDPR's 72-hour notification requirement.  |


**Overall Assessment**

The current design demonstrates several significant privacy governance gaps. The most immediate priorities are eliminating fully automated rejection decisions, introducing clear retention and deletion policies, strengthening contractual controls over the US-based processor, and establishing documented procedures for exercising data subject rights and responding to security incidents. Addressing these areas would substantially improve compliance with the GDPR's data protection by design and by default principles (Article 25 GDPR).

---

## Partner swap and peer review

**Zahra**

## Client recommendation memo

**To:** Nordfracht Logistik GmbH, HR and Legal
**Re:** AI CV and video screening tool, GDPR readiness

**Bottom line: go, with conditions.** The screening idea itself is fine under GDPR, but the current design has three gaps that need to close before it touches real applicants. The biggest one is the auto reject step, which right now has no valid legal basis for a fully automated decision.

**Top three actions, in order:**

1. **Before the tool processes any live applicant:** put a real human check in front of every rejection, not a rubber stamp. A recruiter has to actually look at borderline cases and be able to overturn the score. Without this, Article 22 blocks the auto reject flow as designed.
2. **Before go live:** complete a DPIA covering both the CV parsing and the video tone analysis. This audit already found at least six of the nine EDPB triggers, so this is not optional, and it is the right place to test whether the tone of voice feature can even infer traits like accent or a health condition.
3. **Before any video or audio data leaves the EU:** sign an Article 28 Data Processing Agreement with the US vendor and put Standard Contractual Clauses in place, backed by a transfer impact assessment. No data should flow to the vendor's US infrastructure until this is signed.

**Residual risks, even after these fixes:**

- A human review step on paper does not guarantee a human review in practice. If recruiters keep approving the AI's ranking without real scrutiny, the Article 22 exposure comes right back. This needs monitoring, not just a policy change.
- Tone of voice analysis carries a built in risk of picking up accent, speech patterns, or health related traits, and scoring people on it. A DPIA and safeguards can reduce this risk, but they cannot fully remove the chance of an indirect discrimination claim.
- SCCs and a transfer impact assessment lower the risk of the US transfer, but they cannot fully rule out government access to the data once it sits on the vendor's US infrastructure. That is a legal limit, not a gap in this company's paperwork.

One more note: this system is also high risk under the EU AI Act, which brings its own documentation and oversight duties on top of everything above. We should plan for both audits together, not one after the other.


| Criterion                                         | Score (1–3) | Comment                                                                                                                                                                                                          |
| ------------------------------------------------- | :---------: | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Clear bottom-line recommendation**              |    **3**    | The recommendation ("Go, with conditions") is immediately clear and consistently supported throughout the memo.                                                                                                  |
| **Lawful basis selection is justified**           |    **2**    | The memo correctly identifies Article 22 as a key issue but does not discuss or justify the lawful basis for processing (e.g., legitimate interests, contract, or legal obligation). This could be strengthened. |
| **Top actions are specific and sequenced**        |    **3**    | The actions are concrete, ordered by priority, and clearly linked to implementation milestones before deployment.                                                                                                |
| **Residual risks are named honestly**             |    **3**    | The memo realistically acknowledges that human review, bias mitigation, and international transfer safeguards reduce—but do not eliminate—risk.                                                                  |
| **Law stacking is addressed (AI Act / ePrivacy)** |    **3**    | The interaction between GDPR and the EU AI Act is explicitly recognised. ePrivacy is not applicable to this use case, which is appropriate.                                                                      |


**Client Response**

Thank you for the assessment. We agree that introducing meaningful human review and completing a DPIA should be our immediate priorities before deployment. Our main concern is the recommendation to remove fully automated rejection, as this may reduce the efficiency gains we expected from the system. Could you advise whether there is a compliant way to retain some level of automation while still meeting the requirements of Article 22 GDPR?

**Consultant Response**

Thank you for raising this concern. We agree that automation is an important business objective, and the GDPR does not prohibit the use of AI in recruitment. The key issue is not the use of AI itself, but whether a candidate is subject to a decision based solely on automated processing that has a significant effect, such as an automatic rejection.

A compliant approach would be to retain AI for screening and prioritisation, while introducing meaningful human oversight before any rejection is communicated. For example, the AI could automatically rank applicants into categories (e.g., high priority, review required, low priority), but a recruiter should review candidates in the lower categories before making the final decision. The reviewer should have access to the candidate's application, understand the reasons behind the AI score, and have the authority to disagree with or override the recommendation. This preserves much of the efficiency benefit while significantly reducing Article 22 GDPR risk.

As part of the DPIA, we also recommend evaluating whether the automatic rejection threshold can be replaced with a risk-based workflow. In many organisations, this hybrid approach achieves a good balance between operational efficiency, fairness, and legal compliance. We would be happy to help design a review process that minimises manual effort while remaining compliant with GDPR and the EU AI Act.