## 배열의 삽입 삭제

## 삽입
```cpp
void insert(int idx, int num, int arr[], int& len) {
	for (int i = 0; i <= len - idx; i++)
	{
		arr[len + 1 - i] = arr[len - i];
	}
	arr[idx] = num;
	len++;
}
```
## 삭제
```cpp
void erase(int idx, int arr[], int& len) {
	for (int i = 0; i <= len - idx; i++)
	{
		arr[idx + i] = arr[idx + i + 1];
	}
	len--;
}
```
