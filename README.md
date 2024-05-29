<p align="center">
    <h1 align="center">scripts</h1>
</p>
<p align="center">
    一些脚本，每天定时自动签到
    <br />
    <br />
    <a href="https://github.com/sudojia/scripts/issues/new">上报 Bug、意见反馈</a>
  </p>




- [💍介绍](#介绍)
- [🔛使用](#使用)
- [👍服务器推荐](#服务器推荐)
- [⭐点个 Star 支持作者](#点个-star-支持作者)
- [⚖️许可证](#%EF%B8%8F许可证)
- [🕛历程](#历程)

## 💍介绍

这是一个基于本人无聊时开发的自动化脚本，旨在每天定时自动执行一些签到奖励以及繁琐任务

环境变量参考：[环境变量说明](./docs/ENV_DESC.md)

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

附上：[关于 GitHub Actions 使用条款](https://docs.github.com/github/site-policy/github-terms-for-additional-products-and-features#actions)

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

## 🕛历程

|    时间    |                             事件                             |
| :--------: | :----------------------------------------------------------: |
| 2024-05-29 |                         适配青龙面板                         |
| 2024-05-28 | 1. 重构并新建 script 分支，删除原 master 分支<br>2. 移除 Steam 游玩时长获取脚本 |
| 2024-05-22 |                      新增 V2EX 签到脚本                      |
| 2024-05-21 | 掘金社区大更新<br>1. 添加了成长等级自动任务、目前只写了社区活跃下的任务<br>2. 移动端每日登录访问和发布文章任务有时间再写 |
| 2024-05-20 |                      新增司机社签到脚本                      |
| 2024-05-18 |                新增阿里云盘、百度贴吧签到脚本                |
| 2024-05-17 |               脚本库优化并使用 axios 发送请求                |
| 2023-11-21 |                   新增 Steam 游玩时长获取                    |
| 2022-09-27 |               移除葫芦侠（葫芦侠加了签名参数）               |
| 2022-01-20 | 1. 新增掘金社区签到&抽奖脚本<br>2. 应网友要求新增葫芦侠签到（一开始还以为看剧的葫芦...） |
