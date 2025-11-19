
# 임규성
  

_SpringBoot를 주력기술로 백엔드에서 마주하는 다양한 문제해결을 통해 성장하는 중입니다._

<div align=left><h1>⚡ Core Tech Stack</h1></div>

<div align=left> 
  <br> <strong>🛠 Backend</strong> <br>
  <img src="https://img.shields.io/badge/spring boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white">
  <img src="https://img.shields.io/badge/spring security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white">
  <img src="https://img.shields.io/badge/spring data jpa-6DB33F?style=for-the-badge&logo=spring&logoColor=white">
  <img src="https://img.shields.io/badge/spring data redis-DC382D?style=for-the-badge&logo=redis&logoColor=white">

  <br> <strong>🧪 Testing</strong> <br>
  <img src="https://img.shields.io/badge/junit5-25A162?style=for-the-badge&logo=junit5&logoColor=white">
  <img src="https://img.shields.io/badge/mockito-FF9900?style=for-the-badge&logoColor=white">

  <br> <strong>☁️ Infra</strong> <br>
  <img src="https://img.shields.io/badge/docker-2496ED?style=for-the-badge&logo=docker&logoColor=white">
  <img src="https://img.shields.io/badge/aws ec2-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white">
  <img src="https://img.shields.io/badge/github actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white">
</div>

# Projects
### 1️⃣ 커뮤니티 서비스 덕후감(2025.10) [코드](https://github.com/sb5-team4/sb5-deokhugam-team4)
1) [알림 중복 문제 해결]  [링크](https://velog.io/@gyural/%EC%A2%8B%EC%95%84%EC%9A%94%EB%A5%BC-%EB%88%8C%EB%A0%80%EC%9D%84-%EB%BF%90%EC%9D%B8%EB%8D%B0-%EC%95%8C%EB%A6%BC-%ED%8F%AD%ED%83%84%EC%9D%B4-%EC%98%A8%EB%8B%A4%EA%B3%A0) 
<br/>기존 비지니스로직은 좋아요/취소 무한 반복시 알림이 무한으로 발생됐습니다. 이 문제를 해결하기위해 인메모리 캐시를 도입해, 알림 발송 권한 Lock을 통해 발송되게 리팩토링했습니다.

2) [좋아요/댓글 수 Count(*)쿼리 95% 성능 향상, 이후 사이드 이펙트인 동시성 문제 해결]
<br/> 기존에는 좋아요/댓글 수를 Count(*)쿼리로 가져와 대규모 데이터 환경에서 성능이 떨어졌습니다.
<br/> 이를 해결하기 위해 좋아요/댓글 수 필드를 추가하는 역정규화를 진행했고 쿼리 성능을 95% 향상시켰습니다.
<br/> 이후 대용량 트레픽 환경에서 좋아요/댓글 수 필드에 동시성 문제가 발생하는 사이드 이펙트가 발생했고, Optimistic Lock을 통해 해결했습니다.

### 2️⃣ 투자 지수 대시보드 서비스 Findex(2025.09) [코드](https://github.com/sb5-Findex-team7/sb5-Findex-team7)
1) [커서 페이지네이션 성능 30% 향상]
<br/>기존 오프셋 페이지네이션으로 페이지 깊이에 따른 응답속도가 저하되었습니다.
<br/> 이를 해결하기 위해 커서페이지네이션 리팩토링과 커서필드에 인덱스를 추가해 API 조회성능을 30% 향상시켰습니다.
2) [중복 외부 API 호출 해결]
<br/> 기존 비지니스로직은 사용자가 화면 클릭시마다 외부 API 호출하며 중복 I/O시간 발생, 요청당 150Row 중복 저장되는 문제가 있었습니다.
<br/> 중복 호출을 제거하고 캐싱을 도입해 요청당 150Row를 절감하고, 응답시간 90%를 단축했습니다.

### 3️⃣ (주)아너스 코리아 주차편의 모바일 앱(2025.01) [코드](https://github.com/Team-Devmon-IN-KU/HonorsParking-BE)
1) [동기화 서버 Bulk Insert 최적화]
<br/>스케줄러 기반 매 분 1000건 이상 데이터를 JPA로 처리해 성능이 떨어지는 것을 발견했습니다. 
<br/> 이를 해결하기 위해 JDBC 기반의 쿼리로 리팩토링해 BulkInsert를 적용해 처리속도를 90% 향상시켰습니다.
2) [Redis 알람 워커로 비동기 처리]
<br/>알람 발송 로직이 비지니스 로직 트랜잭션 내부에 위치해 알람 실패시에 전체가 롤백되는 꼬리효과가 발생했습니다.
<br/> 이를 해결하기 위해 푸쉬/알림톡을 추상화한 알람워커를 구현해 비동기처리하며 해결했습니다.

---

### Velog 최신 글 📝
![Velog GitHub stats](https://velog-github-badge.vercel.app/badge/gyural?theme=dark&posts=3)

#### Problem Solving
[![Solved.ac 프로필](https://mazassumnida.wtf/api/v2/generate_badge?boj=dla9319)](https://solved.ac/su1715)

---

# ETC
* <2025 코드잇 스프린트 스프링 백엔드 5기 중급 프로젝트 발표> - 1등 수상 🏆
* <2024 고려대학교 세종캠퍼스 컴퓨터융합 소프트웨어학과 학술제> - 2등 수상 🏆
* <2023 고려대학교 세종캠퍼스 컴퓨터융합 소프트웨어학과 학술제> - 3등 수상 🏆 
* <2023 세종 태크노파크 소프트웨어 클러스터 2.0 해커톤> - 1등 수상 🏆

