## 유니티

## TransForm 컴포넌트



## 스크립트

스크립트는 독립적으로 혼자 실행할 수 없다. 오브젝트에 컴포넌트로 연결해야 함

## Time.deltaTime

>  1 프레임 당 걸리는 시간을 float 형으로 반환

컴퓨터 간 성능 차이로 인해 동일한 프로그램도 다른 컴퓨터에선 1 프레임이 걸리는 시간이 각자 다를 수 있음

Time.deltaTime을 이용해서 이 차이를 메꿀 수 있음
이동을 각자 성능이 다른 컴퓨터에 동일하게 이동하게 하려면

1. 한 프레임에 0.5 초가 걸리는 컴퓨터의 프로그램
   * 이동 속도 x Time.deltaTime(0.5) = 1 프레임 당 이동 거리
   * 30 x 0.5 = 1 프레임 당 15의 이동 거리를 가진다.
2. 한 프레임에 1 초 걸리는 컴퓨터의 프로그램
   * 이동 속도 x Time.deltaTime(1) = 1 프레임 당 이동 거리
   * 30 x 1 = 1 프레임 당 30의 이동 거리를 가진다.

즉 두 컴퓨터 모두 1 초에 30의 이동 거리를 가지게 된다.

## vector 클래스

* ## vector2

  * 

* ## vector3

