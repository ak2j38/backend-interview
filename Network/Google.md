## 주소창에 Google을 치면 발생하는 일 정리

<details>
<summary> 주소창에 Google을 치면 발생하는 일.</summary>
<div markdown="1">
  <br>
1. 유저가 브라우저에서 www.google.com(URL)을 입력을 하면 HTTP request message를 생성합니다.<br>
2. IP주소를 알아야 전송을 할 수 있으므로, DNS lookup을 통해 해당 domain의 server IP주소를 알아냅니다.<br>
3. 반환된 IP주소(구글의 server IP)로 HTTP 요청 메시지(request message) 전송 요청을 합니다.<br>
    1. 생성된 HTTP 요청 메시지를 TCP/IP층에 전달합니다.<br>
    2. HTTP 요청 메시지에 헤더를 추가해서 TCP/IP 패킷을 생성합니다.<br>
4. 해당 패킷은 전기신호로 랜선을 통해 네트워크로 전송되고, 목적지 IP에 도달합니다.<br>
5. 구글 server에 도착한 패킷은 unpacking을 통해 message를 복원하고 server의 process로 보냅니다.<br>
6. server의 process는 HTTP 요청 메시지에 대한 response data를 가지고 HTTP 응답 메시지(response message)를 생성 합니다.<br>
7. HTTP 응답 메시지를 전달 받은 방식 그대로 client IP로 전송을 합니다.<br>
8. HTTP response 메시지에 담긴 데이터를 토대로 웹브라우저에서 HTML 렌더링을 하여 모니터에 검색창이 보여집니다.<br><br>
  
<img width="478" alt="스크린샷 2022-10-08 오후 11 54 06" src="https://user-images.githubusercontent.com/29879110/194713570-cb62d8ce-dfb2-4a06-b8cd-0262b3016aa6.png">

</div>
</details>
