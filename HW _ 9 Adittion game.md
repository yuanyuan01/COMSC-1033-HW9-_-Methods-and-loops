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

## Console output
```
Inside the addition game method.
Inside for loop: 0
Inside check answer method
The variable hardness is :5
Inside for loop: 1
Inside check answer method
The variable hardness is :5
Inside for loop: 2
Inside check answer method
The variable hardness is :5
Inside for loop: 3
Inside check answer method
The variable hardness is :5
Everything completed.


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
