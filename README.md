# Network TCP/IP 교과서
- [Chapter 01. What is TCP/IP?](#chapter-01-what-is-tcpip)
- [Chapter 02. How does TCP/IP work?](#chapter-02-how-does-tcpip-work)
- [Chapter 03. Network Access Layer](#chapter-03-network-access-layer)
- [Chapter 04. Internet Layer](#chapter-04-internet-layer)
- [Chapter 05. Subnetting and CIDR](#chapter-05-subnetting-and-cidr)
- [Chapter 06. Transport Layer](#chapter-06-transport-layer)
- [Chapter 07. Application Layer](#chapter-07-application-layer)
- [Chapter 08. Routing](#chapter-08-routing)
- [Chapter 09. Connecting](#chapter-09-connecting)
- [Chapter 10. Name Check](#chapter-10-name-check)
- [Chapter 11. Firewall](#chapter-11-firewall)
- [Chapter 12. Configuring](#chapter-12-configuring)
- [Chapter 13. Next IPv6](#chapter-13-next-ipv6)
- [Chapter 14. Classic Tool](#chapter-14-classic-tool)
- [Chapter 15. Classic Service](#chapter-15-classic-service)
- [Chapter 16. Detail of Internet](#chapter-16-detail-of-internet)
- [Chapter 17. HTTP, HTML and World Wide Web](#chapter-17-http-html-and-world-wide-web)
- [Chapter 18. Web Service](#chapter-18-web-service)

## Chapter 01. What is TCP/IP?
### 퀴즈
1. 네트워크 프로토콜은 무엇입니까?
- 네트워크 통신의 복잡한 과정을 규정하는 공통 규칙 시스템
- 컴퓨터 애플리케이션 TO 수신하는 애플리케이션까지의 데이터 전송 과정 안내
- 애플리케이션 > 운영 체제의 네트워크 요소 > 네트워크 하드웨어 > 전송 매체 > 대상 컴퓨터의 네트워크 하드웨어 > 대상 컴퓨터의 운영체제 > 수신 애플리케이션

2. 분산 방식으로 작동하게 하는 TCP/IP의 두 가지 기능은 무엇입니까?  
- 엔드 노드 검증: 메시지를 전달하는 체인의 양쪽 끝에 있는 노드 검증
- 동적 라우팅: 현재 상태를 기반으로 경로를 선택

3. 도메인 이름을 IP 주소에 매핑을 담당하는 시스템은 무엇입니까?
- DNS(Domain Name System)
- Name Resolution: 도메인 이름을 IP 주소로 매핑
- Name Server: 도메인 이름을 IP 주소로 변환하는 방법을 보여주는 표를 저장하고 있는 컴퓨터

4. RFC는 무엇입니까?
- Request For Comment
- TCP/IP 및 인터넷 관련 정보를 제공하는 일련의 공식 문서
- 작업 그룹의 인터넷 표준 및 보고서 포함
- IETF 공식 사양 게재

5. 포트는 무엇입니까?
- 네트워크 > 애플리케이션으로의 인터페이스
- 논리적 채널 시스템
- 프로토콜 소프트웨어로 데이터가 이동하는 컴퓨터의 논리적 파이프라인


## Chapter 02. How does TCP/IP work?
### 퀴즈
1. TCP/IP 네트워크 접근 계층에 대응되는 두 개의 OSI 계층은 무엇입니까?
- 데이터 링크 계층: 네트워크 어댑터와 인터페이스 제공 / 서브넷의 논리적 링크 유지
- 물리 계층: 데이터를 실제 전송 매체를 지나는 전기 또는 아날로그 펄스 스트림으로 변환 / 데이터 전송 감독
- 통신 매체 접근과 관련된 기능에서 통신 구성과 관련된 기능을 분리

2. 한 네트워크 세그먼트에서 다른 네트워크 세그먼트로 데이터를 라우팅하는 데 어떤 TCP/IP 계층이 있습니까?
- 인터넷 계층: 물리적 아키텍처가 다른 서브넷 간에 데이터 전달 / 하드웨어와 독립적인 주소 지정

3. TCP와 비교할 때 UDP의 장단점은 무엇입니까?
- 장점: 추가 오류 확인 및 흐름 제어가 TCP보다 빠름
- 단점: 더 많은 오류 제어 책임을 애플리케이션으로 넘기므로 신뢰도가 낮음


4. 계층과 데이터를 캡슐화한다는 것은 무엇을 의미합니까?
- 캡슐화 Encapsulation
- 수신 시스템에 상응하는 계층 관련 데이터를 정보 계층에 추가
- 수신 컴퓨터 계층의 정보가 포함된 헤더를 포함

### 연습문제
1. TCP/IP 스택에서 각 계층이 수행하는 기능을 나열하세요
- 네트워크 접근 계층: 물리적 네트워크와 인터페이스 제공, 전송 매체의 데이터를 포맷하고 물리적 하드웨어 주소 기반의 서브넷 데이터 처리, 실제 네트워크에서 전달되는 데이터에 대한 오류 제어 기능
- 인터넷 계층: 하드웨어와 독립적으로 주소를 지정하는 기능, 물리적 아키텍처가 다른 서브넷 간에 데이터 전달
- 전송 계층: 인터네트워크에 대한 흐름 제어, 오류 제어 및 승인 서비스 담당, 네트워크 애플리케이션을 위한 인터페이스 역할
- 응용 계층: 네트워크 문제 해결, 파일 전송, 원격 제어 및 인터넷 활동을 위한 애플리케이션 제공, API 지원

2. 데이터그램을 다루는 계층을 나열하세요.
- 전송 계층, 인터넷 계층

3. 새로 발명된 유형의 네트워크 하드웨어를 사용하기 위해 TCP/IP를 어떻게 변경해야 하는지 설명하세요.
- 모듈식 설계로 되어 TCP/IP 소프트웨어 패키지를 구축할 필요 없음
- 네트워크접근 계층만 변경하면 됨

4. TCP가 신뢰할 수 있는 프로토콜이라는 말의 의미를 설명하세요.
- 연결 지향 프로토콜로 데이터 전달을 보장하기 위해 많은 노력을 기울임
- 정교한 흐름 제어 및 오류 제어 제공


## Chapter 03 Network Access Layer
### 정리
TCP/IP 프로토콜 스택  
- 네트워크 접근 계층
- 서비스 모음
- 네트워크 하드웨어에 대한 접근을 관리 및 제공하는 사양

네트워크 접근 계층
- 컴퓨터의 네트워크 어댑터와 인터페이스
- 적절한 접근 방법의 규칙을 통한 데이터 전송 조정
- 데이터를 전송 매체를 지나는 전기 또는 아날로그 펄스 스트림으로 변환
- 수신 데이터의 오류 확인
- 수신 컴퓨터가 데이터의 오류를 확인할 수 있게 발신 데이터에 오류 검사 정보 추가
- TCP/IP 네트워크 접근 계층 = OSI 물리 계층, 데이터 링크 계층(미디어 접근 제어, 논리 링크 제어)

네트워크 아키텍처
- LAN 유형, LAN 토폴로지
- 미디어 접근, 물리 주소 지정 및 컴퓨터와 전송 매체의 상호 작용 제어
- 접근 방법: 전송 매체를 공유하는 방법을 정의하는 일련의 규칙
- 데이터 프레임 형식: IP 수준 데이터그램은 미리 정의된 형식의 데이터 프레임으로 캡슐화
- 케이블 연결 유형: 어댑터가 전송하는 비트 스트림의 전기적 특성과 같은 특정 기타 설계 매개변수에 영향
- 케이블 연결 규칙: 프로토콜, 케이블 유형 및 전기적 특성은 케이블 및 케이블 커넥터 사양의 최대 및 최소 길이에 영향
- 하드웨어와의 상호 작용에 대한 모든 세부 사항이 네트워크 접근 계층에서 발생

물리 주소
- 네트워크 소프트웨어 계층은 논리IP주소와 네트워크 어댑터의 실제 영구 물리 주소를 연결하는데 필요
- 물리 주소 지정은 MAC 하위 계층이 담당 / 물리주소(=MAC 주소)
- TCP/IP는 ARP 및 RARP를 사용하여 IP 주소를 네트워크 어댑터의 물리 주소와 연결

이더넷
- LAN
- 저렴하고 쉽게 설치 가능
- 동급 무선 기술보다 빠르며, 스누핑 및 무선 네트워크와 관련된 기타 보안 문제에 대한 기본적인 보안 장벽 제공
- CSMA/CD(Carrier Sense Multiple Access with Collision Detection) 반송파 감지 다중 접속/충돌 감지
- 전송 매체를 모니터에 전송하기 전에 사용 가능한 회선이 있을 때까지 대기, 충돌 발생 시 중지되어 대기했다가 다시 전송

이더넷 프레임
- 네트워크 접근 계층 소프트웨어는 인터넷 계층에서 데이터그램을 받아 해당 데이터를 실제 네트워크 사양과 일치하는 형식으로 변환
- 네트워크 어댑터 카드의 하드웨어를 통해 전송할 데이터를 형식화
1) 필요하다면 데이터 필드에 전송되는 작은 조각으로 분리
2) 데이터 조각을 프레임으로 패키징(프리앰블, 수신자 주소, 소스 주소, 선택적 VLAN 태그, 길이, 데이터, 프레임 검사 순서)

### 퀴즈
1. CRC는 무엇입니까?  
- Cyclic Redundancy Check 주기적 덧붙임 검사
- 데이터 프레임의 내용을 확인하는데 사용되는 체크섬 계산

2. 이더넷 네트워크에서 충돌 감지란 무엇입니까?  
- CD(Collision Detection)
- 이더넷에서 사용하는 네트워크 접근 방법
- 두 대의 컴퓨터가 동시에 전송을 시도하면 충돌이 발생하는데, 이때 컴퓨터는 일시 중지되어 임의의 시간 동안 대기했다가 다시 전송

3. 이더넷 물리 주소는 얼마나 큽니까?  
- 48비트

4. ARP가 하는 일은 무엇입니까?
- IP 주소를 로컬 네트워크에 있는 네트워크 어댑터의 물리 주소와 연결
- 사용자가 보는 논리 IP 주소와 LAN에 사용되는 보이지 않는 하드웨어 주소를 연결

### 연습문제
1. 물리 주소와 IP 주소를 연결하는 두 가지 프로토콜을 나열하세요.  
- ARP, RARP
- ARP(Address Resolution Protocol) 주소 확인 프로토콜
- RARP(Reverse Address Resolution Protocol) 역 ARP

2. 최소 세 가지 네트워크 아키텍처를 나열하세요.  
- LAN(유선), WAN(무선), 인터넷(WAN의 일종, 전세계의 LAN을 연결)

3. OSI 매체 접근 제어 및 논리 링크 제어 계층이 수행하는 기능을 설명하세요.  
- MAC(Media Access Control): 네트워크 어댑터와의 인터페이스를 제공
- LLC(Logical Link Control): 서브넷을 통해 전달된 프레임의 오류를 검사, 서브넷에서 통신하는 장치 간의 링크를 관리


## Chapter 04 Internet Layer
### 정리
IP 주소
- DHCP 서버를 통해 자동으로 IP 주소를 받음
- 네트워크 주소 변환 기술로 인하여 더는 인터넷 IP 주소 계층에 귀속되지 않아도 됨
- 그러나 실제 네트워커의 컴퓨터는 여전히 이 규칙을 사용해 패킷을 전달하고 라우팅 결정을 내림

주소 지정 및 전달
- 네트워크 어댑터 카드와 같은 네트워크 인터페이스 장치를 통해 네트워크와 통신
- 네트워크 인터페이스 장치는 고유한 물리 주소를 가지며, 해당 주소로 전송된 데이터를 수신하도록 설계
- 상위 계층의 세부 사항을 모르고 단지 프레임을 수신하면서 자체 물리 주소로 지정된 프레임을 기다리다가, 들어오면 해당 프레임을 프로토콜 스택으로 전달
- 라우팅된 네트워크에서는 물리 주소로 데이터를 전달할 수 없음
- TCP/IP는 물리 주소를 가리고 논리적, 계층적 주소 지정 체계를 중심으로 네트워크를 구성
- IP 프로토콜: 논리 주소 지정 체계 유지/IP 주소
- ARP: IP 주소를 물리 주소로 매핑하는 테이블 구성

1) 대상 주소가 소스 컴퓨터와 동일한 네트워크 영역에 있다면, 소스 컴퓨터는 대상에게 패킷을 직접 보냄
- ARP를 사용해 IP 주소와 물리 주소 확인
- 데이터는 대상 네트워크 어댑터로 전달
2) 대상 주소가 소스 컴퓨터와 다른 영역에 있으면, 아래 프로세스 실행
- 데이터그램은 게이트웨이(데이터 그램을 다른 네트워크 영역으로 전달하는 로컬 네트워크 영역 장치)로 전달
- ARP를 사용해 게이트웨이 주소를 물리 주소로 확인하고 데이터는 게이트웨이의 네트워크 어댑터로 전송
3) 데이터그램은 게이트웨이를 통해 상위 수준의 네트워크 영역으로 라우팅되며, 프로세스 반복
- 대상 주소가 새 영역에 있으면 데이터가 해당 대상으로 전달, 없으면 다른 게이트웨이로 전송
4) 데이터그램은 게이트웨이 체인을 통해 대상 영역으로 전달
- 대상 IP 주소는 ARP를 통해 물리 주소에 매핑, 데이터는 대상 네트워크 어댑터로 보냄

인터넷 계층 프로토콜
- 로컬 네트워크 컴퓨터 식별
- 게이트웨이를 통해 메시지를 보낼 때를 결정하는 수단 제공
- 대상 네트워크 영역을 식별하는 하드웨어로부터 독립적인 수단 제공
- 논리적 IP 주소를 물리 주소로 변환해 데이터를 대상 컴퓨터의 네트워크 어댑터로 전달할 수 있는 수단 제공

인터넷 프로토콜
- 하드웨어로부터 독립적인 계층적 주소 지정 시스템 제공
- 복잡하게 라우팅된 네트워크에서 데이터를 전달하는데 필요한 서비스 제공
- IP = 네트워크 ID + 호스트 ID
- 클래스A / 클래스B / 클래스C
- 서브네팅을 통해 확장

IP 헤더 필드
- TCP/IP 소프트웨어는 IP 헤더에 포함된 정보를 사용해 데이터그램 처리
- 최소 크기는 20바이트
- 버전, IHL, 서비스 유형, 총 길이, 식별자, 플래그, 프래그먼트 오프셋, TTL, 프로토콜, 헤더 체크섬, 소스 IP 주소, 대상 IP 주소, IP 옵션, 패딩, IP 데이터 페이로드

IP 주소
- IP 주소는 32비트 2진 주소
- 옥텟이라고 하는 4개의 8비트 영역으로 세분화

주소 클래스 시스템
- 클래스 A 주소: 네트워크 8비트, 호스트 24비트, 2진 주소가 0으로 시작
- 클래스 B 주소: 네트워크 16비트, 호스트 16비트, 2진 주소가 10으로 시작
- 클래스 C 주소: 네트워크 24비트, 호스트 8비트, 2진 주소가 110으로 시작

특별한 IP 주소
- 127로 시작하는 주소는 루프백 > 로컬 소프트웨어에 의해 자신에게 전송됨

주소 확인 프로토콜
- ARP 
- 인터넷 계층 프로토콜을 사용해 IP 주소를 물리 주소에 매핑
- 모든 세부 사항이 사용자가 거의 볼 수 없게 구현
- 각 호스트는 ARP 테이블, ARP 캐시라는 메모리상의 테이블 유지
- ARP 캐시를 검사해 수신자의 물리 주소 결정
- ARP 캐시는 동적으로 조립됨
- 역 ARP: 물리 주소는 알지만 IP 주소는 알 수 없을 때 사용함 / BOOTP 프로토콜과 함께 사용

인터넷 제어 메시지 프로토콜
- ICMP Internet Control Message Protocol
- 라우터는 ICMP를 통해 문제를 소스 IP에 알림
- 에코 요청 및 에코 응답
- 소스 퀀치
- 도달 불가 목적지
- 시간 초과
- 조각화 필요

### 퀴즈
1. IP 헤더에서 TTL 필드의 목적은 무엇입니까?  
- Time to Live
- 데이터그램이 삭제되기 전에 존속할 수 있는 시간 또는 라우터 홉
- 라우터 내부에서 데이터그램이 지연되는 시간(초)만큼 TTL 필드 값을 감소시킴

2. 클래스 A 주소의 네트워크 및 호스트 ID 필드는 얼마나 됩니까?  
- 네트워크 8비트, 호스트 24비트

3. 옥텟은 무엇입니까?  
- 컴퓨팅에서 8개의 비트가 하나로 모인것. IP 주소는 총 4개의 옥텟으로 구성됨

4. IP 주소는 무엇입니까?  
- 32비트의 2진 주소
- Internet Protocol Address
- 컴퓨터 네트워크에서 장치들이 서로를 인식하고 통신을 하기 위해 사용하는 특수한 번호

5. ARP와 RARP의 차이점은 무엇입니까?  
- ARP는 IP 주소를 알고, 물리 주소를 모를 때 IP 주소를 물리 주소와 매핑
- RARP는 물리 주소를 알고, IP 주소를 모를 때 물리 주소를 IP 주소와 매핑

### 연습 문제
1. 다음 2진수 옥텟을 10진수로 변환하세요.  
00101011 - 32 + 8 + 2 + 1 = 43  
01010010 - 64 + 16 + 2 = 82  
11010110 - 128 + 64 + 16 + 4 + 2 = 214  
10110111 - 128 + 32 + 16 + 4 + 2 + 1 = 183  
01001010 - 64 + 8 + 2 = 74  
01011101 - 64 + 16 + 8 + 4 + 1 = 93  
10001101 - 128 + 8 + 4 + 1 = 141  
11011110 - 128 + 64 + 16 + 8 + 4 + 2 = 222  

2. 다음 10진수를 2진수 옥텟으로 변환하세요.  
13 = 00001101  
184 = 10111000  
238 = 11101110  
37 = 00100101  
98 = 01100010  
161 = 10100001  
243 = 11110011  
189 = 10111101  

3. 다음 32비트 IP 주소를 점으로 분리된 10진수 표기법으로 변환하세요.  
11001111 00001110 00100001 = 207.14.33  
01011100 00001010 00001101 = 92.10.13  
01011001 01001101 10111101 = 89.77.189  
10010011 01010101 01100001 = 147.85.97  

## Chapter 05. Subnetting and CIDR
### 정리
서브넷 
- subnet
- 데이터그램이 작은 주소 공간을 제공하는 라우터에 도달할 수 있게 클래스 수준의 네트워크를 세분화한 '단위'

서브넷팅
- subnetting
- 기존 주소 클래스 시스템은 네트워크 수준 아래의 주소 공간을 논리적으로 세분화하지 않았음 > 서브넷팅을 통해 보완
- 데이터를 효율적으로 전달하기 위해 주소 공간을 더 작은 네트워크 영역으로 세분화
- 호스트와 라우터가 IP 주소를 통해 어떤 네트워크 영역에 전달돼야 하는지 판단
- 논리적 계층의 두 번째 계층 제공
- 데이터 그램 > (라우터) > 네트워크 내 서브넷 주소 > (ARP) > 물리 주소로 변환

서브넷 마스크
- subnet mask 매개변수
- 호스트 ID에서 비트를 빌려 서브넷 주소로 지정
- 32비트 2진수 / 서브넷ID를 나타내는 패턴으로 정렬
- IP 주소를 읽기 위한 지도
- 데이터그램 > (네트워크ID) > 네트워크에 라우팅
- 네트워크 내 데이터그램 > (서브넷ID) > 서브넷에 라우팅
- 서브넷 내 데이터그램 > (호스트ID) > 지정 컴퓨터에 전달
- 신중히 계산, 네트워크 내부 구성 반영, 동일 서브넷 내 모든 호스트는 동일한 서브넷ID와 서브넷 마스크, 10진 표기법
- 네트워크ID + 서브넷ID는 1로 표기, 호스트ID는 0으로 표기

CIDR 
- 클래스리스 인터도메인 라우팅 Classless Inter-Domain Routing
- 라우터 구성과 전문적인 네트워크 문맥
- 서브넷 마스크 대체
- 라우팅 테이블에서 주소 항목의 확산을 제한할 필요가 생겨 등장
- IP 주소 공간을 집계하고 세분화하도록 균일한 수단을 제공하는 라우팅 표기법
- 라우팅 테이블의 주소 블록을 정의, 유동적이고 유연함
- CIDR 접두사: VLSM(variable-length subnet mask) 사용

CIDR 접두사
- VLSM variable-length subnet mask, supernet mask
- 단일 숫자
- 네트워크/서브넷 ID 역할을 하는 주소 내의 비트 수 지정
- 모든 호스트에 대해 공유되는 IP 주소의 선행 비트 수 정의
- 여러개의 연속된 네트워크를 하나의 항목으로 집계할 수 있게 함

### 퀴즈
1. 서브넷 ID 비트는 어디에서 왔습니까?  
: 호스트 ID에서 빌려옴. 서브넷 마스크를 통해 할당된 비트 확인 가능

2. 예전과 달리 지금 서브넷이 중요하지 않은 이유는 무엇입니까?  
: 네트워크를 클래스만으로 구분시 한계가 있음. 이를 극복하고 서브넷을 대체할 CIDR이 등장하여 서브넷의 중요도가 떨어짐

3. CIDR간 라우팅에서 클래스리스란 무엇을 의미합니까?  
: 네트워크ID로 사용할 범위를 클래스에 국한하지 않고 자유롭게 표기함

4. /26 네트워크에 몇 개의 호스트가 있을 수 있습니까?  
: 2^6 = 64개

5. 작은 네트워크 여러 개를 더 큰 단일 네트워크 범위로 통합하는 것은 무엇입니까?  
: 슈퍼넷팅 Supernetting 여러 라우팅을 하나의 라우팅으로 집계, 요약

### 연습 문제
1. 네트워크 주소 180.4.0.0에서 180.7.255.255를 단일 네트워크로 결합하면 얻을 수 있는 CIDR 네트워크 주소를 계산하세요.  
: 180.4.0.0/18

2. 서브넷 마스크가 255.255.255.244인 경우 서브넷 192.100.50.192에서 가능한 호스트 수를 결정하세요.  
: 11111111 11111111 11111111 11110100 (불가능한 마스크)  
  11111111 11111111 11111111 11111100 으로 계산할 경우 4개(실질적으로 00,11 제외하고 2개)  
  11111111 11111111 11111111 11110000 으로 계산할 경우 16개(실질적으로 0000, 1111 제외하고 14개)  

3. 연습 문제 2번에서 주어진 서브넷 마스크로 가능한 서브넷 수를 계산하세요. (244를 252로 간주)  
: 클래스A일 경우 2^22, 클래스 B일 경우 2^14, 클래스 C일 경우 2^6

4. 네트워크 195.50.100.0/23에서 호스트를 나타내는 가장 낮은 IP 주소를 결정하세요.  
: 195.50.100.0  

5. 연습 문제 4번에서 호스트를 나타내는 최상위 IP 주소를 찾으세요.  
: 195.50.101.255

## Chapter 06. Transport Layer
### 정리
전송 계층
- 네트워크 애플리케이션 인터페이스: 대상 컴퓨터에서 작동하고 있는 특정 애플리케이션에 데이터 전송
- 다중화 multiplexing: 서로 다른 애플리케이션과 컴퓨터에서 데이터를 받아 해당 데이터를 수신 컴퓨터의 애플리케이션에 전달
- 역다중화 demultiplexing: 하나의 컴퓨터에서 여러 네트워크 애플리케이션을 동시에 지원
- 오류 검사, 흐름 제어, 검증

품질 보증
- TCP(전송 제어 프로토콜): 광범위한 오류 제어와 흐름 제어 기능 제공, 연결 지향
- UDP(사용자 데이터그램 프로토콜): 기본적인 오류 검사 제공, 비연결 프로토콜

연결 지향
- 연결 지향: 통신하는 컴퓨터 간의 연결을 설정 및 유지, 연결 상태 모니터링
- 비연결: 단방향 데이터그램을 보내고 알리지 않음

포트 port
- 애플리케이션에서 전송 계층으로 또는 전송 계층에서 애플리케이션으로 이어진 통로 역할을 하는 사전 정의된 내부 주소
- 컴퓨터 > 네트워크 접근 계층 > 인터넷 계층 > TCP 포트 21 > FTP

소켓 socket
- IP 주소 + 포트 번호

잘 알려진 포트
- IANA(인터넷 할당 번호 관리 기관) 제공, ICANN(국제 인터넷 주소 관리 기구) 관리 123pg 참조

다중화/비다중화
- 다중화: 여러 소스의 입력을 하나의 출력으로 묶는 작업
- 비다중화: 단일 소스의 입력을 받아서 다중 출력으로 운반하는 작업
- 소켓 주소가 핵심: 소켓 주소는 특정 기기의 특정 애플리케이션에 대한 고유 식별자 제공

TCP
- Transmission Control Protocol
- 광범위한 오류 제어, 흐름 제어
- 연결 지향 프로토콜
- 안정성
- 상호작용적 세션(SSH, FTP) 제공 시 주로 사용
- 스트림 지향 처리: stream으로 데이터 처리, 한 번에 하나의 바이트로 데이터를 받아들임
- 리시퀀싱: resequencing, 데이터를 재배열해 순서 복원
- 흐름 제어: 수신 데이터 양을 초과하지 않도록 보장
- 우선순위 및 보안: 실제로 많은 TCP 구현 시 제공하지 않음
- 우아한 연결 종료: 연결 종료 전에 모든 세그먼트를 주고받도록 보장
- 엔드 노드는 통신 확인(실제 통신 노드)
- 소스 서브넷 데이터 송신 > (라우터) > 대상 서브넷 데이터 수신

TCP 연결
- TCP는 연결을 통해 데이터 송수신
- TCP 규칙에 따라 요청, 연결, 종료
- 수동 개방: 주어진 애플리케이션은 연결 요청을 받을 준비가 되었음을 알림
- 능동 개방: 수동 연결 상태에 있는 다른 컴퓨터에 연결 요청
- 3방향 핸드셰이크 three-way handshake

TCP 연결 설정
- 시퀀스/확인 시스템 작동 시, 컴퓨터가 반드시 자신의 시퀀스 번호 동기화 필요
- 사용하는 ISN, 사용할 ISN을 알아야 함
 
TCP 흐름 제어
- 헤더의 윈도우 필드는 연결을 위한 흐름 제어 메커니즘 제공
- 슬라이딩 윈도우 sliding window / 버퍼 사이즈 buffer 필드를 사용해 시퀀스 번호를 윈도우에 정의

TCP 연결 종료
- FIN 플래그를 1로 설정하여 큐에 세그먼트를 올려놓음. 애플리케이션은 핀 대기 상태(fin-wait state)에 들어감

UDP
- User Datagram Protocol
- 비교적 덜 정교한 오류 제어
- 비연결 프로토콜
- 속도
- 직접 오류를 검사하거나, 검사 필요 없는 애플리케이션에 사용
- 수신 기기가 데이터 무결성 테스트하도록 체크섬 값 포함하여 전송
- 목적지 주소를 포함하는 psudo 헤더 포함 > 잘못 지정된 데이터 그램 검사
- 도달할 수 없을 경우 ICMP(Internet Control Message Protocol) 반환
- 리시퀀싱 resequencing 제공하지 않음
- 주목적: 애플리케이션 계층에 데이터그램 노출
- TCP 연결의 오버헤드 없이 데이터그램을 송수신하기 위한 메커니즘

방화벽
- 권한이 없는 사용자가 LAN에 접근하려는 공격으로부터 로컬 네트워크를 보호하는 시스템
- 특정 TCP와 UDP 포트의 접근을 차단하는 기능


### 퀴즈
1. TCP 포트 25에는 어떤 서비스가 작동합니까?  
: 간이 우편 전송 프로토콜(smtp)

2. UDP 포트 53에는 어떤 서비스가 작동합니까?  
: 도메인 이름 서버(domain)

3. TCP로 보낼 수 있는 가장 큰 레코드 크기는 얼마입니까?  
: 16비트, 64K

4. TCP 능동 연결 상태와 TCP 수동 연결 상태의 차이점은 무엇입니까?  
: 수동 연결은, 받아들일 상태가 되었다는 것을 알리는 상태이며 능동 연결은, 수동 컴퓨터에게 연결을 요청하는 것

5. TCP 연결을 위한 최소 단계는 몇 단계입니까?  
: 3단계(three-way handshake) A->B / B->A / A->B(수신 확인)

### 연습문제
뇌 수술에 대한 실시간 교육을 제공하기 위해 특수 하드웨어 인터페이스를 통한 원격 사용자와 통신하기
- 프로토콜: UDP
- 실시간 교육이기 때문에 오버헤드가 발생하지 않도록, 안정성은 살짝 떨어지더라도 UDP를 사용하여 성능을 높여야 함
- 연결 단계를 모두 구현할 필요 없기에 개발 시간이 적게 걸림

고성능 클러스터에 사용되는 컴퓨터에 주기적인 통계 정보를 효율적으로 전달하기  
- 프로토콜: TCP
- 주기적으로 통계 정보를 '효율적으로 전달'해야 하므로, 정확히 잘 전달되었는지 안정성을 갖추기 위해 TCP를 사용함
- 고성능 클러스터에 사용되는 컴퓨터이므로, 성능이 받쳐주어 TCP를 소화할 

특수 장치가 환경 데이터를 홈 네트워크에 전달하기
- 프로토콜: TCP
- 홈 네트워크에 전달하는 사항이므로, 보안이 잘 지켜질 수 있도록 TCP를 사용하여 안정성 있게 구현해야 함
- 실시간으로 전달되는 대규모 애플리케이션이 아니므로 TCP를 통해 진행하여도 오버헤드가 크지 않음

## Chapter 07. Application Layer
### 정리
응용 계층
- TCP/IP 프로토콜의 맨 위
- OSI 응용, 표현, 세션 계층
- OSI 응용: 사용자 애플리케이션을 위한 서비스와 네트워크 접근 제공
- OSI 표현: 데이터를 플랫폼 중립 형태로 변환, 암호화 및 데이터 압축 처리
- OSI 세션: 컴퓨터 애플리케이션 간의 통신 관리

네트워크 서비스
- 파일 서비스, 원격 접근 서비스, 이메일과 HTTP 웹 서비스 프로토콜 같은 서비스 제공
- 사용자 경험을 제공

파일 및 프린트
- 파일 서버: 저장 장치 작동, 쓰기 및 읽기 요청 처리
- 프린트 서버: 프린트 작동, 출력 처리
- 네트워크 > 프로토콜 계층 > 전송 계층 > 포트를 통해 파일 서버 서비스로 라우팅

이름 확인 서비스
- name resolution
- 사전 정의되고 사용자에게 친숙한 영숫자 이름을 IP 주소에 매핑하는 과정
- DNS 서비스: 인터넷에 이름 확인 제공, TCP/IP 네트워크에 이름 확인 제공
- DNS는 이름 서버를 사용

원격 접근
- 리다이렉터 redirector, 리퀘스터 requester
- 로컬 컴퓨터의 서비스 요청을 가로채서 해당 요청이 로컬에서 처리되어야 하는지, 다른 컴퓨터로 전달되어야 하는지 확인
- 리다이렉터는 해당 요청을 네트워크로 전송

웹 서비스
- 하이퍼텍스트 전송 서비스(Hypertext Transfer Protocol)
- WWW 응용 계층 프로토콜
- 웹 브라우저 내에서 작동하는 사용자 정의 도구를 구축하기 위한 프로토콜 및 구성 요소 집합

API
- 애플리케이션 프로그래밍 인터페이스 Application Programming Interface
- 애플리 케이션이 운영 환경의 다른 부분에 접근하기 위해 사용할 수 있는 구성 요소의 집합체
- 프로그램 -> (API 함수) -> 운영 시스템

TCP/IP 유틸리티
- 전 세계적으로 TCP/IP 네트워크 구성 및 관리, 문제 해결에 사용

### 퀴즈
1. 연결을 확인할 수 있는 네트워크 유틸리티는 무엇입니까?  
: Ping

2. 웹 페이지를 불러오는 데 사용되는 응용 계층 프로토콜은 무엇입니까?  
: 하이퍼텍스트 전송 프로토콜(HTTP)

3. 메일을 가져오는 데 사용되는 두 응용 계층 프로토콜은 무엇입니까?  
: 인터넷 메시지 접근 프로토콜(IMAP), 포스트 오피스 프로토콜(POP)

4. 호스트 이름을 IP 주소와 매핑하는 데 사용되는 프로토콜은 무엇입니까?  
: 도메인 이름 시스템(DNS)

5. 컴퓨터 시간을 동기화하는 데 사용되는 프로토콜은 무엇입니까?  
: 네트워크 시간 프로토콜(NTP)


## Chapter 08. Routing
### 정리
라우터 router
- 논리 주소에 따라 트래픽을 전달하는 가장 기본적인 형태의 장치
- 인터넷 계층, OSI 3층
- 대규모 TCP/IP 네트워크에 필수
- 하나의 네트워크에서 다음 네트워크로 데이터를 전달할 때 네트워크 접근 계층 헤더 정보 대체
- 서로 다른 네트워크 유형 연결
- 최상의 경로 기술 정보 보유

라우터
- 두 개의 네트워크 어댑터를 가진 컴퓨터의 모양
- IP주소는 어댑터에 속함
- 직접적으로 연결되지 않은 네트워크의 주소 확인
- 어떠한 경로를 사용할지 결정 

라우팅
1) 연결된 네트워크 중 하나에서 데이터 수신
2) 데이터를 프로토콜 스택에서 인터넷 계층으로 전달
3) IP 헤더에서 대상 주소 확인
4) 다른 네트워크로 전달 시, 라우팅 테이블을 통해 해당 데이터를 어디로 전달할지 결정
5) 수신 어댑터를 결정하고 나면 전송에 적절한 네트워크 접근 계층 소프트웨어와 어댑터에 전달
- 정적 라우팅: 네트워크 관리자가 라우팅 정보를 수동으로 입력
- 동적 라우팅: 라우팅 프로토콜을 사용해 얻은 정보를 바탕으로 라우팅 테이블을 동적으로 생성

라우팅 테이블
- routing table
- 적절한 로컬 네트워크에 데이터 전달
- 대상 네트워크 ID를 데이터그램이 대상 네트워크에 도달하는 경로의 중간 지점인 다음 홉의 IP 주소에 ㅁ패ㅣㅇ
- 다음 홉은 대상 네트워크 혹은 다운스트림 라우터

IP 포워딩
1) 호스트가 라우팅 테이블 확인
2) 라우팅 테이블에서 대상 주소와 관련 라우터의 IP 주소 추출
3) 데이터그램을 수신 라우터의 물리 주소와 함께 네트워크 접근 계층으로 전달
4) 라우터의 네트워크 어댑터는 프레임 수신
5) 라우터는 인터넷 계층으로 데이터그램 전달
6) 라우터는 데이터그램 IP 주소 확인, 일치하면 데이터는 라우터를 위한 것, 아니면 라우팅 테이블을 확인하여 데이터 그램 전달
7) 어떤 세그먼트에도 전달될 수 없다면 마지막 라우터가 대상 호스트로 직접 데이터그램 전송할 수 있을 때까지 과정 반복

