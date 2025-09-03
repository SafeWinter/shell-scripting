# S02L06: Practice Exercises 本章习题



## 6.1 习题部分

> 本习题根据配套 PDF 文件 `PracticeExercises-ShellScriptingSuccinctly.pdf` 翻译整理所得。

> **习题1**
>
> 编写一段 shell 脚本，在屏幕上打印出 `"Shell Scripting is Fun!"`。
>
> > [!tip]
> >
> > 提示1：记住用 `chmod` 让文件变为可执行脚本；
> >
> > 提示2：记住在脚本开头使用 `shebang`。

> **习题2**
>
> 修改习题 1 中的 shell 脚本，使其包含一个变量，其内容为 `"Shell Scripting is Fun!"`。

> **习题3**
>
> 将命令 `hostname` 的结果存入一个变量，并在屏幕上显示 `"This script is running on ____."`，其中的 `____` 即 `hostname` 的输出结果。
>
> > [!tip]
> >
> > 提示：如果变量前后都紧挨一些文本或字符内容，最佳作法是使用 `${VARIABLE}` 语法。

> **习题4**
>
> 编写一段 shell 脚本，判定文件 `"/etc/shadow"` 是否存在：若存在，在显示 `"Shadow passwords are enabled."`。接着，再判定该文件是否可写入：若可写，则显示 `"You have permissions to edit /etc/shadow."`；否则显示 `"You do NOT have permissions to edit /etc/shadow."`。

> **习题5**
>
> 编写一段 shell 脚本，依次将 `man`、`bear`、`dog`、`cat` 和 `sheep` 显示在屏幕上，一个单词占一行。要求代码尽可能简短。
>
> > [!tip]
> >
> > 提示：可以用循环来执行重复性任务。

> **习题6**
>
> 编写一段 shell 脚本，提示用户输入一个文件或目录的名称，然后告知用户它是常规文件、目录，还是其他类型的文件。
>
> 此外，再对该文件或目录执行执行带有长列表选项的 `ls` 命令。

> **习题7**
>
> 修改习题 6 中的脚本，将其接收文件或目录名的方式，由此前的通过用户提示输入改为经由参数传入。

> **习题8**
>
> 修改之前习题中的脚本，使其可以接收任意数量的文件和目录作为参数。
>
> > [!tip]
> >
> > 提示：需要用到一个特殊变量。



## 6.2 参考答案

> **习题1**
>
> `solution-01.sh`：
>
> ```shell
> #!/bin/bash
> echo "Shell Scripting is Fun!"
> ```

> **习题2**
>
> `solution-02.sh`：
>
> ```shell
> #!/bin/bash
> MESSAGE="Shell Scripting is Fun!"
> echo "$MESSAGE"
> ```

> **习题3**
>
> `solution-03.sh`：
>
> ```shell
> #!/bin/bash
> HOST_NAME=$(hostname)
> echo "This script is running on ${HOST_NAME}."
> ```

> **习题4**
>
> `solution-04.sh`：
>
> ```shell
> #!/bin/bash
> 
> FILE="/etc/shadow"
> 
> if [ -e "$FILE" ]
> then
>      echo "Shadow passwords are enabled."
> fi
> 
> if [ -w "$FILE" ]
> then
>      echo "You have permissions to edit ${FILE}."
> else
>      echo "You do NOT have permissions to edit ${FILE}."
> fi
> ```

> **习题5**
>
> `solution-05.sh`：
>
> ```shell
> #!/bin/bash
> for ANIMAL in man bear pig dog cat sheep
> do
>      echo "$ANIMAL"
> done
> ```

> **习题6**
>
> `solution-06.sh`：
>
> ```shell
> #!/bin/bash
> 
> read -p "Enter the path to a file or a directory: " FILE
> 
> if [ -f "$FILE" ]
> then
>      echo "$FILE is a regular file."
> elif [ -d "$FILE" ]
> then
>      echo "$FILE is a directory."
> else
>      echo "$FILE is something other than a regular file or directory."
> fi
> 
> ls -l $FILE
> ```

> **习题7**
>
> `solution-07.sh`：
>
> ```shell
> #!/bin/bash
> 
> FILE=$1
> 
> if [ -f "$FILE" ]
> then
>      echo "$FILE is a regular file."
> elif [ -d "$FILE" ]
> then
>      echo "$FILE is a directory."
> else
>      echo "$FILE is something other than a regular file or directory."
> fi
> 
> ls -l $FILE
> ```
>
> 

> **习题8**
>
> `solution-08.sh`：
>
> ```shell
> #!/bin/bash
> 
> for FILE in $@
> do
>      if [ -f "$FILE" ]
>      then
>        echo "$FILE is a regular file."
>      elif [ -d "$FILE" ]
>      then
>        echo "$FILE is a directory."
>      else
>        echo "$FILE is something other than a regular file or directory."
>      fi
> 
>      ls -l $FILE
> done
> ```

