### How to run your scripts from any directory in Ubuntu

##### Create the bin file
From you home directory:
```
cd ~
```
Create the file that will work as a command , in this case i used this to make quick and simple push to my git account:
```
#!/bin/sh
echo "Introduce your commit :"
read commit
git add . ;
git commit -m "Commit : $commit";
git push origin;
```
so i created this file :
```
~$ touch gitpush
```
Now we will edit our file and make it an executable script to run my git commands:
```
~$ sudo chmod +wrx gitpush
```
##### Edit your file



Now we will edit the content of our file/command
```
~$ code gitpush
```
We paste the next code , as a bash script

```
#!/bin/sh
echo "Introduce your commit :"
read commit
git add . ;
git commit -m "Commit : $commit";
git push origin;
```
##### Move your file to /bin
Note : It is important to create the file in a diferent directory first , since the /bin directory requires admin permissions and this makes harder to edit the file directly in there.

Next we have to move our file/command to the /bin directory (This is where all the executable commands are located )
```
~$ sudo mv gitpush /bin
```
and that’s it , now every time i run :
```
~$ gitpush
```
I get my changes added , commited and pushed to my repo in github.
With a little imagination and needs you could use this script execution way to make simplier any repetitive task you do often.

— — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — Tark