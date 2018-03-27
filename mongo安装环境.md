###  安装mongodb之后学会添加系统环境变量 path 
###       把mongod.exe和mongo.exe文件所在的目录添加到Path
##   启动mongo服务
###    在命令行执行 mongod --dbpath=指定目录 --storageEngine=mmapv1
###    服务器开启之后，占用的系统端口号：27017
###    连接服务器 mongo
###     退出mongo环境 ，使用exit或者ctrl+c 默认连接的数据 test(空)
###     当前服务器系统下所有的数据库  show dbs
###     选择/创建数据库（如果不存在自动创建）    use school   switched to db school
###       删除数据库     db.dropDatabase() { "ok" : 1 }
###         查看当前所在的数据库  db schol    db.getName()
##      MongoDB中数据库系统：  
###             数据库	database 
###		            集合 	collection
###			            文档	document
###				            字段 field 字段值 value
###    创建一个stu集合并插入一条文档(如果stu不存在自动创建) 
####        db.stu.insert({"name":"小丁丁","age":"23","sex":"1"})
#####           WriteResult({ "nInserted" : 1 })
###     查询stu集合中的所有的数据
####      db.stu.find()
###     显示当前数据库下所有的集合
####     show collections   
###     // 当前其他集合中所有的索引
####        system.indexes
###     创建集合 class
####       db.createCollection('class')
###   插入数据 -- 插入类型的数据
####     db.stu.insert({"name":"孙悟空","age":300,sex:"1"})
###     删除一条记录
####        db.stu.remove({name:'李世民'}))
###      更新 db.stu.update()