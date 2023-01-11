# Git Study

![Git](images/git.png)

## Git 安装配置

🔗Git 各平台安装包下载地址为：http://git-scm.com/downloads

### Git 配置

Git 提供了一个叫做 **`git config`** 的工具，专门用来配置或读取相应的工作环境变量。

这些环境变量，决定了 Git 在各个环节的具体工作方式和行为。这些变量可以存放在以下三个不同的地方：

- **`/etc/gitconfig`** 文件：系统中对所有用户都普遍适用的配置。若使用 *git config* 时用 **`--system`** 选项，读写的就是这个文件。
- **`~/.gitconfig`** 文件：用户目录下的配置文件只适用于该用户。若使用 *git config* 时用 **`--global`** 选项，读写的就是这个文件。
- 当前项目的 Git 目录中的配置文件（也就是工作目录中的 *.git/config* 文件）：这里的配置仅仅针对当前项目有效。每一个级别的配置都会覆盖上层的相同配置，所以 *.git/config* 里的配置会覆盖 */etc/gitconfig* 中的同名变量。

### 用户信息

配置个人的用户名称和电子邮件地址：

```
$ git config --global user.name "runoob"
$ git config --global user.email test@runoob.com
```

如果用了 --global 选项，那么更改的配置文件就是位于你用户主目录下的那个，以后你所有的项目都会默认使用这里配置的用户信息。

如果要在某个特定的项目中使用其他名字或者电邮，只要去掉 --global 选项重新配置即可，新的设定保存在当前项目的 .git/config 文件里。

### 创建本地空仓库：git init

> init：初始化当前目录为仓库，初始化后会自动将当前仓库设置为master

创建本地仓库的条件是需要一个空目录，然后在空目录中初始化你的项目

如我想创建一个名为“test”的空项目

1.创建目录

```
mkdir test
```
2.进入目录

```
cd test
```
3.使用git init初始化当前仓库
```
git init
```
