# 聚合函数 <Badge text="0.5.5+" type="error"/>

## count
- 入参：`target`:`Object`  
- 返回值：`int`
- 函数说明：计算集合大小
```js
var list = [1,2,3,4,5]
return count(list);  // 5
```

## sum
- 入参：`target`:`Object`  
- 返回值：`Number`
- 函数说明：对集合进行求和
```js
var list = [1,2,3,4,5]
return sum(list);  // 15
```

## max
- 入参：`target`:`Object`  
- 返回值：`Object`
- 函数说明：求集合最大值
```js
var list = [1,2,3,4,5]
return max(list);  // 5
```

## min
- 入参：`target`:`Object`  
- 返回值：`Object`
- 函数说明：求集合最小值
```js
var list = [1,2,3,4,5]
return min(list);  // 5
```

## avg
- 入参：`target`:`Object`  
- 返回值：`Object`
- 函数说明：求集合平均值
```js
var list = [1,2,3,4,5]
return min(list);  // 3
```

## group_concat
- 入参：`target`:`Object`  
- 入参：`separator`:`String` 分隔符，可省略
- 返回值：`Object`
- 函数说明：将集合拼接起来
```js
var list = [1,2,3,4,5]
return group_concat(list);  // "1,2,3,4,5"
// return group_concat(list,'|');  // "1|2|3|4|5"
```