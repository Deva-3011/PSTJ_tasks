import java.util.Scanner;

public class SubstringComparisons {

    public static String getSmallestAndLargest(String s, int k) {
        String smallest = s.substring(0, k);
        String largest = s.substring(0, k);

        for (int i = 1; i <= s.length() - k; i++) {
            String current = s.substring(i, i + k);

            if (current.compareTo(smallest) < 0) {
                smallest = current;
            }

            if (current.compareTo(largest) > 0) {
                largest = current;
            }
        }

        return smallest + "\n" + largest;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String s = sc.next();
        int k = sc.nextInt();

        System.out.println(getSmallestAndLargest(s, k));
    }
}
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/6a793e3d-bb93-414f-855f-361cd42294c1" />
