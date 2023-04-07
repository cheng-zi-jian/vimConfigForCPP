# vimConfigForCPP

### 前提：能科学上网

## 安装步骤

拷贝配置文件
```
cp vimConfigForCPP/.vimrc ~/.vimrc
```
安装vim的Plug管理器
```
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
  https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

进入vim
```
vim
```

vim下执行命令
```
:PulgInstall
```

因为Leader插件需要ripgrep软件
如果熊没有安装(rg)命令， 如下安装
```
#centos
sudo yum-config-manager --add-repo=https://copr.fedorainfracloud.org/coprs/carlwgeorge/ripgrep/repo/epel-7/carlwgeorge-ripgrep-epel-7.repo
sudo yum install ripgrep

#debian（ubuntu）
curl -LO https://github.com/BurntSushi/ripgrep/releases/download/13.0.0/ripgrep_13.0.0_amd64.deb
sudo dpkg -i ripgrep_13.0.0_amd64.deb
```

ctags第一次安装时候， 添加系统参数表
```
ctags -I __THROW -I __attribute_pure__ -I __nonnull -I __attribute__ --file-scope=yes --langmap=c:+.h --languages=c,c++ --links=yes --c-kinds=+p --c++-kinds=+p --fields=+iaS --extra=+q  -f ~/.vim/systags /usr/include/* /usr/include/sys/* /usr/include/bits/*  /usr/include/netinet/* /usr/include/arpa/* /usr/include/mysql/*


后续每次打开项目， 否则C语言的一些变量定义没有
CPP
ctags -R --fields=+iaS --extra=+q *

C语言
ctags -R --fields=+iaS --extra=+q * --languages=c --langmap=c:.c.h
```


## 日常使用快捷键 
在vim中我常用快捷键（我定义的是单引号， 如果不喜欢把let mapleader = "'" 注释掉， 默认就是反斜杠了）
- jk 代替ESC
- 'e 打开文件目录
- 'n new标签页
- 'a 左标签页
- 'd 右标签页
- 'c close标签页
- 'rg 搜索（ctrl  j 或者  k） 选择
- 'f 搜文件名
- 'F 搜索本文件的函数
- 'm 历史打开的文件
- 'b buffer文件
- ctrl i 运行c/cpp程序， demo比较方便
