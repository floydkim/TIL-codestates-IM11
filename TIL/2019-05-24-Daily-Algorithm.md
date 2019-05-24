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

Time Complexity는 O(n)인데, n의 제곱근까지만 계산해도 모든 약수를 구할 수 있다.

```js
function solution(n) {
    let answer = 0;
    if (Math.sqrt(n) % 1 === 0) {
	    // n이 제곱수 형태라면 제곱근을 answer에 더해놓는다.
        answer += Math.sqrt(n);
    }
    for (let i = 1; i * i < n; i++) {
        if (n % i === 0) {
	        // 나누어 떨어진다면 제수와 몫이 둘 다 약수라는 뜻이므로 더한다.
            answer += i;
            answer += Math.trunc(n / i);
        }
    }
    return answer;
}
```
아쉬운 점은, 제곱근을 아래 for문 안에서 처리하고 싶은데 그렇게 못하겠다는거다.
(그리고 반복에 n을 포함시키면 n이 제곱수인 경우 제곱근을 두번 더한다. 예를들어 4의 약수는 1, 2, 4인데 for문을 돌고나면 1+4+2+2가 된다.)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMzI5MTEyMTQsMTAwMjE3MjYsLTYyMTAzND
kxMV19
-->