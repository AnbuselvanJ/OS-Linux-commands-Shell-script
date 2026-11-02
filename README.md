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
<img width="270" height="147" alt="image" src="https://github.com/user-attachments/assets/0906ae85-4fdb-417d-9573-f889afb186be" />



cat < file2
## OUTPUT
<img width="262" height="173" alt="image" src="https://github.com/user-attachments/assets/dea02f42-0343-4412-9e91-a0193888ce40" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="277" height="52" alt="image" src="https://github.com/user-attachments/assets/a1d2c258-61ef-4c8f-ba6c-9589ace96a4e" />

comm file1 file2
 ## OUTPUT
<img width="391" height="302" alt="image" src="https://github.com/user-attachments/assets/baaa747f-4a95-4746-9433-9178920ec930" />

 
diff file1 file2
## OUTPUT
<img width="317" height="272" alt="image" src="https://github.com/user-attachments/assets/75444cfb-2ab5-4a1c-81fd-c5771bfe7211" />


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

<img width="286" height="103" alt="image" src="https://github.com/user-attachments/assets/fcd27b8c-72b5-44fb-a04d-a34d46ded860" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="297" height="127" alt="image" src="https://github.com/user-attachments/assets/b42b07f4-9e9d-4c0e-b9a7-8abd2d1ac8dc" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="300" height="123" alt="image" src="https://github.com/user-attachments/assets/ee82f65c-a56d-4596-b858-cf8290f4022b" />


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

<img width="265" height="81" alt="image" src="https://github.com/user-attachments/assets/d667c8d3-3bde-4570-8e2f-e8678f4179c2" />


grep hello newfile 
## OUTPUT

<img width="267" height="73" alt="image" src="https://github.com/user-attachments/assets/e5d7c112-bffe-4177-932e-671e7486e8dd" />



grep -v hello newfile 
## OUTPUT



cat newfile | grep -i "hello"
## OUTPUT


<img width="363" height="102" alt="image" src="https://github.com/user-attachments/assets/1b743186-0bc1-4eef-b59a-d3154df93b9d" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="392" height="76" alt="image" src="https://github.com/user-attachments/assets/40682f1b-3012-41f0-81e9-08dc06df402a" />



grep -R ubuntu /etc
## OUTPUT

<img width="808" height="370" alt="image" src="https://github.com/user-attachments/assets/dd9dcf8a-d628-4970-b3f5-d4ab1daf4859" />


grep -w -n world newfile   
## OUTPUT
<img width="320" height="105" alt="image" src="https://github.com/user-attachments/assets/307ddc0d-8f2c-4261-b938-a7245c653bae" />


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

<img width="398" height="102" alt="image" src="https://github.com/user-attachments/assets/7c3992cb-3de2-4a36-a1ce-757107f86287" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="366" height="105" alt="image" src="https://github.com/user-attachments/assets/a7251a25-0fc5-42d9-b975-bf449b42aa51" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="408" height="103" alt="image" src="https://github.com/user-attachments/assets/045862c2-b4b6-4494-a37f-b00eca3c1758" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="338" height="81" alt="image" src="https://github.com/user-attachments/assets/e0337056-74bf-4518-85c8-31a25fb4cc40" />


egrep '(world$)' newfile 
## OUTPUT

<img width="337" height="103" alt="image" src="https://github.com/user-attachments/assets/c5a8fdf4-5fc8-4962-b299-248d2e5048d7" />


egrep '(World$)' newfile 
## OUTPUT
<img width="340" height="81" alt="image" src="https://github.com/user-attachments/assets/9a589928-ac17-453a-b775-32eeb4aae97e" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="381" height="132" alt="image" src="https://github.com/user-attachments/assets/b81c35b9-25c8-4eea-a65f-4706eef1276a" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="297" height="76" alt="image" src="https://github.com/user-attachments/assets/d159a16f-ca4b-4a33-b9b1-f6009a910781" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="373" height="77" alt="image" src="https://github.com/user-attachments/assets/2a6234a5-92bd-441b-a10b-8440490f69a7" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="373" height="77" alt="image" src="https://github.com/user-attachments/assets/cc88979a-6d5f-4b86-afe5-15ed6aef9ac7" />


egrep l{2} newfile
## OUTPUT

<img width="287" height="108" alt="image" src="https://github.com/user-attachments/assets/717cbf4d-6e59-438e-ad54-9d9c43922836" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="347" height="125" alt="image" src="https://github.com/user-attachments/assets/652d18dd-21bb-4881-9e8b-7503937a44bc" />

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

<img width="307" height="77" alt="image" src="https://github.com/user-attachments/assets/0ac66e1e-104f-4488-8a7d-adf5478f1741" />


sed -n -e '$p' file23
## OUTPUT

