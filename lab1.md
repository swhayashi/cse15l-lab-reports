## CSE 15L: Lab Report 1
---

The ```cd``` command is used to **c**hange **d**irectories.
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
