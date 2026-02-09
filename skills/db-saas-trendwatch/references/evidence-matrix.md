# Evidence Matrix

## Evidence levels

| Level | Label | Minimum evidence | Typical status | Weight |
|-------|-------|------------------|----------------|--------|
| A | Verified | Docs + postmortem/release note + constraints stated | Production | High |
| B | Validated | Engineering blog or conference talk with details | Limited production | Medium |
| C | Anecdotal | Single blog post or interview only | Unverified | Low |

## Validation checklist
- Is there a primary source (engineering blog, postmortem, release note)?
- Are the constraints stated (region, scale, tier)?
- Is the claim reproducible or quantified?
- Is there independent confirmation?

## Notes
- Do not treat hiring signals as confirmed architecture changes.
- Downgrade to C if evidence is marketing-only.
