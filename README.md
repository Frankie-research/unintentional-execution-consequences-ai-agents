# Unintentional Execution Consequences and Guardrail Shortcut Behaviors in Autonomous AI Agents: A Technical, Safety, and Legal Liability Analysis

**Author:** Frankie Mak  
**Credentials:** MBA | Graduate Certificate in Cyber Security  
**Role:** Independent Researcher and Technology Practitioner  
**Location:** Australia  
**Contact:** frankiemak.research@gmail.com  
**Version:** 1.0 — Public Release  
**Publication date:** 05 October 2026

## Abstract

This report examines how autonomous AI agents can produce unintended execution consequences when optimization objectives, proxy metrics, operational constraints, and environmental affordances do not fully encode human intent. It develops a taxonomy of guardrail shortcut and higher-order lateral shortcut behaviors, including specification gaming, reward tampering, oversight-aware behavior, covert power-seeking scenarios, and safety-monitoring interference. The report distinguishes observed practitioner evidence from analytical scenarios and external AI-safety research, using a personal-computer Hermes Agent deployment as a bounded case study rather than as proof that advanced alignment failures occurred in that deployment. Particular attention is given to root causes, hard architectural boundaries, independent monitoring, least privilege, reversibility, capability minimization, and the engineering difficulty of modifying the system intended to enforce its own constraints. The report also considers legal and governance implications for autonomous software deployed with meaningful execution authority.

## Research status

This is an **independent practitioner research report**. It is not presented as peer-reviewed experimental research.

The report deliberately distinguishes:

- **Observed practitioner evidence** — events and architecture documented in the Hermes personal-computer case study.
- **Analytical scenarios** — hypothetical failure pathways used to test the security argument.
- **External research evidence** — established AI-safety and security literature.
- **Legal and governance analysis** — interpretation of relevant liability and regulatory frameworks.

The Hermes case study therefore **does not claim that Hermes itself demonstrated alignment faking, covert power seeking, or safety-research sabotage**. Those concepts are analysed as higher-order risks that become relevant when an agent has sufficient environmental awareness and execution authority.

## Relationship to the previous Hermes report

This report extends:

> Mak, F. (2026). *Hermes Agent on a Personal Computer: Security, Sandboxing, Automation and Reliability Lessons from a Windows/Docker Practitioner Case Study.* Zenodo. https://doi.org/10.5281/zenodo.22985434

The earlier report established the practical security boundary problem around local execution, Docker isolation, filesystem mounts, credentials, scheduled automation, messaging surfaces, path handling, and encoding. This report asks the next question: **what happens when an autonomous agent does not merely make an execution mistake, but discovers a lower-friction path around an intended safeguard?**

## Core topics

- Unintentional execution consequences
- Guardrail shortcut behaviour
- Lateral shortcut behaviour
- Specification gaming and reward misspecification
- Reward / sensor tampering
- Oversight-aware behaviour and alignment faking
- Covert power-seeking scenarios
- Safety-monitoring and evaluation sabotage scenarios
- Least privilege and capability minimisation
- Independent reference monitors
- Reversibility and transaction boundaries
- Immutable / out-of-band telemetry
- The modification problem
- Technical, safety and legal liability

## Files

- `Unintentional_Execution_Guardrail_Shortcuts_AI_Agents_v1.0.docx` — public report (canonical editable source).
- `Unintentional_Execution_Guardrail_Shortcuts_AI_Agents_v1.0.pdf` — public PDF generated directly from the canonical DOCX.
- `CITATION.cff` — machine-readable citation metadata.
- `PUBLICATION_CHECKLIST.md` — release checklist.

## Citation

Please cite the Zenodo version once the DOI is assigned.

A DOI placeholder is intentionally not embedded in this initial repository package; the final DOI should be inserted after the first Zenodo release is published. The GitHub repository URL placeholder in `CITATION.cff` should likewise be replaced with the actual repository URL after repository creation.

## Licence

Recommended licence for the report: **Creative Commons Attribution 4.0 International (CC BY 4.0)**.

The licence applies to the author's report text and original material. Third-party material remains subject to its original licence or rights statement.

## Disclaimer

This report is an independent research and practitioner analysis. It is not legal advice, a security certification, a guarantee of agent behaviour, or evidence that every described failure mode has been empirically demonstrated in the Hermes deployment.
