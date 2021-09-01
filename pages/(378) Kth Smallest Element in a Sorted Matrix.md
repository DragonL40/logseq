- #Leetcode
- Given an `n x n` `matrix` where each of the rows and columns are sorted in ascending order, return the `k`th smallest element in the matrix. 
  
  Note that it is the `k`th smallest element in the sorted order, not the `k`th distinct element.
## Solution 1: [[Binary Search]] on `matrix`
	-
	  ```c++
	  #include <iostream>
	  #include <vector>
	  
	  using namespace std;
	  
	  class Solution {
	  public:
	      int kthSmallest(vector<vector<int>>& matrix, int k) {
	          int n = matrix.size();
	  
	          int left = matrix[0][0], right = matrix[n - 1][n - 1], mid;
	          while (left <= right) {
	              mid = left + (right - left) / 2;
	              int count = 0;
	  
	              for (size_t i = 0; i < n; i++) {
	                  // upper_bound(first, last, val) returns an iterator pointing to the first element in the range [first,
	                  // last) which compares greater than val.
	                  count += upper_bound(matrix[i].begin(), matrix[i].end(), mid) - matrix[i].begin();
	              }
	  
	              if (count < k) {
	                  left = mid + 1;
	              } else {
	                  right = mid - 1;
	              }
	          }
	  
	          return left;
	      }
	  };
	  ```