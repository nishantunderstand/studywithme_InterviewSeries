You are given an integer array arr.
A subarray(length>=2) is considered valid if is. Strictly increasing or Strictly decreasing. Count and return the total number of such subarrays.

class Main {
    public static void main(String[] args) {
        int[] nums2 = {1,2,3};
        int[] nums1 = {1,3,2};
        int[] nums = {1,3,2,4};
        int count = 0;
        boolean flag = false;
        for(int i=0;i<nums.length-1;i++){
            if(isIncreasing(nums,i,i+1)){
                count++;
                flag = true;
            }else if(!isIncreasing(nums,i,i+1)){
                count++;
                flag = false;
            }
        }
        if(flag){
            count++;
        }
        System.out.println(count);
        
    }
    static boolean isIncreasing(int[] nums,int i,int j){
        return nums[i]<nums[j];
    }
}