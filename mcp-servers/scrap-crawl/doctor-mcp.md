# Doctor MCP Server

**Referenz:** [https://github.com/sisig-ai/doctor](https://github.com/sisig-ai/doctor)

🩺 Doctor

Python Tests codecov License: MIT

Doctor is a system that lets LLM agents discover, crawl, and index web sites for better and more up-to-date reasoning and code generation. 🕸️🔍🧠
🌟 Overview

Doctor provides a complete stack for:

    🕷️ Crawling web pages using crawl4ai
    ✂️ Chunking text with LangChain
    🧩 Creating embeddings with OpenAI via litellm
    💾 Storing data in DuckDB with vector search support
    🚀 Exposing search functionality via a FastAPI web service
    🔌 Making these capabilities available to LLMs through an MCP server

🧩 Components

    DuckDB 📊: Database for storing document data and embeddings with vector search capabilities
    Redis 📬: Message broker for asynchronous task processing
    Crawl Worker 🕸️: Processes crawl jobs, chunks text, creates embeddings
    Web Server 🌐: FastAPI service exposing endpoints for fetching, searching, and viewing data, and exposing the MCP server

🛠️ Setup
Prerequisites

    🐳 Docker and Docker Compose
    🐍 Python 3.10+
    📦 uv (Python package manager)
    🔑 OpenAI API key

Installation
📥 Clone this repository
🔐 Set up environment variables:

export OPENAI_API_KEY=your-openai-key

🚀 Run the stack:

docker compose up

🚀 Usage

    📝 Go to http://localhost:9111/docs to see the OpenAPI docs
    🕸️ Look for the /fetch_url endpoint and start a crawl job by providing a URL
    📊 Use /job_progress to see the current job status
    🔌 Configure your editor to use http://localhost:9111/mcp as an MCP server

Web API

    📤 POST /fetch_url: Start crawling a URL
    🔍 GET /search_docs: Search indexed documents
    📈 GET /job_progress: Check crawl job progress
    📋 GET /list_doc_pages: List indexed pages
    📄 GET /get_doc_page: Get full text of a page

MCP Integration

Ensure that your Docker Compose stack is up, and then add to your Cursor or VSCode MCP Servers configuration:

"doctor": {
    "type": "sse",
    "url": "http://localhost:9111/mcp"
}

🧪 Testing

Doctor uses pytest for running tests. The test suite covers all major components of the system.
Running Tests

To run all tests:

# Run all tests with coverage report
pytest

To run specific test categories:

# Run only unit tests
pytest -m unit

# Run only async tests
pytest -m async_test

# Run tests for a specific component
pytest tests/lib/test_crawler.py

Test Coverage

The project is configured to generate coverage reports automatically:

# Run tests with detailed coverage report
pytest --cov=src --cov-report=term-missing

Test Structure

    📁 tests/conftest.py: Common fixtures for all tests
    📁 tests/lib/: Tests for library components
        test_crawler.py: Tests for the crawler module
        test_chunker.py: Tests for the chunker module
        test_embedder.py: Tests for the embedder module
        test_database.py: Tests for the database module
    📁 tests/common/: Tests for common modules
        test_indexer.py: Tests for the vector indexing functionality
        test_processor.py: Tests for the document processing pipeline
    📁 tests/services/: Tests for service layer
        test_admin_service.py: Tests for admin service
        test_document_service.py: Tests for document service
        test_job_service.py: Tests for job service
    📁 tests/api/: Tests for API endpoints
        test_documents_api.py: Tests for document endpoints

🧹 Code Quality

Doctor uses pre-commit hooks to maintain code quality and consistency.
Pre-commit Hooks

The project is configured with pre-commit hooks that run automatically before each commit:

    🔍 ruff check --fix: Lints code and automatically fixes issues
    🎨 ruff format: Formats code according to project style
    ✂️ Trailing whitespace removal
    📝 End-of-file fixing
    🔎 YAML validation
    📏 Large file checks

Setup Pre-commit

To set up pre-commit hooks:

# Install pre-commit
uv pip install pre-commit

# Install the git hooks
pre-commit install

Running Pre-commit Manually

You can run the pre-commit hooks manually on all files:

# Run all pre-commit hooks
pre-commit run --all-files

Or on staged files only:

# Run on staged files
pre-commit run 