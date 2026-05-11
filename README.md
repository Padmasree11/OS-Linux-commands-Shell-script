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
<img width="601" height="150" alt="Screenshot 2026-05-10 222834" src="https://github.com/user-attachments/assets/ba4f993b-d7db-4e0d-b8ff-0718e0c0f6dc" />

cat < file2
## OUTPUT
<img width="625" height="174" alt="Screenshot 2026-05-10 222857" src="https://github.com/user-attachments/assets/9f1afc90-10a9-4bbf-9dcc-5034e386e25a" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="660" height="234" alt="Screenshot 2026-05-10 222917" src="https://github.com/user-attachments/assets/4aa7a192-d9f8-460a-8f47-9e4420a9cc7a" />

 
comm file1 file2
 ## OUTPUT
 <img width="732" height="286" alt="Screenshot 2026-05-10 222935" src="https://github.com/user-attachments/assets/1186b693-7d11-43ca-8b15-4cab8fb72a70" />
diff file1 file2
## OUTPUT
<img width="520" height="216" alt="Screenshot 2026-05-10 223151" src="https://github.com/user-attachments/assets/a879ede9-ee54-4bd0-9510-98641d240953" />

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
<img width="366" height="113" alt="Screenshot 2026-05-10 223207" src="https://github.com/user-attachments/assets/8f2bf670-1649-45a6-b7e5-e5ac57079bf1" />


cut -d "|" -f 1 file22
## OUTPUT
<img width="460" height="136" alt="Screenshot 2026-05-10 223214" src="https://github.com/user-attachments/assets/172b6c65-9e21-4de0-aabd-fa7643644b5d" />


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

<img width="420" height="186" alt="Screenshot 2026-05-10 223225" src="https://github.com/user-attachments/assets/b2182b12-62b5-4f5a-8b5c-485d296ccfbb" />

<img width="508" height="80" alt="Screenshot 2026-05-10 223232" src="https://github.com/user-attachments/assets/522fb6ea-58c6-4102-8926-34bfe9e39d5d" />

grep hello newfile 
## OUTPUT

<img width="442" height="153" alt="Screenshot 2026-05-10 223247" src="https://github.com/user-attachments/assets/75210ecd-31ce-4d59-82fc-46e92243075c" />



grep -v hello newfile 
## OUTPUT

<img width="528" height="112" alt="Screenshot 2026-05-10 223307" src="https://github.com/user-attachments/assets/02572f65-fbde-41d9-93ec-0562b7b8053a" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="543" height="74" alt="Screenshot 2026-05-10 223314" src="https://github.com/user-attachments/assets/d646d929-89be-4e57-b267-0d8762cf9526" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="803" height="605" alt="Screenshot 2026-05-10 223332" src="https://github.com/user-attachments/assets/480b7c65-a394-41a0-b897-3df005ada12f" />


grep -R ubuntu /etc
## OUTPUT

<img width="402" height="122" alt="Screenshot 2026-05-10 223347" src="https://github.com/user-attachments/assets/eddcf2ab-21d7-46ac-856c-2b65959cb598" />


grep -w -n world newfile   
## OUTPUT

<img width="484" height="348" alt="Screenshot 2026-05-10 223441" src="https://github.com/user-attachments/assets/746f41b1-2363-4d54-aec4-b664abc54cbe" />

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
<img width="454" height="98" alt="Screenshot 2026-05-10 223447" src="https://github.com/user-attachments/assets/622b7b03-dd07-49b5-b99e-5f2d6382aa86" />

## OUTPUT

<img width="539" height="101" alt="Screenshot 2026-05-10 223512" src="https://github.com/user-attachments/assets/fe3146af-13ac-4a82-a451-6834cf0db3a5" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="463" height="79" alt="Screenshot 2026-05-10 223525" src="https://github.com/user-attachments/assets/7c804014-9843-49cf-8e89-d363f12b6ab4" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="463" height="79" alt="Screenshot 2026-05-10 223525" src="https://github.com/user-attachments/assets/7186b0a5-1ff1-4d83-a44a-19f2949ea4b9" />


egrep '(^hello)' newfile 
## OUTPUT
<img width="616" height="122" alt="Screenshot 2026-05-10 223536" src="https://github.com/user-attachments/assets/c00e9b0c-51fe-4a5f-a818-d0cf2d85cef7" />



