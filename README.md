# Windows Caffe

##安装方法：
1 按照下文配置完后，在命令行里进入工程里的scripts目录：
	win 7 运行 build_win.cmd
	win 10 运行 .\build_win.cmd
2 脚本会在 C 盘 user 里下载 .caffe 文件的依赖库并进行caffe的编译
3 编译通过后，将python文件夹里的 caffe 复制到 your\path\to\AnacondaX\Lib\site-packages 下面
4 之后就可以 import caffe 了


##配置caffe 支持 cpu_only py3.5
1 修改build.cmd 如下:
	设置所有 以下选项：
	PYTHON_VERSION=3
	CPU_ONLY=1
	CONDA_ROOT=Your\path\to\Anaconda3
	MSVC_VERSION=14
	
2 配置环境变量为：
	D:\vision studio\software\Anaconda3;
	D:\vision studio\software\Anaconda3\Scripts;
	D:\vision studio\software\Anaconda3\Library\bin;
	3 安装vs2015(可以支持py35)，在安装时，选择安装编程语言VC


##配置caffe 支持 gpu py3.5
1 修改build.cmd 如下:
	设置所有 以下选项：
	PYTHON_VERSION=3
	CPU_ONLY=0
	CONDA_ROOT=Your\path\to\Anaconda3
	MSVC_VERSION=14
	
2 配置环境变量为：
	D:\vision studio\software\Anaconda3;
	D:\vision studio\software\Anaconda3\Scripts;
	D:\vision studio\software\Anaconda3\Library\bin;
	3 安装vs2015(可以支持py35)，在安装时，选择安装编程语言VC

3 安装cuda8.0， 安装cudnn6

##配置caffe 支持 gpu py2.7
1 修改build.cmd 如下:
	设置所有 以下选项：
	PYTHON_VERSION=2
	CPU_ONLY=0
	CONDA_ROOT=Your\path\to\Anaconda2
	MSVC_VERSION=14
	也可以 MSVC_VERSION=12
	
2 配置环境变量为：
	D:\vision studio\software\Anaconda3;
	D:\vision studio\software\Anaconda3\Scripts;
	D:\vision studio\software\Anaconda3\Library\bin;

3 安装vs2015(可以支持py35) 或者vs2013，在安装时，选择安装编程语言VC
	
3 安装cuda8.0， 安装cudnn6

