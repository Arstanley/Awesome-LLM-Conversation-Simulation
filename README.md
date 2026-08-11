

# Awesome-LLM-Conversation-Simulation

[![Awesome](https://awesome.re/badge.svg)](https://github.com/sindresorhus/awesome)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
![PRs-Welcome](https://img.shields.io/badge/PRs-Welcome-red)

🙌 This repository accompanies the survey **[Large Language Models for Conversational User Simulation: A Comprehensive Survey](https://hal.science/hal-05217179)**.
It curates papers, taxonomies, and benchmarks for conversational user simulation with LLMs.

😎 Missing a paper or resource? Please open an **Issue** or **Pull Request** - contributions are very welcome!

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
- [Who: Simulation Targets](#who-simulation-targets)
  - [General User](#general-user)
  - [Persona-level](#persona-level)
  - [Role-play](#role-play)
  - [Individual User](#individual-user)
  - [Hybrid](#hybrid-simulation)
- [What: Interaction Settings](#what-interaction-settings)
  - [Human-AI](#humanai-simulation)
  - [Human-Human](#humanhuman-simulation)
  - [AI-AI](#aiai-simulation)
  - [Many-Human-AI](#many-humanai-simulation)
- [How: Techniques](#how-techniques)
  - [Prompting](#prompting)
  - [RAG & Retrieval](#rag--retrieval)
  - [Fine-tuning](#fine-tuning)
  - [RL/DPO](#rldpo)
  - [Hybrid Approaches](#hybrid-approaches)
- [Evaluation](#-evaluation)
- [Datasets](#-datasets)
- [Applications](#-applications)
- [Open Problems](#-open-problems)
- [Cite Us](#-cite-us)
- [Contributing](#-contributing)
- [License](#license)

---

## TL;DR
We unify the space of LLM-based **conversational user simulation** along three axes:

- **Who** is simulated? → _General user • Persona-level • Role-play • Individual user • Hybrid_
- **What** is simulated? → _Human-AI • Human-Human • AI-AI • Many-Human-AI • Hybrid_
- **How** is it simulated? → _Prompting • RAG • Fine-tuning • RL/DPO • Hybrid stacks_

---

## Taxonomy

The survey organizes conversational user simulation research across three dimensions:

**1. Who (Simulation Targets)** - what kind of user is being simulated
**2. What (Interaction Settings)** - what type of conversational interaction
**3. How (Technical Approaches)** - what methods are used to build the simulator

---

## Who: Simulation Targets

### General User

General user simulation models average behavior from a broad population without specific persona conditioning.

- [Direct Preference Optimization: Your Language Model is Secretly a Reward Model](https://arxiv.org/abs/2305.18290). `2023`
- [Trial and Error: Exploration-Based Trajectory Optimization for LLM Agents](https://arxiv.org/abs/2403.02502). `2024`
- [Building Math Agents with Multi-Turn Iterative Preference Learning](https://arxiv.org/abs/2409.02392). `2024`
- [Reinforcement Learning for Long-Horizon Interactive LLM Agents](https://arxiv.org/abs/2502.01600). `2025`

### Persona-level

Persona-level simulation conditions behavior on explicit demographic, psychometric, or stylistic attributes.

- [When crowd meets persona: Creating a large-scale open-domain persona dialogue corpus](https://arxiv.org/abs/2304.00350). `2023`
- [Synthetic patient-physician dialogue generation from clinical notes using LLM](https://arxiv.org/abs/2408.06285). `2024`
- [Interactive Dialogue Agents via Reinforcement Learning on Hindsight Regenerations](https://arxiv.org/abs/2411.05194). `2024`
- [Quantifying the Persona Effect in LLM Simulations](https://aclanthology.org/2024.acl-long.554/). `2024`
- [Orca: Enhancing role-playing abilities of large language models by integrating per- sonality traits](https://arxiv.org/abs/2411.10006). `2024`
- [Enhancing Persona Consistency for LLMs' Role-Playing using Persona-Aware Contrastive Learning](https://arxiv.org/abs/2503.17662). `2025`
- [Is Persona Enough for Personality? Using ChatGPT to Reconstruct an Agent's Latent Personality](https://arxiv.org/abs/2406.12216). `2024`
- [Personallm: In- vestigating the ability of large language models to express personality traits](https://arxiv.org/abs/2504.17993). `2024`
- [Deal or No Deal? End-to-End Learning for Negotiation Dialogues](https://arxiv.org/abs/1706.05125). `2017`
- [LLM Generated Persona is a Promise with a Catch](https://arxiv.org/abs/2503.16527). `2025`
- [A Survey of Personalized Large Language Models: Progress and Future Directions](https://arxiv.org/abs/2502.11528). `2025`
- [Character is Destiny: Can Role-Playing Language Agents Make Persona-Driven Decisions?](https://arxiv.org/abs/2404.12138). `2024`

### Role-play

Role-play simulation enables LLMs to embody real or fictional identities through latent persona induction.

- [If an LLM were a character, would it know its own story? evaluating lifelong learning in llms](https://arxiv.org/abs/2503.23514). `2025`
- [Agentsociety: Large-scale simulation of llm-driven generative agents advances understanding of human behaviors and society](https://arxiv.org/abs/2502.08691). `2025`
- [RoleBreak: Character Hallucination as a Jailbreak Attack in Role-Playing Systems](https://aclanthology.org/2025.coling-main.494/). `2025`
- [Rolecraft-glm: Advancing person- alized role-playing in large language models](https://arxiv.org/abs/2401.09432). `2024`
- [CharacterEval: A Chinese Benchmark for Role-Playing Conversational Agent Evaluation](https://arxiv.org/abs/2401.01275). `2024`
- [Enhancing Personalized Multi-Turn Dialogue with Curiosity Reward](https://arxiv.org/abs/2504.03206). `2025`
- [Autogen: En- abling next-gen LLM applications via multi-agent conversation framework](https://arxiv.org/abs/2308.08155). `2023`

### Individual User

Individual user simulation grounds behavior in specific user profiles, histories, and long-term memory.

- [SoulChat: Improving LLMs' Empathy, Listening, and Comfort Abilities through Fine-tuning with Multi-turn Empathy Conversations](https://aclanthology.org/2023.findings-emnlp.83/). `2023`
- [Personalizing Dialogue Agents: I have a dog, do you have pets too?](https://arxiv.org/abs/1801.07243). `2018`
- [Call for Customized Conversation: Customized Conversation Grounding Persona and Knowledge](https://arxiv.org/abs/2112.08619). `2022`
- [Beyond Goldfish Memory: Long-Term Open-Domain Conversation](https://arxiv.org/abs/2107.07567). `2021`
- [Mem0: Building Production-Ready AI Agents with Scalable Long-Term Memory](https://arxiv.org/abs/2504.19413). `2025`

### Hybrid Simulation

Hybrid approaches combine multiple simulation targets for richer, more realistic agent behavior.

---

## What: Interaction Settings

### Human-AI Simulation

Models turn-based interactions where users prompt and AI systems respond.

- [Human-ai interaction in lan- guage acquisition: Evaluating llm as a language part- ner](https://arxiv.org/abs/2402.10453). `2025`

### Human-Human Simulation

Models natural dialogues between two human participants.

- [Validating Synthetic Usage Data in Living Lab Environments](https://dl.acm.org/doi/10.1145/3539598.3541381). `2024`
- [A Dynamic Bayesian Network Click Model for Web Search Ranking](https://dl.acm.org/doi/10.1145/1498759.1498818). `2009`
- [LiveChat: A Large-Scale Personalized Dialogue Dataset Automatically Constructed from Live Streaming](https://aclanthology.org/2023.acl-long.858/). `2023`
- [PlatoLM: Teaching LLMs in Multi-Round Dialogue via a User Simulator](https://arxiv.org/abs/2404.02427). `2024`
- [PersonaChat: A Conversational Dialogue Dataset](https://arxiv.org/abs/1801.07243). `2018`
- [Wizard of Wikipedia: Knowledge-Powered Conversational Agents](https://openreview.net/forum?id=r1l73iRqKm). `2019`
- [EmpatheticDialogues: An Emotional Conversation Dataset](https://arxiv.org/abs/1811.00207). `2019`
- [MultiWOZ: A Large-Scale Multi-Domain Wizard-of-Oz Dataset](https://arxiv.org/abs/1810.00278). `2018`

### AI-AI Simulation

Models conversations where both participants are autonomous AI agents, enabling self-play and debate.

- [Improving Factuality and Reasoning in Language Models through Multiagent Debate](https://arxiv.org/abs/2305.14325). `2024`
- [A survey on llm-as-a-judge](https://arxiv.org/abs/2411.15594). `2024`
- [Beyond static responses: Multi-agent LLM systems as a new paradigm for social science research](https://arxiv.org/abs/2506.01839). `2025`
- [Generative Agents: Interactive Simulacra of Human Behavior](https://arxiv.org/abs/2304.03442). `2023`
- [Improving Factuality and Reasoning via Multi-Agent Debate](https://arxiv.org/abs/2305.14325). `2023`

### Many-Human-AI Simulation

Models group dynamics with multiple humans interacting with AI systems.

---

## How: Techniques

### Prompting

Prompt-based methods use zero-shot, few-shot, and chain-of-thought prompting to condition LLM behavior.

- [Let the LLMs Talk: Simulating Human-to-Human Conversational QA via Zero-Shot LLM-to-LLM Interactions](https://dl.acm.org/doi/10.1145/3616855.3635853). `2024`
- [Chain-of-Thought Prompting Elicits Reasoning in Large Language Models](https://arxiv.org/abs/2201.11903). `2022`
- [In-Context Learning User Simulators for Task-Oriented Dialog Systems](https://arxiv.org/abs/2306.00774). `2023`

### RAG & Retrieval

Retrieval-augmented generation (RAG) grounds user simulation in external knowledge and memory.

- [User Simulation for Evaluating Information Access Systems](https://dl.acm.org/doi/10.1145/3624918.3629548). `2023`
- [User simulation in the era of generative AI: user model- ing, synthetic data generation, and system evaluation](https://arxiv.org/abs/2501.04410). `2025`
- [Kaucus: Knowledgeable User Simulators for Training Large Language Models](https://aclanthology.org/2024.scichat-1.8/). `2024`
- [Preference-Based Learning with Retrieval Augmented Generation for Conversational Question Answering](https://arxiv.org/abs/2501.01881). `2025`
- [Retrieval-augmented simulacra: Gen- erative agents for up-to-date and knowledge-adaptive simulations](https://arxiv.org/abs/2503.14620). `2025`

### Fine-tuning

Supervised and parameter-efficient fine-tuning adapt LLMs to user simulation tasks.

- [Build- ing math agents with multi-turn iterative preference learning](https://arxiv.org/abs/2405.13001). `2025`
- [Self-Instruct: Aligning Language Models with Self-Generated Instructions](https://arxiv.org/abs/2212.10560). `2022`
- [WizardLM: Empowering Large Language Models to Follow Complex Instructions](https://arxiv.org/abs/2304.12244). `2023`

### RL/DPO

Reinforcement learning and direct preference optimization enable multi-turn strategy learning.

- [Personalized Steering of Large Language Models: Versatile Steering Vectors through Bi-Directional Preference Optimization](https://arxiv.org/abs/2410.17582). `2024`
- [SDPO: segment- level direct preference optimization for social agents](https://arxiv.org/abs/2501.01821). `2025`
- [Design, Generation and Evaluation of a Synthetic Dialogue Dataset for Contextually Aware Chatbots in Art Museums](https://www.sciencedirect.com/science/article/pii/S0957417424026241). `2025`
- [Deep Reinforcement Learning from Human Preferences](https://arxiv.org/abs/1706.03741). `2017`
- [Direct Preference Optimization: Your Language Model is Secretly a Reward Model](https://arxiv.org/abs/2305.18290). `2023`

### Hybrid Approaches

Hybrid methods combine prompting, RAG, fine-tuning, and RL/DPO for more capable simulators.

---

## 🧪 Evaluation

### Traditional Metrics
- **BLEU/ROUGE**: Surface-level text similarity
- **Slot F1**: Task-oriented dialogue completion
- **Human evaluation**: Quality, consistency, safety

### LLM-as-Judge

- [BERT for joint intent classification and slot filling](https://arxiv.org/abs/1902.10909). `2019`
- [VideoAutoArena: An Automated Arena for Evaluating Large Multimodal Models in Video Analysis through User Simulation](https://arxiv.org/abs/2505.01808). `2025`
- [Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena](https://arxiv.org/abs/2306.05685). `2023`
- [LLM-as-Judge: A Comprehensive Survey](https://arxiv.org/abs/2410.02416). `2024`

---

## 📊 Datasets

Key conversational datasets used for training and evaluating user simulators:

- [Taskmaster-1: Toward a Realistic and Diverse Dialog Dataset](https://arxiv.org/abs/1909.05358). `2019`
- [PersonaChat](https://arxiv.org/abs/1801.07243). `2018`
- [Wizard-of-Wikipedia](https://openreview.net/forum?id=r1l73iRqKm). `2019`
- [EmpatheticDialogues](https://arxiv.org/abs/1811.00207). `2019`
- [MultiWOZ: A Large-Scale Multi-Domain Wizard-of-Oz Dataset for Task-Oriented Dialogue](https://arxiv.org/abs/1810.00278). `2018`
- [Taskmaster](https://arxiv.org/abs/1909.05358). `2019`
- [ABCD: Action-Based Conversations Dataset](https://aclanthology.org/2021.naacl-main.239/). `2021`

---

## 🚀 Applications

- [Counterfactual Reasoning and Learning Systems: The Example of Computational Advertising](https://jmlr.org/papers/v14/bottou13a.html). `2013`
- [An Experimental Comparison of Click Position-Bias Models](https://dl.acm.org/doi/10.1145/1341531.1341545). `2008`

- **Data Augmentation**: Privacy-conscious synthetic dialogue generation
- **Conversational Recommendation & Search**: Simulating user queries and preferences
- **Education & Tutoring**: Adaptive learning systems and student simulation
- **HCI Prototyping**: Testing interfaces and interaction designs
- **Evaluation Arenas**: Benchmarking via debate, Elo ratings, automated assessment

---

## ❗ Open Problems

- **Long-horizon consistency**: Maintaining persona and memory across extended conversations
- **Diversity & strategy**: Moving beyond polite, homogeneous behavior to controllable variation
- **Bias & safety**: Demographic sensitivity, toxicity mitigation, robust safety protocols
- **Evaluation**: Better metrics for realism, consistency, and human alignment

---

## 📚 Cite Us

```bibtex
@misc{ni2025conversational_user_simulation_survey,
  title        = {Large Language Models for Conversational User Simulation: A Comprehensive Survey},
  author       = {Ni, Bo and Wang, Leyao and Wang, Yu and Kveton, Branislav and Dernoncourt, Franck and Xia, Yu and Chen, Hongjie and Leura, Reuben and Basu, Samyadeep and Mukherjee, Subhojyoti and Mathur, Puneet and Ahmed, Nesreen and Wu, Junda and Li, Li and Zhang, Huixin and Zhang, Ruiyi and Yu, Tong and Kim, Sungchul and Gu, Jiuxiang and Tu, Zhengzhong and Siu, Alexa and Wang, Zichao and Yoon, David Seunghyun and Lipka, Nedim and Park, Namyong and Lin, Zihao and Bui, Trung and Zhao, Yue and Derr, Tyler and Rossi, Ryan A.},
  year         = {2025},
  note         = {Survey preprint},
  howpublished = {\url{https://hal.science/hal-05217179}}
}
```

---

## 🤝 Contributing

Contributions are very welcome! Please:
1. Fork the repository
2. Add your paper to the appropriate section with proper formatting
3. Submit a pull request

**Format**: `- [Paper Title](URL). Authors. *Venue*. 'YEAR'`

---

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=Arstanley/Awesome-LLM-Conversation-Simulation&type=Date)](https://star-history.com/#Arstanley/Awesome-LLM-Conversation-Simulation&Date)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
