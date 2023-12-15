# 📍 POP.SPOT (팝업스토어 정보와 사전예약, 웨이팅 시스템이 하나로)

<br>
엘리스 SW 엔지니어 6기 2차 프로젝트<br>

<br>

요즘 핫한 팝업스토어 한눈에 찾아 볼 수 없을까?<br>
팝업스토어 꼭 현장까지 가서 줄을 서야할까? 예약 서비스는 없을까?<br>

<br>

• 위와 같은 관점에서 우리는 POP.SPOT이라는 서비스를 기획하고 개발을 진행하였습니다. 이 서비스는 서울 팝업스토어 정보 공유와 사전예약, 웨이팅 입장 시스템까지 하나로 통합된 서비스이며 팝업스토어 정보를 효율적으로 찾을 수 있도록 도와주고 사용자들이 직접 현장으로 가서 줄을 서야하는 번거로움 없이 사전예약, 원격 줄서기 등 웨이팅 시스템까지 이용할 수 있도록 했습니다.<br>

<br>

## 어떤 문제를 해결하는가?<br>

<br>

1. 한눈에 보기 쉬운 정보 제공<br>
• 서울 구역별로 정리된 팝업스토어 정보를 한눈에 제공하여 사용자들이 쉽게 찾을 수 있도록 했습니다.
2. 원격 웨이팅 시스템 도입<br>
• 현장에 가지 않고도 집에서 웨이팅을 걸 수 있도록 편리한 서비스를 제공하였습니다. 이를 통해 사용자들은 대기 시간을 최소화할 수 있습니다.<br>
3. 사전예약 시스템 구축<br>
• 아직 열리지 않은 팝업스토어에 대해서도 미리 사전 예약할 수 있는 시스템을 도입하여 사용자들의 편의를 높였습니다.<br>
<br>
> 개발은 초기 세팅부터 전부 직접 구현했으며, 실제 사용할 수 있는 서비스 수준으로 개발한 것입니다.<br>
> 디자이너가 없지만 UI/UX도 클론 코딩이 아닌 직접 디자인하여 구현했습니다. 최대한 실제 사이트처럼 보이며 사용자가 이용하기 편리하도록 주력했습니다.

<br>
<br>

## 📍프로젝트 기간 & 인원

- 프로젝트 기간: 3주 (2023.11.13 ~ 2023.12.01)
- 개발 인원: 풀스택 6명 <br>

## 📍사용 기술

- **FrontEnd** <br>
  Next.js / React / SCSS / Prettier / Eslint / AWS s3
  
  <br>

- **BackEnd** <br>
  Node.js / express.js / MongoDB / Mongoose / Amazon S3 / PM2 / Nginx <br>

  <br>

- **협업** <br>
  Git & Git lab / Figma / Postman / Gather / Notion <br>
  
  <br>

## 📍 내가 맡은 구현 페이지 및 기능

### • 담당 UI <br>
1. 메인 페이지
2. 헤더
3. 푸터
4. 팝업 리스트 페이지
5. 검색 모달창
6. 필터 모달창

### • 담당 기능 <br>
1. 캐로셀
2. 자동 롤링
3. 타이머
4. 검색 (최근 검색어, 실시간 인기 검색어)
5. 필터 (구역, 카테고리, 방문날짜, 운영상태)
6. 페이지네이션
7. 위시리스트

<br>

## 1. 메인페이지
메인 페이지에서 다양한 컨텐츠를 보여줌으로써 사용자들에게 더욱 효과적으로 팝업스토어에 참여하도록 유도했습니다. 사용자들에게 흥미를 끄는 컨텐츠를 제공하면서도 너무 복잡하지 않게 디자인 하였으며, 팝업스토어 이미지들이 전체적으로 튀는 색이 많아 웹사이트는 블랙과 화이트로 가면서 포인트 색상으로 블루를 사용했습니다. 폰트, 폰트 크기, 색상, 레이아웃 배치 등 UI 그리는데 여러 요소를 고민하여 실제 사이트처럼 자연스럽게 보이도록 구현했습니다. <br>

<br>

<img src="https://github.com/KIMYOUNGWOON/POP.SPOT/assets/126956430/105bf42d-09bd-4b92-821a-207b29860a98" width="600">

