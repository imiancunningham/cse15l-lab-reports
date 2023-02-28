Steps to the Done Quick Lab

4).![Lab report 4 step 4 logging in](https://user-images.githubusercontent.com/122496390/221759141-ea804640-a45e-4b57-99d5-675749550695.png)
For the step 4 I typed: "cse15lwi23anm@ieng6.ucsd.edu <enter>". This immediately logged me in since I created a key excusing me from needing to use the password.

5).![Lab report 4 step 5 cloning repo](https://user-images.githubusercontent.com/122496390/221759152-044320cc-77ac-4341-83f1-cbaec2018b3d.png)
After copying the HTTPS: link off github, I inputed "git clone <repository link> <enter>". This made my ssh clone the repository.

6).![Lab report 4 step 6 tests failing](https://user-images.githubusercontent.com/122496390/221759165-db941cd3-1dfe-4f13-b911-04501ab54564.png)
Next I copied the compile and run junit tests from week 3's instructions replacing the tests being run. I inputed "javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java; java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamplesTests.java <enter>"

7).![Lab report 4 step 7 fixing with nano](https://user-images.githubusercontent.com/122496390/221759190-dd9a099d-c025-48d3-a7e5-a47da764cd11.png) Next I used nano to fix line 43 from "index1" to "index2". I inputed: "nano ListExamples.java <enter>" then " down-arrow x42" then "right-arrow x10" then "replace 1 with 2" then "^o <enter> ^x".

8).![Lab report 4 step 8 tests should work but still fail](https://user-images.githubusercontent.com/122496390/221759211-cd6294ef-125f-4c64-8164-537d3638d9ac.png) Here the code should have ran properly but still does not despite me verifying I had fixed the correct error with my peers. I again inputed: "javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java; java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamplesTests.java <enter>"

9).![Lab report 4 step 9 commit changes should work](https://user-images.githubusercontent.com/122496390/221759232-f910a9ab-6943-42ed-844b-5bd12535e5e2.png)
 I then entered "git add ListExamples.java <enter> git commit -m "Should've fixed error" <enter> followed by git push git@github.com:imiancunningham/lab7.git
