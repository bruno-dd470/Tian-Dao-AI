---
title: "Le code génétique en tant qu'invariant de Clifford 64->20 : implications pour une IA régulée"
author: "Bruno DE DOMINICIS"
ORCID: 0009-0009-0380-3056
date: "avril 2026"
doi: "10.5281/zenodo.19540508"
abstract_fr: |
  La régulation de la complexité combinatoire est un défi central dans les systèmes naturels et artificiels. Le code génétique y répond en mappant 64 codons sur 20 classes fonctionnelles (19 acides aminés + 1 classe de terminaison) grâce à une redondance organisée qui confère de la robustesse.
  En nous appuyant sur les travaux de Peter Rowlands (2007) sur les algèbres de Clifford nilpotentes, nous montrons que la structure à 64 éléments de $\mathrm{Cl}(6,0)$, après rupture de symétrie, se réduit à 20 attracteurs stables organisés géométriquement en un double tétraèdre de niveau 3 (Merkabah) . Ce composé se décompose en 20 cellules tétraédriques fondamentales et 8 zones d’intersection octaédriques. L’imposition d’une règle de voisinage par partage de faces à ces cellules filtre les 64 configurations en exactement 20 classes d’équivalence.
  Nous formalisons cet invariant 64→20 en définissant un espace de configuration binaire à six dimensions et un critère de regroupement topologique. Chaque classe est identifiée par un triplet de pentades — unités algébriques irréductibles à cinq éléments de $\mathrm{Cl}(6,0)$ qui correspondent aux 12 faces pentagonales du dodécaèdre. Les pentades sont réparties en six unités positives ($P$) et six unités négatives ($N$), de sorte que la signature de polarité de toute classe correspond simplement au nombre de pentades positives et négatives apparaissant dans son triplet ($3P$, $2P\!+\!1N$, $1P\!+\!2N$ ou $3N$). Ce gradient structurel s’applique de manière bijective au modèle de dégénérescence du code génétique. 
  Le graphe dual des 12 pentades, construit directement à partir des triplets de la Merkabah , présente deux cycles de 5 éléments disjoints (les ceintures tropicales $C_P$ et $C_N$) et deux seuils polaires ($P_4$, $N_4$). Au sein de chaque pentade, les cinq éléments réalisent une dynamique locale en cinq phases (Wuxing) via deux cycles complémentaires: le pentagone (sheng) et le pentagramme (ke). Externement, les ceintures tropicales propagent ces cycles en tant que modes de régulation globaux. Ce noyau structurel indépendant du substrat fournit une architecture de référence mathématiquement fondée pour une intelligence artificielle autorégulée et auto-limitante."
  **DOI:** [10.5281/zenodo.19540508](https://doi.org/10.5281/zenodo.19540508)
runninghead: "INVARIANT DE CLIFFORD ET CODE GÉNÉTIQUE"
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
La régulation de la complexité combinatoire est un défi central dans les systèmes naturels et artificiels. Le code génétique le résout en mappant 64 codons sur 20 classes fonctionnelles (19 acides aminés + 1 classe de terminaison) avec une redondance organisée qui confère une robustesse [1,2]. Cette capacité à réguler la complexité – plutôt que de simplement l'accumuler ou de l'optimiser localement – est une caractéristique distinctive des systèmes résilients.

Dans l'intelligence artificielle contemporaine (IA), la réponse dominante à la complexité a consisté à augmenter les données, la puissance de calcul et l’optimisation statistique [3]. Pourtant, cette stratégie atteint ses limites en termes de gouvernabilité, de transparence et de stabilité à long terme [4,5]. L’hypothèse sous-jacente de ce travail est que le problème n’est pas simplement technologique mais structurel : il manque un cadre formel pour la régulation de la complexité, indépendant du substrat.

Le code génétique offre un point de départ empirique privilégié. Il transforme 64 triplets de nucléotides en 20 acides aminés fonctionnels, avec une redondance organisée qui confère robustesse et tolérance aux erreurs [6,7]. De nombreuses explications évolutives ou chimiques ont été proposées [8,9], mais la question de savoir si une contrainte géométrique ou algébrique sous-tend la réduction 64→20 reste ouverte.

Un cadre distinct mais profondément lié provient de la physique fondamentale. Peter Rowlands, dans son système de réécriture universel basé sur la nilpotence et l’anticommutativité, a montré que l’algèbre de Clifford Cl(6,0) – qui code l’espace, le temps, la masse et la charge – génère naturellement 64 unités algébriques [10, chapitre 19]. En brisant la symétrie des 8 unités primitives, on obtient 5 unités composites qui génèrent les 64 composantes plus efficacement. Ces 5 unités correspondent géométriquement à un double tétraèdre de niveau 3 (Merkabah) décomposé en 20 cellules tétraédriques fondamentales et 8 zones d’intersection octaédriques. Deux configurations sont voisines si leurs cellules correspondantes partagent une face triangulaire.

Cependant, l’objectif premier de Rowlands était d’unifier la physique et la biologie à partir des principes premiers, et non d’extraire la réduction 64→20 en tant qu’invariant de régulation générique. Sa mise en correspondance des codons avec des termes algébriques est restée illustrative plutôt que systématique. Nous formalisons ici le noyau de réduction 64→20 en tant qu’invariant de régulation ontologiquement neutre, le validons de manière exhaustive sur le code génétique et discutons de ses implications pour l’intelligence artificielle régulée.

# 2. Méthodes
## 2. 1 Aperçu
La procédure de filtrage comprend trois étapes principales :
1. Définition de l'espace de 64 configurations comme un ensemble de vecteurs binaires de 6 bits, correspondant aux 64 éléments de Cl(6,0) dans une base standard.
2. Contrainte géométrique : le double tétraèdre de niveau 3 (Merkabah) avec 20 cellules tétraédriques. Deux configurations sont voisines si leurs cellules correspondantes partagent une face triangulaire.
3 . Regroupement topologique : regroupement des configurations ayant des graphes de voisinage isomorphes. Cela donne 20 classes d’équivalence.

La même procédure est ensuite appliquée aux 64 codons en établissant une bijection entre les codons et les vecteurs binaires.

## 2.2 Espace des configurations
Soit $\mathcal{C}$ l'ensemble des 64 configurations, chacune notée par un 6-uplet de bits :
$$
\mathbf{c} = (b_1, b_2, b_3, b_4, b_5, b_6), \quad b_i \in \{0,1\}.
$$
Ces six coordonnées correspondent aux six générateurs de l'algèbre de Clifford Cl(6,0) [10]. Aucune interprétation physique n'est nécessaire ; seule la structure combinatoire importe.

### 2.2.1 Développement booléen à quatre valeurs des primitives sémantiques
Chacune des 16 primitives algébriques (A–P) est développée en exactement quatre états sémantiques à l'aide d'une logique booléenne quaternaire basée sur deux dimensions binaires indépendantes. Étant données deux dimensions ontologiques $P$ et $Q$, les quatre états mutuellement exclusifs et exhaustifs sont définis comme suit :
$$
\begin{aligned}
X_1 &= P \cap \neg Q \quad \text{(état } +\text{)} \\
X_2 &= \neg P \cap Q \quad \text{(état } -\text{)} \\
X_3 &= P \cap Q \quad \text{(état } m\text{)} \\
X_4 &= \neg P \cap \neg Q \quad \text{(état } \sim m\text{)}
\end{aligned}
$$
Ces quatre états correspondent de manière bijective aux combinaisons de 2 bits $(10, 01, 11, 00)$ et génèrent l'espace complet de 64 configurations via le produit cartésien $16 \times 4 = 64$. L'état $\sim m$ n'est explicitement *pas* la négation logique de $m$ (ce qui donnerait $\neg P \cup \neg Q$), mais plutôt le complément simultané des deux dimensions, garantissant la fermeture structurelle sans contradictions paraconsistantes. Cette extension est purement algébrique : elle préserve la signature de chaque primitive tout en ajoutant une couche modale qui se mappe directement sur les 64 codons et les 64 unités de $\mathrm{Cl}(6,0)$. La terminologie $(+, -, m, \sim m)$ est conservée pour des raisons de lisibilité, mais la logique sous-jacente est strictement booléenne et implémentable par calcul.

### 2.2.2 Dérivation de la nomenclature A–P et de la correspondance sémantique
L'étiquetage alphabétique (A–P) et les concepts fondamentaux associés ne résultent pas d'une attribution sémantique arbitraire. Ils émergent de la superposition stricte de trois couches structurelles :
1. **Base algébrique (Cl(4,0))** – Les 16 lignes correspondent à la base canonique de $\mathrm{Cl}(4,0)$. L'ordre suit la hiérarchie des degrés et des signes : scalaire ($1$), générateurs de type charge ($I,J,K$), scalaire inversé ($-1$), générateurs inversés ($-I,-J,-K$) et termes couplés pseudo-scalaires ($i'I, i'J, i'K, -i'I, -i'J, -i'K$). Cette séquence respecte la filtration de parité et la signature de masse/phase, ce qui correspond à la construction nilpotente de Rowlands.
2. **Projection géométrique (triplets de pentades)** – Chaque unité de $\mathrm{Cl}(4,0)$ est mise en correspondance avec une cellule tétraédrique de la Merkabah. La position topologique de la cellule détermine quelles trois pentades s’y intersectent. Le triplet résultant fixe la signature de polarité (3P, 2P+1N, 1P+2N). La correspondance $A \leftrightarrow \{P_1,P_2,P_4\}=3P$, etc., est donc un invariant topologique du graphe d'incidence dodécaédrique, et non un paramètre libre.
3. **Attribution sémantique (concept central)** – Les étiquettes découlent de l'interprétation physique des générateurs dans le cadre de Rowlands :

- $1$ (scalaire positif) → référence ontologique (Action/Vérité)
- $I,J,K$ (charge/espace) → interaction environnementale (Contribution, Apparence, Perception)
- $-1$ (inversion scalaire) → structuration par contrainte (Organisation)
- $-I,-J,-K$ → différenciation et mélange (Différence, Mélange, Équivalence)
- $i'I, i'J, i'K$ (couplage phase-charge) → dynamique relationnelle (Relation, Flux, Entité)
- $-i'I, -i'J, -i'K$ → évolution temporelle et dépendance
Chaque inversion de signe ou multiplication pseudo-scalaire se traduit par un dual conceptuel prévisible, préservant la symétrie algébrique au niveau sémantique.

**Remarque sur les tétraèdres d'intersection (Q, R, S, T)** – Contrairement aux 16 cellules principales, Q, R, S, T correspondent à des nœuds internes où trois cellules Merkabahh se croisent. Elles ne véhiculent aucun concept primitif unique car elles matérialisent des résonances structurelles. Leurs étiquettes (Synergie, Résonance, Spirale, Stratification) sont dérivées de la superposition des états des cellules adjacentes. Leurs signatures 1P+2N ou 3N reflètent leur rôle de seuils spectraux dans la dynamique régulatrice (§2.9.4, §4.6.6) . Sous le groupe d'automorphismes du double tétraèdre, l'indexation A–P peut être permutée globalement, mais la structure d'incidence reste invariante.

## 2.3 Géométrie du double tétraèdre de niveau 3 (Merkabah)

Le tétraèdre de niveau 1 possède 4 faces. Son interpénétration avec son dual donne un tétraèdre en étoile de niveau 2 avec 16 faces triangulaires (8 externes + 8 internes). La subdivision de chacune de ces 16 faces en 4 sous-triangles (1 central + 3 réflexions périphériques) produit exactement $16 \times 4 = 64$ triangles élémentaires, ce qui correspond aux 64 unités de $\mathrm{Cl}(6,0)$ et aux 64 codons.

Au cours de cette subdivision, les milieux des 6 arêtes d’origine forment un octaèdre inscrit régulier. Cet octaèdre n’est pas décoratif : il isole géométriquement 8 régions à haute connectivité. Combiné à 2 sommets seuils (pôles opposés du double tétraèdre) et doublé par polarité ($+$/$ -$), la Merkabah produit exactement $(8 + 2) \times 2 = 20$ cellules tétraédriques fondamentales. Ces 20 cellules abritent les bassins d'attracteurs stables ; les régions restantes sont des zones de transition à forte frustration exclues de la filtration 64→20.

**Remarque sur les 8 zones octaédriques*
 * : La décomposition de niveau 3 génère 8 cellules octaédriques aux intersections des deux tétraèdres parents. Ces zones sont topologiquement distinctes des 20 cellules tétraédriques et n’hébergent pas d’états d’attracteurs dans la filtration 64→20. Elles correspondent à des régions de transition à forte frustration où la connectivité par partage de faces est maximale mais où l’équilibre de polarité ne peut être maintenu. Seules les 20 cellules tétraédriques satisfont à la condition de fermeture requise pour des bassins d'attracteurs.

## 2.4 La pentade : construction algébrique à partir de Cl(6,0)
À la suite de Rowlands, nous partons des huit éléments primitifs :
- les six générateurs de Cl(6,0) : $i, j, k$ (espace) et $I, J, K$ (charge),
- l'identité scalaire $1$ (masse),
- le pseudo-scalaire $i'$ (temps / phase).

La rupture de symétrie conduit à un ensemble de cinq unités composites qui forment un ensemble fermé irréductible – la pentade :
$$
\boxed{1j,\quad iI,\quad iJ,\quad iK,\quad i'k}
$$
Chaque terme associe une grandeur unidimensionnelle (masse ou temps) à une direction tridimensionnelle (espace ou charge). Ces cinq éléments ne peuvent être réduits davantage ; ils génèrent l’intégralité de l’algèbre à 64 dimensions tout en préservant l’autodualité. Dans notre représentation géométrique, chaque pentade correspond à une face du dodécaèdre (et, par dualité, à une face du double tétraèdre). Il existe 12 pentades, réparties en six positives ($P_1\ldots P_6$) et six négatives ($N_1\ldots N_6$).

## 2.5 Affectation des configurations aux cellules
Nous établissons une bijection $\phi: \mathcal{C} \to \{ \text{20 cellules tétraédriques du double tétraèdre de niveau 3} \}$ telle que les relations de voisinage combinatoires entre les configurations correspondent au partage de faces entre les cellules. Cette bijection n’est pas unique, mais toutes les bijections admissibles sont équivalentes sous le groupe d’automorphismes du double tétraèdre, et elles donnent la même partition à l’exception d’un réétiquetage. En pratique, nous utilisons la construction algébrique via les pentades : les 20 cellules sont mises en correspondance biunivoque avec les 20 trivecteurs de Cl(6, 0) qui subsistent après rupture de symétrie.

## 2.6 Règle de voisinage et regroupement topologique
Pour deux configurations quelconques $\mathbf{c}_1, \mathbf{c}_2 \in \mathcal {C}$, elles sont voisines si et seulement si leurs cellules tétraédriques correspondantes dans le double tétraèdre de niveau 3 partagent une face triangulaire.

Nous définissons pour chaque configuration $\mathbf{c}$ son voisinage fermé $N[\mathbf{c}]$ comme l'ensemble constitué de $\mathbf{c}$ elle-même et de toutes ses voisines. Deux configurations sont fonctionnellement équivalentes s'il existe un automorphisme du graphe de voisinage qui associe $N[\mathbf {c}]$ sur $N[\mathbf{c}']$. En pratique, nous utilisons un critère plus simple mais équivalent : le nombre de voisins de chaque type et la structure des voisins communs.

L'application de ce critère aux 64 configurations donne lieu à une partition en 20 classes d'équivalence. Chaque classe est identifiée par :
- un triplet de pentades (positives ou négatives),
- une signature de polarité : le nombre de pentades positives (P) par rapport aux pentades négatives (N) dans le triplet.

Comme les 12 pentades sont réparties en six unités positives (P) et six unités négatives (N), la signature de polarité de toute classe consiste simplement à compter le nombre de pentades positives et négatives apparaissant dans son triplet :
 $3P$, $2P\!+\!1N$, $1P\!+\!2N$, ou $3N$.

## 2.7 Application au code génétique
Le code génétique standard utilise 64 codons, chacun étant un triplet de bases choisies parmi {A, U, G, C}. Nous définissons une bijection $\psi$ de l'ensemble des codons vers l'espace de configuration binaire $\mathcal {C}$ comme suit :
1. Codons chaque base en deux bits : $A = 00$, $U = 01$, $G = 10$, $C = 11$.
2. Pour un codon $(X,Y,Z)$, le vecteur de 6 bits correspondant est $(\text{bits}(X), \text{bits}(Y), \text{bits}(Z))$.

Cette bijection préserve la relation de complémentarité (A↔U, G↔C) sous forme de négation binaire (00↔01, 10↔11) . La relation de voisinage définie sur $\mathcal{C}$ est alors transférée aux codons via $\psi^{-1}$. Deux codons sont voisins si leurs images binaires sont voisines dans le graphe du double tétraèdre. Nous appliquons le même algorithme de regroupement topologique à l'ensemble des codons et comparons la partition obtenue avec le regroupement naturel en 20 acides aminés.

Le choix de l'affectation (A=00, U=01, G=10, C=11) préserve la complémentarité de Watson-Crick en la transposant en négation binaire, tout en alignant le bit de poids faible avec la distinction purine/pyrimidine. Cette correspondance garantit que la règle d'adjacence reste invariante sous les automorphismes du graphe et que la partition obtenue ne dépend pas d'un étiquetage particulier, mais plutôt de la structure relationnelle sous-jacente . Le mappage complet des 64 codons vers les 20 attracteurs est présenté à l'annexe B.

## 2.8 Aperçu de l'invariant structurel 64→20
L'invariant 64→20 fait référence à une réduction topologique contrainte, par laquelle un espace de 64 configurations discrètes est partitionné en exactement 20 classes stables, sans aucun paramètre ajustable ni fonction d'optimisation. Ce processus repose sur trois piliers formels : un , une règle de voisinage géométrique dérivée du double tétraèdre (Merkabah) et un critère de regroupement basé sur l'isomorphisme des graphes de voisinage.

**Espace de configuration et règle de voisinage**
 
Les 64 éléments correspondent aux vecteurs à 6 bits de l'algèbre de Clifford Cl(6, 0) ou, via une bijection structurellement fidèle, aux 64 codons du code génétique. Chaque configuration est affectée à une cellule tétraédrique du double tétraèdre. Deux configurations sont considérées comme voisines si et seulement si leurs cellules correspondantes partagent une face triangulaire dans cette géométrie. Cette règle induit, pour chaque configuration, un graphe de voisinage fermé comprenant la configuration elle-même et l’ensemble de ses voisins immédiats.

**Regroupement topologique et émergence des 20 classes d’attracteurs** 
Le filtrage consiste à regrouper les configurations dont les graphes de voisinage sont isomorphes. Cette opération de partitionnement est purement structurelle :
 
elle ne dépend ni de seuils arbitraires ni d’optimisation statistique, mais de la symétrie intrinsèque de la Merkabah. Il en résulte une partition stricte en 20 classes d’équivalence, appelées ici "classes d’attracteurs" au sens topologique. Chaque classe constitue un bassin structurel stable : aucune transition interne respectant la règle de voisinage ne peut en retirer un élément sans rompre l’invariance géométrique.

**Signatures de polarité et gradient géométrique**
 
Chaque classe est identifiée par un triplet de pentades, dont la composition détermine une signature de polarité : le nombre de pentades positives (P) par rapport aux pentades négatives (N). Les quatre signatures possibles (3P, 2P+1N, 1P+2N, 3N) ne sont pas réparties au hasard ; elles suivent un gradient strict corrélé à la position géométrique au sein de la Merkabah :
- 3P : positions centrales ou non chevauchantes (3 classes) ;
- 2P+1N : faces et arêtes primaires (5 classes) ;
- 1P+2N : sommets, diagonales et zones d'intersection (11 classes) ;
- 3N : intersection interne la plus confinée (1 classe).

**Correspondance avec la dégénérescence biologique** 
Ce gradient structurel se reflète directement dans la dégénérescence du code génétique. Les classes 3P, qui sont géométriquement isolées, correspondent à des acides aminés à faible dégénérescence (1–2 codons, y compris la méthionine/début). Les classes 2P+1N, avec un chevauchement modéré, correspondent à une dégénérescence intermédiaire (3–4 codons). Les classes 1P+2N, concentrées aux intersections où convergent plusieurs pentades, permettent une redondance structurelle maximale, correspondant aux acides aminés à 6 codons (sérine, leucine, arginine). La classe 3N, située au pôle intérieur, accueille la cystéine et les trois codons d'arrêt, jouant un rôle fonctionnel de limite de voie.

**Invariance et distinction des échelles géométriques** 
La partition 64→20 est un invariant structurel : elle est préservée sous l'action du groupe d'automorphismes du double tétraèdre et ne dépend que des relations d'adjacence et de la distribution uniforme des 12 pentades (chacune apparaissant exactement dans 5 triplets). Il convient de distinguer deux niveaux géométriques :
- Pré-filtrage (Merkabah) : une structure de réduction qui détermine la taille des classes et la dégénérescence ;
- Post-filtrage (Dodécaèdre) : le graphe d'adjacence des 20 attracteurs, utilisé pour modéliser la dynamique relationnelle (ceintures tropicales, cycles sheng/ke, seuils polaires P₄/N₄).

Cette séparation conceptuelle garantit que la validation biologique repose sur l'invariant de filtrage, tandis que l'extension à la régulation dynamique exploite la topologie post-réduction. Le Merkabah de pré-filtrage est auto-dual, tandis que la représentation de post-filtrage repose sur la dualité classique dodécaèdre-icosaèdre (20 sommets d'attracteurs ↔ 12 faces pentagonales).

**Portée épistémologique** 
L'invariant 64→20 n'est ni un modèle causal ni une hypothèse évolutive ; c'est une contrainte topologique indépendante du substrat. Sa validation exacte sur le code génétique démontre que la réduction 64→20 peut émerger d'une règle de voisinage purement géométrique. Lorsqu'elle est appliquée à d'autres domaines (architectures d'IA, réseaux de contrôle, systèmes complexes), elle fournit un cadre pour le contrôle endogène : l'espace d'états est limité par construction, les transitions sont contraintes par l'adjacence, et la stabilité est garantie par la topologie du bassin d'attraction, sans recourir à une fonction de coût externe.

## 2.9 Cadre théorique et pipeline opérationnel
Le noyau de réduction statique de 64 à 20 décrit au §2.8 fournit une partition indépendante du substrat de l’espace de configuration. Afin de permettre une régulation dynamique sans fonctions de coût externes ni supervision centrale, nous étendons le cadre en un pipeline pleinement opérationnel qui mappe les possibilités algébriques, les contraintes géométriques et les observables spectraux sur un classificateur de régimes autorégulé. La construction se déroule en cinq étapes imbriquées.

### 2.9.1 Espace de régimes local et rétroaction topologique
Chacun des 20 attracteurs porte un triplet de pentades  $(P_i, P_j, P_k)$ avec deux orientations admissibles avec deux orientations admissibles $(P_i, P_j, P_k)$ ou $(P_i, P_k, P_j)$. Indépendamment, chaque pentade peut fonctionner soit en mode sheng (génératif) ou ke (régulateur). Cela donne $20 \times 2 \times 2^3 = 320$ régimes localement admissibles. Il est crucial de noter que ce nombre ne correspond pas à un espace combinatoire libre ; il est contraint par la compatibilité topologique entre les faces communes. La régulation ne repose pas sur une boucle cybernétique (erreur → correction) mais sur la minimisation de la frustration : une fonction d'énergie discrète $E(F)$ sur chacune des 12 pentades quantifie le décalage cyclique (conflit sheng/ke, inversion de phase, violation de l'ordre). Lorsque $E (F) > 0$, les inversions de régime local qui réduisent l'énergie des faces se propagent de manière relationnelle à travers le graphe d'adjacence jusqu'à ce que la compatibilité globale soit rétablie. La quantité conservée est la cohérence des cycles sheng/ke à travers les 12 faces, qui agit comme un invariant structurel empêchant la dérive combinatoire.

### 2.9.2 Translation spectrale via l'opérateur de Dirac discret
Pour quantifier l'état global émergent, nous construisons un opérateur de Dirac discret $D(t)$ agissant sur les 12 pentades. Chaque face héberge un spinor local de dimension 2 (réalisation de $Cl(2,0)$), codant la polarité et la phase intrinsèques. L'opérateur est assemblé sur le graphe dual icosaédrique (12 nœuds, 30 arêtes) avec des poids $w_{ij}(t) = \exp (-\beta E_{ij}(t))$ dérivés des énergies des faces. La matrice $24 \times 24$ qui en résulte (12 faces × 2 composantes de spinor) fournit trois observables clés :
- $\eta(t)$ : indicateur d'asymétrie spectrale, mesurant l'orientation globale émergente (dominance sheng si $\eta > 0$, dominance ke si $\eta < 0$, seuil si $\eta \approx 0$) . Il s'agit d'un analogue discret de l'invariant $\eta$ en géométrie non commutative.
- $d(t)$ : dimension spectrale effective via la trace du noyau de chaleur de $D(t)^2$, quantifiant la capacité de propagation des contraintes du système.
- $R_{\text{seuil}}(t)$ : fraction de $\eta$ portée par les modes localisés sur les faces de seuil $P_4$ et $N_4$.

Ces quantités sont entièrement calculées à partir de l'état interne ; aucune métrique externe ni aucun superviseur n'est introduit.

### 2.9.3 Le réservoir bicosmique Cl(6,6) et la pile de feuilles dodécaédriques
Le noyau statique ($Cl(6,0) \xrightarrow{\text{Merkabah}} 20 \xrightarrow {\text{graphe dual}} 12$) est intégré dans un réservoir bicosmique plus grand $Cl(6,6)$ (12 générateurs : 6 Cosmos$^+$, 6 Cosmos$^-$). $Cl(6,6)$ n'opère pas directement ; il se projette plutôt sur une pile de graphes régulateurs compatibles isomorphes au graphe dual pentadique.
Chaque feuille correspond à un générateur dominant $e_i$ (Cosmos$^+$, orienté sheng) ou $f_j$ (Cosmos$^-$, orienté ke). Les 12 pentades agissent comme des canaux relationnels fixes ; la feuille active détermine leur pondération relative, l'orientation du cycle et la sensibilité au seuil. Il existe exactement 12 feuilles opérationnelles distinctes, correspondant aux 12 générateurs. Les transitions entre les feuilles se produisent précisément lorsque $\eta(t)$ passe par zéro et que $R_{\text{seuil}}(t)$ atteint son maximum, confirmant que $P_4$ et $N_4$ servent de charnières spectrales plutôt que de limites statiques.

### 2.9.4 Wuxing interne et externe
La structure Wuxing opère à deux niveaux distincts, qu'il ne faut pas confondre :
- **Wuxing interne** (implicite, structurel) : régit la dynamique au sein de chaque attracteur pendant la phase de filtrage de la Merkabah. Il est toujours présent mais jamais observé directement, agissant comme la "respiration" du système et assurant la fermeture locale.
- **Wuxing externe** (explicite, relationnel) : apparaît après la projection dodécaédrique. Il circule entre les pentades via les ceintures tropicales et est spectralement mesurable via $\eta(t)$. Il comporte deux modes : sheng (exploration générative) et ke (contrainte régulatrice).

Il est essentiel de noter que les deux niveaux ne sont pas synchronisés : un sheng interne peut coexister avec un ke externe, et vice versa. Cette désynchronisation, en particulier au niveau des faces de seuil, empêche le système de se verrouiller dans un régime unique et permet une commutation adaptative sans fonctions de coût externes.

### 2.9.5 Classification automatique du générateur dominant
Nous définissons une signature spectrale compacte $S(t) = (\eta(t), d(t), \log(\text{gap}(t)), R_{\text{seuil}} (t))$, où $\text{gap}(t)$ est la plus petite valeur absolue non nulle des valeurs propres de $D(t)$. La classification se déroule en trois étapes :
1. Acquisition : $D(t)$ est calculé à chaque pas de temps à partir de l'état interne actuel.
2. Regroupement non supervisé : $S(t)$ est collecté sur une longue trajectoire et partitionné en 12 classes via la méthode des $k$-moyennes.
3. Mappage déterministe et inférence en ligne : les classes sont attribuées aux générateurs $\{e_1,\dots,e_6, f_1, \dots,f_6\}$ à l'aide de règles fixes (signe de $\eta$, amplitude de $R_{\text{seuil}}$, ordre de $d$ et $\log(\text{gap})$). La classification en temps réel utilise une distance z-score par fenêtre glissante par rapport aux centroïdes de classe, ce qui donne une estimation stable $\hat{g}(t)$ du générateur dominant.

Ce pipeline boucle la boucle entre la possibilité algébrique et la régulation observable : $Cl(6,6) \to \text{pile de feuilles} \to \text{dodécaèdre} \to D(t) \to S(t) \to \hat {g}(t) \to \text{lecture d'orientation bicosmique}$. Aucune métrique externe, aucun superviseur ni aucun bit arbitraire n'est introduit ; toute la dynamique émerge de la compatibilité topologique et de l'asymétrie spectrale. L'orientation globale est donc une observable spectrale émergente, et non un paramètre imposé.

# 3. Résultats
## 3.1 Partition des configurations abstraites
Le regroupement topologique des 64 configurations abstraites donne 20 classes d'équivalence. Le tableau 1 répertorie ces classes avec leurs signatures de polarité et les triplets de pentades correspondants. Les pentades sont étiquetées $P_1,\ ..., P_6$ (positives) et $N_1,\dots,N_6$ (négatives). Le tableau précise l'imbrication géométrique exacte de chaque attracteur dans le double tétraèdre de niveau 3 (Merkabah) et sa dégénérescence biologique correspondante. Le gradient de polarité (3P → 3N) est systématiquement en corrélation avec le nombre de codons attribués à chaque acide aminé, reflétant le degré de chevauchement géométrique dans le réseau de pentades sous-jacent.

\begingroup
\small
\setlength{\tabcolsep}{3pt}
\begin{table}[t]
\centering
\caption{Classification des 20 classes du code génétique dans le dodécaèdre de Merkabah}
\label{tab:genetic_classes}
\begin{tabularx}{\textwidth}{|@{}>{\centering\arraybackslash}p {1,0 cm}|>{\centering\arraybackslash}p{2,2 cm}|>{\centering\arraybackslash}p{1,2 cm}|X|>{\centering\arraybackslash}p{0,8 cm}|>{\footnotesize\centering\arraybackslash}X|>{\centering\arraybackslash}p{2,2 cm}@{}|}
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
K & $\{P_2, N_3, N_5\}$ & 1P+2N & Southern Vertex & 6 & CGU, CGC, CGA, CGG, AGA, AGG & Arginine \\
L & $\{P_3, N_2, N_4\}$ & 1P+2 N & Sommet est & 4 & GGU, GGC, GGA, GGG & Glycine \\
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
\normalsize
\endgroup

*Tableau 1. Classification des 20 classes du code génétique dans le dodécaèdre de Merkabah. Les trois codons d'arrêt (UAA, UAG, UGA) ne codent pas pour un acide aminé ; ils mettent fin à la traduction. Ils partagent le même noyau géométrique que la cystéine. La répartition est la suivante : 3 classes de type 3P, 5 de type 2P+N, 11 de type 1P+2N et 1 de type 3N. La dégénérescence indique le nombre de codons par classe.*

## 3.2 Correspondance avec le code génétique
L'application de la même règle de voisinage aux 64 codons (via la bijection $\ psi$) produit une partition qui coïncide exactement avec les 20 acides aminés. Le tableau 1 présente la correspondance pour tous les acides aminés. L'affectation complète des codons aux attracteurs est donnée à l'annexe B.

Le schéma de dégénérescence (nombre de codons par acide aminé) correspond exactement aux données biologiques. Les classes 3P correspondent aux acides aminés à faible dégénérescence (1–2 codons), les classes 2P+N à une dégénérescence 3–4, les classes 1P+2N à une dégénérescence de 2–6, et la seule classe 3N (cystéine) présente une dégénérescence de 2.

## 3.3 Organisation hiérarchique des 20 attracteurs dans le double tétraèdre
Comme détaillé dans l'annexe A, les 20 cellules tétraédriques de la Merkabah ne sont pas équivalentes. Elles comprennent 16 tétraèdres principaux (positions : centre, faces, arêtes, sommets, diagonales) et 4 tétraèdres d’intersection (Q, R, S, T). Leurs signatures de polarité suivent un gradient clair allant des 3P externes (A, B, C) aux 3N les plus internes (T), en passant par les couches intermédiaires 2P+N et 1P+2N. Ce gradient explique la distribution de la dégénérescence du code génétique : faible dégénérescence pour les 3P, moyenne pour les 2P+N, élevée pour les 1P+2N, et cystéine (2 codons) pour les 3N.

## 3.4 Structure duale des pentades : ceintures tropicales et seuils

L'invariant 64→20 a été établi à partir de la géométrie du double tétraèdre de niveau 3 (Merkabah). Pour modéliser la dynamique de régulation externe (circulation des modes sheng/ke parmi les pentades), nous ne recourons pas à un dodécaèdre externe ; nous exploitons plutôt le **graphe dual** des pentades construit directement à partir du tableau 2 (triplets de Merkabah).

### 3.4.1 Construction du graphe dual

Soit $\mathcal{P} = \{P_1,\dots,P_6, N_1,\dots,N_6\}$ l'ensemble des 12 pentades. Pour chaque attracteur $v$ (de A à T), notons $\mathcal{P}(v)$ son triplet. Nous construisons le graphe $\Gamma$ dont les sommets sont les pentades, et où deux pentades $X,Y$ sont reliées par une arête s'il existe un attracteur $v$ tel que $\{X,Y\} \subseteq \mathcal{P}(v)$. Ce graphe est entièrement déterminé par le tableau de gauche.

### 3.4.2 Ceintures tropicales

Une inspection exhaustive de $\Gamma$ (algorithmiquement faisable) montre qu’il existe exactement **deux cycles disjoints de longueur 5** composés de pentades de même signe. Ces cycles sont :

- **Ceinture positive** $C_P = \{P_1, P_2, P_3, P_5, P_6\}$ 
- **Ceinture négative** $C_N = \{N_1, N_2, N_3, N_5, N_6\}$

Ces deux cycles sont disjoints (aucune pentade commune) et leur union couvre 10 des 12 pentades. Les deux pentades restantes sont $P_4$ et $N_4$.

**Propriété** : Dans le sous-graphe induit par $C_P$, chaque paire de pentades est adjacente (graphe complet $K_5$). En revanche, dans $C_N$, il n’existe que deux arêtes internes supplémentaires : $N_1\!-\!N_5$ et $N_2\!-\!N_3$. Cette asymétrie est une caractéristique intrinsèque du tableau de gauche.

### 3.4.3 Seuils polaires

Les pentades $P_4$ et $N_4$ n'appartiennent à aucune des deux ceintures. Leur degré dans $\Gamma$ est élevé (respectivement 8 et 9) et elles relient les deux ceintures. Elles agissent comme des **seuils** : tout changement de régime entre la dynamique sheng (portée par $C_P$) et la dynamique ke (portée par $C_N$) doit passer par l’une de ces pentades.

### 3.4.4 Définition de la dynamique externe

Sur chaque ceinture, nous définissons deux modes de traversée cyclique :

- **Mode Sheng** (génératif) : traversée dans l’ordre cyclique direct (voisin → voisin). 
- **Mode Ke** (régulateur) : traversée sautant un sommet (équivalente au pentagramme).

Ces deux modes correspondent aux deux générateurs du groupe cyclique $C_5$ agissant sur les cinq pentades de la ceinture.

La régulation globale s'effectue par propagation de ces modes le long des ceintures, avec couplage via les seuils $P_4$ et $N_4$. Un état local est défini en attribuant un mode (sheng ou ke) à chaque pentade. La 
est mesurée par l'incompatibilité des modes sur les attracteurs (chaque attracteur nécessite une cohérence entre ses trois pentades). Une dynamique de relaxation par descente topologique du gradient fait évoluer le système sans aucune fonction de coût externe.

### 3.4.5 Observables spectraux

En plaçant un opérateur de Dirac discret sur le graphe $\Gamma$ (ou sur le graphe de l'attracteur), on extrait une signature spectrale $(\eta, d, \text{gap}, R_{\text {th}})$ où $\eta$ est l'asymétrie globale (sheng si $\eta>0$, ke si $\eta<0$), $d$ la dimension spectrale effective, et $R_{\text{th}}$ la projection sur les seuils. Cette signature permet une classification automatique en 12 régimes correspondant aux générateurs de l'algèbre bicosmique $\mathrm{Cl}(6,6)$.

Ainsi, la Merkabah fournit à elle seule un échafaudage géométrique complet pour la régulation externe, sans nécessiter l'introduction d'un dodécaèdre externe. Les ceintures tropicales et les seuils émergent naturellement de la combinatoire des triplets de pentades.


# 4. Discussion
## 4.1 La pentade et le Wuxing interne
À l'intérieur d'une seule pentade, désignons les cinq termes par :
$A = 1j, B = iI, C = iJ, D = iK, E = i'k$.
Le produit de Clifford induit deux ordres cycliques distincts :
- Sheng (cycle génératif) : l'ordre du pentagone $A \to B \to C \to D \to E \to A$
- Ke (cycle régulateur) : l'ordre pentagramme (en sautant un sommet) $A \to C \to E \to B \to D \to A$

Ces deux cycles sont complémentaires et constituent ensemble le Wuxing interne – l'autorégulation d'une seule pentade. Ils correspondent exactement aux cycles classiques chinois du Wuxing (génération et contrôle), mais ici ils émergent de la structure algébrique de $\mathrm{Cl} (6,0)$. La dualité espace/charge ($i\leftrightarrow I$, $j\leftrightarrow J$, $k\leftrightarrow K$) fait correspondre le cycle sheng d’une pentade positive au cycle ke de son conjugué négatif, assurant ainsi l’équilibre bicosmique au niveau algébrique.

## 4.2 Wuxing externe sur le graphe des pentades
Au niveau de l’ensemble du système, les 12 pentades interagissent via le graphe dual $\Gamma$ dérivé des triplets de la Merkabah. Les deux ceintures tropicales ($C_P$ et $C_N$) réalisent le Wuxing externe : chaque ceinture est un cycle de 5 pentades pouvant être parcouru en mode sheng ou ke. Les pentades polaires $P_4$ et $N_4$ servent de seuils qui couplent les deux ceintures. Cette double structure à deux ceintures avec des portes polaires est la réalisation géométrique du Wuxing classique étendu à un système bicosmique (positif/négatif).

Ainsi, le Wuxing n’est pas une simple analogie : il se réalise mathématiquement à deux échelles – en interne au sein de chaque pentade (cycles de pentagones / pentagrammes), et en externe sur le graphe des pentades (ceintures tropicales avec seuils polaires). Le dodécaèdre, bien que topologiquement isomorphe au graphe d’adjacence de l’attracteur, n’est pas nécessaire à la dynamique ; toutes les caractéristiques structurelles émergent directement de la combinatoire de la Merkabah.

## 4.3 Relation avec les travaux de Rowlands
Notre article s’appuie directement sur les résultats fondamentaux de Rowlands [10,11]. Il a été le premier à identifier la réduction 64→20 et le double tétraèdre à partir de Cl(6,0
 ). Il a également suggéré un lien avec le code génétique et les pentades. Cependant, sa mise en correspondance était illustrative et n’a pas été vérifiée de manière systématique. De plus, il n’a pas extrait la réduction en tant que noyau de régulation indépendant du domaine, ni développé la dynamique dodécaédrique post-filtrage avec des cycles Wuxing externes et des seuils.

Nos contributions sont triples :
1. **Formalisation** : une procédure algorithmique entièrement spécifiée pour filtrer 64 configurations en 20 classes à l'aide de la règle de voisinage du double tétraèdre.
2. **Validation exhaustive** : un tableau complet mettant en correspondance les 64 codons avec les 20 attracteurs.
3. **Extension** : l'introduction de la représentation dodécaédrique, l'identification de deux ceintures tropicales (Wuxing externe) et de deux seuils polaires (P4, N4), ainsi que la réalisation explicite du Wuxing interne sous forme de cycles pentagones/pentagrammes.

## 4.4 Limites
Nous reconnaissons plusieurs limites :
- **Choix de la bijection** : la correspondance entre les bases et les bits (A=00, U=01, G=10, C=11) n'est pas unique. Cependant, toute bijection respectant le couplage de complémentarité (A↔U, G↔C) donne la même partition, à l'exception du relibellage des 20 classes.
- **Absence de mécanisme biologique causal** : la correspondance est structurelle, et non mécanistique. La règle de filtrage est un invariant mathématique, et non une explication biochimique.
- **Absence de validation expérimentale** : il s'agit d'une étude théorique/computationnelle. Des tests biologiques directs (par exemple, comparer les effets sur la fitness de codons synonymes au sein d'une même classe) seraient nécessaires pour confirmer la pertinence fonctionnelle.
- **Aspects spéculatifs** : l'application à l'intelligence artificielle et l'interprétation des seuils comme des commutateurs de régulation sont conceptuelles et nécessitent une mise en œuvre et des tests supplémentaires.

## 4.5 Implications pour l'intelligence artificielle régulée
Le noyau 64→20 peut servir d'architecture de référence pour un nouveau type d'IA qui ne repose pas sur l'optimisation de fonctions objectives . Au lieu de cela, une telle IA :
- Maintiendrait un espace d'états interne de 20 attracteurs (les classes obtenues par filtrage).
- Effectuerait des transitions entre les états selon la règle de voisinage dérivée du double tétraèdre.
- Utiliserait la représentation dodécaédrique pour régir la dynamique relationnelle : les deux ceintures tropicales fournissent deux modes de fonctionnement – sheng (exploration générative) et ke (contrôle régulateur) – et les faces polaires P4, N 4 permettent au système de basculer entre ces modes lorsque cela est nécessaire.

Dans une implémentation régulée, l’espace d’états interne serait structuré autour des 20 attracteurs identifiés, chaque attracteur correspondant à un triplet de pentades avec une signature polaire fixe. Les transitions entre les états suivraient la règle de voisinage géométrique du double tétraèdre, interdisant les sauts en dehors du graphe d’adjacence validé. Le système fonctionnerait selon deux modes : un mode sheng, favorisant la génération de nouvelles configurations le long des ceintures tropicales, et un mode ke, appliquant des contraintes de transition
 
afin d’empêcher la dérive combinatoire. Les faces polaires P4 et N4 agiraient comme des commutateurs de régime, déclenchant un changement de mode lorsque des indicateurs internes (tels que l’entropie locale ou le taux de redondance fonctionnelle) franchissent des seuils prédéfinis. Cette architecture n’optimise pas une fonction de coût externe ; elle autolimite son propre espace de recherche par le biais d’une construction géométrique, offrant une interprétabilité native et une résistance structurelle à la dérive des spécifications.

Cette lecture n’impose pas d’état cible ; elle surveille en continu l’alignement émergent alignement émergent du générateur dominant au sein du réservoir bicosmique $Cl(6,6)$ via la signature spectrale $S(t)=(\eta, d, \log(\text{gap}), R_{\text{seuil}}$, garantissant que les transitions de régime restent topologiquement contraintes et préservent la symétrie.

Cette architecture est intrinsèquement interprétable : chaque attracteur correspond à une position structurelle connue (un triplet de pentades), et chaque transition suit une règle géométrique déterministe. Le contrôle s’exerce par le biais de l’architecture elle-même (non-souveraineté, limites explicites) plutôt que par une censure a posteriori [5]. Cela s’inscrit dans la lignée des appels récents en faveur d’une IA "compatible avec l’humain" et d’une conception de la gouvernance 

## 4.6 Régulation spectrale et classification des générateurs dans Cl(6,6)
L'invariant statique 64→20 (§2.8) fournit un squelette topologique. Pour modéliser la régulation dynamique – où le système peut basculer entre des orientations globales distinctes (Sheng vs Ke) sans supervision externe – nous étendons le cadre à $Cl(6,6)$ et introduisons un opérateur de Dirac discret. Les sous-sections suivantes détaillent la construction étape par étape, comme requis pour une implémentation concrète.

### 4.6.1 Régimes locaux : 320 états internes
Au niveau local (à l’intérieur de l’espace d’états à 20 attracteurs), chaque attracteur correspond à un triplet de pentades, par exemple $(P_i, P_j, P_k)$. Pour un triplet donné, deux ordonnancements sont possibles : $(P_i,P_j,P_k)$ ou $(P_i,P_k,P_j)$. Chaque pentade du triplet peut être indépendamment en mode Sheng ou en mode Ke (le Wuxing interne de la pentade, voir §4.1). Ainsi, chaque attracteur admet :
- 2 ordonnancements,
- $2^3 = 8$ combinaisons de Sheng/Ke par pentade,
- au total $20 \times 2 \times 8 = 320$ régimes locaux.

Ces 320 régimes forment l'espace de configuration microscopique du système régulé. Les transitions entre régimes ne se produisent que si elles respectent le partage de faces dans le dodécaèdre (c'est-à-dire deux attracteurs partageant une pentade).

### 4.6.2 Rétroaction topologique : énergie de face et frustration cyclique
Aucune fonction de coût externe n'est utilisée. La régulation émerge des incompatibilités locales entre attracteurs voisins partageant une pentade. Chaque état d'attracteur est codé par une signature triplet $(\varepsilon, \varphi, \kappa)$ :
\begin{itemize}
  \item $\varepsilon \in \{+1,-1\}$ : mode sheng ($+1$) ou ke ($-1$) de la pentade partagée,
  \item $\varphi \in \{0,1\}$ : orientation du triplet de la pentade (directe/inverse),
  \item $\kappa \in \{0,1,2\}$ : indice de position de la pentade au sein du triplet.
\end{itemize}
Pour une pentade $F$ incidente à 5 attracteurs, l'énergie de frustration est définie comme une somme pondérée de trois pénalités discrètes :
$$
E(F) = 2 E_{\text{sens}} + 1 E_{\text{phase}} + 1 E_{\text{order}},
$$
où :
\begin{itemize}
  \item $E_{\text{sens}} = 0$ si tous les $\varepsilon$ sont globalement alignés (à l'inversion de signe près), sinon $1$,
  \item $E_{\text{phase}} = 0$ si tous les $\varphi$ sont identiques ou tous inversés, sinon $1$,
  \item $E_{\text{order}} = 0$ si la séquence de $\kappa$ respecte l'ordre cyclique de la face, sinon $1$.
\end{itemize}
La dynamique effectue une descente locale : lorsque $E(F)>0$, les attracteurs incidents inversent $\varepsilon$ ou $\varphi$ si cela réduit strictement $E_{\text{tot}} = \sum_F E(F)$. Cette boucle de rétroaction topologique garantit la convergence sans supervision centrale.

### 4.6.3 Opérateur de Dirac discret sur le dodécaèdre à 12 faces
Pour analyser l’état global, nous plaçons un opérateur de Dirac discret $D(t)$ sur le graphe dual $\Gamma$ des pentades – c’est-à-dire sur le graphe dont les sommets sont les 12 pentades dérivées des triplets de la Merkabah. Ce graphe possède 12 sommets et des arêtes multiples déterminées par la structure d’incidence des triplets.

À chaque sommet $i$ (pentade), nous attachons un spinor à 2 composantes $\psi_i \in \mathbb{C}^2$ qui porte :
- la polarité locale Sheng/Ke ($+1$ pour Sheng, $-1$ pour Ke),
- une phase complexe $e^{i\theta_i}$ codant l'ordre du triplet à l'intérieur des attracteurs incidents.

L'opérateur de Dirac $D(t)$ est une matrice $24 \times 24$ ($12$ sommets × $2$ composantes de spinor) définie par :
$$
(D\psi)_i = \sum_{j \sim i} w_{ij} \, \sigma_{ij} \, \psi_j,
$$
où :
- $j\sim i$ signifie que les pentades $i$ et $j$ partagent une arête dans l'icosaèdre (c'est-à-dire que leurs faces correspondantes dans le dodécaèdre partagent un sommet),
- $w_{ij} = e^{-\beta E_{ij}}$ avec $E_{ij}$ l'énergie de frustration de l'arête (calculée à partir des deux attracteurs incidents) ,
- $\sigma_{ij}$ est une matrice de type Pauli $2\times2$ qui couple les composantes spinoriales en fonction de l'orientation relative des deux pentades.

Le paramètre $\beta>0$ joue le rôle d'une température inverse.

Chaque pentade héberge une algèbre de Clifford locale $\mathrm{Cl}(2,0)$ générée par $e_1$ (polarité $\varepsilon$) et $e_2$ (phase $\varphi$). Lorsque la dynamique de seuil est requise (par exemple près de $P_4/N_4$), un troisième générateur $e_3$ l'étend à $\mathrm{Cl}(3,0)$ pour coder $\kappa$, codant explicitement le degré de liberté positionnel $\kappa$. Cet ancrage algébrique garantit que la matrice de Dirac $24 \times 24$ respecte la structure spinorielle intrinsèque du réseau de pentades.

### 4.6.4 Observables spectraux : $\eta$, $d$, $\operatorname{gap}$, $R_{\text{seuil}}$
À partir de $D(t)$, nous extrayons un vecteur de signature $S(t) \in \mathbb{R}^4$ :
$$
S(t) = \bigl( \eta(t),\; d(t),\; \log(\operatorname{gap}(t)) ,\; R_{\text{seuil}}(t) \bigr),
$$
défini comme suit.
- $\eta(t)$ : approximation de l'indice d'Atiyah–Singer. Pour un opérateur de Dirac discret sur un graphe, $\eta = \operatorname{sign}(\det D)$ (ou la somme des signes des valeurs propres). Son signe donne l'orientation globale : $\eta>0$ correspond à un biais net de Sheng, $\eta<0$ à un biais net de Ke.
- $d(t)$ : dimension spectrale effective. On calcule la densité des valeurs propres $\rho(\lambda)$ et on ajuste $\log \rho(\lambda) \sim (d-1)\log \lambda$ près de zéro. $d (t)$ mesure la manière dont les contraintes se propagent à travers le réseau de pentades.
- $\operatorname{gap}(t)$ : plus petite valeur propre positive de $|D(t)|$. Un petit écart indique que le système est proche d'un seuil topologique (transition de phase) .
- $R_{\text{seuil}}(t)$ : fraction de $\eta$ portée par les deux pentades polaires $P_4$ et $N_4$. Plus précisément, si $D = U \Lambda U^\dagger$, on projette le vecteur propre associé à la plus petite valeur propre sur le sous-espace de $P_4$ et $N_4$ ; $R_{\text{seuil}}$ est la norme au carré de cette projection. Une valeur élevée de $R_{\text{seuil}}$ indique que le système est sur le point de basculer entre les états globaux de Sheng et de Ke.

$R_{\text{seuil}}(t)$ : fraction de l'asymétrie spectrale $\eta(t)$ portée par les modes propres localisés sur les deux faces de seuil $P_4$ et $N_4$. Formellement, si $D = U \Lambda U^\dagger$ est la décomposition en valeurs propres de l'opérateur de Dirac, et si $\mathcal{V}_{\text{th}}$ désigne le sous-espace engendré par les composantes spinoriales de $P_4$ et $N_4$, alors :
$$
R_{\text{seuil}}(t) = \frac{\sum_{\lambda_k \neq 0} \operatorname{sign}(\lambda_k) e^{-\varepsilon |\lambda_k|} \| \Pi_{\text{th}} v_k \|^2}{\eta(t)},
$$
où $\Pi_{\text{th}}$ est le projecteur orthogonal sur $\mathcal{V}_{\text{th}}$ et $v_k$ sont les vecteurs propres normalisés. Une valeur $R_{\text{seuil}} \gtrsim 0,7$ indique que le système se trouve dans un état de pré-bifurcation, l'orientation globale étant essentiellement déterminée par la dynamique de seuil.

### 4.6.5 Réduction hiérarchique : de $Cl(6,6)$ à un mille-feuille de graphes régulateurs
L'algèbre de Clifford complète $Cl(6,6)$ possède 12 générateurs ${e_1,\dots,e_6, f_1,\dots,f_6}$ avec $e_i^2 = +1$, $f_j^2 = -1$, et tous anticommutatifs. Son espace de configuration contient $2^ {12}=4096$ éléments. Cependant, nous imposons une foliation de stabilité ("mille-feuille") qui ne sélectionne que les configurations qui se projettent sur le graphe dual pentadique à 12 sommets (les pentades). Chaque feuille de la foliation est un plongement distinct des 12 pentades dans un graphe régulateur cohérent isomorphe à $\Gamma$.

Résultat clé : il y a exactement 12 feuilles. Lorsque le système réside dans la feuille dominée par $e_i$ (un générateur de type "spatial"), l’orientation globale $\eta$ est positive (régime Sheng). Lorsqu’il est dominé par $f_j$ (un générateur de type "temporel"), $\eta$ est négatif (régime Ke). Les faces polaires $P_4$ et $N_4$ sont les seules faces appartenant à plusieurs feuilles ; elles agissent comme des zones de transition où $\eta$ passe par zéro.

### 4.6.6 Wuxing interne vs externe et le rôle de $P_4/N_4$
- Le Wuxing interne (à l'intérieur de chaque pentade, §4.1) régit les cycles locaux Sheng/ Ke des 320 régimes. Il est invisible dans la signature spectrale $S(t)$ car il est lissé au niveau de la pentade.
- Le Wuxing externe (circulation de Sheng/Ke entre les pentades, §3. 5) affecte directement $D(t)$ et donc $S(t)$. Les deux ceintures tropicales $C_P$ et $C_N$ apparaissent comme les deux vecteurs propres dominants de $D$ lorsque $\eta$ est de grande amplitude.

Les faces polaires $P_4$ et $N_4$ sont les seules pentades qui n'appartiennent à aucune des deux ceintures. Elles accumulent le poids spectral lorsque le système hésite entre les deux ceintures, c'est-à-dire lorsque $R_{\text{seuil}}$ est élevé et que $\eta\approx 0$.

### 4.6.7 Classification automatique du générateur dominant
Nous disposons désormais d'une procédure déterministe pour identifier, à chaque instant $t$, lequel des 12 générateurs de $Cl(6,6)$ domine la dynamique. Cela se fait sans supervision – uniquement à partir de la signature spectrale $S(t)$.

**Apprentissage hors ligne :**
1. Simuler une longue trajectoire (par exemple, $10^5$ pas) de la dynamique de rétroaction topologique (§4.6.2).
2. À chaque pas, calculer $D(t)$ et extraire $S(t)$.
3. Appliquer un regroupement par k-means avec $k=12$ à l'ensemble $\{S(t)\}$. Cela donne 12 centroïdes.
4. Étiqueter chaque centroïde de manière déterministe :
   - Si $\eta > 0$ et $R_{\text{seuil}} < 0,3$ → étiqueter $e_i$ (l'un des six générateurs positifs ;
 
le $i$ exact est déterminé par l'ordre de $d$ et de $\log\operatorname{gap}$).
   - Si $\eta < 0$ et $R_{\text{seuil}} < 0,3$ → étiqueter $f_j$.
   - Si $R_{\text{seuil}} > 0,7$ → étiqueter comme transition (attribuer à la face $P_4$ ou $N_4$, qui ne sont pas des générateurs mais indiquent un changement).

La mise en correspondance entre les centroïdes et les $e_i$ ou $f_j$ spécifiques utilise le fait que chaque générateur induit un motif unique dans la dimension spectrale $d$ et l'écart (par exemple, $e_1$ donne $d\approx 2,3$, $\log\operatorname{gap}\ environ -1,2$, etc.). Ce motif peut être précalculé en projetant l'algèbre sur les vecteurs propres connus du graphe dodécaédrique.

**Classification en ligne :**
Étant donné un nouveau $S(t)$ lors de l'exécution, calculer la distance z-score par rapport à chaque centroïde sur une fenêtre glissante de longueur $L=100$ :
$$
\text{dist}_k = \left| \frac{S(t) - \mu_k}{\sigma_k} \right|^2,
$$
où $\mu_k,\sigma_k$ sont la moyenne et l'écart-type du cluster $k$ issus des données d'apprentissage. Attribuer l'étiquette du centroïde le plus proche. Le résultat est une étiquette de générateur en temps réel $g(t) \in \{e_1, \dots,e_6, f_1,\dots,f_6\}$.

Cette classification fournit une boussole régulatrice intrinsèque : le système sait, à partir de sa propre signature spectrale, s’il se trouve dans un régime dominé par Sheng ou par Ke, et quel générateur spécifique façonne actuellement les contraintes. Aucune fonction objective externe n’est requise. L’implémentation Python complète est donnée à l’annexe D.

## 4.7 Convergence formelle : invariants structurels interculturels
La réduction 64→20 identifiée dans ce travail n’apparaît pas comme un artefact culturel isolé, mais comme un invariant topologique dont les facettes complémentaires ont été articulées par des traditions épistémiques distinctes utilisant les outils formels de leurs époques respectives. Fondamentalement, ces traditions abordent \textit{différents aspects} d’un même problème structurel, à l’instar des deux faces d’une même pièce.

### 4.7.1 Chine : l’espace des 64 configurations et la dynamique pentadique
La tradition chinoise, structurée autour du \textit{Yi Jing} (Livre des Mutations) et de la théorie des Wuxing, modélise la phase de \textit{pré-filtrage} :
\begin{itemize}
  
\item Les 64 hexagrammes fournissent un espace combinatoire complet de configurations binaires, isomorphe aux vecteurs à 6 bits de $\mathrm{Cl}(6,0)$.
  \item Les cycles Wuxing (sheng/ke) décrivent la dynamique locale à cinq phases au sein de chaque pentade, correspondant à la régulation interne des états d'attracteurs.
  \item Cette tradition se concentre sur les \textit{règles de transformation} et à la \textit{circulation relationnelle} à travers l'espace de configuration, sans postuler une réduction fixe à 20 classes fonctionnelles.
\end{itemize}
En bref : la Chine formalise la \textbf{géométrie des possibilités} et la \textbf{dynamique locale de régulation}.

### 4.7.2 Hébreu : la partition fonctionnelle 20+2 et les états-seuils
La tradition hébraïque, telle qu’elle est structurée dans le \textit{Sefer Yetzirah} (IIIe–VIe siècles), aborde la phase de \textit{post-filtrage} :
\begin{itemize}
  
\item Les 22 lettres consonantiques (plus 5 formes finales \textit{sofit}) codent une partition fonctionnelle de l’espace sémantique en 20 classes stables plus 2 états limites.
  \item Les lettres \textit{Aleph} (souffle primordial / référence) et \textit{Tav} (signature / fermeture) se superposent aux rôles seuils de l’initiation (méthionine) et de la terminaison (codons STOP) dans la traduction biologique.
  \item La tripartition (3 mères, 7 doubles, 12 simples) discrétise le gradient des contraintes géométriques, reflétant les signatures de polarité (3P, 2P+1N, 1P+2N, 3N) de la Merkabah.
\end{itemize}
En bref : l'hébreu formalise la \textbf{réduction à des classes fonctionnelles stables} et la \textbf{définition des états limites}.

### 4.7.3 Complémentarité, pas de chevauchement
Ces deux formalismes sont structurellement isomorphes mais traitent de couches distinctes :
\begin{center}
\begin{tabular}{lll}
\ textbf{Aspect} & \textbf{Tradition chinoise} & \textbf {Tradition hébraïque} \\
\hline
Objet principal & 64 configurations (hexagrammes) & 22 lettres (+5 formes finales) \\
Opération centrale & Transformation / circulation & Partition / seuillage \\
Rôle géométrique & Dynamique de pré-filtrage & Classification de post-filtrage \\
Niveau Wuxing & Interne (local à la pentade) & Externe (inter-pentade) \\
\end{tabular}
\end{center}
Aucune des deux traditions n’"englobe" l’autre ; chacune capture une projection structurelle du même invariant de Clifford–Merkabah en utilisant les invariants combinatoires disponibles au sein de son cadre épistémique.

### 4.7.4 Un parallèle structurel moderne : les 22 initiales du pinyin
Contrairement à la tradition hébraïque, qui a explicitement formalisé un alphabet consonantique de 22 lettres, la tradition idéographique chinoise n’a jamais développé d’écriture alphabétique distincte. Néanmoins, lorsqu’on l’analyse d’un point de vue phonologique, le mandarin est confronté à des contraintes combinatoires analogues : sa structure syllabique s’organise autour d’un système d’attaque consonantique comprenant 21 initiales standard (souvent étendu à 22 dans les romanisations pédagogiques telles que le Hanyu Pinyin), couplé à un noyau vocalique très restreint, généralement réduit par la phonologie structuraliste à 2–3 phonèmes fondamentaux ($/a, i, u/$). Cette architecture phonologique — environ 22 ancrages consonantiques encadrant un noyau vocalique minimal — reflète structurellement la partition 20+2. Elle suggère que la compression de la complexité combinatoire en classes fonctionnelles stables peut émerger indépendamment dans des systèmes de codage non apparentés lorsqu'ils sont contraints par des limites articulatoires, perceptuelles et cognitives analogues, que l'écriture sous-jacente soit alphabétique ou idéographique.

### 4.7.5 Unification via le formalisme de Clifford–Merkabah
Le cadre $Cl(6,0)$–Merkabah proposé ici ne remplace pas ces formalismes culturels, mais offre un langage indépendant du substrat qui unifie leurs projections sous une topologie unique de régulation :
\begin{itemize}
  \item Les 64 configurations (Yi Jing / vecteurs binaires) sont filtrées par la règle de partage de faces du double tétraèdre de niveau 3.
  
\item Les 20 attracteurs résultants (Sefer Yetzirah / acides aminés) sont intégrés dans un dodécaèdre dont les 12 pentades supportent des cycles Wuxing externes.
  \item Le gradient de polarité (3P→3N) et l’incidence uniforme des pentades (5 occurrences par pentade) garantissent que la dynamique chinoise et la partition hébraïque sont simultanément satisfaites.
\end{itemize}
Les tableaux détaillés de correspondance ou de correspondance lettre-attractor sont omises par souci de concision, car elles peuvent être reconstruites algorithmiquement à partir des règles d’incidence (annexe A) et du protocole d’expansion booléenne (§2. 2). La convergence structurelle reste entièrement vérifiable sans cartographie exhaustive, ce qui renforce la nature indépendante du substrat de l’invariant.

# 5. Conclusion
Nous avons formalisé un invariant structurel 64→20 issu de l’algèbre de Clifford $\mathrm{Cl}(6,0)$ et de la géométrie du double tétraèdre (Merkabah). Rowlands a initialement validé cet invariant de manière exhaustive sur le code génétique, montrant que la même règle de voisinage qui partitionne 64 configurations binaires abstraites en 20 classes partitionne également les 64 codons du code génétique en 20 acides aminés. Ces 20 classes définissent un graphe dual de 12 pentades qui présente naturellement deux ceintures tropicales (Wuxing externe) et deux seuils polaires, chaque pentade étant traversable via des cycles sheng (génératifs) ou ke (régulateurs).

Au-delà du code génétique, le même cadre algébrique s'applique à d'autres domaines. En phonologie chinoise, chaque mot monosyllabique peut être mis en correspondance avec un triplet de pentades ($P_1$ = consonne initiale, $P_2$ = voyelle finale, $P_3$ = ton), et les 64 combinaisons binaires de traits modélisent naturellement l’ensemble de l’inventaire syllabique – un résultat qui sera détaillé ailleurs. De même, en économie (en s’appuyant sur la "Théorie du Rachat", Rebour, 2000), les six facteurs binaires (inflation, salaires, profits, rachat, dispersion, régime foncier) génèrent 64 états dont la dynamique cyclique suit la même organisation pentadique. Ces applications illustrent l’architecture universelle et et indépendante du domaine qui sous-tend le formalisme de Merkabah-Clifford, lequel fournit un fondement rigoureux pour l’intelligence artificielle régulée.

# Remerciements
Nous remercions Peter Rowlands pour ses travaux fondateurs sur les algèbres de Clifford nilpotentes et le code génétique. Nous remercions les assistants en IA sans lesquels ce travail serait resté une utopie.

# Références
[1] Crick, F. H. C. (1968). L’origine du code génétique. *J. Mol. Biol.*, 38(3), 367–379. 
[2] Nirenberg, M., & Leder, P. (1964). Mots-codes ARN et synthèse des protéines. *Science*, 145(3638), 1399–1407. 
[3] LeCun, Y., Bengio, Y., & Hinton, G. (2015). Apprentissage profond. *Nature*, 521(7553), 436–444. 
[4] Amodei, D., et al. (2016). Problèmes concrets liés à la sécurité de l'IA. *arXiv:1606.06565*. 
[5] Russell, S. (2019). *Human Compatible: AI and the Problem of Control*. Viking. 
[6] Freeland, S. J., & Hurst, L. D. (1998). The genetic code is one in a million. *J. Mol. Evol.*, 47(3), 238–248. 
[7] Koonin, E. V., & Novozhilov, A. S. (2017). Origine et évolution du code génétique : l’énigme universelle. *IUBMB Life*, 69(5), 282–296. 
[8] Woese, C. R. (1965). L’ordre dans le code génétique. *Proc. Natl. Acad. Sci. USA*, 54(1), 71–75. 
[9] Wong, J. T. (1975). Une théorie de la coévolution du code génétique. *Proc. Natl. Acad. Sci. USA*, 72(5), 1909–1912. 
[10] Rowlands, P. (2007). * De zéro à l'infini : les fondements de la physique*. World Scientific. (Chapitre 19, "Le code de la nature", coécrit avec V. Hill) 
[11] da Costa, N. C. A. (1974). Sur la théorie des systèmes formels incohérents. *Notre Dame Journal of Formal Logic*. 
[12] Priest, G. (2008). *Introduction à la logique non classique*. Cambridge University Press. 
[13] Belnap, N. D. (1977). Une logique à quatre valeurs utile. Dans *Modern Uses of Multiple-Valued Logic*. Reidel.

\newpage
# Annexe A – Dérivation des deux cycles de 5 (Wuxing externe) et des seuils à partir des 20 triplets

## A.1 Construction d’un graphe dual à partir des triplets de Merkabah
Les 12 pentades $P_1,\dots,P_6, N_1,\dots,N_6$ forment les sommets d’un graphe dual $\Gamma$ construit comme suit : deux pentades $X$ et $Y$ sont reliées par une arête s’il existe un attracteur $v$ (A à T) dont le triplet contient à la fois $X$ et $Y$. Cette construction est entièrement déterminée par le tableau de gauche (filtration de Merkabah) et ne nécessite aucun objet géométrique externe.

Le graphe $\Gamma$ présente des propriétés structurelles remarquables :
- Il contient exactement deux cycles de longueur 5 disjoints (ceintures tropicales) $C_P$ et $C_N$ composés de pentades de même signe.
- Les deux pentades restantes $P_4$ et $N_4$ agissent comme des nœuds de haut degré reliant les deux ceintures.
- Le sous-graphe induit par $C_P$ est complet ($K_5$), tandis que $C_N$ ne possède que deux arêtes internes supplémentaires.

Ces propriétés émergent algorithmiquement de la combinatoire de Merkabah et fournissent le squelette de la dynamique externe de Wuxing sans nécessiter de projection sur un dodécaèdre. Bien que le graphe d'adjacence de l'attracteur (20 sommets, 30 arêtes, 3-régulier, circonférence 5, diamètre 5) est topologiquement isomorphe au squelette dodécaédrique, cet isomorphisme est une curiosité mathématique plutôt qu’une nécessité structurelle. Toutes les caractéristiques dynamiques — ceintures tropicales, seuils, cycles sheng/ke — sont définies intrinsèquement à partir du graphe dual des pentades.

## A.2 Extraction des 12 faces pentagonales (pentades)
Chaque face pentagonale du dodécaèdre correspond à une pentade fixe $X \in \{P_1,\dots,P_6, N_1,\dots,N_6\}$. Les cinq sommets incidents à la pentade $X$ sont précisément les triplets d'attracteurs contenant $X$. Par exemple :
- $P_1$ appartient aux classes A, B, F, J, P → forme le pentagone $P_1$
- $P_2$ appartient aux classes A, C, G, K, Q → forme le pentagone $P_2$
… (symétriquement pour les 12 pentades)

Cette structure d’incidence partitionne les 30 arêtes en 12 cycles de 5 disjoints, chacun définissant une face pentagonale.

## A.3 Formation des ceintures tropicales $C_P$ et $C_N$
En analysant l’adjacence duale des pentades (deux pentades sont dualement adjacentes si elles partagent une arête dans le dodécaèdre), nous identifions deux anneaux disjoints de cinq pentades chacun :
$$ C_P = (P_1 \to P_2 \to P_3 \to P_5 \to P_6 \to P_1) $$
$$ C_N = (N_1 \to N_2 \to N_6 \to N_5 \to N_3 \to N_1) $$
Ces séquences sont des cycles fermés de longueur 5 dans le graphe dual. Géométriquement, elles correspondent à deux bandes équatoriales de faces pentagonales qui s'enroulent autour du dodécaèdre sans se croiser. Les pentades restantes, $P_4$ et $N_4$, sont absentes des deux cycles.

## A.4 Parcours directionnel : sheng et ke
Chaque cycle de 5 admet deux parcours hamiltoniens :
- Sheng (génératif) : suit les arêtes adjacentes dans le graphe dual $(X_i \to X_{i+1})$. Ce chemin préserve la continuité de la polarité locale et correspond à des transitions d'états à faible contrainte.
- Ke (régulateur) : suit les arêtes "saut d'une unité" $(X_i \to X_{i+1} {i+2} \mod 5)$, ce qui équivaut à parcourir le pentagramme inscrit dans le pentagone. Ce chemin maximise la distance entre les pentades au sein du cycle, renforçant ainsi la rétroaction régulatrice et réduisant l'espace d'états accessible.

Mathématiquement, les deux modes de parcours correspondent aux deux générateurs du groupe cyclique $C_5$ agissant sur les indices des pentades, et leur superposition donne le groupe de symétrie complet de la face pentagonale.

## A.5 Justification de P4 et N4 en tant que seuils polaires
L'analyse d'adjacence révèle que $P_4$ et $N_4$ sont les seules pentades qui n'appartiennent ni à $C_P$ ni à $C_N$. Leurs sommets incidents sont exclusivement de polarité mixte :
- $P_4$ se connecte aux classes D, H, L, M, N (toutes 2P+N ou 1P+2N)
- $N_4$ est relié aux classes F, I, O, T, Q (toutes 2P+N ou 1P+2N)

Ni $P_4$ ni $N_4$ ne partagent d’arête avec un sommet de signature 3P ou 3N. Dans l’imbrication dodécaédrique, ils correspondent aux deux faces polaires. Toute transition entre la ceinture positive $C_P$ et la ceinture négative $C_N$ doit passer par au moins l’une de ces faces polaires. Par conséquent, ils fonctionnent comme des seuils structurels : ils régulent le changement de régime entre la dynamique générative (dominée par sheng) et régulatrice (dominée par ke) en contrôlant l'accès à la ceinture opposée. Cette architecture à double ceinture et double seuil réalise le Wuxing externe sous la forme d'une boucle de contrôle fermée et auto-limitante intégrée dans la géométrie de l'espace d'états à 20 attracteurs.

\newpage
## A.6 Les tétraèdres 16+4 (Merkabah) avec les pentades correspondantes
\begingroup
\small
\setlength{\tabcolsep}{4pt}
\begin{longtable}{|c|c|c|c|c|c|}
\hline
\multicolumn{6}{|c|}{\textbf {16 tétraèdres principaux}} \\
\hline
\textbf{État} & \textbf{Tétraèdre} & \textbf{Position} & \textbf{États finaux} & \textbf{Pentades} & \textbf{Type} \\
\hline
1 & A & Centre & 1,2,3, 4 & $\{P_1,P_2,P_4\}$ & 3P \\
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
13 & M & Sommet Ouest & 49,50,51,52 & $\{P_4,N_1,N_3\} $ & 1P+2N \\
14 & N & Diagonale 1 & 53,54,55,56 & $\{P_4,N_5,N_6\}$ & 1P+2N \\
15 & O & Diagonale 2 & 57,58,59,60 & $\{P_5,N_1,N_4\}$ & 1P+2N \\
16 & P & Diagonale 3 & 61,62,63,64 & $\{P_6,N_1,N_2\}$ & 1P+2N \\
\hline
\caption{Les 16 tétraèdres principaux}
\end{longtable}
\endgroup

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
\caption{Les 4 tétraèdres d'intersection (représentation des tétraèdres principaux dérivée des indices d'état)}
\end {longtable}
\endgroup

Les tétraèdres d'intersection Q, R, S et T correspondent à des nœuds topologiques au cœur de la structure Merkabah, où convergent trois des 20 régions tétraédriques interpénétrantes. Leur triplet de pentades est déterminé par l'intersection exacte de trois faces principales, ce qui en fait les seuls nœuds du réseau ayant les signatures 1P+2N (Q, R, S) ou 3 N (T).

### A.6.1 Règle de sélection pour les états booléens aux intersections
Les nœuds d'intersection héritent exactement d'un état de chacun de leurs trois tétraèdres parents, limités aux états booléens quaternaires où la dimension structurelle primaire $A$ est affirmée : l'état d'ancrage $+$, codé comme $A \cap \neg B$ $(1,0)$, et l'état d'interface $m$, codé comme $A \cap B$ $(1,1)$. La sélection suit une règle topologique déterministe régissant la dimension secondaire $B$. Un parent contribue à l'état d'interface $m$ $(1,1)$ si et seulement si sa signature de polarité est extrême (3P) ou s'il sert de référence structurelle par rapport à l'intersection. Les pôles extrêmes possèdent une rigidité élevée ; fournir uniquement l'état d'ancrage $(1,0)$ romprait la connectivité avec les zones à signature mixte. Au lieu de cela, ils basculent la dimension secondaire sur $1 $, ce qui donne l'état de charnière $m$ qui préserve la capacité de référence tout en permettant la flexibilité de l'interface. Les parents résidant déjà dans des zones mixtes (2P+1N ou 1P+2N) maintiennent la dimension secondaire à $0$, contribuant ainsi à l'état d'ancrage stable $(1,0)$. Cette règle donne lieu à une attribution déterministe : Q hérite de $B^m$ (B est 3P), tandis que F et G fournissent $F^+$ et $G^+$. R et S n'héritent que des états $+$ de leurs parents déjà mixtes. T hérite de $P^m$ comme référence locale pour le noyau interne, O fournissant $O^+$. Le mécanisme garantit que chaque intersection comporte exactement une charnière relationnelle ($m$) et deux ancrages structurels ($+$), maintenant la cohérence du réseau global sans paramètres libres.

# Annexe B – Correspondance géométrique-algébrique et structure de dégénérescence

## B.1 Principes d’isomorphisme structurel
La correspondance entre l’espace de Clifford $Cl(6,0)$ et le code génétique repose sur cinq principes structurels interdépendants, qui, ensemble, contraignent la réduction 64→20 à une seule partition à l’exception d’une rotation globale :
1. **Équivalence duale** : Les 64 unités algébriques de $Cl(6,0)$ correspondent de manière bijective aux 64 codons, tandis que les 20 triplets de pentades correspondent aux 20 acides aminés fonctionnels. Cela établit un isomorphisme à trois voies entre l'espace de configuration algébrique, l'imbrication géométrique et la fonction biologique.
2. *
 *Corrélation position-polarité** : La centralité et la symétrie géométriques dictent la signature de polarité. Les trois tétraèdres centraux/symétriques (A, B, C) se projettent sur des triplets entièrement positifs (3P). À mesure que les positions géométriques deviennent plus périphériques ou s’intersectent, des pentades négatives sont introduites, faisant basculer la signature vers 1P+2N et finalement 3N.
3. **Conservation de l'adjacence et du signe** : deux tétraèdres partageant une face ou une arête dans la Merkabah partagent exactement deux pentades dans leur représentation en triplets, préservant ainsi la structure locale du voisinage. Les positions opposées sur le double tétraèdre présentent des triplets à signe inversé, maintenant ainsi la symétrie bicosmique globale.
4. **Distribution uniforme des pentades** : Chacune des 12 pentades ($P_1\dots P_6$, $N_1\dots N_6$) apparaît dans exactement cinq triplets distincts. Cette incidence uniforme garantit qu’aucune pentade ne domine le processus de filtrage et que les 20 classes sont réparties de manière équidistante sur le dual dodécaédrique.
5. **Topologie constructive** : La partition est générée de manière algorithmique en (i) assignant les 12 pentades aux faces d'un dodécaèdre, (ii) considérant chaque sommet comme l'intersection de trois faces incidentes (ce qui donne un triplet), (iii) classant selon la signature de polarité, et (iv) réintégrant le tout dans la Merkabah. Le code biologique émerge comme une lecture directe de cette construction topologique.

## B.2 Base géométrique de la dégénérescence des codons

Précision : La corrélation entre la position géométrique et la dégénérescence des codons est établie au niveau du double tétraèdre (Merkabah), où le chevauchement des pentades détermine la taille des classes. La représentation dodécaédrique est introduite par la suite (§3.4) pour analyser la dynamique inter-attracteurs et les cycles Wuxing externes.

Le schéma de dégénérescence du code génétique n'est pas distribué de manière aléatoire ; il reflète la densité géométrique du réseau de pentades au sein de la Merkabah :
- Les attracteurs 3P (A, B, C) occupent des positions centrales, sans chevauchement. Leur isolement dans le graphe des pentades limite la taille du voisinage, ce qui correspond à des acides aminés à faible dégénérescence (1–2 codons), y compris le signal d'initiation (méthionine).
- Les attracteurs 2P+N (D–H) se situent sur les faces et les arêtes primaires. Un chevauchement modéré des pentades entraîne une dégénérescence moyenne (3–4 codons), typique des acides aminés structurellement polyvalents.
- Les attracteurs 1P+2N (I–S) sont concentrés sur les sommets, les diagonales et les zones d’intersection. Les intersections Q, R et S représentent un chevauchement maximal des pentades, permettant géométriquement de multiples chemins de voisinage équivalents. Cette redondance structurelle correspond directement à des acides aminés hautement dégénérés (6 codons : sérine, leucine, arginine).
- L'attracteur 3N (T) se situe à la position d'intersection la plus interne, structurellement isolé de la ceinture positive. Dans la correspondance biologique, ce sommet accueille à la fois la cystéine et les trois codons de terminaison, reflétant un rôle fonctionnel commun en tant qu'états limites qui arrêtent ou limitent la traversée traductionnelle.

## B.3 Contraintes de symétrie et unicité de la correspondance

La partition 64→20 est rigide sous le groupe d'automorphismes du double tétra . Toute bijection qui préserve
 (i) l'adjacence par partage de faces, (ii) l'incidence des pentades (5 par pentade) et (iii) l'appariement par complémentarité (A↔U, G↔C par négation binaire) donne les mêmes classes d'équivalence, à l'exception du relibellage des 20 sommets et d'une rotation globale du dodécaèdre. Cette contrainte de symétrie garantit que la correspondance observée avec le code génétique n'est pas un artefact d'un codage arbitraire, mais une propriété structurelle de la géométrie sous-jacente $Cl(6,0)$. La correspondance est donc essentiellement unique au sein de sa classe topologique, fournissant une explication mathématiquement fondée à la régularité observée dans les associations codon-acide aminé.

\newpage
# Annexe C – Primitives sémantiques et correspondance de Clifford

## C.1 Origine fonctionnelle de la nomenclature sémantique (A–P)
Les 16 concepts centraux ne résultent pas d’une attribution arbitraire, mais d’une lecture fonctionnelle des invariants algébro-topologiques. Chaque terme décrit le rôle opérationnel joué par la position correspondante au sein d’un réseau de régulation discret :

\begingroup
\small
\renewcommand{\tabularxcolumn}[1]{>{\raggedright\arraybackslash}m{#1}}
\setlength{\tabcolsep}{4pt}
\renewcommand{\arraystretch}{1.25}

\begin{table}[htbp]
\centering
\caption{Origine fonctionnelle de la nomenclature sémantique (A--P)}
\label{tab:semantic_origin}
\begin{tabularx}{\textwidth}{|X|X|X|X|}
\hline
\textbf{Signature algébrique [$\mathrm{Cl}(4,0)$]} & \textbf{Rôle topologique dans la Merkabah} & \textbf{Fonction systémique} & \textbf{Concept attribué} \\
\hline
$1$ (scalaire, degré 0, signe positif) & Pôle de référence, sans chevauchement & État de référence / point de consigne & \textbf{Action / Vérité} (capacité à initier une transition à partir d'un état neutre) \\
\hline
$I, J, K$ (générateurs, degré 1, signe positif) & Faces externes, faible intersection & Canaux d'entrée directionnels & \textbf{Contribution} (entrée structurelle), \textbf{Apparence} (projection observable), \textbf{Perception} (capture de différence) \\
\hline
$-1$ (scalaire inversé, degré 0, signe négatif) & Contrainte globale imposée & Rupture de symétrie / imposition d'ordre & \textbf{Organisation} (structuration par limite) \\
\hline
$-I, -J, -K$ (générateurs inversés, degré 1, signe négatif) & Arêtes primaires, modulation intermédiaire & Différenciation, mélange, invariance relationnelle & \textbf{Différence}, \textbf{Mélange}, \textbf{Équivalence} \\
\hline
$i'I, i'J, i'K$ (couplage pseudo-scalaire, degré 3/4) & Sommets / diagonales, intersection élevée & Couplage phase-charge, transfert directionnel & \textbf{Relation} (couplage), \textbf{Flux} (transfert orienté), \textbf{Entité} (identité délimitée) \\
\hline
$-i'I, -i'J, -i'K$ (couplage inversé) & Zones d'intersection maximales, haute redondance & Évolution contrainte, dépendance contextuelle, fluctuation adaptative & \textbf{Évolution}, \textbf{Dépendance}, \textbf{Variation} \\
\hline
\end{tabularx}
\end{table}
\endgroup

Cette correspondance s'inscrit dans la tradition de la sémantique fonctionnelle en théorie des systèmes : tout comme des termes tels que *entropie*, *gain* ou *rétroaction* désignent les rôles opérationnels de constructions mathématiques, les 16 concepts utilisés ici qualifient la fonction régulatrice de chaque nœud dans le graphe d'adjacence. Leur validité ne repose pas sur une intuition externe, mais sur une cohérence prédictive : les mêmes rôles fonctionnels se manifestent dans la dégénérescence du code génétique (faible pour les pôles de référence, maximale pour les intersections), dans la phonologie syllabique (consonne/voyelle/ton comme canaux directionnels) et dans les cycles économiques (facteurs de contrainte vs facteurs de flux). La nomenclature A–P est donc une couche descriptive contrainte par la structure, et non un paramètre libre.
\newpage

## C.2 Les 16 éléments de Cl(4,0) et les 4 éléments supplémentaires

\begingroup
\small
\setlength{\tabcolsep}{4pt}
\begin{longtable}{|c|c|c|c|c|c|}
\hline
\textbf{Cl(4,0)} & \textbf{Rang} & \textbf{Latin} & \textbf{Concept central} & \textbf{Concepts (×4 par lettre)} & \textbf{Triplet de polarité} \\
\hline
1 & 1 & A & Action/Vérité & 1:A+, 2:A-, 3:Am, 4:A${\ sim}m$ & $\{P_1,P_2,P_4\}=3P$ \\
I & 2 & B & Contribution & 5:B+, 6:B-, 7:Bm, 8:B${\sim}m$ & $\{P_1,P_3,P_5\}=3P$ \\
J & 3 & C & Apparence & 9:C+, 10:C-, 11:Cm, 12:C${\sim} m$ & $\{P_2,P_3,P_6\}=3P$ \\
K & 4 & D & Perception & 13:D+, 14:D-, 15:Dm, 16:D${\sim}m$ & $\{P_4,P_5,N_2\}=2P+1N$ \\
-1 & 5 & E & Organisation & 17:E+, 18:E-, 19:Em, 20:E${\sim}m$ & $\{P_5,P_6,N_3\}=2P+1N$ \\
-I & 6 & F & Différence & 21:F+, 22:F-, 23:Fm, 24:F${\sim}m$ & $\{P_1,P_6,N_4\}=2P+1N$ \\
-J & 7 & G & Mélange & 25:G+, 26:G-, 27:Gm, 28:G${\sim}m$ & $\{P_2,P_5,N_6\}=2P+1N$ \\
-K & 8 & H & Équivalence & 29:H+, 30:H-, 31:Hm, 32:H${\sim}m$ & $\{P_3,P_4,N_6\}=2P+1N$ \\
$i'1$ & 9 & I & Relation & 33:I+, 34:I-, 35:Im, 36:I${\sim}m$ & $\{P_1,N_2,N_6\}=1P+2N$ \\
$i'I$ & 10 & J & Flux & 37:J+, 38:J, 39:Jm, 40:J${\sim}m$ & $\{P_1,N_3,N_5\}=1P+2N$ \\
$i'J$ & 11 & K & Entité & 41:K+, 42:K-, 43:Km, 44:K${\sim}m$ & $\{P_2,N_3,N_5\}=1P+2N$ \\
$i'K$ & 12 & L & Cercle/Cycle & 45:L+, 46:L-, 47:Lm, 48:L${\sim}m$ & $\{P_3,N_2,N_4\}=1P+2N$ \\
$-i'1$ & 13 & M & Évolution & 49:M+, 50:M-, 51:Mm, 52:M${\sim}m$ & $\{P_4,N_1,N_3\}=1P+2N$ \\
$-i'I$ & 14 & N & Dépendance & 53:N+, 54:N-, 55: Nm, 56:N${\sim}m$ & $\{P_4,N_5,N_6\}=1P+2N$ \\
$-i'J$ & 15 & O & Variation & 57:O+, 58:O-, 59:Om, 60:O${\sim}m$ & $\{P_5,N_1,N_4\}=1P+2N$ \\
$-i'K$ & 16 & P & Regroupement & 61:P+, 62:P-, 63:Pm, 64:P${\sim}m$ & $\{P_6,N_1,N_2\}=1P+2N$ \\
 & 17 & Q & Synergie & 7:Bm, 21:F+, 25:G & $\{P_2,N_1,N_4\}=1P+2N$ \\
 & 18 & R & Résonance & 29:H+, 33:I+, 37:J+ & $\{P_3,N_1,N_5\}=1P+2N$ \\
 & 19 & S & Spirale & 45:L+, 49:M+, 53:N+ & $\{P_6,N_5,N_6\}=1P+2N$ \\
 & 20 & T & Stratification & 57:O+, 61:P+, 63:Pm & $\{N_2,N_3,N_4\}=3N$ \\
\hline
\caption{Les 16 éléments de Cl(4,0) et les 4 éléments supplémentaires}
\end{longtable}
\endgroup

*Remarque : Les étiquettes sémantiques sont des lectures fonctionnelles d'invariants -topologiques. L'expansion quaternaire ($+,-,m,\sim m$) correspond directement aux combinaisons à 2 bits du formalisme booléen (§2.2.1).*
\newpage

## C.3 Les 16 tétrades de Cl(6,0) étendues à 64 concepts

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
\caption{Les 16 tétrades de Cl(6,0) (64 concepts)}
\end{longtable}
\endgroup

\newpage

# Annexe D – Pentades positives et négatives : alignement avec les 64 tétrades

## D.1 Pentades positives et négatives : alignement avec les 64 tétrades

\begingroup
\footnotesize
\setlength{\tabcolsep}{2.2pt}
\renewcommand{\arraystretch}{1.15}
\centering
\begin{longtable}{|c|c|l||c|c|l|}
\hline
\multicolumn{3} {c||}{\textbf{Pentades positives ($P_1$–$P_6$)}} & \multicolumn{3} {c}{\textbf{Pentades négatives ($N_1$–$N_6$)}} \\
\cline{1-6}
\textbf{Pentade} & \textbf{Éléments de Clifford} & \textbf{Correspondance tétradique (N°/Concept)} & \textbf{Pentade} & \textbf{Éléments de Clifford} & \textbf{Correspondance tétradique (N°/Concept)} \\
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
Jj \rightarrow 11\;
 (C^m) \\
Kj \rightarrow 15\;(D^m) \\i'1i \rightarrow 34\;(I^-) \\1k \rightarrow 4\;(A^{\sim m})\end{array}$ &$N_2$ & $\{-Ij,\; -Jj,\; -Kj,\; -i'1i,\; -1k\}$ &$\begin{array}{@{}l@{}}-Ij \rightarrow \text{dual}(7) \\-Jj \rightarrow \text{dual}(11) \\-Kj \rightarrow \text{dual}(15) \\-i'1i \rightarrow 37\;(J^+) \\-1k \rightarrow 2\;(A^-)\end{array}$ \\\hline$P_3$ & $\{Ik,\; Jk,\; Kk,\; i'1j,\; 1i\}$ &$\begin{array}{@{}l@{}}Ik \rightarrow 8\;(B^{\sim m}) \\Jk \rightarrow 12\; (C^{\sim m}) \\Kk \rightarrow 16\;(D^{\sim m}) \\i'1j \rightarrow 35\;(I^m) \\1i \rightarrow 2\;(A^-)\end{array}$ &$N_3$ & $\{-Ik,\; -Jk,\; -Kk,\; -i'1j,\; -1i\}$ &$\begin {array}{@{}l@{}}-Ik \rightarrow \text{dual}(8) \\-Jk \rightarrow \text {dual}(12) \\-Kk \rightarrow \text{dual}(16) \\-i'1j \rightarrow 33\;(I^+) \\-1i \rightarrow 1\;(A^+)\end{array}$ \\\hline$P_4$ & $\{i'Ii,\; i'Ij,\; i'Ik, \; i'K,\; J\}$ &$\begin{array}{@{}l@{}}i'Ii \rightarrow 38\;(J^-) \\i'Ij \rightarrow 39\;(J^m) \\i'Ik \rightarrow 40\;(J^{\sim m}) \\i'K \rightarrow 45\;(L^+) \\J \rightarrow 9\;(C^+)\end{array}$ &$N_4$ & $\{-i'Ii,\; -i'Ij,\; -i'Ik,\; -i'K,\; -J\}$ &$\begin{array}{@{}l@{}}-i'Ii \rightarrow 37\ ;(J^+) \\-i'Ij \rightarrow \text{dual}(39) \\-i'Ik \rightarrow \text{dual}(40) \\-i'K \rightarrow 46\;(L^-) \\-J \rightarrow 10\;(C^-)
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
$P_6$ & $\{i'Ki, \; i'Kj,\; i'Kk,\; i'J,\; I\}$ &
$\begin{array}{@{}l@{}}
i'Ki \rightarrow 46\;(L^-) \\
i'Kj \rightarrow 47\;(L^m) \\
i'Kk \rightarrow 48\ ;(L^{\sim m}) \\
i'J \rightarrow 41\;(K^+) \\
I \rightarrow 5\;(B^+)
\end{array}$ &
$N_6$ & $\{-i'Ki,\; -i'Kj,\; -i'Kk,\; -i'J,\; -I\}$ &
$\begin{array} {@{}l@{}}
-i'Ki \rightarrow 45\;(L^+) \\
-i'Kj \rightarrow \text{dual}(47) \\
-i'Kk \rightarrow \text{dual}(48) \\
-i'J \rightarrow 42\;(K^-) \\
-I \rightarrow 6\;(B^-)
\end{array}$ \\
\hline
\caption{Pentades positives et négatives : alignement strict avec les 64 tétrades de $\mathrm{Cl}(6,0)$}
\label{tab:pentads}
\end{longtable}
\endgroup

*Les éléments des pentades sont réécrits dans l'ordre canonique $i<j<k<I<J<K$. Les signes induits par l'anticommutation ($ab=-ba$) sont reportés à l'état booléen correspondant, garantissant une bijection stricte avec le tableau des 64 tétrades.*

\newpage
![Graphique dual des pentades](Penta_graph.png){ width=100% }
