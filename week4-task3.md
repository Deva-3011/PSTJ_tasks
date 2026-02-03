import java.util.*;

public class Solution {

    // Function to compare Alice's and Bob's ratings
    public static List<Integer> compareTriplets(List<Integer> a, List<Integer> b) {
        int aliceScore = 0;
        int bobScore = 0;

        // Loop through the ratings and compare each one
        for (int i = 0; i < 3; i++) {
            if (a.get(i) > b.get(i)) {
                aliceScore++;
            } else if (a.get(i) < b.get(i)) {
                bobScore++;
            }
        }

        // Create a list to store the scores of Alice and Bob
        List<Integer> result = new ArrayList<>();
        result.add(aliceScore);
        result.add(bobScore);
        
        return result;
    }

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        
        // Reading Alice's ratings
        List<Integer> a = new ArrayList<>();
        for (int i = 0; i < 3; i++) {
            a.add(scan.nextInt());
        }
        
        // Reading Bob's ratings
        List<Integer> b = new ArrayList<>();
        for (int i = 0; i < 3; i++) {
            b.add(scan.nextInt());
        }
        
        // Get the comparison points
        List<Integer> result = compareTriplets(a, b);
        
        // Output the result
        for (int i : result) {
            System.out.print(i + " ");
        }
    }
}
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/0801b56a-29d9-46b1-976f-468e16df60bb" />
