


import java.util.ArrayList;
import java.util.Scanner;
import java.util.Collections;

public class GradeAnalyzer {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        ArrayList<Integer> grades = new ArrayList<>();
        
        System.out.println("Grade Analyzer");
        System.out.println("Enter students' grades (enter -1 to finish):");
        
        int grade;
        while (true) {
            System.out.print("Enter a grade: ");
            grade = scanner.nextInt();
            
            if (grade == -1) {
                break;
            }
            
            grades.add(grade);
        }
        
        if (grades.isEmpty()) {
            System.out.println("No grades entered.");
            return;
        }
        
        // Calculate average
        double sum = 0;
        for (int g : grades) {
            sum += g;
        }
        double average = sum / grades.size();
        
        // Find highest and lowest grades
        int highest = Collections.max(grades);
        int lowest = Collections.min(grades);
        
        System.out.println("Average Grade: " + average);
        System.out.println("Highest Grade: " + highest);
        System.out.println("Lowest Grade: " + lowest);
    }
}

