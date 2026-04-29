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
<img width="953" height="156" alt="Screenshot 2026-04-29 114735" src="https://github.com/user-attachments/assets/b358671d-321f-4e3c-9619-3f7e111bb047" />



cat < file2
## OUTPUT
c<img width="954" height="174" alt="Screenshot 2026-04-29 114826" src="https://github.com/user-attachments/assets/12e134c1-82c0-4e39-8a83-85de525920e9" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="892" height="91" alt="Screenshot 2026-04-29 114945" src="https://github.com/user-attachments/assets/dd407a56-3da8-4890-b085-905dca91dcf7" />

comm file1 file2
 ## OUTPUT
<img width="949" height="219" alt="Screenshot 2026-04-29 115034" src="https://github.com/user-attachments/assets/bb98dd18-7694-430a-aab4-24bb76e48e6e" />



 
diff file1 file2
## OUTPUT
<img width="889" height="250" alt="Screenshot 2026-04-29 130739" src="https://github.com/user-attachments/assets/af799e19-1259-4b3e-8405-f07445d91a62" />


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
<img width="835" height="169" alt="Screenshot 2026-04-29 131343" src="https://github.com/user-attachments/assets/476242d2-b2dc-43be-ad45-8b1a807081a0" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="764" height="173" alt="Screenshot 2026-04-29 131517" src="https://github.com/user-attachments/assets/5a1940c1-d5d4-44e9-9133-eebbbaf05aa3" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="591" height="189" alt="Screenshot 2026-04-29 131625" src="https://github.com/user-attachments/assets/e055662f-5df1-46c7-8ad5-5c8ad2c295dd" />


