# Lab-04 Shell Scripting

In this lab we will learn how to perform the following task,

1. Conditional Statements
2. Loops
3. Functions

All of these task will be performed using the Shell Scripting which is power way to write the commands in the ubuntu operating system.

In all files it is required that give the permission to read, write and execute by using following command

```bash
chmod 777 [filename]
```

 The 777 grant the  read, write and execute permission.  

## 1. Conditional Statements

The decisions making in the shell scripting give new power to perform the complex task. 

**Syntax** 

```bash
if ((condition))
then # *block of code to be executed if the condition is true*
fi
```

**Note** Make sure that you close the if statement with fi.

#### **Examples**

**Question-01**

Create a Bash script which will take 3 numbers as command line arguments. It
will print to the screen the larger of the three numbers

**Solution**

```bash
nano task2Decision.sh
```

Open the terminal based  text editor using the nano keyword follow by the file name where the  file will be stored. e.g

![image-20230213142952285](image-20230213142952285.png)

After writing the code into the terminal 

Press CTRL+X command to save the file

Save modify buffer by pressing Y 

Press Enter to close the Nano text editor

e.g

![image-20230213143310257](image-20230213143310257.png)

Run the file on the terminal using the following command 

```bash
 ./task1Decision.sh
```

It will run the the script on the terminal.e.g

![image-20230213143435468](image-20230213143435468.png)



**Question-02**

Create a Bash script which will print a message based upon which day of the
week it is (eg. 3 for Wednesday, 5 for Friday etc) using
switch statement.

**Solution**

````bash
nano task2Decision.sh
````

Open the terminal based  text editor using the nano keyword follow by the file name where the  file will be stored. e.g![image-20230213143641976](image-20230213143641976.png)

After writing the code into the terminal 

Press CTRL+X command to save the file

Save modify buffer by pressing Y 

Press Enter to close the Nano text editor

e.g

![image-20230213143612199](image-20230213143612199.png)

Run the file on the terminal using the following command 

```bash
 ./task2Decision.sh
```

It will run the the script on the terminal.e.g

![image-20230213143744991](image-20230213143744991.png)

### 3. Loops

Loops are used to perform the repetitive task in the easier way.

**Syntax** 

```bash
while ((condition))
do
then # *block of code to be executed if the condition is true*
done
```

**Note** Make sure that you close the loop by then keyword.

**Question-01**

**Solution**

````bash
nano task1Loop.sh
````

Open the terminal based  text editor using the Nano keyword follow by the file name where the  file will be stored. e.g

![image-20230213144407963](image-20230213144407963.png)

After writing the code into the terminal 

Press CTRL+X command to save the file

Save modify buffer by pressing Y 

Press Enter to close the Nano text editor

e.g

![image-20230213144452703](image-20230213144452703.png)

Run the file on the terminal using the following command 

```bash
 ./ task1Loop.sh
```

It will run the the script on the terminal.e.g

![image-20230213144431422](image-20230213144431422.png)



**Question-02**

**Solution**

![image-20230213145104088](image-20230213145104088.png)

![image-20230213145238067](image-20230213145238067.png)



![image-20230213145155405](image-20230213145155405.png)

### Task 3 (Functions)

**Question-01**

**Solution**

![image-20230213151857566](image-20230213151857566.png)

![image-20230213151912499](image-20230213151912499.png)

![image-20230213151953994](image-20230213151953994.png)

**Question-02**

**Solution**

![image-20230213152638214](image-20230213152638214.png)

![image-20230213152755194](image-20230213152755194.png)

![image-20230213153216618](image-20230213153216618.png)