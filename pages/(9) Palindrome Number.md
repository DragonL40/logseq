- #Leetcode
- Given an integer `x`, return true if `x` is palindrome integer. 
  
  An integer is a palindrome when it reads the same backward as forward. For example, `121` is palindrome while `123` is not.
  ---
-
  > You can check for a palindrome number by reversing the number and comparing to the original number
- ## Solution 1: Reverse the Entire Number
	-
	  ```c++
	  #include <cmath>
	  
	  using namespace std;
	  
	  class Solution {
	  public:
	      bool isPalindrome(int x) {
	          long ans = 0;
	          int num = x;
	          while (num > 0) {
	              ans = ans * 10 + num % 10;
	              num /= 10;
	          }
	          return x == ans;
	      }
	  };
	  ```
	- However, this solution requires `ans` to be of `long` type, as it may exceed the storage limit for `int` when reversing `x`.
- ## Solution 2: Reverse Half of the Number
	-
	  ```c++
	  class Solution {
	  public:
	    bool isPalindrome(int x) {
	      if (x < 0 || (x % 10 == 0 && x != 0)) {
	        return false;
	      }
	      int num = x;
	      int ans = 0;
	      while (x > ans) {
	        ans = ans * 10 + x % 10;
	        x /= 10;
	      }
	      return x == ans || x == ans / 10;
	    }
	  };
	  ```
	- The code above only reverses `x` up until when the reversed number `ans` is greater than or equal to `x`. When the loop terminates, either that `x` and `ans` have the same number of digits (in which case we compare them directly) or that `ans` have one more digit than `x` (in which case we compare `x` with `ans / 10`).