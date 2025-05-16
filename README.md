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
![1](https://github.com/user-attachments/assets/31c3e109-98ea-4596-a925-c69ee8298c18)



cat < file2
## OUTPUT

![2](https://github.com/user-attachments/assets/83981bec-32ca-44ad-a333-2661cb09ec36)



# Comparing Files
cmp file1 file2
## OUTPUT
 ![3](https://github.com/user-attachments/assets/4e4f50fc-3078-4ed6-a046-43fda8dc7bc5)

comm file1 file2
 ## OUTPUT

 ![4](https://github.com/user-attachments/assets/8d1f0b79-6df2-4b61-b0f5-9aff9728a354)

diff file1 file2
## OUTPUT
![5](https://github.com/user-attachments/assets/8596dfc2-b81f-48e5-986f-6326dcf9108a)


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

![6](https://github.com/user-attachments/assets/23b39ce3-c225-4bf7-8467-f888085414a3)



cut -d "|" -f 1 file22
## OUTPUT

![7](https://github.com/user-attachments/assets/8cd45220-6e18-405b-82e0-48b75bbf4cd3)


cut -d "|" -f 2 file22
## OUTPUT
![8](https://github.com/user-attachments/assets/a9f716a4-86f7-40a4-9b21-36851ffb6056)


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

![9](https://github.com/user-attachments/assets/237f716a-e113-478e-aa27-673e445dc5ce)


grep hello newfile 
## OUTPUT


![10](https://github.com/user-attachments/assets/f3eeaace-a219-4f24-8b59-e14ad26f5e6e)


grep -v hello newfile 
## OUTPUT

![11](https://github.com/user-attachments/assets/af0657a7-fed7-4f4f-b0ac-8891496cef19)


cat newfile | grep -i "hello"
## OUTPUT

![12](https://github.com/user-attachments/assets/6b6b7985-e9b6-4167-9f44-a092fd04e8cd)



cat newfile | grep -i -c "hello"
## OUTPUT

![13](https://github.com/user-attachments/assets/1de00a64-a24e-475a-a4b6-be2608be97b9)



grep -R ubuntu /etc
## OUTPUT
![14](https://github.com/user-attachments/assets/7d21a27d-eabf-4aab-a490-6af79a5cacb6)



grep -w -n world newfile   
## OUTPUT
![15](https://github.com/user-attachments/assets/b7329c69-d656-40d9-a9b9-36a8bdc7dc64)


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

![16](https://github.com/user-attachments/assets/f87881ee-e8c6-427b-803a-3e39b7fd7a83)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![17](https://github.com/user-attachments/assets/ca2f788d-23a1-46ce-8306-31d051a0ea35)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![18](https://github.com/user-attachments/assets/565fa435-447a-43b0-850a-e40519755488)



egrep '(^hello)' newfile 
## OUTPUT

![19](https://github.com/user-attachments/assets/49c4b10b-7c45-4df4-9df0-7d2f467f6a06)


egrep '(world$)' newfile 
## OUTPUT

![20](https://github.com/user-attachments/assets/d84fcfa2-d2b5-49dc-a803-c229260aafce)


egrep '(World$)' newfile 
## OUTPUT

![21](https://github.com/user-attachments/assets/1d4c7658-cda7-4d6b-a980-2b9f403a3b8a)


egrep '((W|w)orld$)' newfile 
## OUTPUT


![22](https://github.com/user-attachments/assets/0c819457-ab43-41c7-958a-94ae0eca34b4)



egrep '[1-9]' newfile 
## OUTPUT

![23](https://github.com/user-attachments/assets/9a7c68ac-e9c8-4161-be00-6ca0f9071e60)



egrep 'Linux.*world' newfile 
## OUTPUT

![24](https://github.com/user-attachments/assets/aa724427-b5fb-4d0e-a64d-65d9789a5d0e)


egrep 'Linux.*World' newfile 
## OUTPUT

![25](https://github.com/user-attachments/assets/9e6c3a64-adca-474a-9c06-1e881abded39)

egrep l{2} newfile
## OUTPUT

![26](https://github.com/user-attachments/assets/c98d5a7b-e66e-4150-ab2d-cd87d1b46211)


egrep 's{1,2}' newfile
## OUTPUT 

![27](https://github.com/user-attachments/assets/0f75b71e-2729-4b04-9950-4253071ca791)


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

![28](https://github.com/user-attachments/assets/3ca0cfaa-f714-4383-b1e2-e92e1c36961b)



sed -n -e '$p' file23
## OUTPUT

![29](https://github.com/user-attachments/assets/64cf7a21-360d-4003-b872-48b66a60e726)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![30](https://github.com/user-attachments/assets/cc39042a-21d7-47a3-8e51-886c7cca566a)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![31](https://github.com/user-attachments/assets/35db3d5b-2a80-4a4b-8a92-d0640f8881de)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![32](https://github.com/user-attachments/assets/a9c943b8-1374-42a7-9e8a-17607ded8799)



sed -n -e '1,5p' file23
## OUTPUT

![33](https://github.com/user-attachments/assets/48d312d0-528c-4213-abdf-c6d75e870234)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![34](https://github.com/user-attachments/assets/44ecfe9a-21d5-42fd-9175-3bc2c7a4d098)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![35](https://github.com/user-attachments/assets/7005e4df-d6e8-4f06-8e4e-a654ee45dcff)


seq 10 
## OUTPUT

![36](https://github.com/user-attachments/assets/34f6159f-8e7f-4d3e-88f9-3a6f37a9cd50)


seq 10 | sed -n '4,6p'
## OUTPUT

![37](https://github.com/user-attachments/assets/bb0fa15b-879d-4a0a-bb56-5546bbb02c4e)



seq 10 | sed -n '2,~4p'
## OUTPUT

![38](https://github.com/user-attachments/assets/114d3901-69fe-4c6e-98c5-c34c11dc1742)



seq 3 | sed '2a hello'
## OUTPUT

![39](https://github.com/user-attachments/assets/8cc8c42a-b8ba-490f-b166-490d5ff28d1f)


seq 2 | sed '2i hello'
## OUTPUT
![40](https://github.com/user-attachments/assets/4271a37d-65db-4861-967f-f76e3f9915bf)


seq 10 | sed '2,9c hello'
## OUTPUT

![41](https://github.com/user-attachments/assets/cd9d4058-1450-4c3f-a725-dd1a3e7d5324)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![42](https://github.com/user-attachments/assets/63fb6393-cf23-4c85-a015-0cf002a746ab)


sed -n '2,4{s/$/*/;p}' file23

![43](https://github.com/user-attachments/assets/a2272ec2-94f0-4970-9c18-db7f5cf35b3c)


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
![44](https://github.com/user-attachments/assets/8a7c34c1-5cce-4020-a813-9ad45abd7bb2)


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
![45](https://github.com/user-attachments/assets/57bad73f-3a84-47bc-851f-d0a1d9cd473d)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![46](https://github.com/user-attachments/assets/a8468c2a-abcc-4c00-a705-28c00b8c8f06)

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

![47](https://github.com/user-attachments/assets/35370159-40a2-471a-8c1d-2432ec25898a)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![48](https://github.com/user-attachments/assets/d821d105-b8b8-4f0e-8669-649bb1a7aba8)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![back](https://github.com/user-attachments/assets/4706aba3-9d78-418c-b619-1182d1407736)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![backup1](https://github.com/user-attachments/assets/4fe4239a-63df-4ea2-a0f7-b571b53cbe87)


tar -xvf backup.tar
## OUTPUT
![backup2](https://github.com/user-attachments/assets/b463ced6-3fe9-454a-9537-d12df09e805b)


gzip backup.tar

ls .gz
## OUTPUT
 ![gz1](https://github.com/user-attachments/assets/1a8b1392-41f9-4ee7-b0f8-36bc2dff782d)

gunzip backup.tar.gz
## OUTPUT
![gz2](https://github.com/user-attachments/assets/27853df5-3d6d-4b15-95b3-9bc59431e3a2)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![50 - shell script](https://github.com/user-attachments/assets/9c706711-202a-4d04-9280-a201c4851b24)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![51](https://github.com/user-attachments/assets/36f7121f-53ab-49f2-b846-c4f71de0fadd)


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
![52](https://github.com/user-attachments/assets/74306290-7688-4a62-a073-8bd7785be73f)

 
ls file1
## OUTPUT
![53](https://github.com/user-attachments/assets/27623c8d-63cf-423e-a9a5-f222d4e2c27e)

echo $?
## OUTPUT

![54](https://github.com/user-attachments/assets/e96593bb-4505-4280-adb4-ad4262844f4d)

./one bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![55](https://github.com/user-attachments/assets/3b957b71-09b9-4049-94e4-dbb11130a4db)

abcd
 
echo $?
 ## OUTPUT
![56](https://github.com/user-attachments/assets/47db6d58-013c-4b30-b165-4f83cde15b9e)


 
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

![57](https://github.com/user-attachments/assets/e444088a-16d1-4365-90b0-55f8889b910e)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![58](https://github.com/user-attachments/assets/2990bb93-9305-4e71-9a9f-223ebcce570a)


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
![59](https://github.com/user-attachments/assets/f30f2546-71ab-4d8d-92a3-30c84819d9cf)

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

![60](https://github.com/user-attachments/assets/77be58a6-cd74-417a-b840-a9e03f387283)


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


![1_](https://github.com/user-attachments/assets/c4d26279-f1c2-4da0-9f5b-d22f82ce1d15)

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


![61](https://github.com/user-attachments/assets/7e48c41c-f78d-4e41-9801-4154250dc54f)

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


![62](https://github.com/user-attachments/assets/997be490-0319-4518-a46e-60dcabae9e2c)


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



![63](https://github.com/user-attachments/assets/639c93a1-f24b-4771-b6b4-e3c8339f5c49)

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


![65](https://github.com/user-attachments/assets/234dedbb-b143-4de5-8106-a38ce5263f69)

 
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

 
![66](https://github.com/user-attachments/assets/7c978a55-784c-42bd-a45a-1f4f17a68295)

 
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
 
![67](https://github.com/user-attachments/assets/8bdb5cad-5e43-4d31-a39e-28b71492a443)

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


![67](https://github.com/user-attachments/assets/cb8bf1ab-8c16-4c6d-b309-65daf6100839)

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


![68](https://github.com/user-attachments/assets/68d3ba47-1b9a-41ce-88cb-af31b29047c3)

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


![69](https://github.com/user-attachments/assets/07282296-d205-41a0-b5de-c25ccc969ce2)

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


![70](https://github.com/user-attachments/assets/d21987cc-a560-4133-b1f9-a5be866e0ad4)


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


![71](https://github.com/user-attachments/assets/5c8529f1-55d3-4658-9282-a49024795900)


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


![72](https://github.com/user-attachments/assets/4b40b642-87ac-4068-81b3-bf9a987aa7c2)

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


![73](https://github.com/user-attachments/assets/8353d3b7-f7e0-44c0-898d-e7440d4884d6)

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

 
![74](https://github.com/user-attachments/assets/59dfca10-a92e-4b64-9ab1-dbe0778d93ab)

 
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


![75](https://github.com/user-attachments/assets/010c56d8-5ba1-49f5-87e4-da99e365e823)

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


![76](https://github.com/user-attachments/assets/68bdeb62-8daa-4bec-8d84-ae5062331f63)

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

![77](https://github.com/user-attachments/assets/9ed4866d-7e93-403a-b595-6e3569c43aff)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![78](https://github.com/user-attachments/assets/f4678e90-9ca8-4fe8-80cb-311f23da823f)


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
 
![79](https://github.com/user-attachments/assets/5733861c-187d-43b5-8d43-d258acb2a4c6)

 
 ./funcex.sh 1 2
 
![80](https://github.com/user-attachments/assets/cb96e98e-9fa7-4cfc-bab6-8ec4997ff04a)

 
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

![81](https://github.com/user-attachments/assets/f68351dd-d8a8-4043-a151-8dc9c3eea0ff)

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


![82](https://github.com/user-attachments/assets/2b929cff-293b-4b3a-96f5-ce00d6aa2247)

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


![83](https://github.com/user-attachments/assets/0b270027-4238-4633-9aea-bd3edebd360d)

 
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

![84](https://github.com/user-attachments/assets/35e8099e-b089-4633-86b0-b3e7e11a61b7)

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

![85](https://github.com/user-attachments/assets/ec20b912-6a2f-4768-94b9-a973e2646ec0)


# RESULT:
The Commands are executed successfully.
