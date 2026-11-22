# TACITUS knowledge-context starting point

Reusable context for teams working with knowledge.

Start with the maintained, tested Python reference below. It builds an explicit source graph, applies a semantic layer, prepares a bounded context capsule and can produce a cited model draft. This organization repository pins the implementation as a Git submodule so the code has one maintained source.

[Website](https://tacitus.me/) · [TACITUS organization](https://github.com/TACITUS-me) · [LinkedIn](https://www.linkedin.com/company/tacitus-me) · [Research index](https://github.com/sargonxg/TACITUS-Knowledge-Pipeline-open/tree/main/research)

## Clone and run

```sh
git clone --recurse-submodules https://github.com/TACITUS-me/Open_Starting_Kpipeline_TACITUS.git
cd Open_Starting_Kpipeline_TACITUS/maintained-pipeline/reference-pipeline
PYTHONPATH=src python -m unittest discover -s tests -v
PYTHONPATH=src python -m tacitus_pipeline build \
  --input examples/team-handoff/collection.json \
  --ontology ontology/team-knowledge.json \
  --layer layers/team-handoff.json \
  --question "What context should travel with a team handoff?" \
  --app-export --output build/team-handoff
```

Python 3.11+ with the standard library. The demonstration discussion is authored fixture data. In the authenticated App Library, choose Import context graph, preview the resulting `app-bundle.json` and save the capsule and artefact. Imported interpretations enter the review flow. Hosted generation is paused.


## Inspect the work

- [Implementation and outputs](https://github.com/sargonxg/TACITUS-Knowledge-Pipeline-open/tree/main/reference-pipeline): graph JSON/JSON-LD, capsule, workflow plan, receipt and review sheet.
- [Ontology guide](https://github.com/sargonxg/TACITUS-Knowledge-Pipeline-open/blob/main/reference-pipeline/docs/ontology.md): entity types and valid relationships.
- [Semantic layers](https://github.com/sargonxg/TACITUS-Knowledge-Pipeline-open/blob/main/reference-pipeline/docs/semantic-layers.md): task selection, evidence requirements and review questions.
- [Model and agent workflow](https://github.com/sargonxg/TACITUS-Knowledge-Pipeline-open/blob/main/reference-pipeline/docs/model-workflows.md): explicit providers and finite evidence inspection before a draft.
- [Workbench reader](https://github.com/sargonxg/tacitus-workbench/blob/main/apps/workbench/docs/policy-workflow.md): inspect the real model draft beside exact evidence.

The Syria example is a historical source exercise, not a current situation assessment. Exact citation checks do not establish semantic truth or expert approval. The one-task model smoke test did not establish general quality or efficiency gains.

![Actual policy draft and retained source evidence](https://raw.githubusercontent.com/sargonxg/TACITUS-Knowledge-Pipeline-open/main/assets/showcase/policy-workflow-desktop.png)

## Earlier notebooks

The original notebooks, queries and requirements remain in this repository, with their [earlier documentation](docs/legacy-notebook.md). They are historical experiments with separate provider and database requirements, not part of the credential-free reference's test result. Verify their service dependencies before running them.

The maintained source currently lives under the founder's public account; it has not been transferred. Original code licenses and third-party source rights remain attached. TACITUS App hosted generation remains paused; the local reference is a separate working path.

## Learn, inspect and verify

[Practical guide, code and research](TACITUS_GUIDE.md) · [Original 8-bit teaching adventure](tacitus-demo/index.html) · [Credits](tacitus-demo/CREDITS.md)

![Original TACITUS Source Workshop: saved sources, typed structure, bounded context and human review](https://raw.githubusercontent.com/sargonxg/sargonxg/a91027079c8ff8ebbd3623898a5e03a13cd80df5/assets/tacitus-source-workshop-8bit.png)

*Original concept illustration; the scene and documents are fictional. [Artwork and reuse](https://github.com/sargonxg/sargonxg/blob/a91027079c8ff8ebbd3623898a5e03a13cd80df5/docs/VISUAL_IDENTITY.md).*

## Format boundaries and verification

The pinned compiler includes the generic team ontology, explicit App export, a reproducible source-edition proof and the controlled model-evaluation protocol. Its 48 tests pass locally without a model account. App import uses its own authenticated preview, native versions and human review flow. [Import contract](https://github.com/sargonxg/TACITUS-Knowledge-Pipeline-open/blob/main/reference-pipeline/docs/app-import.md)

Earlier notebooks and other context formats retain their own contracts. Source rights and licenses remain attached. Hosted generation in the TACITUS App is paused.
