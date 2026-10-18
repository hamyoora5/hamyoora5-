# 제조 데이터 분석 / AI / 스마트팩토리 엔지니어

현재 문제와 요구사항을 정확하게 파악하고 분석하여
데이터 흐름을 이해하고 설계하여 현장 문제를 해결하는 엔지니어입니다.
단순한 일회성 구현을 넘어 성능을 최적화하고, 실질적인 비즈니스 성과를 만드는 시스템을 지향합니다.

---

## 핵심 역량 (Core Skills)

*   **Language:** Python, SQL (Oracle, PostgreSQL)
*   **Backend:** FastAPI, Flask, Spring Boot 3
*   **Frontend:** React 18, Streamlit
*   **Database:** PostgreSQL (Aurora), Redis
*   **Infrastructure:** Docker, AWS App Runner, Celery
*   **AI:** LLM (OpenAI, LangChain, Agentic AI), STT (Whisper), Vision AI (ResNet, YOLOv8)
*   **Data Analysis:** Pandas, NumPy, Matplotlib, Seaborn
*   **업무 시스템 연동:** Microsoft Graph, Power Automate

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

## 실무 프로젝트 (In Production)

> **사내 시스템이라 소스 코드는 공개하지 않습니다.** 화면시안·기획 문서만 HTML로 첨부하며,
> 그 안의 업체명·제품코드·수량·금액·연락처는 **모두 가상의 값으로 가공**했습니다.
> 실제 데이터는 들어 있지 않습니다.

### 1. 외주 생산관리 대시보드 — 운영 중

*   **소개:** 외주 협력사의 발주부터 부자재 전달, 입고 실적, 정산 마감까지를 한 화면에서 관리하는 사내 서비스. 기획·설계·개발·배포·운영을 단독 수행
*   **핵심 가치:**
    *   **진행률·설비 가동 점유율:** 조업일수를 반영한 누적 CAPA 기준으로 외주처별 진행 상황과 설비 여력 산출
    *   **부자재 사용기록서 자동 생성:** ERP BOM 전개 결과를 협력사별 엑셀로 생성, ZIP 일괄 다운로드
    *   **마감 교차 대조:** 기준 파일 5종을 대조해 수량·정산금액 확정
