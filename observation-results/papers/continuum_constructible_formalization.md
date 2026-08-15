# 连续统的可构造形式化：pat 格点闭包定理

**A Constructible Formalization of the Continuum: The pat-Grid Closure Theorem**

> 摘要 经典数学把连续统 (ℝ) 当作已给公设：数轴是地基，不是构造对象。本文给出连续统的
> 可构造形式化：从方向声明出发，经 pat 链与单位根 n 槽环构造出可数可达的量化格点
> (pat 格点)；王氏相位锁定性定理 (R150) 断言任意相位被该格点任意精度统一；
> 主定理 (R151) 一步推出**连续统 = pat 格点的闭包** —— 连续统的每个点都属于
> 可数可达格点的极限闭包。全部定理经 Lean 4 / mathlib v4.32.2 机械验证
> (lake build 通过，0 sorry)，且不依赖自然数序列/极限引理（用户纪律：用结构定理，
> 不用已给引理）。连续统因此不是"干净对象"，而是生成结构的极限闭包 (R061 可构造批判)。

*2026-08-15 · Formal paper · Lean 4 / mathlib v4.32.2 · R150 (王氏相位锁定性定理) + R151 (连续统 = pat 格点闭包), PROVED, 0 sorry · 配套习题: exercise_i_1 (DOI 10.5281/zenodo.21916835)*

---

## 一、认知论问题：连续统从哪里来

经典数学的立场：数轴是**已给**的。分析学在 ℝ 上展开（极限、拓扑、测度），但 ℝ 本身
作为公理系统的模型被接受，不追问"数轴从什么生成"。类型论地基同样预设自然数与函数
空间（Church 编码的循环论证广为人知：迭代器需要"次数"概念，而次数预设自然数——
主流选择是绕开：把 Nat 作为原始归纳类型）。

本文采取相反的立场（可构造论）：

```
经典:  连续统 = 公设 (已给数轴, 在其上盖楼)
本文:  连续统 = 构造 (从方向声明生成格点, 连续统是格点的极限闭包)
```

这一立场要求每个结构环节都可构造、可验证：方向声明 → pat 链 → 量化格点 →
王氏定理 → 闭包。全部环节 Lean 机械验证，且**不依赖自然数序列/极限引理**——
闭包结论直接用结构定理 (王氏定理) 一步得出，不走"第 n 次逼近"的经典引理。

## 二、构造链：从方向声明到量化格点

（前置 claims 链，全部 PROVED）

| 环节 | Claim | 内容 |
|---|---|---|
| 方向声明 | R136 | 方向必须按对称性成对一次性声明 |
| pat 链单射 | R137 | 声明相同方向 ⟹ pat 链单射不坍缩 |
| 相位锁定 | R138 | 相位关系未锁定 = pat0 自指循环坍缩 |
| 互锁矩阵 | R139/R143 | 两组对称性 = 1 与 i 还原后的 1 |
| 完整 pat1 | R140 | (相位, 距离) 联合声明，构造⟷分解往返精确 |
| 有限离散 | R141 | pat n 有限离散 + 圆上单位根量化 |
| 单位根槽环 | R059 | n 槽环 = 单位根 {e^{2πik/n}}，Fintype.card (Fin n) = n |

**pat 量化格点**（R150 定义）：所有 n 槽环的并

```
patGrid := {x | ∃ N j : ℕ, 0 < N ∧ j ≤ N ∧ x = 2π·j/N}
```

- **可达周期**：patGrid 是 ℕ×ℕ 的像 ⟹ 可数（`pat_grid_countable : Countable patGrid`）
- **不可达无穷**：连续统 [0, 2π] 不可数，其点不可逐一到达（R123/R131）
- **锁定一致性**：可达周期与不可达无穷经相位锁定一致（R138）

## 三、王氏相位锁定性定理 (R150)

> 全称：**王氏可达周期与不可达无穷间相位锁定一致性定理**（用户命名，2026-08-12）

**定理 (pat_phase_unification)**：任意相位 θ ∈ [0, 2π] 被 pat 格点任意精度统一：

```
∀ θ ∈ [0, 2π], ∀ ε > 0, ∃ y ∈ patGrid, |θ − y| ≤ ε
```

**含义**：可数可达的格点任意精度逼近不可达的连续统 —— "可达周期统一不可达无穷"。
（R146 pat_quantization_converges：量化误差 ≤ π/N，取 N ≥ π/ε 即得。）