직접 라우팅
- 라우터는 모든 서브넷과 직접적으로 연결
- 직접 라우팅을 통해 모든 데이터그램 전송

간접 라우팅
- 간접 경로 확인: 시스템관리자 확인, 다른 라우터 확인
- 시스템 관리자 라우팅 테이블(정적 라우팅)에 직접 네트워크 경로 입력
- 다른 라우터가 세그먼트 정보 전달(동적 라우팅)
- 정적라우팅: 소규모, 단순 및 영구 네트워크에 효과적 접근 / (-) 세그먼트 추가 시 마다 관리자의 추가 작업 필요/라우팅 루프 비효율성
- 동적라우팅: 최신 라우터의 형태, 각 라우터는 통신 과정을 통해 얻은 정보로 자신만의 라우팅 테이블 생성

동적 라우팅 알고리즘
- 라우팅 프로토콜
- 거리 벡터 라우팅 distance-vector routing
- 링크 상태 라우팅 link-state routing

거리 벡터 라우팅
- 가장 많은 라우팅 프로토콜이 사용하는 효율적이고 간단한 라우팅 방식
- 최근에는 링크 상태 라우팅이 더 정교하여 인기 있음
- 라우터 간 필요한 통신 최소화, 라우팅 테이블 데이터양 최소화
- 홉 카운트: 경로 매개변수

