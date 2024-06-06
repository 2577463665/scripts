<p align="center">
<h1 align="center">scripts</h1>
</p>
<p align="center">
    一些脚本，每天定时自动签到
    <br/>
    <br/>
    <a href="https://github.com/sudojia/scripts/issues/new" target="_blank">🐛上报 Bug、🤔问题反馈、📄需求提报！</a>
</p>
<p align="center">
    <img alt="Gitea Stars" src="https://img.shields.io/github/stars/sudojia/scripts?style=flat-square&logo=GitHub">
    <img alt="GitHub forks" src="https://img.shields.io/github/forks/sudojia/scripts?style=flat-square&logo=GitHub">
    <img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/t/sudojia/scripts?style=flat-square&logo=GitHub">
    <img alt="GitHub Issues or Pull Requests" src="https://img.shields.io/github/issues-closed-raw/sudojia/scripts?style=flat-square&logo=GitHub">
    <img alt="GitHub code size in bytes" src="https://img.shields.io/github/languages/code-size/sudojia/scripts?style=flat-square&logo=GitHub">
    <img alt="GitHub License" src="https://img.shields.io/github/license/sudojia/scripts?style=flat-square">
</p>



- [💍介绍](#介绍)
- [🔛使用](#使用)
- [👍服务器推荐](#服务器推荐)
- [⭐点个 Star 支持作者](#点个-star-支持作者)
- [⚖️许可证](#%EF%B8%8F许可证)
- [⚠️免责声明](#%EF%B8%8F免责声明)
- [🕛更新日志 ](#更新日志)

## 💍介绍

这是一个基于本人无聊时开发的自动化脚本，旨在每天定时自动执行一些签到奖励以及繁琐任务！

- [💡查看环境变量配置指南](./docs/ENV_DESC.md "环境变量配置指南")
- [📑查看脚本列表](./docs/SCRIPT_LIST.md "快速访问所有脚本详情")

## 🔛使用

**青龙面板（推荐）**

1. 在订阅管理创建订阅并在名称处粘贴拉库命令即可

   ```shell
   ql repo https://github.com/sudojia/scripts.git "sudojia_" "" "utils" "script"
   ```

   Cron 建议 `15 8,13,20 */2 * *` 每隔两天检测订阅，名称随意

2. 在环境变量创建对应的变量后即可，脚本会定时运行，你也可以到定时任务里手动运行一次

3. 在依赖管理处创建依赖，并复制添加如下依赖，自动拆分选择 **"是"**

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

**GitHub Actions（不推荐）**

- 在 fork 的仓库中，你可以通过点击 `Settings`（设置）-> `Secrets`（密钥）-> `New repository secret`（新建仓库密钥）来添加所需的环境变量。
- **建议**：如果你有某些 Actions 文件不运行，设置 `Disable workflow`（禁用工作流）以避免触发 GitHub 的某些机制，可能会因为违反使用条款而**导致账号被封**。
- 使用 GitHub Actions 时，请确保遵守 [【GitHub Actions 使用条款】](https://docs.github.com/github/site-policy/github-terms-for-additional-products-and-features#actions)。这些条款详细说明了使用 GitHub Actions 时的限制和规定，确保你的使用行为符合 GitHub 的政策。

![禁用工作流](https://img.gugu.ovh/i/2024/06/04/173912.webp)

## 👍服务器推荐

1. [【阿里云】2核2G3M，99/年，续费同价](https://www.aliyun.com/daily-act/ecs/activity_selection?userCode=ga5zx65v)
2. [【腾讯云】2核2G4M云服务器新老同享99元/年，续费同价](https://curl.qcloud.com/3wQPyTQE)
3. [【UCloud】开年上云，国外服务器2C4G30M新用户一年只需140，国内2C2G4M一年只需59](https://www.ucloud.cn/site/active/kuaijiesale.html?invitation_code=C1xF794E400C078)
4. [【华为云】普惠上云专区限时秒杀：2核2G2M，最低38/年](https://activity.huaweicloud.com/discount_area_v5/index.html)

## ⭐点个 Star 支持作者

维护近三年了还没破百😭

<p align='center'>
  <img src="https://api.star-history.com/svg?repos=sudojia/scripts&type=Date">
</p>


## ⚖️许可证

本脚本库使用 [GPLv3](https://github.com/sudojia/scripts/blob/script/LICENSE) 许可证，脚本库中任何脚本未经允许**不可商用**。宣传或转载时请带上[本脚本库链接](https://github.com/sudojia/scripts)。

## ⚠️免责声明

本脚本库（以下简称”本库“）由 [GitHub@sudojia](https://github.com/sudojia/)（以下简称“本人”）开发，旨在为用户提供一个方便的工具来自动化网站签到和任务执行。在使用本库之前，请仔细阅读以下条款：

1. 本库仅供学习和研究使用。使用本库进行任何非法活动，包括但不限于未经授权的访问、数据窃取、破坏网站服务等，均违反法律，可能导致刑事责任。本人不承担因用户非法使用本库而产生的任何法律后果。
2. 用户应自行承担使用本库所带来的风险。在使用本库时，用户应遵守相关网站的使用条款和隐私政策。本人不对因使用本库而造成的任何损失或损害承担责任。
3. 本人尊重用户隐私。本库不会收集、存储或传输用户的个人信息。用户在使用本库时，应确保不违反任何隐私法规。
4. 本库按“现状”提供，不提供任何形式的保证。本人不对本库的适用性、可靠性、准确性或完整性提供任何保证。用户使用本库是自愿的，应自行承担由此产生的风险。
5. 本人保留随时修改或终止本库的权利，无需事先通知用户。
6. 如果任何单位或个人认为本库中的脚本可能侵犯其合法权益，请及时与我联系并提供相关证明，我将在收到认证文件后删除相关脚本。
7. 本声明的最终解释权归本人所有。

> 您使用或复制了本库中由本人开发的任何脚本，即视为已接受此声明。请在使用前仔细阅读以上条款。

## 🕛更新日志

<details>
<summary>点击展开</summary>


- 2024-05-31

  - 新增海贼王论坛每日签到
  - 新增智能电视每日签到

- 2024-05-29 适配青龙面板
- 2024-05-28
  - 重构并新建 script 分支，删除原 master 分支
  - 移除 Steam 游玩时长获取脚本
- 2024-05-22 新增 V2EX 每日签到
- 2024-05-21 稀土掘金新增[成长等级](https://juejin.cn/user/center/growth)自动任务
- 2024-05-20 新增司机社每日签到
- 2024-05-18
  - 新增阿里云盘每日签到
  - 新增百度贴吧每日签到
- 2024-05-17 优化使用 axios
- 2023-11-21 新增 Steam 游玩时长获取
- 2022-09-27 移除葫芦侠
- 2022-01-20
  - 新增稀土掘金每日签到和抽奖任务
  - 新增葫芦侠三楼板块每日签到
- 2021-09-27 SSPANEL 面板更改变量写法

  - 采用一个变量，单个规则为：网站,账号:密码 多个：网站,账号:密码&网站,账号:密码

- 2021-09-26
  - SSPANEL 面板支持多账号及多网站签到
  - 添加多个消息推送（Telegram、server 酱、Bark、PushPlus、钉钉等）
- 2021-09-25 新增 SSPANEL 面板每日签到

</details>
