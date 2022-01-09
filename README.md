# Network TCP/IP 교과서
- [Chapter 01. What is TCP/IP?](#chapter-01-what-is-tcpip)
- [Chapter 02. How does TCP/IP work?](#chapter-02-how-does-tcpip-work)
- [Chapter 03. Network Access Layer](#chapter-03-network-access-layer)
- [Chapter 04. Internet Layer](#chapter-04-internet-layer)
- [Chapter 05. Subnetting and CIDR](#chapter-05-subnetting-and-cidr)

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
