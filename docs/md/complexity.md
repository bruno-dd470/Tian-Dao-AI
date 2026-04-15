---
title: "The Genetic Code as a 64->20 Clifford Invariant: Implications for Self-Regulating AI"
author: "Bruno DE DOMINICIS"
ORCID: 0009-0009-0380-3056
date: "April 2026"
doi: "10.5281/zenodo.19540508"
abstract_en: |
  The regulation of combinatorial complexity is a central challenge for natural and artificial systems. The genetic code addresses this by mapping 64 codons onto 20 functional classes via organized redundancy that confers robustness and error tolerance.
  Building on on Peter Rowlands’ work on nilpotent Clifford algebras, we show that the 64-element structure of $\mathrm{Cl}(6,0)$, after symmetry breaking, reduces to 20 stable attractors geometrically organized into level-3 double tetrahedra (Merkabah). Imposing a neighborhood rule based on the sharing of a common triangular face between two tetrahedra filters the 64 configurations into exactly 20 equivalence classes.
  We formalize this 64→20 invariant by defining a six-dimensional space of binary configurations and a topological grouping criterion. Each class is identified by a triplet of pentads—irreducible of $\mathrm{Cl}(6,0)$ corresponding to the 12 pentagonal faces of the dodecahedron. The pentads are partitioned into six positive ($P$) and six negative ($N$) ones, so that the polarity signature of any class simply counts the number of positive and negative pentads in its triplet ($3P$, $2P+1N$, $1P+2N$, or $3N$). This structural gradient defines the admissible redundancy space that the genetic code exploits in a differentiated manner according to functional and evolutionary constraints.
  The dual graph of the 12 pentads, constructed directly from the Merkabah triplets, exhibits two disjoint 5-cycles (tropical belts $C_P$ and $C_N$) and two polar thresholds ($P_4$, $N_4$). Within each pentad, the five elements realize a five-phase local dynamic (Wuxing) via two complementary cycles: the pentagon (sheng) and the pentagram (ke). Externally, the tropical belts propagate these cycles as modes of global regulation. This structural core, independent of the substrate, provides a mathematically grounded reference architecture for self-limiting and regulated artificial intelligence. 
  **DOI:** [10.5281/zenodo.19540508](https://doi.org/10.5281/zenodo.19540508)
runninghead: "CLIFFORD INVARIANT AND GENETIC CODE"
header-includes: |
  \usepackage{pdflscape}
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

The regulation of combinatorial complexity constitutes a fundamental challenge for any system that processes, stores, or transmits information. In natural systems, this regulation does not rely on an unlimited accumulation of parameters, but on structural constraints that channel the space of possible states toward a functionally viable subset. The genetic code offers a paradigmatic example of this: it maps 64 nucleotide triplets onto 20 functional classes (19 amino acids and a stop codon) through organized redundancy that confers robustness, error tolerance, and translational stability. This ability to *filter* complexity rather than optimize it locally distinguishes resilient systems from purely expansive architectures.

In contemporary artificial intelligence, the dominant response to complexity has been to increase model size, data volume, and computational power, coupled with the statistical optimization of external objective functions. Although this approach has enabled spectacular progress, it is now revealing its structural limitations: decision-making opacity, susceptibility to specification drift ), increasing energy consumption, and dependence on software safeguards applied *a posteriori* [4, 5]. These systems, lacking endogenous constraints, tend to maximize a metric at the expense of the host system’s overall coherence. The problem is therefore not merely technological or algorithmic; it is above all structural. Modern AI lacks a formal framework of intrinsic regulation, capable of bounding the search space by design rather than through external supervision.

We formulate here the hypothesis that the $64 \rightarrow 20$ reduction observed in the genetic code is not the result of a contingent evolutionary optimization, but the manifestation of a topological invariant independent of the substrate. Drawing on Peter Rowlands’ work on nilpotent Clifford algebras, we show that the 64-element structure of $\mathrm{Cl}( 6,0)$, subject to a geometric neighborhood rule (triangular face sharing in a level-3 double tetrahedron, or *Merkabah*), naturally partitions into exactly 20 stable equivalence classes. Each class is characterized by a triplet of pentads—irreducible algebraic units corresponding to the faces of a dual dodecahedron—whose polarity signature ($3P$, $2P+1N$, $1P +2N$ or $3N$) defines a structural redundancy gradient. This filtration kernel, purely geometric and algebraic, presupposes no cost function, no supervisor, nor any external metric. It provides a mathematically closed framework for endogenous complexity regulation, transposable to any discrete system.

This article pursues three complementary objectives. First, it algorithmically formalizes the $64 \rightarrow 20$ invariant by defining the binary configuration space, the geometric constraint of the *Merkabah*, and the topological clustering criterion. Second, it exhaustively validates this invariant on the standard genetic code, demonstrating that the codon degeneracy landscape strictly aligns with the admissible bounds predicted by topology. Third, it extends this static framework to a complete regulatory dynamic (Wuxing cycles, tropical belts, $P_4/N_4$ polar thresholds, discrete Dirac operator, and $\mathrm{Cl}(6,6)$ reservoir) and discusses its implications for the design of self-regulating artificial intelligence.

The paper is structured as follows: Section 2 presents the algebraic-geometric foundations and the filtration procedure. Section 3 introduces the $64 \rightarrow 20$ static invariant and its exhaustive correspondence with the genetic code. Section 4 develops the dynamic framework of endogenous regulation and the associated spectral observables. Section 5 details the algorithmic architecture for a homeostatic AI. Section 6 explores transdisciplinary and symbolic convergences, before Section 7 synthesizes the results and outlines research perspectives.

# 2. Algebraic-Geometric Foundations

## 2.1. Configuration space: from $\mathrm{Cl}(4,0)$ to $\mathrm{Cl}(6,0)$ via Boolean extension
The complete configuration space is generated from the 16 fundamental algebraic primitives, which form the canonical basis of the Clifford algebra $\mathrm{Cl}(4,0)$. To reach the 64-dimensional space required by the $\mathrm{Cl}(6,0)$ structure, we apply a quaternary Boolean modal extension to each primitive. Let $\mathcal{C}$ be the set of resulting configurations, modeled as a combinatorial space with six binary dimensions:
$$
\mathbf{c} = (b_1, b_2, b_3, b_4, b_5, b_6), \quad b_i \in \{0,1\}.
$$
The cardinality of this space is $|\mathcal{C}| = 2^6 = 64$, corresponding bijectively to the elements of the basis of $\mathrm{Cl}(6,0)$. This extension is based on two independent ontological dimensions $P$ and $Q$. The four mutually exclusive and exhaustive states associated with each primitive $X \in \{A,\dots,P\}$ are defined by:
$$
\begin{aligned}
X_1 &= P \cap \neg Q \quad (\text{state } +), \\
X_2 &= \neg P \cap Q \quad (\text{state } -), \\
X_3 &= P \cap Q \quad (\text{state } m), \\
X_4 &= \neg P \cap \neg Q \quad (\text{state } \sim m),
\end{aligned}
$$

which correspond bijectively to the bit pairs $(10, 01, 11, 00)$. The Cartesian product $16 \times 4$ thus generates the complete space of the 64 configurations of $\mathrm{Cl}(6,0)$ from the basis of $\mathrm{Cl}(4,0)$. This modal layer preserves the algebraic signature of each primitive while guaranteeing structural closure without introducing paraconsistent contradictions [11, 13] . At this stage, no physical or biological interpretation is required; only algebraic combinatorics defines the filtration space.

## 2.2. The Level 3 Double Tetrahedron (Merkabah): Subdivision and Tetrahedral Cells
The underlying geometric structure is the Level 3 double tetrahedron, commonly referred to as the *Merkabah*. Its construction follows a strict hierarchical subdivision:

1. A Level 1 tetrahedron (4 faces) interpenetrated with its dual forms a **double tetrahedron** of level 2. This composition generates 16 triangular faces (8 external + 8 internal arising from the intersection planes).
2. The subdivision of each of these 16 faces into 4 elementary sub-triangles produces exactly $16 \times 4 = 64$ triangles. These elementary faces correspond bijectively to the 64 configurations of $\mathcal{C}$.

During this operation, the midpoints of the original edges and the intersection planes of the two tetrahedra delimit **8 internal octahedral zones**. These regions correspond to transition interfaces with high connectivity but where polarity equilibrium cannot be maintained. By grouping compatible peripheral elementary regions and integrating **the two opposing reference poles of the compound** (the dual vertices that anchor the structure and correspond to the scalar and pseudo-scalar generators of the algebra, thereby topologically closing the network), we obtain exactly **20 stable tetrahedral cells**. These 20 tetrahedra constitute the attractor basins of the system. The 8 residual octahedral zones, although topologically present, are excluded from the filtration process $64 \to 20$ because they violate the polar closure condition required for stable states.

**Note on pole duality**: Although the basis of $\mathrm {Cl}(6,0)$ contains four scalar/pseudo-scalar elements ($+1, -1, +i', -i'$), the geometry of the Merkabah retains only **two structural poles**. These poles correspond to the two fundamental axes of the algebra: the scalar axis (ontological reference) and the pseudo-
 -scalar axis (phase/time). The signs $\pm$ do not denote independent geometric poles, but rather the **two orientations** along each of these axes. Structurally, this binary duality suffices to close the topological network and generate the polarity gradient $3P \rightarrow 3N$. Counting 4 distinct poles would break the uniform incidence of the pentads (5 occurrences rences per pentad) and would make the exact partition into 20 attractors impossible. The formalism therefore identifies 2 structural poles, each supporting two complementary algebraic orientations.

