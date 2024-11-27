import java.util.Scanner;

public class Main{

    public static String decode(String input) {
        StringBuilder decodedString = new StringBuilder();
        
        for (int i = 0; i < input.length(); i += 2) {
            int count = Character.getNumericValue(input.charAt(i));
            char character = input.charAt(i + 1);
            
            for (int j = 0; j < count; j++) {
                decodedString.append(character);
                decodedString.append("cdd");  // Append "cdd" after each character
            }
        }
        
        return decodedString.toString();
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.next();
        scanner.close();
        
        String decodedString = decode(input);
        System.out.println(decodedString);
    }
}
