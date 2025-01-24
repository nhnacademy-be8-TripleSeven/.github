# 📚 NHN24 Bookstore

> **클라우드 기반 Spring Boot 웹 도서 쇼핑몰 서비스**

![Build](https://img.shields.io/badge/Build-Passing-brightgreen?style=flat-square)
![Coverage](https://img.shields.io/badge/Coverage-80%25-blue?style=flat-square)
![Version](https://img.shields.io/badge/Version-1.0.0-orange?style=flat-square)

---
### 📖 도메인
www.nhn24.store/frontend/main

---

## 🧑‍🤝‍🧑 팀원

<table align="center" style="border-collapse: collapse; margin: 20px auto; background: #f9f9f9; border-radius: 15px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
    <tr>
        <td align="center" style="padding: 20px;">
            <a href="https://github.com/janghyunsung2" style="text-decoration: none; color: #333;">
                <img src="https://github.com/Janghyunsung2.png" width="120px" style="border-radius: 50%; border: 3px solid #ddd;" alt="장현성"/><br/>
                <sub><b style="font-size: 14px;">장현성</b></sub>
            </a>
        </td>
        <td align="center" style="padding: 20px;">
            <a href="https://github.com/WillgoNAVER" style="text-decoration: none; color: #333;">
                <img src="https://github.com/WillgoNAVER.png" width="120px" style="border-radius: 50%; border: 3px solid #ddd;" alt="김기현"/><br/>
                <sub><b style="font-size: 14px;">김기현</b></sub>
            </a>
        </td>
        <td align="center" style="padding: 20px;">
            <a href="https://github.com/wjpark4430" style="text-decoration: none; color: #333;">
                <img src="https://github.com/wjpark4430.png" width="120px" style="border-radius: 50%; border: 3px solid #ddd;" alt="박우진"/><br/>
                <sub><b style="font-size: 14px;">박우진</b></sub>
            </a>
        </td>
        <td align="center" style="padding: 20px;">
            <a href="https://github.com/lushlife99" style="text-decoration: none; color: #333;">
                <img src="https://github.com/lushlife99.png" width="120px" style="border-radius: 50%; border: 3px solid #ddd;" alt="정찬"/><br/>
                <sub><b style="font-size: 14px;">정찬</b></sub>
            </a>
        </td>
        <td align="center" style="padding: 20px;">
            <a href="https://github.com/milkymarky" style="text-decoration: none; color: #333;">
                <img src="https://github.com/milkymarky.png" width="120px" style="border-radius: 50%; border: 3px solid #ddd;" alt="최은화"/><br/>
                <sub><b style="font-size: 14px;">최은화</b></sub>
            </a>
        </td>
        <td align="center" style="padding: 20px;">
            <a href="https://github.com/JeongHoeSoek" style="text-decoration: none; color: #333;">
                <img src="https://github.com/JeongHoeSoek.png" width="120px" style="border-radius: 50%; border: 3px solid #ddd;" alt="정회석"/><br/>
                <sub><b style="font-size: 14px;">정회석</b></sub>
            </a>
        </td>
        <td align="center" style="padding: 20px;">
            <a href="https://github.com/jmg5642" style="text-decoration: none; color: #333;">
                <img src="https://github.com/jmg5642.png" width="120px" style="border-radius: 50%; border: 3px solid #ddd;" alt="조문기"/><br/>
                <sub><b style="font-size: 14px;">조문기</b></sub>
            </a>
        </td>
    </tr>
</table>





---

## 🛠️ Service Introduce

> - **NHN24 Bookstore**는 클라우드 환경을 적용한 도서 쇼핑몰 웹 애플리케이션입니다.
>  
> - 주요 기능:
>    - **회원 관리**: 회원가입, 로그인, 권한 설정
>    - **도서 검색 및 관리**: 도서 등록, 검색, 분류, 리뷰
>    - **주문 및 결제**: 장바구니, 주문 생성 및 상태 확인
>    - **포인트 및 쿠폰**: 적립, 쿠폰 관리 및 적용

---

## 🌐 System Architecture
![아키텍쳐_new](https://github.com/user-attachments/assets/4c989462-fb1b-4137-96d5-16d9b0bb7f51)

> - **Backend**: Spring Boot, JPA, QueryDSL
> - **Frontend**: JavaScript, Theamleaf
> - **Database**: MySQL, Redis
> - **CI/CD**: GitHub Actions

---

## 🚀 CI/CD
![cicd](https://github.com/user-attachments/assets/169fb1d3-deca-45a7-913e-3cfee1c122f7)
> - **GitHub Actions**: 코드 테스트 및 빌드 자동화
Github을 통해 코드베이스를 관리하며 기본적으로 Github Action을 통한 CI를 진행하여 빌드하고 테스트가 진행되어 성공 시 통합과정이 이뤄진다.
> * Git Flow 전략 중에서 크게 Main(Master), Develop, Feature 브랜치 이렇게 3개로 나누어 개발을 진행하였다.
> * 모든 서버는 Git Action을 사용하여 배포를 하고 있다.
> * Develop 브랜치에 통합을 진행할 시에 Sonarqube를 통해서 정적 분석이 이뤄진다.
> * Maven Verify 와 Sonarqube를 통해 Test Coverage를 저장한다
> * 통합 과정이 진행된 이후 이상이 없을 시 Main 브랜치에 통합을 하여 NHN Clound 인스턴스에 배포한다.
> * NHN Cloud의 SKM 를 사용하여 만든 P12 파일을 Git 서버에 올려 Github 환경설정을 등록해두었다.
> * Docker Build 시 DockerFile을 통해서 Jar 파일 빌드 및 패키징, 실행하는 이미지를 생성한다.
> * Deploy 과정 시 인스터스 내의 도커에 이중화를 진행하였다.
> * 매 생성 시마다 새로운 이미지를 생성해놓기 때문에 배포 시마다 3일 이상 경과한 이미지를 정리해준다.

---

## 🗓️ WBS & Kanban Board
### Gantt Chart
<img width="860" alt="roadmap" src="https://github.com/user-attachments/assets/7a53f57f-1eb1-4aa1-a24b-b81799c640d3" />


### Kanban Board
![kanban](https://github.com/user-attachments/assets/22e857c7-43fa-41c9-bdbe-9bfb0567d12e)
---

# 🧪 Test Coverage
- **SonarQube**: 코드 품질 검사
- 테스트 커버리지: 80% 이상
### 📕 book-coupon-api
![스크린샷 2025-01-23 오후 5 24 20](https://github.com/user-attachments/assets/6a6f4ce8-b79e-4d99-92fe-84746175058c)
### 🔑 auth-api
![auth](https://github.com/user-attachments/assets/d439fc88-0670-4061-9d3a-5eb95459f1b1)
### 👤 member-api
![member](https://github.com/user-attachments/assets/b5b2564a-5ff5-455d-aa4d-33bb0fc85fa9)

### 🛒 order-api
![order](https://github.com/user-attachments/assets/5a7292ea-1a99-48f9-bd9c-122b2f61551c)

---
## ERD
![통합 ERD](https://github.com/user-attachments/assets/c3fd9b8c-8847-48fb-b4ae-f6b3cf4287a3)

---

# 📖 주요 기능

### 🏗️ 인프라
* 담당자: 정찬, 박우진
- NHN CLOUD 기반 배포
- Docker를 활용한 컨테이너화
- Nginx를 활용한 로드 밸런싱 및 리버스 프록시 설정

### 🖥️ 프론트(figma ,html, css)
* 담당자: 최은화
* 피그마 및 html,css 구현

### 📮 주소
* 담당자: 최은화
* 주소 CRUD 구현
* 주소 등록 페이지 구현

### 👤 도서 제작자
* 담당자: 장현성
* 도서 제작자 CRUD 구현

### 📖 도서
* 담당자: 장현성
* 도서 관리자 페이지 구현
* 도서 CRUD 구현
* 출판사 CRUD 구현
* 정렬(최신순, 제목순, 가격순)

### 🔍 검색(Elastic Search)
* 담당자: 장현성
* 가중치 적용(제목, 작가, 출판사)
* 동의어 및 유의어 검색 적용

### ☑️ 카테고리
* 담당자: 장현성
* 카테고리 관리자 페이지 구현
* 카테고리 CRUD 구현
* 카테고리 계층구조 구현

### 🛒 장바구니
* 담당자: 정찬
* 장바구니 CRUD구현
* 장바구니 영구저장 구현

### 🎟️ 쿠폰
* 담당자: 정회석
* 쿠폰 관리자 페이지 구현
* 쿠폰정책 CRUD 구현
* 쿠폰 CRUD 구현
* 생일, 회원가입 시 쿠폰 자동생성(schedule) 기능 구현
* RabbitMQ 기반 선착순 쿠폰 자동 발급 기능 구현

### 👤 회원
* 담당자: 정찬, 최은화
* 회원 CURD
* 마이페이지 구현

### 📱 주문
* 담당자: 박우진
* 결제 완료 시 주문 내역 및 결재 내역, 저장 기능 구현(+ 트랜잭션 처리)
* 주문 내역 조회 기능 구현
* 주문 반품 및 취소 요청 구현
* 관리자 주문 상태 변경, 반품 처리 및 환불 기능 구현

### 🚚 배송
* 담당자: 박우진
* 스마트 배송 api를 통한 배송사 코드 및 국제 배송 여부 저장 기능 구현
* 배송 정책 추가, 수정 및 기본 배송비 정책 등록 기능 구현

### 💳 결제
* 담당자: 조문기
* 토스 api를 활용한 결제 구현
* 주문페이지,쿠폰적용 구현

### 💰 포인트
* 담당자: 박우진, 정회석
* 포인트 적립 및 사용 기능 구현
* 등급 별 포인트 적립, 기본 구매 적립 기능 구현
* 포인트 정책 추가, 수정 기능 구현
* 기본 포인트 정책 등록 기능 구현
* 포인트 조회기능 구현

### 📝 리뷰/ 도서 상세페이지
* 담당자: 김기현
* 리뷰/도서 상세페이지 구현
* 리뷰 CRUD 구현


### 🏷️ 태그
* 담당자: 김기현
* 태그 관리자 페이지 구현
* 태그 CRUD 구현

### ❤️ 좋아요
* 담당자: 김기현
* 좋아요 내역 페이지 구현
* 좋아요 CRUD 구현

---
## 📄 팀내 자료

JWT

🔍 Elastic
* 장현성
- https://7976-7976.tistory.com/19

Toss

🐰 RabbitMQ
* 박우진
- https://velog.io/@wjpark4430/RabbitMQ-정리
- https://www.notion.so/Order-API-17a9f62925e98068bc06e1ba3e58d1ae

🅽 Nginx
* 박우진
- https://www.notion.so/Nginx-Mac-Os-16c9f62925e98067821ef515b1ee7cf8
- https://www.notion.so/Nginx-16f9f62925e980568596e5a2ac661a93

---

## 🛠️ Stack

<div align="left" style="display: flex; flex-wrap: wrap; gap: 10px;">
    <img src="https://img.shields.io/badge/Apache_Maven-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white" alt="Apache Maven">
    <br>
    <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java">
    <img src="https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white" alt="Spring">
    <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot">
    <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
        <br>
    <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL">
    <img src="https://img.shields.io/badge/JPA-6DB33F?style=for-the-badge&logo=spring&logoColor=white" alt="JPA">
    <img src="https://img.shields.io/badge/QueryDSL-005E95?style=for-the-badge&logo=code&logoColor=white" alt="QueryDSL">
    <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Redis">
        <br>
    <img src="https://img.shields.io/badge/RabbitMQ-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white" alt="RabbitMQ">
    <img src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white" alt="JWT">
    <img src="https://img.shields.io/badge/SonarLint-4E9BCD?style=for-the-badge&logo=sonarsource&logoColor=white" alt="SonarLint">
    <img src="https://img.shields.io/badge/SonarQube-4E9BCD?style=for-the-badge&logo=sonarqube&logoColor=white" alt="SonarQube">
        <br>
    <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white" alt="GitHub Actions">
    <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white" alt="Nginx">
    <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux">
    <img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white" alt="Ubuntu">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
        <br>
    <img src="https://img.shields.io/badge/Elasticsearch-005571?style=for-the-badge&logo=elasticsearch&logoColor=white" alt="Elasticsearch">
    <img src="https://img.shields.io/badge/Logstash-005571?style=for-the-badge&logo=elastic&logoColor=white" alt="Logstash">
    <img src="https://img.shields.io/badge/Kibana-005571?style=for-the-badge&logo=kibana&logoColor=white" alt="Kibana">
</div>


---

## 📬 Contact
- GitHub Repository: [NHN24 Organization](https://github.com/nhnacademy-be8-TripleSeven)

