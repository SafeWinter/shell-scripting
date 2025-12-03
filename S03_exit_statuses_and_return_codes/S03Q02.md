# Quiz 2: Exit Statuses and Return Codes 随堂测试题 2



## 1 Quizes

本章共设计 8 道随堂测试题：

1. All commands, including shell scripts, return an exit status.

   - True
   - False

2. Given the following options, which are the most comprehensive and valid Linux command exit statuses?

   - A. Only 0,1, or 2.
   - B.  Any integer between 0 and 255.
   - C.  Any integer between 1 and 255.
   - D. Any string.

3. Which special variable contains the value of the exit status of the previously executed command?

   - A. `$$`
   - B. `$_`
   - C. `$!`
   - D. `$?`

4. What symbol means "AND"?

   - A. `;`
   - B. `&&`
   - C. `||`

5. What symbol means "OR"?

   - A. `;`
   - B. `&&`
   - C. `||`

6. In the following example, if the `mkdir` command fails, the `cp` command will be executed:

   ```shell
   mkdir /tmp/bak && cp test.txt /tmp/bak/
   ```

   - True
   - False

7. True or False. A command following a semicolon will be executed no matter the exit status of the command that preceded the semicolon.

   - True
   - False

8. What is the exit status of the following shell script?

   ```shell
   #!/bin/bash
   hostname
   uptime
   ```

   - A. 755
   - B. The exit status of the shell script is the exit status of the uptime command.
   - C. The exit status of the shell script is the exit status of the hostname command.
   - D. This shell script has no exit status




## 2 Keys

True,B,D,B,C,False,True,B

