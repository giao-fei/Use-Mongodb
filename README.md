# Use-Mongodb<br>
一、开启mongodb服务：<br>
        (1)、先新建一个文件夹 mongodb 然后在cmd里面  mongod --dbpath D:\nodejs\MongoDB\mongodb<br>   
二、连接Mongodb服务：开启 cmd 输入 mongo<br>
三、创建一个数据库（giao）：use giao 然后再创建一个集合 (giao)<br> 
        (1) use giao<br>
        (2)  db.giao.insert({"":""})<br>
        (3)  展示 giao 这个数据库中所有的集合：先 use 到 giao 数据库中，然后再 show collections<br>
四、删除 giao 这个数据库：先切换到giao这个数据库中：use giao 然后输入db.dropDatabase()<br>
      （1）删除giao库中的giao表: 先进到这个库里面 db.表名.drop()<br>
五、查看所有数据库：show dbs<br>
      （2）查看giao数据库中所有的表：show tables<br>
六、在mongodb数据库中giao这张表中插入数据：db.giao.insert({"name":"hello world","age":"1000"})<br>
七、查找giao数据库中giao表中的数据：db.giao.find()<br>
八、替换giao 数据中giao表中的数据 db.giao.udpade({"name":"hello world","age":"1000"},{"name":"你好 世界",age:"500 "})<br>
九、移除giao数据库中giao表的数据  db.giao.remove({"name":"你好 世界","age":"500"})
十、数据包导出：mongodump -h dbhost(主机+端口号) -d dbname(数据库名称)  -o  dbdirectory(要导出的路径)
十一、数据包导入： mongorestore -h dbhost -d dbname(数据库名称 名称可以随便取一个) <path>(数据包存放的路径)
