  /** Programmer: Craig Wiencek
  * classID: cwienc5421
  * Lecture02: Welcome to Java
  * CIS 2600: Business Application Programming
  * Fall 2016
  * Due date: 09/22/16
  * Date completed: 09/22/16
  **************************************
  * Program Explanation: This program utilizes command line to allow the user to input their name and two integers to see 5 basic math functions used in programming. My code makes this possible by using the scanner class to allow keyboard input by users.
*/


package ex2cwienc5421;
 
import java.util.Scanner;

public class EX2cwienc5421 {


    public static void main(String[] args)
    {
        System.out.println("================================");
         /**
          * here I  specifiy that the word "name" is to be displayed as a
          * text string.
          */      
        String name;
        
    /**
     * Here is where I declared all of my integers and named seven variables.
     * I used "int" because integer can hold quite large values and are good 
     * to use for arithmetics. I named the integers/variables the user will enter
     * numberOne and numberTwo. I created short hand names for the different
     * mathematical operations and declared those as integers as well. I declared
     * div (which represents divide) a double so that it will show decimal places 
     * for non-whole solutions.
     */
        int numberOne = 0;
        int numberTwo = 0;
        int sum = 0;
        int diff = 0;
        int multi = 0;
        double div = (double)0;
        int mod = 0;

      /**
        * Here is where the dialog is scanned and read to the user for their inputs. 
        * "Scanner inputDevice" creates a new scanner to take values inputted by the
        * user and "new Scanner(System.in)" specifies that there will be inputs entered
        * into the system. For each line of text that will be read by the user I used
        * System.out.print(). "System.out" is the instance telling NetBeans to output
        * and "print" is specifying how it ought to be displayed. And of course in side 
        * the () i used " " so that the text is displayed exactly how i entered it.
        * 
       */       
    Scanner inputDevice = new Scanner(System.in);    
    System.out.print("Please enter your name >> ");
        /**
         * Earlier i declared "name" as a string and here at "inputDevice.nextLine()
         * it enables the user to enter their name which will be displayed in the
         * command line.
         */
        name = inputDevice.nextLine();
        /**
         * Line 85 to line 88 operate the same as in the above code, the only 
         * difference is name is replaced by "numberOne" and "numberTwo" which
         * were declared earlier as integers.
         */
        System.out.print("Please enter an integer >> ");
        numberOne = inputDevice.nextInt();
        System.out.print("Please enter another integer >> ");
        numberTwo = inputDevice.nextInt();
        
        System.out.println("================================");
                
        /**
         * Here is where I specify how each declared integers that represent
         * a mathematical function will operate. I was able to make this simple
         * since earlier I declared that "numberOne" and "numberTwo" are what
         * ever integers the user enters and placing the appropriate mathematical
         * function between "numberOne" and "numberTwo" for their respective
         * desired operation.
         */
        sum = numberOne + numberTwo;
        diff = numberOne - numberTwo;
        multi = numberOne * numberTwo;
        div = numberOne / (double)numberTwo;
        mod = numberOne % numberTwo;
             
        /**
         * This will be the output displayed to the user using System.out.printLn().
         * Executed by fairly simple concatenations, inserting declared variables
         * and inputing text between quotation marks, i was able to pull the users
         * name and the 2 integers they entered as well as the results of the 
         * math operations to be displayed in a command line for the user to read.
         * 
         */    
        System.out.println("Hey " + name + " here are your answers:");
        System.out.println(numberOne + " + " + numberTwo + " is " + sum);
        System.out.println(numberOne + " - " + numberTwo + " is " + diff);
        System.out.println(numberOne + " * " + numberTwo + " is " + multi);
        System.out.println(numberOne + " / " + numberTwo + " is " + div);
        System.out.println(numberOne + " % " + numberTwo + " is " + mod);

        
    }
    
}
