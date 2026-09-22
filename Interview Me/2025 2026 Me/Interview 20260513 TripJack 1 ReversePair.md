Reverse Pair
// Divide and Conquer
// MergeSort
// Based on Divide and Conquer 
class Main {
    public static void main(String[] args) {
        int[] nums = {1,3,2,3,1};
        int mid = nums.length-1/2;
        int count = 0;
        
        for(int i=0;i<nums.length;i++){
            merge(nums,0,mid-1);
            merge(nums,mid+1,nums.length-1)
            merge2LL(nums,0,nums.length-1);
        }
        
        int[] left = divide(nums,0,left);
        int[] right = divide(nums,left+1,right);
    }
    
    static void merge(int[] nums, int left, int right){
        
    }
    
    static void merge2LL(int[] left, int i, int[] right ,int j){
        
    }
}