*   **설계 관점:** 기존 엑셀 업무 방식은 유지하고 집계·문서 생성만 자동화하여 현장 도입 저항 최소화
*   **기술 스택:** Python, Flask, SQLAlchemy, PostgreSQL (Aurora), Docker, AWS App Runner, Microsoft Graph, SSO SSO
*   **화면시안:** [23개 화면 동작 시안](https://hamyoora5.github.io/hamyoora5-/showcase/vms/demo.html) · [사용자 매뉴얼 16장](https://hamyoora5.github.io/hamyoora5-/showcase/vms/manual.html) · [설명](showcase/vms/README.md)

### 2. 외주 통합관리 시스템 — 설계 단계

*   **소개:** 발주 → 생산 시작 → 품질검사 → 출고 → 마감 정산 → 지급으로 흩어진 외주 업무를 단일 시스템으로 일원화하는 설계. 1차 범위는 비실시간 원격 품질검사와 거래명세서 등록
*   **산출물:** 화면정의서 42종, 클릭 가능한 화면 시안 57종, 아키텍처 설계, DB 구조 검토안
*   **설계 관점:** 같은 사실을 여러 곳에 중복 기록하는 구조 제거, 증빙 무결성 확보, 향후 검사 자동화를 위한 데이터 축적 전제
*   **화면시안:** [클릭 가능한 화면 시안](https://hamyoora5.github.io/hamyoora5-/showcase/remote-inspection/mockup.html)

### 3. 반복 업무 자동화

*   **소개:** Power Automate 기반으로 거래명세서 반영 및 정보 공유 등 **월 1,000건 이상**의 반복 업무 자동화

---

## 학습 프로젝트 (Projects)

> 교육과정에서 진행한 팀 프로젝트와, 가상의 제조 환경·공개 데이터를 전제로
> 설계·구현한 개인 프로젝트입니다. 각 저장소 README에 설계 근거와 한계를 정리했습니다.

### 1. A4 AI 면접 플랫폼 (실시간 멀티모달 면접 시스템) — 팀 프로젝트

*   **소개:** 지원자가 웹 브라우저에서 WebRTC 기반 화상 면접을 진행하면, AI가 실시간으로 영상·음성·답변 내용을 분석하여 종합 평가 리포트를 생성하는 서비스
*   **시스템 구성:** 역할별로 4개 서비스를 분리하고 Celery 큐로 연결 — API·세션 관리(`backend-core`), WebRTC 미디어 수신(`media-server`), 추론(`ai-worker`), 화면(`frontend`). **추론 워커를 GPU용·CPU용으로 나눠** 무거운 작업과 가벼운 작업이 같은 자원을 두고 경합하지 않도록 구성
*   **핵심 가치:**
    *   **맞춤형 질문 생성:** 이력서·직무·회사 데이터를 종합한 RAG 기반 개인화 질문 제공 (PDF·DOCX 파싱 후 pgvector 유사도 검색)
    *   **멀티모달 분석:** 영상(표정·감정), 음성(STT·음향 특징), 답변 텍스트를 각각 분석해 종합 평가 리포트 생성
*   **성과:** 통합 구현 시 발생한 **최대 200초 이상의 지연 시간**을 분석하여 **최종 응답 시간 11초**까지 단축
*   **핵심 해결 전략:**
    *   **전략적 지연 평가 (Deferred Evaluation):** 면접 중 GPU를 질문 생성에만 100% 집중시키고, 답변 평가는 종료 후 일괄 배치 처리하도록 조정하여 대기 시간을 50% 이상 단축
    *   **STT 전송 구조 최적화:** 3초 단위 반복 전송 구조를 답변 완료 후 1회 전송으로 개편하여 워커 부하 및 대규모 지연 요소 제거
*   **기술 스택:** Python, FastAPI, Celery, Redis, PostgreSQL + pgvector, React, WebRTC (aiortc), LLM (EXAONE-3.5, LangChain), DeepFace, OpenCV, librosa, Docker
*   **GitHub:** [Repository](https://github.com/jaemin1020/Big20_aI_interview_project)

---

### 2. Lala Factory: ERP + AI 분석 자동화 (PoC)

*   **소개:** 가상의 화장품 포장 제조사를 전제로, ERP 생산 데이터 분석과 LLM 기반 공정 분석을 통합한 PoC 시스템
*   **시스템 구성:** FastAPI 백엔드(`:8001`) · Streamlit 대시보드(`:8501`) · PostgreSQL(Docker) · 로컬 LLM 에이전트. 엑셀의 한글 BOM·수주 데이터를 적재 스크립트로 RDBMS 스키마에 이관하고, KPI는 DB View로 사전 집계
*   **핵심 가치:**
    *   **설비 배정 자동화:** 라인별 대기부하(대기·진행중 지시수량)와 직전 작업과의 유사도(규격·용량·카테고리)를 점수화해 **가장 빨리 끝나는 라인을 선택**. 동점 시 분산 배정하여 부하 균등화
    *   **AILA Agent (Text-to-SQL):** DB 스키마를 프롬프트로 전달받은 LLM이 자연어 질문을 SELECT 쿼리로 변환·실행하고, 결과를 다시 자연어 답변으로 반환 (EXAONE-3.5). 질문·생성 SQL·처리 상태를 이력 테이블에 적재
    *   **통합 공정 관리:** 수주 등록부터 생산 지시, 실적 집계, KPI 모니터링까지 전 프로세스 자동화
*   **기술 스택:** Python, FastAPI, Streamlit, SQLAlchemy, PostgreSQL (Docker), LLM (EXAONE-3.5, Llama-CPP)
*   **GitHub:** [Repository](https://github.com/hamyoora5/lala_factory)

---

### 3. Smart Factory Vision AI: 자동차 도어 결함 탐지

*   **소개:** 자동차 생산 라인에서 도어 이미지를 실시간 분석하여 불량 여부 판별 및 결함 위치를 추적하는 AI 비전 시스템 (공개 데이터셋 기반, 가상 라인 조건)
*   **시스템 구성:** 카메라 시뮬레이터가 주기적으로 이미지를 전송 → FastAPI 추론 서버(`:8000`)가 2단 파이프라인 실행 → PostgreSQL(Docker) 적재 → Streamlit 대시보드 시각화. 결함 좌표는 한 장에 여러 개가 나올 수 있어 **JSONB 배열**로 저장하고, 조회가 잦은 검사시각·불량여부·제품ID에 인덱스 구성
*   **핵심 가치:**
    *   **2-Stage 파이프라인:** 이진 분류(ResNet-18)로 양품을 먼저 걸러내고 **불량 판정 건에만** 정밀 탐지(YOLOv8, 1024px)를 적용하여 정확도와 분석 속도 동시 확보. 전수검사에서 대부분이 양품이므로 고해상도 추론 호출이 불량률에 비례해 감소
    *   **실시간 공정 설계:** 컨베이어 속도 3~6m/min 에서 도어(1.2m) 통과시간 12~24초를 역산하고, **누락이 없도록 최소 통과시간 이내인 15초**를 촬영·분석 주기로 설정. 주기가 길면 누락, 짧으면 중복 촬영으로 연산 낭비
    *   **현장 조건 반영:** 카메라 설치 각도 편차(회전 증강)와 좌·우 도어 대칭(상하 반전 증강)을 학습 단계에서 흡수. 스크래치·손상·단차·실링 4종 결함 탐지
*   **기술 스택:** PyTorch, YOLOv8, ResNet-18, OpenCV, FastAPI, Streamlit, PostgreSQL (Docker)
*   **GitHub:** [Repository](https://github.com/hamyoora5/Defect_Classification)

---

### 4. MES + QMS: AI 품질 판정 연동 시스템

*   **소개:** ERP 작업지시 기반 생산 실행부터 AI(미생물) 자동 품질 판정 및 ERP 실적 연동까지 통합된 스마트 팩토리 시스템 (AI 판정은 결과를 가정한 시뮬레이션)
*   **시스템 구성:** Spring Boot API 서버(`:8002`) · React UI(`:3001`) · PostgreSQL(Docker) · Redis. 작업지시·생산이력·불량이력·생산실적·품질검사·ERP전송 결과를 각각의 테이블로 분리해, 집계값이 아니라 **발생 사건 단위로 적재**
*   **핵심 가치:**
    *   **생산 공정 제어:** 작업 지시 수신부터 생산 시작, 중단(STOPPED), 재가동, 종료까지 전 과정 실시간 상태 관리. `READY → IN_PROGRESS → STOPPED → IN_PROGRESS → COMPLETED` 전이를 정의해 **중단·재가동을 예외가 아닌 모델의 일부로 처리**하고, 중단 구간을 별도 이력으로 남겨 가동률 산출의 근거 확보
    *   **AI 품질 판정 연계:** 판정 전 실적은 `WAIT_QC` 로 보류하고, AI 판정 결과(PASS/FAIL)가 품질 상태와 생산 상태에 자동 반영된 뒤 ERP 전송용 데이터로 저장
    *   **추적성(Traceability) 확보:** 작업지시-일일생산코드(DP)-품질테스트번호(QT)를 바코드로 연계하여, 최종 판정 결과에서 생산 시점·설비·중단 이력까지 역추적
    *   **ERP / MES 역할 분리:** ERP는 계획·집계, MES는 실행·기록을 담당하도록 경계 설정
*   **기술 스택:** Java 17, Spring Boot 3, Spring Data JPA, React 18, PostgreSQL (Docker), Redis
*   **GitHub:** [Repository](https://github.com/hamyoora5/mes_project)

---

## 관심 및 학습 분야 (Learning & Growth)

현장에서 반복 업무 자동화와 데이터 연계를 진행하면서, 제약조건이 얽힌 생산계획 문제는
자동화만으로는 풀리지 않는다는 것을 확인했습니다.
**제조 운영 데이터 기반 AI 생산계획 및 스케줄링 최적화**를 중심으로 공부하고 있습니다.

*   **생산계획 및 스케줄링 최적화:** 수주·납기·자재 수급·설비 생산능력 등 다양한 제약조건을 반영한 생산계획 모델을 설계하고, 예측 및 최적화 알고리즘을 결합하여 **납기 준수와 설비 활용 효율**을 개선하는 방안
*   **스마트팩토리 구축:** 설비·IoT 데이터와 ERP·MES 등 제조 시스템을 연계하는 역량
*   **제조 AX — LLM · AI Agent 접목:** 데이터 분석을 넘어 **의사결정 지원과 업무 실행까지** 지능화하는 방향

---

## Contact
*   **GitHub:** [hamyoora5](https://github.com/hamyoora5)
