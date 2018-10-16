以下为windows10下安装docker，创建odoo镜像以及使用pycharm操作docker的教程
一、Window10安装Docker
1. 下载Docker
    国内从官网下载很慢，经过各种挖掘找到以下为网址：https://oomake.com/download/docker-windows，下载速度较快，选择合适的版本下载即可
2. 安装Docker
	windows10安装docker首先需要开启hyper-v
	![Image text](https://raw.githubusercontent.com/lz199409/Docker/master/images/QQ%E5%9B%BE%E7%89%8720181013002555.png)
	如果电脑没有开启虚拟系统，可以进入BOIS进行开启，自行百度即可
	双击运行下载的文件进行安装即可
3. 配置Docker
	成功安装docker之后会在电脑右下角出现一个小鲸鱼的图标，这表示已经成功安装并运行docker
	然后需要进行一些配置，右键点击小鲸鱼图标，然后选择setting进行配置：
	配置共享磁盘，此时可能会报错，需要关掉windows防火墙

