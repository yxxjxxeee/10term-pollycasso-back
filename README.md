# Pollycasso

> 실시간 멀티플레이어 패션 드로잉 게임 플랫폼

폴리카소(Pollycasso)는 주어진 콘셉트에 맞춰 옷을 그리고, 다른 플레이어의 평가로 승패를 결정하는 실시간 멀티플레이어 게임입니다.<br/>
게임방과 실시간 채팅, 친구·차단 등의 소셜 기능을 제공하며, 게임 보상으로 획득한 코인과 경험치를 통해 캐릭터를 성장시키고 꾸밀 수 있습니다.

## 팀원

<table>
  <tr>
    <td align="center" width="200px">
      <a href="https://github.com/yxxjxxeee">
        <img src="https://github.com/yxxjxxeee.png" width="120px" alt="윤지은" />
      </a>
    </td>
    <td align="center" width="200px">
      <a href="https://github.com/dlehdhun">
        <img src="https://github.com/dlehdhun.png" width="120px" alt="이동훈" />
      </a>
    </td>
  </tr>
  <tr>
    <td align="center">
      <b>윤지은</b><br/>
      <a href="https://github.com/yxxjxxeee">@yxxjxxeee</a>
    </td>
    <td align="center">
      <b>이동훈</b><br/>
      <a href="https://github.com/dlehdhun">@dlehdhun</a>
    </td>
  </tr>
</table>

## 주요 기능

### 1. 회원가입 및 사용자 인증

일반 회원가입과 로그인뿐만 아니라 Google·Kakao 소셜 로그인을 지원해요.<br/>
Access Token과 Refresh Token을 이용해 사용자 인증을 관리하고, 토큰 재발급과 로그아웃 기능을 제공해요.

### 2. 게임방 생성 및 실시간 대기실

공개방과 비밀번호가 설정된 비공개방을 만들고, 개인전 또는 팀전으로 게임을 진행할 수 있어요.<br/>
대기실에서는 준비 상태, 소속 팀, 캐릭터 의상과 게임 설정을 실시간으로 공유해요.<br/>
방장은 플레이어 강퇴, 알림 보내기, 게임 시작 등의 기능을 사용할 수 있어요.

### 3. 실시간 패션 드로잉 게임

Socket.IO를 이용해 주제 선정부터 그림 데이터 전송, 작품 제출, 평가와 결과 발표까지 게임 진행 상황을 실시간으로 동기화해요.<br/>
Redis에서 게임 단계와 참가자 상태를 관리해 여러 플레이어가 동일한 게임 상태를 유지할 수 있어요.

### 4. 작품 평가 및 게임 보상

다른 플레이어가 제출한 작품을 점수로 평가하고, 평가 결과를 바탕으로 승패를 결정해요.<br/>
자신의 작품은 평가할 수 없으며, 게임 결과에 따라 경험치와 코인을 획득하고 레벨을 성장시킬 수 있어요.

### 5. 실시간 채팅 및 소셜

로비 채팅과 친구 간 실시간 메시지를 지원해요.<br/>
닉네임과 사용자 태그로 다른 플레이어를 검색하고 친구 요청, 수락, 삭제 및 사용자 차단 기능을 사용할 수 있어요.<br/>
Redis를 통해 친구의 온라인·오프라인 상태도 실시간으로 확인할 수 있어요.

### 6. 상점 및 게임 아이템

획득한 코인으로 캐릭터 코스메틱과 게임에서 사용할 수 있는 소비성 아이템을 구매할 수 있어요.<br/>
게임 아이템은 사용 가능한 단계와 재사용 대기시간 등의 조건에 따라 적용돼요.

### 7. 옷장 및 캐릭터 커스터마이징

구매한 모자, 상의, 하의, 신발, 액세서리와 이펙트 등을 확인하고 캐릭터에 장착할 수 있어요.<br/>
저장한 코디는 대기실과 게임에서 다른 플레이어에게 실시간으로 반영돼요.

### 8. 랭킹 및 전적

점수와 보유 코인을 기준으로 일간·주간·월간 랭킹을 제공해요.<br/>
게임 결과와 작품, 평가 기록을 저장해 플레이어의 성장과 게임 전적을 관리해요.

## 기술 스택
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Socket.IO](https://img.shields.io/badge/Socket.IO-010101?style=for-the-badge&logo=socketdotio&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Traefik](https://img.shields.io/badge/Traefik-24A1C1?style=for-the-badge&logo=traefikproxy&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

## 시스템 아키텍처

- 요청 흐름: `Client` → `Traefik (Reverse Proxy / TLS)` → `NestJS` → `AWS RDS (PostgreSQL)`
- 실시간 통신: `Client` ↔ `NestJS (Socket.IO)`
- 상태 관리: `NestJS` ↔ `Redis (Game / Waiting Room / Presence State)`
- 실행 환경: AWS EC2에서 Docker Compose로 Traefik·NestJS·Redis 컨테이너 운영
- 배포 흐름: `GitHub` → `GitHub Actions` → `Docker Hub` → `EC2 Self-hosted Runner` → `Docker Compose`
- API 문서: Swagger 기반 REST API 문서 제공

<img width="2106" height="1172" alt="pollycasso" src="https://github.com/user-attachments/assets/3af97fd6-db50-4d3c-8f3a-a42471bc7431" />