<br><br>

• 자동 롤링 배너 : 애니메이션과 함께 등록된 모든 팝업스토어를 한눈에 볼 수 있는 자동 롤링 배너를 구현하여 팝업스토어의 다양성과 특별함이 애니메이션으로 살아나 사용자들에게 눈에 띄게 전달했습니다.<br>
• 추천 팝업 : 회원가입 시 설정한 관심 카테고리를 기반으로 한 사용자 맞춤형 팝업스토어를 제공합니다. 로그인 시, 취향에 맞는 팝업 리스트가 메인 페이지에 동적으로 표시되도록 구현했습니다.<br>
• 종료 직전 팝업 : 현재 날짜를 기준으로 마감이 5일 이내로 남은 팝업스토어를 실시간으로 업데이트하여 사용자에게 제공합니다. 또한 남은 시간을 타이머로 시각적으로 표시하여, 소중한 경험을 놓치지 않도록 유도했습니다.<br>
• 성수 팝업 : 성수는 팝업스토어의 성지인만큼 해당 구역에서만 만날 수 있는 팝업 스토어들을 한 눈에 볼 수 있는 섹션을 마련했습니다.<br>

<br>

각 섹션은 각각의 컴포넌트로 만들어 서버에서 섹션에 맞게 팝업스토어 리스트를 가져오도록 데이터 페칭이 이루어집니다. 이를 통해 실시간으로 업데이트되는 팝업스토어 정보를 사용자에게 효과적으로 전달하도록 구현했습니다.<br>

<br>

### 메인페이지에서 필요한 API

