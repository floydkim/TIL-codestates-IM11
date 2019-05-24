---
title: Daily Algorithm
date: 2019-05-24 17:06:23
category: TIL
---
2019-05-24
## Programmers
### 약수의 합
정수 n (0 포함 양수)이 주어졌을 때 n의 모든 약수를 더한 숫자를 리턴하는 문제.
```js
function solution(n) {
    // 1. n의 모든 약수를 구한다
    // 1-1. 2부터 n - 1까지 n 나눠봄. % === 0 때 마다 answer에 더함
    // 2. answer를 리턴
    let answer = n;
    for (let i = 1; i < n; i++) {
        if (n % i === 0) {
            answer += i;
        }
    }
    return answer;
}
```
단순하게 1부터 n-1까지 모두 나눠봐서 구함.
0의 경우 예외처리를 해야겠다고 생각하고 if문을 넣었었는데, 짜놓고 보니 n이 0이나 1이면 for문을 돌지 않으니 answer가 각각 0이나 1이 나올 것으로 보고 예외처리 부분을 제거했다.

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTAzNDk4NjQxLC02MjEwMzQ5MTFdfQ==
-->