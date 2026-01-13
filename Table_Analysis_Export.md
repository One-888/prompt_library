## Table Analysis Export

# Goal
Create a reusable database procedure that, given a table name, generates a single text output containing:
- Table metadata (definition, constraints)
- A reference SELECT statement
- A sample of data rows
- An optional analysis instruction block for AI tools

The output should be formatted as plain text or Markdown so it can be saved as a `.txt` or `.md` file and uploaded to AI systems for profiling, documentation, or analysis.

---

## Core Requirements
1. **Input Parameters**
   - Schema name
   - Table name
   - Number of sample rows (default: 100)
   - Optional custom analysis instructions (default: generic AI prompt)

2. **Output**
   - One consolidated text block with:
     - Header: table name, row count, timestamp
     - Table definition (CREATE TABLE)
     - Reference SELECT statement
     - Sample data in a portable format (CSV or JSON)
     - Optional AI analysis instructions at the top

3. **Design Principles**
   - **Portability**: Avoid database-specific syntax where possible; use system catalog queries for metadata.
   - **Format Neutrality**: Output should be plain text or Markdown, not tied to SSMS or any IDE.
   - **Single Output**: Everything in one text block for easy saving and sharing.
   - **Customizable**: Allow injection of custom prompts or instructions for AI analysis.

4. **Sample Data**
   - Include a small subset of rows (TOP N or LIMIT N).
   - Use a clean, portable format:
     - CSV (quoted, escaped) for simplicity
     - JSON as an alternative if supported

5. **Constraints**
   - Do not include performance tuning details (indexes, statistics) unless explicitly requested.
   - Keep implementation modular so it can be adapted to other platforms (e.g., PostgreSQL, MySQL).

---

## Suggested Output Structure
```markdown
# AI Analysis Instructions
(Insert generic or custom prompt here)

---

## Table Info
- **Name**: schema.table
- **Row Count**: X
- **Generated**: YYYY-MM-DD HH:MM:SS

---

## CREATE TABLE
<Full CREATE TABLE script>

---

## Reference SELECT
SELECT TOP (N) * FROM schema.table;

---

## Sample Data (CSV)
"Column1","Column2","Column3"
"value1","value2","value3"
...
