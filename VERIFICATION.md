# CARE Demo — Feature Verification (Review)

**Date:** Verification run against current `index.html`.

## 1. Attorney dashboard quick-action cards
**Status: Complete.**  
The attorney dashboard includes **8** quick-action cards (more than the original three): Cases Awaiting Attestation, Cases Needing Review, Active Cases, Cases Awaiting Review, RN Coordinated Cases, 7-Day Follow-Up Window, 14-Day Follow-Up Window, 28-Day Follow-Up Window.

## 2. Cases Awaiting Attestation first
**Status: Complete.**  
"Cases Awaiting Attestation" is the **first** card in the dashboard action area and is styled with stronger emphasis (e.g. higher opacity background, border).

## 3. Sample RN Care Plan restored and substantial
**Status: Complete.**  
The Sample RN Care Plan uses expand/collapse (`<details>`/`<summary>`). It includes all nine sections with clinical content: Current Clinical Status, Client Strengths Supporting Recovery, Barriers to Care, Safety Considerations, 4Ps Wellness Review, Functional Capacity Observations, Goals of Care, Interventions, Follow-Up Plan. Current Clinical Status, Barriers to Care, and Functional Capacity Observations are expanded by default.

## 4. Reconcile in front of C.A.R.E. on intro and final screens
**Status: Complete.**  
Both the Introduction screen and the final CTA screen use the same logo markup: `Reconcile <span>C.A.R.E.</span>` (with `title="Reconcile C.A.R.E."`), so "Reconcile" appears in front of "C.A.R.E." on both.

## 5. Pre-existing conditions dropdown-style control
**Status: Complete.**  
Pre-existing Medical Conditions uses a multi-select list: `<select class="form-select form-select-multiple" id="intake-conditions" multiple size="6">` with common options (e.g. Hypertension, Diabetes, Asthma). It is a dropdown-style control (list box) rather than a free-text box.

## 6. Current medications dropdown-based structured control
**Status: Complete.**  
Current Medications uses two medication rows, each with three dropdowns: Medication name (`intake-med1-name`, `intake-med2-name`), Dosage, and Frequency. Layout uses the `.medication-row` grid. Demo shows Lisinopril 10 mg once daily and Ibuprofen 400 mg as needed.

## 7. Client intake summary / print-download screen after submission
**Status: Complete.**  
A dedicated screen `screen-intake-summary` exists after the intake completion transition. It includes: client/case header, client info, injury summary, medical history summary, provider summary, consent/key selections, Next Steps block, and three buttons: Print Intake Summary, Download Intake Summary, Continue to Attorney View. Flow: Submit → transition screen → "View Intake Summary" → summary screen.

## 8. Intake summary reflects demo client’s actual selections
**Status: Complete.**  
On submit, `submitIntake()` captures all relevant form fields (personal, injury, body areas, conditions, medications, allergies, surgeries, PCP, providers, etc.) into `intakeData`. When the summary screen is shown, `populateIntakeSummary()` fills the summary elements from `intakeData`. The download function also uses `intakeData`. The summary therefore reflects the demo client’s actual selections and entered values (e.g. Maria Santos, case number, injury type/date, body areas, Hypertension, Lisinopril/Ibuprofen, providers).

---

**Summary:** All eight items are complete. No corrections required for these checks.