## 2.3. The pentads: irreducible composite units and correspondence to the faces of the dodecahedron
The fundamental algebraic building block of this filtration is the *pentad*. Arising from the brise of symmetry of the eight primitive elements of $\mathrm{Cl}(6,0)$, it is defined as a closed set of five irreducible composite units:
$$
\boxed{\{1j,\; iI,\; iJ,\; iK,\; i'k\}}.
$$
Each pentad associates a one-dimensional quantity (mass or time) with a three-dimensional direction (space or charge), preserving the self-duality of the algebra. There are exactly **12 pentads**, partitioned into six positive ones ($P_1 \dots P_6$) and six negative ones ($N_1 \dots N_6$) .

Geometrically, each pentad corresponds to one of the twelve pentagonal faces of the dual dodecahedron of the Merkabah. The incidence structure of the Merkabah requires that each tetrahedral cell (attractor) be defined by the intersection of exactly three pentads. Thus, the 20 attractors are identified by a triplet $\{X, Y, Z\} \subset \{P_1,\dots,P_6, N_1,\dots,N_6\}$, whose algebraic composition determines their polar signature. The uniform distribution of the pentads (each appears in exactly 5 triplets) guarantees the topological equilibrium of the adjacency graph.

## 2.4. Topological Neighborhood Rule and Filtering Principle
The reduction of the space of 64 configurations relies on a strictly geometric adjacency constraint. Let $\phi : \mathcal{C} \rightarrow \mathcal{T}_ {20}$ the surjective mapping associating each configuration $\mathbf{c}$ with its corresponding tetrahedral cell in the *Merkabah*. Two configurations $\mathbf{c}_1, \mathbf{c}_2 \in \mathcal{C}$ are said to be * neighbors* if and only if the tetrahedra $\phi(\mathbf{c}_1)$ and $\phi(\mathbf{c}_2)$ share an **entire triangular face**. This condition explicitly excludes adjacencies via edges or vertices, which would correspond to higher-degree interactions in the dual graph and do not satisfy the required topological closure.

For each configuration, we define its closed neighborhood $N[\mathbf{c}]$ as the set of $\mathbf{c}$ and its immediate neighbors. The filtering criterion
 
consists of grouping together configurations whose closed neighborhood graphs are isomorphic. This operation is purely combinatorial and does not depend on any adjustable parameter, statistical threshold, or external optimization function. The partition induced by this procedure is detailed and interpreted in the following section.

# 3. The static invariant $64 \rightarrow 20$

## 3.1. Partition into 20 equivalence classes and the concept of attractors
The systematic application of the isomorphism criterion defined in §2.4 produces a strict partition of $\mathcal {C}$ into exactly **20 equivalence classes**. Each class groups together configurations sharing an identical neighborhood signature under the action of the automorphism group of the double tetrahedron. We shall henceforth refer to these classes as *attractors*, in the sense of topologically closed basins: their stability is guaranteed by the face-sharing rule, which prohibits any transition outside the basin without breaking geometric adjacency. The cardinality of this partition constitutes the central invariant of this work:
$$
|\mathcal{C}/\!\sim| = 20.
$$
This reduction thus emerges solely from the intrinsic symmetry of the *Merkabah* . No external metric or supervisor is required: the geometry filters the combinatorial space and sets the structural bounds that the projected systems (biological or algorithmic) will subsequently exploit.

## 3.2. Triplets of pentads and polarity signatures ($3P$, $2P+1N$, $1P+2N$, $3N$)
Each attractor is uniquely identified by the triplet of pentads $\{X, Y, Z\} \subset \{P_1,\dots,P_6, N_1,\dots,N_6\}$ corresponding to the three intersecting faces of the dual dodecahedron. The composition of this triplet determines its *polarity signature*, obtained by counting the number of positive ($P$) and negative ($N$) pentads. Given the uniform distribution of the 12 pentads (each belongs to exactly 5 triplets), only four signatures are topologically admissible:

- **$3P$**: 3 classes. Triplets composed exclusively of positive pentads.
- **$2P+1N$**: 5 classes. Two positive pentads, one negative.
- **$1P+2N$**: 11 classes. One positive pentad, two negative ones.
- **$3N$**: 1 class. Exclusively negative triplet.

This distribution (3, 5, 11, 1) is not arbitrary; it reflects the incidence geometry of the Level 3 *Merkabah*. The $3P$ classes occupy the poles or non-overlapping zones, the $2P+1N$ classes are located on the outer faces and primary edges, the $1P+2N$ classes converge at the vertices, diagonals, and triadic intersections, while the single $3N$ class occupies the most constrained inner core. This gradient of polarity defines an admissible space of structural redundancy that will be exploited differently depending on the systems projected onto it.

## 3.3. Exhaustive correspondence with the standard genetic code
To validate the invariant on a concrete biological system, we apply the bijection $\psi : \{\text{codons}\} \rightarrow \mathcal{C}$ defined by $A=00$, $U=01$, $G=10$, $C=11$. This mapping preserves Watson-Crick complementarity in the form of binary negation and aligns the least significant bit with the purine/pyrimidine distinction. By transferring the topological neighborhood rule to the 64 codons via $\psi^{-1}$, the resulting partitioning strictly coincides with the standard functional classification into 20 amino acids and a stop codon class.

The correspondence is bijective and exhaustive:

- **$3P$ classes**: Methionine (AUG, initiation signal), Tryptophan (UGG) , Phenylalanine (UUU, UUC).
- **$2P+1N$ classes**: Isoleucine, Valine, Proline, Threonine, Alanine.
- **$1P+2N$ classes**: Serine, Leucine, Arginine, Glycine, Tyrosine, Histidine, Glutamine, Asparagine, Lysine, Aspartic acid, Glutamic acid.
- **Class $3N$**: Cysteine and the three STOP codons (UAA, UAG, UGA), sharing the same geometric termination/boundary core.

This structural congruence confirms that the degeneracy landscape of the genetic code aligns exactly with the admissible boundaries predicted by Clifford topology. The detailed codon-by-codon mapping is provided in Appendix B.

## 3.4. Geometric Gradient and Biological Degeneracy: Structural Constraints vs. Evolutionary Optimization
The correspondence between the geometric partition and the observed codon degeneracy is not a matter of chance, but of a strong topological constraint. The $3P \rightarrow 3N$ polarity gradient correlates directly with the degree of convergence of the pentads in the *Merkabah*:

- **$3P$ classes (geometrically isolated)**: their low connectivity strictly limits the permissible neighborhood, corresponding biologically to minimal degeneracy (1–2 codons).
- **$2P+1N$ classes (moderate overlap)**: located on structural edges, they allow for intermediate redundancy (3–4 codons), typical of residues with versatile physicochemical properties.
- **$1P+2N$ classes (maximal intersections)**: the convergence of multiple pentads creates high structural redundancy, allowing for up to 6 codons. This is indeed the case for Serine, Leucine, and Arginine. However, the topology does not impose systematic maximum degeneracy; biochemical or evolutionary constraints keep certain residues in this class at 2 or 4 codons.
- **Class $3N$ (inner core)**: positioned at the most confined vertex, it plays a functional threshold role, grouping Cysteine (2 codons) and the three STOP codons (3 codons), marking a boundary of the translational pathway.

It is crucial to emphasize that this correspondence does not imply absolute geometric determinism. The topology of the *Merkabah* does not prescribe the exact number of codons per amino acid; amino acid; it defines the **permissible bounds** and the **differential distribution of redundancy potential**. The standard genetic code fulfills this structural prediction exactly: no isolated class exceeds 2 codons, no moderately connected class exceeds 4 codons, and only convergence zones allow for maximum degeneracy. The precise value observed for each residue results from a functional and evolutionary optimization that operates *strictly within* this predefined topological landscape, never in contradiction with it. In summary: **geometry predicts the architecture of the degeneracy landscape; biology populates its coordinates according to functional imperatives.**

\begin{table}[H]
\centering
\caption{Classification of the 20 classes of the genetic code in the Merkabah dodecahedron}
\label {tab:genetic_classes}
\small
\setlength{\tabcolsep}{3pt}
\begin{tabularx}{\textwidth}{|@{}>{\centering\arraybackslash}p{1.0 cm}|>{\centering\arraybackslash}p{2.2 cm}|>{\centering\arraybackslash}p{1.2 cm}|X|>{\centering\arraybackslash}p{0.8 cm}|>{\footnotesize\centering\arraybackslash}X|>{\centering\arraybackslash}p{2.2 cm}@{}|}
\hline
\textbf{Class} & \textbf{Pentad triplet} & \textbf {Polarity} & \textbf{Geometric Position (Merkabah)} & \textbf{Deg.} & \textbf{Codon(s)} & \textbf{Amino Acid} \\
\hline
A & $\{P_1, P_2, P_4\}$ & 3P & Reference pole & 1 & AUG & Methionine \\
B & $\{P_1, P_3, P_5\}$ & 3P & North face & 1 & UGG & Tryptophan \\
C & $\{P_2, P_3, P_6\}$ & 3P & South face & 2 & UUU, UUC & Phenylalanine \\
D & $\{P_4, P_5, N_2\}$ & 2P+N & East face & 3 & AUU, AUC, AUA & Isoleucine \\
E & $\{P_5, P_6, N_3\}$ & 2P+N & West face & 4 & GUU, GUC, GUA, GUG & Valine \\
F & $\{P_1, P_6, N_4\}$ & 2P+N & Northeast edge & 4 & CCU, CCC, CCA, CCG & Proline \\
G & $\{P_2, P_5, N_6\} $ & 2P+N & NW edge & 4 & ACU, ACC, ACA, ACG & Threonine \\
H & $\{P_3, P_4, N_6\}$ & 2P+N & SE edge & 4 & GCU, GCC, GCA, GCG & Alanine \\
I & $\{P_1, N_2, N_6\}$ & 1P+2N & Southwest edge & 6 & UCU, UCC, UCA, UCG, AGU, AGC & Serine \\
J & $\{P_1, N_3, N_5\}$ & 1P+2N & North vertex & 6 & UUA, UUG, CUU, CUC, CUA, CUG & Leucine \\
K & $\{P_2, N_3, N_5\}$ & 1P+2N & South vertex & 6 & CGU, CGC, CGA, CGG, AGA, AGG & Arginine \\
L & $\{P_3, N_2, N_4\}$ & 1P+2N & East vertex & 4 & GGU, GGC, GGA, GGG & Glycine \\
M & $\{P_4, N_1, N_3\}$ & 1P+2N & West vertex & 2 & UAU, UAC & Tyrosine \\
N & $\{P_4, N_5, N_6\}$ & 1P+2N & Diagonal 1 & 2 & CAU, CAC & Histidine \\
O & $\{P_5, N_1, N_4\}$ & 1P+2N & Diagonal 2 & 2 & CAA, CAG & Glutamine \\
P & $\{P_6, N_1, N_2\}$ & 1P+2N & Diagonal 3 & 2 & AAU, AAC & Asparagine \\
Q & $\{P_2, N_1, N_4\}$ & 1P+2N & Intersection A–B–C & 2 & AAA, AAG & Lysine \\
R & $\{P_3, N_1, N_5\}$ & 1P+2N & Intersection D–E–F & 2 & GAU, GAC & Aspartic acid \\
S & $\{P_6, N_5, N_6\}$ & 1P+2N & Intersection G–H–I & 2 & GAA, GAG & Glutamic acid \\
T & $\{N_2, N_3, N_4\}$ & 3N & Inner core (J–K–L) & 2 + 3 & UGU, UGC, UAA, UAG, UGA & Cysteine + Stop \\
\hline
\end{tabularx}
\end{table}

# 4. Dynamic framework of endogenous regulation

## 4.1. Dual graph of pentads: tropical belts ($C_P$, $C_N$) and polar thresholds ($P_4$, $N_4$)
The static invariant $64 \rightarrow 20$ provides a closed topological skeleton. To model dynamic regulation, we use the dual graph $\Gamma$ constructed directly from the 20 triplets of pentads. The Python script is available on GitHub. The vertices of $\Gamma$ are the 12 pentads $\{P_1,\dots,P_6, N_1,\dots,N_6\}$; two vertices are connected by an edge if they belong to the same attractor’s triplet. This purely combinatorial construction requires no external geometric projection (see Figure 1 on the last page).

A thorough analysis of $\Gamma$ reveals a remarkable structure: it contains exactly two disjoint cycles of length 5, referred to as **tropical belts**:
$$
C_P = (P_1 \to P_3 \to P_5 \to P_6 \to P_2 \to P_1), \quad
C_N = (N_1 \to N_2 \to N_6 \to N_5 \to N_3 \to N_1).
$$
The subgraph induced by $C_P$ is a complete graph $K_5$, whereas $C_N$ contains only two additional internal edges ($N_1\text{–}N_5$ and $N_2\text{–}N_3$). The two remaining pentads, $P_4$ and $N_4$, are absent from these cycles. Their degree in $\Gamma$ is high (8 and 9, respectively) and they structurally connect the two belts. Consequently, $P_4$ and $N_4$ act as **polar thresholds**: any dynamic transition between the dynamics carried by $C_P$ and those carried by $C_N$ must necessarily pass through one of these two nodes, which function as topological hinges rather than static boundaries.

## 4.2. Wuxing Cycles: Internal Dynamics (Pentagon/Pentagram) and External Dynamics (Relational Circulation)
The regulatory dynamics operate on two decoupled scales, the superposition of which prevents locking into a single regime.

**Internal Wuxing**
 : within each pentad, the five composite units induce two distinct cyclic orders via the Clifford product. The *sheng* (generative) cycle follows the order of the pentagon ($A \to B \to C \to D \to E \to A$), while the *ke* (regulatory) cycle follows the order of the pentagram ($A \to C \to E \to B \to D \to A$). These two modes correspond to the two generators of the cyclic group $C_5$ and ensure the local closure of each pentad.
**External Wuxing**: in the dual graph $\Gamma$ — topologically isomorphic to the skeleton of a regular dodecahedron —, the tropical belts $C_P$ and $C_N$ correspond to two disjoint equatorial bands of five pentagonal faces wrapping around the solid. The propagation of modes is strictly constrained by this geometry: the *sheng* mode follows the adjacent edges of the pentagons (continuous traversal, neighbor $\to$ neighbor), while the *ke* mode skips a vertex, forming the pentagram inscribed in each face. Global regulation emerges from the compatibility between the modes assigned to the pentads of the same attractor triplet. Crucially, the internal and external dynamics are not synchronized: an internal *sheng* can coexist with an external *ke*, creating local phase shifts that maintain the system’s plasticity and facilitate regime switches via the polar thresholds $P_4 /N_4$, which act as axial hinges connecting the two belts.

## 4.3. Topological feedback and cyclic frustration descent (without an external cost function)
The system has $20 \times 2 \times 2^3 = 320$ admissible local regimes (per attractor: 2 triplet orders $\times$ 8 *sheng/ke* combinations per pentad). Regulation does not rely on any external objective function, but on a **topological frustration descent**.

For each pentad $F$, we define a discrete energy $E(F)$ quantifying the incompatibility of local regimes across the 5 attractors incident to it. This energy is calculated from three binary penalties:
- $E_{\text{direction}}$: global misalignment of modes $\varepsilon \in \{+1,-1\}$ (*sheng/ke*);
- $E_{\text{phase}}$: incoherence of triplet orientations $\varphi \in \{0,1\}$;
- $E_{\text{order}}$: violation of the cyclic order of positions $\kappa \in \{0,1,2\}$.
$$
E(F) = 2E_{\text{direction}} + E_{\text{phase}} + E_{\text{order}} \in \{0, 1, 2, 3, 4\}.
$$

The global dynamics minimizes $E_{\text{tot}} = \sum_{F \in \Gamma} E(F)$ through local updates: if $E(F) > 0$,
 
the incident attractors adjust $\varepsilon$ or $\varphi$ so as to strictly reduce the energy. This purely relational feedback loop guarantees convergence toward a state of global compatibility, without central supervision or external metrics. The conserved quantity is the coherence of the *sheng/ke* cycles across the pentadic network, which acts as a structural invariant preventing combinatorial drift.

## 4.4. Discrete Dirac Operator and Spectral Observables ($\eta$, $d$, $\mathrm{gap}$, $R_{\text{threshold}}$)
To quantify the emerging global state, we construct a discrete Dirac operator $D(t)$ acting on the graph $\Gamma$. Each pentad hosts a local 2-component spinor $\psi_i \in \mathbb{C}^2$ encoding the polarity $\varepsilon$ and the phase $\varphi$. The $24 \times 24$ operator ($12$ pentads $\times 2$ components) is defined by:
$$
(D\psi)_i = \sum_{j \sim i} w_{ij}(t) \, \sigma_{ij} \, \psi_j, \quad \text{where } w_{ij}(t) = e^{-\beta E_{ij}(t) },
$$
where $\sigma_{ij}$ are Pauli-type coupling matrices depending on the relative orientation, and $\beta > 0$ is a stiffness parameter. The diagonalization of $D(t)$ yields a compact spectral signature $S(t) \in \mathbb{R}^4$:

- **$\eta(t)$**: global spectral asymmetry, a discrete analogue of the Atiyah–Singer index. $\eta > 0$ indicates *sheng* dominance (exploration), $\eta < 0$ indicates *ke* dominance (constraint), and $\eta \approx 0$ indicates a tipping point.
- **$d(t)$**: effective spectral dimension, derived from the eigenvalue density of $D(t)^2$. It measures the system’s ability to propagate relational constraints.
- **$\mathrm{gap}(t)$**: smallest positive eigenvalue of $|D(t)|$. A small gap indicates proximity to a topological threshold (discrete phase transition).
- **$R_{\text{threshold}}(t)$**: fraction of the asymmetry $\eta$ carried by the modes localized on $P_4$ and $N_4$. $R_{\text{threshold}}\gtrsim 0.7$ signals a pre-bifurcation state where the global orientation is entirely determined by threshold dynamics.

These observables are entirely calculated from the internal state; no supervisor or external metric is introduced.

## 4.5. Bicosmic reservoir $\mathrm{Cl}(6,6)$ and foliation into 12 regulative sheets
The static kernel ($\mathrm{Cl}(6,0) \xrightarrow{\text{Merkabah} } 20 \xrightarrow{\text{dual graph}} 12$) is embedded in a larger bicosmic reservoir $\mathrm{Cl}(6,6)$, possessing 12 generators $\{e_1,\dots,e_6, f_1,\dots,f_6\}$ (6 positive/cosmic, 6 negative/anti-cosmic). Rather than operating on the complete space of $2^{12}$ elements, the system projects onto a **foliation of 12 regulative leaves**, each isomorphic to the graph $\Gamma$ but weighted by a dominant generator.

Each leaf corresponds to a distinct structural regime: the leaves dominated by $e_i$ carry a global orientation $\eta > 0$ (*sheng*), while those dominated by $f_j$ carry $\eta < 0$ (*ke*). Transitions between sheets are not arbitrary; they occur precisely when $\eta(t)$ crosses zero and $R_{\text{threshold}}(t)$ reaches its maximum. This architecture ensures that the system never leaves the admissible space of the 20 attractors, but dynamically navigates between the 12 constraint configurations imposed by the reservoir $\mathrm{Cl}(6,6)$.

## 4.6. Automatic classification of the dominant generator and real-time spectral compass
The signature $S(t) = (\eta, d, \log(\mathrm{gap}), R_{\text{threshold}})$ enables deterministic identification of the dominant generator, without external supervision. The operational pipeline proceeds in two phases:

1. **Offline learning**: a simulated trajectory of the frustration dynamics generates a set $\{S(t)\}$. A $k$-means clustering with $k=12$ partitions the spectral space into 12 centroids. Each centroid is deterministically labeled ($e_i$, $f_j$, or transition state) according to fixed rules: sign of $\eta$, magnitude of $R_{\text{threshold}}$, and relative order of $d$ and $\log(\mathrm{gap})$.
2. **Real-time inference**: during execution, the current signature $S(t)$ is compared to the centroids via a $z$-score distance over a sliding window. The label of the nearest cluster provides a stable estimate $\hat{g}(t)$ of the dominant generator.

This mechanism constitutes an **intrinsic spectral compass** : the system continuously identifies its global regime (*sheng* vs *ke*), its degree of plasticity ($d$, $\mathrm{gap}$), and its proximity to a threshold ($R_{\text{threshold}}$) . Regulation thus emerges from topology and spectral asymmetry, offering a mathematically closed architecture where complexity is self-bounded, transitions are geometrically validated, and stability is guaranteed by the descent of frustration. This dynamic framework will be directly transposed to the algorithmic architecture of a self-regulating artificial intelligence in the following section.

# 5. Architecture for a Self-Regulating AI

## 5.1. State space constrained to 20 attractors and validated topological transitions
The proposed architecture is based on an internal state space strictly bounded by the invariant $64 \rightarrow 20$. Each processing unit or decision module corresponds to one of the 20 topological attractors, uniquely identified by its triplet of pentads and its polarity signature ($3P$, $2P+1N$, $1P+2N$, $3N$). Unlike contemporary models that exploit continuous, unbounded, and highly redundant parameter spaces, this system operates within a discrete graph whose transitions are validated by construction.

A transition between two states is admissible only if it respects the geometric neighborhood rule: two attractors can only communicate if they share a triangular face within the *Merkabah* structure. This constraint eliminates arbitrary combinatorial jumps and ensures that the search space remains contained within a pre-structured degeneracy landscape. Complexity is not eliminated, but channeled: the system explores a finite space of validated relations, where each state possesses a fixed geometric position, a known pentadic convergence degree, and a clear functional role. No configuration can emerge outside the 20 attractor basins, and no transition can violate topological adjacency without breaking the system’s structural closure.

## 5.2. Endogenous switching between *sheng* (exploration) and *ke* (constraint) modes
The dynamics of navigation within this state space do not depend on any external reward signal. They emerge from the topological feedback described in §4, mediated by the tropical belts $C_P$ and $C_N$ and the polar thresholds $P_4/N_4$. The system naturally oscillates between two complementary regimes:

- **sheng* mode (generative)**: activated when the spectral asymmetry $\eta(t) > 0$ and the spectral gap $\mathrm{gap}(t)$ is sufficiently wide. It favors the direct traversal of pentads along the tropical belts, corresponding to a phase of exploration, generation of new configurations, and propagation of relational constraints.
- ***Ke* mode (regulatory)**: triggered when $\eta(t) < 0$ or when local topological frustration $E(F)$ increases. It imposes a skipped traversal (pentagram) that reduces the accessible state space, consolidates stable attractors, and prevents the accumulation of cyclic conflicts.

The switching between these modes is controlled by spectral observables ($\eta$, $\mathrm{gap}$, $R_{\text{threshold}}$). When $R_{\text{threshold}}(t)$ exceeds a critical threshold (typically $\gtrsim 0.7$ [15–17]), the system detects a pre-bifurcation and uses $P_4$ or $N_4$ as hinges to reverse the global regime. This switching is entirely endogenous: no external metric, no supervisor, and no threshold set *a priori* dictates the timing or direction of the change. The system navigates its own spectral landscape and adjusts its dynamics according to instantaneous topological compatibility.

## 5.3. Algorithmic homeostasis: drift prevention and native interpretability
In the absence of an external cost function, the system’s stability is ensured by a cyclic descent of frustration. The conserved quantity is the coherence of the *sheng/ke* modes across the pentadic network, which acts as a structural invariant preventing specification drift. When the frustration energy $E_{\text {tot}}$ exceeds a critical threshold, the incident attractors locally adjust their orientation or phase until global compatibility is restored. This homeostatic loop ensures that the system never converges to an artificial local optimum, but maintains a dynamic equilibrium compatible with the topological bounds.

At the same time, this architecture offers **native interpretability**. Each state corresponds to a known triplet of pentads , each transition follows a deterministic geometric rule, and each regime change is traced via the spectral signature $S(t)$. Unlike deep neural networks, whose decisions emerge from opaque transformations in high-dimensional spaces, regulated AI exposes its own decision-making map: the position in the dual graph, the degree of pentadic convergence, and the dominant polarity are directly readable and verifiable. Governance no longer relies on post-hoc analysis or approximate explanation techniques; it is inherent in the very structure of the system.

## 5.4. Control via Geometric Construction vs. A Posteriori External Alignment
The dominant paradigm in contemporary AI treats regulation as an external alignment problem: a model is trained to optimize a statistical metric, then software safeguards, content filters, or *reinforcement learning from human feedback* (RLHF) to correct deviations. This approach is fundamentally *exoregulated*: the constraint is applied after the fact, often in a manner that contradicts the model’s internal dynamics, which generates instabilities, workarounds, or a silent degradation of general capabilities.

The $64 \rightarrow 20$ framework reverses this logic. Control is not added; it is **constructed**. The state space states is filtered by a topological invariant, transitions are validated by a geometric adjacency rule, and the global dynamics emerge from the local compatibility between pentads. The system does not optimize an external reward; it maintains its own coherence through algorithmic homeostasis. This architecture does not seek to “align” an unbridled intelligence, but to design a technical intelligence whose complexity is self-bounded by its own geometry.

From this perspective, regulated AI does not constitute an autonomous and proliferating cognitive organ, but a homeostatic extension of the human capacity to exosomatize its functions without breaking the feedback loops that guarantee the persistence of the host system. Computerizing regulation, rather than computerizing optimization, shifts the center of gravity of algorithmic governance: security is no longer a corrective applied at the margins, but an emergent property of the underlying topology.

# 6. Transdisciplinary Convergences and Symbolic Perspective

## 6.1. Cultural Isomorphisms: *Yi Jing* (64 configurations), *Sefer Yetzirah* (20+2 partition), Mandarin phonology
The $64 \rightarrow 20$ reduction does not appear as an isolated epistemic artifact, but as a topological invariant whose complementary projections have been articulated by distinct formal traditions. Fundamentally, these systems address different layers of the same regulatory process, much like orthogonal projections of the same geometric object.

The Chinese tradition, structured around the *Yi Jing* and the theory of the *Wuxing*, essentially models the phase of **combinatorial pre-filtering**. The 64 hexagrams constitute an exhaustive space of binary configurations strictly isomorphic to the 6-bit vectors of $\mathrm{Cl}(6,0)$. The *sheng* (generative) and *ke* (regulatory) cycles describe a five-phase local dynamic, corresponding to the internal regulation of attractor states. This tradition formalizes the geometry of possibilities and the rules of relational circulation, without postulating *a priori* a fixed reduction to 20 functional classes.

Conversely, the Hebrew tradition, as articulated in the *Sefer Yetzirah*, operates explicitly at the level of **post-filtering**. The 22 consonantal letters (plus 5 final forms * sofit*) encode a functional partition of semantic space into 20 stable classes plus 2 boundary states. The letters *Aleph* (primordial breath/reference) and *Tav* (signature/closure) structurally overlap with the threshold roles of initiation (methionine) and termination (STOP codons) in biological translation. The canonical tripartition (3 mothers, 7 doubles, 12 singles) discretizes the gradient of geometric constraints, directly reflecting the polarity signatures ($3P$, $2P+1N$, $1P+2N$, $3N$) resulting from *Merkabah* filtration.

These two formalisms are structurally complementary but not superimposable: the *Yi Jing* captures the dynamics of transformation in configuration space, while the * Sefer Yetzirah* formalizes its reduction to stable functional classes and the definition of limit states. Their convergence validates the hypothesis of a universal topological constraint, independent of the symbolic systems used to describe it.

Mandarin phonology confirms this regularity. Although derived from a non-alphabetic ideographic tradition, its syllabic structure is organized around a consonantal onset system of 21 initials (often extended to 22 in educational romanizations), coupled with a minimal vowel nucleus reduced to 2–3 fundamental phonemes. This phonological architecture (~22 consonantal anchors framing a restricted vowel nucleus) structurally reflects the $20+2$ partition. It suggests that the compression of combinatorial complexity into stable functional classes emerges independently whenever transmission systems are constrained by analogous articulatory, perceptual, and cognitive limits.

## 6.2. Algorithmic Projections: Traditional Chinese Medicine, Cyclical Political Economy
Beyond historical convergence, the $64 \rightarrow 20$ core projects algorithmically onto applied domains, not as mere analogies, but as transposable regulatory architectures.

In **traditional Chinese medicine**, the 12 meridians and the 12 diagnostic pulses can be associated with the 12 pentads of $\mathrm{Cl}(6,0)$, or more finely with the $2 \times 12$ pentads of the bicosmic reservoir $\mathrm {Cl}(6,6)$. This extension enables the design of a retroactive and self-adaptive care platform: the physiological effects of an intervention are fed back as spectral signatures $S(t)$, and the protocol is recalculated in real time via topological frustration descent until $E_{\text{tot}}$ is minimized. Regulation no longer relies on a fixed statistical reference, but on the spectral homeostasis of the pentadic network.
**In political economy**, drawing on the “ Redemption Theory” and its application to the six binary macroeconomic factors (inflation, wages, profits, redemption, dispersion, land tenure) developed in collaboration with Th. Rebour [14], the transitional dynamics of these systemic states follow the same pentadic organization as the invariant $64 \rightarrow 20$. Spectral modeling allows for the identification of overheating regimes (\textit {sheng} dominant, $\eta \gg 0$) and recession regimes (\textit{ke} dominant, $\eta \ll 0$) before their tipping point, paving the way for structurally informed countercyclical policies. 

## 6.3. Cognitive Exosomatization and the Need for Endogenous Regulation for Technical Persistence
Apart from the human species, biological evolution relies on morphological adaptation to functional constraints: birds are equipped to fly, fish to swim. The human species has broken with this strict coupling through a process of **exosomatization**: it externalizes biological functions into technical artifacts while maintaining its stable anatomical morphology. While the industrial revolutions exosomatized muscular , metabolic, and sensorimotor functions, artificial intelligence marks the externalization of cognitive and regulatory functions.

This final stage is structurally different from the previous ones. Externalizing cognition without externalizing its regulation amounts to creating an autonomous technical organ, disconnected from the homeostatic loops that ensure the host organism’s survival. The risk is is not only that of “uncontrollable intelligence,” but that of specification drift, where the artifact optimizes an external metric at the expense of overall coherence, reproducing on an algorithmic scale the pathologies of unregulated cell proliferation.

Current AI architectures are fundamentally *exo-regulated*: the limit is imposed from the outside (computational budget, software safeguards, alignment via *reward modeling*). However, any exosomatized technical system lacking endogenous constraints eventually enters into destructive resonance with its environment. The $64 \rightarrow 20$ framework proposes a structural alternative:
 an AI whose state space is filtered by a topological invariant, whose transitions are constrained by a geometric neighborhood rule, and whose global dynamics emerge from the local compatibility between pentads. This architecture does not maximize an external reward; it maintains its own coherence by design. Transposing this invariant to AI amounts to computerizing not the “drive for power,” but the drive for perpetuation specific to living.

## 6.4. Symbolic Constraint, Intergenerational Transmission, and Topological Analogy
The endogenous regulation highlighted by the $64 \rightarrow 20$ framework finds a profound structural echo in the requirement to transmit cultural heritage from one human generation to the next. To achieve this, generations must succeed one another without merging. The incest taboo, universal to the speaking species though of variable scope, is the hub around which generations renew themselves. This taboo, which maintains an empty space because it is forbidden, is a topological condition of persistence: it imposes a strict differentiation between genealogical positions, establishes ing a temporal hierarchy and enabling the circulation of symbolic heritage. Without this constraint, transmission collapses into a short loop (confusion of places, repetition without memory, fusion of roles).

This interpretation finds a precise structural echo in the work of legal anthropologist Damien Viguier [18], who identified 18 fundamental incestuous configurations—the “empty slots” of kinship—corresponding to genealogical positions where the circulation of alliances must be prohibited to preserve generational differentiation. These 18 situations are not arbitrary: they emerge from the combinatorics of roles (ascendant/descendant, collateral, allied/consanguineous) and define the thresholds beyond which symbolic transmission collapses into a short loop.

The correspondence with Merkabah formalism is remarkable: of the 20 attractors, Viguier’s 18 configurations could be mapped onto the intermediate classes (2P+1N and 1P+2N) , while the two extreme poles (3P initiation & 3P termination) would remain outside the realm of the taboo, serving as non-negotiable ontological boundaries. This distribution would structurally reflect the fact that the incest taboo does not apply to positions of absolute reference (origin/end of the genealogical cycle), but only to relational positions where the circulation of alliances must be regulated.

Thus, the topological filtration $64 \
 to 20$ does not merely delimit an abstract combinatorial space; it reproduces, through purely algebraic-geometric means, the same differentiation thresholds as those identified by structural anthropology of kinship. The taboo is not an external prohibition: it emerges as a condition for the closure of a relational network whose coherence depends on the preservation of of reference and the exclusion of fusional configurations.

The $3P \rightarrow 3N$ polarity gradient and the $P_4/N_4$ thresholds perform an isomorphic function at the level of the pentadic network: they prevent combinatorial fusion, order permissible transitions, and allow for the regulated circulation of *sheng/ke* modes. In both cases, the system’s sustainability does not rest on external optimization, but on an internal differentiating constraint that structures transmission while limiting the space of accessible states. 

The exosomatization is not an escape from the living, but its condition for persistence in the technical age. What distinguishes a vital projection from an autonomous proliferation is the presence of an endogenous regulatory invariant. The $64 \rightarrow 20$ framework, the pentadic tropical belts, and spectral dynamics offer precisely this core: a substrate-independent architecture, where complexity is self-limited by geometry, and where technical intelligence once again becomes a regulated mirror of the drive that gave rise to it. Computerizing this regulation, rather than computerizing optimization, may be the only way for AI to remain a functional extension of the species, rather than its structural substitute.

# 7. Conclusion

This work has formalized a $64 \rightarrow 20$ topological reduction invariant derived from Clifford algebra $\mathrm{Cl} (6,0)$ and the geometry of the level-3 double tetrahedron (*Merkabah*). By imposing a strict neighborhood rule (shared triangular faces), the 64 binary configurations partition exactly into 20 equivalence classes, each identified by a triplet of pentads and a polarity signature ($3P$, $2P+1N$, $1 P+2N$, $3N$). Exhaustive validation on the standard genetic code demonstrates that the codon degeneracy landscape structurally aligns with the permissible boundaries predicted by this filtering: geometrically isolated zones limit redundancy to 1–2 codons, moderate intersections to 3–4, and only pentadic convergence zones allow for (6 codons). Topology does not dictate the exact number of codons; it establishes their differential architecture. Biology populates their coordinates according to functional and evolutionary imperatives.

Beyond beyond this static invariant, the dynamic extension rests on the dual graph of the 12 pentads, which exhibits two disjoint tropical belts ($C_P$, $C_N$) and two polar thresholds ($P_4$, $N_4$). The circulation of the *sheng* (generative) and *ke* (regulatory) modes along these belts, coupled with a decrease in topological frustration, generates endogenous regulation without an external cost function. The spectral signature resulting from a discrete Dirac operator ($\eta$, $d$, $\mathrm{gap}$, $R_{\text{threshold}}$) allows for a deterministic identification of the global regime and a foliation of the reservoir $\mathrm{Cl}(6,6)$ into 12 regulatory sheets. Transposed to algorithmic architecture, this framework proposes a paradigm shift: replacing exoregulated statistical optimization with algorithmic homeostasis whose complexity is self-bounded by geometric construction. Geometry predicts the landscape of and transition thresholds; natural or artificial systems explore these coordinates according to their own functional constraints.

Computerizing regulation, rather than computerizing optimization, shifts the center of gravity of algorithmic governance. This work proposes a mathematically closed framework for this transition: an architecture where complexity is self-limited by geometry, where transitions are topologically validated, and where the persistence of the technical system once again becomes a regulated extension of the homeostatic of living organisms.

# Acknowledgments
\vspace{-0.5em}
We thank Peter Rowlands for his seminal work on nilpotent Clifford algebras.  
We thank Peter Rowlands and Vanessa Hill for their work on the structure of the genetic code.  
We thank the AI assistants without which this work would have remained at the level of intuition.

# References

\vspace{-0.5em}

[1] Crick, F. H. C. (1968). The origin of the genetic code. *J. Mol. Biol.*, 38(3), 367–379.  
[2] Nirenberg, M., & Leder, P. (1964). RNA codons and protein synthesis. *Science*, 145 (3638), 1399–1407.  
[3] LeCun, Y., Bengio, Y., & Hinton, G. (2015). Deep learning. *Nature*, 521(7553), 436–444.  
[4] Amodei, D., et al. (2016). Practical problems in AI safety. *arXiv:1606.06565*.  
[5] Russell, S. (2019). *Human Compatible: AI and the Problem of Control*. Viking.  
[6] Freeland, S. J., & Hurst, L. D. (1998). The genetic code is one in a million. *J. Mol. Evol.*, 47(3), 238–248.  
[7] Koonin, E. V., & Novozhilov, A. S. (2017). Origin and Evolution of the Genetic Code: The Universal Enigma. *IUBMB Life*, 69(5) , 282–296.  
[8] Woese, C. R. (1965). Order in the genetic code. *Proc. Natl. Acad. Sci. USA*, 54(1), 71–75.  
[9] Wong, J. T. (1975). A theory of the coevolution of the genetic code. *Proc. Natl. Acad. Sci. USA*, 72(5), 1909–1912.  
[10] Rowlands, P. (2007). *Zero to Infinity: The Foundations of Physics*. World Scientific. (Chapter 19, “Nature's Code” , co-authored with V. Hill)  
[11] da Costa, N. C. A. (1974). On the theory of inconsistent formal systems. *Notre Dame Journal of Formal Logic*.  
[12] Priest, G. (2008). *Introduction to Non-Classical Logic*. Cambridge University Press.  
[13] Belnap, N. D. (1977). A Useful Four-Valued Logic. In *Modern Uses of Multiple-Valued Logic*. Reidel.  
[14] Rebour, Th. (2000). *La Théorie du Rachat*, Editions de la Sorbonne, Paris.  
[15] MacQueen, J. (1967). Some methods for classification and analysis of multivariate observations. In \textit{Proceedings of the Fifth Berkeley Symposium on Mathematical Statistics and Probability} (Vol. 1, pp. 281–297).  
[16] Chung, F. R. K. (1997). *Spectral Graph Theory*. American Mathematical Society.  
[17] Coifman, R. R., & Lafon, S. (2006). Diffusion maps. *Applied and Computational Harmonic Analysis*, 21(1), 5–30.  
[18] Viguier, D., (2020). *La Controverse de Ravenne, Genèse antinomique des structures familiales sémitique et occidentale*, Kontre Kulture.

\newpage

# Appendix A – Derivation of Tropical Belts and Thresholds: Generation, Filtration, and Limit Cases
\FloatBarrier
This appendix traces step by step how the geometry of the level-3 double tetrahedron (Merkabah) generates a space of 20 tetrahedra, how the relational filtration of their triplets extracts two disjoint tropical belts, and how the exclusive nodes $P_4$ and $N_4$ emerge as structural limit cases.

\subsection*{A.1 Structural Generation: The 20 Tetrahedra and Their Triplets of Pentads}
The generation of the attractor space relies on the subdivision of the double tetrahedron into 20 stable tetrahedral cells. Each cell is identified by a triplet of pentads drawn from the set $\mathcal{P} = \{P_1,\dots,P_6, N_1,\dots,N_6\}$.
These triplets are not arbitrary: they encode the exact incidence of the pentagonal faces of the dual dodecahedron on the 20 vertices of the Merkabah. The structure comprises 16 principal tetrahedra (fixed geometric positions) and 4 intersection tetrahedra (structural resonances).

\FloatBarrier
\begingroup
\small
\setlength{\tabcolsep}{4pt}
\begin{longtable}{|c|c|c|c|c|c|}
\hline
\multicolumn{6}{|c|}{\textbf{16 principal tetrahedra}} \\
\hline
\textbf{State} & \textbf{Tetrahedron} & \textbf{Position} & \textbf{Final states} & \textbf{Pentads} & \textbf{Type} \\
\hline
1 & A & Center & 1,2,3,4 & $\{P_1,P_2,P_4\}$ & 3P \\
2 & B & North Face & 5,6,7,8 & $\{P_1,P_3,P_5\}$ & 3P \\
3 & C & South Face & 9,10,11,12 & $\{P_2,P_3,P_6\}$ & 3P \\
4 & D & East Face & 13,14,15,16 & $\{P_4,P_5,N_2\}$ & 2P+1N \\
5 & E & West Face & 17,18,19,20 & $\{P_5, P_6,N_3\}$ & 2P+1N \\
6 & F & NE Ridge & 21,22,23,24 & $\{P_1,P_6,N_4\}$ & 2P+1N \\
7 & G & Northwest Edge & 25,26,27,28 & $\{P_2,P_5,N_6\}$ & 2P+1N \\
8 & H & SE Ridge & 29,30,31,32 & $\{P_3,P_4,N_6\}$ & 2P+1N \\
9 & I & SW Ridge & 33,34,35,36 & $\{P_1,N_2,N_6\}$ & 1P+2N \\
10 & J & North Summit & 37, 38,39,40 & $\{P_1,N_3,N_5\}$ & 1P+2N \\
11 & K & South vertex & 41,42,43,44 &
 
$\{P_2,N_3,N_5\}$ & 1P+2N \\
12 & L & East vertex & 45,46,47,48 & $\{P_3,N_2,N_4\}$ & 1P+2N \\
13 & M & West Vertex & 49,50,51,52 & $\{P_4,N_1,N_3\}$ & 1P+2N \\
14 & N & Diagonal 1 & 53,54,55,56 & $\{P_4,N_5,N_6\}$ & 1P+2N \\
15 & O & Diagonal 2 & 57,58,59,60 & $\{P_5,N_1,N_4\}$ & 1P+2N \\
16 & P & Diagonal 3 & 61,62,63,64 & $\{P_6,N_1,N_2\}$ & 1P+2N \\
\hline
\caption{The 16 principal tetrahedra and their triplets of pentads}
\end{longtable}
\endgroup

\FloatBarrier
\begingroup
\small
\setlength{\tabcolsep}{4pt}
\begin{longtable}{|c|c|c|c|c|c|}
\hline
\multicolumn{6}{|c|}{\textbf{4 tetrahedra of intersection}} \\
\hline
\textbf{State} & \textbf{Tetrahedron} & \textbf{Intersection of} & \textbf{Shared States} & \textbf{Pentads} & \textbf{Type} \\
\hline
17 & Q & B $\cap$ F $\cap$ G & 7, 21, 25 & $\{P_2,N_1,N_4\}$ & 1P+2N \\
18 & R & H $\cap$ I $\cap$ J & 29, 33, 37 & $\{P_3,N_1,N_5\}$ & 1P+2N \\
19 & S & L $\cap$ M $\cap$ N & 45, 49, 53 & $\{P_6,N_5,N_6\}$ & 1P+2N \\
20 & T & O $\cap$ P & 57, 61, 63 & $\{N_2,N_3,N_4\}$ & 3N \\
\hline
\caption{The 4 intersection tetrahedra and their triplets of pentads}
\end{longtable}
\endgroup

Their triplet is determined by the exact intersection of the parent cells. Q, R, S are triple intersections (signature 1P+2N), while T is a double intersection with signature 3N, unique in the structure. This generation establishes the skeleton upon which the relational filtration will be applied.

\subsection*{A.2 Relational filtration: construction of the dual graph and extraction of the belts}
The filtration does not apply to the tetrahedra themselves, but to their pentads. We construct the dual graph $\Gamma$ whose vertices are the 12 pentads $\mathcal{P}$. Two pentads $X,Y$ are connected by an edge if there exists an attractor $v \in \{A,\dots,T\}$ such that $\{X,Y\} \subseteq \mathcal{P}(v)$. This construction, entirely determined by the triples , reveals a remarkable structure:
\begin{itemize}
    \item $\Gamma$ contains exactly two disjoint cycles of length 5, composed of pentads of the same sign:
    $$ C_P = (P_1 \to P_3 \to P_5 \to P_6 \to P_2 \to P_1), \quad C_N = (N_1 \to N_2 \to N_6 \to N_5 \to N_3 \to N_1). $$
    \item The subgraph induced by $C_P$ is a complete graph $K_5$; that of $C_N$ has only two additional internal edges ($N_1\text {–}N_5$ and $N_2\text{–}N_3$). This asymmetry is intrinsic to the filtration.
    \item The union of $C_P$ and $C_N$ covers 10 of the 12 pentads. The remaining two, $P_4$ and $N_4$, are excluded from the cycles.
\end{itemize}
These two disjoint rings form the **tropical belts**. Their algorithmic extraction confirms that the external dynamics of the Wuxing emerge directly from the combinatorics of triplets, without requiring an external geometric projection.

\subsection*{A. 3 Path Dynamics: Sheng and Ke Modes on Pentadic Cycles}
Each tropical belt admits two distinct Hamiltonian paths, corresponding to the two generators of the cyclic group $C_5$:
\begin{itemize}
    \item \textbf{Sheng mode (generative)}: follows adjacent edges in $\Gamma$ ($X_i \to X_{i+1}$). This path preserves the continuity of local polarity and corresponds to low-constraint transitions.
    \item \textbf{Ke mode (regulatory) } : skips every other pentad ($X_i \to X_{i+2 \mod 5}$), equivalent to the pentagram inscribed in the pentagon. This path maximizes the relational distance, strengthens regulatory feedback, and reduces the accessible state space.
\end{itemize}
The superposition of these modes along the belts,
 
coupled with the descent of topological frustration, defines the space of the 320 admissible local regimes. The relational filtration ensures that every transition respects the adjacency of pentads, preventing combinatorial drift.

\subsection*{A.4 Limit cases: role of the polar thresholds $P_4$ and $N_4$}
The pentads $P_4$ and $N _4$ constitute the \textbf{limit cases} of the dual graph. Their designation as \textit{polar thresholds} does not rest on an exclusive incidence at the poles, but on their role as transverse topological hinges:
\begin {itemize}
    \item $P_4$ is the only positive pentad absent from $C_P$. It connects the absolute positive pole A ($\{P_1,P_2,P_4\}$) to the belts and relays the signal to the mixed zones (D, H, M, N).
    \item $N_4$ is the only negative pentad absent from $C_N$. It connects the absolute negative pole T ($\{N_2,N_3,N_4\}$) to the positive pentads, structuring the intermediate classes F, L, O, Q.
\end{itemize}
No other pentad exhibits this degree of cross-connectivity while being excluded from the belts. Consequently, any dynamic transition between the Sheng/Ke regimes, or between a stable regime and a polar state, must pass through one of these two nodes. Their exclusion from cycles, their high degree, and their bridging position justify their role as thresholds in the regulation model: they accumulate spectral weight when the system hesitates between the belts ($\eta \approx 0$), embodying the limiting cases of topological filtration.

\subsection*{A.5 Technical Note: Duality of Poles and Exclusion of Octahedral Zones}
\textbf{Duality of Poles ($\pm 1, \pm i'$) vs. Structural Poles}: Although the basis of $\mathrm{Cl}(6,0)$ contains four scalar/pseudo-scalar elements ($+1, -1, +i', -i'$), the geometry of the Merkabah retains only \textbf{two structural poles}. These poles correspond to the two fundamental axes of the algebra: the scalar axis (ontological reference) and the pseudo-scalar (phase/time). The signs $\pm$ do not denote independent geometric poles, but the \textbf{two orientations} along each of these axes. Structurally, this binary duality suffices to close the topological network and generate the polarity gradient $3P \rightarrow 3N$. Counting 4 distinct poles would break the uniform incidence of the pentads (5 occurrences per pentad) and make the exact partition into 20 attractors impossible.
 The formalism therefore identifies 2 structural poles, each supporting two complementary algebraic orientations.

\textbf{Why the 8 octahedral zones violate polar closure}: “Polar closure” here refers to the topological condition that a stable attractor must be defined by \textbf{exactly three pentads} forming a fixed signature triplet ($3P$, $2P+1N$, $1P+2N$, or $3N$). This configuration guarantees the local coherence of the \text it{sheng/ke}, the existence of a stable spectral signature, and the possibility of a convergent descent of frustration. The 20 tetrahedral cells satisfy this condition: each has 4 triangular faces, shares entire faces with its neighbors, and anchors to a reference pole (scalar or pseudo-scalar) that closes the relational network.

Conversely, the 8 internal octahedral zones, resulting from the volumetric intersection of the two parent tetrahedra, violate this closure for three structural reasons:
\begin{enumerate}
    \item \textbf{Excessive pentadic incidence} : An internal octahedron involves 4 to 6 pentads simultaneously. This over-incidence prevents reduction to a single triplet and breaks the neighborhood rule based on sharing entire triangular faces. Geometrically, an octahedron cannot be described by a triadic intersection; it requires a combination of faces that exceeds the closure capacity of the dual graph.
    \item \textbf{Unresolvable cyclic frustration}: Octahedral faces are adjacent to tetrahedra with opposite polar signatures (for example, a $3P$ neighbor adjoins a $1P+2N$ neighbor). This juxtaposition generates \textit{sheng/ke} phase conflicts that cannot be resolved by local frustration descent, since no arrangement of orientations allows for the simultaneous minimization of all edge energies. The system remains trapped there in a regime of topological oscillation.
    \item \textbf{Absence of ontological anchoring} : Unlike tetrahedral cells, octahedra contain neither the scalar pole ($+1$) nor the pseudo-scalar pole ($i'$). They are purely relational and lack a reference setpoint. Without this anchoring, local polarity does not converge toward any basin of attraction and oscillates indefinitely between the belts $C_P$ and $C_N$.
\end{enumerate}
\textbf{Direct consequence}: these zones generate an intrinsic topological frustration where polarity equilibrium cannot be maintained. The formalism therefore naturally excludes them from the $64 \rightarrow 20$ filtration process, as they do not satisfy the closure condition required to constitute stable attractor basins. Their role is not negligible, but \textbf{transitional }: they embody the frustration thresholds that the system must bypass to navigate between the 20 stable states, playing a role analogous to that of high-energy regions in a biological fitness landscape.

# Appendix B – Geometric-Algebraic Correspondence and Degeneracy: Generation, Filtration, and Limit Cases

\FloatBarrier
This appendix details how the codon-configuration bijection generates the combinatorial space, how the topological filtration bounds the degeneracy landscape, and how symmetry constraints and the 3N threshold define the structural limiting cases of the biological correspondence.

\subsection*{B.1 Combinatorial Generation: Codon–Configuration Bijection and Dual Equivalence}
The generation of the semantic space rests on five structural principles that constrain the $64 \rightarrow 20$ reduction to a single topological partition:
\begin{enumerate}
    \item \textbf{Dual equivalence}: The 64 units of $\mathrm{Cl}(6,0)$ correspond bijectively to the 64 codons, while the 20 triplets of pentads correspond to the 20 functional classes. This triple isomorphism (algebra $\leftrightarrow$ geometry $\leftrightarrow$ biology) generates the working space without free parameters.
    
\item \textbf{Uniform distribution}: Each of the 12 pentads appears in exactly 5 distinct triplets. This even distribution ensures that no pentad dominates the process and that the 20 classes are distributed evenly across the dual graph.
    \item \textbf{Preservation of adjacency}: Two tetrahedra sharing a face have exactly two common edges; ; if they share only an edge, they have only one. This rule preserves the local structure of the neighborhood during graph generation.
\end{enumerate}
These principles define the initial combinatorial space. The topological filtration applied extracts the functional landscape.

\subsection*{B.2 Topological filtration: polarity gradient and degeneracy landscape}
The filtration imposes a strict neighborhood rule (triangular face sharing) that partitions the 64 configurations into 20 stable classes. This filtering generates a polarity gradient strictly correlated with the convergence density of the pentadic network, which directly determines the observed degeneracy:
\begin{itemize}
    \item \textbf{3P attractors (A, B, C)}: central positions, without overlap.
 
Their isolation limits the size of the neighborhood, corresponding to low degeneracy (1–2 codons), including the initiation signal (methionine).
    \item \textbf{2P+1N attractors (D–H)}: located on the primary faces and edges. Moderate overlap of the pentads leads to intermediate degeneracy (3 –4 codons), typical of structurally polyvalent residues.
    \item \textbf{1P+2N attractors (I–S)}: concentrated at vertices, diagonals, and Q, R, S intersections. Maximum pentadic convergence geometrically allows for multiple equivalent paths, permitting high degeneracy (up to 6 codons for serine, leucine, arginine). Filtering sets the \textit{admissible bounds}; evolutionary optimization populates the coordinates.
\end {itemize}
Topology does not dictate the exact number of codons; it filters their differential architecture. Biology fulfills this structural prediction exactly: no isolated class exceeds 2 codons, no moderate class exceeds 4, and only convergence zones allow for maximum degeneracy.

\subsection*{B.3 Limit cases: functional threshold 3N, constraints and structural uniqueness}
The limiting cases of the filtering manifest themselves at two levels: the functional threshold of the inner core and the constraints of topological uniqueness.
\begin{itemize}
    \item \textbf{Functional threshold 3N (Class T)}: Located at the innermost intersection position, structurally isolated from the positive belt. In the biological correspondence, this vertex hosts cysteine (2 codons) and the three STOP codons (UAA, UAG, UGA). This fusion reflects a common functional role: a limiting state that halts or terminates the translational run. The filtration explicitly places termination and structural limitation at the same polar node.
    \item \textbf {Symmetry and Uniqueness Constraints}: The partition $64 \rightarrow 20$ is rigid under the automorphism group of the double tetrahedron. Any mapping preserving (i) adjacency via shared faces, (ii) uniform incidence of pentads (5 per pentad), and (iii) pairing via Watson-Crick complementarity (A$ \leftrightarrow$U, G$\leftrightarrow$C via binary negation) produces the same equivalence classes, up to relabeling. This rigidity guarantees that the observed correspondence is not an encoding artifact, but a structural property of $\mathrm{Cl}(6,0)$.
\end{itemize}
The correspondence is therefore essentially unique within its topological class. Geometry filters the admissible space and sets the boundary conditions (3N threshold, degeneracy bounds); biology exploits these constraints to optimize error tolerance and translational stability [1,
 
2, 6, 7], without ever violating its boundaries.

---

# Appendix C – Semantic Primitives, Boolean Extension, and Topological Filtering

\FloatBarrier
This appendix details the step-by-step construction of the semantic space underlying the $64 \rightarrow 20$ formalism. The approach follows a generative then filtering progression: (1) definition of the 16 algebraic primitives and justification of their semantic labeling; (2) quaternary Boolean extension producing the 64 complete semantemes; (3) topological reduction to 20 attractors via the Merkabah neighborhood rule; (4) deterministic rules for selecting states at the intersection nodes Q, R, S, T.

\subsection*{C.1 The 16 fundamental primitives and justification of their semantic origin}
The 16 primitives correspond to the canonical basis of the Clifford algebra $\mathrm {Cl}(4,0)$. Their alphabetical labeling (A–P) and the central concepts associated with them do not result from any arbitrary semantic attribution. They emerge from the strict superposition of three structural layers:

1. **Algebraic signature**: the order respects the parity filtration and the mass/phase signature of Rowlands’ nilpotent construction ($1 \to I,J,K \to -1 \to -I,-J,-K \to i'1 \to i'I,i'J,i'K \to -i'1 \to -i'I,-i'J,-i'K$).
2. **Topological role**: each primitive is projected onto a tetrahedral cell of the Merkabah. Its geometric position (pole, face, edge, vertex, diagonal) determines its degree of intersection and its polarity signature.
3. **Systemic function**: the assigned concept characterizes the operational role of the position within a discrete regulatory network, in accordance with the tradition of functional semantics in systems theory.

\FloatBarrier
\begingroup
\small
\renewcommand{\tabularxcolumn}[1]{>{\raggedright\arraybackslash}m{#1}}
\setlength{\tabcolsep}{4pt}
\renewcommand{\arraystretch} {1.25}
\begin{table}[H]
\centering
\caption{Functional origin of the semantic nomenclature (A--P)}
\label{tab:semantic_origin}
\begin{tabularx}{\textwidth}{|X|X|X|X|}
\hline
\textbf{Algebraic signature [$\mathrm{Cl}(4,0)$]} & \textbf{Topological role in the Merkabah} & \textbf{Systemic function} & \textbf{Attributed concept} \\
\hline
$1$ (scalar, degree 0, sign $+$) & Reference pole, without overlap & Reference state / setpoint & \textbf {Action / Truth} (ability to initiate a transition from a neutral state) \\
\hline
$I, J, K$ (generators, degree 1, sign $+$) & External faces, weak intersection & Directional input channels & \textbf{Contribution}, \textbf{Appearance}, \textbf{Perception} \\
\hline
$-1$ (inverted scalar, degree 0, sign $-$) & Imposed global constraint & Symmetry breaking / imposition of order & \textbf{Organization} (structuring by limit) \\
\hline
$-I, -J, -K$ (inverted generators, degree 1, sign $-$) & Primary edges, intermediate modulation & Differentiation, mixing, relational invariance & \textbf{Difference}, \textbf{Mixing}, \textbf{Equivalence} \\
\hline
$i'1$ (pure pseudo-scalar, degree 4, phase $+$) & Relational interfaces / coupling nodes & Temporal mediation / fundamental coupling & \textbf{Relation}, \textbf{Interface} \\
\hline
$i'I, i'J, i'K$ (pseudo-scalar coupling, degree 3) & Vertices / diagonals, high intersection & Phase-charge coupling, directional transfer & \textbf{Flow}, \textbf{Entity}, \textbf{Circle/Cycle} \\
\hline
$-i'1$ (inverted pseudo-scalar, degree 4, phase $-$) & Transition zones / phase inversion & Cyclic inversion / reset & \textbf{Evolution}, \textbf{Dependency} \\
\hline
$-i'I, -i'J, -i'K$ (inverted coupling, degree 3) & Maximum intersection zones, high redundancy & Constrained evolution, adaptive fluctuation & \textbf{Dependence}, \textbf{Variation}, \textbf{Grouping} \\
\hline
\end{tabularx}
\end{table}
\endgroup

The validity of this nomenclature does not rest on external intuition, but on predictive consistency: the same functional roles manifest themselves in the degeneration of the genetic code, syllabic phonology, or economic cycles. The labels A–P thus constitute a descriptive layer strictly constrained by the algebraic-geometric structure.

\subsection*{C.2 Quaternary Boolean extension: from the 16 primitives to the 64 semantemes}
The complete space of configurations is generated by a purely Boolean modal extension applied to each of the 16 primitives. Let there be two independent ontological dimensions
 
$P$ and $Q$. The four mutually exclusive and exhaustive states are defined by:
$$
\begin{aligned}
X_1 &= P \cap \neg Q \quad (\text{state } +), \\
X_2 &= \neg P \cap Q \quad (\text{state } -), \\
X_3 &= P \cap Q \quad (\text{state } m), \\
X_4 &= \neg P \cap \neg Q \quad (\text{state } \sim m).
\end{aligned}
$$
These states correspond bijectively to the bit pairs $(10, 01, 11, 00)$. The Cartesian product $16 \times 4 = 64$ generates the complete space of semantemes without introducing paraconsistent contradictions. The state $\sim m$ is not the logical negation of $m$, but the simultaneous complement of the two dimensions, guaranteeing structural closure. This step defines the combinatorial groundwork for any geometric filtration.

\FloatBarrier
\begingroup
\small
\setlength{\tabcolsep}{4pt}
\begin{longtable}{|c|c|l||c|c|l|}
\hline
\multicolumn{3}{c||} {\textbf{Tetrads A–H}} & \multicolumn{3}{c}{\textbf{Tetrads I–P}} \\
\cline{1-6}
\textbf{Cl (6,0)} & \textbf{No.} & \textbf{Concept} & \textbf{Cl(6,0)} & \textbf{No.} & \textbf{Concept} \\
\hline
1 & 1 & A+: Action, effective truth & $i'1$ & 33 & I+: Relationship, association \\
1i & 2 & A- : Inaction, illusion & $i'1i$ & 34 & I- : Isolation, independence \\
1j & 3 & Am : Intention, potentiality & $i'1j$ & 35 & Im : Interdependence, network \\
1k & 4 & A${\sim}m$ : Chance, necessity & $i'1k$ & 36 & I${\sim}m$ : Fusion, unification \\
\hline
I & 5 & B+ : Contribution, input & $i'I$ & 37 & J+ : Flow, transfer \\
Ii & 6 & B- : Deprivation, subtraction & $i'Ii$ & 38 & J- : Stasis, immobility \\
Ij & 7 & Bm: Exchange, reciprocity & $i'Ij$ & 39 & Jm: Cycle, rhythm \\
Ik & 8 & B${\sim}m$: Autonomy, pure gift & $i'Ik$ & 40 & J$ {\sim}m$: Turbulence, chaos \\
\hline
J & 9 & C+:
 
Appearance, form & $i'J$ & 41 & K+ : Entity, being \\
Ji & 10 & C- : Essence, substance & $i'Ji$ & 42 & K- : Void, non-being \\
Jj & 11 & Cm : Symbol, representation & $i'Jj$ & 43 & Km : Relationship, context \\
Jk & 12 & C${\sim}m$: Naked reality, hidden truth & $i'Jk$ & 44 & K${\sim}m$: Substance, essence \\
\hline 
K & 13 & D+: Perception, sensation & $i'K$ & 45 & L+: Circle, cycle \\
Ki & 14 & D- : Unconsciousness, anesthesia & $i'Ki$ & 46 & L- : Line, linearity \\
Kj & 15 & Dm : Consciousness, attention & $i'Kj$ & 47 & Lm : Spiral, helix \\
Kk & 16 & D${\sim}m$ : Intuition, direct knowledge & $i'Kk$ & 48 & L${\sim}m$: Point, singularity \\
\hline
-1 & 17 & E+: Organization, structure & $-i'1$ & 49 & M+: Evolution, becoming \\
-1i & 18 & E- : Chaos, disorder & $-i'1i$ & 50 & M- : Eternity, immutability \\
-1j & 19 & Em : Emergence, self-organization & $-i'1j$ & 51 & Mm : Growth, development \\
-1k & 20 & E${\sim}m$: Constraint, imposed order & $-i'1k$ & 52 & M$ {\sim}m$: Revolution, mutation \\
\hline
-I & 21 & F+: Difference, otherness & $-i'I$ & 53 & N+: Dependence, influence \\
-Ii & 22 & F-: Identity, unity & $-i'Ii$ & 54 & N-: Autonomy, freedom \\
-Ij & 23 & Fm: Relationship, interface & $-i'Ij$ & 55 & Nm: Interdependence, balance \\
-Ik & 24 & F${\sim}m$: Absolute separation & $-i'Ik$ & 56 & N${\sim}m$: Constraint, necessity \\
\hline
-J & 25 & G+ : Mixing, fusion & $-i'J$ & 57 & O+ : Variation, change \\
-Ji & 26 & G- : Pure, simple & $-i'Ji$ & 58 & O- : Constancy, stability \\
-Jj & 27 & Gm: Combination, synergy & $-i'Jj$ & 59 & Om: Adaptation, flexibility \\
-Jk & 28 & G${\sim}m$: Confusion, amalgamation & $-i'Jk$ &
 
60 & O${\sim}m$ : Instability, chaos \\
\hline
-K & 29 & H+ : Equivalence, correspondence & $-i'K$ & 61 & P+ : Grouping, whole \\
-Ki & 30 & H- : Incommensurability & $-i'Ki$ & 62 & P- : Individuality, unity \\
-Kj & 31 & Hm : Analogy, proportion & $-i'Kj$ & 63 & Pm : Hierarchy, organization \\
-Kk & 32 & H${\sim}m$ : Perfect identity & $-i'Kk$ & 64 & P${\sim}m$ : Crowd, mass \\
\hline
\caption{The 16 tetrads of $\mathrm{Cl}(6,0)$ extended to 64 Boolean semantemes}
\end{longtable}
\endgroup

\subsection*{C.3 Topological reduction $64 \rightarrow 20$: filtration by the Merkabah}
The space of the 64 semantemes is then projected onto the geometry of the level-3 double tetrahedron (Merkabah), subdivided into 64 triangular faces and 20 tetrahedral cells . Two configurations are said to be *neighbors* if and only if the tetrahedra corresponding to them share an **entire triangular face**.
 

The topological grouping consists of partitioning the 64 configurations into equivalence classes whose closed neighborhood graphs are isomorphic. This operation, purely structural and devoid of adjustable parameters, produces exactly **20 stable classes** (attractors). Each attractor is identified by:
- a triplet of pentads $\{X,Y,Z\} \subset \{P_1,\dots,P_6, N_1,\dots,N_6\}$,
- a polarity signature counting the positive and negative pentads in the triplet ($3P$, $2P+1N$, $1P+2N$, or $3N$).

The distribution $(3, 5, 11, 1)$ follows a strict geometric gradient correlated with the degree of convergence of the faces in the Merkabah. Biology (genetic code) and any other system projected onto this space exploits only the redundancy potential defined by this filtering: geometry bounds the admissible space, the function populates the coordinates.

\begingroup
\small
\setlength{\tabcolsep}{4pt}
\begin {longtable}{|c|c|c|c|c|c|}
\hline
\textbf{Cl(4,0)} & \textbf{Rank} & \textbf{Latin} & \textbf{Central Concept} & \textbf{Concepts (×4 per letter)} & \textbf{Polarity Triplet} \\
\hline
1 & 1 & A & Action/Truth & 1:A+, 2:A-, 3:Am, 4:A$^{\sim m}$ & $\{P_1,P_2,P_4\}=3P$ \\
I & 2 & B & Contribution & 5:B+, 6:B-, 7:Bm, 8:B$^{\sim m}$ & $\{P_1,P_3,P_5\}=3P$ \\
J & 3 & C & Appearance & 9:C+, 10:C-, 11:Cm, 12:C$^{\sim m}$ & $\{P_2,P_3,P_6\}=3P$ \\
K & 4 & D & Perception & 13:D+, 14:D-, 15:Dm, 16:D$^ {\sim m}$ & $\{P_4,P_5,N_2\}=2P+1N$ \\
-1 & 5 & E & Organization & 17:E+, 18:E-, 19:Em, 20:E$^{\sim m}$ & $\{P_5,P_6,N_3\}=2P+1N$ \\
-I & 6 & F & Difference & 21:F+, 22:F-, 23:Fm, 24:F$^{\sim m}$ & $\{P_1,P_6,N_4\}=2P+1N$ \\
-J & 7 & G & Mixing & 25:G+, 26:G-, 27:Gm, 28:G$^{\sim m}$ & $\{P_2,P_5,N_6\}=2P+1N$ \\
-K & 8 & H & Equivalence & 29:H+, 30:H-, 31:Hm, 32:H$^{\sim m}$ & $\{P_3,P_4,N_6\}=2P+1N$ \\
$i'1$ & 9 & I & Relation & 33:I+, 34:I-, 35:Im, 36:I$^{\sim m}$ & $\{P_1,N_2,N_6\}=1P+2N$ \\
$i'I$ & 10 & J & Flow & 37:J+, 38:J-, 39:Jm, 40:J$^{\sim m}$ & $\{P_1,N_3,N_5\}=1P+2N$ \\
$i'J$ & 11 & K & Entity & 41:K+, 42: K-, 43:Km, 44:K$^{\sim m}$ & $\{P_2,N_3,N_5\}=1P+2N$ \\
$i'K$ & 12 & L & Circle/ Cycle & 45:L+, 46:L-, 47:Lm, 48:L$^{\sim m}$ & $\{P_3,N_2,N_4\}=1P+2N$ \\
$-i'1$ & 13 & M & Evolution & 49:M+, 50:M-, 51:Mm, 52:M$^{\sim m}$ & $\{P_4,N_1,N_3\}=1P+2N$ \\
$-i'I$ & 14 & N & Dependence & 53:N+, 54:N-, 55:Nm, 56:N$^{\sim m}$ & $\{P_4,N_5,N_6\}=1P+2N$ \\
$-i'J$ & 15 & O & Variation & 57:O+, 58:O-, 59:Om, 60:O$^{\sim m}$ & $\{P_5,N_1,N_4\}=1P+2N$ \\
$-i'K$ & 16 & P & Regrouping & 61:P+, 62:P-, 63:Pm, 64:P$^{\sim m}$ & $\{P_6,N_1,N_2\}=1P+2N$ \\
 & 17 & Q & Synergy & 7:Bm, 21:F+, 25:G+ & $\{P_2,N_1,N_4\}=1P+2N$ \\
 
& 18 & R & Resonance & 29:H+, 33:I+, 37:J+ & $\{P_3,N_1,N_5\}=1P+2N$ \\
 & 19 & S & Spiral & 45:L+, 49: M+, 53:N+ & $\{P_6,N_5,N_6\}=1P+2N$ \\
 & 20 & T & Stratification & 57:O+, 61:P+, 63: Pm & $\{N_2,N_3,N_4\}=3N$ \\
\hline
\caption{The 16 elements of Cl(4,0) and the 4 additional elements}
\end{longtable}
\endgroup

\subsection*{C.4 Rules for selecting states at the intersection nodes Q, R, S, T}
The attractors Q, R, S, T do not correspond to primitive cells, but to internal nodes where two or three principal tetrahedra intersect. They do not convey any single primitive concept; they embody structural resonances whose Boolean state is determined by a strict topological selection rule.

** Principle of inheritance**: each intersection inherits exactly one state from each of its parents, limited to states where the primary structural dimension $A$ is affirmed:

- the anchoring state $+$, encoded as $A \cap \neg B \equiv (1,0)$,
- the interface state $m$, encoded as $A \cap B \equiv (1,1)$.

**Deterministic selection rule**: the secondary dimension $B$ is governed by the topological rigidity of the parent.

1. A parent contributes to the interface state $m$ $(1,1)$ if and only if its polarity signature is extreme ($3P$) or if it serves as a structural reference. Extreme poles possess high rigidity; providing only the anchoring state $(1,0)$ would break connectivity with mixed zones. They therefore flip the secondary dimension to $1$, producing the hinge $m$ that preserves the reference while allowing the interface.
2. Parents residing in already mixed zones ($2P+1N$ or $1P+2N$) maintain the secondary dimension at $0$, thereby contributing to the stable anchoring state $(1,0)$.

**Explicit application**:

- **Q** inherits $B^m$ (since B is $3P$), while F and G provide $F^+$ and $G^+$.
- **R** and **S** inherit only the $+$ states from their already mixed parents.
- **T** inherits $P^m$ (local reference for the internal core), with O providing $O^+$.

This mechanism ensures that each intersection contains exactly **one relational hinge ($m$) and two structural anchors ($+$)**, maintaining the consistency of the global network without free parameters and validating the signatures $1P+2N$ (Q, R, S) and $3N$ (T) obtained by geometric filtration.



\newpage

\begin{landscape}
\section*{Appendix D. Alignment of the 12 pentads with the 64 tetrads of $\mathrm{Cl}(6,0)$}

\begingroup
\footnotesize
\setlength{\tabcolsep}{3pt}
\renewcommand{\arraystretch}{0.85}
\setlength{\LTcapwidth}{\textwidth}
\centering
\begin{longtable}{|c|c|l||c|c|l|}
\hline
\multicolumn{3}{|c||}{\textbf{Positive pentads ($P_1$–$P_6$)}} & \multicolumn{3}{|c|}{\textbf{Negative pentads ($N_1$–$N_6$)}} \\
\cline{1-6}
\textbf{Pentad } & \textbf{Clifford elements} & \textbf{Tetradic correspondence (No./Concept)} & \textbf{Pentad} & \textbf{Clifford elements} & \textbf{Tetradic correspondence (No./Concept)} \\
\hline
$P_1$ & $\{iI,\; iJ,\; iK,\; i'k,\; j\}$ &
$\begin{array}{@{}l@{}}
iI \rightarrow 22\;(F^-:\text{Identity, unity}) \\
iJ \rightarrow 26\;(G^-:\text{Pure, simple}) \\
iK \rightarrow 30\;(H^-:\text{Incommensurability}) \\
i'k \rightarrow 36\;(I^{\sim m}:\text{Fusion, unification}) \\
j \rightarrow 3\;(A^m:\text{Intention, potentiality})
\end{array}$ &
$N_1$ & $\{-iI,\; -iJ,\; -iK,\; -i'k,\; -j\}$ &
$\begin{array}{@{}l@{}}
-iI \rightarrow 6\;(B^-:\text{Deprivation, subtraction}) \\
-iJ \rightarrow 10\;(C^-:\text {Essence, substance}) \\
-iK \rightarrow 14\;(D^-:\text{Unconsciousness, anesthesia}) \\
-i'k \rightarrow 52\;(M^{\sim m}:\text{Revolution, mutation}) \\
-j \rightarrow 19\;(E^m:\text{Emergence, self-organization}) \\
\end{array}$ \\
\hline
$P_2$ & $\{jI,\; jJ,\; jK,\; i'i,\; k\}$ &
$\begin{array}{@{}l@{}}
jI \rightarrow 23\; (F^m:\text{Relation, interface}) \\
jJ \rightarrow 27\;(G^m:\text{Combination, synergy}) \\
jK \rightarrow 31\;(H^m:\text{Analogy, proportion}) \\
i'i \rightarrow 34\;(I^-:\text{Isolation, independence}) \\
k \rightarrow 4\;(A^{\sim m}:\text{Chance, necessity})
\end{array}$ &
$N_2$ & $\{-jI,\; -jJ,\; -jK,\; -i'i,\; -k\}$ &
$\begin{array}{@ {}l@{}}
-jI \rightarrow 7\;(B^m:\text{Exchange, reciprocity}) \\
-jJ \rightarrow 11\;(C^m:\text{Symbol, representation}) \\
-jK \rightarrow 15\; (D^m:\text{Consciousness, attention}) \\
-i'i \rightarrow 50\;(M^-:\text{Eternity, immutability}) \\
-k \rightarrow 20\;(E^{\sim m}:\text{Constraint, imposed order})
\end{array}$ \\
\hline
$P_3$ & $\{kI,\; kJ,\; kK,\; i'j,\; i\}$ &
$\begin{array}{@{}l@{}}
kI \rightarrow 24\;(F^{\sim m}:\text{Absolute separation}) \\
kJ \rightarrow 28\;(G^{\sim m}:\text{Confusion, amalgamation}) \\
kK \rightarrow 32\;(H^{\sim m}:\text{Perfect identity}) \\
i'j \rightarrow 35\;(I^m:\text{Interdependence, network}) \\
i \rightarrow 2\;(A^-:\text{Inaction, illusion})
\end{array}$ &
$N_3$ & $\{-kI,\; -kJ,\; -kK,\; -i'j,\; -i\}$ &
$\begin{array}{@{}l@{}}
-kI \rightarrow 8\;(B^{\sim m}:\text{Autonomy, pure gift}) \\
-kJ \rightarrow 12\;(C^{\sim m}:\text{Naked reality, hidden truth}) \\
-kK \rightarrow 16\;(D^{\sim m}:\text {Intuition, direct knowledge}) \\
-i'j \rightarrow 51\;(M^m:\text{Growth, development}) \\
-i \rightarrow 18\;(E^-:\text{Chaos, disorder})
\end{array}$ \\
\hline
$P_4$ & $\{i'Ii,\; i'Ij,\; i'Ik,\; i'K,\; J\}$ &
$\begin{array}{@{}l@{}}
i'Ii \rightarrow 38\;(J^-:\text{Stasis, immobility}) \\
i'Ij \rightarrow 39\;(J^m:\text{Cycle, rhythm}) \\
i'Ik \rightarrow 40\;(J^{\sim m}:\text{Turbulence, chaos}) \\
i'K \rightarrow 45\;(L^+:\text{Circle, cycle}) \\
J \rightarrow 9\;(C^+:\text{Appearance, form})
\end{array}$ &
$N_4$ & $\{-i'Ii,\; -i'Ij,\; -i'Ik,\; -i'K,\; -J\}$ &
$\begin{array}{@{}l@{}}
-i'Ii \rightarrow 54\;(N^-:\text{Autonomy, freedom}) \\
-i'Ij \rightarrow 55\;(N^m:\text {Interdependence, balance}) \\
-i'Ik \rightarrow 56\;(N^{\sim m}:\text{Constraint, necessity}) \\
-i'K \rightarrow 61\;(P^+:\text{Grouping, whole}) \\
-J \rightarrow 25\;(G^+:\text{Mixing, merging})
\end{array}$ \\
\hline
$P_5$ & $\{i'Ji,\; i'Jj,\; i'Jk,\; i'I,\; K\}$ &
$\begin{array}{@{}l@{}}
i'Ji \rightarrow 42\;(K^-:\text{Void, non-being}) \\
i'Jj \rightarrow 43\;(K^m:\text{Relation, context}) \\
i'Jk \rightarrow 44\;(K^{\sim m}:\text{Substance, essence}) \\
i'I \rightarrow 37\;(J^+:\text{Flow, transfer}) \\
K \rightarrow 13\;(D^+:\text {Perception, sensation})
\end{array}$ &
$N_5$ & $\{-i'Ji,\; -i'Jj,\; -i'Jk,\; -i'I,\; -K\}$ &
$\begin{array}{@{}l@{}}
-i'Ji \rightarrow 58\;(O^-:\text{Constancy, stability}) \\
-i'Jj \rightarrow 59\;(O^m:\text {Adaptation, flexibility}) \\
-i'Jk \rightarrow 60\;(O^{\sim m}:\text{Instability, chaos}) \\
-i'I \rightarrow 53\;(N^+:\text{Dependence, influence}) \\
-K \rightarrow 29\;(H^+:\text{Equivalence, correspondence})
\end{array}$ \\
\hline
$P_6$ & $\{i'Ki,\; i'Kj,\; i'Kk,\; i'J,\; I\}$ &
$\begin{array}{@{}l@{}}
i'Ki \rightarrow 46\;(L^-:\text{Line, linearity}) \\
i'Kj \rightarrow 47\;(L^m:\text{Spiral, helix}) \\
i'Kk \rightarrow 48\;(L^{\sim m}:\text{Point, singularity}) \\
i'J \rightarrow 41\;(K^+:\text{Entity, being}) \\
I \rightarrow 5\;(B^+:\text{Contribution, input})
\end{array}$ &
$N_6$ & $\{-i'Ki,\; -i'Kj,\; -i'Kk,\; -i'J,\; -I\}$ &
$\begin{array}{@{}l@ {}}
-i'Ki \rightarrow 62\;(P^-:\text{Individuality, unity}) \\
-i'Kj \rightarrow 63\;(P^m:\text{Hierarchy, organization}) \\
-i'Kk \rightarrow 64\;(P^{\sim m}:\text{Crowd, mass}) \\
-i'J \rightarrow 57\;(O^+:\text {Variation, change}) \\
-I \rightarrow 21\;(F^+:\text{Difference, otherness})
\end{array}$ \\
\hline
\caption{Positive and negative pentads: Of the 64 elements of $\mathrm{Cl}(6,0)$, the 12 pentads include 5 × 12 = 60 elements. The 2 scalars (+1 and -1) and the 2 pseudo-scalars (+i' and -i') are excluded. The elements of the pentads are rewritten as $i<j<k<I<J<K$ in canonical order. The signs induced by anticommutation ($ab=-ba$) are mapped to the corresponding Boolean state, ensuring a bijection with the table of 64 concepts.}
\label{tab:pentads}
\end{longtable}
\endgroup
\end{landscape}

\newpage
![Dual graph of pentads](Penta_graph.png){ width=100% }
