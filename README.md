<div align="center">

# Kansamu216

Minecraft 服务端 mod 开发 · Kotlin / Java

![Kotlin](https://img.shields.io/badge/Kotlin-2.1-7F52FF?logo=kotlin&logoColor=white)
![Java](https://img.shields.io/badge/Java-17%20%7C%2021-ED8B00?logo=openjdk&logoColor=white)
![NeoForge](https://img.shields.io/badge/NeoForge-21.1.x-F16436)
![Forge](https://img.shields.io/badge/Forge-47.4%20%7C%2052.1-1F2A3A)
![Fabric](https://img.shields.io/badge/Fabric-1.21.1-DBD0B4)
![Minecraft](https://img.shields.io/badge/Minecraft-1.20.1%20%7C%201.21.1-62A86B?logo=minecraft&logoColor=white)

</div>

---

**AI 开发工具人** —— 不会写代码，全靠 AI 生成。

## 项目

| 项目 | 说明 | 技术 |
| --- | --- | --- |
| **[Voidkit](https://github.com/KokuuWork/voidkit)** | 纯服务端模组套件，用服务端 mod 实现通用服务器功能：家、传送点、权限、称号、经济、物品清扫等。内核加若干独立组件，每个组件单独一个 jar，可分别安装 / 卸载 | `Kotlin` · NeoForge / Forge / Fabric · 1.20.x–1.21.x |
| **[Voidkit Inspector](https://github.com/KokuuWork/voidkit-inspector)** | 方块 / 容器 / 实体操作记录。按操作来源分类（机械臂、管道、假玩家、树叶腐烂），默认不记自动化产生的噪声；主线程 O(1) 入队，单写线程批量落库，SQLite 存储 | `Kotlin` |
| **[Voidkit Guard](https://github.com/KokuuWork/voidkit-guard-oss)** | 反作弊，客户端 Agent + 服务端校验，拆成两个 jar | `Kotlin` · 1.20.1 / 1.21.1 |
| **[RS Wireless Crafting](https://github.com/KokuuWork/rswirelesscrafting)** | Refined Storage 2 的无线合成扩展：无线合成终端、无线样板终端、6 张升级插件、终端充电站 | `Java` · NeoForge / Fabric · 1.21.1 |
| **[Tint Guard](https://github.com/KokuuWork/tintguard)** | 客户端补丁：给注册进 `BlockColors` 的方块染色处理器包一层异常保护，避免 Voxy / Roxy 烘焙模型时触发 `ClassCastException` 导致客户端退出 | `Java` · NeoForge · 1.21.1 |
| **[DeathBack](https://github.com/KokuuWork/deathback)** | Arclight 端补丁：把死亡坐标补写进 CMI，恢复死亡后的 `/back` | `Java` · Forge + Bukkit |
| **Arcanum Reborn** | Thaumcraft 4 的独立复刻，开发中 | `Java` · Forge · 1.20.1 |
| **[Paperland 绘岛](https://github.com/Kansamu216/paperland-download)** | 客户端安装包分发 | — |

## 技术栈

- **语言** Kotlin · Java 17 / 21 · Gradle
- **平台** Minecraft 1.20.1 / 1.21.1 · NeoForge · Forge · Fabric · Arclight（Forge + Bukkit）
- **方向** 服务端与客户端 mod、Bukkit 插件、事件监听、mixin、嵌入式 SQLite
