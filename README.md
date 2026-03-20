<div align="center">

# 🚕 TalleMalle Backend

### 실시간 위치 기반 동승 매칭 서비스 서버

<img width="300" alt="image" src="https://github.com/user-attachments/assets/3ae14639-49a6-415c-8407-bf0cb62fd85c" />

**안정적인 API 설계와 실시간 통신 기반의 동승 매칭 서버**

</div>

---

## 👥 Team TalleMalle

<table align="center" width="100%">
<tr>
<td align="center" width="20%">
  <a href="https://github.com/shinukang">
    <img src="https://github.com/shinukang.png" width="90"><br/>
    <strong>강신우</strong>
  </a>
</td>
<td align="center" width="20%">
  <a href="https://github.com/saralove20">
    <img src="https://github.com/saralove20.png" width="90"><br/>
    <strong>김사라</strong>
  </a>
</td>
<td align="center" width="20%">
  <a href="https://github.com/pbgodsoo">
    <img src="https://github.com/pbgodsoo.png" width="90"><br/>
    <strong>박범수</strong>
  </a>
</td>
<td align="center" width="20%">
  <a href="https://github.com/hijaehyuk">
    <img src="https://github.com/hijaehyuk.png" width="90"><br/>
    <strong>이재혁</strong>
  </a>
</td>
<td align="center" width="20%">
  <a href="https://github.com/DongHyunj">
    <img src="https://github.com/DongHyunj.png" width="90"><br/>
    <strong>정동현</strong>
  </a>
</td>
</tr>
</table>

---

## 🛠 기술 스택

### Backend

![Spring Boot](https://img.shields.io/badge/SpringBoot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/SpringSecurity-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)
![JPA](https://img.shields.io/badge/JPA-Hibernate-59666C?style=for-the-badge)
![JWT](https://img.shields.io/badge/JWT-Auth-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket-STOMP-00B894?style=for-the-badge)

### DBMS

![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white)

### Infra & Deployment

![AWS EC2](https://img.shields.io/badge/AWS%20EC2-red?style=for-the-badge&logo=amazonaws&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)

### Collaboration

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white)

---

# 🚀 프로젝트 소개

### 🔗 링크 바로가기

<table width="100%">
  <thead>
    <tr>
      <th width="33%" align="left">🌐 API Server</th>
      <th width="33%" align="left">📘 API Docs</th>
      <th width="33%" align="left">📏 Code Convention</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td valign="top">
        <p>
          <a href="https://api.bbsso.kro.kr:8080">
            <img src="https://img.shields.io/badge/API-Server-blue?style=for-the-badge&logo=springboot&logoColor=white">
          </a>
        </p>
      </td>
      <td valign="top">
        <p>
          <a href="https://docs.google.com/spreadsheets/d/1iabBDvrhTMOP8ass_cav91xfmSoGrhqvT-ViAemRS54/edit?usp=sharing">
            <img src="https://img.shields.io/badge/API-명세서-6DB33F?style=for-the-badge&logo=swagger&logoColor=white">
          </a>
        </p>
      </td>
      <td valign="top">
        <p>
          <a href="https://www.notion.so/2dfa4b6b459480e693d3f1e81cf9134a?source=copy_link">
            <img src="https://img.shields.io/badge/Code-Convention-111827?style=for-the-badge&logo=github&logoColor=white">
          </a>
        </p>
      </td>
    </tr>
  </tbody>
</table>

---

### 🎯 서버 한 줄 요약

**TalleMalle Backend는 위치 기반 동승 매칭 서비스를 위한 REST API와 실시간 채팅(WebSocket)을 제공하는 서버입니다.**

---

### 🧩 서버 설계 배경

- 사용자 인증 및 권한 관리 필요 (JWT 기반 인증)
- 동승 모집/참여 상태를 안정적으로 관리해야 함
- 실시간 채팅 기능을 위한 WebSocket 처리 필요
- 확장 가능한 구조의 API 설계 필요

➡️ 이를 위해 Spring Boot 기반의 계층형 아키텍처로 서버를 설계했습니다.

---

### ✨ 핵심 기능

| 기능 | 설명 |
|------|------|
| 🔐 인증/인가 | JWT 기반 로그인 및 사용자 인증 |
| 🚕 모집 관리 | 동승 모집 생성, 조회, 수정, 삭제 |
| 🤝 참여 관리 | 참여 요청, 승인, 상태 관리 |
| 💬 실시간 채팅 | STOMP 기반 WebSocket 채팅 |
| 🔔 알림 시스템 | 웹 푸시 기반 알림 처리 |
| 👤 사용자 관리 | 프로필, 마이페이지, 활동 내역 |

---

# 🧠 백엔드 구현 포인트

### 🔐 인증 & 보안

- Spring Security + JWT 기반 인증 처리  
- Filter를 통한 요청 단위 인증 처리  
- 사용자 권한(Role)에 따른 접근 제어  

---

### 🗂 계층형 아키텍처

- Controller - Service - Repository 구조  
- DTO를 활용한 요청/응답 분리  
- Entity 기반 JPA ORM 설계  

---

### 💬 실시간 채팅 처리

- STOMP 기반 WebSocket 통신  
- 채팅 읽음 처리 (ChatRead)  
- 채팅방 단위 메시지 관리  

---

### 🗄 데이터베이스 설계

- 사용자, 모집, 참여, 채팅 등 도메인별 테이블 분리  
- 연관관계 매핑 (OneToMany, ManyToOne)  
- 상태값 Enum 관리  

---

### 🔔 알림 시스템

- Web Push 기반 알림 처리  
- 사용자 구독 정보 저장 및 관리  
- 이벤트 기반 알림 전송  

---

### 🔄 서비스 흐름

- Flow 1) 회원가입 → 로그인 → 모집 조회 → 참여 요청 → 승인 → 채팅  
- Flow 2) 회원가입 → 로그인 → 모집 생성 → 참여자 모집 → 채팅  

---

# 🏗 서버 아키텍처

Client (Vue)

↓

Spring Boot (Controller)

↓

Service Layer (Business Logic)

↓

JPA Repository

↓

MariaDB

---

<div align="center">

# 🚕 Backend powered by TalleMalle

</div>

---
