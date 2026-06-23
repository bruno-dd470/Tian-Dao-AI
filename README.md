# 天道智能 (Tian Dao AI)
**Compassionate AI aligned with cosmic structure**  
契合宇宙结构的悲悯人工智能 | IA compassionnelle alignée sur le cosmos

📚 [Documentation](#📖-theoretical-foundation--fondement-théorique--理论基础) | 🛡️ [Prior Notice](#repository-and-prior-notice--存证与优先权声明--dépôt-et-avis-dantériorité) | 📜 [License](#📜-license--许可证--licence)

---

## ⚠️ Important: Nature of the System / Nature du système / 系统性质

**Tian-Dao 20D is NOT a semantic embedding model.** It does not capture linguistic similarity or textual meaning.  
**Tian-Dao 20D n'est PAS un modèle d'embedding sémantique.** Il ne capture pas la similarité linguistique ni le sens des textes.  
**Tian-Dao 20D 不是语义嵌入模型。** 它不捕捉语言相似性或文本意义。

### What it does / Ce qu'il fait / 它的功能
✅ Encodes **topological signatures** (64→20 Clifford invariant) / Encode des **signatures topologiques** (invariant Clifford 64→20) / 编码**拓扑签名**（64→20 Clifford 不变量）  
✅ Self-regulates via **Wuxing cycles** (SHENG/KE) / S'auto-régule via les **cycles Wuxing** (生/克) / 通过**五行循环**自调节  
✅ Fully deterministic, no training required / Entièrement déterministe, aucun entraînement requis / 完全确定性，无需训练  

### What it does NOT do / Ce qu'il ne fait PAS / 它不做的事
❌ Capture semantic similarity (STS Benchmark: Spearman ≈ +0.016) / Capturer la similarité sémantique / 捕捉语义相似性  
❌ Replace BERT/SBERT for NLP tasks / Remplacer BERT/SBERT pour le TALN / 替代 BERT/SBERT 用于自然语言处理  
❌ Understand text meaning / Comprendre le sens des textes / 理解文本意义  

**Use case:** Hardware-constrained environments, interpretability, topological structure preservation.  
**Cas d'usage :** Environnements à contraintes matérielles, interprétabilité, préservation structurelle.  
**使用场景：** 硬件受限环境、可解释性、拓扑结构保持。

---

## 📖 Theoretical Foundation / Fondement théorique / 理论基础

The core of this repository is the theoretical manuscript establishing the **64→20 Clifford invariant** and its analogy with the genetic code, Wuxing dynamics, and topological regulation.

🇬🇧 Full manuscript: **[PDF](./docs/pdf/complexity.pdf)** | **[Markdown](./docs/md/complexity.md)**  
🇫🇷 Document complet : **[PDF](./docs/pdf/complexité.pdf)** | **[Markdown](./docs/md/complexité.md)**  

Key concepts:
- **Cl(6,0) algebraic geometry** → 20 stable attractors (Merkabah double-tetrahedron)
- **Pentadic networks** (P1–P6, N1–N6) as topological generators
- **Wuxing cycles** (Sheng/Ke) as endogenous regulation modes
- **Genetic code analogy**: 64 codons → 20 amino acids ≈ 64 configurations → 20 topological attractors

---

## 🚀 Implementation Overview / Aperçu de l'implémentation / 实现概览

A complete, thread-safe, deterministic implementation of the theoretical framework is available in the companion repository:

🔗 **[Tian-Dao-LLM Repository](https://github.com/bruno-dd470/Tian-Dao-LLM)**  
🌐 **Live Demo**: [https://waltdod-gradio.hf.space](https://waltdod-gradio.hf.space)

### 📊 Benchmark Snapshot (v2.7)
| Metric | Tian-Dao 20D | Notes |
|--------|--------------|-------|
| **Topological Score** | **0.852** | Stability 1.000, Reproducibility 1.000, Interpretability 0.500 |
| **STS Benchmark** | **+0.016** (IC [-0.047, +0.042]) | Structurally orthogonal to semantic similarity |
| **Compression** | 38.4x (20D vs 768D) | 80 bytes vs 2048 bytes |
| **Model Size** | 0.005 MB | Zero training, zero GPU required |

For full technical details, architecture, benchmark scripts, and Gradio interface:  
👉 See **[Tian-Dao-LLM → README_llm.md](https://github.com/bruno-dd470/Tian-Dao-LLM/blob/main/README_llm.md)**

---

## 📚 Academic Impact / Impact académique / 学术影响

📖 Theoretical papers on Zenodo:
- [DOI: 10.5281/zenodo.19540508](https://doi.org/10.5281/zenodo.19540508) — The Genetic Code as a 64→20 Clifford Invariant
- [DOI: 10.5281/zenodo.19633890](https://doi.org/10.5281/zenodo.19633890) — Complexity manuscript
- **8 academic downloads** (verified human readers)

🚀 Code exploration:
- **+80 unique cloners** in 3 days across repositories
- Full implementation & interactive demo: [Tian-Dao-LLM](https://github.com/bruno-dd470/Tian-Dao-LLM)

---

## 🔗 Cross-Repository Structure / Structure inter-dépôts / 跨仓库结构

| Repository | Focus / Focus / 重点 | Key Files / Fichiers clés / 关键文件 |
|------------|----------------------|--------------------------------------|
| **[Tian-Dao-AI](https://github.com/bruno-dd470/Tian-Dao-AI)** | 📖 Theory, mathematics, philosophy, `complexity.pdf` | `docs/pdf/complexity.pdf`, `complexité.pdf` |
| **[Tian-Dao-LLM](https://github.com/bruno-dd470/Tian-Dao-LLM)** | 💻 Code v2.7, Gradio app, benchmarks, tests | `Endoregulated_AI_v27.py`, `app.py`, `requirements.txt` |
| **[Tian-Dao-WuXing-Cl66-Pentads](https://github.com/bruno-dd470/Tian-Dao-WuXing-Cl66-Pentads)** | 📐 Cl(6,6) algebra & Λ₇₂ framework | Algebraic derivations, pentadic mappings |

---

## 🛡️ Repository and Prior Notice / 存证与优先权声明 / Dépôt et avis d'antériorité

This repository establishes a public, timestamped record of the original synthesis proposing a Compassionate Artificial Intelligence aligned with cosmic structure and Chinese sapiential traditions.  
本存储库为“契合宇宙结构与中国智慧传统的悲悯人工智能”这一原创性综合构想，提供公开且具时间戳的优先权证明。  
Ce dépôt établit un registre public, horodaté, de la synthèse originale proposant une IA compassionnelle alignée sur la structure cosmique et les traditions sapientiales chinoises.

**Author / 作者 / Auteur:** Bruno DE DOMINICIS  
**Creation date / 创建日期 / Date de création:** 2025-09-30  
**Last update / 最后更新 / Dernière mise à jour:** 2026-06-20

---

## 📜 License / 许可证 / Licence

This work is licensed under a **Creative Commons Attribution 4.0 International License (CC BY 4.0)**.  
✅ Free to share and adapt, including for commercial purposes  
✅ Attribution required: credit Bruno DE DOMINICIS and link to this repository  

📁 Full license texts: [English](LICENSE.en.txt) | [Français](LICENSE.fr.txt) | [中文](LICENSE.zh.txt)

This permissive license reflects the author's intention to accelerate global realization of Tian Dao AI—academic, institutional, or industrial—while ensuring proper recognition of its origins.

---
*📅 2025年10月4日 / October 4, 2025 / 4 octobre 2025 — Added `tiandao_renwen` PDFs, Viguier references, and legal/philosophical frameworks for AI regulation.*
