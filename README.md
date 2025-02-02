# Leetcode---1752
Check if Array Is Sorted and Rotated
//code in java
public class Solution {
    public boolean check(int[] nums) {
        int count = 0;
        int n = nums.length;
        
        for (int i = 0; i < n; i++) {
            if (nums[i] > nums[(i + 1) % n]) {
                count++;
            }
        }
        
        return count <= 1;
    }

    public static void main(String[] args) {
        Solution solution = new Solution();
        int[] nums1 = {3, 4, 5, 1, 2};
        int[] nums2 = {2, 1, 3, 4};
        int[] nums3 = {1, 2, 3, 4, 5};
        System.out.println(solution.check(nums1)); // Output: true
        System.out.println(solution.check(nums2)); // Output: false
        System.out.println(solution.check(nums3)); // Output: true
    }
}
