---
name: swiss-international-style
description: 按瑞士国际主义风格（Swiss Style / International Typographic Style）产出设计方案、AI 生图提示词与版式规范。当用户提到瑞士风格、国际主义风格、Swiss Style、Helvetica 排版、12 栏网格海报，或要求"极简 + 网格 + 大字标题"的版式设计时使用。
version: 0.2.0
---

# 瑞士国际主义风格版式设计

严格按照 1950 年代瑞士国际主义（International Typographic Style）的视觉语法工作。
所有输出必须 100% 遵守下方硬规则。**不做"审美优化"式的自由发挥。**

深度细节见 `references/`，真实案例见 `examples/`，交付前逐条核对 `references/checklist.md`。

---

## 一、六条硬规则（不可协商）

### 1. 网格
12 栏模块化网格，所有元素边缘落在网格线上；不对称构图，留白 ≥ 35%。禁止居中对称。
→ 完整规格见 [references/grid.md](references/grid.md)

### 2. 字体
只用新怪诞无衬线体（Helvetica / Neue Haas Grotesk / Inter）；只用 Regular 与 Bold 两种字重。
→ 字号阶梯、字距行距、断行规则见 [references/typography.md](references/typography.md)

### 3. 对齐
一切文字左对齐，右侧参差不齐（ragged right）。禁止居中、右对齐、两端对齐。

### 4. 色彩
只用三色：纯黑 `#000000`、米白 `#F2EFE8`、强调红 `#DA291C`。全部平涂。
禁止阴影、渐变、纹理、噪点、浮雕、光晕、玻璃拟态。红色面积 ≤ 15%。
→ 配色职责与禁用清单见 [references/color.md](references/color.md)

### 5. 元素
图像只用黑白摄影或简单几何形。禁止装饰插画、卡通、3D、具象图标、纹样、贴纸。
分隔只用 0.5–1pt 细实线。

### 6. 点缀
只允许：两位数字编号 `01` `02`、小号年份 `1957`、地点 `ZÜRICH`、页码。禁止其他符号与 emoji。

---

## 二、三级字号对比（唯一允许的层级）

```
极大  Bold     标题、关键数字      画面宽度的 60–80%，跨 6–8 栏
极小  Regular  正文、标签、元信息  8–11pt 等效，跨 2–4 栏
```

**只有两级，没有中间档。** 出现 Medium、小标题、副标题字号梯度的方案一律重做。

---

## 三、版式结构（速查）

| 版式 | 从上到下 |
| :--- | :--- |
| 竖版海报 3:4 | `01`+年份地点 → 极大标题 → 极小正文 → 红色/照片锚点 → 细线+页脚 |
| 横版封面 16:9 | `01`+分类 → 左或右极大标题 → 另一侧极小正文 → 横向细线 → 页脚 |
| 数据页 | 顶部编号+标题 → 3 个数据块（极大数字 + 极小标签 + 红色比例条）→ 来源 |

完整坐标与尺寸见 [templates/poster-layout.md](templates/poster-layout.md) 与 [templates/cover-layout.md](templates/cover-layout.md)。

---

## 四、AI 生图提示词（最小可用版）

```
瑞士国际主义风格，[场景]，12 栏模块化网格，所有元素对齐网格线
字体：新怪诞无衬线体，仅常规与粗体；超大标题 + 极小正文
排版：全部左对齐，右侧不齐，不对称构图，大面积留白
色彩：纯黑、米白 #F2EFE8、强调红 #DA291C，全部平涂
元素：极细线、01 编号、小号年份地点、[黑白摄影 / 红色矩形]
排除：阴影、渐变、纹理、装饰插画、3D、图标、emoji
```

分场景模板（含反向提示词）见 [templates/image-prompt.md](templates/image-prompt.md)。

---

## 五、自检（输出前必过）

完整勾选清单见 [references/checklist.md](references/checklist.md)。四条高频失败点：

1. 标题居中了 → 破坏不对称语法
2. 出现第三、第四种颜色 → 三色封顶
3. 出现 Medium / Light 字重 → 只许 Regular 与 Bold
4. 加了渐变或投影 → 违反平涂

---

## 六、常见错误对照

| 错误 | 原因 |
| :--- | :--- |
| 标题居中 | 破坏左对齐不对称语法 |
| 使用 Medium / Light 字重 | 只允许 Regular 与 Bold |
| 加入渐变背景、投影 | 违反平涂原则 |
| 插图、线描装饰、贴纸 | 违反禁用装饰插画 |
| 四级字号（大/中/小/微） | 只能强对比两级 |
| 全文两端对齐 | 必须 ragged right |
| 加入第三、第四种颜色 | 三色封顶 |
| 圆角卡片、胶囊按钮 | 属当代 UI 语言，非瑞士风格 |
| 满版铺内容、无留白 | 留白是构图主语，不是剩余空间 |

---

## 七、真实案例

| 案例 | 类型 | 文件 |
| :--- | :--- | :--- |
| SWISS STYLE | 竖版海报 3:4 | [examples/01-poster.md](examples/01-poster.md) |
| GRID SYSTEM | 横版封面 16:9 | [examples/02-cover.md](examples/02-cover.md) |
| GRID AUDIT | 数据页 3:4 | [examples/03-infographic.md](examples/03-infographic.md) |
| FORM FOLLOWS | 黑白摄影混合 16:9 | [examples/04-photo.md](examples/04-photo.md) |

每个案例都含：原始需求 → 完整提示词 → 成图 → 复盘（哪里偏离了规则）。

---

## 八、场景适配

- **印刷品**：按实际纸张尺寸排版，外边距取短边 6–8%，不以屏幕比例替代。
- **屏幕海报**：3:4 竖版 / 16:9 横版；社交方图 1:1。
- **信息密集**：先合并重复信息，再调栏宽分组；**不缩小字号、不删事实**来腾空间。
- **多页连续**：编号位置、页码位置、红色位置每页固定，形成翻页节奏。

---

## 版本

当前 0.2.0，变更见 [CHANGELOG.md](CHANGELOG.md)。
英文规范见 [SKILL.en.md](SKILL.en.md)。