cat > newfile 
```
Hello world
hello world
^d
````
cat < newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
<img width="525" height="74" alt="Screenshot 2026-04-29 131821" src="https://github.com/user-attachments/assets/16b4b846-7f78-418c-acc8-d9f68057b539" />



grep hello newfile 
## OUTPUT
<img width="644" height="72" alt="Screenshot 2026-04-29 131855" src="https://github.com/user-attachments/assets/f255db93-f3f3-4477-a266-f70168ec71e7" />




grep -v hello newfile 
## OUTPUT
<img width="492" height="151" alt="Screenshot 2026-04-29 131927" src="https://github.com/user-attachments/assets/59ee1ca5-cfb8-474e-89c0-2b63ed00cca0" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="694" height="99" alt="Screenshot 2026-04-29 132011" src="https://github.com/user-attachments/assets/71df96f1-514a-4642-b3c6-bc587a9b349a" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="655" height="85" alt="Screenshot 2026-04-29 132336" src="https://github.com/user-attachments/assets/39439461-52a0-4ef2-a234-5545eaa56583" />



grep -w -n world newfile   
## OUTPUT
<img width="673" height="110" alt="Screenshot 2026-04-29 132714" src="https://github.com/user-attachments/assets/1a259bd6-2274-44c6-9d1e-50cf8b8787a3" />


cat > newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat < newfile
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
<img width="693" height="105" alt="Screenshot 2026-04-29 132907" src="https://github.com/user-attachments/assets/532c20ae-f10c-4447-86ab-3dda76a0d9f7" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="590" height="79" alt="Screenshot 2026-04-29 132941" src="https://github.com/user-attachments/assets/67cecbdf-5ce6-43c7-94c8-6574ef40db38" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="539" height="99" alt="Screenshot 2026-04-29 133011" src="https://github.com/user-attachments/assets/fdc201dc-dc14-430d-b157-c30d4396343c" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="598" height="78" alt="Screenshot 2026-04-29 133104" src="https://github.com/user-attachments/assets/6e0f153b-c4a9-4be3-9399-9db1a28383d8" />



egrep '(world$)' newfile 
## OUTPUT
<img width="572" height="90" alt="Screenshot 2026-04-29 133133" src="https://github.com/user-attachments/assets/a3150de3-f15e-4bf5-9c63-3b6682614f10" />



egrep '(World$)' newfile 
## OUTPUT
<img width="683" height="79" alt="Screenshot 2026-04-29 133522" src="https://github.com/user-attachments/assets/0083d4b5-f32c-48a5-97e4-1cf1b7ce0efc" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="610" height="125" alt="Screenshot 2026-04-29 133555" src="https://github.com/user-attachments/assets/10214a5b-efb8-43f2-bf3f-d8117f335303" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="546" height="75" alt="Screenshot 2026-04-29 133639" src="https://github.com/user-attachments/assets/e30207aa-a438-43ea-86e3-cb719c077655" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="522" height="79" alt="Screenshot 2026-04-29 133702" src="https://github.com/user-attachments/assets/967b15b8-aa55-4117-8f54-22ea3a795477" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="656" height="74" alt="Screenshot 2026-04-29 133729" src="https://github.com/user-attachments/assets/3c68d352-a3b4-469a-afda-66e0666ceb88" />


egrep l{2} newfile
## OUTPUT
<img width="604" height="103" alt="Screenshot 2026-04-29 133801" src="https://github.com/user-attachments/assets/a9f61160-2817-4b16-8d52-b0bfaab14bb5" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="579" height="130" alt="Screenshot 2026-04-29 133823" src="https://github.com/user-attachments/assets/2410f5cc-469b-4df7-a6f5-3d1784421ab5" />


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
<img width="670" height="69" alt="Screenshot 2026-04-29 133911" src="https://github.com/user-attachments/assets/86d52a32-7aa5-490c-9379-c163fb97e6dd" />



sed -n -e '$p' file23
## OUTPUT
<img width="679" height="81" alt="Screenshot 2026-04-29 133936" src="https://github.com/user-attachments/assets/80e1e123-1a40-4c46-9185-f541d272dc40" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="588" height="328" alt="Screenshot 2026-04-29 134013" src="https://github.com/user-attachments/assets/13663706-c1b4-4dae-8ec5-6814763f6fc4" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="674" height="325" alt="Screenshot 2026-04-29 134039" src="https://github.com/user-attachments/assets/58deb4c1-0511-43f1-867b-9e7044f31cfb" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="683" height="326" alt="Screenshot 2026-04-29 134115" src="https://github.com/user-attachments/assets/7cc5d484-828d-46fb-aa6b-eb5dfa05957e" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="581" height="176" alt="Screenshot 2026-04-29 134141" src="https://github.com/user-attachments/assets/902ffe8a-14a2-4bde-b37a-4e78b88c37e9" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="654" height="148" alt="Screenshot 2026-04-29 134200" src="https://github.com/user-attachments/assets/74e65bb8-aa00-4cad-8c34-364183e2e138" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="675" height="106" alt="Screenshot 2026-04-29 134222" src="https://github.com/user-attachments/assets/01133966-a760-4661-b67b-5f6a8397ec3b" />



seq 10 
## OUTPUT
<img width="352" height="292" alt="Screenshot 2026-04-29 134244" src="https://github.com/user-attachments/assets/e20a26b9-26c8-4436-866e-9caaf4ca11f3" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="526" height="120" alt="Screenshot 2026-04-29 134311" src="https://github.com/user-attachments/assets/f48215f3-9d97-469b-a914-5b08640cc638" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="519" height="132" alt="Screenshot 2026-04-29 134339" src="https://github.com/user-attachments/assets/35de338b-01d3-4276-a007-7f05cb8d119d" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="448" height="142" alt="Screenshot 2026-04-29 134358" src="https://github.com/user-attachments/assets/88e6fc37-2b0b-4189-af5c-2a0aad90939e" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="470" height="129" alt="Screenshot 2026-04-29 134417" src="https://github.com/user-attachments/assets/04ef8005-fd00-483d-9d46-53b18439fdac" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="525" height="119" alt="Screenshot 2026-04-29 134439" src="https://github.com/user-attachments/assets/ec1b9dad-46eb-43a8-a503-1baef5f19d91" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="563" height="118" alt="Screenshot 2026-04-29 134459" src="https://github.com/user-attachments/assets/b03384e1-4286-4a3f-9927-66b68ce8781c" />


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
<img width="601" height="225" alt="Screenshot 2026-04-29 134623" src="https://github.com/user-attachments/assets/c34de829-aa13-48f8-82f5-4e0907201800" />


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
<img width="560" height="212" alt="Screenshot 2026-04-29 134706" src="https://github.com/user-attachments/assets/f649006e-6bf3-416c-8b25-32fe9bc59a26" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="641" height="325" alt="Screenshot 2026-04-29 134741" src="https://github.com/user-attachments/assets/2525f70e-f0b1-47bf-9983-fe355391222c" />

cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="595" height="186" alt="Screenshot 2026-04-29 134855" src="https://github.com/user-attachments/assets/50689dd5-71c3-4cc0-96ac-a90e46749983" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="568" height="186" alt="Screenshot 2026-04-29 134917" src="https://github.com/user-attachments/assets/5cb8791a-2a8a-46e3-92c1-626b15851df0" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="471" height="597" alt="Screenshot 2026-04-29 135010" src="https://github.com/user-attachments/assets/44e32165-5d05-46f4-9783-d241e4f73abf" />
<img width="435" height="593" alt="Screenshot 2026-04-29 135024" src="https://github.com/user-attachments/assets/f5f1e91d-ab4e-46da-ac08-e39921370756" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="686" height="596" alt="Screenshot 2026-04-29 135148" src="https://github.com/user-attachments/assets/38a512d9-461b-470d-b454-504ae07f94e9" />


tar -xvf backup.tar
## OUTPUT
<img width="523" height="595" alt="Screenshot 2026-04-29 135226" src="https://github.com/user-attachments/assets/a498120f-858b-40ca-ad5a-7880e483c041" />
<img width="461" height="550" alt="Screenshot 2026-04-29 135300" src="https://github.com/user-attachments/assets/940a338c-2d37-44a7-8f76-c2ef38e81e33" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="505" height="70" alt="Screenshot 2026-04-29 135501" src="https://github.com/user-attachments/assets/cbd0504a-3c9a-40ed-b667-0bd421db2aed" />

gunzip backup.tar.gz
## OUTPUT
<img width="526" height="106" alt="Screenshot 2026-04-29 135612" src="https://github.com/user-attachments/assets/b330c5a4-de4a-45fe-8436-9054d1b27805" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="458" height="151" alt="Screenshot 2026-04-29 140032" src="https://github.com/user-attachments/assets/9324f175-682c-4e6b-acd6-ffc407ce08c9" />


cat > scriptest.sh 
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
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
<img width="555" height="163" alt="Screenshot 2026-04-29 140153" src="https://github.com/user-attachments/assets/6b8843d2-f034-4bb1-bf28-2749cf81fa01" />

 
ls file1
## OUTPUT
<img width="379" height="80" alt="Screenshot 2026-04-29 140256" src="https://github.com/user-attachments/assets/23e0f99d-e701-4910-bb0b-f1195522182a" />

echo $?
## OUTPUT 
<img width="238" height="80" alt="Screenshot 2026-04-29 140330" src="https://github.com/user-attachments/assets/01e2bc81-4f5f-40ae-976a-6c56233b6020" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="377" height="84" alt="Screenshot 2026-04-29 140439" src="https://github.com/user-attachments/assets/b808d5f3-6008-4a0d-8c7c-7b683451bda3" />



 
# mis-using string comparisons

cat > strcomp.sh 
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
```
**##OUTPUT
<img width="615" height="357" alt="Screenshot 2026-04-29 140623" src="https://github.com/user-attachments/assets/8c181c3f-9e8d-4292-9f3b-ed46be88916d" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="499" height="128" alt="Screenshot 2026-04-29 140723" src="https://github.com/user-attachments/assets/bf63fd6f-3188-427d-aeaa-70058745b25c" />


