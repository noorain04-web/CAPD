# CAPD Clinical Decision-Support

A browser-based prototype for audiology clinical workflow support: case history, functional listening screening, peripheral audiology data entry, central auditory test results, differential considerations, management planning, and clinical report export.

## Run locally
Open [index.html](index.html) in a modern browser. Core functions work offline; no server or package installation is required.

## Main features
- Child/adolescent and adult screening pathways selected by age.
- Original symptom prompts across functional listening domains.
- Fields for separately administered standardized questionnaires.
- Peripheral audiology entry: otoscopy, tympanometry, pure-tone summary, speech measures, speech-in-noise, reflexes, OAE and ABR.
- Central auditory test entry with domain, test, condition, raw result, Z-score and normative notes.
- Review prompts for entered Z-scores at or below −2 SD and −3 SD; these are not diagnostic thresholds.
- Differential considerations, additional assessment selections and management options.
- Downloadable HTML clinical report, print / Save as PDF, and JSON export.

## Important clinical limitations
This is a prototype, not a validated medical device or autonomous diagnostic system. Its screening prompts are original and are **not** CHAPPS, Fisher's Auditory Problems Checklist, SIFTER or a validated adult questionnaire. They have no diagnostic cut-off. Do not claim CAPD based on screening counts or Z-score flags alone.

A qualified audiologist must select and interpret age- and language-appropriate tests using current test manuals, normative data, peripheral audiology findings and the complete clinical history. Consider language proficiency, attention, cognition, development and other differential or co-occurring conditions. Sudden hearing loss or acute neurological symptoms require urgent medical assessment.

## Privacy
The page does not transmit patient data to a server. Data can still appear in downloaded HTML or JSON reports; store these securely and avoid unnecessary identifiers. This prototype has no authentication, encrypted record storage, audit trail or clinic-grade data retention controls.

## Guidance
- American Speech-Language-Hearing Association (ASHA), Practice Portal: Central Auditory Processing Disorder.
- American Academy of Audiology, Clinical Practice Guidelines: Diagnosis, Treatment, and Management of Children and Adults with CAPD (2010).

Clinical deployment requires qualified review, usability testing, appropriate standardized instruments and validation of scoring and decision rules.
