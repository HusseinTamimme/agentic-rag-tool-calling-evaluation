# Agentic RAG Pipeline with Tool Calling & LLM-as-a-Judge Evaluation

An end-to-end Retrieval-Augmented Generation (RAG) system built with Python, ChromaDB, and Google Gemini[span_0](start_span)[span_0](end_span). The architecture integrates semantic retrieval, deterministic function calling for exact arithmetic, strict Pydantic structured outputs, and an automated evaluation pipeline to audit citation integrity and factual faithfulness[span_1](start_span)[span_1](end_span).

---

## Key Features

* **Token-Bounded Chunking:** Implements sliding window token-level text segmentation using `tiktoken` (`cl100k_base` encoding)[span_2](start_span)[span_2](end_span).
* **Vector Indexing & Retrieval:** Manages document embeddings and semantic similarity queries using an in-memory `chromadb` client[span_3](start_span)[span_3](end_span).
* **Deterministic Tool Calling:** Offloads arithmetic calculations to a dedicated Python function to eliminate calculation errors[span_4](start_span)[span_4](end_span).
* **Strict Schema Validation:** Enforces structured JSON output via `pydantic` (`AssistantResponse`), guaranteeing answers, confidence scores, and source citations[span_5](start_span)[span_5](end_span).
* **Automated LLM-as-a-Judge:** Audits answers against ground-truth context with zero-temperature evaluation, grading faithfulness, citation accuracy, and identifying unsupported claims[span_6](start_span)[span_6](end_span).

---

## Tech Stack

* **Language:** Python 3.12+[span_7](start_span)[span_7](end_span)
* **LLM Engine:** Google Gemini (`gemini-2.5-flash` via `google-genai` SDK)[span_8](start_span)[span_8](end_span)
* **Vector Database:** ChromaDB[span_9](start_span)[span_9](end_span)
* **Data Validation:** Pydantic v2[span_10](start_span)[span_10](end_span)
* **Tokenization:** Tiktoken[span_11](start_span)[span_11](end_span)

---

## Project Structure

```text
.
├── Main_Notebook.ipynb    # Main pipeline implementation and test suite
└── README.md              # Project documentation
