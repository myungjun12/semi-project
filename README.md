# Project Title

<!--배지-->
![MIT License][license-shield] ![Repository Size][repository-size-shield] ![Issue Closed][issue-closed-shield]

<!--프로젝트 대문 이미지-->
![Project Title](./img/spring_boot_thymeleaf_title.png)

<!--프로젝트 버튼-->
 [![Readme in English][readme-eng-shield]][readme-eng-url] [![View Demo][view-demo-shield]][view-demo-url] [![Report bug][report-bug-shield]][report-bug-url] [![Request feature][request-feature-shield]][request-feature-url]

<!--목차-->
# Table of Contents
- [[1] About the Project](#1-about-the-project)
  - [Features](#features)
  - [Technologies](#technologies)
- [[2] Getting Started](#2-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Configuration](#configuration)
- [[3] Usage](#3-usage)
- [[4] Contribution](#4-contribution)
- [[5] Acknowledgement](#5-acknowledgement)
- [[6] Contact](#6-contact)
- [[7] License](#7-license)



# [1] About the Project
*다음 내용을 고려하여 프로젝트에 대한 **전반적인 정보**를 적으세요.*

- ❗️짧은❗️ 도입부/제작 동기
- 웹툰 웹 서비스 개발 프로젝트 
- 일상 속에서 접근하기 쉬운 웹툰 웹 서비스

## Features
*강조하고 싶은 **주요 기능**이나 **차별성 있는 특징**을 적으세요.*
- 최고 멋진 **README**를 쉽게 작성할 수 있도록 *이텔릭체*로 된 **가이드**를 제공
- 뱃지로 **언어 옵션**을 제공

## Technologies
***언어, 프레임워크, 주요 라이브러리**를 **버전**과 함께 나열하세요.*

- [Maven](https://maven.apache.org/) 3.6.3
- [MySQL](https://www.mysql.com/) 8.0
- [Spring](https://spring.io/) 2.4.3



# [2] Getting Started
*만약 운영체제에 따라 프로그램을 다르게 동작시켜야한다면, 운영체제별로 동작 방법을 설명하세요*

Oracle SQL Developer 설치 password 설정 / 사용 폴더 cmd 진입 sqlplus as sysdba 입력 후 password 입력
CREATE USER kh_T IDENTIFIED BY kh1234; // DB 아이디와 비밀번호 생성
GRANT RESOURCE, CONNET TO kh_T; 테이블, DB연결 권한 부여 // DBA를 통해 모든 권한 부여할 수 있습니다. 
CREATE TABLE 테이블명 (테이블 컬럼 정보 값); 테이블 생성

Oracle 홈페이지 접속(www.oracle.com) → 하드웨어 및 소프트웨어 목록에 JAVA 클릭 → Java archive → 
Java SE Development Kit 11(자바 개발자 키트) - window 버전을 다운로드
시스템 환경 변수 편집에서 시스템변수의 path에 C:\Program Files\Java\jdk-11\bin 을 추가
cmd 에서 java –version 을 입력하여 버전 및 올바른 설치가 이루어졌는지 확인
이클립스 다운로드 페이지(https://www.eclipse.org/downloads/) 통해 Eclipse 설치하여 사용했습니다.

Eclipse 실행 후 Spring Starter Project 를 실행하고, 자바 라이브러리 추가 목록으로는 pom.xml 안에
Thymeleaf, Oracle Driver, JDBC API, Lombok, String Boot DevTools, MyBatis Framework, Spring Web 을 사용했습니다.
application.properties 에는 server.port=포트번호, Oracle DB 연결문, DB(아이디, 비밀번호), mybatis를 통해 Java와 xml(sql문) 코드를 연결했습니다. 
xml파일의 sql문은 <mapper namespace="com.kh.mapper.KHMapper"> @Mapper가 존재하는 파일을 통해 연결을 설정했습니다. 
<insert, select, update, delete id="" parameterType="com.kh.dto.DTO"> id 값은 Mapper.java 파일의 메서드명과 일치해야 올바르게 읽고 연결 할 수 있습니다.
DTO.java 파일은 DB에 존재하는 컬럼명과 일치하게 생성하여 parameterType을 통해 값을 읽어왔습니다.
Mapper.java 파일은 interface로 DTO 객체와 sql id값을 통해 구현해야 할 메서드를 생성합니다. 
Service.java 파일에서는 인터페이스를 구현하기 위해 @Service을 사용하며 Mapper 객체를 생성하고 객체를 통해서 메서드를 구현합니다.
사용한 Controller는 일반적인 컨트롤러로 return 값으로 사용자에게 보여 줄 .html 주소 값을 반환합니다.
@GetMapping 또는 @PostMapping을 통해 ("/url") 경로를 받아서 명령을 수행한 뒤 html 주소를 반환했습니다.

## Prerequisites
*프로젝트를 동작시키기 위해 필요한 소프트웨어와 라이브러리를 나열하고 어떻게 다운받을 수 있는지 설명하세요.*

- [OpenWeather API key](https://openweathermap.org/) (무료)
- npm
```bash
npm install npm@latest -g
```

## Installation
*어떻게 이 프로젝트의 소스코드를 다운받을 수 있는지 설명하세요.*
1. Repository 클론
```bash
git clone https://github.com/your-username/project-repository
```
2. NPM packages 설치
```bash
npm install
```

## Configuration
*코드의 어느 부분을 채우거나 수정해야하는지 설명하세요.*
- `config.js`에 Openweather API key를 입력
```bash
const API_KEY = "<Your API key>";
```



# [3] Usage
***스크린샷, 코드** 등을 통해 **사용 방법**과 **사용 예제**를 보여주세요. 사용 예제별로 h2 헤더로 나누어 설명할 수 있습니다.*

![usage](./img/spring_boot_diagram.png)

```java
// 몇 개의 API 사용 예제를 코드와 함께 보여주세요.
```



# [4] Contribution
기여해주신 모든 분들께 대단히 감사드립니다.[`contributing guide`][contribution-url]를 참고해주세요.
이 프로젝트의 기여하신 분들을 소개합니다! 🙆‍♀️
*이모티콘 쓰는 것을 좋아한다면, 버그 수정에 🐞, 아이디어 제공에 💡, 새로운 기능 구현에 ✨를 사용할 수 있습니다.*
- 🐞 [dev-ujin](https://github.com/): 메인페이지 버그 수정



# [5] Acknowledgement
***유사한 프로젝트의 레포지토리** 혹은 **블로그 포스트** 등 프로젝트 구현에 영감을 준 출처에 대해 링크를 나열하세요.*

- [Readme Template - Embedded Artistry](https://embeddedartistry.com/blog/2017/11/30/embedded-artistry-readme-template/)
- [How to write a kickass Readme - James.Scott](https://dev.to/scottydocs/how-to-write-a-kickass-readme-5af9)
- [Best-README-Template - othneildrew](https://github.com/othneildrew/Best-README-Template#prerequisites)
- [Img Shields](https://shields.io/)
- [Github Pages](https://pages.github.com/)



# [6] Contact
- 📧 본인이메일@gmail.com
- 📋 [https://www.github.com](https://www.github.io/contact)



# [7] License
MIT 라이센스
라이센스에 대한 정보는 [`LICENSE`][license-url]에 있습니다.



<!--Url for Badges-->
[license-shield]: https://img.shields.io/github/license/dev-ujin/readme-template?labelColor=D8D8D8&color=04B4AE
[repository-size-shield]: https://img.shields.io/github/repo-size/dev-ujin/readme-template?labelColor=D8D8D8&color=BE81F7
[issue-closed-shield]: https://img.shields.io/github/issues-closed/dev-ujin/readme-template?labelColor=D8D8D8&color=FE9A2E

<!--Url for Buttons-->
[readme-eng-shield]: https://img.shields.io/badge/-readme%20in%20english-2E2E2E?style=for-the-badge
[view-demo-shield]: https://img.shields.io/badge/-%F0%9F%98%8E%20view%20demo-F3F781?style=for-the-badge
[view-demo-url]: https://dev-ujin.github.io
[report-bug-shield]: https://img.shields.io/badge/-%F0%9F%90%9E%20report%20bug-F5A9A9?style=for-the-badge
[report-bug-url]: https://github.com/dev-ujin/readme-template/issues
[request-feature-shield]: https://img.shields.io/badge/-%E2%9C%A8%20request%20feature-A9D0F5?style=for-the-badge
[request-feature-url]: https://github.com/dev-ujin/readme-template/issues

<!--URLS-->
[license-url]: LICENSE.md
[contribution-url]: CONTRIBUTION.md
[readme-eng-url]: ../README.md



