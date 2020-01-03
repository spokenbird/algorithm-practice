# algorithm-practice

Two Sum - Leetcode #1
```javascript
var twoSum = function(nums, target) {
    let visited = {};
    for (let i = 0; i < nums.length; i++) {
        let current = nums[i];
        if (target - current in visited) {
            return [visited[target - current], i]
        } else {
            visited[current] = i;
        }
    }
};
```

Three Sum - Leetcode #15
https://leetcode.com/problems/3sum/