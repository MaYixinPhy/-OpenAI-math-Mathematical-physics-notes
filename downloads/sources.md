# 来源、版本与核验记录

核对日期：2026-10-07（北京时间）。固定提交：[`adc7f1241b42e322a6451854ab7e4b4c146bf78a`](https://github.com/openai/math/commit/adc7f1241b42e322a6451854ab7e4b4c146bf78a)。

## 范围与证据层次

- 全库计数：README 声明 722 篇稿件、372 个问题族。
- 本报告纳入：overview.tex 中 Mathematical physics 类的所有条目 260–284，共 25 族、59 篇；没有按熟悉程度筛选或遗漏其中的计算复杂性条目。
- 稿件说明：读取各论文 LaTeX 摘要，逐族核对主要定理，并检查会改变物理解读的边界条件、极限顺序及部分证明结构。这里的“核对”是原文与报告之间的语义对照，不是独立重证。
- 历史资料：优先使用原始论文的出版社页面、arXiv 摘要及版本记录。除明确读取的部分外，没有对历史论文进行全文证明审查；历史引用不承担验证本次新证明的作用。
- 没有执行 Lean/Comparator 或计算机辅助证书，也没有进行实验、数值模拟或逐行审稿。
- 对潜在研究影响的判断由本报告给出，不能当作稿件已经证明的额外推论。

## 官方资料

- [README：计数、发布说明和验证状态](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/README.md)
- [overview.tex：分类与问题族摘要](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/overview.tex)
- [CONTENTS.md：稿件地图](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/CONTENTS.md)
- [formalization.yaml：形式化目录](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/lean/formalization.yaml)
- [Comparator 验证说明](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/lean/ComparatorChallenges/README.md)

## 形式化目录匹配结果

“已列入”仅表示该稿件路径出现在固定版本 formalization.yaml 的 sources 目录中；不表示本报告已编译证明、审计公理或确认形式命题与全部物理陈述等价。“未列入”也不证明仓库中绝无相关 Lean 文件。

| 问题族 | 稿件数 | 目录列入数 |
|---|---:|---:|
| 260 | 13 | 0 |
| 261 | 2 | 0 |
| 262 | 3 | 1 |
| 263 | 3 | 1 |
| 264 | 3 | 0 |
| 265 | 2 | 0 |
| 266 | 2 | 0 |
| 267 | 5 | 0 |
| 268 | 2 | 0 |
| 269 | 2 | 1 |
| 270 | 2 | 0 |
| 271 | 4 | 0 |
| 272 | 1 | 0 |
| 273 | 1 | 0 |
| 274 | 2 | 2 |
| 275 | 2 | 0 |
| 276 | 1 | 1 |
| 277 | 1 | 1 |
| 278 | 1 | 0 |
| 279 | 1 | 0 |
| 280 | 1 | 0 |
| 281 | 2 | 0 |
| 282 | 1 | 0 |
| 283 | 1 | 0 |
| 284 | 1 | 0 |

合计 59 篇中 7 篇列入，分属 6 个问题族。特别地，262 仅标量稿列入；269 仅无扰动能隙稿列入；不能据此宣称其所有配套推广已形式化。

## 检索过程与覆盖限制

检索采用“官方目录 → 主稿摘要与定理 → 配套稿条件 → 原始历史文献”的顺序，检索日在 2026-10-07。代表查询包括：

- `site:github.com/openai/math physics`：定位官方分类与目录。
- `Penrose inequality review Mars`、`Dafermos Luk Kerr Cauchy horizon`：引力背景及正则性差别。
- `Anderson 1958 scaling theory localization 1979`、`Lieb Thirring inequalities Frank`、`ionization conjecture Solovej`：无序及原子谱背景。
- `Hastings area law 2007`、`Haldane 1983`、`Laughlin 1983`、`Proof of Bose-Einstein Condensation Lieb Seiringer`、`Validity of spin wave theory`：量子多体历史。
- `BFSS M theory matrix model 1996`、`scale conformal invariance Dymarsky`、`vertex operator algebras conformal nets Carpi`：矩阵模型及场论。
- `entropy photon-number inequality`、`generalized amplitude damping capacity`、`secure key from bound entanglement`、`entangled games parallel repetition`：量子信息。
- `QAC0 parity`、`QAOA Sherrington Kirkpatrick`、`Boolean unitary synthesis`、`Huang sensitivity quantum implications`：电路与查询。
- `Kohn Sham representability`、`Schuch Verstraete computational complexity electrons`、`Shor prime factorization`：电子结构与算法。

这是一份围绕指定目录的主题介绍，不是按预注册方案进行的全领域系统综述，也没有声称穷尽 2026 年以前所有独立进展。检索中特别核实了 arXiv:2411.00976 已撤回，未把其摘要里的旧证明主张作为既成事实。

## 59 篇稿件的固定版本链接

下列 Oxxx-yy 是本文检索编号；官方 BibTeX 键保留在每条后面，并收录于 [references.bib](references.bib)。

<a id="family-260"></a>

## 260｜时空 Penrose 不等式：黑洞面积需要多少质量

- **O260-01** [The spacetime Penrose inequality with charge and original-data rigidity](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-spacetime-Penrose-inequality-with-charge-and-original-data-rigidity-October-5-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:The-spacetime-Penrose-inequality-with-charge-and-original-data-rigidity-October-5-2026`。
- **O260-02** [A Charged Reduction of the Spacetime Penrose Inequality in Spatial Dimensions at Least Four](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/A-Charged-Reduction-of-the-Spacetime-Penrose-Inequality-in-Spatial-Dimensions-at-Least-Four-October-5-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:A-Charged-Reduction-of-the-Spacetime-Penrose-Inequality-in-Spatial-Dimensions-at-Least-Four-October-5-2026`。
- **O260-03** [Spacetime Penrose inequalities: enclosing area, charge, and rigidity](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Spacetime-Penrose-inequalities-enclosing-area-charge-and-rigidity-October-5-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Spacetime-Penrose-inequalities-enclosing-area-charge-and-rigidity-October-5-2026`。
- **O260-04** [The Kerr–Newman Penrose Inequality for Axisymmetric Electrovacuum Exteriors](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-Kerr-Newman-Penrose-Inequality-for-Axisymmetric-Electrovacuum-Exteriors-October-5-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:The-Kerr-Newman-Penrose-Inequality-for-Axisymmetric-Electrovacuum-Exteriors-October-5-2026`。
- **O260-05** [Electromagnetic tails and the Kerr–Newman Penrose inequality](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Electromagnetic-tails-and-the-Kerr-Newman-Penrose-inequality-October-5-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Electromagnetic-tails-and-the-Kerr-Newman-Penrose-inequality-October-5-2026`。
- **O260-06** [The nonmaximal anti-de Sitter Penrose Inequality and original-data rigidity](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-nonmaximal-anti-de-Sitter-Penrose-Inequality-and-original-data-rigidity-October-5-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:The-nonmaximal-anti-de-Sitter-Penrose-Inequality-and-original-data-rigidity-October-5-2026`。
- **O260-07** [The Penrose inequality for maximal asymptotically hyperbolic initial data](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-Penrose-inequality-for-maximal-asymptotically-hyperbolic-initial-data-October-5-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:The-Penrose-inequality-for-maximal-asymptotically-hyperbolic-initial-data-October-5-2026`。
- **O260-08** [A local Penrose inequality for conformal perturbations of Schwarzschild–anti-de Sitter data](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/A-local-Penrose-inequality-for-conformal-perturbations-of-Schwarzschild-anti-de-Sitter-data-October-5-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:A-local-Penrose-inequality-for-conformal-perturbations-of-Schwarzschild-anti-de-Sitter-data-October-5-2026`。
- **O260-09** [The spacetime Penrose inequality and enclosing area](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-spacetime-Penrose-inequality-and-enclosing-area-September-27-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:The-spacetime-Penrose-inequality-and-enclosing-area-September-27-2026`。
- **O260-10** [Conformal flow and the Riemannian Penrose inequality with minimizing frontiers](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Conformal-flow-and-the-Riemannian-Penrose-inequality-with-minimizing-frontiers-September-27-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Conformal-flow-and-the-Riemannian-Penrose-inequality-with-minimizing-frontiers-September-27-2026`。
- **O260-11** [Equality and rigidity in the spacetime Penrose inequality](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Equality-and-rigidity-in-the-spacetime-Penrose-inequality-September-27-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Equality-and-rigidity-in-the-spacetime-Penrose-inequality-September-27-2026`。
- **O260-12** [Boundary graph deformations for the spacetime Penrose inequality](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Boundary-graph-deformations-for-the-spacetime-Penrose-inequality-September-27-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Boundary-graph-deformations-for-the-spacetime-Penrose-inequality-September-27-2026`。
- **O260-13** [Area-controlled end replacement and the Bondi–Penrose inequality in the CKS class](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Area-controlled-end-replacement-and-the-Bondi-Penrose-inequality-in-the-CKS-class-September-27-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Area-controlled-end-replacement-and-the-Bondi-Penrose-inequality-in-the-CKS-class-September-27-2026`。

<a id="family-261"></a>

## 261｜Anderson 模型：无序为何在二维和三维表现不同

- **O261-01** [Absolutely Continuous Spectrum for Weak-Disorder Anderson Models in Dimensions at Least Three](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Absolutely-Continuous-Spectrum-for-Weak-Disorder-Anderson-Models-in-Dimensions-at-Least-Three-September-23-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Absolutely-Continuous-Spectrum-for-Weak-Disorder-Anderson-Models-in-Dimensions-at-Least-Three-September-23-2026`。
- **O261-02** [Pure-Point Spectrum for the Two-Dimensional Anderson Model at Every Positive Disorder](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Pure-Point-Spectrum-for-the-Two-Dimensional-Anderson-Model-at-Every-Positive-Disorder-September-23-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Pure-Point-Spectrum-for-the-Two-Dimensional-Anderson-Model-at-Every-Positive-Disorder-September-23-2026`。

<a id="family-262"></a>

## 262｜一维 Lieb–Thirring 最优常数：势阱能束缚多少负能量

- **O262-01** [Equality cases in the sharp one-dimensional matrix Lieb–Thirring inequality](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Equality-cases-in-the-sharp-one-dimensional-matrix-Lieb-Thirring-inequality-October-5-2026/sharp-one-dimensional-lieb-thirring-inequalities-matrix-potentials.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Equality-cases-in-the-sharp-one-dimensional-matrix-Lieb-Thirring-inequality-October-5-2026`。
- **O262-02** [Sharp one-dimensional Lieb–Thirring inequalities for matrix potentials](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Sharp-one-dimensional-Lieb-Thirring-inequalities-for-matrix-potentials-October-5-2026/sharp-matrix-lieb-thirring.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Sharp-one-dimensional-Lieb-Thirring-inequalities-for-matrix-potentials-October-5-2026`。
- **O262-03** [Sharp one-dimensional Lieb–Thirring constants](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Sharp-One-Dimensional-Lieb-Thirring-Constants-September-23-2026/paper.pdf)。形式化目录：已列入。BibTeX 键：`OAI:Sharp-One-Dimensional-Lieb-Thirring-Constants-September-23-2026`。

<a id="family-263"></a>

## 263｜电离猜想：大原子的最外层为何仍保持有限尺度

- **O263-01** [Uniform excess charge for Coulomb molecules and the outer radius of neutral atoms](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Uniform-excess-charge-for-Coulomb-molecules-and-the-outer-radius-of-neutral-atoms-September-24-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Uniform-excess-charge-for-Coulomb-molecules-and-the-outer-radius-of-neutral-atoms-September-24-2026`。
- **O263-02** [Generalized ionization energies for full Coulomb atoms](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Generalized-ionization-energies-for-full-Coulomb-atoms-September-24-2026/paper.pdf)。形式化目录：已列入。BibTeX 键：`OAI:Generalized-ionization-energies-for-full-Coulomb-atoms-September-24-2026`。
- **O263-03** [Generalized outer-electron radii of neutral Coulomb atoms](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Generalized-outer-electron-radii-of-neutral-Coulomb-atoms-September-24-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Generalized-outer-electron-radii-of-neutral-Coulomb-atoms-September-24-2026`。

<a id="family-264"></a>

## 264｜Kerr 附近的强宇宙监督：爱因斯坦方程能预测到哪里

- **O264-01** [Generic Future Inextendibility with Square-Integrable Connection Near a Fixed Kerr Spacetime](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Generic-Future-Inextendibility-with-Square-Integrable-Connection-Near-a-Fixed-Kerr-Spacetime-September-23-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Generic-Future-Inextendibility-with-Square-Integrable-Connection-Near-a-Fixed-Kerr-Spacetime-September-23-2026`。
- **O264-02** [Generic C¹ Future Inextendibility Near Rotating Subextremal Kerr Spacetimes](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Generic-C1-Future-Inextendibility-Near-Rotating-Subextremal-Kerr-Spacetimes-September-23-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Generic-C1-Future-Inextendibility-Near-Rotating-Subextremal-Kerr-Spacetimes-September-23-2026`。
- **O264-03** [Quantitative Near-Kerr Evolution and Generic C² Future Inextendibility](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Quantitative-Near-Kerr-Evolution-and-Generic-C2-Future-Inextendibility-September-23-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Quantitative-Near-Kerr-Evolution-and-Generic-C2-Future-Inextendibility-September-23-2026`。

<a id="family-265"></a>

## 265｜二维有隙面积律：为什么基态纠缠没有铺满体积

- **O265-01** [A two-dimensional area law from a global spectral gap](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/A-two-dimensional-area-law-from-a-global-spectral-gap-September-24-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:A-two-dimensional-area-law-from-a-global-spectral-gap-September-24-2026`。
- **O265-02** [Polynomial PEPS approximation of gapped square-grid ground states](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Polynomial-PEPS-approximation-of-gapped-square-grid-ground-states-September-24-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Polynomial-PEPS-approximation-of-gapped-square-grid-ground-states-September-24-2026`。

<a id="family-266"></a>

## 266｜六维互无偏基：六能级系统能容纳几组完全互补的测量

- **O266-01** [The maximum number of mutually unbiased bases in dimension six](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-maximum-number-of-mutually-unbiased-bases-in-dimension-six-September-24-2026/The-maximum-number-of-mutually-unbiased-bases-in-dimension-six-September-24-2026.pdf)。形式化目录：未列入。BibTeX 键：`OAI:The-maximum-number-of-mutually-unbiased-bases-in-dimension-six-September-24-2026`。
- **O266-02** [Exact Fourier certificates for complex Hadamard matrices of order six](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Exact-Fourier-certificates-for-complex-Hadamard-matrices-of-order-six-September-24-2026/Exact-Fourier-certificates-for-complex-Hadamard-matrices-of-order-six-September-24-2026.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Exact-Fourier-certificates-for-complex-Hadamard-matrices-of-order-six-September-24-2026`。

<a id="family-267"></a>

## 267｜稀薄玻色气体：正温凝聚与量子耗尽

- **O267-01** [Bose–Einstein condensation at positive temperature in the dilute hard-sphere gas](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Bose-Einstein-condensation-at-positive-temperature-in-the-dilute-hard-sphere-gas-October-5-2026/positive-temperature-hard-spheres.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Bose-Einstein-condensation-at-positive-temperature-in-the-dilute-hard-sphere-gas-October-5-2026`。
- **O267-02** [Quantum Depletion and Momentum Distribution in the Dilute Hard-Sphere Bose Gas](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Quantum-Depletion-and-Momentum-Distribution-in-the-Dilute-Hard-Sphere-Bose-Gas-October-5-2026/Quantum-Depletion-in-the-Dilute-Hard-Sphere-Bose-Gas.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Quantum-Depletion-and-Momentum-Distribution-in-the-Dilute-Hard-Sphere-Bose-Gas-October-5-2026`。
- **O267-03** [Quantum Depletion for Fixed Bounded Repulsive Potentials](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Quantum-Depletion-for-Fixed-Bounded-Repulsive-Potentials-October-5-2026/fixed-repulsion-quantum-depletion.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Quantum-Depletion-for-Fixed-Bounded-Repulsive-Potentials-October-5-2026`。
- **O267-04** [A density-uniform condensate bound for dilute Bose gases](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/A-density-uniform-condensate-bound-for-dilute-Bose-gases-September-27-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:A-density-uniform-condensate-bound-for-dilute-Bose-gases-September-27-2026`。
- **O267-05** [Ground-state condensation in the dilute hard-sphere gas](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Ground-state-condensation-in-the-dilute-hard-sphere-gas-September-24-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Ground-state-condensation-in-the-dilute-hard-sphere-gas-September-24-2026`。

<a id="family-268"></a>

## 268｜自旋一 Haldane 能隙：整数自旋链的经典预言

- **O268-01** [The periodic spin-one Haldane gap](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-periodic-spin-one-Haldane-gap-September-24-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:The-periodic-spin-one-Haldane-gap-September-24-2026`。
- **O268-02** [A boundary-field gap for the spin-one Heisenberg chain](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/A-boundary-field-gap-for-the-spin-one-Heisenberg-chain-September-24-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:A-boundary-field-gap-for-the-spin-one-Heisenberg-chain-September-24-2026`。

<a id="family-269"></a>

## 269｜Laughlin 能隙及无序稳定性：分数量子霍尔态为何坚固

- **O269-01** [Uniform Stability of the Spherical Laughlin Gap](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Uniform-Stability-of-the-Spherical-Laughlin-Gap-October-5-2026/uniform-stability-spherical-laughlin-gap.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Uniform-Stability-of-the-Spherical-Laughlin-Gap-October-5-2026`。
- **O269-02** [A Fock-space inequality and the Laughlin spectral gap](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/A-Fock-space-inequality-and-the-Laughlin-spectral-gap-September-24-2026/A-Fock-space-inequality-and-the-Laughlin-spectral-gap-September-24-2026.pdf)。形式化目录：已列入。BibTeX 键：`OAI:A-Fock-space-inequality-and-the-Laughlin-spectral-gap-September-24-2026`。

<a id="family-270"></a>

## 270｜BFSS 矩阵模型的束缚态：D0 膜如何组成一个粒子

- **O270-01** [The unique threshold bound state of the SU(N) BFSS model](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-unique-threshold-bound-state-of-the-SU-N-BFSS-model-September-24-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:The-unique-threshold-bound-state-of-the-SU-N-BFSS-model-September-24-2026`。
- **O270-02** [Positive eigenvalues of the relative SU(2) BFSS Hamiltonian](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Positive-eigenvalues-of-the-relative-SU-2-BFSS-Hamiltonian-October-5-2026/positive-eigenvalues-relative-su2-bfss.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Positive-eigenvalues-of-the-relative-SU-2-BFSS-Hamiltonian-October-5-2026`。

<a id="family-271"></a>

## 271｜Heisenberg 铁磁体：自发磁化与 Bloch 的低温定律

- **O271-01** [Bloch's Law for Finite-Range Heisenberg Ferromagnets in Three Dimensions](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Blochs-Law-for-Finite-Range-Heisenberg-Ferromagnets-in-Three-Dimensions-October-5-2026/bloch-law-heisenberg.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Blochs-Law-for-Finite-Range-Heisenberg-Ferromagnets-in-Three-Dimensions-October-5-2026`。
- **O271-02** [The first lattice correction to Bloch's law](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-first-lattice-correction-to-Blochs-law-October-5-2026/first-lattice-correction-bloch-law.pdf)。形式化目录：未列入。BibTeX 键：`OAI:The-first-lattice-correction-to-Blochs-law-October-5-2026`。
- **O271-03** [The spherical magnetization law for the three-dimensional quantum Heisenberg ferromagnet](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-spherical-magnetization-law-for-the-three-dimensional-quantum-Heisenberg-ferromagnet-October-5-2026/spherical-magnetization.pdf)。形式化目录：未列入。BibTeX 键：`OAI:The-spherical-magnetization-law-for-the-three-dimensional-quantum-Heisenberg-ferromagnet-October-5-2026`。
- **O271-04** [Spontaneous magnetization in the quantum Heisenberg ferromagnet](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Spontaneous-magnetization-in-the-quantum-Heisenberg-ferromagnet-September-24-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Spontaneous-magnetization-in-the-quantum-Heisenberg-ferromagnet-September-24-2026`。

<a id="family-272"></a>

## 272｜有纠缠却提不出密钥：量子资源之间不是一回事

- **O272-01** [Entanglement with zero distillable secret key in local dimension ten](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Entanglement-with-zero-distillable-secret-key-in-local-dimension-ten-September-27-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Entanglement-with-zero-distillable-secret-key-in-local-dimension-ten-September-27-2026`。

<a id="family-273"></a>

## 273｜熵光子数不等式：两束量子光混合后最少有多混乱

- **O273-01** [The entropy photon-number inequality](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-entropy-photon-number-inequality-September-24-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:The-entropy-photon-number-inequality-September-24-2026`。

<a id="family-274"></a>

## 274｜常数深度量子电路不能算奇偶性：浅电路的能力边界

- **O274-01** [Product-projection localization and the QAC⁰ parity lower bound](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Product-projection-localization-and-the-QAC0-parity-lower-bound-September-24-2026/paper.pdf)。形式化目录：已列入。BibTeX 键：`OAI:Product-projection-localization-and-the-QAC0-parity-lower-bound-September-24-2026`。
- **O274-02** [Regular trajectories, pruning and quantum parity](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Regular-trajectories-pruning-and-quantum-parity-September-24-2026/paper.pdf)。形式化目录：已列入。BibTeX 键：`OAI:Regular-trajectories-pruning-and-quantum-parity-September-24-2026`。

<a id="family-275"></a>

## 275｜连续库仑电子问题的 QMA 困难性：困难确实来自物理模型本身

- **O275-01** [Continuum Coulomb hardness with binary nuclear charges](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Continuum-Coulomb-hardness-with-binary-nuclear-charges-September-24-2026/Continuum-Coulomb-hardness-with-binary-nuclear-charges-September-24-2026.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Continuum-Coulomb-hardness-with-binary-nuclear-charges-September-24-2026`。
- **O275-02** [QMA-hardness of continuum Coulomb energy with unit nuclear charges](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/QMA-hardness-of-continuum-Coulomb-energy-with-unit-nuclear-charges-September-24-2026/QMA-hardness-of-continuum-Coulomb-energy-with-unit-nuclear-charges-September-24-2026.pdf)。形式化目录：未列入。BibTeX 键：`OAI:QMA-hardness-of-continuum-Coulomb-energy-with-unit-nuclear-charges-September-24-2026`。

<a id="family-276"></a>

## 276｜广义振幅阻尼信道：热噪声下一个量子比特能传多少经典信息

- **O276-01** [Classical capacity and entropy inequalities for generalized amplitude damping](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Classical-capacity-and-entropy-inequalities-for-generalized-amplitude-damping-September-24-2026/paper.pdf)。形式化目录：已列入。BibTeX 键：`OAI:Classical-capacity-and-entropy-inequalities-for-generalized-amplitude-damping-September-24-2026`。

<a id="family-277"></a>

## 277｜纠缠博弈的阈值重复：量子相关不能无限规避统计放大

- **O277-01** [Threshold parallel repetition for finite-dimensional entangled games](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Threshold-parallel-repetition-for-finite-dimensional-entangled-games-September-25-2026/paper.pdf)。形式化目录：已列入。BibTeX 键：`OAI:Threshold-parallel-repetition-for-finite-dimensional-entangled-games-September-25-2026`。

<a id="family-278"></a>

## 278｜Kohn–Sham 系综表象的反例：相同密度未必来自一个独立粒子势

- **O278-01** [A Coulomb ground-state density without Kohn–Sham ensemble representation](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/A-Coulomb-Ground-State-Density-without-Kohn-Sham-Ensemble-Representation-September-25-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:A-Coulomb-Ground-State-Density-without-Kohn-Sham-Ensemble-Representation-September-25-2026`。

<a id="family-279"></a>

## 279｜固定有限门集的精确量子分解：把成功概率提高到严格的一

- **O279-01** [Exact quantum factoring over a fixed finite gate set](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Exact-quantum-factoring-over-a-fixed-finite-gate-set-September-25-2026/main.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Exact-quantum-factoring-over-a-fixed-finite-gate-set-September-25-2026`。

<a id="family-280"></a>

## 280｜顶点算符代数与共形网：两种共形场论语言何时等价

- **O280-01** [Strongly rational unitary vertex operator algebras and conformal nets](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Strongly-rational-unitary-vertex-operator-algebras-and-conformal-nets-September-25-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Strongly-rational-unitary-vertex-operator-algebras-and-conformal-nets-September-25-2026`。

<a id="family-281"></a>

## 281｜QAOA 达到 SK 基态能量：量子变分电路能否追上自旋玻璃极值

- **O281-01** [QAOA attains the SK ground-state energy in the thermodynamic-first limit](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/QAOA-attains-the-SK-ground-state-energy-in-the-thermodynamic-first-limit-September-25-2026/QAOA-attains-the-SK-ground-state-energy-in-the-thermodynamic-first-limit-September-25-2026.pdf)。形式化目录：未列入。BibTeX 键：`OAI:QAOA-attains-the-SK-ground-state-energy-in-the-thermodynamic-first-limit-September-25-2026`。
- **O281-02** [Full support of the zero-temperature Sherrington–Kirkpatrick order parameter](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Full-support-of-the-zero-temperature-Sherrington-Kirkpatrick-order-parameter-September-27-2026/main.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Full-support-of-the-zero-temperature-Sherrington-Kirkpatrick-order-parameter-September-27-2026`。

<a id="family-282"></a>

## 282｜四维尺度对称能否增强为共形对称

- **O282-01** [Scale and conformal symmetry in four-dimensional operational quantum field theory](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Scale-and-conformal-symmetry-in-four-dimensional-operational-quantum-field-theory-September-26-2026/main.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Scale-and-conformal-symmetry-in-four-dimensional-operational-quantum-field-theory-September-26-2026`。

<a id="family-283"></a>

## 283｜用布尔预言机合成任意幺正：把量子操作编码成经典查询

- **O283-01** [Polynomial-Time Unitary Synthesis from a Boolean Oracle](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/Polynomial-Time-Unitary-Synthesis-from-a-Boolean-Oracle-October-5-2026/paper.pdf)。形式化目录：未列入。BibTeX 键：`OAI:Polynomial-Time-Unitary-Synthesis-from-a-Boolean-Oracle-October-5-2026`。

<a id="family-284"></a>

## 284｜经典随机与量子查询的最优幂次：总布尔函数可有近四次优势

- **O284-01** [A Nearly Quartic Separation Between Randomized and Quantum Query Complexity](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/A-Nearly-Quartic-Separation-Between-Randomized-and-Quantum-Query-Complexity-October-5-2026/quartic-query-separation.pdf)。形式化目录：未列入。BibTeX 键：`OAI:A-Nearly-Quartic-Separation-Between-Randomized-and-Quantum-Query-Complexity-October-5-2026`。

## 正文采用的历史来源链接

以下链接均在正文中与对应论点相邻。以摘要／书目信息为主的核对不代表全文审稿。

- **Background:0705-2024** Hastings, M. B.（2007）。[An Area Law for One Dimensional Quantum Systems](https://arxiv.org/abs/0705.2024)。历史背景；核对论文页面、摘要及书目信息。
- **Background:0710-5666** Guha, Saikat, Erkmen, Baris I., Shapiro, Jeffrey H.（2007）。[The Entropy Photon-Number Inequality and its Consequences](https://arxiv.org/abs/0710.5666)。历史背景；核对论文页面、摘要及书目信息。
- **Background:0712-0483** Schuch, Norbert, Verstraete, Frank（2007）。[Computational Complexity of interacting electrons and fundamental limitations of Density Functional Theory](https://arxiv.org/abs/0712.0483)。历史背景；核对论文页面、摘要及书目信息。
- **Background:0906-5566** Mars, Marc（2009）。[Present status of the Penrose inequality](https://arxiv.org/abs/0906.5566)。历史背景；核对论文页面、摘要及书目信息。
- **Background:1103-1025** Raynal, Philippe, Lü, Xin, Englert, Berthold-Georg（2011）。[Mutually unbiased bases in dimension six: The four most distant bases](https://arxiv.org/abs/1103.1025)。历史背景；核对论文页面、摘要及书目信息。
- **Background:1201-0640** Jaming, Philippe, Matolcsi, Mate, Mora, Peter（2012）。[The problem of mutually unbiased bases in dimension 6](https://arxiv.org/abs/1201.0640)。历史背景；核对论文页面、摘要及书目信息。
- **Background:1309-2921** Dymarsky, Anatoly, Komargodski, Zohar, Schwimmer, Adam, Theisen, Stefan（2013）。[On Scale and Conformal Invariance in Four Dimensions](https://arxiv.org/abs/1309.2921)。历史背景；核对论文页面、摘要及书目信息。
- **Background:1402-6322** Dymarsky, Anatoly, Farnsworth, Kara, Komargodski, Zohar, Luty, Markus A., Prilepina, Valentina（2014）。[Scale Invariance, Conformality, and Generalized Free Fields](https://arxiv.org/abs/1402.6322)。历史背景；核对论文页面、摘要及书目信息。
- **Background:1404-4717** Correggi, Michele, Giuliani, Alessandro, Seiringer, Robert（2014）。[Validity of spin wave theory for the quantum Heisenberg model](https://arxiv.org/abs/1404.4717)。历史背景；核对论文页面、摘要及书目信息。
- **Background:1503-01260** Carpi, Sebastiano, Kawahigashi, Yasuyuki, Longo, Roberto, Weiner, Mihály（2015）。[From vertex operator algebras to conformal nets and back](https://arxiv.org/abs/1503.01260)。历史背景；核对论文页面、摘要及书目信息。
- **Background:1604-04340** Yuen, Henry（2016）。[A parallel repetition theorem for all entangled games](https://arxiv.org/abs/1604.04340)。历史背景；核对论文页面、摘要及书目信息。
- **Background:1710-01722** Dafermos, Mihalis, Luk, Jonathan（2017）。[The interior of dynamical vacuum black holes I: The $C^0$-stability of the Kerr Cauchy horizon](https://arxiv.org/abs/1710.01722)。历史背景；核对论文页面、摘要及书目信息。
- **Background:1903-07747** Khatri, Sumeet, Sharma, Kunal, Wilde, Mark M.（2019）。[Information-theoretic aspects of the generalized amplitude damping channel](https://arxiv.org/abs/1903.07747)。历史背景；核对论文页面、摘要及书目信息。
- **Background:1910-08187** Farhi, Edward, Goldstone, Jeffrey, Gutmann, Sam, Zhou, Leo（2019）。[The Quantum Approximate Optimization Algorithm and the Sherrington-Kirkpatrick Model at Infinite Size](https://arxiv.org/abs/1910.08187)。历史背景；核对论文页面、摘要及书目信息。
- **Background:2007-09326** Frank, Rupert L.（2020）。[The Lieb-Thirring inequalities: Recent results and open problems](https://arxiv.org/abs/2007.09326)。历史背景；核对论文页面、摘要及书目信息。
- **Background:2010-12629** Aaronson, Scott, Ben-David, Shalev, Kothari, Robin, Rao, Shravas, Tal, Avishay（2020）。[Degree vs. Approximate Degree and Quantum Implications of Huang's Sensitivity Theorem](https://arxiv.org/abs/2010.12629)。历史背景；核对论文页面、摘要及书目信息。
- **Background:2110-14206** Basso, Joao, Farhi, Edward, Marwaha, Kunal, Villalonga, Benjamin, Zhou, Leo（2021）。[The Quantum Approximate Optimization Algorithm at High Depth for MaxCut on Large-Girth Regular Graphs and the Sherrington-Kirkpatrick Model](https://arxiv.org/abs/2110.14206)。历史背景；核对论文页面、摘要及书目信息。
- **Background:2310-08870** Lombardi, Alex, Ma, Fermi, Wright, John（2023）。[A one-query lower bound for unitary synthesis and breaking quantum cryptography](https://arxiv.org/abs/2310.08870)。历史背景；核对论文页面、摘要及书目信息。
- **Background:2410-06499** Anshu, Anurag, Dong, Yangjing, Ou, Fengning, Yao, Penghui（2024）。[On the Computational Power of QAC0 with Barely Superlinear Ancillae](https://arxiv.org/abs/2410.06499)。历史背景；核对论文页面、摘要及书目信息。
- **Background:2411-00976** Montanaro, Ashley, Shao, Changpeng, Verdon, Dominic（2024）。[Low-degree approximation of QAC$^0$ circuits](https://arxiv.org/abs/2411.00976)。已撤稿；仅作为版本核验案例。
- **Background:gr-qc-0312047** Bray, Hubert L., Chrusciel, Piotr T.（2003）。[The Penrose Inequality](https://arxiv.org/abs/gr-qc/0312047)。历史背景；核对论文页面、摘要及书目信息。
- **Background:hep-th-9610043** Banks, T., Fischler, W., Shenker, S. H., Susskind, L.（1996）。[M Theory As A Matrix Model: A Conjecture](https://arxiv.org/abs/hep-th/9610043)。历史背景；核对论文页面、摘要及书目信息。
- **Background:math-ph-0012026** Solovej, Jan Philip（2000）。[The Ionization Conjecture in Hartree-Fock Theory](https://arxiv.org/abs/math-ph/0012026)。历史背景；核对论文页面、摘要及书目信息。
- **Background:math-ph-0112032** Lieb, Elliott H., Seiringer, Robert（2001）。[Proof of Bose-Einstein Condensation for Dilute Trapped Gases](https://arxiv.org/abs/math-ph/0112032)。历史背景；核对论文页面、摘要及书目信息。
- **Background:quant-ph-0309110** Horodecki, Karol, Horodecki, Michal, Horodecki, Pawel, Oppenheim, Jonathan（2003）。[Secure key from bound entanglement](https://arxiv.org/abs/quant-ph/0309110)。历史背景；核对论文页面、摘要及书目信息。
- **Background:quant-ph-9508027** Shor, Peter W.（1995）。[Polynomial-Time Algorithms for Prime Factorization and Discrete Logarithms on a Quantum Computer](https://arxiv.org/abs/quant-ph/9508027)。历史背景；核对论文页面、摘要及书目信息。
- **Background:10-1103-PhysRev-109-1492** P. W. Anderson（1958）。[Absence of Diffusion in Certain Random Lattices](https://doi.org/10.1103/PhysRev.109.1492)。历史背景；核对论文页面、摘要及书目信息。
- **Background:10-1103-PhysRev-140-A1133** W. Kohn, L. J. Sham（1965）。[Self-Consistent Equations Including Exchange and Correlation Effects](https://doi.org/10.1103/PhysRev.140.A1133)。历史背景；核对论文页面、摘要及书目信息。
- **Background:10-1103-PhysRevLett-42-673** E. Abrahams, P. W. Anderson, D. C. Licciardello, T. V. Ramakrishnan（1979）。[Scaling Theory of Localization: Absence of Quantum Diffusion in Two Dimensions](https://doi.org/10.1103/PhysRevLett.42.673)。历史背景；核对论文页面、摘要及书目信息。
- **Background:10-1103-PhysRevLett-50-1153** F. D. M. Haldane（1983）。[Nonlinear Field Theory of Large-Spin Heisenberg Antiferromagnets: Semiclassically Quantized Solitons of the One-Dimensional Easy-Axis Neel State](https://doi.org/10.1103/PhysRevLett.50.1153)。历史背景；核对论文页面、摘要及书目信息。
- **Background:10-1103-PhysRevLett-50-1395** R. B. Laughlin（1983）。[Anomalous Quantum Hall Effect: An Incompressible Quantum Fluid with Fractionally Charged Excitations](https://doi.org/10.1103/PhysRevLett.50.1395)。历史背景；核对论文页面、摘要及书目信息。
- **Background:10-1103-PhysRevLett-51-605** F. D. M. Haldane（1983）。[Fractional Quantization of the Hall Effect: A Hierarchy of Incompressible Quantum Fluid States](https://doi.org/10.1103/PhysRevLett.51.605)。历史背景；核对论文页面、摘要及书目信息。

[返回总览](README.md)