# check file ownership
cat > psswdperm.sh 
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

cat > psswdperm.sh 
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
<img width="615" height="357" alt="Screenshot 2026-04-29 140623" src="https://github.com/user-attachments/assets/806de39b-b4e5-426c-8175-091ce42fa0e8" />

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
cat < ifnested.sh 
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

<img width="615" height="357" alt="Screenshot 2026-04-29 140623" src="https://github.com/user-attachments/assets/9e84b540-0826-46d2-ada4-4951b6ae2168" />


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


cat < iftest.sh 
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
<img width="511" height="504" alt="Screenshot 2026-04-29 141101" src="https://github.com/user-attachments/assets/9763d290-2a81-4a19-bc39-7e21eb88cf62" />

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

cat < ifnested.sh 
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
<img width="511" height="504" alt="Screenshot 2026-04-29 141101" src="https://github.com/user-attachments/assets/c300809f-351c-45b9-8ca9-b6e393ac7ac2" />

# looking for a possible value using elif
cat > elifcheck.sh 
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
<img width="511" height="504" alt="Screenshot 2026-04-29 141101" src="https://github.com/user-attachments/assets/45d02a42-5da1-4adc-83dc-7b7ff0cb5f30" />


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
<img width="511" height="504" alt="Screenshot 2026-04-29 141101" src="https://github.com/user-attachments/assets/3bae90c4-69cb-4fcc-af86-a4cee57ba9dc" />

