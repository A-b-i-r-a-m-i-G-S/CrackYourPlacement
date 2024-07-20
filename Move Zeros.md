Given an integer array nums, move all 0's to the end of it while maintaining the relative order of the non-zero elements.

Note that you must do this in-place without making a copy of the array.

```
class Solution {
    public void moveZeroes(int[] nums) {
        int n = nums.length;
        int i = 0;
        for(int j=0;j<n;j++){
            if(nums[j] != 0){
                nums[i] = nums[j];
                i++;
            }
        }

        while(i<n){
            nums[i++] = 0;
        }
    }
}
```
