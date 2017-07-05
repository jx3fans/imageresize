# 图片自动缩放
根据 https://github.com/hopesoft/nginx-lua-image-module 修改而来

****

# 依赖
1. 基于`openresty`开发。
2. 使用`GraphicsMagick`进行图片处理。

## 安装openresty
* 下载源码
> 从 https://openresty.org/cn/ 下载openresty源码，解压后编译。
* 编译参数
> ./configure --prefix=/home/appuser/openresty
* 新增环境变量
> * export OPENRESTY_HOME=/home/emall/openresty
> * PATH=$OPENRESTY_HOME/bin:$OPENRESTY_HOME/nginx/sbin:$PATH

## 安装GraphicsMagick
* 下载源码
> 从 http://www.graphicsmagick.org/download.html 下载GraphicsMagick源码。
* 安装依赖 
> yum install libtiff libtiff-devel libjpeg libjpeg-devel libpng libpng-devel jasper jasper-devel
* 编译参数
> ./configure --prefix=/home/appuser/GraphicsMagick --with-jpeg=yes --with-jp2=yes --with-png=yes --with-tiff=yes  

## 启停
进入imageresize目录，使用如下命令启动停止
* nginx -p \`pwd\`/ -c conf/nginx.conf
* nginx -p \`pwd\`/ -c conf/nginx.conf -s stop
