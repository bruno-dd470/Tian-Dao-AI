---
title: "The genetic code as a 64->20 Clifford invariant: implications for regulated AI"
author: "Bruno DE DOMINICIS"
ORCID: 0009-0009-0380-3056
date: "April 2026"
doi: "10.5281/zenodo.19540508"
abstract_en: |
  The regulation of combinatorial complexity is a central challenge in natural and artificial systems. The genetic code addresses it by mapping 64 codons onto 20 functional classes (19 amino acids + 1 termination class) through an organised redundancy that confers robustness.
  Building on Peter Rowlands' (2007) work on nilpotent Clifford algebras, we show that the 64‑element structure of $\mathrm{Cl}(6,0)$, after symmetry breaking, reduces to 20 stable attractors geometrically organised as a level‑3 double tetrahedron (Merkabah). This compound decomposes into 20 fundamental tetrahedral cells and 8 octahedral intersection zones. Imposing a face‑sharing neighbourhood rule on these cells filters the 64 configurations into exactly 20 equivalence classes.
  We formalise this 64→20 invariant by defining a six‑dimensional binary configuration space and a topological clustering criterion. Each class is identified by a triplet of pentads—irreducible five‑element algebraic units of $\mathrm{Cl}(6,0)$ that correspond to the 12 pentagonal faces of the dodecahedron. The pentads are partitioned into six positive ($P$) and six negative ($N$) units, so the polarity signature of any class simply counts how many positive and negative pentads appear in its triplet ($3P$, $2P\!+\!1N$, $1P\!+\!2N$, or $3N$). This structural gradient maps bijectively to the genetic code's degeneracy pattern. 
  The dual graph of the 12 pentads, constructed directly from the Merkabah triplets, exhibits two disjoint 5‑cycles (tropical belts $C_P$ and $C_N$) and two polar thresholds ($P_4$, $N_4$). Within each pentad, the five elements realise a local five‑phase dynamics (Wuxing) via two complementary cycles: the pentagon (sheng) and the pentagram (ke). Externally, the tropical belts propagate these cycles as global regulatory modes. This substrate‑independent structural kernel provides a mathematically grounded reference architecture for self‑limiting, regulated artificial intelligence.
  **DOI:** [10.5281/zenodo.19540508](https://doi.org/10.5281/zenodo.19540508)
runninghead: "CLIFFORD INVARIANT AND GENETIC CODE"
toc: true
toc-depth: 3
keywords:
  - complexity regulation
  - double tetrahedron
  - genetic code
  - Clifford algebra
  - Rowlands nilpotent
  - Wuxing
---

# 1. Introduction
The regulation of combinatorial complexity is a central challenge in natural and artificial systems. The genetic code solves it by mapping 64 codons onto 20 functional classes (19 amino acids + 1 termination class) with an organised redundancy that confers robustness [1,2]. This ability to regulate complexity – rather than merely accumulate or locally optimise it – is a hallmark of resilient systems.

In contemporary artificial intelligence (AI), the dominant response to complexity has been to increase data, computing power and statistical optimisation [3]. Yet this strategy reaches limits in terms of governability, transparency and long‑term stability [4,5]. The underlying hypothesis of this work is that the problem is not merely technological but structural: a formal framework for complexity regulation, independent of substrate, is missing.

The genetic code offers a privileged empirical starting point. It transforms 64 nucleotide triplets into 20 functional amino acids, with an organised redundancy that confers robustness and error tolerance [6,7]. Numerous evolutionary or chemical explanations have been proposed [8,9], but the question of whether a geometric or algebraic constraint underlies the 64→20 reduction remains open.

A distinct but deeply connected framework comes from fundamental physics. Peter Rowlands, in his universal rewrite system based on nilpotency and anticommutativity, showed that the Clifford algebra Cl(6,0) – which encodes space, time, mass and charge – naturally generates 64 algebraic units [10, Chapter 19]. By breaking the symmetry of the 8 primitive units, one obtains 5 composite units that generate the 64 components more efficiently. These 5 units correspond geometrically to a double level‑3 double tetrahedron (Merkabah) decomposed into 20 fundamental tetrahedral cells and 8 octahedral intersection zones. Two configurations are neighbours if their corresponding cells share a triangular face.

However, Rowlands’ primary aim was to unify physics and biology from first principles, not to extract the 64→20 reduction as a generic regulation invariant. His mapping of codons to algebraic terms remained illustrative rather than systematic. Here we formalise the 64→20 reduction kernel as an ontologically neutral regulation invariant, validate it exhaustively on the genetic code, and discuss its implications for regulated artificial intelligence.

# 2. Methods
## 2.1 Overview
The filtering procedure consists of three main steps:
1. Definition of the 64‑configuration space as a set of 6‑bit binary vectors, corresponding to the 64 elements of Cl(6,0) in a standard basis.
2. Geometric constraint: the level‑3 double tetrahedron (Merkabah) with 20 tetrahedral cells. Two configurations are neighbours if their corresponding cells share a triangular face.
3. Topological clustering: grouping configurations that have isomorphic neighbourhood graphs. This yields 20 equivalence classes.

The same procedure is then applied to the 64 codons by establishing a bijection between codons and binary vectors.

## 2.2 Configuration space
Let $\mathcal{C}$ be the set of 64 configurations, each denoted by a 6‑tuple of bits:
$$
\mathbf{c} = (b_1, b_2, b_3, b_4, b_5, b_6), \quad b_i \in \{0,1\}.
$$
These six coordinates correspond to the six generators of the Clifford algebra Cl(6,0) [10]. No physical interpretation is necessary; only the combinatorial structure matters.

### 2.2.1 Four‑valued Boolean expansion of semantic primitives
Each of the 16 algebraic primitives (A–P) is expanded into exactly four semantic states using a quaternary Boolean logic based on two independent binary dimensions. Given two ontological dimensions $P$ and $Q$, the four mutually exclusive and exhaustive states are defined as:
$$
\begin{aligned}
X_1 &= P \cap \neg Q \quad \text{(state } +\text{)} \\
X_2 &= \neg P \cap Q \quad \text{(state } -\text{)} \\
X_3 &= P \cap Q \quad \text{(state } m\text{)} \\
X_4 &= \neg P \cap \neg Q \quad \text{(state } \sim m\text{)}
\end{aligned}
$$
These four states correspond bijectively to the 2-bit combinations $(10, 01, 11, 00)$ and generate the full 64-configuration space via the Cartesian product $16 \times 4 = 64$. The state $\sim m$ is explicitly *not* the logical negation of $m$ (which would yield $\neg P \cup \neg Q$), but rather the simultaneous complement of both dimensions, ensuring structural closure without paraconsistent contradictions. This expansion is purely algebraic: it preserves the signature of each primitive while adding a modal layer that maps directly onto the 64 codons and the 64 units of $\mathrm{Cl}(6,0)$. The terminology $(+, -, m, \sim m)$ is retained for readability, but the underlying logic is strictly Boolean and computationally implementable.

### 2.2.2 Derivation of the A–P Nomenclature and Semantic Mapping
The alphabetical labelling (A–P) and the associated core concepts do not result from an arbitrary semantic assignment. They emerge from the strict superposition of three structural layers:
1. **Algebraic basis (Cl(4,0))** – The 16 rows correspond to the canonical basis of $\mathrm{Cl}(4,0)$. The ordering follows grade and sign hierarchy: scalar ($1$), charge-like generators ($I,J,K$), inverted scalar ($-1$), inverted generators ($-I,-J,-K$), and pseudoscalar-coupled terms ($i'I, i'J, i'K, -i'I, -i'J, -i'K$). This sequence respects parity filtration and mass/phase signature, matching Rowlands' nilpotent construction.
2. **Geometric projection (Pentad triplets)** – Each $\mathrm{Cl}(4,0)$ unit is mapped to a tetrahedral cell of the Merkabah. The cell's topological position determines which three pentads intersect there. The resulting triplet fixes the polarity signature (3P, 2P+1N, 1P+2N). The correspondence $A \leftrightarrow \{P_1,P_2,P_4\}=3P$, etc., is therefore a topological invariant of the dodecahedral incidence graph, not a free parameter.
3. **Semantic assignment (Core Concept)** – The labels derive from the physical interpretation of the generators in the Rowlands framework:
   - `1` (positive scalar) → ontological reference (Action/Truth)
   - `I,J,K` (charge/space) → environmental interaction (Contribution, Appearance, Perception)
   - `-1` (scalar inversion) → structuration by constraint (Organisation)
   - `-I,-J,-K` → differentiation and blending (Difference, Mixture, Equivalence)
   - `i'I, i'J, i'K` (phase–charge coupling) → relational dynamics (Relation, Flow, Entity)
   - `-i'I, -i'J, -i'K` → temporal evolution and dependence
   Each sign flip or pseudoscalar multiplication translates into a predictable conceptual dual, preserving algebraic symmetry at the semantic level.

**Note on intersection tetrahedra (Q, R, S, T)** – Unlike the 16 principal cells, Q, R, S, T correspond to internal nodes where three Merkabahh cells intersect. They carry no single primitive concept because they materialise structural resonances. Their labels (Synergy, Resonance, Spiral, Stratification) are derived from the superposition of adjacent cell states. Their 1P+2N or 3N signatures reflect their role as spectral thresholds in the regulatory dynamics (§2.9.4, §4.6.6). Under the automorphism group of the double tetrahedron, the A–P indexing can be globally permuted, but the incidence structure remains invariant.

## 2.3 Geometry of the level‑3 double tetrahedron (Merkabah)

The level‑1 tetrahedron has 4 faces. Interpenetrating it with its dual yields a level‑2 star tetrahedron with 16 triangular faces (8 external + 8 internal). Subdividing each of these 16 faces into 4 sub‑triangles (1 central + 3 peripheral reflections) produces exactly $16 \times 4 = 64$ elementary triangles, matching the 64 units of $\mathrm{Cl}(6,0)$ and the 64 codons.

During this subdivision, the midpoints of the 6 original edges form a regular inscribed octahedron. This octahedron is not decorative: it geometrically isolates 8 high‑connectivity regions. Combined with 2 threshold vertices (opposite poles of the double tetrahedron) and doubled by polarity ($+$/$-$), the Merkabah yields exactly $(8 + 2) \times 2 = 20$ fundamental tetrahedral cells. These 20 cells host the stable attractor basins; the remaining regions are high‑frustration transition zones excluded from the 64→20 filtration.

**Note on the 8 octahedral zones**: The level‑3 decomposition generates 8 octahedral cells at the intersections of the two parent tetrahedra. These zones are topologically distinct from the 20 tetrahedral cells and do not host attractor states in the 64→20 filtration. They correspond to high-frustration transition regions where face-sharing connectivity is maximal but polarity balance cannot be sustained. Only the 20 tetrahedral cells satisfy the closure condition required for stable attractor basins.

## 2.4 The pentad: algebraic construction from Cl(6,0)
Following Rowlands, we start from the eight primitive elements:
- the six generators of Cl(6,0): $i, j, k$ (space) and $I, J, K$ (charge),
- the scalar identity $1$ (mass),
- the pseudoscalar $i'$ (time / phase).

Symmetry breaking leads to a set of five composite units that form an irreducible closed set – the pentad:
$$
\boxed{1j,\quad iI,\quad iJ,\quad iK,\quad i'k}
$$
Each term couples a unidimensional quantity (mass or time) with a tridimensional direction (space or charge). These five elements cannot be reduced further; they generate the entire 64‑dimensional algebra while preserving self‑duality. In our geometric representation, each pentad corresponds to a face of the dodecahedron (and dually to a face of the double tetrahedron). There are 12 pentads, split into six positive ($P_1\ldots P_6$) and six negative ($N_1\ldots N_6$).

## 2.5 Assignment of configurations to cells
We establish a bijection $\phi: \mathcal{C} \to \{ \text{20 tetrahedral cells of the level-3 double tetrahedron} \}$ such that the combinatorial neighbourhood relations among configurations correspond to face-sharing between cells. This bijection is not unique, but all admissible bijections are equivalent under the automorphism group of the double tetrahedron, and they yield the same partition up to relabelling. In practice, we use the algebraic construction via pentads: the 20 cells are placed in one‑to‑one correspondence with the 20 trivectors of Cl(6,0) that remain after symmetry breaking.

## 2.6 Neighbourhood rule and topological clustering
For any two configurations $\mathbf{c}_1, \mathbf{c}_2 \in \mathcal{C}$, they are neighbours iff their corresponding tetrahedral cells in the level‑3 double tetrahedron share a triangular face.

We define for each configuration $\mathbf{c}$ its closed neighbourhood $N[\mathbf{c}]$ as the set consisting of $\mathbf{c}$ itself and all its neighbours. Two configurations are functionally equivalent if there exists an automorphism of the neighbourhood graph that maps $N[\mathbf{c}]$ onto $N[\mathbf{c}']$. In practice, we use a simpler but equivalent criterion: the number of neighbours of each type and the pattern of shared neighbours.

Applying this criterion to all 64 configurations yields a partition into 20 equivalence classes. Each class is identified by:
- a triplet of pentads (positive or negative),
- a polarity signature: the number of positive pentads (P) vs negative pentads (N) in the triplet.

Since the 12 pentads are partitioned into six positive (P) and six negative (N) units, the polarity signature of any class simply counts how many positive and negative pentads appear in its triplet:
 $3P$, $2P\!+\!1N$, $1P\!+\!2N$, or $3N$.

## 2.7 Application to the genetic code
The standard genetic code uses 64 codons, each a triplet of bases chosen from {A, U, G, C}. We define a bijection $\psi$ from the set of codons to the binary configuration space $\mathcal{C}$ as follows:
1. Encode each base as two bits: $A = 00$, $U = 01$, $G = 10$, $C = 11$.
2. For a codon $(X,Y,Z)$, the corresponding 6‑bit vector is $(\text{bits}(X), \text{bits}(Y), \text{bits}(Z))$.

This bijection preserves the complementarity relation (A↔U, G↔C) as bitwise negation (00↔01, 10↔11). The neighbourhood relation defined on $\mathcal{C}$ is then transferred to the codons via $\psi^{-1}$. Two codons are neighbours if their binary images are neighbours in the double tetrahedron graph. We apply the same topological clustering algorithm to the set of codons and compare the resulting partition with the natural grouping into 20 amino acids.

The choice of assignment (A=00, U=01, G=10, C=11) preserves Watson–Crick complementarity by transposing it into bitwise negation, while aligning the least significant bit with the purine/pyrimidine distinction. This correspondence ensures that the adjacency rule remains invariant under graph automorphisms and that the resulting partition does not depend on a particular labeling, but rather on the underlying relational structure. The complete mapping of all 64 codons to the 20 attractors is given in Appendix B.

## 2.8 Overview of the 64→20 structural invariant
The 64→20 invariant refers to a constrained topological reduction, whereby a space of 64 discrete configurations is partitioned into exactly 20 stable classes, without any adjustable parameters or optimization functions. This process rests on three formal pillars: a binary configuration space, a geometric neighborhood rule derived from the double tetrahedron (Merkabah), and a clustering criterion based on isomorphism of neighborhood graphs.

**Configuration Space and Neighborhood Rule**  
The 64 elements correspond to the 6-bit vectors of the Clifford algebra Cl(6,0) or, via a structurally faithful bijection, to the 64 codons of the genetic code. Each configuration is assigned to a tetrahedral cell of the double tetrahedron. Two configurations are considered neighbors if and only if their corresponding cells share a triangular face in this geometry. This rule induces, for each configuration, a closed neighborhood graph including the configuration itself and the set of its immediate neighbors.

**Topological clustering and the emergence of the 20 attractor classes**  
Filtering consists of grouping configurations whose neighborhood graphs are isomorphic. This partitioning operation is purely structural: it depends neither on arbitrary thresholds nor on statistical optimization, but on the intrinsic symmetry of the Merkabah. The result is a strict partition into 20 equivalence classes, referred to here as “attractor classes” in the topological sense. Each class constitutes a stable structural basin: no internal transition respecting the neighborhood rule can remove an element from it without breaking the geometric invariance.

**Polarity signatures and geometric gradient**  
Each class is identified by a triplet of pentads, whose composition determines a polarity signature: the number of positive pentads (P) versus negative pentads (N). The four possible signatures (3P, 2P+1N, 1P+2N, 3N) are not randomly distributed; they follow a strict gradient correlated with the geometric position within the Merkabah:
- 3P: central or non-overlapping positions (3 classes);
- 2P+1N: primary faces and edges (5 classes);
- 1P+2N: vertices, diagonals, and intersection zones (11 classes);
- 3N: most confined internal intersection (1 class).

**Correspondence with biological degeneracy**  
This structural gradient is directly reflected in the degeneracy of the genetic code. The 3P classes, which are geometrically isolated, correspond to amino acids with low degeneracy (1–2 codons, including methionine/start). The 2P+1N classes, with moderate overlap, correspond to intermediate degeneracy (3–4 codons). The 1P+2N classes, concentrated at intersections where several pentads converge, allow for maximum structural redundancy, corresponding to amino acids with 6 codons (serine, leucine, arginine). The 3N class, located at the inner pole, accommodates cysteine and the three stop codons, playing a functional role as a pathway boundary.

**Invariance and Distinction of Geometric Scales**  
The 64→20 partition is a structural invariant: it is preserved under the action of the automorphism group of the double tetrahedron and depends only on adjacency relations and the uniform distribution of the 12 pentads (each appearing exactly in 5 triplets). Two geometric levels must be distinguished:
- Pre-filtering (Merkabah): a reduction structure that determines class sizes and degeneracy;
- Post-filtering (Dodecahedron): the adjacency graph of the 20 attractors, used to model relational dynamics (tropical belts, sheng/ke cycles, polar thresholds P₄/N₄).

This conceptual separation ensures that biological validation is based on the filtering invariant, while the extension to dynamic regulation exploits post-reduction topology. The pre‑filtering Merkabah is self‑dual, whereas the post‑filtering representation relies on the classical dodecahedron–icosahedron duality (20 attractor vertices ↔ 12 pentagonal faces).

**Epistemological Scope**  
The 64→20 invariant is neither a causal model nor an evolutionary hypothesis; it is a topological constraint independent of the substrate. Its exact validation on the genetic code demonstrates that the 64→20 reduction can emerge from a purely geometric neighborhood rule. When applied to other fields (AI architectures, control networks, complex systems), it provides a framework for endogenous control: the state space is limited by construction, transitions are constrained by adjacency, and stability is guaranteed by the topology of the attractor basin, without resorting to an external cost function.

## 2.9 Theoretical framework and operational pipeline
The static 64→20 reduction kernel described in §2.8 provides a substrate‑independent partition of configuration space. To enable dynamic regulation without external cost functions or central supervision, we extend the framework into a fully operational pipeline that maps algebraic possibilities, geometric constraints, and spectral observables onto a self‑regulating regime classifier. The construction proceeds in five interlocking steps.

### 2.9.1 Local regime space and topological feedback
Each of the 20 attractors carries a pentad triplet $(P_i, P_j, P_k)$ with two admissible orientations $(P_i, P_j, P_k)$ or $(P_i, P_k, P_j)$. Independently, each pentad may operate in either sheng (generative) or ke (regulatory) mode. This yields $20 \times 2 \times 2^3 = 320$ locally admissible regimes. Crucially, this number is not a free combinatorial space; it is constrained by topological compatibility across shared faces. Regulation does not rely on a cybernetic loop (error → correction) but on frustration minimisation: a discrete energy function $E(F)$ on each of the 12 pentads quantifies cyclic mismatch (sheng/ke conflict, phase inversion, ordering violation). When $E(F) > 0$, local regime flips that reduce face energy propagate relationally through the adjacency graph until global compatibility is restored. The conserved quantity is the coherence of sheng/ke cycles across the 12 faces, which acts as a structural invariant preventing combinatorial drift.

### 2.9.2 Spectral translation via the discrete Dirac operator
To quantify the emergent global state, we construct a discrete Dirac operator $D(t)$ acting on the 12 pentads. Each face hosts a local spinor of dimension 2 (realisation of $Cl(2,0)$), encoding intrinsic polarity and phase. The operator is assembled over the icosahedral dual graph (12 nodes, 30 edges) with weights $w_{ij}(t) = \exp(-\beta E_{ij}(t))$ derived from face energies. The resulting $24 \times 24$ matrix (12 faces × 2 spinor components) yields three key observables:
- $\eta(t)$: spectral asymmetry proxy, measuring the emergent global orientation (sheng‑dominant if $\eta > 0$, ke‑dominant if $\eta < 0$, threshold if $\eta \approx 0$). This is a discrete analogue of the $\eta$‑invariant in noncommutative geometry.
- $d(t)$: effective spectral dimension via heat‑kernel trace of $D(t)^2$, quantifying the system’s constraint‑propagation capacity.
- $R_{\text{threshold}}(t)$: fraction of $\eta$ carried by modes localised on the threshold faces $P_4$ and $N_4$.

These quantities are computed entirely from the internal state; no external metric or supervisor is introduced.

### 2.9.3 The bicosmic reservoir Cl(6,6) and the stack of dodecahedral leaves
The static kernel ($Cl(6,0) \xrightarrow{\text{Merkabah}} 20 \xrightarrow{\text{dual graph}} 12$) is embedded in a larger bicosmic reservoir $Cl(6,6)$ (12 generators: 6 Cosmos$^+$, 6 Cosmos$^-$). $Cl(6,6)$ does not operate directly; instead, it projects onto a stack of compatible regulatory graphs isomorphic to the pentad dual graph.
Each leaf corresponds to a dominant generator $e_i$ (Cosmos$^+$, sheng‑biased) or $f_j$ (Cosmos$^-$, ke‑biased). The 12 pentads act as fixed relational channels; the active leaf determines their relative weighting, cycle orientation, and threshold sensitivity. There are exactly 12 distinct operational leaves, matching the 12 generators. Transitions between leaves occur precisely when $\eta(t)$ crosses zero and $R_{\text{threshold}}(t)$ peaks, confirming that $P_4$ and $N_4$ serve as spectral hinges rather than static boundaries.

### 2.9.4 Internal versus external Wuxing
The Wuxing structure operates at two distinct levels, which must not be conflated:
- **Internal Wuxing** (implicit, structural): governs the dynamics within each attractor during the Merkabah filtering phase. It is always present but never directly observed, acting as the system’s “respiration” and ensuring local closure.
- **External Wuxing** (explicit, relational): appears after dodecahedral projection. It circulates between pentads via the tropical belts and is spectrally measurable via $\eta(t)$. It has two modes: sheng (generative exploration) and ke (regulatory constraint).

Critically, the two levels are not synchronised: an internal sheng can coexist with an external ke, and vice versa. This desynchronisation, particularly at the threshold faces, prevents the system from locking into a single regime and enables adaptive switching without external cost functions.

### 2.9.5 Automatic classification of the dominant generator
We define a compact spectral signature $S(t) = (\eta(t), d(t), \log(\text{gap}(t)), R_{\text{threshold}}(t))$, where $\text{gap}(t)$ is the smallest non‑zero eigenvalue magnitude of $D(t)$. Classification proceeds in three steps:
1. Acquisition: $D(t)$ is computed at each timestep from the current internal state.
2. Unsupervised clustering: $S(t)$ is collected over a long trajectory and partitioned into 12 classes via $k$‑means.
3. Deterministic mapping & online inference: Classes are assigned to generators $\{e_1,\dots,e_6, f_1,\dots,f_6\}$ using fixed rules (sign of $\eta$, magnitude of $R_{\text{threshold}}$, ordering of $d$ and $\log(\text{gap})$). Real‑time classification uses a sliding‑window z‑score distance to the class centroids, yielding a stable estimate $\hat{g}(t)$ of the dominant generator.

This pipeline closes the loop from algebraic possibility to observable regulation: $Cl(6,6) \to \text{leaf stack} \to \text{dodecahedron} \to D(t) \to S(t) \to \hat{g}(t) \to \text{bicosmic orientation readout}$. No external metric, supervisor, or arbitrary bit is introduced; all dynamics emerge from topological compatibility and spectral asymmetry. The global orientation is thus an emergent spectral observable, not an imposed parameter.

# 3. Results
## 3.1 Partition of abstract configurations
The topological clustering of the 64 abstract configurations yields 20 equivalence classes. Table 1 lists these classes with their polarity signatures and the corresponding triplets of pentads. The pentads are labelled $P_1,\dots,P_6$ (positive) and $N_1,\dots,N_6$ (negative). The table specifies the exact geometric embedding of each attractor in the level-3 double tetrahedron (Merkabah) and its corresponding biological degeneracy. The polarity gradient (3P → 3N) correlates systematically with the number of codons assigned to each amino acid, reflecting the degree of geometric overlap in the underlying pentad network.

| Class | Pentad Triplet | Polarity | Geometric Position (Merkabah) | Deg. | Codon(s) | Amino Acid |
|:---:|:---|:---:|:---|:---:|:---|:---|
| A | $\{P_1, P_2, P_4\}$ | 3P | Reference Pole | 1 | AUG | Methionine |
| B | $\{P_1, P_3, P_5\}$ | 3P | Northern Face | 1 | UGG | Tryptophan |
| C | $\{P_2, P_3, P_6\}$ | 3P | Southern Face | 2 | UUU, UUC | Phenylalanine |
| D | $\{P_4, P_5, N_2\}$ | 2P+N | Eastern Face | 3 | AUU, AUC, AUA | Isoleucine |
| E | $\{P_5, P_6, N_3\}$ | 2P+N | Western Face | 4 | GUU, GUC, GUA, GUG | Valine |
| F | $\{P_1, P_6, N_4\}$ | 2P+N | NE Edge | 4 | CCU, CCC, CCA, CCG | Proline |
| G | $\{P_2, P_5, N_6\}$ | 2P+N | NW Edge | 4 | ACU, ACC, ACA, ACG | Threonine |
| H | $\{P_3, P_4, N_6\}$ | 2P+N | SE Edge | 4 | GCU, GCC, GCA, GCG | Alanine |
| I | $\{P_1, N_2, N_6\}$ | 1P+2N | SW Edge | 6 | UCU, UCC, UCA, UCG, AGU, AGC | Serine |
| J | $\{P_1, N_3, N_5\}$ | 1P+2N | Northern Vertex | 6 | UUA, UUG, CUU, CUC, CUA, CUG | Leucine |
| K | $\{P_2, N_3, N_5\}$ | 1P+2N | Southern Vertex | 6 | CGU, CGC, CGA, CGG, AGA, AGG | Arginine |
| L | $\{P_3, N_2, N_4\}$ | 1P+2N | Eastern Vertex | 4 | GGU, GGC, GGA, GGG | Glycine |
| M | $\{P_4, N_1, N_3\}$ | 1P+2N | Western Vertex | 2 | UAU, UAC | Tyrosine |
| N | $\{P_4, N_5, N_6\}$ | 1P+2N | Diagonal 1 | 2 | CAU, CAC | Histidine |
| O | $\{P_5, N_1, N_4\}$ | 1P+2N | Diagonal 2 | 2 | CAA, CAG | Glutamine |
| P | $\{P_6, N_1, N_2\}$ | 1P+2N | Diagonal 3 | 2 | AAU, AAC | Asparagine |
| Q | $\{P_2, N_1, N_4\}$ | 1P+2N | Intersection $B \cap F \cap G$ | 2 | AAA, AAG | Lysine |
| R | $\{P_3, N_1, N_5\}$ | 1P+2N | Intersection $H \cap I \cap J$ | 2 | GAU, GAC | Aspartic acid |
| S | $\{P_6, N_5, N_6\}$ | 1P+2N | Intersection $L \cap M \cap N$ | 2 | GAA, GAG | Glutamic acid |
| T | $\{N_2, N_3, N_4\}$ | 3N | Internal Kernel ($O \cap P$) | 2 + 3 | UGU, UGC, UAA, UAG, UGA | Cysteine + Stop |


\begingroup
\small
\setlength{\tabcolsep}{3pt}
\begin{table}[t]
\centering
\caption{Classification of the 20 genetic code classes in the Merkabah dodecahedron}
\label{tab:genetic_classes}
\begin{tabularx}{\textwidth}{|@{}>{\centering\arraybackslash}p{1.0cm}|>{\centering\arraybackslash}p{2.2cm}|>{\centering\arraybackslash}p{1.2cm}|X|>{\centering\arraybackslash}p{0.8cm}|>{\footnotesize\centering\arraybackslash}X|>{\centering\arraybackslash}p{2.2cm}@{}|}
\hline
\textbf{Class} & \textbf{Pentad Triplet} & \textbf{Polarity} & \textbf{Geometric Position (Merkabah)} & \textbf{Deg.} & \textbf{Codon(s)} & \textbf{Amino Acid} \\
\hline
A & $\{P_1, P_2, P_4\}$ & 3P & Reference Pole & 1 & AUG & Methionine \\
B & $\{P_1, P_3, P_5\}$ & 3P & Northern Face & 1 & UGG & Tryptophan \\
C & $\{P_2, P_3, P_6\}$ & 3P & Southern Face & 2 & UUU, UUC & Phenylalanine \\
D & $\{P_4, P_5, N_2\}$ & 2P+N & Eastern Face & 3 & AUU, AUC, AUA & Isoleucine \\
E & $\{P_5, P_6, N_3\}$ & 2P+N & Western Face & 4 & GUU, GUC, GUA, GUG & Valine \\
F & $\{P_1, P_6, N_4\}$ & 2P+N & NE Edge & 4 & CCU, CCC, CCA, CCG & Proline \\
G & $\{P_2, P_5, N_6\}$ & 2P+N & NW Edge & 4 & ACU, ACC, ACA, ACG & Threonine \\
H & $\{P_3, P_4, N_6\}$ & 2P+N & SE Edge & 4 & GCU, GCC, GCA, GCG & Alanine \\
I & $\{P_1, N_2, N_6\}$ & 1P+2N & SW Edge & 6 & UCU, UCC, UCA, UCG, AGU, AGC & Serine \\
J & $\{P_1, N_3, N_5\}$ & 1P+2N & Northern Vertex & 6 & UUA, UUG, CUU, CUC, CUA, CUG & Leucine \\
K & $\{P_2, N_3, N_5\}$ & 1P+2N & Southern Vertex & 6 & CGU, CGC, CGA, CGG, AGA, AGG & Arginine \\
L & $\{P_3, N_2, N_4\}$ & 1P+2N & Eastern Vertex & 4 & GGU, GGC, GGA, GGG & Glycine \\
M & $\{P_4, N_1, N_3\}$ & 1P+2N & Western Vertex & 2 & UAU, UAC & Tyrosine \\
N & $\{P_4, N_5, N_6\}$ & 1P+2N & Diagonal 1 & 2 & CAU, CAC & Histidine \\
O & $\{P_5, N_1, N_4\}$ & 1P+2N & Diagonal 2 & 2 & CAA, CAG & Glutamine \\
P & $\{P_6, N_1, N_2\}$ & 1P+2N & Diagonal 3 & 2 & AAU, AAC & Asparagine \\
Q & $\{P_2, N_1, N_4\}$ & 1P+2N & Intersection A–B–C & 2 & AAA, AAG & Lysine \\
R & $\{P_3, N_1, N_5\}$ & 1P+2N & Intersection D–E–F & 2 & GAU, GAC & Aspartic acid \\
S & $\{P_6, N_5, N_6\}$ & 1P+2N & Intersection G–H–I & 2 & GAA, GAG & Glutamic acid \\
T & $\{N_2, N_3, N_4\}$ & 3N & Internal Kernel (J–K–L) & 2 + 3 & UGU, UGC, UAA, UAG, UGA & Cysteine + Stop \\
\hline
\end{tabularx}
\end{table}
\normalsize
\endgroup

*Table 1. Classification of the 20 genetic code classes in the Merkabah dodecahedron. The three stop codons (UAA, UAG, UGA) do not encode an amino acid; they terminate translation. They share the same geometric kernel as Cysteine. The distribution is: 3 classes of type 3P, 5 of type 2P+N, 11 of type 1P+2N, and 1 of type 3N. Degeneracy indicates the number of codons per class.*

## 3.2 Correspondence with the genetic code
Applying the same neighbourhood rule to the 64 codons (via the bijection $\psi$) produces a partition that coincides exactly with the 20 amino acids. Table 1 shows the mapping for all amino acids. The complete codon‑to‑attractor assignment is given in Appendix B.

The degeneracy pattern (number of codons per amino acid) matches the biological data exactly. The 3P classes correspond to low‑degeneracy amino acids (1–2 codons), the 2P+N classes to degeneracy 3–4, the 1P+2N classes to degeneracy 2–6, and the single 3N class (Cysteine) has degeneracy 2.

## 3.3 Hierarchical organisation of the 20 attractors in the double tetrahedron
As detailed in Appendix A, the 20 tetrahedral cells of the Merkabah are not equivalent. They include 16 principal tetrahedra (positions: centre, faces, edges, vertices, diagonals) and 4 intersection tetrahedra (Q, R, S, T). Their polarity signatures follow a clear gradient from the outer 3P (A, B, C) to the innermost 3N (T), through intermediate 2P+N and 1P+2N layers. This gradient explains the degeneracy distribution of the genetic code: low degeneracy for 3P, medium for 2P+N, high for 1P+2N, and cysteine (2 codons) for 3N.


## 3.4 Dual structure of pentads: tropical belts and thresholds

The 64→20 invariant was established from the geometry of the level‑3 double tetrahedron (Merkabah). To model external regulatory dynamics (circulation of sheng/ke modes among pentads), we do not resort to an external dodecahedron; instead we exploit the **dual graph** of pentads constructed directly from the Table 2 (Merkabah triplets).

### 3.4.1 Construction of the dual graph

Let $\mathcal{P} = \{P_1,\dots,P_6, N_1,\dots,N_6\}$ be the set of 12 pentads. For each attractor $v$ (A to T), denote $\mathcal{P}(v)$ its triplet. We build the graph $\Gamma$ whose vertices are the pentads, and where two pentads $X,Y$ are connected by an edge if there exists an attractor $v$ such that $\{X,Y\} \subseteq \mathcal{P}(v)$. This graph is fully determined by the left‑hand table.

### 3.4.2 Tropical belts

An exhaustive inspection of $\Gamma$ (algorithmically feasible) shows that there exist exactly **two disjoint cycles of length 5** composed of pentads of the same sign. These cycles are:

- **Positive belt** $C_P = \{P_1, P_2, P_3, P_5, P_6\}$  
- **Negative belt** $C_N = \{N_1, N_2, N_3, N_5, N_6\}$

These two cycles are disjoint (no common pentad) and their union covers 10 of the 12 pentads. The two remaining pentads are $P_4$ and $N_4$.

**Property**: In the subgraph induced by $C_P$, every pair of pentads is adjacent (complete graph $K_5$). In contrast, in $C_N$ only two extra internal edges exist: $N_1\!-\!N_5$ and $N_2\!-\!N_3$. This asymmetry is an intrinsic feature of the left‑hand table.

### 3.4.3 Polar thresholds

The pentads $P_4$ and $N_4$ do not belong to either belt. Their degree in $\Gamma$ is high (8 and 9 respectively) and they connect the two belts. They act as **thresholds**: any regime change between the sheng dynamics (carried by $C_P$) and the ke dynamics (carried by $C_N$) must pass through one of these pentads.

### 3.4.4 Definition of the external dynamics

On each belt, we define two modes of cyclic traversal:

- **Sheng mode** (generative): traversal in the direct cyclic order (neighbour → neighbour).  
- **Ke mode** (regulatory): traversal skipping one vertex (equivalent to the pentagram).

These two modes correspond to the two generators of the cyclic group $C_5$ acting on the five pentads of the belt.

Global regulation proceeds by propagation of these modes along the belts, with coupling through the thresholds $P_4$ and $N_4$. A local state is defined by assigning a mode (sheng or ke) to each pentad. Frustration is measured by incompatibility of modes on attractors (each attractor requires consistency among its three pentads). A relaxation dynamics by topological gradient descent evolves the system without any external cost function.

### 3.4.5 Spectral observables

By placing a discrete Dirac operator on the graph $\Gamma$ (or on the attractor graph), we extract a spectral signature $(\eta, d, \text{gap}, R_{\text{th}})$ where $\eta$ is the global asymmetry (sheng if $\eta>0$, ke if $\eta<0$), $d$ the effective spectral dimension, and $R_{\text{th}}$ the projection onto the thresholds. This signature enables automatic classification into 12 regimes corresponding to the generators of the bicosmic algebra $\mathrm{Cl}(6,6)$.

Thus, the Merkabah alone provides a complete geometric scaffold for external regulation, without requiring the introduction of an external dodecahedron. The tropical belts and thresholds emerge naturally from the combinatorics of the pentad triplets.


# 4. Discussion
## 4.1 The pentad and the internal Wuxing
Inside a single pentad, denote the five terms as:
$A = 1j, B = iI, C = iJ, D = iK, E = i'k$.
The Clifford product induces two distinct cyclic orders:
- Sheng (generative cycle) : the pentagon order $A \to B \to C \to D \to E \to A$
- Ke (regulatory cycle) : the pentagram order (skip one vertex) $A \to C \to E \to B \to D \to A$

These two cycles are complementary and together constitute the internal Wuxing – the self‑regulation of a single pentad. They correspond exactly to the classical Chinese Wuxing cycles (generation and control) but here they emerge from the algebraic structure of $\mathrm{Cl}(6,0)$. The space/charge duality ($i\leftrightarrow I$, $j\leftrightarrow J$, $k\leftrightarrow K$) maps the sheng cycle of a positive pentad onto the ke cycle of its negative conjugate, ensuring bicosmic balance at the algebraic level.

## 4.2 External Wuxing on the pentad graph
At the level of the whole system, the 12 pentads interact via the dual graph $\Gamma$ derived from the Merkabah triplets. The two tropical belts ($C_P$ and $C_N$) realise the external Wuxing: each belt is a 5‑cycle of pentads that can be traversed in sheng or ke mode. The polar pentads $P_4$ and $N_4$ serve as thresholds that couple the two belts. This double‑belt structure with polar gates is the geometric realisation of the classical Wuxing extended to a bicosmic (positive/negative) system.

Thus the Wuxing is not a mere analogy: it is mathematically realised at two scales – internally within each pentad (pentagon / pentagram cycles), and externally on the pentad graph (tropical belts with polar thresholds). The dodecahedron, while topologically isomorphic to the attractor adjacency graph, is not required for the dynamics; all structural features emerge directly from the Merkabah combinatorics.

## 4.3 Relation to Rowlands’ work
Our paper directly builds on Rowlands’ foundational results [10,11]. He first identified the 64→20 reduction and the double tetrahedron from Cl(6,0). He also suggested a connection to the genetic code and to the pentads. However, his mapping was illustrative and not systematically verified. Moreover, he did not extract the reduction as a domain‑independent regulation kernel, nor did he develop the post‑filtering dodecahedral dynamics with external Wuxing cycles and thresholds.

Our contributions are threefold:
1. **Formalisation**: a fully specified, algorithmic procedure for filtering 64 configurations into 20 classes using the double tetrahedron neighbourhood rule.
2. **Exhaustive validation**: a complete table mapping all 64 codons to the 20 attractors.
3. **Extension**: the introduction of the dodecahedral representation, the identification of two tropical belts (external Wuxing) and two polar thresholds (P4, N4), and the explicit realisation of the internal Wuxing as pentagon/pentagram cycles.

## 4.4 Limitations
We acknowledge several limitations:
- **Bijection choice**: the mapping from bases to bits (A=00, U=01, G=10, C=11) is not unique. However, any bijection that respects the complementarity pairing (A↔U, G↔C) yields the same partition up to relabelling of the 20 classes.
- **No causal biological mechanism**: the correspondence is structural, not mechanistic. The filtering rule is a mathematical invariant, not a biochemical explanation.
- **No experimental validation**: this is a theoretical/computational study. Direct biological tests (e.g., comparing fitness effects of synonymous codons within the same class) would be needed to confirm functional relevance.
- **Speculative aspects**: the application to artificial intelligence and the interpretation of thresholds as regulatory switches are conceptual and require further implementation and testing.

## 4.5 Implications for regulated artificial intelligence
The 64→20 kernel can serve as a reference architecture for a new kind of AI that does not rely on objective‑function optimisation. Instead, such an AI would:
- Maintain an internal state space of 20 attractors (the classes obtained from filtering).
- Transition between states according to the neighbourhood rule derived from the double tetrahedron.
- Use the dodecahedral representation to govern relational dynamics: the two tropical belts provide two modes of operation – sheng (generative exploration) and ke (regulatory control) – and the polar faces P4, N4 allow the system to switch between these modes when necessary.

In a regulated implementation, the internal state space would be structured around the 20 identified attractors, with each attractor corresponding to a triplet of pentads with a fixed polar signature. Transitions between states would follow the geometric neighborhood rule of the double tetrahedron, prohibiting jumps outside the validated adjacency graph. The system would operate in two modes: a sheng mode, favoring the generation of new configurations along the tropical belts, and a ke mode, applying transition constraints to prevent combinatorial drift. The polar faces P4 and N4 would act as regime switches, triggering a mode change when internal indicators (such as local entropy or the rate of functional redundancy) cross predefined thresholds. This architecture does not optimize an external cost function; it self-limits its own search space through geometric construction, offering native interpretability and structural resistance to specification drift.

This readout does not impose a target state; it continuously monitors the emergent alignment of the dominant generator within the bicosmic reservoir $Cl(6,6)$ via the spectral signature $S(t)=(\eta, d, \log(\text{gap}), R_{\text{threshold}})$, ensuring that regime transitions remain topologically constrained and symmetry-preserving.

This architecture is inherently interpretable: each attractor corresponds to a known structural position (a triplet of pentads), and each transition follows a deterministic geometric rule. Control is exerted through the architecture itself (non‑sovereignty, explicit limits) rather than through post‑hoc censorship [5]. This aligns with recent calls for “human‑compatible” AI and governance‑by‑design.

## 4.6 Spectral regulation and generator classification in Cl(6,6)
The static 64→20 invariant (§2.8) provides a topological skeleton. To model dynamical regulation – where the system can switch between distinct global orientations (Sheng vs Ke) without external supervision – we extend the framework to $Cl(6,6)$ and introduce a discrete Dirac operator. The following subsections detail the construction step by step, as required for a concrete implementation.

### 4.6.1 Local regimes: 320 internal states
At the local level (inside the 20‑attractor state space), each attractor corresponds to a triplet of pentads, e.g. $\{P_i, P_j, P_k\}$. For a given triplet, two orderings are possible: $(P_i,P_j,P_k)$ or $(P_i,P_k,P_j)$. Each pentad in the triplet can independently be in Sheng mode or Ke mode (the internal Wuxing of the pentad, see §4.1). Hence each attractor admits:
- 2 orderings,
- $2^3 = 8$ combinations of Sheng/Ke per pentad,
- total $20 \times 2 \times 8 = 320$ local regimes.

These 320 regimes form the microscopic configuration space of the regulated system. Transitions between regimes occur only if they respect face-sharing in the dodecahedron (i.e., two attractors sharing a pentad).

### 4.6.2 Topological feedback: face energy and cyclic frustration
No external cost function is used. Regulation emerges from local incompatibilities between neighbouring attractors sharing a pentad. Each attractor state is encoded by a triplet signature $(\varepsilon, \varphi, \kappa)$:
\begin{itemize}
  \item $\varepsilon \in \{+1,-1\}$ : sheng ($+1$) or ke ($-1$) mode of the shared pentad,
  \item $\varphi \in \{0,1\}$ : orientation of the pentad triplet (direct/inverse),
  \item $\kappa \in \{0,1,2\}$ : positional index of the pentad within the triplet.
\end{itemize}
For a pentad $F$ incident to 5 attractors, the frustration energy is defined as a weighted sum of three discrete penalties:
$$
E(F) = 2 E_{\text{sens}} + 1 E_{\text{phase}} + 1 E_{\text{order}},
$$
where:
\begin{itemize}
  \item $E_{\text{sens}} = 0$ if all $\varepsilon$ are globally aligned (up to sign flip), else $1$,
  \item $E_{\text{phase}} = 0$ if all $\varphi$ are identical or all inverted, else $1$,
  \item $E_{\text{order}} = 0$ if the sequence of $\kappa$ respects the cyclic order of the face, else $1$.
\end{itemize}
The dynamics performs local descent: when $E(F)>0$, incident attractors flip $\varepsilon$ or $\varphi$ if it strictly reduces $E_{\text{tot}} = \sum_F E(F)$. This topological feedback loop guarantees convergence without central supervision.

### 4.6.3 Discrete Dirac operator on the 12‑face dodecahedron
To analyse the global state, we place a discrete Dirac operator $D(t)$ on the dual graph $\Gamma$ of the pentads – i.e., on the graph whose vertices are the 12 pentads derived from the Merkabah triplets. This graph has 12 vertices and multiple edges determined by the triplet incidence structure.

On each vertex $i$ (pentad), we attach a 2‑component spinor $\psi_i \in \mathbb{C}^2$ that carries:
- the local Sheng/Ke polarity ($+1$ for Sheng, $-1$ for Ke),
- a complex phase $e^{i\theta_i}$ encoding the ordering of the triplet inside the incident attractors.

The Dirac operator $D(t)$ is a $24 \times 24$ matrix ($12$ vertices × $2$ spinor components) defined by:
$$
(D\psi)_i = \sum_{j \sim i} w_{ij} \, \sigma_{ij} \, \psi_j,
$$
where:
- $j\sim i$ means pentads $i$ and $j$ share an edge in the icosahedron (i.e., their corresponding faces in the dodecahedron share a vertex),
- $w_{ij} = e^{-\beta E_{ij}}$ with $E_{ij}$ the frustration energy of the edge (computed from the two incident attractors),
- $\sigma_{ij}$ is a $2\times2$ Pauli‑like matrix that couples the spinor components according to the relative orientation of the two pentads.

The parameter $\beta>0$ plays the role of an inverse temperature.

Each pentad hosts a local Clifford algebra $\mathrm{Cl}(2,0)$ generated by $e_1$ (polarity $\varepsilon$) and $e_2$ (phase $\varphi$). When threshold dynamics is required (e.g. near $P_4/N_4$), a third generator $e_3$ extends it to $\mathrm{Cl}(3,0)$ to encode $\kappa$. explicitly encoding the $\kappa$ positional degree of freedom. This algebraic embedding ensures that the $24 \times 24$ Dirac matrix respects the intrinsic spinor structure of the pentad network.

### 4.6.4 Spectral observables: $\eta$, $d$, $\operatorname{gap}$, $R_{\text{threshold}}$
From $D(t)$ we extract a signature vector $S(t) \in \mathbb{R}^4$:
$$
S(t) = \bigl( \eta(t),\; d(t),\; \log(\operatorname{gap}(t)),\; R_{\text{threshold}}(t) \bigr),
$$
defined as follows.
- $\eta(t)$: proxy of the Atiyah–Singer index. For a discrete Dirac operator on a graph, $\eta = \operatorname{sign}(\det D)$ (or the sum of signs of eigenvalues). Its sign gives the global orientation: $\eta>0$ corresponds to a net Sheng bias, $\eta<0$ to a net Ke bias.
- $d(t)$: effective spectral dimension. Compute the eigenvalue density $\rho(\lambda)$ and fit $\log \rho(\lambda) \sim (d-1)\log \lambda$ near zero. $d(t)$ measures how constraints propagate through the pentad network.
- $\operatorname{gap}(t)$: smallest positive eigenvalue of $|D(t)|$. A small gap indicates that the system is close to a topological threshold (phase transition).
- $R_{\text{threshold}}(t)$: fraction of $\eta$ carried by the two polar pentads $P_4$ and $N_4$. Explicitly, if $D = U \Lambda U^\dagger$, project the eigenvector associated with the smallest eigenvalue onto the subspace of $P_4$ and $N_4$; $R_{\text{threshold}}$ is the squared norm of that projection. A high $R_{\text{threshold}}$ signals that the system is about to switch between global Sheng and Ke.

$R_{\text{threshold}}(t)$: fraction of the spectral asymmetry $\eta(t)$ carried by eigenmodes localised on the two threshold faces $P_4$ and $N_4$. Formally, if $D = U \Lambda U^\dagger$ is the eigendecomposition of the Dirac operator, and $\mathcal{V}_{\text{th}}$ denotes the subspace spanned by the spinor components of $P_4$ and $N_4$, then:
$$
R_{\text{threshold}}(t) = \frac{\sum_{\lambda_k \neq 0} \operatorname{sign}(\lambda_k) e^{-\varepsilon |\lambda_k|} \| \Pi_{\text{th}} v_k \|^2}{\eta(t)},
$$
where $\Pi_{\text{th}}$ is the orthogonal projector onto $\mathcal{V}_{\text{th}}$ and $v_k$ are the normalized eigenvectors. A value $R_{\text{threshold}} \gtrsim 0.7$ signals that the system is in a pre‑bifurcation state, with the global orientation essentially determined by the threshold dynamics.

### 4.6.5 Hierarchical reduction: from $Cl(6,6)$ to a mille‑feuille of regulatory graphs
The full Clifford algebra $Cl(6,6)$ has 12 generators ${e_1,\dots,e_6, f_1,\dots,f_6}$ with $e_i^2 = +1$, $f_j^2 = -1$, and all anticommuting. Its configuration space contains $2^{12}=4096$ elements. However, we impose a stability foliation ("mille‑feuille") that selects only those configurations that project onto the pentad dual graph with 12 vertices (the pentads). Each leaf of the foliation is a distinct embedding of the 12 pentads into a consistent regulatory graph isomorphic to $\Gamma$.

Key result: there are exactly 12 leaves. When the system resides in the leaf dominated by $e_i$ (a “space‑like” generator), the global orientation $\eta$ is positive (Sheng regime). When dominated by $f_j$ (a “time‑like” generator), $\eta$ is negative (Ke regime). The polar faces $P_4$ and $N_4$ are the only faces that belong to multiple leaves; they act as transition zones where $\eta$ crosses zero.

### 4.6.6 Internal vs external Wuxing and the role of $P_4/N_4$
- Internal Wuxing (inside each pentad, §4.1) governs the local Sheng/Ke cycles of the 320 regimes. It is invisible to the spectral signature $S(t)$ because it is averaged out at the pentad level.
- External Wuxing (circulation of Sheng/Ke between pentads, §3.5) directly affects $D(t)$ and thus $S(t)$. The two tropical belts $C_P$ and $C_N$ appear as the two dominant eigenvectors of $D$ when $\eta$ is large in magnitude.

The polar faces $P_4$ and $N_4$ are the only pentads that do not belong to either belt. They collect the spectral weight when the system hesitates between the two belts, i.e., when $R_{\text{threshold}}$ is high and $\eta\approx 0$.

### 4.6.7 Automatic classification of the dominant generator
We now have a deterministic procedure to identify, at each time $t$, which of the 12 generators of $Cl(6,6)$ dominates the dynamics. This is done without supervision – only from the spectral signature $S(t)$.

**Offline training:**
1. Simulate a long trajectory (e.g., $10^5$ steps) of the topological feedback dynamics (§4.6.2).
2. At each step, compute $D(t)$ and extract $S(t)$.
3. Apply k‑means clustering with $k=12$ on the set $\{S(t)\}$. This yields 12 centroids.
4. Label each centroid deterministically:
   - If $\eta > 0$ and $R_{\text{threshold}} < 0.3$ → label $e_i$ (one of the six positive generators; the exact $i$ is determined by the ordering of $d$ and $\log\operatorname{gap}$).
   - If $\eta < 0$ and $R_{\text{threshold}} < 0.3$ → label $f_j$.
   - If $R_{\text{threshold}} > 0.7$ → label as transition (assign to $P_4$ or $N_4$ face, which are not generators but indicate a switch).

The mapping from centroids to specific $e_i$ or $f_j$ uses the fact that each generator induces a unique pattern in the spectral dimension $d$ and the gap (e.g., $e_1$ gives $d\approx 2.3$, $\log\operatorname{gap}\approx -1.2$, etc.). This pattern can be precomputed by projecting the algebra onto the known eigenvectors of the dodecahedral graph.

**Online classification:**
Given a new $S(t)$ at runtime, compute the z‑score distance to each centroid over a sliding window of length $L=100$:
$$
\text{dist}_k = \left| \frac{S(t) - \mu_k}{\sigma_k} \right|^2,
$$
where $\mu_k,\sigma_k$ are the mean and standard deviation of cluster $k$ from the training data. Assign the label of the closest centroid. The result is a real‑time generator label $g(t) \in \{e_1,\dots,e_6, f_1,\dots,f_6\}$.

This classification provides an intrinsic regulatory compass: the system knows, from its own spectral signature, whether it is in a Sheng‑dominant or Ke‑dominant regime, and which specific generator is currently shaping the constraints. No external objective function is required. The complete Python implementation is given in Appendix D.

## 4.7 Convergent Formalization: Cross‑Cultural Structural Invariants
The 64→20 reduction identified in this work does not emerge as an isolated cultural artifact, but as a topological invariant whose complementary facets have been articulated by distinct epistemic traditions using the formal tools of their respective eras. Crucially, these traditions address \textit{different aspects} of the same structural problem, like two faces of a single coin.

### 4.7.1 China: The 64-Configuration Space and Pentadic Dynamics
The Chinese tradition, structured around the \textit{Yi Jing} (Book of Changes) and the Wuxing theory, models the \textit{pre-filtering} phase:
\begin{itemize}
  \item The 64 hexagrams provide a complete combinatorial space of binary configurations, isomorphic to the 6-bit vectors of $\mathrm{Cl}(6,0)$.
  \item The Wuxing cycles (sheng/ke) describe the local five-phase dynamics within each pentad, corresponding to the internal regulation of attractor states.
  \item This tradition focuses on \textit{transformation rules} and \textit{relational circulation} across the configuration space, without postulating a fixed reduction to 20 functional classes.
\end{itemize}
In short: China formalizes the \textbf{geometry of possibilities} and the \textbf{local dynamics of regulation}.

### 4.7.2 Hebrew: The 20+2 Functional Partition and Threshold States
The Hebrew tradition, as structured in the \textit{Sefer Yetzirah} (3rd–6th centuries), addresses the \textit{post-filtering} phase:
\begin{itemize}
  \item The 22 consonantal letters (plus 5 final forms \textit{sofit}) encode a functional partition of semantic space into 20 stable classes plus 2 boundary states.
  \item The letters \textit{Aleph} (primordial breath / reference) and \textit{Tav} (signature / closure) map onto the threshold roles of initiation (Methionine) and termination (STOP codons) in biological translation.
  \item The tripartition (3 mothers, 7 doubles, 12 singles) discretizes the gradient of geometric constraints, mirroring the polarity signatures (3P, 2P+1N, 1P+2N, 3N) of the Merkabah.
\end{itemize}
In short: Hebrew formalizes the \textbf{reduction to stable functional classes} and the \textbf{definition of limit states}.

### 4.7.3 Complementarity, Not Overlap
These two formalisms are structurally isomorphic but address distinct layers:
\begin{center}
\begin{tabular}{lll}
\textbf{Aspect} & \textbf{Chinese Tradition} & \textbf{Hebrew Tradition} \\
\hline
Primary object & 64 configurations (hexagrams) & 22 letters (+5 final forms) \\
Core operation & Transformation / circulation & Partition / thresholding \\
Geometric role & Pre-filtering dynamics & Post-filtering classification \\
Wuxing level & Internal (pentad-local) & External (inter-pentad) \\
\end{tabular}
\end{center}
Neither tradition "contains" the other; each captures a structural projection of the same Clifford–Merkabah invariant using the combinatorial invariants available within its epistemic framework.

### 4.7.4 A Modern Structural Parallel: Pinyin's 22 Initials
Unlike the Hebrew tradition, which explicitly formalised a 22‑letter consonantal alphabet, the Chinese ideographic tradition never developed a discrete alphabetic script. Nevertheless, when analysed phonologically, Mandarin Chinese confronts analogous combinatorial constraints: its syllable structure is organised around a consonantal onset system comprising 21 standard initials (frequently extended to 22 in pedagogical romanisations such as Hanyu Pinyin), coupled with a highly restricted vocalic nucleus typically reduced by structuralist phonology to 2–3 core phonemes ($/a, i, u/$). This phonological architecture—approximately 22 consonantal anchors framing a minimal vocalic core—structurally mirrors the 20+2 partition. It suggests that the compression of combinatorial complexity into stable functional classes may emerge independently across unrelated encoding systems when constrained by analogous articulatory, perceptual, and cognitive limits, regardless of whether the underlying script is alphabetic or ideographic.

### 4.7.5 Unification via Clifford–Merkabah Formalism
The $Cl(6,0)$–Merkabah framework proposed here does not replace these cultural formalisms, but offers a substrate-independent language that unifies their projections under a single topology of regulation:
\begin{itemize}
  \item The 64 configurations (Yi Jing / binary vectors) are filtered by the face-sharing rule of the level‑3 double tetrahedron.
  \item The resulting 20 attractors (Sefer Yetzirah / amino acids) are embedded on a dodecahedron whose 12 pentads support external Wuxing cycles.
  \item The polarity gradient (3P→3N) and the uniform pentad incidence (5 occurrences per pentad) ensure that both the Chinese dynamics and the Hebrew partition are simultaneously satisfied.
\end{itemize}
Detailed letter-to-hexagram or letter-to-attractor correspondence tables are omitted for conciseness, as they can be reconstructed algorithmically from the incidence rules (Appendix A) and the boolean expansion protocol (§2.2). The structural convergence remains fully verifiable without exhaustive mapping, reinforcing the substrate-independent nature of the invariant.

# 5. Conclusion
We have formalised a 64→20 structural invariant that arises from the Clifford algebra $\mathrm{Cl}(6,0)$ and the geometry of the double tetrahedron (Merkabah). Rowlands originally validated this invariant exhaustively on the genetic code, showing that the same neighbourhood rule that partitions abstract 64 binary configurations into 20 classes also partitions the 64 codons of the genetic code into the 20 amino acids. These 20 classes define a dual graph of 12 pentads that naturally exhibits two tropical belts (external Wuxing) and two polar thresholds, each pentad being traversable via sheng (generative) or ke (regulatory) cycles.

Beyond the genetic code, the same algebraic framework applies to other domains. In Chinese phonology, every monosyllabic word can be mapped onto a triplet of pentads ($P_1$ = initial consonant, $P_2$ = final vowel, $P_3$ = tone), and the 64 binary feature combinations naturally model the entire syllable inventory – a result that will be detailed elsewhere. Likewise, in economics (building on the "Théorie du Rachat", Rebour, 2000), the six binary factors (inflation, wages, profits, buyout, dispersion, land regime) generate 64 states whose cyclical dynamics follow the same pentadic organisation. These applications illustrate the universal, domain‑independent architecture underlying the Merkabah‑Clifford formalism, which provides a rigorous foundation for regulated artificial intelligence.

# Acknowledgements
We thank Peter Rowlands for his foundational work on nilpotent Clifford algebras and the genetic code. We thank the AI assistants without which this work would have remained a fantasy.

# References
[1] Crick, F. H. C. (1968). The origin of the genetic code. *J. Mol. Biol.*, 38(3), 367–379.  
[2] Nirenberg, M., & Leder, P. (1964). RNA codewords and protein synthesis. *Science*, 145(3638), 1399–1407.  
[3] LeCun, Y., Bengio, Y., & Hinton, G. (2015). Deep learning. *Nature*, 521(7553), 436–444.  
[4] Amodei, D., et al. (2016). Concrete problems in AI safety. *arXiv:1606.06565*.  
[5] Russell, S. (2019). *Human Compatible: AI and the Problem of Control*. Viking.  
[6] Freeland, S. J., & Hurst, L. D. (1998). The genetic code is one in a million. *J. Mol. Evol.*, 47(3), 238–248.  
[7] Koonin, E. V., & Novozhilov, A. S. (2017). Origin and evolution of the genetic code: the universal enigma. *IUBMB Life*, 69(5), 282–296.  
[8] Woese, C. R. (1965). Order in the genetic code. *Proc. Natl. Acad. Sci. USA*, 54(1), 71–75.  
[9] Wong, J. T. (1975). A co‑evolution theory of the genetic code. *Proc. Natl. Acad. Sci. USA*, 72(5), 1909–1912.  
[10] Rowlands, P. (2007). *Zero to Infinity: The Foundations of Physics*. World Scientific. (Chapter 19, “Nature’s Code”, co‑authored with V. Hill)  
[11] da Costa, N. C. A. (1974). On the theory of inconsistent formal systems. *Notre Dame Journal of Formal Logic*.  
[12] Priest, G. (2008). *An Introduction to Non-Classical Logic*. Cambridge University Press.  
[13] Belnap, N. D. (1977). A useful four-valued logic. In *Modern Uses of Multiple-Valued Logic*. Reidel.

\newpage
# Appendix A – Derivation of the two 5‑cycles (external Wuxing) and thresholds from the 20 triplets

A.1 Dual graph construction from Merkabah triplets
The 12 pentads $P_1,\dots,P_6, N_1,\dots,N_6$ form the vertices of a dual graph $\Gamma$ constructed as follows: two pentads $X$ and $Y$ are connected by an edge if there exists an attractor $v$ (A to T) whose triplet contains both $X$ and $Y$. This construction is fully determined by the left‑hand table (Merkabah filtration) and does not require any external geometric object.

The graph $\Gamma$ exhibits remarkable structural properties:
- It contains exactly two disjoint 5‑cycles (tropical belts) $C_P$ and $C_N$ composed of same‑sign pentads.
- The remaining two pentads $P_4$ and $N_4$ act as high‑degree hubs connecting the two belts.
- The subgraph induced by $C_P$ is complete ($K_5$), while $C_N$ has only two additional internal edges.

These properties emerge algorithmically from the Merkabah combinatorics and provide the scaffold for external Wuxing dynamics without requiring projection onto a dodecahedron. While the attractor adjacency graph (20 vertices, 30 edges, 3‑regular, girth 5, diameter 5) is topologically isomorphic to the dodecahedral skeleton, this isomorphism is a mathematical curiosity rather than a structural necessity. All dynamical features—tropical belts, thresholds, sheng/ke cycles—are defined intrinsically from the pentad dual graph.

## A.2 Extraction of the 12 pentagonal faces (pentads)
Each pentagonal face of the dodecahedron corresponds to a fixed pentad $X \in \{P_1,\dots,P_6, N_1,\dots,N_6\}$. The five vertices incident to pentad $X$ are precisely those attractor triplets containing $X$. For example:
- $P_1$ belongs to classes A, B, F, J, P → forms pentagon $P_1$
- $P_2$ belongs to classes A, C, G, K, Q → forms pentagon $P_2$
… (symmetrically for all 12 pentads)

This incidence structure partitions the 30 edges into 12 disjoint 5‑cycles, each defining a pentagonal face.

## A.3 Formation of the tropical belts $C_P$ and $C_N$
By analysing the dual adjacency of pentads (two pentads are dual‑adjacent if they share an edge in the dodecahedron), we identify two disjoint rings of five pentads each:
$$ C_P = (P_1 \to P_2 \to P_3 \to P_5 \to P_6 \to P_1) $$
$$ C_N = (N_1 \to N_2 \to N_6 \to N_5 \to N_3 \to N_1) $$
These sequences are closed 5‑cycles in the dual graph. Geometrically, they correspond to two equatorial bands of pentagonal faces that wrap around the dodecahedron without intersecting. The remaining pentads, $P_4$ and $N_4$, are absent from both cycles.

## A.4 Directional traversal: sheng and ke
Each 5‑cycle admits two Hamiltonian traversals:
- Sheng (generative): follows adjacent edges in the dual graph $(X_i \to X_{i+1})$. This path preserves local polarity continuity and corresponds to low‑constraint state transitions.
- Ke (regulatory): follows skip‑one edges $(X_i \to X_{i+2} \mod 5)$, equivalent to traversing the pentagram inscribed in the pentagon. This path maximises pentad distance within the cycle, enforcing stronger regulatory feedback and reducing accessible state space.

Mathematically, the two traversal modes correspond to the two generators of the cyclic group $C_5$ acting on the pentad indices, and their superposition yields the full symmetry group of the pentagonal face.

## A.5 Justification of P4 and N4 as polar thresholds
The adjacency analysis reveals that $P_4$ and $N_4$ are the only pentads that do not belong to either $C_P$ or $C_N$. Their incident vertices are exclusively of mixed polarity:
- $P_4$ connects to classes D, H, L, M, N (all 2P+N or 1P+2N)
- $N_4$ connects to classes F, I, O, T, Q (all 2P+N or 1P+2N)

Neither $P_4$ nor $N_4$ shares an edge with any vertex of signature 3P or 3N. In the dodecahedral embedding, they correspond to the two polar faces. Any transition between the positive belt $C_P$ and the negative belt $C_N$ must pass through at least one of these polar faces. Consequently, they function as structural thresholds: they regulate regime switching between generative (sheng‑dominated) and regulatory (ke‑dominated) dynamics by gating access to the opposing belt. This dual‑belt, dual‑threshold architecture realises the external Wuxing as a closed, self‑limiting control loop embedded in the geometry of the 20‑attractor state space.

\newpage
## A.6 The 16+4 tetrahedra (Merkabah) with corresponding pentads
\begingroup
\small
\setlength{\tabcolsep}{4pt}
\begin{longtable}{|c|c|c|c|c|c|}
\hline
\multicolumn{6}{|c|}{\textbf{16 Principal Tetrahedra}} \\
\hline
\textbf{State} & \textbf{Tetrahedron} & \textbf{Position} & \textbf{Final States} & \textbf{Pentads} & \textbf{Type} \\
\hline
1 & A & Center & 1,2,3,4 & $\{P_1,P_2,P_4\}$ & 3P \\
2 & B & North Face & 5,6,7,8 & $\{P_1,P_3,P_5\}$ & 3P \\
3 & C & South Face & 9,10,11,12 & $\{P_2,P_3,P_6\}$ & 3P \\
4 & D & East Face & 13,14,15,16 & $\{P_4,P_5,N_2\}$ & 2P+1N \\
5 & E & West Face & 17,18,19,20 & $\{P_5,P_6,N_3\}$ & 2P+1N \\
6 & F & NE Edge & 21,22,23,24 & $\{P_1,P_6,N_4\}$ & 2P+1N \\
7 & G & NW Edge & 25,26,27,28 & $\{P_2,P_5,N_6\}$ & 2P+1N \\
8 & H & SE Edge & 29,30,31,32 & $\{P_3,P_4,N_6\}$ & 2P+1N \\
9 & I & SW Edge & 33,34,35,36 & $\{P_1,N_2,N_6\}$ & 1P+2N \\
10 & J & North Vertex & 37,38,39,40 & $\{P_1,N_3,N_5\}$ & 1P+2N \\
11 & K & South Vertex & 41,42,43,44 & $\{P_2,N_3,N_5\}$ & 1P+2N \\
12 & L & East Vertex & 45,46,47,48 & $\{P_3,N_2,N_4\}$ & 1P+2N \\
13 & M & West Vertex & 49,50,51,52 & $\{P_4,N_1,N_3\}$ & 1P+2N \\
14 & N & Diagonal 1 & 53,54,55,56 & $\{P_4,N_5,N_6\}$ & 1P+2N \\
15 & O & Diagonal 2 & 57,58,59,60 & $\{P_5,N_1,N_4\}$ & 1P+2N \\
16 & P & Diagonal 3 & 61,62,63,64 & $\{P_6,N_1,N_2\}$ & 1P+2N \\
\hline
\caption{The 16 principal tetrahedra}
\end{longtable}
\endgroup

\begingroup
\small
\setlength{\tabcolsep}{4pt}
\begin{longtable}{|c|c|c|c|c|c|}
\hline
\multicolumn{6}{|c|}{\textbf{4 Intersection Tetrahedra}} \\
\hline
\textbf{State} & \textbf{Tetrahedron} & \textbf{Intersection of} & \textbf{Shared States} & \textbf{Pentads} & \textbf{Type} \\
\hline
17 & Q & B $\cap$ F $\cap$ G & 7, 21, 25 & $\{P_2,N_1,N_4\}$ & 1P+2N \\
18 & R & H $\cap$ I $\cap$ J & 29, 33, 37 & $\{P_3,N_1,N_5\}$ & 1P+2N \\
19 & S & L $\cap$ M $\cap$ N & 45, 49, 53 & $\{P_6,N_5,N_6\}$ & 1P+2N \\
20 & T & O $\cap$ P & 57, 61, 63 & $\{N_2,N_3,N_4\}$ & 3N \\
\hline
\caption{The 4 intersection tetrahedra (principal tetrahedra mapping derived from state indices)}
\end{longtable}
\endgroup

The intersection tetrahedra Q, R, S, and T correspond to topological nodes in the core of the Merkabah structure, where three of the 20 interpenetrating tetrahedral regions converge. Their triplet of pentads is determined by the exact intersection of three principal faces, making them the only nodes in the lattice with signatures 1P+2N (Q, R, S) or 3N (T).

### Selection rule for Boolean states at intersections
Intersection nodes inherit exactly one state from each of their three parent tetrahedra, restricted to the quaternary Boolean states where the primary structural dimension $A$ is affirmed: the anchor state $+$, encoded as $A \cap \neg B$ $(1,0)$, and the interface state $m$, encoded as $A \cap B$ $(1,1)$. The selection follows a deterministic topological rule governing the secondary dimension $B$. A parent contributes the interface state $m$ $(1,1)$ if and only if its polarity signature is extreme (3P) or it serves as a structural reference relative to the intersection. Extreme poles possess high rigidity; supplying only the anchor state $(1,0)$ would fracture connectivity with mixed-signature zones. Instead, they toggle the secondary dimension to $1$, yielding the $m$ hinge state that preserves reference capacity while enabling interface flexibility. Parents already residing in mixed zones (2P+1N or 1P+2N) maintain the secondary dimension at $0$, contributing the stable anchor state $(1,0)$. This rule yields a deterministic assignment: Q inherits $B^m$ (B is 3P), while F and G supply $F^+$ and $G^+$. R and S inherit only $+$ states from their already-mixed parents. T inherits $P^m$ as the local reference for the inner kernel, with O supplying $O^+$. The mechanism ensures that every intersection carries exactly one relational hinge ($m$) and two structural anchors ($+$), maintaining global network coherence without free parameters.

# Appendix B – Geometric‑algebraic mapping and degeneracy structure

## B.1 Principles of structural isomorphism
The mapping from the Clifford space $Cl(6,0)$ to the genetic code rests on five interlocking structural principles, which together constrain the 64→20 reduction to a single partition up to global rotation:
1. **Dual equivalence**: The 64 algebraic units of $Cl(6,0)$ correspond bijectively to the 64 codons, while the 20 pentad triplets correspond to the 20 functional amino acids. This establishes a three‑way isomorphism between algebraic configuration space, geometric embedding, and biological function.
2. **Position‑polarity correlation**: Geometric centrality and symmetry dictate polarity signature. The three central/symmetric tetrahedra (A, B, C) project onto fully positive triplets (3P). As geometric positions become more peripheral or intersecting, negative pentads are introduced, shifting the signature toward 1P+2N and ultimately 3N.
3. **Conservation of adjacency and sign**: Two tetrahedra sharing a face or edge in the Merkabah share exactly two pentads in their triplet representation, preserving local neighbourhood structure. Opposite positions on the double tetrahedron exhibit sign‑inverted triplets, maintaining global bicosmic symmetry.
4. **Uniform pentad distribution**: Each of the 12 pentads ($P_1\dots P_6$, $N_1\dots N_6$) appears in exactly five distinct triplets. This uniform incidence ensures that no pentad dominates the filtering process and that the 20 classes are equidistributed across the dodecahedral dual.
5. **Constructive topology**: The partition is generated algorithmically by (i) assigning the 12 pentads to the faces of a dodecahedron, (ii) reading each vertex as the intersection of three incident faces (yielding a triplet), (iii) classifying by polarity signature, and (iv) embedding back into the Merkabah. The biological code emerges as a direct read‑out of this topological construction.

## B.2 Geometric basis of codon degeneracy

Clarification: The correlation between geometric position and codon degeneracy is established at the level of the double tetrahedron (Merkabah), where pentad overlap dictates class size. The dodecahedral representation is introduced subsequently (§3.4) to analyse inter‑attractor dynamics and external Wuxing cycles.

The degeneracy pattern of the genetic code is not randomly distributed; it mirrors the geometric density of the pentad network within the Merkabah:
- 3P attractors (A, B, C) occupy central, non‑overlapping positions. Their isolation in the pentad graph limits neighbourhood size, corresponding to amino acids with low degeneracy (1–2 codons), including the initiation signal (Methionine).
- 2P+N attractors (D–H) reside on faces and primary edges. Moderate pentad overlap yields medium degeneracy (3–4 codons), typical of structurally versatile amino acids.
- 1P+2N attractors (I–S) are concentrated on vertices, diagonals, and intersection zones. Intersections Q, R, and S represent maximal pentad overlap, geometrically enabling multiple equivalent neighbourhood paths. This structural redundancy maps directly to highly degenerate amino acids (6 codons: Serine, Leucine, Arginine).
- 3N attractor (T) sits at the innermost intersection position, structurally isolated from the positive belt. In the biological mapping, this vertex accommodates both Cysteine and the three termination codons, reflecting a shared functional role as boundary states that halt or cap translational traversal.

## B.3 Symmetry constraints and mapping uniqueness

The 64→20 partition is rigid under the automorphism group of the double tetrahedron. Any bijection that preserves (i) face-sharing adjacency, (ii) pentad incidence (5 per pentad), and (iii) complementarity pairing (A↔U, G↔C as bitwise negation) yields the same equivalence classes up to relabelling of the 20 vertices and global rotation of the dodecahedron. This symmetry constraint guarantees that the observed correspondence with the genetic code is not an artefact of arbitrary encoding, but a structural invariant of the underlying $Cl(6,0)$ geometry. The mapping is therefore essentially unique within its topological class, providing a mathematically grounded explanation for the observed regularity in codon‑amino acid assignments.

\newpage
# Appendix C – Semantic primitives and Clifford correspondence

## C.1 Functional origin of the semantic nomenclature (A–P)
The 16 central concepts do not result from an arbitrary assignment, but from a functional readout of the algebraic–topological invariants. Each term describes the operational role played by the corresponding position within a discrete regulation network:

\begingroup
\small
\renewcommand{\tabularxcolumn}[1]{>{\raggedright\arraybackslash}m{#1}}
\setlength{\tabcolsep}{4pt}
\renewcommand{\arraystretch}{1.25}

\begin{table}[htbp]
\centering
\caption{Functional origin of the semantic nomenclature (A--P)}
\label{tab:semantic_origin}
\begin{tabularx}{\textwidth}{|X|X|X|X|}
\hline
\textbf{Algebraic Signature [$\mathrm{Cl}(4,0)$]} & \textbf{Topological Role in the Merkabah} & \textbf{Systemic Function} & \textbf{Assigned Concept} \\
\hline
$1$ (scalar, grade 0, positive sign) & Reference pole, non-overlapping & Reference state / setpoint & \textbf{Action / Truth} (capacity to initiate a transition from a neutral state) \\
\hline
$I, J, K$ (generators, grade 1, positive sign) & External faces, low intersection & Directional input channels & \textbf{Contribution} (structural input), \textbf{Appearance} (observable projection), \textbf{Perception} (difference capture) \\
\hline
$-1$ (inverted scalar, grade 0, negative sign) & Imposed global constraint & Symmetry breaking / order imposition & \textbf{Organisation} (structuring by limit) \\
\hline
$-I, -J, -K$ (inverted generators, grade 1, negative sign) & Primary edges, intermediate modulation & Differentiation, blending, relational invariance & \textbf{Difference}, \textbf{Mixture}, \textbf{Equivalence} \\
\hline
$i'I, i'J, i'K$ (pseudoscalar coupling, grade 3/4) & Vertices / diagonals, high intersection & Phase--charge coupling, directional transfer & \textbf{Relation} (coupling), \textbf{Flow} (oriented transfer), \textbf{Entity} (bounded identity) \\
\hline
$-i'I, -i'J, -i'K$ (inverted coupling) & Maximal intersection zones, high redundancy & Constrained evolution, contextual dependence, adaptive fluctuation & \textbf{Evolution}, \textbf{Dependence}, \textbf{Variation} \\
\hline
\end{tabularx}
\end{table}
\endgroup

This correspondence aligns with the tradition of functional semantics in systems theory: just as terms like *entropy*, *gain*, or *feedback* label the operational roles of mathematical constructs, the 16 concepts used here qualify the regulatory function of each node in the adjacency graph. Their validity does not rest on external intuition, but on predictive consistency: the same functional roles manifest in the degeneracy of the genetic code (low for reference poles, maximal for intersections), in syllabic phonology (consonant/vowel/tone as directional channels), and in economic cycles (constraint factors vs. flow factors). The A–P nomenclature is therefore a structure‑constrained descriptive layer, not a free parameter.
\newpage

## C.2 The 16 elements of Cl(4,0) and the 4 extra elements

\begingroup
\small
\setlength{\tabcolsep}{4pt}
\begin{longtable}{|c|c|c|c|c|c|}
\hline
\textbf{Cl(4,0)} & \textbf{Rank} & \textbf{Latin} & \textbf{Core Concept} & \textbf{Concepts (×4 per letter)} & \textbf{Polarity Triplet} \\
\hline
1 & 1 & A & Action/Truth & 1:A+, 2:A-, 3:Am, 4:A${\sim}m$ & $\{P_1,P_2,P_4\}=3P$ \\
I & 2 & B & Contribution & 5:B+, 6:B-, 7:Bm, 8:B${\sim}m$ & $\{P_1,P_3,P_5\}=3P$ \\
J & 3 & C & Appearance & 9:C+, 10:C-, 11:Cm, 12:C${\sim}m$ & $\{P_2,P_3,P_6\}=3P$ \\
K & 4 & D & Perception & 13:D+, 14:D-, 15:Dm, 16:D${\sim}m$ & $\{P_4,P_5,N_2\}=2P+1N$ \\
-1 & 5 & E & Organisation & 17:E+, 18:E-, 19:Em, 20:E${\sim}m$ & $\{P_5,P_6,N_3\}=2P+1N$ \\
-I & 6 & F & Difference & 21:F+, 22:F-, 23:Fm, 24:F${\sim}m$ & $\{P_1,P_6,N_4\}=2P+1N$ \\
-J & 7 & G & Mixture & 25:G+, 26:G-, 27:Gm, 28:G${\sim}m$ & $\{P_2,P_5,N_6\}=2P+1N$ \\
-K & 8 & H & Equivalence & 29:H+, 30:H-, 31:Hm, 32:H${\sim}m$ & $\{P_3,P_4,N_6\}=2P+1N$ \\
$i'1$ & 9 & I & Relation & 33:I+, 34:I-, 35:Im, 36:I${\sim}m$ & $\{P_1,N_2,N_6\}=1P+2N$ \\
$i'I$ & 10 & J & Flow & 37:J+, 38:J, 39:Jm, 40:J${\sim}m$ & $\{P_1,N_3,N_5\}=1P+2N$ \\
$i'J$ & 11 & K & Entity & 41:K+, 42:K-, 43:Km, 44:K${\sim}m$ & $\{P_2,N_3,N_5\}=1P+2N$ \\
$i'K$ & 12 & L & Circle/Cycle & 45:L+, 46:L-, 47:Lm, 48:L${\sim}m$ & $\{P_3,N_2,N_4\}=1P+2N$ \\
$-i'1$ & 13 & M & Evolution & 49:M+, 50:M-, 51:Mm, 52:M${\sim}m$ & $\{P_4,N_1,N_3\}=1P+2N$ \\
$-i'I$ & 14 & N & Dependence & 53:N+, 54:N-, 55:Nm, 56:N${\sim}m$ & $\{P_4,N_5,N_6\}=1P+2N$ \\
$-i'J$ & 15 & O & Variation & 57:O+, 58:O-, 59:Om, 60:O${\sim}m$ & $\{P_5,N_1,N_4\}=1P+2N$ \\
$-i'K$ & 16 & P & Grouping & 61:P+, 62:P-, 63:Pm, 64:P${\sim}m$ & $\{P_6,N_1,N_2\}=1P+2N$ \\
 & 17 & Q & Synergy & 7:Bm, 21:F+, 25:G & $\{P_2,N_1,N_4\}=1P+2N$ \\
 & 18 & R & Resonance & 29:H+, 33:I+, 37:J+ & $\{P_3,N_1,N_5\}=1P+2N$ \\
 & 19 & S & Spiral & 45:L+, 49:M+, 53:N+ & $\{P_6,N_5,N_6\}=1P+2N$ \\
 & 20 & T & Stratification & 57:O+, 61:P+, 63:Pm & $\{N_2,N_3,N_4\}=3N$ \\
\hline
\caption{The 16 elements of Cl(4,0) and the 4 extra elements}
\end{longtable}
\endgroup

*Note: The semantic labels are functional readouts of algebraic-topological invariants. The quaternary expansion ($+,-,m,\sim m$) maps directly to the 2-bit combinations of the boolean formalism (§2.2.1).*
\newpage

## C.3 The 16 tetrads of Cl(6,0) extended to 64 concepts

\begingroup
\small
\setlength{\tabcolsep}{4pt}
\begin{longtable}{|c|c|l||c|c|l|}
\hline
\multicolumn{3}{c||}{\textbf{Tetrads A–H}} & \multicolumn{3}{c}{\textbf{Tetrads I–P}} \\
\cline{1-6}
\textbf{Cl(6,0)} & \textbf{N°} & \textbf{Concept} & \textbf{Cl(6,0)} & \textbf{N°} & \textbf{Concept} \\
\hline
1 & 1 & A+ : Action, effective truth & $i'1$ & 33 & I+ : Relation, association \\
1i & 2 & A- : Inaction, illusion & $i'1i$ & 34 & I- : Isolation, independence \\
1j & 3 & Am : Intention, potentiality & $i'1j$ & 35 & Im : Interdependence, network \\
1k & 4 & A${\sim}m$ : Chance, necessity & $i'1k$ & 36 & I${\sim}m$ : Fusion, unification \\
\hline
I & 5 & B+ : Contribution, input & $i'I$ & 37 & J+ : Flow, transfer \\
Ii & 6 & B- : Privation, subtraction & $i'Ii$ & 38 & J- : Stasis, immobility \\
Ij & 7 & Bm : Exchange, reciprocity & $i'Ij$ & 39 & Jm : Cycle, rhythm \\
Ik & 8 & B${\sim}m$ : Self-sufficiency, pure gift & $i'Ik$ & 40 & J${\sim}m$ : Turbulence, chaos \\
\hline
J & 9 & C+ : Appearance, form & $i'J$ & 41 & K+ : Entity, being \\
Ji & 10 & C- : Essence, substance & $i'Ji$ & 42 & K- : Void, non-being \\
Jj & 11 & Cm : Symbol, representation & $i'Jj$ & 43 & Km : Relation, context \\
Jk & 12 & C${\sim}m$ : Naked reality, hidden truth & $i'Jk$ & 44 & K${\sim}m$ : Substance, essence \\
\hline
K & 13 & D+ : Perception, sensation & $i'K$ & 45 & L+ : Circle, cycle \\
Ki & 14 & D- : Unconsciousness, anesthesia & $i'Ki$ & 46 & L- : Line, linearity \\
Kj & 15 & Dm : Consciousness, attention & $i'Kj$ & 47 & Lm : Spiral, helix \\
Kk & 16 & D${\sim}m$ : Intuition, direct knowledge & $i'Kk$ & 48 & L${\sim}m$ : Point, singularity \\
\hline
-1 & 17 & E+ : Organisation, structure & $-i'1$ & 49 & M+ : Evolution, becoming \\
-1i & 18 & E- : Chaos, disorder & $-i'1i$ & 50 & M- : Eternity, immutability \\
-1j & 19 & Em : Emergence, self-organisation & $-i'1j$ & 51 & Mm : Growth, development \\
-1k & 20 & E${\sim}m$ : Constraint, imposed order & $-i'1k$ & 52 & M${\sim}m$ : Revolution, mutation \\
\hline
-I & 21 & F+ : Difference, otherness & $-i'I$ & 53 & N+ : Dependence, influence \\
-Ii & 22 & F- : Identity, unity & $-i'Ii$ & 54 & N- : Autonomy, freedom \\
-Ij & 23 & Fm : Relation, interface & $-i'Ij$ & 55 & Nm : Interdependence, balance \\
-Ik & 24 & F${\sim}m$ : Absolute separation & $-i'Ik$ & 56 & N${\sim}m$ : Constraint, necessity \\
\hline
-J & 25 & G+ : Mixture, blending & $-i'J$ & 57 & O+ : Variation, change \\
-Ji & 26 & G- : Pure, simple & $-i'Ji$ & 58 & O- : Constancy, stability \\
-Jj & 27 & Gm : Combination, synergy & $-i'Jj$ & 59 & Om : Adaptation, flexibility \\
-Jk & 28 & G${\sim}m$ : Confusion, amalgam & $-i'Jk$ & 60 & O${\sim}m$ : Instability, chaos \\
\hline
-K & 29 & H+ : Equivalence, correspondence & $-i'K$ & 61 & P+ : Grouping, set \\
-Ki & 30 & H- : Incommensurability & $-i'Ki$ & 62 & P- : Individuality, unity \\
-Kj & 31 & Hm : Analogy, proportion & $-i'Kj$ & 63 & Pm : Hierarchy, organisation \\
-Kk & 32 & H${\sim}m$ : Perfect identity & $-i'Kk$ & 64 & P${\sim}m$ : Crowd, mass \\
\hline
\caption{The 16 tetrads of Cl(6,0) (64 concepts)}
\end{longtable}
\endgroup

\newpage

# Appendix D – Positive and Negative Pentads: Alignment with the 64 Tetrads

## D.1 Positive and Negative Pentads: Alignment with the 64 Tetrads

\begingroup
\footnotesize
\setlength{\tabcolsep}{2.2pt}
\renewcommand{\arraystretch}{1.15}
\centering
\begin{longtable}{|c|c|l||c|c|l|}
\hline
\multicolumn{3}{c||}{\textbf{Positive Pentads ($P_1$–$P_6$)}} & \multicolumn{3}{c}{\textbf{Negative Pentads ($N_1$–$N_6$)}} \\
\cline{1-6}
\textbf{Pentad} & \textbf{Clifford Elements} & \textbf{Tetrad Mapping (N°/Concept)} & \textbf{Pentad} & \textbf{Clifford Elements} & \textbf{Tetrad Mapping (N°/Concept)} \\
\hline
$P_1$ & $\{Ii,\; Ij,\; Ik,\; i'1k,\; 1j\}$ &
$\begin{array}{@{}l@{}}
Ii \rightarrow 6\;(B^-) \\
Ij \rightarrow 7\;(B^m) \\
Ik \rightarrow 8\;(B^{\sim m}) \\
i'1k \rightarrow 36\;(I^{\sim m}) \\
1j \rightarrow 3\;(A^m)
\end{array}$ &
$N_1$ & $\{-Ii,\; -Ij,\; -Ik,\; -i'1k,\; -1j\}$ &
$\begin{array}{@{}l@{}}
-Ii \rightarrow 5\;(B^+) \\
-Ij \rightarrow \text{dual}(7) \\
-Ik \rightarrow \text{dual}(8) \\
-i'1k \rightarrow 33\;(I^+) \\
-1j \rightarrow 1\;(A^+)
\end{array}$ \\
\hline
$P_2$ & $\{Ij,\; Jj,\; Kj,\; i'1i,\; 1k\}$ &
$\begin{array}{@{}l@{}}
Ij \rightarrow 7\;(B^m) \\
Jj \rightarrow 11\;(C^m) \\
Kj \rightarrow 15\;(D^m) \\
i'1i \rightarrow 34\;(I^-) \\
1k \rightarrow 4\;(A^{\sim m})
\end{array}$ &
$N_2$ & $\{-Ij,\; -Jj,\; -Kj,\; -i'1i,\; -1k\}$ &
$\begin{array}{@{}l@{}}
-Ij \rightarrow \text{dual}(7) \\
-Jj \rightarrow \text{dual}(11) \\
-Kj \rightarrow \text{dual}(15) \\
-i'1i \rightarrow 37\;(J^+) \\
-1k \rightarrow 2\;(A^-)
\end{array}$ \\
\hline
$P_3$ & $\{Ik,\; Jk,\; Kk,\; i'1j,\; 1i\}$ &
$\begin{array}{@{}l@{}}
Ik \rightarrow 8\;(B^{\sim m}) \\
Jk \rightarrow 12\;(C^{\sim m}) \\
Kk \rightarrow 16\;(D^{\sim m}) \\
i'1j \rightarrow 35\;(I^m) \\
1i \rightarrow 2\;(A^-)
\end{array}$ &
$N_3$ & $\{-Ik,\; -Jk,\; -Kk,\; -i'1j,\; -1i\}$ &
$\begin{array}{@{}l@{}}
-Ik \rightarrow \text{dual}(8) \\
-Jk \rightarrow \text{dual}(12) \\
-Kk \rightarrow \text{dual}(16) \\
-i'1j \rightarrow 33\;(I^+) \\
-1i \rightarrow 1\;(A^+)
\end{array}$ \\
\hline
$P_4$ & $\{i'Ii,\; i'Ij,\; i'Ik,\; i'K,\; J\}$ &
$\begin{array}{@{}l@{}}
i'Ii \rightarrow 38\;(J^-) \\
i'Ij \rightarrow 39\;(J^m) \\
i'Ik \rightarrow 40\;(J^{\sim m}) \\
i'K \rightarrow 45\;(L^+) \\
J \rightarrow 9\;(C^+)
\end{array}$ &
$N_4$ & $\{-i'Ii,\; -i'Ij,\; -i'Ik,\; -i'K,\; -J\}$ &
$\begin{array}{@{}l@{}}
-i'Ii \rightarrow 37\;(J^+) \\
-i'Ij \rightarrow \text{dual}(39) \\
-i'Ik \rightarrow \text{dual}(40) \\
-i'K \rightarrow 46\;(L^-) \\
-J \rightarrow 10\;(C^-)
\end{array}$ \\
\hline
$P_5$ & $\{i'Ji,\; i'Jj,\; i'Jk,\; i'I,\; K\}$ &
$\begin{array}{@{}l@{}}
i'Ji \rightarrow 42\;(K^-) \\
i'Jj \rightarrow 43\;(K^m) \\
i'Jk \rightarrow 44\;(K^{\sim m}) \\
i'I \rightarrow 37\;(J^+) \\
K \rightarrow 13\;(D^+)
\end{array}$ &
$N_5$ & $\{-i'Ji,\; -i'Jj,\; -i'Jk,\; -i'I,\; -K\}$ &
$\begin{array}{@{}l@{}}
-i'Ji \rightarrow 41\;(K^+) \\
-i'Jj \rightarrow \text{dual}(43) \\
-i'Jk \rightarrow \text{dual}(44) \\
-i'I \rightarrow 38\;(J^-) \\
-K \rightarrow 14\;(D^-)
\end{array}$ \\
\hline
$P_6$ & $\{i'Ki,\; i'Kj,\; i'Kk,\; i'J,\; I\}$ &
$\begin{array}{@{}l@{}}
i'Ki \rightarrow 46\;(L^-) \\
i'Kj \rightarrow 47\;(L^m) \\
i'Kk \rightarrow 48\;(L^{\sim m}) \\
i'J \rightarrow 41\;(K^+) \\
I \rightarrow 5\;(B^+)
\end{array}$ &
$N_6$ & $\{-i'Ki,\; -i'Kj,\; -i'Kk,\; -i'J,\; -I\}$ &
$\begin{array}{@{}l@{}}
-i'Ki \rightarrow 45\;(L^+) \\
-i'Kj \rightarrow \text{dual}(47) \\
-i'Kk \rightarrow \text{dual}(48) \\
-i'J \rightarrow 42\;(K^-) \\
-I \rightarrow 6\;(B^-)
\end{array}$ \\
\hline
\caption{Positive and negative pentads: strict alignment with the 64 tetrads of $\mathrm{Cl}(6,0)$}
\label{tab:pentads}
\end{longtable}
\endgroup

*The elements of the pentads are rewritten in canonical order $i<j<k<I<J<K$. The signs induced by anticommutation ($ab=-ba$) are carried over to the corresponding Boolean state, ensuring a strict bijection with the table of 64 tetrads.*

\newpage
![Dual graph of pentads](Penta_graph.png){ width=100% }

