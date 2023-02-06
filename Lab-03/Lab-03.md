# Lab-03 Shell Scripting

**Question#01**

Create a simple script which will take two command line arguments and then multiply them together

**Solution**

Create a new file using nano command 

![image-20230206133902734](D:\COMPUTER SCIENCE\Repo_OS\Lab-03\image-20230206133902734.png)

```bash
nano multiply.sh
```

![image-20230206134009600](D:\COMPUTER SCIENCE\Repo_OS\Lab-03\image-20230206134009600.png)

```bash
#!/bin/bash
a=0
b=0
echo "Enter first number"
read a
echo "Enter second number"
read b
let sum=a*b
echo "Sum of two number is" $sum
```

Enter CTRL+X command to save the file

Save modify buffer by pressing Y 

Press Enter to close the nano window



![image-20230206134117397](D:\COMPUTER SCIENCE\Repo_OS\Lab-03\image-20230206134117397.png)

```bash
chmod 777 multiply.sh
```

![image-20230206134156002](D:\COMPUTER SCIENCE\Repo_OS\Lab-03\image-20230206134156002.png)

```
./multiply.sh
```

**Question#02**

Create a simple script, which will ask the user for a few pieces of information then combine this into a message which is echo'd to the screen.

**Solution**

Create a new file using nano command 

![image-20230206135512376](D:\COMPUTER SCIENCE\Repo_OS\Lab-03\image-20230206135512376.png)

```bash
nano join.sh
```



![image-20230206135538313](D:\COMPUTER SCIENCE\Repo_OS\Lab-03\image-20230206135538313.png)

```bash
#!/bin/bash
s1=""
s2=""
echo "Enter first name"
read s1
echo "Enter last name"
read s2
echo "Full name is" $s1 $s2
```

Enter CTRL+X command to save the file

Save modify buffer by pressing Y 

Press Enter to close the nano window

![](D:\COMPUTER SCIENCE\Repo_OS\Lab-03\image-20230206135624639.png)

```bash
chmod 777 join.sh
./join.sh
```

**Question#03**

Now Mr. Tom suddenly lost the track of his current location. Help him find his location.

**Solution**

![image-20230206135702418](D:\COMPUTER SCIENCE\Repo_OS\Lab-03\image-20230206135702418.png)

```bash
pwd
```

**Question#04**

He wants the list of all files present on home directory.

**Solution**

![image-20230206135746170](C:\Users\Hammad Hassan\AppData\Roaming\Typora\typora-user-images\image-20230206135746170.png)

```bash
ls
```

**Question#05**

Display the current time.

**Solution**

![image-20230206135929934](C:\Users\Hammad Hassan\AppData\Roaming\Typora\typora-user-images\image-20230206135929934.png)

```bash
timedatectl
```

**Question#06**

He is done with the task and he is happy with your work. He want to display a thankyou message.

**Solution**

![image-20230206140042578](C:\Users\Hammad Hassan\AppData\Roaming\Typora\typora-user-images\image-20230206140042578.png)

```bash
echo "Thank you so much"
```

---



**Question#01**

Write a simple shell script that uses arithmetic operators (+, -,*) using double parenthesis with printing your own roll # with the results of operations.

**Solution**

Create a new file using nano command 

![image-20230206140742803](D:\COMPUTER SCIENCE\Repo_OS\Lab-03\image-20230206140742803.png)

```bash
nano sumDoubleParenthesis.sh
```

![image-20230206140818574](D:\COMPUTER SCIENCE\Repo_OS\Lab-03\image-20230206140818574.png)

```bash
#!/bin/bash
a=0
b=0
echo "Enter first number"
read a
echo "Enter second number"
read b
echo "2021-CS-33"
echo "Sum is" $((a+b))
echo "Multiplication is" $((a*b))
echo "Division is" $((a/b))
```

Enter CTRL+X command to save the file

Save modify buffer by pressing Y 

Press Enter to close the nano window

![image-20230206140922229](D:\COMPUTER SCIENCE\Repo_OS\Lab-03\image-20230206140922229.png)

```bash
chmod 777 sumDoubleParenthesis.sh
./sumDoubleParenthesis.sh
```

**Question#02**

Write a simple shell script that uses all relational operators with printing your own roll # with the results of operations.

**Solution**

Create a new file using nano command 

```bash
nano sumDouble.sh
```

![image-20230206141548510](D:\COMPUTER SCIENCE\Repo_OS\Lab-03\image-20230206141548510.png)

![image-20230206144133062](D:\COMPUTER SCIENCE\Repo_OS\Lab-03\image-20230206144133062.png)

```bash
#!/bin/bash
a=0
b=0
echo "Enter first number"
read a
echo "Enter second number"
read b
echo "2021-CS-33: " $((a>b))
echo "2021-CS-33: " $((a<b))
echo "2021-CS-33: " $((a=b))
```

Enter CTRL+X command to save the file

Save modify buffer by pressing Y 

Press Enter to close the nano window

![image-20230206144300054](D:\COMPUTER SCIENCE\Repo_OS\Lab-03\image-20230206144300054.png)

```bash
chmod 777 sumDouble.sh
./sumDouble.sh
```

