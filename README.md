# Docker
Windows下Odoo的Docker环境的搭建以及pycharm使用docker运行odoo

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
	a. 配置共享磁盘，此时可能会报错，需要关掉windows防火墙
		![Image text](https://raw.githubusercontent.com/lz199409/Docker/master/images/97JE_S574O%24L%60WH1PQMFE%250.png)
	b. 关掉防火墙之后共享磁盘
		![Image text](https://raw.githubusercontent.com/lz199409/Docker/master/images/QQ%E5%9B%BE%E7%89%8720181013003446.png)
	c. 配置docker的默认选项
		![Image text](https://raw.githubusercontent.com/lz199409/Docker/master/images/%245UW%251)%60X6CP%25X%24WTEW0GR7.jpg)
	Doker在拉取镜像时会从国外的源进行拉取，速度较慢，我们可以将docker的源设置为阿里的源，这样下载速度较快
	登录https://cr.console.aliyun.com/cn-hangzhou/mirrors获取阿里的docker镜像获取地址
	然后在setting里面配置docker的镜像地址：
		![Image text](https://raw.githubusercontent.com/lz199409/Docker/master/images/9E)LV%7B9(LNVZIU%25%24LA%5D_4%405.jpg)
	以上就是docker的基本配置，配置完成后就可以了

二、 创建镜像
	1. 首先从自己的仓库拉取完整的目录结构
	2. 拉取完成代码后，开始创建镜像，有两种创建镜像的方式
		a. 使用Dockerfile创建镜像
			从刚才拷贝下来的代码结构，切换到docker目录下，运行docker build f ./Dockerfile-dev:1.0 .
			注意：不要省略掉最后面的.
			这种方式是通过Dockerfile新建镜像
		b. 使用已经拷贝的本地镜像压缩包，然后加载生成镜像
			切换到压缩包目录下：
			docker load -i pscloud-dev.tar
			注意：加载速度较慢
	

