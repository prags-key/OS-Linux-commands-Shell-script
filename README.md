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
<img width="165" height="86" alt="image" src="https://github.com/user-attachments/assets/2810fcb6-87dc-493d-abeb-39104867ab70" />




cat < file2
## OUTPUT
<img width="157" height="104" alt="image" src="https://github.com/user-attachments/assets/cc1cdffd-a8e4-4951-a91b-d7a875a877b3" />




# Comparing Files
cmp file1 file2
## OUTPUT
<img width="271" height="36" alt="image" src="https://github.com/user-attachments/assets/f7ebcedf-255e-4c9e-ac90-5b6d9a9e2bb6" />


 
comm file1 file2
 ## OUTPUT
 <img width="294" height="181" alt="image" src="https://github.com/user-attachments/assets/de3bb975-bc79-4fec-818c-bd5714515133" />

 

 
diff file1 file2
## OUTPUT
<img width="200" height="171" alt="image" src="https://github.com/user-attachments/assets/87dc48dc-94a1-4a5f-86df-f4668092a115" />



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
<img width="199" height="75" alt="image" src="https://github.com/user-attachments/assets/5cd09f71-e935-4441-ad92-e15f620908f8" />





cut -d "|" -f 1 file22
## OUTPUT
<img width="220" height="68" alt="image" src="https://github.com/user-attachments/assets/f5837748-852f-4b92-852b-068d229c97f2" />




cut -d "|" -f 2 file22
## OUTPUT
<img width="201" height="95" alt="image" src="https://github.com/user-attachments/assets/4f90524d-9df5-4239-a942-b0d7a33be7dd" />



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
<img width="282" height="38" alt="image" src="https://github.com/user-attachments/assets/285f7565-bee8-42b1-beba-4bfa9b577ee8" />



grep hello newfile 
## OUTPUT
<img width="190" height="35" alt="image" src="https://github.com/user-attachments/assets/0dd3df21-72d5-46df-aa83-8d7edeb59834" />






grep -v hello newfile 
## OUTPUT
<img width="195" height="35" alt="image" src="https://github.com/user-attachments/assets/c6ce6c8f-ba73-49ef-808e-331d1ee2cb85" />




cat newfile | grep -i "hello"
## OUTPUT
<img width="286" height="55" alt="image" src="https://github.com/user-attachments/assets/0b51d8ff-1729-4512-a4b2-87be8d01836a" />





cat newfile | grep -i -c "hello"
## OUTPUT
<img width="263" height="36" alt="image" src="https://github.com/user-attachments/assets/8d3e9e62-6c91-4f58-9af4-71d7058bf763" />





grep -R ubuntu /etc
## OUTPUT
<img width="1289" height="446" alt="image" src="https://github.com/user-attachments/assets/1dc252fa-9be7-4cda-91c6-9b561bef6e4e" />





grep -w -n world newfile   
## OUTPUT
<img width="217" height="50" alt="image" src="https://github.com/user-attachments/assets/6270718a-876a-486d-8e28-9961665e7753" />



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
<img width="321" height="58" alt="image" src="https://github.com/user-attachments/assets/545f81a6-855b-45f7-bba2-f4e4ab233602" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="320" height="78" alt="image" src="https://github.com/user-attachments/assets/8d3dc26e-18a4-42a9-a87a-2fa1f3d0c289" />





egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="258" height="73" alt="image" src="https://github.com/user-attachments/assets/27c585bc-9af0-4fae-b47c-2c20558fffce" />





egrep '(^hello)' newfile 
## OUTPUT
<img width="256" height="73" alt="image" src="https://github.com/user-attachments/assets/9204b6a8-1c03-4952-9c94-d7c831c27942" />




egrep '(world$)' newfile 
## OUTPUT
<img width="219" height="67" alt="image" src="https://github.com/user-attachments/assets/5c1318aa-9a0d-4d28-ba5c-205b1306bb77" />




egrep '(World$)' newfile 
## OUTPUT
<img width="234" height="58" alt="image" src="https://github.com/user-attachments/assets/f4b74579-36e1-412d-be69-5d348b73370e" />




egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="242" height="35" alt="image" src="https://github.com/user-attachments/assets/75c35fb7-2c7f-4752-ab78-5494f0302a5a" />





egrep '[1-9]' newfile 
## OUTPUT
<img width="249" height="68" alt="image" src="https://github.com/user-attachments/assets/98c8802a-f09d-4daf-884b-1759b6faf395" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="262" height="33" alt="image" src="https://github.com/user-attachments/assets/fc90a423-6626-40be-abe4-824fd8b391e3" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="271" height="55" alt="image" src="https://github.com/user-attachments/assets/c6b65c62-3483-467f-b4f0-b7fefe1f3ff7" />




