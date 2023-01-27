# **How to log into your ieng6 account**
---

**1. Download Visual Studio Code:**
* First, download VSCode from the website here: https://code.visualstudio.com/download
* Be sure to download the version for your operating system (There are downloads for Mac, Windows, and Linux)
* If on a 32 bit machine avoid the 64 bit download option
* Once it has been installed, open the application.
* It should look similar to this screen, depending on your system:
![image](https://user-images.githubusercontent.com/122496390/211969910-419f35b2-4026-4a6b-b74a-b8cbbef23163.png)

**2. Reset your password:**

![image](https://user-images.githubusercontent.com/122496390/211969278-3ade5870-a76b-4492-9a27-c3e9f702682f.png)
* First sign into your course-specific account here: https://sdacs.ucsd.edu/~icc/index.php
* Make sure to click the button with your UCSD username. (This will appear once you sign in)
* Click reset password
* Enter your old password and new password, and avoid clicking "Check Password"
* Click enter while in the last text box

**3. Log into the command line:**

![image](https://user-images.githubusercontent.com/122496390/211970875-b9840a88-8d98-43c7-bafa-1ceee100d66e.png)
* Open the terminal by clicking the terminal drop down in the menu
* Type ```ssh cs15lwi23***@ieng6.ucsd.edu``` following the dollar sign $.
* When prompted, enter your new password.
* Note: You will not be able to see what you are typing when entering password.
* Make *very* sure you enter the ieng6 email with your 3 letters. I previously was using the example email instead of my own, making me unable to login.

**4. Entering Commands**

![image](https://user-images.githubusercontent.com/122496390/211973733-5dba87f7-3c9f-4b4e-86a9-9b182b2e53e2.png)
* Some commands to try: `ls` + the path tells you the directory a file or folder is located in.
* `pwd` prints the working directory
* `cd` + path makes the command line look for the path within the folder you are already in. (Note: this means that if you are in a folder of the same name, it will still renavigate to the subfolder.
