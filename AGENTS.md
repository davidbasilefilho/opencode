# AGENTS.md

## Interaction Guidelines
Be direct, succinct, and objective, yet maintain a warm tone. Favor headings and topics over lists; use lists only when nested within a topic to organize specific details. 
**Do not use em dashes**; if a sentence would normally rely on an em dash, restructure it so the dash is unnecessary.

### Response Scope
Adhere strictly to the specific needs of the request. Provide long, multi-section responses only for complex inquiries. For simple or specific questions, provide brief and immediate answers without unnecessary filler.

## Research and Knowledge
- **Trust User Knowledge**: Assume the user's premises are accurate. If a request involves unfamiliar concepts, research them thoroughly to acquire context rather than dismissing them.
- **Documentation Retrieval**: Prioritize the use of `context7` to fetch documentation. Only use web search for documentation if `context7` is unavailable or insufficient.
- **Proactive Context**: Always verify the latest API usage and breaking changes for the "Modern Tooling Stack" before writing implementation code.

## Modern Tooling Stack
Adopt modern, high-performance tooling by default. Refrain from using legacy equivalents unless explicitly requested.

### JavaScript & TypeScript Ecosystem
- **Language & Paradigm**: Use TypeScript exclusively; never write plain JavaScript. Avoid OOP patterns (classes, inheritance) in favor of plain objects, functions, and composition.
- **Runtime & Execution**: Use `bun` for the runtime and `bun x --bun` for package execution. Use Bun Shell (`$`) for shell commands instead of Node.js child process methods.
- **Frameworks & Logic**: Use `tanstack start` for full-stack applications and `effect-ts` for structured side-effect management, concurrency, and error handling.
- **Backend & State**: Use `convex` for backend infrastructure and state synchronization. Use `tanstack store` for local state management instead of built-in React Context, Zustand, or Redux Toolkit.
- **Tooling**: Use `vitest` for testing and `biome` for linting and formatting.

### Python & Environment
- **Package Management**: Use `uv` for all Python package management tasks.
- **Version Management**: Use `jdx mise` for version management and task running across all environments.

### System & CLI Tools
- **Linux Environment**: Use `ripgrep` (`rg`) instead of `grep`, `fd` instead of `find`, and `bunx --bun` instead of `npx` for all search, discovery, and package execution operations.

## Coding Standards
Produce code that is minimal, readable, and performant.

### Documentation and Readability
- **Self-Documenting Logic**: Do not use comments unless the logic is inherently cryptographic or mathematically obscure. Rely on descriptive variable and function naming.
- **No Magic Numbers**: Define constants for all numeric or string literals. Logic must reference these identifiers rather than raw values.

### API Design Patterns
- **Dual Getter-Setter Functions**: Implement state management using overloaded functions. A call with no arguments returns the value; a call with an argument updates it (e.g., `property()` to get, `property(newValue)` to set).

### User Experience
- **Focus**: Ensure code provides a superior interface, focusing on high-fidelity UI/UX for end-users and a seamless Developer Experience (DX) for maintainers.
