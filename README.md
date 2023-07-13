## Homework Linux terminal (GitBash) - part 1
**1. See the current working directory path**
```
$ pwd
/c/QA
```
**2. Create directory**
```
AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA
$ mkdir dir_1

AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA
$ ls -l
total 0
drwxr-xr-x 1 AnDer 197121 0 Apr 16 22:15 dir_1/
```
**3. Go to the directory, which was created**
```
$ cd dir_1

AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA/dir_1
```
**4. Create 3 directories**
```
$ mkdir dir_11 dir_12 dir_13

AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA/dir_1
$ ls -l
total 0
drwxr-xr-x 1 AnDer 197121 0 Apr 16 22:24 dir_11/
drwxr-xr-x 1 AnDer 197121 0 Apr 16 22:24 dir_12/
drwxr-xr-x 1 AnDer 197121 0 Apr 16 22:24 dir_13/
```
**5. Go to any directory**
```
AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA/dir_1
$ cd ../dir_2

AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA/dir_2
```
**6. Create 5 files: 3 txt, 2 json**
```
AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA/dir_2
$ touch 1.txt 2.txt 3.txt 4.json 5.json

AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA/dir_2
$ ls -l
total 0
-rw-r--r-- 1 AnDer 197121 0 Apr 16 23:20 1.txt
-rw-r--r-- 1 AnDer 197121 0 Apr 16 23:20 2.txt
-rw-r--r-- 1 AnDer 197121 0 Apr 16 23:20 3.txt
-rw-r--r-- 1 AnDer 197121 0 Apr 16 23:20 4.json
-rw-r--r-- 1 AnDer 197121 0 Apr 16 23:20 5.json
```
**7. Create 3 directories**
```
AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA/dir_2
$ mkdir dir_21 dir_22 dir_23
```
**8. Display contain of directory**
```
AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA/dir_2
$ ls -l
total 0
-rw-r--r-- 1 AnDer 197121 0 Apr 16 23:20 1.txt
-rw-r--r-- 1 AnDer 197121 0 Apr 16 23:20 2.txt
-rw-r--r-- 1 AnDer 197121 0 Apr 16 23:20 3.txt
-rw-r--r-- 1 AnDer 197121 0 Apr 16 23:20 4.json
-rw-r--r-- 1 AnDer 197121 0 Apr 16 23:20 5.json
drwxr-xr-x 1 AnDer 197121 0 Apr 16 23:23 dir_21/
drwxr-xr-x 1 AnDer 197121 0 Apr 16 23:23 dir_22/
drwxr-xr-x 1 AnDer 197121 0 Apr 16 23:23 dir_23/
```
**9,10,11. Open any text file, write something, save and close**
```
AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA/dir_2
$ vim 1.txt

In the window that appears:
1) Press the key "I"
2) Enter text
3) Press the key "esc" to save
4) Enter: ":wq"
5) Press the key "Enter"
```
**12 Shift one level above the current directory**
```
AnDer@DESKTOP-6**6P2OE0 MINGW64 /c/QA/dir_2
$ cd ..

AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA
```

**13 Move any 2 files to any directory**
```
AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA
$ mv dir_2/{1.txt,2.txt} dir_3
```
**14 Copy any 2 files to any directory**
```
AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA
$ cp dir_2/{3.txt,4.json} dir_3/
```
**15 Find the file by name**
```
AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA
$ find -name "1.txt"
./dir_3/1.txt
```
**16 View the contents of a file in real time**
```
AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA/dir_3
$ tail -f 1.txt
Streams full of stars, like skies at night.

No time to turn at Beauty’s glance,
And watch her feet, how they can dance.

No time to wait till her mouth can
Enrich that smile her eyes began.

A poor life this if, full of care,
We have no time to stand and stare.


111
222
333
```
**17 Print several first lines of the  file**
```
AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA/dir_3
$ head -4 1.txt
tWhat is this life if, full of care,
We have no time to stand and stare.

No time to stand beneath the boughs
```
**18 Print several last lines of the  file**
```
AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA/dir_3
$ tail -6 1.txt
We have no time to stand and stare.

111
222
333

```
**19 Read the contents of a large text file**
```
AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA/dir_3
$ less 1.txt

To close the window that appears press the key "q"
```
**20 Display date and time**
```
AnDer@DESKTOP-66P2OE0 MINGW64 /c/QA/dir_3
$ date
Mon Apr 17 00:46:51     2023
```
**21 Send an HTTP request to the server**
```
$ curl http://162.55.220.72:5005/
```
**22 Write a script that will automatically execute steps 3-8,13**
```
# Create the file script.txt
$ touch script.txt

# Open a file
vim script.txt

# Write a script
#!/bin/bash
cd /c/QA/Terminal_HW/dir_1/dir_11/dir_22
mkdir dir_31 dir_32 dir_33
cd dir_33
touch file1.txt file2.txt file3.txt file4.json file5.json
mkdir dir1 dir2 dir3
ls -la
mv /c/QA/Terminal_HW/dir_1/dir_11/dir_22/dir_33/{file1.txt,file4.json} /c/QA/Terminal_HW/dir_1/dir_13

# Make script executable
$ chmod +x script.txt

# Run a script
$ ./script.txt
```
## Homework Linux terminal (GitBash) - part 2

