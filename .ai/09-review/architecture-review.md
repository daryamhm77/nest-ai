# Architecture Review Rubric
1. Dependency rule holds (`infra → app → domain`).
2. Bounded contexts cohesive; coupling minimized; integration explicit.
3. Aggregates correctly sized; one aggregate per transaction.
4. CQRS/events used only where justified.
5. NFRs (latency, scale, availability) addressed.
6. Failure modes + consistency strategy defined.
Flag accidental complexity and missing seams.
