# Daily Algorithm
19-05-14
### Codility
A 배열은 다음 엘리먼트들로 이뤄져있다: 짝을 이루는 숫자들, 짝을 이루지 않는 하나의 숫자.

짝을 이루지 않는 숫자를 리턴한다.

(codility의 테스트는 999,999 length의 랜덤 내용 배열까지 테스트한다. 아래 답안은 결과 len
```js
function solution(A) {
    // 1. 엘리먼트의 값을 key로, 각 값에 해당하는 엘리먼트 개수를 센다.
    // 1-1. 셀때 unpaired 후보 오브젝트에 등록한다.
    // 1-2. 이미 있다면 후보 오브젝트에서 지운다.
    // 2. 반복이 끝나면, 유일한 object의 키를 리턴한다.
    
    const dict = {};
    const nominee = {};
    A.forEach(cur => {
        if (!dict[cur]) {
            dict[cur] = 1;
            nominee[cur] = cur;
        } else {
            // dict[cur] += 1;
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
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg4NTk5ODY2MCwyODA4NDQ3MjFdfQ==
-->