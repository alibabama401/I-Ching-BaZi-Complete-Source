<div align="center">

# 周易八字排盘源码

### I Ching BaZi Chart Source Code

四柱八字 · 十神藏干 · 纳音五行 · 真太阳时 · 大运流年 · Java 服务接口

[简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [English](README.en.md) · [在线产品页](https://alibabama401.github.io/I-Ching-BaZi-Complete-Source/)

</div>

## 项目简介

这是一个面向周易、八字排盘和传统历法软件研究的源码展示项目。仓库根目录提供可直接在浏览器阅读的 HTML/JavaScript 八字演示：输入姓名、性别、出生日期时间后，页面展示四柱干支、十神、藏干、纳音、平太阳时/真太阳时提示和大运表格。

仓库同时公开用户、订单、排盘记录、任务结果和五行配置等 Java 服务接口，并提供八张真实产品截图，展示八字、流年、大六壬、七政四余和五行分析等产品界面。

> **公开范围说明：** 当前 Java 文件是服务接口片段，不是完整可构建后端。根页面中的节气、纳音和大运算法包含简化或占位实现。截图展示产品场景，不代表所有截图对应算法均已在本仓库完整公开。

## 产品功能

| 功能 | 当前公开内容 |
|---|---|
| 四柱八字排盘 | 年柱、月柱、日柱、时柱的浏览器端展示 |
| 十神与藏干 | 日主关联十神与十二地支藏干页面逻辑 |
| 纳音五行 | 四柱纳音展示和五行产品截图 |
| 时间输入 | 出生日期时间、时区、经纬度及太阳时提示 |
| 大运流年 | 年龄区间、大运干支和年份表格示例 |
| 排盘记录 | `PanRecordService` 的新增、查询、删除接口 |
| 多术数任务 | `MoiraRecordService` / `MoiraTaskService` 方法签名 |
| 用户与配置 | 用户、订单、短信、五行配置的服务接口 |
| 多语言产品页 | 简体中文、繁體中文、English GitHub Pages 页面 |

## 玩法与使用流程

```mermaid
flowchart LR
  A[输入姓名、性别与出生时间] --> B[时区与太阳时处理]
  B --> C[生成四柱干支]
  C --> D[展示十神、藏干与纳音]
  D --> E[浏览大运和流年表格]
```

1. 在浏览器打开根目录的 `index.html`。
2. 填写姓名，选择性别和出生日期时间。
3. 点击“开始排盘”。
4. 阅读年、月、日、时四柱及十神、藏干、纳音。
5. 向下查看大运年龄区间和年份表格。

## 技术组成

| 层级 | 技术与文件 |
|---|---|
| 前端演示 | HTML5、CSS3、原生 JavaScript，集中在 `index.html` |
| 服务边界 | Java interface，覆盖用户、订单、排盘、任务和配置 |
| 页面发布 | GitHub Actions + GitHub Pages，发布目录为 `docs/` |
| 搜索优化 | canonical、hreflang、Open Graph、JSON-LD、robots、sitemap |
| 图片资源 | `docs/assets/Screenshots/` 中的真实产品截图 |

## 产品截图

| 四柱八字排盘 | 大六壬排盘 |
|---|---|
| ![四柱八字排盘源码产品截图](docs/assets/Screenshots/001baizhipaipan.png) | ![大六壬排盘产品截图](docs/assets/Screenshots/002daliuren.png) |
| **大运流年分析** | **综合排盘系统** |
| ![八字大运流年分析截图](docs/assets/Screenshots/003liunian.png) | ![周易综合排盘系统截图](docs/assets/Screenshots/004paipan.png) |
| **七政四余** | **七政四余详细盘** |
| ![七政四余产品页面截图](docs/assets/Screenshots/005qizheng2.png) | ![七政四余详细排盘截图](docs/assets/Screenshots/006qizhengsiyu.png) |
| **无极八字** | **五行分析** |
| ![无极八字排盘产品截图](docs/assets/Screenshots/007wujibazi.png) | ![八字五行分析产品截图](docs/assets/Screenshots/008wuxing.png) |

## 源码导航

| 文件 | 用途 |
|---|---|
| [`index.html`](index.html) | 可交互的八字排盘前端演示 |
| [`UserService.java`](UserService.java) | 注册、登录、资料和坐标相关接口 |
| [`PanRecordService.java`](PanRecordService.java) | 排盘记录接口 |
| [`MoiraRecordService.java`](MoiraRecordService.java) | 多术数数据及导出接口 |
| [`MoiraTaskService.java`](MoiraTaskService.java) | 排盘任务执行与状态接口 |
| [`WuXingConfigService.java`](WuXingConfigService.java) | 五行配置接口 |
| [`docs/index.html`](docs/index.html) | 三语 GitHub Pages 入口 |

## 快速查看

```bash
git clone https://github.com/alibabama401/I-Ching-BaZi-Complete-Source.git
cd I-Ching-BaZi-Complete-Source
```

随后用浏览器打开 `index.html`。它是静态演示页，不需要安装依赖。Java 接口如需编译，必须补齐领域模型、实现类、第三方依赖和构建配置。

## 适用场景

- 八字排盘与四柱产品界面原型
- 周易、易经和中国传统历法软件研究
- 十神、藏干、纳音、五行页面结构参考
- Java 服务接口和排盘任务边界评估
- GitHub Pages 多语言产品展示

## 常见问题

### 这是完整可部署系统吗？

公开仓库不是完整可部署商业系统。可直接运行的是根目录静态演示；Java 文件只公开接口层片段。

### 截图里的大六壬、七政四余都包含完整算法吗？

不能仅凭截图得出该结论。截图用于证明产品界面和应用范围，算法交付情况需要按实际源码清单核验。

### 排盘结果可以用于专业决策吗？

演示代码包含简化规则，正式使用前应明确历法、节气、真太阳时、子初换日和流派规则，并用权威样例测试。

## 相关关键词

周易源码、易经源码、八字源码、八字排盘、四柱八字、十神、藏干、五行分析、大运流年、I Ching source code、BaZi chart、Four Pillars of Destiny、Chinese astrology software。

## 许可与联系

使用前请阅读 [LICENSE](LICENSE) 与 [License.md](License.md)。

- Email: [ttpoker40@gmail.com](mailto:ttpoker40@gmail.com)
- Telegram: [@alibabama401](https://t.me/alibabama401)

本项目用于传统文化软件展示、技术研究与产品评估，不构成确定性预测，也不构成医疗、法律、金融或人生决策建议。
