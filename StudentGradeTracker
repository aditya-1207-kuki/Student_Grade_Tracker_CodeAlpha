import java.util.*;

public class StudentGradeTracker {
    static class Student {
        String name;
        int score;

        Student(String name, int score) {
            this.name = name;
            this.score = score;
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ArrayList<Student> students = new ArrayList<>();

        System.out.print("Enter number of students: ");
        int n = sc.nextInt();
        sc.nextLine(); 

        for (int i = 0; i < n; i++) {
            System.out.print("Enter student name: ");
            String name = sc.nextLine();
            System.out.print("Enter " + name + "'s score: ");
            int score = sc.nextInt();
            sc.nextLine(); 

            students.add(new Student(name, score));
        }

        int total = 0;
        int highest = Integer.MIN_VALUE;
        int lowest = Integer.MAX_VALUE;
        String topStudent = "", bottomStudent = "";

        for (Student s : students) {
            total += s.score;
            if (s.score > highest) {
                highest = s.score;
                topStudent = s.name;
            }
            if (s.score < lowest) {
                lowest = s.score;
                bottomStudent = s.name;
            }
        }

        double average = (double) total / n;

        System.out.println("\n--- Student Grades Summary ---");
        for (Student s : students) {
            System.out.println(s.name + ": " + s.score);
        }
        System.out.println("------------------------------");
        System.out.println("Average Score: " + average);
        System.out.println("Highest Score: " + highest + " (by " + topStudent + ")");
        System.out.println("Lowest Score: " + lowest + " (by " + bottomStudent + ")");
    }
}
