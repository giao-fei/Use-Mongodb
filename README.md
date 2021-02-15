 ## Use-Mongodb
```
一、开启mongodb服务：
        (1)、先新建一个文件夹 mongodb 然后在cmd里面  mongod --dbpath D:\nodejs\MongoDB\mongodb
二、连接Mongodb服务：开启 cmd 输入 mongo
三、创建一个数据库（giao）：use giao 然后再创建一个集合 (giao) 
        (1) use giao
        (2)  db.giao.insert({"":""})
        (3)  展示 giao 这个数据库中所有的集合：先 use 到 giao 数据库中，然后再 show collections
四、删除 giao 这个数据库：先切换到giao这个数据库中：use giao 然后输入db.dropDatabase()
      （1）删除giao库中的giao表: 先进到这个库里面 db.表名.drop()
五、查看所有数据库：show dbs
      （2）查看giao数据库中所有的表：show tables
六、在mongodb数据库中giao这张表中插入数据：db.giao.insert({"name":"hello world","age":"1000"})
七、查找giao数据库中giao表中的数据：db.giao.find()
八、替换giao 数据中giao表中的数据 db.giao.udpade({"name":"hello world","age":"1000"},{"name":"你好 世界",age:"500 "})
九、移除giao数据库中giao表的数据  db.giao.remove({"name":"你好 世界","age":"500"})
十、数据包导出：mongodump -h dbhost(主机+端口号) -d dbname(数据库名称)  -o  dbdirectory(要导出的路径)
十一、数据包导入： mongorestore -h dbhost -d dbname(数据库名称 名称可以随便取一个) <path>(数据包存放的路径)
十二、Mongodb账户权限配置
              (1)、超级管理员账户配置：
                       (1)、先开启mongodb服务：mongo
                       (2)、然后 use admin
                       (3)、查看admin数据库中的用户账号：show users
                       (4)、如果已存在账号则：db.dropUser('admin') 再重新创建一个用户 db.createUser({user: 'admin', pwd: '123456', roles: [{role: 'root', db: 'admin'}]})
                       (5)、在 mongodb.cfg 文件中 添加：(注意：一定要对齐)
                                     security:
                                         authorization: enabled
                       (6)、重新启动mongodb服务：ctrl+r 中搜索 services.msc 中找到  Mongodb Server 并重启它
                       (7)、用超级管理员开启mongo服务：mongo admin -u 账户名 -p 密码
              (2)、给指定数据库创建账号和密码，只能访问当前的数据库(admin2)：
                       (1)、先use到你要设置的集合里面：use admin2
                       (2)、然后show users 看是否存在管理员账号，如果有则删除当前账户 db.dropUser(账户的名称)例如：db.dropUser('admin2')
                       (3)、给当前数据库新增一个账号：db.createUser({user: 'admin2', pwd: '123456', roles: [{role: 'dbOwner', db: 'admin2'}]})
                       (4)、连接该数据库：mongo 用户名 -u 用户名 -p 密码
```
