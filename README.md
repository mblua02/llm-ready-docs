# llm-ready-docs

## Overview

**llm-ready-docs** is a documentation framework designed to centralize technical knowledge in a format that is both human-readable and fully optimized for Large Language Models (LLMs). This project establishes a clear, scalable structure for creating, maintaining and evolving documentation used across architecture, design, integration, agentic workflows and technical enablement.

The approach is based entirely on Markdown and textual diagram definitions, allowing documentation to be version-controlled, collaboratively improved and easily ingested by LLMs or DevAgents. This enables automated reasoning, summarization, validation and code or design assistance based on the knowledge contained in the repository.

This repository was inspired by and initially seeded with the **MuleSoft Agent Fabric Compendium**, a deeply structured, LM-ready technical asset that demonstrated the benefits of this documentation pattern.

---

## Why LM-Ready Documentation?

Traditional documentation formats are not suited for modern agentic workflows. PDFs, screenshots and graphical diagram files are difficult for LLMs to interpret, impossible to diff properly and slow to update.

This repository adopts a set of principles that ensure long-term usability, precision and alignment with intelligent development frameworks.

## Advantages of This Documentation Model

| Benefit                          | Description                                                        |
| -------------------------------- | ------------------------------------------------------------------ |
| **Versionability**               | Markdown + Git enables full history tracking and rollback          |
| **Collaboration**                | Pull request workflows enable peer review and quality control      |
| **LLM Interpretability**         | Structured text is ideal for DevAgents, bots, and RAG systems      |
| **Portability**                  | Renders consistently across editors, IDEs, and platforms           |
| **Agentic Automation**           | Docs can be auto-generated or auto-updated using AI tools          |
| **Reduced Staleness**            | Single source of truth eliminates wiki drift and duplication       |
| **Content/Rendering Separation** | No binary diagram files; all content is human and machine readable |

---

## Repository Structure

The following structure is recommended for organizing LM-ready assets:

```
/docs
  /compendiums
  /concepts
  /architectures
  /patterns
  /governance
  /observability

/diagrams
  /mermaid
  # This folder is optional and should only be used for diagrams that need to be reused across multiple documents.
  # All other Mermaid diagrams should remain inline within the Markdown documents to preserve LM-readiness and context clarity.

/examples

/templates
  documentation-template.md
  mermaid-template.md

/conventions
  style-guide.md
  lm-readiness-checklist.md
```

This structure ensures clarity, modularity and ease of automated consumption.

---

## Key Principles

### LM-Ready by Design

All documentation must follow consistent structural patterns:

* **Clear metadata**: Frontmatter or header sections identifying purpose, scope, and audience
* **Predictable structure**: Standardized heading hierarchy and section ordering
* **Diagram support**: Visual representations using text-based formats

### Mermaid-First Diagrams

All diagrams must be written using [Mermaid](https://mermaid.js.org/) syntax to ensure:

* Version control friendliness (diff-able text)
* Portability across rendering platforms
* LLM interpretability without image processing
* Easy maintenance and updates

### Customer-Agnostic Content

Documents must be:

* Free of sensitive or proprietary customer information
* Suitable for internal automation and DevAgent consumption
* Generalizable patterns rather than implementation-specific details

---

## How to Contribute

Contributions are welcome and encouraged. This repository is intended to evolve collaboratively.

### Contribution Workflow

1. **Create a feature branch** for your update.
2. Follow all LM-ready conventions described in `/conventions`.
3. Ensure all diagrams are in Mermaid.
4. Verify that no customer-specific details are included.
5. Submit a **Pull Request** with a clear description of:

   * what was changed,
   * why it was changed,
   * and any implications for existing docs.
6. At least one reviewer must validate:

   * clarity,
   * LM-readiness,
   * alignment with style guide,
   * and correctness of technical content.
7. Once approved, the PR can be merged.

### Submitting Corrections

If you detect an error:

* Open an Issue describing the problem, or
* Submit a PR directly with the fix.

Both small corrections and large enhancements are equally welcome.

---

## Best Practices for LM-Ready Docs

To maximize LLM performance and output consistency, apply the following guidelines:

### Do:

* Use short, declarative sentences.
* Prioritize structure over prose.
* Include examples whenever possible.
* Keep diagrams simple and descriptive.
* Use headings to break down concepts.
* Keep related files close in the folder hierarchy.

### Avoid:

* Screenshots of diagrams.
* Embedding unstructured large text blocks.
* Mixing customer-specific and general technical content.
* Using ambiguous terminology.

---

## Validating Documentation

Before merging new or updated documentation, validate compliance with LM-readiness standards. Use an LLM to perform automated verification using the following prompt:

```
Verify the document [DOCUMENT_PATH] against the LM-readiness guidelines defined in README.md.

Evaluate compliance across these criteria:
1. LM-Ready by Design: Clear metadata, predictable structure, diagram support
2. Mermaid-First Diagrams: All diagrams in Mermaid syntax, no image files
3. Customer-Agnostic Content: No sensitive data, generalizable patterns
4. Best Practices: Short sentences, structured content, examples, proper headings
5. Avoidances: No screenshots, no unstructured blocks, no ambiguous terminology

Provide a compliance summary table with status (✅/❌) and evidence for each criterion.
```

This validation can be performed manually by a reviewer or integrated into CI/CD pipelines using LLM-based tooling.

---

## Future Enhancements

Planned expansions for this repository include:

* Automated generation of documentation from source assets.
* Creation of an internal **DevAgent** preloaded with this repository.
* Scripts to validate LM-readiness (syntax checks, metadata completeness).
* Interactive applications for pre-sales demonstrations.
* Integration with internal wikis, referencing the repository as the single source of truth.

---

## License

Documentation in this repository is intended for internal enablement and technical acceleration. Distribution must follow organizational guidelines.

---

## Acknowledgments

This repository grows from the initial effort of consolidating deep technical material into LM-ready structures, starting with the **MuleSoft Agent Fabric Compendium**, which validated the value of this approach.
