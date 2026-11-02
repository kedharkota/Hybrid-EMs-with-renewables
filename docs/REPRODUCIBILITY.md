# Reproducibility and visual sources

## Scope

This guide describes what is available in the committed project and what is required to reproduce it. The documentation update inspected source and saved outputs; it did not rerun model training or hardware/simulation experiments.

## Required inputs

Supply model-specific input signals and any external workspace variables requested by Simulink. Fuzzy Logic Toolbox may be required by fuzzy-controller blocks. MATLAB simulations were not executed during this documentation update.

## Entry point

Requires MATLAB and Simulink. The repository does not specify a MATLAB release or complete toolbox list. Check model dependencies in your installation before running.

From MATLAB, change to the repository directory and inspect the models:

```matlab
open_system('base.slx');
open_system('ev_fuzzy.slx');
```

Review initial conditions, source inputs, controller configuration, and simulation stop time before selecting **Run**.

## Evidence and interpretation

The committed presentation includes simulation results and a literature review. Literature-review cost-reduction figures belong to cited studies and should not be presented as measured results from this repository. The preview above reproduces an original controller-model image from the presentation.

## Visual provenance

All screenshots and experiment figures are tied to repository material. Workflow SVGs are explanatory illustrations. The full image inventory is in [assets/sources.json](assets/sources.json).

| Visual | Source |
| --- | --- |
| [overview.svg](assets/overview.svg) | New explanatory project-workflow diagram based on the committed source and documentation; not a screenshot or measured result. |
| [simulation.png](assets/simulation.png) | CS Final.pptx, slide 16, original embedded fuzzy-controller model image ppt/media/image9.png |

## Validation

```bash
python tools/check_docs.py
```

The standard-library checker validates README/docs local link destinations and SVG/PNG/JPEG headers. It makes no external requests and installs no project runtime dependencies. External web links, model accuracy, image semantics, and full application execution need separate review.

## Reproduction record

For a new experiment or demo, record the source commit, environment versions, data provenance and split, configuration, command/notebook order, and resulting artifacts. Only label a measurement as reproduced after completing that run. Keep credentials and restricted datasets outside version control.
