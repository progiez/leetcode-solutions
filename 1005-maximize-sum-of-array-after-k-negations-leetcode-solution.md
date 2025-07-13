# LeetCode 1005. Maximize Sum Of Array After K Negations LeetCode Solution

🔗 [View full solution with explanation here](https://progiez.com/1005-maximize-sum-of-array-after-k-negations-leetcode-solution)

---
### 🚀 Python

```python
class Solution:
  def largestSumAfterKNegations(self, nums: list[int], k: int) -> int:
    nums.sort()

    for i, num in enumerate(nums):
      if num > 0 or k == 0:
        break
      nums[i] = -num
      k -= 1

    return sum(nums) - (k % 2) * min(nums) * 2 # code by PROGIEZ
```

---
