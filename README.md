
# Better In Focus (BIF) - AI 기반 자립 지원 서비스

> "나만의 속도로 세상과 연결될 수 있도록"

**Better In Focus(BIF)**는 경계선 지능인들이 일상적인 과업을 관리하고, 사회적 상호작용을 연습하며, 자신의 감정을 더 잘 이해하고 표현할 수 있도록 돕는 AI 기반 자립 지원 서비스입니다. 저희 팀 SAGE는 기술의 힘을 통해 복지 사각지대에 있는 분들의 자립을 돕고, 그들이 사회의 일원으로 자신감을 가질 수 있도록 지원하고자 합니다.

<br>

## ✨ 주요 기능 (Key Features)

BIF는 사용자의 인지적 부담을 최소화하고, 긍정적인 피드백을 통해 자기 효능감을 높일 수 있도록 설계되었습니다.

| 기능 | 설명 |
| :--- | :--- |
| **💬 AI 감정 일기** | 사용자가 자신의 하루와 감정을 기록하면, Azure OpenAI 기반의 AI가 안전하고 따뜻한 공감과 지지를 제공합니다. 캘린더에서 감정의 흐름을 한눈에 파악할 수 있습니다. |
| **📊 감정 통계** | (마이페이지) 월별 감정 변화, 주요 감정 키워드 분석 등 데이터 시각화를 통해 자신의 감정 패턴을 객관적으로 이해하고 관리할 수 있도록 돕습니다. |
| **✅ AI 할 일 관리** | "내일 10시에 병원 예약"과 같이 간단한 문장만 입력하면 AI가 날짜, 시간, 내용을 분석하여 할 일을 자동으로 등록하고, 지정된 시간에 알림을 보내 체계적인 생활 관리를 지원합니다. |
| **🎭 사회성 훈련 시뮬레이션** | 직장, 친구 관계 등 다양한 사회적 상황에 대한 대화 시뮬레이션을 통해 상호작용을 연습할 수 있습니다. TTS(Text-to-Speech) 기능으로 실제 대화와 유사한 경험을 제공합니다. |
| **👨‍👩‍👧 보호자 연동** | 보호자는 사용자의 감정 통계와 할 일 목록을 확인하며 사용자의 상태를 이해하고, 필요시 할 일 수정 등을 통해 정서적, 실질적 지원을 제공할 수 있습니다. |

<br>

## 🛠️ 기술 스택 (Tech Stack)

| 구분 | 기술 |
| :--- | :--- |
| **Back-end** | <img src="https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white"> <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white"> <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=spring-security&logoColor=white"> <img src="https://img.shields.io/badge/JPA-5A2D23?style=for-the-badge&logo=hibernate&logoColor=white"> <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"> <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white"> <img src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=json-web-tokens&logoColor=white"> <img src="https://img.shields.io/badge/Gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white"> |
| **Front-end** | <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black"> <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white"> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"> <img src="https://img.shields.io/badge/Zustand-000000?style=for-the-badge&logo=zustand&logoColor=white"> <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white"> <img src="https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white"> |
| **AI** | <img src="https://img.shields.io/badge/Azure_OpenAI-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white"> <img src="https://img.shields.io/badge/Azure_AI_Content_Safety-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white"> |
| **DevOps & Infra** | <img src="https.img.shields.io/badge/Microsoft_Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white"> <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"> <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white"> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white"> |

<br>

## 🏛️ 아키텍처 (Architecture)

BIF는 확장성과 안정성을 고려하여 MSA(Micro-Service Architecture) 기반으로 설계되었습니다. 주요 구성은 다음과 같습니다.

- **Frontend**: React와 Vite를 기반으로 한 SPA로, Azure Static Web Apps에 배포되어 전 세계 사용자에게 빠른 속도를 제공합니다.
- **Backend**: Spring Boot 기반의 API 서버로, Docker 컨테이너화되어 Azure Container Apps에서 운영됩니다. 인증/인가, 비즈니스 로직 처리를 담당합니다.
- **Database**: 사용자 데이터와 서비스의 핵심 정보는 **Azure Database for MySQL**에 저장되며, **Azure Cache for Redis**를 통해 자주 사용되는 데이터를 캐싱하여 성능을 최적화합니다.
- **AI Service**: **Azure OpenAI**를 활용하여 자연스러운 대화형 AI 기능을 구현했으며, **Azure AI Content Safety**를 통해 유해 콘텐츠를 필터링하여 안전한 서비스 환경을 보장합니다.
- **CI/CD**: **GitHub Actions**를 통해 소스 코드 변경 시 자동으로 빌드, 테스트, 배포가 이루어지는 CI/CD 파이프라인을 구축하여 개발 효율성과 안정성을 높였습니다.

