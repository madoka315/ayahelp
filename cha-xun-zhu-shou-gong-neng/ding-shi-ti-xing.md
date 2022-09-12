# 定时提醒

<details>

<summary>开源地址</summary>

[https://github.com/Tsuk1ko/cq-picsearcher-bot](https://github.com/Tsuk1ko/cq-picsearcher-bot)

</details>

{% hint style="info" %}
`<>`表示参数任取；`[]`表示参数可以省略。
{% endhint %}

{% hint style="info" %}
需要学会<mark style="color:blue;">crontab表达式</mark>才可以方便地使用这个功能。可以[参考这里](https://www.cnblogs.com/yanghj010/p/10875151.html)。
{% endhint %}

#### 该服务默认<mark style="color:green;">启用</mark>；不可开关

| 指令示例                                                                                                                                                                                                                                                                                                                                                                                  | 功能说明           | 备注                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------- | ------------------------------------------------------------------------------------- |
| <p>--time=<em>cron表达式</em> [--origin] --rmd=<em>内容</em><br><mark style="background-color:red;">例：</mark><br><mark style="background-color:red;">--time=</mark><em><mark style="background-color:red;">/60;</mark></em><mark style="background-color:red;">/1;</mark><em><mark style="background-color:red;">;</mark></em><mark style="background-color:red;">;* --rmd=阿巴阿巴</mark></p> | 设置定时提醒         | <p>--time= 后接crontab表达式（示例指令表示每小时提醒） --rmd= 后接提醒内容，可为任意类型内容 <br>--origin 为转义CQ码选项</p> |
| --rmd-list                                                                                                                                                                                                                                                                                                                                                                            | 查看已设置的定时提醒及其编号 |                                                                                       |
| --rmd-del=_编号_                                                                                                                                                                                                                                                                                                                                                                        | 删除指定编号的定时提醒    |                                                                                       |
