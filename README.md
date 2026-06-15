# Awesome Spatial Reasoning and Simulation-Ready Scene Generation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Curated papers, datasets, benchmarks, and systems for spatial perception,
> spatial reasoning, planning-oriented simulation, controllable scene generation,
> and embodied 3D environments.

**Languages:** English | [中文](README.zh-CN.md)

This list is about **spatial intelligence for usable worlds**, not just pretty
renders. It prioritizes work that builds or uses structured spatial state:
objects, geometry, relations, affordances, constraints, physics, tasks, actions,
and feedback loops.

The working lens is functional: renderers produce observations, simulators
maintain and roll forward world state, and planners choose actions over that
state. This repo primarily tracks the simulator/planner side of spatial
intelligence: work that can support action, task execution, validation,
counterfactual editing, data generation, or robot policy learning.

**Scope:** spatial perception, cognitive maps, 3D scene graphs, object-centric
memory, spatial reasoning, layout planning, controllable scene generation,
simulation-ready environments, embodied tasks, and robot policy data engines.

**High priority:** methods that expose editable objects, metric or relational
state, collision/support/clearance constraints, physical attributes,
simulator-in-the-loop validation, or planning interfaces.

**Lower priority:** renderer-only world models, text-to-video systems, NeRFs, or
Gaussian-splatting worlds that do not expose manipulable objects, physical state,
planning affordances, or simulation transfer.

## Contents

