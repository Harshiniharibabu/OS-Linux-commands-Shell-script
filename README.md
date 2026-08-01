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

<img width="802" height="155" alt="image" src="https://github.com/user-attachments/assets/4a8916ab-6a67-4b3f-acca-6bd2a012167c" />


cat < file2
## OUTPUT

<img width="851" height="182" alt="image" src="https://github.com/user-attachments/assets/086a344d-c8fb-42da-8be9-24c9e51e959d" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="1055" height="68" alt="image" src="https://github.com/user-attachments/assets/86a93e42-af50-4a93-8483-221f08b2e3a6" />
 
comm file1 file2
 ## OUTPUT

<img width="1224" height="224" alt="image" src="https://github.com/user-attachments/assets/937e992e-7ced-42ec-bb7b-0c29ecc760b4" />

 
diff file1 file2
## OUTPUT

<img width="602" height="274" alt="image" src="https://github.com/user-attachments/assets/9af55b92-a0cf-4877-aaea-f8bcf4d831ae" />


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


<img width="681" height="98" alt="image" src="https://github.com/user-attachments/assets/8f5a08b6-9ceb-4223-837d-e9a519c2ff3a" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="696" height="128" alt="image" src="https://github.com/user-attachments/assets/cab70fbb-7493-45ae-b1f2-9fbbb52ac681" />

cut -d "|" -f 2 file22
## OUTPUT

<img width="750" height="123" alt="image" src="https://github.com/user-attachments/assets/c12a0869-a78b-418e-8d63-507871bed090" />



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

<img width="592" height="73" alt="image" src="https://github.com/user-attachments/assets/50adc11b-c17e-4c79-8fdc-e78d663d379e" />


grep hello newfile 
## OUTPUT

<img width="672" height="76" alt="image" src="https://github.com/user-attachments/assets/35eca914-8ef6-4926-818a-eb7ecd87213c" />



grep -v hello newfile 
## OUTPUT

<img width="747" height="75" alt="image" src="https://github.com/user-attachments/assets/468369de-c45b-464a-a732-f140f4e63191" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="962" height="103" alt="image" src="https://github.com/user-attachments/assets/28e0aac9-1db5-422a-9ec0-0911f101f1f4" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="631" height="69" alt="image" src="https://github.com/user-attachments/assets/82b57c71-38fa-47dc-a03e-66e58e076774" />



grep -R ubuntu /etc
## OUTPUT

<img width="2164" height="727" alt="ChatGPT Image Jul 27, 2026, 02_13_00 PM" src="https://github.com/user-attachments/assets/31924747-6b5c-48bb-9c41-4a052520984e" />


grep -w -n world newfile   
## OUTPUT

<img width="617" height="108" alt="image" src="https://github.com/user-attachments/assets/e5560b59-d331-4f44-bae3-406c8a53ed0a" />


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

<img width="700" height="99" alt="image" src="https://github.com/user-attachments/assets/242e9bb5-3fa1-4e56-b480-d23d7c8c6c13" />

egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="1035" height="103" alt="image" src="https://github.com/user-attachments/assets/99f84206-de21-4ae3-9e40-e7c211101275" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="790" height="102" alt="image" src="https://github.com/user-attachments/assets/17c568e7-55a8-4332-b7a2-8c5708b7888f" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="892" height="80" alt="image" src="https://github.com/user-attachments/assets/423cb0b0-3191-4460-b379-07ff415a350a" />


egrep '(world$)' newfile 
## OUTPUT

<img width="1142" height="123" alt="image" src="https://github.com/user-attachments/assets/9af67513-65bc-40fb-8c73-714d3f75c62b" />


egrep '(World$)' newfile 
## OUTPUT

<img width="995" height="77" alt="image" src="https://github.com/user-attachments/assets/dc9969bd-27fb-4034-b162-89e6f1e71121" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="1003" height="126" alt="image" src="https://github.com/user-attachments/assets/eff93696-f19d-4e96-8039-e1a99ddee68a" />


egrep '[1-9]' newfile 
## OUTPUT


<img width="1090" height="78" alt="image" src="https://github.com/user-attachments/assets/50111380-fdda-482b-a5ce-8a12e029d565" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="1097" height="76" alt="image" src="https://github.com/user-attachments/assets/15a103c4-ffd5-4191-83e6-f63db932b751" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="1141" height="75" alt="image" src="https://github.com/user-attachments/assets/ced3f647-3013-4749-82f3-0ee7acd231e4" />


egrep l{2} newfile
## OUTPUT

<img width="892" height="109" alt="image" src="https://github.com/user-attachments/assets/4dbab1df-2d74-475a-865c-94a5a1c22427" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="936" height="129" alt="image" src="https://github.com/user-attachments/assets/13bc7b8d-b3ff-4c4a-b640-1d956d1b87b0" />


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

<img width="727" height="74" alt="image" src="https://github.com/user-attachments/assets/5fc3e895-c91a-46ce-8b9c-046e5f9f8717" />