링크 상태 라우팅
- 거리 벡터 라우팅의 단점 극복: 교차하는 라우터 개수가 일치할 때만 가치있음, 대규모 라우터 그룹에서는 확장이 어려움
- 모든 라우터가 네트워크 토폴로지 자체 내부 맵 작성
- 라우터가 다른 라우터와 링크 상태 나열
- 현재 조건을 기반으로 목적지에 도달하는 최상의 경로 선택
- (-) 각 라우터에 더 많은 처리 시간 필요
- (+) 대역폭의 소비가 줄어듦, 네트워크 문제점을 찾기 쉬움

외부 라우터
- 자율 네트워크와 라우팅 정보를 주고 받음
- 자신과 인접한 자율 네트워크의 라우팅 정보 유지
- 외부 게이트웨이 프로토콜(EGP) 사용 (ex)BGP Border Gateway Protocol

내부 라우터
- 라우팅 정보를 공유하는 자율 지역 내 라우터, 내부 게이트웨이
- IGP Internal Gateway Protocol
- (ex) RIP, OSPF

RIP
- 거리 벡터 프로토콜
- 홉 카운트로 목적지에 도달하는 최상의 경로 결정
- 수신 대기 라우터 필요, 다른 라우터로부터 경로와 홉 카운트 메시지를 수신하고 통합 필요
- 능동 RIP 노드: 데이터 교환 과정에 참여하는 라우터, 전송 및 변경 사항 수신 대기
- 수동 RIP 노드: 변경 사항을 수신 대기하지만, 자신의 라우팅 테이블을 전파하지는 않음
- 네트워크가 평형 상태일 때 가장 잘 작동
- OSPF 프로토콜로 대체되고 있음

