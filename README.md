Redis 学习记录
Redis 五中数据结构
//String
操作指令
set [key] [value]
get [key] [value]

Hash Table(Map)
hset tablename [key] [vale]
hset tablename [key2] [value2]
hgetall tablename
hget table [key]

 List
 list 包括 ziplist 、linkedlist
 linkedlist 占用的内存比ziplist多，所以当创建新的列表时，会优先选择ziplist,当一下条件发生时，ziplist -> linkedlist
 1. 向列表中添加一个值时,当值的长度大于64
 2. ziplist的节点长度大于512

Set

Sorted Set
