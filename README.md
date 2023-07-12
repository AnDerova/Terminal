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
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
```
**15. Create the text file tF_5.txt, containing 13 lines**
```
$ cat > tF_5.txt
1
2
3
4
5
6
7
8
9
10
11
12
13
```

16. Вывести список всех файлов в папке.
 17. Выйти из папки inner_dir_1
 18. Вывести содержимое файла tf_3.txt в терминал.
 19. Найти путь к файлу tf_4.txt
 20. Отчистить файл tf_4.txt от содержимого без удаления самого файла.
 21. Найти путь к файлам у которых есть  “tf” в названии.
 22. Найти путь к файлам у которых есть  “tf” в названии и буквы в любом регистре.
 23. Найти строки в файлах где есть комбинация букв “sec” в текущей папке
 24. Найти строки в файлах где есть комбинация букв “sec” в любом регистре в текущей папке
 25. Найти строки в файлах где есть только комбинация букв “sec” в текущей папке
 26. Найти строки в файлах где есть только комбинация букв “sec” в любом регистре в текущей папке
 27. Найти строки в файлах где есть комбинация букв “second” в текущей папке
 28. Найти строки в файлах где есть комбинация букв “second” в любом регистре в текущей папке
 29. Найти строки в файлах где есть комбинация букв “second” во всех папках ниже уровнем
 30. Найти только путь и название файла в строках которых есть комбинация букв “second” в текущей папке
 31. Найти все строки во всех файлах где нет комбинации “second”
 32. Найти только название и путь к файлам где нет комбинации “second”
 33. Вывести в терминал 4 последних строк любого текстового файла
 34. Вывести в терминал 4 первые строки любого текстового файла.
 35. Команда в одну строку. Создать папку и создать текстовый файл с содержиммым.
 36. Команда в одну строку. Переместить в любую одну папку текстовые файлы у которых в содержимом есть слово “sec”
 37. Команда в одну строку. Скопировать в любую одну папку текстовые файлы у которых в содержимом есть слово “sec”
 38. Команда в одну строку. Найти все строки c “sec” во всех текстовых файлах, скопировать и вставить эти строки в один новый созданный текстовый файл.
 39. Команда в одну строку. Удалить текстовые файлы у которых в содержимом есть слово “sec”
 40. Просто вывести в терминал строку “Good job!!”

