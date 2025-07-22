### 工具介绍

🚀 DeepSeek-V3 & R1大模型逆向API【特长：良心厂商】（官方贼便宜，建议直接走官方），支持高速流式输出、多轮对话，联网搜索，R1深度思考，零配置部署，多路token支持，仅供测试，如需商用请前往官方开放平台。

> 更新说明：原作者v0.0.21版本由于官方更新了接口已无法在客户端正常使用，根据issue中其他人提供的fork项目修改，构建了v0.0.22版本

> 这是修改版本的地址 [https://github.com/Fu-Jie/deepseek-free-api](https://github.com/Fu-Jie/deepseek-free-api),风险自行承担，或暂停使用等待原作者更新吧


![](https://cdn.jsdelivr.net/gh/xiaoY233/PicList@main/public/assets/Free-API.png)

![](https://img.shields.io/badge/Copyright-arch3rPro-ff9800?style=flat&logo=github&logoColor=white)

### 风险说明

- 逆向API是不稳定的，建议前往DeepSeek官方 https://platform.deepseek.com/ 付费使用API，避免封禁的风险。

- 本组织和个人不接受任何资金捐助和交易，此项目是纯粹研究交流学习性质！

- 仅限自用，禁止对外提供服务或商用，避免对官方造成服务压力，否则风险自担！

### 使用说明

#### 版本说明： 

- latest：其他fork修改版，本人clone后构建镜像，打包上传dockerhub，无任何代码修改
- 0.0.21: 原作者docker镜像版本，暂时无法使用，等待后续更新
- 0.0.22: 其他fork修改版，本人clone后构建镜像，打包上传dockerhub，无任何代码修改


请确保您在中国境内或者拥有中国境内的个人计算设备，否则部署后可能因无法访问DeepSeek而无法使用。

从 [DeepSeek](https://chat.deepseek.com/) 获取userToken value

进入DeepSeek随便发起一个对话，然后F12打开开发者工具，从Application > LocalStorage中找到`userToken`中的value值，复制这个值填写到Lobechat或者CherryStudio等工具中，作为API密钥，API地址是你部署应用的IP加端口，例如:`https://192.168.1.105:8001/v1/chat/completions`，注意某些工具只需要填写`https://192.168.1.105:8001/`即可。

[![获取userToken](https://cdn.jsdelivr.net/gh/LLM-Red-Team/deepseek-free-api@master/doc/example-0.png)](https://cdn.jsdelivr.net/gh/LLM-Red-Team/deepseek-free-api@master/doc/example-0.png)

### 多账号接入

目前同个账号同时只能有*一路*输出，你可以通过提供多个账号的userToken value并使用`,`拼接提供：

```
API密钥：TOKEN1,TOKEN2,TOKEN3
```

每次请求服务会从中挑选一个。
