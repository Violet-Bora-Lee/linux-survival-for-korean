# 그룹별 권한

?> 링크: [https://linuxsurvival.com/linux-groups-command/]()

The default Linux security model is a bit inflexible. To give special access (such as modification privileges) to a group of people, you have to get your system administrator to create a group with those people in it. Furthermore, if you would like to give a different set of access privileges (such as read access) to another group of people, you can't do it because you can only assign one group owner per file or directory. To solve this problem, you can use ACLs (Access Control Lists), a topic which is beyond the scope of this tutorial.

While we're on the subject of groups, we should see which groups you're in. To get a listing of your group memberships, type

> groups

Try it at the command prompt.

  > `명렁어입력`

- 다이얼로그 창

```다이얼로그 창
맞았습니다.
```

```다이얼로그 창
Notice that you aren't in the "prim" group, but that doesn't matter because you are the owner of these files anyway.
```

```다이얼로그 창
Now we'll have a final quiz before we wrap things up.
```