egrep l{2} newfile
## OUTPUT
<img width="234" height="67" alt="image" src="https://github.com/user-attachments/assets/bc516d88-8c91-45b6-903e-f8c3c7cb680a" />




egrep 's{1,2}' newfile
## OUTPUT 
<img width="304" height="78" alt="image" src="https://github.com/user-attachments/assets/b98e4a31-1782-486f-ab79-1e2556460948" />



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
<img width="226" height="51" alt="image" src="https://github.com/user-attachments/assets/4a680df7-469d-481c-a23a-c56a5e5e637c" />




sed -n -e '$p' file23
## OUTPUT
<img width="226" height="51" alt="image" src="https://github.com/user-attachments/assets/c15002a6-db90-454f-80d4-51e6696a9d4f" />





sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="291" height="170" alt="image" src="https://github.com/user-attachments/assets/b09f0e77-7131-4e28-a1bd-f8cc1c09cdff" />





sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="301" height="173" alt="image" src="https://github.com/user-attachments/assets/ae6cc5f7-be94-40e5-b346-b239fd49957b" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="315" height="179" alt="image" src="https://github.com/user-attachments/assets/1c693796-8848-4675-801b-7037b334b578" />




sed -n -e '1,5p' file23
## OUTPUT
<img width="297" height="119" alt="image" src="https://github.com/user-attachments/assets/a2d5a12e-a5df-47b3-9133-0e6d8904eb8a" />




sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="304" height="64" alt="image" src="https://github.com/user-attachments/assets/0fc5215f-ea7e-456e-a440-cf18b42ce2b2" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="291" height="69" alt="image" src="https://github.com/user-attachments/assets/d55397ab-67f0-4952-8ff2-eee5be6bee8b" />




seq 10 
## OUTPUT
<img width="266" height="205" alt="image" src="https://github.com/user-attachments/assets/6fc7a52f-abe2-4ead-bca1-c4556a2a3dc0" />




seq 10 | sed -n '4,6p'
## OUTPUT
<img width="279" height="87" alt="image" src="https://github.com/user-attachments/assets/f83204bb-35f3-4a4c-a12f-6f85e627e741" />





seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="278" height="84" alt="image" src="https://github.com/user-attachments/assets/a6e7d20c-242e-4d36-acfc-62ca488fd2df" />




seq 3 | sed '2a hello'
## OUTPUT
<img width="291" height="102" alt="image" src="https://github.com/user-attachments/assets/b59847dd-ad8f-40f7-8337-bf82d6f2f5ab" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="246" height="86" alt="image" src="https://github.com/user-attachments/assets/7b33f1b4-8f56-4a0c-b5df-710cfde56196" />



seq 10 | sed '2,9c hello'
## OUTPUT
<img width="267" height="85" alt="image" src="https://github.com/user-attachments/assets/c53ff756-c239-4081-a264-221569979454" />




sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="290" height="91" alt="image" src="https://github.com/user-attachments/assets/fe879f32-dce4-49bd-902d-b507c0c389f5" />




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
<img width="238" height="114" alt="image" src="https://github.com/user-attachments/assets/2ac68f37-5320-4b24-81dc-24ad4f59b4a2" />



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
<img width="245" height="117" alt="image" src="https://github.com/user-attachments/assets/7e8d99cd-d3d7-454c-b8d2-d97231d51613" />




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="311" height="166" alt="image" src="https://github.com/user-attachments/assets/cc19ff16-21f2-4c6f-b88f-298468d37458" />

 

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
 <img width="314" height="92" alt="image" src="https://github.com/user-attachments/assets/1a741481-90cb-43b2-a02f-6c157dd22f22" />

 


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="328" height="92" alt="image" src="https://github.com/user-attachments/assets/791213ac-35cc-40d3-8ccf-c8d1a5cac2e1" />





#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="230" height="208" alt="image" src="https://github.com/user-attachments/assets/ac5dbfc6-90bb-4086-89e1-0e1e7c5c69df" />




mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="553" height="203" alt="image" src="https://github.com/user-attachments/assets/e6adb52b-d582-4bfb-9aeb-729a90aec4f5" />



tar -xvf backup.tar
## OUTPUT
<img width="219" height="208" alt="image" src="https://github.com/user-attachments/assets/9946c104-233f-4ceb-a83f-096c131b7d6a" />



gzip backup.tar

ls .gz
## OUTPUT
<img width="125" height="57" alt="image" src="https://github.com/user-attachments/assets/4921ecb2-f157-4436-9654-cbeefbee46a8" />


 
gunzip backup.tar.gz
## OUTPUT
<img width="123" height="54" alt="image" src="https://github.com/user-attachments/assets/ebc63929-f299-4d93-8024-d43312c8a7b4" />



 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="376" height="110" alt="image" src="https://github.com/user-attachments/assets/4eb89257-2f5f-42f8-83cd-12347667f42d" />


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="260" height="85" alt="image" src="https://github.com/user-attachments/assets/a11f13b4-b67a-4c09-aa4d-71c8623b011b" />





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
<img width="460" height="362" alt="image" src="https://github.com/user-attachments/assets/84c217cf-580c-4063-9390-468ab3621af4" />


 
ls file1
## OUTPUT
<img width="122" height="56" alt="image" src="https://github.com/user-attachments/assets/a8170fbd-44dc-4309-876a-4dd65510a62f" />



echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
 
<img width="136" height="55" alt="image" src="https://github.com/user-attachments/assets/7536912f-1167-426e-b079-2adb51d5db39" />


 
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




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="265" height="192" alt="image" src="https://github.com/user-attachments/assets/a5372a54-8c35-4622-87b7-4f6de06aa432" />


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
<img width="470" height="125" alt="image" src="https://github.com/user-attachments/assets/0a26866d-8fcd-4987-b89b-af9441b9aded" />





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
<img width="455" height="106" alt="image" src="https://github.com/user-attachments/assets/876987e4-b03e-49ec-81ec-e4342a9bb99c" />


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
<img width="448" height="122" alt="image" src="https://github.com/user-attachments/assets/e132b8e0-f38b-485b-bc3a-711eaeebaca5" />



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
<img width="508" height="85" alt="image" src="https://github.com/user-attachments/assets/ae1077e1-96ca-4fdb-a741-347042fe38b3" />



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
<img width="451" height="89" alt="image" src="https://github.com/user-attachments/assets/e114145d-05b7-4355-98fb-e55f61caf1ac" />


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
# Output
<img width="319" height="75" alt="image" src="https://github.com/user-attachments/assets/72173393-d534-4a78-b201-b2d2afff3f45" />

 
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
# Output
<img width="254" height="229" alt="image" src="https://github.com/user-attachments/assets/55cd8832-f290-452d-bc52-7c1393f1508d" />

 
 
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
# Output
<img width="258" height="120" alt="image" src="https://github.com/user-attachments/assets/57ebf1ac-635e-4810-9990-728b5033e4dd" />

 
 
 
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
# Output
<img width="214" height="151" alt="image" src="https://github.com/user-attachments/assets/cd1455dd-c80c-497c-b113-15f01eb5f261" />

 
 
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
# Output
<img width="275" height="106" alt="image" src="https://github.com/user-attachments/assets/63742277-c676-4eee-8d41-0dc596402bdd" />


 
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
# Output
<img width="249" height="159" alt="image" src="https://github.com/user-attachments/assets/23edd403-1c2b-4be9-801e-d33ee093ced6" />

 
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
<img width="339" height="284" alt="image" src="https://github.com/user-attachments/assets/eae30345-24bf-46e4-91b2-dd8228d7082d" />



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
<img width="255" height="145" alt="image" src="https://github.com/user-attachments/assets/b38c7e4a-e734-4344-bbde-ed1c92808f5b" />


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
<img width="243" height="129" alt="image" src="https://github.com/user-attachments/assets/94ff04e3-0c97-435a-80d0-f6ac4b2b3b5d" />



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
 <img width="283" height="250" alt="image" src="https://github.com/user-attachments/assets/cc2d9164-0f30-4ea0-80f1-70d974905999" />

 

 
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
<img width="352" height="141" alt="image" src="https://github.com/user-attachments/assets/dab36865-3fc0-4b0c-839b-71347eb74396" />


 
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
<img width="338" height="95" alt="image" src="https://github.com/user-attachments/assets/57e0d202-b53a-4006-96c0-59f6128d3b46" />



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="196" height="106" alt="image" src="https://github.com/user-attachments/assets/ec094dd7-ae23-4114-bd45-6350c81f072d" />





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
 <img width="229" height="121" alt="image" src="https://github.com/user-attachments/assets/07644db7-d9cf-4366-aa11-afbca16ed43e" />


 
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
<img width="282" height="139" alt="image" src="https://github.com/user-attachments/assets/88fb50f5-d36c-4814-9774-5ee278bc67e0" />


 
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
<img width="240" height="118" alt="image" src="https://github.com/user-attachments/assets/f5ace05a-3311-43f1-870f-307bfb4fdf2b" />

 
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
 <img width="295" height="307" alt="image" src="https://github.com/user-attachments/assets/88e4d13d-e2ee-4386-a3f5-3932c7eece60" />

 
 
 
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
<img width="290" height="256" alt="image" src="https://github.com/user-attachments/assets/02240ee3-dc63-48e1-a882-dd42bfe1db72" />

 
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
<img width="250" height="103" alt="image" src="https://github.com/user-attachments/assets/d14f8bbf-1567-434d-bfd0-50ba83eecf7d" />



# RESULT:
The Commands are executed successfully.
