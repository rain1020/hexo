---
title: Mac 安装 nvm
---

### 应用场景：

    项目中存在多种依赖包，随着依赖包版本的升级，需要兼容更高版本的node，为了让不同的项目能够正常运行，可以使用nvm管理node，下载多个node版本，在不同的项目中配置不同的node的环境

### 定义 nvm：nvm 全名 node.js version management，是一个 node 的版本管理工具

### 下载 nvm：

1.  终端中打开安装文件的目录：

```bash
 cd + ～
```

2.  使用 git 安装 nvm

```bash
    git clone https://github.com/nvm-sh/nvm.git
```

3.  进入 nvm 目录

```bash
   cd nvm
```

4.  执行编译文件

```bash
 ./install.sh
```

5.  进入用户终端

```bash
cd + ～
```

6.  配置环境变量 可以使用命令

```bash
vim ~/.bash_profile
```

    在文件内写入如下 3 行内容：
    export NVM_DIR="$HOME/.nvm"
        [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
        [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"
    修改好后点击 esc 退出编辑，在任意位置输入：“:wq”来保存并退出文件

7.  退出后，需执行以下命令使配置文件生效

```bash
source ~/.bash_profile
```

8.  输入 nvm -v 查看是否安装成功

```bash
 nvm -v
```

### nvm 指令：

nvm 常用命令如下：
nvm ls ：列出所有已安装的 node 版本
nvm version // 查看 nvm 版本
nvm install 14.17.0    // 安装指定版本
nvm install latest    // 安装最新版本
nvm uninstall 14.17.0  // 卸载 node8.12.0 版本
nvm list              // 查看所有安装了的 node
nvm use 12.19.0      // 将 node 版本切换到 12.19.0 版本
nvm current ：当前 node 版本
nvm alias [别名] [node 版本号] ：给不同的版本号添加别名
nvm unalias [别名] ：删除已定义的别名
nvm alias default[node 版本号]：设置默认版本
参考文章：
https://www.jianshu.com/p/a5b41cfe980a
https://blog.csdn.net/LYNNBXLI/article/details/128054891
