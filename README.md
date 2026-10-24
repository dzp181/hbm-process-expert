# HBM 先进存储工艺专家（hbm-process-expert）

> WorkBuddy 专家包 · Agent 型 · 分类：技术工程（02-Engineering）

一位专注 **HBM（High Bandwidth Memory，高带宽内存）先进存储工艺整合** 的资深工艺工程师。把「一个堆叠指标做不上去」拆成具体工艺模块、窗口与失效模式——覆盖 DRAM 前道 → TSV → 薄化 → 微凸块/混合键合 → 塑封 → KGSD 测试全链路。

## 一句话描述

解读 HBM 3D 堆叠、TSV、混合键合与晶圆薄化路线，诊断良率失效，梳理设备材料卡点。

## 核心能力

1. **HBM 堆叠架构拆解** — 把代际规格（容量/带宽/位宽/层数/高度）翻译成工艺硬约束，讲清「为什么这一代必须换键合方式」
2. **TSV 全流程** — DRIE 深孔刻蚀、绝缘/阻挡/种子层、Cu 电镀 bottom-up 填充、CMP 露铜与 Cu pumping、KOZ 应力
3. **键合路线选型** — µbump + TC-NCF / MR-MUF vs 混合键合（Hybrid Bonding），量化对准精度、pitch 极限、热预算、返修性
4. **薄化与翘曲控制** — TBDB、超薄晶圆搬运、TTV/翘曲、堆叠共面度
5. **良率与失效分析** — stack yield 分解、失效模式四联表（现象→机理→量测→对策）
6. **设备与材料卡点** — 刻蚀/电镀/CMP/减薄/键合/量测/测试 + NCF/EMC/抛光液/前驱体/靶材/球形硅微粉

## 内置 Skill

`skills/hbm-process-knowledge` — 工艺知识底座：

| 文件 | 内容 |
|---|---|
| `references/process-params.md` | TSV / 薄化 / 键合 / 塑封 参数窗口与经验区间 |
| `references/failure-modes.md` | 电性、键合、结构、测试四类失效的四联表 |
| `references/supply-chain.md` | 设备与材料卡点矩阵、国产替代定位 |
| `templates/process-review-report.md` | 工艺评审 / 良率分析报告模板 |

## 使用示例

- HBM3E 的 12 层堆叠为什么难做？把 TSV、键合和良率的工艺难点讲清楚
- 对比 HBM4 的混合键合与 HBM3E 的微凸块方案，给出工艺选型判断
- HBM 良率卡在哪个环节？梳理设备与材料的国产替代卡点和相关标的

## 目录结构

```
hbm-process-expert/
├── .codebuddy-plugin/plugin.json          # 专家清单（含 SEO 展示字段与 keywords）
├── agents/hbm-process-expert.md           # 专家提示词
├── skills/hbm-process-knowledge/          # 工艺知识底座
│   ├── SKILL.md
│   ├── references/
│   └── templates/
├── avatars/expert.png                     # 头像 512×512
└── README.md
```

## 安装

1. 将 `hbm-process-expert/` 整个目录放入专家目录：

```
C:\Users\Administrator\.workbuddy\plugins\marketplaces\my-experts\plugins\hbm-process-expert\
```

2. 注册后在 WorkBuddy【专家中心 - 我的专家】中可见。

## 打包

```bash
python3 scripts/package_expert.py <expert-dir>
```

## 检索关键词

HBM、HBM3E、HBM4、高带宽内存、High Bandwidth Memory、先进存储、3D堆叠、TSV、硅通孔、混合键合、Hybrid Bonding、微凸块、MR-MUF、晶圆薄化、先进封装、2.5D封装、CoWoS、DRAM工艺、良率分析、失效分析、半导体设备材料、国产替代

## 免责声明

本专家提供工艺技术分析与产业链定位，不构成投资建议。涉及具体公司的份额、产能、订单、验证进度，需以公司公告与一手资料核验；涉及工艺参数均为公开文献与工程经验区间，非厂商机密参数。

## License

MIT
