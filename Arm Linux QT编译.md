# Arm Linux QT编译

### 1 生产pro文件

在项目目录下执行：

```
 qmake -project
```

就会生成xxx.pro文件，这个文件用于生成Makefile用的；

### 2 生成Makefile

在以上生成xxx.pro文件后，可以直接在项目目录下执行：

```
qmake
```

命令，来生成Makefile。

### 3 生成某个平台可执行的程序

生成Makefile之后，直接make即可。

### 4 buildroot编译完成后编译qt

生成的qmake在output/build/..../bin/下。

执行生成的example里面的例程，进入example中的例程，在项目的目录下执行如下命令：（例如在analogclock例程中）

```
1.生成Makefile：
$ ./.../output/build/..../bin/qmake analogclock.pro
2.编译:
make
```

拷贝到Linux 中使用 :

```
./analogclock -platform linuxfb
```

