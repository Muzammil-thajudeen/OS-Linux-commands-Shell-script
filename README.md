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

<img width="229" height="66" alt="image" src="https://github.com/user-attachments/assets/2771a0ce-11b9-4b51-bc9d-b03b5d66f74e" />


cat < file2
## OUTPUT
<img width="213" height="73" alt="image" src="https://github.com/user-attachments/assets/8d0844c8-4c3a-41ba-8ba4-28d041ec99ab" />



# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="240" height="33" alt="image" src="https://github.com/user-attachments/assets/4570ca74-db98-4350-8b08-b946fadac4fc" />

comm file1 file2
 ## OUTPUT
 <img width="338" height="89" alt="image" src="https://github.com/user-attachments/assets/54d34c51-a328-45a1-b686-32d8055c1ec4" />


 
diff file1 file2
## OUTPUT
<img width="345" height="113" alt="image" src="https://github.com/user-attachments/assets/05e0d2fb-485b-4b11-af2a-38d0f5059db4" />


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
<img width="287" height="44" alt="image" src="https://github.com/user-attachments/assets/504f8dd9-7650-456d-a520-787784fba128" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="218" height="42" alt="image" src="https://github.com/user-attachments/assets/35e2b0cd-2a55-4d24-9b07-5b6644dfc2dd" />



cut -d "|" -f 2 file22
## OUTPUT


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

<img width="366" height="35" alt="image" src="https://github.com/user-attachments/assets/4e3bbeb1-b219-46c9-8dd6-bb952c86eb7e" />


grep hello newfile 
## OUTPUT
<img width="366" height="35" alt="image" src="https://github.com/user-attachments/assets/d7c35e22-39b1-41ef-9d7c-69b5e7df4e0d" />




grep -v hello newfile 
## OUTPUT

<img width="355" height="30" alt="image" src="https://github.com/user-attachments/assets/cafdb6f5-679a-4639-81fc-3e7276af492c" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="355" height="40" alt="image" src="https://github.com/user-attachments/assets/bc8561a0-ec9e-4d84-8100-0fc92a94627b" />


cat newfile | grep -i -c "hello"
## OUTPUT


<img width="355" height="35" alt="image" src="https://github.com/user-attachments/assets/79908b24-5b77-4fc6-9a78-28234eb45132" />


grep -R ubuntu /etc
## OUTPUT

<img width="813" height="364" alt="image" src="https://github.com/user-attachments/assets/9297a149-0630-458a-9725-8935473d6c8b" />
<img width="943" height="321" alt="image" src="https://github.com/user-attachments/assets/be56ed1a-a0bd-4e01-adcf-dbd400c70886" />


grep -w -n world newfile   
## OUTPUT

<img width="835" height="54" alt="image" src="https://github.com/user-attachments/assets/fb38f2cc-8590-4801-a6c4-22e2689ba8c4" />

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

<img width="828" height="53" alt="image" src="https://github.com/user-attachments/assets/f9d47a54-ef6f-4e03-953c-a06e048a7c61" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="717" height="45" alt="image" src="https://github.com/user-attachments/assets/fdf7a7a6-59fe-47f2-ae0b-973f215ed780" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="471" height="30" alt="image" src="https://github.com/user-attachments/assets/dffa9a8e-04e6-4f82-a58b-0db9f8ab24bd" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="471" height="30" alt="image" src="https://github.com/user-attachments/assets/aa3da4a5-eff7-48b5-9fd9-0d7b106631ab" />


egrep '(world$)' newfile 
## OUTPUT
<img width="285" height="88" alt="Screenshot 2026-05-01 091435" src="https://github.com/user-attachments/assets/2dd61146-cebc-4cc2-b1c2-99f1adb66a2b" />






