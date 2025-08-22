<img width="863" height="157" alt="Screenshot from 2025-08-19 20-54-56" src="https://github.com/user-attachments/assets/f813d211-bfb1-47ab-931b-b255616473aa" />## OS-Linux-commands-Shell-scripting
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
<img width="578" height="100" alt="Screenshot from 2025-08-15 12-43-00" src="https://github.com/user-attachments/assets/9d0842be-dd75-4d7e-9cf4-cc3bd3faf861" />



cat < file2
## OUTPUT
<img width="578" height="118" alt="Screenshot from 2025-08-15 12-43-20" src="https://github.com/user-attachments/assets/00e462b8-ad2d-48a7-8cde-bd93780f3f65" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="578" height="42" alt="Screenshot from 2025-08-15 12-43-35" src="https://github.com/user-attachments/assets/fe345edd-f6fa-4ef0-b317-6bbcaa4943b7" />


comm file1 file2
 ## OUTPUT
<img width="527" height="167" alt="Screenshot from 2025-08-15 12-47-07" src="https://github.com/user-attachments/assets/200473f6-a04e-42ea-ad4b-1c8474940406" />

 
diff file1 file2
## OUTPUT
<img width="527" height="181" alt="Screenshot from 2025-08-15 12-47-49" src="https://github.com/user-attachments/assets/9dd2b856-e57d-4a0a-968f-9584479299d5" />


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
<img width="527" height="58" alt="Screenshot from 2025-08-15 13-02-15" src="https://github.com/user-attachments/assets/e3e1201c-8be4-4d2e-bebc-06049c01f279" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="553" height="78" alt="Screenshot from 2025-08-15 13-02-45" src="https://github.com/user-attachments/assets/4e73c07c-2ab1-4f10-b30a-5428eb4b62ef" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="553" height="78" alt="Screenshot from 2025-08-15 13-02-53" src="https://github.com/user-attachments/assets/5b4749e1-81b4-4258-a9c4-a2464f4f600c" />


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
<img width="553" height="42" alt="Screenshot from 2025-08-15 13-06-55" src="https://github.com/user-attachments/assets/203f0225-2817-43a3-9b22-1896c562ca6c" />



grep hello newfile 
## OUTPUT
<img width="553" height="42" alt="Screenshot from 2025-08-15 13-07-02" src="https://github.com/user-attachments/assets/a1584b8c-d453-4c08-96a5-57f24fb91cca" />




grep -v hello newfile 
## OUTPUT
<img width="553" height="42" alt="Screenshot from 2025-08-15 13-07-11" src="https://github.com/user-attachments/assets/ddcc76d1-618c-4723-94c5-b2e60d4ebfa1" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="613" height="63" alt="Screenshot from 2025-08-15 13-07-44" src="https://github.com/user-attachments/assets/97925125-db2d-4529-9031-cd3291a88d06" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="643" height="39" alt="Screenshot from 2025-08-15 13-07-59" src="https://github.com/user-attachments/assets/d7c0d880-fb8d-45f8-a562-23caac3d2546" />




grep -R ubuntu /etc
## OUTPUT
<img width="920" height="326" alt="Screenshot from 2025-08-15 13-10-17" src="https://github.com/user-attachments/assets/70f9e940-d982-43e7-8cdb-4978bd629b40" />



grep -w -n world newfile   
## OUTPUT
<img width="610" height="57" alt="Screenshot from 2025-08-15 13-10-58" src="https://github.com/user-attachments/assets/8e076f17-c02e-4fec-848e-17c7aa7c6d46" />


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
<img width="627" height="63" alt="Screenshot from 2025-08-18 11-31-41" src="https://github.com/user-attachments/assets/879359d9-2bbd-4c50-a8f5-d1d780122887" />



egrep -w '(H|h)ello' newfile 
## OUTPUT



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="643" height="60" alt="Screenshot from 2025-08-18 11-31-57" src="https://github.com/user-attachments/assets/cbc36843-788c-4c2c-9bc7-ef98786a41a0" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="643" height="47" alt="Screenshot from 2025-08-18 11-32-05" src="https://github.com/user-attachments/assets/084a1c44-fd83-4478-b05e-8b764badb1d2" />



egrep '(world$)' newfile 
## OUTPUT

<img width="643" height="59" alt="Screenshot from 2025-08-18 11-32-16" src="https://github.com/user-attachments/assets/2477b62a-c626-4348-88cf-92c9198c0af0" />


