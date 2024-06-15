# 青龙面板方式（推荐）

1. 在订阅管理创建订阅并在名称处粘贴拉库命令即可

   ```shell
   ql repo https://github.com/sudojia/scripts.git "sudojia_" "" "utils" "script"
   ```

   `cron` 定时和名称随意

2. 在依赖管理处创建依赖，并复制如下依赖，自动拆分选择 **"是"**

   ```shell
   axios
   cheerio
   download
   http-server
   moment
   tough-cookie
   tunnel
   ws
   got
   ```

3. 在环境变量创建对应的变量即可，脚本会自动定时运行，你也可以到定时任务里手动运行一次！

# GitHub Actions 方式（不推荐）

- 在 fork 的仓库中，通过点击 `Settings`（设置）-> `Secrets`（密钥）-> `New repository secret`（新建仓库密钥）来添加所需的环境变量。

- **建议**：如果你有某些 Actions 文件不运行，设置 `Disable workflow`（禁用工作流）以避免触发 GitHub 的某些机制，可能会因为违反使用条款而**导致账号被封**。

- 使用 GitHub Actions 时，请确保遵守 [【GitHub Actions 使用条款】](https://docs.github.com/github/site-policy/github-terms-for-additional-products-and-features#actions)。这些条款详细说明了使用 GitHub Actions 时的限制和规定，确保你的使用行为符合 GitHub 的政策。

  ![禁用工作流](https://img.gugu.ovh/i/2024/06/04/173912.webp)

# 变量及脚本说明

> 你需要运行哪个脚本，就设置对应的脚本变量名即可

## [稀土掘金](https://juejin.cn/)

脚本名：`sudojia_juejin.js`

1. 每日签到获得矿石、矿石可用于兑换实物
2. 白嫖次数幸运抽奖，满 6000 幸运值必出实物
3. 升级任务：成长等级的社区活跃任务！

<img src="https://img.gugu.ovh/i/2024/06/15/195147.webp" alt="juejin" style="zoom: 50%;" />

### 变量说明

|       Env       |         Value         |                             说明                             |
| :-------------: | :-------------------: | :----------------------------------------------------------: |
| `JUEJIN_COOKIE` | `xxxxxxxxxxxxxxxxxxx` | 稀土掘金 Cookie，打开[掘金社区](https://juejin.cn/) F12，选择 Application，点击 Cookies 只要 `sessionid` 的值并填入 Secrets 即可，多个账号用 `&` 隔开 `xxxxxxxx&xxxxxxxx` |

<img src="https://img.gugu.ovh/i/2024/06/10/173932.webp" alt="juejin" style="zoom:67%;" />

## SSPANEL面板

脚本名：`sudojia_sspanel.js`

每日签到获得流量

### 变量说明

|       Env       |               Value               |                             说明                             |
| :-------------: | :-------------------------------: | :----------------------------------------------------------: |
| `SITE_ACCOUNTS` | `网站,账号:密码`，多个用 `&` 隔开 | 单账号填写规则：`https://paolu.com,aaa@gmail.com:123456`<br/>多个填写规则：`https://aaa.com,aaa@gmail.com:aaa&https://bbb.com,bbb@gmail.com:bbb&...以此类推`<br/>中文说明：`网站,账号:密码`，多个：`网站,账号:密码&网站2,账号2:密码2` |

**注意事项：**

1. SSPANEL 签到暂不支持密码带  `,`  与  `:`  的字符！
2. **<font color='red'>SSPANEL 签到暂不支持带有图形验证码的网站！</font>**

## [阿里云盘](https://www.aliyundrive.com/)

脚本名：`sudojia_aliyundrive.js`

获取奖励接口加签本人实力无法获取，仅支持每日签到

### 变量说明

|         Env         |              Value              |                  说明                   |
| :-----------------: | :-----------------------------: | :-------------------------------------: |
| `ALI_REFRESH_TOKEN` | `e7b02b2k52074om8td187c62952cf` | 阿里云盘 referesh token 多个用 `&` 分开 |

如何获取 **referesh token?**

**第一种**：打开[阿里云盘](https://www.aliyundrive.com/)，登录后 `F12` 在控制台输入以下代码即可获取

```javascript
JSON.parse(localStorage.token).refresh_token
```

**第二种**： 使用 Alist 的在线获取

打开 [Alist 文档#刷新令牌](https://alist.nn.ci/zh/guide/drivers/aliyundrive.html#%E5%88%B7%E6%96%B0%E4%BB%A4%E7%89%8C)，点击获取 Token，然后使用阿里云盘 APP 扫描，扫描完成后再点击一次即可获取

两种方式任选一种获取 `Referesh Token `

## [百度贴吧](https://tieba.baidu.com/)

脚本名：`sudojia_tieba.js`

每日签到所有贴吧

### 变量说明

|       Env       |                Value                |                             说明                             |
| :-------------: | :---------------------------------: | :----------------------------------------------------------: |
| `TIE_BA_COOKIE` | eg: `xxxxxxxxxxxxxxxxxxxxxxxxxxxxx` | 打开[百度贴吧](https://tieba.baidu.com/) -> F12，选择 Application，点击 Cookies<br/>只要 `BDUSS` 的值即可<br>多个账号用 `&` 分开 |

<img src="https://img.gugu.ovh/i/2024/06/10/174000.webp" alt="tieba" style="zoom: 67%;" />

## 司机社

脚本名：`sudojia_sijishe.js`

每日签到获得车票，车票可用于购买、发布悬赏车牌号等

### 变量说明

|     Env      |          Value          |                             说明                             |
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

## [V2EX](https://www.v2ex.com/)

脚本名：`sudojia_v2ex.js`

每日签到

### 变量说明

|      Env      | Value  |                             说明                             |
| :-----------: | :----: | :----------------------------------------------------------: |
| `V2EX_COOKIE` | Cookie | F12，选择 Network 网络，然后请求选择 `Doc`，把 Cookie 全选复制<br>没有出现 `v2ex.com` 那就 F5 刷新一下 |

<img src="https://img.gugu.ovh/i/2024/06/10/174112.webp" alt="v2ex" style="zoom: 67%;" />

## [海贼王论坛](https://bbs.talkop.com/)

脚本名：`sudojia_talkop.js`

每日签到获得贝里

### 变量说明

|       Env       |                   Value                    |                             说明                             |
| :-------------: | :----------------------------------------: | :----------------------------------------------------------: |
| `TALKOP_COOKIE` | `3yWf_2132_auth=xxx;3yWf_2132_saltkey=xxx` | 打开司机社网站，F12，选择 Application，点击 Cookies 获取键值对：`3yWf_2132_auth=xxx;3yWf_2132_saltkey=xxx` |

## [智能电视](https://www.znds.com/)

脚本名：`sudojia_znds.js`

每日签到获得金币

### 变量说明

|      Env      |                   Value                    |                             说明                             |
| :-----------: | :----------------------------------------: | :----------------------------------------------------------: |
| `ZNDS_COOKIE` | `s9it_2132_auth=xxx;s9it_2132_saltkey=xxx` | 打开司机社网站，F12，选择 Application，点击 Cookies 获取键值对：`s9it_2132_auth=xxx;s9it_2132_saltkey=xxx` |

## [库街区](https://www.kurobbs.com/)

脚本名：` sudojia_kuro.js `

1. 库街区APP，每日签到获得库洛币
2.  鸣潮每日签到获得签到奖励
3. 战双每日签到获得签到奖励

> 脚本默认用浏览器的方式检测 Token，若失效，再用 APP 的方式检测，所以，任选一种方式获取 Token 即可

### 变量说明

|     Env      |   Value    |                             说明                             |
| :----------: | :--------: | :----------------------------------------------------------: |
| `KURO_TOKEN` | `xxxxxxxx` | 打开 APP 登录，抓包 Host：`https://api.kurobbs.com` <br>随便哪个请求，找到请求头 **token**<br>多个账号用 `&` 隔开 |

**PC 端 Token 获取：**

- 浏览器打开[库街区](https://www.kurobbs.com/mc/home/9)，登录之后，`F12 -> Application -> 左侧 Local storage -> 找到 auth_token 复制其 Value`

<img src="https://img.gugu.ovh/i/2024/06/10/173834.webp" alt="kuro_get_token" style="zoom: 50%;" />

## [皮皮世界](https://pipix.com/)

> 入口：皮皮虾 APP -> 我的 -> 进入宠物乐园

脚本名：`sudojia_ppworld.js`

通过喂食宠物升级，升级可解锁对应的等级奖励

一天喂食最大三次，每次喂食掉落经验值和喂食奖品

领狗粮接口官方未做限制，可无限领取，脚本已限制领取三次，足矣

<img src="https://img.gugu.ovh/i/2024/06/15/201849.webp" alt="pp_world" style="zoom: 25%;" />

### 变量说明

|     Env      |   Value    |                             说明                             |
| :----------: | :--------: | :----------------------------------------------------------: |
| `PPX_COOKIE` | `xxxxxxxx` | 打开 APP 登录，抓包 Host：`https://api.pipix.com` <br>随便哪个请求，找到 Cookie，只要 `sessionid=`后面的值<br>多个账号用 `&` 隔开 |

**PC 端获取方式：**

打开[【皮皮虾】](https://pipix.com/)官网，右上角登录之后，F12 -> 选择 Application，点击 Cookies

<img src="https://img.gugu.ovh/i/2024/06/15/202827.webp" alt="pp_world" style="zoom: 50%;" />

## 消息推送变量（可选）

如果你想要程序运行后进行消息推送，那么任选一种或多种方式进行配置

配置的方式与脚本配置的变量方式是一样的

如果你使用 Telegram 进行消息推送，那么在 Bot 创建后需要先给 Bot 发送一条消息，Bot 才能给你发消息 [issues#9](https://github.com/sudojia/scripts/issues/9)

|        Env        |                             归属                             |  属性  |                             说明                             |
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