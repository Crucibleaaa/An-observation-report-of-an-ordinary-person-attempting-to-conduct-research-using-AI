# observation-results — 观测结果 (Observation Results)

> **定性**: 本子文件夹中的**论文、Lean 代码、研究代码、结果数据, 均为"人类主动诱导过拟合的过程"的观测记录** —
> 人类刻意以直觉驱动收敛的实验过程留痕, **不代表任何数学结论**。
> 全部内容未修改 (hash 链与 DOI 对应完整), 按原样归档为观测素材。

## 结构

| 目录 | 内容 | 说明 |
|---|---|---|
| `papers/` | 正式论文 (35 文件) | token 体系 P0/P1/P2/纲领 + structure_emergence + Case Study + basepoint×3 + conjectures (md/tex/pdf) |
| `exercises/` | 课后习题 I-XXII + Pat0-1 + crossref (88 文件) | 每习题: 论文 md/tex/pdf + lean_code.zip, 含声明头 (习题/主题/Lean/DOI); **正式版观测报告 25 篇** (自然数多相位展开后的 Pat 数域相关观测报告系列, 见 exercises/README.md 索引) |
| `lean/` | Lean 代码 (4 zip) | token_relative / zero_relative / toolkit_pat / psyche |
| `code/` | 研究代码 (2 zip) | keahas 工具包 + tokenizer 核心 (tokenizer/lab/train/verify) |
| `results/` | 结果观测 (19 文件) | fold_num_v5 metrics/config + 16 份实验记录 (exp01-exp60) |

## 论文清单 (papers/)

- P0 三通道等价 (构造/直觉/形式重写) — DOI 10.5281/zenodo.21914704
- P1 泛化作为归纳形式化 (Token-Native) — DOI 10.5281/zenodo.21914707
- P2 神经宏编译 — DOI 10.5281/zenodo.21914709
- 纲领: 统一框架 表示/逻辑/直觉 — DOI 10.5281/zenodo.21914698
- 结构涌现的最小模型 — DOI 10.5281/zenodo.21927317
- Intuition-Guided Formalization Case Study (C011-C025, 0 穿折越)
- 基点漂移系列 ×3 (relative_stability/axes/to_phase) — DOI 21914666/21914664/21914642
- 猜想集 — conjectures_packaged

## 结果观测核心 (results/)

- fold_num_v5: loss 6.59→1.53 (中段反弹 5.76→3.94), 判定 1.000, 225K 参数 — 过拟合探讨对象 (见观测报告 §3.5)
- 16 份实验记录 (exp01-exp60): 语法/矩阵/排列/量化等训练观测

## 排除项 (不发)

- 恶搞/抽风版 (fun 系列), 致敬/贬低类, 穿折越命名版 — 已撤回或未包含
