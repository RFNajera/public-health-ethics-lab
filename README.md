# Public Health Ethics Lab

A lightweight, mobile-friendly, classroom-ready web application for progressive-disclosure public health ethics exercises. Case 001 examines the Los Angeles Edmonston–Zagreb measles vaccine study (1990–1991) and subsequent consent controversy (1996).

## Features

- Five sequential stage reveals with changing stakeholder roles and discussion prompts
- Group reflections saved locally in the current browser (`localStorage`)
- Export responses as a `.txt` file, final debrief, sources, and print view
- Keyboard-friendly, responsive interface
- No logins, tracking, analytics, external libraries, servers or API keys

## Local preview

Open `index.html` in any modern browser. No build or installation required.

For an optional local web server:

```bash
python3 -m http.server 8000
# Open http://localhost:8000
```

## Publish through GitHub Pages

1. On GitHub, create a **public** repository named `public-health-ethics-lab` (or any name you prefer).
2. Upload these files directly into its top-level directory (or push them using Git).
3. In the repository, open **Settings → Pages**, and under **Build and deployment**, choose **Deploy from a branch**. Select the `main` branch and `/(root)` folder, and save.
4. GitHub will show your live page URL when it is ready, usually in the form `https://YOUR-USERNAME.github.io/public-health-ethics-lab/`.

To push from a cloned or local directory, run (replace the placeholder with the actual GitHub account):

```bash
git init
git add .
git commit -m "Initial public health ethics case"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/public-health-ethics-lab.git
git push -u origin main
```

## Classroom packet (included)

The `handouts/` folder contains the following paired **PDF and editable Word (.docx)** documents:

1. `01_Measles_and_Vaccine_History_Fact_Sheet` — scientific context, vaccine timeline, and the Edmonston–Zagreb formulation.
2. `02_FICTIONAL_Consent_Form_For_Critique` — a simulated, **explicitly fictional** and deliberately deficient consent document for student critique. **Not** the original study consent form.
3. `03_Instructor_Moderator_Guide` — facilitation plan, staged case notes, answer key, and assessment rubric.

The web app links to the fictional consent PDF **at stage 2** and the full fact sheet **during the final debrief**. The instructor guide is intentionally *not* linked from the student interface.

**Spoiler and visibility warning:** In a *public* GitHub repository and GitHub Pages site, files remain publicly accessible by direct link, including the instructor guide. Client-side stage controls do not provide real access restrictions. To protect the answer key, keep the instructor guide in a separate private repository or distribute it directly to teachers instead of publishing the `handouts/03_*` files. For an instructor-led classroom exercise, project the app and control the stage reveals, and distribute PDF pages when appropriate. The two-page fact sheet should be **distributed as page 1 initially**, and page 2 only during the final debrief if you want to avoid spoilers.

## Facilitation suggestion

Share or project the application and give each stage 7–10 minutes. Pause before advancing. Each table should commit to a course of action in writing and say **what additional facts would change its mind**. Close with a discussion of research ethics, community accountability, consent, and uncertainty.

## History and accuracy

This exercise is adapted from historical events, not a verbatim reenactment. The fictitious group roles and prompts are pedagogical devices. Important distinctions:

- Parents **knew** they were participating in a vaccine study and signed forms. The defect was inadequate disclosure that one formulation was *experimental and unlicensed in the United States*.
- Reports about higher mortality after high-titer measles vaccine in some overseas studies prompted concern and action; these reports do **not** establish mortality caused by the Los Angeles trial.
- Historical accounts report no documented vaccine-linked injuries in the Los Angeles cohort. No documented physical harm does not validate an inadequate informed-consent process.
- Historical sources differ slightly on the 1989 study-planning period vs. 1990 enrollment start, so the stages use 1990–1991 for enrollment and 1996 for public disclosures.

### References

- [1997 US congressional hearing and CDC testimony](https://www.govinfo.gov/content/pkg/CHRG-105hhrg44389/pdf/CHRG-105hhrg44389.pdf)
- [Marwick (1996), *JAMA*: Questions Raised About Measles Vaccine Trial](https://pubmed.ncbi.nlm.nih.gov/8861973/)
- [Los Angeles Times (1996): CDC Says It Erred in Measles Study](https://www.latimes.com/archives/la-xpm-1996-06-17-mn-15871-story.html)
- [FactCheck.org on historical claims about the vaccine study](https://www.factcheck.org/2021/03/scicheck-rfk-jr-video-pushes-known-vaccine-misrepresentations/)

## Privacy and limitations

Group notes are stored on the device/browser currently running the exercise and aren't sent anywhere. This is not an LMS and does not collect student identities or submissions. Browser storage can be cleared; export notes before leaving. A shared link to this static app does not synchronize stage reveals or notes between devices. In addition, because all case text is delivered to the browser, a technically adept learner could inspect unrevealed material. Real instructor-controlled remote reveals would require a backend and authentication.

## Possible next steps

- Separate instructor/student URLs and synchronized stages
- More cases in portable JSON format (outbreak response, environmental justice, quarantine, resource allocation)
- Instructor case builder, group submission, LMS export
- Optional English/Spanish localization

## License

MIT License — see `LICENSE`.