**1. Create the directory**
```
$ mkdir dir_1
```
**2. Go to the directory, which was created**
```
$ cd dir_1
```
**3. Create the directory inner_dir_1**
```
$ mkdir inner_dir_1
```
**4. See the current working directory path**
```
$ pwd
```
**5. Create the empty file tf_1.txt**
```
$ touch tf_1.txt
```
**6. Using the command cat, create file tf_2.txt, containing lines: the first 1, the second 2, the third 3**
```
$ cat > tf_2.txt
the first 1
the second 2
the third 3
```
**7. Go to a directory inner_dir_1**
```
$ cd inner_dir_1
```
**8. Using the command cat, create file tf_3.txt, containing any lines**
```
$ cat > tf_3.txt
All I know
It's so unreal
Watch you go
I tried so hard and got so far
But in the end, it doesn't even matter
I had to fall to lose it all
But in the end, it doesn't even matter
```
**9. Using the command cat, add to tf_3.txt line “the second 2”**
```
$ cat >> tf_3.txt
the second 2
```
**10. Using the command cat, add to tf_3.txt line “the sec 2”**
```
$ cat >> tf_3.txt
the sec 2
```

**11. Using the command cat, add to tf_2.txt line “the sec 3”**
 ```
$ cd .. && cat >> tf_2.txt
the sec 3
```
**12. Using the command cat, add to tf_3.txt line “the SeCoNd 2”**
```
$ cd inner_dir_1 && cat >> tf_3.txt
the SeCoNd 2
```
**13. Using the command cat, add to tf_2.txt line “the seConD 2”**
```
$ cd .. && cat >> tf_2.txt
the seConD 2
```
**14. Create the text file tf_4.txt, containing 15 lines**
```
$ cat > tf_4.txt
```
**15. Create the text file tF_5.txt, containing 13 lines**
```
$ cat > tF_5.txt
```
**16. Display the list of the contents of your current working directory**
```
$ ls -la
total 6
drwxr-xr-x 1 AnDer 197121   0 Jul 12 20:54 ./
drwxr-xr-x 1 AnDer 197121   0 Jul 12 20:54 ../
-rw-r--r-- 1 AnDer 197121  30 Jul 12 20:54 tF_5.txt
-rw-r--r-- 1 AnDer 197121 193 Jul 12 20:41 tf_3.txt
-rw-r--r-- 1 AnDer 197121  36 Jul 12 20:52 tf_4.txt
```
**17. Move up one  directory level**

```
$ cd ..
```
**18. Display contain of the file tf_3.txt**
```
$ cat inner_dir_1/tf_3.txt
```
**19. Find the path to the file tf_4.txt**
```
$ find . -name tf_4.txt
./inner_dir_1/tf_4.txt
```
**20. Clear the file tf_4.txt from the contents without deleting the file itself**
```
$ > ./inner_dir_1/tf_4.txt
```
**21. Find the path to files that have "tf" in their names**
```
$ find . -name '*tf*'
./inner_dir_1/tf_3.txt
./inner_dir_1/tf_4.txt
./tf_1.txt
./tf_2.txt
```
**22. Find the path to files that have "tf" in their names in a case-insensitive manner**
```
$ find . -iname '*tf*'
./inner_dir_1/tf_3.txt
./inner_dir_1/tf_4.txt
./inner_dir_1/tF_5.txt
./tf_1.txt
./tf_2.txt
```
**23. Find lines in files where there is a combination of letters "sec" in the current directory**
```
$ grep -r "sec"
```
**24. Find lines in files where there is a combination of letters "sec" in a case-insensitive manner in the current directory**
```
$ grep -i -r "sec"
```
**25. Find lines in files where there is only a combination of letters "sec" in the current directory**
```
$ grep -rw "sec"
```
**26. Find lines in files where there is only a combination of letters "sec" in a case-insensitive manner in the current directory**
```
$ grep -irw "sec"
```
**27. Find lines in files where there is a combination of letters "second" in the current directory**

```
$ grep -r "second"
```
**28. Find lines in files where there is a combination of letters "second" in a case-insensitive manner in the current directory**
```
$ grep -ir "second"
```
**29. Find lines in files where there is a combination of letters "second" in subdirectories of the current directory**

```
$ grep -r "second" ./*/*
```
**30. Find the name and path to files where there is a combination of letters "second" in the current directory**
```
$ grep -rl "second"
```
**31. Find lines in files where there isn't a combination of letters "second"**
```
$ grep -rv "second"
```
**32. Find the name and path to files where there isn't a combination of letters "second"**
``` 
$ grep -rL "second"
```
**33. Display the last 4 lines of any text file**
```
$ tail -n 4 ./*/tf_3.txt
```

**34. Display the first 4 lines of any text file**
```
$ head -n 4 ./*/tf_3.txt
```

**35. Command in a single line. Create a directory and create a text file with contents**

```
$ mkdir Hello && echo 'Hello' >> hello.txt
```
**36. Command in a single line. Move text files where there is a word "sec" to any directory**

```
$ grep -rwl "sec" ./* | xargs -I{} mv {} Hello
```

**37. Command in a single line. Cory text files where there is a word "sec" to any directory**
```
$ grep -rwl "sec" | xargs -I {} cp {} inner_dir_1
```
**38. Command in a single line. Find lines in files where there is a combination of letters "sec". Cory these lines to new text files**
```
$ grep -rh "sec" | xargs -I {} echo {} >> echo.txt
```
**39. Command in a single line. Delete files where there is a word "sec"**

```
$ grep -rwl "sec" | xargs -I {} rm {}
```
**40. Display the spring "Good Job!!" to the screen**
```
$ echo 'Goo job!!'
```



