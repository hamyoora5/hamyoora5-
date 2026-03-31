# 제조 데이터 분석 / AI / 스마트팩토리 엔지니어

현재 문제와 요구사항을 정확하게 파악하고 분석하여
데이터 흐름을 이해하고 설계하여 현장 문제를 해결하는 엔지니어입니다.
단순한 일회성 구현을 넘어 성능을 최적화하고, 실질적인 비즈니스 성과를 만드는 시스템을 지향합니다.

---

## 핵심 역량 (Core Skills)

*   **Language:** Python, SQL (Oracle, PostgreSQL)
*   **Backend:** FastAPI
*   **Database:** PostgreSQL, Redis
*   **Infrastructure:** Docker, Celery
*   **AI:** LLM (OpenAI, LangChain, Agentic AI), STT (Whisper), Vision AI (ResNet, YOLOv8)
*   **Data Analysis:** Pandas, NumPy, Matplotlib, Seaborn

---

## 교육 과정 (Education)

**빅데이터 분석 및 AI(머신·딥러닝) 활용 개발 전문가 취업캠프**
*   Oracle SQL 고급 쿼리 및 데이터베이스 조작 학습
*   Python 기반 데이터 수집·전처리 및 분석 (Pandas, NumPy)
*   탐색적 데이터 분석(EDA) 및 통계 기반 데이터 해석 (Matplotlib, Seaborn)
*   머신러닝·딥러닝 모델 학습 및 성능 최적화
*   Pytorch·Transformer/LLM 기반 AI 모델 활용 및 튜닝
*   데이터·AI 서비스 API 개발 및 NLP·STT 기반 음성 데이터 처리
*   Agentic AI 기반 음성·PDF 처리 및 멀티에이전트 시스템 구현

---

## 주요 프로젝트 (Projects)

### 1. A4 AI 면접 플랫폼 (실시간 멀티모달 면접 시스템)
*   **소개:** 지원자가 웹 브라우저에서 WebRTC 기반 화상 면접을 진행하면, AI가 실시간으로 영상·음성·답변 내용을 분석하여 종합 평가 리포트를 생성하는 서비스
*   **핵심 가치:** 
    *   **맞춤형 질문 생성:** 이력서·직무·회사 데이터를 종합한 RAG 기반 개인화 질문 제공
*   **성과:** 통합 구현 시 발생한 **최대 200초 이상의 지연 시간**을 분석하여 **최종 응답 시간 11초**까지 단축
*   **핵심 해결 전략:**
    *   **전략적 지연 평가 (Deferred Evaluation):** 면접 중 GPU를 질문 생성에만 100% 집중시키고, 답변 평가는 종료 후 일괄 배치 처리하도록 조정하여 대기 시간을 50% 이상 단축.
    *   **STT 전송 구조 최적화:** 3초 단위 반복 전송 구조를 답변 완료 후 1회 전송으로 개편하여 워커 부하 및 대규모 지연 요소 제거.
*   **GitHub:** [Repository](https://github.com/jaemin1020/Big20_aI_interview_project)

---

### 2. Lala Factory: ERP + AI 분석 자동화 (PoC)
*   **소ㄱ개:** ERP 생산 데이터 분석 및 LLM 기반 지능형 공정 분석이 통합된 PoC 시스템
*   **핵심 가치:** 
    *   **AILA Agent (Text-to-SQL):** 사용자의 자연어 질문을 SQL로 변환하여 실시간 데이터 분석 및 통찰 제공 (EXAONE-3.5 활용)
    *   **통합 공정 관리:** 수주 등록 부터 생산 지시, 실적 집계, KPI 모니터링까지 전 프로세스 우선 생성 자동화
*   **기술 스택:** Python, FastAPI, Streamlit, PostgreSQL (Docker), LLM (EXAONE-3.5, Llama-CPP)
*   **GitHub:** [Repository](https://github.com/hamyoora5/lala_factory)

---

### 3. Smart Factory Vision AI: 자동차 도어 결함 탐지
*   **소개:** 자동차 생산 라인에서 도어 이미지를 실시간 분석하여 불량 여부 판별 및 결함 위치를 추락하는 AI 비전 시스템
*   **핵심 가치:** 
    *   **2-Stage 파이프라인:** 이진 분류(ResNet-18)와 정밀 결함 탐지(YOLOv8)를 결합하여 정확도와 분석 속도 동시 확보
    *   **실시간 공정 설계:** 컨베이어 벨트 속도(3~6m/min)를 고려해 15초 주기로 이미지 촬영 및 분석이 수행되도록 가상 시뮬레이션 시스템 설계
*   **기술 스택:** PyTorch, YOLOv8, ResNet-18, OpenCV, FastAPI, Streamlit, PostgreSQL (Docker)
*   **GitHub:** [Repository](https://github.com/hamyoora5/Defect_Classification)

---

### 4. MES + QMS: AI 품질 판정 연동 시스템
*   **소개:** ERP 작업지시 기반 생산 실행부터 AI(미생물) 자동 품질 판정 및 ERP 실적 연동까지 통합된 스마트 팩토리 시스템
*   **핵심 가치:** 
    *   **생산 공정 제어:** 작업 지시 수신부터 생산 시작, 중단(STOPPED), 재가동, 종료까지 전 과정 실시간 상태 관리
    *   **AI 품질 판정 연계:** AI 판정 결과(PASS/FAIL)를 생산 데이터와 연동하여 품질 상태 업데이트 자동화
    *   **추적성(Traceability) 확보:** 작업지시-일일생산코드(DP)-품질테스트번호(QT)를 연계하여 생산부터 최종 판정까지 전 공정 이력 추적
*   **기술 스택:** Java 17, Spring Boot 3, React 18, PostgreSQL (Docker), Redis
*   **GitHub:** [Repository](https://github.com/hamyoora5/mes_project)

---

## 관심 및 학습 분야 (Learning & Growth)

스마트 팩토리의 고도화를 지향하며 지속적으로 역량을 확장하고 있습니다.
*   **Java:** 엔터프라이즈 환경 및 다양한 제조 시스템과의 연동을 위한 역량 확보
*   **SAP / ABAP:** SAP ERP 기반의 데이터 연동 및 생산 관리 최적화를 위한 언어 학습

---

## Contact
*   **GitHub:** [hamyoora5](https://github.com/hamyoora5)