- [Surveys and Roadmaps](#surveys-and-roadmaps)
- [Spatial Perception and Representations](#spatial-perception-and-representations)
- [Spatial Reasoning and Planning](#spatial-reasoning-and-planning)
- [Benchmarks and Evaluation](#benchmarks-and-evaluation)
- [Symbolic and Procedural Scene Generation](#symbolic-and-procedural-scene-generation)
- [3D Data-Driven Scene Generation](#3d-data-driven-scene-generation)
- [LLM and VFM Static Scene Pipelines](#llm-and-vfm-static-scene-pipelines)
- [Agent-Based Scene Generation and Simulation Loops](#agent-based-scene-generation-and-simulation-loops)
- [Embodied Simulation and Robot Learning](#embodied-simulation-and-robot-learning)
- [Tools, Assets, and Physics Engines](#tools-assets-and-physics-engines)

## Surveys and Roadmaps

| Title                                                                                                                                   | Year | Venue                   | Desc                                                                                         |
| --------------------------------------------------------------------------------------------------------------------------------------- | ---- | ----------------------- | -------------------------------------------------------------------------------------------- |
| [Spatial Intelligence from a Cognitive Map Perspective: A Survey](https://github.com/Klingsor-tyx/Awesome-Spatial-Cognitive-Map#readme) | 2026 | Preprint / Awesome list | Organizes spatial intelligence as cognitive-map construction, reasoning, and generation.     |
| [World-Model Functional Taxonomy](https://x.com/drfeifei/status/2062247238143996275)                                                    | 2026 | X / Blog                | Separates visual rendering from stateful simulation and planning for action-capable worlds.  |
| [Aligning Cyber Space with Physical World: A Comprehensive Survey on Embodied AI](https://arxiv.org/abs/2407.06886)                     | 2025 | arXiv                   | Surveys embodied AI across perception, action, simulation, and cyber-physical alignment.     |
| [A Survey of Self-Evolving Agents](https://arxiv.org/abs/2507.21046)                                                                    | 2025 | arXiv                   | Reviews self-improvement loops that are increasingly used in agentic environment generation. |

## Spatial Perception and Representations

| Title                                             | Year | Venue   | Desc                                                                                         |
| ------------------------------------------------- | ---- | ------- | -------------------------------------------------------------------------------------------- |
| [OpenScene](https://arxiv.org/abs/2211.15654)     | 2023 | CVPR    | Learns open-vocabulary 3D point features aligned with image and text embeddings.             |
| [CLIP-Fields](https://arxiv.org/abs/2210.05663)   | 2023 | RSS     | Builds semantic robot memory by mapping 3D locations to language-aligned features.           |
| [VLMaps](https://arxiv.org/abs/2210.05714)        | 2023 | ICRA    | Fuses visual-language features with 3D maps for language-indexed robot navigation.           |
| [OpenMask3D](https://arxiv.org/abs/2306.13631)    | 2023 | NeurIPS | Performs open-vocabulary 3D instance segmentation with multi-view CLIP features.             |
| [ConceptGraphs](https://arxiv.org/abs/2309.16650) | 2024 | ICRA    | Builds open-vocabulary 3D scene graphs for perception, memory, and planning.                 |
| [SpatialVLM](https://arxiv.org/abs/2401.12168)    | 2024 | CVPR    | Trains VLMs with spatial reasoning data for metric distance, size, and relation reasoning.   |
| [SceneGraphLoc](https://arxiv.org/abs/2404.00469) | 2024 | ECCV    | Localizes images against object-level multimodal 3D scene graphs.                            |
| [LERF](https://arxiv.org/abs/2303.09553)          | 2023 | ICCV    | Embeds open-vocabulary language features in radiance fields for 3D localization and queries. |

## Spatial Reasoning and Planning

| Title                                                        | Year | Venue | Desc                                                                                   |
| ------------------------------------------------------------ | ---- | ----- | -------------------------------------------------------------------------------------- |
| [Visual Spatial Reasoning](https://arxiv.org/abs/2205.00363) | 2023 | arXiv | Studies visual recognition of spatial relations in natural images.                     |
| [SayPlan](https://arxiv.org/abs/2307.06135)                  | 2023 | CoRL  | Grounds LLM planning in large 3D scene graphs for multi-room robot tasks.              |
| [cuRobo](https://arxiv.org/abs/2310.17274)                   | 2023 | arXiv | Provides parallelized collision-free robot motion generation for simulation pipelines. |
| [M2T2](https://arxiv.org/abs/2311.00926)                     | 2023 | arXiv | Uses an object-centric transformer for pick-and-place grasp and placement reasoning.   |

## Benchmarks and Evaluation

| Title                                                                                                                       | Year | Venue  | Desc                                                                                      |
| --------------------------------------------------------------------------------------------------------------------------- | ---- | ------ | ----------------------------------------------------------------------------------------- |
| [RelScene](https://doi.org/10.1145/3664647.3681653)                                                                         | 2024 | ACM MM | Benchmarks spatial relations in text-driven 3D scene generation.                          |
| [WorldScore](https://arxiv.org/abs/2504.00983)                                                                              | 2025 | arXiv  | Evaluates world generation with explicit camera-trajectory layout specifications.         |
| [SceneEval](https://arxiv.org/abs/2503.14756)                                                                               | 2026 | WACV   | Evaluates semantic coherence and implicit plausibility in text-conditioned indoor scenes. |
| [Spatial-DISE](https://arxiv.org/abs/2510.13394)                                                                            | 2026 | ICLR   | Evaluates intrinsic/extrinsic and static/dynamic spatial reasoning in VLMs.               |
| [SpatialBench](https://arxiv.org/abs/2511.21471)                                                                            | 2025 | arXiv  | Benchmarks multimodal spatial cognition from observation to planning.                     |
| [Benchmarking and Learning Multi-Dimensional Quality Evaluator for Text-to-3D Generation](https://arxiv.org/abs/2412.11170) | 2025 | arXiv  | Studies multi-dimensional quality evaluation for text-to-3D generation.                   |

## Symbolic and Procedural Scene Generation

Rule-based and procedural methods are useful baselines because they expose
geometry and structure, but they often trade away open-vocabulary flexibility
and adaptive self-correction.

| Title                                                                                                  | Year | Venue    | Desc                                                                                  |
| ------------------------------------------------------------------------------------------------------ | ---- | -------- | ------------------------------------------------------------------------------------- |
| [WordsEye](https://doi.org/10.1145/383259.383316)                                                      | 2001 | SIGGRAPH | Early text-to-scene system using symbolic language-to-3D conversion.                  |
| [Learning Spatial Knowledge for Text to 3D Scene Generation](https://aclanthology.org/D14-1217/)       | 2014 | EMNLP    | Learns spatial knowledge for placing objects in language-driven 3D scenes.            |
| [Language-Driven Synthesis of 3D Scenes from Scene Databases](https://doi.org/10.1145/3272127.3275025) | 2018 | TOG      | Synthesizes 3D scenes from natural language using scene database priors.              |
| [PlanIT](https://doi.org/10.1145/3306346.3322941)                                                      | 2019 | SIGGRAPH | Plans and instantiates indoor scenes with relation graphs and spatial prior networks. |
| [ProcTHOR](https://arxiv.org/abs/2206.06994)                                                           | 2022 | NeurIPS  | Procedurally generates large-scale embodied AI environments.                          |
| [Infinigen Indoors](https://arxiv.org/abs/2406.11824)                                                  | 2024 | CVPR     | Procedurally generates photorealistic indoor scenes.                                  |

## 3D Data-Driven Scene Generation

Data-driven scene generators learn spatial priors from existing 3D scenes,
layouts, floor plans, scene graphs, or object distributions.

| Title                                                                                                                                                                           | Year | Venue    | Desc                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | -------- | ---------------------------------------------------------------------------------- |
| [GRAINS](https://arxiv.org/abs/1807.09193)                                                                                                                                      | 2019 | SIGGRAPH | Uses recursive generative models for indoor scene structure.                       |
| [ATISS](https://arxiv.org/abs/2110.03675)                                                                                                                                       | 2021 | NeurIPS  | Applies autoregressive transformers to indoor scene synthesis.                     |
| [Text2Room](https://arxiv.org/abs/2303.11989)                                                                                                                                   | 2023 | ICCV     | Extracts textured 3D room meshes from text-to-image priors.                        |
| [CommonScenes](https://arxiv.org/abs/2305.16283)                                                                                                                                | 2023 | NeurIPS  | Generates commonsense 3D indoor scenes with scene graph diffusion.                 |
| [DiffuScene](https://openaccess.thecvf.com/content/CVPR2024/html/Tang_DiffuScene_Denoising_Diffusion_Models_for_Generative_Indoor_Scene_Synthesis_CVPR_2024_paper.html)         | 2024 | CVPR     | Uses diffusion models for generative indoor scene synthesis.                       |
| [PhyScene](https://openaccess.thecvf.com/content/CVPR2024/html/Yang_PhyScene_Physically_Interactable_3D_Scene_Synthesis_for_Embodied_AI_CVPR_2024_paper.html)                   | 2024 | CVPR     | Generates physically interactable 3D scenes for embodied AI.                       |
| [EchoScene](https://www.ecva.net/papers/eccv_2024/papers_ECCV/papers/03146.pdf)                                                                                                 | 2024 | ECCV     | Improves scene graph diffusion through information echo over generated structures. |
| [GraphDreamer](https://openaccess.thecvf.com/content/CVPR2024/html/Gao_GraphDreamer_Compositional_3D_Scene_Synthesis_from_Scene_Graphs_CVPR_2024_paper.html)                    | 2024 | CVPR     | Generates compositional 3D scenes from explicit scene graphs.                      |
| [SceneFactor](https://openaccess.thecvf.com/content/CVPR2025/html/Bokhovkin_SceneFactor_Factored_Latent_3D_Diffusion_for_Controllable_3D_Scene_Generation_CVPR_2025_paper.html) | 2025 | CVPR     | Uses factored latent 3D diffusion for controllable scene generation.               |

## LLM and VFM Static Scene Pipelines

These methods use LLMs, VLMs, image generators, or code generation to produce
scenes, but typically follow a fixed pipeline or provide limited iterative
simulation feedback.

| Title                                                                                                                                                                      | Year | Venue        | Desc                                                                                         |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------ | -------------------------------------------------------------------------------------------- |
| [LayoutGPT](https://arxiv.org/abs/2305.15393)                                                                                                                              | 2023 | NeurIPS      | Uses LLMs for compositional visual planning and 3D layout generation.                        |
| [3D-GPT](https://arxiv.org/abs/2310.12945)                                                                                                                                 | 2023 | arXiv        | Uses LLMs for procedural 3D modeling and scene construction.                                 |
| [Holodeck](https://arxiv.org/abs/2312.09067)                                                                                                                               | 2024 | CVPR         | Uses LLMs to generate 3D embodied AI environments from language.                             |
| [AnyHome](https://arxiv.org/abs/2312.06644)                                                                                                                                | 2024 | ECCV         | Generates structured and textured 3D homes with open-vocabulary prompts.                     |
| [Open-Universe Indoor Scene Generation](https://arxiv.org/abs/2403.09675)                                                                                                  | 2024 | arXiv        | Uses LLM program synthesis and uncurated object databases for open-universe indoor scenes.   |
| [I-Design](https://doi.org/10.1007/978-3-031-73036-8_13)                                                                                                                   | 2024 | ECCV         | Uses LLMs as personalized interior designers for layout and furnishing.                      |
| [SceneTeller](https://doi.org/10.1007/978-3-031-72658-3_21)                                                                                                                | 2024 | ECCV         | Converts language into 3D scene generation plans.                                            |
| [Architect](https://arxiv.org/abs/2411.09823)                                                                                                                              | 2024 | NeurIPS      | Generates interactive 3D scenes with hierarchical 2D inpainting and lifting.                 |
| [GenUSD](https://doi.org/10.1145/3641520.3665306)                                                                                                                          | 2024 | SIGGRAPH RTL | Generates 3D scenes in Universal Scene Description workflows.                                |
| [LayoutVLM](https://openaccess.thecvf.com/content/CVPR2025/html/Sun_LayoutVLM_Differentiable_Optimization_of_3D_Layout_via_Vision-Language_Models_CVPR_2025_paper.html)    | 2025 | CVPR         | Optimizes 3D layouts with VLM-derived objectives and physically grounded semantic alignment. |
| [ArtiScene](https://openaccess.thecvf.com/content/CVPR2025/html/Gu_ArtiScene_Language-Driven_Artistic_3D_Scene_Generation_Through_Image_Intermediary_CVPR_2025_paper.html) | 2025 | CVPR         | Uses generated 2D images as intermediaries for language-driven 3D scene generation.          |
| [Hierarchically-Structured Open-Vocabulary Indoor Scene Synthesis](https://ojs.aaai.org/index.php/AAAI/article/view/32874)                                                 | 2025 | AAAI         | Uses pretrained LLMs for hierarchical open-vocabulary indoor scene synthesis.                |
| [Scene Language](https://openaccess.thecvf.com/content/CVPR2025/html/Zhang_The_Scene_Language_Representing_Scenes_with_Programs_Words_and_Embeddings_CVPR_2025_paper.html) | 2025 | CVPR         | Represents scenes with programs, words, and embeddings for controllable generation.          |
| [Scenethesis](https://arxiv.org/abs/2505.02836)                                                                                                                            | 2025 | arXiv        | Combines LLM planning with vision-guided spatial refinement for 3D scene generation.         |
| [Holodeck 2.0](https://arxiv.org/abs/2508.05899)                                                                                                                           | 2026 | CVPR         | Uses VLM-guided decomposition, generated 3D assets, spatial constraints, and editing.        |

## Agent-Based Scene Generation and Simulation Loops

Agent-based methods emphasize tool use, feedback, self-improvement, or
simulator-in-the-loop validation. The stronger entries in this section move from
plausible scenes toward deployable environments for embodied AI.

| Title                                                        | Year | Venue        | Desc                                                                                     |
| ------------------------------------------------------------ | ---- | ------------ | ---------------------------------------------------------------------------------------- |
| [SceneCraft](https://arxiv.org/abs/2403.01248)               | 2024 | arXiv        | Uses an LLM agent to synthesize 3D scenes as Blender code.                               |
| [EnvGen](https://arxiv.org/abs/2403.12014)                   | 2024 | arXiv        | Generates and adapts environments via LLMs for embodied agent training.                  |
| [WorldCraft](https://arxiv.org/abs/2502.15601)               | 2025 | arXiv        | Creates and customizes photorealistic 3D worlds with LLM agents.                         |
| [SceneGenAgent](https://arxiv.org/abs/2410.21909)            | 2025 | arXiv        | Uses a coding agent for precise industrial scene generation.                             |
| [SceneWeaver](https://arxiv.org/abs/2509.20414)              | 2025 | arXiv        | Uses an extensible self-reflective agent to refine scenes through tool-based feedback.   |
| [UnrealLLM](https://aclanthology.org/2025.findings-acl.994/) | 2025 | ACL Findings | Connects LLM-powered procedural content generation to controllable UE5 scene generation. |
| [VULCAN](https://arxiv.org/abs/2512.22351)                   | 2026 | arXiv        | Uses tool-augmented multi-agent iteration for relation-aware 3D object arrangement.      |
| [SAGE](https://arxiv.org/abs/2602.10116)                     | 2026 | arXiv        | Generates simulator-validated 3D environments with visual and physics critics.           |
| [SimWorld Studio](https://arxiv.org/abs/2605.09423)          | 2026 | arXiv        | Generates evolving Gym-style embodied environments with a self-evolving coding agent.    |
| [Code2Worlds](https://arxiv.org/abs/2602.11757)              | 2026 | arXiv        | Uses coding LLMs for 4D world generation.                                                |
| [AutoUE](https://arxiv.org/abs/2603.07106)                   | 2026 | arXiv        | Automates Unreal Engine 3D game generation with multi-agent systems.                     |

## Embodied Simulation and Robot Learning

| Title                                                                                                                          | Year | Venue    | Desc                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------ | ---- | -------- | ------------------------------------------------------------------------------------------------------- |
| [AI2-THOR](https://arxiv.org/abs/1712.05474)                                                                                   | 2017 | arXiv    | Provides interactive 3D indoor environments for visual and embodied AI.                                 |
| [VirtualHome](https://openaccess.thecvf.com/content_cvpr_2018/html/Puig_VirtualHome_Simulating_Household_CVPR_2018_paper.html) | 2018 | CVPR     | Simulates household activities as programs in 3D home environments.                                     |
| [Habitat](https://aihabitat.org/)                                                                                              | 2019 | ICCV     | Provides simulation infrastructure for embodied AI research.                                            |
| [ThreeDWorld](https://github.com/threedworld-mit/tdw#readme)                                                                   | 2020 | arXiv    | Provides interactive multimodal physical simulation.                                                    |
| [iGibson 2.0](https://arxiv.org/abs/2108.03272)                                                                                | 2021 | arXiv    | Provides object-centric simulation for everyday household robot tasks.                                  |
| [CALVIN](https://ieeexplore.ieee.org/document/9762919)                                                                         | 2022 | RA-L     | Benchmarks language-conditioned long-horizon robot manipulation.                                        |
| [BEHAVIOR-1K](https://arxiv.org/abs/2403.09227)                                                                                | 2023 | CoRL     | Defines 1,000 everyday embodied activities in realistic simulated scenes.                               |
| [LIBERO](https://arxiv.org/abs/2306.03310)                                                                                     | 2023 | NeurIPS  | Benchmarks knowledge transfer for lifelong robot learning.                                              |
| [RoboGen](https://arxiv.org/abs/2311.01455)                                                                                    | 2024 | ICML     | Uses generative simulation to create tasks, scenes, and supervision for robot learning.                 |
| [ManiSkill3](https://arxiv.org/abs/2410.00425)                                                                                 | 2024 | arXiv    | Provides GPU-parallelized robotics simulation and rendering for generalizable embodied AI.              |
| [RoboCasa](https://arxiv.org/abs/2406.02523)                                                                                   | 2024 | arXiv    | Scales realistic household simulation for everyday generalist robot tasks.                              |
| [MetaUrban](https://arxiv.org/abs/2407.08725)                                                                                  | 2024 | arXiv    | Simulates urban micromobility for embodied AI.                                                          |
| [LEGENT](https://aclanthology.org/2024.acl-demos.32/)                                                                          | 2024 | ACL Demo | Provides an open platform for embodied agents and data generation.                                      |
| [RoboVerse](https://arxiv.org/abs/2504.18904)                                                                                  | 2025 | arXiv    | Unifies platform, dataset, and benchmarks for scalable robot learning.                                  |
| [UnrealZoo](https://arxiv.org/abs/2412.20977)                                                                                  | 2025 | arXiv    | Enriches photorealistic virtual worlds for embodied AI.                                                 |
| [VirtualEnv](https://arxiv.org/abs/2601.07553)                                                                                 | 2026 | arXiv    | Provides a platform for embodied AI research.                                                           |
| [MolmoSpaces](https://arxiv.org/abs/2602.11337)                                                                                | 2026 | arXiv    | Provides large-scale simulator-agnostic environments and objects for robot navigation and manipulation. |
| [SimWorld-Robotics](https://arxiv.org/abs/2512.10046)                                                                          | 2026 | arXiv    | Synthesizes photorealistic dynamic urban environments for multimodal robot navigation.                  |

## Tools, Assets, and Physics Engines

| Title                                                                                                                                           | Year | Venue    | Desc                                                                             |
| ----------------------------------------------------------------------------------------------------------------------------------------------- | ---- | -------- | -------------------------------------------------------------------------------- |
| [MuJoCo](https://doi.org/10.1109/IROS.2012.6386109)                                                                                             | 2012 | IROS     | Physics engine for model-based control and robot simulation.                     |
| [PyBullet](https://pybullet.org/wordpress/)                                                                                                     | 2016 | Software | Python physics simulation module for robotics, games, and machine learning.      |
| [UnrealCV](https://doi.org/10.1145/3123266.3129396)                                                                                             | 2017 | ACM MM   | Connects Unreal Engine virtual worlds to computer vision workflows.              |
| [SAPIEN](https://openaccess.thecvf.com/content_CVPR_2020/html/Xiang_SAPIEN_A_Simulated_Part-Based_Interactive_Environment_CVPR_2020_paper.html) | 2020 | CVPR     | Simulates articulated objects and part-based interaction.                        |
| [PartNet-Mobility](https://arxiv.org/abs/2003.08515)                                                                                            | 2020 | arXiv    | Provides articulated objects with motion annotations for interaction simulation. |
| [Objaverse](https://arxiv.org/abs/2212.08051)                                                                                                   | 2023 | CVPR     | Large annotated 3D object dataset used by many scene-generation pipelines.       |
| [Objaverse-XL](https://arxiv.org/abs/2307.05663)                                                                                                | 2023 | NeurIPS  | Expands Objaverse to 10M+ 3D objects.                                            |
| [Isaac Lab / Orbit](https://arxiv.org/abs/2301.04195)                                                                                           | 2023 | RA-L     | Unified framework for interactive robot learning environments.                   |
| [Genesis](https://github.com/Genesis-Embodied-AI/Genesis#readme)                                                                                | 2024 | GitHub   | Generative and universal physics engine for robotics and beyond.                 |
| [TRELLIS](https://arxiv.org/abs/2412.01506)                                                                                                     | 2025 | CVPR     | Generates structured 3D latents for scalable and versatile 3D asset generation.  |
| [Objaverse++](https://arxiv.org/abs/2504.07334)                                                                                                 | 2025 | arXiv    | Curates 3D objects with quality annotations for asset selection.                 |
| [Hunyuan3D 2.1](https://arxiv.org/abs/2506.15442)                                                                                               | 2025 | arXiv    | Generates high-fidelity 3D assets with production-ready PBR materials.           |
| [NVIDIA Isaac Sim](https://github.com/isaac-sim/IsaacSim#readme)                                                                                | 2025 | Software | Simulation platform for physically grounded robotics scenes and data generation. |

## Related Lists

- [Awesome Spatial Cognitive Map](https://github.com/Klingsor-tyx/Awesome-Spatial-Cognitive-Map) - Related list for cognitive-map-based spatial intelligence.
- [Awesome Embodied AI](https://github.com/haoranD/Awesome-Embodied-AI#readme) - Related list for embodied AI papers, tasks, and platforms.
- [Awesome 3D Generation](https://github.com/justimyhxu/awesome-3D-generation#readme) - Related list for 3D generation papers and resources.

## Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md)
before opening a pull request.
