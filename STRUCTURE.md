# Worky Dashboard - Repository Structure

**Single source of truth for all job search data.**

```
worky-dashboard/
├── README.md                 # Overview and setup guide
├── STRUCTURE.md             # This file - explains organization
├── index.html               # Dashboard (pulls from data/)
├── data/                    # 📊 SOURCE OF TRUTH
│   ├── README.md            # Data schemas and usage
│   ├── leads.json           # All job leads
│   ├── tasks.json           # Todos and action items
│   ├── applications.json    # Submitted applications
│   ├── rejections.json      # Passed/rejected companies
│   └── notes.md             # Strategy notes and journal
└── assets/                  # (future: screenshots, resumes, etc.)
```

---

## Data Flow

### Reading Data
```
GitHub (data/*.json)
    ↓
Dashboard (index.html)
    ↓
Display in UI
```

### Writing Data
```
User edits in dashboard
    ↓
GitHub API
    ↓
Update data/*.json
    ↓
Commit to GitHub
    ↓
GitHub Pages rebuilds
    ↓
Next load shows updated data
```

---

## Key Principles

1. **Single Source of Truth**: All data lives in `data/` directory
2. **Structured Data**: JSON for machine-readable, MD for human notes
3. **Version Controlled**: Every change tracked in Git
4. **Dashboard Agnostic**: Data structure works with any UI
5. **Clear Schemas**: Each file has documented structure in data/README.md

---

## Current Data

- **10 leads** (5 queue, 5 sent)
- **3 tasks** (all active)
- **0 applications** (formal submissions)
- **0 rejections**

---

## Future Expansion

Can easily add:
- `data/contacts.json` - Network contacts
- `data/companies.json` - Company research
- `data/interviews.json` - Interview tracking
- `assets/resumes/` - Resume versions
- `assets/emails/` - Email templates

---

**Everything organized. Everything version controlled. Everything in one place.** 🎯