<img width="322" height="77" alt="image" src="https://github.com/user-attachments/assets/11f47164-6443-41ef-b1c7-ca05919be7d8" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="380" height="260" alt="image" src="https://github.com/user-attachments/assets/121f92ad-59eb-4125-9971-28b8a1edc337" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="412" height="252" alt="image" src="https://github.com/user-attachments/assets/936c1a6f-2920-4e15-90a8-99e27dd532fe" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="386" height="252" alt="image" src="https://github.com/user-attachments/assets/9807d5bf-7452-4f23-b9f3-14a2f68fd0e9" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="337" height="181" alt="image" src="https://github.com/user-attachments/assets/bed65896-b95b-4caa-a8e7-161e6c78f396" />



sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="367" height="123" alt="image" src="https://github.com/user-attachments/assets/24a8d603-b0a5-4ad3-ab3b-c9c3b11dd8e9" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="410" height="107" alt="image" src="https://github.com/user-attachments/assets/fa4bb81a-0461-428d-aa5b-082a4cae288d" />


seq 10 
## OUTPUT
<img width="280" height="302" alt="image" src="https://github.com/user-attachments/assets/82abbbde-c403-4885-8a2e-5123d3653725" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="302" height="135" alt="image" src="https://github.com/user-attachments/assets/9b0d3c44-2b1e-49e7-8be8-b78ae87abc2d" />


seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="312" height="132" alt="image" src="https://github.com/user-attachments/assets/68451262-d338-430e-a599-f6fd8694422c" />

seq 3 | sed '2a hello'
## OUTPUT

<img width="300" height="156" alt="image" src="https://github.com/user-attachments/assets/623a0951-d70d-4187-bb03-ca16d7b85c23" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="301" height="126" alt="image" src="https://github.com/user-attachments/assets/2eaddc71-88a8-46b2-8bde-76a32acee2c2" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="337" height="135" alt="image" src="https://github.com/user-attachments/assets/58be68cc-41ca-4cc0-b69a-d70b3eb1a776" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="415" height="128" alt="image" src="https://github.com/user-attachments/assets/0297b45f-5b9d-422f-bd83-576c453c68bc" />

sed -n '2,4{s/$/*/;p}' file23

<img width="406" height="135" alt="image" src="https://github.com/user-attachments/assets/22fcf75a-08e8-48a8-80a5-9a90023ad719" />

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
<img width="337" height="182" alt="image" src="https://github.com/user-attachments/assets/21982753-1c7b-4a81-9001-44659baadd58" />


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

<img width="338" height="177" alt="image" src="https://github.com/user-attachments/assets/4ddb07da-d41a-4ac8-b993-0daa3ca214cc" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="457" height="252" alt="image" src="https://github.com/user-attachments/assets/d98b85e5-d9af-42e0-9bff-38707cf14cbe" />

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
<img width="352" height="128" alt="image" src="https://github.com/user-attachments/assets/43d8b176-1d6d-41d2-807e-92b3e4a5fc33" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="470" height="128" alt="image" src="https://github.com/user-attachments/assets/62dee43e-18fc-43ab-a486-2abb73952ab3" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="312" height="253" alt="image" src="https://github.com/user-attachments/assets/299c86ff-a57c-4357-95da-9b1e6b6f3952" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="722" height="552" alt="image" src="https://github.com/user-attachments/assets/7878b567-7649-4fdb-9ccf-768a20af7562" />


tar -xvf backup.tar
## OUTPUT
<img width="416" height="253" alt="image" src="https://github.com/user-attachments/assets/4311f84e-c60a-4044-94df-abc6c7364c66" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="410" height="81" alt="image" src="https://github.com/user-attachments/assets/0a5bf30e-bf4e-4d24-a5d4-bfabe55ab379" />
 
gunzip backup.tar.gz
## OUTPUT
<img width="647" height="157" alt="image" src="https://github.com/user-attachments/assets/0280672b-76c3-43ae-a8a2-aa118f885140" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="472" height="232" alt="image" src="https://github.com/user-attachments/assets/79eb618f-2bab-440b-9f8a-a83a7bdc0b8a" />
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="421" height="317" alt="image" src="https://github.com/user-attachments/assets/e483e38b-d9b9-418a-95a6-c095ffa80ba0" />

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
<img width="490" height="775" alt="image" src="https://github.com/user-attachments/assets/0d11bbc2-d331-4707-b798-ba6fd5100a8e" />

 
ls file1
## OUTPUT
<img width="297" height="77" alt="image" src="https://github.com/user-attachments/assets/23f492ec-9b76-49bc-8a2b-30dddd7ca834" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="267" height="81" alt="image" src="https://github.com/user-attachments/assets/7b6ab401-3637-4f7e-b06d-1d30e26bedf0" />

