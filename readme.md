# 前后端分离项目





## 数据来源

爬取爱课程网站上的部分课程信息
运行icourse-spider.py之后就会生成一个icourse.txt文件
会保存部分课程信息。



## 后端

后端采用python的web框架flask

数据库采用sqlite

操作步骤

进入到course-server目录下	(由于pip服务器在海外，这里使用清华镜像源进行下载)

```shell
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple -r requirements.txt
```

数据库操作	依次输入下面命令

```shell
python manage.py db init
python manage.py db migrate
python manage.py db upgrade
```

启动 后端服务

```shell
python manage.py runserver -r -d	
```



## 前端

前端采用vue框架

操作步骤

搭建vue环境

- 安装node.js 

- 在终端输入npm --version

  出现版本号 6.12.0 即为安装成功

- 由于npm服务器在海外，为了方便下载依赖库，需要转换镜像

  ```shell
  npm install -g cnpm --registry=https://registry.npm.taobao.org
  ```

- 查看cnpm版本   

  ```shell
  cnpm --veriosn
  ```

- 安装 vue-cli 脚手架

  ```shell
  cnpm install --global vue-cli
  ```



进入到 course-web文件夹下在终端下输入

```shell
cnpm install 
```

安装vue依赖包

```shell
cnpm run dev
```

运行前端项目

