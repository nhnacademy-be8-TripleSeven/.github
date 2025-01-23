# 📚 NHN24 Bookstore

> **클라우드 기반 Spring Boot 웹 도서 쇼핑몰 서비스**

![Build](https://img.shields.io/badge/Build-Passing-brightgreen?style=flat-square)
![Coverage](https://img.shields.io/badge/Coverage-80%25-blue?style=flat-square)
![Version](https://img.shields.io/badge/Version-1.0.0-orange?style=flat-square)

---

## 👨‍👩‍👧‍👦 팀원

<table align="center">
    <tr>
        <td align="center" style="padding: 20px;">
            <a href="https://github.com/janghyunsung2">
                <img src="https://github.com/Janghyunsung2.png" width="120px;" style="border-radius: 50%;" alt="장현성"/><br/>
                <sub><b>장현성</b></sub>
            </a>
        </td>
        <td align="center" style="padding: 20px;">
            <a href="https://github.com/WillgoNAVER">
                <img src="https://github.com/WillgoNAVER.png" width="120px;" style="border-radius: 50%;" alt="김기현"/><br/>
                <sub><b>김기현</b></sub>
            </a>
        </td>
        <td align="center" style="padding: 20px;">
            <a href="https://github.com/wjpark4430">
                <img src="https://github.com/wjpark4430.png" width="120px;" style="border-radius: 50%;" alt="박우진"/><br/>
                <sub><b>박우진</b></sub>
            </a>
        </td>
        <td align="center" style="padding: 20px;">
            <a href="https://github.com/lushlife99">
                <img src="https://github.com/lushlife99.png" width="120px;" style="border-radius: 50%;" alt="정찬"/><br/>
                <sub><b>정찬</b></sub>
            </a>
        </td>
        <td align="center" style="padding: 20px;">
            <a href="https://github.com/milkymarky">
                <img src="https://github.com/milkymarky.png" width="120px;" style="border-radius: 50%;" alt="최은화"/><br/>
                <sub><b>최은화</b></sub>
            </a>
        </td>
        <td align="center" style="padding: 20px;">
            <a href="https://github.com/JeongHoeSoek">
                <img src="https://github.com/JeongHoeSoek.png" width="120px;" style="border-radius: 50%;" alt="정회석"/><br/>
                <sub><b>정회석</b></sub>
            </a>
        </td>
        <td align="center" style="padding: 20px;">
            <a href="https://github.com/jmg5642">
                <img src="https://github.com/jmg5642.png" width="120px;" style="border-radius: 50%;" alt="조문기"/><br/>
                <sub><b>조문기</b></sub>
            </a>
        </td>
    </tr>
</table>





---

## 🛠️ Service Introduce

- **NHN24 Bookstore**는 클라우드 환경을 적용한 도서 쇼핑몰 웹 애플리케이션입니다.
- 주요 기능:
  - **회원 관리**: 회원가입, 로그인, 권한 설정
  - **도서 검색 및 관리**: 도서 등록, 검색, 분류, 리뷰
  - **주문 및 결제**: 장바구니, 주문 생성 및 상태 확인
  - **포인트 및 쿠폰**: 적립, 쿠폰 관리 및 적용

---

## 🌐 System Architecture
![System Architecture](https://via.placeholder.com/800x400?text=System+Architecture+Diagram)

- **Backend**: Spring Boot, JPA, QueryDSL
- **Frontend**: JavaScript, Theamleaf
- **Database**: MySQL, Redis
- **CI/CD**: GitHub Actions

---

## 🚀 CI/CD
- **GitHub Actions**: 코드 테스트 및 빌드 자동화
Github을 통해 코드베이스를 관리하며 기본적으로 Github Action을 통한 CI를 진행하여 빌드하고 테스트가 진행되어 성공 시 통합과정이 이뤄진다.
- Git Flow 전략 중에서 크게 Main(Master), Develop, Feature 브랜치 이렇게 3개로 나누어 개발을 진행하였다.
- 모든 서버는 Git Action을 사용하여 배포를 하고 있다.
- Develop 브랜치에 통합을 진행할 시에 Sonarqube를 통해서 정적 분석이 이뤄진다.
- Maven Verify 와 Sonarqube를 통해 Test Coverage를 저장한다
- 통합 과정이 진행된 이후 이상이 없을 시 Main 브랜치에 통합을 하여 NHN Clound 인스턴스에 배포한다.
- NHN Cloud의 SKM 를 사용하여 만든 P12 파일을 Git 서버에 올려 Github 환경설정을 등록해두었다.
- Docker Build 시 DockerFile을 통해서 Jar 파일 빌드 및 패키징, 실행하는 이미지를 생성한다.
- Deploy 과정 시 인스터스 내의 도커에 이중화를 진행하였다.
- 매 생성 시마다 새로운 이미지를 생성해놓기 때문에 배포 시마다 3일 이상 경과한 이미지를 정리해준다.

---

## 🗓️ WBS & Kanban Board
### Gantt Chart
![Gantt Chart](https://via.placeholder.com/800x400?text=Gantt+Chart+Preview)

### Kanban Board
![Kanban Board](https://via.placeholder.com/800x400?text=Kanban+Board+Preview)

---

## 🧪 Test Coverage
- **SonarQube**: 코드 품질 검사
- 테스트 커버리지: 90% 이상

---

## 📖 주요 기능

### 🏗️ 인프라
* 담당자: 정찬, 박우진
- NHN CLOUD 기반 배포
- Docker를 활용한 컨테이너화
- Nginx를 활용한 로드 밸런싱 및 리버스 프록시 설정

### 주소
* 담당자: 최은화

### 저자
* 담당자: 장현성

### 도서
* 담당자: 장현성

### 카테고리
* 담당자: 장현성

### 장바구니
* 담당자: 정찬

### 쿠폰
* 담당자: 정회석

### 회원
* 담당자: 정찬, 최은화

### 주문
* 담당자: 박우진

### 결제
* 담당자: 조문기

### 포인트
* 담당자: 박우진

### 리뷰
* 담당자: 김기현

### 태그
* 담당자: 김기현

--
## 팀내 자료

JWT

Elastic

Toss

RabbitMQ
* 박우진
- https://velog.io/@wjpark4430/RabbitMQ-정리
- https://www.notion.so/Order-API-17a9f62925e98068bc06e1ba3e58d1ae

Nginx
* 박우진
- https://www.notion.so/Nginx-Mac-Os-16c9f62925e98067821ef515b1ee7cf8
- https://www.notion.so/Nginx-16f9f62925e980568596e5a2ac661a93


  
--

## 🛠️ Stack

<div align="center" style="display: flex; flex-wrap: wrap; gap: 10px;">
    <img src="https://img.shields.io/badge/Apache_Maven-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white" alt="Apache Maven">
    <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java">
    <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot">
    <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
    <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL">
    <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Redis">
    <img src="https://img.shields.io/badge/JPA-6DB33F?style=for-the-badge&logo=spring&logoColor=white" alt="JPA">
    <img src="https://img.shields.io/badge/Elasticsearch-005571?style=for-the-badge&logo=elasticsearch&logoColor=white" alt="Elasticsearch">
    <img src="https://img.shields.io/badge/SonarQube-4E9BCD?style=for-the-badge&logo=sonarqube&logoColor=white" alt="SonarQube">
    <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white" alt="Nginx">
</div>

---

## 📬 Contact
- GitHub Repository: [NHN24 Organization](https://github.com/nhn24)

