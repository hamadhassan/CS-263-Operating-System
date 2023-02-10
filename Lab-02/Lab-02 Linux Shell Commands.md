

# Lab-02 Linux Shell Commands

It is a guide that help new Ubuntu user in performing Ubuntu commands.

---

## Task-01

**Question # 01**: 

Create a file named “XXXX-CS-XXX.txt”. File must contain at least 10 lines.

**Solution**

![image-20230127165352320](.\Images\image-20230127165352320.png)

```
touch 2021-CS-33.txt
```

**touch** : Creating file.

```
nano 2021-CS-33.txt
```

**nano** : Write the file content.

```
cat 2021-CS-33.txt
```

**cat**: View the file content.

**Question # 02**: 

Create another file named “your name.txt”. File must contain at least 10 lines

**Solution**

![image-20230127170014823](.\Images\image-20230127170014823.png)

```bash
touch M.HamadHassan.txt
```

**touch** : Creating file.

```bash
nano M.HamadHassan.txt
```

**nano** : Write the file content.

```bash
cat M.HamadHassan.txt
```

**cat**: View the file content.

**Question # 03**: 

Merge the data of both files.

**Solution**

![image-20230127170328519](.\Images\image-20230127170328519.png)

```bash
cat 2021-CS-33.txt M.HamadHassan.txt
```

**Question # 04**:

Redirect the output to a new file.

**Solution**

![image-20230127170605666](.\Images\image-20230127170605666.png)

````bash
cat 2021-CS-33.txt M.HamadHassan.txt > mergeContent.txt
cat mergeContent.txt
````

**>**: To redirect output from all the files to a new file

**Question # 05**:

Display the first two lines of first file.

**Solution**

![image-20230127171320885](.\Images\image-20230127171320885.png)

```bash
head -2 2021-CS-33.txt
```

**Question # 06**: 

Display the last two lines of second file.

**Solution**

![image-20230127171502210](.\Images\image-20230127171502210.png)

```bash
tail -2 M.HamadHassan.txt
```

**Question # 07**: 

Finds the string (your roll#) from the first file.

**Answer**

![image-20230127171652935](D:\COMPUTER SCIENCE\Repo_OS\Lab-02\Task-01\image-20230127171652935.png)

```bash
grep "2021-CS-33" 2021-CS-33.txt
```

**Question # 08**: 

Grant the execute permission of the second file to the group.

**Solution**

![image-20230127172651413](.\Images\image-20230127172651413.png)

```bash
ls -l
chmod g+x M.HamadHassan.txt
ls -l
```

**Question # 09**: 

Remove the write permission for the owner.

**Solution**

![image-20230127173201581](.\Images\image-202301271730295482.png)

```bash
ls -l
chmod u-w M.HamadHassan.txt
ls -l
```

**Question # 10**: 

Now Mr. Tom suddenly lost the track of his current location. Help him find his
location.

**Solution**

![image-20230127173342182](.\Images\image-20230127173342182.png)

```bash
pwd
```

**Question # 11**: 

He wants the list of all files present on Desktop directory.

**Solution**

![image-20230127173431832](.\Images\image-20230127173431832.png)

```bash
ls
```



**Question # 12**: 

Now he wanted to create a folder of his personal files and pictures named as
your roll#.

**Solution**

![image-20230127173549582](C:\Users\Hammad Hassan\AppData\Roaming\Typora\typora-user-images\image-20230127173549582.png)

```bash
mkdir 2021-CS-33
```

**Question # 13**: 

Display the current time.

**Solution**

![image-20230127174110182](.\Images\image-20230127174110182.png)

```bash
timedatectl
```

**Question # 14**: 

He is done with the task and he is happy with your work. He want to display a
thankyou message.

**Solution**

![image-20230127174303101](.\Images\image-20230127174303101.png)

```bash
Thanks you so much
```

---

## Task-02

**Question # 1**: 

Create a file named XXXX-CS-XXX_OS-lab_rules.txt” using linux commands.
The file must contain all lab rules covered in first lab.

**Solution**

![image-20230127175601046](.\Images\image-20230127175601046.png)



````bash
touch 2021-CS-33_OS-lab-rules.txt
nano 2021-CS-33_OS-lab-rules.txt
ls -l
````

**Question # 2**: 

You want to set the rights of created file to this (- rwx r-x r--). 

**Solution**

![image-20230127175431538](.\Images\image-20230127175431538.png)

```bash
chmod g-w 2021-CS-33_OS-lab-rules.txt
chmod g+x 2021-CS-33_OS-lab-rules.txt
chmod u+x 2021-CS-33_OS-lab-rules.txt
ls -l
```

**Question # 3**: 

Append the output of ls command to created file.

**Solution**

![image-20230127180803463](.\Images\image-20230127180803463.png)

```bash
cat 2021-CS-33_OS-lab-rules.txt >> fileContents
cat 2021-CS-33_OS-lab-rules.txt >> fileContents 
cat fileContents
```

