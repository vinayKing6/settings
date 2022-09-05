## map keys in order to replace all strings:

 :s/procat/law/ 替换当前行第一个 procat为 law；

```vim
:s/procat/law/g 替换当前行所有 procat为 law；

:n,$s/procat/law/ 替换第n行开始到最后一行中每一行的第一个procat为law；

:n,$s/procat/law/g 替换第n行开始到最后一行中每一行所有 procat为law，其中n 为数字，若n为“.”，则表示从当前行开始到最后一行；

:%s/procat/law/(等同于 :g/procat/s//law/) 替换每一行的第一个procat为law；

:%s/procat/law/g(等同于 :g/procat/s//law/g) 替换每一行中所有procat为law；

:%s/procat/law/gc(等同于 :g/procat/s//law/gc) 一查询方式替换每一行中所有procat为law；

若替换字符串中需要替换“/”，则不能使用“/”在命令中作分割符，此时可以可以使用“#”作为分隔符，当命令中出现“#”，则“/”不再被系统认作分隔符
```

## some quick keys:

```
    <normal>A:jump to the line end and insert
```

## 宏操作:

```
    1.<normal>q:进入宏录制
    2.<normal><name>:输入宏录制名称
    3.process
    4.<normal>q:退出宏录制
    5.<normal>e<num>@<name>:对几行重复宏操作    

```

## neo升级:

```shell
   sudo dpkg -i --force-overwrite <deb file>
   sudo apt -f install <deb file>
```

