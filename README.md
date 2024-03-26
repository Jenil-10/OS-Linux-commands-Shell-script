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
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/d4804939-ac2f-412d-a271-a9a42bf3f3e3)



cat < file2
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/57e02b1c-1bb9-40d6-b1ea-b52658cc99ae)


# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/4df82913-5e3a-4eca-8676-e4a15a7dc609)
 
comm file1 file2
 ## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/97a59147-dce9-49e9-b685-cccaeeca5d18)

 
diff file1 file2
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/0788812f-955b-48cf-95a8-449c930846c3)


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
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/487007d9-0934-442e-a5ff-dcf6e00ebeef)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/c552094b-3cbb-4995-9495-f6e55c808dfa)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/108c482d-a069-4c34-9223-bbcb61c7fc51)


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
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/d450944d-04ec-4a24-9380-39fcffb020d6)



grep hello newfile 
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/ab588dcd-4376-4110-a9ba-8437d82269a7)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/4f37a0a2-60c9-49cd-9b47-fc5b09fe1b76)



cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/eb149988-488d-44c0-a9c1-f6c296255fcc)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/ae3e1a2f-3be5-4c82-be7f-a97b4d321ae1)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/5a5a5dca-ec32-45f0-a5db-5b4ca708ca74)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/d0acd277-93d4-410f-9000-2b4b069195e1)


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
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/f836b922-407c-4488-aa42-78e610360c1d)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/e1f91480-609d-4062-a221-bf349b67670d)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/84cb4969-341d-4728-a639-92863eadffd2)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/235debf4-63f3-411e-95c2-e6f984434f85)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/1645a6d6-c092-4379-b49b-afad37ad783f)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/8ee9c6d5-b9f5-4802-9543-21c36fd03175)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/7b9b8788-4ffb-48ae-bea4-f5972f904b5b)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/280fb5ef-4cd3-41ee-aed9-29ad99bde492)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/675574bf-5e41-4882-ba09-cc1dc04e9dd7)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/c12c370f-2152-4e33-8d43-1c7bdc5e832f)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/5c10ff0c-95cf-4341-a246-139fac576a33)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/f950df9d-12ed-4b4e-9e3f-4055b82b9cbb)


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
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/b6e480e4-f214-4d9d-abb1-f77927c9c88d)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/730d957c-ebe8-4ef4-90e2-b66c939bbe01)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/ed294015-c6bf-4399-b529-8d25c96c995b)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/bd154668-0069-4a31-8a75-f3e1dbb4fc95)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/f574a17a-afed-4959-b7b1-cc20c6de1480)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/2617eae4-bf1c-4743-a268-f57e41a1cd41)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/cd8cfc80-2fd1-4312-b380-82c13d024cd0)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/d2ddcc12-a679-4a90-b016-9552f86541c4)



seq 10 
## OUTPUT

![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/98ded5f5-5325-4e61-8f25-e2c8503e12c3)




seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/0d1e82ef-0858-4cd3-90a7-45d3b43597e8)



seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/b51ae742-36b5-4dbf-ae19-37a48553173a)



seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/18098721-57cb-4191-880b-e69a29a89e18)



seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/61976016-029e-4951-a513-4b37c4740ebb)


seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/330dd0f0-82ed-486a-8364-496d855e527c)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/72ee3c34-b624-40fb-97f9-776b7564b33c)



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

![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/f729ce42-4d21-422b-83da-91585b302322)


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

![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/5141df36-16ef-48f5-a152-6213c8e9492d)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/e8e7e8e0-1e87-40a7-b249-c20428b720db)

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

![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/6375e8fe-38cf-4df2-beef-30d39a96f62f)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/4049cb99-3762-40cb-a090-784db5464042)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
-rw-r--r-- user/group 0 2024-02-25 14:30:00 file1.txt
drwxr-xr-x user/group 0 2024-02-25 14:30:00 directory1/
-rw-r--r-- user/group 1024 2024-02-25 14:30:00 directory1/file2.txt
-rw-r--r-- user/group 2048 2024-02-25 14:30:00 directory1/file3.txt

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
x file1.txt
x directory1/
x directory1/file2.txt
x directory1/file3.txt

tar -xvf backup.tar
## OUTPUT
 backup.tar.gz
gzip backup.tar

ls .gz
## OUTPUT
backup.tar 
gunzip backup.tar.gz
## OUTPUT
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/dc18fb5e-9855-4cdc-bd15-ba340c92bbe8)


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
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
 
ls file1
## OUTPUT

![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/7030707e-af98-467c-b6fe-04385d862727)

echo $?
## OUTPUT 

![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/298f78e7-639a-473b-83b8-682a9449090b)

 
echo $?
## OUTPUT 

 ![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/79a0a25e-720f-43bb-ad15-53b476e90d98)

abcd
 
echo $?
 ## OUTPUT

![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/3c712735-a485-419f-bace-d29c6faebbd0)


 
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


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi

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

![image](https://github.com/Jenil-10/OS-Linux-commands-Shell-script/assets/145972423/54679063-3319-44c0-8c76-6551f811b6b5)

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
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d


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
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 
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
Enter your name: John
Hello John, welcome to my program.
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
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “ 
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

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done


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
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
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
 + (( 0 ))
+ set +x
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
 total characters 75
Number of Lines are 10
No of Words count: 10
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
Enter the number
121
Number is palindrome
Enter the number
69
Number is NOT palindrome

# RESULT:
The Commands are executed successfully.
