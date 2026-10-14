# Business concept: roadmap, business model and risks

## MVP

Do **not** start with MIS integration.

The MVP should prove the central educational loop first.

Suggested first version:

1. Teacher creates a class manually.
2. Teacher selects a curriculum objective.
3. Platform generates or provides a short diagnostic.
4. Pupils complete the diagnostic.
5. Platform analyses responses.
6. Platform identifies prerequisite gaps and likely misconceptions.
7. Platform groups similar needs where appropriate.
8. Platform recommends adaptations.
9. Platform generates:
   - a core task
   - optional scaffolds
   - reasoning/challenge tasks
10. Teacher reviews and downloads / prints resources.

Initial subject:

> Primary maths

Maths is likely a good starting point because:

- learning objectives are relatively structured
- prerequisite knowledge can be mapped
- misconceptions can often be modelled
- diagnostic questions can be carefully designed
- answers are easier to evaluate reliably than open-ended subjects

## Phase 2

Once the core loop works:

- Wonde integration
- automatic class rosters
- SEND/EAL information where appropriate
- teacher-defined pupil strategies
- historic assessment profiles
- adaptive recommendations based on prior lessons
- intervention suggestions
- SENCO views
- curriculum sequencing
- school-wide reporting

## Longer-term possibility

Eventually the platform could create a continually updated model of each pupil's knowledge.

For example:

```text
Fractions
├── Recognise half             ✓ Secure
├── Recognise quarter          ✓ Secure
├── Equivalent fractions       △ Developing
├── Add same denominators      ✓ Secure
└── Add different denominators ✗ Not taught
```

Combine this with today's lesson:

```text
Today's LO
        ↓
Required prerequisite knowledge
        ↓
Pupil knowledge model
        ↓
Likely barrier
        ↓
Best classroom adaptation
```

This would make the platform progressively more useful as the school uses it.

## Business model

A sensible route may be to start with a combination of software and implementation.

For example:

### Initial school setup

- curriculum mapping
- class setup
- adaptive-teaching templates
- staff training
- AI / data-protection guidance

Potential setup fee:

**£750–£3,000**, depending on scope.

### SaaS

Possible pricing could later be:

- per teacher
- per pupil
- per school
- MAT-wide licence

A school-level subscription may ultimately be easier to sell than individual teacher subscriptions because MIS integration and pupil data require institutional approval.

## Biggest risks

### 1. Diagnostic quality

If the diagnostic questions are poor, everything downstream becomes unreliable.

The assessment model may actually be the hardest and most defensible part of the product.

### 2. Hallucinated pedagogical recommendations

The AI cannot simply invent interventions.

Recommendations should ideally come from:

- validated teaching strategies
- curriculum knowledge
- school-approved approaches
- structured rules
- teacher input

rather than unrestricted LLM generation.

### 3. Teacher trust

Teachers must understand *why* a recommendation was made.

Bad:

> Give Ben manipulatives.

Better:

> Ben answered Q2 and Q4 using the correct place-value method but failed both questions requiring an exchange. Place-value counters are suggested to make the exchange explicit.

### 4. Workload

The platform must reduce workload.

If teachers have to configure 20 options before every lesson, it will fail.

The ideal interaction is probably:

```text
Choose lesson
↓
Review diagnostic
↓
Review suggested adaptations
↓
Accept / edit
↓
Teach
```

### 5. Data privacy

MIS and SEND integration raises the compliance bar considerably.

This should be treated as a core product requirement, not an afterthought.

## Strongest version of the idea

The most compelling version is not:

> AI makes personalised worksheets.

It is:

> A teacher chooses what the class is learning. The platform already understands each pupil's prior knowledge and learning needs, checks what they know before the lesson, identifies likely misconceptions, and recommends the smallest adaptations necessary for every pupil to access the same ambitious learning objective.

That combines:

- assessment
- curriculum
- adaptive teaching
- SEND awareness
- teacher judgement
- AI
- school data

into one coherent product.
