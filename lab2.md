**Lab 2:**

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
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
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
![Lab 3 part 1 string server part 1 (really lab 2)](https://user-images.githubusercontent.com/122496390/218288857-040c964b-936a-43d0-8517-8a3d3c19afb5.png)

* The methods called when running this code include: handleRequest() and start().
* The relevant arguments to handleRequest() is the url of type URI. Although it has no instance variables of its own, it manipulates the runningString and tempString variables to add new strings to a running list. Before the /add-message, runningString and tempString contain "" and null respectively. After /add-message, tempMessage contains what the user just inputted into the system ("strings"), while runningString holds all the previous messages the user inputted.("string strings").
* The relevant arguments to start() include the port of type integer and the handler of type URLHandler. The port tells the user what port to input in their URL. The port tells the server where to run itself. This port number differentiates it from other server ports. When adding the port to the URL, the URLHandler inputs into the serverHttpHandler method. Instance variables include the server of type HttpServer that hosts the server itself.
* This specific request causes the URL input variable to change based on the user's input following the equals sign. runningMessage's contents are updated to include the old user input and the new user input. This is then printed to the screen.

**Screenshot 2: using /add-message**
![Lab 3 part 1 string server part 2 (really lab 2)](https://user-images.githubusercontent.com/122496390/218288859-3444fc69-1a3c-4550-be54-89f6fc75846e.png)

* The methods called when running this code include: handleRequest(), handle(), and start().
* The relevant arguments to handleRequest() is the url of type URI. Although it has no instance variables of its own, it manipulates the runningString and tempString variables to add new strings to a running list. Before the /add-message, runningString and tempString contain "" and null respectively. After /add-message, tempMessage contains what the user just inputted into the system ("more strings"), while runningString holds all the previous messages the user inputted.("string strings more strings").
* The relevant arguments to handle() include the exchage input of type HttpExchange, which is responsible for getting the response from the user. The instance variable response stores the user's input.
* The relevant arguments to start() include the port of type integer and the handler of type URLHandler. The port tells the user what port to input in their URL. The port tells the server where to run itself. This port number differentiates it from other server ports. When adding the port to the URL, the URLHandler inputs into the serverHttpHandler method. Instance variables include the server of type HttpServer that hosts the server itself.
* This specific request causes the URL input variable to change based on the user's input following the equals sign. runningMessage's contents are updated to include the old user input and the new user input. This is then printed to the screen.
# Part 2:
For the reversed method, I made a list that the method incorrectly reversed. 
I created this junit test for {1, 2, 3}. The expected output is {3, 2, 1}.
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
  
This code worked for empty arrays. The expected output when flipping " " is " ".
```
  @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```

Here are the symptoms for the failed test alongside the working test:
![ArrayTests Symptoms Lab 3 (really lab 2)](https://user-images.githubusercontent.com/122496390/218288865-115f5a00-349f-4c0a-a452-205f77a4a75f.png)

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
Here is the code after fixing the bug. The fix was to return the newArray instead of the original inputted array.
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
