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

## 📜 Survey
**Large Language Models for Conversational User Simulation: A Comprehensive Survey**  
Bo Ni, Leyao Wang, Yu Wang, Branislav Kveton, Franck Dernoncourt, Yu Xia, Hongjie Chen, Reuben Leura, Samyadeep Basu, Subhojyoti Mukherjee, Puneet Mathur, Nesreen Ahmed, Junda Wu, Li Li, Huixin Zhang, Ruiyi Zhang, Tong Yu, Sungchul Kim, Jiuxiang Gu, Zhengzhong Tu, Alexa Siu, Zichao Wang, David Seunghyun Yoon, Nedim Lipka, Namyong Park, Zihao Lin, Trung Bui, Yue Zhao, Tyler Derr, Ryan A. Rossi

- **[PDF](https://hal.science/hal-05217179)** 
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

---

## Taxonomy
**Who (Targets):**
- **General User** → average, unconditioned behavior  
- \[[arxiv](https://arxiv.org/abs/2305.18290)\] Direct Preference Optimization: Your Language Model is Secretly a Reward Model. `2023.05`
- \[[arxiv](https://arxiv.org/abs/2403.02502)\] Trial and Error: Exploration-Based Trajectory Optimization for LLM Agents. `2024.03`
- \[[arxiv](https://arxiv.org/abs/2409.02392)\] Building Math Agents with Multi-Turn Iterative Preference Learning. `2024.09`
- \[[arxiv](https://arxiv.org/abs/2502.01600)\] Reinforcement Learning for Long-Horizon Interactive LLM Agents. `2025.02`

- **Persona-level** → demographic/trait-grounded prompts  
- \[[ACL](https://aclanthology.org/2024.acl-long.554/)\] Quantifying the Persona Effect in LLM Simulations. `2024.08`
- \[[ACM](https://dl.acm.org/doi/10.1145/3708985)\] User Behavior Simulation with Large Language Model-based Agents. `2025.01`
- \[[ArXiv](https://arxiv.org/abs/2206.07550)\] Evaluating and Inducing Personality in Pre-trained Language Models. `2023.05`
- \[[ArXiv](https://arxiv.org/abs/2305.02547)\] PersonaLLM: Investigating the Ability of Large Language Models to Express Personality Traits. `2023.05`
- \[[ArXiv](https://arxiv.org/abs/2307.00184)\] Personality Traits in Large Language Models. `2023.07`
- \[[ArXiv](https://arxiv.org/abs/2406.12216)\] Is persona enough for personality? Using ChatGPT to reconstruct an agent's latent personality from simple descriptions. `2024.06`
- \[[ArXiv](https://arxiv.org/abs/2411.10006)\] Orca: Enhancing Role-Playing Abilities of Large Language Models by Integrating Personality Traits. `2024.11`
- \[[ArXiv](https://arxiv.org/abs/2304.05335)\] Toxicity in ChatGPT: Analyzing Persona-assigned Language Models. `2023.04`

- **Role-play** → real/fictional identities via latent persona induction  
- \[[ArXiv](https://arxiv.org/abs/2404.12138)\] Character is Destiny: Can Role-Playing Language Agents Make Persona-Driven Decisions?. `2024.11`
- \[[ArXiv](https://arxiv.org/abs/2304.03442)\] Generative Agents: Interactive Simulacra of Human Behavior. `2023.08`
- \[[ArXiv](https://arxiv.org/abs/2503.23514)\] If an LLM Were a Character, Would It Know Its Own Story? Evaluating Lifelong Learning in LLMs. `2025.03`
- \[[ACL](https://aclanthology.org/2025.coling-main.494/)\] RoleBreak: Character Hallucination as a Jailbreak Attack in Role-Playing Systems. `2025.01`
- \[[ArXiv](https://arxiv.org/abs/2406.17260)\] Mitigating Hallucination in Fictional Character Role-Play. `2024.11`
- \[[ArXiv](https://arxiv.org/abs/2405.14231)\] From Role-Play to Drama-Interaction: An LLM Solution. `2024.05`

- **Individual User** → profile/history/memory grounded  
- \[[ArXiv](https://arxiv.org/abs/1801.07243)\] Personalizing Dialogue Agents: I have a dog, do you have pets too?. `2018.09`
- \[[ArXiv](https://arxiv.org/abs/2112.08619)\] Call for Customized Conversation: Customized Conversation Grounding Persona and Knowledge. `2022.05`
- \[[ArXiv](https://arxiv.org/abs/2103.09534)\] Dialogue History Matters! Personalized Response Selectionin Multi-turn Retrieval-based Chatbots. `2021.03`
- \[[ArXiv](https://arxiv.org/abs/2107.07567)\] Beyond Goldfish Memory: Long-Term Open-Domain Conversation. `2021.07`
- \[[ArXiv](https://arxiv.org/abs/2504.19413)\] Mem0: Building Production-Ready AI Agents with Scalable Long-Term Memory. `2025.04`
- \[[ACL](https://aclanthology.org/2023.paclic-1.85/)\] RealPersonaChat: A Realistic Persona Chat Corpus with Interlocutors’ Own Personalities. `2023.12`
- \[[ACL](https://aclanthology.org/2023.acl-long.858/)\] LiveChat: A Large-Scale Personalized Dialogue Dataset Automatically Constructed from Live Streaming. `2023.07`


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
