# secrets-unmasking

Exploring "techniques" to disable secrets-masking on CircleCI


## Brief

CircleCI masks secrets from **build outputs** as a sane default.
Ref: https://circleci.com/docs/env-vars/#secrets-masking

At times, users may not want a specific output's value to be masked, depending on the situation.

## Techniques

We explore possible techniques (workarounds) here.

### 1. Base64

By encoding an output (e.g., Base64), this "prevents" the value from being masked.

### 2. Artifacts

Note that [secrets' values are not masked in the artifact contents](https://circleci.com/docs/env-vars/#secrets-masking).

Hence, this can be another workaround for teams.
