## 스프링 AOP 정리

<details>
<summary>스프링 AOP에 대해서 설명해 보세요.</summary>
<div markdown="1">
AOP란 간단하게 말해서 관점지향 프로그래밍입니다.<br>
관점지향 프로그래밍이란, 핵심적인 관점과 부가적인 관점으로 나누어 핵심적인 비즈니스 로직과 반복해서 쓰이는 코드를 분리 개발하여, 반복적인 코드의 재사용을 늘리는 것입니다.<br><br>
  
@Aspect : 해당 클래스가 부가기능을 갖는 clas임을 알려주는 어노테이션입니다.<br>
@Pointcut : 상세스펙정의(특정 패키지나 클래스 혹은 메소드 등)
Advice : 부가기능을 담은 구현체 - 어떤 기능을 언제 넣을 것인지<br>
Target : aspect를 적용하는 곳<br>
Joinpoint : advice의 적용위치<br><Br>
  
@Before : Advice 타겟 메소드가 호출되기 전에 Advice 기능 수행
@After : 타겟 메소드의 결과에 관게없이 타겟 메소드가 완료되면 Advice 기능 수행
@AfterRunning : 타겟 메소드가 성공적으로 결과값을 반환 한 후에 Advice 기능 수행
@AfterThrowing : 타겟 메소드가 수행 중 예외를 던지면 Advice 기능 수행
@Around : Advice가 타겟 메소드를 감싸 타겟 메소드 호출 전, 후에 Adivce 기능 수행 
  
  
</div>
</details>
