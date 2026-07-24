# XyCore 0.3.3

XyCore 是一款面向 `Paper 1.12.2 build 1620` 的 RPG/MMO 服务器底层核心插件。

它的定位不是把所有玩法都塞进 Core，而是给后续的 `XyJob`、`XyForge`、符文、职业、锻造、活动等插件提供统一、稳定、可复用的底层服务。

当前设计为只安装在 RPG 主服；Velocity 登录服只做中转，不需要安装 XyCore。

## Core 负责什么

- 玩家数据会话与模块数据容器，供 XyJob、XyForge 和后续 Xy 系列插件使用。
- YML、SQLite、MySQL/MariaDB 三种数据存储。
- JDBC 存储使用 HikariCP 数据库连接池。
- Vault 经济接口桥接。
- PlaceholderAPI 正式新版变量扩展与动态变量命名空间。
- AttributePlus 属性读取桥接与属性源直接写入/移除桥接。
- DragonCore GUI、按键、变量、客户端数据包桥接。
- 原版物品与 MythicMobs 物品库软桥接。
- 可开关的内置模块系统。

职业等级、职业经验、锻造配方、技能、专精徽章、符文雕刻等具体玩法，建议交给独立插件实现。XyCore 只提供底座、接口和公共能力。

## 快速使用

1. 将 `XyCore-0.3.3.jar` 放入 `plugins` 文件夹。
2. 启动服务器生成 `plugins/XyCore/config.yml`。
3. 在 `config.yml` 中开启需要的模块。
4. 使用 `/xycore reload` 或重启服务器。
5. 开启后的模块配置会生成在 `plugins/XyCore/modules/`。

第一次加载时，默认只生成主配置 `config.yml`。模块配置不会提前生成，只有模块开关打开后才会创建。
<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
