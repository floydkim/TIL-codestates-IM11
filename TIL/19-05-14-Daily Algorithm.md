# Daily Algorithm
19-05-14
### Codility
A 배열은 다음 엘리먼트들로 이뤄져있다: 짝을 이루는 숫자들, 짝을 이루지 않는 하나의 숫자.

짝을 이루지 않는 숫자를 리턴한다.

```js
function solution(A) {
    // 1. 엘리먼트의 값을 key로, 각 값에 해당하는 엘리먼트 개수를 센다.
    // 1-1. 셀때 unpaired 후보 오브젝트에 등록한다.
    // 1-2. 이미 있다면 후보 오브젝트에서 지운다.
    // 2. 반복이 끝나면, 유일한 object의 키를 리턴한다.
    
    const dict = {};
    const nominee = {};
    A.forEach(cur => {
        if (!dict[cur] || dict[cur] % 2 === 0) {
            dict[cur] = 1;
            nominee[cur] = cur;
        } else {
            dict[cur] += 1;
            delete nominee[cur];
        }
    });
    
    const keys = Object.keys(nominee);
    if (keys.length === 0) {
        return 0;
    }
    return Number(keys[0])
}
```

깔끔하게 풀지는 못한거같다. 테스트 케이스를 모두 알 수 없어서, 제출 후 결과로 어떤부분이 문제인지 유추해야 하는

> Detected time complexity: O(N) or O(N*log(N))
<!--stackedit_data:
eyJoaXN0b3J5IjpbNzAyNjUwODEsLTIwMTUyMTg4NDEsNjMzMj
I4ODQ5LDI4MDg0NDcyMV19
-->