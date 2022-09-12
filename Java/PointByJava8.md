## 자바 8버전 특징

<details>
<summary>Java 8</summary>
<div markdown="1">
자바8에서는 여러 가지 변화들이 추가되었습니다. `Lambda 표현식`, `Stream API`, `Joda-Time을 이용한 새로운 날짜와 시간 API`, `StringJoiner` 등이 추가되었고 람다와 스트림을 통해 함수형 프로그래밍을 자바에서도 어느정도 사용할 수 있게 되었습니다.<br>
Lambda와 Stream을 통해 자바에서도 함수형 프로그래밍을 어느 정도 적용할 수 있게 되었고 Joda-time을 이용해 LocalDateTime등 새로운 API등이 등장했습니다.<br>
또한 StringJoiner을 통해 편리하게 문자열을 연결할 수 있게 되었습니다.<br><br>
  
자바8부터는 Heap영역의 Permanent Generation이 Metaspace로 대체되었습니다. <br>
자바8 이전에는 개발자가 직접 PermSize와 MaxPermSize를 설정해 주어야 했으나 자바8부터는 Metaspace가 런타임시 자동으로 메모리 요구사항에 맞추어 크기를 조절하고 필요하다면 MaxMetaspaceSize 조절을 통해 개발자가 직접 크기를 조절할 수 있습니다.<br>
PG가 Metaspace로 대체된 이유는 Metaspace 영역은 Heap이 아닌 Native 메모리 영역으로 취급하게 됩니다. (Heap 영역은 JVM에 의해 관리된 영역이며, Native 메모리는 OS 레벨에서 관리하는 영역으로 구분됩니다) Metaspace가 Native 메모리를 이용함으로서 개발자는 영역 확보의 상한을 크게 의식할 필요가 없어지게 되었습니다.<br><br>
  
`HashMap`, `LinkedHashMap`, `ConcurrentHashMap`의 퍼포먼스가 향상되었습니다.<br>
기존에는 키 충돌이 많은 아이템들을 LinkedList로 관리했는데, 8부터는 일정 이상 길어지면 balanced tree로 관리하게 되었습니다.<br>
결과적으로 최악의 경우 시간복잡도가 O(n)에서 O(log n)으로 향상되었습니다.

</div>
</details>

[Java8 vs Java11](https://steady-coding.tistory.com/598)<br>
[Java8부터의 HashMap 성능향상](https://johngrib.github.io/wiki/java8-performance-improvement-for-hashmap/)
