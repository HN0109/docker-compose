启动后初始化复制集

   ```shell
   # 进入容器
   $ docker exec -it mongo1 bash
   # 连接mongodb
   $ mongosh
   # 切换到admin数据库
   $ use admin
   # 复制集配置
   $ var cfg ={
       "_id": "rs0",
       "protocolVersion": 1,
       "members": [
           {
               "_id": 1,
               "host": "192.168.60.1:27011",
               "priority": 10
           },
           {
               "_id": 2,
               "host": "192.168.60.1:27012",
               "priority": 20
           },
           {
               "_id": 3,
               "host": "192.168.60.1:27013",
               "priority": 5
           }
       ]
   }
   # 初始化复制集
   $ rs.initiate(cfg)
   # 查看复制集状态
   $ rs.status()
   ```