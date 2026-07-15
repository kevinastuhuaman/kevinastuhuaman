# Structured review: PR #18

## Scope

This PR changes only `assets/trackly-demo-preview.gif`. It moves the source-video start time from 5.0 seconds to 3.5 seconds while preserving the 13.5-second ending.

## Binary verification

- Dimensions: 800 x 450
- Frame rate: 10 fps
- Frame count: 100
- Duration: 10.0 seconds
- Size: 8,659,385 bytes (below GitHub's 10 MB GIF limit)
- SHA-256: `e93f7be6ddfda0c97ae1b1e279d2e9d23c9bcd1438153e79d91f6733b1b75295`

## Visual verification

A half-second contact sheet was inspected against the source video. The new opening contains these consecutive beats:

1. `Looking`
2. `Looking for a`
3. `Looking for a job`
4. `shouldn't feel like`
5. `a full-time job.`

The existing phone-notification, positioning, and Trackly ending frames remain in the loop.

## Risk review

- No README markup, links, copy, or layout changed.
- The GIF remains below GitHub's documented upload limit.
- The output preserves the existing 16:9 aspect ratio and 10 fps playback rate.
- `git diff --check` passes.

## Conclusion

No blocking issues found. The binary change fixes the truncated opening without changing the surrounding profile structure.