sed -n -e '$p' file23
## OUTPUT

<img width="727" height="74" alt="image" src="https://github.com/user-attachments/assets/57173978-92ea-4dc0-be72-d462617750ed" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="837" height="252" alt="image" src="https://github.com/user-attachments/assets/273c33d2-7ffa-4492-9f38-44c1bf6dafe5" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="795" height="261" alt="image" src="https://github.com/user-attachments/assets/80159b48-7e42-4187-9071-f1b7439b0af5" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="758" height="257" alt="image" src="https://github.com/user-attachments/assets/a0613ab4-d882-4400-a25b-d241d45b3380" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="685" height="176" alt="image" src="https://github.com/user-attachments/assets/ee944924-5af4-4d6a-bbcb-14236c7d5ba7" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="766" height="130" alt="image" src="https://github.com/user-attachments/assets/913035a4-2447-4d68-abca-084109d19d0d" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="1019" height="106" alt="image" src="https://github.com/user-attachments/assets/f74d9b63-09cc-46fb-ac5d-6a241a881324" />


seq 10 
## OUTPUT

<img width="891" height="299" alt="image" src="https://github.com/user-attachments/assets/de249806-5ab2-4f37-8305-654e55b4a263" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="631" height="125" alt="image" src="https://github.com/user-attachments/assets/6dbe0b9d-6674-4c9f-a0a7-01f2e007b585" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="807" height="130" alt="image" src="https://github.com/user-attachments/assets/cb161ddb-b2a7-401b-8ccb-6bf97151890a" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="620" height="152" alt="image" src="https://github.com/user-attachments/assets/1c1ea885-0cc7-4413-ae14-f525c26258fc" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="700" height="129" alt="image" src="https://github.com/user-attachments/assets/a52669d7-ace5-4142-958d-cad0345b0df0" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="677" height="123" alt="image" src="https://github.com/user-attachments/assets/f949ae4d-41ac-47ad-b38d-c163336d1e06" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="672" height="128" alt="image" src="https://github.com/user-attachments/assets/346e7f9b-9b63-4fb3-859b-21b8c0f9fbf9" />


sed -n '2,4{s/$/*/;p}' file23

## OUTPUT

<img width="747" height="124" alt="image" src="https://github.com/user-attachments/assets/45a7bb7f-bad9-4e3d-8fad-5e2ca8ed7cc8" />


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

<img width="713" height="178" alt="image" src="https://github.com/user-attachments/assets/e0df9bcf-9484-409b-bb06-c34ba5fee0b3" />


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

<img width="848" height="175" alt="image" src="https://github.com/user-attachments/assets/5e21d657-c038-4a0e-accc-91e19957f889" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="843" height="199" alt="image" src="https://github.com/user-attachments/assets/51208e3b-7fb5-4e0b-a169-4b7726416e3a" />


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

<img width="583" height="130" alt="image" src="https://github.com/user-attachments/assets/2f70f581-6009-4664-807a-325d82d765fc" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="691" height="180" alt="image" src="https://github.com/user-attachments/assets/6e853f75-f975-4a73-858a-38f8af92ecd7" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="832" height="830" alt="image" src="https://github.com/user-attachments/assets/77d7241f-6416-4abe-ad33-52f9b6291bc3" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="1022" height="779" alt="image" src="https://github.com/user-attachments/assets/3354569b-a3e0-4005-b22d-d54565cab856" />


tar -xvf backup.tar
## OUTPUT

<img width="567" height="800" alt="image" src="https://github.com/user-attachments/assets/ab0e1c66-bd57-4926-9c52-ffa2dedd3360" />


gzip backup.tar

ls .gz
## OUTPUT


 <img width="1914" height="822" alt="ChatGPT Image Jul 28, 2026, 02_35_18 PM" src="https://github.com/user-attachments/assets/62d3c8a5-f867-4106-bfdb-ec2a13d34793" />


gunzip backup.tar.gz
## OUTPUT

<img width="1081" height="215" alt="image" src="https://github.com/user-attachments/assets/f46d4ece-8d0e-4203-a6ec-44a4f97f8756" />


# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="578" height="79" alt="image" src="https://github.com/user-attachments/assets/7bc8e809-1037-415c-9978-1ef2e2bfa9c2" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="651" height="176" alt="image" src="https://github.com/user-attachments/assets/f6de9337-1877-4d97-9026-a719c4b45b29" />


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

<img width="1056" height="402" alt="image" src="https://github.com/user-attachments/assets/2e1c8121-0556-4278-bbb9-51ddc90538c4" />

 
ls file1
## OUTPUT

<img width="632" height="124" alt="image" src="https://github.com/user-attachments/assets/9c2308e1-5b8d-4fba-a56e-27dcf2970b28" />


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 <img width="434" height="78" alt="image" src="https://github.com/user-attachments/assets/0c86f1b0-f8cb-428a-b548-8aa3b7374a47" />


