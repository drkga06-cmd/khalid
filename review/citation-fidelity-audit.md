# Scientific Citation and Evidence Fidelity Audit

**Course:** EMDR with Complex Trauma and Structural Dissociation (EMDR ARABIA, 4 days, handoff package of 26 September 2026)
**Audit date:** 26 September 2026
**Status:** AI-assisted audit. It checks claims against the supplied full texts and against published research found by web search. It is not a substitute for review by the course director or an independent subject expert.

---

## 1. Bottom line

The book citations are accurate. Where the problems exist, they are about **evidence strength**, not about whether a source says something.

- **Locators check out almost everywhere.** About 150 book claims were traced to the supplied full texts. More than 140 were found at the cited chapter or page, most of them close to verbatim. Two citation errors were found (F-05, F-06).
- **Earlier defects are fixed.** Three defects from the 24 September review are resolved in this package:
  - IHD is now correctly cited to Knipe (2019) ch. 14.
  - The RDI evidence statement now matches Leeds.
  - The suicide-risk wording now sets NICE NG225 and Franklin et al. (2017) against the "strongest predictor" claim.
- **The main weakness is asymmetric evidence labelling.** Flash is the only specialist procedure given an evidence caveat. CIPOS, Loving Eyes, IHD and LOUA/LOPA are taught with the same authority, yet their evidence is the developer's case material, plus one laboratory pilot for CIPOS.
- **Phase-oriented treatment for DID reads as settled on the slides.** Stabilization before memory work for dissociative disorders is stated as a rule on the slides and in the "basic training" recap. The guide itself is more careful ("weak outcome evidence either way"). Research published since the books (2022–2026) is not reflected.
- **Three live scientific debates are not mentioned anywhere:**
  - the experimental evidence on inter-identity amnesia;
  - the trauma-model versus sociocognitive-model debate on the origins of DID;
  - the unresolved mechanism of EMDR, including the "not exposure therapy" claim.
- **A few clinical heuristics read as findings.** The clearest case is Leeds's "more than 50% of the time" rule of thumb, which the guide presents as a result.

No finding shows the course teaching something its sources contradict. The corrections needed are about certainty, attribution and omitted context.

---

## 2. Scope and method

### What was audited

| Material | Coverage |
|---|---|
| `guide/guide.md` (English theoretical guide, 14 chapters, 30 references) | Read in full. Every book citation checked against `src/` |
| 100 theory-depth speaker notes (`sample/theory_d1–d4.js`) | Read in full. Book claims spot-checked, with a focus on quotations, numbers and case examples |
| 312 slides plus base speaker notes (Days 1–4, extracted from `sample/dN_v2.js`) | Read in full |
| Pre/post test and answer key (`man1/build_wb.py`) | All 12 items and rationales |
| Participant manuals, Modern Standard Arabic and colloquial (`man1/pm*.py`) | Every citation string extracted and checked |

### How claims were checked

- **Books:** the full texts supplied in `src/` (TTRD, *Haunted Self*, Leeds 2016, Knipe 2019, *Coping*). Page markers in the Knipe text were mapped automatically (309 pages). Leeds, TTRD, HS and *Coping* were mapped by chapter using the line offsets in the README.
- **External studies and guidelines:** checked by web search. Research sites (PubMed/PMC, NICE, WHO ICD browser, ScienceDirect, Crossref) cannot be reached from this environment, so these checks rest on abstracts and search summaries, not full texts. Each external verdict below says so.

### Not audited

- **Arabic translation fidelity.** `msa.md` and `col.md` were not compared line by line with `guide.md`.
- **Full text of the trainer manuals and workbooks.** Only their citation strings were checked.
- **Visual rendering.**
- **Primary texts that were not supplied:** the ICD-11 CDDR, the DSM-5-TR, Shapiro (2018), the ISSTD (2011) guidelines, and the Carlson papers.

### Rating key

| Code | Meaning |
|---|---|
| **S** | Supported: the source says it, at the same strength |
| **OS** | Overstated: said more strongly or more generally than the source or evidence allows |
| **CE** | Citation error: wrong source, chapter or page, or wrong metadata |
| **TF** | Theory presented as established fact |
| **OP** | Clinical opinion or heuristic presented as research evidence |
| **OM** | Omission: material uncertainty, controversy or newer evidence left out |
| **OD** | Outdated: matches the source, but later evidence qualifies it |

