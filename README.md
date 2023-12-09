# 📍 POP.SPOT (팝업스토어 정보와 사전예약, 웨이팅 시스템이 하나로)

<br>
• 엘리스 SW 엔지니어 6기 2차 프로젝트<br>

<br>

## 요즘 핫한 팝업스토어 한눈에 찾아 볼 수 없을까?<br>
## 팝업스토어 꼭 현장까지 가서 줄을 서야할 까? 예약 서비스는 없을까?<br>

<br>

• 위와 같은 관점에서 우리는 POP.SPOT이라는 서비스를 기획하고 개발을 진행하였습니다. 이 서비스는 서울 팝업스토어 정보와 사전예약, 웨이팅 입장 시스템까지 하나로 통합된 서비스이며 팝업스토어 정보를 효율적으로 찾을 수 있도록 도와주고 사용자들이 직접 현장으로 가서 줄을 서야하는 번거로움 없이 사전예약, 원격 줄서기 등 웨이팅 시스템까지 이용할 수 있도록 했습니다.<br>

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

## 📍프로젝트 기간 & 인원

- 프로젝트 기간: 3주 (2023.11.13 ~ 2023.12.01)
- 개발 인원: 풀스택 6명 <br>

## 📍사용 기술

- **FrontEnd** <br>
  Next.js <br>
  React <br>
  SCSS <br>
  Prettier <br>
  Eslint <br>
  AWS s3 <br>
  <br>

- **BackEnd** <br>
  Node.js <br>
  express.js <br>
  MongoDB <br>
  Mongoose <br>
  Amazon S3 <br>
  PM2 <br>
  Nginx <br>

  <br>

- **협업** <br>
  Git & Git lab <br>
  Figma <br>
  Postman <br>
  Gather <br>
  Notion <br>
  <br>

## 📍내가 맡은 구현 페이지 및 기능

## 내가 구현한 UI <br><br>

1. 메인 페이지
2. 헤더
3. 팝업 리스트 페이지
4. 검색 모달창
5. 필터 모달창

## 내가 구현한 기능 <br><br>

1. 메인 페이지
2. 헤더
3. 팝업 리스트 페이지
4. 검색 모달창
5. 필터 모달창

### 1. 회원가입

