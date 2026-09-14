# Onyx Subsystem Analysis & Implementation Report

## 1. Subsystem Architecture & Tracing
- **UI Layer:** web/src/app/admin/connectors/github/page.tsx
- **API Controller:** backend/onyx/server/manage/connectors.py
- **Background Scheduler:** backend/onyx/background/indexing/run_indexing.py
- **Connector Logic:** backend/onyx/connectors/github/connector.py
- **Vector Pipeline:** backend/onyx/indexing/indexing_pipeline.py

## 2. Code Modification
Implemented `_fetch_with_exponential_backoff` in `backend/onyx/connectors/github/connector.py` to handle GitHub API rate limit (HTTP 429) errors gracefully with exponential delays.

## 3. AI Workflow
Used Cursor AI to trace dependencies across the codebase and refactor error-handling logic efficiently.