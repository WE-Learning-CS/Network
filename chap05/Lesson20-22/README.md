## 네트워크 주소와 브로드 캐스트 주소의 구조

네트워크 주소와 브로드 캐스트 주소는 컴퓨터에 할당할 수 없는 IP 주소이다.

![Network IP 주소의 특징과 클래스 구조란?](https://media.vlpt.us/images/jkl133/post/6b42fa0e-496e-46f8-a454-3f0d095d9e82/image.png)

출처 : https://www.google.co.kr/url?sa=i&url=https%3A%2F%2Fdevlog-wjdrbs96.tistory.com%2F287&psig=AOvVaw2nd8hwCZJ7JLbKjyWdJ1tP&ust=1639752927692000&source=images&cd=vfe&ved=0CAwQjhxqFwoTCKDGzujJ6PQCFQAAAAAdAAAAABAD

### 네트워크 주소

- 호스트 ID 가 10진수로 0이고, 2진수면 00000000인 주소
- 전체 네트워크에서 작은 네트워크를 식별하는 데 사용
- 호스트 ID가 10진수로 0이면 그 네트워크 전체를 대표하는 주소가 된다

### 브로드 캐스트 주소

- 호스트 ID 가 10진수로 255이고, 2진수면 11111111인 주소
- 네트워크에 있는 컴퓨터나 장비 모두에게 한번에 데이터를 전송하는데 사용되는 전용 IP 주소

## 서브넷의 구조

네트워크를 분할하는 것을 서브넷팅이라고 한다.

![img](https://t1.daumcdn.net/cfile/tistory/99CC58465BF1066636)

출처 : http://korean-daeddo.blogspot.com/2016/01/blog-post_26.html

### 서브넷팅

- 네트워크를 분할하는 것

### 서브넷

- 분할된 네트워크
- IP 주소에서 네트워크 영역을 부분적으로 나눈 망, 부분 네트워크

### 예시

``` markdown
// A 클래스를 서브넷팅 하기 전
000000001 00000000 00000000 00000000
네트워크 ID |         호스트 ID

// A 클래스를 서브넷팅 한 후
000000001 00000000 00 000000 00000000
네트워크 ID | 서브넷 ID  |  호스트 ID
```

호스트 ID에서 비트를 빌려 서브넷 ID로 바꿈

## 서브넷 마스크

IP 주소를 서브넷팅 하면 어디까지가 네트워크 ID 이고, 어디부터가 호스트 ID인지 판단하기 어려울 때가 있다.
그럴 때 사용하는 것이 **서브넷 마스크**이다

- 네트워크 ID와 호스트 ID를 식별하기 위한 값

![Crocus](https://t1.daumcdn.net/cfile/tistory/9926943C5BB8ED8F2F)

출처 : https://www.crocus.co.kr/1379

### 프리픽스 표기법

- 서브넷 마스크를 슬래시(/비트  수)로 나타낸 것.
- 사진에서 /8, /16 등

## 라우터의 구조

서로 다른 네트워크와 통신하기 위해 필요한 라우터

### 라우터

<img src="https://lh3.googleusercontent.com/proxy/NZ_pYfv4lvHokN_KlaUTqX_qIZKJHkX_A9J-tcVbOjY_M_wVSUG_N9TBYLMwFJPfMi-hzzoKil4EEglFHh-aaQ" alt="라우터란? 작동원리" style="zoom:200%;" />

출처 : https://www.google.co.kr/url?sa=i&url=http%3A%2F%2Fwww.deadfire.net%2Ftcpip%2Ftcpip08.html&psig=AOvVaw3iUXnJtUOizCZAklp_WX7u&ust=1639751315587000&source=images&cd=vfe&ved=0CAwQjhxqFwoTCPjJj-vD6PQCFQAAAAAdAAAAABAD

- 네트워크 계층을 통해 다른 네트워크로 데이터를 전송하는데 필요한 장비
- 패킷을 추출하여 데이터의 목적지가 정해지면 해당 목적지까지 어떤 경로로 가는 것이 좋은지 알려주는 기능을 제공
- 네트워크를 식별할 수 있는 IP주소가 필요
- LAN과 LAN을 연결하거나 LAN과 WAN을 연결하기 위한 인터넷 네트워킹 장비

### 기본 게이트 웨이

- 네트워크를 분할 한 다음 컴퓨터가 다른 네트워크로 접속하기 위해 라우터의 IP 주소를 설정하는 것
- 네트워크의 출입구를 설정하는 것
- 컴퓨터가 다른 네트워크로 데이터를 보낼 때 어디로 전송해야 하는 지 알지 못하므로 네트워크 출입구를 지정하고 일단은 라우터로 데이터를 전송

### 라우팅

- 경로 정보를 기반으로 현재의 네트워크에서 다른 네트워크로 최적의 경로를 통해 데이터를 전송하는 것

### 라우팅 테이블

- 경로 정보가 등록되어 있는 테이블
- 소규모 네트워크에 적합한 네트워크 관리자가 수동으로 등록하는 방법과, 대규모 네트워크에 적합한 자동으로 등록하는 방법이 있다.

### 라우팅 프로토콜

- 라우터 간에 라우팅 정보를 교환하기 위한 프로토콜
- 라우팅 프로토콜을 설정하여 라우터 간에 경로 정보를 서로 교환하고 라우팅 테이블에 등록해 나가는 것
- RIP, OSPF, BGP 등이 있다.

| 프로토콜 | 설명                                                         |
| :------: | :----------------------------------------------------------- |
|   RIP    | - 최초의 라우팅 프로토콜<br />- 거리 벡터 알고리즘 활용 <br />- 30초 주기로 전체 라우팅 정보를 갱신 <br />- 변화 업데이트 시 많은 시간이 소요<br />- 라우팅 루프 발생 가능 |
|   IGRP   | - RIP의 문제점 개선을 위해 시스코에서 개발 <br />- 네트워크 상태를 고려하여 라우팅(대역폭, 속도 등) |
|   OSPF   | - 링크 상태 알고리즘을 사용<br />- 발생한 변경 정보에 대해 RIP 보다 빠른 업데이트<br />- 토폴로지에 대한 정보가 전체 라우터에 동일하게 유지 |
|   BGP    | - 규모가 큰 네트워크의 상호 연결<br />- 대형 사업자(ISP)간의 상호 라우팅 |










