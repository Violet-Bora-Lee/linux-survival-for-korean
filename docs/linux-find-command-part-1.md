# 파일 찾기

?> 링크: [https://linuxsurvival.com/linux-find-command-part-1/](https://linuxsurvival.com/linux-find-command-part-1/)

The command used to find files is called, appropriately enough, "find". But even though the name is easy to remember, the syntax is quite treacherous. A typical "find" command looks something like this:

                    find ~ -name "poem*"

This example is shown at right. The first argument you specify is the directory to start the search from. If "find" always searched the entire tree on a system, it would be very inefficient, so this first argument allows you to limit your search. In the above example, it will be started from your home directory (~) and will then search the entire tree under it.

The "-name" option says that you are searching for a file's name. At first, this might seem obvious and redundant, but you have to understand just how powerful the "find" command is. You can use it to search for files of a particular size, date, owner, and a variety of other criteria.

The argument to "-name" can be as simple as "poem" if you know that is the exact name of the file. But, if you're not sure whether the file is called "poem", "poems", or even "poem-favorite", then you can use a wildcard, like '*'. However, when you use a wildcard, you need to surround the argument in quotes. If you don't, you will receive a rude error message.

Now we'll give you a hint that will save you a bit of typing. Your first try at using this command to find joke files in Greg's home directory would probably begin with

                          find ~jester ...

But there is a simpler way. Remember the '..' symbol which is used to represent a parent directory (e.g. "cd ..")? Well, there is a similar symbol which represents your current directory. It is just a single '.'. So, since you are already in the "~jester" directory, you can begin your command with "find .".

Whew! That was a heck of a lot of explanation for just one command.

Click the right arrow.

<br>
<br>

?> 링크: [https://linuxsurvival.com/linux-find-command-part-2/](https://linuxsurvival.com/linux-find-command-part-2/)

Here is that example again:

                    find ~ -name "poem*"

Now it's time to try your luck with "find". By the way, you're pretty sure that Greg's joke files begin with the letters "joke".

  > `명렁어입력`

- 다이얼로그 창

```다이얼로그 창
맞았습니다.
```

```다이얼로그 창
Notice that "find" reported ALL of the files which matched your pattern, not just the first one. Also notice that "find" used '.' in the pathnames it printed. Pay attention to the name of the directory where the joke files were found -- you'll need to know it in a couple of pages.
```	