# Daily Algorithm
### Haker rank
`ar` : 양말의 색을 숫자로 표현한 어레이
만약 [10, 20, 20, 10, 10, 30]이 주어졌다면, 같은 색 양말이 10 한 쌍, 20 한 쌍으로 총 두 쌍 존재하며 그 총 수를 리턴하는 문제.



```javascript
function sockMerchant(n, ar) {
    let dic = {};
    let count = 0;
    ar.forEach(cur => {
        if (!dic[cur]) {
            dic[cur] = 1;
        } else {
            dic[cur] += 1;
        }
        if (dic[cur] % 2 === 0) {
            count++;
        }
    })
    return count;
}
```

### codility


```javascript
function solution(N) {
    // write your code in JavaScript (Node.js 8.9.4)
    let binary = N.toString(2);
    // 10001001
    // 1. binary string에서 모든 1의 인덱스를 순서대로 저장한다 (어레이에)
    // 2. 각 엘리먼트간 차를 구해 가장 큰 수를 리턴한다.
    // (예외처리) 1이 없거나, 1이 하나뿐이면 0을 리턴한다. (어레이 length로 판단)
    
    let indices = [];
    
    for (let i = 0; i < binary.length; i++) {
        if (binary[i] === "1") {
            indices.push(i);
        }
    }
    
    if (indices.length === 0 || indices.length === 1) {
        return 0;
    }
    
    let largest = 0;
    for (let i = 1; i < indices.length; i++) {
        if (indices[i] - indices[i - 1] - 1 > largest) {
            largest = indices[i] - indices[i - 1] - 1;
        }
    }
    return largest;
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTg2MTM5MDIwNiw3MDU3MzQ5ODBdfQ==
-->