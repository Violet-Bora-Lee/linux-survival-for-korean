# 파일 보안

?> 링크: [https://linuxsurvival.com/linux-file-security-permissions-part-1/
]()

Now it's time to talk about security. Linux is a multi-user operating system, so it has security to prevent people from accessing each other's confidential files.

In our zoo, we don't want anyone to modify the primate files except for those workers who take care of the primates. It will take quite a bit of explanation before we can show you how to arrange this sort of security.

When you execute an "ls" command, you are not given any information about the security of the files, because by default "ls" only lists the names of files. You can get more information by using an "option" with the "ls" command. All options start with a '-'. For example, to execute "ls" with the "long listing" option, you would type

		ls -l

When you do so, each file will be listed on a separate line in long format. There is an example in the window on the right.

There are lots of other options you can use with the ls command, but we won't need them to accomplish our goals at the zoo.

Click the right arrow to continue.

<br>
<br>

?> 링크: [https://linuxsurvival.com/linux-file-security-permissions-part-2/
]()

There's a lot of information in those lines (and we've even simplified things for clarity).

The first character will almost always be either a '-', which means it's a file, or a 'd', which means it's a directory. In our example, all three of them are files.

The next nine characters (rw-r--r--) show the security; we'll talk about them on the next page.

The next column shows the owner of the file. In our imaginary zoo, your UserID is "keeper".

The next column shows the group owner of the file. Recall that we want to give the "prim" group of people special access to these files.

The next column shows the size of the file in bytes.

The next column shows the time the file was last modified (in reality, it would also show the date).

And, of course, the final column gives the filename.

Click the right arrow to continue.


<br>
<br>

?> 링크: [https://linuxsurvival.com/linux-file-security-permissions-part-3/
]()

Deciphering the security characters will take a bit more work.

First, you must think of those nine characters as three sets of three characters (see bottom right). Each of the three "rwx" characters refers to a different operation you can perform on the file.

The 'r' means you can "read" the file's contents.
The 'w' means you can "write", or modify, the file's contents.
The 'x' means you can "execute" the file. This permission is given only if the file is a program.
If any of the "rwx" characters is replaced by a '-', then that permission has been revoked.

For example, the owner's permissions for our three primate files are "rw-". This means that the owner of the file ("keeper", i.e. you) can "read" it (look at its contents) and "write" it (modify its contents). You cannot execute it because it is not a program; it is a text file.

Members of the group "prim" can only read the files ("r--"). We want to change the second permission character from '-' to 'w' so that those people can modify the contents of these files as well.

The final three characters show the permissions allowed to anyone who has a UserID on this Linux system. We prefer to refer to this set as "world". Our three primate files are "world-readable", that is, anyone in our Linux world can read their contents, but they cannot modify the contents of the files. This is the way we want to leave it.

Click the right arrow to continue.


