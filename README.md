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

![image](https://github.com/user-attachments/assets/653c8ea0-868a-47b2-aee1-59de290bad1f)


cat < file2
## OUTPUT

![image](https://github.com/user-attachments/assets/b7d7a2b8-da7a-45e5-986d-95d588164022)


# Comparing Files
cmp file1 file2
## OUTPUT

![image](https://github.com/user-attachments/assets/1e69ef65-23f5-4b93-9cf8-67711e4bead8)

 
comm file1 file2
 ## OUTPUT

 ![image](https://github.com/user-attachments/assets/d218bffd-b853-4160-9908-455b265e4856)


diff file1 file2
## OUTPUT

![image](https://github.com/user-attachments/assets/0ae7de68-1f24-4c06-a3b6-cdbc23a7eae6)


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

![image](https://github.com/user-attachments/assets/dbeb0e80-5c8f-40d4-895f-4498f53d03a3)


cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/94c8f468-f81e-499b-bda9-a50cc7fd67d7)


cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/f2cb5f3f-107f-4659-b928-4c0551473c5c)


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

![image](https://github.com/user-attachments/assets/592f293b-628c-4ec9-a3ba-fc9aeeae0f44)

grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/f39d88a7-1fca-4a34-bebf-1d70215c340b)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/8d6b7b17-dbd9-46af-9916-b17a010bcb58)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/8ef0eb40-a4da-4767-aea6-b41d7956ac86)


cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/d10156e8-b88e-4944-a308-729ceb45dc8e)



grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/user-attachments/assets/d62bc4d8-66b4-486a-8e24-bbdf48205999)


grep -w -n world newfile   
## OUTPUT

![image](https://github.com/user-attachments/assets/ff670839-d12c-4cdb-ac03-69c129470710)


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

![image](https://github.com/user-attachments/assets/9b36902d-0890-4c7b-977f-1a0d6f54f8ac)


egrep -w '(H|h)ello' newfile 
## OUTPUT


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/a703ceb3-bc2f-4389-ab84-1f0c69adf39d)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/1ef5b02b-7e1d-4cb6-901b-010037118cca)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/eb660ec7-2d29-4c50-b842-d290815a9f68)


egrep '(World$)' newfile 
## OUTPUT


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/395ece0d-4e8c-4989-bff2-4c0d93487625)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/e8648591-cbf1-426d-ba5c-aa8a85b085bb)


egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/70e55c7c-bf63-4917-8cae-762a7747a100)


egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/5b7b5fcc-bcf8-410d-9bef-299bc4e81722)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/0f5e4747-bfa4-4dab-832b-75724c2a2a54)



egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/user-attachments/assets/d4985662-bde3-4024-ac59-d4272b124685)


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

![image](https://github.com/user-attachments/assets/b2f2185e-48d6-4d62-af19-ffcf8eba9aba)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/d409bf9d-9830-4dcb-945d-058b40f16984)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/84c66f68-f4dd-4c2a-bf14-8e1e5fb99279)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/c4a902b3-f0ec-4c3b-81c4-a22817f0bac7)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/a1e4aacf-b838-4f7c-8f75-ed703ccd925e)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/fc9e925d-5bdb-40e4-ac71-37bbec368cc8)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/4b3f6386-bb32-4ace-a4a6-57455530a8e4)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/d5752229-12af-456f-a733-cd292e7b4fb3)


seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/2d5054ac-cf59-461f-8cdb-4a2c74ef5f97)


seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/user-attachments/assets/acd53b5d-0098-466c-934f-b1f37e413f3a)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/user-attachments/assets/e16fc6cd-ea01-4820-aa87-4005592b2786)


seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/9a47c10f-8b50-43a5-86f2-62d6b9fe5390)


seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/53b73818-5a0a-41f4-81c8-c81f78dbb336)


seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/f873bb0e-ece8-4df7-a90e-aa4bbdfa114d)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/5c918765-bf68-455e-b460-07e0f52ff8fd)

sed -n '2,4{s/$/*/;p}' file23