OSPF
- 최신 내부 라우팅 프로토콜
- 링크 상태 라우팅 프로토콜
- 각 라우터는 라우터 ID 할당받음
- 링크 상태 라우터는 네트워크 토폴로지의 내부 맵을 만듦
- 각 라우터는 루트에서 네트워크를 트리 형식으로 구성 (SPT Short Path Tree)
- 라우터는 각 경로에 대한 비용 계산(라우터 홉의 개수 매개변수, 회선의 속도, 안정성)

BGP
- 외부 라우터
- 경계 게이트웨이 프로토콜
- 매우 강력하고 확장 가능
- 초기 외부 프로토콜 대체, 인터넷 요구 충족위해 설계
- ASN 사용하여 인터넷 맵 설계, 자율 시스템을 통해 CIDR 기반의 클래스리스 IP 주소를 경로에 연결
- 안정적인 TCP 기반 연결을 통해 주소 범위에 대한 정보 전달
- 네트워크를 통해 경로를 알려주는 ASN 연결 고리 생성
- 경로 발견을 위한 다양한 조항과 여러 옵션 중 가장 효율적인 경로를 선택하는 기술 포함

클래스리스 라우팅
- CIDR 클래스리스 인터도메인 라우팅은 주소 할당과 경로 결정에 대안 방식 제공
- 라우터가 다중 클래스 네트워크를 단일 엔터티로 취급할 수 있게 해서 라우터 간 반드시 전송해야 하는 필수 정보를 줄임

### 퀴즈
1. 동적 라우팅의 두 가지 종류는 무엇입니까?  
: 거리 벡터 라우팅, 링크 상태 라우팅

2. 라우터가 멀티홈이 돼야 하는 이유는 무엇입니까?  
: IP 주소가 컴퓨터가 아닌, 어댑터에 속해있어서 정보를 주고 받을 때 직접적으로 연결되지 않은 세그먼트의 정보 수신 가능

3. 외부 라우터에 가장 흔한 라우터 프로토콜은 무엇입니까?  
: EGP External Gateway Protocol

4. 클래스리스 라우팅이 더 효율적인 이유는 무엇입니까?  
: 다중 클래스 네트워크를 단일 엔터티로 취급, 라우터 간 반드시 전송해야 할 필수 정보를 줄임

5. OSPF는 어떤 유형의 라우팅의 예입니까?  
: 내부 라우팅 프로토콜, 링크 상태 라우팅 프로토콜

### 연습 문제
1. 현재 사용되는 라우팅 프로토콜 3개를 나열하세요.  
- RIP: 거리 벡터 프로토콜
- OSPF: 링크 상태 라우팅 프로토콜
- BGP: 외부 라우터
- 클래스리스 라우팅

2. OSPF가 어떻게 RIP보다 더 유연한 최상 경로 선택 방식을 제공하는지 설명하세요.
- 각 라우터가 네트워크 토폴로지 내부 맵을 만듦
- 네트워크 트리를 최단 경로 트리로 만듦
- 라우터는 각 경로에 대한 비용을 계산하여 경로 지정

3. 정적 라우팅의 장점과 단점을 나열하세요.
- 장점:특정 경로에 트래픽을 강제할 수 있음
- 단점: 대규모 네트워크에 적합하지 않음, 관리자의 시간 투자가 필요, 네트워크 변화에 빠르게 적응 불가능


## Chapter 09. Connecting
### 퀴즈
4. 독립 기본 서비스 집합 무선 네트워크의 다른 이름은 무엇입니까?  
: 무선 BSS, IBSS

5. 허브와 스위치의 차이점은 무엇입니까?  
허브
- 자신의 포트 중 하나에서 전송을 수신하고 전송을 다른 모든 포트에 알리는 네트워크 장치
- 데이터를 필터링하거나 라우팅하지 않고 단순히 신호를 수신하고 재전송
- 네트워크 배선 작업을 단순화하여 쉽게 분리, 재연결 가능하게 함
- 스위치로 대체됨

