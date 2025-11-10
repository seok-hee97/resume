## **장석희 (SeokHee Chang)**  
## **Portfolio**

## **CONTACT**
- **Email**: <cycloevan97@gmail.com>  
- **GitHub**: <https://github.com/seok-hee97>  
- **LinkedIn**: <https://www.linkedin.com/in/seokhee-chang97/>  
- **Hugging Face**: <https://huggingface.co/cycloevan>

**Core Skills**:  
**Languages**: Python, C, C++, SQL (MySQL, PostgreSQL, MongoDB), Bash  
**Libraries & Frameworks**: PyQt, Scikit-Learn, PyTorch, TensorFlow, Pandas, NumPy, Django, Flask, PySpark  
**Tools & Platforms**: Docker, AWS (S3, EC2, API Gateway, Lambda, SageMaker, CloudFormation), Git

## **PROJECTS**

### **[KOR]**
### **AI 기반 코드 취약점 탐지 시스템**
**Meta Llama Academy 1기 | 수상: 우수상 (한국전파진흥협회장상)**

멀티 에이전트 LLM 아키텍처를 활용한 자동화된 코드 분석 시스템으로, 취약점 탐지, 심각도 평가 및 패치 생성 기능을 제공.

**프로젝트 개요**:  
- 소스 코드의 보안 취약점을 자동으로 탐지하고, CVE 데이터베이스 비교를 통해 심각도를 평가하며, 고위험 이슈에 대한 수정 패치를 생성하는 멀티 LLM 에이전트 시스템 설계 및 구현  
- RAG (Retrieval-Augmented Generation) 아키텍처를 배포하여 탐지된 취약점을 벡터화된 CVE 데이터베이스와 비교해 심각도 점수(CVSS 0.0-10.0 척도) 산출  
- LangChain 프레임워크를 통합하여 전체 워크플로우 조율: 취약점 탐지 → 심각도 평가 → 패치 생성 → 리포트 작성

**핵심 기술**:  
- **On-device LLM**: QLoRA로 파인튜닝한 Llama-3.2-1B 모델  
- **RAG 시스템**: 자동 CVSS 점수 산출을 위한 유사도 기반 검색이 가능한 벡터화된 CVE 데이터베이스  
- **외부 LLM**: CVSS ≥ 7.0인 취약점에 대한 자동 패치 코드 생성을 위한 Solar Pro2  
- **Framwork**: 멀티 에이전트 조율 및 워크플로우 통합을 위한 LangChain  

**검증 및 결과**:  
- 500개 검증 데이터셋에서 100개 샘플씩 5회 반복 랜덤 샘플링을 수행하여 모델 성능 검증  
- 코드 분석부터 패치 권장까지 전체 보안 검토 파이프라인 자동화 성공

