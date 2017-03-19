# 1. 先列出可用的安装包：

```
# yum list postgres*

# 比如，要安装基础的PostgreSQL 9.3 server：

# yum install postgresql93-server

# 自动选择：

# yum install postgresql-server 
```

![](file:///C:/Users/iris/AppData/Local/YNote/data/xq_iris@163.com/0edd7888f96b4a858f92a075ee459ef5/clipboard.png)

  


# 2.进入目录查看安装的pg的服务名 

```
# cd /etc/rc.d/init.d 

# ls
```

![](file:///C:/Users/iris/AppData/Local/YNote/data/xq_iris@163.com/6126aeb908324684a072db7c4a27f68e/clipboard.png)



# 3.初始化数据库：  

```
# service postgresql initdb

出现 ： error 1：

Solution: 修改文件夹权限 ：

# chmod 665 pgsql
```

![](file:///C:/Users/iris/AppData/Local/YNote/data/xq_iris@163.com/db4870b955934e08a1b6234838f636c6/clipboard.png)

解决方法：

![](file:///C:/Users/iris/AppData/Local/YNote/data/xq_iris@163.com/47c6a2de42584e5085ebdeea1fff7566/clipboard.png)

```
error 2: 初始化 失败
Solution:
            查看启动日志 ： # less /var/lib/pgsql/pgstartup.log
```

![](file:///C:/Users/iris/AppData/Local/YNote/data/xq_iris@163.com/e1460265091144eba82b2a0aae992f15/clipboard.png)

  


      


![](file:///C:/Users/iris/AppData/Local/YNote/data/xq_iris@163.com/e69a6d75dda24868b5ae1762388b7798/clipboard.png)

            发现问题：没有是用　ｐｏｓｔｇｒｅｓ　超级用户登录

  


    修改postgres用户 密码 ： \# passwd postgres  ---》

121314

  


    要加入ｗｈｅｌｌ用户组　

  


使用postgres 用户登录 \# su - postgres

然后进入 \# cd /var/lib/pgsql  目录

  


\# chomod 777 pgStartup\_log

\# chomod 777 data/pg\_log

...

  


拥有所有读写权限后 \# service postgresql initdb

初始化完成后   \#　service　ｐｏｓｔｇｒｅｓｑｌ start

进入命令行模式：＃　ｐｓｑｌ

。。。  

  


  




