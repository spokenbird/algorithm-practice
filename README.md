# algorithm-practice

Stones and Jewels - Leetcode #771
```javascript 
var numJewelsInStones = function(J, S) {
    let jewels = new Set();
    let myJewelsCount = 0;
    
    for (const char of J) {
        jewels.add(char);
    }
    for (const char of S) {
        if (jewels.has(char)) myJewelsCount++;
    }
    
    return myJewelsCount;
};
```

Defanging an IP Address - Leetcode #1108
```javascript
var defangIPaddr = function(address) {
    let output = '';
    for (let i = 0; i < address.length; i++) {
        address[i] === '.' ? output += '[.]' : output += address[i];
    }
    
    return output;
};
```

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

Reverse Int - Leetcode #7
``` JavaScript

function reverse(int) {
    let reversedStr = parseInt(
        int.toString()
        .split('')
        .reverse()
        .join('')
    );
    let reversedInt = parseInt(reversedStr) * Math.sign(int);
    let max = Math.pow(2, 31) - 1;
    let min = Math.pow(-2, 31);
    
    return reversedInt > min && reversedInt < max ? reversedInt : 0;
    
}

```