egrep '(World$)' newfile 
## OUTPUT
<img width="261" height="71" alt="Screenshot 2026-05-01 091748" src="https://github.com/user-attachments/assets/5e4bb8d0-2d4a-49f4-8eb5-214a1feb647b" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="277" height="77" alt="Screenshot 2026-05-01 091834" src="https://github.com/user-attachments/assets/594b92bd-ae04-4059-a74d-3c9e20caf0a5" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="243" height="49" alt="Screenshot 2026-05-01 091919" src="https://github.com/user-attachments/assets/7b25c40c-8d79-42ac-b83f-b807d00643e1" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="312" height="89" alt="Screenshot 2026-05-01 092028" src="https://github.com/user-attachments/assets/2ad58d59-4948-4ac8-9f4e-875c55c7cf7d" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="318" height="82" alt="Screenshot 2026-05-01 092125" src="https://github.com/user-attachments/assets/bf7ba799-66fe-4d34-a7e0-bd58009d931d" />


egrep l{2} newfile
## OUTPUT

<img width="215" height="59" alt="Screenshot 2026-05-01 092216" src="https://github.com/user-attachments/assets/70fe44f0-7c1a-4daa-b8e8-a21c6a5d670f" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="262" height="96" alt="Screenshot 2026-05-01 092253" src="https://github.com/user-attachments/assets/223277bb-0f52-4638-b426-1aea292164e1" />


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

<img width="242" height="45" alt="Screenshot 2026-04-30 112749" src="https://github.com/user-attachments/assets/54a9849b-cbc0-4ef9-a860-0bea290aae88" />


sed -n -e '$p' file23
## OUTPUT

<img width="280" height="49" alt="Screenshot 2026-04-30 112834" src="https://github.com/user-attachments/assets/2700785c-bed5-48df-90aa-c55df9c0388e" />


sed  -e 's/Ram/Sita/' file23D
## OUTPUT

<img width="354" height="113" alt="Screenshot 2026-04-30 112925" src="https://github.com/user-attachments/assets/727340e9-9ef6-4db3-abc8-cae892e0d8f3" />


sed  -e '2s/Ram/Sita/' file23D
## OUTPUT

<img width="335" height="107" alt="image" src="https://github.com/user-attachments/assets/5285f4b2-6e4d-4a4c-bf65-e76e028a52cc" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT



sed -n -e '1,5p' file23
## OUTPUT
<img width="421" height="113" alt="Screenshot 2026-04-30 113040" src="https://github.com/user-attachments/assets/183ac569-fda3-4e04-8205-a1ffd62d1af9" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="382" height="99" alt="Screenshot 2026-04-30 113111" src="https://github.com/user-attachments/assets/5f0b5b8b-01a1-4326-8996-d6dc1b6e7cdd" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="433" height="102" alt="Screenshot 2026-04-30 113146" src="https://github.com/user-attachments/assets/55024b45-f565-43ea-9acc-7771d5755d93" />


seq 10 
## OUTPUT
<img width="285" height="177" alt="Screenshot 2026-04-30 113221" src="https://github.com/user-attachments/assets/14871d64-3ce1-4089-ae3d-c149d8009992" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="349" height="81" alt="Screenshot 2026-04-30 113312" src="https://github.com/user-attachments/assets/c1058357-d9d9-4ae4-ad05-0955d2bb0b1c" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="322" height="81" alt="Screenshot 2026-04-30 113348" src="https://github.com/user-attachments/assets/975ba276-2e5b-4eea-a753-cf3baeb8ac80" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="269" height="99" alt="Screenshot 2026-05-01 092335" src="https://github.com/user-attachments/assets/2076d34c-5a48-4683-92ab-926d0a9d18af" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="229" height="86" alt="Screenshot 2026-05-01 092423" src="https://github.com/user-attachments/assets/04d5c41f-26ae-4e41-90ec-27e440924e38" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="283" height="79" alt="Screenshot 2026-05-01 092506" src="https://github.com/user-attachments/assets/03a4f09d-17de-4b62-8319-ae6f3533cab6" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="296" height="76" alt="Screenshot 2026-05-01 092554" src="https://github.com/user-attachments/assets/47bba2f7-3e57-43e9-97d3-91aed47c1f9c" />


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

