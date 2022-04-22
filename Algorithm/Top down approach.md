## Top Down Approach (하향식 접근법)

- 복잡한 알고리즘을 작은 부분으로 나누어 문제 해결을 더욱 쉽게 하는 방법
- 위에서 아래로 접근하는 문제 해결 방식 아래로 갈수록 내용이 명확해짐
- 재귀적 호출을 이용해서 문제를 해결함

### 피보나치 수열
재귀적으로 구현한 피보나치 수열 하향식 접근법의 예시     
가장 큰 위의 문제를 부분 문제로 나눠서 결과를 보관한다.
<p><img src="https://user-images.githubusercontent.com/50188317/164586603-8da95933-b595-4461-bebc-37780772e346.png" height="300px" width="300px"></p>

```c
int f(int n){
	if(n == 1 || n == 2){
		return 1;
	}
	return f(n - 1) + f(n - 2);
}
```
