🛍️ React 개인 프로젝트 - 하이츠 스토어(HEIGHTS)
----------------------------------------------------------------------------------------------
**React, Context API, React-Router를 기반으로 구현한 트렌디한 패션 이커머스 웹 프로젝트입니다.**

📌 목차
----------------------------------------------------------------------------------------------
* **[개요](#-개요)**
 
* **[기술 스택](#-기술-스택)**
 
* **[주요 기능 및 기술적 특징](#-주요-기능-및-기술적-특징)**
  
* **[기능 구현 PPT](#-기능-구현-ppt)**
  
* **[개선사항 및 회고 (추후 업데이트 예정)](#-개선사항-및-회고-추후-업데이트-예정)**

🗂 개요
----------------------------------------------------------------------------------------------
* **프로젝트 목표:** 하이츠 스토어의 감각적인 UI/UX 구현 및 이커머스 핵심 비즈니스 로직(동적 라우팅, 전역 상태를 활용한 장바구니, 관계형 게시판 데이터 처리)의 프론트엔드 아키텍처 설계

* **개발 인원:** 1인 (프론트엔드 개인 프로젝트)

* **배포 주소:** [여기에 GitHub Pages 링크 입력]

🛠 기술 스택
----------------------------------------------------------------------------------------------
* **Language:** JavaScript (ES6+), HTML5

* **Framework / Library:** React (Hooks), React Router DOM v6

* **State Management:** Context API

* **Styling:** Inline Styles (컴포넌트 스코프 스타일링), React Icons, FontAwesome

* **Data & Deploy:** Local JSON (Mock Data 비동기 시뮬레이션), GitHub Pages

* **Tool:** VS Code, Git / GitHub

💻 주요 기능 및 기술적 특징
----------------------------------------------------------------------------------------------
**1.** Context API 기반 전역 상태 관리 (Prop Drilling 방지)
장바구니 로직 (CartContext): 상품 상세 페이지에서 장바구니에 상품을 추가하면, 최상단 헤더(Header)의 장바구니 배지 카운트가 페이지 새로고침 없이 즉각적으로 동기화되도록 전역 상태를 설계했습니다.

**게시판 로직 (BoardContext)**: 리뷰 및 Q&A 작성 시, 입력된 데이터를 전역 상태 배열에 추가하여 모달창을 닫자마자 리스트에 반영되도록 구현했습니다.

**2.** 렌더링 최적화를 고려한 UI 인터랙션 (requestAnimationFrame)
스크롤 이벤트 최적화: 사용자의 스크롤 방향에 따라 네비게이션 바가 숨겨지거나 나타나는 애니메이션을 구현했습니다. 단순 scroll 이벤트 리스너 대신 requestAnimationFrame을 적용하여 브라우저의 렌더링 과부하(Jank)를 방지하고 부드러운 성능을 확보했습니다.

**3.** 컴포넌트 재사용성 극대화 및 관심사 분리
도메인 분리: Home.js(남성), Women.js(여성) 등 성격이 다른 페이지를 물리적으로 분리하여 스파게티 코드를 방지했습니다.

**UI 부품화:** <Ranking />, <TrendingBrands /> 등 핵심 UI를 공통 컴포넌트로 분리하고, 부모 컴포넌트에서 서로 다른 JSON 데이터(Props)만 주입하여 화면을 재사용하는 효율적인 구조를 설계했습니다.

**4.** 확장성을 고려한 논리적 데이터 모델링 (Mock Data)
실제 백엔드 DB가 없는 프론트엔드 환경이지만, JSON 데이터를 관계형 데이터베이스처럼 논리적으로 설계했습니다.

특정 상품을 클릭했을 때 전달받은 파라미터(useParams)를 고유 ID로 활용하여, 전체 리뷰/Q&A 데이터 중 해당 productId와 일치하는 데이터만 필터링(Array.filter)하여 렌더링합니다.

🖥 기능 구현 PPT
----------------------------------------------------------------------------------------------
<img width="1280" height="720" alt="19" src="https://github.com/user-attachments/assets/287c3934-8821-44bb-b659-5176d9187743" />
<img width="1280" height="720" alt="18" src="https://github.com/user-attachments/assets/8ebe7f79-19f2-445e-8550-93453045f7e2" />
<img width="1280" height="720" alt="17" src="https://github.com/user-attachments/assets/2baf3bf6-3975-4c1a-a24f-b9aa337518ee" />
<img width="1280" height="720" alt="16" src="https://github.com/user-attachments/assets/2d362e6c-de08-43b3-8a2e-92093625f302" />
<img width="1280" height="720" alt="15" src="https://github.com/user-attachments/assets/524492c7-99d2-49ef-859d-fcc9798f91d5" />
<img width="1280" height="720" alt="14" src="https://github.com/user-attachments/assets/45f0109b-56c0-4b8b-99f8-8d2b42f286be" />
<img width="1280" height="720" alt="13" src="https://github.com/user-attachments/assets/702af8dd-5e85-4e36-aa43-9a359fa97d2a" />
<img width="1280" height="720" alt="12" src="https://github.com/user-attachments/assets/73e47cd2-49ea-463f-b0f6-7fad5119ecad" />
<img width="1280" height="720" alt="11" src="https://github.com/user-attachments/assets/18b9dc95-cb37-4221-870d-4e2ec1899054" />
<img width="1280" height="720" alt="10" src="https://github.com/user-attachments/assets/391ba222-a58e-4484-9066-f3e37c92f89b" />
<img width="1280" height="720" alt="09" src="https://github.com/user-attachments/assets/ac667de9-4f94-406e-af9a-d094856c1dde" />
<img width="1280" height="720" alt="08" src="https://github.com/user-attachments/assets/e0f4980e-ee9b-45d0-825c-7e54efdd3545" />
<img width="1280" height="720" alt="07" src="https://github.com/user-attachments/assets/000b1f90-608c-4c73-b714-104ba4f2c735" />
<img width="1280" height="720" alt="06" src="https://github.com/user-attachments/assets/650af583-6aff-4d6e-b099-3122a9e1b4c5" />
<img width="1280" height="720" alt="05" src="https://github.com/user-attachments/assets/fdc94e28-73e3-4685-8759-b1ddb337dc40" />
<img width="1280" height="720" alt="04" src="https://github.com/user-attachments/assets/67efe432-c8ab-4884-b467-ff96477a6e73" />
<img width="1280" height="720" alt="03" src="https://github.com/user-attachments/assets/95926307-0847-47d9-a14e-25f6927393e6" />
<img width="1280" height="720" alt="02" src="https://github.com/user-attachments/assets/e32aea47-0962-407e-8926-bd7a4354991d" />
<img width="1280" height="720" alt="01" src="https://github.com/user-attachments/assets/7f095ef1-8091-4929-b1ed-48a71b2494e1" />

🚀 개선사항 및 회고 (추후 업데이트 예정)
----------------------------------------------------------------------------------------------
* **반응형 웹 적용:** 현재 데스크탑 기준의 UI를 모바일 및 태블릿 환경에서도 최적화되도록 미디어 쿼리(Media Query)를 적용할 예정입니다.

* **성능 최적화:** 컴포넌트 지연 로딩(Lazy Loading) 및 이미지 최적화를 도입하여 초기 렌더링 속도와 체감 성능을 개선할 예정입니다.

* **백엔드 연동 확장:** 현재 Mock Data와 Context API로 구현된 데이터 제어 로직을 추후 Firebase 또는 Node.js/MongoDB와 연동하여 실제 DB 기반의 CRUD 애플리케이션으로 고도화할 계획입니다.











