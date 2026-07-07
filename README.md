<h1 align="center">Geonsik "GS" Moon</h1>

<p align="center"><code>AI Platform Developer @ IBM Research</code> · <code>ML Systems × Compilers</code> · <code>AI Inference Optimization</code></p>

<p align="center">
   <a href="https://linkedin.com/in/gsmoon97" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="gsmoon97" height="30" width="40" /></a>
   <a href="https://gsmoon97.github.io" target="blank"><img align="center" src="https://cdn.jsdelivr.net/gh/jdecked/twemoji@15.1.0/assets/svg/1f310.svg" alt="website" height="30" width="30" /></a>
   <a href="https://scholar.google.com/citations?user=si3AXV8AAAAJ" target="blank"><img align="center" src="https://upload.wikimedia.org/wikipedia/commons/c/c7/Google_Scholar_logo.svg" alt="google-scholar" height="30" width="40" /></a>
   <a href="https://orcid.org/0009-0001-5646-466X" target="blank"><img align="center" src="https://upload.wikimedia.org/wikipedia/commons/0/06/ORCID_iD.svg" alt="orcid" height="30" width="40" /></a>
   &nbsp;<img src="https://komarev.com/ghpvc/?username=gsmoon97&style=flat-square&color=1d4ed8" alt="profile-views" />
</p>

```console
$ ssh gsmoon97@portfolio-os
Welcome to PORTFOLIO_OS (GNU/Linux 6.1.0 aarch64)

 [ OK ]  Mounted /dev/brain
 [ OK ]  Started service: AI Platform Developer @ IBM Research
 [ OK ]  Loaded backend: torch-spyre  (target: Spyre AIU accelerator)
 [ OK ]  Reached target: AI Inference Optimization
 [WARN]  impostor_syndrome.service masked — will not start
 System ready. 1 recruiter session waiting on /dev/hire ...

$ whoami
> "Geonsik" / "Gun-Shik" / "/kʌn.ɕik/" — call me "GS" 🙋🏻‍♂️
```

## `> source ./about_me`

I'm an **AI Platform Developer** building the systems layer that makes large models run **fast on real hardware**. My work sits where **ML compilers, model serving, and inference optimization** meet: I extend PyTorch's `torch.compile` stack, trace performance down to individual kernels, and turn that visibility into speed.

Right now I'm at **IBM Research** on **[torch-spyre](https://github.com/torch-spyre/torch-spyre)** — IBM's PyTorch backend for the **Spyre AI inference accelerator** — building compiler-level provenance so kernel hotspots can be attributed back to the exact source line that produced them.

That systems focus is grounded in a research background: **5 peer-reviewed papers** (ICLR / ACL / AACL / EACL) and hands-on **LLM training, evaluation, and NLP** at ByteDance, Apple, and NUS. I like problems where a paper-grade idea has to survive contact with a production pipeline.

## `> cat ./focus.md`

### 🛠️ ML Systems & Compilers
- **PyTorch compilation stack** — `torch.compile` internals: TorchDynamo, AOTAutograd, and Inductor lowering to custom hardware backends
- **Kernel-level performance** — source-to-kernel provenance, profiling, hotspot attribution, quantization, FlashAttention
- **Hardware backends** — lowering ATen ops → optimized kernels for the Spyre AIU inference accelerator

### ⚡ LLM Infrastructure & Inference
- **Serving & runtimes** — vLLM, llama.cpp, Ollama; backend integration for accelerated inference
- **Efficient adaptation** — LoRA / QLoRA / PEFT, 4-bit quantization for parameter-efficient fine-tuning
- **RAG & orchestration** — LangChain / LangGraph pipelines, vector search over Chroma / Pinecone

### 🧪 LLM Training, Evaluation & NLP
- **Training-data & RL pipelines** — end-to-end data ops for code-generation and agentic RL benchmarks
- **Agent evaluation** — failure-mode analysis and eval feedback loops for SWE agents; LM Eval Harness, W&B
- **NLP research** — timeline summarization, lexical semantics, grammatical error correction (ACL / EACL / AACL)

## `> ls ./featured_projects`

