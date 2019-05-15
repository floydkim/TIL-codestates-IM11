# Daily Algorithm
19-05-15
### Codility

```js
function solution(A, K) {
    // boundary condition 적용
    // K만큼 미룬 인덱스를 길이로 나눈 나머지가 다시 어레이의 앞쪽으로 가리킬 것이므로
    // 자연스럽게 loop이 형성된다.
    
    // 길이만큼 미뤄서 변화가 없어야 할 경우 바로 원본 어레이 리턴
    if (A.length / K === 1) {
        return A;
    }
    
    let resultArr = [];
    for (let i = 0; i < A.length; i++) {
        resultArr[i] = A[(i + K - 1) % A.length];
    }
    return resultArr;
}
```

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc3MzU0NTk5MywxMTU1MzUwNzkxXX0=
-->