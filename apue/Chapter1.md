## UNIX体系结构
1. 操作系统：可定义为一种软件，**控制计算机硬件资源，提供程序运行环境**（这种软件称为 ***内核***）。
2. 内核的**接口**称为 ***系统调用***。***公有函数库***构建在系统调用接口上；应用程序既可以使用公有函数库，也可以使用系统调用。
3. ***shell*** 是一个特殊应用程序，为运行其他应用程序提供了一个接口。
## 登录
1. 口令文件可在 `/etc/passwd` 中查看。
2. shell：一个命令行解释器，读取用户输入然后执行命令。系统从口令文件中登录项的值应该为某用户启动执行哪一个shell。（bash是`Bourne again shell` ）。
## 文件和目录
    gcc -o myls ls1.c -lapue   //进行编译 
#### 1. 文件系统
1. 所有东西的起点是 ***根（root）*** 目录,其名称是`/`。
2. ***目录***也是文件，是一个包含目录项的文件。
3. ***目录项***包含一个文件名和说明该文件属性的信息：文件类型、文件大小、文件所有者、文件权限、文件最后修改时间等。`stat` 和 `fstat`返回包含文件属性的信息结构。
#### 2. 文件名
1. 只有`/` 和 ***空格***不能包含在文件名中。
2. `.`是当前目录， `..`是父目录。
#### 3. 路径名
1. 绝对路径：以/（root）开头。
2. 相对路径：1的否则。
#### 4. 工作目录
所有相对路径都从当前工作目录开始；进程可以用`chdir`更改工作目录。
#### 5. 起始目录
登录时的工作目录。从口令文件中获取。
## 输入和输出


