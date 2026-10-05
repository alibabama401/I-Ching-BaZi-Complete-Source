# 八字排盘源码｜四柱、十神、藏干、五行与大运流年

[主 README](README.md) · [繁體中文](README.zh-TW.md) · [English](README.en.md) · [简体中文产品页](https://alibabama401.github.io/I-Ching-BaZi-Complete-Source/zh-cn/)

本仓库展示周易八字排盘产品与部分源码。根目录 `index.html` 是可直接打开的 HTML/JavaScript 演示，包含姓名、性别、出生日期时间输入，以及四柱干支、十神、藏干、纳音、太阳时提示和大运表格。Java 文件展示用户、订单、排盘记录、任务结果及五行配置的服务接口。

## 功能范围

| 功能 | 可核验内容 |
|---|---|
| 四柱八字 | 年柱、月柱、日柱、时柱页面展示 |
| 十神藏干 | 十神映射与地支藏干数据 |
| 纳音五行 | 纳音展示、五行配置接口和产品截图 |
| 时间处理 | 出生时间、时区、经纬度和太阳时提示 |
| 大运流年 | 大运年龄、干支和年份表格示例 |
| 数据服务 | 用户、排盘记录、任务、订单及五行配置接口 |

## 操作流程

打开 `index.html`，选择出生日期时间与性别，点击“开始排盘”，然后查看四柱、十神、藏干、纳音和大运表格。该页面适合产品原型和代码阅读；其中部分历法逻辑为简化或占位实现。

## 产品截图

| 八字排盘 | 流年分析 |
|---|---|
| ![八字排盘源码界面](docs/assets/Screenshots/001baizhipaipan.png) | ![八字流年分析界面](docs/assets/Screenshots/003liunian.png) |
| **七政四余** | **五行分析** |
| ![七政四余排盘界面](docs/assets/Screenshots/006qizhengsiyu.png) | ![五行分析产品界面](docs/assets/Screenshots/008wuxing.png) |

## 技术与源码

- `index.html`：HTML、CSS、原生 JavaScript 交互演示。
- `PanRecordService.java`：排盘记录服务接口。
- `MoiraRecordService.java`：多术数数据与导出方法签名。
- `MoiraTaskService.java`：任务执行、状态和排序接口。
- `UserService.java` / `UserOrderService.java`：用户及订单服务接口。
- `docs/`：简体、繁体、英文 GitHub Pages 页面与搜索引擎文件。

## 公开范围

当前 Java 文件并非完整工程，缺少实现类、领域模型、依赖和构建配置。截图展示产品功能场景，不等同于对应算法全部开源。评估与二次开发时请以实际文件和授权范围为准。

## 联系

[Email](mailto:ttpoker40@gmail.com) · [Telegram @alibabama401](https://t.me/alibabama401) · [GitHub 仓库](https://github.com/alibabama401/I-Ching-BaZi-Complete-Source)
