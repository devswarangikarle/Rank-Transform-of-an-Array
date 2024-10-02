# Rank-Transform-of-an-Array

Given an array of integers arr, replace each element with its rank.

Given an array of integers arr, replace each element with its rank.

The rank represents how large the element is. The rank has the following rules:
-Rank is an integer starting from 1.
-The larger the element, the larger the rank. If two elements are equal, their rank must be the same.
-Rank should be as small as possible.

Constraints:

0 <= arr.length <= 10^5
-10^9 <= arr[i] <= 10^9

class Solution:

    def arrayRankTransform(self, arr: List[int]) -> List[int]:
        value_to_rank = {}  
        sorted_unique_numbers = sorted(list(set(arr)))  
        
        for index in range(len(sorted_unique_numbers)): 
            value_to_rank[sorted_unique_numbers[index]] = index + 1
          
        for index in range(len(arr)): 
            arr[index] = value_to_rank[arr[index]]
        
        return arr  


