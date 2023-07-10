# 📖 Installation

[Wiki.js](https://js.wiki/) 를 사용한 Teamcenter, Active Workspace KnowledgeBase 구축을 위한 개발 환경 세팅 가이드

## 📜 Installation Details

### Dependencies

[Wiki.js v2.5.299 - 변경될 수 있음](https://js.wiki/get-started)

#### Node.JS

홀수 버전 및 18은 지원 안함. 지원목록

- [Node.js v12.22.12](https://nodejs.org/download/release/v12.22.12/node-v12.22.12-x64.msi)
- [Node.js v14.21.3](https://nodejs.org/download/release/v14.21.3/node-v14.21.3-x64.msi)
- [Node.js v16.20.1](https://nodejs.org/download/release/v16.20.1/node-v16.20.1-x64.msi)

#### Database

- PostgreSQL 9.5 or later
  - [v9.5.25](https://sbp.enterprisedb.com/getfile.jsp?fileid=1257550)
  - [Latest Stable v15.3](https://sbp.enterprisedb.com/getfile.jsp?fileid=1258514)

사이트에서는 최신을 쓰면 좋다고 되어있으나 혹시 몰라 둘다 명시

## 🚀 Getting Started

[공식 문서 가이드](https://docs.requarks.io/install)

### Install Environment

[PostgreSQL 15.3](https://sbp.enterprisedb.com/getfile.jsp?fileid=1258514)

[Node.js v16.20.1](https://nodejs.org/download/release/v16.20.1/node-v16.20.1-x64.msi)

[Wiki.js v2.5.299 - 변경될 수 있음](https://js.wiki/get-started)

#### Step 1. Install DB Server

PostgreSQL 15.3 버전을 다운로드 한 뒤 설치

도중에 나오는 postgres 계정에 대한 비밀번호는 꼭 기억할것.

#### Step 2. Setting DB Environment

프로그렘 메뉴에서 SQL Shell (psql) 을 찾아서 실행한다음 암호 입력창이 나올때까지 Enter키 입력.

암호 입력창이 나올경우 설치할때 입력했던 암호 입력.

![image](https://github.com/Zeliper/TC_WIKI/assets/24862471/cb4c8e04-0ef9-48c4-88ff-80fb700c29f7)

위와 같이 정상적으로 postgres=# 이런식으로 접속이 된경우 아래 명령어를 통해 위키 DB 계정 생성

* 아래 SQL 명령들은 Wiki.js Configuration의 기본값을 기준으로 설명함.

* 세미콜론을 빼먹으면 정상적으로 실행되지 않음.

* '비밀번호'는 나중에 위키 Configuration 할때 사용할 비밀번호 사용.

```psql
CREATE USER wikijs WITH ENCRYPTED PASSWORD '비밀번호';
```

정상적으로 실행 된 경우 다음 명령을 통해 wiki Database 생성 및 권한 부여

```psql
CREATE DATABASE wiki;
GRANT ALL PRIVILEGES ON DATABASE wiki TO wikijs;
ALTER USER wikijs WITH SUPERUSER;
```

위 명령들에 문제가 없을경우 정상적으로 DB는 준비가 완료됨.
