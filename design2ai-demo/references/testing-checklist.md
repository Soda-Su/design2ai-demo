# Testing Checklist

Use this in Week 6 or whenever the user asks whether the demo is reliable enough to share.

## Minimum AI Demo Test Set

Run:

- 3 realistic tasks
- 2 failure samples
- 1 manual takeover or fallback scenario

## Test Categories

### Input Reality

Check:
- Does the input look like what the target user would actually provide?
- Is the input too clean compared with real life?
- Can the user submit partial, messy, or ambiguous input?

### Output Usefulness

Check:
- Is the output actionable?
- Does it preserve domain-specific constraints?
- Does it show reasoning or evidence when needed?
- Can the user edit, copy, or apply the result?

### Failure Behavior

Check:
- Empty input
- Too-long input
- Irrelevant input
- Contradictory input
- Model returns weak or malformed output
- API failure or rate limit

### Human Override

Check:
- Can the user revise the prompt or input?
- Can the user ignore or edit AI suggestions?
- Is there a clear next step after a weak output?

### Cost and Latency

Check:
- Does the demo feel slow?
- Does loading feedback appear quickly?
- Is the model call scoped enough to avoid waste?
- Is the learner aware of approximate cost risk?

## Portfolio Testing Notes Template

```markdown
## Test Notes

Target user:

Task 1:
- Input:
- Expected behavior:
- Actual behavior:
- Fix:

Task 2:

Task 3:

Failure sample 1:

Failure sample 2:

Manual takeover:

Top fixes before sharing:
1.
2.
3.
```
