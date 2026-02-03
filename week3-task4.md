class Solution {
    public boolean containsDuplicate(int[] nums) {
        HashSet<Integer> set = new HashSet<>();
        
        for (int i = 0; i < nums.length; i++) {
            if (set.contains(nums[i])) {
                return true;
            }
            set.add(nums[i]);
        }
        
        return false;
    }
}
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/72d1057d-de14-4749-8615-2711e3eaa15d" />
