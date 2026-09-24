# BAGH_SIR — asteroid volume, density and macroporosity from 3D shape models

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21433682.svg)](https://doi.org/10.5281/zenodo.21433682)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](bagh_sir_release/LICENSE)

**Live demo:** https://bagh-sir-tools.streamlit.app

BAGH_SIR is an open Python tool by **Promod Bagh** that computes the volume, bulk density and
macroporosity of asteroids and comets from 3D shape models, and audits the SiMDA catalogue for
physical plausibility.

## What it does

1. **Volume** — signed-tetrahedron and prism methods, cross-verified against each other.
2. **Bulk density** — derived when a mass is supplied.
3. **Macroporosity** — estimated from rock type or grain density.
4. **Plausibility audit** — flags bulk densities that exceed the grain density of the matching
   meteorite class, which are physically impossible.

This is established computational geometry: a validated, transparent implementation, not new
mathematics.

## Validation against spacecraft-measured bodies

| Body | BAGH_SIR (g/cm³) | Published (g/cm³) |
| --- | --- | --- |
| 67P/Churyumov–Gerasimenko | 0.535 | 0.536 |
| Bennu | 1.190 | 1.190 |
| Ryugu | 1.195 | 1.19 |
| Itokawa | 1.865 | 1.9 |

## Audit findings

The audit identifies carbonaceous asteroids carrying catalogued bulk densities of 4.5–6.1 g/cm³,
well above the grain density of carbonaceous meteorites (~2.2–2.9 g/cm³) — among them
(206) Hersilia, (410) Chloris and (34) Circe. Predicted mass corrections are given for each, as
falsifiable targets for future measurement.

## Getting started

```
pip install -r requirements.txt
python3 bagh_sir_release/code/small_body_volume.py bennu.obj 7.329e10
```

Shape models are available from DAMIT, NASA PDS, JAXA and 3d-asteroids.space.
Full documentation, data and worked examples are in [`bagh_sir_release/`](bagh_sir_release/).

## Citing this software

Bagh, Promod (2026). *BAGH_SIR: volume, density and macroporosity of small bodies from 3D shape
models, with a physical-plausibility audit of the SiMDA catalogue*, v1.0.0. Zenodo.
https://doi.org/10.5281/zenodo.21433682

Machine-readable metadata: [`bagh_sir_release/CITATION.cff`](bagh_sir_release/CITATION.cff).

## Author

**Promod Bagh** — Senior Manager (Mechanical), Field Quality Assurance & NDT,
Damodar Valley Corporation, India.

- ORCID: https://orcid.org/0009-0003-1066-4791
- Google Scholar: https://scholar.google.com/citations?user=kmmErswAAAAJ
- GitHub: https://github.com/promodtrishika

## Other work by the author

| Work | Type | DOI |
| --- | --- | --- |
| Mass as Trans-Dimensional Binding: A Dimensional-Accessibility Account of Measurement, the Dark Sector, Space, and Time | Preprint (2026) | [10.5281/zenodo.21581847](https://doi.org/10.5281/zenodo.21581847) |
| The Dimensional Visualization and Interaction Theory: Observation as Dimensional Projection and the Affine-Span Origin of Space | Preprint (2026) | [10.5281/zenodo.19434127](https://doi.org/10.5281/zenodo.19434127) |
| The Geometric Foundation of Dimensional Perception and Space Creation: Proving the Visualization & Interaction Theory (VIT) | Preprint (2026) | [10.5281/zenodo.19860632](https://doi.org/10.5281/zenodo.19860632) |
| The Complete Mathematical Formulation and Sequential Framework of the Multidimensional Mass-Energy Theory (MMET-EXTENDED) | Preprint (2026) | [10.6084/m9.figshare.31428131](https://doi.org/10.6084/m9.figshare.31428131) |
| Multidimensional Mass-Energy Theory: A Unified Framework for Observer-Dependent Reality | Preprint (2025) | [10.6084/m9.figshare.30489179](https://doi.org/10.6084/m9.figshare.30489179) |

## License

MIT — see [`bagh_sir_release/LICENSE`](bagh_sir_release/LICENSE).
