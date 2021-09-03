# 系统简介

### 欢迎加入我们的QQ群：**822767462**

木屋海鸥交易系统由**海鸥令主（QQ：960269073）**设计开发，**彩色の小木屋\(QQ：429690798\)**提供页面模板，本系统的基本结构由**dll的组件**和**exe的管理端**组成，以下是详细结构

## 系统文件结构 

```text
HioldMod_funcs (主目录)
│  hioldsstarter.dll (主载入程序)
│  LiteDB.dll (轻量数据模块)
│  main.bin (mod本体)
│  main.dlc (mod载入体,后续版本将把main.dlc改为不定名称)
│  ModInfo.xml (描述信息)
│  modversion.json (版本信息)
│  NaiwaziBot_Points.dll (共享naiwaibot积分)
│
├─api (管理程序主目录)
│  │  apiversion.json (版本信息)
│  │  hiold-api.exe (管理程序主体)
│  │  .env (管理程序配置文件)
│  │  .inited (初始化锁定)
│  │  .locked (配置文件锁定)
│  │  foo.db (数据库)
│  │  license (授权信息)
│  ├─hioldcustom (玩家端页面)
│  └─static (管理端页面)
│
└─config (dll组件配置)
    │  ActionItemConfig.xml (拍卖物品)
    │  ActionItemPriceConfig.xml (拍卖价格)
    │  ActionKillAwardConfig.xml (击杀奖励)
    │  ActionMainConfig.xml (主配置)
    │  ActionQuestAwardConfig.xml (任务奖励)
    │  ActionUserConfig.xml (玩家配置)
    │  CommonConfig.xml (杂项配置)
    │  Language.xml (自定义提示信息)
    ├─db (dll组件数据库)
    └─Logs (dll组件日志)
```

* 所有配置建议从管理端进行修改，非必要的情况下请不要直接手动编辑，配置文件异常可能导致系统不稳定
* 由于本程序和奶naiwazibot都具有击杀奖励功能，建议在本程序和naiwazibot之间二选一，使用naiwazibot进行击杀基本管理本系统将无法记录玩家击杀数据，无法回溯和统计，除此以外不影响系统正常运行

