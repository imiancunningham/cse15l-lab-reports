# 4 uses of the grep command

## 1) grep -l finds file names matching the given text.
   Source: [[Link](https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/)](https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/)

![Lab report 3 grep -l example 1](https://user-images.githubusercontent.com/122496390/218268260-f3643999-5758-4d9b-857d-c811cff29578.png)

The `-l` command for `grep` allows you to search for a sequence of characters in a files name. Here we search for the prefix "non" and the terminal returns the `non-fiction` directory.

![Lab report 3 grep -l example 2](https://user-images.githubusercontent.com/122496390/218268276-a9434976-48f4-49d8-8286-c2226f6b55d6.png)

In this second example of the `-l` command, `grep` searches for a set of characters shared by multiple files. By searching for "ch", all of the `chapter` text files appear.

## 2) grep -n shows which lines the text appears on.
   Source: [[Link](https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/)](https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/)

![Lab report 3 grep -n example 1](https://user-images.githubusercontent.com/122496390/218268285-2744dfae-ff3d-4837-9072-6ab28a0f6e88.png)

The `-n` `grep` command allows you to search for a set of characters in a file, then the terminal will tell you the line number it appears on and print out the entire line of text. In this example, the word "possible" (displayed in red) appears on line 86 as can be seen by the green text on the left side.

![Lab report 3 grep -n example 2](https://user-images.githubusercontent.com/122496390/218268292-f9b8d31b-146c-42a6-8e9c-a52588f4b189.png)

For the second example, the `grep -n` command searches for "founders" and finds it on two separate lines, appearing twice in one of them. It will display the entirety of each of those lines along with red font for the specific set of characters searched.

## 3) grep -i does a search ignoring the case of the text.
   Source: [[Link](https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/)](https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/)

![Lab report 3 grep -i example 1](https://user-images.githubusercontent.com/122496390/218268302-40bf899c-072b-4cb5-b30c-2e428f7bbf44.png)

The `grep -i` command performs a search looking for a set of characters while ignoring whether they are upper or lower case. The word `suffering` is purposely capitalized incorrectly in order to show how the `grep -i` command does not care about the case of each character.

![Lab report 3 grep -i example 2](https://user-images.githubusercontent.com/122496390/218268305-bd273d52-8442-467c-8611-a5770c365b88.png)

The word "defined" is given to the `grep -i` command, appearing twice despite the capitalization being completely different from how it appears in the document.

## 4) `grep -A` displays N lines after the text it matches.
   Source: [[Link](https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/)](https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/)

![Lab report 3 grep -A example 1](https://user-images.githubusercontent.com/122496390/218268308-aad3d60b-18f7-4552-b211-9029bd4a5bf7.png)

The `grep -A` command displays the line where a piece of text appears, along with a number of lines after it determined by the user. In this example I chose two lines following the line that contains the given piece of text.

![Lab report 3 grep -A example 2](https://user-images.githubusercontent.com/122496390/218268311-acd54f6d-2f31-4ef8-b7bf-77fe154f6f83.png)

Here I only asked the terminal to display one line following the line containing the set of characters.

