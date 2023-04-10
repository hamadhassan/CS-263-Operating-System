# Lab-08 Process Creation

In this reading you will learn how to used process creation in the bash. 

There are some **System Calls** that used in the reading.

```
fork() 
exec() 
wait() 
exit() 
getpid(), getppid() 
getpgrp() 

```

In all files it is required that give the permission to read, write and execute by using following command

```bash
chmod 777 [filename]
```

 The 777 grant the  read, write and execute permission.  

## Task-01

Open the terminal based  text editor using the nano keyword follow by the file name where the  file will be stored. e.g

````bash
nano task01.sh
````

After writing the code into the terminal 

Press CTRL+X command to save the file

Save modify buffer by pressing Y 

Press Enter to close the Nano text editor

e.g

```bash
include <stdio.h>

include <unistd.h>

int main() {
    printf("Parent process ID: %d\n", getpid());
   // Fork first child
    pid_t pid1 = fork();
    if (pid1 > 0) {
        printf("First child process ID: %d\n", pid1);
    }
    else if (pid1 == 0) {
        printf("First child process ID: %d\n", getpid());
        return 0;
    }
    // Fork second child
    pid_t pid2 = fork();
    if (pid2 > 0) {
        printf("Second child process ID: %d\n", pid2);
    }
    else if (pid2 == 0) {
        printf("Second child process ID: %d\n", getpid());
        return 0;
    }
    // Third child process (original parent process)
    printf("Third child process ID: %d\n", getpid());
    return 0;
}
```

Run the file on the terminal using the following command 

```bash
 ./task01.sh
```

It will run the the script on the terminal.

## Task-02 

Open the terminal based  text editor using the nano keyword follow by the file name where the  file will be stored. e.g

````bash
nano Task02.sh
````

After writing the code into the terminal 

Press CTRL+X command to save the file

Save modify buffer by pressing Y 

Press Enter to close the Nano text editor

e.g

```bash
include <stdio.h>

include <unistd.h>

int main() {
    printf("PID of example %d\n", getpid());
     printf("This is hello file \n");
     printf("PID of Hello %d\n", getpid());
    execl("/usr/bin/gcc", "gcc", "hello.c", "-o", "hello", NULL);
    printf("This line will not be executed\n");
    return 0;
}
```

Run the file on the terminal using the following command 

```bash
 ./Task02.sh
```

It will run the the script on the terminal.



## Task-03

Open the terminal based  text editor using the nano keyword follow by the file name where the  file will be stored. e.g

````bash
nano Task03.sh
````

After writing the code into the terminal 

Press CTRL+X command to save the file

Save modify buffer by pressing Y 

Press Enter to close the Nano text editor

e.g

```bash
include <iostream>

int main()
{
    int a = 10, b = 20;
    int sum = a + b;
    std::cout << "The sum of " << a << " and " << b << " is " << sum << std::endl;
    return 0;
}
```

Run the file on the terminal using the following command 

```bash
 ./Task03.sh
```

It will run the the script on the terminal.

#### **Conclusion** 

In the reading you have learn how to create process.