*(시스템 구성도 이미지는 프로젝트 발표 자료를 참고하여 추가해주세요.)*

<br>

## 🚀 시작하기 (Getting Started)

### Backend

1.  `bif-back` 디렉토리로 이동합니다.
2.  `src/main/resources/application.yml` 파일을 열어 환경에 맞게 DB, Redis, Azure OpenAI Key 등의 정보를 수정합니다.
3.  아래 명령어를 실행하여 서버를 구동합니다.
    ```bash
    ./gradlew bootRun
    ```

### Frontend

1.  `bif-front` 디렉토리로 이동합니다.
2.  아래 명령어를 실행하여 의존성을 설치합니다.
    ```bash
    npm install
    ```
3.  `.env.local` 파일을 생성하고 백엔드 API 서버 주소를 환경 변수로 설정합니다.
    ```
    VITE_API_BASE_URL=http://localhost:8080
    ```
4.  아래 명령어를 실행하여 개발 서버를 시작합니다.
    ```bash
    npm run dev
    ```

<br>

## 🧑‍💻 나의 기여 (My Contributions)

이 프로젝트에서 저는 다음과 같은 역할을 수행하며 기여했습니다.

#### **1. 기능 개발 (BE/FE)**
-   **마이페이지 & 감정 통계**: 사용자가 자신의 감정 데이터를 시각적으로 탐색하고 이해할 수 있는 마이페이지와 통계 기능을 Full-Stack으로 개발했습니다. Chart.js를 활용하여 월별 감정 비율, 감정 변화 추이 등을 시각화하고, 백엔드에서는 통계 데이터를 효율적으로 집계하고 분석하는 API를 설계 및 구현했습니다.
-   **ERD 설계**: 프로젝트의 핵심 도메인(사용자, 일기, 할 일, 시뮬레이션 등)을 정의하고, 확장성과 데이터 무결성을 고려한 ERD(Entity-Relationship Diagram)를 설계했습니다.

#### **2. 클라우드 인프라 및 DevOps**
-   **Microsoft Azure 총괄 운영**: 프로젝트에 필요한 모든 인프라(BE, FE, DB, Cache)를 **Microsoft Azure** 환경에 구축하고 운영했습니다.
    -   **Backend**: Spring Boot 애플리케이션을 Docker 이미지로 빌드하여 **Azure Container Apps**에 배포.
    -   **Frontend**: React 기반의 정적 파일을 **Azure Static Web Apps**에 배포.
    -   **Database/Cache**: **Azure Database for MySQL**과 **Azure Cache for Redis** 인스턴스를 생성하고 애플리케이션과 연동.
-   **Azure OpenAI 연동**: 감정 일기 기능의 핵심인 AI 응답 생성을 위해 **Azure OpenAI Service**를 백엔드 시스템에 연동하는 작업을 주도했습니다.

#### **3. 프로젝트 정책 및 환경 설정**
-   **전역 에러 코드 및 메시지 정책 수립**: 클라이언트와 서버 간의 원활한 통신과 효율적인 에러 핸들링을 위해 프로젝트 전반에 사용될 에러 코드와 메시지 포맷에 대한 정책을 수립하고 적용했습니다.

<br>

## 👨‍👩‍👧‍👦 팀 SAGE

| 이름 | 역할 | GitHub |
| :--- | :--- | :--- |
| **유동기** | **마이페이지/통계(BE/FE), Azure 인프라 총괄, ERD 설계, 에러 정책** | `(본인 GitHub ID)` |
| 장민호 | GitHub Projects/Issues 관리, Todo 기능(BE/FE), Azure 배포 | `(팀원 GitHub ID)` |
| 노종현 | 시뮬레이션 기능(BE/FE), 회의록 작성 | `(팀원 GitHub ID)` |
| 오영화 | Figma 디자인, 소셜 로그인(BE/FE), 인증/인가, Azure 배포 | `(팀원 GitHub ID)` |
| 김소영 | 서비스 기획/발표, Figma 디자인, 감정 일기(BE/FE) | `(팀원 GitHub ID)` |


