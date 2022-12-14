# 다이나믹 프로그래밍

다이나믹 프로그래밍은 메모리를 적절히 사용하여 시간복잡도를 비약적으로 단축시킬 수 있는 방법이다.
즉, 이미 계산된 결과를 별도의 메모리 공간에 저장하여 다시 계산하지 않는 방법이다.

## 다이나믹 프로그래밍의 조건
1. 최적 부분 구조
큰 문제를 작은 문제로 나눌 수 있으며, 작은 문제의 답을 모아서 큰 문제를 해결할 수 있다.
2. 중복되는 부분 문제
동일한 작은 문제를 반복적으로 해결한다.

## 피보나치 수열
피보나치 수열은 첫째, 둘째 항이 1이고 그 뒤의 모든 항은 바로 앞의 두 항의 합으로 이루어진 수열이다.
<br>
만약 재귀 함수를 사용하여 피보나치 수열을 구하게 된다면 o(2^n)의 시간복잡도를 가진다. 

## 메모제이션
메모제이션은 다이나믹 프로그래밍을 구현하는 방법 중 하나로서, 한 번 계산한 결과를 메모리 공간에 메모해두는 기법이다.
- 같은 문제를 다시 호출하면 메모리에 저장해둔 결과를 그대로 가져온다.
- 값을 기록해놓는다는 점에서 캐싱이라고도 부른다.

## 상향식 vs 하향식
#### 상향식
아래쪽에서부터 작은 문제들을 하나씩 해결해 나가면서 최종적으로 큰 문제의 해를 구한다.<br>
프로그래밍 언어에서는 반복문을 사용해서 구현한다.<br>
다이나믹 프로그래밍의 전형적인 방식이며, 부분해의 결과를 임시적으로 저장하는 배열을 dp 테이블이라고도 부른다.

#### 하향식
큰 문제를 작은 문제로 나눠서 작은 문제들의 해를 '재귀적으로' 구하고, 이를 취합하여 큰 문제의 해를 구하낟. 한 번 계산된 결과를 기억하기 위해 메모이제이션 기법을 이용한다. 

## DP vs 분할정복 알고리즘
다이나믹 프로그래밍과 분할정복 알고리즘은 모두 최적 부분 구조를 가질 때 사용할 수 있다.
즉, 큰 문제를 작은 문제로 나눌 수 있으며, 작은 문제의 답을 모아서 큰 문제를 해결할 수 있는 상황일 때 쓰인다. 
<br>
하지만 다이나믹 프로그밍은 각 부분 문제들이 독립되지 않고, 중복되는 부분 문제가 있어야 한다. 그리고 주로 점화식에 따라 작은 문제부터 하나씩 해결해나가면서 상향식으로 최종적인 해를 구하낟.
<br>
반면, 분할정복 알고리즘은 각 부분 문제가 독립적이고, 동일한 부분 문제가 반복적으로 계산되지 않는다. 그리고 큰 문제를 작은 문제로 분할하여 하향식으로 부분해를 구하고 이를 다시 취합하여 최종적인 해를 구한다.

## DP vs 그리디 알고리즘
매 단계마다 현재 최적이라고 판단되는 것만 근시안적으로 선택하는 그리디 알고리즘은 오직 현재의 최대 만족만을 추구하기 때문에 전체적인 최적해는 보장하지 못하는 경우가 많다.<br> 따라서 단순히 가장 좋아보이는 것만 반복적으로 선택해도 최적의 해를 구할 수 있는지 정당성을 분석하는 게 중요하다.
반면, 다이나믹 프로그래밍은 작은 문제에 대한 모든 가능성을 고려하여 다음 크기의 문제에 대한 최적해를 구하기 때문에 항상 최적의 결과를 얻을 수 있다. 

## 다이나믹 프로그래밍 적용 단계
1. 문제의 특성을 분석하여 최적 부분 구조가 성립하는지 확인
2. 주어진 문제에 대해 최적해를 제공하는 점화식을 도출
3. 가장 작은 부분 문제부터 점화식의 해를 구한 뒤 이를 테이블에 저장
4. 테이블에 저장되어 있는 부분 문제의 해를 이용하여 점차적으로 입력 크기가 큰 상위 문제의 해를 구한다.
