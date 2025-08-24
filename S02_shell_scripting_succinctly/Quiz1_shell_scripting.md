# Quiz 1: Shell Scripting 随堂测试题 1



## 1 Quizes

本章共设计 8 道随堂测试题：

1. Which of the following choices is the best first line of a shell script?

   - A. The first line of a shell script should be blank.
   - B. `#`
   - C. `# /bin/bash`
   - D. `#!/bin/bash`

2. The first line of a shell script typically starts with a shebang, followed by the path to an interpreter that will be used to execute the commands in the script.

   - True
   - False

3. The commands in a script will be executed using the current shell of the user executing that script if a shebang followed by a path to an interpreter are not specified on the first line of the script.

   - True
   - False

4. Which of the following variables is valid to use in a shell script?

   - A. `3LETTERS="ABC"`
   - B. `first-three-letters="ABC"`
   - C. `first@Three@Letters="ABC"`
   - D. `FIRST3LETTERS="ABC"`

5. What is the value of "`$1`" given the following command line:

   `$ ./add-user.sh tom richard harry`

   - A. `./add-user.sh`
   - B. `tom`
   - C. `richard`
   - D. `harry`

6. Which is the proper way to assign a value to a variable?

   - A. `VAR="VALUE"`
   - B. `VAR = "VALUE"`

7. Which of the following will assign the output of the "hostname" command to the variable HOSTNAME?

   - A. HOSTNAME=$(hostname)
   - B. HOSTNAME=\`hostname\`
   - C. All of the above

8. What is the output of the following shell script?

   ```shell
   #!/bin/bash
   MY_SHELL="csh"
   if [ "$MY_SHELL" = "bash" ]
   then
     echo "You seem to like the bash shell."
   elif [ "$MY_SHELL" = "csh" ]
   then
     echo "You seem to like the csh shell."
   else
     echo "You don't seem to like the bash or csh shells."
   fi
   ```

   - A. You seem to like the bash shell.
   - B. You seem to like the csh shell.
   - C. You don't seem to like the bash or csh shells.



## 2 Keys

D,True,True,D,B,A,C,B