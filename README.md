## Homework Linux terminal (GitBash)
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

