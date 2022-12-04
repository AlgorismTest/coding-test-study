# 📍 2주차 개념 정리

## 1. 에라토스테네스의 체
### 1.1 에라토스테네스의 체란?
소수 구하는 알고리즘
### 1.2 에라토스테네스의 체 구현 방법
1. 2부터 소수를 구하고자 하는 구간의 모든 수를 나열한다.
2. 소수가 되는 수의 배수를 지우면 남은 건은 소수만 된다
3. 자기 자신을 제외한 2의 배수를 모두 지운다.
4. 남아 있는 수 가운데 3은 소수이므로 오른쪽에 3을 쓴다.
5. 자기 자신을 제외한 3의 배수를 모두 지운다.
6. 남아 있는 수 가운데 5는 소수이므로 오른쪽에 5를 쓴다.
7. 자기 자신을 제외한 5의 배수를 모두 지운다.
8. 위 과정을 반복한다.
### 1.3 에라토스테네스의 체 구현 소스(JAVA)
예제로 4000000까지의 소수 구하기
```java
public class Solution {

	// 예제와 같이 120까지의 소수를 구하기 위해 120 선언.
	static boolean prime[] = new boolean[4000001];
	static ArrayList<Integer> prime_numbers = new ArrayList<>();
    
    public static void main(String[] args) throws Exception{
		
		// 구하고자 하는 숫자 범위
        int N = 4000000;
        
        // 소수는 false
        // 1은 소수가 아니므로 제외
        prime[0] = prime[1] = true;
        
        for(int i=2; i*i<=N; i++){
        	// prime[i]가 소수라면
            if(!prime[i]){
            	// prime[j] 소수가 아닌 표시
            	for(int j=i*i; j<=N; j+=i) prime[j]=true;                
            }        
        }    
        
        // 소수 출력
        for(int i=1; i<=N;i++){
        	if(!prime[i]) prime_numbers.add(i);     
        }
        
        // 4000000까지 소수 개수
        System.out.println(prime_numbers.size());
        // 소수 확인 
        for(int i=1; i<=10; i++) {
        	System.out.println(prime_numbers.get(i));
        }
        
    }
}
```