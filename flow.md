# Writer flow

foyer-storage/src/engine/block/engine.rs:591 enforces the queue threshold.
foyer-storage/src/engine/block/flusher.rs:237 submits and charges entries.
foyer-storage/src/engine/block/flusher.rs:350 preserves one pending submission.
foyer-storage/src/engine/block/flusher.rs:420 retries or consumes the entry.

Regression tests validate burst retention, disk recovery, oversized-entry progress and queue accounting.
