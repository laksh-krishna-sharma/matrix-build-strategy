# Multi-Platform Matrix Build with Artifacts

This repository demonstrates a GitHub Actions matrix build that produces and uploads unique artifacts per matrix job.

## What it does

- Runs parallel jobs across multiple matrix variants (OS × Node.js versions).
- Each job generates a unique, non-empty artifact file.
- Artifacts are uploaded with the prefix `build-f777b6b-<variant>`.
- Includes a step named `matrix-f777b6b` for validation.

## How to run

Push a commit to trigger the workflow automatically. You can also run it manually from the Actions tab using "Run workflow".

## Verify

1. Go to **Actions** → select the workflow run.
2. Confirm at least 3 matrix jobs succeeded.
3. In the run view, open the **Artifacts** section and verify artifacts with names like:
   - `build-f777b6b-ubuntu-latest-node14`
   - `build-f777b6b-windows-latest-node18`
   - etc.
4. Download an artifact and confirm it contains text (non-empty).

## Contact

For questions: `23f3002362@ds.study.iitm.ac.in`
