# 매뉴얼 페이지

?> 링크: [https://linuxsurvival.com/linux-manual-pages/](https://linuxsurvival.com/linux-manual-pages/)

Now it's time to work on a task.

The last time you saw your friend Greg, he told you that he had a couple of joke files in his home directory that he thought your kids would like. He also said that he had opened up the permissions on his home directory so that you could look through it. Now you want to find those joke files and print them out, so that you can show them to your kids.

The first step is to figure out Greg's User ID, so you can go skulking in his home directory. You could discover which command will give you this sort of user information by finding a good Linux book to look through, but fortunately, there's an easier way. The entire contents of your system's Linux manual is available online. The command which displays portions of this online documentation is called "man", which stands for "manual".

For example, if you don't know which "ls" option displays hidden files, you can display the manual pages describing "ls" by typing

                               man ls

Obviously, in order to use the "man" command in this way, you already have to know the name of the command that you are interested in. Unfortunately, in this case you don't know the name of the command, so you can't do that. But don't despair. There's an option to "man" which allows you to search for commands which pertain to a particular subject. And how do you figure out which option to "man" allows you to do this? It's simple. Just type

                              man man

which displays the manual pages describing the "man" command. In other words, you can use "man" to explain itself. A simplified version of the output of this command is shown at right.

The heading begins with "man(1)". The "(1)" means that the "man" command is found in Section 1 of the manual. The number of sections in the online manual varies from system to system, but Section 1 is always the "User Commands" section. In fact, unless you are a programmer or a system administrator, you will probably never need to look in any other section.

Here is a description of the different parts of a "man" page:

NAME contains the name of the command and a brief description of what it does.

SYNOPSIS shows the syntax of the command. In the page at right, "[-k]" refers to all of the possible options to the man command. In this case there is only one. The "-k" is surrounded by square brackets because it is an optional part of the command. That is, if you do not include it, the command will still function. The meaning of each option is explained in the OPTIONS section below. Notice the explanation of "-k" at right.

"keyword ..." refers to the possible arguments to the command. Since it is not surrounded by square brackets, it is not optional. That is, you must always include a "keyword" argument to the "man" command. The "..." means that you can specify more than one keyword.

DESCRIPTION gives an overview of the purpose of the command.

OPTIONS lists all of the possible options and arguments for this command and what they do.

SEE ALSO is not of direct importance, but it can be quite useful because it lists commands which have a related purpose.

After examining this output, it is obvious that the "-k" option will help you find a command that will show you Greg's User ID. On the next page, you'll find an example of "man -k".

Click the right arrow.


<br>
<br>

?> 링크: [https://linuxsurvival.com/linux-man-k-command/](https://linuxsurvival.com/linux-man-k-command/)

If you wanted to figure out which command is used to spell-check a document, you would type

                           man -k spell

This would show you every command which has the letters "spell" somewhere in its brief description.

Since you want to find the command which will tell you Greg's User ID, you should probably do a manual search on the word "user". Type the appropriate command at the prompt.

  > `명렁어입력`

- 다이얼로그 창

```다이얼로그 창
맞았습니다.
```	

```다이얼로그 창
Once again, we are simplifying the output for clarity. On a real system, you would see a huge number of commands listed. You will notice that the output looks just like the NAME section in a manual page. That's because "man -k" searches the NAME section of all manual pages to find what you are looking for. Remember that you can ignore any commands which have a section other than '1'. So, for instance, you can ignore "newusers (8)".
```	