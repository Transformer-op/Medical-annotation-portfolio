# Label Decisions — Edge Cases and Reasoning

## Why this file exists
Real annotation always involves ambiguous cases. This file documents
my reasoning on difficult labelling decisions, demonstrating
clinical judgment beyond mechanical labelling.

---

## Decision 1
Sentence: "The patient is diabetic and has a prior history 
of coronary artery disease."
Entity: "Diabetic"
Question: Should "diabetic" be labelled DIAGNOSIS or left 
out because it is an adjective describing the patient, 
not a formal diagnosis name?
Decision: DIAGNOSIS
Reason: In clinical documentation, "diabetic" is used 
interchangeably with "type 2 diabetes mellitus" as a confirmed 
diagnosis. As a nurse, I know that when a provider writes 
"the patient is diabetic" in a clinical note, it is not a 
casual description — it is a documented medical history entry. 
The adjective form does not change the clinical meaning. 
I labelled it DIAGNOSIS and noted it in the notes column 
to flag the non-standard form.

---

## Decision 2
Sentence: "Ms. ABCD is a 69-year-old lady who was admitted 
to the hospital with chest pain and respiratory insufficiency."
Entity: "Respiratory insufficiency"
Question: Is "respiratory insufficiency" a SYMPTOM or 
a DIAGNOSIS?
Decision: DIAGNOSIS
Reason: This was a genuine edge case. Respiratory 
insufficiency can present as a symptom (laboured breathing, 
low oxygen) but in this sentence it is listed as a reason 
for admission alongside chest pain. In clinical documentation, 
when a condition is cited as an admission reason, it has 
already been assessed and classified by the provider — making 
it a DIAGNOSIS. If the sentence had said "patient complains 
of difficulty breathing," I would have labelled it SYMPTOM. 
The clinical context of the sentence changed the label.

---

## Decision 3
Sentence: "Cultures taken from the wound on 06/25/2008 
were reported positive for methicillin-sensitive 
Staphylococcus aureus (MSSA)."
Entity: "Positive"
Question: Should I label "positive" alone as TEST_RESULT, 
or should the full phrase "positive for MSSA" be the entity?
Decision: "Positive for methicillin-sensitive 
Staphylococcus aureus (MSSA)" as TEST_RESULT
Reason: I initially labelled just "positive" as the 
TEST_RESULT because that is the outcome of the culture. 
However, "positive" without context loses critical clinical 
meaning — positive for what? The organism identified is 
inseparable from the result in this case. A medical AI 
model trained on this data needs to understand that the 
full result includes both the outcome and the pathogen. 
I revised the entity_text to capture the complete finding. 
This also reflects a broader rule I applied throughout: 
TEST_RESULT should capture enough text to be clinically 
meaningful on its own.

---
## Decision 4
During annotation I realised TEST and TEST_RESULT needed to be 
separated. I updated the guidelines at row 3 when I found 
"chest X-ray" and "normal" were being conflated into one label. 
Keeping them separate improves label precision.
