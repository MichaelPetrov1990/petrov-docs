# MVP intent: risks, hypothesis and definition of done

## Known risks

### Diagnostic validity

If diagnostic questions do not accurately test prerequisite knowledge, downstream recommendations will be unreliable.

### False certainty

The platform may mistake an incorrect answer for a specific misconception.

The UI must distinguish:

- observed response
- supported inference
- uncertainty

### AI hallucination

Unconstrained generation could create unsupported pedagogical recommendations.

Structured rules and approved adaptation strategies should constrain AI output.

### Teacher workload

If the system requires excessive setup or review, it fails its primary value proposition.

### Over-scaffolding

Recommendations may inadvertently reduce challenge.

The product should prefer the minimum useful support and encourage scaffold removal when the pupil is ready.

### Privacy

Future use of MIS/SEND information substantially increases privacy and governance requirements.

This must be addressed before school-level integrations are introduced.

## Business hypothesis

Schools and teachers will value a product that uses formative assessment to turn pupil understanding into immediately actionable adaptive-teaching recommendations for the physical classroom.

The strongest positioning is not:

> AI-generated personalised worksheets.

It is:

> Adaptive teaching powered by formative assessment.

Or:

> Know what every pupil needs before you start teaching.

The differentiator is the connection between:

```text
Curriculum objective
        +
Diagnostic evidence
        +
Pupil learning context
        ↓
Misconception / barrier analysis
        ↓
Targeted adaptive-teaching recommendation
        ↓
Teacher action
```

rather than keeping pupils inside a personalised digital-learning platform.

## Definition of done

This intent is complete when the success criteria above are verified and the resulting MVP is sufficiently usable to demonstrate the complete core loop to primary teachers and collect evidence against the product-validation questions.

MIS integration and broader commercialisation are deliberately deferred to subsequent intents.
