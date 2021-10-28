# 《计算机程序设计与艺术：卷1，基本算法》  

## 安装编译和运行流程  

安装mdk  
```
sudo apt install mdk
```

创建`hello.mixal`，使用vim  
```
TERM    EQU     19
        ORIG    3000
START   OUT     MSG(TERM)
        HLT
MSG     ALF     "MIXAL"
        ALF     " HELL"
        ALF     "O WOR"
        ALF     "LD   "
        END     START
```

编译  
```
$ mixasm hello.mixal 
$ ls
hello.mix  hello.mixal
```

运行  
```
$ mixvm -r hello.mix
Program loaded. Start address: 3000
Running ...
MIXAL HELLO WORLD                                                     
... done
```

### 注意  

交互式：在shell中输入mixvm,即可进入交互式环境,输入help，就可以看到支持的命令了  

```
    load 导入源文件
    compile 编译
    run 运行
```