### `01`  torch-spyre — PyTorch backend for the Spyre AI accelerator  &nbsp;[[`Repo`](https://github.com/torch-spyre/torch-spyre) | [`Epic #2573`](https://github.com/torch-spyre/torch-spyre/issues/2573)]
- Contributing to **IBM's open-source ML compiler stack** that lowers `torch.compile` graphs to optimized kernels for the **Spyre AIU inference accelerator**.
- Built **source-to-kernel provenance**: a Phase-1 audit ([`PR #2720`](https://github.com/torch-spyre/torch-spyre/pull/2720), *merged*) that pinpointed where source attribution was dropped in the Inductor → `OpSpec` → SuperDSC path, then a `debug_handle` schema ([`PR #2945`](https://github.com/torch-spyre/torch-spyre/pull/2945), *in review*) threading each kernel back to its **PyTorch source line + ATen op** — the foundation for source-level inference-perf tuning.
- **Tech Stack**: `PyTorch` `torch.compile` `Inductor` `AOTAutograd` `ATen` `Spyre AIU`

### `02`  Granite Speech → Foundation Model Stack (FMS)  &nbsp;[[`PR`](https://github.com/foundation-model-stack/foundation-model-stack/pull/499) | [`Project Log`](https://github.com/columbia-hpml-granite)]
- Integrated the **Granite Speech 3.3** model into IBM's **[Foundation Model Stack](https://github.com/foundation-model-stack/foundation-model-stack)** — Conformer encoder, Q-Former projector, LoRA-adapted decoder — with `torch.compile` optimization. Opened a PR to the upstream repo.
- **Tech Stack**: `PyTorch` `FMS` `Granite-Speech-3.3` `LoRA` `torch.compile`

### `03`  AetherCode — Can LLMs win premier programming competitions? (ICLR 2026)  &nbsp;[[`Dataset`](https://huggingface.co/datasets/m-a-p/AetherCode) | [`Paper`](https://openreview.net/pdf?id=lSM6MtjQcM)]
- Co-authored an **open-source competitive-programming benchmark** (released on Hugging Face) evaluating whether frontier LLMs can win IOI/ICPC-tier contests. Orchestrated data pipelines across 17K+ samples and 70+ annotators.
- **Tech Stack**: `LLM Evaluation` `RL Benchmarks` `Hugging Face` `Multi-Agent Codegen`

### `04`  Incremental Timeline Summarization with LLMs (ACL 2024, Main)  &nbsp;[[`Code`](https://github.com/gsmoon97/LLM-TLS) | [`Paper`](https://aclanthology.org/2024.acl-long.390/)]
- LLM-driven **incremental event clustering** and timeline construction from text streams; outperformed SOTA on 4 TLS benchmarks.
- **Tech Stack**: `PyTorch` `vLLM` `Llama-2-13B` `LangChain` `ChromaDB`

### `05`  Encoder-only vs. Decoder-only for Word Meaning (ACL 2024, Findings)  &nbsp;[[`Code`](https://github.com/gsmoon97/llm-semantic-understanding) | [`Paper`](https://aclanthology.org/2024.findings-acl.967/)]
- Framework showing encoder-only models outperform decoder-only LLMs on **lexical semantic** tasks (WSD, WiC).
- **Tech Stack**: `PyTorch` `Transformers` `LoRA` `PEFT` `W&B`

## `ls ./side_projects`

### Email Prime — AI-powered email classification & summarization  &nbsp;[[`Code`](https://github.com/Amazon-Bedrock-Innovation-Challenge/email-prime) | [`Demo`](https://github.com/user-attachments/assets/d190f941-0af7-40c7-887a-2807640d5a83)]
- End-to-end Gmail pipeline: topic classification via **AWS Bedrock** LLMs, RAG-enriched semantic search, and AI-generated thread summaries, with a Streamlit UI and structured outputs (`instructor` + Pydantic).
- **Tech Stack**: `AWS Bedrock` `Streamlit` `instructor` `Pydantic` `Gmail API` `FAISS` `Titan Embeddings` `LangChain`

### LLM Agent Evaluation  &nbsp;[[`Code`](https://github.com/gsmoon97/swe-agent-eval)]
- Research toolkit for **analyzing LLM-agent trajectories** on software-engineering tasks — surfacing failure modes across thousands of runs.
- **Tech Stack**: `Python` `Jupyter` `Agent Frameworks`

## `> cat ./skills.md`

**Programming Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-025E8C?style=flat-square&logo=postgresql&logoColor=white)

**ML Frameworks**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)

