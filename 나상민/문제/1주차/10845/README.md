# 큐

### 문제 이해하기
큐의 6가지의 명령어(push,pop,size,empty,front,back)를 받아서 처리하는 프로그램 만들기
### 문제 접근 방법
배열을 이용하여 queue 자료구조를 만들어야 한다.
### 구현 배경 지식
queue 메소드에 대한 지식이 필요하다.
### 해결하지 못한 이유 (적을게 있을 경우에만)
1. size필드를 first와 last로 두개를 지정하는게 중요하다.
2. pop메소드를 사용할때 맨 앞의 값을 지우지는 못하니까 값을 가져온뒤 first값을 올린다.
3. 배열의 크기가 계속 늘어나기 때문에 10001로 넉넉하게 준다.
### 문제를 해결한 방법
명령문 별로 메소드를 구성한 다음 N번 루프를 돌면서 case문으로 명령문에 맞는 메소드를 호출한다.
