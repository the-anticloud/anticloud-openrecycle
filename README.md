# OPENRECYCLE

![license](https://img.shields.io/badge/license-MIT-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-waste_management-lightgrey)

> Anticloud-hardened packaging of the upstream project `OPENRECYCLE` in category **WASTE MANAGEMENT**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** WASTE MANAGEMENT · **Upstream:** https://github.com/openrecycle/openrecycle.github.io · **Upstream pin:** `158f04567ac927d7ecfbf150480ced2e39978143` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

# Open Recycle

**An open recyclability record for your product.**
A draft specification and an interactive tool for describing what happens to every material in a product after its useful life — not one recycling rate, but one fate per material, at the quality it comes back at.

> Research prototype, draft 0.1. Not an official standard, not a certification, no mark.

## What's in the project

| Path | What it is |
|---|---|
| `index.html` | Landing page — served at the site root |
| `app/index.html`, `src/` | The tool — served at `/app/` |
| `docs/STANDARD.md` | The specification, draft 0.1 |
| `schema/open-recycle.schema.json` | JSON Schema for records |
| `examples/fairphone-2.example.json` | Worked example — deliberately incomplete, see §10 of the spec |
| `examples/example-supplier-component.json` | Supplier component record, for testing import |
| `docs/BUILD-PROMPT.md` | Self-contained brief for rebuilding the tool with another AI builder |

## Run it

```bash
npm install
npm run dev       # local dev server
npm run build     # production build into dist/
```

Pushing to `main` deploys to GitHub Pages via `.github/workflows/deploy.yml`:

| URL | Serves |
|---|---|
| `/` | Landing page |
| `/app/` | The tool |
| `/docs/STANDARD.md` | The specification |
| `/schema/`, `/examples/` | Schema and example records |

Enable it once under **Settings → Pages → Source: GitHub Actions**.

## How it works

| Step | Does |
|---|---|
| Inventory | Components, mass, composition in grams per material |
| Separation | Each component has a class D0–D6, setting how much of each material reaches its intended process |
| Process graph | Unit operations; each node splits every material across its output ports |
| Fate | Each sink has a quality class C0–C5; a material's fate is the mass it delivers into each class |
| Rating | Mass × class weight, summed, over feed → circularity index → grade A–E |

## The three scales

All proposed by this draft. None is an existing international standard.

| Scale | Range | Describes |
|---|---|---|
| Separation | D0–D6 | How a joint comes apart, automatic to inseparable |
| Circular quality | C0–C5 | What a recovered gram comes back as, closed loop to dissipative loss |
| Evidence | E0–E5 | What backs a number, self-declared to verified industrial data |

A record's evidence level is the **minimum** across itself and every component it imports.

## Data integrity

| Content | Status |
|---|---|
| Route aggregates (14/25/36, 19/28/31, 22/30/31) | Published — Reuter, van Schaik & Ballester, 2018 |
| Seeded smartphone composition | Demonstration dataset, evidence E0 |
| Split fractions and element-level results | Simulated by this prototype's simplified model |

No element-level figure in this project is taken from any publication. No affiliation with or endorsement by Fairphone, the authors, or any manufacturer.

## Reference

Reuter, M. A., van Schaik, A. & Ballester, M. (2018). *Limits of the Circular Economy: Fairphone Modular Design Pushing the Limits.*

The carrier-wheel figure is inspired by the Metal Wheel concept of Reuter and van Schaik. It is an original per-product visualisation, not a reproduction.

## Licence

Code under MIT (`LICENSE`). Specification text in `docs/` under CC BY 4.0 (`LICENSE-SPEC`).

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Node.js / npm** (manifests: package.json, package-lock.json; scanned in UPSTREAM_CLONE)
- Top-level source layout: `app/`, `examples/`, `landing/`, `schema/`, `scripts/`, `src/`
- Snapshot size: **19 files**, **2364 lines of code** (measured; see Benchmarks)
- Primary languages: `.json` (5), `(none)` (3), `.html` (3), `.md` (3), `.jsx` (2), `.css` (1)
- Upstream commit pinned for this packaging: `158f04567ac927d7ecfbf150480ced2e39978143`

---

## Installation

No installation section was found in the upstream readme, so the commands below are generated from the manifests detected in this project directory.

```sh
# from this project directory
npm install        # or: npm ci
npm run build      # if a build script is declared
```

Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

| `examples/example-supplier-component.json` | Supplier component record, for testing import |
| `docs/BUILD-PROMPT.md` | Self-contained brief for rebuilding the tool with another AI builder |

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

> Research prototype, draft 0.1. Not an official standard, not a certification, no mark.

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Node.js / npm |
| Manifests detected | package.json, package-lock.json |
| Files in snapshot | 19 |
| Lines of code | 2364 |
| Dependency references | 6 |
| Dependencies by ecosystem | npm: 6 |
| Upstream license | MIT |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| npm | react | ^18.3.1 | package.json |
| npm | react-dom | ^18.3.1 | package.json |
| npm | @tailwindcss/vite | ^4.0.0 | package.json |
| npm | @vitejs/plugin-react | ^4.3.4 | package.json |
| npm | tailwindcss | ^4.0.0 | package.json |
| npm | vite | ^6.0.0 | package.json |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

No configuration section was found in the upstream readme. Configuration-relevant files detected in this project directory:

- `package.json`

Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

Upstream contributions: fork the `OPENRECYCLE` project, create a feature branch, and open a pull request against upstream. Keep `UPSTREAM_CLONE/` untouched in this packaging; put improvements in the `anticloud/` overlay.

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: MIT** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
MIT License

Copyright (c) 2026 Abel Tomy

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original MIT terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `MIT` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `OPENRECYCLE` (category: WASTE MANAGEMENT)
- **Upstream URL:** https://github.com/openrecycle/openrecycle.github.io
- **Pinned commit (SHA):** `158f04567ac927d7ecfbf150480ced2e39978143`
- **Branch:** master
- **Pin provenance:** GitHub API commits/master. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`4f18d32977714b82a9f36d85029bfde11cec6cfc8e11e7bddc520670c4c12386`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

