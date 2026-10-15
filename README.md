<div align="center">

# Kansamu216

**Minecraft 服务端模组 / 工具链开发**

用服务端 mod 做原版做不到的事 —— 玩家用**原版客户端**进服，什么都不用装。

![Kotlin](https://img.shields.io/badge/Kotlin-2.1-7F52FF?logo=kotlin&logoColor=white)
![Java](https://img.shields.io/badge/Java-17%20%7C%2021-ED8B00?logo=openjdk&logoColor=white)
![NeoForge](https://img.shields.io/badge/NeoForge-21.1.x-F16436)
![Forge](https://img.shields.io/badge/Forge-47.4%20%7C%2052.1-1F2A3A)
![Fabric](https://img.shields.io/badge/Fabric-1.21.1-DBD0B4)
![Minecraft](https://img.shields.io/badge/Minecraft-1.20.1%20%7C%201.21.1-62A86B?logo=minecraft&logoColor=white)

[谷雨工坊 · KokuuWork](https://github.com/KokuuWork) · [kokuu.org](https://kokuu.org) · [Voidkit 文档](https://kokuuwork.github.io/voidkit/) · [QQ 群 498700382](https://qm.qq.com/q/ueYTU8T3xK)

</div>

---

在 [谷雨工坊](https://github.com/KokuuWork) 开发和维护 Minecraft 服务端工具链，全部面向**几百个 mod 的大型整合包**：从零写起，写完就开源，让别的服务器直接拿去用。

不做概念验证，也不做 demo。所有项目都在真实运营的服务器里跑过，每一行代码的底线是 —— **装上就能用，用着不出问题**。

## 主要项目

| 项目 | 说明 | 技术 |
| --- | --- | --- |
| **[Voidkit](https://github.com/KokuuWork/voidkit)** | 纯服务端模组套件。用服务端 mod 实现 Bukkit / Essentials / CMI 那一类通用服务器功能，外加管理平台。内核 + 多个独立组件，每个都是可单独安装、单独卸载、单独发布的 jar | `Kotlin` · NeoForge / Forge / Fabric · 1.20.x–1.21.x |
| **[Voidkit Inspector](https://github.com/KokuuWork/voidkit-inspector)** | 操作审计。CoreProtect 风格的方块 / 容器 / 实体记录，**来源分类**把自动化产线噪声与真实破坏行为分开；多线程入队 + 独立写线程 + 嵌入式 SQLite，不卡 TPS | `Kotlin` · 零 mixin |
| **[Voidkit Guard](https://github.com/KokuuWork/voidkit-guard-oss)** | 反作弊。客户端 Agent + 服务端校验拆成两个 jar，客户端 jar 物理上不含任何服务端代码 | `Kotlin` · 1.20.1 / 1.21.1 |
| **[RS Wireless Crafting](https://github.com/KokuuWork/rswirelesscrafting)** | 给 [Refined Storage 2](https://github.com/refinedmods/refinedstorage) 补上原版缺失的**无线合成**能力：无线合成终端、无线样板终端、六张装配式升级插件与终端充电站 | `Java` · NeoForge / Fabric · 1.21.1 |
| **[Tint Guard](https://github.com/KokuuWork/tintguard)** | 客户端补丁。把每个 `BlockColor` 包成异常安全，写坏的方块染色处理器（如 Waystones）再也不能通过 Voxy / Roxy 把游戏打崩 | `Java` · NeoForge · 1.21.1 |
| **[DeathBack](https://github.com/KokuuWork/deathback)** | Arclight 混合端补丁。把死亡坐标补写进 CMI，让 `/back` 在死亡场景下恢复可用（附字节码层面的成因分析） | `Java` · Forge + Bukkit |
| **Arcanum Reborn**（开发中 · 暂未公开） | Thaumcraft 4 的非官方独立复刻 —— 魔法、研究、探索系统在 Minecraft 1.20.1 (Forge) 上重建 | `Java` |
| **[Paperland 绘岛](https://github.com/Kansamu216/paperland-download)** | 客户端下载分发 | `Release` |

## 工程原则

- **低耦合是铁律** —— 每个组件只依赖 `voidkit_core`，core + 任意一个组件都能单独跑起来；缺了的组件有保守兜底，装了的不拖累别人
- **零 mixin** —— 全部走事件监听，不跟整合包里已有的 mixin mod 抢类改写
- **构造期零 IO** —— 配置读取推迟到服务端启动之后，不拖累几百个 mod 的并行加载
- **配置有界、干预保守** —— 配置写错的代价只是少干活，不碰方块、不碰机器、不碰存档
- **存储用嵌入式** —— SQLite 单文件而非 MySQL / Redis，不要求服主额外运维任何东西
- **零配置默认可用** —— 默认值要聪明，装上去就能用；能不让人配的就不让人配

## 联系

- Bug 反馈 / 功能建议 → 对应仓库的 [Issues](https://github.com/KokuuWork)，或 **QQ 群 [498700382](https://qm.qq.com/q/ueYTU8T3xK)**
- 团队主页 → [kokuu.org](https://kokuu.org) · [@KokuuWork](https://github.com/KokuuWork)
