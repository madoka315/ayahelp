---
description: 此页介绍的指令用于PCR公会战功能
---

# 公会战功能

{% hint style="info" %}
处理查看`<>`表示参数任取；`[]`表示参数可以省略。
{% endhint %}

{% hint style="success" %}
**请注意：**Aya是以yobot为基础提供公会战功能的。\
~~根据~~[~~官方repo~~](https://github.com/yuudi/yobot)~~的说明，它不会为PCR新版公会战（即5个boss可同时出刀、存补偿等）的规则提供适配和支持，**而Hoshino ClanbattleV4是一个非开源项目**。~~\
~~因此预计在2023年6月左右，Aya将移除公会战功能，或仅保留一部分功能。除非本人有足够精力开发，或有新的开源替代。~~\
2023年4月，Aya已迁移至yobot\_remix，适配新版公会战
{% endhint %}

## 核心指令

注：仅列举常用。更详细的帮助请查看[yobot帮助](https://madoka.fun/help/)。

注：如你是第一次使用公会战而不知道怎么开始，可以看一遍[yobot公会战手册](https://madoka.fun/manual)。

建议一般出刀按照以下流程使用指令：\
<mark style="color:green;">申请出刀x(使用补偿时注明)</mark> -> <mark style="color:green;">更新出刀：...</mark> 或 <mark style="color:green;">挂树|SL</mark>-> <mark style="color:green;">状态</mark> -> <mark style="color:green;">报刀xxx</mark> 或 <mark style="color:green;">尾刀</mark>

| 指令示例                                                                                                                                                                                                                                                                                                                          | 功能说明                      | 备注                                                                                                      |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------- | ------------------------------------------------------------------------------------------------------- |
| 面板                                                                                                                                                                                                                                                                                                                            | 公会战网页端                    | 也可以在此帮助文档的上方点击                                                                                          |
| <p>申请出刀 <em>boss编号</em> <em>[是否补偿] [@qq]</em><br><em><mark style="background-color:red;">例如：</mark></em><br><em><mark style="background-color:red;">申请出刀 2补</mark></em></p>                                                                                                                                                   | 决定出刀                      | <p>是否是补偿可用&#x3C;b,补>表示；<br>如不指定是补偿，则只有当完整刀使用完后自动使用补偿</p>                                                |
| 取消出刀 _\[@qq]_                                                                                                                                                                                                                                                                                                                 | 放弃刚才的申请                   |                                                                                                         |
| <p>更新出刀[：][秒数]<em>伤害数字[备注] [@qq]</em><br><em><mark style="background-color:red;">例如：</mark></em><br><em><mark style="background-color:red;">更新出刀：1000w</mark></em><br><em><mark style="background-color:red;">更新出刀：200万 打烂了</mark></em><br><em><mark style="background-color:red;">更新出刀：5s500w</mark></em></p>                | 更新自己的出刀情况                 | 伤害数字最好使用...w(万)，否则可能有显示的问题                                                                              |
| <p>报刀 <em>[boss编号]</em> <em>伤害数字 [是否补偿] [@qq]</em> [昨日]<br><em><mark style="background-color:red;">例如：</mark></em><br><em><mark style="background-color:red;">报刀 1000w</mark></em><br><em><mark style="background-color:red;">报刀 200w补</mark></em><br><em><mark style="background-color:red;">报刀 5 200w</mark></em><br>撤销</p> | 报刀与撤销                     | <p>已经申请出刀的情况下，不用指定boss编号；<br>申请出刀时已经指定补偿的情况下，报刀无需指定，否则需要；<br>如不指定是补偿，则会自动判断，可能错误使用完整刀；<br>撤销仅能一刀一刀来</p> |
| 尾刀                                                                                                                                                                                                                                                                                                                            | 击败boss时尾刀                 |                                                                                                         |
| <p>SL<br>SL?</p>                                                                                                                                                                                                                                                                                                              | 记录与查询SL                   | 可在面板查看全员sl情况                                                                                            |
| 状态                                                                                                                                                                                                                                                                                                                            | 查询当前公会战进展                 |                                                                                                         |
| 刀伤 _\[@qq]_                                                                                                                                                                                                                                                                                                                   | 查询今日出刀的伤害                 |                                                                                                         |
| <p>预约 <em>数字</em><br>取消预约 <em>数字</em></p>                                                                                                                                                                                                                                                                                     | 预约boss，当状态来到对应boss时获得艾特提醒 |                                                                                                         |
| 预约表                                                                                                                                                                                                                                                                                                                           | 查询预约列表                    |                                                                                                         |

## 附加指令

提供公会战的其他便利功能。

<details>

<summary>开源地址</summary>

公会战报告：[https://github.com/zyujs/clanbattle\_report](https://github.com/zyujs/clanbattle\_report)

公会战排名：[https://github.com/zyujs/clanbattle\_rank](https://github.com/zyujs/clanbattle\_rank)

补偿轴计算器：[https://github.com/OREOCODEDEV/pcr\_time\_calculator](https://github.com/OREOCODEDEV/pcr\_time\_calculator)

</details>

### 助战需求提醒

**该服务默认**<mark style="color:red;">**禁用**</mark>

<table><thead><tr><th>指令示例</th><th width="294">功能说明</th><th>备注</th></tr></thead><tbody><tr><td>助战需求</td><td>查看当前助战需求列表</td><td>有助战需求时，会定时推送</td></tr><tr><td>&#x3C;挂个,挂一下,挂只><em>[等级][rank][星级]角色</em></td><td>新增一个助战需求，有人挂时会获得at提醒</td><td></td></tr><tr><td>&#x3C;挂了,已挂><em>[@qq]</em></td><td><p>表示挂了助战</p><p>如果只有一个助战需求则表示挂了相应助战，否则需要at成员来表示已经帮ta挂了助战</p></td><td></td></tr><tr><td>&#x3C;挂了,已挂> <em>编号</em></td><td>表示挂了对应编号的助战</td><td></td></tr></tbody></table>

### 公会战报告

**该服务默认**<mark style="color:green;">**启用**</mark>

<table><thead><tr><th>指令示例</th><th width="294">功能说明</th><th>备注</th></tr></thead><tbody><tr><td>设置公会api <em>地址</em></td><td>为报告的生成提供数据来源地址</td><td>在面板-统计-获取api按钮可以取得公会的对应地址<br>至少需要管理员</td></tr><tr><td>查看公会api</td><td></td><td>至少需要管理员</td></tr><tr><td>清除公会api</td><td></td><td>至少需要管理员</td></tr><tr><td>生成会战报告 <em>[@qq]</em></td><td>根据yobot的报刀数据生成报告图</td><td>至少需要管理员</td></tr></tbody></table>

### 合刀与垫刀计算

**该服务默认**<mark style="color:green;">**启用**</mark>

<table><thead><tr><th width="326.5619596541787">指令示例</th><th width="203.14936861562407">功能说明</th><th>备注</th></tr></thead><tbody><tr><td>合刀计算 <em>刀1伤害</em> <em>刀2伤害</em> <em>BOSS血量</em></td><td>计算合刀时每个人能返还多少补偿</td><td></td></tr><tr><td>垫刀计算 <em>BOSS血量</em> <em>当前伤害</em> <em>当前显示秒数 目标补偿秒数</em></td><td>计算某boss需要垫多少伤害才能达到目标补偿秒数</td><td>一般用于一穿二</td></tr></tbody></table>

### **补偿轴计算**

**该服务默认**<mark style="color:green;">**启用**</mark>

<table><thead><tr><th width="326.5619596541787">指令示例</th><th width="203.14936861562407">功能说明</th></tr></thead><tbody><tr><td>补偿轴 <em>返还时间</em> <em>时间1</em> <em>[时间2 ...]</em><br><em><mark style="background-color:red;">例：</mark></em><br><mark style="background-color:red;">补偿轴 56 102 100 56 54</mark></td><td>计算返还时间下对应的时间轴</td></tr></tbody></table>

### 公会战排名

**该服务默认**<mark style="color:green;">**启用**</mark>

<table><thead><tr><th width="250.74654477477173">指令示例</th><th width="203.14936861562407">功能说明</th><th>备注</th></tr></thead><tbody><tr><td>查询排名 <em>公会名</em> <em>[会长名</em>]</td><td>查询指定公会排名</td><td>如果公会重名了 需要附带会长名</td></tr><tr><td>添加关注 <em>公会名 [会长名</em>]</td><td>关注公会，这样就可以直接<code>查询关注</code></td><td>至少需要管理员</td></tr><tr><td>查询关注</td><td>查询关注的公会信息</td><td></td></tr><tr><td>查询分段</td><td>查询分段信息</td><td></td></tr><tr><td>删除关注 <em>公会名</em></td><td>删除指定的关注公会</td><td>至少需要管理员</td></tr><tr><td>清空关注</td><td>清空关注列表</td><td>至少需要管理员</td></tr></tbody></table>

### 公会战作业

{% content-ref url="cha-xun-zhu-shou-gong-neng/gong-hui-zhan-zuo-ye.md" %}
[gong-hui-zhan-zuo-ye.md](cha-xun-zhu-shou-gong-neng/gong-hui-zhan-zuo-ye.md)
{% endcontent-ref %}
