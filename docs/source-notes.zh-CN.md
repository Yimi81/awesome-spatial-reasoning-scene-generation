# 来源笔记

**语言:** [English](source-notes.md) | 中文

这些笔记说明初始列表如何从当前工作区的本地材料中整理出来。它们不能替代论文、项目页或仓库等 canonical 链接。

## 标题选择

推荐项目标题是 **Awesome Spatial Reasoning and Scene Generation**。

这个标题比 `awesome-spatial-reason-gen` 更明确：它保留 awesome-list 的命名习惯，同时避免 `gen` 缩写的歧义。"Scene Generation" 也能覆盖室内场景、室外世界、可仿真环境、游戏世界和具身 AI 训练环境。

## 种子来源

- `amara_whitepaper_summary.md`
- `spatial-reason-survey.pdf`
- `simworld-studio.pdf`
- `molmospaces.pdf`
- `Spatial-reason-gen/SimWorld-Studio/references.bib`

## 使用的分类法

初始 README 结构遵循四个相互连接的层次：

- 空间表征与推理：认知地图、object-centric state、场景图、metric map、relational map 和持久空间记忆。
- 评测：空间关系基准、语义一致性指标和世界生成质量评估。
- 可控生成：text-to-scene、graph-to-scene、扩散布局、agentic 场景构建和代码驱动生成。
- 具身环境：为 agent learning 暴露任务、奖励、动作、观测和反馈循环的生成式或高多样性仿真器。

## Amara 白皮书摘要

本地 Amara 摘要将核心问题定义为 reasoning gap，而不是 tooling gap。它给这个 awesome list 提供的筛选标准是：一个工作是否帮助系统通过以下机制维护或生成空间自洽世界：

- 物体位置与包围体。
- 碰撞、支撑、邻接、对齐和 clearance 约束。
- 约束图或结构化空间状态。
- 带语义元数据的资产检索或生成。
- 场景级和物体级 ground truth。
- 能持续改进空间推理或生成场景的反馈循环。

## 空间综述摘要

`spatial-reason-survey.pdf` 中的 "Spatial Intelligence from a Cognitive Map Perspective: A Survey" 从认知地图视角组织空间智能：

- 感知构建内部空间表征。
- 推理在这些表征上进行 inference。
- 生成将这些表征实现为外部空间形式。

README 采用了这一逻辑作为主干。

## SimWorld Studio 摘要

`simworld-studio.pdf` 强调静态场景生成和可部署具身环境生成之间的区别。它给本列表提供的主要纳入标准是：

- 生成场景应当具备物理 grounding。
- 生成世界应当支持任务、奖励、观测和动作。
- Agent 反馈可以引导未来环境生成。
- 验证可以包含规则检查、物理检查和 VLM critique。

## MolmoSpaces 摘要

`molmospaces.pdf` 贡献了本列表的机器人侧视角：

- 大规模场景和物体多样性。
- 丰富的物体元数据和抓取标注。
- 与仿真器无关的环境。
- 支持导航、操作和长时程任务的基准。
- 以 sim-to-real correlation 作为评测信号。

## 待验证条目

以下名称出现在本地笔记或 BibTeX 中，但在提升为 README 正式条目前应补充 canonical 链接：

- Spatial-DISE.
- SpatialBench.
- PLATO.
- SceneEval.
- SenseNova SI.
- Amara.
