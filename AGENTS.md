## Project purpose
This repository contains an uncalibrated physics-informed surrogate simulator for IGO / In-Ga-O oxide semiconductor DOE ranking.

Use it for:
- relative DOE ranking,
- hypothesis organization,
- planning calibration with future experimental data.

This is not calibrated TCAD and not experimental proof.

## Scientific claim boundaries
Do not claim:
- calibrated TCAD prediction,
- experimental proof,
- single-crystal IGO,
- epitaxial IGO on SiO2,
- DRAM-ready vertical IGO,
- exact oxygen vacancy concentration from XPS O 1s,
- Samsung/internal/confidential assumptions.

Use cautious terms:
- physics-informed surrogate,
- DOE ranking,
- hypothesis organization,
- oxygen-defect proxy,
- process-structure-electrical correlation.

## Coding rules
- Prefer small, reviewable patches.
- Preserve existing public API unless explicitly asked.
- Add tests when changing model logic.
- Keep deterministic behavior for model outputs.
- Do not use Python built-in hash() for deterministic seeds.
- Use hashlib.sha256 for stable config-level seeding.
- If generated CSV/figures/report outputs change, state how to regenerate them.

## Required checks
Run when possible:
- python -m py_compile igo_semi_tcad_simulator_v1.py igo_visual_doe_v2.py run_igo_modeler_v3.py
- python run_igo_modeler_v3.py
- python -m pytest -q

## Final response format
Every Codex final response must include:
- Files changed
- Summary of changes
- Commands run
- Test results
- Generated output row counts
- Remaining risks / assumptions
- Whether PR is safe to create