egrep '(World$)' newfile 
## OUTPUT
<img width="643" height="42" alt="Screenshot from 2025-08-18 11-32-24" src="https://github.com/user-attachments/assets/204f5dcb-f487-4266-88a2-ebae273800b7" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="643" height="76" alt="Screenshot from 2025-08-18 11-32-32" src="https://github.com/user-attachments/assets/b79838b0-8c41-480c-a144-59c69f97351e" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="643" height="47" alt="Screenshot from 2025-08-18 11-32-45" src="https://github.com/user-attachments/assets/9b8ee160-801b-408c-9814-61a7f98e1cce" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="643" height="45" alt="Screenshot from 2025-08-18 11-32-55" src="https://github.com/user-attachments/assets/c8cfa7b5-a90a-41c1-9cc5-f4c4344da76c" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="643" height="45" alt="Screenshot from 2025-08-18 11-33-01" src="https://github.com/user-attachments/assets/4d783e1a-cc75-486d-8b9c-b80721f29908" />


egrep l{2} newfile
## OUTPUT

<img width="643" height="57" alt="Screenshot from 2025-08-18 11-33-09" src="https://github.com/user-attachments/assets/fd3092b0-0da8-42aa-8388-b5a0d955e9f2" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="643" height="75" alt="Screenshot from 2025-08-18 11-33-16" src="https://github.com/user-attachments/assets/17bacc15-d7c9-4749-b5b0-a35b192d9101" />

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
<img width="643" height="46" alt="Screenshot from 2025-08-18 11-45-45" src="https://github.com/user-attachments/assets/b452adb4-f5dd-4517-94e2-f2d483b4b8ec" />



sed -n -e '$p' file23
## OUTPUT
<img width="643" height="39" alt="Screenshot from 2025-08-18 11-45-54" src="https://github.com/user-attachments/assets/f16fea85-b26d-4b58-8268-410e08c44303" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="643" height="169" alt="Screenshot from 2025-08-18 11-46-01" src="https://github.com/user-attachments/assets/c6fb0260-1ef6-406b-bb27-957369c43caa" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="643" height="169" alt="Screenshot from 2025-08-18 11-46-10" src="https://github.com/user-attachments/assets/ac9ecc02-7213-4d0c-bdd3-9f122cd8a255" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="643" height="169" alt="Screenshot from 2025-08-18 11-46-16" src="https://github.com/user-attachments/assets/4e3da0a1-ad1f-4dee-bd39-323ecae327dc" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="643" height="113" alt="Screenshot from 2025-08-18 11-46-26" src="https://github.com/user-attachments/assets/564c2ed2-d867-46d2-b8e9-3a6a0b1ff4e1" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="643" height="77" alt="Screenshot from 2025-08-18 11-47-09" src="https://github.com/user-attachments/assets/479639d4-4232-4a5d-b0d4-cd590374c78d" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="643" height="60" alt="Screenshot from 2025-08-18 11-47-20" src="https://github.com/user-attachments/assets/97325966-b216-4e31-94af-847d2525882d" />



seq 10 
## OUTPUT

<img width="643" height="203" alt="Screenshot from 2025-08-18 11-47-28" src="https://github.com/user-attachments/assets/f71292b4-5a27-4b4f-81a5-60ee9bc82713" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="643" height="75" alt="Screenshot from 2025-08-18 11-47-40" src="https://github.com/user-attachments/assets/79f32a69-a347-4cdd-a0fb-e90bc501bafa" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="643" height="75" alt="Screenshot from 2025-08-18 11-48-02" src="https://github.com/user-attachments/assets/92576aea-ff42-4b6b-b7a5-503f01b3954c" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="643" height="94" alt="Screenshot from 2025-08-18 11-48-13" src="https://github.com/user-attachments/assets/cf0e81f1-a1aa-4cbe-b014-a4f0d2c1791a" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="643" height="83" alt="Screenshot from 2025-08-18 11-48-20" src="https://github.com/user-attachments/assets/1417b1e8-e264-4da7-8b42-259764e81476" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="643" height="80" alt="Screenshot from 2025-08-18 11-48-26" src="https://github.com/user-attachments/assets/964b8327-8046-4767-8f2b-2e7d4779770a" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="643" height="90" alt="Screenshot from 2025-08-18 11-48-38" src="https://github.com/user-attachments/assets/d88c5c3b-23f4-4dcb-b88f-f1a648c11161" />


