# A/B Testing — Designing the Data-Generating Process

## Objective
I estimated the effect of a job training program and a mobile game change using randomized experiments, and I showed how selection bias, significance testing, and power analysis affect what those experiments can tell us.

## Methodology
- Loaded the LaLonde NSW job training experiment (445 people: 185 trainees and 260 controls) and computed the experimental average treatment effect (ATE).
- Simulated an observational comparison group and split the gap between the two estimates as Observational ATE = True ATE + Selection Bias.
- Ran a permutation test with 9,999 shuffles to test whether the ATE differs from zero.
- Built a bootstrap BCa 95% confidence interval for the ATE.
- Ran a power analysis to find the power of this study and the sample size needed to detect three different dollar effects.
- Applied the same tests to the Cookie Cats mobile game A/B test (90,189 players, with the gate at level 30 or level 40, measuring Day-1 retention).
- Wrote a sample-size function, `n_needed()`, checked its output against the power analysis, and used it to size a rerun of the Cookie Cats test.

## Key Findings
- **NSW experiment:** Trainees earned $[YOUR VALUE] more than controls (permutation p = [YOUR VALUE], 95% CI $[YOUR VALUE] to $[YOUR VALUE]).
- **Selection bias:** The simulated comparison group gave an ATE of $[YOUR VALUE], which differs from the experimental estimate by the amount of selection bias.
- **Cookie Cats:** Day-1 retention differed by [YOUR VALUE] percentage points between the level 30 and level 40 groups (p = [YOUR VALUE]).
- **Rerun sizing:** A rerun of the Cookie Cats test would need [YOUR VALUE] players per group.
