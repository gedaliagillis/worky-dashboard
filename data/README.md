# Worky Data - Source of Truth

This directory contains all job search data in structured JSON files.

## Files

### `leads.json`
All job leads tracked in the pipeline.

**Schema:**
```json
{
  "id": "string",
  "company": "string",
  "role": "string",
  "pipeline": "startup|enterprise",
  "source": "string",
  "status": "queue|draft|sent|replied",
  "notes": "string",
  "url": "string",
  "date": "YYYY-MM-DD",
  "contact": "string",
  "lastUpdate": "YYYY-MM-DD"
}
```

### `tasks.json`
Todos and action items.

**Schema:**
```json
{
  "id": "string",
  "text": "string",
  "done": boolean,
  "category": "outreach|research|prep|interview",
  "priority": "high|medium|low",
  "created": "YYYY-MM-DD"
}
```

### `applications.json`
Formally submitted job applications (not just outreach).

**Schema:**
```json
{
  "id": "string",
  "company": "string",
  "role": "string",
  "appliedDate": "YYYY-MM-DD",
  "status": "submitted|screening|interview|offer|rejected",
  "notes": "string"
}
```

### `rejections.json`
Companies that passed or rejected.

**Schema:**
```json
{
  "id": "string",
  "company": "string",
  "role": "string",
  "reason": "string",
  "date": "YYYY-MM-DD"
}
```

### `notes.md`
Strategy notes, insights, and journal.

---

## Usage

**Dashboard pulls from:**
- `leads.json` for main pipeline
- `tasks.json` for task list
- `applications.json` for submitted applications

**All edits via dashboard auto-commit back to these files.**

**Single source of truth = GitHub repo.**
