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
|![reverse-integer](https://leetcode.com/problems/reverse-integer)| ✔️ ||
|   |   |   |
|   |   |   |
|   |   |   |
|   |   |   |
|   |   |   |

## Hard questions 
|Name of Question|Status of Completion|Solution|
|--:|---|---|
|   |   |   |
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



