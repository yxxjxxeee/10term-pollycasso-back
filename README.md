# Pollycasso Backend

개발 기간: 2025.09 ~ 2025.12

폴리카소(Pollycasso)는 실시간 멀티플레이어 패션 드로잉 게임 플랫폼입니다.<br/>
주어진 컨셉에 맞는 옷을 그리고, 다른 플레이어들의 별점으로 승패가 결정됩니다.<br/>
친구 추가 / 차단, 실시간 채팅 등 소셜 기능을 갖추고 있으며,<br/>
레벨 / 경험치 / 코인 시스템과 상점에서 구매한 코스메틱 아이템으로 나만의 캐릭터를 커스터마이징할 수 있습니다.

## Tech Stack

![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Socket.IO](https://img.shields.io/badge/Socket.IO-010101?style=for-the-badge&logo=socket.io&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black)

## System Architecture

<img width="3251" height="1169" alt="image" src="https://github.com/user-attachments/assets/215cccee-6c5b-4597-96af-5c8fbca8ac0a" />

- 요청 흐름: `Client` → `Traefik (Reverse Proxy / TLS)` → `NestJS` → `RDS (PostgreSQL)`
- 실시간 게임: `Client` ↔ `NestJS (Socket.IO WebSocket)`
- 실시간 상태: `NestJS` ↔ `Redis (Game State / Session Management)`
- 배포: `GitHub` → `GitHub Actions` → `DockerHub` → `EC2 Self-hosted Runner` → `Docker Compose`

## ERD
<img width="2973" height="1483" alt="폴리카소 (pollycasso)" src="https://github.com/user-attachments/assets/7c5c402e-946f-4045-8bee-36842746959c" />

## 멤버

<table>
  <tr>
    <td align="center" width="200px">
      <img src="https://github.com/yxxjxxeee.png" width="120px" /><br/>
      윤지은<br/>
      <b>yxxjxxeee</b><br/>
      <a href="https://github.com/yxxjxxeee">@yxxjxxeee</a>
    </td>
    <td align="center" width="200px">
      <img src="https://github.com/dlehdhun.png" width="120px" /><br/>
      이동훈<br/>
      <b>dlehdgns</b><br/>
      <a href="https://github.com/dlehdhun">@dlehdhun</a>
    </td>
  </tr>
</table>
