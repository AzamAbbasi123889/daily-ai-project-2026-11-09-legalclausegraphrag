# Implementation Checklist

Build the application yourself using `PROJECT_BRIEF.md`.

## Initial setup

- [ ] Read the project specification.
- [ ] Review the architecture and data model.
- [ ] Create a Python virtual environment.
- [ ] Install and pin the required dependencies.
- [ ] Configure credentials through environment variables.
- [ ] Review the data privacy and security requirements.

## Project acceptance criteria

- [ ] User can upload up to 10 contracts in a single session
- [ ] Each uploaded contract yields ≥95% clause extraction accuracy vs. manual annotation
- [ ] All clause nodes are searchable via vector index and appear in Neo4j with proper relationships
- [ ] Response latency ≤ 1.5 s for 5‑clause queries
- [ ] Returned result includes clause ID, contract name, and graph path (e.g., "Amendment → inherits from")
- [ ] Confidence score is provided
- [ ] Answer shows clickable clause IDs that open a modal with full clause text
- [ ] Citations are accurate for ≥90% of test queries (manual verification)
- [ ] Set up repo, Docker compose with Postgres, Neo4j, FastAPI skeleton
- [ ] Implement PDF/DOCX upload & clause splitter (regex + spaCy)
- [ ] Generate embeddings via sentence‑transformers and store in pgvector
- [ ] Create Neo4j nodes & basic "belongs_to" relationship
- [ ] Build LangChain vector retriever
- [ ] Integrate Neo4j traversal to enrich results
- [ ] Expose /api/v1/query endpoint with streaming response
- [ ] Add Supabase JWT auth
- [ ] Create React UI with query box & answer display
- [ ] Implement citation modals linking to clause view
- [ ] Write unit & integration tests (pytest, playwright)
- [ ] Add OpenTelemetry instrumentation
- [ ] Unit tests for document parser, embedding generator, and Neo4j writer
- [ ] Integration tests for /api/v1/query verifying response schema and citation links
- [ ] End‑to‑end UI tests with Playwright covering upload → query → citation click flow
- [ ] Security tests: JWT validation, SQL/graph injection attempts
- [ ] Dockerize services; use docker‑compose for local dev
- [ ] Push images to GitHub Container Registry via Actions
- [ ] Deploy to Fly.io (or Render) with managed Postgres & Neo4j add‑on
- [ ] Configure HTTPS via Fly.io certificates; environment variables for API keys

## Before completion

- [ ] Implement the planned MVP features.
- [ ] Add unit and integration tests.
- [ ] Run the test suite.
- [ ] Measure the evaluation metrics in the brief.
- [ ] Record actual results and known limitations.
- [ ] Document setup and deployment.
- [ ] Update the README to reflect the implemented features.
- [ ] Add only verified outcomes to your resume.
