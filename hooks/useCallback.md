# useCallback
<a href ='https://reactjs.org/docs/hooks-reference.html#usecallback'>official doc</a>

    const memoizedCallback = useCallback(
    () => {
        doSomething(a, b);
    },
    [a, b],
    );

Returns a memoized callback.
### Memoized
In computing, memoization or memoisation is an optimization technique used primarily to speed up computer programs by storing the results of expensive function calls and returning the cached result when the same inputs occur again. 

## 기능
Pass an inline callback and an array of dependencies. useCallback will return a memoized version of the callback that only changes if one of the dependencies has changed. 

## useMemo 와의 관계
useCallback(fn, deps) is equivalent to useMemo(() => fn, deps).

### 주의사항
every value referenced inside the callback should also appear in the dependencies array.
( dependency 배열에 포함된 친구들이 변경되는 경우에만 callback 을 던져주는 기능을 하는거니까, 당연히 callback 에 사용되는 변수들이 다 dependency 배열에 포함되어야 하는 것은 당연한 이야기!)

