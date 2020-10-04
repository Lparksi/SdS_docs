## 插件
星之子使用[Nonebot](https://github.com/nonebot/nonebot) ，采用模块化设计。
最新的插件列表参见[README](https://github.com/Lparksi/Sohn_des_Sterns/blob/master/README.md) 或相应版本的 [Releases](https://github.com/Lparksi/Sohn_des_Sterns/releases)说明。
## 插件列表：
| 插件 | 详情 | Only to me* | Version | 权限 All/Super/Admin |
| --- | --- | --- | ---| --- |
| info | 显示当前群信息 | False | 0.0.1 | All |
| hitokoto | 发送一句诗词 | False | 0.0.1 | All |
| weather | 查询天气 | False | 0.0.1 | All |
|Authority | 权限管理 | -| 0.0.1 | -|
| Restart | 重启 | False | 0.0.1 | Admin |
| BingImage | 必应每日/随机图片 | False | 0.0.1 | All|
| TTS | 语音转文字 | False | 0.0.1 | All |
|word_slices| 分词 | False | 0.0.1 | All |

## 插件详情
### info
发送当前群和机器人的基本消息。
.info
### hitokoto
采用 [hitokoto](https://hitokoto.cn/) 提供的API接口
.一言
### weather
采用 [和风天气](https://dev.heweather.com/) 作为数据源，*需要配制key*。
.weather
### Authority
权限系统。
获取权限：在管理员列表中的用户,向`机器人`发送' .sudo或.以神之名 即可获得限时的对应的权限。
提供方法：
- `plugins.Authority.checkSupers` 检查超级管理员权限，返回值为布尔型。
- `plugins.Authority.checkAdmins` 检查管理员权限，返回值为布尔型。
.sudo .以神之名
### Restart
重启服务端(go-cqhttp)，需要权限：最低`管理员`
.restart
### BingImage
必应每日/随机图片。
.每日一图 .一图
### TTS
文字转语音。
.tts
### word_slices
分词。
.分词