![image](https://github.com/user-attachments/assets/b0efbfce-2298-4165-bb3a-775bda7c570a)


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

![image](https://github.com/user-attachments/assets/df0b98b0-eb1a-4f1b-b055-b6d91b35168c)

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

![image](https://github.com/user-attachments/assets/102e664b-3730-4300-b4da-50673397520d)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image](https://github.com/user-attachments/assets/5cd5ac11-13d4-4388-a6b6-a075016a1ca9)

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

![image](https://github.com/user-attachments/assets/b038b2c1-82f5-4eb6-8896-d826237dbe1f)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/user-attachments/assets/129cc109-7133-4801-a931-79bc77c7098b)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/user-attachments/assets/d0c5947b-14e2-4c31-86f0-c0968efb48f2)
![image](https://github.com/user-attachments/assets/ade49598-50ce-419a-a3eb-13c53da8a3d5)
![image](https://github.com/user-attachments/assets/940f8b27-08d9-4901-b50e-251b1ee341e5)
![image](https://github.com/user-attachments/assets/24942b72-c5aa-4684-9d24-2e475e9cf27c)


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/01f2c007-4b59-4c86-8cd4-ca5d1a891e45)
![image](https://github.com/user-attachments/assets/5a20a07f-c2f3-4b18-9fc0-5cb231841761)


tar -xvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/d2f8ab3b-f2cf-4c68-9b09-167de0f37b5c)
![image](https://github.com/user-attachments/assets/9eebf044-3f8d-4742-8a7b-0486dd4a2883)
![image](https://github.com/user-attachments/assets/87eec1fd-e1be-4464-b91f-d349c0cb9986)



gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/ed58b4b4-eacf-4ef3-a3cc-0328aa32f045)


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

![image](https://github.com/user-attachments/assets/b4d57990-5934-4c96-b888-5a48667e7d56)

 
ls file1
## OUTPUT

![image](https://github.com/user-attachments/assets/d60f01e7-63e8-4869-9fe2-e338aa5336b7)

echo $?
## OUTPUT 

![image](https://github.com/user-attachments/assets/c7ea8c24-4af2-4e68-8feb-31d97e08b7b8)

./one
bash: ./one: Permission denied
 

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

![image](https://github.com/user-attachments/assets/94a0019c-00a7-443e-ba04-163b13d73e7e)


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

![image](https://github.com/user-attachments/assets/da65b0d5-71da-4353-8814-7e7cf8068b8b)

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

![image](https://github.com/user-attachments/assets/401b7ffa-fc46-49bd-8f51-33b4d07c1013)


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

## OUTPUT

![image](https://github.com/user-attachments/assets/52e8ae3a-ac51-4e9c-866f-afb6eea985d4)


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

![image](https://github.com/user-attachments/assets/99d48990-e5c9-439c-b02e-99c4ce7167f2)


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

![image](https://github.com/user-attachments/assets/4666ca42-2e1d-4bb7-9ec8-578da838ae77)


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

 ![image](https://github.com/user-attachments/assets/f24b03db-e3fa-4827-b44f-9baf55beb28e)

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
 
![image](https://github.com/user-attachments/assets/dfb3cffe-722e-448a-a39f-a8f911b37e5d)

 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
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

 ![image](https://github.com/user-attachments/assets/1fcb6396-eeb8-4055-8823-ebc8c4c3f636)

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


![image](https://github.com/user-attachments/assets/74a5137b-4ec2-4530-8374-98999d0d8d0b)


 
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


![image](https://github.com/user-attachments/assets/16b30496-aaa4-4835-88c4-5643ca12a72a)

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


 ![image](https://github.com/user-attachments/assets/21276545-b28c-4116-ae6b-f8d502deb1d7)

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


![image](https://github.com/user-attachments/assets/a4107881-cdce-47a5-b877-9b55b76ecdda)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT


![image](https://github.com/user-attachments/assets/ca911418-6b03-4989-bb0a-c20b31cf3edd)


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

 ![image](https://github.com/user-attachments/assets/dfc75dce-ab9c-4851-87bf-3accac1d854a)


 
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

 ![image](https://github.com/user-attachments/assets/4f918b0c-f9df-43ec-961e-569e294b78c1)

 
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


 ![image](https://github.com/user-attachments/assets/ac6ac54f-7518-460a-8531-58e9a43f7a0b)

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


![image](https://github.com/user-attachments/assets/d469442c-9228-4987-881c-46a07fa07b32)


# RESULT:
The Commands are executed successfully.
