# 《Shell Scripting: Discover How to Automate Command Line Tasks》Learning Notes



## 1. Profiles

![Redis 4.x Cookbook](assets/cover.png)

|    **Title**     | **Shell Scripting: Discover How to Automate Command Line Tasks** |
| :--------------: | :----------------------------------------------------------: |
|    **Author**    |                       **Jason Cannon**                       |
| **Publication**  |                      **Udemy, 2025.8**                       |
| **Total length** |           **14 sections \| 48 lectures \| 5h53m**            |

> ## Requirements
>
> - Some knowledge of the command line would be helpful, but not required.
>
> - Access to a Mac, Unix, or Linux computer.
>
> ## Description
>
> Here is what you will get and learn by taking this *Shell Scripting* course:
>
> - A step-by-step process of writing shell scripts that solve real-world problems.
>- The #1 thing you must do every time you create a shell script.
> - How to quickly find and fix the most common shell scripting errors.
>- For those of you who want to start scripting right away, watch the two video shell scripting crash course. If you do nothing else than watch these two videos you'll be ahead of most shell programmers.
> - How to accept input from a user and then make decisions on that input.
>- How to accept and process command line arguments.
> - What special variables are available, how to use them in your shell scripts, and when to do so.
>- A shell script creation check list -- You'll never have to guess what to include in each of your shell scripts again. Just use this simple check list.
> - A shell script template (boilerplate). Use this format for each of your shell scripts. It shows exactly what to include and where everything goes. Eliminate guesswork!
>- Practice exercises with solutions so you can start using what you learn right away.
> - Real-world examples of shell scripts from my personal collection.
>- A download that contains the scripts used in the presentations and lessons. You'll be able to look at and experiment with everything you're learning.
> - Quizzes after each section just to make sure you're learning the most important aspects of shell scripting.
>



## 2. Outlines

Status available：:heavy_check_mark: (Completed) | :hourglass_flowing_sand: (Working) | :no_entry: (Not Started) | :orange_book: (Learning finished)

|  No.   |                        Chapter Title                         |          Status          |
| :----: | :----------------------------------------------------------: | :----------------------: |
|        |  **Section 1: Start Here - Course Overview and Downloads**   |                          |
|  L01   | [Course Overview](./S01_start_here_course_overview_and_downloads/S01L01_course_overview.md) |    :heavy_check_mark:    |
|  L02   | [Course Downloads, Including the scripts used in the course and a cheat sheet](./S01_start_here_course_overview_and_downloads/S01L02_course_downloads_including_the_scripts_used_in_the_course_and_a_cheat_sheet.md) |    :heavy_check_mark:    |
|        |          **Section 2: Shell Scripting, Succinctly**          |                          |
|  L03   | [Section Introduction](./S02_shell_scripting_succinctly/S02L03_section_introduction.md) |    :heavy_check_mark:    |
|  L04   | [Shell Scripting, Part I](./S02_shell_scripting_succinctly/S02L04_shell_scripting_part_i.md) |    :heavy_check_mark:    |
|  L05   | [Shell Scripting, Part II](./S02_shell_scripting_succinctly/S02L05_shell_scripting_part_ii.md) |    :heavy_check_mark:    |
| Quiz 1 | [Quiz 1: Shell Scripting](./S02_shell_scripting_succinctly/Quiz1_shell_scripting.md) |    :heavy_check_mark:    |
|  L06   | [Practice Exercises](./S02_shell_scripting_succinctly/S02L06_practice_exercises.md) |    :heavy_check_mark:    |
|        |        **Section 3: Exit Statuses and Return Codes**         | :hourglass_flowing_sand: |
|        |                   **Section 4: Functions**                   |      :orange_book:       |
|        |      **Section 5: Shell Script Checklist and Template**      |      :orange_book:       |
|        |                   **Section 6: Wildcards**                   |      :orange_book:       |
|        |                **Section 7: Case Statements**                |      :orange_book:       |
|        |                    **Section 8: Logging**                    |      :orange_book:       |
|        |                  **Section 9: While Loops**                  |      :orange_book:       |
|        |                  **Section 10: Debugging**                   |      :orange_book:       |
|        | **Section 11: Data Manipulation and Text Transformations with Sed** |      :orange_book:       |
|        |      **Section 12: Scripts Used to Create This Course**      |      :orange_book:       |



Powershell script for generating markdown files in batch:

```powershell
# Create 13 empty markdown files named Ch##.md:
for($i=1; $i -le 12; $i=$i+1){ New-Item -Name "Ch$('{0:d2}' -f $i).md"; }
```

 
