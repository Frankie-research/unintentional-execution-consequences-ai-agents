# Public Release Checklist — Version 1.0

## 1. Pre-publication evidence and privacy review

- [ ] Confirm author name, credentials, affiliation and contact email.
- [ ] Confirm no private ChatGPT conversation URLs are exposed.
- [ ] Confirm no API keys, Telegram tokens, SMTP credentials, passwords or filesystem secrets are included.
- [ ] Confirm personal Windows paths, usernames and identifiers are generalised where appropriate.
- [ ] Confirm the report does not expose unnecessary operational details that could weaken the author's own system.
- [ ] Confirm all third-party figures, quotations, screenshots and copyrighted material have an appropriate citation/licence.
- [ ] Confirm the report states that it is an independent practitioner report and not peer-reviewed.
- [ ] Confirm the evidence boundary between observed facts, analytical scenarios and external research.

## 2. File integrity

- [ ] Open the DOCX in Microsoft Word.
- [ ] Check formulas and mathematical symbols.
- [ ] Check tables, page numbers, headers/footers and references.
- [ ] Check the title page and author/contact information.
- [ ] Calculate SHA-256 before upload.
- [ ] Preserve the exact v1.0 file after publication.

## 3. GitHub

Suggested repository name:

`unintentional-execution-consequences-ai-agents`

Suggested root files:

- report DOCX
- README.md
- CITATION.cff
- LICENSE / CC BY 4.0 notice
- release notes
- optional `docs/` folder for supplementary material

Create the repository as public only after the privacy/security review.

Create the first release as:

`v1.0.0`

Do not overwrite the v1.0.0 report after Zenodo archives it. If the report changes materially, create a new version/release.

## 4. Zenodo

Recommended role: authoritative DOI/preservation record.

Metadata:

Title:
Unintentional Execution Consequences and Guardrail Shortcut Behaviors in Autonomous AI Agents: A Technical, Safety, and Legal Liability Analysis

Creator:
Frankie Mak

Publication date:
2026-10-05

Resource type:
Publication / Report

Version:
1.0

Access:
Open

Recommended licence:
CC BY 4.0

Related identifier:
https://doi.org/10.5281/zenodo.22985434

After publication:
- [ ] Record DOI
- [ ] Record version DOI
- [ ] Record concept DOI if supplied
- [ ] Add the DOI to GitHub README and CITATION.cff in a subsequent metadata commit.
- [ ] Do not silently replace the published v1.0 file.

## 5. Hugging Face

Hugging Face is best treated initially as a **discoverability / companion artifact platform**, not as the authoritative DOI archive.

Recommended options:

A. If an arXiv version is later published:
- [ ] Index the paper on Hugging Face Papers.
- [ ] Claim authorship.
- [ ] Link the GitHub repository and Zenodo DOI.

B. If there is no arXiv version:
- [ ] Use a clearly labelled companion repository only if there is a useful AI artifact to host (e.g. evaluation data, taxonomy tables, machine-readable references or reproducibility material).
- [ ] Do not falsely label the report itself as an AI model or dataset.

## 6. Final cross-platform verification

- [ ] GitHub repository opens publicly.
- [ ] GitHub release v1.0.0 is visible.
- [ ] Zenodo DOI resolves.
- [ ] GitHub README points to Zenodo DOI.
- [ ] Zenodo record points back to GitHub.
- [ ] Hugging Face companion page points to GitHub and Zenodo.
- [ ] Citation metadata is consistent across all platforms.
- [ ] Author name and report title are identical everywhere.


## Pre-flight correction record (2026-10-06)
- [x] Corrected EU Product Liability Directive wording to "after 8 December 2026".
- [x] Corrected Australian Government National AI Centre Guidance for AI Adoption publication year to 2025.
- [x] Removed three references not cited in the body: Christiano et al. (2017), Russell (2019), and Orseau & Armstrong (2016).
- [x] Renumbered remaining references and in-text citations consistently.
- [x] Rebuilt the DOCX from the canonical source while preserving native OMML equations.
- [x] Generated PDF directly from the corrected DOCX.
- [x] Rebuilt package SHA-256 manifest.