Severity: **High** (misleads trainees about the evidence base for a clinical decision) · **Medium** (misleads on certainty or attribution) · **Low** (precision or metadata).

---

## 3. Findings

Ranked most severe first. Locations use D = day and S = slide number in the built deck. Theory notes are labelled by day and order, for example D4-13.

### High

**F-01. The evidence status of the Knipe procedures is not stated, while Flash's is.** Codes: OM, OP.

- **Where:** Guide ch. 13; slides D4S48–S53; theory notes D4-13, D4-16, D4-17; D2S27 (LOUA/LOPA).
- **What the course does:** Flash carries an explicit caveat: "evidence still limited", one RCT, no systematic review. CIPOS, Loving Eyes, IHD and LOUA/LOPA are presented with purpose, indications, preconditions and limits, but no evidence grade. A trainee will reasonably infer that these are better established than Flash.
- **The evidence:**
  - **Loving Eyes and IHD:** Knipe's own case examples (Knipe, 2019, chs. 11 and 14–17).
  - **CIPOS:** Knipe's case experience ("From my own experience, and many reports from colleagues", Knipe, 2019, p. 243), plus one laboratory pilot in 30 healthy volunteers ([Stingl et al., 2022, *Frontiers in Psychology*](https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2022.1035371/full)).
  - **Clinical trials:** the search found none in dissociative clients for any of the four procedures. This is abstract-level; absence was not exhaustively confirmed.
- **Fix:** Add one evidence line per procedure in guide ch. 13 and in the D4S48–S53 notes. For example: "developer case series; no controlled clinical trials; one laboratory study in non-clinical volunteers (CIPOS)." Use the same template as Flash.

**F-02. Phase-oriented treatment for dissociative disorders is stated as a rule; the guide's nuance and post-2016 evidence do not reach the slides.** Codes: OS, OM, OD.

