# Part 1: ADD FORMATIIING!!!

# Part 2:
For the reversed method, I made a list {1, 2, 3} that the method incorrectly reversed. 
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
Use photo from Ubuntu files.


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
I did not know I could access online code from a remote terminal until week 3's lab.
