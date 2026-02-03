import java.util.*;

// Student class
class Student {
    private int id;
    private String fname;
    private double cgpa;

    public Student(int id, String fname, double cgpa) {
        this.id = id;
        this.fname = fname;
        this.cgpa = cgpa;
    }

    public int getId() {
        return id;
    }

    public String getFname() {
        return fname;
    }

    public double getCgpa() {
        return cgpa;
    }
}

// Comparator class
class StudentComparator implements Comparator<Student> {

    @Override
    public int compare(Student a, Student b) {
        // 1. Sort by CGPA (descending)
        if (Double.compare(b.getCgpa(), a.getCgpa()) != 0) {
            return Double.compare(b.getCgpa(), a.getCgpa());
        }
        // 2. Sort by First Name (ascending)
        if (!a.getFname().equals(b.getFname())) {
            return a.getFname().compareTo(b.getFname());
        }
        // 3. Sort by ID (ascending)
        return a.getId() - b.getId();
    }
}

// Main class
public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        List<Student> students = new ArrayList<>();

        for (int i = 0; i < n; i++) {
            int id = sc.nextInt();
            String fname = sc.next();
            double cgpa = sc.nextDouble();
            students.add(new Student(id, fname, cgpa));
        }

        Collections.sort(students, new StudentComparator());

        for (Student s : students) {
            System.out.println(s.getFname());
        }
    }
}
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/d911cb7f-7e95-4596-8b3c-26e74534d69c" />
