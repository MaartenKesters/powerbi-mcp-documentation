# 📊 powerbi-mcp-documentation

A Claude skill for generating comprehensive, standardized documentation for Power BI semantic models. Built for use with [Claude.ai](https://claude.ai) and the `powerbi-modeling-mcp` server.

---

## 📁 What's in this repository

```
powerbi-mcp-documentation/
└── SKILL.md        # The skill definition file used by Claude
```

The `SKILL.md` file contains all instructions, workflow logic, formatting rules, and output templates that guide Claude through the documentation process.

---

## ⚡ Quick Start

### Prerequisites

- A [Claude.ai](https://claude.ai) account (Pro or Team recommended)
- The **powerbi-modeling-mcp** MCP server installed and connected in Claude
- A running Power BI Desktop instance, PBIP folder, or Fabric workspace to connect to

### Installation

1. Clone or download this repository.
2. In Claude.ai, go to your **Project settings** and add the `SKILL.md` file as a project document, or reference it in your system prompt.
3. Make sure the `powerbi-modeling-mcp` server is active and listed under your connected MCP tools.

### Usage

Once the skill is loaded, simply ask Claude to document your model:

```
Document this Power BI model
```
```
Generate documentation for my semantic model
```
```
Create a Power BI documentation report
```

Claude will connect to your semantic model, gather metadata, and walk you through an interactive configuration process before generating the final output.

---

## ✨ Features

**Interactive, guided workflow**
Claude asks configuration questions one at a time — no long forms to fill in upfront. You stay in control of what gets documented.

**Two documentation presets + manual mode**
- *Internal preset* — comprehensive, technical, includes all DAX code and recommendations
- *Client preset* — polished, business-focused, less technical detail
- *Manual mode* — configure every section individually

**Business context upload**
Upload existing documents (requirements, data dictionaries, stakeholder briefs, wiki pages) before generation. Claude uses this context to write richer, domain-specific descriptions and summaries.

**Sections you can include or skip**
- Executive Summary
- Data Sources (with Power Query M code)
- Visual ER Diagram (exported as a `.mermaid` file)
- Relationships overview
- Tables (grouped by type: fact, dimension, parameter, other)
- Measures (grouped by display folder)
- Calculation Groups
- Recommendations (Kimball methodology + Power BI Best Practices)
- Business Glossary

**Word document output**
The final document is a styled `.docx` file with consistent headers, tables, and code blocks — ready to share with stakeholders or save to a project wiki.

**Mermaid ER diagram**
A separate `.mermaid` file is generated alongside the Word document, which can be rendered in tools like GitHub, Notion, or any Mermaid-compatible viewer.

---

## 📄 Output Files

After a documentation run, Claude will provide:

| File | Description |
|------|-------------|
| `[ModelName]_Documentation.docx` | The main documentation Word document |
| `[ModelName]_DataModel.mermaid` | Entity-relationship diagram (if selected) |

---

## 🔧 Requirements

| Requirement | Details |
|------------|---------|
| Claude | Claude.ai Pro, Team, or Enterprise |
| MCP Server | `powerbi-modeling-mcp` |
| Power BI | Desktop, PBIP folder, or Fabric workspace |
