# S03L09: Practice Exercises 本章习题



## 9.1 习题部分

> 本习题根据配套 PDF 文件 `PracticeExercises-ExitStatusesandReturnCodes.pdf` 翻译整理所得。

> **习题1**
>
> 编写一段 `shell` 脚本，在屏幕上打印出 `"This script will exit with a 0 exit status."`。
>
> > [!tip]
> >
> > 注意：脚本必须以 `0` 的退出状态退出执行。
> >

> **习题2**
>
> 编写一段 `Shell` 脚本，接收一个文件名或文件夹作为参数，使其自动判定传入的是一个普通文件、文件夹、还是文件的其他类型？若为普通文件，则用退出状态 `0` 结束；文件夹则为 `1`；其他文件类型则以 `2` 退出。

> **习题3**
>
> 编写一段 `Shell` 脚本，执行命令 `cat /etc/shadow`。如果返回的退出状态为 `0` 提示 `Command succeeded`，并按 `0` 退出；若非 `0` 则提示 `Command failed` 并以 `1` 的状态码退出。



## 9.2 参考答案

> **习题1**
>
> `solution-01.sh`：
>
> ```shell
> #!/bin/bash
> 
> echo "This script will exit with a 0 exit status."
> exit 0
> ```

> **习题2**
>
> `solution-02.sh`：
>
> ```shell
> #!/bin/bash
> 
> FILE=$1
> 
> if [ -f "$FILE" ]
> then
>      echo "$FILE is a regular file."
>      exit 0
> elif [ -d "$FILE" ]
> then
>      echo "$FILE is a directory."
>      exit 1
> else
>      echo "$FILE is something other than a regular file or directory."
>      exit 2
> fi
> ```

> **习题3**
>
> `solution-03.sh`：
>
> ```shell
> #!/bin/bash
> 
> cat /etc/shadow
> if [ "$?" -eq "0" ]
> then
>      echo "Command succeeded"
>      exit 0
> else
>      echo "Command failed"
>      exit 1
> fi
> ```