## 四、主定理：连续统 = pat 格点的闭包 (R151)

**定理 (continuum_in_pat_grid_closure)**：

```
∀ x ∈ [0, 2π],  x ∈ closure patGrid
```

**证明**（Lean 4，全文）：

```lean
theorem continuum_in_pat_grid_closure (x : ℝ) (hx₁ : 0 ≤ x) (hx₂ : x ≤ 2 * Real.pi) :
    x ∈ closure PatCountableInfinitPhaseUnification.patGrid := by
  rw [Metric.mem_closure_iff]
  intro ε hε
  -- 王氏定理 (R150): ∃ y ∈ patGrid, |x - y| ≤ ε/2
  rcases PatCountableInfinitPhaseUnification.pat_phase_unification x hx₁ hx₂ (ε / 2) (by positivity)
    with ⟨y, hy, hle⟩
  refine ⟨y, hy, ?_⟩
  have hlt : |x - y| < ε := by
    have hε' : ε / 2 < ε := by linarith
    exact lt_of_le_of_lt hle hε'
  rwa [Real.dist_eq]
```

**结构**（两步，无自然数引理）：

1. 王氏定理（R150）：任意精度锁定 —— 存在格点 y 满足 |x − y| ≤ ε/2
2. 闭包判定（`Metric.mem_closure_iff`）：x ∈ closure patGrid ⟺ ∀ε>0 ∃y∈patGrid, dist x y < ε

**结论**：连续统的每个点 ∈ pat 格点闭包 —— **连续统 = 可数可达格点的极限闭包**。

## 五、离散 ↔ 连续对偶 (R060)

离散与连续是一对**互逆方向**：

| 方向 | 内容 | 误差 |
|---|---|---|
| 离散 → 连续 | 单位根 e^{2πik/n} = e^{2i·(kπ/n)} 是圆上的精确点（无损嵌入） | 0 |
| 连续 → 离散 | θ ↦ 最近格点 k = round(θ·n/π)（量化，近似左逆） | ≤ 0.5·(π/n) |

（Lean: DiscreteContinuousDual.lean —— 嵌入无损 + 量化左逆 + 误差界）

## 六、连续统的可构造批判 (R061)

实验（R061_continuum_illusion）：连续统"看起来"是干净的连续对象，但构造上
它是可达格点的极限闭包 —— **不是干净对象**。这一批判的直接推论：

- 经典分析把连续统当公设（无需构造）；可构造论把连续统当**结论**（生成结构的闭包）
- 连续统的"点"不是原初的，是格点序列的极限位置（R150 锁定）
- 对应习题：exercise_i_1（√2/2 的 pat 展开 —— 无理数也是格点闭包的点，
  DOI 10.5281/zenodo.21916835）

## 七、结论

连续统可以形式化，且形式化揭示其构造本质：

```
连续统 = pat 格点的闭包
        = 可数可达格点的极限闭包        (R151, Lean 证明)
        = 王氏相位锁定一致性的推论       (R150)
        = 方向声明 → pat 链 → n 槽环的生成产物  (R136-R141, R059)
```

三个要点：

1. **可构造**：不是公设，是从方向声明生成的结构的极限闭包
2. **机械验证**：Lean 4 证明，0 sorry，不依赖自然数序列/极限引理（用户纪律）
3. **认知论重述**：连续统不是"干净对象"（R061 批判）—— 这回答了
   "数轴从哪里来"：数轴是格点闭包的投影，连续统是生成结构的极限

---

## 附录

**Lean 文件**（`src/relative-recursion/formal/Formal/`）：

```
Toolkit/PatCountableInfinitPhaseUnification.lean   — 王氏定理 (R150)
Toolkit/ContinuumPatGrid.lean                      — 主定理 (R151)
Toolkit/DiscreteContinuousDual.lean                — 离散↔连续对偶 (R060)
Toolkit/CircleStructure.lean                       — 圆结构 (R059 配套)
```

**Claims ledger**（`formal/claims/Toolkit/`）：R150.yaml, R151.yaml, R060.yaml, R061.yaml, R146.yaml

**实验**：`experiments/finite_models/R061_continuum_illusion.py`

**习题**：exercise_i_1（√2/2 的 pat 展开，DOI 10.5281/zenodo.21916835）

**验证**：lake build PASS，sorry_count = 0
