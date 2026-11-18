# ADL Independence Measure Web App

Touch-friendly, static web app for iPad/desktop use. It implements the supplied ADL Independence Measure with eight ADLs scored 0-5 (maximum 40) and the source-document interpretation bands.

## Features
- Admit, Reassessment, and Discharge scoring
- Automatic total and interpretation
- Admit-to-latest and Admit-to-D/C change calculation
- ADL-by-ADL change table and visual comparison
- Copyable OT documentation summary
- Print / Save PDF results
- Optional patient initials only
- No analytics, third-party scripts, server, database, or API
- Session-only browser storage (sessionStorage), cleared with New Patient and normally when the browser session closes

## Privacy / clinical deployment
This app is intentionally PHI-minimized. Do not enter patient name, MRN, DOB, room number, diagnosis, free-text identifiers, or other PHI. Initials are provided only as a limited session identifier. Initials plus clinical scores should not be assumed to meet HIPAA de-identification standards in every context.

The app is not an EHR and should not be used as the system of record. Generated documentation should be reviewed and entered into the organization's approved medical record. Organizational Privacy / Information Security approval is recommended before clinical deployment.

## GitHub Pages deployment
1. Create a repository in your GitHub account.
2. Upload `index.html`, `styles.css`, `app.js`, and `manifest.webmanifest` to the repository root.
3. In GitHub: Settings > Pages.
4. Under Build and deployment, choose Deploy from a branch.
5. Select the main branch and `/ (root)`, then Save.
6. Open the generated GitHub Pages URL in Safari on the iPad.
7. Optional: Safari Share > Add to Home Screen.

Do not commit patient data, exported results, screenshots containing patient information, or clinical records to the GitHub repository.

## Scoring implemented from supplied source
- 32-40: Independent
- 23-31: Mod I/Sup
- 14-22: CGA/Min A
- 5-13: Mod A
- 1-4: Max A
- 0: Dependent

## Source wording requiring local verification
The supplied source says `75% or more` for UB Dressing / Max A while comparable Max A criteria generally say `76% or more`. The source also says `100% assistance required for toileting tasks` in the Transfers / Dependent cell. Both are preserved exactly rather than silently corrected.

## Files
- `index.html` - application structure
- `styles.css` - responsive/iPad/print styling
- `app.js` - assessment descriptors, scoring, comparison, and documentation logic
- `manifest.webmanifest` - installable web-app metadata
