# TEAM_CONTRIBUTIONS.md — Group 5

## Project: ProfessorGPT — AI-Powered Lecture Assistant
**Course:** BANA 275  
**Team:** Group 5

---

## Team Members & Roles

### Spencer Cao — Project Coordinator & Backend Lead
**Responsibilities:**
- Defined project timeline and milestone tracking
- Led weekly team meetings and managed GitHub repository
- Architected the overall system pipeline (input → preprocessing → RAG → generation → UI)
- Implemented `rag_engine.py` — TF-IDF chunking, vectorization, cosine similarity retrieval
- Wrote `ARCHITECTURE.md` and coordinated documentation efforts

**Key contributions:**
- Designed the 5-stage processing pipeline
- Built and tested the RAG retrieval system
- Integrated session state management in Streamlit

---

### Lily Cen — AI Integration & Prompt Engineering
**Responsibilities:**
- Designed and iterated on all LLM prompt templates
- Implemented all Claude API calls (`generate_notes`, `generate_flashcards`, `generate_qa`, `generate_exam`)
- Conducted prompt engineering experiments to minimize hallucination
- Tested output quality across different lecture types (STEM, business, humanities)

**Key contributions:**
- Structured JSON output prompts for reliable parsing
- Developed hallucination mitigation strategies (grounding, format constraints)
- Wrote the RAG chat integration with multi-turn conversation history

---

### Raye Chiang — Frontend & UI/UX
**Responsibilities:**
- Designed and implemented the full Streamlit interface
- Built tab navigation, sidebar, session state display
- Implemented interactive flashcard, Q&A accordion, and exam UI components
- Created the custom CSS styling and visual design
- Wrote `USER_GUIDE.md`

**Key contributions:**
- Multi-tab layout with persistent session state across tabs
- Exam grading UI with color-coded correct/incorrect display
- Download functionality for notes export
- Loading progress indicators and success feedback

---

### Seunghyun Kim — Transcript Processing & Data Pipeline
**Responsibilities:**
- Implemented `transcript_processor.py` — text cleaning and normalization
- Researched and integrated Whisper API for audio transcription
- Handled edge cases: caption artifacts, timestamps, Unicode normalization
- Conducted testing with real lecture transcripts from various sources

**Key contributions:**
- Robust preprocessing pipeline supporting multiple transcript formats
- Whisper API integration for audio/video input
- Overlap-based chunking strategy for RAG
- TF-IDF vocabulary building and IDF weighting

---

### Xinyi Wang — Business Analysis & User Research
**Responsibilities:**
- Conducted user research with MSBA students on study habits and pain points
- Validated ProfessorGPT's feature set against actual student needs
- Wrote the Executive Summary and Problem & Motivation sections of the proposal
- Coordinated demo preparation and final presentation
- Wrote `README.md`, `SETUP.md`, and `USER_GUIDE.md`

**Key contributions:**
- Defined target user personas (MSBA students, online learners, professionals)
- Validated 70% study time reduction claim through informal interviews
- Defined the 5-tool feature set based on student feedback
- Ensured the app addresses real exam-preparation workflows

---

## Contribution Summary

| Member | Primary Domain | Files Owned |
|--------|---------------|-------------|
| Spencer Cao | Architecture, RAG | `rag_engine.py`, `ARCHITECTURE.md` |
| Lily Cen | AI/LLM Integration | `app.py` (generation functions) |
| Raye Chiang | Frontend/UI | `app.py` (UI/Streamlit), `USER_GUIDE.md` |
| Seunghyun Kim | Data Pipeline | `transcript_processor.py` |
| Xinyi Wang | Business/Docs | `README.md`, `SETUP.md`, proposal |

---

## Phase Timeline

| Phase | Weeks | Status | Lead |
|-------|-------|--------|------|
| Phase 1: Requirements & Setup | 3–4 | ✅ Complete | Spencer |
| Phase 2: Ingestion, RAG, Notes | 5–6 | ✅ Complete | Seunghyun + Lily |
| Phase 3: Flashcards, Q&A, Exam, Chat | 7–8 | ✅ Complete | Lily + Raye |
| Phase 4: Testing, Refinement, Docs | 9 | ✅ Complete | All |

---

## Team Reflection

The project was completed successfully with equal participation across all members. Weekly syncs via Discord and shared GitHub kept development on track. The hardest technical challenge was ensuring consistent JSON output from the LLM — solved by explicit format constraints in prompts and robust parsing fallbacks. The most valuable learning was how RAG grounding dramatically reduces hallucinations in domain-specific chat.
