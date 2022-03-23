/*
Given a list of numbers and a number k, return whether any two numbers from the list add up to k.

For example, given [10, 15, 3, 7] and k of 17, return true since 10 + 7 is 17.
*/

/*
Brute Force Solution
We will run two loops one from the beginning element and one from its succeeding element. It checks each and every pair and then returns the sum whenever it sees it.
Time Complexity: O(n^2)
Reference Code: Two Sum from LeetCode
*/
for(int i=0;i<nums.size();i++)
        {
            for(int j=i+1;j<nums.size();j++)
            {
                if(nums[i]+nums[j]==target)
                {
                    twoSum.push_back(i);
                    twoSum.push_back(j);
                    flag=1;
                    break;
                }
            }
            if(flag==1)
                break;
        }
        return twoSum;
 
 /*
 Optimized Solution
 We can solve in linear time using Hashmap. We store the indices of the elements already visited. 
 Steps to be followed:
 1. Create a Hashmap that accepts integer values for key and value.
 2. Iterate through each element in the given array starting from the first element.
 3. In each iteration check if required number (required  number = target sum - current number) is present in the given array.
 4. If present, return {required number index, current number index} as  result.
 5. Otherwise add the current iteration number as key and its index as value to the hashmap. Repeat this  until you find the result.
 
 Time Complexity: O(n)
 
 */
 
#include<bits/stdc++.h>
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        vector<int>v;
        unordered_map<int,int>m;
        for(int i=0;i<nums.size();i++)
        {
            int reqnum=target-nums[i];
            if(m.find(reqnum)!=m.end()){
                auto it = m.find(reqnum); 
                v.push_back(it->second);
                v.push_back(i);
            return v;}
            m.insert({nums[i],i});
        }
        return v;
    }
};
