## 配置(小白向)  
### 基本配置
参见[此处](https://sds.parksi.top/guide/#how-to-use-it)  
### 更名
将 `configDefault.py` 更名为 `config.py`
将 `pluginsConfigDefault.py` 更名为 `pluginsConfig.py`
### 找到3个配置文件
打开星之子的配置文件`config.py` , `pluginsConfig.py` 与 go-cqhttp的配置文件`config.json`
::: details 星之子配置
```py {9-10}
from nonebot.default_config import *

SUPERUSERS = {} # 超级管理员
ADMINS = {} # 管理员
OWNER = {} # 所有者

COMMAND_START = {'.', '/', '／'} # 命令前置符

HOST = "0.0.0.0" # go-cqhttp主机
PORT = 5867 # go-cqhttp端口
```
:::
::: details 星之子插件配置
```py {3-4}
# HTTP Config
# HTTP 配置
HTTP_HOST = "127.0.0.1"
HTTP_PORT = 5700

# 和风天气
# heweather.com
HEWEATHER_KEY = ''
```
:::
::: details go-cqhttp配置
``` js {2,3,35,36,20,22,24}
{
	"uin": 0,  //账户
	"password": "", //密码
	"encrypt_password": false,
	"password_encrypted": "",
	"enable_db": true,
	"access_token": "",
	"relogin": {
		"enabled": true,
		"relogin_delay": 3,
		"max_relogin_times": 0
	},
	"_rate_limit": {
		"enabled": false,
		"frequency": 1,
		"bucket_size": 1
	},
	"ignore_invalid_cqcode": false,
	"force_fragmented": true,
	"heartbeat_interval": 20, //心跳时间
	"http_config": {
		"enabled": true, //开启http
		"host": "127.0.0.1",
		"port": 5700, //配置端口
		"timeout": 0,
		"post_urls": {}
	},
	"ws_config": {
		"enabled": false,
		"host": "0.0.0.0",
		"port": 6700
	},
	"ws_reverse_servers": [
		{
			"enabled": true, //开启反向ws
			"reverse_url": "ws://127.0.0.1:5867/ws/", //配置反向ws
			"reverse_api_url": "ws://you_websocket_api.server",
			"reverse_event_url": "ws://you_websocket_event.server",
			"reverse_reconnect_interval": 3000
		}
	],
	"post_message_format": "string",
	"debug": false,
	"log_level": "",
	"web_ui": {
		"enabled": true,
		"web_ui_port": 9999,
		"web_input": false
	}
}
```
:::
### 进行配置
将所有的主机(HOST)配置为 `127.0.0.1`  
**反向ws与HTTP不要使用一个端口**
下面给出可用的配置：  
主机(HOST):127.0.0.1
反向ws端口：5867
HTTP端口：5700
::: details 星之子配置(config.py)
```py {9-10}
from nonebot.default_config import *

SUPERUSERS = {} # 超级管理员
ADMINS = {} # 管理员
OWNER = {} # 所有者

COMMAND_START = {'.', '/', '／'} # 命令前置符

HOST = "0.0.0.0" # go-cqhttp主机
PORT = 5867 # go-cqhttp端口
```
:::
::: details 星之子插件配置(pluginsConfig.py)
```py {3-4}
# HTTP Config
# HTTP 配置
HTTP_HOST = "127.0.0.1"
HTTP_PORT = 5700

# 和风天气
# heweather.com
HEWEATHER_KEY = ''
```
:::
::: details go-cqhttp配置(config.json)  
**自行配置账户密码**
``` js {2,3,35,36,20,22,24}
{
	"uin": 0,  
	"password": "",
	"encrypt_password": false,
	"password_encrypted": "",
	"enable_db": true,
	"access_token": "",
	"relogin": {
		"enabled": true,
		"relogin_delay": 3,
		"max_relogin_times": 0
	},
	"_rate_limit": {
		"enabled": false,
		"frequency": 1,
		"bucket_size": 1
	},
	"ignore_invalid_cqcode": false,
	"force_fragmented": true,
	"heartbeat_interval": 20,
	"http_config": {
		"enabled": true,
		"host": "127.0.0.1",
		"port": 5700,
		"timeout": 0,
		"post_urls": {}
	},
	"ws_config": {
		"enabled": false,
		"host": "0.0.0.0",
		"port": 6700
	},
	"ws_reverse_servers": [
		{
			"enabled": true,
			"reverse_url": "ws://127.0.0.1:5867/ws/",
			"reverse_api_url": "ws://you_websocket_api.server",
			"reverse_event_url": "ws://you_websocket_event.server",
			"reverse_reconnect_interval": 3000
		}
	],
	"post_message_format": "string",
	"debug": false,
	"log_level": "",
	"web_ui": {
		"enabled": true,
		"web_ui_port": 9999,
		"web_input": false
	}
}
```
:::
