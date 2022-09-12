## 스프링 빈 스코프 정리

<details>
<summary>Bean Scope</summary>
<div markdown="1">
빈 스코프는 빈이 존재할 수 있는 범위를 뜻하며 싱글톤, 프로토타입, request, session, application, websocket등이 있습니다.<br><br>

싱글톤은 기본 스코프이며 스프링 컨테이너의 시작과 종료까지 유지되는 가장 넓은 범위의 스코프입니다. 어플리케이션에 오직 하나만 생성됩니다.<br>
프로토타입은 빈의 생성과 의존관계 주입까지만 관여하고 더는 관리하지 않는 매우 짧은 범위의 스코프입니다. 컨테이너에게 빈을 요청할 때마다 매번 새로운 객체를 생성해줍니다.<br>
request는 웹 요청이 들어오고 나갈때까지 유지, session은 웹 세션이 생성, 종료될 때까지, application은 웹 서블릿 컨텍스트와 같은 범위로 유지하는 스코프입니다.<br>

</div>
</details>