- **Where:** Slide D1S4 ("with dissociative disorders, sufficient stabilization precedes memory work", presented as a basic-training rule); D3S65 ("sufficient stabilization is a condition before memory work"); theory notes D2-20, D3-20; guide ch. 7.
- **What the sources say:**
  - TTRD (ch. 20) is accurately quoted: "there is not sufficient evidence at present to demonstrate that stabilization is unnecessary in dissociative disorders." That is an absence-of-evidence argument by the model's originators. It is not evidence that stabilization is necessary.
  - The ISSTD guidelines cited are the 2011 third revision. No later revision was found ([ISSTD adult guidelines page](https://www.isst-d.org/publications-resources/resources-for-professionals/adult-treatment-guidelines/)).
  - The only RCT in DID and OSDD-1, a 20-session group built on *Coping*, found no between-group difference ([Bækkelund et al., 2022](https://pubmed.ncbi.nlm.nih.gov/35578194/)).
  - A 2025 review states that practice-based, phase-based psychodynamic treatment of DID shows small effects on dissociative symptoms. It reports large preliminary effects from newer approaches, including schema therapy with early, graded trauma processing, which explicitly does not use a phase-based structure ([Bachrach & Huntjens, 2025, *Frontiers in Psychiatry*](https://www.researchgate.net/publication/395818435_Recent_evidence-based_developments_in_the_treatment_of_DID)).
- **Assessment:** Guide ch. 7 ("weak outcome evidence either way") is a fair statement. The slides are not; they present the phase rule as settled.
- **Fix:**
  - Label D1S4 and D3S65 as "the specialist consensus (ISSTD 2011; TTRD), with weak outcome evidence."
  - Add the 2025 review to guide ch. 7 and to the references.
  - Keep the task-specific readiness question, which the course already teaches well, as the operative rule.

### Medium

**F-03. Inter-identity amnesia is treated as established; the experimental evidence is not mentioned.** Code: OM.

- **Where:**
  - Guide ch. 2: "depth of amnesic barriers" as the criterion that separates secondary from tertiary dissociation.
  - Guide ch. 11: "not all parts have access to a given memory."
  - Theory note D1-23; D2S9 notes.
- **The evidence:**
  - Controlled studies by Huntjens and colleagues (from 2002 onward) repeatedly find objective transfer of information between identities, despite self-reported amnesia ([review: "Interidentity amnesia in dissociative identity disorder", *Cognitive Neuropsychiatry*, 2017](https://www.tandfonline.com/doi/abs/10.1080/13546805.2017.1327848)).
  - A 2024 meta-analysis found transfer when DID patients were compared with simulators, but patterns consistent with amnesia when identities were compared within patients. It concluded that "methodological limitations hinder theoretical conclusions" ([Beker, Dorahy et al., 2024, *Clinical Psychology Review* 114:102514](https://pubmed.ncbi.nlm.nih.gov/39541721/)).
- **Why it matters here:** The clinical guidance, which is to ask directly about self-harm the client may not remember, stays valid, because *subjective* amnesia is what the clinician works with. The theoretical claim should be framed as reported or subjective amnesia.
- **Fix:** Add one paragraph to guide ch. 2 and one sentence to the D1-23 note.

**F-04. The debate over the origins of DID is omitted.** Code: OM.

- **Where:** Guide chs. 1–2; slides D1S37–S46.
- **The issue:** The course teaches the trauma model (structural dissociation) as its framework, which is a legitimate choice. But it never tells trainees that the origins of DID are contested. On one side is the trauma model ([Dalenberg et al., 2012, *Psychological Bulletin*](https://pubmed.ncbi.nlm.nih.gov/22409505/)). On the other is the sociocognitive model, which adds suggestion, media and iatrogenesis ([Lynn et al., 2014](https://pubmed.ncbi.nlm.nih.gov/24773505/)). Integrative positions have since been proposed (["Beyond sociocognitive and trauma models", *Annual Review of Clinical Psychology*](https://www.annualreviews.org/content/journals/10.1146/annurev-clinpsy-081219-102424)).
- **Why it matters:** The course already teaches the right defence against iatrogenesis: non-leading descriptive questions (1.4), no naming of parts, and TTRD's imitative-DID warning signs. Naming the debate would explain why those habits exist.
- **Fix:** Add a short box in guide ch. 1 or ch. 5 and one sentence in the D1S59 or D1S71 notes.

**F-05. The "three levels" slide cites a book that does not contain the model, and maps ICD-11 CPTSD onto it without a label.** Codes: CE, TF.

- **Where:** Slide D1S43 (source tag "TTRD"): primary = PTSD; secondary = CPTSD and partial DID; tertiary = DID.
- **The citation error:** A full-text search of TTRD finds no occurrence of "tertiary", "secondary structural" or "primary structural". The three levels come from *The Haunted Self* (Introduction table; chs. 2–4) and Leeds (ch. 5).
- **The unlabelled extrapolation:**
  - HS places "Complex PTSD / DESNOS" and DDNOS at the secondary level. Applying that to ICD-11 CPTSD is the course's own update of the mapping. Theory note D1-22 says so correctly; the slide does not.
  - D1S29 labels the spectrum as "the model's view"; D1S43 carries no such label.
- **Fix:** Change the source tag to "HS (2006); Leeds ch. 5". Add "model's mapping, updated from DSM-IV terms" to the slide.

**F-06. The participant manuals cite the wrong Leeds chapter for the RDI evidence statement.** Code: CE.

- **Where:** `man1/pm3_msa.py` and `man1/pm3_col.py`, line 42: "(Leeds, 2016, chs. 8 and 9)".
- **The source:** The statement "there is as yet no high-quality controlled research published on the full RDI protocol" is in Leeds, ch. 6 (`leeds.txt` line 6277). Chapters 8–9 deal with desensitization. The slide (D3S32) and the guide cite ch. 6 correctly.
- **Fix:** Change the locator to ch. 6 in both files, then rebuild.

**F-07. A training heuristic is presented as a quantitative finding.** Code: OP.

- **Where:** Guide ch. 12: "change the bilateral stimulation first; this alone restores processing in more than half of cases (Leeds, 2016, ch. 8)."
- **The source:** Leeds, ch. 8: "As you are learning to use EMDR therapy, remember that more than 50% of the time, merely changing the characteristics of the BLS will be enough." No study is cited, and the surrounding rationale leans on speculation about limbic mechanisms (Servan-Schreiber, 2004).
- **Fix:** Rephrase as "Leeds's rule of thumb for trainees is that changing the stimulation alone often restores processing (he says more than half the time; no data are given)."

**F-08. Contested mechanistic claims are presented as settled.** Codes: TF, OM.

- **Where:** Guide ch. 12 ("Leeds is clear that EMDR is not exposure therapy … processing at some distance does better than vivid reliving"); theory note D4-3; guide ch. 11 (AIP as the account of how EMDR works); slide D3S6 notes.
- **The source:** Leeds attributes this correctly, but it rests on two small studies (Lee et al., 2006; Lee & Drummond, 2008). How EMDR works is unresolved. The working-memory taxation account has the largest body of laboratory support. AIP is a clinical model that has not been directly tested. The APA practice guideline Leeds himself quotes treats EMDR as an exposure variant. A systematic review of 87 mechanism studies did not settle the question (Landin-Romero et al., 2018; found by search, not opened).
- **Fix:** Present both as positions: "Leeds argues … ; others classify EMDR as a trauma-focused therapy with exposure elements; the mechanism is not established."

**F-09. The source's evidence claim for the symptom-informed target model is repeated without qualification.** Code: OS.

- **Where:** Guide ch. 11 ("the target-sequencing model for PTSD with support from controlled research"); theory note D3-16.
- **What Leeds actually says (ch. 4):** The model "was used for" the van der Kolk et al. (2007) RCT, which compared EMDR, fluoxetine and placebo. That trial did not compare sequencing strategies. The other support Leeds cites is two conference sources, one of them his own (Korn, Weir & Rozelle, 2004; Leeds, 2004). Leeds is also the model's author.
- **Also:** The rationale for starting with the earliest memory, that it lowers the risk of earlier material being triggered outside awareness, is theoretical.
- **Fix:** "Leeds's model, used as the targeting approach in one RCT of EMDR for PTSD; sequencing itself has not been compared experimentally."

**F-10. The course's theory rests mainly on the model developers' own books, and this is not flagged.** Codes: OM (source appropriateness).

- **The pattern:**
  - TTRD, *The Haunted Self* and *Coping* share authors. They are the originators of the structural dissociation theory and of the stabilization curriculum.
  - Knipe is the source for his own procedures.
  - Leeds co-developed RDI and wrote the rebuttal to the laboratory study that challenged it (Hornsveld et al., 2011); the guide notes this rebuttal fairly.
- **Why it matters:** This is normal for a clinical training course. But it means "the sources agree" often amounts to "the developers agree."
- **Fix:** Add one sentence to the guide's "Sources" section saying this, and add one independent review per contested topic. Candidates: the 2025 DID treatment review (F-02), the 2024 meta-analysis of inter-identity amnesia (F-03), and the Dalenberg and Lynn exchange (F-04).

**F-11. Hoeboer et al. (2020) is applied to the whole spectrum without its sampling limits.** Codes: OS, OD.

- **Where:** Theory note D1-15 ("the spectrum tells us how cautious to be, not who can be treated"); guide ch. 7.
- **What the study showed:** Across 21 studies, dissociation did not moderate the outcome of psychotherapy for PTSD. The authors note that study quality was low in several of them ([Hoeboer et al., 2020](https://www.cambridge.org/core/journals/bjpsych-open/article/impact-of-dissociation-on-the-effectiveness-of-psychotherapy-for-posttraumatic-stress-disorder-metaanalysis/E685776A001999072BC8F8E3FA259CBB)). The samples were PTSD samples, not people with DID or partial DID. The course cannot use the study to speak to the dissociative-disorder end of its own spectrum.
- **Newer evidence:** A 2026 meta-analysis of 13 controlled trials found a small effect of current trauma treatments on dissociation itself (g = −0.28) ([Akoral et al., 2026, *Journal of Trauma & Dissociation*](https://pubmed.ncbi.nlm.nih.gov/41830109/)).
- **Fix:** Add "in PTSD samples; dissociative disorders largely not represented; study quality mixed". Add the 2026 meta-analysis to guide ch. 7.

**F-12. A causal conclusion is drawn from two case anecdotes.** Code: OS.

- **Where:** Theory note D1-16: "in both cases the missed diagnosis caused the problem, not EMDR itself."
- **The sources:** Leeds (chs. 3 and 6) and TTRD (ch. 5, the case of "Bob") describe the cases accurately. Neither states the exonerating conclusion. Two anecdotes cannot separate the effect of the missed diagnosis from the effect of the procedure.
- **Fix:** "Both authors use these cases to argue for screening before any bilateral stimulation."

### Low

| ID | Location | Issue | Code | Fix |
|---|---|---|---|---|
| F-13 | Test key, Q6 rationale; slide D1S73 body | The rationale says "previous attempts are among the strongest indicators" and gives no NICE qualification. The slide body has the same bullet; the qualification is only in the notes. D2S8 already carries it | OD | Add "but no single factor predicts accurately (NICE NG225)". NICE wording confirmed ([NG225 recommendations](https://www.nice.org.uk/guidance/ng225/chapter/Recommendations)) |
| F-14 | Guide ch. 13 (CIPOS "rationale") and theory note D4-4: "stimulation loosens dissociative barriers" | Knipe (p. 236) cites Paulsen (1995), a clinical observation. No experimental evidence is given | OP | "Knipe, following Paulsen, holds that …" |
| F-15 | Guide ch. 4, citing Knipe p. 60: working on a defense first lowers the risk of dissociative abreaction | Knipe's words are "It has been my impression that …" | OP | Add "in Knipe's clinical impression" |
| F-16 | Theory note D2-20 ("ISTSS paper 2019"); `refs.md` ("n.d.") | The ISTSS adult CPTSD position paper was published in November 2018. The note also puts Karatzias & Cloitre (2019) in the source line for the ISTSS paper's position; they are separate papers | CE | Date the paper 2018 and cite it separately from Karatzias & Cloitre |
| F-17 | Slide D1S71: "TADS-I (Boon & Matthess)"; "structured diagnostic interviews" | `refs.md` lists only Boon (2023). SCID-D and TADS-I are semi-structured; the guide gets this right | CE | Align the slide attribution with `refs.md`; change "structured" to "semi-structured" |
| F-18 | Guide, "The sources" section | It promises that "the 2011 article is cited instead" for HS's revised definition, but no 2011 article is in the references and none is cited | CE | Add the reference, or remove the sentence |
| F-19 | Guide ch. 12, two citations of "(Leeds, 2016)" with no chapter | "Slow is not stuck" is ch. 8 (line 7431). The warning about intervening because of one's own affect tolerance is ch. 9 (lines 7765 and 7841). Project rule 5 requires a chapter | CE | Add the chapters |
| F-20 | Guide ch. 5; slide D1S70; theory note D1-31: DES figures | The numbers are correct: at a cutoff of 30, sensitivity 74% and specificity 80% for MPD ([confirmed via the Carlson update](https://scholarsbank.uoregon.edu/server/api/core/bitstreams/28b2dc3b-66c3-4b4e-b05f-efe842ee473f/content)). But they come from the multicenter study (Carlson et al., 1993, *Am J Psychiatry* 150:1030–1036), not only from the update paper. The 17% figure depends on an assumed base rate. The validation sample was DSM-III-R MPD, so sensitivity for partial DID or OSDD was not established | CE, OM | Add the primary reference; add "at the prevalence the authors assumed; validated for DID/MPD only" |
| F-21 | Guide ch. 7; theory note D2-13: Bækkelund (2022) "functioning improving in both arms" | Within-group change to the end of treatment was non-significant in both arms. Improvement appeared over the 6-month follow-up | OS | "Both arms improved over follow-up; no between-group difference" |
| F-22 | Slide D3S51: "then in chronological order" | Leeds (ch. 4), cited in the same unit and in theory note D3-16, gives earliest, then worst, then most recent. Shapiro (2018) was not supplied, so the basic-training wording could not be checked | CE | Align with Leeds, or cite the source of the chronological rule |
| F-23 | Guide ch. 3 | "The book is not fully consistent in how it distinguishes 'mental level' from 'mental efficiency'" is the guide author's own judgment, with no source | OP | Mark it as the guide's reading |

---

## 4. The eight audit questions

| # | Question | Answer from this audit |
|---|---|---|
| 1 | Does the cited source contain the claim? | Yes, in almost every case. Exceptions: F-05 (TTRD), F-06 (Leeds chs. 8–9), F-18 (missing reference) |
| 2 | Same strength? | Mostly. Stronger than the source or the evidence: F-02, F-07, F-09, F-11, F-12, F-21 |
| 3 | Right purpose? | Mostly. Misused: F-11 (a PTSD-sample meta-analysis used for the DID end of the spectrum); F-16 (Karatzias & Cloitre cited for the ISTSS paper) |
| 4 | Appropriate source type? | Adequate for a clinical course. Heavy reliance on the model developers' own books is not disclosed (F-10) |
| 5 | Consistent with current evidence? | Not fully. Post-2016 and 2022–2026 work on DID treatment, inter-identity amnesia and treatment effects on dissociation is missing (F-02, F-03, F-11) |
| 6 | Uncertainty omitted? | Yes: F-01, F-03, F-04, F-08 |
| 7 | Theory presented as fact? | F-05 (unlabelled level-to-diagnosis mapping); F-08 (AIP and "not exposure"). Elsewhere the course labels the model well (D1S29; guide ch. 1: "a model, not a classification") |
| 8 | Clinical opinion presented as evidence? | F-01, F-07, F-14, F-15, F-23 |

---

## 5. Verified as accurate (selected)

**Knipe (2019, 2nd ed.).** Every page citation in the guide was checked, and all hold:

| Pages | Claim |
|---|---|
| 51–54 | Definition of defense; positive affect of defense |
| 56, 75–76 | "It is not about fear, but about relief" |
| 98, 103–104 | Idealization defenses |
| 110–112 | LOPA "not a rote formulaic procedure" |
| 125–127 | Addiction memory |
| 159, 161–162 | Parts as extreme adaptations |
| 177 | EMD-like tightening of focus |
| 180–181 | "Slow is fast"; resource installation as a "platform" |
| 211–215 | Loving Eyes steps; "dissociative cliff"; the "too much / too little" indications |
| 235–244 | CIPOS; Back of the Head Scale; the 2-second limit; "carefully controlled dissociative process"; Manfield's Flash safety caveat |
| 247–254 | IHD |

IHD is correctly placed in ch. 14 of the 2nd edition, which resolves the earlier review's finding F-02.

**TTRD.** All of these are verbatim or close:

| Chapter | Claim |
|---|---|
| ch. 5 | Blatant switching in "about 5–6% of cases of DID" |
| ch. 5 | Tigers and mammals (after Kluft) |
| ch. 5 | Hypnosis and EMDR ego states do not by themselves indicate a dissociative disorder |
| ch. 5 | "Cookbook answers" |
| ch. 11 | "Resistance is perhaps best conceptualized as phobic avoidance of what the patient believes is too overwhelming to realize" |
| ch. 11 | Consider ongoing abuse when a client does not improve |
| ch. 12 | "As slow as the slowest part" |
| ch. 18 | 60% amnesia around self-injury (Coons & Milstein, 1990) |
| ch. 18 | "It is the patient as a whole who is ultimately responsible" |
| ch. 20 | The readiness capacities |
| ch. 20 | "Not sufficient evidence … that stabilization is unnecessary in dissociative disorders" |
| ch. 20 | Neither AIP nor dual representation theory explains divided identity |
| ch. 21 | "Exposure is not synthesis"; start with the least intense memory |
| Appendix C | "My Safety Plan" |

**The Haunted Self.** All verbatim:

| Location | Claim |
|---|---|
| Preface | "Unduly rigid and closed to each other" |
| ch. 5 | Alterations of consciousness are "sensitive but not specific" |
| ch. 5 | DES-T predicts DDNOS and DID better than the DES |
| ch. 6 | "PTSD can thus be regarded as a dissociative disorder … This hypothesis is open to empirical test" |
| ch. 8 | Presentification as "an ultimate goal of therapy" |
| ch. 9 | "Clinically convenient" hierarchy of action tendencies |
| ch. 10 | "I hate you, don't leave me" |
| ch. 16 | Realization as the "crucial missing link" |
| ch. 17 | Overcoming the phobia of intimacy as "perhaps the pinnacle of successful treatment" |

**Leeds (2016).**

| Chapter | Claim |
|---|---|
| ch. 3 | Preparation "may need to expand to become the central focus" |
| ch. 4 | Persistent crises can lead clinicians to overextend preparation |
| ch. 5 | Past attempts as the "single greatest predictor—but by no means the only one" |
| ch. 5 | Cutting or burning must be controlled before reprocessing |
| ch. 5 | DES-II is a "weak instrument"; the minimum screening battery |
| ch. 6 | Screen "before offering any bilateral stimulation procedures, including RDI" |
| ch. 6 | Fewer than 5% of subjects needed RDI (Korn et al., 2004) |
| ch. 6 | The invalid reasons for using RDI |
| ch. 6 | The 0–10 version of the BHS; CIPOS as an "alternate EMDR therapy procedure" |
| ch. 8 | Change the stimulation after two unchanged sets |
| ch. 9 | The four categories of ineffective reprocessing |
| ch. 10 | The Installation Phase resembles the original EMD |
| ch. 11 | "Tendency of the brain to retain threat cues" (LeDoux) |
| ch. 14 | Hofmann's inverted protocol |

**External sources (checked at abstract level):**

- **van Vliet et al. (2021):** n = 121; STAIR plus EMDR no better than EMDR alone; similar dropout ([EMDRIA summary](https://www.emdria.org/resource/phase-based-treatment-versus-immediate-trauma-focused-treatment-for-post-traumatic-stress-disorder-due-to-childhood-abuse-randomised-clinical-trial-bjpsych-open/)).
- **Hoeboer et al. (2020):** 21 studies; no moderation by dissociation.
- **NICE NG225:** three "do not use" recommendations on risk tools and stratification, plus risk formulation.
- **Cloitre et al. (2011):** 84% of 50 experts endorsed a phase-based approach.
- **Flash:** one clinical RCT (Yaşar et al., 2022; comparator psychoeducation; one-month follow-up). The ENHANCE RCT protocol was published in 2023; no results were found. No systematic review of Flash was found. The course's Flash claims are current as of this search.
- **ICD-11 CPTSD and personality disorder:** the course's wording (differentiate; the two can co-occur; add the second diagnosis when it adds clinical information) matches published interpretations of ICD-11. The WHO CDDR text itself could not be opened from this environment.

---

## 6. Corrections in priority order

1. **F-01:** evidence lines for CIPOS, Loving Eyes, IHD and LOUA/LOPA (guide ch. 13; D4S48–S53 notes).
2. **F-02:** relabel D1S4 and D3S65; add the 2025 DID treatment review to guide ch. 7.
3. **F-05, F-06:** fix the two citation errors (D1S43 source tag; `pm3_msa.py` and `pm3_col.py` locator). Both are mechanical and participant-facing.
4. **F-03, F-04, F-08:** one short paragraph each in the guide, with one sentence in the matching theory note.
5. **F-07, F-09, F-11, F-12, F-13:** wording changes.
6. **Low items:** batch them into the next build.

Following the README workflow: edit the source files → run `bash build.sh` → run `python3 verify.py` (must print PASS). Consider adding a check to `verify.py` that fails on "chs. 8 and 9" near "RDI", and on "TTRD" as the only source on the three-levels slide.

---

## 7. What would make this audit complete

- **Primary diagnostic texts:** the ICD-11 CDDR (WHO, 2024) PDF and the DSM-5-TR dissociative-disorders text, to check the diagnostic wording word for word.
- **Unsupplied sources:** Shapiro (2018), ISSTD (2011), and the two Carlson (1993) papers, to close F-20 and F-22 and the ISSTD page citations (pp. 133–134, 143).
- **Network access** to PubMed/PMC, NICE and WHO from this environment, to move the external checks from abstract level to full text.
- **A bilingual reviewer** for the Arabic guides (`msa.md`, `col.md`), which were not compared against `guide.md` in this audit.