egrep '(world$)' newfile 
## OUTPUT

<img width="616" height="122" alt="Screenshot 2026-05-10 223536" src="https://github.com/user-attachments/assets/65a20f44-fb0f-4309-98bb-b6535232100e" />


egrep '(World$)' newfile 
## OUTPUT

<img width="471" height="124" alt="Screenshot 2026-05-10 223551" src="https://github.com/user-attachments/assets/7fb4b34a-0ec6-4170-9a23-032fbd551c05" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="465" height="69" alt="Screenshot 2026-05-10 223559" src="https://github.com/user-attachments/assets/1e4e0eb5-d1d2-41fe-a31b-b9cac3abe99d" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="461" height="80" alt="Screenshot 2026-05-10 223610" src="https://github.com/user-attachments/assets/a4600655-8916-4963-9ede-e119ac440d21" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="487" height="61" alt="Screenshot 2026-05-10 223618" src="https://github.com/user-attachments/assets/a78c6ef0-8b87-4bfe-8de8-8f133b607167" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="418" height="99" alt="Screenshot 2026-05-10 223653" src="https://github.com/user-attachments/assets/85800d7c-42fa-4b92-b1a4-6c83451f41d3" />

egrep l{2} newfile
## OUTPUT



egrep 's{1,2}' newfile
## OUTPUT 
<img width="422" height="497" alt="Screenshot 2026-05-10 224000" src="https://github.com/user-attachments/assets/6c3f66ed-25bb-4200-8130-8d3cefebe1e1" />


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
<img width="480" height="79" alt="Screenshot 2026-05-10 224010" src="https://github.com/user-attachments/assets/7bbe4662-02ab-4bcd-b4d0-f301c59b3896" />


sed -n -e '3p' file23
## OUTPUT

<img width="418" height="99" alt="Screenshot 2026-05-10 223653" src="https://github.com/user-attachments/assets/e3b6cd4e-ca37-4747-b991-fbc66313fd15" />


sed -n -e '$p' file23
## OUTPUT

<img width="562" height="253" alt="Screenshot 2026-05-10 224032" src="https://github.com/user-attachments/assets/65eda700-2aa0-4ac8-ac6a-65a854ed7bae" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="621" height="259" alt="Screenshot 2026-05-10 224040" src="https://github.com/user-attachments/assets/b838f3a4-6165-4d4a-b4ea-4a0829b67847" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="534" height="251" alt="Screenshot 2026-05-10 224107" src="https://github.com/user-attachments/assets/fff9ad12-75c6-4580-a73e-00969fcdce65" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="485" height="180" alt="Screenshot 2026-05-10 224116" src="https://github.com/user-attachments/assets/94705446-599d-45be-abc7-792159c38be2" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="545" height="136" alt="Screenshot 2026-05-10 224133" src="https://github.com/user-attachments/assets/0099a0d3-1926-4b68-94d8-fbc73dc852b7" />


sed -n -e '2,/Joe/p' file23
## OUTPUT



<img width="579" height="114" alt="Screenshot 2026-05-10 224140" src="https://github.com/user-attachments/assets/3b06b5ac-c4b4-4753-8b91-1642261950aa" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="579" height="114" alt="Screenshot 2026-05-10 224140" src="https://github.com/user-attachments/assets/be806d3c-980c-4627-acd7-0ebf7f4910ee" />


seq 10 
## OUTPUT



<img width="505" height="139" alt="Screenshot 2026-05-10 224158" src="https://github.com/user-attachments/assets/f92f2c18-c5cd-43cd-b331-14a16de129db" />

seq 10 | sed -n '4,6p'
## OUTPUT



<img width="469" height="126" alt="Screenshot 2026-05-10 224203" src="https://github.com/user-attachments/assets/bbda7deb-41ae-4c0d-9820-f2a8e4a7cc06" />

seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="493" height="155" alt="Screenshot 2026-05-10 224208" src="https://github.com/user-attachments/assets/533fd931-0d3f-4c47-b1b4-c53ec8cdf956" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="479" height="143" alt="Screenshot 2026-05-10 224215" src="https://github.com/user-attachments/assets/13773fb6-d2fb-453f-9d9c-1ef5dac2f627" />



seq 2 | sed '2i hello'
## OUTPUT


