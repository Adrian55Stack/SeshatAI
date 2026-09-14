# SeshatAI

Main monorepo for the SeshatAI fullstack application. SeshatAI is a RAG-powered, context-based application for answering mythology-related questions in any language. Composed of two independent submodules — a frontend and a backend — each maintained in their own repository.

---

## Project Structure

```
SeshatAI/
├── SeshatAIFE/          # Angular frontend submodule
├── SeshatAIBE/          # Node.js backend submodule
├── .gitmodules
├── .gitignore
└── README.md
```

---

## Submodules

- [SeshatAIFE](https://github.com/Adrian55Stack/SeshatAIFE) — Angular 19 frontend, handles UI and API calls towards the backend
- [SeshatAIBE](https://github.com/Adrian55Stack/SeshatAIBE) — Node.js backend, receives client calls, performs RAG retrieval, and forwards context to Grok AI

---

## Getting Started

### Clone with submodules

```bash
git clone --recurse-submodules https://github.com/Adrian55Stack/SeshatAI
```

If you already cloned without submodules:

```bash
git submodule update --init --recursive
```

### Update submodules to latest

```bash
git submodule update --remote
```

---

## Prerequisites

- Node.js v18+
- npm v9+
- A valid Grok API key
- A valid translation API key

---

## .gitignore Setup

| File | Scope |
|------|-------|
| `/.gitignore` | Root — ignores workflow artifacts, editor files, OS files |
| `/SeshatAIFE/.gitignore` | Angular-specific — `node_modules`, `dist`, `coverage` |
| `/SeshatAIBE/.gitignore` | Node.js-specific — `node_modules`, `coverage`, `.env` |