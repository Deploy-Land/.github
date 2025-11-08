# 🚀 [Deploy.Land](https://dev.d20iv4pldubgty.amplifyapp.com/)

> **AWS 기반 완전 자동화된 CI/CD 파이프라인**

## 😁 팀원 소개
|                                                                 **고동현**                                                                  |                                                              **백동민**                                                               |                                                               **최윤호**                                                                |
| :-----------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------: |
| [<img src="https://avatars.githubusercontent.com/u/93601786?v=4" height=150 width=150> <br/> @Gosorasora](https://github.com/Gosorasora) <br/> **Infra, BE** | [<img src="https://avatars.githubusercontent.com/u/84498742?v=4" height=150 width=150> <br/> @dongmin0204](https://github.com/dongmin0204) <br/> **Infra, FE** | [<img src="https://avatars.githubusercontent.com/u/151824752?v=4" height=150 width=150> <br/> @yunhoch0i](https://github.com/yunhoch0i) <br/> **Infra, QA** |


## 📋 프로젝트 소개

Deploy Land는 **AWS에서 프로덕션 배포까지** 전 과정을 자동화하고, **재밌는 그래픽**으로 실시간으로 모니터링 및 알림을 제공하는 서버리스 CI/CD 플랫폼입니다.

### ✨ 주요 기능

- 🔄 **완전 자동화된 CI/CD** - GitHub Push → Build → Deploy → Validation
- 🎮 **게임형 모니터링** - AWS Amplify를 통한 시각적 파이프라인 진행 상황 확인
- 📊 **실시간 알림** - Discord/Slack으로 배포 성공/실패 즉시 알림
- 🔍 **자동 헬스체크** - 배포 후 서비스 상태 자동 검증
- 🛡️ **유령 배포 방지** - 잘못된 배포 설정 자동 감지 및 알림

---

## 🏗️ 아키텍처

<img width="720" height="584" alt="image" src="https://github.com/user-attachments/assets/0714e3b2-04ca-4664-99cd-16e82f27807d" />


### 🧩 컴포넌트 설명

| 서비스 | 역할 | 설명 |
|--------|------|------|
| **GitHub** | Source | 소스 코드 저장소 |
| **CodePipeline** | Orchestration | CI/CD 파이프라인 오케스트레이션 |
| **CodeBuild** | Build | 애플리케이션 빌드 |
| **Elastic Beanstalk** | Deployment | 프로덕션 환경 배포 |
| **DynamoDB** | State Management | 파이프라인 상태 추적 |
| **EventBridge** | Event Routing | Lambda 트리거 |
| **Lambda (write)** | API | 배포 과정 DB 작성 및 알림 전송 |
| **Lambda (read)** | API | 상태 조회 API |
| **Lambda (Validation)** | Notification | Health Check 검증 알림 전송 |
| **API Gateway** | API Endpoint | REST API 엔드포인트 |
| **Amplify** | Monitoring | 게임형 파이프라인 모니터링 앱 |
| **Discord/Slack** | Notification | 실시간 알림 수신 |


## 🛠️ 기술 스택

### Infrastructure
- **AWS CodePipeline** - CI/CD 오케스트레이션
- **AWS CodeBuild** - 빌드 자동화
- **AWS Elastic Beanstalk** - 애플리케이션 배포
- **AWS Lambda** - 서버리스 함수
- **Amazon DynamoDB** - NoSQL 데이터베이스
- **Amazon EventBridge** - 이벤트 라우팅
- **AWS Amplify** - 프론트엔드 호스팅

### Monitoring & Notification
- **Discord Webhooks** - 실시간 알림
- **Slack Webhooks** - 팀 협업 알림
- **Amazon CloudWatch** - 로그 및 메트릭

### Development
- **Python 3.13** - Lambda 함수 개발
- **React** - DeployLand App
- **Nest.js** - Test 애플리케이션 

---
