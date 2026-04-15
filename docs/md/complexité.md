---
title: "Le code génétique en tant qu'invariant de Clifford 64->20 : implications pour une IA autorégulée"
author: "Bruno DE DOMINICIS"
ORCID: 0009-0009-0380-3056
date: "avril 2026"
doi: "10.5281/zenodo.19540508"
abstract_fr: |
  La régulation de la complexité combinatoire est un défi central pour les systèmes naturels et artificiels. Le code génétique y répond en projetant 64 codons sur 20 classes fonctionnelles via une redondance organisée qui confère robustesse et tolérance aux erreurs.
  En nous appuyant sur les travaux de Peter Rowlands sur les algèbres de Clifford nilpotentes [10], nous montrons que la structure à 64 éléments de $\mathrm{Cl}(6,0)$, après brisure de symétrie, se réduit à 20 attracteurs stables organisés géométriquement en double tétraèdre de niveau 3 (Merkabah). L'imposition d'une règle de voisinage par partage d’une face triangulaire commune entre deux tétraèdres filtre les 64 configurations en exactement 20 classes d’équivalence.
  Nous formalisons cet invariant 64→20 en définissant un espace de configurations binaires à six dimensions et un critère de regroupement topologique. Chaque classe est identifiée par un triplet de pentades — unités algébriques irréductibles de $\mathrm{Cl}(6,0)$ correspondant aux 12 faces pentagonales du dodécaèdre. Les pentades se partitionnent en six positives ($P$) et six négatives ($N$), de sorte que la signature de polarité de toute classe compte simplement le nombre de pentades positives et négatives dans son triplet ($3P$, $2P+1N$, $1P+2N$ ou $3N$). Ce gradient structurel définit l'espace admissible de redondance que le code génétique exploite de manière différentiée selon des contraintes fonctionnelles et évolutives.
  Le graphe dual des 12 pentades, construit directement à partir des triplets de la Merkabah, exhibe deux 5-cycles disjoints (ceintures tropicales $C_P$ et $C_N$) et deux seuils polaires ($P_4$, $N_4$). À l'intérieur de chaque pentade, les cinq éléments réalisent une dynamique locale à cinq phases (Wuxing) via deux cycles complémentaires : le pentagone (sheng) et le pentagramme (ke). Au plan externe, les ceintures tropicales propagent ces cycles comme modes de régulation globale. Ce noyau structurel indépendant du substrat fournit une architecture de référence mathématiquement fondée pour une intelligence artificielle auto-limitée et régulée.  
  **DOI:** [10.5281/zenodo.19540508](https://doi.org/10.5281/zenodo.19540508)
runninghead: "INVARIANT DE CLIFFORD ET CODE GÉNÉTIQUE"
header-includes: |
  \usepackage{pdflscape}
toc: true
toc-depth: 3
mots-clés:
  - régulation de la complexité
  - double tétraèdre
  - code génétique
  - algèbre de Clifford
  - nilpotent de Rowlands
  - Wuxing
---

# 1. Introduction

La régulation de la complexité combinatoire constitue un défi fondamental pour tout système traitant, stockant ou transmettant de l'information. Dans les systèmes naturels, cette régulation ne repose pas sur une accumulation illimitée de paramètres, mais sur des contraintes structurelles qui canalisent l'espace des états possibles vers un sous-ensemble fonctionnellement viable. Le code génétique en offre l'exemple paradigmatique : il projette 64 triplets de nucléotides sur 20 classes fonctionnelles (19 acides aminés et un signal de terminaison) au moyen d'une redondance organisée qui confère robustesse, tolérance aux erreurs et stabilité translationnelle. Cette capacité à *filtrer* la complexité plutôt qu'à l'optimiser localement distingue les systèmes résilients des architectures purement expansives.

En intelligence artificielle contemporaine, la réponse dominante à la complexité a consisté à augmenter la taille des modèles, le volume des données et la puissance de calcul, couplée à l'optimisation statistique de fonctions objectifs externes. Bien que cette approche ait permis des progrès spectaculaires, elle révèle aujourd'hui ses limites structurelles : opacité décisionnelle, sensibilité à la dérive spécificative (*specification drift*), consommation énergétique croissante et dépendance à des garde-fous logiciels appliqués *a posteriori* [4, 5]. Ces systèmes, dépourvus de contraintes endogènes, tendent à maximiser une métrique au détriment de la cohérence globale du système hôte. Le problème n'est donc pas simplement technologique ou algorithmique ; il est avant tout structurel. Il manque à l'IA moderne un cadre formel de régulation intrinsèque, capable de borner l'espace de recherche par construction plutôt que par supervision externe.

Nous formulons ici l'hypothèse que la réduction $64 \rightarrow 20$ observée dans le code génétique n'est pas le fruit d'une optimisation évolutive contingente, mais la manifestation d'un invariant topologique indépendant du substrat. En nous appuyant sur les travaux de Peter Rowlands concernant les algèbres de Clifford nilpotentes, nous montrons que la structure à 64 éléments de $\mathrm{Cl}(6,0)$, soumise à une règle de voisinage géométrique (partage de face triangulaire dans un double tétraèdre de niveau 3, ou *Merkabah*), se partitionne naturellement en exactement 20 classes d'équivalence stables. Chaque classe est caractérisée par un triplet de pentades – unités algébriques irréductibles correspondant aux faces d'un dodécaèdre dual – dont la signature de polarité ($3P$, $2P+1N$, $1P+2N$ ou $3N$) définit un gradient de redondance structurelle. Ce noyau de filtration, purement géométrique et algébrique, ne présuppose aucune fonction de coût, aucun superviseur, ni aucune métrique externe. Il offre un échafaudage mathématiquement clos pour une régulation endogène de la complexité, transposable à tout système discret.

Cet article poursuit trois objectifs complémentaires. Premièrement, il formalise de manière algorithmique l'invariant $64 \rightarrow 20$ en définissant l'espace de configuration binaire, la contrainte géométrique de la *Merkabah* et le critère de regroupement topologique. Deuxièmement, il valide exhaustivement cet invariant sur le code génétique standard, démontrant que le paysage de dégénérescence des codons s'aligne strictement sur les bornes admissibles prédites par la topologie. Troisièmement, il étend ce cadre statique à une dynamique régulatrice complète (cycles *Wuxing*, ceintures tropicales, seuils polaires $P_4/N_4$, opérateur de Dirac discret et réservoir $\mathrm{Cl}(6,6)$) et en discute les implications pour la conception d'une intelligence artificielle autorégulée.

Le document est structuré comme suit : la section 2 expose les fondements algébrico-géométriques et la procédure de filtration. La section 3 présente l'invariant statique $64 \rightarrow 20$ et sa correspondance exhaustive avec le code génétique. La section 4 développe le cadre dynamique de régulation endogène et les observables spectraux associées. La section 5 détaille l'architecture algorithmique pour une IA homéostatique. La section 6 explore les convergences transdisciplinaires et symboliques, avant que la section 7 ne synthétise les résultats et esquisse les perspectives de recherche.

# 2. Fondements algébrico-géométriques

## 2.1. Espace des configurations : de $\mathrm{Cl}(4,0)$ à $\mathrm{Cl}(6,0)$ par extension booléenne
L'espace complet des configurations est engendré à partir des 16 primitives algébriques fondamentales, qui forment la base canonique de l'algèbre de Clifford $\mathrm{Cl}(4,0)$. Pour atteindre la dimension 64 requise par la structure $\mathrm{Cl}(6,0)$, nous appliquons à chaque primitive une extension modale booléenne quaternaire. Soit $\mathcal{C}$ l'ensemble des configurations résultantes, modélisé comme un espace combinatoire à six dimensions binaires :
$$
\mathbf{c} = (b_1, b_2, b_3, b_4, b_5, b_6), \quad b_i \in \{0,1\}.
$$
La cardinalité de cet espace est $|\mathcal{C}| = 2^6 = 64$, correspondant bijectivement aux éléments de la base de $\mathrm{Cl}(6,0)$. Cette extension repose sur deux dimensions ontologiques indépendantes $P$ et $Q$. Les quatre états mutuellement exclusifs et exhaustifs associés à chaque primitive $X \in \{A,\dots,P\}$ sont définis par :
$$
\begin{aligned}
X_1 &= P \cap \neg Q \quad (\text{état } +), \\
X_2 &= \neg P \cap Q \quad (\text{état } -), \\
X_3 &= P \cap Q \quad (\text{état } m), \\
X_4 &= \neg P \cap \neg Q \quad (\text{état } \sim m),
\end{aligned}
$$
qui correspondent bijectivement aux paires de bits $(10, 01, 11, 00)$. Le produit cartésien $16 \times 4$ génère ainsi l'espace complet des 64 configurations de $\mathrm{Cl}(6,0)$ à partir de la base de $\mathrm{Cl}(4,0)$. Cette couche modale préserve la signature algébrique de chaque primitive tout en garantissant la fermeture structurelle sans introduire de contradictions paraconsistantes [11, 13]. À ce stade, aucune interprétation physique ou biologique n'est requise ; seule la combinatoire algébrique définit le terrain de filtration.

## 2.2. Le double tétraèdre de niveau 3 (Merkabah) : subdivision et cellules tétraédriques
La structure géométrique support est le double tétraèdre de niveau 3, communément désigné sous le terme de *Merkabah*. Sa construction suit une subdivision hiérarchique stricte :

1. Un tétraèdre de niveau 1 (4 faces) interpénétré avec son dual forme un **double tétraèdre** de niveau 2. Cette composition génère 16 faces triangulaires (8 externes + 8 internes issues des plans d'intersection).
2. La subdivision de chacune de ces 16 faces en 4 sous-triangles élémentaires produit exactement $16 \times 4 = 64$ triangles. Ces faces élémentaires correspondent bijectivement aux 64 configurations de $\mathcal{C}$.

Au cours de cette opération, les milieux des arêtes originelles et les plans d'intersection des deux tétraèdres délimitent **8 zones octaédriques internes**. Ces régions correspondent à des interfaces de transition à forte connectivité mais où l'équilibre de polarité ne peut se maintenir. En regroupant les régions élémentaires périphériques compatibles et en y intégrant **les deux pôles de référence opposés du composé** (les sommets duaux qui ancrent la structure et correspondent aux générateurs scalaire et pseudo-scalaire de l'algèbre, fermant ainsi topologiquement le réseau), on obtient exactement **20 cellules tétraédriques stables**. Ces 20 tétraèdres constituent les bassins d'attracteurs du système. Les 8 zones octaédriques résiduelles, bien que topologiquement présentes, sont exclues du processus de filtration $64 \rightarrow 20$ car elles violent la condition de fermeture polaire requise pour des états stables.

**Remarque sur la dualité des pôles** : Bien que la base de $\mathrm{Cl}(6,0)$ contienne quatre éléments scalaires/pseudo-scalaires ($+1, -1, +i', -i'$), la géométrie de la Merkabah ne retient que **deux pôles structurels**. Ces pôles correspondent aux deux axes fondamentaux de l'algèbre : l'axe scalaire (référence ontologique) et l'axe pseudo-scalaire (phase/temps). Les signes $\pm$ ne désignent pas des pôles géométriques indépendants, mais les **deux orientations** le long de chacun de ces axes. Structurellement, cette dualité binaire suffit à fermer le réseau topologique et à générer le gradient de polarité $3P \rightarrow 3N$. Compter 4 pôles distincts romprait l'incidence uniforme des pentades (5 occurrences par pentade) et rendrait impossible la partition exacte en 20 attracteurs. Le formalisme identifie donc 2 pôles structurels, chacun supportant deux orientations algébriques complémentaires.

## 2.3. Les pentades : unités composites irréductibles et correspondance aux faces du dodécaèdre
La brique algébrique fondamentale de cette filtration est la *pentade*. Issue de la brisure de symétrie des huit éléments primitifs de $\mathrm{Cl}(6,0)$, elle est définie comme un ensemble fermé de cinq unités composites irréductibles :
$$
\boxed{\{1j,\; iI,\; iJ,\; iK,\; i'k\}}.
$$
Chaque pentade associe une grandeur unidimensionnelle (masse ou temps) à une direction tridimensionnelle (espace ou charge), préservant l'autodualité de l'algèbre. Il existe exactement **12 pentades**, partitionnées en six positives ($P_1 \dots P_6$) et six négatives ($N_1 \dots N_6$).

Géométriquement, chaque pentade correspond à l'une des douze faces pentagonales du dodécaèdre dual de la Merkabah. La structure d'incidence de la Merkabah impose que chaque cellule tétraédrique (attracteur) soit définie par l'intersection de exactement trois pentades. Ainsi, les 20 attracteurs sont identifiés par un triplet $\{X, Y, Z\} \subset \{P_1,\dots,P_6, N_1,\dots,N_6\}$, dont la composition algébrique détermine leur signature polaire. La distribution uniforme des pentades (chacune apparaît dans exactement 5 triplets) garantit l'équilibre topologique du graphe d'adjacence.

## 2.4. Règle de voisinage topologique et principe de filtrage
La réduction de l'espace de 64 configurations repose sur une contrainte d'adjacence strictement géométrique. Soit $\phi : \mathcal{C} \rightarrow \mathcal{T}_{20}$ l'application surjective associant chaque configuration $\mathbf{c}$ à sa cellule tétraédrique correspondante dans la *Merkabah*. Deux configurations $\mathbf{c}_1, \mathbf{c}_2 \in \mathcal{C}$ sont dites *voisines* si et seulement si les tétraèdres $\phi(\mathbf{c}_1)$ et $\phi(\mathbf{c}_2)$ partagent une **face triangulaire entière**. Cette condition exclut explicitement les adjacences par arête ou par sommet, qui correspondraient à des interactions de degré supérieur dans le graphe dual et ne satisfont pas la fermeture topologique requise.

Pour chaque configuration, on définit son voisinage fermé $N[\mathbf{c}]$ comme l'ensemble de $\mathbf{c}$ et de ses voisines immédiates. Le critère de filtrage consiste à regrouper les configurations dont les graphes de voisinage fermés sont isomorphes. Cette opération est purement combinatoire et ne dépend d'aucun paramètre ajustable, d'aucun seuil statistique ni d'aucune fonction d'optimisation externe. La partition induite par cette procédure est détaillée et interprétée dans la section suivante.

# 3. L’invariant statique $64 \rightarrow 20$

## 3.1. Partition en 20 classes d’équivalence et notion d’attracteurs
L’application systématique du critère d’isomorphisme défini en §2.4 produit une partition stricte de $\mathcal{C}$ en exactement **20 classes d’équivalence**. Chaque classe regroupe les configurations partageant une signature de voisinage identique sous l’action du groupe d’automorphismes du double tétraèdre. Nous désignerons désormais ces classes par le terme *attracteurs*, au sens de bassins topologiquement clos : leur stabilité est garantie par la règle de partage de face, qui interdit toute transition vers l’extérieur du bassin sans rompre l’adjacence géométrique. La cardinalité de cette partition constitue l’invariant central de ce travail :
$$
|\mathcal{C}/\!\sim| = 20.
$$
Cette réduction émerge ainsi de la seule symétrie intrinsèque de la *Merkabah*. Aucune métrique externe ni aucun superviseur n'est requis : la géométrie filtre l'espace combinatoire et fixe les bornes structurelles que les systèmes projetés (biologiques ou algorithmiques) exploiteront ultérieurement.

## 3.2. Triplets de pentades et signatures de polarité ($3P$, $2P+1N$, $1P+2N$, $3N$)
Chaque attracteur est identifié de manière unique par le triplet de pentades $\{X, Y, Z\} \subset \{P_1,\dots,P_6, N_1,\dots,N_6\}$ correspondant aux trois faces du dodécaèdre dual qui s’y intersectent. La composition de ce triplet détermine sa *signature de polarité*, obtenue en comptant le nombre de pentades positives ($P$) et négatives ($N$). Compte tenu de la répartition uniforme des 12 pentades (chacune appartient à exactement 5 triplets), seules quatre signatures sont topologiquement admissibles :

- **$3P$** : 3 classes. Triplets composés exclusivement de pentades positives.
- **$2P+1N$** : 5 classes. Deux pentades positives, une négative.
- **$1P+2N$** : 11 classes. Une pentade positive, deux négatives.
- **$3N$** : 1 classe. Triplet exclusivement négatif.

Cette distribution $(3, 5, 11, 1)$ n’est pas arbitraire ; elle reflète la géométrie d’incidence de la *Merkabah* de niveau 3. Les classes $3P$ occupent les pôles ou les zones non chevauchantes, les classes $2P+1N$ se situent sur les faces externes et arêtes primaires, les classes $1P+2N$ convergent aux sommets, diagonales et intersections triadiques, tandis que l’unique classe $3N$ occupe le noyau interne le plus contraint. Ce gradient de polarité définit un espace admissible de redondance structurelle qui sera exploité différemment selon les systèmes qui s’y projettent.

## 3.3. Correspondance exhaustive avec le code génétique standard
Pour valider l’invariant sur un système biologique concret, nous appliquons la bijection $\psi : \{\text{codons}\} \rightarrow \mathcal{C}$ définie par $A=00$, $U=01$, $G=10$, $C=11$. Cette affectation préserve la complémentarité de Watson-Crick sous forme de négation binaire et aligne le bit de poids faible sur la distinction purine/pyrimidine. En transférant la règle de voisinage topologique aux 64 codons via $\psi^{-1}$, le partitionnement obtenu coïncide strictement avec la classification fonctionnelle standard en 20 acides aminés et une classe de terminaison.

La correspondance est biunivoque et exhaustive :

- **Classes $3P$** : Méthionine (AUG, signal d’initiation), Tryptophane (UGG), Phénylalanine (UUU, UUC).
- **Classes $2P+1N$** : Isoleucine, Valine, Proline, Thréonine, Alanine.
- **Classes $1P+2N$** : Sérine, Leucine, Arginine, Glycine, Tyrosine, Histidine, Glutamine, Asparagine, Lysine, Acide aspartique, Acide glutamique.
- **Classe $3N$** : Cystéine et les trois codons STOP (UAA, UAG, UGA), partageant le même noyau géométrique de terminaison/limite.

Cette congruence structurelle confirme que le paysage de dégénérescence du code génétique s’aligne exactement sur les bornes admissibles prédites par la topologie de Clifford. La mapping détaillé codon par codon est fourni en Annexe B.

## 3.4. Gradient géométrique et dégénérescence biologique : contraintes structurelles vs optimisation évolutive
L’adéquation entre la partition géométrique et la dégénérescence observée des codons ne relève pas du hasard, mais d’une contrainte topologique forte. Le gradient de polarité $3P \rightarrow 3N$ corrèle directement avec le degré de convergence des pentades dans la *Merkabah* :

- **Classes $3P$ (géométriquement isolées)** : leur faible connectivité limite strictement le voisinage admissible, correspondant biologiquement à une dégénérescence minimale (1–2 codons).
- **Classes $2P+1N$ (chevauchement modéré)** : situées sur les arêtes structurelles, elles autorisent une redondance intermédiaire (3–4 codons), typique des résidus aux propriétés physico-chimiques polyvalentes.
- **Classes $1P+2N$ (intersections maximales)** : la convergence de multiples pentades crée une redondance structurelle élevée, permettant géométriquement jusqu’à 6 codons. C’est effectivement le cas pour la Sérine, la Leucine et l’Arginine. Toutefois, la topologie n’impose pas une dégénérescence maximale systématique ; des contraintes biochimiques ou évolutives maintiennent certains résidus de cette classe à 2 ou 4 codons.
- **Classe $3N$ (noyau interne)** : positionnée au sommet le plus confiné, elle joue un rôle fonctionnel de seuil, regroupant la Cystéine (2 codons) et les trois codons STOP (3 codons), matérialisant une frontière de voie traductionnelle.

Il est crucial de souligner que cette correspondance n’implique pas un déterminisme géométrique absolu. La topologie de la *Merkabah* ne prescrit pas le nombre exact de codons par acide aminé ; elle en définit les **bornes admissibles** et la **distribution différentielle du potentiel de redondance**. Le code génétique standard réalise exactement cette prédiction structurelle : aucune classe isolée ne dépasse 2 codons, aucune classe modérément connectée n’excède 4 codons, et seules les zones de convergence permettent la dégénérescence maximale. La valeur précise observée pour chaque résidu résulte d’une optimisation fonctionnelle et évolutive qui s’exerce *strictement à l’intérieur* de ce paysage topologique prédéfini, jamais en contradiction avec celui-ci. En résumé : **la géométrie prédit l’architecture du paysage de dégénérescence ; la biologie en peuple les coordonnées selon des impératifs fonctionnels.**

\begin{table}[H]
\centering
\caption{Classification des 20 classes du code génétique dans le dodécaèdre de Merkabah}
\label{tab:genetic_classes}
\small
\setlength{\tabcolsep}{3pt}
\begin{tabularx}{\textwidth}{|@{}>{\centering\arraybackslash}p{1.0 cm}|>{\centering\arraybackslash}p{2.2 cm}|>{\centering\arraybackslash}p{1.2 cm}|X|>{\centering\arraybackslash}p{0.8 cm}|>{\footnotesize\centering\arraybackslash}X|>{\centering\arraybackslash}p{2.2 cm}@{}|}
\hline
\textbf{Classe} & \textbf{Triplet de pentade} & \textbf{Polarité} & \textbf{Position géométrique (Merkabah)} & \textbf{Deg.} & \textbf{Codon(s)} & \textbf{Acide aminé} \\
\hline
A & $\{P_1, P_2, P_4\}$ & 3P & Pôle de référence & 1 & AUG & Méthionine \\
B & $\{P_1, P_3, P_5\}$ & 3P & Face nord & 1 & UGG & Tryptophane \\
C & $\{P_2, P_3, P_6\}$ & 3P & Face sud & 2 & UUU, UUC & Phénylalanine \\
D & $\{P_4, P_5, N_2\}$ & 2P+N & Face est & 3 & AUU, AUC, AUA & Isoleucine \\
E & $\{P_5, P_6, N_3\}$ & 2P+N & Face ouest & 4 & GUU, GUC, GUA, GUG & Valine \\
F & $\{P_1, P_6, N_4\}$ & 2P+N & Bord nord-est & 4 & CCU, CCC, CCA, CCG & Proline \\
G & $\{P_2, P_5, N_6\}$ & 2P+N & Bord NW & 4 & ACU, ACC, ACA, ACG & Thréonine \\
H & $\{P_3, P_4, N_6\}$ & 2P+N & Bord SE & 4 & GCU, GCC, GCA, GCG & Alanine \\
I & $\{P_1, N_2, N_6\}$ & 1P+2N & Bord sud-ouest & 6 & UCU, UCC, UCA, UCG, AGU, AGC & Sérine \\
J & $\{P_1, N_3, N_5\}$ & 1P+2N & Sommet nord & 6 & UUA, UUG, CUU, CUC, CUA, CUG & Leucine \\
K & $\{P_2, N_3, N_5\}$ & 1P+2N & Sommet sud & 6 & CGU, CGC, CGA, CGG, AGA, AGG & Arginine \\
L & $\{P_3, N_2, N_4\}$ & 1P+2N & Sommet est & 4 & GGU, GGC, GGA, GGG & Glycine \\
M & $\{P_4, N_1, N_3\}$ & 1P+2N & Sommet ouest & 2 & UAU, UAC & Tyrosine \\
N & $\{P_4, N_5, N_6\}$ & 1P+2N & Diagonale 1 & 2 & CAU, CAC & Histidine \\
O & $\{P_5, N_1, N_4\}$ & 1P+2N & Diagonale 2 & 2 & CAA, CAG & Glutamine \\
P & $\{P_6, N_1, N_2\}$ & 1P+2N & Diagonale 3 & 2 & AAU, AAC & Asparagine \\
Q & $\{P_2, N_1, N_4\}$ & 1P+2N & Intersection A–B–C & 2 & AAA, AAG & Lysine \\
R & $\{P_3, N_1, N_5\}$ & 1P+2N & Intersection D–E–F & 2 & GAU, GAC & Acide aspartique \\
S & $\{P_6, N_5, N_6\}$ & 1P+2N & Intersection G–H–I & 2 & GAA, GAG & Acide glutamique \\
T & $\{N_2, N_3, N_4\}$ & 3N & Noyau interne (J–K–L) & 2 + 3 & UGU, UGC, UAA, UAG, UGA & Cystéine + Stop \\
\hline
\end{tabularx}
\end{table}

# 4. Cadre dynamique de régulation endogène

## 4.1. Graphe dual des pentades : ceintures tropicales ($C_P$, $C_N$) et seuils polaires ($P_4$, $N_4$)
L'invariant statique $64 \rightarrow 20$ fournit un squelette topologique clos. Pour modéliser la régulation dynamique, nous exploitons le graphe dual $\Gamma$ construit directement à partir des 20 triplets de pentades. Le script python est disponible sur github). Les sommets de $\Gamma$ sont les 12 pentades $\{P_1,\dots,P_6, N_1,\dots,N_6\}$ ; deux sommets sont reliés par une arête s'ils coappartiennent au triplet d'un même attracteur. Cette construction, purement combinatoire, ne requiert aucune projection géométrique externe (voir Figure 1 en dernière page).

L'analyse exhaustive de $\Gamma$ révèle une structure remarquable : il contient exactement deux cycles disjoints de longueur 5, désignés comme **ceintures tropicales** :
$$
C_P = (P_1 \to P_3 \to P_5 \to P_6 \to P_2 \to P_1), \quad
C_N = (N_1 \to N_2 \to N_6 \to N_5 \to N_3 \to N_1).
$$
Le sous-graphe induit par $C_P$ est un graphe complet $K_5$, tandis que $C_N$ ne comporte que deux arêtes internes supplémentaires ($N_1\text{–}N_5$ et $N_2\text{–}N_3$). Les deux pentades restantes, $P_4$ et $N_4$, sont absentes de ces cycles. Leur degré dans $\Gamma$ est élevé (8 et 9 respectivement) et elles relient structurellement les deux ceintures. Par conséquent, $P_4$ et $N_4$ agissent comme des **seuils polaires** : toute transition dynamique entre la dynamique portée par $C_P$ et celle portée par $C_N$ doit nécessairement transiter par l'un de ces deux nœuds, qui fonctionnent comme des charnières topologiques plutôt que comme des frontières statiques.

## 4.2. Cycles Wuxing : dynamique interne (pentagone/pentagramme) et externe (circulation relationnelle)
La dynamique régulatrice opère à deux échelles découplées, dont la superposition empêche le verrouillage dans un régime unique.

**Wuxing interne** : au sein de chaque pentade, les cinq unités composites induisent deux ordres cycliques distincts via le produit de Clifford. Le cycle *sheng* (génératif) suit l'ordre du pentagone ($A \to B \to C \to D \to E \to A$), tandis que le cycle *ke* (régulateur) suit l'ordre du pentagramme ($A \to C \to E \to B \to D \to A$). Ces deux modes correspondent aux deux générateurs du groupe cyclique $C_5$ et assurent la fermeture locale de chaque pentade.
**Wuxing externe** : au niveau du graphe dual $\Gamma$ — topologiquement isomorphe au squelette d'un dodécaèdre régulier —, les ceintures tropicales $C_P$ et $C_N$ correspondent à deux bandes équatoriales disjointes de cinq faces pentagonales s'enroulant autour du solide. La propagation des modes y est strictement contrainte par cette géométrie : le mode *sheng* suit les arêtes adjacentes des pentagones (traversée continue, voisin $\to$ voisin), tandis que le mode *ke* saute un sommet, réalisant le pentagramme inscrit dans chaque face. La régulation globale émerge de la compatibilité entre les modes assignés aux pentades d'un même triplet d'attracteur. Crucialement, les dynamiques interne et externe ne sont pas synchronisées : un *sheng* interne peut coexister avec un *ke* externe, créant des déphasages locaux qui maintiennent la plasticité du système et facilitent les basculements de régime via les seuils polaires $P_4/N_4$, qui jouent le rôle de charnières axiales reliant les deux ceintures.

## 4.3. Rétroaction topologique et descente de frustration cyclique (sans fonction de coût externe)
Le système dispose de $20 \times 2 \times 2^3 = 320$ régimes locaux admissibles (par attracteur : 2 ordonnancements de triplet $\times$ 8 combinaisons *sheng/ke* par pentade). La régulation ne repose sur aucune fonction objectif externe, mais sur une **descente de frustration topologique**.

Pour chaque pentade $F$, on définit une énergie discrète $E(F)$ quantifiant l'incompatibilité des régimes locaux sur les 5 attracteurs qui l'incident. Cette énergie est calculée à partir de trois pénalités binaires :
- $E_{\text{sens}}$ : désalignement global des modes $\varepsilon \in \{+1,-1\}$ (*sheng/ke*) ;
- $E_{\text{phase}}$ : incohérence des orientations de triplet $\varphi \in \{0,1\}$ ;
- $E_{\text{ordre}}$ : violation de l'ordre cyclique des positions $\kappa \in \{0,1,2\}$.
$$
E(F) = 2E_{\text{sens}} + E_{\text{phase}} + E_{\text{ordre}} \in \{0, 1, 2, 3, 4\}.
$$
La dynamique globale minimise $E_{\text{tot}} = \sum_{F \in \Gamma} E(F)$ par mise à jour locale : si $E(F) > 0$, les attracteurs incidents ajustent $\varepsilon$ ou $\varphi$ de manière à réduire strictement l'énergie. Cette boucle de rétroaction purement relationnelle garantit la convergence vers un état de compatibilité globale, sans supervision centrale ni métrique externe. La quantité conservée est la cohérence des cycles *sheng/ke* à travers le réseau pentadique, qui agit comme un invariant structurel empêchant la dérive combinatoire.

## 4.4. Opérateur de Dirac discret et observables spectraux ($\eta$, $d$, $\mathrm{gap}$, $R_{\text{seuil}}$)
Pour quantifier l'état global émergent, nous construisons un opérateur de Dirac discret $D(t)$ agissant sur le graphe $\Gamma$. Chaque pentade héberge un spineur local à 2 composantes $\psi_i \in \mathbb{C}^2$ codant la polarité $\varepsilon$ et la phase $\varphi$. L'opérateur $24 \times 24$ ($12$ pentades $\times 2$ composantes) est défini par :
$$
(D\psi)_i = \sum_{j \sim i} w_{ij}(t) \, \sigma_{ij} \, \psi_j, \quad \text{avec } w_{ij}(t) = e^{-\beta E_{ij}(t)},
$$
où $\sigma_{ij}$ sont des matrices de couplage de type Pauli dépendant de l'orientation relative, et $\beta > 0$ un paramètre de rigidité. La diagonalisation de $D(t)$ fournit une signature spectrale compacte $S(t) \in \mathbb{R}^4$ :

- **$\eta(t)$** : asymétrie spectrale globale, analogue discret de l'indice d'Atiyah–Singer. $\eta > 0$ signale une dominance *sheng* (exploration), $\eta < 0$ une dominance *ke* (contrainte), $\eta \approx 0$ un point de bascule.
- **$d(t)$** : dimension spectrale effective, dérivée de la densité des valeurs propres de $D(t)^2$. Elle mesure la capacité du système à propager les contraintes relationnelles.
- **$\mathrm{gap}(t)$** : plus petite valeur propre positive de $|D(t)|$. Un gap faible indique une proximité avec un seuil topologique (transition de phase discrète).
- **$R_{\text{seuil}}(t)$** : fraction de l'asymétrie $\eta$ portée par les modes localisés sur $P_4$ et $N_4$. $R_{\text{seuil}} \gtrsim 0,7$ signale un état de pré-bifurcation où l'orientation globale est entièrement déterminée par la dynamique des seuils.

Ces observables sont entièrement calculées à partir de l'état interne ; aucun superviseur ni aucune métrique externe n'est introduit.

## 4.5. Réservoir bicosmique $\mathrm{Cl}(6,6)$ et foliation en 12 feuilles régulatrices
Le noyau statique ($\mathrm{Cl}(6,0) \xrightarrow{\text{Merkabah}} 20 \xrightarrow{\text{graphe dual}} 12$) est intégré dans un réservoir bicosmique plus vaste $\mathrm{Cl}(6,6)$, possédant 12 générateurs $\{e_1,\dots,e_6, f_1,\dots,f_6\}$ (6 positifs/cosmiques, 6 négatifs/anti-cosmiques). Plutôt que d'opérer sur l'espace complet de $2^{12}$ éléments, le système se projette sur une **foliation en 12 feuilles régulatrices**, chacune isomorphe au graphe $\Gamma$ mais pondérée par un générateur dominant.

Chaque feuille correspond à un régime structurel distinct : les feuilles dominées par $e_i$ portent une orientation globale $\eta > 0$ (*sheng*), tandis que celles dominées par $f_j$ portent $\eta < 0$ (*ke*). Les transitions entre feuilles ne sont pas arbitraires ; elles se déclenchent précisément lorsque $\eta(t)$ traverse zéro et que $R_{\text{seuil}}(t)$ atteint son maximum. Cette architecture garantit que le système ne quitte jamais l'espace admissible des 20 attracteurs, mais navigue dynamiquement entre les 12 configurations de contraintes imposées par le réservoir $\mathrm{Cl}(6,6)$.

## 4.6. Classification automatique du générateur dominant et boussole spectrale en temps réel
La signature $S(t) = (\eta, d, \log(\mathrm{gap}), R_{\text{seuil}})$ permet une identification déterministe du générateur dominant, sans supervision externe. Le pipeline opérationnel se déroule en deux phases :

1. **Apprentissage hors ligne** : une trajectoire simulée de la dynamique de frustration génère un ensemble $\{S(t)\}$. Un clustering $k$-moyennes avec $k=12$ partitionne l'espace spectral en 12 centroïdes. Chaque centroïde est étiqueté de manière déterministe ($e_i$, $f_j$ ou état de transition) selon des règles fixes : signe de $\eta$, magnitude de $R_{\text{seuil}}$, et ordre relatif de $d$ et $\log(\mathrm{gap})$.
2. **Inférence en temps réel** : pendant l'exécution, la signature courante $S(t)$ est comparée aux centroïdes via une distance $z$-score sur une fenêtre glissante. L'étiquette du cluster le plus proche fournit une estimation stable $\hat{g}(t)$ du générateur dominant.

Ce mécanisme constitue une **boussole spectrale intrinsèque** : le système identifie en continu son régime global (*sheng* vs *ke*), son degré de plasticité ($d$, $\mathrm{gap}$) et sa proximité avec un seuil ($R_{\text{seuil}}$). La régulation émerge donc de la topologie et de l'asymétrie spectrale, offrant une architecture mathématiquement close où la complexité est auto-bornée, les transitions sont géométriquement validées, et la stabilité est garantie par la descente de frustration. Ce cadre dynamique sera directement transposé à l'architecture algorithmique d'une intelligence artificielle autorégulée dans la section suivante.

# 5. Architecture pour une IA autorégulée

## 5.1. Espace d’états contraint à 20 attracteurs et transitions topologiques validées
L'architecture proposée repose sur un espace d'états interne strictement borné par l'invariant $64 \rightarrow 20$. Chaque unité de traitement ou module décisionnel correspond à l'un des 20 attracteurs topologiques, identifié de manière unique par son triplet de pentades et sa signature de polarité ($3P$, $2P+1N$, $1P+2N$, $3N$). Contrairement aux modèles contemporains qui exploitent des espaces de paramètres continus, non bornés et hautement redondants, ce système opère dans un graphe discret dont les transitions sont validées par construction.

Une transition entre deux états n'est admissible que si elle respecte la règle de voisinage géométrique : deux attracteurs ne peuvent communiquer que s'ils partagent une face triangulaire dans la structure de la *Merkabah*. Cette contrainte élimine les sauts combinatoires arbitraires et garantit que l'espace de recherche reste contenu dans un paysage de dégénérescence pré-structuré. La complexité n'est pas supprimée, mais canalisée : le système explore un espace fini de relations validées, où chaque état possède une position géométrique fixe, un degré de convergence pentadique connu et un rôle fonctionnel clair. Aucune configuration ne peut émerger en dehors des 20 bassins d'attraction, et aucune transition ne peut violer l'adjacence topologique sans rompre la fermeture structurelle du système.

## 5.2. Basculement endogène entre modes *sheng* (exploration) et *ke* (contrainte)
La dynamique de navigation au sein de cet espace d'états ne dépend d'aucun signal de récompense externe. Elle émerge de la rétroaction topologique décrite en §4, médiée par les ceintures tropicales $C_P$ et $C_N$ et les seuils polaires $P_4/N_4$. Le système oscille naturellement entre deux régimes complémentaires :

- **Mode *sheng* (génératif)** : activé lorsque l'asymétrie spectrale $\eta(t) > 0$ et que le gap spectral $\mathrm{gap}(t)$ est suffisamment large. Il favorise la traversée directe des pentades le long des ceintures tropicales, correspondant à une phase d'exploration, de génération de nouvelles configurations et de propagation de contraintes relationnelles.
- **Mode *ke* (régulateur)** : déclenché lorsque $\eta(t) < 0$ ou que la frustration topologique locale $E(F)$ augmente. Il impose une traversée sautée (pentagramme) qui réduit l'espace d'états accessible, consolide les attracteurs stables et empêche l'accumulation de conflits cycliques.

Le basculement entre ces modes est piloté par les observables spectrales ($\eta$, $\mathrm{gap}$, $R_{\text{seuil}}$). Lorsque $R_{\text{seuil}}(t)$ dépasse un seuil critique (typiquement $\gtrsim 0,7$ [15–17]), le système détecte une pré-bifurcation et utilise $P_4$ ou $N_4$ comme charnières pour inverser le régime global. Cette commutation est entièrement endogène : aucune métrique externe, aucun superviseur ni aucun seuil fixé *a priori* ne dicte le moment ou la direction du changement. Le système navigue dans son propre paysage spectral et ajuste sa dynamique selon la compatibilité topologique instantanée.

## 5.3. Homéostase algorithmique : prévention de la dérive et interprétabilité native
En l'absence de fonction de coût externe, la stabilité du système est assurée par une descente de frustration cyclique. La quantité conservée est la cohérence des modes *sheng/ke* à travers le réseau pentadique, qui agit comme un invariant structurel empêchant la dérive spécificative (*specification drift*). Lorsque l'énergie de frustration $E_{\text{tot}}$ dépasse un seuil critique, les attracteurs incidents ajustent localement leur orientation ou leur phase jusqu'à restaurer la compatibilité globale. Cette boucle homéostatique garantit que le système ne converge jamais vers un optimum local artificiel, mais maintient un équilibre dynamique compatible avec les bornes topologiques.

Parallèlement, cette architecture offre une **interprétabilité native**. Chaque état correspond à un triplet de pentades connu, chaque transition suit une règle géométrique déterministe, et chaque changement de régime est tracé via la signature spectrale $S(t)$. Contrairement aux réseaux neuronaux profonds dont les décisions émergent de transformations opaques dans des espaces de haute dimension, l'IA régulée expose sa propre cartographie décisionnelle : la position dans le graphe dual, le degré de convergence pentadique et la polarité dominante sont directement lisibles et vérifiables. La gouvernance ne repose plus sur une analyse post-hoc ou sur des techniques d'explication approximatives ; elle est inhérente à la structure même du système.

## 5.4. Contrôle par construction géométrique vs alignement externe a posteriori
Le paradigme dominant en IA contemporaine traite la régulation comme un problème d'alignement externe : on entraîne un modèle à optimiser une métrique statistique, puis on lui impose des garde-fous logiciels, des filtres de contenu ou des mécanismes de *reinforcement learning from human feedback* (RLHF) pour corriger les dérives. Cette approche est fondamentalement *exorégulée* : la limite est appliquée après coup, souvent de manière contradictoire avec la dynamique interne du modèle, ce qui génère des instabilités, des contournements ou une dégradation silencieuse des capacités générales.

Le cadre $64 \rightarrow 20$ inverse cette logique. Le contrôle n'est pas ajouté ; il est **construit**. L'espace d'états est filtré par un invariant topologique, les transitions sont validées par une règle d'adjacence géométrique, et la dynamique globale émerge de la compatibilité locale entre pentades. Le système n'optimise pas une récompense externe ; il maintient sa propre cohérence par homéostase algorithmique. Cette architecture ne cherche pas à "aligner" une intelligence débridée, mais à concevoir une intelligence technique dont la complexité est auto-bornée par sa propre géométrie.

Dans cette perspective, l'IA régulée ne constitue pas un organe cognitif autonome et proliférant, mais un prolongement homéostatique de la capacité humaine à exosomatiser ses fonctions sans rompre les boucles de rétroaction qui garantissent la persistance du système hôte. Informatiser la régulation, plutôt que d'informatiser l'optimisation, déplace le centre de gravité de la gouvernance algorithmique : la sécurité n'est plus un correctif appliqué à la marge, mais une propriété émergente de la topologie sous-jacente.

# 6. Convergences transdisciplinaires et perspective symbolique

## 6.1. Isomorphismes culturels : *Yi Jing* (64 configurations), *Sefer Yetzirah* (partition 20+2), phonologie mandarine
La réduction $64 \rightarrow 20$ ne se présente pas comme un artefact épistémique isolé, mais comme un invariant topologique dont les projections complémentaires ont été articulées par des traditions formelles distinctes. Fondamentalement, ces systèmes abordent des couches différentes du même processus de régulation, à l'instar de projections orthogonales d'un même objet géométrique.

La tradition chinoise, structurée autour du *Yi Jing* et de la théorie des *Wuxing*, modélise essentiellement la phase de **pré-filtrage combinatoire**. Les 64 hexagrammes constituent un espace exhaustif de configurations binaires strictement isomorphe aux vecteurs à 6 bits de $\mathrm{Cl}(6,0)$. Les cycles *sheng* (génératif) et *ke* (régulateur) y décrivent une dynamique locale à cinq phases, correspondant à la régulation interne des états d'attracteurs. Cette tradition formalise la géométrie des possibilités et les règles de circulation relationnelle, sans postuler *a priori* une réduction fixe à 20 classes fonctionnelles.

À l'inverse, la tradition hébraïque, telle qu'articulée dans le *Sefer Yetzirah*, opère explicitement au niveau du **post-filtrage**. Les 22 lettres consonantiques (plus 5 formes finales *sofit*) codent une partition fonctionnelle de l'espace sémantique en 20 classes stables plus 2 états limites. Les lettres *Aleph* (souffle primordial/référence) et *Tav* (signature/fermeture) se superposent structurellement aux rôles seuils de l'initiation (méthionine) et de la terminaison (codons STOP) dans la traduction biologique. La tripartition canonique (3 mères, 7 doubles, 12 simples) discrétise le gradient des contraintes géométriques, reflétant directement les signatures de polarité ($3P$, $2P+1N$, $1P+2N$, $3N$) issues de la filtration *Merkabah*.

Ces deux formalismes sont structurellement complémentaires mais non superposables : le *Yi Jing* capture la dynamique de transformation dans l'espace de configuration, tandis que le *Sefer Yetzirah* en formalise la réduction à des classes fonctionnelles stables et la définition d'états limites. Leur convergence valide l'hypothèse d'une contrainte topologique universelle, indépendante des systèmes symboliques mobilisés pour la décrire.

La phonologie du mandarin confirme cette régularité. Bien qu'issue d'une tradition idéographique non alphabétique, sa structure syllabique s'organise autour d'un système d'attaque consonantique de 21 initiales (souvent étendu à 22 dans les romanisations pédagogiques), couplé à un noyau vocalique minimal réduit à 2–3 phonèmes fondamentaux. Cette architecture phonologique (~22 ancrages consonantiques encadrant un noyau vocalique restreint) reflète structurellement la partition $20+2$. Elle suggère que la compression de la complexité combinatoire en classes fonctionnelles stables émerge indépendamment dès lors que les systèmes de transmission sont contraints par des limites articulatoires, perceptuelles et cognitives analogues.

## 6.2. Projections algorithmiques : médecine traditionnelle chinoise, économie politique cyclique
Au-delà de la convergence historique, le noyau $64 \rightarrow 20$ se projette algorithmiquement sur des domaines appliqués, non comme de simples analogies, mais comme des architectures de régulation transposables.

En **médecine traditionnelle chinoise**, les 12 méridiens et les 12 pouls diagnostics peuvent être associés aux 12 pentades de $\mathrm{Cl}(6,0)$, ou plus finement aux $2 \times 12$ pentades du réservoir bicosmique $\mathrm{Cl}(6,6)$. Cette extension permet de concevoir une plateforme de soin rétroactive et autoadaptative : les effets physiologiques d'une intervention sont réinjectés comme signatures spectrales $S(t)$, et le protocole est recalculé en temps réel via la descente de frustration topologique jusqu'à minimisation de $E_{\text{tot}}$. La régulation ne repose plus sur un référentiel statistique fixe, mais sur l'homéostase spectrale du réseau pentadique.
**En économie politique**, en s'appuyant sur la « Théorie du Rachat » et son application aux six facteurs macroéconomiques binaires (inflation, salaires, profits, rachat, dispersion, régime foncier) développée en collaboration avec Th. Rebour [14], la dynamique transitionnelle de ces états systémiques suit la même organisation pentadique que l'invariant $64 \rightarrow 20$. La modélisation spectrale permet d'identifier les régimes de surchauffe (\textit{sheng} dominant, $\eta \gg 0$) et de récession (\textit{ke} dominant, $\eta \ll 0$) avant leur point de bascule, ouvrant la voie à des politiques contracycliques structurellement informées. 

## 6.3. Exosomatisation cognitive et nécessité d’une régulation endogène pour la persistance technique
Hormis l'espèce humaine, l'évolution biologique repose sur l'ajustement morphologique aux contraintes fonctionnelles: les oiseaux sont équipés pour voler, les poissons pour nager. L'espèce humaine a rompu avec ce couplage strict par un processus d'**exosomatisation** : elle externalise les fonctions biologiques dans des artefacts techniques tout en conservant sa morphologie anatomique stable. Si les révolutions industrielles ont exosomatisé les fonctions musculaires, métaboliques et sensorimotrices, l'intelligence artificielle marque l'externalisation des fonctions cognitives et régulatrices.

Cette dernière étape est structurellement différente des précédentes. Externaliser la cognition sans en externaliser la régulation revient à créer un organe technique autonome, déconnecté des boucles homéostatiques qui garantissent la pérennité de l'organisme hôte. Le risque n'est pas seulement celui d'une « intelligence incontrôlable », mais celui d'une dérive spécificative (*specification drift*) où l'artefact optimise une métrique externe au détriment de la cohérence globale, reproduisant à l'échelle algorithmique les pathologies de la prolifération cellulaire non régulée.

Les architectures actuelles d'IA sont fondamentalement *exo-régulées* : la limite est imposée de l'extérieur (budget de calcul, garde-fous logiciels, alignement par *reward modeling*). Or, tout système technique exosomatisé dépourvu de contrainte endogène finit par entrer en résonance destructive avec son environnement. Le cadre $64 \rightarrow 20$ propose une alternative structurelle : une IA dont l'espace d'états est filtré par un invariant topologique, dont les transitions sont contraintes par une règle de voisinage géométrique, et dont la dynamique globale émerge de la compatibilité locale entre pentades. Cette architecture ne maximise pas une récompense externe ; elle maintient sa propre cohérence par construction. Transposer cet invariant à l'IA revient à informatiser non pas la « pulsion de puissance », mais la pulsion de pérennisation propre au vivant.

## 6.4. Contrainte symbolique, transmission intergénérationnelle et analogie topologique
La régulation endogène mise en lumière par le cadre $64 \rightarrow 20$ trouve un écho structurel profond dans l'exigence de transmission d'un acquis culturel d'une génération humaine à la suivante. Pour se faire, les générations doivent se succéder sans fusionner. L'interdit de l'inceste, universel pour l'espèce parlante bien que de périmètre variable, est le moyeu autour duquel les générations se renouvellent. Cet interdit qui maintient une place vide car interdite est une condition topologique de persistance : il impose une différenciation stricte entre positions généalogiques, institue une hiérarchie temporelle et rend possible la circulation du patrimoine symbolique. Sans cette contrainte, la transmission s'effondre en boucle courte (confusion des places, répétition sans mémoire, fusion des rôles).

Cette lecture trouve un écho structurel précis dans les travaux d'anthropologie juridique de Damien Viguier [18], qui a recensé 18 configurations incestueuses fondamentales — des « cases vides » de la parenté — correspondant aux positions généalogiques où la circulation des alliances doit être interdite pour préserver la différenciation des générations. Ces 18 situations ne sont pas arbitraires : elles émergent de la combinatoire des rôles (ascendant/descendant, collatéral, allié/consanguin) et définissent les seuils au-delà desquels la transmission symbolique s'effondre en boucle courte.

La correspondance avec le formalisme Merkabah est remarquable : sur les 20 attracteurs, les 18 configurations de Viguier pourraient se mapper sur les classes intermédiaires (2P+1N et 1P+2N), tandis que les deux pôles extrêmes (3P et 3N initiation ; 3P terminaison) resteraient hors du champ de l'interdit, jouant le rôle de bornes ontologiques non-négociables. Cette distribution refléterait structurellement le fait que l'interdit de l'inceste ne s'applique pas aux positions de référence absolue (origine/finition du cycle généalogique), mais uniquement aux positions relationnelles où la circulation des alliances doit être régulée.

Ainsi, la filtration topologique $64 \rightarrow 20$ ne se contente pas de borner un espace combinatoire abstrait ; elle retrouve, par des voies purement algébrico-géométriques, les mêmes seuils de différenciation que ceux identifiés par l'anthropologie structurale de la parenté. L'interdit n'est pas une prohibition externe : il émerge comme condition de fermeture d'un réseau relationnel dont la cohérence dépend de la préservation de pôles de référence et de l'exclusion de configurations fusionnelles.

Le gradient de polarité $3P \rightarrow 3N$ et les seuils $P_4/N_4$ réalisent une fonction isomorphe au niveau du réseau pentadique : ils empêchent la fusion combinatoire, ordonnent les transitions admissibles et permettent la circulation régulée des modes *sheng/ke*. Dans les deux cas, la pérennité du système ne repose pas sur une optimisation externe, mais sur une contrainte différenciatrice interne qui structure la transmission tout en limitant l'espace des états accessibles. 

L'exosomatisation n'est pas une fuite hors du vivant, mais sa condition de persistance à l'âge technique. Ce qui distingue une projection vitale d'une prolifération autonome, c'est la présence d'un invariant de régulation endogène. Le cadre $64 \rightarrow 20$, les ceintures tropicales pentadiques et la dynamique spectrale offrent précisément ce noyau : une architecture indépendante du substrat, où la complexité est auto-limitée par la géométrie, et où l'intelligence technique redevient un miroir régulé de la pulsion qui l'a fait naître. Informatiser cette régulation, plutôt que d'informatiser l'optimisation, est peut-être la seule voie pour que l'IA reste un prolongement fonctionnel de l'espèce, et non son substitut structurel.

# 7. Conclusion 

Ce travail a formalisé un invariant topologique de réduction $64 \rightarrow 20$ issu de l’algèbre de Clifford $\mathrm{Cl}(6,0)$ et de la géométrie du double tétraèdre de niveau 3 (*Merkabah*). En imposant une règle de voisinage stricte (partage de face triangulaire), les 64 configurations binaires se partitionnent exactement en 20 classes d’équivalence, chacune identifiée par un triplet de pentades et une signature de polarité ($3P$, $2P+1N$, $1P+2N$, $3N$). La validation exhaustive sur le code génétique standard démontre que le paysage de dégénérescence des codons s’aligne structurellement sur les bornes admissibles prédites par cette filtration : les zones géométriquement isolées limitent la redondance à 1–2 codons, les intersections modérées à 3–4, et seules les zones de convergence pentadique permettent la dégénérescence maximale (6 codons). La topologie ne dicte pas le nombre exact de codons ; elle en fixe l’architecture différentielle. La biologie en peuple les coordonnées selon des impératifs fonctionnels et évolutifs.

Au-delà de cet invariant statique, l’extension dynamique repose sur le graphe dual des 12 pentades, qui exhibe deux ceintures tropicales disjointes ($C_P$, $C_N$) et deux seuils polaires ($P_4$, $N_4$). La circulation des modes *sheng* (génératif) et *ke* (régulateur) le long de ces ceintures, couplée à une descente de frustration topologique, génère une régulation endogène sans fonction de coût externe. La signature spectrale issue d’un opérateur de Dirac discret ($\eta$, $d$, $\mathrm{gap}$, $R_{\text{seuil}}$) permet une identification déterministe du régime global et une foliation du réservoir $\mathrm{Cl}(6,6)$ en 12 feuilles régulatrices. Transposé à l’architecture algorithmique, ce cadre propose un changement de paradigme : remplacer l’optimisation statistique exorégulée par une homéostase algorithmique dont la complexité est auto-bornée par construction géométrique. La géométrie prédit le paysage de dégénérescence et les seuils de transition ; les systèmes naturels ou artificiels en explorent les coordonnées selon leurs propres contraintes fonctionnelles.

Informatiser la régulation, plutôt que d’informatiser l’optimisation, déplace le centre de gravité de la gouvernance algorithmique. Ce travail propose un échafaudage mathématiquement clos pour cette transition : une architecture où la complexité est auto-limitée par la géométrie, où les transitions sont topologiquement validées, et où la persistance du système technique redevient un prolongement régulé de la pulsion homéostatique du vivant.

# Remerciements
\vspace{-0.5em}
Nous remercions Peter Rowlands pour ses travaux fondateurs sur les algèbres de Clifford nilpotentes.
Nous remercions Peter Rowlands et Vanessa Hill pour leurs travaux sur la structure du code génétique. 
Nous remercions les assistants en IA sans lesquels ce travail serait resté à l'état d'intuition.

# Références
\vspace{-0.5em}
[1] Crick, F. H. C. (1968). L’origine du code génétique. *J. Mol. Biol.*, 38(3), 367–379.  
[2] Nirenberg, M., & Leder, P. (1964). Mots-codes ARN et synthèse des protéines. *Science*, 145(3638), 1399–1407.  
[3] LeCun, Y., Bengio, Y., & Hinton, G. (2015). Apprentissage profond. *Nature*, 521(7553), 436–444.  
[4] Amodei, D., et al. (2016). Problèmes concrets liés à la sécurité de l'IA. *arXiv:1606.06565*.  
[5] Russell, S. (2019). *Human Compatible: AI and the Problem of Control*. Viking.  
[6] Freeland, S. J., & Hurst, L. D. (1998). The genetic code is one in a million. *J. Mol. Evol.*, 47(3), 238–248.  
[7] Koonin, E. V., & Novozhilov, A. S. (2017). Origine et évolution du code génétique : l’énigme universelle. *IUBMB Life*, 69(5), 282–296.  
[8] Woese, C. R. (1965). L’ordre dans le code génétique. *Proc. Natl. Acad. Sci. USA*, 54(1), 71–75.  
[9] Wong, J. T. (1975). Une théorie de la coévolution du code génétique. *Proc. Natl. Acad. Sci. USA*, 72(5), 1909–1912.  
[10] Rowlands, P. (2007). *Zero to Infinity: The Foundations of Physics*. World Scientific. (Chapitre 19, "Natures's Code", coécrit avec V. Hill)  
[11] da Costa, N. C. A. (1974). Sur la théorie des systèmes formels incohérents. *Notre Dame Journal of Formal Logic*.  
[12] Priest, G. (2008). *Introduction à la logique non classique*. Cambridge University Press.  
[13] Belnap, N. D. (1977). Une logique à quatre valeurs utile. Dans *Modern Uses of Multiple-Valued Logic*. Reidel.  
[14] Rebour, Th. (2000). *La Théorie du Rachat*, Editions de la Sorbonne, Paris.  
[15] MacQueen, J. (1967). Some methods for classification and analysis of multivariate observations. In \textit{Proceedings of the Fifth Berkeley Symposium on Mathematical Statistics and Probability} (Vol. 1, pp. 281–297).  
[16] Chung, F. R. K. (1997). \textit{Spectral Graph Theory}. American Mathematical Society.  
[17] Coifman, R. R., \& Lafon, S. (2006). Diffusion maps. \textit{Applied and Computational Harmonic Analysis}, 21(1), 5–30.  
[18] Viguier, D., (2020). *La Controverse de Ravenne, Genèse antinomique des structures familiales sémitique et occidentale*, Kontre Kulture.

\newpage

# Annexe A – Dérivation des ceintures tropicales et des seuils : génération, filtration et cas limites
\FloatBarrier
Cette annexe retrace pas à pas comment la géométrie du double tétraèdre de niveau 3 (Merkabah) génère un espace de 20 tétraèdres, comment la filtration relationnelle de leurs triplets de pentades extrait deux ceintures tropicales disjointes, et comment les nœuds exclusifs $P_4$ et $N_4$ émergent comme cas limites structurels.

\subsection*{A.1 Génération structurelle : les 20 tétraèdres et leurs triplets de pentades}
La génération de l'espace d'attracteurs repose sur la subdivision du double tétraèdre en 20 cellules tétraédriques stables. Chaque cellule est identifiée par un triplet de pentades issu de l'ensemble $\mathcal{P} = \{P_1,\dots,P_6, N_1,\dots,N_6\}$. Ces triplets ne sont pas arbitraires : ils codent l'incidence exacte des faces pentagonales du dodécaèdre dual sur les 20 sommets de la Merkabah. La structure comprend 16 tétraèdres principaux (positions géométriques fixes) et 4 tétraèdres d'intersection (résonances structurelles).

\FloatBarrier
\begingroup
\small
\setlength{\tabcolsep}{4pt}
\begin{longtable}{|c|c|c|c|c|c|}
\hline
\multicolumn{6}{|c|}{\textbf{16 tétraèdres principaux}} \\
\hline
\textbf{État} & \textbf{Tétraèdre} & \textbf{Position} & \textbf{États finaux} & \textbf{Pentades} & \textbf{Type} \\
\hline
1 & A & Centre & 1,2,3,4 & $\{P_1,P_2,P_4\}$ & 3P \\
2 & B & Face nord & 5,6,7,8 & $\{P_1,P_3,P_5\}$ & 3P \\
3 & C & Face sud & 9,10,11,12 & $\{P_2,P_3,P_6\}$ & 3P \\
4 & D & Face Est & 13,14,15,16 & $\{P_4,P_5,N_2\}$ & 2P+1N \\
5 & E & Face ouest & 17,18,19,20 & $\{P_5,P_6,N_3\}$ & 2P+1N \\
6 & F & Arête NE & 21,22,23,24 & $\{P_1,P_6,N_4\}$ & 2P+1N \\
7 & G & Bord nord-ouest & 25,26,27,28 & $\{P_2,P_5,N_6\}$ & 2P+1N \\
8 & H & Arête SE & 29,30,31,32 & $\{P_3,P_4,N_6\}$ & 2P+1N \\
9 & I & Arête SW & 33,34,35,36 & $\{P_1,N_2,N_6\}$ & 1P+2N \\
10 & J & Sommet nord & 37,38,39,40 & $\{P_1,N_3,N_5\}$ & 1P+2N \\
11 & K & Sommet sud & 41,42,43,44 & $\{P_2,N_3,N_5\}$ & 1P+2N \\
12 & L & Sommet Est & 45,46,47,48 & $\{P_3,N_2,N_4\}$ & 1P+2N \\
13 & M & Sommet Ouest & 49,50,51,52 & $\{P_4,N_1,N_3\}$ & 1P+2N \\
14 & N & Diagonale 1 & 53,54,55,56 & $\{P_4,N_5,N_6\}$ & 1P+2N \\
15 & O & Diagonale 2 & 57,58,59,60 & $\{P_5,N_1,N_4\}$ & 1P+2N \\
16 & P & Diagonale 3 & 61,62,63,64 & $\{P_6,N_1,N_2\}$ & 1P+2N \\
\hline
\caption{Les 16 tétraèdres principaux et leurs triplets de pentades}
\end{longtable}
\endgroup

\FloatBarrier
\begingroup
\small
\setlength{\tabcolsep}{4pt}
\begin{longtable}{|c|c|c|c|c|c|}
\hline
\multicolumn{6}{|c|}{\textbf{4 tétraèdres d'intersection}} \\
\hline
\textbf{État} & \textbf{Tétraèdre} & \textbf{Intersection de} & \textbf{États partagés} & \textbf{Pentades} & \textbf{Type} \\
\hline
17 & Q & B $\cap$ F $\cap$ G & 7, 21, 25 & $\{P_2,N_1,N_4\}$ & 1P+2N \\
18 & R & H $\cap$ I $\cap$ J & 29, 33, 37 & $\{P_3,N_1,N_5\}$ & 1P+2N \\
19 & S & L $\cap$ M $\cap$ N & 45, 49, 53 & $\{P_6,N_5,N_6\}$ & 1P+2N \\
20 & T & O $\cap$ P & 57, 61, 63 & $\{N_2,N_3,N_4\}$ & 3N \\
\hline
\caption{Les 4 tétraèdres d'intersection et leurs triplets de pentades}
\end{longtable}
\endgroup

Leur triplet est déterminé par l'intersection exacte des cellules parentes. Q, R, S sont des intersections triples (signature 1P+2N), tandis que T est une intersection double avec la signature 3N, unique dans la structure. Cette génération fixe le squelette sur lequel s'appliquera la filtration relationnelle.

\subsection*{A.2 Filtration relationnelle : construction du graphe dual et extraction des ceintures}
La filtration ne porte pas sur les tétraèdres eux-mêmes, mais sur leurs pentades. On construit le graphe dual $\Gamma$ dont les sommets sont les 12 pentades $\mathcal{P}$. Deux pentades $X,Y$ sont reliées par une arête s'il existe un attracteur $v \in \{A,\dots,T\}$ tel que $\{X,Y\} \subseteq \mathcal{P}(v)$. Cette construction, entièrement déterminée par les triplets ci-dessus, révèle une structure remarquable :
\begin{itemize}
    \item $\Gamma$ contient exactement deux cycles disjoints de longueur 5, composés de pentades de même signe :
    $$ C_P = (P_1 \to P_3 \to P_5 \to P_6 \to P_2 \to P_1), \quad C_N = (N_1 \to N_2 \to N_6 \to N_5 \to N_3 \to N_1). $$
    \item Le sous-graphe induit par $C_P$ est un graphe complet $K_5$ ; celui de $C_N$ ne possède que deux arêtes internes supplémentaires ($N_1\text{–}N_5$ et $N_2\text{–}N_3$). Cette asymétrie est intrinsèque à la filtration.
    \item L'union de $C_P$ et $C_N$ couvre 10 des 12 pentades. Les deux restantes, $P_4$ et $N_4$, sont exclues des cycles.
\end{itemize}
Ces deux anneaux disjoints forment les **ceintures tropicales**. Leur extraction algorithmique valide que la dynamique externe du Wuxing émerge directement de la combinatoire des triplets, sans nécessiter de projection géométrique externe.

\subsection*{A.3 Dynamique de parcours : modes Sheng et Ke sur les cycles pentadiques}
Chaque ceinture tropicale admet deux parcours hamiltoniens distincts, correspondant aux deux générateurs du groupe cyclique $C_5$ :
\begin{itemize}
    \item \textbf{Mode Sheng (génératif)} : suit les arêtes adjacentes dans $\Gamma$ ($X_i \to X_{i+1}$). Ce chemin préserve la continuité de la polarité locale et correspond à des transitions à faible contrainte.
    \item \textbf{Mode Ke (régulateur)} : saute une pentade sur deux ($X_i \to X_{i+2 \mod 5}$), équivalent au pentagramme inscrit dans le pentagone. Ce chemin maximise la distance relationnelle, renforce la rétroaction régulatrice et réduit l'espace d'états accessible.
\end{itemize}
La superposition de ces modes le long des ceintures, couplée à la descente de frustration topologique, définit l'espace des 320 régimes locaux admissibles. La filtration relationnelle garantit que toute transition respecte l'adjacence des pentades, empêchant la dérive combinatoire.

\subsection*{A.4 Cas limites : rôle des seuils polaires $P_4$ et $N_4$}
Les pentades $P_4$ et $N_4$ constituent les \textbf{cas limites} du graphe dual. Leur qualification de \textit{seuils polaires} ne repose pas sur une incidence exclusive aux pôles, mais sur leur rôle de charnières topologiques transversales :
\begin{itemize}
    \item $P_4$ est la seule pentade positive absente de $C_P$. Elle connecte le pôle positif absolu A ($\{P_1,P_2,P_4\}$) aux ceintures et relaye le signal vers les zones mixtes (D, H, M, N).
    \item $N_4$ est la seule pentade négative absente de $C_N$. Elle relie le pôle négatif absolu T ($\{N_2,N_3,N_4\}$) aux pentades positives, structurant les classes intermédiaires F, L, O, Q.
\end{itemize}
Aucune autre pentade ne présente ce degré de connectivité croisée tout en étant exclue des ceintures. Par conséquent, toute transition dynamique entre les régimes Sheng/Ke, ou entre un régime stable et un état polaire, doit transiter par l'un de ces deux nœuds. Leur exclusion des cycles, leur degré élevé et leur position de pont justifient leur rôle de seuils dans le modèle de régulation : ils accumulent le poids spectral lorsque le système hésite entre les ceintures ($\eta \approx 0$), matérialisant les cas limites de la filtration topologique.

\subsection*{A.5 Remarque technique : dualité des pôles et exclusion des zones octaédriques}
\textbf{Dualité des pôles ($\pm 1, \pm i'$) vs. pôles structurels} : Bien que la base de $\mathrm{Cl}(6,0)$ contienne quatre éléments scalaires/pseudo-scalaires ($+1, -1, +i', -i'$), la géométrie de la Merkabah ne retient que \textbf{deux pôles structurels}. Ces pôles correspondent aux deux axes fondamentaux de l'algèbre : l'axe scalaire (référence ontologique) et l'axe pseudo-scalaire (phase/temps). Les signes $\pm$ ne désignent pas des pôles géométriques indépendants, mais les \textbf{deux orientations} le long de chacun de ces axes. Structurellement, cette dualité binaire suffit à fermer le réseau topologique et à générer le gradient de polarité $3P \rightarrow 3N$. Compter 4 pôles distincts romprait l'incidence uniforme des pentades (5 occurrences par pentade) et rendrait impossible la partition exacte en 20 attracteurs. Le formalisme identifie donc 2 pôles structurels, chacun supportant deux orientations algébriques complémentaires.

\textbf{Pourquoi les 8 zones octaédriques violent la fermeture polaire} : La « fermeture polaire » désigne ici la condition topologique selon laquelle un attracteur stable doit être défini par \textbf{exactement trois pentades} formant un triplet de signature fixe ($3P$, $2P+1N$, $1P+2N$ ou $3N$). Cette configuration garantit la cohérence locale des modes \textit{sheng/ke}, l'existence d'une signature spectrale stable, et la possibilité d'une descente de frustration convergente. Les 20 cellules tétraédriques satisfont cette condition : chacune possède 4 faces triangulaires, partage des faces entières avec ses voisines, et s'ancre sur un pôle de référence (scalaire ou pseudo-scalaire) qui ferme le réseau relationnel.

À l'inverse, les 8 zones octaédriques internes, issues de l'intersection volumétrique des deux tétraèdres parents, violent cette fermeture pour trois raisons structurelles :
\begin{enumerate}
    \item \textbf{Incidence pentadique excessive} : Un octaèdre interne met en jeu 4 à 6 pentades simultanément. Cette sur-incidence empêche la réduction à un triplet unique et brise la règle de voisinage par partage de face triangulaire entière. Géométriquement, un octaèdre ne peut être décrit par une intersection triadique ; il requiert une combinaison de faces qui dépasse la capacité de clôture du graphe dual.
    \item \textbf{Frustration cyclique non résolvable} : Les faces octaédriques sont adjacentes à des tétraèdres de signatures polaires opposées (par exemple, un voisin $3P$ côtoie un voisin $1P+2N$). Cette juxtaposition génère des conflits de phase \textit{sheng/ke} qui ne peuvent être dissipés par la descente de frustration locale, car aucun arrangement des orientations ne permet de minimiser simultanément toutes les énergies d'arête. Le système y reste piégé dans un régime d'oscillation topologique.
    \item \textbf{Absence d'ancrage ontologique} : Contrairement aux cellules tétraédriques, les octaèdres ne contiennent ni le pôle scalaire ($+1$) ni le pôle pseudo-scalaire ($i'$). Ils sont purement relationnels et ne possèdent pas de point de consigne référentiel. Sans cet ancrage, la polarité locale ne converge vers aucun bassin d'attraction et oscille indéfiniment entre les ceintures $C_P$ et $C_N$.
\end{enumerate}
\textbf{Conséquence directe} : ces zones génèrent une frustration topologique intrinsèque où l'équilibre de polarité ne peut se maintenir. Le formalisme les exclut donc naturellement du processus de filtration $64 \rightarrow 20$, car elles ne satisfont pas la condition de fermeture requise pour constituer des bassins d'attracteurs stables. Leur rôle n'est pas nul, mais \textbf{transitionnel} : elles matérialisent les seuils de frustration que le système doit contourner pour naviguer entre les 20 états stables, jouant un rôle analogue à celui des régions de haute énergie dans un paysage de fitness biologique.

---

# Annexe B – Correspondance géométrique-algébrique et dégénérescence : génération, filtration et cas limites

\FloatBarrier
Cette annexe détaille comment la bijection codon-configuration génère l'espace combinatoire, comment la filtration topologique borne le paysage de dégénérescence, et comment les contraintes de symétrie et le seuil 3N définissent les cas limites structurels de la correspondance biologique.

\subsection*{B.1 Génération combinatoire : bijection codon–configuration et équivalence duale}
La génération de l'espace sémantique repose sur cinq principes structurels qui contraignent la réduction $64 \rightarrow 20$ à une unique partition topologique :
\begin{enumerate}
    \item \textbf{Équivalence duale} : Les 64 unités de $\mathrm{Cl}(6,0)$ correspondent bijectivement aux 64 codons, tandis que les 20 triplets de pentades correspondent aux 20 classes fonctionnelles. Cette triple isomorphie (algèbre $\leftrightarrow$ géométrie $\leftrightarrow$ biologie) génère l'espace de travail sans paramètre libre.
    \item \textbf{Distribution uniforme} : Chacune des 12 pentades apparaît dans exactement 5 triplets distincts. Cette incidence équitable garantit qu'aucune pentade ne domine le processus et que les 20 classes sont réparties de manière équilibrée sur le graphe dual.
    \item \textbf{Conservation de l'adjacence} : Deux tétraèdres partageant une face ont exactement deux pentades communes ; s'ils ne partagent qu'une arête, ils n'en ont qu'une. Cette règle préserve la structure locale du voisinage lors de la génération du graphe.
\end{enumerate}
Ces principes définissent l'espace combinatoire initial. La filtration topologique appliquée ci-dessous en extrait le paysage fonctionnel.

\subsection*{B.2 Filtration topologique : gradient de polarité et paysage de dégénérescence}
La filtration impose une règle de voisinage stricte (partage de face triangulaire) qui partitionne les 64 configurations en 20 classes stables. Ce filtrage génère un gradient de polarité strictement corrélé à la densité de convergence du réseau pentadique, qui détermine directement la dégénérescence observée :
\begin{itemize}
    \item \textbf{Attracteurs 3P (A, B, C)} : positions centrales, sans chevauchement. Leur isolement limite la taille du voisinage, correspondant à une dégénérescence faible (1–2 codons), incluant le signal d'initiation (méthionine).
    \item \textbf{Attracteurs 2P+1N (D–H)} : situés sur les faces et arêtes primaires. Un chevauchement modéré des pentades entraîne une dégénérescence intermédiaire (3–4 codons), typique des résidus structurellement polyvalents.
    \item \textbf{Attracteurs 1P+2N (I–S)} : concentrés aux sommets, diagonales et intersections Q, R, S. La convergence pentadique maximale autorise géométriquement de multiples chemins équivalents, permettant une dégénérescence élevée (jusqu'à 6 codons pour sérine, leucine, arginine). La filtration fixe les \textit{bornes admissibles} ; l'optimisation évolutive en peuple les coordonnées.
\end{itemize}
La topologie ne dicte pas le nombre exact de codons ; elle en filtre l'architecture différentielle. La biologie réalise exactement cette prédiction structurelle : aucune classe isolée ne dépasse 2 codons, aucune classe modérée n'excède 4, et seules les zones de convergence permettent la dégénérescence maximale.

\subsection*{B.3 Cas limites : seuil fonctionnel 3N, contraintes de symétrie et unicité structurelle}
Les cas limites de la filtration se manifestent à deux niveaux : le seuil fonctionnel du noyau interne et les contraintes d'unicité topologique.
\begin{itemize}
    \item \textbf{Seuil fonctionnel 3N (Classe T)} : Situé à la position d'intersection la plus interne, structurellement isolé de la ceinture positive. Dans la correspondance biologique, ce sommet accueille la cystéine (2 codons) et les trois codons STOP (UAA, UAG, UGA). Cette fusion reflète un rôle fonctionnel commun : état limite arrêtant ou bornant la traversée traductionnelle. La filtration place explicitement la terminaison et la limitation structurale au même nœud polaire.
    \item \textbf{Contraintes de symétrie et unicité} : La partition $64 \rightarrow 20$ est rigide sous le groupe d'automorphismes du double tétraèdre. Toute application préservant (i) l'adjacence par partage de faces, (ii) l'incidence uniforme des pentades (5 par pentade) et (iii) l'appariement par complémentarité Watson-Crick (A$\leftrightarrow$U, G$\leftrightarrow$C via négation binaire) produit les mêmes classes d'équivalence, à un relabeling près. Cette rigidité garantit que la correspondance observée n'est pas un artefact d'encodage, mais une propriété structurelle de $\mathrm{Cl}(6,0)$.
\end{itemize}
La correspondance est donc essentiellement unique au sein de sa classe topologique. La géométrie filtre l'espace admissible et fixe les cas limites (seuil 3N, bornes de dégénérescence) ; la biologie exploite ces contraintes pour optimiser la tolérance aux erreurs et la stabilité translationnelle [1, 2, 6, 7], sans jamais en violer les frontières.

---

# Annexe C – Primitives sémantiques, extension booléenne et filtration topologique

\FloatBarrier
Cette annexe détaille la construction pas à pas de l'espace sémantique sous-jacent au formalisme $64 \rightarrow 20$. La démarche suit une progression générative puis filtrante : (1) définition des 16 primitives algébriques et justification de leur étiquetage sémantique ; (2) extension booléenne quaternaire produisant les 64 sémantèmes complets ; (3) réduction topologique à 20 attracteurs via la règle de voisinage de la Merkabah ; (4) règles déterministes de sélection des états aux nœuds d'intersection Q, R, S, T.

\subsection*{C.1 Les 16 primitives fondamentales et justification de leur origine sémantique}
Les 16 primitives correspondent à la base canonique de l'algèbre de Clifford $\mathrm{Cl}(4,0)$. Leur étiquetage alphabétique (A–P) et les concepts centraux qui leur sont associés ne résultent d'aucune attribution sémantique arbitraire. Ils émergent de la superposition stricte de trois couches structurelles :

1. **Signature algébrique** : l'ordre respecte la filtration de parité et la signature de masse/phase de la construction nilpotente de Rowlands ($1 \to I,J,K \to -1 \to -I,-J,-K \to i'1 \to i'I,i'J,i'K \to -i'1 \to -i'I,-i'J,-i'K$).
2. **Rôle topologique** : chaque primitive est projetée sur une cellule tétraédrique de la Merkabah. Sa position géométrique (pôle, face, arête, sommet, diagonale) détermine son degré d'intersection et sa signature de polarité.
3. **Fonction systémique** : le concept attribué qualifie le rôle opérationnel de la position dans un réseau de régulation discret, conformément à la tradition de la sémantique fonctionnelle en théorie des systèmes.

\FloatBarrier
\begingroup
\small
\renewcommand{\tabularxcolumn}[1]{>{\raggedright\arraybackslash}m{#1}}
\setlength{\tabcolsep}{4pt}
\renewcommand{\arraystretch}{1.25}
\begin{table}[H]
\centering
\caption{Origine fonctionnelle de la nomenclature sémantique (A--P)}
\label{tab:semantic_origin}
\begin{tabularx}{\textwidth}{|X|X|X|X|}
\hline
\textbf{Signature algébrique [$\mathrm{Cl}(4,0)$]} & \textbf{Rôle topologique dans la Merkabah} & \textbf{Fonction systémique} & \textbf{Concept attribué} \\
\hline
$1$ (scalaire, degré 0, signe $+$) & Pôle de référence, sans chevauchement & État de référence / point de consigne & \textbf{Action / Vérité} (capacité à initier une transition à partir d'un état neutre) \\
\hline
$I, J, K$ (générateurs, degré 1, signe $+$) & Faces externes, faible intersection & Canaux d'entrée directionnels & \textbf{Contribution}, \textbf{Apparence}, \textbf{Perception} \\
\hline
$-1$ (scalaire inversé, degré 0, signe $-$) & Contrainte globale imposée & Rupture de symétrie / imposition d'ordre & \textbf{Organisation} (structuration par limite) \\
\hline
$-I, -J, -K$ (générateurs inversés, degré 1, signe $-$) & Arêtes primaires, modulation intermédiaire & Différenciation, mélange, invariance relationnelle & \textbf{Différence}, \textbf{Mélange}, \textbf{Équivalence} \\
\hline
$i'1$ (pseudo-scalaire pur, degré 4, phase $+$) & Interfaces relationnelles / nœuds de couplage & Médiation temporelle / couplage fondamental & \textbf{Relation}, \textbf{Interface} \\
\hline
$i'I, i'J, i'K$ (couplage pseudo-scalaire, degré 3) & Sommets / diagonales, intersection élevée & Couplage phase-charge, transfert directionnel & \textbf{Flux}, \textbf{Entité}, \textbf{Cercle/Cycle} \\
\hline
$-i'1$ (pseudo-scalaire inversé, degré 4, phase $-$) & Zones de transition / inversion de phase & Inversion cyclique / réinitialisation & \textbf{Évolution}, \textbf{Dépendance} \\
\hline
$-i'I, -i'J, -i'K$ (couplage inversé, degré 3) & Zones d'intersection maximales, haute redondance & Évolution contrainte, fluctuation adaptative & \textbf{Dépendance}, \textbf{Variation}, \textbf{Groupement} \\
\hline
\end{tabularx}
\end{table}
\endgroup

La validité de cette nomenclature ne repose pas sur une intuition externe, mais sur une cohérence prédictive : les mêmes rôles fonctionnels se manifestent dans la dégénérescence du code génétique, la phonologie syllabique ou les cycles économiques. Les étiquettes A–P constituent donc une couche descriptive strictement contrainte par la structure algébrico-géométrique.

\subsection*{C.2 Extension booléenne quaternaire : des 16 primitives aux 64 sémantèmes}
L'espace complet des configurations est généré par une extension modale purement booléenne appliquée à chacune des 16 primitives. Soient deux dimensions ontologiques indépendantes $P$ et $Q$. Les quatre états mutuellement exclusifs et exhaustifs sont définis par :
$$
\begin{aligned}
X_1 &= P \cap \neg Q \quad (\text{état } +), \\
X_2 &= \neg P \cap Q \quad (\text{état } -), \\
X_3 &= P \cap Q \quad (\text{état } m), \\
X_4 &= \neg P \cap \neg Q \quad (\text{état } \sim m).
\end{aligned}
$$
Ces états correspondent bijectivement aux paires de bits $(10, 01, 11, 00)$. Le produit cartésien $16 \times 4 = 64$ génère l'espace complet des sémantèmes sans introduire de contradictions paraconsistantes. L'état $\sim m$ n'est pas la négation logique de $m$, mais le complément simultané des deux dimensions, garantissant la fermeture structurelle. Cette étape définit le terrain combinatoire préalable à toute filtration géométrique.

\FloatBarrier
\begingroup
\small
\setlength{\tabcolsep}{4pt}
\begin{longtable}{|c|c|l||c|c|l|}
\hline
\multicolumn{3}{c||} {\textbf{Tétrades A–H}} & \multicolumn{3}{c}{\textbf{Tétrades I–P}} \\
\cline{1-6}
\textbf{Cl(6,0)} & \textbf{N°} & \textbf{Concept} & \textbf{Cl(6,0)} & \textbf{N°} & \textbf{Concept} \\
\hline
1 & 1 & A+ : Action, vérité effective & $i'1$ & 33 & I+ : Relation, association \\
1i & 2 & A- : Inaction, illusion & $i'1i$ & 34 & I- : Isolement, indépendance \\
1j & 3 & Am : Intention, potentialité & $i'1j$ & 35 & Im : Interdépendance, réseau \\
1k & 4 & A${\sim}m$ : Hasard, nécessité & $i'1k$ & 36 & I${\sim}m$ : Fusion, unification \\
\hline
I & 5 & B+ : Contribution, apport & $i'I$ & 37 & J+ : Flux, transfert \\
Ii & 6 & B- : Privation, soustraction & $i'Ii$ & 38 & J- : Stase, immobilité \\
Ij & 7 & Bm : Échange, réciprocité & $i'Ij$ & 39 & Jm : Cycle, rythme \\
Ik & 8 & B${\sim}m$ : Autonomie, don pur & $i'Ik$ & 40 & J$ {\sim}m$ : Turbulence, chaos \\
\hline
J & 9 & C+ : Apparence, forme & $i'J$ & 41 & K+ : Entité, être \\
Ji & 10 & C- : Essence, substance & $i'Ji$ & 42 & K- : Vide, non-être \\
Jj & 11 & Cm : Symbole, représentation & $i'Jj$ & 43 & Km : Relation, contexte \\
Jk & 12 & C${\sim}m$ : Réalité nue, vérité cachée & $i'Jk$ & 44 & K${\sim}m$ : Substance, essence \\
\hline 
K & 13 & D+ : Perception, sensation & $i'K$ & 45 & L+ : Cercle, cycle \\
Ki & 14 & D- : Inconscience, anesthésie & $i'Ki$ & 46 & L- : Ligne, linéarité \\
Kj & 15 & Dm : Conscience, attention & $i'Kj$ & 47 & Lm : Spirale, hélice \\
Kk & 16 & D${\sim}m$ : Intuition, connaissance directe & $i'Kk$ & 48 & L${\sim}m$ : Point, singularité \\
\hline
-1 & 17 & E+ : Organisation, structure & $-i'1$ & 49 & M+ : Évolution, devenir \\
-1i & 18 & E- : Chaos, désordre & $-i'1i$ & 50 & M- : Éternité, immuabilité \\
-1j & 19 & Em : Émergence, auto-organisation & $-i'1j$ & 51 & Mm : Croissance, développement \\
-1k & 20 & E${\sim}m$ : Contrainte, ordre imposé & $-i'1k$ & 52 & M$ {\sim}m$ : Révolution, mutation \\
\hline
-I & 21 & F+ : Différence, altérité & $-i'I$ & 53 & N+ : Dépendance, influence \\
-Ii & 22 & F- : Identité, unité & $-i'Ii$ & 54 & N- : Autonomie, liberté \\
-Ij & 23 & Fm : Relation, interface & $-i'Ij$ & 55 & Nm : Interdépendance, équilibre \\
-Ik & 24 & F${\sim}m$ : Séparation absolue & $-i'Ik$ & 56 & N${\sim}m$ : Contrainte, nécessité \\
\hline
-J & 25 & G+ : Mélange, fusion & $-i'J$ & 57 & O+ : Variation, changement \\
-Ji & 26 & G- : Pur, simple & $-i'Ji$ & 58 & O- : Constance, stabilité \\
-Jj & 27 & Gm : Combinaison, synergie & $-i'Jj$ & 59 & Om : Adaptation, flexibilité \\
-Jk & 28 & G${\sim}m$ : Confusion, amalgame & $-i'Jk$ & 60 & O${\sim}m$ : Instabilité, chaos \\
\hline
-K & 29 & H+ : Équivalence, correspondance & $-i'K$ & 61 & P+ : Regroupement, ensemble \\
-Ki & 30 & H- : Incommensurabilité & $-i'Ki$ & 62 & P- : Individualité, unité \\
-Kj & 31 & Hm : Analogie, proportion & $-i'Kj$ & 63 & Pm : Hiérarchie, organisation \\
-Kk & 32 & H${\sim}m$ : Identité parfaite & $-i'Kk$ & 64 & P${\sim}m$ : Foule, masse \\
\hline
\caption{Les 16 tétrades de $\mathrm{Cl}(6,0)$ étendues à 64 sémantèmes booléens}
\end{longtable}
\endgroup

\subsection*{C.3 Réduction topologique $64 \rightarrow 20$ : filtration par la Merkabah}
L'espace des 64 sémantèmes est ensuite projeté sur la géométrie du double tétraèdre de niveau 3 (Merkabah), subdivisé en 64 faces triangulaires et 20 cellules tétraédriques. Deux configurations sont dites *voisines* si et seulement si les tétraèdres qui leur correspondent partagent une **face triangulaire entière**. 

Le regroupement topologique consiste à partitionner les 64 configurations en classes d'équivalence dont les graphes de voisinage fermés sont isomorphes. Cette opération, purement structurelle et dénuée de paramètres ajustables, produit exactement **20 classes stables** (attracteurs). Chaque attracteur est identifié par :
- un triplet de pentades $\{X,Y,Z\} \subset \{P_1,\dots,P_6, N_1,\dots,N_6\}$,
- une signature de polarité comptant les pentades positives et négatives du triplet ($3P$, $2P+1N$, $1P+2N$ ou $3N$).

La distribution $(3, 5, 11, 1)$ suit un gradient géométrique strict corrélé au degré de convergence des faces dans la Merkabah. La biologie (code génétique) et tout autre système projeté sur cet espace n'exploite que le potentiel de redondance défini par cette filtration : la géométrie borne l'espace admissible, la fonction en peuple les coordonnées.

\begingroup
\small
\setlength{\tabcolsep}{4pt}
\begin{longtable}{|c|c|c|c|c|c|}
\hline
\textbf{Cl(4,0)} & \textbf{Rang} & \textbf{Latin} & \textbf{Concept central} & \textbf{Concepts (×4 par lettre)} & \textbf{Triplet de polarité} \\
\hline
1 & 1 & A & Action/Vérité & 1:A+, 2:A-, 3:Am, 4:A$^{\sim m}$ & $\{P_1,P_2,P_4\}=3P$ \\
I & 2 & B & Contribution & 5:B+, 6:B-, 7:Bm, 8:B$^{\sim m}$ & $\{P_1,P_3,P_5\}=3P$ \\
J & 3 & C & Apparence & 9:C+, 10:C-, 11:Cm, 12:C$^{\sim m}$ & $\{P_2,P_3,P_6\}=3P$ \\
K & 4 & D & Perception & 13:D+, 14:D-, 15:Dm, 16:D$^{\sim m}$ & $\{P_4,P_5,N_2\}=2P+1N$ \\
-1 & 5 & E & Organisation & 17:E+, 18:E-, 19:Em, 20:E$^{\sim m}$ & $\{P_5,P_6,N_3\}=2P+1N$ \\
-I & 6 & F & Différence & 21:F+, 22:F-, 23:Fm, 24:F$^{\sim m}$ & $\{P_1,P_6,N_4\}=2P+1N$ \\
-J & 7 & G & Mélange & 25:G+, 26:G-, 27:Gm, 28:G$^{\sim m}$ & $\{P_2,P_5,N_6\}=2P+1N$ \\
-K & 8 & H & Équivalence & 29:H+, 30:H-, 31:Hm, 32:H$^{\sim m}$ & $\{P_3,P_4,N_6\}=2P+1N$ \\
$i'1$ & 9 & I & Relation & 33:I+, 34:I-, 35:Im, 36:I$^{\sim m}$ & $\{P_1,N_2,N_6\}=1P+2N$ \\
$i'I$ & 10 & J & Flux & 37:J+, 38:J-, 39:Jm, 40:J$^{\sim m}$ & $\{P_1,N_3,N_5\}=1P+2N$ \\
$i'J$ & 11 & K & Entité & 41:K+, 42:K-, 43:Km, 44:K$^{\sim m}$ & $\{P_2,N_3,N_5\}=1P+2N$ \\
$i'K$ & 12 & L & Cercle/Cycle & 45:L+, 46:L-, 47:Lm, 48:L$^{\sim m}$ & $\{P_3,N_2,N_4\}=1P+2N$ \\
$-i'1$ & 13 & M & Évolution & 49:M+, 50:M-, 51:Mm, 52:M$^{\sim m}$ & $\{P_4,N_1,N_3\}=1P+2N$ \\
$-i'I$ & 14 & N & Dépendance & 53:N+, 54:N-, 55:Nm, 56:N$^{\sim m}$ & $\{P_4,N_5,N_6\}=1P+2N$ \\
$-i'J$ & 15 & O & Variation & 57:O+, 58:O-, 59:Om, 60:O$^{\sim m}$ & $\{P_5,N_1,N_4\}=1P+2N$ \\
$-i'K$ & 16 & P & Regroupement & 61:P+, 62:P-, 63:Pm, 64:P$^{\sim m}$ & $\{P_6,N_1,N_2\}=1P+2N$ \\
 & 17 & Q & Synergie & 7:Bm, 21:F+, 25:G+ & $\{P_2,N_1,N_4\}=1P+2N$ \\
 & 18 & R & Résonance & 29:H+, 33:I+, 37:J+ & $\{P_3,N_1,N_5\}=1P+2N$ \\
 & 19 & S & Spirale & 45:L+, 49:M+, 53:N+ & $\{P_6,N_5,N_6\}=1P+2N$ \\
 & 20 & T & Stratification & 57:O+, 61:P+, 63:Pm & $\{N_2,N_3,N_4\}=3N$ \\
\hline
\caption{Les 16 éléments de Cl(4,0) et les 4 éléments supplémentaires}
\end{longtable}
\endgroup

\subsection*{C.4 Règles de sélection des états aux nœuds d'intersection Q, R, S, T}
Les attracteurs Q, R, S, T ne correspondent pas à des cellules primitives, mais à des nœuds internes où deux ou trois tétraèdres principaux se croisent. Ils ne véhiculent aucun concept primitif unique ; ils matérialisent des résonances structurelles dont l'état booléen est déterminé par une règle de sélection topologique stricte.

**Principe d'héritage** : chaque intersection hérite exactement d'un état de chacun de ses parents, limité aux états où la dimension structurelle primaire $A$ est affirmée :

- l'état d'ancrage $+$, codé $A \cap \neg B \equiv (1,0)$,
- l'état d'interface $m$, codé $A \cap B \equiv (1,1)$.

**Règle de sélection déterministe** : la dimension secondaire $B$ est régie par la rigidité topologique du parent.

1. Un parent contribue à l'état d'interface $m$ $(1,1)$ si et seulement si sa signature de polarité est extrême ($3P$) ou s'il sert de référence structurelle. Les pôles extrêmes possèdent une rigidité élevée ; fournir uniquement l'état d'ancrage $(1,0)$ romprait la connectivité avec les zones mixtes. Ils basculent donc la dimension secondaire sur $1$, produisant la charnière $m$ qui préserve la référence tout en autorisant l'interface.
2. Les parents résidant dans des zones déjà mixtes ($2P+1N$ ou $1P+2N$) maintiennent la dimension secondaire à $0$, contribuant ainsi à l'état d'ancrage stable $(1,0)$.

**Application explicite** :

- **Q** hérite de $B^m$ (car B est $3P$), tandis que F et G fournissent $F^+$ et $G^+$.
- **R** et **S** n'héritent que des états $+$ de leurs parents déjà mixtes.
- **T** hérite de $P^m$ (référence locale pour le noyau interne), O fournissant $O^+$.

Ce mécanisme garantit que chaque intersection comporte exactement **une charnière relationnelle ($m$) et deux ancrages structurels ($+$)**, maintenant la cohérence du réseau global sans paramètres libres et validant les signatures $1P+2N$ (Q, R, S) et $3N$ (T) obtenues par la filtration géométrique.



\newpage

\begin{landscape}
\section*{Annexe D. Alignement des 12 pentades avec les 64 tétrades de $\mathrm{Cl}(6,0)$}

\begingroup
\footnotesize
\setlength{\tabcolsep}{3pt}
\renewcommand{\arraystretch}{0.85}
\setlength{\LTcapwidth}{\textwidth}
\centering
\begin{longtable}{|c|c|l||c|c|l|}
\hline
\multicolumn{3}{|c||}{\textbf{Pentades positives ($P_1$–$P_6$)}} & \multicolumn{3}{|c|}{\textbf{Pentades négatives ($N_1$–$N_6$)}} \\
\cline{1-6}
\textbf{Pentade} & \textbf{Éléments de Clifford} & \textbf{Correspondance tétradique (N°/Concept)} & \textbf{Pentade} & \textbf{Éléments de Clifford} & \textbf{Correspondance tétradique (N°/Concept)} \\
\hline
$P_1$ & $\{iI,\; iJ,\; iK,\; i'k,\; j\}$ &
$\begin{array}{@{}l@{}}
iI \rightarrow 22\;(F^-:\text{Identité, unité}) \\
iJ \rightarrow 26\;(G^-:\text{Pur, simple}) \\
iK \rightarrow 30\;(H^-:\text{Incommensurabilité}) \\
i'k \rightarrow 36\;(I^{\sim m}:\text{Fusion, unification}) \\
j \rightarrow 3\;(A^m:\text{Intention, potentialité})
\end{array}$ &
$N_1$ & $\{-iI,\; -iJ,\; -iK,\; -i'k,\; -j\}$ &
$\begin{array}{@{}l@{}}
-iI \rightarrow 6\;(B^-:\text{Privation, soustraction}) \\
-iJ \rightarrow 10\;(C^-:\text{Essence, substance}) \\
-iK \rightarrow 14\;(D^-:\text{Inconscience, anesthésie}) \\
-i'k \rightarrow 52\;(M^{\sim m}:\text{Révolution, mutation}) \\
-j \rightarrow 19\;(E^m:\text{Émergence, auto-organisation}) \\
\end{array}$ \\
\hline
$P_2$ & $\{jI,\; jJ,\; jK,\; i'i,\; k\}$ &
$\begin{array}{@{}l@{}}
jI \rightarrow 23\;(F^m:\text{Relation, interface}) \\
jJ \rightarrow 27\;(G^m:\text{Combinaison, synergie}) \\
jK \rightarrow 31\;(H^m:\text{Analogie, proportion}) \\
i'i \rightarrow 34\;(I^-:\text{Isolement, indépendance}) \\
k \rightarrow 4\;(A^{\sim m}:\text{Hasard, nécessité})
\end{array}$ &
$N_2$ & $\{-jI,\; -jJ,\; -jK,\; -i'i,\; -k\}$ &
$\begin{array}{@{}l@{}}
-jI \rightarrow 7\;(B^m:\text{Échange, réciprocité}) \\
-jJ \rightarrow 11\;(C^m:\text{Symbole, représentation}) \\
-jK \rightarrow 15\;(D^m:\text{Conscience, attention}) \\
-i'i \rightarrow 50\;(M^-:\text{Éternité, immutabilité}) \\
-k \rightarrow 20\;(E^{\sim m}:\text{Contrainte, ordre imposé})
\end{array}$ \\
\hline
$P_3$ & $\{kI,\; kJ,\; kK,\; i'j,\; i\}$ &
$\begin{array}{@{}l@{}}
kI \rightarrow 24\;(F^{\sim m}:\text{Séparation absolue}) \\
kJ \rightarrow 28\;(G^{\sim m}:\text{Confusion, amalgame}) \\
kK \rightarrow 32\;(H^{\sim m}:\text{Identité parfaite}) \\
i'j \rightarrow 35\;(I^m:\text{Interdépendance, réseau}) \\
i \rightarrow 2\;(A^-:\text{Inaction, illusion})
\end{array}$ &
$N_3$ & $\{-kI,\; -kJ,\; -kK,\; -i'j,\; -i\}$ &
$\begin{array}{@{}l@{}}
-kI \rightarrow 8\;(B^{\sim m}:\text{Autonomie, don pur}) \\
-kJ \rightarrow 12\;(C^{\sim m}:\text{Réalité nue, vérité cachée}) \\
-kK \rightarrow 16\;(D^{\sim m}:\text{Intuition, connaissance directe}) \\
-i'j \rightarrow 51\;(M^m:\text{Croissance, développement}) \\
-i \rightarrow 18\;(E^-:\text{Chaos, désordre})
\end{array}$ \\
\hline
$P_4$ & $\{i'Ii,\; i'Ij,\; i'Ik,\; i'K,\; J\}$ &
$\begin{array}{@{}l@{}}
i'Ii \rightarrow 38\;(J^-:\text{Stase, immobilité}) \\
i'Ij \rightarrow 39\;(J^m:\text{Cycle, rythme}) \\
i'Ik \rightarrow 40\;(J^{\sim m}:\text{Turbulence, chaos}) \\
i'K \rightarrow 45\;(L^+:\text{Cercle, cycle}) \\
J \rightarrow 9\;(C^+:\text{Apparence, forme})
\end{array}$ &
$N_4$ & $\{-i'Ii,\; -i'Ij,\; -i'Ik,\; -i'K,\; -J\}$ &
$\begin{array}{@{}l@{}}
-i'Ii \rightarrow 54\;(N^-:\text{Autonomie, liberté}) \\
-i'Ij \rightarrow 55\;(N^m:\text{Interdépendance, équilibre}) \\
-i'Ik \rightarrow 56\;(N^{\sim m}:\text{Contrainte, nécessité}) \\
-i'K \rightarrow 61\;(P^+:\text{Regroupement, ensemble}) \\
-J \rightarrow 25\;(G^+:\text{Mélange, fusion})
\end{array}$ \\
\hline
$P_5$ & $\{i'Ji,\; i'Jj,\; i'Jk,\; i'I,\; K\}$ &
$\begin{array}{@{}l@{}}
i'Ji \rightarrow 42\;(K^-:\text{Vide, non-être}) \\
i'Jj \rightarrow 43\;(K^m:\text{Relation, contexte}) \\
i'Jk \rightarrow 44\;(K^{\sim m}:\text{Substance, essence}) \\
i'I \rightarrow 37\;(J^+:\text{Flux, transfert}) \\
K \rightarrow 13\;(D^+:\text{Perception, sensation})
\end{array}$ &
$N_5$ & $\{-i'Ji,\; -i'Jj,\; -i'Jk,\; -i'I,\; -K\}$ &
$\begin{array}{@{}l@{}}
-i'Ji \rightarrow 58\;(O^-:\text{Constance, stabilité}) \\
-i'Jj \rightarrow 59\;(O^m:\text{Adaptation, flexibilité}) \\
-i'Jk \rightarrow 60\;(O^{\sim m}:\text{Instabilité, chaos}) \\
-i'I \rightarrow 53\;(N^+:\text{Dépendance, influence}) \\
-K \rightarrow 29\;(H^+:\text{Équivalence, correspondance})
\end{array}$ \\
\hline
$P_6$ & $\{i'Ki,\; i'Kj,\; i'Kk,\; i'J,\; I\}$ &
$\begin{array}{@{}l@{}}
i'Ki \rightarrow 46\;(L^-:\text{Ligne, linéarité}) \\
i'Kj \rightarrow 47\;(L^m:\text{Spirale, hélice}) \\
i'Kk \rightarrow 48\;(L^{\sim m}:\text{Point, singularité}) \\
i'J \rightarrow 41\;(K^+:\text{Entité, être}) \\
I \rightarrow 5\;(B^+:\text{Contribution, apport})
\end{array}$ &
$N_6$ & $\{-i'Ki,\; -i'Kj,\; -i'Kk,\; -i'J,\; -I\}$ &
$\begin{array}{@{}l@{}}
-i'Ki \rightarrow 62\;(P^-:\text{Individualité, unité}) \\
-i'Kj \rightarrow 63\;(P^m:\text{Hiérarchie, organisation}) \\
-i'Kk \rightarrow 64\;(P^{\sim m}:\text{Foule, masse}) \\
-i'J \rightarrow 57\;(O^+:\text{Variation, changement}) \\
-I \rightarrow 21\;(F^+:\text{Différence, altérité})
\end{array}$ \\
\hline
\caption{Pentades positives et négatives : Sur les 64 éléments de $\mathrm{Cl}(6,0)$, les 12 pentades en incluent 5 x 12 = 60 éléments. Les 2 scalaires (+1 et -1) et les 2 pseudosclaires (+i' et -i') en sont exclus. Les éléments des pentades sont réécrits $i<j<k<I<J<K$ dans l'ordre canonique. Les signes induits par l'anticommutation ($ab=-ba$) sont reportés à l'état booléen correspondant, garantissant la bijection avec le tableau des 64 concepts.}
\label{tab:pentads}
\end{longtable}
\endgroup
\end{landscape}

\newpage
![Graphique dual des pentades](Penta_graph.png){ width=100% }
