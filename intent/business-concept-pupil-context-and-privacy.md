# Business concept: pupil context and privacy

## MIS integration

A major future feature would be integration with the school's MIS.

Examples:

- SIMS
- Arbor
- Bromcom
- other UK school MIS platforms

Instead of integrating separately with each MIS, a platform such as **Wonde** could provide a single integration layer.

Conceptually:

```text
SIMS ─────┐
Arbor ────┤
Bromcom ──┤
Other ────┤
          ↓
        Wonde
          ↓
    Your platform
```

Wonde:
<https://www.wonde.com/>

This could allow the platform to automatically understand class membership and selected pupil information.

## Pupil model

The most useful pupil profile would probably combine three sources.

```text
                ┌──────────────┐
                │     MIS      │
                │ SEND / EAL   │
                │ class / year │
                └──────┬───────┘
                       │
                       ↓
                 PUPIL MODEL
                       ↑
          ┌────────────┴────────────┐
          │                         │
   Assessment history        Teacher / SENCO input
   Knowledge gaps            Classroom observations
   Misconceptions            Helpful strategies
   Prior responses           Pupil passport information
```

The platform then uses that information to recommend adaptations.

## SEND integration

Knowing that a child is on the SEND register is not enough.

The useful information is often:

- what barriers they experience
- what classroom strategies help
- what representations work
- whether instructions need chunking
- whether writing demand should be reduced
- whether visual prompts help
- whether additional processing time is useful

For example:

```text
Pupil: Ben

School context
────────────────────────
Year 2
SEND: Yes
Primary need: Cognition & Learning

Known helpful strategies
────────────────────────
Visual representations
Chunked instructions
Reduced copying

Assessment data
────────────────────────
✓ Place value
✓ Number bonds
✗ Exchanging across 10

Today's objective
────────────────────────
Add two 2-digit numbers crossing 10

Suggested adaptation
────────────────────────
• Same learning objective
• Use place-value counters
• Reduce unnecessary written instructions
• Present one question at a time initially
• Provide a worked example
• Check understanding after Q2
• Remove scaffold if secure
```

## Important SEND principle

The system should not reason simplistically from a diagnosis.

Avoid:

```text
ADHD
  ↓
AI decides what work the pupil receives
```

Prefer:

```text
Known classroom needs
        +
Current diagnostic evidence
        ↓
Suggested adaptation
        ↓
Teacher approval
```

For example, rather than sending:

> "This pupil has autism."

to the AI model, it may be more useful and privacy-preserving to send:

> "This pupil benefits from concise instructions, visual scaffolding and advance modelling."

This is both pedagogically more useful and less intrusive.

## Teacher remains in control

The platform should recommend, not dictate.

The teacher should be able to:

- accept an adaptation
- reject it
- change it
- add their own strategy
- temporarily override the pupil profile
- remove a scaffold during the lesson
- mark a recommendation as useful / not useful

This could improve the pupil model over time.

## Data protection

This becomes a serious design consideration once MIS and SEND data are involved.

The platform should be designed around:

- data minimisation
- strict role-based access
- school-controlled permissions
- audit logs
- clear retention periods
- UK GDPR compliance
- DPIAs
- encryption
- avoiding unnecessary pupil identifiers
- ensuring pupil data is not used to train third-party foundation models

Useful DfE guidance:

- Data protection in schools:
  <https://www.gov.uk/guidance/data-protection-in-schools>

- Sharing personal data:
  <https://www.gov.uk/guidance/data-protection-in-schools/sharing-personal-data>

- Generative AI and data protection:
  <https://www.gov.uk/guidance/data-protection-in-schools/generative-artificial-intelligence-ai-and-data-protection-in-schools>

## Privacy-first architecture

The LLM should not need the pupil's identity.

Example:

```text
MIS

Michael Smith
SEND information
Known classroom strategies
        ↓
Your application

pupil_847291
needs_visual_support: true
needs_chunked_instructions: true
        ↓
LLM

"Pupil requires visual representations
and chunked instructions.

Generate an appropriate scaffold for
today's learning objective."
```

Identity stays inside the secure application boundary.

The generative model receives only the information necessary to generate the educational adaptation.
