# Daily Algorithm
> Haker rank



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

<!--stackedit_data:
eyJoaXN0b3J5IjpbNzA1NzM0OTgwXX0=
-->