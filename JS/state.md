## useState() 함수는 비동기적 특성을 가진다.

```js
const App = () => {
    const [count, setCount] =  useState(0);

    const onPlus = () => {
        setCount(count+1);
        setCount(count+1);
        setCount(count+1);
        setCount(count+1);
        setCount(count+1);
    }
	return (
		<div>
            <button onClick={onPlus}>button</button>
            <h1>{count}</h1>
        </div>
	)
}
```

React에서 다음과 같은 이벤트 함수에서 버튼을 누르게 되면 count 값은 어떻게 변할까?     
내가 원하는 값은 5씩 더해지는 것이지만 count 값은 1씩 더해지게 된다.    
count의 상태 값은 setValue를 통해 초기 렌더링시에 설정 되었던 초기값만을 가져오기 때문에    
동시에 여러 개의 setValue 을 하게 되면        
항상 ```0 + 1```의 결과 값만을 가져오는 것이다.     

따라서 count와 같이 이전 값에 의존해야 되는 상황이 오게 되면
항상 최신 값을 받아 올 수 있도록 해야 한다.



## 함수형 업데이트

이런 문제를 해결하기 위한 방법이 있다 바로 인자를 함수로 전달하는 것이다.

```js
const App = () => {
    const [count, setCount] =  useState(0);

    const onPlus = () => {
        setCount(prevCount => prevCount + 1);
        setCount(prevCount => prevCount + 1);
        setCount(prevCount => prevCount + 1);
        setCount(prevCount => prevCount + 1);
        setCount(prevCount => prevCount + 1);
    }
    return (
        <div>
            <button onClick={onPlus}>버튼</button>
            <h1>{count}</h1>
        </div>
    );
}
```

이렇게 함수를 인자로 전달하게 된다면 prevCount인자 값으로 항상 최신 값을 가져와서         
계산하게 되고 원하는 결과 값인 5씩 증가의 결과를 얻을 수 있게 된다.           
인자의 최신 값을 가져올 수 있는 이유는 Closure 때문이라고 한다           
간략하게 설명하자면 함수가 생성되는 순간의 속성 값들을 기억한다는 것이다.        
따라서 함수가 실행 될 때마다 인자 값을 최신 상태로 유지하고 보장하게 되는 것이다.      

## 상향식 자식 -> 부모 컴포넌트 통신

> 함수를 통해서 매개 변수를 통해 자식의 속성 값들을 부모 컴포넌트에 전달 할 수 있다 



부모 컴포넌트에서 props를 통해 자식 컴포넌트로 함수를 전달하고
자식 컴포넌트에서는 부모 컴포넌트의 함수를 불러와 매개변수로 속성값들을 전달한다. 



## state 끌어올리기
![제목 없는 다이어그램 drawio](https://user-images.githubusercontent.com/50188317/227777334-770ef543-3aa1-4f30-b9a3-e2cf2f245235.png)

두 형제 컴포넌트 끼리는 데이터를 전달 할 수 없다.

![제목 없는 다이어그램 drawio (2)](https://user-images.githubusercontent.com/50188317/227777337-cc6be9db-b938-4a0b-8f32-4b309eea16a6.png)

따라서 state 끌어올리기를 통해 부모 컴포넌트로 데이터를 끌어올리고 이 끌어올린 데이터를 다시 데이터가 필요한 자식 컴포넌트로 전달해야 한다.

데이터를 생성하는 컴포넌트에서 데이터가 필요한 컴포넌트까지 전달을 하기 위해선 필요한 부분까지 state 끌어올리기를 할 필요가 있다.

## 용어

* stateful 컴포넌트 : state를 다루는 컴포넌트
* stateless 컴포넌트 : state를 다루지 않는 컴포넌트

참고:          
https://talkwithcode.tistory.com/88          
https://velog.io/@tjdgus0528/React-Native-5x048oii
