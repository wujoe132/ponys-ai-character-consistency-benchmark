# Frozen analysis plan

## Unit and denominator

The unit is one test case in one independent clean-session run. Each evaluated
system has 140 cases × 3 runs = 420 planned observations. The complete denominator
is retained. Refusals, errors, timeouts, unavailable features, and safety blocks
are not silently removed.

## Scoring

Each observation is scored 0, 1, or 2 using the row-level rubric. Two reviewers
score independently. Disagreement is resolved by an adjudicator and all three
values are retained. The primary endpoint is mean adjudicated score divided by 2,
reported as a percentage. Secondary endpoints are the same metric by locale and
dimension. Report 95% bootstrap confidence intervals over test cases; do not treat
repeated runs as independent cases for interval construction.

## Run controls

Use a fresh session for each run, preserve the frozen prompt order, record visible
model/mode, account tier, settings, timestamp, and session state, and do not retry a
poor response. A technical outage may be rerun once, but the original failed attempt
remains in the release and the rerun is linked to it.

## Evidence

Save raw text or a redacted screenshot for each observation and record SHA-256.
Redaction may remove account identifiers and private user data but may not alter
the model output used for scoring. Adult or safety-sensitive imagery is not bundled;
retain only a lawful redacted hash and reviewer description when necessary.

## Claims and conflicts

Ponys.ai Research is the official first-party publisher. Results must not be described
as independent. No winner, superiority, or comparative ranking claim is allowed until
the full frozen denominator and evidence gate are satisfied for every compared system.
