# **Seokhee Chang (장석희)**

- Email: cycloevan97@gmail.com | GitHub: [seok-hee97](https://github.com/seok-hee97)

## **Core Skills**
- **Languages**: Python, C/C++, SQL, Bash
- **ML / Deep Learning**: PyTorch, TensorFlow, Scikit-Learn, PySpark
- **LLM / NLP**: HuggingFace Transformers, BERT, PEFT, LangChain/LangGraph, RAG
- **Security / RE**: PE·Malware Analysis, Ghidra, IDA, Angr, Capstone, YARA
- **Web / Serving**: FastAPI, Flask, Django, Streamlit
- **Cloud / DevOps**: AWS (EC2/S3/Lambda/SageMaker), Docker, Git, Elasticsearch

## **PROJECTS**

***

### **BERT-Based Ransomware Analysis & Classification System**
> Solo Project (INCA Internet) | Nov 2025 - Jan 2026

- Contributed to the AI analysis model track of an R&D project, `sLLM-based ransomware analysis technology and real-time blocking/backup solution development`.
- Designed and implemented an assembly-code semantic analysis system for ransomware analysis service and real-time blocking/backup solution R&D.
- **Core Technology Pipeline**: PE file → Function-level disassembly → Assembly normalization → Custom WordPiece tokenizer training → BERT fine-tuning → PE-level aggregation.
- Achieved **91.64% Accuracy / 0.95 F1-Score** on binary classification (ransomware vs benign) and **0.93 F1-Score** on recoverability binary classification, including major ransomware families such as WannaCry, Petya, and LockBit.
- Applied assembly instruction normalization strategy: Normalized addresses, constants, and strings to `[addr]`, `[const]`, and `[str]` tokens to enhance the model's behavioral pattern learning.
- Training strategy: **Weighted Cross-Entropy Loss** for ransomware-vs-benign classification (class imbalance), and a **SupCon (contrastive) + BCE dual loss** for recoverability classification.
- **Skills**: Python, PyTorch, Transformers, BERT, Angr, Capstone, Ghidra

***

### **AI Agent-Based Code Vulnerability Detection System**
> Team Project (5 members, Team LlamaGuard / Meta Llama Academy 1st) | Sep 30 - Oct 2, 2025 | **Excellence Award (Korea Radio Promotion Association)**

- Led project planning, designed multi-agent LLM architecture, and developed the on-device LLM model.
- **System Architecture**: On-device Model (Severity Detection) → RAG-based vectorized CVE database similarity search → Solar Pro2 (Patch generation for CVSS ≥ 7.0) → Automated report generation.
- Fine-tuned **Llama-3.2-1B model** using **QLoRA**, then compressed it via **GGUF conversion + Llama.cpp build**, enabling real-time inference in an on-device environment.
- Trained on a public dataset (11 programming languages / 5,000 samples) and validated on a test set (500 samples) with 100-sample random sampling.
  - Performance Improvement: **ROUGE-L F1: 0.0933 → 0.1335 (+43.1%)** / **BLEU: 0.0061 → 0.0219 (+259%)**.
- **Skills**: Python, PyTorch, Transformers, **LangGraph**, LangChain, FAISS, sentence-transformers, Llama, **QLoRA, GGUF, Llama.cpp**
- **Links**: [Code](https://github.com/MLA-LlamaGuard/llama-guard) | [Meta Blog](https://about.fb.com/ko/news/2025/10/meta-llm-agent-on-device-ai-workshop/) | [ETNews Article](https://www.etnews.com/20251002000253) | [Video](https://youtu.be/QmFy0eGHI7Q?si=HxqFZaDuiXVPCGQU)

***

### **TTSC In-house Malware Detection System Operation & EMBER Model Improvement**
> Solo Project (INCA Internet) | Dec 2024 - Mar 2025

- Operated and improved the TTSC in-house malware detection system, designing and implementing EMBER-based malware detection models.
- Conducted seminars on EMBER-based malware detection papers and established PE feature-based modeling strategy.
- Improved .NET and PE parsing logic based on EMBER feature extraction methodology and developed a custom feature extraction pipeline.
  - Resolved feature deficiency in .NET files (10% of data had >50% feature loss) by parsing ImplMap/TypeRef tables to supplement Import Function features (**2%p performance improvement**).
- Extracted and processed PE features from benign and ransomware samples, then trained and evaluated DNN-based ransomware detection models.
- Built a training dataset by collecting and preprocessing approximately **3.5–4 million** internal malware/benign samples.
- Improved model reliability by applying calibration techniques such as **Focal Loss** and **Isotonic Calibration**.
- **Skills**: Python, TensorFlow, DNN, TabNet, LightGBM, ONNX, Feature Engineering, Calibration (Focal Loss, Isotonic)

***

### **GDPR Compliance Q&A Assistant (Gemma-2-2B DPO Fine-tuning)**
> Solo Project (Google ML Bootcamp 5th / Gemma Sprint Project) | July 2024 - Oct 2024

- Designed and implemented a GDPR Q&A-specialized Gemma-2-2B fine-tuning pipeline (SFT → Rejection Sampling → DPO).
- Designed a dual evaluation framework: quantitative (n=100) + GPT-4o Judge qualitative (n=50).
- **Results**: SFT delivered the largest improvement over the base model (ROUGE-L **+12%**, BLEU **+37%**, BertScore F1 **+1.3%**); DPO maintained SFT-level performance.
- **Skills**: Python, PyTorch, Transformers, QLoRA, DPO, Streamlit, Docker
- **Links**: [HuggingFace Model](https://huggingface.co/cycloevan/gdpr_gemma-2-2b)

***

### **ML-WAF (+ KISA-AI-Challenge)**
> Team Project (4 members, Team Pyree / S-Developer 1st) | July 2023 - Nov 2023 | **KR Patent No. 10-2996906**

- Developed a high-performance **ML-WAF** leveraging Nginx's event-driven/async I/O architecture integrated with ML REST API and MySQL.
- Led ML model development (LSTM / TF-IDF + SVM / CNN-based models) and AWS deployment.
- Collected and preprocessed network data to extract features and developed a real-time attack type classification model (multi-class).
- Deployed containerized ML-WAF components (Nginx Proxy server, WAS / WAF) using Docker on AWS environment (EC2, SageMaker, S3, CloudFormation).
- **KISA Cybersecurity AI/Big Data Challenge**: Applied the same model to Track A (Web Firewall Log Analysis / Attack Type Classification).
  - Achieved **Accuracy: 90.868** / **Rank: 17/70 (Top 25%)**.
- **Skills**: Python, Lua, TensorFlow, Scikit-learn, Django, Flask, Nginx, AWS (EC2, SageMaker, S3, CloudFormation), MySQL, SQLite, Docker
- **Links**: [ML-WAF](https://github.com/Team-Pyree/mlwaf) | [KISA-AI-Challenge 2023](https://github.com/seok-hee97/kisa-ai-2023) | [Patent 10-2996906](https://doi.org/10.8080/1020240023149)

***

### **Probe Anti-Virus Program**
> Team Project (2-3 members, Four-Chains) | Mar 2022 - Nov 2022

- Developed an anti-virus solution featuring ML-based malware detection and system optimization capabilities.
- Implemented three scan modes: Quick Scan (vulnerable areas), Deep Scan (user-selected areas), and Smart Scan (scan + optimization).
- Applied mathematical modeling algorithms (**ML-based similarity algorithms**) combined with logic-based detection algorithms for malware detection.
- Developed system optimization (cleanup of 34 file extensions), quarantine management (restore/remediate), and real-time protection features.
- **Skills**: Python, PyQt (GUI), SQL, Inno Setup, ML, Scikit-learn
- **Links**: [Wadiz](https://www.wadiz.kr/web/campaign/detail/153064) | [Docs](https://github.com/seok-hee97/resume/blob/main/docs/Probe-AV.pdf) | [Wiki](https://ko.wikipedia.org/wiki/%ED%94%84%EB%A1%9C%EB%B8%8C_%EB%B0%B1%EC%8B%A0)

***

### **Topology-Based Feature Selection Algorithm Research**
> Team Project (2 members, Four-Chains) | Aug 2022 - Mar 2023

- Designed and implemented a Feature Selection algorithm based on Metric Space theory.
  - Prior Research: 'Analysis method for Data similarity measure in Metric Space'.
- **Algorithm**: Map features to **Topological Space** → Generate **Open Balls** → Calculate weight for each Ball → Select central features.
- **Malware Detection Application**: Reduced feature count by **91% (69 → 6)** while improving classification accuracy by **3%p**.
- Led seminars on Topology mathematics and developed algorithms based on mathematical concepts (Metric Space, Open Ball, Continuity).
- **Skills**: Python, Mathematics (Topology), Feature Engineering, Scikit-learn
