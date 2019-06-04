---
title: Daily Algorithm
date: 2019-06-04 17:06:23
category: TIL
---
2019-06-04
## Programmers
### 폰켓몬



```javascript
function solution(nums) {
    // input [3,2,1,3] output 2
    // 1. 엘리먼트의 종류:갯수 를 오브젝트에 기록
    // 2. 종류의 수가 length/2 보다 크거나 같으면 length/2 가 최대값
    // 3. 종류의 수가 length/2 보다 작으면 종류의 수가 최대값
    var answer = 0;
    const dictionary = {};
    // let numberOfMons = 0;
    for (let i = 0; i < nums.length; i++) {
        if (!dictionary[nums[i]]) {
            dictionary[nums[i]] = 1;
            answer += 1;
        }
    }
    
    // const numberOfMons = Object.keys(dictionary).length;
    
    // if (numberOfMons >= nums.length / 2) {
    //     answer = nums.length / 2;
    // } else {
    //     answer = numberOfMons;
    // }
    
    const halfOfNumslength = nums.length / 2;
    return answer >= halfOfNumslength ? halfOfNumslength : answer;
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbNzg5MjU5MDM0LDE4NjMwMTA1NjVdfQ==
-->