# using the case command
cat > casecheck.sh 
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
 
 
cat >untiltest.sh 
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
 
 
 
cat >forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat >forin2.sh 
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
<img width="511" height="504" alt="Screenshot 2026-04-29 141101" src="https://github.com/user-attachments/assets/a3740698-655a-4b30-aec1-022415e50a4a" />

cat >forinfile.sh 
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
<img width="511" height="504" alt="Screenshot 2026-04-29 141101" src="https://github.com/user-attachments/assets/2673cfcb-4e55-490a-b10d-c122fe69c3d1" />


cat >forctype.sh 
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
<img width="511" height="504" alt="Screenshot 2026-04-29 141101" src="https://github.com/user-attachments/assets/cae4dda4-fe7f-4e86-bfcf-6b23b6125b0b" />

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
<img width="511" height="504" alt="Screenshot 2026-04-29 141101" src="https://github.com/user-attachments/assets/afe14045-d31d-4fab-aace-d233553c483f" />

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
<img width="511" height="504" alt="Screenshot 2026-04-29 141101" src="https://github.com/user-attachments/assets/f2765fdd-3fc8-4cd1-80e5-c28d36570668" />

 
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
<img width="511" height="504" alt="Screenshot 2026-04-29 141101" src="https://github.com/user-attachments/assets/aac80f71-d34d-4b81-bad4-b39bf278434b" />

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
 <img width="511" height="504" alt="Screenshot 2026-04-29 141101" src="https://github.com/user-attachments/assets/004eefcf-ed60-4c66-9b1e-6b1aad53dd5d" />

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
<img width="511" height="504" alt="Screenshot 2026-04-29 141101" src="https://github.com/user-attachments/assets/c0573afb-b377-4a20-952e-cd6e8032039b" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT


<img width="511" height="504" alt="Screenshot 2026-04-29 141101" src="https://github.com/user-attachments/assets/2f0a3c70-e0ed-4cdc-a8d4-5c33e8b233d4" />

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
<img width="238" height="80" alt="Screenshot 2026-04-29 140330" src="https://github.com/user-attachments/assets/fbf2687e-99c5-456d-8157-dc710c9e34d9" />

 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat > argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
<img width="615" height="357" alt="Screenshot 2026-04-29 140623" src="https://github.com/user-attachments/assets/cf3f067b-cd23-4bc5-84e6-9417d20b5154" />

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
<img width="615" height="357" alt="Screenshot 2026-04-29 140623" src="https://github.com/user-attachments/assets/86a9c88c-0ccd-45c3-aeee-2f4348a73d71" />

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
<img width="615" height="357" alt="Screenshot 2026-04-29 140623" src="https://github.com/user-attachments/assets/2d84bf0e-275f-41f8-9f95-3eca6e46d4c6" />

 ./argshift.sh 1 2 3
 
 
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
 <img width="648" height="523" alt="Screenshot 2026-04-29 141632" src="https://github.com/user-attachments/assets/a29c24ef-2204-4978-b8f8-40a5cc9e6177" />

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
<img width="475" height="594" alt="Screenshot 2026-04-29 141729" src="https://github.com/user-attachments/assets/5fc395ee-ac28-4773-9cea-32a1124c37f3" />


# RESULT:
The Commands are executed successfully.
