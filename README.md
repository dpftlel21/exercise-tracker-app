<center><img width="250px" src="public/images/Beenzinoo.png"></center>

## Project. Exercise Tracker

**개발기간 : 2023.7.17 ~ 2023.08.09**

- **[Figma Link](https://www.figma.com/file/ZB9OIXLqpcUhWNcic0Q0q3/exercise-tracker-app?type=design&node-id=0%3A1&mode=design&t=T2uuBCz2Ned8Xngp-1)**
- **[배포 사이트](https://dpftlel21.github.io/exercise-tracker-app/)**

### 동작 화면

<img src = "public/images/movie.gif">

---

## ✔️ 기획

#### 지도 API를 활용하여 개인화된 주변 헬스장 추천 서비스를 제공하고, 효과적인 운동 루틴 기록 및 관리 기능을 통해 사용자들에게 효율적이고 맞춤형 운동 경험을 제공하고자 기획

---

## ✔️ 설계

#### - Figma를 활용하여 초기 화면 설계

#### - 컴포넌트 기반의 재사용성, 뛰어난 성능 및 커뮤니티 지원을 고려하여 React 프레임워크 선택

#### - 컴포넌트 간의 데이터 공유와 효율적인 전역 상태 관리 및 데이터의 일관성을 유지하기 위해 Redux 선택

---

## ✔️ 주요 기능

### 운동 루틴 작성

- 💪 일주일에 맞춰 7가지 운동 루틴 기록이 가능하도록 구현
  - 루틴 데이터를 로컬 스토리지에 저장
- 💪 푸터와 캘린더에 연동
  - 푸터에 경우, 화면전환이 되어도 루틴에 접근이 가능
  - 캘린더에 경우, 루틴 데이터에 개수만큼 날짜별로 반복해서 출력이 가능

### 운동 기록

- 💪 약 200개 이상의 운동 목록들을 출력
  - 해당 운동을 편리하게 선택이 가능
- 💪 원하는 날짜 별도로 설정이 가능
  - 운동 데이터는 로컬 스토리지에 저장

### 주변 헬스장

- 💪 사용자에 현재 위치를 반영해서 지도에 반영
- 💪 지역명 + 헬스장 입력 시 추천
  - 원하는 결과를 클릭 시 해당 상세 사이트 **(카카오맵)** 로 이동

### 로그인 / 로그아웃

- 💪 소셜 로그인 기능 구현
  - 카카오, 구글 API를 이용
- 💪 유저 정보 저장
  - API에서 받아온 데이터 **(유저 이름)** 세션 스토리지에 저장 후 화면에 반영
- 💪 로그아웃 클릭 시 로그인 된 유저정보를 초기화 후 초기 화면으로 이동

### 캘린더

- 💪 해당 날짜에 운동한 기록을 볼 수 있도록 날짜 선택 가능
- 💪 현재 날짜와 운동이 기록된 날짜 각각 표시

### 타이머 / 스톱워치

- 💪 원하는 시간을 설정하면 타이머 작동
- 💪 스톱워치 사용 시 소수점 둘째 자리까지 보이도록 구현

### 회원정보

- 💪 회원 신체정보 (성별, 나이, 키, 체중) 입력 후 저장
  - 저장된 정보는 이후에도 확인이 가능

---

## ✔️ **Stack**

### - **Environment**

<img src="https://img.shields.io/badge/visual studio code-007ACC?style=flat&logo=visualstudiocode&logoColor=white"/> <img src="https://img.shields.io/badge/git-F05032?style=flat&logo=git&logoColor=white"/> <img src="https://img.shields.io/badge/git hub-181717?style=flat&logo=github&logoColor=white"/>

### - **Config**

<img src="https://img.shields.io/badge/npm-CB3837?style=flat&logo=npm&logoColor=white"/> <img src="https://img.shields.io/badge/kakaotalk-FFCD00?style=flat&logo=kakaotalk&logoColor=white"/> <img src="https://img.shields.io/badge/google-4285F4?style=flat&logo=google&logoColor=white"/> <img src="https://img.shields.io/badge/kakaomap-FFCD00?style=flat&logo=kakao&logoColor=white"/> <img src="https://img.shields.io/badge/.env-ECD53F?style=flat&logo=dotenv&logoColor=white"/>

### - **Development**

<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=JavaScript&logoColor=white"/> <img src="https://img.shields.io/badge/React-61DAFB?style=flat&logo=React&logoColor=white"/> <img src="https://img.shields.io/badge/Tailwind CSS-06B6D4?style=flat&logo=Tailwind CSS&logoColor=white"/> <img src="https://img.shields.io/badge/styledcomponents-DB7093?style=flat&logo=styledcomponents&logoColor=white"/> <img src="https://img.shields.io/badge/Redux-764ABC?style=flat&logo=redux&logoColor=white"/> <img src="https://img.shields.io/badge/react router-CA4245?style=flat&logo=reactrouter&logoColor=white"/> <img src="https://img.shields.io/badge/axios-5A29E4?style=flat&logo=axios&logoColor=white"/>

---

## ✔️ User Flow

<img src="public/images/빈진우 User Flow.png">

---

## 👥 역할

#### 1. Google 및 Kakao API를 활용하여 OAuth 로그인 구현, 로그인 시 로컬 스토리지를 활용하여 유저 정보 저장, 로그아웃 시 저장된 정보를 초기화하는 기능을 구현

#### 2. Redux로 사용자 신체 정보를 입력하고 저장하는 기능 구현

#### 3. useState, setInterval, Math.floor 등을 활용하여 타이머와 스톱워치 기능 구현

#### 4. 카카오 맵 API를 활용하여 사용자의 현재 위치를 geolocation 함수로 받아오고, 주변 헬스장을 검색하여 지도에 표시하는 기능 구현

#### 5. env 파일을 생성해 중요 정보 노출 최소화하도록 생성하고 dotenv 라이브러리를 사용해 적용

#### 6. Git Action으로 자동 배포를 구현하여 소스 코드의 변경 시 자동으로 최신 버전을 서비스에 반영

---

## 📝 문제 발생 및 해결

### <span style="color:#90caf9">1. 카카오 지도 API </span>

#### ✔️ API 숨김

카카오 맵 API를 받아오고 , 띄우는 것을 성공했다. 하지만 API키는 공개되면 안되기에 처음에는 팀원들과 컴포넌트도 만들어 보고, 변수로 할당도 해보고 했으나 작동하지 않았다.

그러던 중 API 키 숨기는 방법에 대해 구글링을 하게 되었고, [참고자료 - API 키 숨기기](https://velog.io/@edie_ko/React-%ED%99%98%EA%B2%BD%EB%B3%80%EC%88%98-%EC%82%AC%EC%9A%A9%ED%95%98%EC%97%AC-API-key-%EC%88%A8%EA%B8%B0%EA%B8%B0.env-%EC%9D%B4%EC%9A%A9)를 접하게 되었다.

dotenv를 사용하여 API 키를 숨길 수 있는데 npm install dotenv를 우선적으로 터미널에 입력하여 다운을 받고, `.env` 파일을 최상위 위치에 만들었다. API 키는 깃에 올라가면 안되기에 `.gitignore`에 `.env`를 추가하여 github에 안 올라가게 설정했다.

그 뒤 env 파일에 API키를 적어주면 되는데, 반드시 `REACT_APP_`으로 시작해야 한다. 그 뒤 jsx나 js에서는 `process.env.REACT_APP_이름` 변수명을 사용해서 넣어준다. HTML에서는 API 키 입력란에 `%REACT_APP_이름%`을 넣어주면 된다.

우리는 HTML에 적용하기로 했고, 후자의 방법을 이용하여 원하고자 하는 결과를 잘 도출할 수 있었다.

#### ✔️ 현재 위치를 불러오는 과정에서 발생한 UseEffect 에러

지도를 켰을 때 사용자의 현재 위치가 바로 반영되도록 하기 위해 Geolocation API를 사용하여 위도와 경도 즉, latitude, longitude 각각의 값을 상태변경 해준 후 option 값에 넣었으나 작동하지는 않았다.

useEffect 의존성 배열에 latitude, longitude 값을 넣어주어야 사용자의 위치값을 받아온 후 상태가 변경된 latitude, longitude가 적용된다는 것을 알았고, 실제 지도에 사용자의 위치가 표시되며 제대로 작동하는 것을 확인했다.

### <span style="color:#90caf9">2. 운동 목록 API (공공 데이터 포털) </span>

한국건강증진개발원의 운동 목록을 받아와 이 데이터를 화면에 나타날 수 있게끔 하는 작업이었다.

받아온 데이터가 data라는 껍데기로 감싸져있는 형태라 return문 안에 단순히 Exercise를 map 메소드를 통해 화면에 띄울 때 에러가 발생했다. 이를 ExerciseData.data 로 문제를 해결했다.

### <span style="color:#90caf9">3. 카카오, 구글 간편 로그인</span>

Rest API 키와 Rest API URI 를 받아왔고, .env 파일에 입력 후 컴포넌트에서 호출하고 버튼에 onClick 이벤트를 실행시켜 버튼 클릭 시 간편 로그인이 진행 되도록 했으나 KOE001 오류 발생

뭐지??? 해서 구글링을 했으나 답을 찾지 못했다.. 콘솔창에는 401 (unauthorized) 오류라고 나와 있었는데 이건 또 뭐지 ??? 하다가 [401 에러 해결 참고자료](https://velog.io/@spig0126/HTTP-401Unauthorized-error%EC%97%90-%EB%94%B0%EB%A5%B8-%ED%95%B4%EA%B2%B0%EC%B1%85)를 접하게 되었다.

여기서 환경 변수가 잘못되었음을 인지하게 되었고, env파일의 위치가 잘못 되었다... env 파일의 기본 위치는 root 디렉토리인데, 나는 src 폴더 안에 넣어서 작동이 안된 것이었다..

즉, env 파일은 root 위치가 아니면 동작하지 않는다. 따라서 root위치로 이동 시킨 후 저장하고 재시작 하니 정상적으로 실행 되었다 !!

> - KOE001 오류 : 잘못된 형식의 요청, 해결 방법: 요청에 포함된 파라미터를 확인한 후 재요청하기 !
> - 401(unauthorized) 오류 : 클라이언트 오류 상태 응답 코드는 해당 리소스에 유효한 인증 자격 증명이 없기 때문에 요청이 적용되지 않았음

### <span style="color:#90caf9">4. Git</span>

#### ✔️ git 에 .env 파일 올라감

개발을 하는데 있어서 .gitignore 파일에 .env 파일을 등록하여 git에 안 올라가게 하는 것이 보안 측면에 있어서 매우 중요하다. 하지만 .gitignore 파일에 .env를 적어놨음에도 불구하고, git에 올라가는 트러블이 발생했다.

이유가 뭘까 찾아보니 .gitignore 파일을 처음에 만들기 전에 이미 .env로 푸시한 상황이라 발생한 것이었다...

다음과 같이 해결할 수 있었다.

1. git에서 .env 파일 삭제

2. .gitignore에서 .env 코드 삭제

3. 커밋 및 푸시 (원격 저장소에 .env 사라짐)

4. 지운 .env 파일 되살리기

5. .gitignore에 .env 코드 추가

### <span style="color:#90caf9">5. 로컬스토리지 저장된 유저 정보</span>

#### ✔️ 로컬스토리지 저장된 유저 정보 받아오기 에러

우선적으로 마이인포 모달창을 열었을 때 유저의 신체정보를 입력하고 저장하면 그 정보가 유지되게끔 기능구현을 했어야했다.

1. 로컬스토리지에 `localStorage.getItem("key")`를 이용하여 성별, 나이, 키, 몸무게를 저장했다.

2. 저장 후 이 저장된 데이터를 이용하여 saveInfo 함수를 이용한 저장하기 버튼을 구현하였고, 버튼 클릭시 로컬스토리지에 저장되는 것 까지 확인했다.

3. 이 로컬스토리지에 저장된 데이터를 화면에 나타내기 위해 성별, 나이, 키, 몸무게가 적힌 value 값에 로컬스토리지 데이터 (localAge, localWeight ... 등)를 넣고 실행시켰을 때 전혀 작동하지 않았다.

   - 현재 코드에서 로컬스토리지에 저장된 값을 화면에 표시하지 않고, 값을 변경할 때에도 초기값만 보여주는 문제 발생

해결방법을 고민하던 중 처음 useState 초기값을 빈 문자열로 설정했는데, `const [gender, setGender] = useState(localGender || "");` 과 같이 로컬스토리지에 저장된 값을 넣어주니 제대로 작동했다.

위와 같이 수정하면 초기값으로 로컬스토리지의 값을 사용하며, 입력 값이 변경되면 해당 상태를 업데이트하여 제대로 반영되는 것을 확인할 수 있었다.

---
