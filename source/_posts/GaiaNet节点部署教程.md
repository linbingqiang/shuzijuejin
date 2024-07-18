---
title: GaiaNet节点部署教程
date: 2024-07-15 17:14:22
categories: 节点教程
cover: ![gaianet.png](..%2Fimages%2Fcover%2Fgaianet.png)
---

# 项目介绍
## 项目基本信息
GaiaNet 是一个去中心化网络，提供安全、抗审查和可货币化的人工智能代理，融合每个人的专有知识和技能，同时保护隐私。 GaiaNet 没有建立集中式服务器，而是构建一个由个人和企业控制的边缘计算节点的分布式网络，以基于节点运营商专有的领域知识和专业知识来托管经过微调的人工智能模型。
## 融资信息
| 序号 | 时间  | 金额  |  轮次   |
| ------ | ------ | ------ | ------ |
| 1    | 2024-05-28 | 1000美元 | 种子轮   |

# 节点部署教程
## 节点配置要求
最低需要8G内存
## 部署教程
以下脚本不区分具体的操作系统类型。Windows系统可以打开powershell执行。
1. 执行命令
```shell 
curl -sSfL 'https://github.com/GaiaNet-AI/gaianet-node/releases/latest/download/install.sh' | bash
```
当出现以下结果时，说明命令执行成功。
![install.jpg](..%2Fimages%2Fpage%2F%08gaianet%2Finstall.jpg)
2. 执行命令
```shell 
source /root/.bashrc
```
3. 执行初始化命令
```shell
gaianet init
```
执行结果如下图所示
![init命令.jpg](..%2Fimages%2Fpage%2F%08gaianet%2Finit%E5%91%BD%E4%BB%A4.jpg)
4. 执行启动命令
```shell
gaianet start
```
执行过程如下图所示
![start.jpg](..%2Fimages%2Fpage%2F%08gaianet%2Fstart.jpg)
<span style="background-color:rgb(100,200,200,0.5)">PS:当这一步执行时，没有出现https://0x************.us.gaianet.network时，说明机器的配置不足，可以换一下具体的模型。
比如对于只有6G内存的机器，可以使用其他模型，如：Qwen-1.5-0.5b-chat node。只需要替换第三步的init命令为如下命令即可：
</span>
```shell
gaianet init --config https://raw.githubusercontent.com/GaiaNet-AI/node-configs/main/qwen-1.5-0.5b-chat/config.json
```
其余步骤均一样。
5. 连接钱包
访问项目网站[GaiaNet官网](https://www.gaianet.ai/)，连接钱包
![website.jpg](..%2Fimages%2Fpage%2F%08gaianet%2Fwebsite.jpg)
6. 查询节点信息
执行以下命令获取已经部署上去的节点信息
```shell
gaianet info
```
![nodeinfo.jpg](..%2Fimages%2Fpage%2F%08gaianet%2Fnodeinfo.jpg)
7. 绑定节点
选择AddNode按钮。如图所示。
![addNode.jpg](..%2Fimages%2Fpage%2F%08gaianet%2FaddNode.jpg)
将第六步的NodeId和DeviceId填入，然后点击Join就可以。
![addNode1.jpg](..%2Fimages%2Fpage%2F%08gaianet%2FaddNode1.jpg)
8. 与机器人聊天
进入chat页面，选择对应的node进行聊天即可。
![chat.jpg](..%2Fimages%2Fpage%2F%08gaianet%2Fchat.jpg)