스위치
- 이더넷의 문제점 해결: 트래픽 증가에 따른 성능 저하, 회선이 비어있지 않으면 전송 불가능 등
- 불필요한 전송을 줄여 네트워크의 성능을 높임

## Chapter 10. Name Check
### 정리
이름 확인
- 호스트 이름: 영숫자 이름
- 호스트 파일: 호스트 이름-IP 주소 관계 목록 (-) 대형 네트워크에서 미작동
- 도메인 이름 시스템 DNS: 인터넷에서 사용하는 이름 확인 방식, 개방형 인터넷 이름의 출처

 호스트 파일
 - 호스트 이름-IP 주소 연관시키는 테이블을 가진 파일
 - hosts.txt
 - 시스템은 호스트 파일을 살펴보고 일치하는 이름이 있으면 ip 주소를 로컬 컴퓨터로 반환
 - IP와 ARP 전송 기술을 사용해서 수행
 - 네트워크 변경 시 모든 컴퓨터에서 호스트 파일 수정, 교체
 - (+) 소규모, 고립된 네트워크를 위한 효율적이고 간단한 방법
 - (-) 현재는 고립된 네트워크가 거의 없음, DNS로 넘어감

DNS
- 각 컴퓨터에서 이름 확인 파일을 업데이트하는 것을 피하고 싶음
- 하나 이상의 특별한 서버에 이름 확인 데이터를 올려 놓음
- DNS 서버: 네트워크를 위한 이름 확인 서비스 제공
- 네트워크 변화 시 DNS 구성만 변경
- 검색 속도 최적화, 더 큰 데이터베이스 제공
- (+) 단일 DNS 구성, 효율적인 네트워크 자원 사용 제공
- DNS는 호스트 이름과는 작동하지 않고 FQDN과 작동
- FQDN: 호스트 이름과 도메인을 명시하는 이름으로 구성
- 루트 - 최상위 도메인(TLD) - 기관 이름

도메인 등록
- ICANN: 도메인 이름 등록에 대한 전반적인 권한
- VeriSIgn: DNS 루트 존의 관리자

이름 서버 유형
- 존 파일(zone file)에서 정보를 가져옴
- 존 전송(zone transfer): 보조 서버 - 주 서버간 정보 교환
- 캐싱 전용 서버: 클라이언트 쿼리에 응답
- 역방향 조회 존 파일: 클라이언트가 IP 주소를 제공, 호스트 이름을 요청할 때 사용

DNS 보안 확장
- DNS 쿼리 응답이 실제 DNS 서버에서 왔따는 것을 보장하는 수단이 필요
- DNS 보안 확장 DNSSEC(DNS SEcurity Extension): 데이터 검증 시스템 제공

DNS 유틸리티
- 네트워크가 올바르게 이름을 확인하는지 테스트 가능
- 핑: 신호 전달, 응답을 기다림
- NSLookup: DNS 서버에 쿼리를 보내고, 리소스 레코드 같은 정보를 볼 수 있음
- 도메인 정보 그로퍼(dig): 호스트 이름 입력 시 해당 IP 주소 반환
- 파워셸: 마이크로소프트 명령줄 환경, DNS 연결을 위한 명령어 포함

동적 DNS
- IP 주소가 종종 동적으로 할당됨
- DNS 레코드의 동적 업데이트 제공
- 호스트가 DHCP 서버로부터 IP 주소 획득, 새로운 주소로 DNS 서버 업데이트

NetBIOS 이름 확인
- API
- IBM의 이름 확인 시스템
- TCP/IP를 사용하지 않는 네트워크를 위해 개발됨

### 퀴즈
1. 별칭에 사용되는 리소스 레코드의 유형은 무엇입니까?  
: CNAME

2. DS 리소스 레코드와 DNSKEY 리소스 레코드는 왜 다른 서버에 저장되어 있습니까?  
: 데이터 위-변조 취약점을 보완하기 위해 다른 서버에 저장하여 '공개키 암호화 방식'으로 제공

## Chapter 11. Firewall
### 정리
방화벽
- 네트워크 통로에 위치
- 네트워크의 인바운드 패킷 헤더 검사, 수락, 거부
- 초기: 패킷 필터 - 전송 계층 헤더에 암호화된 TCP와 UDP 포트 번호를 주시
- 진화: 상태 보존 방화벽 - 패킷 개별 검사X 트릭을 주시
- 최신: TCP/IP 응용 계층에서 작동, 패킷과 관련된 프로토콜과 서비스 이해

방화벽 옵션
1) 개인 데스크톱 방화벽 애플리케이션
2) 소규모 사무실 네트워크에 사용 가능한 방화벽
3) 네트워크 방화벽
- 반드시 둘 이상의 네트워크 카드 장착
- 포트 포워딩 설정

DMZ
- 방화벽 외부에 인터넷 접근 가능 서비스를 둠
- 정말 필요한 포트만 열고 필요한 서비스만 실행
- 두 개의 방화벽 사용: 인터넷 서버 앞에 1개, 인터넷 서버 뒤에 1개
- 3개 이상 인터페이스를 가진 단일 방화벽은, 각 내부 세그먼트에 방화벽 규칙 구성 시 DMZ와 동일한 역할 수행

방화벽 규칙
- 방화벽의 행동을 정의하는 일련의 명령어 또는 규칙으로 표현된 방화벽 구성 사용하여 구성 파일 생성

프록시 서비스
- 프록시 서버: 인터넷 자원에 대한 요청을 가로채서 클라이언트 - 서버 간 중개자 역할 수행
- 방화벽과 함께 사용하여 네트워크 보호
- 콘텐츠 캐싱: 접근한 웹 페이지를 복사해 저장

리버스 프록시
- 외부 소스로부터 요청을 수신해서 내부 네트워크로 전달
- 기존 프록시 서버가 제공하는 캐싱과 콘텐츠 필터링 기능 동일하게 제공
- 클라이언트 요청을 처리하는 컴퓨터의 세부 사항을 숨김
- 캐싱으로 성능을 높임

공격 기술
- 자격 증명 공격: 시스템에 로그인하기 위한 자격 증명을 가져오는데 집중
- 네트워크 수준 공격: 방화벽의 틈새를 찾아 침입
- 애플리케이션 수준 공격: 코드의 허점을 찾아 임의의 명령을 실행, 작동
- 백도어: 시스템 전체에 무제한 접근을 위한 뒷문, 루트킷 사용

자격 증명 공격
- 창의적 사고
- 트로이 목마
- 추측
- 가로채기

네트워크 수준 공격
- nmap, nessus 스캐닝 도구를 통해 열린 포트를 찾는 과정을 자동화

애플리케이션 수준 공격
- 버퍼 오버플로: 사용자 입력이 버퍼를 넘어갔을 때 오버 플로를 통해 컴퓨터로 전송된 명령이 실행
- 주입공격: SQL 또는 LDAP 같은 서비스의 문제점 악용

루트 접근
- 루트킷 rootkit: 시스템의 영구적인 발판을 설정하기 위해 사용되는 도구의 집합
- 키로거 key loggers: 키보드 입력 캡처, 기록

피싱
- 실제와 다른 페이지로 연결되도록 함

서비스 거부 공격
- DoS Denial-ofService
- 침입자에게 시스템의 특정 권한이 필요하지 않기에, 한 번 시작되면 멈추는 것 불가능
- 많은 요청을 보내 시스템 마비
- 분산 DoS: 여러 원격 컴퓨터를 사용해 공격

### 퀴즈
1. 프록시 서버는 어떻게 웹 브라우저의 응답 속도를 높입니까?  
: 캐싱을 통해 접근한 페이지를 복사해서 저장. 추후 요청이 있을 때 내부적으로 빠르게 제공 가능

2. 업데이트하는 것이 왜 중요합니까?  
: 시스템을 최신으로 유지하면, 최근에 발견된 공격을 막을 수 있음

3. 스크립트에 사용자의 입력 문자열의 유형과 길이를 확인하는 단계를 추가해야 하는 이유는 무엇입니까?  
: 단순 추측으로 인한 비밀번호 유출 (자격 증명 공격)을 막을 수 있는 방법이기 때문에

## Chapter 12. Configuring
### 정리
네트워크 연결
- 정적 IP 주소 설정
- DHCP를 통해 동적 IP 주소 설정

정적 IP 주소
- 각 컴퓨터가 IP 주소로 사전 구성된 논리적 조건에 맞게 설계
- 소규모 영구 네트워크에서 잘 작동
- (-) 각 클라이언트를 반드시 개별 구성해야 함
- (-) 현재 네트워크와 연결되어 있는지 상관없이 IP 주소 사용
- (-) 다른 서브 네트워크에 할당 시 반드시 수동으로 재구성

DHCP
- IP 주소의 공급 감소와 대규모 동적 네트워크 성장으로 급 성장
- 컴퓨터에 자동으로 TCP/IP 구성 매개변수 할당하는 프로토콜
- DHCP 서버만 정적 IP 주소로 구성
- 각 클라이언트는 주소에 대해 제한된 임대 기간을 가짐

DHCP 작동 원리
- HDCPDISCOVER: UDP 포트 67에 지정된 데이터그램을 브로드캐스팅 / DHCP 클라이언트의 물리 주소를 가짐
- DHCPOFFER: DHCP 오퍼 응답 데이터그램 구성, 브로드캐스트를 통해 송신함 / IP 주소, 서브넷 마스크, DHCP 서버의 물리 주소 및 IP 주소
- DHCPREQUEST: 클라이언트가 오퍼를 선택, 데이터 그램 구성하고 브로드캐스트 수행 / DHCP 클라이언트 오퍼, 물리 주소를 발급한 서버의 IP 주소
- DHCPACK: 데이터그램 수신하고 임대 과정의 마지막 데이터그램 구성 / 클라이언트 IP 주소, 서브넷 마스크 포함

릴레이 에이전트
- BOOTP 릴레이 에이전트, DHCP 릴레이 에이전트
- DHCP 프로세스를 돕는 중개자 역할
- 정적 IP 주소로 구성, DHCP 서버의 IP 주소를 알고 있음
- 브로드 캐스트 수신, 요청 재전송, 브로드캐스팅

DHCP 서버 구성
- IP 예약: 특정 물리 주소로 특정 IP 주소로 연결할 수 있게하는 기능 / 장치가 항상 동일한 IP 주소를 받는 것을 보장

네트워크 주소 변환
- NAT
- 로컬 네트워크의 세부 내용을 가리고 존재를 숨김
- 로컬 네트워크에 있는 컴퓨터의 게이트웨이 역할을 함
- 인터넷 자원에서 받은 모든 패킷을 로컬 네트워크의 주소 체계로 변환, 연결을 시작한 로컬 컴퓨터로 전송
- 보안 향상

