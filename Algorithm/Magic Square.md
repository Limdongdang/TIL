마방진(magic square)
========================


## 마방진(magic square)이란? 
>정사각형에 1부터 차례로 숫자 적되 숫자를 중복하거나 빠뜨리지 않고 가로,세로, 대각선에 있는 수들의 합이 모두 같도록 만든 숫자의 배열을 의미

### coxeter's 방법
홀수 크기의 마방진이여야 한다.
***
1. 첫 번째 행의 중앙에 1을 넣는다.
2. 왼쪽 대각선 위 방향으로 올라가면서 1증가 값을 넣는다.
3. 이때 행렬의 밖으로 벗어나면 그 방향의 반대편에서 계속한다
4. 이동하려는 자리에 숫자가 이미 채워져 있으면 지금 위치 바로 아래에 숫자를 놓는다.
