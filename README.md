<p align="center">
<h1 align="center">scripts</h1>
</p>
<p align="center">
    一些脚本，每天定时自动签到
    <br/>
    <br/>
    <a href="https://github.com/sudojia/scripts/issues/new" target="_blank">🐞上报 Bug、🤔问题反馈、📄需求提报！</a>
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

   Cron 建议 `15 8,13,20 */3 * *` 每隔三天检测订阅，名称随意

2. 在环境变量创建对应的变量后即可，脚本会定时运行，你也可以到定时任务里手动运行一次

3. 在依赖管理处创建依赖，并复制添加如下依赖，自动拆分选择 "是"

   ```shell
   axios
   cheerio
   download
   http-server
   moment
   tunnel
   ws
   ```

**GitHub Actions（不建议）**

为了防止违反这些限制和滥用 GitHub Actions，GitHub 可能会监控您对 GitHub Actions 的使用。滥用 GitHub Actions 可能会导致工作终止、限制您使用 GitHub Actions 的能力、禁用为以违反这些条款的方式运行 Actions 而创建的存储库，或者在某些情况下暂停或终止您的 GitHub 帐户

附上：[【关于 GitHub Actions 使用条款】](https://docs.github.com/github/site-policy/github-terms-for-additional-products-and-features#actions)

如若真没服务器，又想白嫖

那么填入 Secrets 变量，然后直接运行 Actions Workflows 文件即可

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
