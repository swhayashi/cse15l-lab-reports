# CSE 15L: Lab Report 1
---

   **Author**: Sam Hayashi
    
   **Date**: 10/02/2023
    
   **Section**: CSE 15L Lab, Mondays @ 10:00am - 11:50pm

## The ```cd``` command is used to **c**hange **d**irectories.
---

1. Simply using ```cd``` with no additional arguments will take us to the root/home directory. In the following example, our working directory is ```lecture1``` when we run the ```cd``` command:

    ```
    [user@sahara ~/lecture1]$ cd
    [user@sahara ~]$
    ```
   As indicated by the square brackets, our working directory changes to the root after running the command with no arguments. This is not an error!

2. Suppose we added an argument to the ```cd``` command. This argument allows us to change our directory from the working directory to a specific directory *using a path from the working directory to the desired one.* For example, from the root directory we can use ```cd lecture1``` to select the ```lecture1``` directory:
    ```
    [user@sahara ~]$ cd lecture1
    [user@sahara ~/lecture1]$
    ```
   There are no errors, and our working directory has changed to ```lecture1```. If we were to run the command again from here, however, we would see:
   ```
    [user@sahara ~/lecture1]$ cd lecture1
    bash: cd: lecture1: No such file or directory
    ```
   This is an error, and it appears because the directory ```lecture1``` is already the working directory, and ```lecture1``` doesn't contain an additional directory called ```lecture1```.
   

3. Lastly, if we target a specific file with the ```cd``` command instead of a directory, we will get an error message. In the below example, we try to select ```Hello.java```, a file inside of directory ```lecture1```, and see an error:

    ```
    [user@sahara ~/lecture1]$ cd Hello.java
    bash: cd: Hello.java: Not a directory
    ```
   We get the error because ```Hello.java``` is not a directory, and we can't *change directories* to something that isn't a directory.

## The ```ls``` command is used to list the contents of a directory.
---

1. Simply using ```ls``` with no arguments lists all contents in the current working directory. For example, with the directory ```lecture1``` as the working directory, we can use ```ls``` to list its contents:

   ```
   [user@sahara ~]$ cd lecture1
   [user@sahara ~/lecture1]$ ls
   Hello.class  Hello.java  messages  README
   [user@sahara ~/lecture1]$
   ```

   There was no error. The first command we used to set ```lecture1``` as the working directory. The second command ```ls``` listed its contents, which are displayed in the third line. They are ```Hello.class```, ```Hello.java```, ```messages```, and ```README```.

2. We can use a directory as an argument for ```ls```. For example:

   ```
   [user@sahara ~]$ ls lecture1
   Hello.class  Hello.java  messages  README
   [user@sahara ~]$
   ```

   In this, our working directory is the root. We use the command ```ls lecture1``` to list all the contents of ```lecture1``` without actually setting it as our working directory. In the second line, the expected contents of ```lecture1``` are listed, and in the third line, we can see that the root is still our working directory.

3. Finally, we can also use a file as an argument for ```ls```. For example:

   ```
   [user@sahara ~/lecture1]$ ls Hello.java
   Hello.java
   [user@sahara ~/lecture1]$
   ```

   Above, we have ```lecture1``` as our working directory. We use the command ```ls Hello.java``` and in the following line, it simply lists ```Hello.java```. There is no error, but it's a bit silly.
