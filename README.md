# Brandon Connell

**Software engineer | Game engines, systems programming, native software, and GPU architecture**

I build a mix of software: native game engines and tools, gameplay systems, GPU architecture research, backend APIs, and lead generation software. What keeps me interested is figuring out how the underlying systems work and making them efficient and dependable. I care about performance on ordinary hardware, clear interfaces, repeatable validation, and being able to show what actually works.

I work with C, C++, C#, .NET, Java, Python, and TypeScript. I choose languages for the work rather than defining myself by one of them. My experience also includes web and backend development, especially software built around a specific business problem. General website development and e-commerce aren't the direction I'm looking to pursue.

**Open to remote, full-time software engineering opportunities.** I'm most interested in game engines and games, rendering, native and systems development, GPU-related engineering, and simulation. I'm also interested in moving into robotics and developing experience with sensors, controls, and physical systems. Purpose-built backend services and lead generation platforms remain part of the work I enjoy.

[Selected work](#selected-engineering-work) · [How I work](#engineering-approach) · [Contact](#contact)

## Selected engineering work

The projects below are publicly accessible and are presented with their actual maturity and limitations.

### [TriageDock](https://github.com/bconnell/TriageDock) · Python, Django, PostgreSQL, React

An incident intake and response application. It groups repeat alerts under one incident, records status changes, and lets operators review, acknowledge, and resolve incidents through a browser. Celery and Redis handle optional notification attempts, with failures recorded rather than hidden.

**Maturity:** [v1.0.0 released](https://github.com/bconnell/TriageDock/releases/tag/v1.0.0) for local evaluation. It is not an internet-ready monitoring or paging service.

**What to inspect:** [Dashboard screenshot](https://github.com/bconnell/TriageDock/blob/main/docs/screenshots/dashboard.webp) · [Engineering walkthrough](https://github.com/bconnell/TriageDock/blob/main/docs/PROJECT_OVERVIEW.md) · [API contract](https://github.com/bconnell/TriageDock/blob/main/docs/API.md)

### [OnceLedger](https://github.com/bconnell/OnceLedger) · Java 21, Spring Boot, PostgreSQL

A demonstration transfer ledger for handling repeated requests safely. PostgreSQL coordinates requests sharing an idempotency key and commits balance updates, ledger entries, and the saved response in one transaction. A matching retry reuses its receipt; a different request with the same key is rejected.

**Maturity:** Local technical demonstration with simulated credits, not a payment service. The full Maven and Testcontainers suite is provided but has not yet been verified by a completed run.

**What to inspect:** [Application and API](https://github.com/bconnell/OnceLedger#readme) · [Transaction and failure model](https://github.com/bconnell/OnceLedger/blob/main/docs/architecture.md) · [Local verification](https://github.com/bconnell/OnceLedger#local-quality-gates)

### [LogSpindle](https://github.com/bconnell/LogSpindle) · Rust, CLI, JSONL

A lightweight command-line tool for filtering and summarizing structured application logs without a database or server. The source handles timestamp and severity filters, standard input, malformed records, and deterministic error summaries. Local text validation, integration tests, and release verification scripts are included.

**Maturity:** Source implementation merged. Rust compilation, integration tests, and release behavior have not yet been verified; dependency lockfile generation remains pending.

**What to inspect:** [CLI and input format](https://github.com/bconnell/LogSpindle#readme) · [Rust source](https://github.com/bconnell/LogSpindle/blob/main/src/main.rs) · [CLI tests](https://github.com/bconnell/LogSpindle/blob/main/tests/cli.rs) · [Validation contract](https://github.com/bconnell/LogSpindle/blob/main/docs/VALIDATION.md)

### [GroundedTrail](https://github.com/bconnell/GroundedTrail) · Python, FastAPI, LangChain, PostgreSQL/pgvector

A document retrieval and evidence workspace for indexing Markdown and plain text, finding source passages, and inspecting citations. It includes a browser interface, optional model-generated answers, and reference-based retrieval evaluation.

**Maturity:** Local technical demonstration. API tests cover the temporary backend; a completed PostgreSQL integration test run is not yet documented.

**What to inspect:** [Application screenshot](https://github.com/bconnell/GroundedTrail/blob/main/docs/screenshots/workspace.png) · [Overview and setup](https://github.com/bconnell/GroundedTrail#readme) · [Evaluation cases](https://github.com/bconnell/GroundedTrail/blob/main/eval/questions.json)

### [Lead Intake API](https://github.com/bconnell/lead-intake-api) · Java 21, Spring Boot, PostgreSQL

A REST API for creating, searching, updating, and reporting on leads. It separates HTTP contracts, services, persistence, and database migrations. The repository documents validation with H2-backed tests and PostgreSQL integration tests using Testcontainers.

**What to inspect:** [API and setup](https://github.com/bconnell/lead-intake-api#readme) · [Validation contract](https://github.com/bconnell/lead-intake-api/blob/main/docs/VALIDATION.md) · [Portfolio scope and limits](https://github.com/bconnell/lead-intake-api/blob/main/docs/PORTFOLIO_COMPLETENESS.md)

### [CGX1](https://github.com/bconnell/CGX1) · GPU architecture, RTL, C++

An engineering reference for a compact GPU architecture, covering execution, memory, scheduling, graphics, power, and the prototype path. The repository includes design contracts and validation material.

**Maturity:** Architectural and prototype design. **No custom ASIC has been fabricated.** Performance figures are targets, not measured hardware results.

**What to inspect:** [Engineering specification](https://github.com/bconnell/CGX1/blob/main/docs/ENGINEERING_SPEC.md) · [Project status](https://github.com/bconnell/CGX1/blob/main/docs/STATUS.md) · [Validation](https://github.com/bconnell/CGX1/blob/main/docs/VALIDATION.md)

### [Henka Engine](https://github.com/bconnell/HenkaEngine) · C17, native runtime and editor

An early-stage game engine with a native editor, rendering, terrain, physics, asset authoring, persistence, and headless runtime foundations. Its documentation distinguishes working capabilities from unfinished or planned features.

**Maturity:** Active engine development, not a finished commercial game engine.

**What to inspect:** [Capability matrix](https://github.com/bconnell/HenkaEngine#capability-matrix) · [Current capabilities](https://github.com/bconnell/HenkaEngine/blob/main/docs/current-capabilities.md) · [Build instructions](https://github.com/bconnell/HenkaEngine/blob/main/docs/building.md)

### [Rapid Robot Job Assistant](https://github.com/bconnell/Rapid-Robot-Job-Assistant) · TypeScript, React, Chromium extensions

A local-first browser extension for reviewing job listings and preparing application field suggestions. Its form-fill process requires user approval and keeps final application submission manual. The implementation emphasizes validation of persisted data, safe field handling, and page identity checks.

**What to inspect:** [Overview and usage](https://github.com/bconnell/Rapid-Robot-Job-Assistant#readme) · [Roadmap and known limits](https://github.com/bconnell/Rapid-Robot-Job-Assistant/blob/main/docs/roadmap.md)

## Engineering approach

- **Boundaries first.** Define what a component owns, what callers can assume, and how invalid input is handled.
- **Test evidence over optimistic claims.** Keep validation instructions, limitations, and failure cases visible. A design target is not a benchmark, and a test plan is not a passing test.
- **Practical performance.** Favor restrained dependencies, maintainable code, and support for machines without expensive hardware.
- **Non-destructive changes.** Use source control, reviews, reproducible builds, and targeted regression checks to protect existing work.

The repositories are independent projects with different release stages and contribution policies. Check each README for its current scope, licensing, and setup instructions.

## Contact

I'm based in Illinois and open to **remote software engineering roles** involving game engines, gameplay systems, native applications, rendering, graphics, simulation, and systems programming. I'm also interested in growing into robotics, and I remain open to substantial backend or lead generation engineering work.

- **Email:** [brandon@brandonconnell.com](mailto:brandon@brandonconnell.com)
- **LinkedIn:** [Brandon Connell](https://www.linkedin.com/in/brandon-connell-b317a81b/)

You can explore the [public repositories](https://github.com/bconnell?tab=repositories) for additional work.
