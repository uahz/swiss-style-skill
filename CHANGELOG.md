# Changelog

## 0.2.0 — 2026-11-17

### 结构升级
- `SKILL.md` 精简为「入口 + 六条硬规则 + 速查表」，深度内容下沉到 `references/`
- 新增 `references/grid.md`：含 23U 闭式解、栏坐标公式、四类画幅参数表、跨栏允许表、三项快速验算
- 新增 `references/typography.md`：字重白名单、两级字号倍数、tracking / leading 数值表、断行规则、中英混排
- 新增 `references/color.md`：三色职责与面积、为什么禁止第四色、红色使用规则与量判法、平涂禁用清单、对比度底线
- 新增 `references/checklist.md`：A–H 共 36 项可勾选清单 + 30 秒三问

### 新增内容
- 新增 `SKILL.en.md`：完整英文规范（解决英文 README 中"规范仅中文"的缺口）
- 新增 `examples/`：4 个真实案例，每个含「原始需求 → 决策链 → 完整提示词 → 复盘」
  - 01 竖版海报（字体主导）
  - 02 横版封面（字体 + 红块）
  - 03 数据页（成果数字主导）
  - 04 黑白摄影混合（场景主导）
- 新增 2 张样张：`assets/preview-infographic.png`、`assets/preview-photo.png`
- 新增 `CHANGELOG.md`

### 修正
- 「三级字号对比」表述有歧义，改为「两级字号阶梯」，避免被误读成三级
- 补齐中文标题不做负字距、红色不可用于小字正文两条无障碍约束

## 0.1.0 — 2026-11-14

- 首版发布：`SKILL.md`（完整准则）、3 个版式/提示词模板、MIT 协议
- 2 张样张：竖版海报、横版封面
