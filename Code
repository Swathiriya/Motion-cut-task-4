import java.util.Scanner;
import java.util.Random;

public class TypingSpeedTest {
    private static final String[] SENTENCES = {
        "Java is a versatile programming language.",
        "Typing speed tests can improve efficiency.",
        "Practice makes a person perfect.",
        "The quick brown fox jumps over the lazy dog.",
        "Consistent effort leads to success."
    };
    
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();
        
        // Select a random sentence
        String sentence = SENTENCES[random.nextInt(SENTENCES.length)];
        System.out.println("Type the following sentence:");
        System.out.println("\"" + sentence + "\"");
        
        // Start time
        long startTime = System.currentTimeMillis();
        
        // Get user input
        String userInput = scanner.nextLine();
        
        // End time
        long endTime = System.currentTimeMillis();
        
        // Calculate typing speed
        double timeTaken = (endTime - startTime) / 1000.0; // Convert to seconds
        int wordCount = sentence.split(" ").length;
        double wpm = (wordCount / timeTaken) * 60;
        
        // Calculate accuracy
        int correctChars = 0;
        int minLength = Math.min(sentence.length(), userInput.length());
        for (int i = 0; i < minLength; i++) {
            if (sentence.charAt(i) == userInput.charAt(i)) {
                correctChars++;
            }
        }
        double accuracy = ((double) correctChars / sentence.length()) * 100;
        
        // Display results
        System.out.printf("\nTime taken: %.2f seconds\n", timeTaken);
        System.out.printf("Typing Speed: %.2f WPM\n", wpm);
        System.out.printf("Accuracy: %.2f%%\n", accuracy);
        
        // Feedback
        if (accuracy > 90) {
            System.out.println("Excellent typing skills!");
        } else if (accuracy > 75) {
            System.out.println("Good job! Keep practicing.");
        } else {
            System.out.println("You can do better! Keep practicing.");
        }
        
        scanner.close();
    }
}
