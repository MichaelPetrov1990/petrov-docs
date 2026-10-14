# Agentic workflow

## Adversarial review on every PR

After opening a PR, review it with 3 Sonnet subagents before handing it over.

- Each reviewer starts from a fresh, independent context.
- All three get the same short prompt: the PR, its base branch, any source material, read-only, and "report real defects with file:line, evidence and severity".
- Don't put your own reasoning, an angle, a checklist or a list of "deliberate" changes in the prompt. It biases the review.
- Treat each finding as a claim: verify it yourself before acting. Fix the real ones and push. Keep the PR description accurate to what changed.
