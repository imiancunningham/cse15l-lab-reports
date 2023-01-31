# Part 1:
**Here is the code for StringServer:**
```
import java.io.IOException;
import java.net.URI;




class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    int num = 0;
    String tempMessage;
    public static String runningMessage="";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Ian's Number: %d", num);
        } else if (url.getPath().equals("/increment")) {
            num += 1;
            return String.format("Number incremented!");
        } else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
//                    runningMessage.append += String.parse(parameters[1]);
                    tempMessage = parameters[1];
                    runningMessage = runningMessage + '\n' + tempMessage;
                    return String.format("%s\n", runningMessage);
                }
            }
            return "404 Not Found!";
        }
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```
**Screenshot 1: using /add-message**
![image](https://github.com/imiancunningham/cse15l-lab-reports/blob/main/Lab%203%20part%201%20string%20server%20part%201.png)
* The methods called when running this code include: handleRequest(), handle(), and start().
* The relevant arguments to handleRequest() is the url of type URI. Although it has no instance variables of its own, it manipulates the runningString and tempString variables to add new strings to a running list.
* The relevant arguments to handle() include the exchage input of type HttpExchange, which is responsible for getting the response from the user. The instance variable response stores the user's input.
* The relevant arguments to start() include the port of type integer and the handler of type URLHandler. The port tells the user what port to input in their URL. The URLHandler inputs into the serverHttpHandler method. Instance variables include the server of type HttpServer that hosts the server itself.
* This specific request causes the URL input variable to change based on the user's input following the equals sign. runningMessage's contents are updated to include the old user input and the new user input. This is then printed to the screen.

**Screenshot 2: using /add-message**
![image](https://github.com/imiancunningham/cse15l-lab-reports/blob/main/Lab%203%20part%201%20string%20server%20part%202.png)
* The methods called when running this code include: handleRequest(), handle(), and start().
* The relevant arguments to handleRequest() is the url of type URI. Although it has no instance variables of its own, it manipulates the runningString and tempString variables to add new strings to a running list.
* The relevant arguments to handle() include the exchage input of type HttpExchange, which is responsible for getting the response from the user. The instance variable response stores the user's input.
* The relevant arguments to start() include the port of type integer and the handler of type URLHandler. The port tells the user what port to input in their URL. The URLHandler inputs into the serverHttpHandler method. Instance variables include the server of type HttpServer that hosts the server itself.
* This specific request causes the URL input variable to change based on the user's input following the equals sign. runningMessage's contents are updated to include the old user input and the new user input. This is then printed to the screen.
# Part 2:
For the reversed method, I made a list that the method incorrectly reversed. 
I created this junit test for {1, 2, 3}:
```
  @Test
  public void testReversedMultiple() {
    int[] input1 = {1,2,3};
    System.out.println("reversed is: ");
    for(int i =0; i<input1.length; i++){
      System.out.println(input1[i]);
    }
    assertArrayEquals(new int[]{3,2,1}, ArrayExamples.reversed(input1));
  }
```
  
This code worked for empty arrays:
```
  @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```

Here are the symptoms for the failed test alongside the working test:
![image](https://github.com/imiancunningham/cse15l-lab-reports/blob/main/ArrayTests%20Symptoms%20Lab%203.png)

Here is the original code before fixing the bug:
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
Here is the code after fixing the bug:
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
```

# Part 3:
I learned how to edit files from github and push the changes back to the repository. 
I did not know I could access online code from a remote terminal until I attended week 3's lab.