제로 구성
- 정적, DHCP 구성 없이 로컬 네트워크에 컴퓨터를 연결할 수 있게 하는 기술
- 링크 로컬 주소 지정(IPv4LL): 자동 개인 IP 주소 지정(APIPA)
- 제로콘프 Zeroconf): 전혀 구성할 필요 없는 강력한 환경 제공
- 링크 로컬 주소 지정, 멀티캐스트 DNS, DNS 서비스 검색
- 링크 로컬 멀티캐스트 이름 확인, 단순 서비스 검색 프로토콜

### 퀴즈
1. 다른 네트워크의 DHCP 서버로부터 한 네트워크의 DHCP 클라이언트가 IP 주소를 임대받기 위해 요구되는 것은 무엇입니까?  
: BOOTP 릴레이 에이전트 or DHCP 릴레이 에이전트

2. DNS-SD는 주로 어떤 DNS 레코드에 의존합니까?  
: TXT 리소스 레코드


## Chapter 13. Next IPv6
### 정리
IPv6
- IPng IP next generation
- 128비트 주소 호출
- 확장된 주소 지정 기능: 더 많은 계층적 주소 지정 수준 제공, 주소 자동 구성 기능 개선, 애니캐스트 주소 지정
- 더 간단한 헤더 형식: 일부 IPv4 헤더 필드 삭제, 다른 필드는 선택사항
- 확장과 옵션에 대한 지원 개선: 선택적 확장 헤더에 일부 헤더 정보 포함
- 흐름 레이블링: 데이터그램을 특정 흐름 레벨로 표시
- 인증 및 개인 정보 보호 향상: 인증, 기밀성, 데이터 무결성 기술 지원

IPv6 헤더 형식
- IPv4 헤더보다 단순
- 상세 정보가 기본 헤더 다음에 오는 특수 확장 헤더에 위임
- 확장 헤더에서 옵션 정보 번들 제공

홉별 옵션 헤더
- 목적: 전송 경로를 따라 라우터를 선택적 정보와 연관
- 옵션 유형 지정, 데이터를 정렬할 수 있는 일부 패딩 옵션 포함
- 점보 페이로드 jumbo paylod 옵션

수신지 옵션 헤더
- 목적: 선택적 정보를 수신 노드에 연결
- 주로 추후 옵션 개발을 위한 프레임워크에 포함

라우팅 헤더
- 목적: 목적지까지 가는 경로를 라우팅하는 하나 이상의 라우터를 명시하는데 사용

프레그먼트 헤더
- 메시지 경로의 각 라우터는 최대 전송단위 MTU(Maximum Transmission Unit) 설정
- 경로 MTU: 경로에 보낼 수 있는 가장 큰 데이터 단위
- 조각난 데이터그램을 재조립하는 데 필요한 정보 포함

인증 헤더
- 보안과 인증 정보 제공

암호화된 보안 페이로드 헤더
- ESP Encrypted Security Payload hader
- 암호화, 기밀성 제공
- ESP를 사용하여 일부 또는 모든 데이터 암호화 가능

IPv6 주소 지정
- 중앙 인터넷 기관이 할당, 인터넷 서비스 제공자와 다른 광대역 제공자의 시스템을 통해 분석
- 불특정, 루프백, 매핑된 IPv4, 멀티캐스트, 링크 로컬 유니캐스트, 범용 유니캐스트

서브넷팅
- CIDR 스타일의 표기법 사용
- 128비트는 네트워크와 주소의 호스트 부분을 위한 많은 공간을 남겨둠
- 서브넷: 주소의 첫 644비트
- 호스트: 나머지 64비트 혹은 그 이상

멀티캐스팅
- 단일 전송과 전체 전송 사이의 중간 옵션 제공
- 호스트는 단일 멀티캐스트 주소를 공유하는 멀티캐스트 그룹에 참여
- 많은 백그라운드 검색 프로세스를 수행

링크 로컬
- 라우터를 통과하지 않고 로컬 네트워크 세그먼트 간의 통신에만 사용
- 컴퓨터가 수동 구성 단계 없이 로컬 네트워크 세그먼트에서 통신할 수 있도록 허용
- 라우팅 할 수 없으므로 더 큰 규모의 네트워크와 연결할 수 없음

인적 탐색
- NDP Neighbor Discovery Protocol 인접 탐색 프로토콜을 사용해서 IP 주소를 물리 주소로 매핑

자동 구성
- 비보존형 자동 설정 기능
- 물리 주소의 해시를 기반으로 컴퓨터에 링크 로컬 주소 할당
- 중복 주소 검출 DAD Duplicate Address Detection > 주소가 로컬 세그먼트에서 사용 중이지 않다면 자동 구성된 주소로 가정

IPv6 터널
- IPv6 터널 브로커 사용
- IPv4 내에 IPv6 캡슐화
- IPv6 패킷을 받아 IPv4 헤더 안에 포함 > IPv6 패킷 추출하여 대상 IPv6 네트워크에 전송되는 또 다른 엔드포인트로 전송

6in4와 6to4
- 터널링 기술
- IPv4 IP 헤더의 8비트 프로토콜 헤더 활용
- 프로토콜 헤더의 41값을 사용해 IPv6 터널링 패킷 신호를 보냄

TSP
- Tunnel Setup Protocol
- 터널 매개변수의 동적인 협상을 허용하는 기술
- IPv6 네트워크의 엔드 포인트는 TSP 서버와 계약
- 서버는 목적지 네트워크의 엔드 포인트와 연결 매개변수를 협상하여 두 엔드 포인트를 연결

### 퀴즈
1. 왜 멀티캐스트가 브로드캐스트보다 더 효율적입니까?  
: 멀티캐스트 그룹에 속하지 않은 호스트는 메시지에 신경을 쓸 필요가 없어서

2. 왜 IPv6 자동 구성이 IPv4 제로콘프 자동 구성보다 더 안정적입니까?  
: 물리 주소를 해시 기반으로 할당, 물리 주소와 링크 로컬 주소가 모두 고유하여 IPv4 제로콘프에서 발생하는 몇몇 주소 충돌 문제 예방 가능

3. 6to4를 위해 예약된 IPv6 주소 접두사는 무엇입니까?  
: 2002::/16

## Chapter 14. Classic Tool
### 정리
연결 문제
- 프로토콜 장애 또는 잘못된 구성
- 회선 문제: 허브, 라우터, 스위치 미작동
- 잘못된 이름 확인: 호스트 이름, DNS이름으로 접근 불가
- 과도한 트래픽: 느리게 작동

프로토콜 장애와 잘못된 구성
- ping: 네트워크 연결 테스트 진행
- 구성 정보 유틸리티: TCP/IP 구성 정보 표시, IP 주소, 서브넷 마스크, DNS 서버 및 다른 매개변수 구성 확인
- arp: ip 주소를 물리 주소로 연결하는 arp 캐시 콘텐츠 ㅎ확인 및 구성

ping
- 최소한의 네트워크 연결 테스트
- 메시지를 보내고 응답을 기다림

구성 정보 유틸리티
- TCP/IP 구성 볼 수 있음
- 로컬 컴퓨터 ip 주소, 서브넷 마스크 및 기본 게이트웨이 정보 출력
- ifconfig: IP 주소 정보 표기

주소 확인 프로토콜
- ARP
- IP 주소와 상응하는 물리 주소를 확인하기 위한 프로토콜

회선 문제
- ping을 통해 회신 문제 식별 가능
- 자신의 주소르는 핑 가능, 다른 주소로는 핑 불가능 시 케이블 세그먼트 문제 가능성

이름 확인 문제
- 메시지 주소가 지정된 호스트 이름이 네트워크에서 확인되지 않을 때 발생
- 이름 서버에 핑을 보내 온라인 상태인지 확인
- 이름 서버가 로컬 서브넷의 범위를 벗어날 경우 게이트웨이에 핑을 보내 도달 가능한지 확인

네트워크 성능 문제
- 과도한 트래픽, 브로드캐스트 폭풍
- 오작동 네트워크 어댑터, 병목 현상을 일으키는 고장 난 라우터가 원인 가능

traceroute
- 데이터그램이 대상 기기로 이동하면서 통과하는 경로 추적
- 느린 명령, 라우터마다 10~15초 기다려야 함

route
- 호스트로부터 패킷이 효과적으로 라우팅되지 않을 때 라우팅 테이블을 표시하기 위해 사용
- 라우팅 테이블의 엔트리를 수동으로 추가, 삭제 및 변경할 수 있음

netstat
- IP, TCP, UDP 및 ICMP 프로토콜과 관련된 통계 표시
- 전송된 데이터그램, 수신한 데이터그램 및 일어날 수 있는 다양한 에러와 같은 항목 수 표시

텔넷
- telnet
- 원격 컴퓨터에 터미널과 같은 접근을 제공하는 구성 요소의 집합
- 최근에는 SSH 프로토콜이 터미널 적븐을 위한 표준이 됨

버클리 원격 유틸리티
- BSD 유닉스
- 원격 접근 제공을 위해 설계된 명령줄 유틸리티 집합
- r* 유틸리티: 네트워크를 위해 더 빠르고 단순하게 설게됨, 신뢰할 수 있는 접근이라는 개념 사용

보안 셸
- 원격 셀 세션은 일반적으로 보안 셀(SSH, Secure Shell)에 속하는 프로토콜과 유틸리티의 스위트를 통해 관리
- 많은 방화벽이 SSH 연결을 통해 내부 네트워크에 외부 접근을 지원하므로 네트워크 관리자는 SSH를 사용해 내부 네트워크에 인터넷을 통해 로그인
- 포트 형식의 전송 지원, 안전하지 않은 애플리케이션을 SSH 기반의 암호화 연결을 통해 안전하게 작동 가능

네트워크 관리
- 단일 인터페이스에서 원격 시스템과 장치를 구성하고 모니터링, 관리
- 단순 망 관리 프로토콜, 원격 모니터링

단순 망 관리 프로토콜
- 네트워크에서 원격 장치 관리, 모니터링하기 위해 설게된 프로토콜
- SNMP를 사용해 컴퓨터, 라우터 및 다른 네트워크 장치 관리하고 모니터링할 수 있는단일 워크스테이션을 원격으로 운영
- 에이전트: 원격 노드에서 작동하는 프로그램으로 네트워크 모니터에서 실행 중인 관리시스템과 통신
- 관리 정보 베이스(MIB, Management Information Base) 매개변수를 사용해 에이전트로부터 정보 요청, 구성 설정 변경

SNMP 주소 공간
- MIB 각 정보의 고유한 주소를 포함하는 계층적 주소 공간
- 편리한 탈중앙화 허용

