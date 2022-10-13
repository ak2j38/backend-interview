## 스프링 ComponentScan 정리

<details>
<summary> 컴포넌트 스캔에 대해 설명해주세요. </summary>
<div markdown="1">
컴포넌트 스캔은 스프링이 직접 클래스를 검색해서 빈으로 등록해주는 기능입니다. 설정 클래스에 빈으로 등록하지 않아도 원하는 클래스를 빈으로 등록할 수 있으므로 컴포넌트 스캔 기능을 사용하면 설정 코드가 크게 줄어듭니다.<br>
스프링이 검색해서 빈으로 등록할 수 있으려면 클래스에 @Component 어노테이션을 붙입니다. 이후 @ComponentScan 어노테이션이 붙어있는 패키지와 하위 패키지에서 @Component, @Controller, @Service, @Repoistory 어노테이션 등이 붙어있는 클래스들을 스캔해 빈으로 등록합니다.<br>
만약 제외시키고 싶은 클래스들이 있다면 excludeFilter 속성을 사용해 제외하면 됩니다.<br>  
</div> 
</details>
