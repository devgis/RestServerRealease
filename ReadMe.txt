各版本目录下游使用说明书

RestServer直接发布数据库为json格式提供方法

RestSerRestServer直接发布数据库为json格式 支持MySQL,SqlServer,Oracle直接发布为Rest服务， 返回json格式宫客户端

下载文件后解压

 

RestServer是一个快捷的rest服务器，用于直接将数据库数据发布成json格式方便其他需要json格式数据的地方调用。此程序免费，代码有偿提供。1.0.0.22支持所有表数据返回以及表数据条件返回。

使用环境：

1)     服务器:windows xp,7,8,10,windows server 2003,2008,2012。.

2)     .netFrameWork 4.0。

3)     数据库:oracle 9i,10g,11g,MSSql2000,2005,2008,2012,MySQL5以上。

 

1)     解压软件到相应目录。解压后主要有以下文件：

 

2)     安装.net Framework4.0(去微软官方网站下载或者网络搜索即可。)

3)     配置配置文件，配置文件在目录下RestServer.exe.config使用记事本打开即可进行编辑修改。只需修改configuration/appSettings配置节下面的内容（配置之前最好先进行复制备份，然后再进行修改），配置文件说明如下：

<add key="HOSTNAME"value="localhost"/><!--服务器名称-->

    <addkey="PORT" value="9001"/><!--Restf服务端口-->

    <add key="DBTYPE"value="MYSQL"/><!--ORACLE,MSSQL,MYSQL-->

    <addkey="DBCONSTRING" value="UserId=root;Host=localhost;Database=db_carmanager;password=root"/>

    <!--[SQL]: Data Source= 192.168.0.21; Initial Catalog = testtable; User Id = sa; Password = 123456;-->

    <!--[ORACLE]: DataSource = Data Source=carorcl;Persist Security Info=True;UserID=zcb;Password=zcb-->

    <!--[MySQL]: UserId=root;Host=localhost;Database=db_carmanager;password=root-->

<add key="TABLES"value="t_log,t_car"/> <!--t_test ,分割-->

a)        HOSTNAME为当前主机名称,id地址或域名

b)        PORT为需要使用的端口，请使用系统没有用的否则会创建失败。

c)        DBTYPE为数据库类型 必须为ORACLE,MSSQL或MYSQL，分别对应使用ORACLE数据库,MSSqlServer,MySQL数据库。

d)        DBCONSTRING为数据库的链接内容 请参考下方样本按照DBTYPE类型进行配置。

4)     启动软件注意win7以上系统包括Server 2008以上系统请使用右键管理员方式执行，否则会启动失败。启动成功后会有如下提示：

 

表示服务已经启动成功。接下来我们就可以受用了。

 

1.  开始使用

启动成功后就可以使用了。比如上一节配置了t_log和t_car两张表

这时候我们就可以在IE里边输入以下内容进行操作。

1)     查询表中所有内容返回json,输入http://localhost:9001/rest/t_car/query我们就可以在浏览器中看到如下结果：

 

2)     我们需要对标进行查询，比如carno="山A23392"这时候我们可以进行如下查询：http://localhost:9001/rest/t_car/query/carno=carno="山A23392"这时浏览器中显示如下：

 

当然这里边可以支持sql语句中的where语句进行组合查询。这里就不再做详细说明了。

 


BUG反馈
 QQ:80163278
 邮箱:devgis@qq.com
 淘宝:http://flysoft.taobao.com
 ----------------------------------------------------------------------------------------------
 1.1
 jsonp格式支持方便JQUERY调用
 日志记录功能
 采用流的方式写数据进行优化优化
 ----------------------------------------------------------------------------------------------
 1.0
 基本功能
 ----------------------------------------------------------------------------------------------

 

百度网盘下载地址：http://pan.baidu.com/s/1bn2szDH 
 CSDN下载地址：http://download.csdn.net/user/devgis

C#,WinForm ,数据库，MapXtreme, Arcgis Engine 相关的开发,正规211高校毕业，本人已经搞了8年相关开发，技术精良！有需求的朋友联系我QQ ：80163278邮箱:devgis@qq.com价格绝对公道，合理！欢迎长期合作！！！