SNMP 명령어
- get, getNext, set
- SNMP 소프트웨어는 실제 네트워크 관리자의 필요에 따라 다르게 작동

SNMP 단점
- 하위 계층을 볼 수 없음
- 운영 프로토콜 스택이 필요
- 많은 네트워크 트래픽 생성
- 너무 많은 데이터와 너무 적은 정보 제공
- 기계의 모습 제공, 네트워크의 모습 미제공

원격 모니터링
- RMON
- MIB 주소 공간의 확장판
- 원격 LAN 모니터링, 관리할 목적으로 개발
- 네트워크 미디어에서 직접 데이터 캡처, LAN 전체에 대한 모습 제공
- RMON 1: 이더넷 LAN 모니터링, 물리와 데이터 링크 계층 모니터링
- RMON 2: RMON 1 + 상위 다섯 계층 관리

### 퀴즈
1. 웹 서핑 중 페이지 로딩이 멈췄습니다. 가장 먼저 사용해야 할 문제 해결 도구는 무엇입니까?  
: ping

2. ARP 캐시의 콘텐츠를 보여 주는 명령어는 무엇입니까?  
: arp

3. TCP를 통해 어떤 호스트가 연결되었는지 어떻게 볼 수 있습니까?  
: route를 사용하여 현재 라우팅 테이블 표시

4. 일부 route의 버전은 라우팅 테이블을 출력하는 옵션이 없습니다. 어떤 유틸리티를 사용해야 합니까?  
: netstat

5. 텔넷 대신 SSH를 선호하는 이유는 무엇입니까?  
: 안전한 원격 셸 연결 제공, 포트 형식의 전송 지원을 통해 애플리케이션을 안전하게 작동하게 함

## Chapter 15. Classic Service
### 정리
HTTP
- Hyper Text Transfer Protocol
- 하이퍼텍스트 마크업 언어 형식
- 데이터와 이미지 전송, 요청
- 응용 계층 프로토콜

이메일
- 클라이언트 애플리케이션 - 서버 애플리케이션 간의 상호 작용
- SMTP Simple Mail Transfer Protocol

FTP
- File Transfer Protocol
- 파일 전송 프로토콜
- TCP/IP 네트워크를 사용하는 두 컴퓨터 간에 파일을 전송하는 프로토콜
- 신뢰할 수 있는 연결 지향 세션 사용
- 오래된 프로토콜로 안전하지 않다고 간주됨
- 그러나 이메일로 전달하기에는 어려운 큰 일반 문서와 파일 업로드하거나 편리한 내려받기 환경을 제공
- 최근에는 scp, sftp 유틸리티를 포함하는 SSH 툴킷 주목

TFTP
- Trivial File Transfer Protocol
- 단순 파일 전송 프로토콜
- TFTP 클라이언트와 TFTP 데몬을 실행하고 있는 TFTP 서버 간에 파일 전송 시 사용
- UDP 전송 수단 사용
- Read, Write 기능만 있음
- 넷아스키 ASCII 형식 또는 옥텟으로 알려진 바이너리 형식으로 파일 전송

파일 및 프린트 서비스
- redirector, requestor 필요
- 네트워크 파일 시스템 NFS: 유닉스/리눅스
- 공용 인터넷 파일 시스템 CIFS/서버 메시지 블록 SMB: 윈도우

네트워크 파일 시스템
- Network File System
- 사용자가 원격 컴퓨터에 위치한 디렉터리와 파일을 로컬 컴퓨터에 위치한 것처럼 접근하도록 허용
- UDP 프로토콜 사용, LAN에서 사용
- 이후에는 TCP 프로토콜 사용, WAN에서 작동할 수 있도록 NFS 기능 확장
- 운영 체제, 전송 프로토콜 및 물리적 네트워크 아키텍처와 독립적으로 설계
- NFS 클라이언트가 모든 NFS 서버와 상호 운용하도록 함
- 원격 프로시저 호출을 통해 독립성 확보

서버 메시지 블록
- Server Message Block
- 탐색기, 네트워크 환경 및 맵 네트워크 드라이브 기능 등 윈도 사용자 통합 도구 지원
- 윈도 프로토콜

공용 인터넷 파일 시스템
- Common Internet File System
- 유닉스/리눅스 시스템을 위한 SMB 파일 서비스 제공

경량 디렉터리 접근 프로토콜
- Light Directory Access Protocol
- 디렉터리 서비스
- 논리적이고 트리와 같은 계층으로 구성된 네트워크 리소스 정보의 디렉터리를 유지 관리
- 식별 이름, 상대 식별 이름
- LDAP 데이터 교환 형식 (LADP Data Interchange Format)

원격 제어
- A의 응용 계층에서 작동하는 소프트웨어 구성 요소가 프로토콜 스택을 통해 컴퓨터 B에 리다이렉팅
- 컴퓨터 B에서 나온 출력 데이터는 네트워크를 통해 컴퓨터 A에 전송
- RDP Remote Desktop Protocol

### 퀴즈
1. FTP의 put과 mput 명령어의 차이점은 무엇입니까?  
: put은 하나의 명령에 하나의 파일 전송 가능, mput은 하나의 명령에 여러 파일 전송 가능

2. TFTP를 사용해 디렉터리의 파일을 나열할 수 있습니까?  
: 불가능. TFTP는 파일을 읽고 쓸 수만 있음

3. 유닉스/리눅스 삼바 파일 서버에 사용되는 파일 서비스 프로토콜은 무엇입니까?  
: CIFS

## Chapter 16. Detail of Internet
### 정리
인터넷
- 개인 네트워크가 다른 네트워크에 대한 접근을 공유하고 파는 대규모 집합체
- 티어 1 네트워크: 다른 모든 티어 1 네트워크에서 트래픽을 무료로 전달하는 피어링 장치를 가짐
- 티어 2 네트워크: 티어 1 네트워크 가장자리에서 작동, 티어 1 제공자에게 접근 임대 가능, 티어 2와 피어링, 티어 3에게 접근 임대
- 티어 3 네트워크: 일반적인 인터넷 서비스 제공 업체, 업스트림 공급자에게 접근 권한 구매하고 개인 및 기업에게 인터넷 접근 판매, POP 연결 임대
- 인터넷 익스체인지 포인트 IXP Internet eXchange Point: 1, 2 티어 네트워크가 교차하는 대규모 스위칭 시설
- 단일 응집체: 공통의 규칙 집합, 공통의 기관 집합이 관리하고 유지, 공통의 언어 유사

인터넷 생태계
- DNS 서버: 대상 도메인의 이름을 IP 주소로 확인
- 사용자 컴퓨터의 클라이언트 소프트웨어: 연결 설정
- 서버: 웹 페이지, 인스턴트 메시징 혹은 FTP로 내려받을 수 있는 파일 제공

URI와 URL
- URL Uniform Resource Locator 유일 자원 지시자
- URI Uniform Resource Indentifier 통합 자원 식별자
- 지시자보다 식별자라는 용어가 더 적절함
- 스킴 scheme: 요청 해석하기 위해 시스템 식별

### 퀴즈
1. 티어 1과 티어 2 네트워크의 차이점은 무엇입니까?  
- 티어 1 끼리는 무료로 트래픽을 전달하는 피어링 장치를 가짐
- 티어 2는 티어 1의 접근 임대, 티어 2끼리 피어링을 맺어 작동, 티어 3에게 인터넷 접근 임대

2. URL의 어느 부분이 스킴입니까?  
: 맨 앞쪽

3. URL에서 스킴은 어디에 위치합니까?  
: :// 이전

4. 인터넷에서 일반적으로 사용되는 네 가지 스킴은 무엇입니까?  
: file, ftp, http, https

5. URL의 대상 디렉터리에서 파일 이름이 생략되어 있다면 대부분의 웹 서버에서 기본적으로 보내는 파일은 무엇입니까?  
: 도메인의 웹 페이지(홈페이지)

## Chapter 17. HTTP, HTML and World Wide Web
### 정리
월드 와이드 웹
- HTTP 하이퍼텍스트 전송 프로토콜: 브라우저-웹서버간 대화에 사용된 언어
- HTML 하이퍼텍스트 마크업 언어: 클라이언트로 전달된 데이터가 해당 언어를 통해 통합된 문서로 렌더링됨
- 기본 HTML 문서: 헤더 정보, 텍스트, 그래픽, 텍스트 서식 코드, 그래픽 파일과 같은 보조 파일에 대한 참고, 다른 문서 혹은 현재 문서의 위치 링크

HTML
- HTTP의 과정을 통해 전달되는 페이로드
- 텍스트, 서식 코드, 다른 파일에 대한 참고 및 링크 포함
- 실제로는 일반 텍스트 파일
- 정적인 html 문서가 기본, 오늘날에는 동적 html 기술도 많이 사용

CSS
- Cascading Style Sheet
- 문서의 표준 스타일 요소를 정의, 한곳에 담아 두어 텍스트에서 해당 요소 참고
- HTML을 사전 정의된 문자나 단락 스타일의 목록에서 고를 수 있는 전자 출판 도구처럼 만들기 위함
- 폰트 크기, 색상, 간격, 패딩 및 여백 같은 매개변수 집합
- HTML 파일에서는 link href를 통해 참고

HTTP
- 웹 서버 및 브라우저는 HTTP를 통해 통신
- 응용 계층 수준의 프로토콜
- HTML 문서를 전송하는 것이 목적
- HTTP 클라이언트 및 서버는 TCP 전송 프로토콜을 사용해 연결 설정
- 브라우저와 서버 연결, 세션 설정 지정 및 매개 변수 지정, HTML 콘텐츠 순서대로 전송, 서버와 연결 종료
- 1) 브라우저에 URL 입력
- 2) URL의 스킴 체크, 프로토콜 결정
- 3) URL이 HTP 사이트의 리소스를 참조한다고 판단되면, URL에서 DNS 이름을 추출해 이름 확인
- 4) 브라우저는 서버의 IP 주소로 서버와 TCP 연결
- 5) TCP 연결 후 HTTP GET 명령으로 서버에 웹 페이지 요청

연결 상태
- 100: 요청 진행 중
- 200: 요청 성공
- 202: 요청 수락, 완료되지 않음
- 301: 리소스가 새로운 주소를 가짐
- 302: 리소스가 새 임시 주소를 가짐
- 400: 서버가 요청을 인식하지 못함
- 404: 요청한 리소스가 존재하지 않음
- 406: 브라우저가 콘텐츠 수락할 수 없음
- 500: 서버에 오류 발생
- 503: 서버 과부하, 작동하지 않음

