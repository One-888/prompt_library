
# Prompt Library

## Overview
**Prompt Library** is a centralized collection of reusable prompts designed for AI-assisted code generation and analysis.  
Instead of storing actual implementation code, this library focuses on **requirements, objectives, and constraints** for various projects.  
The goal is to make prompts **portable, future-proof, and adaptable** across different platforms, programming languages, and database systems.

---

## Why This Project?
- **Future-Proof**: Hardware, libraries, and frameworks evolve. By keeping only conceptual requirements, we can regenerate code on demand using the latest technologies.
- **Portability**: Prompts are written in a generalized way, avoiding vendor-specific details.
- **Consistency**: Standardized prompts ensure uniform quality and structure across projects.
- **AI-Ready**: Each prompt is optimized for feeding into AI tools for code generation, documentation, or analysis.

---

## What’s Inside?
- **Project Prompts**: High-level descriptions of what needs to be built (e.g., stored procedures, ETL pipelines, data profiling tools).
- **Requirements & Constraints**: Functional and non-functional requirements, portability guidelines, and acceptance criteria.
- **Output Structure**: Suggested formats for generated outputs (e.g., Markdown, CSV, JSON).
- **Analysis Prompts**: Instructions for AI to perform data profiling, BI recommendations, and quality checks.

---

## Key Principles
- **No Hardcoded Code**: Only conceptual prompts, not implementation details.
- **Markdown Format**: All prompts are stored in `.md` for readability and easy integration.
- **Flat Structure (for now)**: Simple organization; future versions may introduce folders by domain or project type.
- **Regenerable**: Prompts can be reused to generate fresh code that matches current requirements and technology stack.

---

## Example Use Case
Need a stored procedure to export table metadata and sample data?  
→ Use the **Table Analysis Export Prompt** from this library.  
→ Feed it to your AI tool to generate code for SQL Server, PostgreSQL, or any other engine.

---

## Future Plans
- Add folder structure for categorizing prompts (e.g., Database, ETL, Analytics).
- Include versioning for prompts to track evolution of requirements.
- Provide sample AI workflows for regenerating code from prompts.

---

### ✅ Why Markdown?
Markdown ensures clarity, portability, and compatibility with GitHub and AI tools.
