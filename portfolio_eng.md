## **장석희 (Seokhee Chang)**  
## **Portfolio**

### **CONTACT**
- **Email**: <cycloevan97@gmail.com>  
- **GitHub**: <https://github.com/seok-hee97>  
- **LinkedIn**: <https://www.linkedin.com/in/seokhee-chang97/>  
- **Hugging Face**: <https://huggingface.co/cycloevan>

### **Core Skills**:  
- **Languages**: Python, C, C++, SQL (MySQL, PostgreSQL, MongoDB), Bash  
- **Libraries & Frameworks**: PyQt, Scikit-Learn, PyTorch, TensorFlow, Pandas, NumPy, Django, Flask, PySpark, Transformers  
- **Tools & Platforms**: Docker, AWS (S3, EC2, API Gateway, Lambda, SageMaker, CloudFormation), Git
***

## **PROJECTS**

***

### **Ransomware Similarity Research**
> Solo Project (INCA Internet) | Oct 2025, Nov 2025, Jan 2026

- Designed and implemented a ransomware family classification system utilizing BERT-based assembly code semantic analysis.
- **Core Technology Pipeline**: PE file → Function-level disassembly → Assembly normalization → Custom WordPiece tokenizer training → BERT fine-tuning → PE-level aggregation.
- Achieved **92% F1-Score** at the function level and **88% accuracy** at the file level (detected major families including WannaCry, Petya, and LockBit).
- Applied assembly instruction normalization strategy: Normalized addresses, constants, and strings to `[addr]`, `[const]`, and `[str]` tokens to enhance the model's behavioral pattern learning.
- Implemented **Weighted Cross-Entropy Loss** to resolve class imbalance issues and improve detection performance for minority families.
- **Skills**: Python, PyTorch, Transformers, BERT, Angr, Capstone

***

### **AI Agent-Based Code Vulnerability Detection System**
> Team Project (5 members, Team LlamaGuard / Meta Llama Academy 1st) | Oct 2, 2025 | **Excellence Award (Korea Radio Promotion Association)**

- Led project planning, designed multi-agent LLM architecture, and developed the on-device LLM model.
- **System Architecture**: On-device Model (Severity Detection) → RAG-based vectorized CVE database similarity search → Solar Pro2 (Patch generation for CVSS ≥ 7.0) → Automated report generation.
- Fine-tuned **Llama-3.2-1B model** using **QLoRA** and optimized performance with **Llama.cpp** build for on-device deployment.
- Trained on a public dataset (11 programming languages / 5,000 samples) and validated on a test set (500 samples) with 100-sample random sampling.
  - Performance Improvement: **ROUGE-L F1: 0.0933 → 0.1335 (+43.1%)** / **BLEU: 0.0061 → 0.0219 (+259%)**.
- **Skills**: Python, PyTorch, Transformers, LangChain, FAISS, Llama, QLoRA
- **Links**: [Meta Blog](https://about.fb.com/ko/news/2025/10/meta-llm-agent-on-device-ai-workshop/) | [ETNews Article](https://www.etnews.com/20251002000253) | [Video](https://youtu.be/QmFy0eGHI7Q?si=HxqFZaDuiXVPCGQU)

***

### **Malware Detection Model Development & Performance Improvement**
> Solo Project (INCA Internet) | Dec 2024 - Mar 2025

- Conducted seminars on DNN-based malware detection papers and designed/implemented detection models.
- Improved .NET and PE parsing logic based on EMBER feature extraction methodology and developed a custom feature extraction pipeline.
  - Resolved feature deficiency in .NET files (10% of data had >50% feature loss) by parsing ImplMap/TypeRef tables to supplement Import Function features (**2%p performance improvement**).
- Built a training dataset by collecting and preprocessing approximately **3.5–4 million** internal malware/benign samples.
- Improved model reliability by applying calibration techniques such as **Focal Loss** and **Isotonic Calibration**.
- **Skills**: Python, TensorFlow, DNN, Feature Engineering, Calibration (Focal Loss, Isotonic)

***

### **Google ML Bootcamp**
> Solo Project (Google ML Bootcamp 5th) | July 2024 - Oct 2024

- Completed Coursera Deep Learning Specialization and participated in study groups.
- **Kaggle Competition**: *Binary Prediction of Poisonous Mushrooms* – Achieved **Top 5%**.
  - **MCC Score: 0.98502** (Rank: 76/2,422, **Top 3.1%**) | Utilized feature engineering, XGBoost, and LightGBM.
- **Gemma Sprint Project**: Developed a GDPR compliance Q&A assistant.
  - Fine-tuned **Gemma-2-2B model** using **Direct Preference Optimization (DPO)** methodology.
- **Skills**: PyTorch, TensorFlow, Transformers, XGBoost, LightGBM, ML
- **Link**: [gdpr-gemma model](https://huggingface.co/cycloevan/gdpr_gemma-2-2b)

***

### **ML-WAF (+ KISA-AI-Challenge)**
> Team Project (4 members, Team Pyree / S-Developer 1st) | July 2023 - Nov 2023

- Developed a high-performance **ML-WAF** leveraging Nginx's event-driven/async I/O architecture integrated with ML REST API and MySQL.
- Led ML model development (LSTM / TF-IDF + SVM / CNN-based models) and AWS deployment.
- Collected and preprocessed network data to extract features and developed a real-time attack type classification model (multi-class).
- Deployed containerized ML-WAF components (Nginx Proxy server, WAS / WAF) using Docker on AWS environment (EC2, SageMaker, S3, CloudFormation).
- **KISA Cybersecurity AI/Big Data Challenge**: Applied the same model to Track A (Web Firewall Log Analysis / Attack Type Classification).
  - Achieved **Accuracy: 90.868** / **Rank: 17/70 (Top 25%)**.
- **Skills**: Python, Lua, Django, Flask, Nginx, AWS (EC2, SageMaker, S3, CloudFormation), MySQL, SQLite, Docker
- **Links**: [ML-WAF](https://github.com/Team-Pyree/mlwaf) | [KISA-AI-Challenge 2023](https://github.com/seok-hee97/kisa-ai-2023)

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
- **Malware Detection Application**: Reduced feature count by **92% (69 → 6)** while improving classification accuracy by **3%p**.
- Led seminars on Topology mathematics and developed algorithms based on mathematical concepts (Metric Space, Open Ball, Continuity).
- **Skills**: Python, Mathematics (Topology), Feature Engineering, Scikit-learn

***

### **Gray Sample Automated Collection System (Auto-Installation & Query System)**
> Solo Project (INCA Internet) | Oct 2024, May 2025 - June 2025

- Designed and implemented an automated installer execution and PE file collection system to build a gray sample (white-list/training data) dataset.
- **Auto-Installation System**: Implemented automated installation pipelines for **16 installer types** (Inno Setup, NSIS, MSI, etc.).
  - Applied a 3-step strategy (7-Zip extraction → Silent Mode execution → PyWinAuto GUI automation) achieving an **87% automatic collection rate** (516 out of 587 samples).
- Implemented installation process tracking based on file system real-time monitoring (**Watchdog**) and automated classification/verification logic for generated PE files.
- **Sample Query System**: Built a Django-based web dashboard to manage collected sample metadata (MD5, registration date, file path) and implemented upload/download functions; scheduled batch jobs using **APScheduler**.
- **Skills**: Python, Django, PyWinAuto, Watchdog, APScheduler, MySQL