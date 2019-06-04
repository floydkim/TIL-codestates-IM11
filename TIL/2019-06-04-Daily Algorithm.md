---
title: Daily Algorithm
date: 2019-06-04 17:06:23
category: TIL
---
2019-06-04
## Programmers
### 폰켓몬

nums 배열에 폰켓몬 종류에 대응하는 숫자가 담겨있다.
> [3, 2, 1, 3]

nums에 담겨 온 폰켓몬 N개 중 N/2개 가져가는데, 최대한 많은 종류를 골라 가져간다.
이 때

```javascript
function solution(nums) {
    // input [3,2,1,3] output 2
    // 1. 엘리먼트의 종류:갯수 를 오브젝트에 기록
    // 2. 종류의 수가 length/2 보다 크거나 같으면 length/2 가 최대값
    // 3. 종류의 수가 length/2 보다 작으면 종류의 수가 최대값
    var answer = 0;
    const dictionary = {};
    // let numberOfMons = 0; // answer로 대체
    for (let i = 0; i < nums.length; i++) {
        if (!dictionary[nums[i]]) {
            dictionary[nums[i]] = 1;
            answer += 1;
        }
    }
    
    // const numberOfMons = Object.keys(dictionary).length; // answer로 대체

    // return 시 삼항연산자로 대체
    // if (numberOfMons >= nums.length / 2) {
    //     answer = nums.length / 2;
    // } else {
    //     answer = numberOfMons;
    // }
    
    const halfOfNumslength = nums.length / 2; // 변수를 하나 늘리지만 나누기 연산을 한번만 하기 위함
    return answer >= halfOfNumslength ? halfOfNumslength : answer;
}
```

스터디하는 날 페어 코딩 인터뷰 문제로 받아 풀었음.

<!--stackedit_data:
eyJoaXN0b3J5IjpbNjk1MDU4OTU0LDE4NjMwMTA1NjVdfQ==
-->