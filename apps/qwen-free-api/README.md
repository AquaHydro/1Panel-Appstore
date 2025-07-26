### 工具介绍

🚀 阿里通义千问2.5大模型逆向API【特长：六边形战士】，支持高速流式输出、无水印AI绘图、长文档解读、图像解析、联网检索、多轮对话，零配置部署，多路token支持，自动清理会话痕迹，仅供测试，如需商用请前往官方开放平台。

![](https://cdn.jsdelivr.net/gh/xiaoY233/PicList@main/public/assets/Free-API.png)

![](https://img.shields.io/badge/Copyright-arch3rPro-ff9800?style=flat&logo=github&logoColor=white)

### 风险说明

- 逆向API是不稳定的，建议前往阿里云官方 https://dashscope.console.aliyun.com/ 付费使用API，避免封禁的风险。

- 本组织和个人不接受任何资金捐助和交易，此项目是纯粹研究交流学习性质！

- 仅限自用，禁止对外提供服务或商用，避免对官方造成服务压力，否则风险自担！


### 使用说明

从 [通义千问](https://tongyi.aliyun.com/qianwen) 登录

进入通义千问随便发起一个对话，然后F12打开开发者工具，从Application > Cookies中找到tongyi_sso_ticket的值，复制这个值填写到Lobechat或者CherryStudio等工具中，作为API密钥，API地址是你部署应用的IP加端口，例如:`https://192.168.1.105:8001/v1/chat/completions`，注意某些工具只需要填写`https://192.168.1.105:8001/`即可。

![获取tongyi_sso_ticket](https://cdn.jsdelivr.net/gh/LLM-Red-Team/qwen-free-api@master/doc/example-0.png)

### 支持qwen3模型

Qwen3是阿里云Qwen团队研发的大型语言模型系列。

当前版本支持Qwen3和Qwen3-Coder等模型使用，需要手动添加模型，模型ID为`qwen3-coder-plus`, 模型名称随便填写

![](https://cdn.jsdelivr.net/gh/xiaoY233/PicList@main/public/assets/Qwen3-Coder.png)

详细模型ID参考
[阿里云百炼官方文档](https://bailian.console.aliyun.com/?tab=doc#/doc/?type=model&url=https%3A%2F%2Fhelp.aliyun.com%2Fdocument_detail%2F2840914.html&renderType=iframe)


### 多账号接入

目前同个账号同时只能有*一路*输出，你可以通过提供多个账号的userToken value并使用`,`拼接提供：

```
API密钥：TOKEN1,TOKEN2,TOKEN3
```
每次请求服务会从中挑选一个。
