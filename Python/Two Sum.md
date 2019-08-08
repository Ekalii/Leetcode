## 문제
--------
Given an array of integers, return indices of the two numbers such that they add up to a specific target.<br></br>
You may assume that each input would have exactly one solution, and you may not use the same element twice.


해석하자면, 정수배열(nums)이 있고 정수형 변수(target)이 있다.<br></br>
정수배열 안에있는 **정수 2개**를 더해서 target값이 되는데, 그때 **두 정수의 인덱스값을 리스트형으로** 반환하면 된다.<br></br>


예제를 보자.

Given nums = [2, 7, 11, 15], target = 9,<br></br>
Because nums[0] + nums[1] = 2 + 7 = 9,<br></br>
return [0, 1].<br></br>
* 즉, 2의 인덱스값이 0이고, 7의 인덱스값이 1이므로 반환값으로 [0,1]이 된다.


## 답
-------
```python
class Solution(object):
    def twoSum(self, nums, target): 
        for i in range(len(nums)): 
            for j in range(i+1, len(nums)):
                if nums[i]+nums[j] == target:
                    return [i,j]
```        

필자는 이중for문을 사용해서 문제를 해결했다.<br></br>
항상 i는 j보다 작아야 하므로 2번째 반복문에는 j의 범위를 i보다 크게 설정했다.
