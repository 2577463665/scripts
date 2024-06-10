- [环境变量说明](#环境变量说明)
  - [掘金社区](#掘金社区)
  - [SSPANEL面板](#sspanel面板)
  - [阿里云盘](#阿里云盘)
  - [百度贴吧](#百度贴吧)
  - [司机社](#司机社)
  - [V2EX](#v2ex)
  - [海贼王论坛](#海贼王论坛)
  - [智能电视](#智能电视)
  - [消息推送变量（可选）](#消息推送变量可选)

### 掘金社区

|      Name       |         Value         |                             说明                             |
| :-------------: | :-------------------: | :----------------------------------------------------------: |
| `JUEJIN_COOKIE` | `xxxxxxxxxxxxxxxxxxx` | 掘金 Cookie，打开[掘金社区](https://juejin.cn/) F12，选择 Application，点击 Cookies 只要 `sessionid` 的值并填入 Secrets 即可，多个掘金号用 `&` 隔开 `xxxxxxxx&xxxxxxxx` |

![images](https://img2.imgtp.com/2024/05/19/M3EbSqId.png)

### SSPANEL面板

|      Name       |                      Value                      |                             说明                             |
| :-------------: | :---------------------------------------------: | :----------------------------------------------------------: |
| `SITE_ACCOUNTS` | 要执行签到的`网站,账号:密码`，多个请用 `&` 分割 | 单账号填写规则 e.g：`https://paolu.com,aaa@gmail.com:123456`<br/>多个填写规则：`https://aaa.com,aaa@gmail.com:aaa&https://bbb.com,bbb@gmail.com:bbb&...以此类推`<br/>中文说明：`网站,账号:密码`，多个：`网站,账号:密码&网站,账号:密码`<br/>网站与账号密码之间用`英文逗号`（`,`）分割，账号与密码之间用`英文冒号`（`:`）分割 |

**说明**

1. SSPANEL 签到暂不支持密码带  `,`  与  `:`  的字符！
2. **<font color='red'>SSPANEL 签到暂不支持带有图形验证码的机场网站！</font>**

### 阿里云盘

|        Name         |              Value              |                  说明                   |
| :-----------------: | :-----------------------------: | :-------------------------------------: |
| `ALI_REFRESH_TOKEN` | `e7b02b2k52074om8td187c62952cf` | 阿里云盘 referesh token 多个用 `&` 分开 |

**5.22：抓包发现获取奖励的接口请求头多了签名算法，本人能力有限，暂时移除了获取奖励接口，仅支持签到，介意勿用!!**

**说明**：如何获取 **referesh token?**

**第一种**：打开[阿里云盘](https://www.aliyundrive.com/)，登录后 `F12` 在控制台输入以下代码即可获取

```javascript
JSON.parse(localStorage.token).refresh_token
```

**第二种**： 使用 Alist 的在线获取

打开 [Alist 文档#刷新令牌](https://alist.nn.ci/zh/guide/drivers/aliyundrive.html#%E5%88%B7%E6%96%B0%E4%BB%A4%E7%89%8C)，点击获取 Token，然后使用阿里云盘 APP 扫描，扫描完成后再点击一次即可获取

两种方式任选一种获取 `Referesh Token `

### 百度贴吧

|      Name       |                Value                |                             说明                             |
| :-------------: | :---------------------------------: | :----------------------------------------------------------: |
| `TIE_BA_COOKIE` | eg: `xxxxxxxxxxxxxxxxxxxxxxxxxxxxx` | 打开[百度贴吧](https://tieba.baidu.com/) -> F12，选择 Application，点击 Cookies<br/>只要 `BDUSS` 的值即可<br>多个账号用 `&` 分开 |

![images](https://img2.imgtp.com/2024/05/19/HnlsgpaF.png)

### 司机社

|     Name     |          Value          |                             说明                             |
| :----------: | :---------------------: | :----------------------------------------------------------: |
| `SJS_COOKIE` | eg: `司机社网站@cookie` | 打开司机社网站，F12，选择 Application，点击 Cookies<br/>获取键值对：`SgL6_2132_auth=xxxxxxxxxxx;SgL6_2132_saltkey=xxxxxx` |

**说明：**

由于司机社镜像站有很多，所以任意选择一个网站登录之后，获取 `SgL6_2132_auth` 和 `SgL6_2132_saltkey` 的值即可（包括键也要填写）

网站和 cookie 之间用 `@` 隔开，多个账号用 `&` 隔开。第二个的键值对后面就不要加 `;` 了

单个填写示例：

```markdown
https://xxxxx.com@SgL6_2132_auth=xxxxxxxxxxx;SgL6_2132_saltkey=xxxxxx
```

多个填写示例：用 `&` 隔开

```markdown
https://xxxxx.com@SgL6_2132_auth=xxxxxxxxxxx;SgL6_2132_saltkey=xxxxxx&https://xxxxx.com@SgL6_2132_auth=xxxxxxxxxxx;SgL6_2132_saltkey=xxxxxx
```

### V2EX

|     Name      | Value  |                             说明                             |
| :-----------: | :----: | :----------------------------------------------------------: |
| `V2EX_COOKIE` | Cookie | F12，选择 Network 网络，然后请求选择 `Doc`，把 Cookie 全选复制<br>没有出现 `v2ex.com` 那就 F5 刷新一下 |

![v2ex](https://img2.imgtp.com/2024/05/22/Ce612EwM.png)

### 海贼王论坛

|      Name       |                   Value                    |                             说明                             |
| :-------------: | :----------------------------------------: | :----------------------------------------------------------: |
| `TALKOP_COOKIE` | `3yWf_2132_auth=xxx;3yWf_2132_saltkey=xxx` | 打开司机社网站，F12，选择 Application，点击 Cookies 获取键值对：`3yWf_2132_auth=xxx;3yWf_2132_saltkey=xxx` |

### 智能电视

|     Name      |                   Value                    |                             说明                             |
| :-----------: | :----------------------------------------: | :----------------------------------------------------------: |
| `ZNDS_COOKIE` | `s9it_2132_auth=xxx;s9it_2132_saltkey=xxx` | 打开司机社网站，F12，选择 Application，点击 Cookies 获取键值对：`s9it_2132_auth=xxx;s9it_2132_saltkey=xxx` |

### 库街区

|      Name       |   Value    |                             说明                             |
| :-------------: | :--------: | :----------------------------------------------------------: |
| `KUROAPP_TOKEN` | `xxxxxxxx` | 打开 APP 登录，抓包 Host：`https://api.kurobbs.com` <br>随便哪个请求，找到请求头 **token**<br>多个账号用 `&` 隔开 |

### 消息推送变量（可选）

如果你想要程序执行后进行消息推送，那么任选一种或多种方式进行配置

如果你使用 Telegram 进行消息推送，那么在 Bot 创建后需要先给 Bot 发送一条消息，Bot 才能给你发消息 [issues#9](https://github.com/sudojia/scripts/issues/9)

|       Name        |                             归属                             |  属性  |                             说明                             |
| :---------------: | :----------------------------------------------------------: | :----: | :----------------------------------------------------------: |
|    `PUSH_KEY`     |                      微信 server 酱推送                      | 非必须 | server 酱的微信通知[官方文档](http://sc.ftqq.com/3.version)，已兼容 [Server 酱·Turbo 版](https://sct.ftqq.com/) |
|    `BARK_PUSH`    | [BARK 推送](https://apps.apple.com/us/app/bark-customed-notifications/id1403753865) | 非必须 | IOS 用户下载 BARK 这个 APP，填写内容是 app 提供的`设备码` 例如：https://api.day.app/123 ，那么此处的设备码就是 `123` |
|   `BARK_SOUND`    | [BARK 推送](https://apps.apple.com/us/app/bark-customed-notifications/id1403753865) | 非必须 | bark 推送声音设置，例如 `choo`，具体值请在 `bark`-`推送铃声`-`查看所有铃声` |
|  `TG_BOT_TOKEN`   |                        Telegram 推送                         | 非必须 | `TG_BOT_TOKEN` 和 `TG_USER_ID` 两者必需 填写自己申请 [@BotFather](https://t.me/BotFather)的 Token 如 `10xxx4:AAFcqxxxxgER5uw` |
|   `TG_USER_ID`    |                        Telegram 推送                         | 非必须 | `TG_BOT_TOKEN` 和 `TG_USER_ID` 两者必需 私聊它 [@userinfobot](https://t.me/userinfobot) 随便发点什么即可获取到自己的 ID |
|  `DD_BOT_TOKEN`   |                           钉钉推送                           | 非必须 | (`DD_BOT_TOKEN` 和 `DD_BOT_SECRET` 两者必需)[官方文档](https://developers.dingtalk.com/document/app/custom-robot-access)  只需 `https://oapi.dingtalk.com/robot/send?access_token=XXX` 等于 `=` 符号后面的 XXX 即可 |
|  `DD_BOT_SECRET`  |                           钉钉推送                           | 非必须 | (`DD_BOT_TOKEN` 和 `DD_BOT_SECRET` 两者必需) ，密钥，机器人安全设置页面，加签一栏下面显示的 SEC 开头的 `SECXXXXXXXXXX` 等字符，注：钉钉机器人安全设置只需勾选`加签`即可，其他选项不要勾选 |
|    `QYWX_KEY`     |                      企业微信机器人推送                      | 非必须 | 密钥，企业微信推送 webhook 后面的 key [详见官方说明文档](https://work.weixin.qq.com/api/doc/90000/90136/91770) |
|  `IGOT_PUSH_KEY`  |                          iGot 推送                           | 非必须 | iGot 聚合推送，支持多方式推送，确保消息可达。 [参考文档](https://wahao.github.io/Bark-MP-helper) |
| `PUSH_PLUS_TOKEN` |                        pushplus 推送                         | 非必须 | 微信扫码登录后一对一推送或一对多推送下面的 token(您的 Token) [官方网站](http://www.pushplus.plus/) |
| `PUSH_PLUS_USER`  |                        pushplus 推送                         | 非必须 | 一对多推送的 “群组编码”（一对多推送下面 -> 您的群组(如无则新建)->群组编码） 注：(1、需订阅者扫描二维码  2、如果您是创建群组所属人，也需点击“查看二维码”扫描绑定，否则不能接受群组消息推送) 只填 `PUSH_PLUS_TOKEN` 默认为一对一推送 |