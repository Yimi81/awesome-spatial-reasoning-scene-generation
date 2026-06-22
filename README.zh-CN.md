# Awesome Spatial Reasoning and Simulation-Ready Scene Generation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> 空间感知、空间推理、面向规划的仿真、可控场景生成，以及具身 3D 环境相关论文、数据集、基准和系统精选列表。

**语言:** [English](README.md) | 中文

这个列表关注的是**能用于行动和规划的空间智能**，而不只是好看的渲染结果。它优先收录能够构建或使用结构化空间状态的工作：物体、几何、关系、可供性、约束、物理属性、任务、动作和反馈循环。

这里采用一个功能性筛选视角：renderer 生成观测，simulator 维护并推进世界状态，planner 在该状态上选择动作。本仓库主要关注 spatial intelligence 中偏 simulator/planner 的工作：能够支持行动、任务执行、验证、反事实编辑、数据生成或机器人策略学习的方向。

**收录范围:** 空间感知、认知地图、3D 场景图、object-centric memory、空间推理、布局规划、可控场景生成、仿真就绪环境、具身任务和机器人策略数据引擎。

**高优先级:** 输出可编辑物体、metric/relational state、碰撞/支撑/clearance 约束、物理属性、仿真器闭环验证或规划接口的工作。

**低优先级:** 只生成视频、NeRF、Gaussian Splatting 或视觉渲染结果，但不暴露可操作物体、物理状态、规划 affordance 或 sim-to-real 迁移路径的世界模型。

## 目录

