# Deferred writer entry

On a failed insertion into a nonempty buffer, preserve one pending cache entry and retain its submit-queue charge. Stop receiving further entries until the pending entry is consumed. A failure on an empty buffer still follows the existing drop path, preventing oversized-entry livelock. No buffer sizes, public APIs or dependency versions change.
