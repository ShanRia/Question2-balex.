import java.util.HashMap;
import java.util.Map;
import java.util.Scanner;

public class courses {
    public static void main(String[] args) {
        // Create a map to store course details
        Map<String, String[]> courseDetails = new HashMap<>();
        courseDetails.put("BSE", new String[]{"Software Engineering", "900,000"});
        courseDetails.put("BIT", new String[]{"Information Technology", "750,000"});
        courseDetails.put("BCS", new String[]{"Computer Science", "800,000"});
        courseDetails.put("BCE", new String[]{"Computer Engineering", "950,000"});

        // Create a Scanner object for input
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the CourseID: ");
        String courseID = scanner.nextLine().toUpperCase();

        // Check if the courseID exists in the map
        if (courseDetails.containsKey(courseID)) {
            String[] details = courseDetails.get(courseID);
            System.out.println("Course Name: " + details[0]);
            System.out.println("Tuition Fee: " + details[1]);
        } else {
            System.out.println("Wrong CourseID details");
        }

        // Close the scanner
        scanner.close();
    }
}

