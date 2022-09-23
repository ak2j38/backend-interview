## 자동 주입 중 @Autowired 정리

<details>
<summary>@Autowired가 무엇인지 어떻게 동작하는지 설명해주세요.</summary>
<div markdown="1">
필드에 @Autorwired 어노테이션이 붙어있으면 스프링이 해당 타입의 빈 객체를 찾아서 필드에 할당합니다. 메소드에 @Autowired 어노테이션을 붙인다면 메소드 파라미터 타입에 해당하는 빈 객체를 찾아 인자로 주입합니다.<br>
일치하는 빈이 없다면 NoSuchBeanDefinitionException이 발생하고, 둘 이상의 빈이 검색된다면 NoUniqueBeanDefinitionException을 발생시킵니다.<br>
</div>
</details>

<details>
<summary>명시적으로 의존성을 주입했는데 자동 주입대상이면 어떻게 될까요?</summary>
<div markdown="1">
설정 클래스에서 수정자 메소드를 통해 의존성을 주입해도 해당 수정자 메소드에 @Autowired 어노테이션이 붙어있으면 자동 주입을 통해 일치하는 빈을 주입합니다. 이렇게 자동 주입과 수동 주입이 코드에 섞여 있으면 주입을 제대로 하지 않아 NPE가 발생할 수 있으므로 일관되게 사용하는 편이 낫습니다.<br>
</div>
</details>
