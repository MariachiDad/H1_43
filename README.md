# H1_43
Homework 4.3

package H1_43;

/**
 * This program prompts users for a Java source code file name, reads the source
 * code file and outputs the contents to a new file named the same as the input
 * file, but with a .txt file name extension. The output file is formatted with
 * reference code line numbers using the Java API PrintWriter.printf() and the
 * format specifier of %03d.
 *
 * @authors chris d'amore and andrew hoertt
 *
 */
//import java.util.ArrayList;
//import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.File;
import java.io.FileWriter;
import java.io.PrintWriter;
import java.util.Scanner;

public class H1_43 {

    /**
     * @param args the command line arguments
     */
    public static int main(String[] args) throws IOException {

        File fileInput = new File("C:\\Users\\chris\\Desktop\\ASU\\2020\\Fall 2020\\77038 CSE 205 Object-Oriented Program & Data\\_Homework\\HW1\\H1_43\\src\\H1_43\\h1_43_test.java");
        Scanner scan = new Scanner(fileInput);

        int count = 0;

        String fileText = "";
        String printText = "";

        while (scan.hasNextLine() && count >= 0) {
            count++;
            fileText = fileText.concat(scan.nextLine() + "\n");
            printText = fileText;
        }

        FileWriter writeText = new FileWriter("C:\\Users\\chris\\Desktop\\ASU\\2020\\Fall 2020\\77038 CSE 205 Object-Oriented Program & Data\\_Homework\\HW1\\H1_43\\src\\H1_43\\h1_43_test.java.txt");
        FileWriter outPrint = new FileWriter("C:\\Users\\chris\\Desktop\\ASU\\2020\\Fall 2020\\77038 CSE 205 Object-Oriented Program & Data\\_Homework\\HW1\\H1_43\\src\\H1_43\\h1_43_test2.java.txt");
        PrintWriter rePrint = new PrintWriter("C:\\Users\\chris\\Desktop\\ASU\\2020\\Fall 2020\\77038 CSE 205 Object-Oriented Program & Data\\_Homework\\HW1\\H1_43\\src\\H1_43\\h1_43_test2.java.txt");
        rePrint.printf("%003d" + count + rePrint);
        writeText.close();
        outPrint.close();
        return 0;

        /**
         * System.out.printf("%03d" + count + fileText); PrintWriter writeText =
         * new PrintWriter("C:\\Users\\chris\\Desktop\\ASU\\2020\\Fall
         * 2020\\77038 CSE 205 Object-Oriented Program &
         * Data\\_Homework\\HW1\\H1_43\\src\\H1_43\\h1_43_test.java.txt");
         * writeText.close();
         */
    }

}
