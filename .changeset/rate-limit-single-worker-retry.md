---
"openwiki": patch
---

Retry a rate-limited page instead of skipping it when the run has a single page worker. A pool that is already down to one worker has no concurrency to hand back, so the throttled page is now retried like any other failure instead of being dropped from the update.
