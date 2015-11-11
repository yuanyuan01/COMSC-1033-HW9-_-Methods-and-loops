# COMSC-1033-HW9-_-Methods-and-loops
```
We are going to rework the addition game using methods and for loops.
```
## code
```
import java.util.Scanner;
public class HomeWork_9 {

    public static void main(String[] args) {
        // Call the addition game method.
                //call the method to test is AnswerCorrectMethod
                additionGameMethod();

                System.out.println("Everything completed.");
            }
                public static void additionGameMethod(){
                    System.out.println("Inside the addition game method.");
                    int hardness = 5;
                    int score = 0;
                     int roundCount = 4;
                     boolean isAnswerCorrect;
                     for(int counter = 0; counter < roundCount; counter = counter + 1){
                         System.out.println("Inside for loop: " + counter );
                         isAnswerCorrect = isAnswerCorrectMethod(hardness);

                     }
                     return;
                }
                public static boolean isAnswerCorrectMethod(int hardness){
                    System.out.println("Inside check answer method");
                    System.out.println("The variable hardness is :" + hardness);
                    return false;


    }

}
```