HTTP/2
- 연결 내 평행 프로세싱: 한 번에 여러 요청을 처리할 수 있도록 함
- 헤더 압축: 새로운 연결 시작 시 헤더 정보가 응답 시간을 지연시키는데, 헤더를 압축하여 전체 크기를 줄임으로써 단축
- 서버 '푸시' 응답: 추가 항목에 대한 요청을 예상해 직접 콘텐츠 푸시
- 암호화 강력히 지원, TLS 암호화에 대한 표준 프로필 제공

스크립팅
- 자동 웹 코드 생성
- 서버 사이드 스크립팅
- 클라이언트 사이드 스크립팅

서버 사이드 스크립팅
- 서버가 클라이언트에서 입력을 받아 처리
- 브라우저는 서버가 요청할 때에만 콘텐츠 전송
- 공용 게이트웨이 인터페이스 CGI(Common Gateway Interface): 웹 사용자에게 양식에 기반한 입력을 받아 처리, HTML 형식으로 출력
- PHP, ASP.NET

클라이언트 사이드 스크립팅
- 자바스크립트, VB 스크립트
- 특정 유형의 애플리케이션에 더 효율적
- 로컬 환경에 더 상세한 뷰, 대화형 클라이언트 네트워크 트래픽을 줄이고 성능을 높임

웹 브라우저
- 브라우저를 제어해 웹 서버, 운영 체제와 상호 작용하는 개발 도구 및 API를 제공 가능
- 반드시 자바스크립트 or ㄹ스크립팅 기술을 통해 클라이언트 사이드 스크립팅 지원
- 디지털 서명 및 인증서 지원 제공해야 함
- 외부 애플리케이션: 플러그인, 헬퍼 애플리케이션

시맨틱 웹
- 웹 정보의 의미를 컴퓨터가 쉽게 접근해 처리할 수 있는 방식으로 암호화하는 것이 목적

자원 기술 프레임워크
- RDF Resource Description Framework
- 트리플: 주제, 술어, 목적어

마이크로포맷
- Microformat
- 웹 관리 전문가가 접근하기 쉽고 관리하기 쉬운 대안
- 완전한 문장 구조와 구문 구조를 표현하려 하지 않음
- 단순히 텍스트의 섹션을 미리 정의된 의미와 연결되도록 플래그 지정
- 특정 목적을 위해 설계된 이름/값 쌍의 특정 어휘

XHTML
- HTML-XML 웹 환경을 연결하기 위한 노력의 결과
- XML 구문을 따르는 HTML 기능을 공식화
- 다른 프로그램들과 스크립트를 만드는 개발자에게 유연함 제공
- 수신 엔터티의 동적 해석 또는 수정에 적합
- HTML5의 출현으로 중요성 감소

HTML5
- 새로운 HTML 표준 채택
- 모바일 혁명을 만들기 위한 도구
- 웹 환경이 추가적으로 진화한 모습 반영, 애드온과 확장프로그렘에서 제공하는 기능을 HTML5에 통합 

HTML5 로컬 스토리지 및 오프라인 애플리케이션 지원
- 기존 쿠키: 저장 용량이 작아, 일부 기본적인 데이터만 저장
- HTML5 저장소: 웹 애플리케이션 내 저장된 값 저장 가능
- 네트워크를 통한 서버와의 통신의 필요성을 줄여 성능을 높임
- 연결이 끊겨도 일부 복원 가능
- 캐시 매니페스트 포함
- (-) 업체에 저장하는 기능을 확장하면 개인 정보 보호 문제 발생 가능

HTML5 드로잉
- svg 요소를 통해 스칼라 그래픽 제공
- XML 이름 공간 참조
  
HTML5 임베디드 오디오 및 비디오
- video 요소 사용
- 비디오 및 오디오 코덱 참고를 위한 직접적 지원 제공

HTML5 위치 정보
- API
- 지리적 위치 데이터를 위해 애플리케이션이 장치를 쿼리할 수 있는 표준 방법 제공
  
HTML5 시맨틱
- 텍스트에 의미를 제공하는 일련의 정의된 HTML5 요소 사용
- 마이크로데이터 microdata: 마이크로포맷의 확장
  
### 퀴즈
1. HTTP가 협상 단계를 지원하는 이유는 무엇입니까?  
: 브라우저가 제공한 선호도에 따라 자원의 가장 적합한 표현을 선택하기 위해서

2. HTML 문서의 주요 섹션은 무엇입니까?  
: head, body 섹션

3. 책 제목과 가격 정보와 함께 백엔드 데이터베이스를 포함한 웹 사이트가 있습니다. 사용자에게 해당 정보를 제공하기 위해 서버 사이드 스크립트를 사용해야 합니까? 아니면 클라이언트 사이드 스크립트를 사용해야 합니까?  
: 서버 사이드 스크립트

4. 막 새로운 시스템을 설치해 잘 작동하고 있는데, 웹 사이트에 가서 PDF 파일을 클릭하면 열리지 않습니다. 어떻게 고쳐야 합니까?  
: 브라우저 플러그인 설치

5. RDF 트리플의 세 부분은 무엇입니까?  
: 주제, 술어, 목적어

6. 왜 일부 전문가들은 어도비 플래시 및 유사 도구가 몇 년 안에 영향력을 잃을 것이라고 생각합니까?  
: svg, video 등 HTML5의 요소를 사용하면 타사 애플리케이션 적용 없이 직접 지원 가능하므로

## Chapter 18. Web Service
### 정리
콘텐츠 관리 시스템
- WYSIWYG: What You See is What You Get, 사용자에게 나타나는 컨텍스트에서 텍스트, 이미지 및 기타 기능 조작 가능
- CMS: 웹 서버의 확장 기능, 웹 서버에서 작동하며 사용자는 원격 클라이언트 워크스테이션에서 웹 인터페이스를 통해 상호 작용

소셜 네트워크  
블로그
- 새로운 글이 목록 상단에 올라가고 오래된 글이 내려가는 전자 잡지 또는 온라인 저널
- 전문화된 형태의 CMS

위키
- 간단한 공동 작업 및 정보 공유를 위한 공간을 제공하는 웹 사이트
- 정보를 포스팅하는 공간을 확장하기 쉬움

피어 투 피어
- 정보 공유 기술
- 각 피어는 클라이언트(데이터 요청)와 서버(요청 충족)의 역할 수행해야 함
- 중앙 서버를 통해 연결 정보 분배, 클라이언트가 해당 정보로 서로 연결을 설정할 수 있도록 함

웹 서비스
- 웹 서비스 아키텍처: 웹 브라우저, 웹 서버 및 TCP/IP 프로토콜 스택이 네트워킹 세부사항을 처리해 개발자가 애플리케이션의 세부 사항에 집중하게 함
- HTTP 운송 시스템: 웹 서비스의 일부
- XML(확장 가능 마크업 언어), JSON(자바스크립트 객체 표기)

XML
- 마크업 언어의 개념을 텍스트 및 그래픽 서식을 위한 수단을 넘어 단순히 데이터 전송을 위한 수단으로 사용하고자 함
- 자신만의 요소 정의 가능
- 데이터 부분 강조 가능, 데이터 표시 위한 태그 만들 수 있음
- XML 스키마 포함
- 마크업 언어를 생성하기 위한 마크업 언어

SOAP
- 웹 서비스 클라이언트와 서버 간 XML 기반 메시지를 교환하기 위한 표준 프로토콜
- 해당 데이터 구조화, 해석하기 위한 표준 형식

WSDL
- 웹 서비스 기술 언어
- 웹 서비스 애플리케이션과 관련된 서비스를 설명하기 위한 XML 형식 제공
- 정의 모음, 전송되는 데이터 및 해당 데이터와 연관된 작업과 서비스 위치와 관련된 다른 데이터 정보 명시
- SOAP에 국한, 다른 웹 서비스 통신 프로토콜에도 사용
- HTTP와 직접 사용해 디자인 단순화, HTTP 중심에서 더 기본적인 GET 및 POST 형식 작업에 행동 제한

웹 서비스 스택
- LAMP
- LINUX: 서버 시스템에서 자동하는 서버 애플리케이션을 지원하는 운영 체제
- APACHE: XML 기반 SOAP 메시지를 제공하는 웹 서버
- MySQL: 데이터베이스 시스템
- PHP: 커스텀 웹 서비스 애플리케이션의 세부 사항 코딩 위한 웹 프로그래밍 언어

REST
- 표현 상태 전송
- 리소스: 클라이언트가 원하는 요청의 대상. 웹 페이지, 데이터 베이스 레코드, 프로그래밍 객체 등
- 리소스 식별자: 리소스 URI
- 표현: 서버로부터의 응답
- 클라이언트는 요청을 완료하기 위해 URI 본문 내 필요한 정보를 추가, 보기 또는 수정을 원하는 리소스를 식별하는 URI 형식의 리소스 식별자 전송
- GET: 서버로부터 리소스 획득
- PUT: 리소스를 직접 생성 혹은 수정
- POST: 서버에 데이터 전송, 리소스 수정
- HEAD: 리소스와 관련된 메타데이터 획득
- DELETE: 리소스 삭제
- PUT은 전체 리소스 콘텐츠 교체, POST는 서버에 정보를 접수해 업데이트가 어떻게 진행되는지 추정하지 않고 리소스를 업데이트하기 위해 사용
- URI는 계층적이며 객체를 가리킴
- RESTful: REST 패러다임으로 설계된 웹 사이트, 서비스 혹은 개발 프레임워크

전자 상거래
- 웹 도구를 사용해 애플리케이션과 구성 요소를 합치는 방법
- 트랜잭션 서버 애플리케이션

### 퀴즈
1. CMS 도구가 보통 웹 브라우저를 통해 접근할 수 있는 이유는 무엇입니까?  
: Web에 대한 지식 없이도 콘텐츠를 관리할 수 있게함

2. 피어 투 피어 네트워크의 특징은 무엇입니까?  
: 각 피어가 반드시 클라이언트와 서버의 역할을 충족해야함/중앙 서버를 통해 연결 정보를 분배하는 방식으로 이러한 연결을 가능하게 함

3. XML 스키마는 무엇입니까?  
: XML 데이터를 서식화하고 해석하기 위한 로드맵 / XML 데이터 유효성 확인

4. HTTP PUT과 POST 방식의 차이점은 무엇입니까?  
: PUT은 전체 리소스 콘텐츠 교체, POST는 진행을 추정하지 않고 리소스를 업데이트함.

5. REST가 PUT을 강조하는 이유는 무엇입니까?  
: REST는 멱등한 작업을 강조함. PUT은 늘 동일 행동, 동일 결과를 끌어내는 멱등한 작업을 수행함

6. 왜 믾은 전문가가 다른 유사 웹 서비스 아키텍처와 비교해 REST가 더 안전하다고 생각합니까?  
: 서버 내부와 인터페이스로부터 모든 작업을 숨기기 때문에 더 좋고 균일한 보안을 제공함
