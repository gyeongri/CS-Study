# 네트워크 스터디 2주차

![Untitled 1](https://github.com/gyeongri/CS-Study/assets/50294908/922c079e-4e7c-4072-966a-3a745bfb0b3a)

하나의 네트워크 대역 = 하나의 LAN

흐름 제어: 누가 누구한테 보내는지, 오류제어: 오류가 있는지 없는지

![Untitled2](https://github.com/gyeongri/CS-Study/assets/50294908/efd0a387-48a1-4aa9-97f0-357e761d1893)



![Untitled 3](https://github.com/gyeongri/CS-Study/assets/50294908/18a18867-45c7-4bef-8ea2-0188454cea04)

MAC 주소: 물리적인 주소

16진수 2개씩 나눠서 6개, 총 12개로 구성?

-로 쓰기도 하고 :으로 쓰기도 함.

![Untitled 4](https://github.com/gyeongri/CS-Study/assets/50294908/799a0b8c-50ac-499b-851b-edbc268abd6a)

앞의 6개: 고유한 ID/OUI(MAC 주소를 부여한 회사의 고유값(ex) 삼성에서 만들었으면 삼성

뒤의 6개: 고유한 번호/삼성에서 만든 ~번??

![Untitled 5](https://github.com/gyeongri/CS-Study/assets/50294908/71fe0143-c64c-4307-86fc-fda678c4bdbd)

목적지 주소: MAC 주소

보내는 사람 주소, 받는 사람 주소

목적지 맥주소 6바이트, 출발지 맥주소 6바이트

- 이더넷 프로토콜: 보내는 사람, 받는 사람, 이더넷 타입 → 14바이트

![Untitled 6](https://github.com/gyeongri/CS-Study/assets/50294908/977805da-1e43-4bc4-bf9a-e628a4e38fda)

받는사람:BB.., 보내는 사람:AA…

이더넷 타입: 상위 프로토콜이 뭔지 알려주는 역할

→ 0800: IPV4(이더넷 프로토콜의 상위 프로토콜), 0806: ARP

![Untitled 7](https://github.com/gyeongri/CS-Study/assets/50294908/01d862a3-59c1-4e0b-a752-f40c499c08b4)

L2 스위치

L2 스위치는 Mac 주소로 스위칭을 한다. MC주소는 48비트다

PC: Endpoint

L2Access switch: Endpoint와 직접 맞닿는 스위치 (방)

L2Distribution 스위치: 일반적으로 스위치를 위한 스위치 (건물 한층)

uplink: 상위 계층 스위치로 랜선이 연결되는 것(상향 연결일 때, 더 큰 네트워크로 나가는 것을 의미)

link up: 연결이 됐다(녹색)

link down: 연결이 끊겼다. (선에 문제가 생겼나 물리적으로 연결이 끊어짐)

![Untitled 8](https://github.com/gyeongri/CS-Study/assets/50294908/fab233c0-074f-40b0-bd47-f820dfe981f1)

L2 디스트리뷰션 스위치는 마지막으로 라우터로 모인다.

라우터가 전체 PC들의 게이트웨이

포트(단자, 인터페이스)가 16개,

연결한 수 있는 endpoint가 16개

범링크 하나는 써야하니까 15개에 PC 연결가능

L2 스위치는 MAC주소 기반 통신. MAC 주소는 48bit로 이루어져 있고 8bit 씩 끊어 표기되며 각 자리 숫자는 16진수로 표기 됨

L2 스위치는 종류가 크게 2개로 구분

1. 단말과 바로 맞닿고 상위 L2로 데이터 보내는 L2 Access 스위치
2. L2 Access와 맞닿고 Router로 데이터를 보내는 L2 Distribution

이 둘의 차이점은 연결된 대상의 차이

L2 스위치는 Mac 주소로 스위치한다
pc를 위한 스위치는 L2 access 스위치
스위치를 위한 스위치는 L2 distribution 스위치
access 스위치와 언결된 pc를 endpoint
uplink 상위계층으로의 연결
link up, down 연결, 연결끊김
단자=인터페이스=포트
