## Pyenv 安装

- 安装git：`~]# yum install -y git`
- 安装依赖：`~]#  yum install zlib-devel bzip2 bzip2-devel readline-devel sqlite sqlite-devel openssl-devel xz xz-devel libffi-devel findutils`
- 添加python用户：`~]# useradd  python`
- 安装pyenv：` ~]$ curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash`
- 添加变量：`~]$ vim ~/.bashrc`
```
export PATH="/home/python/.pyenv/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

## Pyenv 使用

- 安装指定版本：`pyenv install 3.5.2`
- 使用缓存安装
```
~]$ mkdir .pyenv/cache
~]$ mv Python-3.5.2.tgz  Python-3.5.2.tar.xz  Python-3.5.2.tar.gz .pyenv/cache
~]$ pyenv install 3.5.2
```
- 查看当前的版本：`pyenv version`
- 列出所有的版本：`pyenv versions`
- 设置当前目录及子目录的版本：`pyenv local 3.5.2`

## Virtualenv

使用插件 `virtualenv` 创建独立空间，实现模块/包之间的隔离

- 创建虚拟环境：`pyenv virtualenv 3.5.2 py352`
- 使用虚拟环境：`pyenv local py352`