sed -n '2,4{s/$/*/;p}' file23

<img width="643" height="77" alt="Screenshot from 2025-08-18 11-48-49" src="https://github.com/user-attachments/assets/d5b1358a-4c04-4978-9016-9934ed02ea47" />

## Sorting File content
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

<img width="643" height="93" alt="Screenshot from 2025-08-18 11-51-45" src="https://github.com/user-attachments/assets/c4856833-66a4-4afb-a052-3d98e163852a" />

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
<img width="643" height="115" alt="Screenshot from 2025-08-18 11-51-56" src="https://github.com/user-attachments/assets/357171d6-973a-470a-a4b2-c2a005ae8c10" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="677" height="166" alt="Screenshot from 2025-08-18 11-52-07" src="https://github.com/user-attachments/assets/6cdd5f6b-b715-45b8-b200-5eba4fd06d5c" />


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
<img width="677" height="85" alt="Screenshot from 2025-08-18 11-53-43" src="https://github.com/user-attachments/assets/acce5e14-8348-498a-9a50-7a8894b8b38e" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="728" height="79" alt="Screenshot from 2025-08-18 11-55-31" src="https://github.com/user-attachments/assets/75fc8043-d5d0-4336-891b-a2350c634579" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="863" height="157" alt="Screenshot from 2025-08-19 20-54-56" src="https://github.com/user-attachments/assets/1efaf374-3d44-4136-95f9-45cb40eec453" />



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


<img width="844" height="204" alt="Screenshot from 2025-08-19 21-03-08" src="https://github.com/user-attachments/assets/d010d304-fec1-41ab-8b3a-aa9fad9e6a34" />


tar -xvf backup.tar
## OUTPUT

<img width="518" height="200" alt="Screenshot from 2025-08-19 21-07-33" src="https://github.com/user-attachments/assets/55eee3f5-7a66-48ca-ba6f-58675c626168" />

gzip backup.tar

ls .gz
## OUTPUT

 <img width="518" height="44" alt="Screenshot from 2025-08-19 21-08-54" src="https://github.com/user-attachments/assets/57dc30dc-3842-41b4-8b67-4db9d9a63fdf" />

gunzip backup.tar.gz
## OUTPUT

<img width="704" height="308" alt="Screenshot from 2025-08-19 21-10-00" src="https://github.com/user-attachments/assets/ee05aa3b-86a9-49a8-92b8-e6100066d6b2" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="529" height="48" alt="Screenshot from 2025-08-19 21-16-59" src="https://github.com/user-attachments/assets/fbade7d9-5448-48be-b90a-429bae6748d0" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="532" height="63" alt="Screenshot from 2025-08-19 21-20-55" src="https://github.com/user-attachments/assets/0803df7b-df72-419d-bba4-7b2ce295e28a" />


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
<img width="571" height="345" alt="Screenshot from 2025-08-19 21-24-36" src="https://github.com/user-attachments/assets/9c1fc6cc-e14c-4d6f-b1a8-0f18f3cac7af" />

 
ls file1
## OUTPUT
<img width="571" height="49" alt="Screenshot from 2025-08-19 21-26-06" src="https://github.com/user-attachments/assets/2d8527f6-4321-4c6c-9e17-2ed7da053d1e" />

echo $?

## OUTPUT
<img width="571" height="43" alt="Screenshot from 2025-08-19 21-26-20" src="https://github.com/user-attachments/assets/6644972f-385c-4bbb-9ee8-454169b43af6" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="571" height="43" alt="Screenshot from 2025-08-19 21-27-19" src="https://github.com/user-attachments/assets/b43ba01e-998d-4a01-8414-7c395febbe03" />

 
abcd
 
echo $?
 ## OUTPUT

<img width="571" height="43" alt="Screenshot from 2025-08-19 21-27-51" src="https://github.com/user-attachments/assets/4517a19b-a02d-422a-a458-5dc6787d424f" />

 
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
<img width="571" height="62" alt="Screenshot from 2025-08-19 21-31-19" src="https://github.com/user-attachments/assets/31ff086a-1214-4e2d-a14d-35c159f2a7e6" />



chmod 755 strcomp.sh
 
