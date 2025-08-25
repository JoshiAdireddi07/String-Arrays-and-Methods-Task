# String-Arrays-and-Methods-Task
Creating a program that manages a list of student names using string arrays and methods.

    public class StringArrays {

    // 1. Find longest name
    public static String findLongestName(String[] names) {
        String longest = names[0];
        for (String name : names) {
            if (name.length() > longest.length()) {
                longest = name;
            }
        }
        return longest;
    }

    // 2. Count names starting with a given letter
    public static int countNamesStartingWith(String[] names, char letter) {
        int count = 0;
        letter = Character.toLowerCase(letter);
        for (String name : names) {
            if (Character.toLowerCase(name.charAt(0)) == letter) {
                count++;
            }
        }
        return count;
    }

    // 3. Format names as "Last, First"
    public static String[] formatNames(String[] names) {
        String[] formatted = new String[names.length];
        for (int i = 0; i < names.length; i++) {
            String[] parts = names[i].split(" ");
            if (parts.length >= 2) {
                formatted[i] = parts[1] + ", " + parts[0];
            } else {
                formatted[i] = names[i]; // fallback if no last name
            }
        }
        return formatted;
    }

    public static void main(String[] args) {
        String[] students = {
            "John Smith", 
            "Alice Johnson", 
            "Bob Brown", 
            "Carol Davis", 
            "David Wilson"
        };

        System.out.println("Longest Name: " + findLongestName(students));
        System.out.p

