# CSE 15L Lab Reports
## Lab 1
### cd
cd stands for <ins>"Change Directory"</ins>. It changes the current working directory to a target directory. 

- When using 'cd' with no arguments, the working directory is set to the default directory.
```
[user@sahara ~/lecture1/messages]$ cd
[user@sahara ~]$ pwd
/home
```
In Edstem, the default directory is the root, therefore it changes the working directory to the root directory.
- When using 'cd' with a path to a directory as an argument, the working directory is changed to that directory.
```
[user@sahara ~/lecture1]$ cd /messages
[user@sahara ~/lecture1/messages]$ pwd
~/lecture1/messages
```
The command successfully changed the working directory to a directory with relative path of '/messages'. 
- When using 'cd' with a path to a file as an argument, an exception will be thrown.
```
[user@sahara ~/lecture1/messages]$ cd /zh-cn.txt
bash: cd: zh-cn.txt: Not a directory
```
'cd' has to take a directory as an argument, inputing a file as the argument will cause an error. 
### ls
ls stands for <ins>"list"</ins>. It lists **all** entries under the current working directory

- When using 'ls' with no arguments, it lists **all** entries under the current working directory
```
[user@sahara ~/lecture1/messages]$ ls
en-us.txt  es-mx.txt  ja-jp.txt  zh-cn.txt
```
In this case, the working directory is /home/lecture1/messages, the 'ls' command prints out the 4 entries under the working directory.
- When using 'ls' with a path to a directory as an argument, it lists **all** entries under the given path
```
[user@sahara ~/lecture1/messages]$ ls ..
Hello.class  Hello.java  messages  README
```
the relative path '..' is translated to '/home/lecture1/', the 'ls' command succesfully prints out all entries under the designated directory.
- When using 'ls' with a path to a file as an argument, the *name* of the file will be printed.
```
[user@sahara ~/lecture1/messages]$ ls zh-cn.txt
zh-cn.txt
```
this output makes sense, since there is only one file that satisfies the given argument. 
### cat
cat stands for <ins>"Concatenate"</ins>, but, for most of the time, it is used to get the content of a given file.
- When using cat without arguments, the terminal repeats what I entered.
```
    [user@sahara ~/lecture1/messages]$ cat
    asdf
    asdf
    ddd
    ddd
    123123123
    123123123
```
Definitely not an error, probably a specified use of cat command.

- When using cat with a path to a directory as an argument, it prompts an error.
```
    [user@sahara ~/lecture1]$ cat ./messages
    cat: ./messages: Is a directory
```
For a slip of a second I expected that it automatically concatenate all files under that directory. The fact that it creates an error make sense, since it is impossible to the content of a directory.

- When using cat with a path to a file as an argument, it prints out the content of that file.
```
    [user@sahara ~/lecture1]$ cat Hello.java
    import java.io.IOException;
    import java.nio.charset.StandardCharsets;
    import java.nio.file.Files;
    import java.nio.file.Path;

    public class Hello {
    public static void main(String[] args) throws IOException {
        String content = Files.readString(Path.of(args[0]), StandardCharsets.UTF_8);    
        System.out.println(content);
    }
    }
```
The most common way of using cat command. Every character in the file gets printed.
