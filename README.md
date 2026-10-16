# Brandon Connell

**Software engineer | Backend systems, native software, and performance-conscious engineering**

I build software that has to work outside the happy path. My public work spans backend APIs, C and C++ systems, hardware architecture research, native tooling, and practical browser software. I care about clear interfaces, repeatable validation, accurate documentation, and making failure states visible instead of hiding them.

**Open to remote, full-time software engineering opportunities.** My strongest professional focus is C#, .NET, backend systems, and systems-level problem solving. I also work in Java, C17, C++, and TypeScript.

[Selected work](#selected-engineering-work) · [How I work](#engineering-approach) · [Contact](#contact)

## Selected engineering work

The projects below are publicly accessible and are presented with their actual maturity and limitations.

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

I am based in Illinois and interested in **remote software engineering roles** involving backend development, .NET/C#, systems programming, and technical problem solving.

- **Email:** [brandon@brandonconnell.com](mailto:brandon@brandonconnell.com)
- **LinkedIn:** [Brandon Connell](https://www.linkedin.com/in/brandon-connell-b317a81b/)

You can explore the [public repositories](https://github.com/bconnell?tab=repositories) for additional work.
