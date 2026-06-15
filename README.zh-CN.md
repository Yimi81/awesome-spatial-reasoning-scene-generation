# Awesome Spatial Reasoning and Scene Generation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> 空间推理、空间智能、可控 3D 场景生成与世界生成相关论文、数据集、评测基准和系统的精选列表。

**语言:** [English](README.md) | 中文

当一个系统需要维护物体、几何、关系、约束、可供性和反馈等结构化状态，并把这些状态实现为自洽的 3D 场景、仿真器或具身环境时，空间推理与场景生成就汇合在一起。

## 目录

- [综述与路线图](#综述与路线图)
- [空间推理与认知地图](#空间推理与认知地图)
- [基准与评测](#基准与评测)
- [室内场景合成与布局](#室内场景合成与布局)
- [Agentic 与代码驱动场景生成](#agentic-与代码驱动场景生成)
- [世界生成与世界模型](#世界生成与世界模型)
- [具身环境与机器人](#具身环境与机器人)
- [工具与资产生态](#工具与资产生态)

本列表最初由父目录中的本地笔记和论文资料整理而来。种子分类法和待验证条目见[来源笔记](docs/source-notes.zh-CN.md)。

## 综述与路线图

| Title                                                                                                                                   | Year | Venue                   | 摘要                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------- | ---- | ----------------------- | ------------------------------------------------------ |
| [Spatial Intelligence from a Cognitive Map Perspective: A Survey](https://github.com/Klingsor-tyx/Awesome-Spatial-Cognitive-Map#readme) | 2026 | Preprint / Awesome list | 从认知地图的构建、推理和实现三个过程组织空间智能研究。 |

## 空间推理与认知地图

| Title                                                        | Year | Venue  | 摘要                                                 |
| ------------------------------------------------------------ | ---- | ------ | ---------------------------------------------------- |
| [Visual Spatial Reasoning](https://arxiv.org/abs/2205.00363) | 2023 | arXiv  | 研究自然图像中的空间关系验证问题。                   |
| [LayoutGPT](https://arxiv.org/abs/2305.15393)                | 2023 | arXiv  | 使用 LLM 进行组合式视觉规划和布局生成。              |
| [InstructScene](https://arxiv.org/abs/2402.04717)            | 2024 | arXiv  | 结合语义图先验，从指令生成 3D 室内场景。             |
| [RelScene](https://doi.org/10.1145/3664647.3681653)          | 2024 | ACM MM | 面向文本驱动 3D 场景生成中的空间关系建立基准和评测。 |
| [VULCAN](https://arxiv.org/abs/2512.22351)                   | 2026 | arXiv  | 通过工具增强的多智能体迭代进行 3D 物体摆放。         |

## 基准与评测

| Title                                                                                                                       | Year | Venue | 摘要                                 |
| --------------------------------------------------------------------------------------------------------------------------- | ---- | ----- | ------------------------------------ |
| [WorldScore](https://arxiv.org/abs/2504.00983)                                                                              | 2025 | arXiv | 提供面向世界生成的统一评测基准。     |
| [WorldLens](https://arxiv.org/abs/2512.10958)                                                                               | 2025 | arXiv | 从真实世界维度全面评测驾驶世界模型。 |
| [Benchmarking and Learning Multi-Dimensional Quality Evaluator for Text-to-3D Generation](https://arxiv.org/abs/2412.11170) | 2025 | arXiv | 研究文本到 3D 生成的多维质量评估器。 |

## 室内场景合成与布局

| Title                                                                                                                                                                           | Year | Venue    | 摘要                                             |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | -------- | ------------------------------------------------ |
| [GRAINS](https://arxiv.org/abs/1807.09193)                                                                                                                                      | 2019 | arXiv    | 使用生成式递归自编码器建模室内场景。             |
| [PlanIT](https://doi.org/10.1145/3306346.3322941)                                                                                                                               | 2019 | SIGGRAPH | 结合关系图和空间先验，规划并实例化室内场景。     |
| [ATISS](https://arxiv.org/abs/2110.03675)                                                                                                                                       | 2021 | NeurIPS  | 将自回归 Transformer 用于室内场景合成。          |
| [Text2Room](https://arxiv.org/abs/2303.11989)                                                                                                                                   | 2023 | ICCV     | 从 2D 文生图模型中提取带纹理的 3D 房间网格。     |
| [CommonScenes](https://arxiv.org/abs/2305.16283)                                                                                                                                | 2023 | arXiv    | 使用场景图扩散生成符合常识的 3D 室内场景。       |
| [SceneWiz3D](https://arxiv.org/abs/2312.08885)                                                                                                                                  | 2023 | arXiv    | 探索文本引导的 3D 场景组合。                     |
| [AnyHome](https://arxiv.org/abs/2312.06644)                                                                                                                                     | 2024 | arXiv    | 面向开放词汇生成结构化且带纹理的 3D 家居场景。   |
| [DiffuScene](https://openaccess.thecvf.com/content/CVPR2024/html/Tang_DiffuScene_Denoising_Diffusion_Models_for_Generative_Indoor_Scene_Synthesis_CVPR_2024_paper.html)         | 2024 | CVPR     | 使用去噪扩散模型进行生成式室内场景合成。         |
| [ArtiScene](https://arxiv.org/abs/2506.00742)                                                                                                                                   | 2025 | arXiv    | 通过图像中介生成语言驱动的艺术化 3D 场景。       |
| [SceneFactor](https://openaccess.thecvf.com/content/CVPR2025/html/Bokhovkin_SceneFactor_Factored_Latent_3D_Diffusion_for_Controllable_3D_Scene_Generation_CVPR_2025_paper.html) | 2025 | CVPR     | 使用因子化 latent 3D 扩散实现可控场景生成。      |
| [AnchoredDream](https://arxiv.org/abs/2601.16532)                                                                                                                               | 2026 | arXiv    | 通过几何 grounding 从单视角生成 360 度室内场景。 |
| [Text-Image Conditioned 3D Generation](https://arxiv.org/abs/2603.21295)                                                                                                        | 2026 | arXiv    | 同时使用文本和图像条件进行 3D 生成。             |

## Agentic 与代码驱动场景生成

| Title                                                        | Year | Venue        | 摘要                                                 |
| ------------------------------------------------------------ | ---- | ------------ | ---------------------------------------------------- |
| [Holodeck](https://arxiv.org/abs/2312.09067)                 | 2024 | CVPR         | 从语言生成 3D 具身 AI 环境。                         |
| [SceneCraft](https://arxiv.org/abs/2403.01248)               | 2024 | arXiv        | 使用 LLM agent 将 3D 场景合成为 Blender 代码。       |
| [EnvGen](https://arxiv.org/abs/2403.12014)                   | 2024 | arXiv        | 通过 LLM 生成和改造具身智能体训练环境。              |
| [SceneGenAgent](https://arxiv.org/abs/2410.21909)            | 2025 | arXiv        | 使用 coding agent 生成精确工业场景。                 |
| [UnrealLLM](https://aclanthology.org/2025.findings-acl.994/) | 2025 | ACL Findings | 将 LLM 驱动的程序化内容生成连接到可控 UE5 场景生成。 |
| [WorldCraft](https://arxiv.org/abs/2502.15601)               | 2025 | arXiv        | 使用 LLM agents 创建和定制照片级 3D 世界。           |
| [3Dify](https://arxiv.org/abs/2510.04536)                    | 2025 | arXiv        | 结合 LLM、MCP 和 RAG 构建程序化 3D-CG 生成流程。     |
| [SAGE](https://arxiv.org/abs/2602.10116)                     | 2026 | arXiv        | 面向具身 AI 扩展 agentic 3D 场景生成。               |
| [SceneSmith](https://arxiv.org/abs/2602.09153)               | 2026 | arXiv        | 使用 agentic 流程生成可用于仿真的室内场景。          |
| [Code2Worlds](https://arxiv.org/abs/2602.11757)              | 2026 | arXiv        | 赋能 coding LLM 进行 4D 世界生成。                   |
| [AutoUE](https://arxiv.org/abs/2603.07106)                   | 2026 | arXiv        | 通过多智能体系统自动生成 Unreal Engine 3D 游戏。     |
| [SimWorld Studio](https://arxiv.org/abs/2605.09423)          | 2026 | arXiv        | 使用自进化 coding agent 生成可演化的具身学习环境。   |

## 世界生成与世界模型

| Title                                                                                                                  | Year | Venue           | 摘要                                            |
| ---------------------------------------------------------------------------------------------------------------------- | ---- | --------------- | ----------------------------------------------- |
| [SceneScape](https://arxiv.org/abs/2302.01133)                                                                         | 2023 | arXiv           | 生成一致的文本驱动场景。                        |
| [Learning Interactive Real-World Simulators](https://arxiv.org/abs/2310.06114)                                         | 2023 | arXiv           | 研究可交互真实世界动态的学习型仿真器。          |
| [LucidDreamer](https://arxiv.org/abs/2311.13384)                                                                       | 2023 | arXiv           | 生成不受领域约束的 3D Gaussian Splatting 场景。 |
| [WonderJourney](https://arxiv.org/abs/2312.03884)                                                                      | 2024 | arXiv           | 从任意起点扩展到更大范围的场景和世界。          |
| [Video Generation Models as World Simulators](https://openai.com/research/video-generation-models-as-world-simulators) | 2024 | OpenAI Research | 将视频生成视为通向世界模拟的一条路线。          |
| [Genie](https://arxiv.org/abs/2402.15391)                                                                              | 2024 | ICML            | 学习生成式可交互环境。                          |
| [WonderWorld](https://arxiv.org/abs/2406.09394)                                                                        | 2025 | arXiv           | 支持从单张图像进行交互式 3D 场景生成。          |
| [Cosmos World Foundation Model Platform](https://arxiv.org/abs/2501.03575)                                             | 2025 | arXiv           | 为 physical AI 提供世界基础模型平台。           |
| [WorldGen](https://github.com/ZiYang-xie/WorldGen#readme)                                                              | 2025 | GitHub          | 在数秒内生成 3D 场景。                          |
| [Agent-World](https://arxiv.org/abs/2604.18292)                                                                        | 2026 | arXiv           | 合成真实世界环境以促进通用智能体演化。          |

## 具身环境与机器人

| Title                                                   | Year | Venue    | 摘要                                                 |
| ------------------------------------------------------- | ---- | -------- | ---------------------------------------------------- |
| [AI2-THOR](https://ai2thor.allenai.org/)                | 2017 | Platform | 为具身 AI 提供可交互 3D 环境。                       |
| [CARLA](https://carla.org/)                             | 2017 | CoRL     | 提供自动驾驶研究开放仿真器。                         |
| [Habitat](https://aihabitat.org/)                       | 2019 | ICCV     | 为具身 AI 提供仿真基础设施。                         |
| [iGibson](https://github.com/StanfordVL/iGibson#readme) | 2021 | IROS     | 为具身智能体提供交互式仿真环境。                     |
| [RoboTHOR](https://arxiv.org/abs/2004.06799)            | 2020 | arXiv    | 连接仿真与真实机器人具身 AI 评测。                   |
| [MetaUrban](https://arxiv.org/abs/2407.08725)           | 2024 | arXiv    | 为城市微出行构建具身 AI 仿真平台。                   |
| [LEGENT](https://aclanthology.org/2024.acl-demos.32/)   | 2024 | ACL Demo | 提供开放的具身智能体平台。                           |
| [UnrealZoo](https://arxiv.org/abs/2412.20977)           | 2025 | arXiv    | 丰富用于具身 AI 的照片级虚拟世界。                   |
| [VirtualEnv](https://arxiv.org/abs/2601.07553)          | 2026 | arXiv    | 提供具身 AI 研究平台。                               |
| [MolmoSpaces](https://arxiv.org/abs/2602.11337)         | 2026 | arXiv    | 提供大规模开放机器人导航与操作生态。                 |
| [SimWorld-Robotics](https://arxiv.org/abs/2512.10046)   | 2026 | arXiv    | 合成照片级动态城市环境，用于多模态机器人导航与协作。 |

## 工具与资产生态

| Title                                                                        | Year | Venue    | 摘要                                            |
| ---------------------------------------------------------------------------- | ---- | -------- | ----------------------------------------------- |
| [UnrealCV](https://doi.org/10.1145/3123266.3129396)                          | 2017 | ACM MM   | 将 Unreal Engine 虚拟世界接入计算机视觉工作流。 |
| [ThreeDWorld](https://github.com/threedworld-mit/tdw#readme)                 | 2020 | Platform | 提供可交互、多模态、物理仿真的平台。            |
| [Infinigen](https://arxiv.org/abs/2306.09310)                                | 2023 | CVPR     | 通过程序化生成构建无限照片级世界。              |
| [MolmoSpaces Code and Assets](https://github.com/allenai/molmospaces#readme) | 2026 | GitHub   | 提供机器人仿真的开放资产、场景和工具。          |

## 相关列表

- [Awesome Embodied AI](https://github.com/haoranD/Awesome-Embodied-AI#readme) - 具身 AI 论文、任务和平台列表。
- [Awesome 3D Generation](https://github.com/justimyhxu/awesome-3D-generation#readme) - 3D 生成论文和资源列表。

## 贡献

欢迎贡献。提交 PR 前请阅读 [CONTRIBUTING.md](CONTRIBUTING.md)。
