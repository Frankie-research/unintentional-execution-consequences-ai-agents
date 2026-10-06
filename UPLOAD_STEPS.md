# Upload Procedure — GitHub → Zenodo → Hugging Face

## Phase 0 — Freeze the release

1. Open the final DOCX.
2. Perform the final Word visual check.
3. Do not edit the document after computing its release hash.
4. Keep the v1.0 file as an immutable release artifact.

## Phase 1 — GitHub

### Web UI

1. Sign in to GitHub.
2. Create a new **Public** repository.
3. Suggested name:
   `unintentional-execution-consequences-ai-agents`
4. Do not initialise with unrelated files if you will upload the prepared package.
5. Upload:
   - report DOCX
   - README.md
   - CITATION.cff
   - release notes
6. Add the appropriate CC BY 4.0 licence.
7. Review the public repository as an anonymous visitor.
8. Create a GitHub Release:
   - Tag: `v1.0.0`
   - Target: default branch
   - Title: `v1.0.0 — Public Release`
   - Attach the final report DOCX if desired.
9. Publish the release.

### Optional Git CLI

```powershell
git init
git add .
git commit -m "Initial public release v1.0.0"
git branch -M main
git remote add origin <YOUR_GITHUB_REPOSITORY_URL>
git push -u origin main
git tag -a v1.0.0 -m "Public Release v1.0.0"
git push origin v1.0.0
```

Do not put passwords, tokens or private configuration files in the repository.

## Phase 2 — Zenodo

1. Sign in to Zenodo.
2. Connect GitHub if not already connected.
3. In Zenodo, open the GitHub integration and sync repositories.
4. Enable the new GitHub repository.
5. Confirm the repository is enabled for archiving.
6. The next GitHub release can then be archived by Zenodo.
7. Open the resulting Zenodo draft.
8. Check:
   - title
   - creator
   - publication date
   - version
   - description / abstract
   - keywords
   - licence
   - related identifier to the previous Hermes report
   - file name
9. Preview the record.
10. Publish.
11. Copy the assigned DOI.

Important: Zenodo states that files cannot normally be modified after publication except under its documented post-publication rules. Treat the published v1.0 artifact as frozen.

## Phase 3 — DOI metadata update

After the Zenodo DOI is known:

1. Update GitHub README with the DOI.
2. Update `CITATION.cff` with the DOI.
3. Commit the metadata-only change.
4. Do not retag or replace v1.0.0 merely to add the DOI.
5. If a future report revision is needed, create v1.1.0 or v2.0.0 according to the magnitude of the change.

## Phase 4 — Hugging Face

### Recommended route

For this report, do not create a model repository merely because the report concerns AI agents.

If you later have a useful machine-readable research artifact, create a Hugging Face dataset repository and upload:
- taxonomy tables
- evaluation cases
- structured references
- reproducibility material
- non-sensitive examples

The README should clearly state that it is a companion research artifact, not a model.

### Web UI

1. Sign in to Hugging Face.
2. Select New Dataset only if the repository genuinely contains dataset/research-artifact material.
3. Choose public/private visibility.
4. Upload the companion files.
5. Create the Dataset Card / README.
6. Include links to GitHub and Zenodo.
7. Add CC BY 4.0 metadata if appropriate.
8. Review the public page.

### CLI

```powershell
hf auth login
hf repo create <YOUR_HF_REPOSITORY_NAME> --repo-type dataset
hf upload <YOUR_USERNAME>/<YOUR_HF_REPOSITORY_NAME> . --repo-type dataset
```

Use a Hugging Face Paper Page only when an eligible paper identifier (currently the Paper Pages workflow is based around arXiv) is available.

## Phase 5 — Final public landing-page consistency

Use the same canonical title everywhere.

Canonical citation:

Mak, F. (2026). Unintentional Execution Consequences and Guardrail Shortcut Behaviors in Autonomous AI Agents: A Technical, Safety, and Legal Liability Analysis. Version 1.0. Zenodo.

Then add the DOI after Zenodo publication.