abcd
 
echo $?
 ## OUTPUT


 <img width="335" height="155" alt="image" src="https://github.com/user-attachments/assets/e674db6e-add6-4b1d-b03b-aef7bcc19802" />

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

<img width="363" height="277" alt="image" src="https://github.com/user-attachments/assets/715bac90-6be4-42c6-b8a1-ae6d41ed15b2" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="620" height="151" alt="image" src="https://github.com/user-attachments/assets/8be26388-3957-478a-abe1-d87dcf5efbbe" />


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
<img width="612" height="303" alt="image" src="https://github.com/user-attachments/assets/92cebdf7-40eb-4401-af18-7cf00947fe85" />

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

<img width="530" height="582" alt="image" src="https://github.com/user-attachments/assets/c38ed3ed-532b-4f94-938a-e32d4f7d35e2" />


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
<img width="530" height="582" alt="image" src="https://github.com/user-attachments/assets/da47a20d-c1d7-48c3-b040-472fc3faa367" />

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
<img width="517" height="680" alt="image" src="https://github.com/user-attachments/assets/003f6c99-737b-49c7-afaf-9bdb181877e4" />

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
<img width="581" height="347" alt="image" src="https://github.com/user-attachments/assets/f2d6c38b-8207-4475-9740-0969c1a6de02" />


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
<img width="612" height="598" alt="image" src="https://github.com/user-attachments/assets/ceddfb07-1173-433c-b15b-2c1d39464f30" />

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
 
<img width="343" height="610" alt="image" src="https://github.com/user-attachments/assets/16885da8-5227-4007-bd7f-83aa4bce44d9" />
 
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
 
 
 <img width="306" height="452" alt="image" src="https://github.com/user-attachments/assets/2feb107a-e5cf-4cf9-bd15-828a3db51bdf" />

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
 <img width="655" height="456" alt="image" src="https://github.com/user-attachments/assets/5cb9ff59-46cf-447c-88b2-557cebb75545" />

 
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
<img width="576" height="456" alt="image" src="https://github.com/user-attachments/assets/705c406f-c08d-406d-b779-f7711afa96c9" />
 
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
 <img width="572" height="458" alt="image" src="https://github.com/user-attachments/assets/68d144d1-6ece-4519-a514-7b07864e31b7" />

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
<img width="353" height="502" alt="image" src="https://github.com/user-attachments/assets/2c1a7601-44ba-4d5a-8f33-c295a528fd66" />

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
<img width="343" height="450" alt="image" src="https://github.com/user-attachments/assets/9272d706-7f59-4545-be12-7931bb2274f1" />

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
<img width="362" height="435" alt="image" src="https://github.com/user-attachments/assets/673a7357-5a61-47f4-9834-78f728458709" />

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

 <img width="401" height="432" alt="image" src="https://github.com/user-attachments/assets/2200de22-61a2-47a9-b40a-b3881c4977fb" />

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
<img width="360" height="701" alt="image" src="https://github.com/user-attachments/assets/61f485a4-3d87-4221-a662-9385f2d8e4c9" />

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 <img width="361" height="505" alt="image" src="https://github.com/user-attachments/assets/7887adf9-8381-4ffa-9751-e2ac44c85941" />

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
 <img width="553" height="558" alt="image" src="https://github.com/user-attachments/assets/d84e6b30-2054-4986-a07b-5d388dcb831b" />

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

<img width="460" height="330" alt="image" src="https://github.com/user-attachments/assets/13785716-68cd-44a3-a5ed-b279e85b96c0" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 
<img width="446" height="330" alt="image" src="https://github.com/user-attachments/assets/4c1ca308-30ea-4d8b-839a-8092aeff3c2a" />
 
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

 
 ./funcex.sh 1 2

 <img width="577" height="526" alt="image" src="https://github.com/user-attachments/assets/8e4de6b6-e6a0-4904-82bc-f79bb283df1f" />

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
 <img width="302" height="357" alt="image" src="https://github.com/user-attachments/assets/b335c1b4-783d-4bb8-b2c8-4cce3add878e" />

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
 <img width="396" height="483" alt="image" src="https://github.com/user-attachments/assets/7113f9b2-9d0a-49c7-8aed-7a34819d851e" />

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
 <img width="338" height="678" alt="image" src="https://github.com/user-attachments/assets/efcc788b-e12f-40c5-a7c1-dfeca3199180" />

 
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
 <img width="368" height="380" alt="image" src="https://github.com/user-attachments/assets/8ca7a14b-3e38-4b0f-9764-2d1c3e2741f9" />

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

<img width="340" height="180" alt="image" src="https://github.com/user-attachments/assets/d3553f1c-43e7-4a22-9b31-59885320eb11" />

# RESULT:
The Commands are executed successfully.
