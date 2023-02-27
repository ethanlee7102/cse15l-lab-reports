# **Instructions for Challenge Tasks**  
## **Step 4. Log into ieng6**  
![Image]()  
To log into ieng6 I first typed `ssh cs15lwi23abt@ieng6.ucsd.edu` and then I pressed `<enter>`. This logs me into the ieng6 server and I get a message of when I was last logged in.  
## **Step 5. Clone your fork of the repository from your Github account**  
![Image]()  
Next I type `git clone git@github.com:ethanlee7102/lab7.git` then press `<enter>` in order to clone the fork of the lab7 repository. By doing this I am able to access a copy of the file within the ieng6 server.  
## **Step 6. Run the tests, demonstrating that they fail**  
![Image]()  
I first type `cd lab7` then press `<enter>` to enter the lab7 file. Then I type `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` and press `<enter>`, and this compiles the testers for TestListExamples.java. I then type `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` and press `<enter>`, and this runs the tester. We see that this results in a message saying that there was 1 failure from the `testMerge2(ListExamplesTests)` test.  
## **Step 7. Edit the code file to fix the failing test**  
![Image]()  
I enter the command `nano ListExamples` and scoll down to line 43. I then press `<side>` 12 times and `<delete>` and enter `<2>`. This changes the code `index1 += 1` to `index2 += 2`. This fixes the bug of the code running forever and being forced to terminate at 500 ms. Next I press `<^O>` and `<enter>` to save the code and `<^X>` and `<enter>` to exit.  
## **Step 8. Run the tests, demonstrating that they now succeed**  
![Image]()  
I then run the tests by compiling again using `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` pressing `<enter>` and `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` pressing `<enter>`. This time it says `OK (2 Tests)` meaning the tests pass.  
## **Step 8. Commit and push the resulting change to your Github account**  
![Image]()  
Lastly I type `git add ListExamples.java` and press `<enter>`, `git commit -m ListExamples.java` and press `<enter>`, and `git push origin main` and press `<enter>`. This commits the file changes and pushes them to my Github account.