<img width="241" height="136" alt="Screenshot 2026-05-01 092650" src="https://github.com/user-attachments/assets/a6fb85b7-d565-4eb0-8e97-e8464c2607fe" />

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

<img width="253" height="88" alt="Screenshot 2026-05-01 092738" src="https://github.com/user-attachments/assets/4d0dd534-547b-49ab-bcb3-01705006f810" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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

<img width="442" height="79" alt="image" src="https://github.com/user-attachments/assets/cdad867d-3e7b-47aa-b33d-adf07cd12f1f" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="442" height="93" alt="image" src="https://github.com/user-attachments/assets/9881315d-f58a-4764-9c1e-4a86b4057c41" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="442" height="202" alt="image" src="https://github.com/user-attachments/assets/77c69525-b39e-4fc8-97c0-50c26c3eaa0b" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="867" height="529" alt="image" src="https://github.com/user-attachments/assets/7cb28b97-352f-4b8d-bd95-212a9f7e59ef" />

tar -xvf backup.tar
## OUTPUT
<img width="596" height="619" alt="image" src="https://github.com/user-attachments/assets/bcedcc76-d98f-4982-b9cd-6a61eb2d0e38" />

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
<img width="919" height="77" alt="image" src="https://github.com/user-attachments/assets/e564fea1-4dc4-43d1-ba05-476ffe9d3925" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="919" height="92" alt="image" src="https://github.com/user-attachments/assets/151e4a24-62ab-43aa-8e07-9c97e100b21a" />


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
<img width="919" height="157" alt="image" src="https://github.com/user-attachments/assets/157515ab-1ff8-4426-bc81-fea75c74837c" />
<img width="813" height="126" alt="image" src="https://github.com/user-attachments/assets/23a39cdb-44d8-4e3b-b833-df8b18ad6598" />

 
ls file1
## OUTPUT
<img width="813" height="52" alt="image" src="https://github.com/user-attachments/assets/a238dd0c-922a-4cc1-bcfa-075b3b826424" />


echo $?
## OUTPUT 
.<img width="813" height="51" alt="image" src="https://github.com/user-attachments/assets/1a067ee8-7586-4052-98ea-e747bfc0e155" />

## OUTPUT 
 <img width="813" height="51" alt="image" src="https://github.com/user-attachments/assets/678c4c62-52bb-4926-b6e3-73cf05cbddfc" />

 
echo $?
 ## OUTPUT
<img width="813" height="51" alt="image" src="https://github.com/user-attachments/assets/30b4a878-de61-442c-88d6-480e7a040793" />


 
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
<img width="813" height="126" alt="image" src="https://github.com/user-attachments/assets/86d0fe4e-8347-4a5c-bb5e-67d1304a5688" />
<img width="802" height="73" alt="image" src="https://github.com/user-attachments/assets/e59271a3-f01f-4720-850e-ceb34d846116" />




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="802" height="115" alt="image" src="https://github.com/user-attachments/assets/fc88df4e-8725-4afe-9f59-0347234c3164" />


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
<img width="802" height="161" alt="image" src="https://github.com/user-attachments/assets/a2942341-9b44-4067-bfd4-30d8f2abed5f" />

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

