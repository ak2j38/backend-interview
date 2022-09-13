## 스프링 빈 생명 주기 정리

<details>
<summary>빈 생명주기</summary>
<div markdown="1">
Spring Bean의 생명주기는 객체생성 -> 의존성 설정 -> 초기화 -> 사용 -> 소멸 과정의 생명주기를 갖고 있습니다.<br>
Bean은 스프링 컨테이너에 의해 생명주기가 관리되며 Bean을 초기화할 때는 @PostConstruct를 Bean을 소멸할 때는 @PreDestroy를 사용합니다.<br>
생성된 Spring Bean을 등록할 때는 Component Scan에 의해 자동으로 등록되거나 @Bean 어노테이션을 사용하거나 빈 설정파일(XML)에 직접 등록할 수 있습니다. 
</div>
</details>
