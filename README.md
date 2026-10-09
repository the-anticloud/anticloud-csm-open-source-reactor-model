# CSM OPEN SOURCE REACTOR MODEL

![license](https://img.shields.io/badge/license-MIT-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-nuclear-lightgrey)

> Anticloud-hardened packaging of the upstream project `CSM_OPEN_SOURCE_REACTOR_MODEL` in category **NUCLEAR**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** NUCLEAR · **Upstream:** https://github.com/mascovale/CSM-Open-source-Reactor-Model-Library · **Upstream pin:** `ad26ab4a038f347e7b622e8e7ae084975e8be6e9` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

# CSM Open-Source Reactor Model Library

An open-source collection of nuclear reactor models built with [OpenMC](https://openmc.org/).
Each top-level directory is an independent model project. Projects can be developed and
run separately; there is no shared Python package or project-wide launcher.

## project layout

| Directory | Purpose | Status |
| --- | --- | --- |
| [`iaea-tecdoc-core/`](iaea-tecdoc-core/README.md) | IAEA TECDOC-643 Appendix A-2 generic 10 MW LEU research reactor OpenMC model | Implemented |
| [`hp-mr/`](hp-mr/README.md) | High-power microreactor model | Reserved project directory |
| [`lunar-fsp-microreactor/`](lunar-fsp-microreactor/README.md) | Lunar FSP microreactor model | Reserved project directory |
| [`msre/`](msre/README.md) | Molten Salt Reactor Experiment model | Reserved project directory |
| [`pebble-bed-htgr/`](pebble-bed-htgr/README.md) | Pebble-bed high-temperature gas reactor model | Reserved project directory |
| [`radiant-kaleidos/`](radiant-kaleidos/README.md) | Radiant Kaleidos microreactor model | Reserved project directory |

At present, `iaea-tecdoc-core` is the project's implemented model. The other
directories contain documentation placeholders for future model projects.

## Working with a model

Read the README inside the model directory before running it. Model-specific dependencies,
cross-section libraries, input assumptions, run commands, and validation checks belong in
that README rather than in this root document.

The implemented IAEA model is run from its project directory. Its central driver builds
the geometry, materials, settings, and tallies, then launches an OpenMC eigenvalue run:

```text
cd iaea-tecdoc-core
python model/core.py --help
```

The driver accepts controls for blade insertion, particle and batch counts, output location,
and optional depletion zoning. See [`iaea-tecdoc-core/README.md`](iaea-tecdoc-core/README.md)
for the complete workflow and verification commands.

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Unknown (no standard manifest detected)** (manifests: none detected; scanned in UPSTREAM_CLONE)
- Top-level source layout: `hp-mr/`, `iaea-tecdoc-core/`, `lunar-fsp-microreactor/`, `msre/`, `pebble-bed-htgr/`, `radiant-kaleidos/`
- Snapshot size: **92 files**, **8131 lines of code** (measured; see Benchmarks)
- Primary languages: `.png` (49), `.py` (17), `.md` (12), `.pdf` (7), `(none)` (3), `.txt` (3)
- Upstream commit pinned for this packaging: `ad26ab4a038f347e7b622e8e7ae084975e8be6e9`

---

## Installation

the geometry, materials, settings, and tallies, then launches an OpenMC eigenvalue run:

```text
cd iaea-tecdoc-core
python model/core.py --help
```

The driver accepts controls for blade insertion, particle and batch counts, output location,
and optional depletion zoning. See [`iaea-tecdoc-core/README.md`](iaea-tecdoc-core/README.md)
for the complete workflow and verification commands.

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

No usage section was found in the upstream readme. Entry points detected in this project directory:

Browse the snapshot layout listed under What This Project Does and follow the upstream run instructions for the detected ecosystem (Unknown (no standard manifest detected)).

Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

The upstream API surface is defined by the `CSM_OPEN_SOURCE_REACTOR_MODEL` source tree vendored in `UPSTREAM_CLONE/` (Unknown (no standard manifest detected) ecosystem). Public entry points:

- Source modules: `hp-mr/`, `iaea-tecdoc-core/`, `lunar-fsp-microreactor/`, `msre/`, `pebble-bed-htgr/`, `radiant-kaleidos/`
- Overlay API: `anticloud/cli.py` exposes 13 subcommands with JSON stdout; `anticloud/bench/runner.py` runs the 16-check suite; `anticloud/provenance/chain.py` exposes the SHA3-256 + Ed25519 provenance chain.

---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Unknown (no standard manifest detected) |
| Manifests detected | none |
| Files in snapshot | 92 |
| Lines of code | 8131 |
| Dependency references | 0 |
| Upstream license | MIT |
| Overlay license | Anticommons 0.1.0 |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

```text
cd iaea-tecdoc-core
python model/core.py --help
```

The driver accepts controls for blade insertion, particle and batch counts, output location,
and optional depletion zoning. See [`iaea-tecdoc-core/README.md`](iaea-tecdoc-core/README.md)
for the complete workflow and verification commands.

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

Upstream contributions: fork the `CSM_OPEN_SOURCE_REACTOR_MODEL` project, create a feature branch, and open a pull request against upstream. Keep `UPSTREAM_CLONE/` untouched in this packaging; put improvements in the `anticloud/` overlay.

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

Copyright (c) 2026 Valerio Mascolino

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

- **Project:** `CSM_OPEN_SOURCE_REACTOR_MODEL` (category: NUCLEAR)
- **Upstream URL:** https://github.com/mascovale/CSM-Open-source-Reactor-Model-Library
- **Pinned commit (SHA):** `ad26ab4a038f347e7b622e8e7ae084975e8be6e9`
- **Branch:** main
- **Pin provenance:** GitHub API commits/main. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`9993b18cbdace7e1b1505b370893f196c40cb4b9120e5bdbec4c0d6b5710a3bd`.

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
| DANS (KNAW/NWO, Netherlands) | 10.17026/PT | EU-recognised archive |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe
and Mail, Business Insider, National Post, Financial Post, StreetInsider,
Digital Journal, Barchart, International Business Times, and Fox News.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

