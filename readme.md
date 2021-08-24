## tofu-middleware-cors
CORS （Cross-Origin Resource Sharing，跨域资源共享）middleware of tofu

### 安装

```lua
-- 在项目配置文件 tofu.package.lua 添加

deps = {

	-- 
	-- 其它配置 ... 
	--

	'd80x86/tofu-middleware.cors',
}

```

```sh
## 使用tofu安装
./tofu install

```




### 使用

```lua
-- 项目配置文件 conf/middleware.lua

middleware = {
	-- ... trace 中间件
	-- ..
	-- 添加跨域中间件
	'resty.tofu.middleware.cors'

	-- .. 其它中间件.. router, payload, ....
}

```




### 配置options

| 参数名            | 类型   | 缺省值                         |
| ----------------- | ------ | ------------------------------ |
| allow_methods     | string | GET,HEAD,PUT,POST,DELETE,PATCH |
| allow_credentials | bool   | 不置将怱略                     |
| allow_origin      | string | 不置将自动检测                 |
| allow_headers     | string | 不置将自动检测                 |
| expose_heaers     | string | 不置将自动检测                 |
| max_age           | int    | 不置将使用设备默认             |

> 参数详细可参考 https://developer.mozilla.org/zh-CN/docs/Glossary/CORS



