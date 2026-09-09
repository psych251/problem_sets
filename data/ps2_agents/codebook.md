# Codebook: flanker_rt.csv

Trial-level data from a flanker task. Forty participants each completed a practice block
and two main blocks. Within each main block, participants completed 12 congruent and 12
incongruent trials in randomized order. The research question is whether response time
differs between congruent and incongruent trials.

| Column | Description |
|---|---|
| `trial_id` | Row identifier |
| `subject` | Participant identifier, `s01`–`s40` |
| `block` | `0` = practice block; `1`, `2` = main blocks |
| `condition` | `congruent` or `incongruent` |
| `trial` | Trial number within block and condition |
| `rt` | Response time in milliseconds |
| `correct` | `1` if the response was correct, `0` otherwise |

## Preprocessing rules

1. Practice trials (`block == 0`) are not analyzed.
2. Response times below 200 ms or above 3000 ms are invalid and are dropped.
3. Participants whose accuracy on valid main-block trials is below 75% are excluded entirely.
4. Response-time analyses use correct trials only.

The data are simulated; the generating script will be released with the answer key after the deadline.
