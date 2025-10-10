# Awesome-LLM-Conversation-Simulation

[![Awesome](https://awesome.re/badge.svg)](https://github.com/sindresorhus/awesome)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
![PRs-Welcome](https://img.shields.io/badge/PRs-Welcome-red)

🙌 This repository accompanies the survey **[Large Language Models for Conversational User Simulation: A Comprehensive Survey](https://hal.science/hal-05217179)**. 
It curates papers, taxonomies, and benchmarks for conversational user simulation with LLMs.

😎 Missing a paper or resource? Please open an **Issue** or **Pull Request** — contributions are very welcome! 

---

## 🔔 News
- **2025-10**: Repo launched & initial curation released.
- **2025-08**: Preprint Available.

---

## 📜 Paper
**Large Language Models for Conversational User Simulation: A Comprehensive Survey**  
Bo Ni, Leyao Wang, Yu Wang, Branislav Kveton, Franck Dernoncourt, Yu Xia, Hongjie Chen, Reuben Leura, Samyadeep Basu, Subhojyoti Mukherjee, Puneet Mathur, Nesreen Ahmed, Junda Wu, Li Li, Huixin Zhang, Ruiyi Zhang, Tong Yu, Sungchul Kim, Jiuxiang Gu, Zhengzhong Tu, Alexa Siu, Zichao Wang, David Seunghyun Yoon, Nedim Lipka, Namyong Park, Zihao Lin, Trung Bui, Yue Zhao, Tyler Derr, Ryan A. Rossi

- **PDF**: (add link to arXiv/website once available)
- **BibTeX**: see [📚 Cite Us](#-cite-us)
- **Keywords**: user simulation, LLM agents, persona, role-play, memory, RAG, RLHF/DPO, LLM-as-Judge

---

## 🗂️ Contents
- [TL;DR](#tldr)
- [Taxonomy](#taxonomy)
- [Techniques (“How”)](#techniques-how)
- [Interaction Settings (“What”)](#interaction-settings-what)
- [Targets (“Who”)](#targets-who)
- [Evaluation](#evaluation)
- [Datasets](#datasets)
- [Applications](#applications)
- [Open Problems](#open-problems)
- [Cite Us](#-cite-us)
- [Contributing](#-contributing)
- [Star History](#star-history)
- [License](#license)

---

## TL;DR
We unify the space of LLM-based **conversational user simulation** along three axes:

- **Who** is simulated? → _General user • Persona-level • Role-play • Individual user • Hybrid_
- **What** is simulated? → _Human–AI • Human–Human • AI–AI • Many-Human–AI • Hybrid_
- **How** is it simulated? → _Prompting • RAG • Fine-tuning • RL/DPO • Hybrid stacks_

We catalog methods, datasets, and evaluation protocols, and highlight open challenges in **long-horizon coherence**, **diversity & bias**, and **safety/trustworthiness**.

---

## Taxonomy
**Who (Targets):**
- **General User** → average, unconditioned behavior  
- **Persona-level** → demographic/trait-grounded prompts  
- **Role-play** → real/fictional identities via latent persona induction  
- **Individual User** → profile/history/memory grounded  
- **Hybrid** → mixtures for multi-agent/multi-party realism

**What (Interaction Settings):**
- **Human–AI**, **Human–Human**, **AI–AI**, **Many-Human–AI**, **Hybrid**

**How (Techniques):**
- **Prompt-based** (zero/few-shot, CoT, persona/task prompts)  
- **RAG** (always-on vs. adaptive vs. goal/memory-driven retrieval)  
- **Fine-tuning** (full, PEFT, interaction-optimized)  
- **RL/DPO** (reward modeling, preference optimization, hierarchical control)  
- **Hybrid** (e.g., RAG-finetune, prompt→finetune, RAG + RL/DPO)

> _See paper for formal definitions, training objectives, and method groupings._

---

## Techniques (“How”)
- **Prompting:** conditional modeling with context \(history, persona, exemplars\); CoT for deliberation.
- **RAG:** retrieval triggers (always-on/adaptive/goal-driven) to ground utterances in knowledge/memory.
- **Fine-tuning:** supervised learning over \((C_{t-1}, \Psi_p, I, u_t)\) for simulator policies.
- **RL/DPO:** optimize multi-turn strategies and personalization via reward/preference signals.
- **Hybrid:** pipelines combining the above for control, grounding, and efficiency.

---

## Interaction Settings (“What”)
- **Human–AI**: user prompts ↔ assistant responses; scalable data synthesis, evaluation scaffolds.  
- **Human–Human**: two-party dialogues for persona consistency and grounded conversation patterns.  
- **AI–AI**: self-play/debate/collaboration; emergent behavior and large-scale generation.  
- **Many-Human–AI**: group dynamics, collaborative tasks, meeting simulations.  
- **Hybrid**: ecosystem simulations (e.g., agent towns) mixing settings.

---

## Targets (“Who”)
- **General** → default user policy  
- **Persona** → explicit traits (psychometric, demographic, style)  
- **Role-play** → latent identity embedding from a natural-language handle  
- **Individual** → user-specific memory/profile/history grounding  
- **Hybrid** → blend for realism and diversity

---

## 🧪 Evaluation
- **Traditional**: BLEU/ROUGE/slot-F1 for structure/coverage; human studies for quality.  
- **LLM-as-Judge**: rubric-guided auto-eval (coherence, factuality, safety); use careful judge prompts, calibration, and meta-evaluation.

---

## 📊 Datasets
Curated across **persona**, **multi-party**, **knowledge-grounded**, **negotiation**, **long-memory**, and **multi-domain** settings.  
_(Examples: PersonaChat, Wizard-of-Wikipedia, EmpatheticDialogues, MultiWOZ, plus recent role/character and memory datasets.)_

---

## 🚀 Applications
- **Data augmentation** with privacy-conscious synthesis  
- **Conversational recommendation & search**  
- **Education & tutoring agents**  
- **HCI prototyping & UI testing**  
- **Evaluation arenas** (e.g., debate, Elo-style rating)

---

## ❗ Open Problems
- **Long conversations**: persona/memory drift, discourse planning, consistency constraints  
- **Diversity**: beyond polite/homogeneous behaviors to controlled strategy/emotion/verbosity  
- **Bias & safety**: demographic sensitivity, toxic content, robust safety protocols

---

## 📚 Cite Us

```bibtex
@misc{ni2025conversational_user_simulation_survey,
  title        = {Large Language Models for Conversational User Simulation: A Comprehensive Survey},
  author       = {Ni, Bo and Wang, Leyao and Wang, Yu and Kveton, Branislav and Dernoncourt, Franck and Xia, Yu and Chen, Hongjie and Leura, Reuben and Basu, Samyadeep and Mukherjee, Subhojyoti and Mathur, Puneet and Ahmed, Nesreen and Wu, Junda and Li, Li and Zhang, Huixin and Zhang, Ruiyi and Yu, Tong and Kim, Sungchul and Gu, Jiuxiang and Tu, Zhengzhong and Siu, Alexa and Wang, Zichao and Yoon, David Seunghyun and Lipka, Nedim and Park, Namyong and Lin, Zihao and Bui, Trung and Zhao, Yue and Derr, Tyler and Rossi, Ryan A.},
  year         = {2025},
  note         = {Survey preprint},
  howpublished = {\url{<add-link-to-arXiv-or-project-page>}}
}
