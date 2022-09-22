## TCP와 UDP 비교 정리

<details>
<summary> TCP와 UDP를 비교하여 설명해주세요.</summary>
<div markdown="1">
TCP는 연결형, 신뢰성 전송 프로토콜입니다. 연결지향적 서비스를 제공하기 위해 데이터를 전송하기 전에 3 way handshaking을 하여 두 호스트의 전송 계층 사이에 논리적 연결을 설립합니다. 신뢰성 있는 서비스를 제공하기 위해 오류제어, 흐름제어, 혼잡제어 등을 실행합니다. 신뢰성을 보장하기 위해서 header가 더 크고 속도가 비교적 느리다는 단점이 있습니다.<br>
UDP는 비연결형 프로토콜로 3way handshake 등의 세션 수립 과정이 없습니다. 또한 비신뢰성 프로토콜로 흐름제어, 오류제어, 혼잡 제어를 제공하지 않습니다. 이러한 단순성 덕분에 적은 양의 오버헤드를 갖고 수신여부를 확인하지 않아서 속도가 빠릅니다.<br>
TCP는 신뢰성이 중요한 통신(HTTP, File 전송 등)에 쓰이고, UDP는 실시간성이 중요한 통신(동영상 스트리밍 등)에 주로 사용됩니다.  
  
</div>
</details>

<details>
<summary> TCP/IP 전송계층 </summary>
<div markdown="1">
TCP/IP는 인터넷에서 사용하는 프로토콜 그룹을 칭합니다. TCP/IP는 Application Layer(응용 계층), Transport layer(전송 계층), Network layer, Data link layer, Physical layer로 5개의 계층으로 나뉩니다.<br>
그 중에 전송계층은 두 응용계층 사이에서의 process to process 통신을 제공합니다. 전송계층은 응용계층으로부터 메시지를 받아 전송계층 패킷으로 캡슐화하여 전송합니다. (segment 또는 datagram으로 부릅니다.)<br>
전송계층의 주된 프로토콜은 TCP, UDP입니다. TCP는 연결형, 신뢰성, 전송 프로토콜입니다. TCP로 전송하는 패킷을 segment라고 부릅니다. UDP(User Datagram Protocol)는 비연결형, 비신뢰성 전송 프로토콜입니다. UDP로 전송하는 패킷을 Datagram이라고 합니다.
</div>
</details>

<details>
<summary> TCP(Transfer Control Protocol) </summary>
<div markdown="1">
TCP는 연결형, 신뢰성 전송 프로토콜입니다.<br>
연결지향적 서비스를 제공하기 위해 데이터를 전송하기 전에 먼저 두 호스트의 전송 계층 사이에 논리적 연결을 설립합니다. 그 후 데이터 전송을 하고 데이터 전송을 완료했으면 연결을 해제합니다. TCP의 통신은 이렇게 connection setup, data transfer, connection termination의 세 단계로 나뉩니다.<br>
신뢰성있는 서비스를 제공하기 위해 TCP가 전체 스트림을 순서에 맞고 오류없이 또한 부분적인 손실이나 중복없이 전송하는 것을 보장합니다. 이를 가능하게 하는 방법은 오류제어, 흐름제어, 혼잡제어 등이 있습니다.<br>
흐름제어는 데이터를 보내는 속도와 데이터를 받는 속도의 균형을 맞추는 것을 뜻합니다.<br>
오류제어는 훼손된 segment의 감지 및 재전송, 손실된 segment의 재전송, 순서가 맞지 않게 도착한 segment를 정렬하고 중복 segment 감지 및 폐기를 합니다. 이는 TCP Header의 checksum, 확인응답, 타임아웃 등을 통해 수행됩니다.<br>
</div>
</details>

<details>
<summary> UDP(User Datagram Protocol) </summary>
<div markdown="1">
UDP는 비연결성, 비신뢰성 전송 프로토콜입니다.<br>
UDP는 논리적 연결을 설립하지 않고 datagram을 전송하는 비연결형 프로토콜입니다. 또한 흐름제어, 오류제어, 혼잡제어를 제공하지 않는 간단한 프로토콜입니다. 이러한 단순성은 적은 양의 오버헤드를 갖기 때문에 작은 메시지를 보내거나 신뢰성을 크게 고려하지 않아도 되는 상황에서 사용합니다.<br>
매우 큰 문서파일같이 신뢰성이 중요한 전송은 TCP를 live방송과 같이 신뢰성보다는 실시간성이 중요한 전송은 UDP를 사용합니다.

</div>
</details>
