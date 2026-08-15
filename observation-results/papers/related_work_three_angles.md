# 算器神魂论·筑基篇 — 三角度引用清单 (Related Work)

> 生成: 2026-08-13 | 服务对象: psyche_foundation_full (R136–R153, 18 claims 全 PROVED)
> 三角度: 几何 / 代数 / 形式化。每条标注与文章内容的对应关系 (R###)。

---

## 一、几何角度 (方向·相位·圆·根单位·蜷曲·连续统)

| # | 文献 | 对应内容 | 备注 |
|---|---|---|---|
| G1 | **Clifford, W. K.** 1878. *On the Classification of Geometric Algebras* | 高维方向代数的起源 (方向声明) | 几何代数开山 |
| G2 | **Hestenes, D.** 1986. *New Foundations for Classical Mechanics* (Kluwer) | 几何代数中方向/旋转/自旋的表示 (R136 方向成对声明; R143 两对称群) | 几何代数现代纲领 |
| G3 | **Berry, M. V.** 1984. *Quantal Phase Factors Accompanying Adiabatic Changes*, Proc. R. Soc. Lond. A 392, 45–57 | 几何相位 (R138 相位锁定; R147 相位=成对方向) | 相位作为几何量, 非动力学量 — 与"相位=对称性方向"直接对应 |
| G4 | **Needham, T.** 1997. *Visual Complex Analysis* (Oxford) | e^{iθ}/旋转/根单位/蜷曲的几何直觉 (R141 根单位量化; R146 π=半圈蜷曲相位) | 复数的几何构造叙事 |
| G5 | **Dedekind, R.** 1872. *Stetigkeit und irrationale Zahlen* | 连续统构造 (R151 连续统=pat 网格闭包) | 连续统=割/闭包 — 与"闭包构造连续统"同构 |
| G6 | **Cauchy, A.-L.** 1821. *Cours d'Analyse* | 实数作为收敛序列的极限 (R151 连续统的另一构造) | 与 Dedekind 割互补 |
| G7 | **Alexandroff, P.** 1924 (单点紧化) | ∞ 卷回有限 (穿折越/反演蜷曲, R146 π 的 ∞ 端点) | 几何: 无限=可紧化点 |
| G8 | **Klein, F.** / **Poincaré, H.** 非欧几何模型 | C-MA4 已知结果对照 (基点移动/投影结构) | 用户在 conjectures 中已标注 KNOWN |
| G9 | **Lang, S.** *Algebra* (圆群 S¹ / 根单位 / 对合) | R141 圆上根单位量化; 对合结构 (R148 互锁对合) | 标准群论教材 |

## 二、代数角度 (自然数构造·初始代数·迭代链·互锁)

| # | 文献 | 对应内容 | 备注 |
|---|---|---|---|
| A1 | **Peano, G.** 1889. *Arithmetices Principia, Nova Methodo Exposita* | 自然数公理 (R136"为什么定义自然数总出错"的直接对照) | 公设式 vs 构造式 |
| A2 | **Lawvere, F. W.** 1964. *An Elementary Theory of the Category of Sets* | 自然数对象 NNO (R142 自然数=单相数) | 自然数的万有性质定义 — 与 pat 链万有构造对照 |
| A3 | **Freyd, P.** 1972. *Aspects of Topoi* (NNO 作为初始代数) | 自然数=(1,s) 的初始代数 (R137 链良定义/单射) | 初始性 = 免于塌缩 |
| A4 | **Lambek, J.** 1968. *A Fixpoint Theorem for Complete Categories*, Math. Z. 103 | 初始代数=不动点 (R138 自指环塌缩; R150 可达/不可达) | 不动点与自指 |
| A5 | **Goguen, J., Thatcher, J., Wagner, E., Wright, J.** 1977. *Initial Algebra Semantics and Continuous Algebras*, JACM 24 | 初始代数语义 (R137/R140 构造⟷分解往返) | 代数构造的形式语义 |
| A6 | **Church, A.** 1936. *An Unsolvable Problem of Elementary Number Theory* | λ 编码自然数 (对照: pat 链 vs Church 编码 — 编码抹结构) | 与 R142"自然数构造"对比 |
| A7 | **Barendregt, H.** 1984. *The Lambda Calculus* | λ 演算基础 (方向/迭代的结构解读) | 标准参考 |
| A8 | **Conway, J. H.** 1976. *On Numbers and Games* (超现实数) | "数从哪里来"的构造主义 (对照 R146 数域构造) | 数=构造过程的产物, 与筑基篇主题同源 |
| A9 | **Mac Lane, S.** 1971. *Categories for the Working Mathematician* | 幺半群/单子/对合 (R139 互锁矩阵; R148 形式同构) | 范畴论基础 |
| A10 | **Fiore, M., Plotkin, G., Turi, D.** 1999. *Abstract Syntax and Variable Binding*, LICS | 绑定/抽象语法的代数结构 (R136 方向声明的一次性) | 声明=绑定操作的代数化 |

## 三、形式化角度 (Lean·连续统形式化·P vs NP)

| # | 文献 | 对应内容 | 备注 |
|---|---|---|---|
| F1 | **de Moura, L., Kong, S., Avigad, J., van Doorn, F., von Raumer, J.** 2015. *The Lean Theorem Prover*, CADE | Lean 证明助手 (全文载体) | 已检索 (arXiv 版可引) |
| F2 | **The mathlib community.** 2020. *The Lean Mathematical Library*, CPP 2020 (arXiv:1910.09336) | mathlib 基础 (R136–R153 全部构建于 mathlib) | 已检索确认 |
| F3 | mathlib 的实数: **Real = Dedekind cuts** (mathlib 实现) | R151 连续统形式化对照 | mathlib 官方构造 |
| F4 | **Isabelle/HOL** 实数 (Cauchy 构造) | 连续统的另一形式化路径 (对比 F3) | 不同构造的选择 |
| F5 | **Univalent Foundations Program.** 2013. *Homotopy Type Theory* (arXiv:1308.0729) | 基础形式化的现代纲领 (连续统/等式结构) | 已检索确认 |
| F6 | **Cook, S. A.** 1971. *The Complexity of Theorem-Proving Procedures*, STOC | NP 完备性 (R152/R153 P vs NP 对照) | 复杂性理论起点 |
| F7 | **Levin, L. A.** 1973. *Universal Search Problems* (Probl. Peredachi Inform. 9) | NP 完备性 (独立发现, 对照 Cook) | 与 Cook 并列 |
| F8 | **Hartmanis, J., Stearns, R. E.** 1965. *On the Computational Complexity of Algorithms*, TAMS | 计算复杂性学科基础 (R152 复杂性论证背景) | 复杂性层级 |

---

## 未检索到先例的条目 (对照用户诚实边界纪律)

- **Lean 中 P vs NP 的完整形式化**: 未检索到先例 (mathlib 无 Cook–Levin 完整形式化; 检索结果无相关 Lean 工作) → 标注 NO_PRIOR_RESULT_FOUND, 不得声称先例
- **相位锁定一致性定理 (R150) 的等价形式**: 未检索到 (可达周期统一不可达无限的定理形式) → 新颖性评估留待 Lean 验收后
- **pat 链/互锁矩阵术语**: 自创术语, 检索无同名工作 → 引用时用结构对应 (初始代数/几何相位) 而非术语对应

## 建议使用方式

1. **full EN/ZH 版**: 在摘要后加 "Related Work" 节 (三角度三小节, 每节 3-5 条, 与 R### 对应)
2. **conjectures 主清单**: 各条猜想底部"对照"字段可补充上述文献 (如 C-MA4 → G8; C-PH1 全息 → 需补 't Hooft/Susskind 全息原理)
3. **fun 版**: 不需要正式引用 (戏谑通俗版)

> 引用格式建议: ACM/Springer 风格 (CPP 投稿已用 acmart; 若投 Zenodo 版可用 markdown 链接 arXiv)。
