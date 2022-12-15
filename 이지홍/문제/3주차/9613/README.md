# GCD 합

### 문제 이해하기

### 문제 접근 방법

### 구현 배경 지식

> 📍 최대공약수
> - 최대공약수는 두 수 A와 B의 공통된 약수 중에 가장 큰 정수이다.
> - 최대공약수를 구하는 가장 쉬운 방법은 2부터 min(A, B)까지 모든 정수로 나누어보는 방법이다.

```javascript
let getGCD = (num1, num2) => {
    let gcd = 1;

    for(let i=2; i<=Math.min(num1, num2); i++){
        if(num1 % i === 0 && num2 % i === 0){
            gcd = i;
        }
    }

    return gcd;
}
```

> 📍 최소공배수
> - 두 수, 혹은 그 이상의 여러 수의 공통인 배수 중 가장 작은 수이다.
- lcm을 1부터 시작하여 점차 lcm++하면서 각각의 두 수를 lcm으로 나누었을 때 나머지 값이 0인지를 비교한다.

```javascript
let getLCM = (num1, num2) =>{
	let lcm = 1;
   
    while(true){
      if((lcm % num1 == 0) && (lcm % num2 == 0)){
        break;
      }
      lcm++;
    }
  	return lcm
}
```

참고 : https://velog.io/@devjade/JavaScript%EB%A1%9C-%EC%B5%9C%EB%8C%80%EA%B3%B5%EC%95%BD%EC%88%98GCD-%EC%B5%9C%EC%86%8C%EA%B3%B5%EB%B0%B0%EC%88%98LCM-%EA%B5%AC%ED%95%98%EA%B8%B0

### 해결하지 못한 이유

### 문제를 해결한 방법

입력되는 값들을 gcd function에 각각 보내주어 최대공약수를 구한 후, 결과값을 result에 더한 후, answer에 각각 줄에 대한 result값을 더해줌.