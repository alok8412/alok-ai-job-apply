# ALOK AI — Job Apply Assistant

A responsive, browser-based job search and application tracker configured for:
- Faridabad, Haryana (including Ballabhgarh / IMT Faridabad)
- MIS Manager, Administration Manager, MIS & Administration Manager, Power BI Analyst
- 5–10 years' experience
- Minimum monthly salary: ₹35,000 (preferred range ₹35,000–₹45,000)
- Immediate joining
- Daily application target: 25

## Run locally
1. Extract the ZIP.
2. Open `index.html` in Chrome, Edge or Firefox.
3. No installation or server is required for the local prototype.

For a local development server, run:
```bash
python -m http.server 8000
```
Then open http://localhost:8000.

## Features
- Dashboard and daily target progress
- Job matching score based on saved preferences
- Add/edit opportunities manually
- Import jobs from CSV
- Application pipeline and status tracking
- Export application records to CSV
- Candidate profile and resume filename tracking
- Responsive desktop and mobile layout
- Local browser storage

## CSV import format
Required columns: `title`, `company`

Optional columns: `location`, `salary`, `experience`, `source`, `url`, `description`

Example:
```csv
title,company,location,salary,experience,source,url,description
MIS Manager,Example Manufacturing,Faridabad,42000,7,Company website,https://example.com/careers,Manage MIS reporting
```

## Important scope and limitations
This is a working front-end prototype, not a live multi-site job bot. It does not scrape job portals, log in to accounts, solve CAPTCHAs, bypass platform restrictions, or submit applications in the background. Job portal terms and technical restrictions differ. Use official APIs, approved integrations, or workflows explicitly permitted by each site. The app opens the saved application URL for the candidate to review and complete. Do not represent a job as verified unless you have checked the original posting.

### Production upgrade path
To make this a multi-user production web app:
1. Add a secure backend (e.g. Node.js + PostgreSQL) and authentication.
2. Add approved job-feed/API integrations with each provider's permission.
3. Add secure resume storage with encryption, access controls and deletion.
4. Build per-site application adapters only where the provider expressly permits them.
5. Add a review queue, audit log, duplicate detection and submission receipts.
6. Deploy with HTTPS, privacy notice, retention policy and backups.

## Privacy
The prototype stores profile details and job records in this browser's `localStorage`. Avoid shared/public computers. Resume file contents are not uploaded or stored by this prototype; only the selected filename is retained.
