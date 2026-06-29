# Code Smells
- God service / util dumping ground; long parameter lists.
- Primitive obsession (use value objects).
- Anemic domain (logic leaked into services) — push behaviour into the domain.
- Leaky abstractions (ORM types crossing layers).
- Boolean flags driving branching (split responsibilities).
- Duplicated validation across layers.
- Magic numbers/strings; deep nesting; large functions.
Refactor toward the templates in `06-templates/*`.
