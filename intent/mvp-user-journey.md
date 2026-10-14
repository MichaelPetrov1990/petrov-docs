# MVP intent: user journey and required behaviour

## Core user journey

### 1. Create class

The teacher can create a class and add pupils manually.

No external pupil data is required for the MVP.

### 2. Select learning objective

The teacher chooses a supported primary maths learning objective.

Example:

> Add two 2-digit numbers crossing 10.

### 3. Run diagnostic

The platform presents a short diagnostic designed to test prerequisite knowledge and expose relevant misconceptions.

Example areas might include:

- number bonds
- place value
- adding ones
- understanding exchange

### 4. Analyse responses

For each pupil, the platform determines:

- which prerequisite concepts appear secure
- which appear insecure
- whether a recognised misconception pattern is present
- the evidence used to reach that conclusion

The platform must distinguish evidence from inference.

For example:

```text
Evidence:
Ben answered both non-exchange questions correctly
and both exchange questions incorrectly.

Inference:
Ben may understand place-value addition but have
a misconception around exchanging across ten.
```

### 5. Recommend adaptations

The system proposes an adaptation linked to the identified barrier.

Example:

```text
Likely barrier:
Exchanging across ten.

Suggested adaptation:
- Explicitly model the exchange.
- Make the exchange visible with place-value counters.
- Provide a worked example for the first question.
- Check understanding after question 2.
- Remove the scaffold if secure.
```

### 6. Present class view

The teacher sees a concise overview of the class.

Example:

```text
28 pupils assessed

17 — ready for planned lesson
5  — likely need support with exchanging
3  — number bonds appear insecure
3  — already secure with the objective
```

Similar needs may be presented together to make the information usable in a real classroom.

These are not permanent ability groups.

### 7. Teacher reviews

The teacher can:

- accept a recommendation
- reject it
- edit it
- choose a different adaptation

AI recommendations must remain advisory.

## Required behaviour

### Learning objective remains central

Every diagnostic question and recommended adaptation must be traceable to:

1. the selected learning objective, or
2. prerequisite knowledge required to access that objective.

### Recommendations must explain why

The system must not output unexplained recommendations.

Bad:

> Give Ben counters.

Good:

> Ben answered the questions that did not require an exchange correctly but answered both exchange questions incorrectly. Use place-value counters during modelling to make the exchange visible.

### Prefer the minimum useful adaptation

The system should avoid unnecessary support.

If a pupil can access the core task without a scaffold, it should not recommend one simply because the pupil has previously needed support.

### Scaffolds should be removable

Where appropriate, recommendations should include a point at which the teacher can check whether the scaffold is still required.

### Teacher remains responsible

The system recommends teaching actions; it does not autonomously assign educational provision or make high-stakes decisions about pupils.
