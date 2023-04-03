# vimConfigForCPP


Linux 能科学下安装插件管理器
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

## 在vim中我常用快捷键
- \e 打开文件目录
- \rg 搜索（ctrl  j 或者  k 或者 l  或者 h） 选择
- \f 搜文件
- \F
- ctrl i 运行c/cpp程序， demo比较方便
