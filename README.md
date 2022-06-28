# Interview-prep
![Cute Key Illustration Motivational Quote Instagram Post](https://user-images.githubusercontent.com/42097653/175800538-fef5f94e-70ab-4cda-9074-dbc1fe59a460.png)

Repo for managing my interview prepration. 

## Resources: 
* Leetcode: https://leetcode.com/
* CodeForces: https://codeforces.com/

## Overall Progress. 
## Easy questions 

|Name of Question|Status of Completion|Solution|
|---|---|---|
|   |   |   |
|   |   |   |
|   |   |   |
|   |   |   |
|   |   |   |
|   |   |   |

## Medium Questions 
|Name of Question|Status of Completion|Solution|
|--:|---|---|
|[reverse-integer](https://leetcode.com/problems/reverse-integer)| ✅ |[goto_day](https://github.com/someshfengde/Interview-prep/blob/main/README.md#26th-june)|
|[3sum](https://leetcode.com/problems/3sum/)| ✅ | [goto_day](https://github.com/someshfengde/Interview-prep/blob/main/README.md#28th-june)   |
|   |   |   |
|   |   |   |
|   |   |   |
|   |   |   |

## Hard questions 
|Name of Question|Status of Completion|Solution|
|--:|---|---|
|[regular-expression-matching](https://leetcode.com/problems/regular-expression-matching)| ✅ |[goto_day](https://github.com/someshfengde/Interview-prep/blob/main/README.md#28th-june)   |
|   |   |   |
|   |   |   |
|   |   |   |
|   |   |   |
|   |   |   |

## Solutions 
### 26Th June 
```
class Solution:
    def reverse(self, x: int) -> int:    
        fin_str = ""
        if x < 0 :
            fin_str = "-"
        x = str(abs(x))[::-1]
        fin_str += x 
        if (abs(int(x)) > int(2**31 - 1)):
            return 0 
        return int(fin_str)
 ```
### 28th June 
`re`
```
import re 
class Solution:
    def isMatch(self, s: str, p: str) -> bool:
        r = re.search(p, s) 
        if r and r.group(0) == s:
            return True
        return False
```
`three sum`
```
class Solution:
    def threeSum(self, nums: List[int]) -> List[List[int]]:
        sorted_num = sorted(nums)
        ans_arr = []
        for x in range(len(nums)-2):
            if x == 0 or ( x> 0 and sorted_num[x] != sorted_num[x-1]):
                lo = x + 1 
                hi = len(nums) -1 
                while lo < hi: 
                    dum = sorted_num[lo] + sorted_num[hi] 
                    req = sorted_num[x] * -1 
                    if  sorted_num[lo] + sorted_num[hi] == req :
                        ans_arr.append([sorted_num[lo], sorted_num[hi], sorted_num[x]] )
                        while lo < hi and sorted_num[lo] == sorted_num[lo + 1 ]: 
                            lo+=1 
                        while lo< hi and sorted_num[hi] == sorted_num[hi-1]:
                            hi -=1 
                        lo +=1 
                        hi -=1 
                    elif dum < req: 
                        lo += 1 
                    else : 
                        hi -= 1 

        return ans_arr
                    
                    
```