**Links**:  
- Press Coverage: [Meta Blog](https://about.fb.com/ko/news/2025/10/meta-llm-agent-on-device-ai-workshop/), [ETNews Article](https://www.etnews.com/20251002000253)
***

### **Probe 안티바이러스 프로그램**

악성코드 탐지 및 시스템 최적화 기능을 갖춘 안티바이러스 솔루션.

**프로젝트 개요**:  
- 다양한 검사 모드(빠른 검사, 정밀 검사, 스마트 검사)와 시스템 최적화 기능을 갖춘 완전한 안티바이러스 애플리케이션 개발  
- 자체 악성코드 탐지 알고리즘을 설계하고 핵심 AV 엔진과 통합  
- 포괄적인 엔드포인트 보호를 위한 격리소 관리 시스템 및 PC 최적화 모듈 구현

**주요 기능**:  
- **다중 모드 검사**: 유연한 위협 탐지를 위한 빠른 검사, 정밀 검사, 스마트 검사 기능  
- **시스템 최적화**: 내장된 PC 성능 최적화 도구  
- **격리소 관리**: 탐지된 위협의 안전한 격리 및 관리  
- **실시간 보호**: 지속적인 모니터링 및 위협 방지

**사용 기술**:  
- **언어**: Python  
- **프레임워크**: PyQt (GUI)  
- **데이터베이스**: SQL (시그니처 관리)  
- **패키징**: Inno Setup

**링크**:  
- 자료 : [Wadiz](https://www.wadiz.kr/web/campaign/detail/153064), [문서](https://github.com/seok-hee97/resume/blob/main/docs/Probe-AV.pdf)

***

### **ML-WAF (머신러닝 웹 애플리케이션 방화벽)**
**Team Pyree**

머신러닝 기반 위협 탐지 기능을 갖춘 Nginx의 이벤트 기반 아키텍처를 활용한 고성능 웹 애플리케이션 방화벽.

**프로젝트 개요**:  
- ML 엔드포인트 REST API 호출 및 MySQL 데이터베이스 통합을 위해 Nginx의 비동기 I/O 구조를 활용한 확장 가능한 WAF 시스템 구축  
- 웹 공격 분류를 위한 머신러닝 모델을 사용한 실시간 위협 탐지 구현  
- 효율적인 요청 처리 및 모델 추론을 통해 고성능 방화벽 기능 달성

**아키텍처 및 설계**:  
- **이벤트 기반 처리**: 동시 요청 처리를 위한 Nginx의 논블로킹 I/O 활용  
- **ML 통합**: 실시간 위협 분류를 위한 REST API 엔드포인트  
- **데이터베이스 계층**: 로깅 및 공격 패턴 저장을 위한 MySQL  
- **컨테이너화**: 확장성 및 이식성을 위한 Docker 배포

**사용 기술**:  
- **언어**: Python, Lua  
- **프레임워크**: Django (관리 인터페이스), Flask (웹 개발), Nginx (프록시 계층)  
- **ML 도구**: 모델 개발을 위한 Jupyter Notebook  
- **클라우드 플랫폼**: AWS (EC2, SageMaker, S3, CloudFormation)  
- **데이터베이스**: MySQL, SQLite  
- **DevOps**: 컨테이너화를 위한 Docker

**링크**:  
- GitHub: [https://github.com/Team-Pyree/mlwaf](https://github.com/Team-Pyree/mlwaf)

***

### **KISA AI Challenge 2023**
**한국인터넷진흥원**

공격 유형 다중 클래스 분류에 초점을 맞춘 네트워크 트래픽 분석 챌린지.

**프로젝트 개요**:  
- 네트워크 트래픽 공격 분류를 위한 A-트랙 챌린지 참가  
- 다중 클래스 공격 탐지를 위한 TF-IDF 벡터화 및 SVM 분류기를 사용한 ML 파이프라인 개발  
- 70명의 참가자 중 상위 25% 내에서 경쟁력 있는 성능 달성

**접근 방식 및 결과**:  
- **특징 추출**: 네트워크 트래픽 패턴 추출을 위한 TF-IDF (Term Frequency-Inverse Document Frequency)  
- **분류 모델**: 다중 클래스 공격 분류를 위한 Support Vector Machine (SVM)  
- **성능**: 90.868점, 70개 팀 중 17위  

**사용 기술**:  
- **머신러닝**: Scikit-learn (TF-IDF, SVM)  
- **언어**: Python  
- **데이터 처리**: Pandas, NumPy

**링크**:  
- GitHub: [https://github.com/seok-hee97/kisa-ai-2023](https://github.com/seok-hee97/kisa-ai-2023)

***

### **Google ML Bootcamp 5기**

**프로젝트 개요**:  
- Deep Learning Specialization Coursera 교육 수료.  
- Kaggle 대회 "Binary Prediction of Poisonous Mushrooms"에서 상위 5% 달성 (2,422명 중 76위)  
- GDPR 준수 Q&A 어시스턴트를 위한 Gemma-2-2B 모델 파인튜닝

**대회 성과**:  
- **챌린지**: Binary Prediction of Poisonous Mushrooms  
- **순위**: 2,422명 중 76위 (상위 3.1%)  
- **접근 방식**: Feature engineering과 XGBoost, LightGBM 앙상블 전략 활용

**Gemma Sprint 프로젝트**:  
- Direct Preference Optimization (DPO)를 사용하여 GDPR 준수 Q&A를 위한 Gemma-2-2B 모델 파인튜닝  
- Hugging Face 플랫폼에 특화된 모델 배포  

**사용 기술**:  
- **딥러닝**: TensorFlow, PyTorch  
- **LLM 파인튜닝**: Transformers, Gemma-2  
- **모델 배포**: Hugging Face Hub  
- **대회**: Kaggle 플랫폼

**링크**:  
- Gemma Sprint 모델: [https://huggingface.co/cycloevan/gdpr_gemma-2-2b](https://huggingface.co/cycloevan/gdpr_gemma-2-2b)

***

## **수상 및 인정**

**우수상 (한국전파진흥협회장상)**  
Meta LLM Agent & On-device AI Workshop 1기  
주최: Meta, 한국전파진흥협회, Upstage  
날짜: 2025년 10월 2일  
프로젝트: AI 코드 리뷰 기반 자동 취약점 분석 시스템 (팀 'LLaMA Guard')


### **[ENG]**
### **AI-Powered Code Vulnerability Detection System**
**Meta Llama Academy 1th | Award: Excellence Award RAPA(Korea Radio Promotion Association)**  

An automated code security analysis system utilizing multi-agent LLM architecture for vulnerability detection, severity assessment, and patch generation.

**Project Overview**:  
- Designed and implemented a multi-LLM agent system that automatically detects security vulnerabilities in source code,             
  evaluates severity using CVE database comparison, and generates remediation patches for high-risk issues                   
- Deployed RAG (Retrieval-Augmented Generation) architecture to compare detected vulnerabilities against vectorized CVE database for severity scoring (CVSS 0.0-10.0 scale)  
- Integrated LangChain framework to orchestrate the complete workflow: vulnerability detection → severity assessment → patch generation → report creation

**Key Technologies**:  
- **On-device LLM**: Fine-tuned Llama-3.2-1B model using QLoRA with Hugging Face's code_vulnerability_security DPO dataset for Supervised Fine-Tuning  
- **RAG System**: Vectorized CVE database with similarity-based retrieval for automated CVSS scoring  
- **External LLM**: Solar Pro2 for automated patch code generation for vulnerabilities with CVSS ≥ 7.0  
- **Framework**: LangChain for multi-agent orchestration and workflow integration  

**Validation & Results**:  
- Conducted 5 iterations of random sampling (100 samples each) from 500 validation datasets to verify model performance  
- Successfully automated the entire security review pipeline from code analysis to patch recommendation

**Links**:  
- Press Coverage: [Meta Blog](https://about.fb.com/ko/news/2025/10/meta-llm-agent-on-device-ai-workshop/), [ETNews Article](https://www.etnews.com/20251002000253)

***

### **Probe Anti-Virus Program**

Antivirus solution with comprehensive malware detection and system optimization capabilities.

**Project Overview**:  
- Developed complete antivirus application with multiple scan modes (Quick Scan, Deep Scan, Smart Scan) and system optimization features  
- Engineered proprietary malware detection algorithms and integrated them with the core AV engine  
- Implemented quarantine management system and PC optimization module for comprehensive endpoint protection

**Key Features**:  
- **Multi-mode Scanning**: Quick, Deep, and Smart scan capabilities for flexible threat detection  
- **System Optimization**: Built-in PC performance optimization tools  
- **Quarantine Management**: Secure isolation and management of detected threats  
- **Real-time Protection**: Continuous monitoring and threat prevention

**Technologies Used**:  
- **Languages**: Python  
- **Frameworks**: PyQt for GUI development  
- **Database**: SQL for threat signature management  
- **Packaging**: Inno Setup for distribution

**Links**:  
- DOCS : [Wadiz](https://www.wadiz.kr/web/campaign/detail/153064), [Docs](https://github.com/seok-hee97/resume/blob/main/docs/Probe-AV.pdf)

***

### **ML-WAF (Machine Learning Web Application Firewall)**

High-performance web application firewall leveraging Nginx's event-driven architecture with machine learning-based threat detection.

**Project Overview**:  
- Built scalable WAF system utilizing Nginx's asynchronous I/O structure for ML endpoint REST API calls and MySQL database integration  
- Implemented real-time threat detection using machine learning models for web attack classification  
- Achieved high-performance firewall capabilities through efficient request processing and model inference     

**Architecture & Design**:  
- **Event-Driven Processing**: Leveraged Nginx's non-blocking I/O for concurrent request handling  
- **ML Integration**: REST API endpoint for real-time threat classification  
- **Database Layer**: MySQL for logging and attack pattern storage  
- **Containerization**: Docker deployment for scalability and portability

**Technologies Used**:  
- **Languages**: Python, Lua  
- **Frameworks**: Django (WAS), Flask (web develop), Nginx (proxy layer)  
- **ML Tools**: Jupyter Notebook for model development  
- **Cloud Platform**: AWS (EC2, SageMaker, S3, Cloudformation)  
- **Databases**: MySQL, SQLite  
- **DevOps**: Docker for containerization

**Links**:  
- GitHub : https://github.com/Team-Pyree/mlwaf

***

### **KISA AI Challenge 2023**

Network traffic analysis competition focused on attack type multi-class classification.

**Project Overview**:  
- Participated in A-track challenge for network traffic attack classification  
- Developed ML pipeline using TF-IDF vectorization and SVM classifier for multi-class attack detection  
- Achieved competitive performance ranking in top 25% among 70 participants

**Approach & Results**:  
- **Feature Engineering**: TF-IDF (Term Frequency-Inverse Document Frequency) for network traffic pattern extraction  
- **Classification Model**: Support Vector Machine (SVM) for multi-class attack categorization  
- **Performance**: Score of 90.868, ranked 17th out of 70 teams  

**Technologies Used**:  
- **Machine Learning**: Scikit-learn (TF-IDF, SVM)  
- **Languages**: Python  
- **Data Processing**: Pandas, NumPy

**Links**:  
- GitHub : https://github.com/seok-hee97/kisa-ai-2023

***

### **GOOGLE-ML-BOOTCAMP 5th**

**Project Overview**:  
- Completed Deep Learning Specialization certification  
- Achieved top 5% ranking in Kaggle competition "Binary Prediction of Poisonous Mushrooms" (76/2,422 participants)  
- Fine-tuned Gemma-2-2B model for GDPR compliance Q&A assistant

**Competition Achievement**:  
- **Challenge**: Binary Prediction of Poisonous Mushrooms  
- **Ranking**: 76 out of 2,422 participants (top 3.1%)  
- **Approach**: Feature engineering with XGBoost and LightGBM ensemble strategy

**Gemma Sprint Project**:  
- Fine-tuned Gemma-2-2B model for GDPR compliance Q&A using Direct Preference Optimization (DPO)
- Deployed specialized GDPR assistant model on Hugging Face platform  

**Technologies Used**:  
- **Deep Learning**: TensorFlow, PyTorch  
- **LLM Fine-tuning**: Hugging Face Transformers, Gemma-2  
- **Model Deployment**: Hugging Face Hub  
- **Competition**: Kaggle platform

**Links**:  
- Gemma Sprint Model : https://huggingface.co/cycloevan/gdpr_gemma-2-2b

***

## **AWARDS & RECOGNITION**

**Excellence Award (Korea Radio Promotion Association Director Award)**  
Meta LLM Agent & On-device AI Workshop 1st Cohort  
Organized by: Meta, RAPA, Upstage  
Date: October 2, 2025  
Project: AI Code Review-Based Automated Vulnerability Analysis System (Team 'LLaMA Guard')

***


