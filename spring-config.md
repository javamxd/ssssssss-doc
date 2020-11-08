# spring-boot配置

## prefix
- 类型：`String`
- 默认值：`null`

`magic-api.prefix` 接口路径的前缀，可空

## web
- 类型：`String`
- 默认值：`null`

`magic-api.web` WEB页面的请求路径，可空，填写时开启，否则不开启，生产环境建议不开启

## banner
- 类型：`boolean`
- 默认值：`true`

`magic-api.banner` 是否打印banner

## map-underscore-to-camel-case
- 类型：`boolean`
- 默认值：`true`

`magic-api.map-underscore-to-camel-case` 是否开启下划线转驼峰命名

## throw-exception
- 类型：`boolean`
- 默认值：`false`

`magic-api.throw-exception` 执行出现异常时是否抛出异常（默认不抛出异常）

## datasource
- 类型：`String`
- 默认值：`null`(默认数据源)

`magic-api.datasource` 接口存储选择的数据源（默认使用默认数据源）

## auto-import-module <Badge text="0.3.2+" type="error"/>
- 类型：`String`
- 默认值：`db`(默认导入db模块，多个值时用","分隔)

`magic-api.auto-import-module` 默认导入的模块

## refresh-interval <Badge text="0.3.4+" type="error"/>
- 类型：`int`
- 默认值：`0` （<=0为不启用）

`magic-api.refresh-interval` 自动刷新间隔(单位为秒)，开启后定期从数据库读取接口信息并刷新映射。

## auto-import-package <Badge text="0.4.0+" type="error"/>

- 类型：`String`
- 默认值(v0.4.0+)：`java.lang.*,java.util.*`(多个值时用","分隔，目前只支持以.*结尾的通配符)
- 默认值(v0.4.5+)：`null`，`java.lang.*,java.util.*`转为内置自动导入

`magic-api.auto-import-package` 默认导入的包

## allow-override <Badge text="0.4.0+" type="error"/>

- 类型：`boolean`
- 默认值：`false`

`magic-api.allow-override` 是否允许覆盖应用接口

## thread-pool-executor-size <Badge text="0.4.5+" type="error"/>

- 类型：`int`
- 默认值 : `0`  `<=0` 表示`CPU 核心数 * 2`

`magic-api.thread-pool-executor-size` 异步调用的线程池大小

## page-config

分页配置

### page
- 类型:`string`
- 默认值:`page`

`magic-api.page-config.page`页码参数名

### size
- 类型:`string`
- 默认值:`size`

`magic-api.page-config.size`页大小参数名

### default-page
- 类型:`long`
- 默认值:`1`

`magic-api.page-config.default-page`取不到页码参数时的默认页码

### default-size
- 类型:`long`
- 默认值:`10`

`magic-api.page-config.default-size`取不到页大小参数时的默认页大小

## cache-config

缓存配置

### enable
- 类型:`boolean`
- 默认值:`false`

`magic-api.cache-config.enable`是否开启缓存(默认缓存实现是LRU+TTL)

### capacity
- 类型:`long`
- 默认值:`10000`

`magic-api.cache-config.capacity`缓存容量

### ttl
- 类型:`long`
- 默认值:`-1`

`magic-api.cache-config.ttl`缓存过期时间，默认是`-1`即永不过期

## debug-config

DEBUG配置

### timeout

- 类型:`int`
- 默认值：`60`

`magic-api.debug-config.timeout`DEBUG断点等待时间，单位秒，默认为60秒

## swagger-config <Badge text="0.3.0+" type="error"/>

Swagger 配置

### name

- 类型:`string`
- 默认值:`MagicAPI接口`

`magic-api.swagger-config.name` 资源名称

### location
- 类型:`string`
- 默认值:`/v2/api-docs/magic-api/swagger2.json`

`magic-api.swagger-config.location` 资源位置

### title

- 类型:`string`
- 默认值:`MagicAPI Swagger Docs`

`magic-api.swagger-config.title` 文档标题

### description

- 类型:`string`
- 默认值:`MagicAPI 接口信息`

`magic-api.swagger-config.description` 文档描述

### version

- 类型:`string`
- 默认值:`1.0`

`magic-api.swagger-config.version` 文档版本

## security-config  <Badge text="0.4.0+" type="error"/>

安全配置

### username

- 类型: `string`
- 默认值： `null`

`magic-api.security-config.username` 配置登录用的用户名，当用户名和密码都配置时，页面需登录才能访问

### password

- 类型: `string`
- 默认值： `null`

`magic-api.security-config.password` 配置登录用的密码，当用户名和密码都配置时，页面需登录才能访问