<img width="802" height="292" alt="image" src="https://github.com/user-attachments/assets/f355de44-1e85-4061-b347-c62491aefd27" />


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
<img width="761" height="124" alt="image" src="https://github.com/user-attachments/assets/a7983a86-b6ee-4bc2-848a-c7c556bf6ba0" />

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
<img width="705" height="236" alt="Screenshot 2026-04-29 213215" src="https://github.com/user-attachments/assets/de31d95a-843f-4649-9106-669b3d902810" />

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
<img width="547" height="652" alt="Screenshot 2026-04-29 225715" src="https://github.com/user-attachments/assets/1aae6d61-5f7f-4bae-91eb-9a974c11df8d" />


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
<img width="547" height="75" alt="image" src="https://github.com/user-attachments/assets/774e7b07-6ba2-49cc-9bab-a68786e84ab5" />
<img width="726" height="155" alt="image" src="https://github.com/user-attachments/assets/f94da50f-6214-43f6-a223-e99e19404fc3" />

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
 <img width="246" height="224" alt="Screenshot 2026-05-01 093417" src="https://github.com/user-attachments/assets/1c04fd49-e0c9-4ac3-9b67-660d6628c325" />

 
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
 
 <img width="399" height="102" alt="Screenshot 2026-05-01 093602" src="https://github.com/user-attachments/assets/3c414ae8-7e4f-4cd9-923b-384c6c85a5d7" />

 
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
 <img width="477" height="153" alt="Screenshot 2026-05-01 093802" src="https://github.com/user-attachments/assets/79bb19cb-bcc6-4a27-b5c7-b3a125bb0129" />

 
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
 <img width="368" height="109" alt="Screenshot 2026-05-01 093914" src="https://github.com/user-attachments/assets/d5f28ecf-2b07-4c4b-a49b-e6e4d2857289" />

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
 <img width="559" height="109" alt="image" src="https://github.com/user-attachments/assets/52a05af8-8f50-4967-bc7f-68ace16dd1ec" />

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
 <img width="559" height="138" alt="image" src="https://github.com/user-attachments/assets/f795389c-7558-4e4a-838d-94e3adb48187" />

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
<img width="482" height="186" alt="Screenshot 2026-05-01 094035" src="https://github.com/user-attachments/assets/6bc82ceb-dcac-4b30-9d27-52da817d27fc" />

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

<img width="559" height="144" alt="image" src="https://github.com/user-attachments/assets/37577752-8c04-497e-8c3d-05476453545a" />

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
<img width="304" height="140" alt="Screenshot 2026-04-30 110855" src="https://github.com/user-attachments/assets/89292328-812a-4299-ad01-9bf1c8dd6434" />

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
<img width="381" height="220" alt="Screenshot 2026-04-30 111104" src="https://github.com/user-attachments/assets/1054cc05-3700-40e6-b8ab-269b7912e2db" />

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
<img width="562" height="136" alt="Screenshot 2026-04-30 111309" src="https://github.com/user-attachments/assets/6c66c967-c87e-47b8-8ef5-81fcad79aa27" />

 
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
 <img width="620" height="149" alt="Screenshot 2026-04-30 111505" src="https://github.com/user-attachments/assets/f34364b8-b3b4-40d8-8552-b319ec815fb5" />

cat forcontinue.sh 
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
 <img width="641" height="155" alt="Screenshot 2026-04-30 111701" src="https://github.com/user-attachments/assets/f62d6592-8923-4c67-8544-e4e38be8cb95" />

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
<img width="399" height="187" alt="Screenshot 2026-04-30 111818" src="https://github.com/user-attachments/assets/a4c986a5-184e-4aae-8d87-864f34d19ade" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

$ ./exread1.sh
## OUTPUT

<img width="541" height="184" alt="Screenshot 2026-04-30 112008" src="https://github.com/user-attachments/assets/3ecef764-6baf-4534-8f02-08236e86ae36" />

 
 
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
<img width="515" height="318" alt="Screenshot 2026-04-30 112231" src="https://github.com/user-attachments/assets/4de77912-3645-431a-87a6-41ac7cb2da2a" />

 
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
 <img width="321" height="101" alt="Screenshot 2026-04-30 112346" src="https://github.com/user-attachments/assets/c150b1e5-fbaa-4057-b52e-d77e111a5031" />

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
 <img width="321" height="101" alt="Screenshot 2026-04-30 112346" src="https://github.com/user-attachments/assets/564d77d4-e87e-4fa2-a733-760639baf1a2" />

 
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
 <img width="434" height="415" alt="Screenshot 2026-04-30 112547" src="https://github.com/user-attachments/assets/25439dd1-a6ea-4d14-a5a0-8de539493859" />

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
<img width="486" height="362" alt="Screenshot 2026-04-30 112645" src="https://github.com/user-attachments/assets/fb512a38-21af-4ef9-a438-df7433e9a2b9" />
## OUTPUT 


# RESULT:
The Commands are executed successfully.