<img width="517" height="129" alt="Screenshot 2026-05-10 224227" src="https://github.com/user-attachments/assets/d8ea32cd-f8fb-45e9-8d02-61f810fa60d2" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="601" height="137" alt="Screenshot 2026-05-10 224232" src="https://github.com/user-attachments/assets/0d81f2fc-c053-4761-bbf1-7c0d842969fc" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="531" height="126" alt="Screenshot 2026-05-10 224243" src="https://github.com/user-attachments/assets/0fa8eac6-d087-4a36-9e9c-f158240187cf" />


sed -n '2,4{s/$/*/;p}' file23


#Sorting File content

<img width="516" height="177" alt="Screenshot 2026-05-10 224305" src="https://github.com/user-attachments/assets/12dd8d92-007e-403b-b1bf-4848b95c4756" />

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

<img width="555" height="195" alt="Screenshot 2026-05-10 224310" src="https://github.com/user-attachments/assets/61b274e9-b50e-4607-a3db-bd57ba0d80f2" />



cat > file22

<img width="513" height="210" alt="Screenshot 2026-05-10 224320" src="https://github.com/user-attachments/assets/ee49ac08-edb9-452f-a67b-c80946dd9ef7" />

```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22

<img width="568" height="181" alt="Screenshot 2026-05-10 224323" src="https://github.com/user-attachments/assets/63e64765-0303-41e7-a607-8536114eeab4" />

## OUTPUT

<img width="570" height="258" alt="Screenshot 2026-05-10 224341" src="https://github.com/user-attachments/assets/041775a3-889a-47df-a786-ead06558b027" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 <img width="685" height="257" alt="Screenshot 2026-05-10 224346" src="https://github.com/user-attachments/assets/fc50c137-b548-4ec5-9b1e-a11aa45890d3" />


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


<img width="426" height="139" alt="Screenshot 2026-05-10 224415" src="https://github.com/user-attachments/assets/6f1a1f82-51ac-4e20-afb6-755de21ebf99" />

<img width="477" height="134" alt="Screenshot 2026-05-10 224420" src="https://github.com/user-attachments/assets/14340bbc-4fc4-443d-a538-d86684fe107e" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="556" height="129" alt="Screenshot 2026-05-10 224430" src="https://github.com/user-attachments/assets/563aea0a-fa5c-4689-ad12-8755371f96cc" />




#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="805" height="599" alt="Screenshot 2026-05-10 224446" src="https://github.com/user-attachments/assets/70b6d1d0-00b7-4337-a17a-85d0b5dd4ce5" />



mkdir backupdir
 
mv backup.tar backupdir

<img width="809" height="604" alt="Screenshot 2026-05-10 224513" src="https://github.com/user-attachments/assets/be259b96-732c-411a-8234-343f8796b854" />


cd backupdir
 
tar -tvf backup.tar

<img width="596" height="254" alt="Screenshot 2026-05-10 224553" src="https://github.com/user-attachments/assets/fa519053-6e39-440f-acfd-6d7b5df0b64e" />

## OUTPUT

<img width="558" height="164" alt="Screenshot 2026-05-10 224600" src="https://github.com/user-attachments/assets/6db7d1f5-d5e4-4d30-bc3e-acb6606f8831" />



tar -xvf backup.tar
## OUTPUT

gzip backup.tar

<img width="596" height="254" alt="Screenshot 2026-05-10 224553" src="https://github.com/user-attachments/assets/6b246879-590a-4a2c-b100-c7e26cfdb32c" />

ls .gz
## OUTPUT
 
gunzip backup.tar.gz

<img width="596" height="254" alt="Screenshot 2026-05-10 224553" src="https://github.com/user-attachments/assets/d5938af7-bd3a-4a2f-bbe5-3af98b445435" />

## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT


 <img width="581" height="138" alt="Screenshot 2026-05-10 224604" src="https://github.com/user-attachments/assets/fb1e577f-733c-486d-9efd-1f4eb4dad521" />

cat << stop > herecheck.txt

<img width="558" height="164" alt="Screenshot 2026-05-10 224600" src="https://github.com/user-attachments/assets/2ed241f6-6e19-4da1-beae-55407564538d" />

```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt

<img width="581" height="138" alt="Screenshot 2026-05-10 224604" src="https://github.com/user-attachments/assets/7df9755e-af06-4d7f-8719-ec69781cbea4" />