![Sign Up](https://user-images.githubusercontent.com/126956430/246651264-2970799f-697d-433f-835c-ffaff97732ff.gif)

- 회원 유형 : 일반회원 / 공급회원
- 회원 정보 입력 : 일반회원 가입의 경우 추가 항목이 있습니다. (생년월일 / 운전자면허증 번호)
  <br> - 라디오 버튼 체크시 회원 유형에 따라 하나의 컴포넌트에서 다른 UI가 그려지도록 구현함
- 비밀번호 확인 : 비밀번호 확인 입력란을 추가하여 실시간으로 비밀번호를 일치 여부를 확인할 수 있습니다.
  <br> - 비밀번호가 다르게 입력되면 하단에 빨간 글씨로 일치하지 않는 메시지 표시 / 비밀번호가 동일하게 입력되면 파란 글씨로 일치한다는 메시지 표시
- 필수 개인 정보 수집 동의 : 필수 개인 정보 수집 동의 체크시에만 가입하기 버튼이 활성화됩니다.

<br> 위와 같이 차량 공유 서비스의 회원가입을 일반회원과 공급회원으로 구분하여 처리합니다.

<br>
  
### 2. 로그인
  
![Login](https://user-images.githubusercontent.com/126956430/246653550-dcb32e58-9b3c-42b4-89ab-b138af3f4687.gif)

- 회원 유형 : 일반회원 / 공급회원
  <br>- 로그인 시 가입한 회원 유형과 일치하지 않을 경우 알림창을 통해 회원 유형을 확인하도록 하여 올바른 회원 유형을 선택하도록 안내하여 사용자의 불필요한 행동을 줄였습니다.
  <br>- 패스 파라미터에 회원 유형 타입을 포함시켜 해당 API로 아이디와 비밀번호를 BODY에 담아 서버에 POST 요청을 보냅니다.
- 유효성 검사를 통해 이메일 형식과 비밀번호의 길이를 확인하여 로그인 버튼은 유효한 조건을 충족할 때만 활성화되며, 아이디 또는 비밀번호가 맞지 않을 경우에도 알림창을 통해 사용자에게 확인 메시지를 제공합니다. 이를 통해 사용자에게 명확하고 깔끔한 안내를 제공할 수 있습니다.
- 로그인 성공 시 : 요청에 대한 response의 상태가 201일 경우 accessToken, refreshToken을 localStorage애 저장합니다.
- 로그인 실패 시 : 요청에 대한 response의 상태가 404일 경우 alert창에 '회원 유형을 확인해주세요.' 메시지가 뜨게 하고 response의 상태가 400일 경우에는 alert창에 '이메일 또는 비밀번호를 확인해주세요.' 메시지가 뜨도록 서버의 응답 상태 코드를 확인하여 알림 메시지를 표시했습니다. 이를 통해 사용자가 현재 문제에 대해 인지할 수 있으며, 서버에 불필요한 요청을 계속 보내는 것을 방지하거나 불필요한 행동을 줄일 수 있습니다.

<br>
    
### 3. 차량 등록 (어드민 페이지)
  
![registration](https://user-images.githubusercontent.com/126956430/246664516-17b9ba74-3101-4926-bd74-60ae2af04a9f.gif)

- 어드민 페이지 구현:
  <br>- 호스트가 차량 정보 등을 입력하여 등록할 수 있는 어드민 페이지를 구현했습니다.
  <br>- 어드민 페이지에서는 차량에 관련된 정보를 입력하고, 등록 버튼을 눌러서 차량을 등록할 수 있습니다. 또한 등록된 차량을 확인할 수 있으며 해당 차량이 예약된 경우 예약내역도 확인할 수 있습니다.
  <br>- 어드민 페이지는 공급회원으로 가입한 유저에게만 접근이 가능하도록 인증 기능을 추가했습니다.
  <br>
- 차량 등록 요청 처리:
  <br>- 어드민 페이지에서 등록 버튼을 누르면, 클라이언트는 해당 정보를 서버로 전송하는 POST 요청을 보냅니다.
  <br>- 서버는 해당 요청을 받아 차량 정보를 확인하고, 필요한 유효성 검사를 수행 후에 호스트가 등록한 차량 정보를 데이터 베이스에 저장합니다.
  <br>
- 차량 등록 페이지 핵심 구현 사항:
  <br>- 브랜드를 선택하면 해당 브랜드에 맞는 차량들만 표시되는 드롭다운을 사용하여 사용자에게 불필요한 선택지를 제거하고 편리한 차량 선택을 도와주도록 구현했습니다.
  <br>- 차량을 선택하면 외형 / 차종 / 승차 정원은 라디오 버튼으로 활용해 디폴트값으로 차량에 맞는 정보로 고정되도록 구현했습니다.
  <br>- 차량 등록 과정에서 사진 파일 업데이트는 AWS의 S3를 활용하여, 서버에서 생성된 signed url을 받아와 클라이언트가 해당 url로 파일을 업로드하는 방식으로 구현했습니다.
  <br>- 픽업 / 반납 주소 등록은 카카오 주소 API를 활용하여 구현했습니다.

<br> 위와 같이 차량을 등록하면 메인 페이지의 차량 리스트가 업데이트 되어 가장 최신 순서로 업로드됩니다.

<br>

### 4. 메인 페이지

![Main](https://user-images.githubusercontent.com/126956430/246668331-c3009f4d-7705-4231-9a4e-c288a68b43a3.gif)

- 예약 가능한 host car 리스트를 제공하는 API의 query parameter에 브랜드 필터 조건과 pagenation을 위한 page number를 포함하여 서버에 요청을 보냅니다.
- 메인 페이지에 차량 리스트가 보여지는데, 한 번에 너무 많은 차량을 리스트를 불러오면 로딩 속도가 느려지는 문제가 발생할 수 있기 때문에 페이지네이션을 적용하여 한 번에 12개의 차량만 보여주도록 구현했습니다.
- 상단 필터바에서 브랜드를 클릭하면 해당 브랜드에 속하는 차량 리스트만 서버로부터 가져와서 사용자는 특정 브랜드의 차량만 볼 수 있습니다.
- 상단 필터바 오른쪽에 위치한 '모두보기' 버튼을 클릭하면 모든 차량 리스트를 서버로부터 가져와서 사용자는 다시 전체 차량 리스트를 볼 수 있습니다.

<br>

### 5. 검색 기능

![Search](https://user-images.githubusercontent.com/126956430/246670134-021051dd-e810-40a2-bdea-b0f4e1bf5da0.gif)

- 사용자가 원하는 지역, 탑승일 및 반납일, 탑승 인원 등의 조건을 설정하여 상세한 차량을 찾을 수 있는 검색 기능을 구현했습니다.
  <br>- 원하는 지역 선택: 사용자는 특정 지역을 선택하여 해당 지역에서 이용 가능한 차량을 검색할 수 있습니다. 이를 통해 사용자는 특정 도시 또는 장소에서 차량을 찾을 수 있습니다.
  <br>- 탑승일 및 반납일 설정: 사용자는 탑승일 및 반납일을 선택하여 해당 기간 동안 이용 가능한 차량을 검색할 수 있습니다. 이를 통해 사용자는 원하는 기간에 차량을 예약할 수 있습니다.
  <br>- 탑승 인원 설정: 사용자는 탑승 인원을 지정하여 해당 인원 수에 맞는 차량을 검색할 수 있습니다. 이를 통해 사용자는 예약하려는 인원에 맞는 충분한 공간을 제공받을 수 있습니다.
- useSearchParams 훅을 이용하여 URL 쿼리 부분을 필터 조건으로 바꾸고 해당 쿼리 부분을 가져와서 API 엔드포인트에 포함시켜 요청을 보냅니다.
- 이러한 조건들을 동시에 적용하거나 하나씩 선택하여 사용자가 상세한 차량을 찾을 수 있습니다. 사용자는 자신의 요구 사항에 맞는 차량을 쉽게 필터링하여 검색 결과를 확인할 수 있습니다. 이를 통해 사용자는 원하는 지역, 날짜, 탑승 인원 등을 고려하여 최적의 차량을 찾을 수 있습니다.

<br>

### 6. 필터 기능

![filter](https://user-images.githubusercontent.com/126956430/246728102-e5f4ca11-b914-4c91-afdd-19828c9a6df2.gif)

- useSearchParams 훅을 이용하여 URL 쿼리 부분을 필터 조건으로 바꾸고 해당 쿼리 부분을 가져와서 API 엔드포인트에 포함시켜 요청을 보냅니다.
- 검색 기능에서 좀 더 세밀하게 필터링 할 수 있도록 다양한 필터 조건 제공합니다. 적용될 수 있는 필터에는 '브랜드', '배기량', '차량 유형', '연료 유형', '일일 최소 대여료', '일일 최대 대여료', '탑승 정원', '차량 옵션'이 있으며, 모두 동시에 적용 가능합니다.
- 사용자는 원하는 조건을 선택하거나 조합하여 차량을 쉽게 필터링할 수 있습니다.
- 필터 조건이 많이 걸려서 다시 초기로 돌아가고 싶으면 전체 해제 버튼을 누르면 설정된 조건이 초기화됩니다.
- 여러 필터 조건을 조합하여 필터링 했을 때 조건에 맞는 차량이 없으면 '해당 조건에 맞는 차량이 없습니다.' 라고 표시해줍니다.

<br>

### 7. 제품 디테일 페이지

![detail](https://user-images.githubusercontent.com/126956430/246733998-3beeeb1d-240d-4b04-a894-6d808beebd2d.gif)

- 동적 라우팅을 구현하여 useNavigate 훅과 useParams 훅을 사용해 path parameter에 productId를 포함시켜 서버에 요청을 보내고 서버로부터 차량의 상세 정보를 받아와서 제품 상세 페이지에 차량 정보를 표시합니다.
- 카카오 지도 API를 사용하여 차량 등록 시 입력한 픽업 및 반납 위치를 기반으로 핀을 꽂아 지도로 보여주어 사용자에게 위치를 시작적으로 전달할 수 있게 구현했습니다.
- react-calendar 라이브러리르 활용하여 예약 전 탑승일과 반납일을 지정할 수 있는 기능을 구현하고, 선택한 날짜에 따라 자동으로 이용 일수, 금액, 수수료, 최종 금액 등이 계산되어 표시됩니다.
- react-calendar 라이브러리 기능을 활용하여 호스트가 차량 등록 시 설정한 기간 이외에는 날짜를 선택할 수 없도록 제한되며, 예약이 체결된 경우에도 해당 예약된 날짜에 다른 사용자가 예약할 수 없도록 날짜 선택을 제한하였습니다.
- 날짜 초기화 버튼 누르면 지정한 날짜가 리셋되는 기능도 추가하였습니다.

<br>

### 8. 결제 페이지

![payment](https://user-images.githubusercontent.com/126956430/246740828-cb632cbd-db14-4775-857b-ea218f6eacae.gif)

- 사용자는 결제 수단을 토스로 선택하고 예약 요청 버튼을 클릭해 Toss 결제 API를 호출하여 결제를 진행합니다.
- 결제 완료 후, 서버에 결제 정보를 전송합니다. 이후 서버에서는 Toss 결제 API의 secret key를 사용하여 결제 승인 요청을 생성합니다.
- 결제 승인이 성공적으로 이루어진 경우, 완료 페이지로 이동하여 사용자가 상세한 예약 내역을 확인할 수 있습니다.
  <br>

### 8. 예약 내역 확인

![confirm](https://user-images.githubusercontent.com/126956430/246745312-3eba0fa4-4e61-4a85-bbdd-584bdc2f56da.gif)

- 해당 차량의 호스트 계정으로 로그인하여 어드민 페이지의 예약 내역에서 예약된 리스트를 확인할 수 있습니다. 이를 통해 호스트는 자신의 차량에 대한 예약 상황을 실시간으로 파악할 수 있습니다.
  <br>

  ## 📍느낀점/회고

  > 3차 프로젝트 회고록: https://youngwoonkim.tistory.com/15 > <br>

## Reference

- 이 프로젝트는 [airbnb](https://www.airbnb.co.kr/) 사이트를 참조하여 학습목적으로 만들었습니다.
- 실무수준의 프로젝트이지만 학습용으로 만들었기 때문에 이 코드를 활용하여 이득을 취하거나 무단 배포할 경우 법적으로 문제될 수 있습니다.
- 이 프로젝트에서 사용하고 있는 사진 대부분은 위코드에서 구매한 것이므로 해당 프로젝트 외부인이 사용할 수 없습니다.
