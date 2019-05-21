Network 기본 개념

Network 개요

LAN

WAN

Protocol

OSI 7 layer

 

계층별 Network Devices 인 Repeaters, Hubs, Switch, Bridge, Router 의 기능과 역할

 

Network의 개념과 LAN에서 사용되는 CSMA/CD를 이해할 수 있다.

OSI 7 layer 에서 각 계층별 역할과 장비를 설명할 수 있다.

 

 

Network의 기본 구성

-       논리적으로 나누면, Node, Link, Station 으로 나눌 수 있다.

-       Node : 일반적으로 교환기를 나타낸다.

-       Link : 전송로, 즉 통신회선으로 이해하면 된다.

-       Station(Terminal) : 컴퓨터, 팩스 등의 장비로 실제 운영하는 장비, 즉 Terminal 을 말한다.

![Alt text](https://github.com/kckwon1101/study/blob/master/picture/network/net1.jpg)


Host 간의 통신방식
-       Anycast, Multicast, Broadcast, Unicast 의 4가지 형태로 나눌 수 있다.

-       Unicast : Data Packet을 각 호스트에게 각각 보내는 것이다. 현재의 인터넷은 unicast에 기반을 두고 있다.

-       Anycast : 단일 송신자와 그룹 내에서 가장 가까운 곳에 있는 일부 수신자들 사이의 통신을 말한다. IPv6는 어떤 호스트가 가장 가까이 있는지를 결정할 수 있으며, 마치 unicast 통신인 것처럼 그 호스트에 보낼 수 있다.

-       Multicast : 일-대-다 또는 다-대-다의 전송방식을 말한다. 하나의 소스가 특정 host group에 Data를 전송하는 것.

-       Broadcast : 하나의 source 가 네트워크 상의 모든 호스트에게 data를 전송하는 방식.

LAN(Local Area Network) 이란?

-       LAN은 1975년 미국의 제록스사가 개발한 이더넷(Ethernet) 시스템을 효시로 하여 어느 한정된 공간에서 구성된 Network를 말하며, CSMA/CD 방식으로 동작한다.

-       Ethernet의 전송 프로토콜인 CSMA/CD에 대해 좀 더 알아보자.

CSMA/CD 동작방식

-       CS(Carrier Sense) : 데이터를 보내기 전에 네트워크가 사용 중인지 알아낸다.

-       MA(Multiple Access) : 네트워크가 비어 있으면 누구든 사용 가능하다.

-       CD(Collision Detect) : 메시지를 전달하면서 충돌 여부를 살펴본다.

CSMA/CD 동작원리

1.     데이터를 보내고 싶은 단말은 회선에 다른 신호가 흐르고 있는지 감지한다.

2.     회선에 이미 데이터가 흐르고 있으면 대기한다.

3.     회선에 아무 데이터도 흐르고 있지 않으면 데이터를 보낸다.

4.     내가 보낸 데이터가 잘 나갔으면 전송완료.

*내가 보낸 데이터가 회선으로 나가는 도중에 다른 호스트가 동시에 데이터를 보내서 충돌이 발생했을 때è일정 시간 대기 했다가 다시 보낸다. 충돌된 데이터에 대한 복구는 없음.

WAN(Wide Area Network) 이란?

-       WAN은 공중회선망을 이용한 컴퓨터 네트워크로 광역 네트워크를 뜻하는 wide area network 의 약칭으로, 은행의 온라인 시스템에서 발전했다.

-       WAN과 LAN을 가르는 기준은 일반적으로 LAN케이블로 직접 연결되지 않은 모든 경우를 WAN으로 분류한다. 보다 기술적으로는 공중 전화망(PSTN)이나 공중 데이터망(PSDN)을 경유하는 경우는 WAN연결이라고 할 수 있다.

-       방대한 지역에서 사용자들에게 서비스를 제공하고 종종 일반적인 통신 사업자가 제공하는 전송 서비스를 사용하는 데이터 통신 네트워크를 말한다. 즉, X.25, Frame Relay, ATM, ISDN, FDDI, SONET, Fiber Channel 등을 말한다.

Protocol

-       Protocol은 네트워크 상에서 네트워크로 연결된 컴퓨터끼리 데이터를 주고 받을 수 있도록 미리 약속된 전송규약을 말한다.

-       기능

| 기능 | 내용 |
|:--------|:--------|
|Segmentation (데이터 분할) | 적당한 크기의 패킷 단위로 데이터를 분할하여 데이터의 전송지연 및 손실을 최소화 |
|Framing (프레임의 경계표시)과 Transparency (투명도)|실제 네트워크상에 형성된 링크에 개개의 정보 블록을 전송할 수 있도록 한다.|
|Blocking (정보의 결합)|여러 사용자에 속하는 데이터를 하나의 패킷에 같이 묶어 패킷당 회선 오버헤드를 줄이는 방법|
|Flow control (흐름제어)|송수신국간의 데이터 전송속도를 제어하는 기능|
|Error control (오류제어)|전송 중 발생한 오류를 검증하고 복원하는 방법|
|Sequencing/Ordering (순서제어)|송신측에서 보낸 데이터 순서대로 수신측에서 데이터를 받을 수 있도록 해주는 기능|
|Interrupt (인터럽트)|특정한 action이 즉시 처리될 수 있도록 함|
|Priority and Preemption(우선순위와 선점)|프레임간에 전송 지연이 일어나지 않도록 프레임간에 적절한 우선순위를 부여한다.|
|Connection 확립및 종료|Connection 확립은 상대방이 데이터를 주고 받을 수 있는 상태가 되었음을 의미한다.|
|Addresssing (주소식별)|송수신지 주소를 정확히 명기하여 데이터의 손실이 없도록 함|

 

OSI 7 layer 란?

-       OSI 7 layer는 국제 표준화 기구(ISO)에서 제안한 네트워크 프로토콜의 기준 모델이다.

-       통신망을 통한 상호접속에 필요한 제반 통신절차를 정희하고 이 가운데 비슷한 기능을 제공하는 모듈을 동일계층으로 분할하여 모두 7개층으로 분할한 것을 말한다.

|계층이름|계층단계|레이어|
|:----|:----:|:----:|
|응용계층(application layer)|7계층|upper layer|
|표현계층(presentation layer)|6계층|upper layer|
|세션계층(session layer)|5계층|upper layer|
|전송계층(transport layer)|4계층|lower layer|
|네트워크계층(network layer)|3계층|lower layer|
|데이터링크계층(data link layer)|2계층|lower layer|
|물리계층(physical layer)|1계층|lower layer|

-       왜 OSI 7 layer를 사용하나?

n  Network 표준은 다양한 벤더의 개발과 지원을 가능하도록 한다.

n  서로 다른 network H/W와 S/W간의 통신을 가능하게 한다.

n  한 계층에서의 변화가 다른 계층에 영향을 미치지 않도록 하여, 개발하기 더 쉽게 한다.

n  Network 통신을 더 작은 부분으로 나누어 이해하기 쉽고 개발하기 쉽도록 한다.

-       upper layer의 각 기능과 사용되는 예

n  응용계층

u  사용자의 응용 program 이 네트워크에 접근하는 창구 역할을 수행

u  Telnet, FTP

n  표현계층

u  데이터를 표현, 암호화하는 방식, 데이터 표현을 서로 가능하게 하는 표준인터페이스 제공

u  ASCII, EBCDIC, JPEG

n  세션계층

u  세션을 확립하여 데이터 흐름을 제공하고, 전송 방향을 결정

u  Operation System(OS)

-       lower layer의 각 기능과 사용되는 예

n  전송계층

u  에러 검출, 흐름제어, 사용자간에 연결을 확립하고 유지

u  TCP, UDP, SPX

n  네트워크계층

u  논리적 주소로 최적의 라우팅 경로를 통해 데이터를 전송

u  IP, IPX

n  데이터링크계층

u  MAC address 를 사용해서 장비에 접속, 오류 검출 및 복원, 시작과 끝 인지

u  HDLC, 802.2, 802.3

n  물리계층

u  전송 매체를 통하여 어떤 전기적 신호로 전송할 것인지 결정

u  EIA/TIA-232. V.35

암호화(Encapsulation)는 무엇인고 왜 사용할까?

-       상위 레이어의 데이터가 전송되기 위해서 하위의 각 레이어에서 이해할 수 있는 헤더(header)라는 정보를 붙여서 아래 레이어로 전달하게 된다. 

![Alt text](https://github.com/kckwon1101/study/blob/master/picture/network/net2.jpg)


-       암호풀기(De-encapsulating)은 encapsulation의 반대 개념으로 생각하면 된다.
Layer 1에 속하는 장비

-       physical layer는 장치간의 물리적인 접속을 제어하기 위한 기능을 제공하는 계층으로, 데이터 부호화방식, 신호형식, 데이터 충돌 감지 등을 정의한다.

-       이 계층에는 Repeater 와 Hub 장치가 있다.
![Alt text](https://github.com/kckwon1101/study/blob/master/picture/network/net3.jpg)



Repeater와 Hub 의 장단점
-       Repeater와 Hub는 멀티 포트를 수용하기 위해 많이 사용되는 장비.

-       하지만, 요새는 아래의 장,단점으로 인해 스위치가 더 많이 사용되고, Repeater와 Hub는 network 의 상황에 따라 제한적으로 사용되고 있다.

-       장점

n  장비의 bandwidth 를 각 포트별로 나누어서 사용한다.

n  가격이 저렴하다

n  별도의 config 설정이 필요없다.

-       단점

n  컴퓨터가 늘어나서 hub로 계속 연결하면 collision domain이 늘어나서 통신이 불가할 수도 있다.

layer 2에 속하는 장비

-       data link layer는 정보의 오류와 흐름을 관리하여 안전한 정보의 전달을 수행할 수 있도록 하는 계층.

-       이 계층에는 switch 와 bridge 장치가 있다.

-       switch 와 bridge의 특징

n  collision domain 을 분리할 수 있다.

n  각각의 포트별로 연결된 컴퓨터가 독자적으로 스위치 속도에 따라 보장 가능

n  broadcast 는 모든 segment 로 전송된다.

n  MAC address 기반으로 패킷을 전송

Hub vs. Switching Hub

![Alt text](https://github.com/kckwon1101/study/blob/master/picture/network/net4.jpg)


Layer 3에 속하는 장비
-       network layer는 하나 또는 복수의 통신망을 통하여 컴퓨터나 단말 장치 등의 시스템 간에 데이터 전송을 한다.

-       이 계층에는 Router 장치가 있다.

-       Router는 네트워크와 네트워크 간의 경로(Route)를 설정하고 가장 빠른 길로 트래픽을 이끌어 주는 네트워크 장비이다.

n  경로선택, 최적의 route로 패킷 스위칭 기능

n  logical 주소 사용(Network address)

n  Broadcast domain 분리

-       스위치가 MAC address 를 기반으로 패킷을 전달하는 것처럼, 라우터는 Network address table에 해당하는 routing table 을 기반으로 패킷을 전달한다.

-       static, dynamic routing으로 구분되며, routing table 을 통해 가장 최적의 경로를 찾아낸다.

CSU와 DSU 장비란?

-       CSU/DSU는 근거리 통신망에 사용되는 통신기술로부터 나온 디지털 데이터 프레임들을 광역통신망에 보낼 수 있도록 적절한 프레임으로 변환하는 외장형 모뎀 크기의 하드웨어 장치이다.

-       DSU(Digital Service Unit) : ISDN 등 디지털전화망의 가입자선 전송에 있어 가입자 택내에 설치하는 디지털회선 종단장치를 말한다.

-       CSU(Channel Service Unit) : T1 또는 E1트렁크를 수용할 수 있는 장비로서 각각의 트렁크를 받아서 속도에 맞게 나누어 분할하여 쓸 수 있는 장비이다. 여기서 channel 이란 한 개의 채널에 64kbps 또는 56kbps 의 전송속도를 갖는 것을 말한다. 
