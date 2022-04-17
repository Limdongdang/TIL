## 이진 탐색(Binary_Search)
>오름차순으로 정렬된 n 개의 데이터를 검색하는데 0 ~ n-1까지의 검색범위에서 중앙값을 찾아 이것을 키 값과 비교해서 검색 범위를 절반씩 줄여서 검색하는 알고리즘이다.

### 장점
> 더 적은 연산 횟수 구성으로 빠른 검색 가능
### 알고리즘 구상
1. 입력데이터 준비
2. 검색구간 설정
3. 검색구간에 데이터가 있으면 다음 수행 없으면 4.로 
4. 주어진 데이터 집합 안에 key값이 없으면 -1 반환

### 코드(C언어)
```c
while(left <= right){   // 검색 범위에 값이 있는 경우
  mid = (left+right)/2; // 중앙 값 설정
  if (key < list[mid]) {right = mid - 1;}  //찾으려는 값이 왼쪽에 있는 경우 오른쪽 범위를 축소
  else if(key > list[mid]) {left = mid + 1;} // .. 오른쪽에 있는 경우 왼쪽 범위 축소
  else return mid;   // 결과 값을 찾고 return
}
return -1;
```