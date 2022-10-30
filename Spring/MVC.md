## 스프링 MVC 핵심 구성 요소에 대한 정리

<details>
<summary>스프링 MVC 핵심 구성 요소</summary>
<div markdown="1">
1. 웹 브라우저로부터 DispatcherServlet으로 요청이 전송됩니다.<br>
2. DispatcherServlet은 HandlerMapping을 통해 요청 URL과 매칭되는 컨트롤러를 검색합니다.<br>
3. 이후 HandlerAdapter를 통해 해당 컨트롤러에 처리를 요청합니다.<br>
4. 컨트롤러 실행 결과를 ModelAndView로 변환해서 DispatcherServlet에 반환받습니다.<br>
5. DispatcherServlet은 ViewResolver를 통해 컨트롤러 실행 결과를 보여줄 View를 검색합니다.<br>
6. DispatcherServlet은 응답 요청을 생성해 View에 넘겨주고 View는 해당 내용을 출력합니다.<br>
</div>
</details>
