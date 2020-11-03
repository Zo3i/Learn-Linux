### 前言

就像我们平时在可视化界面操作一样，我们学会了怎么在文件夹直接切换跳转，接下来我们学习文件、文件夹的相关操作。这里我先抛出一个概念，就是在Linux中一切皆为文件（这个不懂没关系）。在Linux中目录只是一个特殊的文件，文件后缀有和没有是一样的。因为Linux并不识别后缀，只是便于用户区分。但是在win中我们是需要识别文件后缀的。

### 创建文件

```shell
touch test
```

![image.png](https://zxx.sh/images/2020/11/02/image.png)

### 编辑文件

刚开始没使用过Linux，会非常不习惯使用Linux的编辑器。因为没有鼠标，编辑文件就显的非常麻烦。这里我建议下载一个[Xftp](https://www.ghpym.com/xftp.html)在线编辑文件，然后再保存。

![image35811.png](https://zxx.sh/images/2020/11/02/image35811.png)

![image09ec3.png](https://zxx.sh/images/2020/11/02/image09ec3.png)

右键打开文件，编辑完，记得保存就可以了。这是对新手最友好的方式了（当然我自己也经常这样）。但是命令还是要学的。

**VIM大法好**

vim 是Linux 内置的编辑器（有些版本的Linux 内置的版本只有vi编辑器）。那么问题来了最简单的编辑文件，我们直接输入vim后面加文件名回车即可。

```shell
vim test
```

![imaged800c.png](https://zxx.sh/images/2020/11/02/imaged800c.png)

出现这个界面后你可能发现你输入内容是打不出来的。这是因为vim有两种模式（这里只说两种，其他的太复杂）一种是**命令模式**，一种是**插入模式**。进入vim编辑器之后默认模式是命令模式，在这种模式下我们可以输入神秘代码操作文件。这里我们就不介绍vim的使用了（因为太难了）放一张图感受一下。

![vim_cheat_sheet_for_programmers_screene6925.png](https://zxx.sh/images/2020/11/02/vim_cheat_sheet_for_programmers_screene6925.png)

---

我们常用：

- 退出 :q
- 强制退出 :q!
- 保存并退出 :wq
- 文件内查找 ?查找内容

在命令模式下，直接输入即可注意前面的符号也要输入。

以上我们学会了保存，退出。然后我们学习编辑模式。上文提到我们刚刚进去vim编辑器的时候默认是命令模式，我们只需要输入一个i或者按键盘的insert键就可以进入编辑模式，就可以编辑文件了。有关于vim的操作有兴趣的小伙伴看这个文章就行了[https://github.com/dofy/learn-vim](https://github.com/dofy/learn-vim)

PS： 另外提一下，创建文件的另一种办法就是使用vim 编辑。直接输入vim 你想要保存文件的名字，然后编辑完了直接保存就可以了。

---

### 查看文件

```shell
cat test
```

![image4cb29.png](https://zxx.sh/images/2020/11/02/image4cb29.png)

### 删除文件

```shell
# 带有询问的删除文件
rm test
```

![image7f369.png](https://zxx.sh/images/2020/11/02/image7f369.png)

当你删除文件的时候，系统问你是否删除文件，你输入y即可。

```shell
# 不带询问的删除
rm -f test
```

### 创建目录

```shell
mkdir filetest
```

![imagef7eec.png](https://zxx.sh/images/2020/11/02/imagef7eec.png)

### 删除目录

```shell
rmdir filetest
```

[![image23da5.png](https://zxx.sh/images/2020/11/02/image23da5.png)](https://zxx.sh/image/ahFZ)

这个命令在文件夹内部还有文件的时候是删不掉的，只能用于删除空文件夹。所以我们一般都不用这个命令。下面我介绍一个最屌的删除命令，很多人在网上调侃删机跑路就是用这条命令。

```shell
rm -rf filetest
```

[![image40bf1.png](https://zxx.sh/images/2020/11/02/image40bf1.png)](https://zxx.sh/image/aqz0)

以上你可以看到，可以删除文件夹，并且没有删除提示，也不会因为文件夹内有文件就无法删除。既可以删除文件夹，也可以删除文件。之所以这个命令屌，是因为他会把文件夹里面所有的内容全部删除。如果执行

```shell
rm -rf /*
```

那么将意味着，你会把服务器上所有内容删除，并且不带提示。（PS：星号是匹配所有内容的意思，后面会解释）

---

### 文件复制

```
cp ./file /root
```

### 文件移动

```
mv ./file /root
```

### 文件重命名

```
mv file fileRename
```



