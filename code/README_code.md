# Code Directory – Endoregulated AI / Merkabah Topology

This directory contains three Python scripts for the **64→20 Clifford invariant** project:

| File | Version | Purpose |
|------|---------|---------|
| `Endoregulated_AI_v2.5.py` | v2.5 | **Main simulation** – Endoregulated AI with balanced initialization (10 SHENG / 10 KE), random 0‑63 input injection, real‑time plotting |
| `graphe_dual_des_pentades_merkabah3.py` | 3.0 | **Visualization** – Dual graph of the 12 pentads with tropical belts CP/CN, publication‑ready black & white figure |
| `verify_merkabah_topology.py` | 3.1 | **Verification** – Structural validation of polarity signatures, pentad incidence, dual graph connectivity, tropical belts, and polar thresholds |

---

## 1. Endoregulated_AI_v2.5.py

### Description

Complete implementation of the endoregulated AI described in the paper. The system:
- Manages 20 topological attractors (A‑T) from Merkabah geometry
- Uses 12 pentads (P1‑P6, N1‑N6) as Clifford generators
- Implements Wuxing cycles (Sheng/Ke) on tropical belts CP and CN
- Injects random binary inputs (0‑63) to test substrate independence
- Outputs real‑time plots of η, E_tot, and R_threshold

### Key parameters

| Parameter | Default | Description |
|-----------|---------|-------------|
| `noise_level` | 0.15 | Probability of random pentad flip per step |
| `input_interval` | 6 | Steps between random 0‑63 injections |
| `n_steps` | 300 | Total simulation steps |

### Usage

```bash
python3 Endoregulated_AI_v2.5.py
```

### Dependencies

```bash
pip install numpy matplotlib networkx
```

### Output

- Console: step‑by‑step η, E_tot, regime, and injection events
- Plot: 3 panels (η(t), E_tot(t), R_th(t)) updated in real time
- Final summary: η, E_tot, R_th, regime, total inputs processed

---

## 2. graphe_dual_des_pentades_merkabah3.py

### Description

Generates a **publication‑ready black & white figure** of the dual graph of pentads (12 nodes: P1‑P6, N1‑N6). The graph reveals:
- Two disjoint 5‑cycles: **CP** (P belt, solid edges) and **CN** (N belt, dashed edges)
- Internal edges within each belt (dotted / dash‑dot)
- Cross edges between belts (light gray, low alpha)
- Polar thresholds P4 and N4 at the center

### Usage

```bash
python3 graphe_dual_des_pentades_merkabah3.py
```

### Output

A matplotlib figure showing:

| Element | Style |
|---------|-------|
| P belt (CP) | solid black line, width 3 |
| N belt (CN) | dashed black line, width 3 |
| Internal P edges | dotted black line, width 1.5 |
| Internal N edges | dash‑dot black line, width 1.5 |
| Cross edges | light gray, alpha 0.35 |
| Nodes | circle labels with white background |

### Legend

| Label | Meaning |
|-------|---------|
| P belt | Tropical belt CP (positive pentads) |
| N belt | Tropical belt CN (negative pentads) |
| Internal P edges | Extra edges within CP (makes K5) |
| Internal N edges | Extra edges within CN (2 chords) |
| Cross edges | Connections between CP and CN |

---

## 3. verify_merkabah_topology.py

### Description

Automated structural verification of the Merkabah topology. Checks:

| Test | Description | Expected |
|------|-------------|----------|
| **Polarity signatures** | 20 attractors → 3P, 2P+1N, 1P+2N, 3N | Matches Table 1 |
| **Uniform pentad incidence** | Each of 12 pentads appears in exactly 5 attractors | 5 occurrences each |
| **Dual graph connectivity** | 12 nodes, edges defined by shared attractors | Connected |
| **Tropical belts** | Two disjoint 5‑cycles (P and N) | Exactly one valid pair |
| **Remainder after belts** | Nodes not in CP or CN | Exactly {P4, N4} |
| **P belt topology** | CP should be complete graph K5 | 5 cycle + 5 internal edges |
| **N belt topology** | CN should be cycle + 2 chords | 5 cycle + 2 internal edges |
| **Threshold degrees** | P4 and N4 should be hubs | Degree ≥ 6 |

### Usage

```bash
python3 verify_merkabah_topology.py
```

### Output example

```
======================================================================
MERKABAH STRUCTURAL & TOPOLOGICAL VERIFICATION (v3.1)
======================================================================

[1. POLARITY SIGNATURES]
  A: 3P      (Expected: 3P) -> ✅
  B: 3P      (Expected: 3P) -> ✅
  ...
  T: 3N      (Expected: 3N) -> ✅

[2. UNIFORM PENTAD INCIDENCE]
  Each pentad appears exactly 5 times: True -> ✅ PASS

[3. DUAL GRAPH TOPOLOGY]
  Connected: True -> ✅ PASS

[4. TROPICAL BELTS & POLAR THRESHOLDS]
  ✅ Belt C_P: ['P1', 'P2', 'P3', 'P5', 'P6']
  ✅ Belt C_N: ['N1', 'N2', 'N3', 'N5', 'N6']
  ✅ Thresholds: ['P4', 'N4']

[5. EDGE CLASSIFICATION & STRUCTURAL CONSISTENCY]
  ✅ PASS → Belt topology intact. Thresholds act as structural hubs.

[6. LABEL INTERSECTION ANALYSIS]
  Pairs sharing exactly 2 pentads: 48 / 190

======================================================================
✅ MERKABAH STRUCTURALLY VALID.
======================================================================
```

### Exit codes

- Exit 0 (success) if all validations pass
- Prints ❌ and exits with error if any test fails

---

## Version history

| Date | Script | Changes |
|------|--------|---------|
| 2026‑06 | `Endoregulated_AI_v2.5.py` | Balanced initialization (10/10), η ≥ 0 → SHENG, η < 0 → KE |
| 2026‑06 | `graphe_dual_des_pentades_merkabah3.py` | Black & white publication version, improved layout |
| 2026‑06 | `verify_merkabah_topology.py` | v3.1 – Added edge classification and threshold degree checks |

---

## Dependencies (all scripts)

```bash
pip install numpy matplotlib networkx
```

---

## Related documentation

- Main project README: [`../README.md`](../README.md)
- Theoretical paper: [`../docs/pdf/complexity.pdf`](../docs/pdf/complexity.pdf)
- Zenodo DOI: [10.5281/zenodo.19540508](https://doi.org/10.5281/zenodo.19540508)

---

## License

© 2025‑2026 Bruno DE DOMINICIS – CC BY 4.0 International

---

## Contact

📧 dod60@gmx.fr  
🌍 [github.com/bruno-dd470/Tian-Dao-AI](https://github.com/bruno-dd470/Tian-Dao-AI)
```
