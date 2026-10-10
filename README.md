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

The main screening workflow is intentionally limited to two Indian-developed checklists:

- **SCAP (children)** — a 12-item screening checklist studied in school-age samples. Research has reported a cutoff around 6 in studied samples, but the authorised form, scoring direction and local protocol must be verified. The app does not reproduce verified official items. [SCAP research record](https://www.researchgate.net/publication/284588609_Utility_of_the_screening_checklist_for_auditory_processing_SCAP_in_detecting_CAPD_in_children).
- **SCAP-A (adults)** — the preliminary development evidence involved older adults aged 55–75 and included self-report and family-informant forms. Do not assume validation for all adults aged 18+. [Article and PDF](https://www.journalofhearingscience.com/Screening-checklist-for-auditory-processing-nin-adults-SCAP-A-Development-and-preliminary,120593,0,2.html) · [Later study](https://pmc.ncbi.nlm.nih.gov/articles/PMC10152099/).

Other screening questionnaires and screening-resource panels have been removed from the main interface to keep the workflow focused. This does **not** mean SCAP and SCAP-A are sufficient to diagnose CAPD or are validated for every Indian age group, language or population. Clinicians may still select appropriate diagnostic tests and further assessments based on the referral question, age, language, peripheral audiology, norms and clinical history.

The app's SCAP/SCAP-A wording and scoring remain subject to the limitations described below. Obtain and use the authorised forms and their official instructions for standardized clinical administration. A screening result is not a diagnosis.

## English, Hindi and Punjabi interface

The interface language selector offers English, Hindi (हिन्दी) and Punjabi (ਪੰਜਾਬੀ). The app's original supplementary listening prompts and in-app SCAP and SCAP-A prompts, response choices, guidance and live interpretations have Hindi and Punjabi wording; entered answers are preserved when switching languages. Some technical labels may remain in English where appropriate. The downloadable clinical report remains English.

**Important:** the Hindi and Punjabi wording is provided for accessibility and is **not** a validated translation of SCAP or SCAP-A. The in-app prompts are not verified verbatim official items. Do not apply official cutoffs to an unofficial translation. Use the authorised instrument, language/version, administration and scoring instructions.

## SCAP checklist entry and scoring

When **SCAP** is selected in the screening-tool selector, the app displays a 12-item yes/no checklist, a selectable threshold (6 or 7), a live total, an at-risk / below-threshold / incomplete interpretation, and a list of possible follow-up assessment domains. The responses and interpretation are included in the generated clinical report and JSON export.

**Clinical validity note:** the in-app prompts are adapted from the item descriptions supplied for this prototype and have not been verified as verbatim official SCAP wording. The in-app scoring is a descriptive aid using Yes = 1 and No = 0, not a substitute for official SCAP administration/scoring. The literature reports a score threshold of 6 or greater in some uses, but clinicians must verify the authorised checklist, scoring direction and local protocol. A positive screen is not a CAPD diagnosis; a low score does not rule out the need for assessment when clinically indicated. Hindi/Punjabi translations are not validated versions of SCAP.

## SCAP-A adult checklist entry and interpretation

When **SCAP-A** is selected, the screening panel provides 12 adult symptom prompts with response options **1 = difficulty present** and **0 = difficulty absent**. The app records item-level responses, lists any positive symptom identifiers, calculates the descriptive count out of 12, and includes the entries and interpretation in the downloadable clinical report and JSON export. A response of 1 on any item is treated as a positive symptom identifier that prompts clinician review; the app does not apply a total-score cut-off. A completed score of 0 does not rule out CAPD when clinical concerns persist.

**Important wording and validation limitation:** the supplied material did not provide verbatim question text for items 5, 7 and 11, only a description of their intended focus. Those three prompts are explicitly marked as app-adapted wording; the remaining prompts use the wording supplied for this prototype but have not been independently verified against the authorised publication. Hindi and Punjabi question translations are provided for convenience and are not validated SCAP-A versions. The SCAP-A development evidence is preliminary and focused mainly on adults aged 55–75; do not assume validation for every adult age group. Obtain and administer the authorised form and follow its official instructions for standardized clinical use. A positive screen is not a diagnosis, and any referral decision should consider the complete case history, peripheral hearing, language, cognition, test norms and clinical question.

Possible follow-up domains include speech-in-noise / monaural low-redundancy speech, dichotic listening, temporal processing (such as gap detection), and binaural interaction. This list is illustrative rather than a mandatory test battery.

