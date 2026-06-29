# Indexing

- Index foreign keys and frequent filter/sort/join columns.
- Composite index column order = most selective / equality first, range last.
- Add covering indexes for hot read paths; verify with `EXPLAIN ANALYZE`.
- Use partial indexes for sparse/boolean predicates.
- Don't over-index — every index slows writes. Measure before adding.
