## 코틀린에서 null을 다루기

<details>
<summary> 코틀린에서는 null 처리를 어떻게 하나요?</summary>
<div markdown="1">
Safe Call -> null이 아니면 실행하고, null이면 실행하지 않는다. 표기법은 "test?.fieldName" <br>
Elvis 연산자 -> 식의 연산 결과가 null이면 뒤의 값을 사용한다. 표기법은 "test?.length ?: 0"<br>
단언 연산자 -> nullable type이지만 아무리 생각해도 null이 될 수 없는 경우에 사용한다. 정말 확실한 경우에만 사용하자! 표기법은 "test!!"<br>
<br><br>


</div>
</details>
