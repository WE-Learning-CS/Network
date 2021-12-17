# 네트워크 계층의 역할

## 네트워크 간의 연결 구조

데이터 링크 계층에서는 이더넷 규칙을 기반으로 데이터의 전송을 담당하는데, 이 규칙에 따라 같은 네트워크에 있는 컴퓨터로는 데이터를 전송할 수 있지만 인터넷이나 다른 네트워크로는 데이터를 전송할 수 없다.

즉, 데이터 링크 계층의 기능만으로는 해당 네트워크 안에서만 통신이 가능하다.

네트워크 계층은 네트워크 간의 통신을 가능하게 한다.

### 라우터

<img src="https://lh3.googleusercontent.com/proxy/NZ_pYfv4lvHokN_KlaUTqX_qIZKJHkX_A9J-tcVbOjY_M_wVSUG_N9TBYLMwFJPfMi-hzzoKil4EEglFHh-aaQ" alt="라우터란? 작동원리" style="zoom:200%;" />

출처 : https://www.google.co.kr/url?sa=i&url=http%3A%2F%2Fwww.deadfire.net%2Ftcpip%2Ftcpip08.html&psig=AOvVaw3iUXnJtUOizCZAklp_WX7u&ust=1639751315587000&source=images&cd=vfe&ved=0CAwQjhxqFwoTCPjJj-vD6PQCFQAAAAAdAAAAABAD

- 네트워크 계층을 통해 다른 네트워크로 데이터를 전송하는데 필요한 장비
- 패킷을 추출하여 데이터의 목적지가 정해지면 해당 목적지까지 어떤 경로로 가는 것이 좋은지 알려주는 기능을 제공
- 네트워크를 식별할 수 있는 IP주소가 필요
- LAN과 LAN을 연결하거나 LAN과 WAN을 연결하기 위한 인터넷 네트워킹 장비

### 라우팅

- 데이터를 어떤 경로로 보낼지도 결정하는 것
- 원하는 목적지까지 지정된 데이터가 안전하게 전달되도록 함

### 라우팅 테이블

- 경로 정보를 등록하고 관리

## IP

네트워크 계층에서는 캡슐화 할 때 IP 헤더를 붙인다.

### IP 헤더의 구조

![IP 헤더 구조, IP 패킷 구조, IP 헤더 패킷 구조](https://t1.daumcdn.net/cfile/tistory/2310AD4551B6E9462B)

출처 : https://www.google.co.kr/url?sa=i&url=https%3A%2F%2Fthemangs.tistory.com%2Fentry%2FIP-%25ED%2597%25A4%25EB%258D%2594-%25EA%25B5%25AC%25EC%25A1%25B0-IP-%25ED%258C%25A8%25ED%2582%25B7-%25EA%25B5%25AC%25EC%25A1%25B0-IP-%25ED%2597%25A4%25EB%258D%2594-%25ED%258C%25A8%25ED%2582%25B7-%25EA%25B5%25AC%25EC%25A1%25B0&psig=AOvVaw1VYDS5b5yJFg3kCGtpr4ln&ust=1639751369470000&source=images&cd=vfe&ved=0CAwQjhxqFwoTCOj8nILE6PQCFQAAAAAdAAAAABAD

### IP 패킷

- IP 프로토콜을 사용하여 캡슐화 할때 데이터에 IP 헤더가 추가되어 만들어진 것

## IP 주소의 구조

- IP 주소는 인터넷 서비스 제공자(ISP)에게서 받을 수 있다.

### IPv4

![IPv4 헤더](https://lh3.googleusercontent.com/proxy/uDSksHpNHr916eR2dkkm1CJ89DtUdv3zrWbbCMtUJDGAxDQ5Gh0c_I0Aq9_9MaJkbrQg0p66i3MQ-SUXar-WR1eD2Q)

출처 : https://www.google.co.kr/url?sa=i&url=http%3A%2F%2Fwww.ktword.co.kr%2Ftest%2Fview%2Fview.php%3Fm_temp1%3D1859&psig=AOvVaw1nYxItMR7UjZw4jWLzfzGb&ust=1639751616249000&source=images&cd=vfe&ved=0CAwQjhxqFwoTCJj5sPfE6PQCFQAAAAAdAAAAABAD

- 인터넷에서 사용되는 패킷 교환 네트워크상에서 데이터를 교환하기 위한 32비트 주소 체계를 갖는 네트워크 계층의 프로토콜
- 32비트로 되어있어 IP주소를 약 43억개 만들 수 있다

**IPv4 헤더**

- IP 패킷의 앞부분에서 주소 등 각종 제어 정보를 담고있는 부분
- 헤더의 사이즈는 옵션 미 지정시 최소 20 바이트 이상

### IPv6

- 인터넷 프로토콜 스택 중 네트워크 계층의 프로토콜로서 버전 6 인터넷 프로토콜로 제정된 차세대 인터넷 프로토콜을 말한다.
- 128비트로 되어있어 IP주소를 약 340간 개 만들 수 있다

**IPv6의 특징**

- IP주소의 확장 : 128비트의 주소 공간을 제공
- 이동성 : IPv6호스트는 네트워크의 물리적 위치에 제한받지 않고 같은 주소를 유지하면서도 자유롭게 이동 가능
- 인증 및 보안 기능 : 패킷 출처 인증과 데이터 무결성 및 비밀 보장 기능을 IP 프로토콜 체계에 반영, IPSEC 기능 적용
- 개선된 QoS지원 : 흐름 레이블 개념을 도입, 특정 트래픽은 별도의 특별한 처리(실시간 통신 등)를 통해 높은 품질의 서비스 제공
- Plug & Play 지원 : IPv6호스트는 IPv6 네트워크에 접속하는 순간 자동적으로 네트워크 주소를 부여받음
- Ad-hoc 네트워크 지원 : Ad-hoc네트워크를 위한 자동 네트워킹 및 인터넷 연결 지원
- 단순 헤더 적용 : IP 패킷의 처리를 신속하게 할 수 있도록 고정 크기의 단순 헤더를 사용하는 동시에, 확장 헤더를 통해 기능에 대한 확장 및 옵션 기능의 사용이 용이한 구조
- 실시간 패킷 추적 가능 : 흐름 레이블을 사용하여 패킷의 흐름을 실시간 제공

### 네트워크 ID

- 어떤 네트워크인지 나타냄

### 호스트 ID

- 해당 네트워크의 어느 컴퓨터인지 나타냄

## IP 주소의 클래스 구조

IP주소는 네트워크의 규모에 따라 A~E 클래스로 나누어져 있다

### IP 주소 클래스

- 네트워크 크기를 클래스라는 개념으로 구분

| 클래스 이름 |          내용          |
| :---------: | :--------------------: |
|  A 클래스   |  대규모 네트워크 주소  |
|  B 클래스   |   중형 네트워크 주소   |
|  C 클래스   |  소규모 네트워크 주소  |
|  D 클래스   |    멀티캐스트 주소     |
|  E 클래스   | 연구 및 특수 용도 주소 |

- 일반 네트워크에서는 A~C 클래스 까지 사용 가능하다.

![Network IP 주소의 특징과 클래스 구조란?](https://yohanpro.com/media/images/network/class-2.png)

![ip](https://yohanpro.com/media/images/network/class-3.png)

출처 : https://devlog-wjdrbs96.tistory.com/287