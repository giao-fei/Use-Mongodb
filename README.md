# Use-Mongodb<br>
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
