# Medical Annotation Portfolio — NER and Text Classification

## What this project is
A medical data annotation project demonstrating two core annotation
task types: Named Entity Recognition (NER) and Text Classification,
applied to real anonymised clinical text.

## Annotator background
Favour Nwatu — BNSc — ESUT College of Medicine (expected 2026) and NMCN licensure examination passed. Clinical experience across psychiatric, community health,
and teaching hospital settings. This background informs the clinical
accuracy and reasoning behind every label in this dataset.

## Dataset source
All text sourced from MTSamples.com — a publicly available collection
of anonymised medical transcription samples.

## Files in this project
- ner-dataset.csv — 25 clinical sentences with entity-level labels
- classification-dataset.csv — 25 sentences with category and urgency labels
- annotation-guidelines.md — full labelling rules and definitions
- label-decisions.md — documented reasoning on edge cases

## NER label types used
SYMPTOM | DIAGNOSIS | MEDICATION | DOSAGE | BODY_PART | TEST | TEST_RESULT

## Classification label types used
primary_category: SYMPTOM_REPORT | DIAGNOSIS_STATEMENT | TREATMENT_PLAN
| TEST_ORDER | TEST_RESULT | PATIENT_HISTORY | PATIENT_DENIAL

secondary_category: CARDIOVASCULAR | RESPIRATORY | NEUROLOGICAL
| ENDOCRINE | GENERAL | MUSCULOSKELETAL | RENAL

clinical_urgency: ROUTINE | MONITOR | URGENT

## What this demonstrates
- Understanding of annotation methodology and label schema design
- Ability to apply clinical knowledge to improve label accuracy
- Quality control thinking through documented edge case reasoning
- Familiarity with NER and classification task types used in medical AI
