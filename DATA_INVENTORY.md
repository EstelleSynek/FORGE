# Utah FORGE — Fiber-Optic Sensing Data from Circulation Tests: Data Inventory

- **Compiled:** 2026-10-09 by Sarah Synek, with Claude Code
- **Source:** DOE Geothermal Data Repository (GDR), https://gdr.openei.org — all files licensed CC BY 4.0 unless noted on the GDR page
- **Local root:** `/data2/FORGE/data/` (relative paths below are from this root)
- **Search basis:** GDR search "circulation fiber" (first page of 140 results reviewed) plus targeted web searches. Some smaller related submissions may have been missed.
- **Metadata snapshots:** `_metadata/gdr_pages/<id>.html` (GDR landing pages as of download date), `_metadata/gdr_manifest.json` (parsed file list with remote sizes/descriptions), `_metadata/checksums.sha256`

## Context

All fiber-optic data are from **well 16B(78)-32** (production well) during cross-well circulation from injector **16A(78)-32**.

- **2023–2024:** fibers permanently installed behind casing in 16B (FOGMORE/Rice-Silixa cable, and a second cable installed by UT Austin/Shell; Neubrex interrogation).
- **Aug 2025:** fibers in metal tubes inside 1.75-in coiled tubing run to the bottom of the cased section (~10,100 ft MD).
- Depths are generally MD relative to the rotary kelly bushing (RKB) in feet; times are UTC; Neubrex DTS temperatures in °F.

## Summary by test

| Test | Fiber data available locally | Key submissions |
|---|---|---|
| July 2023 low-rate circulation (Jul 13–20 cementing/circulation; DAS MEQ on Jul 19–20) | Neubrex DAS, absolute strain, RFS strain change & rate, DTS, FBE; Rice/Silixa raw DAS event triggers (SEG-Y); DAS MEQ catalogs | 1565, 1747, 1739, 1613, 1559 |
| April 2024 9-hr dual-well circulation (post-stimulation, Apr 27) | Neubrex DTS (Apr–May 2024, stimulation + circulation) | 1617, 1685, 1624 |
| August 2024 extended dual-well circulation (Aug 4–Sep 5; fiber data Aug 4–16) | Neubrex DTS, Brillouin absolute strain, RFS DSS strain change & rate | 1721, 1687, 1670 |
| August 2025 circulation + huff-and-puff (Texas Tech / CSULB) | Neubrex RFS DSS strain change & rate; calibrated DTS (HDF5 + PRODML) | 1825, 1826, 1822 |

## Detailed inventory

### 00 — Fiber installation (reference)

**GDR 1603 — Utah FORGE 3-2417: Well 16B(78)-32 Fiber-Optic Cable Installation Report** · https://gdr.openei.org/submissions/1603
`00_fiber_installation/GDR1603_Rice_Silixa_fiber_install_report/`
- `milestone7p2p1_fiberInstaRiceSilixa_FORGE.pdf` (5.93 MB) — FOGMORE behind-casing cable installation, July 2023.

### July 2023 circulation test

