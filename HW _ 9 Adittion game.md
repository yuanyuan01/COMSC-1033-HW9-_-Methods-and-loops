# COMSC-1033-HW9-_-Methods-and-loops
## Intriduction
```
We are going to rework the addition game using methods and for loops.
```
## Outline
```
```
## References and Literature
```
```
## Code
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
					 int roundCount = 2;
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
Everything completed.

```
## Command prompt
```
```
## Summary
```
```
