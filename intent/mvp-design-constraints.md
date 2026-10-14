# MVP intent: design constraints

## SEND and pupil context

The eventual product should combine assessment information with relevant pupil context.

Possible sources include:

- SEND information
- EAL information
- teacher observations
- SENCO guidance
- pupil passports
- known helpful classroom strategies
- historic assessment information

However, the MVP must **not infer teaching strategies directly from a diagnostic label**.

Avoid:

```text
Pupil has ADHD
      ↓
System automatically selects work
```

Prefer:

```text
Known classroom need
        +
Current assessment evidence
        ↓
Suggested adaptation
        ↓
Teacher approval
```

For the MVP, any additional pupil context should be entered manually as teaching-relevant information such as:

> Benefits from visual representations.

or:

> Written instructions should be chunked.

This intent does not require storage or processing of formal SEND diagnoses.

## Misconception model

A core part of the product is identifying *why* an answer may be wrong rather than only calculating a score.

Example:

```text
Question:
1/2 + 1/4 = ?

Response:
2/6

Possible misconception:
The pupil may be adding denominators as well as numerators.
```

Misconception identification must be based on known response patterns defined for the supported diagnostic content.

The MVP must not rely on unrestricted LLM speculation to invent a misconception from arbitrary pupil responses.

Where evidence is insufficient, the platform should say so.

Example:

> No specific misconception can be identified from the available responses.

## Resource model

The MVP should avoid producing one completely different worksheet for every child.

The preferred model is:

```text
Core task
   +
Optional scaffold(s)
   +
Optional reasoning / greater-depth extension
```

Example:

```text
CORE TASK
Q1–Q8

Available adaptations:
- worked example
- place-value representation
- number-bond prompt
- partially completed first question
- chunked instructions

Further reasoning:
- explain your method
- spot the mistake
- prove your answer
```

The diagnostic determines which adaptations are suggested to the teacher.

## Data model — conceptual

The MVP needs to represent the relationship between:

```text
Pupil
  ↓
Diagnostic response history

Learning objective
  ↓
Prerequisite concepts
  ↓
Diagnostic questions
  ↓
Known response / misconception patterns
  ↓
Adaptation strategies
```

A pupil's state should be evidence-based and update as new diagnostic responses are recorded.

The exact technical schema is a construction decision and is not prescribed by this intent.

## AI usage

AI may be useful for:

- explaining assessment evidence to teachers
- turning structured diagnostic findings into concise summaries
- adapting wording or presentation of an approved scaffold
- generating variations of safe, constrained practice questions
- producing teacher-facing explanations

AI should **not** be the sole source of truth for:

- curriculum dependency relationships
- whether prerequisite knowledge is secure
- recognised misconception definitions
- SEND provision
- high-stakes pupil decisions

The core diagnostic logic should be grounded in structured curriculum and assessment data.

## Privacy principles

Although the MVP does not integrate with an MIS, its architecture should not create an obvious dead end for future school deployment.

Principles:

- minimise pupil data
- avoid sending pupil names to an LLM where identity is unnecessary
- separate pupil identity from AI prompt context
- do not use pupil data to train third-party foundation models
- make teacher-facing evidence auditable
- design for role-based access in future
- retain human approval for recommendations

Example future pattern:

```text
School system:
Michael Smith

Application:
pupil_847291
needs_visual_support: true

LLM context:
"Pupil benefits from visual representation."
```
