class Solution {
    public int minSwaps(int[] nums) {
        int n = nums.length;

        int countOnes = Arrays.stream(nums).sum();

        int i = 0;
        int j = 0;
        int currCount = 0;
        int maxCount = 0;

        while (j < 2 * n) {
            if (nums[j % n] == 1) {
                currCount++;
            }

            if (j - i + 1 > countOnes) {
                currCount -= nums[i % n];
                i++;
            }

            maxCount = Math.max(maxCount, currCount);
            j++;
        }

        return countOnes - maxCount;
    }
}
