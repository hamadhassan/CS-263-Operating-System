# Lab-05 Shell Scripting (Array)

In this lab we will learn how to perform the following task,

1. **Arrays**

An array is a systematic arrangement of the same type of data. But in Shell script Array is a variable which contains multiple values may be of same type or different type since by default in shell script everything is treated as a string. An array is zero-based i.e indexing start with 0.

1. **Indirect Declaration**

In Indirect declaration, We assigned a value in a particular index of Array Variable. No need to first declare.

```bash
ARRAYNAME[INDEXNR]=value
```

2. **Explicit Declaration**

In Explicit Declaration, First We declare array then assigned the values.

```bash
declare -a ARRAYNAME
```

3. **Compound Assignment**

In Compound Assignment, We declare array with a bunch of values. We can add other values later too.

```bash
ARRAYNAME=(value1 value2  .... valueN)
```

---

In all files it is required that give the permission to read, write and execute by using following command

```bash
chmod 777 [filename]
```

 The 777 grant the  read, write and execute permission.  

**Question 01**

Create a Bash script to find the most occurring element in an array of integers.

**Solution** 

Open the terminal based  text editor using the nano keyword follow by the file name where the  file will be stored. e.g

```bash
nano task1.sh
```

![image-20230220150757854](D:\COMPUTER SCIENCE\Repo_OS\Lab-05 Solution\image-20230220150757854.png)

After writing the code into the terminal 

Press CTRL+X command to save the file

Save modify buffer by pressing Y 

Press Enter to close the Nano text editor

e.g

```bash
#!/bin/bash
if [ -z "$1" ]; then
   echo "No argument supplied. Please supply an array of integers as argument."
   exit 1
fi
array=($1)
most_occur=0
for i in "${array[@]}"
do
   count=0
   for j in "${array[@]}"
   do
      if [ $i -eq $j ]; then
         ((count++))
      fi
   done
   if [ $count -gt $most_occur ]; then
      most_occur=$i
   fi
done
echo $most_occur
```

Run the file on the terminal using the following command 

```bash
 ./task1.sh
```

It will run the the script on the terminal.e.g

![image-20230220151136847](image-20230220151136847.png)

**Question 02**

Create a Bash script to find the largest element of a given array of integers.

**Solution**

Open the terminal based  text editor using the nano keyword follow by the file name where the  file will be stored. e.g

```
nano task2.sh
```

After writing the code into the terminal 

Press CTRL+X command to save the file

Save modify buffer by pressing Y 

Press Enter to close the Nano text editor

e.g

```bash
#!/bin/bash
array=(5 10 15 20 25 30 35 40 45 50)
max=${array[0]}
for i in "${array[@]}"
do
    if (( $i > $max ))
    then
        max=$i
    fi
done
echo "The largest element in the array is: $max"
```

Run the file on the terminal using the following command 

```bash
 ./task2.sh
```

**Question 03**

Create a Bash script to separate 0s and 1s from a given array of values 0 and 1.

**Solution**

Open the terminal based  text editor using the nano keyword follow by the file name where the  file will be stored. e.g

```
nano task3.sh
```

After writing the code into the terminal 

Press CTRL+X command to save the file

Save modify buffer by pressing Y 

Press Enter to close the Nano text editor

e.g

```
!/bin/bash
arr=(0 0 1 1 0 1 0)
zeros=()
ones=()
for i in "${arr[@]}"
do
    # If element is 0, append it to zeros array
    if [ $i -eq 0 ]
    then
        zeros+=("$i")
    else
        # Else, append it to ones array
        ones+=("$i")
    fi
done
echo "Zeros Array: ${zeros[@]}"
echo "Ones Array: ${ones[@]}"
```

Run the file on the terminal using the following command 

```bash
 ./task3.sh
```

**Question 04**

Open the terminal based  text editor using the nano keyword follow by the file name where the  file will be stored. e.g

```
nano task4.sh
```

After writing the code into the terminal 

Press CTRL+X command to save the file

Save modify buffer by pressing Y 

Press Enter to close the Nano text editor

e.g

```bash
!/bin/bash
arr=(4 6 3 2 8 6 1 9)
for i in "${!arr[@]}"; do
  for j in "${arr[@]:$i+1}"; do
    if [[ $j -eq ${arr[$i]} ]]; then
      echo "${arr[$i]}"
      exit 0
    fi
  done
done
echo "No repeating elements found"
exit 1
```

Run the file on the terminal using the following command 

```bash
 ./task4.sh
```

**Conclusion**

Array provide the user to store large amount of data efficiently and also able to access
