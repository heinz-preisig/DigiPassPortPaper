# Project status

## Portal architecture clarity (completed)

The portal is now described explicitly as a **federation of national portals** — one or several per EU member state, all sharing a common API and data model and linked to external authoritative registries — rather than a single central service.

- [x] Clarify the opening of Section 4 with an explicit federated-portal definition.
- [x] Replace the "centralised triple-store" wording with a federation description.
- [x] Add a dedicated `Federation of National Portals` subsection.
- [x] Ensure the abstract and conclusions reflect the federated concept.
- [x] Refine the wording to allow one or several national portals per member state and clarify cross-federation / external link traversal.
- [x] Commit and push the final changes.

## What changed

- `4_portal_architecture.tex`: added `Federation of National Portals` subsection, replaced "centralised triple-store" with a federation of per-member-state triple-stores, and expanded link traversal to work within and across the federation and to external authoritative registries.
- `1_ESPR.tex`, `2_problem_statement.tex`, `3_Network_model.tex`, `8_discussion.tex`: replaced remaining "centralised" descriptions of the portal with "federated" wording, including figure captions and link-rot discussion.
- `abstract.tex` and `9_conclusions.tex`: now explicitly state the portal is a federation of national portals, one or several per EU member state.

## Notes

- The EU central registry provides identifier resolution, regulatory metadata, and oversight.
- Each national portal stores its own jurisdiction’s DPP data in a triple-store.
- The federation is uniform in API, data model, access governance, and SHACL validation, but operates on national data.
- Links are materialised as persistent IRIs, so information remains resolvable independently of any single endpoint and can span the federation as well as external registries (ECHA, standards bodies, health and safety authorities).

## Authors' Q&A file (completed)

Set up a flat question-and-answer file for the co-authors. Each question names the author it is for, and answers are added directly underneath.

- [x] Decide on a simple Q&A format with the author named in each question.
- [x] Replace `AUTHORS.md` with `AUTHORS_Questions_Answers.md`.
- [x] Commit and push the change.