**ML Systems & Performance**

![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)
![torch.compile](https://img.shields.io/badge/torch.compile-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TorchDynamo](https://img.shields.io/badge/TorchDynamo-1D4ED8?style=flat-square)
![AOTAutograd](https://img.shields.io/badge/AOTAutograd-1D4ED8?style=flat-square)
![Inductor](https://img.shields.io/badge/Inductor-1D4ED8?style=flat-square)
![Profiling](https://img.shields.io/badge/Profiling-1D4ED8?style=flat-square)
![Quantization](https://img.shields.io/badge/Quantization-1D4ED8?style=flat-square)
![FlashAttention](https://img.shields.io/badge/FlashAttention-1D4ED8?style=flat-square)

**LLM Training & Evaluation**

![LoRA / PEFT](https://img.shields.io/badge/LoRA%20%2F%20PEFT-6D28D9?style=flat-square)
![QLoRA](https://img.shields.io/badge/QLoRA-6D28D9?style=flat-square)
![LM Eval Harness](https://img.shields.io/badge/LM%20Eval%20Harness-6D28D9?style=flat-square)
![Weights & Biases](https://img.shields.io/badge/Weights%20&%20Biases-FFBE00?style=flat-square&logo=weightsandbiases&logoColor=black)

**LLM Infrastructure**

![vLLM](https://img.shields.io/badge/vLLM-30A2FF?style=flat-square)
![llama.cpp](https://img.shields.io/badge/llama.cpp-1C1C1C?style=flat-square)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square)
![Chroma](https://img.shields.io/badge/Chroma-FEC925?style=flat-square)
![Pinecone](https://img.shields.io/badge/Pinecone-1C1C1C?style=flat-square&logo=pinecone&logoColor=white)

**Systems & DevOps**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

## `> head -5 ./publications.md`

1. **AetherCode: Evaluating LLMs' Ability to Win in Premier Programming Competitions**  
   ICLR 2026 · [[`Dataset`](https://huggingface.co/datasets/m-a-p/AetherCode) | [`Paper`](https://openreview.net/pdf?id=lSM6MtjQcM)]

2. **From Moments to Milestones: Incremental Timeline Summarization Leveraging Large Language Models**  
   ACL 2024 (Main Conference) · [[`Code`](https://github.com/gsmoon97/LLM-TLS) | [`Paper`](https://aclanthology.org/2024.acl-long.390/)]

3. **Are Decoder-Only Language Models Better than Encoder-Only Language Models in Understanding Word Meaning?**  
   ACL 2024 (Findings) · [[`Code`](https://github.com/gsmoon97/llm-semantic-understanding) | [`Paper`](https://aclanthology.org/2024.findings-acl.967/)]

4. **WAMP: Writing, Annotation, and Marking Platform**  
   IJCNLP-AACL 2023 (System Demonstrations) · [[`Code`](https://github.com/nusnlp/WAMP) | [`Paper`](https://aclanthology.org/2023.ijcnlp-demo.8.pdf)]

5. **ALLECS: A Lightweight Language Error Correction System**  
   EACL 2023 (System Demonstrations) · [[`Code`](https://github.com/nusnlp/ALLECS) | [`Paper`](https://aclanthology.org/2023.eacl-demo.32/)]

## `> contact --help`

```console
$ cat /etc/gsmoon97/contact.conf
  location   = New York, NY
  website    = https://gsmoon97.github.io
  linkedin   = https://linkedin.com/in/gsmoon97
  scholar    = https://scholar.google.com/citations?user=si3AXV8AAAAJ
  orcid      = https://orcid.org/0009-0001-5646-466X
  status     = open to full-time roles (starting Jan 2027)

$ echo "Ping me before my RAM gets overwritten."
```
