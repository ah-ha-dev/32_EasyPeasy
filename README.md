# 📌 32_EasyPeasy (Team AH-HA)

## 🖐 Introduction
**다크 데이터**는 저장하고 있으나 내용 또는 가치가 확인되지 않는 데이터를 말합니다.

베리타스에 따르면 다크데이터때문에 2020년에 **약 580만톤**의 이산화탄소가 배출되었고, 이 배출량은 자동차로 지구를 무려 **575000바퀴** 돌았을 때와 동일하다고 합니다.  

손가락 하나만 까딱해서 다크데이터를 줄여 지구를 함께 지켜보시겠어요?

저희 **AH-HA** 팀은 우리의 일상 속에서 다크 데이터를 줄여 환경을 보호하고 이를 생활습관화할 수 있는 서비스, **EasyPeasy**를 제안합나다.

## 🔨 Tech Stack

|         Frontend         |         Backend (API)         |         
| :----------------------: | :---------------------------: | 
| ![Android](https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=Android&logoColor=white) ![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=Kotlin&logoColor=white) | ![Nestjs](https://img.shields.io/badge/nestjs-white?style=flat-square&logo=nestjs&color=E0234E) ![GoogleCloud](https://img.shields.io/badge/GoogleCloud-4285F4?style=flat-square&logo=GoogleCloud&logoColor=white) ![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazon-aws&logoColor=white) ![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=Firebase&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=Docker&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=MySQL&logoColor=white) ![AmazonDynamoDB](https://img.shields.io/badge/AmazonDynamoDB-4053D6?style=flat-square&logo=AmazonDynamoDB&logoColor=white) ![Sentry](https://img.shields.io/badge/Sentry-362D59?style=flat-square&logo=Sentry&logoColor=white)| 

<br>

# 💚 Frontend - Android

## 🔖 주요 기능
- 회원 가입
  - 구글 로그인
  - 내 캐릭터 생성
  - 캐릭터 이름 설정
- 홈
  - 메일함 관리
  - 캐릭터 히스토리
  - 내 캐릭터 변경
- 설정
  - 정보성 푸시 알림 설정
  - 이메일 삭제 알림 설정

## 💻 Android Tech Stack
- Kotlin
  - Standard Library
  - Coroutine
- Material Design
- Android Jetpack
  - LifeCycle (ViewModel, LiveData, LifeCycleObserver)
  - DataBinding
  - Jetpack Navigation Component
  - ViewPager2
- Glide
- Retrofit / OkHttp

## 🗂 Package

<br>

# 👻 Backend

## ✨ The technology we used
- Google OAuth2.0  
  사용자 인증 정보를 얻기 위해 사용하였습니다.
- Google Gmail API  
  사용자의 실시간 메일 개수를 얻기 위해 사용하였습니다.
- Google Cloud Platform PUB/SUB  
  사용자의 메일함에 이벤트가 있을 때마다, 비동기적으로 통신하여, 데이터를 수집하기 위해 사용하였습니다.
- Firebase Cloud Messaging  
  사용자에게 푸시 알람을 보내기 위해 사용하였습니다.
- DynamoDB  
  푸시 알람을 받는 사용자를 저장하기 위해 사용하였습니다. RDS만을 사용했을 때보다, 39%의 속도 향상을 얻었습니다. (더미 데이터 50000개 기준)
- Sentry / Slack  
  실시간 버그 트래킹을 위해 사용하였습니다.

## 🛠️ Dev Server
http://3.35.131.195/api/v1

## 📖 API Documentation
http://3.35.131.195/api/v1/docs/
 
## 🌱 Getting Started
`node: 14.16.0`  
`npm: 6.14.11`

### 1. Cloning
```
$ git clone https://github.com/ah-ha-dev/ah-ha-api-server.git
$ cd ah-ha-api-server
$ npm install
```

### 2. Setting dotenv at Root Directory
```
JWT_SECRET=<YOUR_JWT_SECRET>
GOOGLE_CLIENT_ID=<YOUR_GOOGLE_CLIENT_ID>
GOOGLE_CLIENT_SECRET=<YOUR_GOOGLE_CLIENT_SECRET>
GOOGLE_REDIRECT_URI=<YOUR_GOOGLE_REDIRECT_URI>
FIREBASE_PROJECT_ID=<YOUR_FIREBASE_PROJECT_ID>
FIREBASE_PRIVATE_KEY=<YOUR_FIREBASE_PRIVATE_KEY>
FIREBASE_CLIENT_EMAIL=<YOUR_FIREBASE_CLIENT_EMAIL>
GOOGLE_CREDENTIALS_TYPE=<YOUR_GOOGLE_CREDENTIALS_TYPE>
GOOGLE_CREDENTIALS_PRIVATE_KEY=<YOUR_GOOGLE_CREDENTIALS_PRIVATE_KEY>
GOOGLE_CREDENTIALS_CLIENT_EMAIL=<YOUR_GOOGLE_CREDENTIALS_CLIENT_EMAIL>
GOOGLE_CREDENTIALS_CLIEND_ID=<YOUR_GOOGLE_CREDENTIALS_CLIEND_ID>
GOOGLE_PROJECT_ID=<YOUR_GOOGLE_PROJECT_ID>
GOOGLE_PUBSUB_TOPIC_NAME=<YOUR_GOOGLE_PUBSUB_TOPIC_NAME>
GOOGLE_PUBSUB_SUBSCRIPTION_NAME=<YOUR_GOOGLE_PUBSUB_SUBSCRIPTION_NAME>
AWS_ACCESS_ID=<YOUR_AWS_ACCESS_ID>
AWS_SECRET_ACCESS_KEY=<YOUR_AWS_SECRET_ACCESS_KEY>
AWS_REGION=<YOUR_AWS_REGION>
SENTRY_DSN=<YOUR_SENTRY_DSN>
SLACK_WEBHOOK=<YOUR_SLACK_WEBHOOK>
```

### 3. Run the MySQL with Docker
```
$ docker-compose -f "docker-compose.yml" up -d --build                                   
```

### 4. Start Local Server
```
$ npm run start                         
```

## 🌸 About Server
### Server Architecture
![image](https://user-images.githubusercontent.com/66551410/152565647-551079d2-7643-4ac0-ba6e-28f02c7d96b9.png)

### CICD Architecture
![image](https://user-images.githubusercontent.com/66551410/152016992-cff6b052-35d7-416e-868c-b2702a3ef692.png)

### MySQL ERD
![image](https://user-images.githubusercontent.com/66551410/152563288-231e1ff3-1394-424e-8fe9-0a387324d730.png)

## 🌈 Contributors

| Sohee Lee | Heewon Kang | Hyuna Kim | Sunwoo Ho | 
| :----: | :----: | :----: |:----: 
| [@heehee.dsgn](https://www.instagram.com/heehee.dsgn/) | [@ymcho24](https://github.com/ymcho24) | [@akimcse](https://github.com/akimcse) | [@hocaron](https://github.com/hocaron) |
|Designer |Android |Android |Backend | 
