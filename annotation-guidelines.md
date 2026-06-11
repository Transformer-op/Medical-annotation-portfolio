# Annotation Guidelines — Medical NER and Text Classification

 Project Overview
This document defines the labelling rules used for this annotation project.
All text is sourced from MTSamples.com (anonymised clinical notes).
Annotator: Favour Nwatu 

---

 NER Label Definitions

SYMPTOM — A condition or experience reported by the patient or observed clinically.
Rule: Label only the symptom itself, not the body part unless they are inseparable.
Example: "chest pain" = SYMPTOM. "pain" alone without context = do not label.

DIAGNOSIS — A confirmed clinical condition documented by the provider.
Rule: Distinguish from SYMPTOM. "chest pain" is a symptom. "angina" is a diagnosis.
Example: "hypertension", "type 2 diabetes mellitus", "acute MI"

MEDICATION — Any pharmaceutical drug name, brand or generic.
Rule: Label the drug name only. The dose is a separate DOSAGE entity.
Example: "metformin", "lisinopril", "aspirin"

DOSAGE — The amount, frequency, or route of a medication.
Rule: Always appears near a MEDICATION entity. Label together if inseparable.
Example: "10mg daily", "twice daily", "500mg orally"

BODY_PART — Anatomical structure or location.
Example: "left ventricle", "lower extremities", "lung fields"

TEST — Any diagnostic investigation ordered or performed.
Example: "ECG", "chest X-ray", "HbA1c", "complete blood count"

TEST_RESULT — The outcome or finding of a test.
Example: "sinus tachycardia", "normal sinus rhythm", "elevated troponin"

---

## Text Classification Label Definitions

primary_category — The functional purpose of the sentence in clinical documentation.
secondary_category — The body system the sentence relates to.
clinical_urgency — My clinical assessment of how time-sensitive the content is,
based on nursing training and clinical posting experience.

URGENT: content that would typically prompt immediate clinical response
MONITOR: content that requires follow-up but not immediate action
ROUTINE: standard documentation with no immediate concern

---

## Edge Cases and Decisions
See label-decisions.md for specific difficult cases encountered during annotation.
