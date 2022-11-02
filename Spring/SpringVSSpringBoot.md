## 스프링, 스프링부트 차이 정리

<details>
<summary>스프링, 스프링부트 차이에 대해서 설명해 보세요.</summary>
<div markdown="1">
스프링부트는 스프링의 복잡한 과정들을 단순화해줍니다.<br>

먼저 Dependency를 자동으로 설정해줍니다. 스프링의 경우에는 모든 dependency에 대해 버전관리를 하나하나 해줘야 하며 설정 파일도 매우 길게 작성해야 했습니다. 하지만 스프링부트는 spring boot starter web을 의존성에 추가하면 모든 dependency를 적절한 버전으로 자동으로 추가하고 관리해줍니다.<br>

Configuration이 매우 간편해졌습니다. 기본적인 configuration 설정도 매우 길고 모든 어노테이션 및 빈 등록을 설정해줘야 했지만 스프링부트에서는 application.yml 혹은 application.properties에 간편하게 설정할 수 있습니다. <br>

또한 @SpringBootApplication이라는 것이 있습니다. 이 어노테이션에는 @EnableAutoConfiguration, @ComponentScan등의 어노테이션들이 포함되어 있어 많은 외부라이브러리, 내장 톰캣 서버, 객체들을 자동으로 빈에 등록해줍니다.<br>

마지막으로는 내장 was를 가지고 있어 jar로 쉽게 배포할 수 있습니다.
  
  
</div>
</details>
