## JWT 개념과 사용 이유

<details> 
<summary>JWT란 무엇인가요?</summary>
<div markdown="1">
JWT란 토큰 인증 방식의 일종으로 서버에 세션 정보를 저장하지 않고, 로그인 시 클라이언트에게 로그인 사용자 정보가 포함된 토큰을 발행하고 클라이언트는 특정 요청마다 이 토큰을 함께 보냅니다. 토큰을 받은 서버는 토큰을 파싱해 인증과 인가 작업을 진행합니다.<Br>
JWT는 헤더, 시그니쳐, 페이로드로 구성되어 있습니다. 헤더는 토큰의 타입(Bearer), 암호화 알고리즘을 담고 있고, 페이로드는 토큰의 정보를 담습니다. 시그니쳐는 jwt 비밀키로 만들어진 일련의 문자열로 토큰의 정보가 신뢰할 수 있는 것인지 판단할 수 있도록 합니다.<br>
</div>
</details>



<details>
<summary>JWT를 왜 사용했나요?</summary>
<div markdown="1">
REST의 특징 중 stateless라는 특징이 있는데 사용자의 상태 정보를 서버에 저장하지 않는 특성입니다. <br>
또한 Scale-out의 가능성을 고려해 세션의 정합성을 맞추는 작업보다 JWT를 사용하는 것이 더 좋다고 판단했습니다.<br>
</div>
</details>
  
  
[JWT 인증은 무엇이고 어떻게 사용해야 할까](https://www.popit.kr/jwt-%ec%9d%b8%ec%a6%9d%ec%9d%80-%eb%ac%b4%ec%97%87%ec%9d%b4%ea%b3%a0-%ec%96%b4%eb%96%bb%ea%b2%8c-%ec%82%ac%ec%9a%a9%ed%95%b4%ec%95%bc-%ed%95%a0%ea%b9%8c/)