## OUTPUT


<img width="789" height="600" alt="Screenshot 2026-05-10 224726" src="https://github.com/user-attachments/assets/bca8fe21-ead7-4f6a-9392-e4abca764831" />

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

 <img width="789" height="600" alt="Screenshot 2026-05-10 224726" src="https://github.com/user-attachments/assets/ce37ecb3-0082-411a-85e7-f3a18b02f0ed" />

chmod 777 scriptest.sh

 <img width="659" height="434" alt="Screenshot 2026-05-10 224751" src="https://github.com/user-attachments/assets/bdd7618c-9613-420d-9fc9-8a3f17019c67" />

./scriptest.sh 1 2 3

<img width="659" height="434" alt="Screenshot 2026-05-10 224751" src="https://github.com/user-attachments/assets/48680c70-12ee-4755-bed9-1b06edb0358d" />


## OUTPUT


 <img width="415" height="88" alt="Screenshot 2026-05-10 224757" src="https://github.com/user-attachments/assets/dcd9bfa8-b077-4e1f-8166-52abb34a9a70" />

ls file1
## OUTPUT

<img width="479" height="75" alt="Screenshot 2026-05-10 224802" src="https://github.com/user-attachments/assets/d877e633-3c85-4155-b1ef-9dbda30982d2" />


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd



 
echo $?
 ## OUTPUT


 
# mis-using string comparisons

<img width="562" height="276" alt="Screenshot 2026-05-10 224837" src="https://github.com/user-attachments/assets/e2efb255-9c82-412e-bda8-588d26dc6ac5" />

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

<img width="562" height="276" alt="Screenshot 2026-05-10 224837" src="https://github.com/user-attachments/assets/06f24836-3a82-4e09-b048-7c062e109ac0" />


<img width="504" height="281" alt="Screenshot 2026-05-10 224856" src="https://github.com/user-attachments/assets/cbd60b69-d46e-4ac8-8a22-c2342b5b8fbb" />


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

<img width="704" height="233" alt="Screenshot 2026-05-10 224916" src="https://github.com/user-attachments/assets/060a9852-cd59-4859-b25e-2282e3465d62" />

<img width="723" height="236" alt="Screenshot 2026-05-10 224922" src="https://github.com/user-attachments/assets/c725b702-e3b1-42c6-acab-0a7ecc127d18" />


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

<img width="771" height="577" alt="Screenshot 2026-05-10 224941" src="https://github.com/user-attachments/assets/8adac131-9fc0-4830-ac76-de219ddbd99c" />




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

<img width="631" height="527" alt="Screenshot 2026-05-10 224949" src="https://github.com/user-attachments/assets/e0686012-9b86-42a5-89d9-71de193c6cd6" />


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

<img width="609" height="609" alt="Screenshot 2026-05-10 225011" src="https://github.com/user-attachments/assets/bdda5c7f-44ab-46f0-b6f2-170514ff1ef4" />


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

<img width="605" height="501" alt="Screenshot 2026-05-10 225023" src="https://github.com/user-attachments/assets/73fd2cdf-4926-4f75-bd88-649a315a5a79" />



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

<img width="580" height="302" alt="Screenshot 2026-05-10 225032" src="https://github.com/user-attachments/assets/a0bd9eb1-b81a-430d-a4c9-768ff0b184a1" />


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

<img width="643" height="385" alt="Screenshot 2026-05-10 225042" src="https://github.com/user-attachments/assets/f82ca4f4-59a5-4244-ae49-5500fbfaaf8d" />

cat forinfile.sh 

<img width="703" height="559" alt="Screenshot 2026-05-10 225055" src="https://github.com/user-attachments/assets/963d959a-bc39-49a8-bfe5-c4ca15e5b01a" />

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

<img width="703" height="559" alt="Screenshot 2026-05-10 225055" src="https://github.com/user-attachments/assets/580c1261-92df-48a3-80b1-4bcbc009fda8" />

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

<img width="664" height="212" alt="Screenshot 2026-05-10 225254" src="https://github.com/user-attachments/assets/81519908-8eae-40dd-8483-2aa9e2856a29" />

## OUTPUT

<img width="703" height="559" alt="Screenshot 2026-05-10 225055" src="https://github.com/user-attachments/assets/a827f7c3-ff59-40d2-9efd-540ced75041d" />

cat fornested1.sh 

