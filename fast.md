

# 快速入门



## 1 注册UCloud账户

如果已注册了UCloud账户，则可以立即开始使用USQL。如果尚未注册，请参见 [账号注册](/account/register/register_flow)

注册UCloud时，账户会自动注册UCloud中的所有服务，包括USQL。用户只需为使用的服务付费，USQL会使用UFile来存储数据。

## 2 示例查询

1、选择USQL标签可以跳转到USQL操作界面（如果没有这个标签，请联系客服申请开通）。
![](/images/usql位置.png)

2、示例查询：在USQL操作界面中，点击‘示例SQL’进行查询测试。

![](/images/示例选项.png)

3、选择任意示例SQL（例如：示例01），点击‘立即运行’，即可在下方显示运行结果。可以选择全屏查看运行结果或下载结果。运行结果将以csv文件格式下载。

![](/images/示例运行.png)

## 3 自主查询

### 3.1 上传数据文件

1、选择UFile标签可以跳转到UFile操作界面，在此操作界面进行数据上传。

2、将数据文件上传到UFile，目前USQL支持CSV格式文件。具体文件上传步骤请参考
[UFile-快速上手](/storage_cdn/ufile/quick/quick_start)。

![](/images/文件上传.png)

### 3.2 创建数据库

1、输入以下SQL语句，并点击立即运行，创建数据库database01。

``` 
           CREATE DATABASE database01
```

2、点击刷新并确认数据库database01出现在选项中。 
![](/images/创建数据库.png)

### 3.3 创建表

1、选择数据库database01，点击‘创建数据表’。 
![](/images/创建数据表.png)

2、输入表名称、数据存储位置，选择数据格式并输入字段列表，然后点击创建数据表。 
![](/images/创建数据表2.png)
![](/images/数据表.png)

### 3.4 查询数据

1、基于以上步骤，用户已经在数据库database01中建立了数据表client\_details。

在查询框根据需要，输入SQL语句进行查询，示例：

```    
       select * from client_details
       where city='Beijing'
```

点击‘立即运行’，返回查询结果如图，可以选择全屏查看结果或下载结果。 
![](/images/运行结果.png)

2、可以选择保存当前输入的SQL查询语句，可以在‘已保存SQL’中进行查看。

3、支持查看历史SQL，即所有查询记录。
