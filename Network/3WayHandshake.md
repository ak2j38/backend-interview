## 3 Way Handshake 정리

<details>
<summary> 3 way handshake는 무엇이고 각 과정은 어떻게 되나요?</summary>
<div markdown="1">
3 way handshake는 TCP/IP 프로토콜로 통신하기 전, 정확한 정보 전송을 위해 상대방 컴퓨터와 세션을 수립, 즉 연결하는 과정입니다.<br>
클라이언트가 서버에게 접속을 요청하는 SYN 패킷을 보내면, 서버는 요청을 수락하는 ACK를 포함하여 SYN+ACK 패킷을 클라이언트에게 발송합니다. 클라이언트가 이것을 수신한 후, 다시 ACK를 서버에게 발송하면 연결이 이루어지고, 이로써 데이터를 주고 받을 수 있게 됩니다.
</div>
</details>

<details>
<summary> TCP 3 way handshake </summary>
<div markdown="1">
TCP 통신은 아래와 같은 3단계의 과정을 거칩니다.<br>
1. Connection Setup(tcp 연결 초기화) - 3 way handshake<br>
2. Data Transfer(데이터 전송)<br>
3. Connection Termination(TCP 연결 종료) - 4 way handshake<br>  
<img width="640" alt="스크린샷 2022-09-22 오후 10 11 17" src="https://user-images.githubusercontent.com/29879110/191756075-41499b1a-820b-433e-92c0-e192f24f6d6e.png">

</div>
</details>

<details>
<summary> TCP 4 way handshake </summary>
<div markdown="1">
3 way handshake를 통해 Connection Setup을 했다면 tcp 연결을 종료하는 Connection Termination 과정은 4 way handshake를 통해 이루어집니다.<br>
TCP connection termination은 양방향으로 2개의 연결이 독립적으로 닫히기 때문에 4-way 단계를 밟게 됩니다.<br>  
1. Client process에서 active close를  하면 client tcp에서 FIN 세그먼트를 보냅니다.<br>
2. Server는 FIN 세그먼트를 받았다는 응답에 대한 ACK를 client로 보냅니다. 이때, server내의 process에게 EOF를 보내지만, 아직 process는 close되지 않을 수 있습니다.<br>
3. Server process로부터 passive close를 받으면 server tcp에서 FIN 세그먼트를 client TCP에게 보냅니다.<br>  
4. Server tcp가 ACK를 받게되면 연결이 종료됩니다.<br>  
<img width="674" alt="스크린샷 2022-09-22 오후 10 26 01" src="https://user-images.githubusercontent.com/29879110/191759370-bb708a4c-d136-4ee6-9c4d-565398c60940.png">

</div>
</details>
