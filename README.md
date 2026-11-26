## Hi, I'm Unmesh Pawar

**.NET Backend Developer** · C# · ASP.NET Core Web API · EF Core · SQL Server · AI-integrated applications

I build backend services and REST APIs with C#, ASP.NET Core and SQL Server, and I integrate large language
models into business software in a way that stays predictable: validated outputs, deterministic fallbacks and AI
that suggests rather than decides. I'm based in Pune, India and currently work at Aligned Automation.

Earlier work in process automation (Blue Prism RPA and Tulip frontline apps) shaped how I approach business
workflows: validate early, report every error clearly, and keep an audit trail.

### Tech stack

| Area | Tools |
|---|---|
| Backend (.NET) | C#, ASP.NET Core Web API, Entity Framework Core, SQL Server, background services, FluentValidation, Serilog |
| Backend (Python) | Python, FastAPI, Pydantic, SQLAlchemy (async), PostgreSQL + pgvector, Alembic |
| AI integration | OpenAI and Anthropic APIs, retrieval-augmented generation, embeddings, structured-output validation, prompt versioning |
| Frontend | React, TypeScript |
| Testing and delivery | xUnit, WebApplicationFactory, pytest, Docker, docker compose, GitHub Actions |

### Featured projects

| Project | What it does | Stack |
|---|---|---|
| [**mdr-document-platform**](https://github.com/unmeshpawar7-cpu/mdr-document-platform) | Validates engineering Master Deliverables Register (MDR) CSV files in the background, reports every problem with a stable code and saves the valid rows; a Python sidecar adds advisory AI classification | ASP.NET Core 8, EF Core, SQL Server, FastAPI |
| [**workflow-orchestrator**](https://github.com/unmeshpawar7-cpu/workflow-orchestrator) | Runs multi-step DAG workflows reliably: leased step execution, retries with backoff, saga compensation, schedules and dead letters | ASP.NET Core 8, EF Core, SQL Server, Redis |
| [**ai-rule-engine**](https://github.com/unmeshpawar7-cpu/ai-rule-engine) | Versioned, explainable business rules evaluated deterministically with a per-condition trace; AI drafts rules from plain English but never publishes or runs them | ASP.NET Core 8, EF Core, SQL Server |
| [**ai-requirements-agent**](https://github.com/unmeshpawar7-cpu/ai-requirements-agent) | Turns requirement documents into traceable requirements, user stories, test cases and an OpenAPI spec using RAG with source citations | FastAPI, PostgreSQL + pgvector |
| [**resume-job-matching**](https://github.com/unmeshpawar7-cpu/resume-job-matching) | Explainable resume-to-job matching with a reproducible score and evidence breakdown; the LLM explains the score but cannot change it | FastAPI, PostgreSQL + pgvector |

Each repository has architecture notes, architecture decision records, setup instructions, API examples and a
GitHub Actions pipeline that runs the test suite.

### How I integrate AI

- **Deterministic first.** Scoring, validation and rule evaluation are plain code; the model adds suggestions,
  drafts or explanations on top.
- **Validate everything the model returns.** Responses are parsed into typed schemas, checked against known values
  and retried with the validation errors before falling back.
- **Grounded output.** Generated items must cite the source text they came from; uncited items are dropped.
- **Works without an API key.** Each AI feature has an offline provider, so the system runs and tests run with no
  external calls.
- **Observable and private.** Prompt versions, model, attempts and token usage are logged; document text, personal
  data and keys are not.

### Currently learning

- OpenTelemetry tracing across APIs, background workers and sidecar services
- Durable messaging for background work (Azure Service Bus)
- Testcontainers for running integration tests against real SQL Server and PostgreSQL

### Connect

[LinkedIn](https://www.linkedin.com/in/unmeshpawar7/) · [GitHub](https://github.com/unmeshpawar7-cpu)
