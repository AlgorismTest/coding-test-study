### 문제 이해하기
스택의 개념 관련 문제

### 문제 접근 방법


### 구현 배경 지식


### 해결하지 못한 이유
연산자가 나오는 경우에만 스택을 이용한다라는 개념에는 잘 접근했다. 하지만, 백준에 존재하는 테스트 케이스 이외의 케이스에 대한 해결책을 찾지 못했음.
<br>
ex) A+(B+C)*D
<br>
연산자의 우선순위에 대한 접근을 세부적으로 하지 못해서 오류가 발생


### 문제를 해결한 코드

### 문제를 해결한 방법
() < +- < */ 이런식으로 연산자의 우선순위를 명확하게 잡은뒤 스택에 우선순위가 낮은 연산자가 들어오려고 한다면 바로 전체 pop을 진행한다.
