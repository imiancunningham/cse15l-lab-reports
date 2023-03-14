# 4 uses of the find command

## 1) find file name ignoring capitals.
   Source: [https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/](https://www.redhat.com/sysadmin/linux-find-command)
   
![Lab report 5 find example 1](https://user-images.githubusercontent.com/122496390/224914313-9b94eec8-f8e9-426b-8ad9-c068bbec2c85.png)

Using asterisks before letters that could be capitalized in the file name causes bash to ignore case sensitivity for that character. Although my bash failed to find the file, it should have successfully found Server.java even though I did not capitalize server.

## 2) find -ls recursively looks for files within directories.
   Source:[https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/](https://www.redhat.com/sysadmin/linux-find-command)

![Lab report 5 find example 2](https://user-images.githubusercontent.com/122496390/224914392-9bcf6a72-7838-428f-bdc7-5a89a9462ce3.png)

The -ls command caused bash to look inside every directory for any file that refrenced the text.

## 3) find -type f for files of a specific type.
   Source: [https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/](https://www.redhat.com/sysadmin/linux-find-command)

![Lab report 5 find example 3](https://user-images.githubusercontent.com/122496390/224914441-a0b83073-996d-4996-995d-0b40c5b6cd4c.png)

the -type f command searches for files only (no directories). Many files showed up here since we included all of the cache folder.

## 4) find -type d looks for only directories.
   Source:[https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/](https://www.redhat.com/sysadmin/linux-find-command)

![Lab report 5 find example 4](https://user-images.githubusercontent.com/122496390/224914488-73a35855-d3b9-43d1-90c9-bdd911392934.png)

Here, only the directories are printed out by bash. This includes cache and all of its subdirectories.
