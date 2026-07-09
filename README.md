<div align="center">

# Léon Àmi Wagner

**AI Engineer — NLP & LLM Systems**

Vienna, Austria

[Website](https://www.leonamiwagner.com) · [LinkedIn](https://www.linkedin.com/in/leon-ami-wagner/) · [CV](https://www.leonamiwagner.com/cv.pdf) · [Email](mailto:leon.ami.wagner@gmail.com)

</div>

I build production LLM systems — retrieval, fine-tuning, evaluation, and fully on-premise deployment.

Currently AI Engineer on the AI-Taskforce at the **AIT Austrian Institute of Technology** (Vienna), where I built the enterprise RAG platform that was rated 8/10 by domain experts and selected for company-wide rollout. M.Sc. Computer Science (NLP) at Humboldt University of Berlin; my thesis introduces a continual-learning framework for LLMs. Previously Full-Stack Developer at Fraunhofer IPK (Berlin), where I built the first prototype of the EU Digital Battery Passport.

**Available for new roles from August 2026.**

---

## Selected work

### [Patch-and-Route (PnR)](https://github.com/Leon-AW/PnR-framework) — continual learning in LLMs without catastrophic forgetting

Master's thesis ([PDF](https://www.leonamiwagner.com/Leon-Wagner-master-thesis.pdf)), Humboldt University of Berlin. Discrete QLoRA "knowledge patches" over a frozen Mistral-7B with two-stage dynamic routing, so the model integrates new and conflicting knowledge without ever training the base weights.

- **86.4% edit success at ~0% forgetting** — Pareto-dominant among all evaluated baselines (monolithic LoRA, LoRA+RAG, X-LoRA, RECIPE) on SituatedQA, CounterFact, and an enterprise corpus
- ~7% inference-latency overhead vs. the frozen base (X-LoRA: ~60× slower); **O(K) update cost** vs. O(K²) for monolithic retraining

`PyTorch` · `PEFT / QLoRA` · `Hugging Face` · `MLflow`

### Enterprise RAG platform — AIT (closed source)

RAG chatbot over ~2,000 quality-management documents across four knowledge bases. Hybrid retrieval stack (dense + learned-sparse bge-m3 fused via RRF, HyDE, multi-query expansion, cross-encoder reranking), served as an OpenAI-compatible FastAPI service and deployed **fully on-premise** in three environments: Docker Swarm, HPC/SLURM with vLLM on NVIDIA MIG slices, and an ARM64 GH200 server.

- **4.61/5 overall (90.3% rated Good or better) on 2,000 real-world queries**, measured with a rubric-based LLM-as-a-judge framework I designed on 4,017 validated QA pairs — consistent across German and English
- Rated **8/10 by QM domain experts** in hands-on testing; selected for company-wide rollout

### [Small-model reasoning study](https://github.com/Leon-AW/Experimenting_Reasoning_on_SLMs) — can a 1B model beat a 3B?

Yes: a **LoRA-fine-tuned Llama 3.2 1B outperforms the stock 3B on GSM8K** using mixed-data fine-tuning and Plan-and-Solve prompting — a case for task-specific tuning over brute-force scaling. [Write-up](https://www.leonamiwagner.com/en/blog/slm-reasoning-study).

### [leonamiwagner.com](https://www.leonamiwagner.com) — portfolio with self-hosted AI infrastructure

Bilingual Next.js site whose centerpiece is a **self-hosted agentic graph-RAG assistant**: hybrid retrieval over a knowledge graph with a live retrieval-trace visualization, running on Ollama. Includes in-browser ML demos (MobileNetV2 classifier with CAM heat maps, TensorFlow.js sentiment analysis) — no inference backend required.

---

## Stack

**LLM & ML:** RAG, fine-tuning (LoRA/QLoRA/PEFT), continual learning, multi-agent systems, LLM evaluation, PyTorch, Hugging Face, vLLM, llama.cpp, MLflow
**Engineering:** Python, TypeScript, SQL, C++, FastAPI, Docker & Docker Swarm, HPC/SLURM, NVIDIA MIG, Linux, CI/CD, React/Next.js
