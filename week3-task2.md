import java.util.*;
import java.lang.*;
import java.io.*;

class Codechef {
    public static void main (String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine(); // FIX 1: consume newline

        for(int i = 0; i < n; i++){
            String s = sc.nextLine();
            String res = lapindrome(s) ? "Yes" : "No";
            System.out.println(res);
        }
    }

    public static boolean lapindrome(String s){
        HashMap<Character, Integer> map = new HashMap<>();
        int n = s.length();
        int mid = n / 2;

        // first half
        for(int i = 0; i < mid; i++){
            map.put(s.charAt(i), map.getOrDefault(s.charAt(i), 0) + 1);
        }

        // FIX 2: skip middle character if odd length
        int startSecondHalf = (n % 2 == 0) ? mid : mid + 1;

        for(int i = startSecondHalf; i < n; i++){
            map.put(s.charAt(i), map.getOrDefault(s.charAt(i), 0) - 1);
        }

        for(int val : map.values()){
            if(val != 0) return false;
        }
        return true;
    }
}

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/58e85042-9da2-4e81-bec5-4daf1474cf2d" />
