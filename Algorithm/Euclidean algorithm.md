## 유클리드 알고리즘(Euclidean algorithm)
2개 자연수의 최대공약수(gcd)를 구하는 알고리즘이다  

**원리**
>1. 두 수 x, y(x > y)를 입력
>2. y가 0이라면 x가 최대공약수(gcd)
>3. 아니라면 x에 y대입 y에 x % y를 대입하고 다시 반복한다.

### 코드(C언어) 재귀 이용
```c
void gcd(int a, int b){
	if (b == 0){
		printf("최대공약수는 %d",a);
	}
	else{
		gcd(b,a%b);
	}
}
```
### 코드(C언어) 반복 이용
```c
int gcd(int a, int b){
	int temp;
	while(b != 0){
		temp = a%b;
		a = b;
		b = temp;
	}
	return a;
}
```
