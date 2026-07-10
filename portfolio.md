# **장석희 (Seokhee Chang)**

- Email: cycloevan97@gmail.com | GitHub: [seok-hee97](https://github.com/seok-hee97)

## **Core Skills**
- **Languages**: Python, C/C++, SQL, Bash
- **ML / Deep Learning**: PyTorch, TensorFlow, Scikit-Learn, PySpark
- **LLM / NLP**: HuggingFace Transformers, BERT, Fine-tuning (SFT/DPO/QLoRA), LangChain/LangGraph, RAG, FAISS
- **Security / RE**: PE·Malware Analysis, Ghidra, IDA, Angr, Capstone, YARA, CAPE Sandbox, EMBER
- **Web / Serving**: FastAPI, Flask, Django, Streamlit
- **Cloud / DevOps**: AWS (EC2/S3/Lambda/SageMaker), Docker, Git, Elasticsearch

## **PROJECTS**

***

### **BERT 기반 랜섬웨어 분석·분류 시스템**
> 1인 (INCA Internet) | 2025.11 - 2026.01
- R&D 과제 `sLLM 기반 랜섬웨어 분석 기술 및 실시간 차단/백업 솔루션 개발`의 AI 분석 모델 파트 수행
- 랜섬웨어 분석 서비스 및 실시간 차단/백업 솔루션을 목표로, 어셈블리 코드 의미 분석 기반 랜섬웨어 분류 시스템 설계 및 구현
- 핵심 기술 : PE 파일 → 함수 단위 디스어셈블리 → 어셈블리 정규화 → 커스텀 WordPiece 토크나이저 학습 → BERT 파인튜닝 → PE-Level 집계
- 이진분류 (랜섬웨어 vs 정상) 테스트 결과 Accuracy 91.64% / F1-Score 0.95 달성, 복호화 가능여부 이진분류 F1-Score 0.93 달성 (WannaCry, Petya, LockBit 등 주요 랜섬웨어 포함)
- 어셈블리 명령어 정규화 전략 적용: 주소/상수/문자열을 [addr], [const], [str]로 정규화하여 모델의 행위 패턴 학습 강화
- 학습 전략 이원화: 랜섬웨어 vs 정상 분류는 Weighted Cross-Entropy Loss(클래스 불균형·소수 클래스 탐지 개선), 복호화 가능여부 판별은 SupCon(대조학습) + BCE 듀얼 로스로 학습
- Skills: Python, PyTorch, Transformers, BERT, Angr, Capstone, Ghidra

***

### **AI Agent 기반 코드 취약점 탐지 시스템**
> 5인 (Team LlamaGuard / Meta Llama Academy 1기) | 2025.10.02 | **우수상 (한국전파진흥협회장상)**
- 프로젝트 기획 및 Multi-agent LLM 아키텍처 설계, On-device LLM 모델 개발 담당
- 시스템 구성 : On-device Model (취약점 종류 탐지 (Severity)) → RAG 기반 CVE database (vectorized) similarity search
   →  Solar Pro2 (CVSS≥7.0 시 패치 생성) → 자동 리포트 작성
- Llama-3.2-1B 모델을 fine-tuning (**QLoRA**) 후 **GGUF 변환 + Llama.cpp 빌드로 경량화**, On-device 환경에서 실시간 추론 구현.
- 공개 데이터셋 (개발언어 11개 / 데이터 5,000개)으로 학습 및 테스트셋(500개)에서 100개씩 랜덤샘플링해 모델 성능 검증.
  (ROUGE-L F1: 0.0933 → 0.1335, +43.1% / BLEU: 0.0061 → 0.0219, +259% 성능 개선)
- Skills : Python, PyTorch, Transformers, **LangGraph**, LangChain, FAISS, sentence-transformers, Llama, **QLoRA, GGUF, Llama.cpp**
- Links : [Meta Blog](https://about.fb.com/ko/news/2025/10/meta-llm-agent-on-device-ai-workshop/) | [ETNews Article](https://www.etnews.com/20251002000253) | [Video](https://youtu.be/QmFy0eGHI7Q?si=HxqFZaDuiXVPCGQU)

***

### **TTSC 사내 악성코드 탐지 시스템 운영 및 EMBER 모델 개선**
> 1인 (INCA Internet) | 2024.12 - 2025.03
- TTSC 사내 악성코드 탐지 시스템 운영 및 개선 업무를 수행하며, EMBER 기반 탐지 모델 설계·구현.
- 악성코드 탐지 관련 EMBER 기반 논문 리뷰 세미나 진행 및 PE feature 기반 모델링 전략 수립.
- EMBER 특징 추출 방식을 기반으로 .NET 및 PE 파싱 로직을 개선하고, 별도 파서 구현을 통해 특징 추출 파이프라인 개발.
  .NET 파일(데이터의 10%) 특징 절반 이상 결손 → ImplMap/TypeRef 테이블 파싱으로 Import Function 특징 보완 (성능 2%p 향상)
- 랜섬웨어 탐지 모델 개발을 위해 정상/랜섬웨어 PE feature를 추출·가공하고 DNN 기반 분류 모델 학습 및 성능 검증 수행.
- 사내 악성코드/정상 샘플 약 350–400만 건 수집·정제하여 학습 데이터셋을 구축, Focal Loss·Isotonic Calibration 등 보정 기법 적용해 신뢰도 개선.
- Skills: Python, TensorFlow, DNN, TabNet, LightGBM, Feature Engineering, Calibration(Focal Loss, Isotonic)

***

### **GDPR Compliance Q&A Assistant (Gemma-2-2B DPO 파인튜닝)**
> 1인 (Google ML Bootcamp 5기 / Gemma Sprint Project) | 2024.07 - 2024.10
- GDPR Q&A 특화 Gemma-2-2B 파인튜닝 파이프라인 설계·구현 (SFT → Rejection Sampling → DPO).
- 이중 평가 프레임워크 설계: 정량 n=100 + GPT-4o Judge 정성 n=50.
- 실험 결과: Base 대비 SFT에서 최고 성능 개선 (ROUGE-L **+12%**, BLEU **+37%**, BertScore F1 **+1.3%**). DPO도 SFT 수준 유지.
- Skills: Python, PyTorch, Transformers, QLoRA, DPO, Streamlit, Docker
- Links: [HuggingFace Model](https://huggingface.co/cycloevan/gdpr_gemma-2-2b)

***

### **ML-WAF (+ KISA-AI-Challenge)**
> 4인 (Team Pyree / S-Developer 1st) | 2023.07 - 2023.11
- Nginx event-driven / async I/O 구조를 활용해 ML REST API와 MySQL을 연동한 고성능 ML-WAF.
- ML 모델 개발 (LSTM / TF-IDF + SVM / CNN 기반 모델 개발 및 평가) 및 AWS 배포 담당.
- 네트워크 데이터를 수집·전처리해 특징 추출 및 ML 기반 실시간 공격 타입 분류 모델(다중 분류) 개발.
- AWS (EC2, SageMaker, S3, Cloudformation) 환경에 Docker 기반으로 서비스 운영 환경을
  컨테이너화한 ML-WAF 구성 요소(Nginx Proxy 서버, WAS / WAF) 배포.
- (KISA)사이버보안 AI/빅데이터 챌린지 A-트랙(웹 방화벽 로그 분석/ 공격유형 분류) 동일 모델 적용하여
  Accuracy : 90.868 / Rank : 17/70(top 25%) 성적 달성.
- Skills : Python, Lua, Django, Flask, Nginx, AWS (EC2, SageMaker, S3, CloudFormation), MySQL, SQLite, Docker
- Links : [ML-WAF](https://github.com/Team-Pyree/mlwaf) | [kisa-ai-challenge 2023](https://github.com/seok-hee97/kisa-ai-2023)

***

### **Probe Anti-Virus 프로그램**
> 2-3인 (Four-Chains) | 2022.03 - 2022.11
- ML 기반 악성코드 탐지 및 시스템 최적화 기능을 갖춘 안티바이러스 솔루션 개발.
- 빠른검사 (취약 영역 중점) / 정밀검사 (사용자 선택 영역) / 스마트 검사 (스캔 + 최적화) 검사 기능 개발.
  (악성코드 탐지) 수학적 모델링 알고리즘(ML 기반 유사도 알고리즘) + 로직 기반 탐지 알고리즘 적용.
- 시스템 최적화(34개 확장자 불필요 파일 (경로) 삭제), 격리소 관리(복원/치료), 실시간 보호 기능 구현 개발.
- Skills : Python, PyQt (GUI), SQL, Inno Setup, ML, Scikit-learn
- Links : [Wadiz](https://www.wadiz.kr/web/campaign/detail/153064) | [Docs](https://github.com/seok-hee97/resume/blob/main/docs/Probe-AV.pdf) | [Wiki](https://ko.wikipedia.org/wiki/%ED%94%84%EB%A1%9C%EB%B8%8C_%EB%B0%B1%EC%8B%A0)

***

### **위상수학 (Topology) 기반 Feature Selection 알고리즘 연구**
> 2인 (Four-Chains) | 2022.08 - 2023.03
- Metric Space 이론 기반 Feature Selection 알고리즘 설계 및 구현.
  선행연구 : 'Analysis method for Data similarity measure in Metric Space'
- 알고리즘: Feature를 위상공간(Topological Space)에 매핑하여 Open Ball 생성 → 각 Ball의 가중치 계산 → 중심 Feature 선택.
- (악성코드 탐지) 알고리즘 적용 시 Feature 수 69개 → 6개로 91% 감소, 분류 정확도 +3%p 향상.
- 위상수학 Topology 세미나 진행 및 수학적 개념(Metric Space, Open Ball, Continuity) 기반 알고리즘 개발.
- Skills : Python, Mathematics (Topology), Feature Engineering, Scikit-learn
