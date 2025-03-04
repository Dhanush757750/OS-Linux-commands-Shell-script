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
![Screenshot from 2025-03-03 18-27-30](https://github.com/user-attachments/assets/3a845d13-a792-4837-937a-3c59bfb8339d)

cat < file2
## OUTPUT
![Screenshot from 2025-03-03 18-28-12](https://github.com/user-attachments/assets/823b03c3-b0bc-4669-acb3-8d34fae33c1a)

# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot from 2025-03-03 18-28-47](https://github.com/user-attachments/assets/165a5693-3ceb-4d64-8a75-58dabfcc173c)

comm file1 file2
## OUTPUT
![Screenshot from 2025-03-03 18-29-18](https://github.com/user-attachments/assets/fbcc11a2-2bd7-4f42-ad47-6f847cea86d9)
 
diff file1 file2
## OUTPUT
![Screenshot from 2025-03-03 18-29-43](https://github.com/user-attachments/assets/b7cb95ed-226c-4645-abd8-a840235f31ec)

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
![Screenshot from 2025-03-03 18-32-11](https://github.com/user-attachments/assets/6cfb9f10-4ca0-4925-9271-81518107d7c2)

cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-03-03 18-33-16](https://github.com/user-attachments/assets/40fb4eda-28cb-465f-8b2f-0a018abb4a17)

cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-03-03 18-33-46](https://github.com/user-attachments/assets/24c0acb2-2633-4622-bbb5-8d40b28bb86d)

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
![Screenshot from 2025-03-03 18-40-29](https://github.com/user-attachments/assets/cfb2dd2b-d081-4ac3-b20a-6edea170c463)

grep hello newfile 
## OUTPUT
![Screenshot from 2025-03-03 18-40-54](https://github.com/user-attachments/assets/cb089f59-ec9b-4552-88f4-10437662957f)

grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-03-03 18-41-27](https://github.com/user-attachments/assets/f0deba70-fa6a-4071-840a-64f04e4cd769)

cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2025-03-03 18-42-13](https://github.com/user-attachments/assets/1cfbbc01-126c-4ed0-b0d3-c2dce9f84829)

cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2025-03-03 18-42-58](https://github.com/user-attachments/assets/a8267c2e-0489-4167-bc99-31a92a7aeae1)

grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2025-03-03 18-44-53](https://github.com/user-attachments/assets/eeb3a7ba-ea5d-47f2-baf7-dd0384b51765)

grep -w -n world newfile   
## OUTPUT
![Screenshot from 2025-03-03 18-45-54](https://github.com/user-attachments/assets/cd777aec-c89e-42f3-a9c7-35926410051c)

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
![Screenshot from 2025-03-03 18-50-28](https://github.com/user-attachments/assets/7f1052a2-e127-4798-a713-f5993278a63a)

egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2025-03-03 18-51-19](https://github.com/user-attachments/assets/0e12d613-8ca5-4c00-8668-7f812809ec67)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot from 2025-03-03 18-52-09](https://github.com/user-attachments/assets/3fdc9d9f-0fb9-4980-9bf5-90513b44a28f)

egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2025-03-03 18-52-45](https://github.com/user-attachments/assets/de6e6baf-a3f2-4291-8794-cee493db5e3f)

egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2025-03-03 18-53-27](https://github.com/user-attachments/assets/beaef0c6-c8bd-41b3-a050-d608baf7be66)

egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-03-03 20-59-06](https://github.com/user-attachments/assets/adc415e3-9f4c-4914-b745-6564379ad7b5)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2025-03-03 20-59-54](https://github.com/user-attachments/assets/5e936b29-7eb5-4bcf-b588-28900ba77397)

egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2025-03-03 22-00-48](https://github.com/user-attachments/assets/025f5558-dde0-4bb1-b77b-5b9783cb17fd)

egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-03-03 22-16-48](https://github.com/user-attachments/assets/7d31d2d4-12ab-4507-9f84-2107a6f9731a)

egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2025-03-03 22-17-38](https://github.com/user-attachments/assets/788c1dea-fb71-4564-b8bc-ea361d5b78ca)

egrep l{2} newfile
## OUTPUT
![Screenshot from 2025-03-03 22-18-57](https://github.com/user-attachments/assets/0710b9df-12a6-4588-814b-489c6fbec2ec)

egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2025-03-03 22-19-59](https://github.com/user-attachments/assets/293f351a-6be5-4914-b052-45622aa711c1)

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
![Screenshot from 2025-03-03 22-26-52](https://github.com/user-attachments/assets/b70709aa-288a-481f-8961-c4939a855f6a)

sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2025-03-03 22-28-52](https://github.com/user-attachments/assets/1ecaf6c2-2f13-4765-8fb5-18a1773fac3d)

sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-03-03 22-30-30](https://github.com/user-attachments/assets/8babd838-c109-4d0d-bfbf-f55c29c71894)

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-03-03 22-31-40](https://github.com/user-attachments/assets/1314d706-4871-4807-ae07-c2831c229743)

sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2025-03-03 22-32-44](https://github.com/user-attachments/assets/60ad468a-a28c-46a4-ba21-608af3f2c88a)

sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2025-03-03 22-33-49](https://github.com/user-attachments/assets/c4729540-b1f9-4232-90bd-a95b38d01cfe)

sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-03-04 08-46-24](https://github.com/user-attachments/assets/077d2aa7-2ebb-4dbe-91d6-6e4b1851b9a2)

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-03-03 22-33-49](https://github.com/user-attachments/assets/ff721fa2-ef3b-476e-bc3c-02870181456c)

seq 10 
## OUTPUT
![Screenshot from 2025-03-03 22-35-52](https://github.com/user-attachments/assets/0b83d838-fc15-4eec-bbcd-65d3edae54a8)

seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2025-03-03 22-36-33](https://github.com/user-attachments/assets/e5fb56f5-8ae2-4b29-acdf-6543007ef9dc)

seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2025-03-03 22-37-07](https://github.com/user-attachments/assets/d4db8310-1271-405a-a716-7fa55a6b9117)

seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2025-03-03 22-37-38](https://github.com/user-attachments/assets/2954145d-f924-477c-adcb-8b1559eed66d)

seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2025-03-03 22-38-02](https://github.com/user-attachments/assets/5c2c53df-b5e0-4cb0-b604-04ea98cde5db)

seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2025-03-03 22-38-36](https://github.com/user-attachments/assets/cd1107fe-0cde-4e6a-8beb-064a79750a42)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2025-03-03 22-39-45](https://github.com/user-attachments/assets/d85d436a-2c76-4500-b2a4-4e24d131959e)

sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![Screenshot from 2025-03-03 22-40-29](https://github.com/user-attachments/assets/79e7e98e-d99b-41c3-aebd-a1138c5ba3dc)

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
![Screenshot from 2025-03-03 22-43-46](https://github.com/user-attachments/assets/8ebc3095-3592-4030-b63b-6364911ca732)

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
![Screenshot from 2025-03-03 22-46-13](https://github.com/user-attachments/assets/9529c55c-8f84-440d-a50d-d2a4b1656ef8)

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
![Screenshot from 2025-03-03 22-54-40](https://github.com/user-attachments/assets/28307b51-7c1c-49cd-bd67-daaa81fb36e0)
 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2025-03-03 22-56-51](https://github.com/user-attachments/assets/aca018a8-c5a6-4df2-8c9d-7c25bfca80c3)

#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2025-03-03 23-01-49](https://github.com/user-attachments/assets/814cb374-e13c-4c48-a0ac-49967958d542)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot from 2025-03-03 23-11-15](https://github.com/user-attachments/assets/abb58563-82db-4fef-9805-13e2b2c1b1f6)

tar -xvf backup.tar
## OUTPUT
![Screenshot from 2025-03-03 23-11-33](https://github.com/user-attachments/assets/210ab4c1-6238-4e51-89fb-a6defc2367f8)

gzip backup.tar

ls .gz
## OUTPUT
![Screenshot from 2025-03-03 23-12-01](https://github.com/user-attachments/assets/ea46d27a-6795-410b-a40c-181c635dfc7b)

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
