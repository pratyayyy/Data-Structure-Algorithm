class Solution {
    public int[] maxSlidingWindow(int[] nums, int k) {
        int[] res = new int[nums.length - k + 1];
        int j=0;
        ArrayDeque<Integer> deq = new ArrayDeque<Integer>();
        for(int i=0;i<nums.length;i++)
        {
            while(!deq.isEmpty() && nums[deq.getLast()] < nums[i]){
                deq.removeLast();
            }

            deq.addLast(i);

            if(deq.getFirst() + k == i){
                deq.removeFirst();
            }
            if(i >= k-1){
                res[j] = nums[deq.getFirst()];
                j++;
            }
        }
        return res;
    }
}
