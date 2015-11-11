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
import java.util.Scanner;
public class HomeWoke_9 {
	public static void main(String[] args) {

        System.out.println("Hello Dr.Evert.");

        //Call the addition game method.
        AdditonGameMethod();
    }
    public static void AdditonGameMethod() {
        System.out.println("Inside the addition game method.");

        int hardness = 5;
        int hardnessStep = 2;
        int score = 0;

        // Set up my for loop to go through the number of rounds
        int numberOfRounds = 4;
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
Hello Dr.Evert.
Inside the addition game method.
Inside the for loop. Round: 1
Inside get and check student answer method.
Add 0 and 0.
0
Good work, your answer was correct.
Your score was 0 and is now 5.
Your hardness was 5 and is now 10.
Inside the for loop. Round: 2
Inside get and check student answer method.
Add 6 and 6.
12
Good work, your answer was correct.
Your score was 5 and is now 15.
Your hardness was 10 and is now 20.
Inside the for loop. Round: 3
Inside get and check student answer method.
Add 13 and 7.
20
Good work, your answer was correct.
Your score was 15 and is now 35.
Your hardness was 20 and is now 40.
Inside the for loop. Round: 4
Inside get and check student answer method.
Add 26 and 3.
29
Good work, your answer was correct.
Your score was 35 and is now 75.
The game is complete.
Your final score was 75

```

## Command prompt
```
$1 Start a local ewpository
1. Navigate to the foler we just created.
--use dir to see what is on the directory.
2. Set up my local repository.
--use git init to start a local repository.
--use git add . to add all my files.


Microsoft Windows [Version 6.1.7601]
Copyright (c) 2009 Microsoft Corporation.  All rights reserved.

C:\Users\User>E:
E:\>dir
 Volume in drive E is YUANYUAN
 Volume Serial Number is 8A4A-E951

 Directory of E:\

11/05/2015  03:06 PM         1,226,240 hhhahhahahhhahhhhaha ??.doc
04/23/2015  08:51 PM    <DIR>          ???
04/23/2015  08:52 PM    <DIR>          ??????
11/04/2015  11:34 AM            92,218 unforgetabble expeience.docx
11/10/2015  06:54 PM            18,944 You Zeng Field Experience Packet.doc
05/18/2015  09:30 AM    <DIR>          ?????
05/18/2015  09:32 AM    <DIR>          ??????
05/18/2015  09:33 AM    <DIR>          ? ? ?
05/20/2015  10:10 AM    <DIR>          English
05/27/2015  03:55 PM    <DIR>          Skypee
07/21/2015  07:30 PM    <DIR>          ????
08/30/2015  06:11 PM    <DIR>          ????
08/30/2015  06:12 PM    <DIR>          SWOSU
10/02/2015  10:17 AM    <DIR>          Camon Workspace
10/08/2015  03:03 PM    <DIR>          Users
11/01/2015  05:47 PM    <DIR>          New folder
               3 File(s)      1,337,402 bytes
              13 Dir(s)  10,100,121,600 bytes free


E:\>cd SWOSU

E:\SWOSU>dir
 Volume in drive E is YUANYUAN
 Volume Serial Number is 8A4A-E951

 Directory of E:\SWOSU

08/30/2015  06:12 PM    <DIR>          .
08/30/2015  06:12 PM    <DIR>          ..
10/12/2015  08:30 AM           417,625 English????--??????_????.htm
08/31/2015  08:13 AM    <DIR>          CS1_Workspace
09/01/2015  09:58 AM    <DIR>          eclipse-java-mars-R-win32
09/18/2015  09:42 AM    <DIR>          Operating Systems Class
09/21/2015  05:28 PM    <DIR>          Computer Science I
09/08/2015  03:33 PM    <DIR>          Fund of English
10/12/2015  08:30 AM    <DIR>          English????--??????_????_files
               1 File(s)        417,625 bytes
               8 Dir(s)  10,099,064,832 bytes free

E:\SWOSU>cd Computer Science I

E:\SWOSU\Computer Science I>dir
 Volume in drive E is YUANYUAN
 Volume Serial Number is 8A4A-E951

 Directory of E:\SWOSU\Computer Science I

09/21/2015  05:28 PM    <DIR>          .
09/21/2015  05:28 PM    <DIR>          ..
10/19/2015  10:18 AM    <DIR>          .metadata
11/09/2015  07:05 PM    <DIR>          Listing 4.16
11/09/2015  07:05 PM    <DIR>          rhftghn
09/14/2015  05:02 PM            18,846 HW _ 2.docx
09/15/2015  12:04 PM            45,568 HW _3.doc
09/14/2015  05:44 PM            11,776 HW3.doc
08/31/2015  08:26 AM       189,603,416 jdk-8u60-windows-i586.exe
08/31/2015  08:27 AM       171,043,550 eclipse-java-mars-R-win32.zip
10/19/2015  10:10 PM            56,320 Pre_Exam.HW _ 7.doc
10/26/2015  10:51 AM            19,840 1412_Fun_With_Functions_Project.docx
11/02/2015  03:04 PM    <DIR>          .recommenders
11/09/2015  06:21 PM    <DIR>          HomeWork _9
11/09/2015  07:05 PM    <DIR>          Listing_4_16 project
11/09/2015  07:13 PM    <DIR>          GitHub_files
11/09/2015  07:13 PM            38,802 GitHub.htm
11/10/2015  10:29 AM    <DIR>          Test
09/22/2015  01:08 PM            18,613 HW_4.1.docx
09/22/2015  01:11 PM            21,498 HW_4.2.docx
09/19/2015  11:53 AM         2,331,164 This work is licensed under the Creative
Commons A.doc
11/09/2015  10:52 AM            12,651 public class strings111232435465.docx
09/30/2015  03:43 PM            18,517 HW_5.docx
10/08/2015  02:52 PM    <DIR>          eclipse-java-mars-R-win32
10/09/2015  02:07 PM    <DIR>          AdditionGame1214_Project
10/13/2015  11:14 AM            12,706 GIT.docx
10/13/2015  03:18 PM            56,832 AdditionGameHW_6.doc
              15 File(s)    363,310,099 bytes
              12 Dir(s)  10,096,107,520 bytes free

E:\SWOSU\Computer Science I>cd "HomeWork _9"

E:\SWOSU\Computer Science I\HomeWork _9>git init
Reinitialized existing Git repository in E:/SWOSU/Computer Science I/HomeWork _9
/.git/

E:\SWOSU\Computer Science I\HomeWork _9>git add .

$2 Connect our local respository to our global repository
--1. Open a brower of choice
--2. Go to Github and sign in: https://github.com/login
--3. Add a new repositoryby clicking the green button .
--4. Follow the introductions to …or create a new repository on the command line

echo # Hello-Candy >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:yuanyuan01/Hello-Candy.git
git push -u origin master

…or push an existing repository from the command line

git remote add origin git@github.com:yuanyuan01/Hello-Candy.git
git push -u origin master

…or import code from another repository

You can initialize this repository with code from a Subversion, Mercurial, or TFS project.

```
## Summary
```
A for loop generally uses a variable to control how many times
the loop body is executed and when the loop generally terminates. 
This variable is referred to as a control variable.
```
