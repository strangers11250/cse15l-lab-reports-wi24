# CSE 15L Lab Reports
## Lab 1
### cd
cd stands for <ins>"Change Directory"</ins>

- When using cd with no arguments, the working directory is set to the root directory.
```
[user@sahara ~/lecture1/messages]$ cd
[user@sahara ~]$ pwd
/home
```
- When using cd with a path to a directory as an argument, the working directory is changed to that directory.
```
[user@sahara ~/lecture1]$ cd /messages
[user@sahara ~/lecture1/messages]$ pwd
~/lecture1/messages
```
- When using cd with a path to a file as an arguemtn, an exception will be thrown.
```
[user@sahara ~/lecture1/messages]$ cd /zh-cn.txt
bash: cd: zh-cn.txt: Not a directory
```
### ls
### cat
