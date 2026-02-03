import java.util.*;

// Player class (given in the problem, included here for completeness)
class Player {
    String name;
    int score;

    Player(String name, int score) {
        this.name = name;
        this.score = score;
    }
}

// Comparator class
class Checker implements Comparator<Player> {

    @Override
    public int compare(Player a, Player b) {
        // Sort by score in descending order
        if (a.score != b.score) {
            return b.score - a.score;
        }
        // If scores are equal, sort by name alphabetically
        return a.name.compareTo(b.name);
    }
}

// Main solution class (locked-style compatible)
public class Solution {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        Player[] players = new Player[n];

        for (int i = 0; i < n; i++) {
            String name = sc.next();
            int score = sc.nextInt();
            players[i] = new Player(name, score);
        }

        Arrays.sort(players, new Checker());

        for (Player p : players) {
            System.out.println(p.name + " " + p.score);
        }
    }
}

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/43ed3364-c346-4c37-b94d-0e5799eb315e" />
