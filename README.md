# 局域网PC与手机互传文件

## 目的

为了进一步学习Go语言，了解Go语言开发项目的流程。

## 收获

- 知道websocket与http的区别
- 知道如何用 Go 写一个发布订阅（websocket）
- `channel可以在go协程之间通信`这句话理解更深了
- 知道Gin框架中文件流是直接下载（c.File），而c.Data可以展示在前端页面（不是直接下载的）

## 参考
```text
https://github.com/FrankFang/synk

https://www.bilibili.com/video/BV1aF411t7w9/?share_source=copy_web&vd_source=1068a5fa51e306b8564255b5bf628111
```

## 使用

1. `main.go`中第`30`行是固定的chrome路径，如果你的电脑没有chrome，可以换成edge或者其他。
```text
30 | chromePath := "C:\\Program Files\\Google\\Chrome\\Application\\chrome.exe"
```
2. Windows用户需要在防火墙的入站规则中运行 27149 端口的连接，否则此软件无法被手机访问。
```text
打开Windows安全中心，选择“防火墙和网络保护”，选择“高级设置”，选择“入站规则”，选择“新建规则”，选择“端口”，选择“TCP“，输入27149，点击“下一步”，选择“允许连接”，点击“完成”。
```