- [综述与路线图](#综述与路线图)
- [空间感知与表征](#空间感知与表征)
- [空间推理与规划](#空间推理与规划)
- [基准与评测](#基准与评测)
- [符号式与程序化场景生成](#符号式与程序化场景生成)
- [3D 数据驱动场景生成](#3d-数据驱动场景生成)
- [LLM 与 VFM 静态场景生成流水线](#llm-与-vfm-静态场景生成流水线)
- [Agent-Based 场景生成与仿真循环](#agent-based-场景生成与仿真循环)
- [具身仿真与机器人学习](#具身仿真与机器人学习)
- [工具、资产与物理引擎](#工具资产与物理引擎)

## 综述与路线图

| Title                                                                                                                                   | Year | Venue                   | 摘要                                                       |
| --------------------------------------------------------------------------------------------------------------------------------------- | ---- | ----------------------- | ---------------------------------------------------------- |
| [Spatial Intelligence from a Cognitive Map Perspective: A Survey](https://github.com/Klingsor-tyx/Awesome-Spatial-Cognitive-Map#readme) | 2026 | Preprint / Awesome list | 从认知地图的构建、推理和生成三个过程组织空间智能研究。     |
| [World-Model Functional Taxonomy](https://x.com/drfeifei/status/2062247238143996275)                                                    | 2026 | X / Blog                | 区分视觉渲染、状态仿真和面向行动世界的规划。               |
| [Amara Whitepaper](https://docsend.com/view/a4bz2ffc35gqaqru)                                                                           | 2026 | [01C](https://01c.ai/)  | 将场景生成定义为结构化空间状态、约束和几何感知规划问题。   |
| [Aligning Cyber Space with Physical World: A Comprehensive Survey on Embodied AI](https://arxiv.org/abs/2407.06886)                     | 2025 | arXiv                   | 综述具身 AI 中的感知、行动、仿真和物理世界对齐问题。       |
| [A Survey of Self-Evolving Agents](https://arxiv.org/abs/2507.21046)                                                                    | 2025 | arXiv                   | 梳理自改进 agent 循环，这类机制正被用于 agentic 环境生成。 |

## 空间感知与表征

| Title                                             | Year | Venue   | 摘要                                                     |
| ------------------------------------------------- | ---- | ------- | -------------------------------------------------------- |
| [OpenScene](https://arxiv.org/abs/2211.15654)     | 2023 | CVPR    | 学习与图像和文本嵌入对齐的开放词表 3D 点特征。           |
| [CLIP-Fields](https://arxiv.org/abs/2210.05663)   | 2023 | RSS     | 将 3D 位置映射到语言对齐特征，构建语义机器人记忆。       |
| [VLMaps](https://arxiv.org/abs/2210.05714)        | 2023 | ICRA    | 将视觉语言特征融合进 3D 地图，用于语言索引的机器人导航。 |
| [OpenMask3D](https://arxiv.org/abs/2306.13631)    | 2023 | NeurIPS | 基于多视角 CLIP 特征进行开放词表 3D 实例分割。           |
| [ConceptGraphs](https://arxiv.org/abs/2309.16650) | 2024 | ICRA    | 构建开放词表 3D 场景图，用于感知、记忆和规划。           |
| [SpatialVLM](https://arxiv.org/abs/2401.12168)    | 2024 | CVPR    | 用空间推理数据训练 VLM，支持距离、尺寸和关系推理。       |
| [SceneGraphLoc](https://arxiv.org/abs/2404.00469) | 2024 | ECCV    | 将图像定位到由物体级多模态 3D 场景图表示的参考地图中。   |
| [LERF](https://arxiv.org/abs/2303.09553)          | 2023 | ICCV    | 在辐射场中嵌入开放词表语言特征，支持 3D 查询和定位。     |

## 空间推理与规划

| Title                                                        | Year | Venue | 摘要                                                           |
| ------------------------------------------------------------ | ---- | ----- | -------------------------------------------------------------- |
| [Visual Spatial Reasoning](https://arxiv.org/abs/2205.00363) | 2023 | arXiv | 研究自然图像中的视觉空间关系识别。                             |
| [SayPlan](https://arxiv.org/abs/2307.06135)                  | 2023 | CoRL  | 将 LLM 规划 grounding 到大型 3D 场景图，用于多房间机器人任务。 |
| [cuRobo](https://arxiv.org/abs/2310.17274)                   | 2023 | arXiv | 提供并行化、无碰撞、最小 jerk 的机器人运动生成。               |
| [M2T2](https://arxiv.org/abs/2311.00926)                     | 2023 | arXiv | 使用 object-centric transformer 进行抓取与放置推理。           |
| [S-Agent](https://arxiv.org/abs/2606.20515)                  | 2026 | arXiv | 使用层级空间工具和记忆机制进行多视角/视频空间推理。           |

## 基准与评测

| Title                                                                                                                       | Year | Venue  | 摘要                                                           |
| --------------------------------------------------------------------------------------------------------------------------- | ---- | ------ | -------------------------------------------------------------- |
| [RelScene](https://doi.org/10.1145/3664647.3681653)                                                                         | 2024 | ACM MM | 评测文本驱动 3D 场景生成中的空间关系。                         |
| [WorldScore](https://arxiv.org/abs/2504.00983)                                                                              | 2025 | arXiv  | 用显式相机轨迹布局规范评估世界生成。                           |
| [SceneEval](https://arxiv.org/abs/2503.14756)                                                                               | 2026 | WACV   | 评估文本条件室内场景的语义一致性和隐式合理性。                 |
| [Spatial-DISE](https://arxiv.org/abs/2510.13394)                                                                            | 2026 | ICLR   | 评测 VLM 中 intrinsic/extrinsic、static/dynamic 空间推理能力。 |
| [SpatialBench](https://arxiv.org/abs/2511.21471)                                                                            | 2025 | arXiv  | 从观察到规划评测多模态空间认知。                               |
| [Benchmarking and Learning Multi-Dimensional Quality Evaluator for Text-to-3D Generation](https://arxiv.org/abs/2412.11170) | 2025 | arXiv  | 研究 text-to-3D 生成的多维质量评估器。                         |

## 符号式与程序化场景生成

规则和程序化方法通常能暴露几何与结构，是重要基线；但它们往往牺牲开放词表灵活性和自适应自修正能力。

| Title                                                                                                  | Year | Venue    | 摘要                                           |
| ------------------------------------------------------------------------------------------------------ | ---- | -------- | ---------------------------------------------- |
| [WordsEye](https://doi.org/10.1145/383259.383316)                                                      | 2001 | SIGGRAPH | 早期文本到场景系统，使用符号式语言到 3D 转换。 |
| [Learning Spatial Knowledge for Text to 3D Scene Generation](https://aclanthology.org/D14-1217/)       | 2014 | EMNLP    | 学习语言驱动 3D 场景中的物体空间摆放知识。     |
| [Language-Driven Synthesis of 3D Scenes from Scene Databases](https://doi.org/10.1145/3272127.3275025) | 2018 | TOG      | 利用场景数据库先验从自然语言合成 3D 场景。     |
| [PlanIT](https://doi.org/10.1145/3306346.3322941)                                                      | 2019 | SIGGRAPH | 结合关系图和空间先验网络规划并实例化室内场景。 |
| [ProcTHOR](https://arxiv.org/abs/2206.06994)                                                           | 2022 | NeurIPS  | 程序化生成大规模具身 AI 环境。                 |
| [Infinigen Indoors](https://arxiv.org/abs/2406.11824)                                                  | 2024 | CVPR     | 程序化生成照片级室内场景。                     |

## 3D 数据驱动场景生成

数据驱动场景生成方法从已有 3D 场景、布局、平面图、场景图或物体分布中学习空间先验。

| Title                                                                                                                                                                           | Year | Venue    | 摘要                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | -------- | ----------------------------------------------------- |
| [GRAINS](https://arxiv.org/abs/1807.09193)                                                                                                                                      | 2019 | SIGGRAPH | 使用递归生成模型建模室内场景结构。                    |
| [ATISS](https://arxiv.org/abs/2110.03675)                                                                                                                                       | 2021 | NeurIPS  | 将自回归 Transformer 用于室内场景合成。               |
| [Text2Room](https://arxiv.org/abs/2303.11989)                                                                                                                                   | 2023 | ICCV     | 从 text-to-image 先验中提取带纹理的 3D 房间 mesh。    |
| [CommonScenes](https://arxiv.org/abs/2305.16283)                                                                                                                                | 2023 | NeurIPS  | 使用场景图扩散生成具备常识的 3D 室内场景。            |
| [DiffuScene](https://openaccess.thecvf.com/content/CVPR2024/html/Tang_DiffuScene_Denoising_Diffusion_Models_for_Generative_Indoor_Scene_Synthesis_CVPR_2024_paper.html)         | 2024 | CVPR     | 使用扩散模型进行室内场景生成。                        |
| [PhyScene](https://openaccess.thecvf.com/content/CVPR2024/html/Yang_PhyScene_Physically_Interactable_3D_Scene_Synthesis_for_Embodied_AI_CVPR_2024_paper.html)                   | 2024 | CVPR     | 生成可物理交互的 3D 场景，用于具身 AI。               |
| [EchoScene](https://www.ecva.net/papers/eccv_2024/papers_ECCV/papers/03146.pdf)                                                                                                 | 2024 | ECCV     | 通过 scene graph diffusion 中的信息回声改进场景生成。 |
| [GraphDreamer](https://openaccess.thecvf.com/content/CVPR2024/html/Gao_GraphDreamer_Compositional_3D_Scene_Synthesis_from_Scene_Graphs_CVPR_2024_paper.html)                    | 2024 | CVPR     | 从显式场景图生成组合式 3D 场景。                      |
| [SceneFactor](https://openaccess.thecvf.com/content/CVPR2025/html/Bokhovkin_SceneFactor_Factored_Latent_3D_Diffusion_for_Controllable_3D_Scene_Generation_CVPR_2025_paper.html) | 2025 | CVPR     | 使用因子化 latent 3D 扩散进行可控场景生成。           |

## LLM 与 VFM 静态场景生成流水线

这些方法使用 LLM、VLM、图像生成器或代码生成来产生场景，但通常遵循固定流水线，或者只提供有限的迭代式仿真反馈。

| Title                                                                                                                                                                      | Year | Venue        | 摘要                                                             |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------ | ---------------------------------------------------------------- |
| [LayoutGPT](https://arxiv.org/abs/2305.15393)                                                                                                                              | 2023 | NeurIPS      | 使用 LLM 进行组合式视觉规划和 3D 布局生成。                      |
| [3D-GPT](https://arxiv.org/abs/2310.12945)                                                                                                                                 | 2023 | arXiv        | 使用 LLM 进行程序化 3D 建模和场景构建。                          |
| [Holodeck](https://arxiv.org/abs/2312.09067)                                                                                                                               | 2024 | CVPR         | 使用 LLM 从语言生成 3D 具身 AI 环境。                            |
| [AnyHome](https://arxiv.org/abs/2312.06644)                                                                                                                                | 2024 | ECCV         | 生成开放词表、结构化、带纹理的 3D 家居场景。                     |
| [Open-Universe Indoor Scene Generation](https://arxiv.org/abs/2403.09675)                                                                                                  | 2024 | arXiv        | 使用 LLM 程序合成和未整理物体数据库生成开放室内场景。            |
| [I-Design](https://doi.org/10.1007/978-3-031-73036-8_13)                                                                                                                   | 2024 | ECCV         | 使用 LLM 作为个性化室内设计师。                                  |
| [SceneTeller](https://doi.org/10.1007/978-3-031-72658-3_21)                                                                                                                | 2024 | ECCV         | 将语言转换为 3D 场景生成计划。                                   |
| [Architect](https://arxiv.org/abs/2411.09823)                                                                                                                              | 2024 | NeurIPS      | 通过层级 2D inpainting 与提升生成可交互 3D 场景。                |
| [GenUSD](https://doi.org/10.1145/3641520.3665306)                                                                                                                          | 2024 | SIGGRAPH RTL | 在 Universal Scene Description 工作流中生成 3D 场景。            |
| [LayoutVLM](https://openaccess.thecvf.com/content/CVPR2025/html/Sun_LayoutVLM_Differentiable_Optimization_of_3D_Layout_via_Vision-Language_Models_CVPR_2025_paper.html)    | 2025 | CVPR         | 使用 VLM 派生目标优化 3D 布局，并评估物理 grounding 的语义对齐。 |
| [ArtiScene](https://openaccess.thecvf.com/content/CVPR2025/html/Gu_ArtiScene_Language-Driven_Artistic_3D_Scene_Generation_Through_Image_Intermediary_CVPR_2025_paper.html) | 2025 | CVPR         | 以生成的 2D 图像为中间表示，进行语言驱动 3D 场景生成。           |
| [Hierarchically-Structured Open-Vocabulary Indoor Scene Synthesis](https://ojs.aaai.org/index.php/AAAI/article/view/32874)                                                 | 2025 | AAAI         | 使用预训练 LLM 进行层级化开放词表室内场景合成。                  |
| [Scene Language](https://openaccess.thecvf.com/content/CVPR2025/html/Zhang_The_Scene_Language_Representing_Scenes_with_Programs_Words_and_Embeddings_CVPR_2025_paper.html) | 2025 | CVPR         | 用程序、词和 embedding 表示场景，支持可控生成。                  |
| [Scenethesis](https://arxiv.org/abs/2505.02836)                                                                                                                            | 2025 | arXiv        | 结合 LLM 规划与视觉引导空间优化生成 3D 场景。                    |
| [Holodeck 2.0](https://arxiv.org/abs/2508.05899)                                                                                                                           | 2026 | CVPR         | 使用 VLM 场景分解、生成式 3D 资产、空间约束和交互编辑生成世界。  |

## Agent-Based 场景生成与仿真循环

Agent-based 方法强调工具使用、反馈、自改进或仿真器闭环验证。本节中更强的条目从“语义上合理的场景”推进到可供具身 AI 使用的可部署环境。

| Title                                                        | Year | Venue        | 摘要                                                    |
| ------------------------------------------------------------ | ---- | ------------ | ------------------------------------------------------- |
| [SceneCraft](https://arxiv.org/abs/2403.01248)               | 2024 | arXiv        | 使用 LLM agent 将 3D 场景合成为 Blender 代码。          |
| [EnvGen](https://arxiv.org/abs/2403.12014)                   | 2024 | arXiv        | 使用 LLM 生成并适配具身 agent 训练环境。                |
| [WorldCraft](https://arxiv.org/abs/2502.15601)               | 2025 | arXiv        | 使用 LLM agents 创建和定制照片级 3D 世界。              |
| [SceneGenAgent](https://arxiv.org/abs/2410.21909)            | 2025 | arXiv        | 使用 coding agent 生成精确工业场景。                    |
| [SceneWeaver](https://arxiv.org/abs/2509.20414)              | 2025 | arXiv        | 使用可扩展、自反思 agent，通过工具反馈迭代优化场景。    |
| [UnrealLLM](https://aclanthology.org/2025.findings-acl.994/) | 2025 | ACL Findings | 将 LLM 驱动的程序化内容生成连接到可控 UE5 场景生成。    |
| [VULCAN](https://arxiv.org/abs/2512.22351)                   | 2026 | arXiv        | 使用工具增强多智能体迭代进行关系感知的 3D 物体摆放。    |
| [SAGE](https://arxiv.org/abs/2602.10116)                     | 2026 | arXiv        | 使用视觉和物理 critics 生成经过仿真器验证的 3D 环境。   |
| [SimWorld Studio](https://arxiv.org/abs/2605.09423)          | 2026 | arXiv        | 使用自进化 coding agent 生成可演化的 Gym 风格具身环境。 |
| [Code2Worlds](https://arxiv.org/abs/2602.11757)              | 2026 | arXiv        | 使用 coding LLM 进行 4D 世界生成。                      |
| [AutoUE](https://arxiv.org/abs/2603.07106)                   | 2026 | arXiv        | 通过多智能体系统自动生成 Unreal Engine 3D 游戏。        |

## 具身仿真与机器人学习

| Title                                                                                                                          | Year | Venue    | 摘要                                                     |
| ------------------------------------------------------------------------------------------------------------------------------ | ---- | -------- | -------------------------------------------------------- |
| [AI2-THOR](https://arxiv.org/abs/1712.05474)                                                                                   | 2017 | arXiv    | 为视觉和具身 AI 提供交互式 3D 室内环境。                 |
| [VirtualHome](https://openaccess.thecvf.com/content_cvpr_2018/html/Puig_VirtualHome_Simulating_Household_CVPR_2018_paper.html) | 2018 | CVPR     | 将家庭活动以程序形式在 3D 家庭环境中仿真。               |
| [Habitat](https://aihabitat.org/)                                                                                              | 2019 | ICCV     | 为具身 AI 研究提供仿真基础设施。                         |
| [ThreeDWorld](https://github.com/threedworld-mit/tdw#readme)                                                                   | 2020 | arXiv    | 提供可交互、多模态的物理仿真。                           |
| [iGibson 2.0](https://arxiv.org/abs/2108.03272)                                                                                | 2021 | arXiv    | 为日常家庭机器人任务提供 object-centric 仿真。           |
| [CALVIN](https://ieeexplore.ieee.org/document/9762919)                                                                         | 2022 | RA-L     | 评测语言条件长时程机器人操作。                           |
| [BEHAVIOR-1K](https://arxiv.org/abs/2403.09227)                                                                                | 2023 | CoRL     | 在真实感仿真场景中定义 1,000 个日常具身活动。            |
| [LIBERO](https://arxiv.org/abs/2306.03310)                                                                                     | 2023 | NeurIPS  | 评测终身机器人学习中的知识迁移。                         |
| [RoboGen](https://arxiv.org/abs/2311.01455)                                                                                    | 2024 | ICML     | 用生成式仿真创建任务、场景和监督信号来训练机器人。       |
| [ManiSkill3](https://arxiv.org/abs/2410.00425)                                                                                 | 2024 | arXiv    | 提供 GPU 并行机器人仿真与渲染，用于泛化具身 AI。         |
| [RoboCasa](https://arxiv.org/abs/2406.02523)                                                                                   | 2024 | arXiv    | 扩展真实感家庭仿真，用于日常通用机器人任务。             |
| [MetaUrban](https://arxiv.org/abs/2407.08725)                                                                                  | 2024 | arXiv    | 为城市微出行构建具身 AI 仿真平台。                       |
| [LEGENT](https://aclanthology.org/2024.acl-demos.32/)                                                                          | 2024 | ACL Demo | 提供开放的具身 agent 平台和数据生成管线。                |
| [RoboVerse](https://arxiv.org/abs/2504.18904)                                                                                  | 2025 | arXiv    | 统一平台、数据集和基准，支持可扩展机器人学习。           |
| [UnrealZoo](https://arxiv.org/abs/2412.20977)                                                                                  | 2025 | arXiv    | 丰富用于具身 AI 的照片级虚拟世界。                       |
| [VirtualEnv](https://arxiv.org/abs/2601.07553)                                                                                 | 2026 | arXiv    | 提供具身 AI 研究平台。                                   |
| [MolmoSpaces](https://arxiv.org/abs/2602.11337)                                                                                | 2026 | arXiv    | 提供大规模、仿真器无关的机器人导航和操作环境与物体资产。 |
| [SimWorld-Robotics](https://arxiv.org/abs/2512.10046)                                                                          | 2026 | arXiv    | 合成照片级动态城市环境，用于多模态机器人导航。           |

## 工具、资产与物理引擎

| Title                                                                                                                                           | Year | Venue    | 摘要                                                      |
| ----------------------------------------------------------------------------------------------------------------------------------------------- | ---- | -------- | --------------------------------------------------------- |
| [MuJoCo](https://doi.org/10.1109/IROS.2012.6386109)                                                                                             | 2012 | IROS     | 用于 model-based control 和机器人仿真的物理引擎。         |
| [PyBullet](https://pybullet.org/wordpress/)                                                                                                     | 2016 | Software | 用于机器人、游戏和机器学习的 Python 物理仿真模块。        |
| [UnrealCV](https://doi.org/10.1145/3123266.3129396)                                                                                             | 2017 | ACM MM   | 将 Unreal Engine 虚拟世界接入计算机视觉工作流。           |
| [SAPIEN](https://openaccess.thecvf.com/content_CVPR_2020/html/Xiang_SAPIEN_A_Simulated_Part-Based_Interactive_Environment_CVPR_2020_paper.html) | 2020 | CVPR     | 支持 articulated objects 和 part-based interaction 仿真。 |
| [PartNet-Mobility](https://arxiv.org/abs/2003.08515)                                                                                            | 2020 | arXiv    | 提供带运动标注的 articulated objects，用于交互仿真。      |
| [Objaverse](https://arxiv.org/abs/2212.08051)                                                                                                   | 2023 | CVPR     | 大规模带标注 3D 物体数据集，被大量场景生成管线使用。      |
| [Objaverse-XL](https://arxiv.org/abs/2307.05663)                                                                                                | 2023 | NeurIPS  | 将 Objaverse 扩展到 1,000 万以上 3D 物体。                |
| [Isaac Lab / Orbit](https://arxiv.org/abs/2301.04195)                                                                                           | 2023 | RA-L     | 面向交互式机器人学习环境的统一框架。                      |
| [Genesis](https://github.com/Genesis-Embodied-AI/Genesis#readme)                                                                                | 2024 | GitHub   | 面向机器人等场景的生成式通用物理引擎。                    |
| [TRELLIS](https://arxiv.org/abs/2412.01506)                                                                                                     | 2025 | CVPR     | 生成结构化 3D latent，用于可扩展 3D 资产生成。            |
| [Objaverse++](https://arxiv.org/abs/2504.07334)                                                                                                 | 2025 | arXiv    | 带质量标注的 curated 3D 物体数据集。                      |
| [Hunyuan3D 2.1](https://arxiv.org/abs/2506.15442)                                                                                               | 2025 | arXiv    | 生成带 production-ready PBR 材质的高保真 3D 资产。        |
| [NVIDIA Isaac Sim](https://github.com/isaac-sim/IsaacSim#readme)                                                                                | 2025 | Software | 用于物理 grounding 机器人场景和数据生成的仿真平台。       |

## 相关列表

- [Awesome Spatial Cognitive Map](https://github.com/Klingsor-tyx/Awesome-Spatial-Cognitive-Map) - 认知地图视角下的空间智能列表。
- [Awesome Embodied AI](https://github.com/haoranD/Awesome-Embodied-AI#readme) - 具身 AI 论文、任务和平台列表。
- [Awesome 3D Generation](https://github.com/justimyhxu/awesome-3D-generation#readme) - 3D 生成论文和资源列表。

## 贡献

欢迎贡献。提交 PR 前请阅读 [CONTRIBUTING.md](CONTRIBUTING.md)。
