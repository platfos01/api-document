## 개요

### 서버정보

개발서버: dev.pongift.com

운영버서: pongift.com

- - -

### API

서버 IP를 등록 후 이용할 수 있습니다.
hklee@platfos.com 로 전달바랍니다.

[카테고리](https://github.com/platfos01/api-document/blob/master/%EC%B9%B4%ED%85%8C%EA%B3%A0%EB%A6%AC.md)

[상품](https://github.com/platfos01/api-document/blob/master/%EC%83%81%ED%92%88.md)

[비회원](https://github.com/platfos01/api-document/blob/master/%EB%B9%84%ED%9A%8C%EC%9B%90.md)

[주문 생성](https://github.com/platfos01/api-document/blob/master/%EC%A3%BC%EB%AC%B8%20%EC%83%9D%EC%84%B1.md)

[주문 성공](https://github.com/platfos01/api-document/blob/master/%EC%A3%BC%EB%AC%B8%20%EC%84%B1%EA%B3%B5.md)

[주문 취소](https://github.com/platfos01/api-document/blob/master/%EC%A3%BC%EB%AC%B8%20%EC%B7%A8%EC%86%8C.md)

- - -

### 주문 프로세스

1. 비회원 API를 이용하여 비회원 생성 (비회원 ID 발급)
2. 주문 생성 API 호출
3. K-STAR 결제
	1. 결제 실패 시 주문완료 API 호출 X
	2. 대기상태의 주문건은 자동으로 삭제됩니다.
4. 주문 완료 API 호출

- - -

### 주문 취소 프로세스

1. 주문 취소 API 호출 (발급된 쿠폰을 먼저 취소해야합니다.)
2. K-STAR 결제 취소