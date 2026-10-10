# CAPD Clinical Decision-Support

A browser-based prototype for audiology clinical workflow support: case history, functional listening screening, peripheral audiology data entry, central auditory test results, differential considerations, management planning, and clinical report export.

## Run locally
Open [index.html](index.html) in a modern browser. Core functions work offline; no server or package installation is required.

## Main features
- Child/adolescent and adult screening pathways selected by age.
- Live guided-workflow banner with a suggested next step, updated from age, safety flags, screening selection, peripheral findings and central-test documentation.
- Guided status is saved in JSON export and included as a snapshot in the clinical report; English, Hindi and Punjabi guidance is available.
- Original symptom prompts across functional listening domains.
- Fields for separately administered standardized questionnaires.
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

## Indian-developed CAPD screening resources

The screening section now links to published Indian resources and records clinician-entered results without reproducing author-controlled item wording:

- **SCAP (children)** — Screening Checklist for Auditory Processing, associated with Yathiraj and Mascarenhas and studied in school-age children. An accessible research record is available at [ResearchGate](https://www.researchgate.net/publication/284588609_Utility_of_the_screening_checklist_for_auditory_processing_SCAP_in_detecting_CAPD_in_children). Published work reports a cut score of 6 in the studied sample, with sensitivity 71% and specificity 68%; these estimates are not universal and should not be applied without the authorised version and its instructions.
- **SCAP-A (adults)** — [Vaidyanath & Yathiraj, 2014, article and PDF](https://www.journalofhearingscience.com/Screening-checklist-for-auditory-processing-nin-adults-SCAP-A-Development-and-preliminary,120593,0,2.html). The original development study involved adults aged 55–75 and self-report/family forms; the article describes preliminary findings and says further validation was needed. Do not assume validity for all adults aged 18+.
- **STAP** — [Preliminary report](https://pubmed.ncbi.nlm.nih.gov/24224993/) and [validation study](https://pubmed.ncbi.nlm.nih.gov/24447685/). STAP is a performance-based child screening test, not a questionnaire, and requires appropriate test materials and trained administration.
- **Indian clinical practice context** — [A Survey on Screening and Diagnostic Criteria of Auditory Processing Disorders in India](https://pmc.ncbi.nlm.nih.gov/articles/PMC10909056/).

The web pages and papers are research sources, not automatic permission to redistribute full test materials. The app does not embed the official questionnaire items, claim licensing, or auto-score the standardized tools. The clinician must obtain and use an authorised version, follow its administration/scoring instructions, check language and age suitability, and enter the official result. The original app prompts remain explicitly labelled as supplementary, non-validated history questions.

## BMQ-R workflow (official source-linked form)

The screening page includes a BMQ-R workflow with links to the official [questionnaire PDF](https://www.edaud.org/assets/docs/Questionnaires/BMQ-R%20form%209-2020.pdf), [administration and interpretation manual](https://www.edaud.org/assets/docs/Questionnaires/BMQ-R%20Manual%209-2020%20Update.pdf), and [Educational Audiology Association information page](https://www.edaud.org/bmqr). The 48 item prompts are not copied into this repository. Administer the official form externally, then enter category-level Yes and NA counts into the app.

The app calculates ΣCAP from DEC + TFM + INT + ORG + APD, excludes GEN, adjusts the denominator for applicable NA responses, and displays a prompt for further APD testing when ΣCAP is 8 or more as described in the official manual. This is a screening prompt only—not a diagnosis or a substitute for professional interpretation. The manual identifies age groups under 6, 6–18 and over 18 years and notes the relevance of educational exposure, respondent and prior therapies. Use the official manual to verify all entries and interpretation.

BMQ-R is not an India-specific instrument. Do not imply that its English-language results are validated for Hindi, Punjabi or other Indian languages without evidence of an appropriate validated version. The app's custom symptom prompts remain separate and explicitly non-validated.

## English, Hindi and Punjabi interface

The interface language selector offers English, Hindi (हिन्दी) and Punjabi (ਪੰਜਾਬੀ). The app's original supplementary listening prompts and the in-app SCAP and SCAP-A questionnaire prompts, response choices, guidance and live interpretations have Hindi and Punjabi wording; entered answers are preserved when switching languages. The BMQ-R category-entry workflow and its dynamic score feedback are also translated. Some technical labels may remain in English where appropriate. The downloadable clinical report remains English.

**Important:** these are interface translations and translations of original, non-standardized supplementary history prompts only. They are **not** validated Hindi or Punjabi versions of BMQ-R, SCAP, SCAP-A, STAP or APDQ. Do not translate standardized item wording yourself or apply the original cut-offs to an unofficial translation. Use the official instrument, authorised language/version, administration and scoring instructions.

## Age-guided screening instrument selector

The Screening tab has a selectable tool guide:
- **SCAP** — Indian-developed child checklist; published evidence highlighted in the app is primarily for school-aged children, particularly ages 8–13.
- **STAP** — performance-based child screening test, not a questionnaire; validation study focused on ages 8–13 and requires proper materials/administration.
- **BMQ-R** — use the official questionnaire and manual for the relevant age band (under 6, 6–18, over 18); not India-specific.
- **APDQ** — official child/adolescent differential screening tool for ages 7–18; use the official source and scoring process.
- **SCAP-A** — evidence is primarily from older adults, including ages 55–75; do not assume it is validated for all adults.

The selector provides age-based guidance, not an automatic test choice. There is no universally accepted CAPD screening questionnaire for every adult. The app links to official or research sources and does not reproduce copyrighted or author-controlled standardized item text.

## SCAP checklist entry and scoring

When **SCAP** is selected in the screening-tool selector, the app displays a 12-item yes/no checklist, a selectable threshold (6 or 7), a live total, an at-risk / below-threshold / incomplete interpretation, and a list of possible follow-up assessment domains. The responses and interpretation are included in the generated clinical report and JSON export.

**Clinical validity note:** the in-app prompts are adapted from the item descriptions supplied for this prototype and have not been verified as verbatim official SCAP wording. The in-app scoring is a descriptive aid using Yes = 1 and No = 0, not a substitute for official SCAP administration/scoring. The literature reports a score threshold of 6 or greater in some uses, but clinicians must verify the authorised checklist, scoring direction and local protocol. A positive screen is not a CAPD diagnosis; a low score does not rule out the need for assessment when clinically indicated. Hindi/Punjabi translations are not validated versions of SCAP.

## SCAP-A adult checklist entry and interpretation

When **SCAP-A** is selected, the screening panel provides 12 adult symptom prompts with response options **1 = difficulty present** and **0 = difficulty absent**. The app records item-level responses, lists any positive symptom identifiers, calculates the descriptive count out of 12, and includes the entries and interpretation in the downloadable clinical report and JSON export. A response of 1 on any item is treated as a positive symptom identifier that prompts clinician review; the app does not apply a total-score cut-off. A completed score of 0 does not rule out CAPD when clinical concerns persist.

**Important wording and validation limitation:** the supplied material did not provide verbatim question text for items 5, 7 and 11, only a description of their intended focus. Those three prompts are explicitly marked as app-adapted wording; the remaining prompts use the wording supplied for this prototype but have not been independently verified against the authorised publication. Hindi and Punjabi question translations are provided for convenience and are not validated SCAP-A versions. The SCAP-A development evidence is preliminary and focused mainly on adults aged 55–75; do not assume validation for every adult age group. Obtain and administer the authorised form and follow its official instructions for standardized clinical use. A positive screen is not a diagnosis, and any referral decision should consider the complete case history, peripheral hearing, language, cognition, test norms and clinical question.

Possible follow-up domains include speech-in-noise / monaural low-redundancy speech, dichotic listening, temporal processing (such as gap detection), and binaural interaction. This list is illustrative rather than a mandatory test battery.

