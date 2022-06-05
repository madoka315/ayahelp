---
description: 此页介绍的指令用于QQ群管理
---

# 群管理

<details>

<summary>开源地址</summary>

[https://github.com/pcrbot/group-manager](https://github.com/pcrbot/group-manager)

</details>

{% hint style="info" %}
`<>`表示参数任取；`[]`表示参数可以省略。
{% endhint %}

{% hint style="warning" %}
若有功能在你的群不可用，可能是由于近期发生管理员变动/群主变动/Gocq框架缓存问题，等待一段时间即可。&#x20;

多个指令涉及群管操作，慎重将群主转移给Aya(可从[huifu.qq.com](https://huifu.qq.com/)恢复群主)。如转移后可私聊我为你设置管理员。
{% endhint %}

#### 该服务默认<mark style="color:green;">启用</mark>

| 指令示例                | 功能说明            | 备注      |
| ------------------- | --------------- | ------- |
| 申请头衔 \[_@qq_] _内容_  | (为@qq)申请专属头衔    | 至少需要群主  |
| 删除头衔 \[_@qq_]       | (为@qq)删除头衔      | 至少需要群主  |
| 塞口球 \[_@qq_] _秒数_   | 禁言自己/禁言@qq      | 至少需要管理员 |
| 解除口球 _@qq_          | 解除@qq的禁言        | 至少需要管理员 |
| 全员禁言                |                 | 至少需要群主  |
| 取消全员禁言              |                 | 至少需要群主  |
| 修改名片 \[_@qq_] _内容_  | 修改群名片/修改@qq的群名片 | 至少需要管理员 |
| 修改群名 _内容_           |                 | 至少需要管理员 |
| 帮我发公告 _内容_          | 发公告             | 至少需要管理员 |
