# CAPD Clinical Decision-Support

A browser-based prototype for audiology clinical workflow support: case history, functional listening screening, peripheral audiology data entry, central auditory test results, differential considerations, management planning, and clinical report export.

## Run locally
Open [index.html](index.html) in a modern browser. Core functions work offline; no server or package installation is required.

## Main features
- Child/adolescent and adult screening pathways selected by age.
- Live guided-workflow banner with a suggested next step, updated from age, safety flags, screening selection, peripheral findings and central-test documentation.
- Guided status is saved in JSON export and included as a snapshot in the clinical report; English, Hindi and Punjabi guidance is available.
- Original symptom prompts across functional listening domains.
- Primary checklist workflow: SCAP for children and SCAP-A for adults, with official result recording and explicit population/translation caveats.
- Peripheral audiology entry: otoscopy, tympanometry, pure-tone summary, speech measures, speech-in-noise, reflexes, OAE and ABR.
- Central auditory test entry with domain, test, condition, raw result, Z-score and normative notes.
- Review prompts for entered Z-scores at or below −2 SD and −3 SD; these are not diagnostic thresholds.
- Differential considerations, additional assessment selections and management options.
- Downloadable HTML clinical report, print / Save as PDF, and JSON export.

## Important clinical limitations

The guided workflow is an organisational aid, not a validated decision rule. It prioritises urgent review when sudden hearing change or acute neurological symptoms are recorded, prompts review of other safety flags, and reminds the clinician to review peripheral audiology before interpreting central test results. A non-normal or missing peripheral result is not an automatic CAPD exclusion or diagnosis. Phone microphone/noise checks and uncalibrated earphone tasks must not be presented as calibrated dB HL hearing tests. The workflow does not implement automated psychoacoustic testing or an autonomous CAPD classifier.
This is a prototype, not a validated medical device or autonomous diagnostic system. Its screening prompts are original and are **not** CHAPPS, Fisher's Auditory Problems Checklist, SIFTER or a validated adult questionnaire. They have no diagnostic cut-off. Do not claim CAPD based on screening counts or Z-score flags alone.

A qualified audiologist must select and interpret age- and language-appropriate tests using current test manuals, normative data, peripheral audiology findings and the complete clinical history. Consider language proficiency, attention, cognition, development and other differential or co-occurring conditions. Sudden hearing loss or acute neurological symptoms require urgent medical assessment.

## Privacy
The page does not transmit patient data to a server. Data can still appear in downloaded HTML or JSON reports; store these securely and avoid unnecessary identifiers. This prototype has no authentication, encrypted record storage, audit trail or clinic-grade data retention controls.

## Guidance
- American Speech-Language-Hearing Association (ASHA), Practice Portal: Central Auditory Processing Disorder.
- American Academy of Audiology, Clinical Practice Guidelines: Diagnosis, Treatment, and Management of Children and Adults with CAPD (2010).

Clinical deployment requires qualified review, usability testing, appropriate standardized instruments and validation of scoring and decision rules.

## Indian checklist workflow: SCAP and SCAP-A

The main screening workflow is age-guided:

