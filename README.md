这是说明文件

在测试 submodule 功能

这是一个由配置运行py-faster-rcnn项目而引申出来的思考.

#### 下载的工程带有submodule
当下载下来的工程带有submodule时, 初始的时候, 如果直接使用`git clone url`, submodule的内容并不会自动下载下来; 此时需要额外执行：
```
git submodule update --init --recursive
```
或者, 直接使用这种命令格式
```
# Make sure to clone with --recursive
git clone --recursive url
```

我在尝试 包含 自己的 js4sloth 项目
```
# 命令格式
# git submodule add 仓库地址 路径(会显示为当前项目下的一个目录)
git submodule add https://github.com/wanghao00/js4sloth.git utils
```

命令执行完毕后,在当前项目目录下生成了`utils`目录 和 `.gitmodules`文件, 文件内容如下：
```
[submodule "utils"]
	path = utils
	url = https://github.com/wanghao00/js4sloth.git
```

