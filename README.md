# copy-file
## AIM:
To write a python program for copying the contents from one file to another file.
## EQUIPEMENT'S REQUIRED: 
PC
Anaconda - Python 3.7
## ALGORITHM: 
### Step 1:
From shutil import copy file


### Step 2: 
From sys import exit 
### Step 3: 
Getting input for source file


### Step 4:  
Getting input for target file


### Step 5: 

Giving condition for files


### Step 6: 
Getting statement from the user to print or not want to print


## PROGRAM:
#Developed by : TH KARTHIK KRISHNA 
#Reg no : 23014165

import sys

count=0

with open(sys.argv[1],'r') as f:
```
    for line in f:
    
        word=line.split()
        
        count+=len(word)
```
print("Word Count in File=",count)

from shutil import copyfile

from sys import exit

source = input("Enter source file with full path: ")

target = input("Enter target file with full path: ")

###adding exception handling
try:
```
copyfile(source, target)
```
except IOError as e:
```
print("Unable to copy file. %s" % e)

exit(1)

```
except:

print("Unexpected error:", sys.exc_info())

exit(1)
print("\nFile copy done!\n")

while True:

print("Do you like to print the file ? (y/n): ")

check = input()

if check == 'n':

    break

elif check == 'y':

    file = open(target, "r")
```    
    print("\nHere follows the file content:\n")
    
    print(file.read())
    
    file.close()
    
    print()
    
    break

else:
   
    continue
```


### OUTPUT:
![screenshot2](https://github.com/anushanirudh/copy-file/assets/151725737/071b7a3c-6c35-4948-8322-08df792d04ed)



## RESULT:
Thus the program is written to copy the contents from one file to another file.
