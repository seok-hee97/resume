## **장석희 (Seokhee Chang)**  
## **Portfolio**

***

### **CONTACT**
- **Email**: <cycloevan97@gmail.com>  
- **GitHub**: <https://github.com/seok-hee97>  
- **LinkedIn**: <https://www.linkedin.com/in/seokhee-chang97/>  
- **Hugging Face**: <https://huggingface.co/cycloevan>

### **Core Skills**:  
- **Languages**: Python, C, C++, SQL (MySQL, PostgreSQL, MongoDB), Bash  
- **Libraries & Frameworks**: PyQt, Scikit-Learn, PyTorch, TensorFlow, Pandas, NumPy, Django, Flask, PySpark  
- **Tools & Platforms**: Docker, AWS (S3, EC2, API Gateway, Lambda, SageMaker, CloudFormation), Git

## **PROJECTS**

***

### AI Agent 기반 코드 취약점 탐지 시스템
> 5인 (Team LlamaGurad / Meta Llama Academy 1th) | 2025.10.02 | **우수상 (한국전파진흥협회장상)**
- 프로젝트 기획 및 Multi-agent LLM 아키텍처 설계, On-device LLM 모델 개발 담당
- 시스템 구성 : On-device Model (취약점 종류 탐지(Severnity)) → RAG 기반 CVE database (vectorized) similarity search →  Solar Pro2 (CVSS≥7.0 시 패치 생성) → 자동 리포트 작성
- Llama-3.2-1B 모델을 fine-tuning (QLoRA)하여 코드 취약점 탐지 성능 개선. 
- 500개 validation dataset에서 100개씩 5회 반복 random sampling으로 모델 성능 검증 완료.
  > (ROUGE-L F1: 0.0933 → 0.1335, +43.1% / BLEU: 0.0061 → 0.0219, +259%)
- Skills : Python, ​PyTorch, Transformers, LangChain, FAISS​, Llama-3.2
- 링크 : [Meta Blog](https://about.fb.com/ko/news/2025/10/meta-llm-agent-on-device-ai-workshop/) | [ETNews Article](https://www.etnews.com/20251002000253) | 


***

### Google ML Bootcamp
> 1인 (Google ML Bootcamp 5th) | 기간: 2024.07 - 2024.10
- (Coursera) Deep Learning Specialization 교육 과정 수료 및 스터디 진행.
- (Kaggle Competition) Binary Prediction of Poisonous Mushrooms 상위 5% 달성.
-  MCC Score : 0.98502 (Rank :76/2,422, top 3.1% | Feature engineering과 XGBoost, LightGBM 등 활용)
- (Gemma Sprint Project) GDPR compliance Q&A assistant 개발.
  - Gemma-2-2B model을 Direct Preference Optimization (DPO) 방식으로 fine-tuning.
- Skill: PyTorch, TensorFlow, Transformers, XGBoost, LightGBM, ML
- 링크: [모델 링크](https://huggingface.co/cycloevan/gdpr_gemma-2-2b)

***

### ML-WAF (+ KISA-AI-Challenge)
> 4인 (Team Pyree / S-Developer 1th) | 기간 : 2023.07 - 2023.11
- Nginx event-driven / async I/O 구조를 활용해 ML REST API와 MySQL을 연동한 고성능 ML‑WAF.
- ML 모델 개발 (LSTM / TF-IDF + SVM / CNN 기반 모델 개발 및 평가) 및 AWS 배포 담당.
- 네트워크 데이터를 수집·전처리해 특징 추출 및 ML 기반 실시간 공격 타입 분류 모델(다중 분류) 개발.
- AWS (EC2, SageMaker, S3, Cloudformation) 환경에 Docker 기반으로 서비스 운영 환경을 컨테이너화한 ML‑WAF 구성 요소(Nginx Proxy 서버, WAS / WAF) 배포.  
- (KISA)사이버보안 AI/빅데이터 챌린지 A‑트랙(웹 방화벽 로그 분석/ 공격유형 분류) 동일 모델 적용하여 Accuracy : 90.868 / Rank : 17/70(top 25%) 성적 달성.  
- Skills : Python, Lua, Django, Flask, Nginx, AWS (EC2, SageMaker, S3, CloudFormation), MySQL, SQLite, Docker
- 링크 : [ML-WAF](https://github.com/Team-Pyree/mlwaf) | [사이보보안 AI 챌린지 2023](https://github.com/seok-hee97/kisa-ai-2023)

***

### Probe Anti-Virus 프로그램
> 2 - 3인 (Four-Chains) | 2022.03 - 2022.11
- ML 기반 악성코드 탐지 및 시스템 최적화 기능을 갖춘 안티바이러스 솔루션 개발.
- 빠른검사 (취약 영역 중점) / 정밀검사 (사용자 선택 영역) / 스마트 검사 (스캔 + 최적화) 검사 기능 개발.
  > (악성코드 탐지) 수학적 모델링 알고리즘(ML 기반 유사도 알고리즘) + 로직 기반 탐지 알고리즘 적용.
- 시스템 최적화(34개 확장자 불필요 파일 (경로) 삭제), 격리소 관리(복원/치료), 실시간 보호 기능 구현 개발. 
- Skills : Python, PyQt (GUI), SQL, Inoo Setup, ML
- 링크 : [Wadiz](https://www.wadiz.kr/web/campaign/detail/153064) | [문서](https://github.com/seok-hee97/resume/blob/main/docs/Probe-AV.pdf) | [Wiki](https://ko.wikipedia.org/wiki/%ED%94%84%EB%A1%9C%EB%B8%8C_%EB%B0%B1%EC%8B%A0)