<img width="664" height="212" alt="Screenshot 2026-05-10 225254" src="https://github.com/user-attachments/assets/2e28c0b8-dc96-48bf-97f6-c7c036e8ec49" />

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

<img width="657" height="336" alt="Screenshot 2026-05-10 225339" src="https://github.com/user-attachments/assets/e96c4ce3-ab14-47c7-ad9e-42edfb9a161a" />

 
$ ./fornested1.sh 

<img width="572" height="333" alt="Screenshot 2026-05-10 225332" src="https://github.com/user-attachments/assets/75c69790-2a01-4bca-9275-0e70e2803d25" />

 ## OUTPUT

 <img width="703" height="559" alt="Screenshot 2026-05-10 225055" src="https://github.com/user-attachments/assets/380f2569-189d-43f8-98f5-b39ca668bb69" />


 
cat forbreak.sh 

<img width="570" height="329" alt="Screenshot 2026-05-10 225316" src="https://github.com/user-attachments/assets/ac39bc67-83c5-4233-aaeb-8be2a735a5fe" />

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

<img width="609" height="336" alt="Screenshot 2026-05-10 225309" src="https://github.com/user-attachments/assets/d248a38b-cc57-45f5-aaaa-f19480879aea" />

 
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

<img width="703" height="559" alt="Screenshot 2026-05-10 225055" src="https://github.com/user-attachments/assets/57d177d2-00a0-4ef3-aeb5-dbe7099239de" />

 
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

<img width="703" height="559" alt="Screenshot 2026-05-10 225055" src="https://github.com/user-attachments/assets/db13edfa-f7ba-4160-8be5-76ad3f542e06" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="703" height="559" alt="Screenshot 2026-05-10 225055" src="https://github.com/user-attachments/assets/7e00ebe3-2a9c-41a8-bc4b-960b4476f115" />




$ ./exread1.sh 

<img width="585" height="166" alt="Screenshot 2026-05-10 225348" src="https://github.com/user-attachments/assets/a31329bf-eb0d-4f03-80ac-7bd99c084595" />

 
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

 <img width="719" height="347" alt="Screenshot 2026-05-10 225402" src="https://github.com/user-attachments/assets/d7912235-9181-4597-9ae5-e332dc5f7ff7" />


 
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

<img width="703" height="559" alt="Screenshot 2026-05-10 225055" src="https://github.com/user-attachments/assets/3a572d5f-36e1-4c21-b46f-831e92ea69cf" />

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

<img width="582" height="184" alt="Screenshot 2026-05-10 225429" src="https://github.com/user-attachments/assets/73c0bc4f-11eb-4a2d-8b0f-d737af86e64a" />

$ ./argshift.sh 1 2 3

<img width="511" height="192" alt="Screenshot 2026-05-10 225418" src="https://github.com/user-attachments/assets/28cc4ffa-e501-40ac-ae5a-da9b8ac6e78f" />

 
cat argshift.sh

<img width="387" height="198" alt="Screenshot 2026-05-10 225412" src="https://github.com/user-attachments/assets/bc6ece5f-ae2b-495b-bb98-e270510e952d" />

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

 <img width="613" height="400" alt="Screenshot 2026-05-10 225445" src="https://github.com/user-attachments/assets/4d207390-f58b-4c43-966e-1e377408580e" />

 
 
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

<img width="555" height="335" alt="Screenshot 2026-05-10 225450" src="https://github.com/user-attachments/assets/e36dc01b-4c77-452f-95dd-0af01751a59f" />


 <img width="574" height="302" alt="Screenshot 2026-05-10 225456" src="https://github.com/user-attachments/assets/9a3fea7c-7d17-417b-8681-1d3a3d861145" />

 <img width="831" height="377" alt="Screenshot 2026-05-10 225502" src="https://github.com/user-attachments/assets/b7c90a47-0506-4713-8ad2-14da37ad1617" />


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


<img width="737" height="586" alt="Screenshot 2026-05-10 225512" src="https://github.com/user-attachments/assets/794d5535-9108-4b54-a513-2714dc6e01ab" />


<img width="528" height="184" alt="Screenshot 2026-05-10 225520" src="https://github.com/user-attachments/assets/c6607a3d-d61a-4279-9d74-7de7d51b8edd" />

# RESULT:
The Commands are executed successfully.
