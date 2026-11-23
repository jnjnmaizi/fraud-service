# Lab 5: CI/CD Benchmarks

## GitHub Actions Performance

| Job | First Run (#1) | Latest Run (#6) |
|---|---|---|
| lint | 44s | 30s |
| test | 47s | 38s |
| image-smoke | 2m 24s | 37s |
| publish | 31s | Skipped |
| Total | 3m 50s | 1m 37s |

## Analysis

All required checks passed in both runs.

The image-smoke job improved from 144 seconds to
37 seconds, a reduction of approximately 74%.

Docker BuildKit caching likely contributed to this
improvement by reusing previously built image layers.

Run #6 was manually triggered, so the publish job
was skipped. Therefore, the total pipeline durations
are not directly comparable.

## Conclusion

Automated CI/CD validates code quality, tests,
architecture constraints, and Docker functionality.

Caching can reduce build time while preserving
the same quality checks.