**GDR 1565 — Neubrex Well 16B(78)-32 Circulation Test Fiber Optics Monitoring Data and Reports – July 2023** · DOI [10.15121/2222469](https://doi.org/10.15121/2222469)
`2023-07_circulation/GDR1565_Neubrex_DAS_DSS_DTS_FBE_data/`
- `Neubrex.zip` (3.36 GB) — DAS, absolute strain, strain change, strain change rate, DTS, FBE; includes collection report and read instructions. Processed Sep–Oct 2023.

**GDR 1747 — 3-2417: DAS Microseismic Event Records From Circulation Test – July 2023** (Rice / FOGMORE) · https://gdr.openei.org/submissions/1747
`2023-07_circulation/GDR1747_DAS_microseismic_event_records_SEGY/`
- `SEG.tar.gz` (17.07 GB) — raw DAS triggered-event waveforms, SEG-Y, nanostrain-rate units; Silixa Carina and iDAS v2.
- `FORGE_DAS_Circulation2023_ChannelMapping.csv` (160 kB) — channel coordinates.
- `README_CirculationTriggers_2023.txt`

**GDR 1739 — 3-2417: DAS Microseismic Event and MT Catalog [Final, Relocated], 2023** · https://gdr.openei.org/submissions/1739
`2023-07_circulation/GDR1739_DAS_microseismic_catalog_final/`
- `FOGMORE_DAS_event_catalogue_circulation2023.csv` — relocated catalog with moment tensors / Mw where determinable.
- `Header_Description.txt`, `README_CirculationCatalog_2023.txt`
- `VeraRodriguez_etal_SGW2025.pdf` — Stanford Geothermal Workshop 2025 paper (workflow).

**GDR 1613 — 3-2417: DAS Microseismic Event Catalog, 2023 (preliminary)** · DOI [10.15121/2376139](https://doi.org/10.15121/2376139)
`2023-07_circulation/GDR1613_DAS_microseismic_catalog_prelim/`
- `FORGE_DAS_event_catalogue_circulation.csv`, `Inverted_1D_VelocityModel.csv`, `README.txt`
- `FOGMORE_MEQ_Circulation2023.pdf` — methods report (IMAGE 2024). Superseded by 1739.

**GDR 1559 — Neubrex Cementing and Circulation Fiber Optics Monitoring Reports – July 2023** · https://gdr.openei.org/submissions/1559
`2023-07_circulation/GDR1559_Neubrex_cementing_circulation_reports/`
- Cementing technical report (7.49 MB PDF); circulation test DAS-FBE report (4.25 MB PDF).

### April 2024 circulation test (post-stimulation, 9 hr)

**GDR 1617 — Well 16B(78)-32 Distributed Temperature Sensing Data from April and May 2024** · DOI [10.15121/2407047](https://doi.org/10.15121/2407047)
`2024-04_circulation/GDR1617_Neubrex_DTS_Apr-May2024/`
- `Stimulation Neubrex DTS_new.zip` (5.17 GB) — HDF5 DTS + PowerPoint report. Yokogawa 3000DTSX, 3.28 ft spatial / 129 s temporal sampling.
- ⚠ Third-party P-T gauge data unreliable after 2024-04-20 (per GDR).
- ⚠ No standalone RFS-DSS strain dataset for the April 2024 circulation was found on GDR; strain results appear only in reports (1685, 1624, 1670).

**GDR 1685 — Post Hydraulic Fracturing 9 Hour Dual Well Circulation Test Fiber Optic Monitoring Report – April 2024** · https://gdr.openei.org/submissions/1685
`2024-04_circulation/GDR1685_Neubrex_9hr_circulation_report/`
- `Neubrex_2024_FORGE_Evo3_April_2024_Circulation_Test_Analysis_Final.pdf` (5.78 MB) — RFS-DSS + DTS analysis integrated with pump/discharge rates.

**GDR 1624 — Neubrex Stimulation Fiber Optic Monitoring Reports – April and May 2024** (context for 1617) · https://gdr.openei.org/submissions/1624
`2024-04_circulation/GDR1624_Neubrex_stimulation_reports/`
- Stimulation of 16A stages 3–10 technical report (9.45 MB PDF).
- Frac-period thermal DTS analysis rev3 (3.37 MB PDF) — documents correction for nonlinear optical losses on the multimode fiber.

### August 2024 extended circulation test

**GDR 1721 — Well 16B(78)-32 DTS, RFS DSS Strain, and Absolute Strain Circulation Test Fiber Optic Data – August 2024** · DOI [10.15121/2531108](https://doi.org/10.15121/2531108)
`2024-08_circulation/GDR1721_Neubrex_DTS_DSS_absolute_strain_data/`

| File | Measurement | Coverage (UTC) | Size |
|---|---|---|---|
| `...DTS - mmf 2 - evo 4 - part 1.h5` | DTS, multimode, 1 m | Aug 4 18:13 – Aug 4 20:29 | 0.9 MB |
| `...DTS - mmf 2 - evo 4 - part 2.h5` | DTS | Aug 12 19:24 – Aug 16 14:12 | 3.8 MB |
| `...absolute strain - smf 2 - evo 4 - part 1.h5` | Brillouin absolute strain, 20 cm | Aug 4 20:51 – Aug 11 15:08 | 537 MB |
| `...absolute strain - smf 2 - evo 4 - part 2.h5` | Brillouin absolute strain | Aug 12 20:04 – Aug 16 14:05 | 687 MB |
| `...strain change - smf 2 - evo 4 - part 1.h5` | RFS DSS strain change, 20 cm | Aug 9 20:00 – Aug 11 15:00 | 223 MB |
| `...strain change - smf 2 - evo 4 - part 2.h5` | RFS DSS strain change | Aug 12 18:37 – Aug 16 14:12 | 275 MB |
| `...strain change rate - smf 2 - evo 4 - part 1.h5` | RFS DSS strain change rate | Aug 9 20:00 – Aug 11 15:00 | 137 MB |
| `...strain change rate - smf 2 - evo 4 - part 2.h5` | RFS DSS strain change rate | Aug 12 18:37 – Aug 16 14:17 | 174 MB |
| `FORGE Utah Beaver well 16B(78)-32 - EVO 4 - Neubrex Transmittal document.pdf` | File structure documentation | — | 0.8 MB |

**GDR 1687 — Extended Dual Well Circulation Testing Fiber Optic Monitoring Report – August 2024** · https://gdr.openei.org/submissions/1687
`2024-08_circulation/GDR1687_Neubrex_extended_circulation_report/`
- Neubrex Evo4 analysis report with SLB PLT metadata (10.95 MB PDF).

**GDR 1670 — Neubrex Stimulation and Circulation Fiber Optics Reports – Summer 2024** · DOI [10.15121/2448100](https://doi.org/10.15121/2448100)
`2024-08_circulation/GDR1670_Neubrex_stim_circ_reports_summer2024/`
- `Neubrrex Fiber Optic.zip` (13.26 MB) — reports on strain-rate and temperature-change data (filename spelling as published).

### August 2025 circulation and huff-and-puff tests (Texas Tech / CSULB)

**GDR 1825 — Neubrex RFS DSS Fiber Optic Strain Data – August 2025** · https://gdr.openei.org/submissions/1825 (no DOI yet)
`2025-08_circulation_huffpuff/GDR1825_Neubrex_RFS_DSS_strain_data/`
- `Utah Forge 16B(79)-32 - strain change - evo 5.h5` (2.72 GB) — ⚠ "79" is a typo in the published filename; it is well 16B(78)-32.
- `Utah Forge 16B(78)-32 - strain change - prodml - evo 5.h5` (4.13 GB)
- `Utah Forge 16B(78)-32 - strain change rate - evo 5.h5` (1.10 GB)
- `Utah Forge 16B(78)-32 - strain change rate - prodml - evo 5.h5` (2.38 GB)
- Units: microstrain, ft, UTC.

**GDR 1826 — Neubrex DTS Fiber Optic Temperature Data – August 2025** · https://gdr.openei.org/submissions/1826 (no DOI yet)
`2025-08_circulation_huffpuff/GDR1826_Neubrex_DTS_data/`
- `Utah Forge 16B(78)-32 - DTS calibrated - evo 5.h5` (124 MB)
- `Utah Forge 16B(78)-32 - DTS calibrated - prodml - evo 5.h5` (323 MB)
- Units: °F, ft.

**GDR 1822 — Report on Fiber Optic Monitoring of August 2025 Circulation and Huff and Puff Tests** · https://gdr.openei.org/submissions/1822
`2025-08_circulation_huffpuff/GDR1822_Neubrex_technical_report/`
- Neubrex technical report (14.67 MB PDF) — test context, depth calibration, RFS DSS / DTS / DAS results. Required for interpreting 1825/1826.

**GDR 1827 — Neubrex-Texas Tech-CSULB Circulation Fiber Optic DAS Data – August 2025** · https://gdr.openei.org/submissions/1827
- ⚠ **NOT DOWNLOADED** — submission "in progress", no files published as of 2026-10-09. Processed DAS / LF-DAS / FBE expected. Re-check later.

### Related

**GDR 1837 — 4-2492 (UT Austin): Final Report and Presentation on Innovative Stimulation Design and Fiber-Optic Diagnostics** · https://gdr.openei.org/submissions/1837
`related/GDR1837_UTAustin_4-2492_fiber_diagnostics_final_report/`
- Final technical report (16.13 MB PDF); closeout presentation video (269 MB MP4). Covers DTS/DAS/DSS integration for stimulation and circulation in 16A/16B.

## Known gaps / caveats

1. August 2025 DAS (GDR 1827) not yet published.
2. No standalone April 2024 RFS-DSS strain data file found; only DTS (1617) plus reports.
3. No August 2024 DAS dataset turned up in this search (only DTS/DSS in 1721); not exhaustively checked.
4. 1825 filename typo "16B(79)-32".
5. One listing of the 2025 report gives an acquisition date of August 2024; the report title and data say August 2025.
6. Multimode-fiber DTS requires correction for nonlinear optical losses (see 1624 DTS analysis report).
