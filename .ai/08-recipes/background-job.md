# Recipe: Background Job (BullMQ)
1. Define a queue; producers add jobs with idempotency keys.
2. Worker processes with concurrency limits + retry/backoff.
3. Persist job outcome; emit domain/integration events on completion.
4. Monitor queue depth + failures (`01-rules/monitoring/README.md`). DLQ for poison jobs.
