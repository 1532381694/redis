  # Redis 学习记录 
  ### Redis 五中数据结构 
  **1. String** 

  操作指令  

  set [key] [value]  

  get [key] [value]  


  Hash Table(Map)
  hset tablename [key] [vale] 
  hset tablename [key2] [value2]
  hgetall tablename \<br>
  hget table [key] \<br>

 **2. List**  

 lpush [listname] [value]
 lrange [listname] [i] [k]
 lpol [listname]
 list 包括 ziplist 、linkedlist
 linkedlist 占用的内存比ziplist多，所以当创建新的列表时，会优先选择ziplist,当一下条件发生时，ziplist -> linkedlist
 1. 向列表中添加一个值时,当值的长度大于64
 2. ziplist的节点长度大于512
 
 
 最开始的数据li

**3. Set**

**4. Sorted Set**


//查看所有key
keys *
//查看特定开头的key
keys name*
//scan
scan 0 match name*

//scan 和keys的区别
使用keys 时会阻塞io主线程 ，而scan 不会阻塞主线程
keys 是一次性返回,scan是多次返回，scan 扫描出来的数据有可能重复，需要业务逻辑去重




## redis mysql 数据同步
查看mysql binlog 模式  
show variables like "%binlog_format%";
