- 创建`pip`目录：`~]$ mkdir ~/.pip`
- 配置文件在`~/.pip/pip.conf`
```
[global]
index-url=https://mirrors.aliyun.com/pypi/simple/
trusted-host=mirrors.aliyun.com
```

- 安装ipython：` pip install ipython`
- 安装jupyther：`pip install jupyter`
- 设置jupyter-notebook的密码：`jupyter notebook password`
- 启动jupyter-notebook：`$ jupyter notebook --ip=0.0.0.0`

## pip 使用

- 导出虚拟环境中的模块：`$ pip freeze > /tmp/package.txt`
- 导入模块：`$ pip install -r /tmp/package.txt`