./strcomp.sh 

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
<img width="564" height="155" alt="Screenshot from 2025-08-20 13-57-26" src="https://github.com/user-attachments/assets/19a1fe31-ad1c-476f-bb48-bf68d176d019" />


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
<img width="812" height="114" alt="Screenshot from 2025-08-21 15-56-08" src="https://github.com/user-attachments/assets/04633a17-fb38-422f-ac58-0bc7c72cea1c" />

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
<img width="812" height="79" alt="Screenshot from 2025-08-21 15-57-28" src="https://github.com/user-attachments/assets/b6bee413-cfde-4bf1-9088-d5b85b75822d" />


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
<img width="812" height="79" alt="Screenshot from 2025-08-21 15-58-26" src="https://github.com/user-attachments/assets/16ea1424-d569-4d3c-bd27-494a9572a678" />

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
## output

 <img width="728" height="79" alt="Screenshot from 2025-08-21 16-00-11" src="https://github.com/user-attachments/assets/e021f185-1e5e-40f5-9aa9-58848edf8b23" />

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
 ## output
 <img width="595" height="133" alt="Screenshot from 2025-08-21 16-02-54" src="https://github.com/user-attachments/assets/4a5bbf4c-8903-4141-b8b6-e1e455470f1d" />

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
 ## output
 <img width="595" height="133" alt="Screenshot from 2025-08-21 16-04-01" src="https://github.com/user-attachments/assets/f7c9c25b-f0e4-4652-ac77-fb1173abe43c" />

 
 
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

 ## output
<img width="595" height="129" alt="Screenshot from 2025-08-21 16-06-38" src="https://github.com/user-attachments/assets/c39207c3-285d-4ca8-ad0a-5f45ff4f12ea" />


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
 ## output
 <img width="595" height="183" alt="Screenshot from 2025-08-21 16-08-24" src="https://github.com/user-attachments/assets/7f0ddea9-9dc6-46fb-b7ce-2c9e82558847" />

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
![Uploading Screenshot from 2025-08-21 16-05-17.png…]()

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
<img width="595" height="133" alt="Screenshot from 2025-08-21 16-10-31" src="https://github.com/user-attachments/assets/c2b61b4a-c7f7-4c72-a14a-d5b17a5331ee" />

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
<img width="595" height="133" alt="Screenshot from 2025-08-21 16-12-08" src="https://github.com/user-attachments/assets/dc69236d-e4f6-4765-80ce-856518344798" />


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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

 ## OUTPUT
 <img width="595" height="133" alt="Screenshot from 2025-08-21 16-15-27" src="https://github.com/user-attachments/assets/97766d3d-75f0-4e70-8c0b-4cedab8048c4" />


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
<img width="595" height="78" alt="Screenshot from 2025-08-21 16-16-30" src="https://github.com/user-attachments/assets/98f7d65c-9a1f-49e2-b927-704aaa134b4f" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="595" height="59" alt="Screenshot from 2025-08-21 16-18-14" src="https://github.com/user-attachments/assets/970c95cb-60f4-459c-b29d-8a0716f7ea0c" />



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

<img width="595" height="59" alt="Screenshot from 2025-08-21 16-19-05" src="https://github.com/user-attachments/assets/c9b7ba9c-8ba7-4e2e-8fce-f6cf5e0c02c7" />

 
 ./funcex.sh 1 2

<img width="595" height="41" alt="Screenshot from 2025-08-21 16-19-26" src="https://github.com/user-attachments/assets/b6510fd7-f06a-4fda-b8fb-8d1f0c1f54bd" />

 
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


<img width="595" height="76" alt="Screenshot from 2025-08-21 16-20-23" src="https://github.com/user-attachments/assets/2bfde4f7-b7d6-477d-9336-13ec8d98bdd2" />

 
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

<img width="595" height="76" alt="Screenshot from 2025-08-21 16-21-05" src="https://github.com/user-attachments/assets/bdcd5b8a-b0c0-4665-b99b-049c67e571ab" />

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

 <img width="595" height="291" alt="Screenshot from 2025-08-21 16-21-47" src="https://github.com/user-attachments/assets/b1331efe-f6d5-46ae-9503-8e3f68348deb" />

 
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

 <img width="559" height="281" alt="Screenshot from 2025-08-21 22-42-43" src="https://github.com/user-attachments/assets/7f2adff0-f978-4f38-8baa-f548f21385c8" />

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

<img width="599" height="112" alt="Screenshot from 2025-08-21 22-44-13" src="https://github.com/user-attachments/assets/f8c954dc-f442-4840-95b5-4cd8908e2c18" />


# RESULT:
The Commands are executed successfully.