1. 자동 롤링 배너 API <br>
• 역할 : 등록된 모든 팝업스토어 리스트를 불러오는 API <br>
• 구현 : 📌[코드 보러가기](https://github.com/KIMYOUNGWOON/POP.SPOT/blob/main/server/services/popupListService.js#L4) <br>
2. 추천 팝업 API <br>
• 역할 : validateToken 미들웨어로 유저를 검증하고 해당 유저 데이터에서 설정한 카테고리 정보를 가져와서 해당 카테고리의 팝업스토어 리스트를 불러오는 API <br>
• 구현 : 📌[코드 보러가기](https://github.com/KIMYOUNGWOON/POP.SPOT/blob/main/server/services/popupListService.js#L42) <br>
3. 종료 직전 팝업 API <br>
• 역할 : 현재 날짜 기준 팝업스토어의 end_date가 5일 이하로 남은 팝업스토어 리스트를 불러오는 API <br>
• 구현 : 📌[코드 보러가기](https://github.com/KIMYOUNGWOON/POP.SPOT/blob/main/server/services/popupListService.js#L23) <br>
4. 성수 팝업 API <br>
• 역할 : 주소가 성수이며 현재 진행중인 팝업스토어 리스트를 불러오는 API <br>
• 구현 : 📌[코드 보러가기](https://github.com/KIMYOUNGWOON/POP.SPOT/blob/main/server/services/popupListService.js#L11) <br>

<br><br>

### 메인페이지 간단 기능

사용자가 메인페이지에서 팝업스토어를 편리하게 탐색할 수 있도록 자동 롤링과 캐로셀을 통해 직관적이고 효과적인 경험을 제공했습니다.

<br>

<img src="https://github.com/KIMYOUNGWOON/POP.SPOT/assets/126956430/4a07a3b1-89c1-4425-92ae-77d711b22ba3" width="600">

<br><br>

1. 자동 롤링 배너 기능 <br>
• 플렉스 박스 구성 : 리스트를 담은 플렉스 박스를 사용하여 롤링 배너 아이템을 가로로 배열했습니다. <br>
• 카피본 생성 : 동일한 플렉스 박스의 카피본을 하나 더 생성했습니다. <br>
• 이동 : @keyframes 규칙을 사용하여 이동 애니메이션을 정의하고 infinite로 설정하여 애니메이션이 무한으로 반복되도록 했습니다. <br>
• 채우기 : 일정 주기마다 원본 플렉스 박스가 왼쪽으로 이동하면서 빈 공간이 발생하는데 이때 카피본이 왼쪽으로 이동하면서 원본 플렉스 박스의 빈 공간을 채워주도록 구현했습니다. <br>
• 멈추기 : 팝업스토어 이미지에 호버시 애니메이션이 멈추고 호버하지 않으면 다시 애니메이션이 동작하도록 하였고 클릭시 해당 팝업스토어 상세페이지로 이동되도록 구현했습니다.

이렇게 함으로써 사용자는 웹 페이지를 로드할 때부터 자동으로 롤링 배너를 볼 수 있으며, 플렉스 박스와 카피본을 이용하여 부드러운 롤링 효과를 경험할 수 있습니다.

<br>

2. 캐로셀 기능 <br>
• 두 가지 캐로셀 구현:<br>
한 칸씩 이동하는 캐로셀: 버튼을 클릭하면 캐로셀이 한 칸씩 오른쪽으로 이동합니다.<br>
전체가 넘어가는 캐로셀: 버튼을 클릭하면 캐로셀이 전체적으로 한 번에 이동합니다. <br>
• 동적인 버튼 표시: 처음에는 오른쪽으로 넘기는 버튼만 표시되며, 한 번 이동하면 왼쪽으로 넘기는 버튼이 나타납니다. 그리고 캐로셀이 끝까지 이동하면 오른쪽으로 넘기는 버튼이 사라지도록 구현하여 더 이상 넘길 수 없다는 시각적인 피드백을 제공했습니다.<br>

<br>

## 2. 검색 모달창 

검색 기능은 사용자가 입력한 키워드를 팝업스토어의 브랜드, 이름, 카테고리, 주소 등에서 찾아 해당 키워드가 포함된 팝업스토어를 검색합니다. 이를 통해 사용자는 다양한 정보를 기반으로 검색을 수행할 수 있어 브랜드명이나 특정 카테고리, 주소 등으로 팝업스토어를 효과적으로 찾을 수 있습니다. 키워드 입력 후 검색시 URL 쿼리스트링이 변경되면서 페이지가 새로 로드되어 해당 쿼리 스트링 값을 가져와 데이터 페칭이 이루어지도록 구현했습니다. (ex. /popupList/search?pageNumber=1&limit=8&keyword=강남)

<br>

<img src="https://github.com/KIMYOUNGWOON/POP.SPOT/assets/126956430/4b07b5d6-e0f7-4001-ac35-6d8c3ba63f8d" width="600">

<br><br>

더 나은 검색 경험을 위해서 아래와 같은 기능을 구현했습니다.<br>

1. 최근 검색어<br>
• 사용자가 검색한 키워드를 로컬 스토리지에 저장하여 키워드와 검색한 날짜 및 시간이 함께 표시되도록 구현했습니다.<br>
• 동일한 키워드를 검색했을 경우, 이전에 남아 있는 키워드는 제거되고 최근 위치에 새로운 기록이 남도록 구현했습니다.<br>
• 사용자에게는 최근 검색어 목록을 날짜/시간 순으로 보여주고, 개별적 또는 전체적으로 삭제할 수 있도록 구현했습니다.<br>
• 사용자가 최근 검색어를 클릭하면 추가적인 입력없이 즉시 검색이 되도록 구현했습니다.<br>

2. 실시간 인기 검색어<br>
• 실시간 인기 검색어를 노출하여 사용자들이 현재 뜨고 있는 팝업스토어를 신속하게 파악할 수 있도록 구현했습니다.<br>
• 실시간으로 검색이 많이 되는 키워드를 카운팅하여 사용자에게 제공해 인기 검색어가 동적으로 노출되도록 구현했습니다.<br>
• 사용자가 인기 검색어를 클릭하면 추가적인 입력없이 즉시 검색이 되도록 구현했습니다.<br>

3. 검색 결과 표시<br>
• 검색어를 입력한 후 검색을 실행하면 해당 검색어로 총 몇개의 팝업스토어가 검색되었는지 표시되도록 구현했습니다.<br>

4. 페이지 네이션<br>
• 해당 검색어에 대한 팝업스토어를 모두 불러오지 않고, 페이지네이션을 적용하여 일정 개수의 데이터만을 가져오도록 구현했습니다.<br>

<br>

### 검색 기능에서 필요한 API

1. 검색 API <br>
• 역할 : 검색한 키워드에 해당하는 팝업스토어 리스트를 불러오는 API <br>
• 구현 : 쿼리스트링으로 전달한 pageNumber, limit, keyword 값을 추출하여 브랜드, 팝업스토어 이름, 카테고리, 주소를 탐색하여 입력한 키워드가 포함된 팝업스토어 리스트를 가져옵니다. 이때 페이지네이션이 적용되어 페이지별로 8개씩만 데이터를 불러오도록 구현되었습니다. 또한, 검색된 전체 팝업스토어 갯수, 페이지네이션이 적용된 팝업 리스트, 토탈 페이지 수를 응답으로 전달합니다.📌[코드 보러가기](https://github.com/KIMYOUNGWOON/POP.SPOT/blob/main/server/services/popupListService.js#L75) <br>
2. 검색 키워드 저장 API  <br>
• 역할 : 키워드 입력 후 검색 진행 시 해당 검색어를 DB에 저장하는 API <br>
• 구현 : 사용자가 검색어를 입력하고 검색을 실행하면 해당 검색어를 DB의 검색 컬렉션에 저장합니다. 만약 이미 저장되어 있는 검색어일 경우에는 새로 저장하지 않고 해당 검색어의 카운트 필드의 숫자만 1씩 증가시킵니다.📌[코드 보러가기](https://github.com/KIMYOUNGWOON/POP.SPOT/blob/main/server/services/searchService.js#L8) <br>
3. 인기 검색어 API <br>
• 역할 : 사용자들이 많이 검색한 키워드를 불러오는 API <br>
• 구현 : 검색어들의 카운트 필드를 내림차순으로 정렬하여 검색 키워드 리스트를 응답으로 전달합니다. 상위 14개 키워드만 노출시킵니다.📌[코드 보러가기](https://github.com/KIMYOUNGWOON/POP.SPOT/blob/main/server/services/searchService.js#L3) <br>

<br>

## 3. 팝업리스트 페이지

곧 오픈예정, 현재 운영중, 종료 등 상태에 따라 팝업스토어의 썸네일 이미지를 다르게 보여주어 사용자가 시각적으로 빠르게 구분할 수 있도록 구현했습니다. 그리고 팝업 스토어의 정보 부분에 곧 오픈 예정, 현재 운영중, 종료와 같은 상태에 대한 텍스트를 활용하여 상세페이지에 들어가지 않아도 미리 상태 정보를 알 수 있도록 표시했습니다. (곧 오픈 예정일 경우는 사전예약 / 현재 운영중일 경우는 웨이팅)

<br>

<img src="https://github.com/KIMYOUNGWOON/POP.SPOT/assets/126956430/69e7b21f-4b03-41f2-a1f1-621272b08fc9" width="600">

<br><br>

### 팝업리스트 페이지 기능 구현

1. 페이지네이션<br>

<br>

<img src="https://github.com/KIMYOUNGWOON/POP.SPOT/assets/126956430/dd0bd1a1-6da8-4d5a-971e-622c43a95bd3" width="600">

<br><br>

• 초기 진입 : 사용자가 처음 팝업 리스트 페이지에 접근할 때, /popupList/all?pageNumber=1&limit=8과 같은 패스와 쿼리스트링이 포함된 URL로 로드되고 패스와 쿼리스트링 값을 가져와서 API 요청을 보냅니다. 서버는 해당 페이지네이션에 맞는 팝업 리스트(총 8개의 리스트를 불러옴)와 전체 페이지 수를 응답합니다.<br>
• 동적 페이지 버튼 생성 : 받은 응답을 기반으로 팝업리스트 페이지 하단에는 페이지 수에 따라 동적으로 페이지 이동 버튼을 생성합니다. 예를 들어, 총 페이지 수가 5라면 1, 2, 3, 4, 5의 버튼이 생성됩니다.<br>
• 페이지 이동 : 사용자가 페이지 버튼을 클릭하면 해당 페이지에 맞는 API 요청이 발생합니다. 예를 들어, 2페이지를 클릭하면 /popupList/all?pageNumber=2&limit=8으로 쿼리스트링이 변경되고, 이에 따라 서버에서는 새로운 팝업 리스트를 반환합니다.<br>
• 동적 리스트 갱신 : 받은 새로운 팝업 리스트를 이용하여 화면에 표시될 리스트를 갱신합니다. 남은 리스트 개수가 현재 페이지의 limit보다 적은 경우, 남은 리스트만큼만 가져와서 표시합니다.<br>

<br>

### 페이지네이션 API

• 역할 : 모든 팝업스토어 리스트를 한번에 불러오지 않고 페이지별로 쪼개서 불러오는 API <br>
• 구현 : 쿼리스트링에서 pageNumber 및 limit 값을 추출하여 MongoDB에서 페이지네이션에 맞는 팝업 리스트 조회합니다. 이때 skip() 메소드를 이용해서 현재 페이지에서 몇개의 아이템을 건내뛰어야 하는지 계산합니다. 조회된 팝업스토어 리스트와 전체 페이지수를 함께 응답으로 반환합니다. 📌[코드 보러가기](https://github.com/KIMYOUNGWOON/POP.SPOT/blob/main/server/services/popupListService.js#L54) <br>


<br>



<br>

2. 운영상태 필터링

<img src="https://github.com/KIMYOUNGWOON/POP.SPOT/assets/126956430/51de889d-9391-4a1a-adbb-ea60860e7fb7" width="600">

<br><br>

• 사용자가 리스트 상단의 셀렉트 박스를 통해 곧 오픈, 운영 중, 종료 상태의 팝업리스트를 필터링하여 볼 수 있도록 구현했습니다.<br>
• 사용자가 선택한 상태에 따라 필터링하기 위해 URL의 쿼리스트링에 order 파라미터를 추가합니다. (ex.?pageNumber=1&limit=8&order=ongoing)<br>
• order의 값이 바뀔 때마다 API 요청을 보냅니다.<br>

### 운영상태 필터 API

• 역할 : 선택된 운영상태에 따라 그에 맞는 팝업스토어 리스트를 불러오는 API <br>
• 구현 : 
1. 서버에서는 쿼리스트링으로부터 order 값을 추출합니다.<br>
2. 추출한 order 값을 기반으로 아래와 같은 쿼리를 추가하여 해당하는 상태의 팝업리스트를 데이터베이스에서 조회합니다.<br>
"ongoing": 현재 날짜가 start_date보다 크거나 같고, end_date보다 작거나 같은 팝업스토어를 필터링합니다. 즉, 현재 진행 중인 팝업스토어입니다.<br>
"comingSoon": 현재 날짜가 start_date보다 크거나 같은 팝업스토어를 필터링합니다. 즉, 곧 시작될 팝업스토어입니다.<br>
"close": 현재 날짜가 end_date보다 작거나 같은 팝업스토어를 필터링합니다. 즉, 이미 종료된 팝업스토어입니다.<br>
3. 여기서도 페이지네이션이 적용되어 조회된 리스트가 8개가 넘으면 8개 리스트만 반환합니다. 전체 페이지수, 조회된 모든 리스트 수도 함께 반환합니다.<br>
📌[코드 보러가기](https://github.com/KIMYOUNGWOON/POP.SPOT/blob/main/server/services/popupListService.js#L132) <br>

<br>

3. 위시리스트

<img src="https://github.com/KIMYOUNGWOON/POP.SPOT/assets/126956430/73621d70-60b8-4ee9-ac16-9a362dad3c79" width="600">

• 위시리스트 추가 및 삭제 : 하트 아이콘을 클릭하여 팝업스토어를 위시리스트에 추가할 수 있으며, 토글로 하트 아이콘 클릭을 해제하면 추가된 팝업스토어를 다시 위시리스트에서 삭제할 수 있도록 구현했습니다. <br>
• 로그인 알림 및 이동 : 사용자 경험을 향상시키기 위해 로그인하지 않은 상태에서 하트 아이콘 클릭 시, 로그인이 필요하다는 알림과 함께 사용자를 로그인 페이지로 자동으로 이동시키게끔 구현했습니다. <br>

<br><br>

<img src="https://github.com/KIMYOUNGWOON/POP.SPOT/assets/126956430/d44694da-97e7-4d74-829f-7c5288ab4031" width="600">

• 상태 유지 : 추가한 팝업스토어는 새로고침이나 페이지 이동 후에도 하트가 클릭된 상태로 유지되도록 구현했습니다. <br>
• 관심 팝업리스트 확인 : 마이페이지 관심팝업 탭에서 사용자가 위시리스트에 추가한 팝업스토어 리스트를 확인할 수 있습니다. <br>

<br>
 
### 위시리스트 API

1. 관심 팝업스토어 저장 API <br>
• 역할 : 하트 아이콘을 누르면 위시리스트 컬렉션에 해당 팝업스토어를 저장하는 API <br>
• 구현 : validateToken 미들웨어로 로그인 했는지 확인 후 통과되면 요청 바디에 담긴 팝업스토어 ID와 미들웨어에서 넘겨 받은 사용자 ID를 함께 MongoDB 위시리스트 컬렉션에 하나의 도큐먼트로 저장합니다. 📌[코드 보러가기](https://github.com/KIMYOUNGWOON/POP.SPOT/blob/main/server/services/interestService.js#L10) <br>
2. 관심 팝업스토어 삭제 API <br>
• 역할 : 토글로 하트 아이콘을 클릭을 해제하면 위시리스트 컬렉션에 해당 팝업스토어를 삭제하는 API <br>
• 구현 : validateToken 미들웨어로 로그인 했는지 확인 후 통과되면 미들웨어에서 넘겨준 사용자 정보로 사용자 ID를 추출하고 패스파라미터로 전달 받은 팝업스토어 ID를 활용하여 위시리스트 컬렉션에서 해당 팝업스토어를 삭제합니다. 📌[코드 보러가기](https://github.com/KIMYOUNGWOON/POP.SPOT/blob/main/server/services/interestService.js#L37) <br>
3. 관심 팝업리스트 불러오는 API <br>
• 역할 : 사용자가 저장한 관심 팝업리스트를 전부 불러오는 API  <br>
• 구현 : validateToken 미들웨어에서 넘겨 받은 사용자 정보로 사용자 ID를 추출하여 해당 ID로 저장된 관심 팝업 리스트를 불러옵니다.📌[코드 보러가기](https://github.com/KIMYOUNGWOON/POP.SPOT/blob/main/server/services/interestService.js#L20) <br>

<br>

## 4. 필터 모달창

<img src="https://github.com/KIMYOUNGWOON/POP.SPOT/assets/126956430/7e1f011d-b5f9-4d13-b956-3d74b1ad3d02" width="600">

<br><br>

• 다양한 필터링 옵션 : 서울 구역, 카테고리, 방문 날짜 등 다양한 옵션을 활용하여 팝업스토어 리스트를 효과적으로 필터링하여 볼 수 있도록 구현했습니다. <br>
• 중첩 필터링 : 구역, 카테고리, 방문일을 중첩해서 필터를 적용하여 더 세부적으로 원하는 팝업스토어를 찾을 수 있도록 구현했습니다. <br>
• 시각적인 필터 UI :<br>
  1. 서울 지도를 활용한 구역 선택 : 사용자가 원하는 지역을 직관적으로 선택할 수 있도록 구현했습니다. SVG 파일로 표현된 지도는 사용자에게 자세한 지리적 정보를 제공하며, 사용자가 원하는 위치에 쉽게 접근할 수 있습니다.<br>
  2. 카테고리 선택 : 다양한 카테고리가 제공되며, 각 카테고리에 해당하는 이미지를 함께 보여주어 좀 더 시각적으로 잘 이해하고 구분할 수 있도록 구현했습니다.<br>
  3. 방문일 선택 : 날짜 선택을 편리하게 하기 위해 달력 형태의 UI를 도입하여 사용자가 원하는 날짜를 직관적으로 선택할 수 있도록 구현했습니다.<br>
  
<br>

### 필터 API

• 역할 : 사용자가 설정한 필터 옵션에 따라 필터링된 팝업스토어 리스트를 불러오고 페이지네이션 하는 API <br>
• 구현 : <br>
1. 서버에서는 쿼리스트링으로 전달받은 페이지번호(pageNumber), 제한된 결과 수(limit), 지역(area), 카테고리(category), 날짜(date) 값을 추출합니다.<br>
2. MongoDB에서 사용할 쿼리 객체를 초기화합니다.<br>
3. 각 필터 옵션은 개별로 적용하거나 중첩해서 적용할 수 있습니다.<br>
 - 만약 area 매개변수가 존재한다면, query 객체에 address 필드를 추가하고 해당 지역을 대소문자 구분 없이 검색할 수 있도록 정규식을 사용합니다.<br>
 - 만약 category 매개변수가 존재한다면, query 객체에 category 필드를 추가하고 해당 카테고리를 대소문자 구분 없이 검색할 수 있도록 정규식을 사용합니다.<br>
 - 만약 date 매개변수가 존재한다면, query 객체에 시작 날짜(start_date)와 종료 날짜(end_date)를 추가합니다. 선택된 날짜와 비교하여 해당 날짜 범위에 속하는 결과를 필터링합니다.<br>
4. 필터링된 쿼리를 사용하여 MongoDB에서 팝업 스토어를 조회합니다. skip을 사용하여 올바른 페이지의 결과를 가져옵니다. 또한, limit을 사용하여 페이지 당 결과 수를 제한합니다.<br>
5. 전체 문서 수를 가져와서 페이지 수를 계산합니다. 이를 클라이언트에게 반환될 응답에 포함시킵니다.<br>
6. 계산된 페이지 수, 필터링된 팝업 스토어 목록, 그리고 전체 문서 수를 객체로 묶어 반환합니다.<br>

📌[코드 보러가기](https://github.com/KIMYOUNGWOON/POP.SPOT/blob/main/server/services/popupListService.js#L101) <br>

<br>

## 5. 반응형 

### 메인페이지 / 검색 모달창 / 헤더 / 푸터

<br>

<img src="https://github.com/KIMYOUNGWOON/POP.SPOT/assets/126956430/af2079aa-2120-4298-a991-5b95d0127542" width="600"> <img src="https://github.com/KIMYOUNGWOON/POP.SPOT/assets/126956430/4ee9f29e-b591-42a2-9e96-2bd2d64964d2" width="200">



<br>

### 리스트페이지 / 필터 모달창

<br>

<img src="https://github.com/KIMYOUNGWOON/POP.SPOT/assets/126956430/29d96a0a-f068-4ae4-b51e-25c77d227b55" width="600">

<br>

• 반응형 구현<br>
프로젝트 초기 웹페이지 레이아웃을 구성할 때 반응형을 고려하지 않아서 창이 줄었을 때의 레이아웃 구조에 대한 고민이 많이 필요했습니다. 레이아웃이 주로 플렉스 박스와 그리드로 짜여 있어 브라우저창 크기에 따라 동적으로 변하는 레이아웃을 아래와 같이 구현했습니다. <br>
- 플렉스 박스 레이아웃 : 플렉스 박스를 사용한 레이아웃은 미디어쿼리를 통해 창의 크기에 따라 정렬, 아이템 크기, 한 줄에 보여질 아이템 갯수 등이 동적으로 바뀌도록 구현했습니다.<br>
- CSS 그리드 레이아웃 :   CSS 그리드를 사용한 레이아웃은 그리드 아이템의 크기와 위치를 정의하고 미디어쿼리를 통해 창의 크기에 따라 그리드 레이아웃을 동적으로 조절했습니다.<br>
- 모달창 : 브라우저창을 줄였을 때 모달창의 가로 세로 넓이를 화면에 꽉 채우도록 구현하여 사용자가 어떤 환경에서도 모달을 편리하게 사용할 수 있도록 했습니다.<br>
- 헤더 : 브라우저창을 줄였을 때 헤더 요소를 숨기고 햄버거 버튼을 생성하여 누르면 모달창 안에 숨긴 버튼들을 보여주는 방식으로 구현했습니다.<br>

<br>

기한이 정해진 프로젝트이다 보니 세밀한 수준의 반응형 구현은 어려웠지만 창이 줄어들었을 때 레이아웃 배치에 대한 고민을 통해 기본적인 이해를 높일 수 있었습니다.<br>




