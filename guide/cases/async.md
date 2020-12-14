# 异步调用

## 调用普通方法
```javascript    
// 使用async关键字，会启动一个线程去执行，返回Future，并不等待结果继续执行后续代码
var user1 = async db.select("select * from sys_user where id = 1");
var user2 = async db.select("select * from sys_user where id = 2");
// 调用get方法表示阻塞等待获取结果
return [user1.get(),user2.get()];
```

## 调用lambda
```javascript
var list = [];
/*
var selectUser = (userId)=>db.select("select * from sys_user where id = #{userId}");
for(index in range(1,10)){
    list.add(async selectUser(index));
}
*/
for(index in range(1,10)){
    list.add(async (index)=>db.select("select * from sys_user where id = #{index}"));
}
// 以上两种方式都可以
return list.map(item=>item.get());
```