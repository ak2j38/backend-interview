## OSI 7계층과 TCP/IP 4계층 정리

<details>
<summary> OSI 7계층과 TCP/IP 4계층을 비교하여 설명해주세요.</summary>
<div markdown="1">
OSI 7계층은 네트워크 통신을 표준화한 모델로, 통신 시스템을 7단계로 나누어 설명한 것입니다.<br>
하지만 OSI 모델이 실무적으로 이용하기에 복잡한 탓에 실제 인터넷에서는 이를 단순화한 TCP/IP 4계층이 사용되고 있습니다.<br>
  
</div>
</details>

<details>
<summary> OSI 7계층과 TCP/IP 4계층</summary>
<div markdown="1">
<img width="682" alt="스크린샷 2022-09-22 오후 9 00 09" src="https://user-images.githubusercontent.com/29879110/191740987-f1b6d2eb-0ed6-42bb-a344-8509f4e62b06.png">
<br>
OSI 7계층과 TCP/IP 4계층 모델에서 각 계층은 하위 계층의 기능을 이용하고, 상위 계층에게 기능을 제공합니다. 예를 들어서 HTTP는 TCP와 IP를 이용해서 작동합니다.<br>
</div>
</details>


<details>
<summary> 캡슐화 & 역캡슐화 </summary>
<div markdown="1">
<img width="695" alt="스크린샷 2022-09-22 오후 9 05 44" src="https://user-images.githubusercontent.com/29879110/191742051-0a0e19f0-2274-4f91-a71b-c45bc4f3f14f.png">
<br>
캡슐화란 통신 프로토콜의 특성을 포함한 정보를 Header에 포함시켜서 하위 계층에 전송하는 것을 말합니다. 통신 상대측에서 이러한 Header를 역순으로 제거하면서 원래의 Data를 얻는 과정을 역캡슐화라고 합니다.<br>
예를 들어, 사용자는 최상위 계층인 응용 계층에서 인터넷 접속(HTTP), 메일 전송(SMTP), 파일 전송(FTP), 원격 로그인(Telnet)등의 작업을 수행합니다.<br>
각 사용자 입장에서 보면 data가 그냥 전송되는 것처럼 보이게 됩니다. 하지만 이 과정을 OSI 7계층 관점의 캡슐화/역캡슐화 과정까지 바라보면 다음과 같습니다.<br>
사용자가 전송하고자 하는 데이터는 각 프로토콜의 정보를 Header에 포함시켜서 하위 계층에 전달하고, 이것은 최종적으로 물리 계층에서 binary 데이터로 변환되어 전송됩니다.<br>
상대측에서는 이러한 Header를 역순으로 하나씩 제거하면서 상위 계층으로 데이터를 전달하고, 최종적으로 원본 데이터를 수신하게 됩니다.


</div>
</details>
