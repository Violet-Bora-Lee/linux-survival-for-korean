# 파일 권한 수정하기

?> 링크: [https://linuxsurvival.com/linux-change-file-permissions-command-part-1/]()

The command you use to change the security permissions on files has a horribly cryptic name. It's called "chmod", which stands for "change mode", because the nine security characters are collectively called the security "mode" of the file.

Now it will become clear why we named the three "rwx" sets "user", "group", and "other". The first argument you give to the "chmod" command is 'u', 'g', 'o', or a combination of them which specifies which of the three "rwx" sets you want to modify. For example, if you want to give "execute" permission to the world ("other") for file "gorillas", you would start by typing

                            chmod o

Now you would type a '+' to say that you are "adding" a permission.

                            chmod o+

Then you would type an 'x' to say that you are adding "execute" permission.

                            chmod o+x

Finally, specify which file you are changing.

                      chmod o+x gorillas

You can also change multiple permissions at once. For example, if you want to take all permissions away from everyone, you would type

                    chmod ugo-rwx gorillas

Click the right arrow to continue.

<br>
<br>

?> 링크: [https://linuxsurvival.com/linux-change-file-permissions-command-part-2/]()

Okay, time to get back into action. Type the command to give "write" permission to the prim "group" for file "chimps".

Then type the command to give a long listing of the files so you can check your handiwork.

  > `명렁어입력`

- 다이얼로그 창

```다이얼로그 창
맞았습니다.
```

  > `명렁어입력`

- 다이얼로그 창

```다이얼로그 창
맞았습니다.
```

chmod g+w chimps
ls -l