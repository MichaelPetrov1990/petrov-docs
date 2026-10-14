# MVP intent: build the adaptive teaching MVP

## Intent

Create an MVP for a primary-school adaptive teaching platform that helps a teacher understand what pupils know before a lesson, identify likely knowledge gaps or misconceptions, and recommend targeted adaptations so that pupils can work towards the same ambitious learning objective.

The MVP should prove the core educational loop:

> Assess → Diagnose → Recommend adaptation → Teach

It should not attempt to build the full commercial platform or integrate with school MIS systems yet.

## Problem statement

Teachers need to adapt teaching to pupils' current understanding while maintaining ambitious learning objectives for all pupils.

Today, this commonly requires the teacher to manually combine:

- curriculum objectives
- prior assessment information
- pupil responses
- knowledge of common misconceptions
- SEND/EAL considerations
- classroom observations
- suitable scaffolds and representations

Existing adaptive-learning platforms typically assess pupils and then direct them into personalised digital content.

Existing AI resource generators typically create worksheets or differentiated resources from a learning objective but do not have a reliable model of what individual pupils already know.

The opportunity is to connect these workflows for the physical classroom.

The platform should help answer:

1. What prerequisite knowledge does today's learning objective require?
2. Which prerequisites has each pupil demonstrated?
3. What likely misconception or knowledge gap is present?
4. What is the smallest useful adaptation that could help the pupil access the same learning objective?
5. Which pupils have sufficiently similar needs that the teacher can support them together?
6. When is a pupil ready for reduced scaffolding or greater depth?

## Target user

### Primary user

A UK primary classroom teacher.

For the MVP, assume:

- one teacher
- one manually created class
- primary mathematics
- no school-wide administration
- no live MIS integration

### Future users

Potential later users include:

- SENCOs
- subject leaders
- school leaders
- teaching assistants
- MAT leaders

These are not required for this intent.

## Product principle

The product must support **adaptive teaching**, not create fixed ability groups or permanently simplified work.

All pupils should work towards the same intended learning objective wherever appropriate.

Adaptation may change:

- scaffolding
- representations
- manipulatives
- worked examples
- language demand
- chunking
- prompts
- sentence stems
- question sequencing
- teacher check-ins
- depth of reasoning
- timing of scaffold removal

The platform must not default to:

```text
Low group    → easy worksheet
Middle group → normal worksheet
High group   → hard worksheet
```

Instead:

```text
Same learning objective
        ↓
Different current barriers
        ↓
Targeted temporary adaptations
        ↓
Teacher reviews and applies them
```
