# 🍽️ Next.js 맛집 지도

<!-- ![image](https://github.com/SeoeunCho/react-twitter/blob/main/src/preview/react-twitter_preview.gif)

> 👉 [사이트 바로가기](https://react-twitter-nine.vercel.app/)<br />
> 작업 기간 : 7일

<br />

## 📋 Project

- 이 프로젝트는 React에서 Firebase와 Redux를 연습하며 익숙해지기 위해 제작한 반응형 앱입니다.<br />
  Firebase를 이용하여 데이터를 생성하고 사용자 인증에서 회원가입 및 로그인을 구축하고<br />
  CRUD를 구현하여 게시글 등록, 답글, 리트윗, 좋아요 등의 소셜 SNS 기능 및 실시간 업데이트와 알림목록을 생성했습니다.<br />
  Sass와 Media Query를 사용해 어떤 기기에도 모바일에 대응하는 반응형으로 작업했습니다.<br />
  전역 상태 라이브러리 Recoil로 메뉴명 다국어 처리 기능을 추가하고 Vercel로 배포했습니다.
  - Fastcampus에서 트위터 클론코딩을 수강하고 Kim-jaeoh의 nwitter를 참고하여 최대한 트위터앱과 비슷하게 구현했습니다.

<br /> -->

## 💡 학습

- 웹 구조 : Next.js SSR
- 스타일링 : 심화된 스택 사용을 위한 Tailwind
- 상태관리 : 전역 상태관리를 위한 Recoil + 캐싱을 위한 React-query
- 백엔드 관련 : 외부 API 연동(카카오 지도 & 위치 정보 가져오기)과 데이터 처리에 대한 경험(Prisma)
  - [ **Kakao map API** ](https://developers.kakao.com/)에서 앱 생성 후, Javascript 키 필요
  - [ **Supabase** ](https://supabase.com/)에서 프로젝트 세팅 필요
  - [ **Next-auth & Prisma** ](https://authjs.dev/reference/adapter/prisma)
    - [Prisma Adapter](https://authjs.dev/reference/adapter/prisma) 세팅 필요
    - [Middleware](https://next-auth.js.org/configuration/nextjs#middleware) 세팅 필요
    - [Google](https://console.developers.google.com/apis/credentials)에서 API키 생성필요
    - [Naver](https://developers.naver.com/main/)에서 오픈 API 이용 신청 및 서비스 URL에 로컬 호스트 추가 필요
    - [Kakao](https://developers.kakao.com/)에서 앱 등록 후 동의 항목 설정 및 API키, 활성화 필요
- 배포 관련: CI/CD(Vercel)

<br />

## ⚙️ 사용 스택

<div>
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat&logo=Next.js&logoColor=white" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=TypeScript&logoColor=white" />
  <img src="https://img.shields.io/badge/Tailwind-06B6D4?style=flat&logo=tailwindcss&logoColor=white" />
  <img src="https://img.shields.io/badge/Prisma-2D3748?style=flat&logo=prisma&logoColor=white" />
  <img src="https://img.shields.io/badge/Supabase-3FCF8E?style=flat&logo=supabase&logoColor=white" />
  <img src="https://img.shields.io/badge/React Hook Form-EC5990?style=flat&logo=reacthookform&logoColor=white" />
  <img src="https://img.shields.io/badge/React Query-FF4154?style=flat&logo=reactquery&logoColor=white" />
  <img src="https://img.shields.io/badge/Recoil-3578E5?style=flat&logo=Recoil&logoColor=white" />
  <img src="https://img.shields.io/badge/Kakao map API-FFCD00?style=flat&logo=kakao&logoColor=white" />
<!--   <img src="https://img.shields.io/badge/GoDaddy-1BDBDB?style=flat&logo=godaddy&logoColor=white" /> -->
  <img src="https://img.shields.io/badge/Google Analytics-E37400?style=flat&logo=googleanalytics&logoColor=white" />
  <img src="https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white" />
</div>

<br />

## 🛠️ 프로젝트 실행

- Yarn으로 Next.js앱을 설치합니다. `yarn create next-app`
- React-Icons를 설치합니다. `yarn add react-icons`
- Prisma를 설치합니다. `yarn add --dev prisma` `yarn add @prisma/client` `yarn add --dev ts-node`
- React Query를 설치합니다. `yarn add react-query`
- Axios를 설치합니다. `yarn add axios`
- Next-auth를 설치합니다. `yarn add next-auth` `yarn add @auth/prisma-adapter`
- Recoil을 설치합니다. `yarn add recoil`
- React Hook Form을 설치합니다. `yarn add react-hook-form`
- React-Toastify을 설치합니다. `yarn add react-toastify`
- React Daum Postcode를 설치합니다. `yarn add react-daum-postcode`
- Vercel CLI를 설치합니다. `yarn global add vercel`
- 프로젝트 시작 `yarn dev`

<!-- supabase pw: mVOa4tdlt8lkIrcF -->

<br />

## 🔑 페이지 설명

<!--
<details>
<summary>회원가입/로그인</summary>
<div markdown="1">

- 회원가입/로그인
  - 토글 버튼으로 회원가입/로그인 화면 전환
  - 아이디·비밀번호 중복확인 및 유효성 체크
  - 일반 이메일 형식 뿐만 아니라 구글·깃허브 계정으로도 로그인 가능
  - 사이트에 들어왔을 때 유저의 상태 변화 추적 가능
    - 로그인, 로그아웃, 어플리케이션 초기화(새로고침 or 재시작) 시 변화 추적
</div>
</details>

<details>
<summary>홈</summary>
<div markdown="2">

- 실시간 업데이트
- 트윗 작성
  - 홈이 아닌 다른 페이지에서도 트윗할 수 있도록 왼쪽 메뉴바에 트윗하기 버튼 추가
  - 이미지 추가 및 삭제 기능
  - 이모지 입력 기능
  - 해쉬태그 입력 기능
  - 트윗 수정·삭제
- 왼쪽 사이드 메뉴
  - 홈, 탐색하기, 알림, 북마크, 프로필 메뉴로 이동
  - 홈이 아닌 다른 페이지에서도 트윗할 수 있도록 왼쪽메뉴바에 트윗하기 버튼 추가
  - 유저 정보 확인 및 로그아웃 기능
- 오른쪽 사이드 메뉴
  - 트윗·유저 검색 기능
  - 본인 제외한 유저 목록 조회 및 팔로우 추천(팔로우, 언팔로우 기능)
- 반응형 액션 (답글, 리트윗, 좋아요, 북마크)
</div>
</details>

<details>
<summary>탐색하기</summary>
<div markdown="3">

※ '탐색하기'에서의 대부분 기능들은 '홈'과 같으며 반복되는 코드들을 하나의 컴포넌트로 묶어 재사용할 수 있게 했습니다.

- 검색창 및 트윗·사용자 탭
  - 반응형 액션 (답글, 리트윗, 좋아요, 북마크)
  - 유저 목록 조회 및 팔로우, 언팔로우 가능
</div>
</details>

<details>
<summary>알림/북마크</summary>
<div markdown="4">

- 알림 리트윗/답글/팔로우 탭
  - 누군가가 트윗에 리트윗·답글을 하면 실시간 알림 생성
  - 트윗 링크 및 리트윗·답글한 유저의 프로필 정보 링크로 이동 가능
  - 팔로우한 유저의 프로필 정보 링크로 이동 가능

- 북마크 트윗/답글 탭
  - 북마크한 트윗·답글 목록 조회 및 취소 시 실시간 반영
</div>
</details>

<details>
<summary>프로필</summary>
<div markdown="5">

- 헤더에 트윗한 개수 표시 및 로그아웃 가능
- '프로필 수정', '북마크' 탭은 본인 프로필에서만 노출 됨
- '한국어/English' 버튼으로 언어 변경 가능
- '프로필 수정' 클릭 시 모달창이 활성화 되어 배경·프로필 이미지, 닉네임·자기소개 추가/변경/삭제 가능
- 가입일과 팔로잉, 팔로워 숫자 확인

</div>
</details>-->

<!-- ## 🖥️ Screenshots -->
<!-- <p>
  <img src="./README/1.png"  width="47%" />
  <img src="./README/2.png" width="47%" />
  <img src="./README/3.png"  width="47%" />
  <img src="./README/4.png" width="47%" />
  <img src="./README/5.png"  width="47%" />
</p> -->