abcd
 
echo $?
 ## OUTPUT

<img width="574" height="75" alt="image" src="https://github.com/user-attachments/assets/22de120f-4a7f-4ef2-aa21-a79092461d0c" />

 
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

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="737" height="181" alt="image" src="https://github.com/user-attachments/assets/14e0f9e0-fee2-49ef-a40d-f3b608fd3843" />




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

<img width="623" height="121" alt="image" src="https://github.com/user-attachments/assets/ac6e6559-0f22-49a2-8eae-ae6deded0b42" />


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

<img width="682" height="148" alt="image" src="https://github.com/user-attachments/assets/42a7fd92-6d57-4d45-a958-c2f008393bef" />


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

<img width="686" height="129" alt="image" src="https://github.com/user-attachments/assets/96cab7bc-7c09-4cff-99c8-1e3c360fc6d1" />



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

<img width="686" height="156" alt="image" src="https://github.com/user-attachments/assets/d86a702f-dc61-4d5c-ab65-fefc3191b2be" />



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

<img width="700" height="176" alt="image" src="https://github.com/user-attachments/assets/6e865ba4-f685-4217-a00c-c28fcb77b08f" />



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

<img width="666" height="144" alt="image" src="https://github.com/user-attachments/assets/9a289b41-6178-4074-b2a8-17bdc3c291c5" />



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

## OUTPUT

<img width="692" height="449" alt="image" src="https://github.com/user-attachments/assets/2d6ee3c5-7d7f-42f2-be2d-cde6e7f536c5" />


 
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

## OUTPUT

<img width="600" height="395" alt="image" src="https://github.com/user-attachments/assets/f5394751-d49e-4366-a903-16c6253eb0ac" />

 
 
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

## OUTPUT

<img width="565" height="202" alt="image" src="https://github.com/user-attachments/assets/db32ffe0-312f-4463-8efd-e83ce2ad8731" />

 
 
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

 ## OUTPUT


<img width="566" height="236" alt="Screenshot 2026-08-01 223926" src="https://github.com/user-attachments/assets/289b219b-1881-4575-b031-12bed701b226" />

 
 
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

 ## OUTPUT

<img width="585" height="124" alt="image" src="https://github.com/user-attachments/assets/71341864-53da-4a2f-8f7e-e6317023aec0" />

 
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

## OUTPUT

<img width="676" height="244" alt="image" src="https://github.com/user-attachments/assets/8eaa8f37-7393-4c7d-86e3-751a40f87d7a" />


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

<img width="666" height="223" alt="image" src="https://github.com/user-attachments/assets/0b81ee9d-09b2-4eb4-af90-350d45a9cc9d" />



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

<img width="655" height="270" alt="image" src="https://github.com/user-attachments/assets/83ecb90f-9cff-4a76-95f5-9e6a83d88c01" />


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

 <img width="699" height="445" alt="image" src="https://github.com/user-attachments/assets/15d38b18-c55d-4838-8089-76cbacac143b" />


 
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

<img width="595" height="138" alt="image" src="https://github.com/user-attachments/assets/0905ba25-3186-4dca-9313-30b346d05800" />


 
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

<img width="636" height="191" alt="image" src="https://github.com/user-attachments/assets/5adec8d2-e4ec-4c82-8f1c-1360c4699a17" />


 
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

<img width="670" height="147" alt="image" src="https://github.com/user-attachments/assets/e3b5dbdd-7dd2-4c21-84ee-7dedd794205d" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT


<img width="1944" height="809" alt="ChatGPT Image Aug 1, 2026, 11_01_42 PM" src="https://github.com/user-attachments/assets/c9f3ddeb-fbc7-473d-9e01-cb6f761cb57b" />


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

 
 ./funcex.sh 1 2

## OUTPUT


<img width="1622" height="969" alt="ChatGPT Image Aug 1, 2026, 10_57_33 PM" src="https://github.com/user-attachments/assets/237dc7af-4e5b-4f84-b16d-a37e66acafe7" />

 
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

<img width="536" height="120" alt="image" src="https://github.com/user-attachments/assets/4f136680-264f-4b35-9754-0ecb55dfe6b7" />

 
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

<img width="675" height="165" alt="image" src="https://github.com/user-attachments/assets/cb17e80b-d4cb-43d5-99f7-95f2e51ddf1c" />

 
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

<img width="1337" height="1177" alt="ChatGPT Image Aug 1, 2026, 11_06_33 PM" src="https://github.com/user-attachments/assets/d68be73f-78f5-48ad-bfbb-2283ebdaf082" />

 
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

<img width="963" height="481" alt="image" src="https://github.com/user-attachments/assets/fb472fdb-a070-409e-9da6-e461763e4774" />

 
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


<img width="675" height="224" alt="image" src="https://github.com/user-attachments/assets/d89b9d40-af45-4ad4-8829-d6175b9949d8" />


# RESULT:
The Commands are executed successfully.
