# COMSC-1033-HW9-_-Methods-and-loops

```
We are going to rework the addition game using methods and for loops.
```
## Intriduction

```
$ A for loop has a concise syntax for writing loops
$ The for loop statement starts with the keyword for,
  followed by a pair of parentheses enclosing the control structure of the loop.
$ This stucture consists of inittial-action, 
  loop- continuation-condition, and action- after - each - iteration.
$ The inittial-action often initializes a control variable;
$ The loop- continuation-condition usually increments or decrements the control variable;
$ The action- after - each - iteration test whether the control variable has termination value.


```

## Project Outline
```
Main() 
int hardness = 10;
int score = 0;
int roundCount=4;

    for(int counter = 0; counter < roundCount; counter++)
    {
    //Do something
    }
    print the results
```

## References and Literature
```
*  liang,Y. Daniel. *Introduction to JAVA Programming: 
Comprehensive Version. * 10th edition : Pearson, 2014.print.
reference pages : * P170--P174.
```

## Java Code
```
import java.util.Scanner;

public class ComputAreaWithConso1eInput {
    public static void main(String[] args) {

            System.out.println("Hello class.");

            //Call the addition game method.
            AdditonGameMethod();
        }
        public static void AdditonGameMethod() {
            System.out.println("Inside the addition game method.");

            int hardness = 5;
            int hardnessStep = 2;
            int score = 0;

            // Set up my for loop to go through the number of rounds
            int numberOfRounds = 3;
            for(int roundNumber = 1; 
            roundNumber <= numberOfRounds;  
            roundNumber = roundNumber + 1){
                System.out.println("Inside the for loop. Round: " + roundNumber);
                boolean isAnswerCorrect = getAndCheckStudentAnswer(hardness);
                if(isAnswerCorrect){
                    System.out.print("Your score was " + score + " and is now ");
                    score = score + hardness;
                    System.out.println(score + ".");

                    if(roundNumber<numberOfRounds){
                        System.out.print("Your hardness was " + hardness + " and is now ");
                        hardness = hardness * hardnessStep;
                        System.out.println(hardness + ".");
                    }
                }else{
                    if(roundNumber<numberOfRounds){
                        System.out.print("Your hardness was " + hardness + " and is now ");
                        if(hardness>5){
                            hardness = hardness / hardnessStep;

                        }
                        System.out.println(hardness + ".");

                    }

                }
            }
            System.out.println("The game is complete.");
            System.out.println("Your final score was " + score );
        }

        public static boolean getAndCheckStudentAnswer(int hardness) {
            System.out.println("Inside get and check student answer method.");
            int number1 = (int)(Math.random()*hardness);
            int number2 = (int)(Math.random()*hardness);
            System.out.println("Add " + number1 + " and " + number2 +".");
            //Scanner input = new Scanner(System.in);
            //int studentAnswer = input.nextInt();
            Scanner get = new Scanner(System.in);
            int studentAnswer = get.nextInt();
            if(studentAnswer == (number1 + number2)){
                System.out.println("Good work, your answer was correct.");
                return true;
            }else{
                System.out.println("Nice try, but the correct answer was " + (number1 + number2));
                return false;
            }
        }
    }

```

## Console output
```
Hello class.
Inside the addition game method.
Inside the for loop. Round: 1
Inside get and check student answer method.
Add 0 and 4.
4
Good work, your answer was correct.
Your score was 0 and is now 5.
Your hardness was 5 and is now 10.
Inside the for loop. Round: 2
Inside get and check student answer method.
Add 2 and 6.
8
Good work, your answer was correct.
Your score was 5 and is now 15.
Your hardness was 10 and is now 20.
Inside the for loop. Round: 3
Inside get and check student answer method.
Add 12 and 7.
19
Good work, your answer was correct.
Your score was 15 and is now 35.
The game is complete.
Your final score was 35


```

## Command prompt
```
```

## Summary
```
A for loop generally uses a variable to control how many times
the loop body is executed and when the loop generally terminates. 
This variable is referred to as a control variable.
```
