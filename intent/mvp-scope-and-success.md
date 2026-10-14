# MVP intent: scope and success criteria

## Out of scope

The following are explicitly out of scope for this intent:

- Wonde integration
- SIMS integration
- Arbor integration
- Bromcom integration
- live SEND data import
- automated EAL data import
- SENCO dashboards
- MAT dashboards
- parent accounts
- pupil accounts beyond what is needed to complete a diagnostic
- whole-school analytics
- automatic intervention scheduling
- arbitrary subjects
- secondary education
- automated lesson-plan generation
- fully personalised digital tutoring
- permanent ability grouping
- high-stakes assessment
- automatic educational or SEND decisions
- production billing
- school procurement workflows

These should become separate intents after the core proposition is validated.

## Future intent: MIS integration

A later intent should investigate integrating the product with school MIS data.

Potential route:

```text
SIMS ─────┐
Arbor ────┤
Bromcom ──┤
Other ────┤
          ↓
        Wonde
          ↓
    Adaptive teaching platform
```

The objective would be to import only the minimum information required to improve recommendations.

Potential sources:

- class membership
- year group
- selected SEND/EAL information
- teaching strategies
- pupil passport information

This future work must include:

- UK GDPR analysis
- school data-controller responsibilities
- DPIA requirements
- data-processing agreements
- permissions/scopes
- retention
- deletion
- model-provider data policies
- auditability

## Success criteria

- [ ] A teacher can manually create a class containing at least 30 pupils.
- [ ] A teacher can select at least one supported primary maths learning objective and launch a diagnostic mapped to that objective's prerequisite knowledge.
- [ ] After diagnostic responses are submitted, every pupil receives an evidence-based prerequisite-knowledge summary that identifies secure/insecure areas without relying solely on an overall percentage score.
- [ ] For predefined misconception response patterns, the system identifies the matching likely misconception and shows the pupil responses that support that inference; where no supported pattern matches, it explicitly reports that no specific misconception can be determined.
- [ ] The system produces a class-level adaptive teaching view that groups similar current needs and recommends targeted support while keeping the selected learning objective common to the class.
- [ ] Every recommended adaptation contains a human-readable rationale linked to diagnostic evidence, can be accepted/edited/rejected by the teacher, and does not use a formal SEND diagnosis as the sole reason for the recommendation.
- [ ] An end-to-end automated test demonstrates the flow: create class → select learning objective → complete diagnostic for multiple pupils → analyse responses → display class findings → display editable adaptive-teaching recommendations.

## Product validation questions

This intent proves technical and workflow feasibility, but it should also produce enough of the experience to test the following with real teachers:

1. Would teachers run a short diagnostic before a lesson or unit?
2. How short must the diagnostic be to fit normal classroom practice?
3. Is lesson-level assessment useful, or is unit-level assessment more realistic?
4. Do teachers trust misconception-level analysis?
5. Are recommendations sufficiently specific to change teaching?
6. Does the class view reduce planning workload?
7. Do teachers prefer a core task plus scaffolds over separately generated worksheets?
8. Which pupil-context information genuinely improves recommendations?
9. How often do teachers override the system?
10. Would schools pay for this independently, or does MIS integration need to exist first?

Answers to these questions should inform subsequent intents rather than being assumed.
