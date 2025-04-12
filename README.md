# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT

cat < file2![Screenshot from 2025-03-08 11-04-37](https://github.com/user-attachments/assets/2a74f2f6-4b2a-45cf-a33c-302e4d4774df)



## OUTPUT

![Screenshot from 2025-04-12 13-52-24](https://github.com/user-attachments/assets/f6b8823c-22a9-4f1d-860f-658cd21aa2a6)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot from 2025-03-08 11-08-01](https://github.com/user-attachments/assets/138f89a4-db43-4eef-8899-f52635967e42)

comm file1 file2
 ## OUTPUT
![Screenshot from 2025-03-08 11-09-09](https://github.com/user-attachments/assets/90da3e70-edd6-48eb-b4cf-c2ad17db83a3)

 
diff file1 file2
## OUTPUT
![Screenshot from 2025-03-08 11-10-27 (Copy)](https://github.com/user-attachments/assets/2cdb69f4-d19b-4b76-97e9-cde88fca01cf)


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
![Screenshot from 2025-03-08 11-26-29](https://github.com/user-attachments/assets/6be8a211-bba1-4d9e-a72c-ce495503524a)




cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-03-08 11-29-32](https://github.com/user-attachments/assets/3bdd1090-9475-40b7-b50c-c15c184dee84)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-03-08 11-27-45](https://github.com/user-attachments/assets/b407a84a-aedb-45fc-aac7-a3424dd93a67)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

![Screenshot from 2025-03-08 11-34-16](https://github.com/user-attachments/assets/9634ae40-3cfc-41b3-a04e-5147227b2a9f)


grep hello newfile 
## OUTPUT
![Screenshot from 2025-03-08 11-35-25](https://github.com/user-attachments/assets/3c71eb79-44f9-41e7-8c6d-1c1e7d2bc88b)




grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-03-08 11-36-42](https://github.com/user-attachments/assets/c7150c19-d2d3-4ba6-b529-e5d0d9bb2b5c)



cat newfile | grep -i "hello"
## OUTPUT

![Screenshot from 2025-03-08 11-37-49](https://github.com/user-attachments/assets/1de4941b-12ff-42b5-8304-13ee0b2e7f26)



cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2025-03-08 11-37-49](https://github.com/user-attachments/assets/1c4ae9b0-18c7-43e6-be2e-2af7d8a13b07)




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2025-04-12 14-18-54](https://github.com/user-attachments/assets/242a7ff4-8afb-4c67-8113-e4be317183b0)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot from 2025-04-12 14-19-22](https://github.com/user-attachments/assets/93af6a85-1819-4036-a8d8-3d015333ca23)




egrep '(^hello)' newfile 
## OUTPUT

![Screenshot from 2025-04-12 14-19-54](https://github.com/user-attachments/assets/6ac55ef3-aced-4258-a282-613cb393041e)


egrep '(world$)' newfile 
## OUTPUT

![Screenshot from 2025-04-12 14-20-17](https://github.com/user-attachments/assets/6e3ecc4d-4b7e-42fa-a74c-200dbf44b7f3)


egrep '(World$)' newfile 
## OUTPUT

![Screenshot from 2025-04-12 14-20-40](https://github.com/user-attachments/assets/c99c0d21-c8e4-45b1-a393-86bf38fdcf0d)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot from 2025-04-12 14-21-03](https://github.com/user-attachments/assets/78ab0e42-d385-4ba9-a34a-bdfd10f6b82e)


egrep '[1-9]' newfile 
## OUTPUT

![Screenshot from 2025-04-12 14-21-25](https://github.com/user-attachments/assets/ce48f5d8-bff6-41cc-b78a-8b0cdff177d8)


egrep 'Linux.*world' newfile 
## OUTPUT


![Screenshot from 2025-04-12 14-24-19](https://github.com/user-attachments/assets/b12642c7-21ef-4c37-ac60-79ee7fb58662)


egrep 'Linux.*World' newfile 
## OUTPUT

![Screenshot from 2025-04-12 14-24-39](https://github.com/user-attachments/assets/1178900d-f6b1-4d87-b34e-46269da45872)


egrep l{2} newfile
## OUTPUT


![Screenshot from 2025-04-12 14-26-55](https://github.com/user-attachments/assets/c69df5d6-4851-4bdc-a867-2ed609bbb31a)


egrep 's{1,2}' newfile
## OUTPUT 


![Screenshot from 2025-04-12 14-28-05](https://github.com/user-attachments/assets/8f5aab7b-1c60-4b21-9e06-b77a4564985f)

cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT

![Screenshot from 2025-04-12 17-57-20](https://github.com/user-attachments/assets/bfa9f600-6896-47fe-ba5c-72891e506c0c)


sed -n -e '$p' file23
## OUTPUT

![Screenshot from 2025-04-12 17-58-06](https://github.com/user-attachments/assets/49e60597-10c3-4f07-92d0-31d71c5a5941)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-04-12 17-59-04](https://github.com/user-attachments/assets/aebe71fe-52e2-4517-a37f-d43268e428fa)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-04-12 17-59-04](https://github.com/user-attachments/assets/23156dc5-9a08-4261-bcef-91a62b710ea3)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot from 2025-04-12 17-59-44](https://github.com/user-attachments/assets/e06e6006-ae4c-4ce7-a199-5ec5c47ea46b)


sed -n -e '1,5p' file23
## OUTPUT

![Screenshot from 2025-04-12 18-00-27](https://github.com/user-attachments/assets/acbb2779-fdd9-4524-a4f4-a728efd771e4)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-04-12 18-01-24](https://github.com/user-attachments/assets/0ed77c65-f1be-49be-a26d-7428db7ceef0)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-04-12 18-02-35](https://github.com/user-attachments/assets/099a3d38-e6f0-4ebb-9817-ff42234ed993)


seq 10 
## OUTPUT

![Screenshot from 2025-04-12 18-02-58](https://github.com/user-attachments/assets/a68bf9db-b7c2-429b-9805-f6b4700ab98c)


seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot from 2025-04-12 18-03-42](https://github.com/user-attachments/assets/0515eb1f-df9a-4222-9d50-831233f2dcdb)


seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot from 2025-04-12 18-04-30](https://github.com/user-attachments/assets/5e20bcb2-7ecd-43fe-8eb6-ee9262a00438)


seq 3 | sed '2a hello'
## OUTPUT

![Screenshot from 2025-04-12 18-05-24](https://github.com/user-attachments/assets/0afe3433-709a-4a57-9e52-e411c2a671a9)


seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2025-04-12 18-05-54](https://github.com/user-attachments/assets/96ddbf03-f7ff-45b0-9790-d26cd2c62cf2)


seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot from 2025-04-12 18-06-34](https://github.com/user-attachments/assets/911203b1-0df8-4fad-b914-65bd05901753)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


![Screenshot from 2025-04-12 18-06-54](https://github.com/user-attachments/assets/08121726-12ca-45f7-8d88-76178516a62c)


sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT

![Screenshot from 2025-04-12 18-25-04](https://github.com/user-attachments/assets/733360f2-0cc8-4564-9433-2997e038a157)


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

![Screenshot from 2025-04-12 18-25-57](https://github.com/user-attachments/assets/208598fe-93f3-4c9b-a1c2-c70783c4bc28)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2025-04-12 18-26-56](https://github.com/user-attachments/assets/51efaa25-32ec-41c7-857a-c387757e9b35)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![Screenshot from 2025-04-12 18-27-45](https://github.com/user-attachments/assets/1e376c3b-9666-4680-af6d-af63d554363e)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2025-04-12 18-28-59](https://github.com/user-attachments/assets/8e6a575e-3667-45a0-a5c3-0422e71e5186)


#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot from 2025-04-12 18-30-48](https://github.com/user-attachments/assets/31f31183-6c34-4bf6-a97e-6c3c16f7e8a1)



tar -xvf backup.tar
## OUTPUT

![Screenshot from 2025-04-12 18-38-40](https://github.com/user-attachments/assets/eef9f4b6-f0d8-44df-8176-809ac3626285)

gzip backup.tar

ls .gz
## OUTPUT
 ![Screenshot from 2025-04-12 18-38-40](https://github.com/user-attachments/assets/204f2c7b-e139-429e-aafb-980fef3a4c3a)

gunzip backup.tar.gz
## OUTPUT
![Screenshot from 2025-04-12 18-39-27](https://github.com/user-attachments/assets/1fa53ed1-70d5-45db-a5b7-034623ef1fa3)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot from 2025-04-12 18-40-12](https://github.com/user-attachments/assets/200239d9-4053-4cae-b31b-5b9b3e31b294)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot from 2025-04-12 18-40-49](https://github.com/user-attachments/assets/97f64eaf-977a-42c4-8b44-cf9b42ff3e0f)


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![Screenshot from 2025-04-12 18-53-15](https://github.com/user-attachments/assets/c1ca2c53-da4b-4ebe-bfb2-2f7e97048c59)

 
ls file1
## OUTPUT
![Screenshot from 2025-04-12 18-53-15](https://github.com/user-attachments/assets/00c3b103-54f2-422d-ac92-27a0c1dce159)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 ![Screenshot from 2025-04-12 18-54-39](https://github.com/user-attachments/assets/b005841a-7afc-4a2c-84d8-2ada90dd7304)

echo $?
## OUTPUT 
 ![Screenshot from 2025-04-12 18-56-04](https://github.com/user-attachments/assets/8e020e6e-e8cb-439f-a2ea-398c45808a17)

abcd
 
echo $?
 ## OUTPUT

![Screenshot from 2025-04-12 18-56-38](https://github.com/user-attachments/assets/3c6037d4-2263-4cd5-8709-aea32077cd23)

 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT

![Screenshot from 2025-04-12 18-58-26](https://github.com/user-attachments/assets/7a005138-4dea-4646-991c-1948da0339bd)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot from 2025-04-12 18-59-20](https://github.com/user-attachments/assets/a17ed75f-5adc-4f71-9dae-bf2afae9cd32)


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
![Screenshot from 2025-04-12 19-06-56](https://github.com/user-attachments/assets/b114db17-ce64-4837-ab59-6f39f5adaa07)

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT

![Screenshot from 2025-04-12 19-09-09](https://github.com/user-attachments/assets/87197e4d-a912-4f3a-a424-78c786f5ef11)


# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
![Screenshot from 2025-04-12 19-11-15](https://github.com/user-attachments/assets/0fcfc9d5-e6a4-44fe-a62f-b45ec5fd69f5)

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
![Screenshot from 2025-04-12 19-15-45](https://github.com/user-attachments/assets/9fa176e5-b82e-4bbc-a2ce-33388bc23326)

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT


![Screenshot from 2025-04-12 19-22-35](https://github.com/user-attachments/assets/67d23544-cd3f-4c5c-b9bc-048b4e7db9d8)


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![Screenshot from 2025-04-12 19-23-52](https://github.com/user-attachments/assets/25ea03fd-adb2-41b6-aa26-3dad24d33bf5)

# using the case command

cat >casecheck.sh 

```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
![Screenshot from 2025-04-12 19-25-14](https://github.com/user-attachments/assets/0d924b02-cdc9-4f35-9843-d33877e4ca93)

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
![Screenshot from 2025-04-12 19-26-18](https://github.com/user-attachments/assets/dfe3671b-3400-4939-a8fb-62985bf8cd6d)


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![Screenshot from 2025-04-12 19-26-29](https://github.com/user-attachments/assets/69164e28-752e-42bc-8a52-c7e811c51b35)

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
![Screenshot from 2025-04-12 19-26-46](https://github.com/user-attachments/assets/d79599c8-1582-4879-ae85-a2876e060388)

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
![Screenshot from 2025-04-12 19-26-58](https://github.com/user-attachments/assets/d575a381-471a-4198-a53c-bc82d54ec158)

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
![Screenshot from 2025-04-12 19-27-08](https://github.com/user-attachments/assets/15ad31aa-f478-46db-967f-ea40969e9140)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 ![Screenshot from 2025-04-12 19-27-21](https://github.com/user-attachments/assets/33901b5e-fc5b-4556-8705-334d9a141212)

cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
![Screenshot from 2025-04-12 19-27-36](https://github.com/user-attachments/assets/77d7119e-a08b-4e3b-a87b-37ed1d2a2a8d)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![Screenshot from 2025-04-12 19-27-49](https://github.com/user-attachments/assets/fdfa0c68-b184-4cbc-8dfa-5001892b8000)


$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 
![Screenshot from 2025-04-12 19-28-03](https://github.com/user-attachments/assets/35259df3-f9f8-447c-bf6f-79c9c91a41fb)

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3

![Screenshot from 2025-04-12 19-28-16](https://github.com/user-attachments/assets/7330bd8e-343e-4f8c-a7fe-c61e351e17d9)


 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 ![Screenshot from 2025-04-12 19-28-26](https://github.com/user-attachments/assets/d49a181b-1433-4598-87fd-19a729efad1d)

cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 ![Screenshot from 2025-04-12 19-28-39](https://github.com/user-attachments/assets/b3c04c87-a44c-4772-8eb0-979dd58e0c4c)

 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 ![Screenshot from 2025-04-12 19-28-52](https://github.com/user-attachments/assets/69077483-bbe4-4ecb-9b9b-369e8647a7ed)

cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
![Screenshot from 2025-04-12 19-29-12](https://github.com/user-attachments/assets/935772c7-91a1-440c-a0a2-0b8c12cd9b37)


# RESULT:
The Commands are executed successfully.
