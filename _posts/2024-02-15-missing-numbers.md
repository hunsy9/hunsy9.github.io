---
title:  "[LeetCode] Missing Numbers"
date: 2024-02-15 11:48:00 +/-TTTT
categories: [Algorithm, LeetCode]
tags: [Hashing]
image:
  path: /assets/img/algorithm/leetcode.png
  alt: LeetCode
---

**문제 설명**:
Given an array ```nums``` containing ```n``` distinct numbers in the range ```[0, n]```, return the only number in the range that is missing from the array.

**제약 조건**:
- ``` n == nums.length ```
- ``` 1 <= n <= 10^4 ```
- ``` 0 <= nums[i] <= n```
- All the numbers of ```nums``` are **unique**

**난이도**: ```EASY```

**Follow up**
- Could you implement a solution using only O(1) extra space complexity and O(n) runtime complexity?
  <br>
  <br>

## 문제 이해
---
- 입력으로 들어오는 Nums의 length가 n 이다.
- range [0, n] 와 nums를 비교해서 nums에 없는 수를 출력한다.
- 공간 복잡도 O(1), 시간 복잡도 O(n)에 풀자...

<br>


## 문제를 보며 처음 한 생각
---
만약 n이 3이라고 하고, nums = [3,0,1]이라고 하자.
range [0,3] 즉 0,1,2,3 중에 nums에 없는 것을 찾는건데..

$$\sum_{k=1}^{n} k$$ = (n * (n+1)) / 2
이므로, (n * (n+1)) / 2 - sum(nums) 하면 되지 않을까??

<br>


## 문제를 해결한 방법
---

처음 생각한 방법이 잘들어맞았다.
파이썬 sum() 함수는 O(n)이고, 추가적인 공간은 변수 선언한 것 뿐이니 제약조건도 알맞다

```python
class Solution:
    def missingNumber(self, nums: List[int]) -> int:
        n = len(nums)
        return int(((n * (n+1)) / 2) - sum(nums))
```

<br>




