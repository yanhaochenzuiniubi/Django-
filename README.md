# Django毕业设计项目
基于python django项目的一个简单的展馆信息。
此APP系统主要是数据库主要还是依靠调用的WEB后台服务和服务器对应的数据库，数据库采用MySQL8.0.26版本，MySQL 是一个具有客户端-服务器模型的开源关系数据库管理系统，具有性能高，成本低，可靠性强的特点，在设计数据库时，首先创建了一个名为mysite的数据库，其次在mysite数据库中创建一个db_beacon数据表，并且还有基站的基本信息:

beacon_uuid	展台的宣传活动主题	CHAR类型数据
beacon_mac	基站的MAC地址，用来获取iBeacon的MAC地址和数据库的匹配,CHAR类型数据。	CHAR类型数据，为主键(primary key)
beacon_name	展台号	CHAR类型数据
beacon_major	展台主题类型	CHAR类型数据
beacon_minor	展台活动类型介绍	CHAR类型数据
imgs	存储展台宣传视频	VARCHAR类型数据

![image](https://user-images.githubusercontent.com/70590957/177801138-7e096970-d832-49dd-b96d-515519d954a2.png)

WEB前端采用BootStarp框架搭建的页面，并且结合Django框架运行静态文件的服务；首先在阿里云服务器Ubuntu20.04里面创建一个Django项目，并且命名为Bluetooth，在Bluetooth中创建一个templates文件夹，该文件夹的主要作用是专门用来运行静态文件；在该文件夹中创建一个base.html，这个静态文件主要写入bootstarp框架，然后再创建一个home.html文件，home.html中调用base的框架，从而显示界面。
![image](https://user-images.githubusercontent.com/70590957/177801343-ec71a39a-ab97-41ca-9eac-ee91d5e46c38.png)
![image](https://user-images.githubusercontent.com/70590957/177801389-f9888700-47c5-4b66-b079-1d14045028e6.png)
在后台管理系统中，使用Django自带的admin框架，并且使用SimpleUI来进行后台界面的美化。在Django项目中修改settings.py，首先先用Python自带的pip安装，安装依赖，pip3 install django-simpleui，然后在settings.py中INSTALLED_APPS中引入这个‘simpleui’，然后重启Django服务。