- **SCAP (children)** — a 12-item screening checklist studied in school-age samples. Research has reported a cutoff around 6 in studied samples, but the authorised form, scoring direction and local protocol must be verified. The app does not reproduce verified official items. [SCAP research record](https://www.researchgate.net/publication/284588609_Utility_of_the_screening_checklist_for_auditory_processing_SCAP_in_detecting_CAPD_in_children).
- **BMQ-R (child pathway)** — the interface offers an item-by-item draft based on the 6 therapy-history prompts and 42 behavioural prompts supplied for this project. It records therapy history separately, calculates descriptive Yes counts by supplied category (DEC, TFM Noise/Memory/Variable, INT, ORG and APD), and includes the answers in HTML report and JSON export. The 42-item count is **not verified as the official BMQ-R wording, category structure or scoring** and no official age-norm threshold is applied. Use the current [official EAA form](https://www.edaud.org/assets/docs/Questionnaires/BMQ-R%20form%209-2020.pdf) and [administration/interpretation manual](https://www.edaud.org/assets/docs/Questionnaires/BMQ-R%20Manual%209-2020%20Update.pdf) for standardized administration.
- **SCAP-A (adults)** — the preliminary development evidence involved older adults aged 55–75 and included self-report and family-informant forms. Do not assume validation for all adults aged 18+. [Article and PDF](https://www.journalofhearingscience.com/Screening-checklist-for-auditory-processing-nin-adults-SCAP-A-Development-and-preliminary,120593,0,2.html) · [Later study](https://pmc.ncbi.nlm.nih.gov/articles/PMC10152099/).

The selector hides child checklist options for adults and the adult checklist option for children when age is entered. This is an interface aid, not an automatic test recommendation. None of these screeners independently diagnoses CAPD. Clinicians must consider the referral question, age, language, peripheral audiology, norms, developmental context and clinical history, and use authorised forms/instructions for standardized administration.

## English, Hindi and Punjabi interface

The interface language selector offers English, Hindi (हिन्दी) and Punjabi (ਪੰਜਾਬੀ). The app's original supplementary listening prompts and in-app SCAP, SCAP-A and child BMQ-R draft prompts, response choices, guidance and live interpretations have Hindi and Punjabi wording; entered answers are preserved when switching languages. Some technical labels may remain in English where appropriate. The downloadable clinical report remains English.

**Important:** the Hindi and Punjabi wording is provided for accessibility and is **not** a validated translation of SCAP or SCAP-A. The in-app prompts are not verified verbatim official items. Do not apply official cutoffs to an unofficial translation. Use the authorised instrument, language/version, administration and scoring instructions.

## SCAP checklist entry and scoring

When **SCAP** is selected in the screening-tool selector, the app displays a 12-item yes/no checklist, a selectable threshold (6 or 7), a live total, an at-risk / below-threshold / incomplete interpretation, and a list of possible follow-up assessment domains. The responses and interpretation are included in the generated clinical report and JSON export.

**Clinical validity note:** the in-app prompts are adapted from the item descriptions supplied for this prototype and have not been verified as verbatim official SCAP wording. The in-app scoring is a descriptive aid using Yes = 1 and No = 0, not a substitute for official SCAP administration/scoring. The literature reports a score threshold of 6 or greater in some uses, but clinicians must verify the authorised checklist, scoring direction and local protocol. A positive screen is not a CAPD diagnosis; a low score does not rule out the need for assessment when clinically indicated. Hindi/Punjabi translations are not validated versions of SCAP.

## SCAP-A adult checklist entry and interpretation

When **SCAP-A** is selected, the screening panel provides 12 adult symptom prompts with response options **1 = difficulty present** and **0 = difficulty absent**. The app records item-level responses, lists any positive symptom identifiers, calculates the descriptive count out of 12, and includes the entries and interpretation in the downloadable clinical report and JSON export. A response of 1 on any item is treated as a positive symptom identifier that prompts clinician review; the app does not apply a total-score cut-off. A completed score of 0 does not rule out CAPD when clinical concerns persist.

**Important wording and validation limitation:** the supplied material did not provide verbatim question text for items 5, 7 and 11, only a description of their intended focus. Those three prompts are explicitly marked as app-adapted wording; the remaining prompts use the wording supplied for this prototype but have not been independently verified against the authorised publication. Hindi and Punjabi question translations are provided for convenience and are not validated SCAP-A versions. The SCAP-A development evidence is preliminary and focused mainly on adults aged 55–75; do not assume validation for every adult age group. Obtain and administer the authorised form and follow its official instructions for standardized clinical use. A positive screen is not a diagnosis, and any referral decision should consider the complete case history, peripheral hearing, language, cognition, test norms and clinical question.

Possible follow-up domains include speech-in-noise / monaural low-redundancy speech, dichotic listening, temporal processing (such as gap detection), and binaural interaction. This list is illustrative rather than a mandatory test battery.


## Phone stimulus lab (pilot / research use only)

The Central Auditory Test Results panel includes a phone stimulus lab with:
- Original two-tone same/different practice trials.
- Original three-tone low/high pattern practice.
- A short-gap-in-noise demonstration.
- A stereo left/right tone routing demonstration.
- Local playback of clinician-provided authorised audio for speech-in-noise, degraded-speech, or other tasks.
- An observation log that is included in the case JSON and clinical report.

These are **not standardized CAPD tests**, do not reproduce official Dichotic Digits, Pitch Pattern Sequence, GIN/RGDT, MLD, or speech-in-noise test items, and do not provide clinical norms or diagnostic thresholds. Phone output level, transducer frequency response, channel routing, room noise and device variability are not calibrated by this app. The dichotic demo requires stereo headphones and a verified left/right channel; a phone loudspeaker or mono route is unsuitable. For localization, binaural interaction/MLD, speech-in-noise and other standardized measures, use the authorised stimulus set, its exact manual, the appropriate calibrated equipment and age/language-specific norms. A local audio file is played only in the browser and is not uploaded to a server.

Reference links in the interface include ASHA's CAPD Practice Portal, the VA NCRAR overview of auditory processing measures, a GitHub temporal-processing training/demo project (EarSync; not a diagnostic test), the UCL HeadphoneCheck research task (not a CAPD test), and a published tablet-based CAP assessment study. Reuse any external code or audio only after checking its license, intended use and study protocol.


### Additional original pilot substitutes

The stimulus lab also provides original, non-standardized demonstrations for auditory domains that previously only had instructions:
- **Speech-in-noise feasibility demo:** plays an authorised local speech recording mixed with generated white noise. The slider controls digital noise gain only, not calibrated SNR. Record file/version/language and the nominal mix; do not apply standard speech-in-noise norms.
- **Virtual lateralization demo:** randomizes a tone's left/center/right stereo pan for verified headphones. This is not real-world sound localization and is not a clinical localization substitute.
- **Binaural phase demonstration:** presents a tone as present or absent in correlated noise with a nominal S0/Sπ phase relationship. It illustrates the concept behind masking-level differences, but is not the official MLD procedure and has no threshold or norms.

All three tasks log descriptive responses in the case report and JSON. They are pilot/familiarisation demonstrations only. Browser audio output, channel routing, transducer response, room acoustics, signal level and timing are not clinically calibrated. Do not use these tasks to diagnose, rule out, or assign severity to CAPD.


## Protocol-fidelity audit and multilingual SPIN-style practice

**Audit result: the interface does not reproduce every standardized CAPD test's complete stimulus set and administration sequence.** It contains original demonstrations and manual-entry workflows; do not describe all of them as standardized or validated.

| Interface task | Relationship to published procedures | Current limit |
|---|---|---|
| Two-tone discrimination | General same/different auditory-discrimination principle | One original tone pair at a time; no universal published CAPD sequence, full trial set or norms |
| Three-tone pitch pattern | Now schedules 3 random practice patterns plus 30 test patterns; the six possible patterns occur five times each in randomized order; 880/1122 Hz, 150 ms tones, 200 ms within-pattern interval and 6 seconds between pattern onsets | FPT-inspired timing/list structure, not official FPT recordings; stereo panning is not calibrated monaural audiometry; no norms or automated scoring |
| Gap-in-noise | Updated to a GIN-inspired list architecture: 36 six-second noise segments, 5-second inter-segment intervals, 60 gaps total; ten gap durations (2, 3, 4, 5, 6, 8, 10, 12, 15, 20 ms) appear six times each, with no more than three gaps per segment | Original browser-generated noise, not official GIN recordings or RGDT; no calibrated presentation, validated norms, false-positive analysis or clinical threshold calculation |
| Dichotic | Demonstrates simultaneous left/right stereo routing | Pure tones, not dichotic digits/words/sentences; not a clinical dichotic test |
| SPIN-style practice | 15 newly written sentences each in English, Hindi and Punjabi; browser speech synthesis plus generated background noise; response and target key can be recorded | Not official SPIN/SINCA materials, no validated language equivalence, talker recording, calibrated SNR or norms; browser voice availability/pronunciation varies |
| Localization/lateralization | Randomized virtual left/centre/right stereo panning | Not real-world localization and not a validated clinical localization protocol |
| Binaural interaction / MLD | Illustrates a tone in correlated noise with nominal S0/Sπ conditions | Not the official MLD procedure; no threshold, calibrated phase/level or norms |
| Clinician-selected local audio | Supports local playback of an authorized recording | The clinician must follow the material's own manual and scoring procedure; the app does not verify that sequence |

### SPIN-style item bank

The app contains 15 original short sentences per language. It cycles through a shuffled list before repeating items, plays each through the browser's speech-synthesis service while noise is played, hides the answer key until requested, and stores the response, item text, target key, language and condition in the case report/JSON. These are practice/feasibility prompts only. Speech synthesis may use a fallback voice or may not have an appropriate Punjabi/Hindi voice installed; if pronunciation is unsuitable, use an authorized local recording instead. The noise control is a digital gain setting, not a calibrated SNR. Do not compare scores across languages or use these items to diagnose, rule out or grade CAPD.

### Evidence used for the audit

- ASHA, [Central Auditory Processing Disorder Practice Portal](https://www.asha.org/practice-portal/clinical-topics/central-auditory-processing-disorder/): describes auditory-discrimination, temporal, dichotic, monaural low-redundancy speech, binaural-interaction and localization domains; there is no universally accepted CAPD screening method.
- Musiek et al., [GIN test procedure (PubMed)](https://pubmed.ncbi.nlm.nih.gov/16377996/): describes 6-second white-noise segments with 0–3 gaps, gap durations from 2–20 ms and 60 gap events per list.
- [Published GIN protocol details (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC9443716/): describes practice, monaural presentation, 5-second interstimulus intervals, gap durations, repeat counts and the threshold method.
- [MAPA-2 validity study (ASHA Journals)](https://pubs.asha.org/doi/10.1044/2020_LSHSS-20-00001): illustrates that a specific battery's speech-in-noise and pitch-pattern subtests have defined item sets; these cannot be replaced by arbitrary browser-generated phrases and called equivalent.

The pitch-pattern practice path uses a published FPT-style architecture of three practice patterns followed by 30 test patterns; an example protocol reports 30 test items per ear, 880/1122 Hz tones, 150 ms tones, 200 ms within-pattern intervals and about 6 seconds between patterns ([published FPT procedure](https://api.mdsoar.org/server/api/core/bitstreams/d3ede1eb-c620-4a6d-83c0-3d23644d9a55/content)). The app uses browser stereo panning for a left/right-channel demonstration, not calibrated monaural audiometry, so this remains an FPT-inspired research/familiarisation sequence rather than a clinical administration.
 
This audit implements reproducible timing/list structure where a published description supports it, while deliberately not claiming equivalence to copyrighted or standardized materials. Clinical use still requires authorized materials, the exact test manual, calibrated equipment, suitable age/language norms and qualified interpretation. Browser end-to-end testing, acoustic calibration and multilingual speech-quality validation have not been completed.
