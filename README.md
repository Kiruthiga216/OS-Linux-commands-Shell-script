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

![Screenshot from 2025-02-27 17-54-14](https://github.com/user-attachments/assets/b532614e-9fe9-4107-8ecf-5aac2c75bc8a)




cat < file2
## OUTPUT
![Screenshot from 2025-02-27 17-54-31](https://github.com/user-attachments/assets/40d94bdb-efbd-4d59-b419-1a3f6c15a453)


# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot from 2025-02-27 17-55-04](https://github.com/user-attachments/assets/47619b05-c77e-4242-a834-0fa0698f9538)

 
comm file1 file2
 ## OUTPUT
 ![Screenshot from 2025-02-27 17-55-23](https://github.com/user-attachments/assets/c7702b1a-066e-42e0-9f20-6b3d2f8e63b0)


 
diff file1 file2
## OUTPUT
![Screenshot from 2025-02-27 17-55-51](https://github.com/user-attachments/assets/dfa9b9fd-be73-4e8f-af4c-9720ebd6f56c)



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

![Screenshot from 2025-02-27 18-05-44](https://github.com/user-attachments/assets/059bb6db-7bc4-483c-9046-bc56409fea1f)



cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-02-27 18-06-04](https://github.com/user-attachments/assets/edf9d432-916c-45ac-8c73-83c70bdf3401)




cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-02-27 18-06-17](https://github.com/user-attachments/assets/3462a65a-4cc8-45bf-848b-4013d4754fbe)



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

![Screenshot from 2025-02-27 18-07-37](https://github.com/user-attachments/assets/edbfce9a-f378-4290-b740-0e3108b80bbd)



grep hello newfile 
## OUTPUT

![Screenshot from 2025-02-27 18-07-22](https://github.com/user-attachments/assets/966c8bb4-710f-4e96-908e-5f2184bc5505)



grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-02-27 18-07-50](https://github.com/user-attachments/assets/5a744f02-e73c-491e-9dc6-7323a4e54234)




cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2025-02-27 18-08-01](https://github.com/user-attachments/assets/4250bfd3-8333-4c9f-a37b-aec984e907c7)





cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2025-02-27 18-08-19](https://github.com/user-attachments/assets/3d11c04a-ccc2-4ff5-a68a-268b22778c1d)




grep -R ubuntu /etc
## OUTPUT

![Screenshot from 2025-03-03 09-23-05](https://github.com/user-attachments/assets/61f65b20-831a-40f3-970e-d4a9b9305648)


grep -w -n world newfile   
## OUTPUT
![Screenshot from 2025-02-27 18-08-39](https://github.com/user-attachments/assets/f445a998-7969-4451-98cc-009d0178d942)




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
![Screenshot from 2025-02-27 18-51-32](https://github.com/user-attachments/assets/34ec52fa-20c0-4bdb-8cd1-b23e3723d675)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2025-02-27 18-51-48](https://github.com/user-attachments/assets/fa0ed32e-84f0-410e-8447-3ed2a4af34eb)





egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot from 2025-02-27 18-52-03](https://github.com/user-attachments/assets/10382418-97cb-43eb-aef3-129aa80f45f1)



egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2025-02-27 18-52-20](https://github.com/user-attachments/assets/8841135b-85a7-45a8-9666-08703c832883)




egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2025-02-27 18-52-37](https://github.com/user-attachments/assets/db4d8f2b-d634-4260-988d-75c3a282a48f)




egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-02-27 18-52-54](https://github.com/user-attachments/assets/ea5dd31e-838f-4d8c-8d59-222742b3d698)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2025-02-27 18-53-06](https://github.com/user-attachments/assets/9431071a-49c4-4992-b804-9887ed5be198)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2025-02-27 18-53-19](https://github.com/user-attachments/assets/c5fc3174-d0b7-4cdf-8cba-54e7c28922bc)




egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-02-27 18-53-29](https://github.com/user-attachments/assets/6afb1bd7-9c86-4c4e-a63d-fd5f966b2fec)



egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2025-02-27 18-53-39](https://github.com/user-attachments/assets/a5a631b6-1326-4bb5-a332-e2e47ac7d8f0)



egrep l{2} newfile
## OUTPUT
![Screenshot from 2025-03-03 09-33-18](https://github.com/user-attachments/assets/45ba9e29-4679-4ed8-b9eb-986e18c93b39)




egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2025-03-03 09-33-28](https://github.com/user-attachments/assets/ee3500ba-7078-4e2c-b239-bb0448e40e3b)



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
![Screenshot from 2025-02-27 19-07-58](https://github.com/user-attachments/assets/47605da7-c673-419e-89c9-5b080d1b665a)



sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2025-02-27 19-08-08](https://github.com/user-attachments/assets/33319282-41f8-4225-b0aa-69f452454940)




sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-02-27 19-08-19](https://github.com/user-attachments/assets/109422e5-07ca-4908-a773-15598590a86e)




sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-02-27 19-08-28](https://github.com/user-attachments/assets/acb1b888-46f3-4837-a91b-72570b8b5c77)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot from 2025-02-27 19-08-36](https://github.com/user-attachments/assets/c2572b6b-0708-4c29-a8e3-b82377b1bc16)



sed -n -e '1,5p' file23
## OUTPUT

![Screenshot from 2025-02-27 19-09-21](https://github.com/user-attachments/assets/93f6293a-aa53-469c-96f5-70403c140d5f)




sed -n -e '2,/Joe/p' file23
## OUTPUT


![Screenshot from 2025-02-27 19-09-41](https://github.com/user-attachments/assets/f3c0d57f-4ace-4ea4-a732-85ee2f8bd2b2)






sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-02-27 19-09-28](https://github.com/user-attachments/assets/f31b6ddc-f689-4c3e-99ba-46214fa2ef24)




seq 10 
## OUTPUT

![Screenshot from 2025-02-27 19-09-48](https://github.com/user-attachments/assets/a3df73af-4988-4b70-baa0-7b1407bfa3a3)




seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot from 2025-02-27 19-10-05](https://github.com/user-attachments/assets/87eb122b-c5a5-4ba2-b690-377954cbf112)




seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot from 2025-02-27 19-10-13](https://github.com/user-attachments/assets/a35e752c-4f33-42ee-b6d0-cb6f82f4bd73)




seq 3 | sed '2a hello'
## OUTPUT

![Screenshot from 2025-02-27 19-10-22](https://github.com/user-attachments/assets/ec0f5d07-2e10-48b5-ac45-501fbb6812d1)



seq 2 | sed '2i hello'
## OUTPUT

![Screenshot from 2025-02-27 19-10-28](https://github.com/user-attachments/assets/2b23b750-7112-4134-a6bc-ccef56a07468)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2025-02-27 19-10-37](https://github.com/user-attachments/assets/0fafd9c5-18a6-4d64-8b3b-1fe4cd36dcf6)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2025-02-27 19-10-48](https://github.com/user-attachments/assets/2b66f38b-01d9-4580-935c-5b9e20a803b2)




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
![Screenshot from 2025-02-27 20-06-00](https://github.com/user-attachments/assets/97b3f279-23a7-45fb-ac5a-b5dbbc033449)


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
![Screenshot from 2025-02-27 20-06-19](https://github.com/user-attachments/assets/a579ec5f-8815-4538-b94b-1ed6368fb402)




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 ![Screenshot from 2025-02-27 20-06-32](https://github.com/user-attachments/assets/8fceac13-ed67-4195-8dce-d9a27e0051e0)


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
 ![Screenshot from 2025-02-27 20-07-03](https://github.com/user-attachments/assets/f3a19a7c-3564-4019-99c7-939588a7c0cc)



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2025-02-27 20-07-13](https://github.com/user-attachments/assets/0a2cec9f-7d81-4cdb-8528-c6fbf898cd64)



#Backup commands
tar -cvf backup.tar *
## OUTPUT

![Screenshot from 2025-03-03 18-42-53](https://github.com/user-attachments/assets/11ef7c5d-f0f5-4d56-8764-b3afdf6e7b19)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![Screenshot from 2025-03-03 18-43-10](https://github.com/user-attachments/assets/e4f20658-69e5-4bb6-a695-b72634967cc7)


tar -xvf backup.tar

gzip backup.tar

ls .gz
## OUTPUT

 ![Screenshot from 2025-03-03 18-43-28](https://github.com/user-attachments/assets/cadcad00-5929-497d-a1a9-40442f6edfc6)

gunzip backup.tar.gz
## OUTPUT


 ![Screenshot from 2025-03-03 18-43-42](https://github.com/user-attachments/assets/e66f1bd3-d63a-485a-b6dc-99035dc5ccd4)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT


 ![Screenshot from 2025-03-03 18-44-00](https://github.com/user-attachments/assets/216ec80e-5d81-4d2f-a1f3-af447cecf773)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![Screenshot from 2025-03-03 18-44-13](https://github.com/user-attachments/assets/9a6c1776-9838-4a9d-b9c8-0d697a337bb9)


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


 ![Screenshot from 2025-03-03 18-44-33](https://github.com/user-attachments/assets/3c6d9a2d-9777-4d2d-82c9-34e71ed0700d)

ls file1
## OUTPUT

![Screenshot from 2025-03-03 18-44-55](https://github.com/user-attachments/assets/116f6d62-d5a0-4375-93c4-e91ab142e05a)

echo $?
## OUTPUT 

![Screenshot from 2025-03-03 18-45-14](https://github.com/user-attachments/assets/a3677958-74b2-42d2-91b9-3a447b6122a8)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

![Screenshot from 2025-03-03 18-45-14](https://github.com/user-attachments/assets/d3d32396-db59-472d-83b9-dc594c6f7887)

 
abcd
 
echo $?
 ## OUTPUT


![Screenshot from 2025-03-03 18-45-29](https://github.com/user-attachments/assets/bcc3bfca-1ecd-4c3e-94bb-bc3d5267d966)

 
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


![Screenshot from 2025-03-03 18-46-14](https://github.com/user-attachments/assets/46d9ab61-5950-4b1a-9cac-f4281e8bd983)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![Screenshot from 2025-03-03 18-46-31](https://github.com/user-attachments/assets/f81234b0-7873-4365-aef1-3990fea542c8)



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

![Screenshot from 2025-03-03 18-47-00](https://github.com/user-attachments/assets/8b10e28a-7aca-4686-baf5-cf95c22e9b7f)

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

![Screenshot from 2025-03-03 18-47-15](https://github.com/user-attachments/assets/38447675-5b08-4b86-a133-5df316b92209)



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

![Screenshot from 2025-03-01 18-20-48](https://github.com/user-attachments/assets/3204b4cc-8f13-475f-9dc0-19b8a02d0824)


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

![Screenshot from 2025-03-03 18-48-03](https://github.com/user-attachments/assets/d14686ff-f981-4cda-ad87-cfa857dc991e)

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
![Screenshot from 2025-03-01 18-21-37](https://github.com/user-attachments/assets/38e95126-c721-4ec5-a56e-7493bf74c616)


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
![Screenshot from 2025-03-01 18-21-53](https://github.com/user-attachments/assets/67b480da-09ee-4c23-ae01-3edbffc152ce)

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
![Screenshot from 2025-03-01 18-43-59](https://github.com/user-attachments/assets/cfc1c8ae-76ab-4528-bc48-3a948a5a3ef8)

 
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
 ![Screenshot from 2025-03-01 18-44-21](https://github.com/user-attachments/assets/6135e3df-d4c5-4f8e-8f10-0ef22d398680)

 
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
 
 ![Screenshot from 2025-03-01 18-44-55](https://github.com/user-attachments/assets/258132cf-0d6f-4423-885c-b6bece0894b1)

 
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
 

 ![Screenshot from 2025-03-03 18-48-28](https://github.com/user-attachments/assets/fc270fd6-b89d-4d05-8fee-dbf04c63aea2)

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

 ![Screenshot from 2025-03-01 18-45-54](https://github.com/user-attachments/assets/9cbb9c04-6d7e-474d-98af-f64698c38ae0)

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

![Screenshot from 2025-03-03 18-49-12](https://github.com/user-attachments/assets/7716587a-c558-4dbe-a642-49d874ec119f)


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
![Screenshot from 2025-03-01 19-00-28](https://github.com/user-attachments/assets/6bd07d74-e59c-4847-a1ae-140a94aceee9)


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
![Screenshot from 2025-03-01 19-00-50](https://github.com/user-attachments/assets/492bd643-232f-4a8b-8ada-25b3a7b14df4)


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
![Screenshot from 2025-03-01 19-01-09](https://github.com/user-attachments/assets/ac3399a6-f9e8-48dd-943f-a9c21e387159)

 
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
![Screenshot from 2025-03-01 19-01-24](https://github.com/user-attachments/assets/95911383-71d5-488b-b355-6b33c78bbf85)


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
 ![Screenshot from 2025-03-01 19-01-42](https://github.com/user-attachments/assets/e2efc54c-d80a-4756-8dc1-22f0d687bfb5)

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

![Screenshot from 2025-03-01 19-16-12](https://github.com/user-attachments/assets/6b9d5472-5e5b-4a02-8b5c-ba436b2aa740)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT


![Screenshot from 2025-03-01 19-16-34](https://github.com/user-attachments/assets/28b6089c-34f0-4437-ae60-49aa0899cb51)


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

![Screenshot from 2025-03-03 18-49-34](https://github.com/user-attachments/assets/6dbfcc44-d56c-4325-bfb6-de1de0f04c3d)

 
 ./funcex.sh 1 2

 ![Screenshot from 2025-03-03 18-49-48](https://github.com/user-attachments/assets/39173d2e-859b-4d5e-9885-20dd59871dbe)


 
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

![Screenshot from 2025-03-01 19-17-33](https://github.com/user-attachments/assets/cab69592-d854-4340-ad26-cb46adac38ca)

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

![Screenshot from 2025-03-01 19-17-48](https://github.com/user-attachments/assets/615a3c4b-949a-4854-a1f7-d21b4fdd4ae0)

 ./argshift.sh 1 2 3
 

 ![Screenshot from 2025-03-01 19-18-06](https://github.com/user-attachments/assets/c6bf797d-07ae-44da-989b-d171ceaa7323)

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

![Screenshot from 2025-03-01 21-37-03](https://github.com/user-attachments/assets/3c699a89-cf6e-4a8a-b0a6-bbd556154e8a)

 
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

![Screenshot from 2025-03-01 21-37-43](https://github.com/user-attachments/assets/c1fd4963-d057-4a4b-a2a1-b53d2fb5802e)



# RESULT:
The Commands are executed successfully.
