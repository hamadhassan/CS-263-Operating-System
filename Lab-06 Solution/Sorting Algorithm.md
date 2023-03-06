# Sorting Algorithm 

In this reading you will learn how to implement the sorting algorithm in the bash. You will learn the following algorithm 

1. Selection Sort
2. Bubble Sort

In all files it is required that give the permission to read, write and execute by using following command

```bash
chmod 777 [filename]
```

 The 777 grant the  read, write and execute permission.  

## 1. Selection Sort 

Selection sort is an in-place comparison sorting algorithm. It has an O(n²) time complexity, which makes it inefficient on large lists, and generally performs worse than the similar insertion sort

Open the terminal based  text editor using the nano keyword follow by the file name where the  file will be stored. e.g

````bash
nano selectionSort.sh
````

After writing the code into the terminal 

Press CTRL+X command to save the file

Save modify buffer by pressing Y 

Press Enter to close the Nano text editor

e.g

```bash
#!/bin/bash
arr=(64 25 12 22 11)
n=${#arr[@]}
for ((i=0; i<n-1; i++))
do
  min_idx=$i
  
  for ((j=i+1; j<n; j++))
  do
    if [ ${arr[j]} -lt ${arr[min_idx]} ]
    then
      min_idx=$j
    fi
  done
 
  temp=${arr[i]}
  arr[i]=${arr[min_idx]}
  arr[min_idx]=$temp
done

echo "Sorted array: ${arr[@]}"
```

Run the file on the terminal using the following command 

```bash
 ./selectionSort.sh
```

It will run the the script on the terminal.

## 1. Bubble Sort 

Bubble sort, sometimes referred to as sinking sort, is a simple sorting algorithm that repeatedly steps through the input list element by element, comparing the current element with the one after it, swapping their values if needed.

Open the terminal based  text editor using the nano keyword follow by the file name where the  file will be stored. e.g

````bash
nano bubbleSort.sh
````

After writing the code into the terminal 

Press CTRL+X command to save the file

Save modify buffer by pressing Y 

Press Enter to close the Nano text editor

e.g

```bash
#!/bin/bash

arr=(64 25 12 22 11)

n=${#arr[@]}

for ((i=0; i<n-1; i++))
do
  for ((j=0; j<n-i-1; j++))
  do
    if [ ${arr[j]} -gt ${arr[j+1]} ]
    then
      temp=${arr[j]}
      arr[j]=${arr[j+1]}
      arr[j+1]=$temp
    fi
  done
done

# Print the sorted array
echo "Sorted array: ${arr[@]}"
```

Run the file on the terminal using the following command 

```bash
 ./bubbleSort.sh
```

It will run the the script on the terminal.

#### **Conclusion** 

You have learn how to implement the sorting algorithm using bash scripting 