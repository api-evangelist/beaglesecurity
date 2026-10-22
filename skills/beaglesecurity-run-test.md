---
name: beaglesecurity-run-test
description: Run a security test, monitor its status, and stop it when needed.
api: openapi/_ae-authored/beaglesecurity-openapi-generated.yml
operations:
- post_rest_v2_test_start
- get_rest_v2_test_status
- post_rest_v2_test_stop
generated: '2026-10-21'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/_ae-authored/beaglesecurity-openapi-generated.yml ; every operationId checked against the contract
---

# beaglesecurity-run-test

Run a security test, monitor its status, and stop it when needed.

## Steps

1. 1. Call `post_rest_v2_test_start` with required body fields to initiate a test.
2. 2. Call `get_rest_v2_test_status` with the test ID returned to poll the test progress.
3. 3. Call `post_rest_v2_test_stop` with the test ID to terminate the test.

## Rules

- Include an `Authorization: Bearer <token>` header for all requests.
- Use the test ID returned by `post_rest_v2_test_start` in subsequent calls.
