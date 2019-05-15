# Daily Algorithm
19-05-15
### Codility
A 어레이가 주어지고, K 정수 만큼 오른쪽으로 어레이 내용을 미루는 문제. (rotate 시키는 문제)

pop과 unshift를 이용해 하나씩 옮겨줄 수도 있겠지만, 이전에 물리 계산 C 프로그램 짤 때 boundary condition을 만들던것 생각나서 array의 length라는 boundary를 벗어날 때 array의 0번 인덱스쪽으로 연결하는 방식으로 궇

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
        resultArr[(i + K) % A.length] = A[i];
    }
    return resultArr;
}
```

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTI2MDY4NjI2OSwtNzczNTQ1OTkzLDExNT
UzNTA3OTFdfQ==
-->