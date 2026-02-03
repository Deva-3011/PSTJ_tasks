class Solution {
    public boolean halvesAreAlike(String s) {
        int n=s.length();
        int mid=n/2;
        int count=0;
        Set<Character> set= new HashSet<>(Arrays.asList('A','E','I','O','U','a','e','i','o','u'));
        for(int i=0;i<mid;i++){
            if(set.contains(s.charAt(i)))
                count++;
        }
        for(int i=mid;i<n;i++){
            if(set.contains(s.charAt(i)))
                count--;
        }
        return count==0;
    }
}
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/e47f9d7a-8d80-4577-b5bd-b86d1a330791" />
