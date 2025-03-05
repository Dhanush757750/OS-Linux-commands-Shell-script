![Screenshot from 2025-03-05 14-07-11](https://github.com/user-attachments/assets/a81cad30-7841-45d9-9d58-be88d0e2ed2e)![Screenshot from 2025-03-05 13-59-46](https://github.com/user-attachments/assets/6e18854c-f965-4f20-92c1-c2db222c7281)![Screenshot from 2025-03-05 13-45-19](https://github.com/user-attachments/assets/dbaf7103-d14e-4980-86db-1607edd9054f)# OS-Linux-commands-Shell-scripting
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
![Screenshot from 2025-03-05 13-16-18](https://github.com/user-attachments/assets/8d076338-eda4-49d7-bc2c-2bab680ed9c3)
cat < file2
## OUTPUT
![Screenshot from 2025-03-05 13-21-38](https://github.com/user-attachments/assets/1f7e7180-6cac-4b26-9fe2-73bc47cf0cc1)
# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot from 2025-03-05 13-23-53](https://github.com/user-attachments/assets/10dd6688-9883-499d-ac4d-c7184f0ce7cb)
comm file1 file2
## OUTPUT
![Screenshot from 2025-03-05 13-24-59](https://github.com/user-attachments/assets/14a65f94-1384-4fdc-96d0-449d420df50f)
diff file1 file2
## OUTPUT
![Screenshot from 2025-03-05 13-26-03](https://github.com/user-attachments/assets/47940243-bb76-4a23-892d-5d35cce18085)
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
![Screenshot from 2025-03-05 13-29-31](https://github.com/user-attachments/assets/204f1ecb-9952-4f09-807e-a9b605d45bd0)
cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-03-05 13-30-48](https://github.com/user-attachments/assets/dfacf8c6-ed3a-431a-bbc6-b4f8e69077f7)
cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-03-05 13-31-54](https://github.com/user-attachments/assets/c8fedf0a-e81e-46cc-a803-c6d9b6b77bec)
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
![Screenshot from 2025-03-05 13-34-04](https://github.com/user-attachments/assets/fb820b23-f4ff-4278-b382-088042bd5b5d)
grep hello newfile 
## OUTPUT
![Screenshot from 2025-03-05 13-35-15](https://github.com/user-attachments/assets/271036cd-8467-43f8-b938-b8f3aa845025)
grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-03-05 13-36-09](https://github.com/user-attachments/assets/1b44791b-19f2-4a30-a5bf-af0c131259d9)
cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2025-03-05 13-37-11](https://github.com/user-attachments/assets/caccc3e4-8b53-4899-9034-25aa8e325c94)
cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2025-03-05 13-38-18](https://github.com/user-attachments/assets/f43d04f9-f073-4165-b6c5-f36487a4b464)
grep -R ubuntu /etc
## OUTPUT
grep -w -n world newfile   
## OUTPUT
![Screenshot from 2025-03-05 13-40-00](https://github.com/user-attachments/assets/e5e7dc3a-e7b1-4382-adc4-c42aeec98851)
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
![Screenshot from 2025-03-05 13-44-15](https://github.com/user-attachments/assets/139d40b7-1405-49e9-9dee-bff32762d2db)
egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2025-03-05 13-45-19](https://github.com/user-attachments/assets/b13e6626-859c-4b6e-9570-4abdf59dfb8e)
egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot from 2025-03-05 13-46-39](https://github.com/user-attachments/assets/174478d2-ff01-4f33-a393-9b7500bc37a2)
egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2025-03-05 13-47-45](https://github.com/user-attachments/assets/d5d733ae-c79c-4ec0-91cf-012bdf81a237)
egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2025-03-05 13-48-54](https://github.com/user-attachments/assets/079dbfd7-fbcc-40bc-9f7a-c088e7c34bf6)
egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-03-05 13-50-56](https://github.com/user-attachments/assets/aef33e43-653d-4638-af06-28d66d4510ba)
egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2025-03-05 13-52-32](https://github.com/user-attachments/assets/1fd5dcdb-f876-49d2-aba9-7714e82c248d)
egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2025-03-05 13-53-51](https://github.com/user-attachments/assets/e81a56d1-08c0-47fd-91c6-73c0391f8c95)
egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-03-05 13-54-53](https://github.com/user-attachments/assets/62835a24-0c23-4487-b477-4ff0cc5560dd)
egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2025-03-05 13-56-24](https://github.com/user-attachments/assets/c1e481e4-e534-46c8-a652-28ed158ba47b)
egrep l{2} newfile
## OUTPUT
![Screenshot from 2025-03-05 13-58-00](https://github.com/user-attachments/assets/be693841-c36e-4da5-9bb9-12f039e1debf)
egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2025-03-05 13-59-46](https://github.com/user-attachments/assets/0ea1b4d7-a006-4186-9eed-bdb7981dea99)
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
![Screenshot from 2025-03-05 14-05-49](https://github.com/user-attachments/assets/00d16168-b363-4bb2-a2cb-addc8e75b948)
sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2025-03-05 14-07-11](https://github.com/user-attachments/assets/b4fa9fe6-91e2-4e05-867e-e660aae1ad7a)
sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-03-05 14-09-02](https://github.com/user-attachments/assets/7a38d134-a31a-4678-a3aa-669890fe9b2a)
sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-03-05 14-09-58](https://github.com/user-attachments/assets/f112cfb8-3209-474c-9487-4cd7f4a5980a)
sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2025-03-05 14-12-56](https://github.com/user-attachments/assets/e609c55e-2d06-470d-ba03-af08b6a450b1)
sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2025-03-05 14-14-36](https://github.com/user-attachments/assets/0b944475-aa22-419f-ad65-81fa58aa0c63)
sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-03-05 14-15-59](https://github.com/user-attachments/assets/93d529c1-66ff-49a2-8cb9-295aa9bd70d9)
sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-03-05 14-16-58](https://github.com/user-attachments/assets/6487c8fb-18d7-401c-9d75-e25db48e39ff)
seq 10 
## OUTPUT
![Screenshot from 2025-03-05 14-17-48](https://github.com/user-attachments/assets/7c86a23c-0b5c-4f31-8137-bfdd0fcbd2e2)
seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2025-03-05 14-18-47](https://github.com/user-attachments/assets/4e7ebfef-4e2d-4c3a-bd77-ad1dde9fba20)
seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2025-03-05 14-19-55](https://github.com/user-attachments/assets/b60b8a51-c1c2-446e-834b-e1c8f510933c)
seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2025-03-05 14-26-01](https://github.com/user-attachments/assets/89eaaa54-8ca9-47ca-af28-095c9e6852b1)
seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2025-03-05 14-27-00](https://github.com/user-attachments/assets/bf89331f-eb04-4a87-a0f5-7afe85372380)
seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2025-03-05 14-28-22](https://github.com/user-attachments/assets/7237aa5c-4fb8-4bd1-a49d-00fc21ba23dd)
sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2025-03-05 14-29-33](https://github.com/user-attachments/assets/c079e75c-9658-44ca-8254-ad3b9d153da6)
sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![Screenshot from 2025-03-05 14-31-30](https://github.com/user-attachments/assets/39ec26f9-d218-4d3b-a75e-eb10d0c1d39d)
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
![Screenshot from 2025-03-05 14-36-56](https://github.com/user-attachments/assets/e62047c6-8f4d-4ba2-9d23-6a94c7b72d9f)
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

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2025-03-03 22-47-30](https://github.com/user-attachments/assets/694a47ae-c8db-4cfe-96dd-68f4ab4a40cb)

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
![Screenshot from 2025-03-05 22-31-15](https://github.com/user-attachments/assets/e22fd9fc-a249-427a-8192-157d0fef8abd)
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2025-03-05 22-32-46](https://github.com/user-attachments/assets/669ac3c1-03a4-4eb9-83b8-c139b73809b6)
#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2025-03-05 22-35-36](https://github.com/user-attachments/assets/03d1bc9e-5841-4e0d-8ad4-86302ab6f7f0)
mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot from 2025-03-05 22-38-48](https://github.com/user-attachments/assets/91f0d03f-a75e-4d96-b25a-c0c94b0b17b3)
tar -xvf backup.tar
## OUTPUT
![Screenshot from 2025-03-05 22-39-47](https://github.com/user-attachments/assets/09ff8a18-744b-4ef2-94eb-abe44390769c)
gzip backup.tar

ls .gz
## OUTPUT

gunzip backup.tar.gz
## OUTPUT
![Screenshot from 2025-03-03 23-20-01](https://github.com/user-attachments/assets/074c15f2-0069-45b0-9f45-e5a9ee44476e)
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot from 2025-03-03 23-36-59](https://github.com/user-attachments/assets/b4d05516-49ce-4886-8b3f-28e6b3909e4d)
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot from 2025-03-03 23-42-28](https://github.com/user-attachments/assets/2c939050-e867-4a6b-a703-356a1c5ba2b6)

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
![Screenshot from 2025-03-03 23-42-55](https://github.com/user-attachments/assets/d001da68-91dc-46f8-9570-c03198872d3f)
 
ls file1
## OUTPUT
![Screenshot from 2025-03-03 23-43-46](https://github.com/user-attachments/assets/6a2930ba-d2d7-4c2a-a19f-946b79a3ffe7)

echo $?
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![Screenshot from 2025-03-03 23-44-14](https://github.com/user-attachments/assets/1e3ebdc9-fd73-4605-a1e6-3b22efea658e)

abcd
 
echo $?
 ## OUTPUT
![Screenshot from 2025-03-03 23-45-50](https://github.com/user-attachments/assets/b398b761-ac02-4ee0-9584-7beef61c836e)
 
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
## OUTPUT
![Screenshot from 2025-03-04 07-03-03](https://github.com/user-attachments/assets/ef734e34-ffb8-450b-9fb5-be080d16b668)

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot from 2025-03-04 07-04-09](https://github.com/user-attachments/assets/3d40c376-b62a-4509-8e37-251112ce196b)

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
![Screenshot from 2025-03-04 07-04-37](https://github.com/user-attachments/assets/c784406b-8ed9-4170-8def-ae0cf761ea61)

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
![Screenshot from 2025-03-04 07-05-08](https://github.com/user-attachments/assets/dced86e7-f908-4bf0-bc62-31a962f39768)

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
![Screenshot from 2025-03-04 07-06-01](https://github.com/user-attachments/assets/21ed6570-0a73-43e1-a603-1d57ae35d84d)

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
## OUTPUT
![Screenshot from 2025-03-04 07-05-08](https://github.com/user-attachments/assets/96dbd86f-2d84-4a29-b150-1351d7562cbb)

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
![Screenshot from 2025-03-04 07-06-56](https://github.com/user-attachments/assets/b8af18a2-0fee-4a9e-abe5-ca9783b3c0ba)

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
![Screenshot from 2025-03-04 07-07-18](https://github.com/user-attachments/assets/1bf9f23c-0c4f-4465-8643-0cd14eb3ed40)

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
![Screenshot from 2025-03-04 07-07-56](https://github.com/user-attachments/assets/9b6c5a8a-f971-4ea7-8ca9-cfa0f072ba05)
 
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
![Screenshot from 2025-03-04 07-09-09](https://github.com/user-attachments/assets/da10184d-5849-467d-8eed-eea79528e38f)
 
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
![Screenshot from 2025-03-04 07-09-32](https://github.com/user-attachments/assets/10689530-bf0d-4769-ae77-b2a397ba03e5)

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
![Screenshot from 2025-03-04 07-10-27](https://github.com/user-attachments/assets/dd67b704-b925-483a-b84b-998bd22aae07)
 
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
![Screenshot from 2025-03-04 07-10-43](https://github.com/user-attachments/assets/b727d1d2-fb30-4f06-9e27-c45e1b545b45)
 
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
![Screenshot from 2025-03-04 07-10-54](https://github.com/user-attachments/assets/d427083d-9f92-469f-9b4c-c3d8bb7a0a07)
 
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
![Screenshot from 2025-03-04 07-11-11](https://github.com/user-attachments/assets/50a6da5d-dc0a-43b2-b452-8c7bab40d771)

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
![Screenshot from 2025-03-04 07-11-38](https://github.com/user-attachments/assets/962e7c74-ee51-4248-9f54-b67dd4cd581a)

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
![Screenshot from 2025-03-04 07-11-45](https://github.com/user-attachments/assets/6ded9d37-e5d5-4443-94ec-d7b91d7dc3dc)

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
![Screenshot from 2025-03-04 07-12-36](https://github.com/user-attachments/assets/fe190170-4be5-4d9a-83c7-7482d5233d56)

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
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
![Screenshot from 2025-03-04 07-12-53](https://github.com/user-attachments/assets/d4aa8975-c621-4a9d-8c54-cfb191aaca16)
 
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
![Screenshot from 2025-03-04 07-13-13](https://github.com/user-attachments/assets/5372f72d-88d4-45a4-b743-cb235d921fb9)
 
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
![Screenshot from 2025-03-04 07-13-37](https://github.com/user-attachments/assets/3b17d329-f3c0-4cb8-98d0-175aca201e3a)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![Screenshot from 2025-03-04 07-13-43](https://github.com/user-attachments/assets/9ff0629c-5c68-4f69-acc8-eb2e4567c11b)

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
./funcex.sh 
## OUTPUT
![Screenshot from 2025-03-04 07-13-58](https://github.com/user-attachments/assets/77526b0c-4e24-408f-8ed9-7b1ca276cf06)

./funcex.sh 1 2
## OUTPUT
![Screenshot from 2025-03-04 07-15-06](https://github.com/user-attachments/assets/05ca4f38-a1d5-4fcb-b1ac-94bad9368390)
 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

$ ./argshift.sh 1 2 3
 ## OUTPUT
 ![Screenshot from 2025-03-04 07-15-22](https://github.com/user-attachments/assets/e658bb89-b8f4-4dc0-ad23-42ca674f9ba9)

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
$ ./argshift.sh 1 2 3
## OUTPUT
![Screenshot from 2025-03-04 07-15-34](https://github.com/user-attachments/assets/d0eb1687-4806-466f-aaaf-3c69d9c3c299)

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
 ./argshift.sh 1 2 3
## OUTPUT 
![Screenshot from 2025-03-04 07-15-57](https://github.com/user-attachments/assets/f01707e3-fbfb-4a10-8014-5adc77aaa9cd)

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
![Screenshot from 2025-03-04 07-16-17](https://github.com/user-attachments/assets/993b0f58-1d6d-427e-9cc2-cc8e49cc5114)
 
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
![Screenshot from 2025-03-04 07-16-34](https://github.com/user-attachments/assets/a4dc5683-ce3e-400a-800b-cf0837369127)

# RESULT:
The Commands are executed successfully.
