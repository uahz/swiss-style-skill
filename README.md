# swiss-style-skill

**中文** · [English](README.en.md)

> 瑞士国际主义风格（Swiss Style / International Typographic Style）AI 设计技能包。
> 把 1950 年代国际主义平面设计的视觉语法，固化成可复用的 Skill 与可套用的版式规范。

<p>
  <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-DA291C?style=flat-square&labelColor=000000">
  <img alt="Version" src="https://img.shields.io/badge/Version-0.2.0-000000?style=flat-square&labelColor=000000">
  <img alt="Grid" src="https://img.shields.io/badge/Grid-12%20Columns-000000?style=flat-square&labelColor=000000">
  <img alt="Palette" src="https://img.shields.io/badge/Palette-3%20Colors-000000?style=flat-square&labelColor=000000">
</p>

## 效果样张

<table>
  <tr>
    <td width="50%"><img src="assets/preview-poster.png" alt="竖版海报：SWISS STYLE"></td>
    <td width="50%"><img src="assets/preview-cover.png" alt="横版封面：GRID SYSTEM"></td>
  </tr>
  <tr>
    <td><sub>01 竖版海报 3:4 · 字体主导 · 编号 + 年份地点 + 极大标题 + 极小正文 + 红色锚点</sub></td>
    <td><sub>02 横版封面 16:9 · 不对称分栏 · 细线只走 8 栏 · 单点强调红</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="assets/preview-infographic.png" alt="数据页：GRID AUDIT"></td>
    <td width="50%"><img src="assets/preview-photo.png" alt="摄影海报：FORM FOLLOWS"></td>
  </tr>
  <tr>
    <td><sub>03 数据页 3:4 · 成果数字主导 · 三块指标 + 红色长度条</sub></td>
    <td><sub>04 黑白摄影混合 16:9 · 场景主导 · 窗洞节奏与网格同构</sub></td>
  </tr>
</table>

四张样张均为 AI 生成成品，用于验证这套规则的可执行性：12 栏网格、双字重强对比、左对齐、三色平涂、零装饰。每一张的完整提示词与偏差复盘都在 [`examples/`](examples/)。

## 核心特性

- **12 栏模块化网格**：栏宽 = 间距，`23U` 闭式解给出精确坐标；留白 ≥ 35%
- **两级字号阶梯**：极大标题 + 极小正文，比值 ≥ 8，**不允许中间档**
- **只用两种字重**：Regular 与 Bold；强调靠尺寸和位置，不靠字重堆叠
- **统一左对齐**：ragged right，不居中、不两端对齐
- **三色体系**：黑 `#000000` / 米白 `#F2EFE8` / 红 `#DA291C`，红色面积 ≤ 15%
- **纯平涂**：无阴影、渐变、纹理、装饰插画、3D
- **可量判**：36 项校验清单 + 30 秒三问，出稿能自己判合格

## 仓库结构

```
swiss-style-skill/
├── SKILL.md                   中文技能定义（入口 + 六条硬规则）
├── SKILL.en.md                英文技能定义
├── CHANGELOG.md               版本变更
├── references/                深度规范
│   ├── grid.md                网格计算、坐标公式、验算方法
│   ├── typography.md          字重白名单、字号倍数、tracking/leading
│   ├── color.md               三色职责、红色量判、平涂禁用清单
│   └── checklist.md           36 项交付校验清单
├── templates/                 可直接套用的模板
│   ├── image-prompt.md        6 组生图提示词（含反向提示词）
│   ├── poster-layout.md       竖版海报版式规范
│   └── cover-layout.md        横版封面与信息页规范
├── examples/                  真实案例：需求 → 提示词 → 成图 → 复盘
│   ├── 01-poster.md           竖版海报
│   ├── 02-cover.md            横版封面
│   ├── 03-infographic.md      数据页
│   └── 04-photo.md            黑白摄影混合
└── assets/                    四张样张
```

## 使用方式

### 一、直接当提示词用

1. 打开 [`templates/image-prompt.md`](templates/image-prompt.md)
2. 复制对应场景的模板
3. 把 `[场景]` 替换成你的主题
4. 粘贴到任意生图工具

### 二、作为 Skill 接入 AI 客户端

`SKILL.md` 带 YAML frontmatter（`name` / `description` / `version`），符合通用 Skill 规范：

```
<skill_root>/swiss-international-style/SKILL.md
```

`references/` 与 `templates/` 需与 `SKILL.md` 同级放置，Skill 会按链接渐进读取。
适用于 Cherry Studio、扣子 Coze、各类 Agent 框架的自定义技能目录。

### 三、作为设计交付规范

把 [`references/checklist.md`](references/checklist.md) 打印出来当验收单交给设计师，能砍掉大部分"再大气一点 / 再高级一点"的来回。

### 四、作为训练自己的教材

`examples/` 里每篇都有「决策链 + 偏差复盘」，比单纯给提示词更能说明**为什么这么做**。

## 快速示例

```
瑞士国际主义风格，平面设计百年展览海报，12 栏模块化网格系统
字体：新怪诞无衬线体，仅常规与粗体；超大号标题与极小号正文强对比
排版：全部左对齐，右侧不齐，不对称构图，大面积留白
色彩：纯黑、米白、强调红 #DA291C，全部平涂
元素：细实线分隔，01 编号，1924–2024 年份，单块红色几何矩形
排除：阴影、渐变、纹理、装饰插画、3D、图标
```

## 常见错误（生成后对照检查）

| 错误 | 为什么不行 |
| :--- | :--- |
| 标题居中 | 破坏左对齐不对称语法 |
| 用了 Medium / Light 字重 | 只允许 Regular 与 Bold |
| 加了渐变背景、投影 | 违反平涂原则 |
| 出现插画、图标、贴纸 | 违反禁用装饰 |
| 四级字号（大 / 中 / 小 / 微） | 只能强对比两级 |
| 全文两端对齐 | 必须 ragged right |
| 加入第三、第四种颜色 | 三色封顶 |
| 圆角卡片、胶囊按钮 | 属当代 UI 语言，非瑞士风格 |

## 版本

当前 **0.2.0**（2026-11-17）：结构升级 + 英文规范 + 4 个案例 + 2 张新样张。详见 [CHANGELOG.md](CHANGELOG.md)。

## 开源协议

MIT License，可自由商用、修改、再分发。

## 致谢

视觉规则源自 Josef Müller-Brockmann《Grid Systems in Graphic Design》与 1950–60 年代苏黎世 / 巴塞尔学派的平面设计实践。
