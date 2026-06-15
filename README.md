# Awesome Spatial Reasoning and Scene Generation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Curated papers, datasets, benchmarks, and systems for spatial reasoning,
> spatial intelligence, and controllable 3D scene or world generation.

**Languages:** English | [中文](README.zh-CN.md)

Spatial reasoning and scene generation meet when a system must maintain
structured state over objects, geometry, relations, constraints, affordances, and
feedback, then realize that state as a coherent 3D scene, simulator, or embodied
environment.

## Contents

- [Surveys and Roadmaps](#surveys-and-roadmaps)
- [Spatial Reasoning and Cognitive Maps](#spatial-reasoning-and-cognitive-maps)
- [Benchmarks and Evaluation](#benchmarks-and-evaluation)
- [Indoor Scene Synthesis and Layout](#indoor-scene-synthesis-and-layout)
- [Agentic and Code-Based Scene Generation](#agentic-and-code-based-scene-generation)
- [World Generation and World Models](#world-generation-and-world-models)
- [Embodied Environments and Robotics](#embodied-environments-and-robotics)
- [Tools and Asset Ecosystems](#tools-and-asset-ecosystems)

This list was initially seeded from local notes and papers in the parent
workspace. See [source notes](docs/source-notes.md) for the seed taxonomy and
open verification backlog.

## Surveys and Roadmaps

| Title                                                                                                                                   | Year | Venue                   | Desc                                                                                      |
| --------------------------------------------------------------------------------------------------------------------------------------- | ---- | ----------------------- | ----------------------------------------------------------------------------------------- |
| [Spatial Intelligence from a Cognitive Map Perspective: A Survey](https://github.com/Klingsor-tyx/Awesome-Spatial-Cognitive-Map#readme) | 2026 | Preprint / Awesome list | Organizes spatial intelligence as cognitive-map construction, inference, and realization. |

## Spatial Reasoning and Cognitive Maps

| Title                                                        | Year | Venue  | Desc                                                                     |
| ------------------------------------------------------------ | ---- | ------ | ------------------------------------------------------------------------ |
| [Visual Spatial Reasoning](https://arxiv.org/abs/2205.00363) | 2023 | arXiv  | Studies spatial relation verification in natural images.                 |
| [LayoutGPT](https://arxiv.org/abs/2305.15393)                | 2023 | arXiv  | Uses LLMs for compositional visual planning and layout generation.       |
| [InstructScene](https://arxiv.org/abs/2402.04717)            | 2024 | arXiv  | Generates 3D indoor scenes from instructions with semantic graph priors. |
| [RelScene](https://doi.org/10.1145/3664647.3681653)          | 2024 | ACM MM | Benchmarks spatial relations in text-driven 3D scene generation.         |
| [VULCAN](https://arxiv.org/abs/2512.22351)                   | 2026 | arXiv  | Uses tool-augmented multi-agent iteration for 3D object arrangement.     |

## Benchmarks and Evaluation

| Title                                                                                                                       | Year | Venue | Desc                                                          |
| --------------------------------------------------------------------------------------------------------------------------- | ---- | ----- | ------------------------------------------------------------- |
| [WorldScore](https://arxiv.org/abs/2504.00983)                                                                              | 2025 | arXiv | Provides a unified benchmark for evaluating world generation. |
| [WorldLens](https://arxiv.org/abs/2512.10958)                                                                               | 2025 | arXiv | Evaluates driving world models across real-world dimensions.  |
| [Benchmarking and Learning Multi-Dimensional Quality Evaluator for Text-to-3D Generation](https://arxiv.org/abs/2412.11170) | 2025 | arXiv | Studies quality assessment for text-to-3D generation.         |

## Indoor Scene Synthesis and Layout

| Title                                                                                                                                                                           | Year | Venue    | Desc                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | -------- | ---------------------------------------------------------------------------------- |
| [GRAINS](https://arxiv.org/abs/1807.09193)                                                                                                                                      | 2019 | arXiv    | Uses generative recursive autoencoders for indoor scenes.                          |
| [PlanIT](https://doi.org/10.1145/3306346.3322941)                                                                                                                               | 2019 | SIGGRAPH | Plans and instantiates indoor scenes with relation graphs and spatial priors.      |
| [ATISS](https://arxiv.org/abs/2110.03675)                                                                                                                                       | 2021 | NeurIPS  | Applies autoregressive transformers to indoor scene synthesis.                     |
| [Text2Room](https://arxiv.org/abs/2303.11989)                                                                                                                                   | 2023 | ICCV     | Extracts textured 3D room meshes from 2D text-to-image models.                     |
| [CommonScenes](https://arxiv.org/abs/2305.16283)                                                                                                                                | 2023 | arXiv    | Generates commonsense 3D indoor scenes with scene graph diffusion.                 |
| [SceneWiz3D](https://arxiv.org/abs/2312.08885)                                                                                                                                  | 2023 | arXiv    | Moves toward text-guided 3D scene composition.                                     |
| [AnyHome](https://arxiv.org/abs/2312.06644)                                                                                                                                     | 2024 | arXiv    | Generates structured and textured 3D homes with open vocabulary prompts.           |
| [DiffuScene](https://openaccess.thecvf.com/content/CVPR2024/html/Tang_DiffuScene_Denoising_Diffusion_Models_for_Generative_Indoor_Scene_Synthesis_CVPR_2024_paper.html)         | 2024 | CVPR     | Uses denoising diffusion models for generative indoor scene synthesis.             |
| [ArtiScene](https://arxiv.org/abs/2506.00742)                                                                                                                                   | 2025 | arXiv    | Generates artistic 3D scenes through image intermediaries.                         |
| [SceneFactor](https://openaccess.thecvf.com/content/CVPR2025/html/Bokhovkin_SceneFactor_Factored_Latent_3D_Diffusion_for_Controllable_3D_Scene_Generation_CVPR_2025_paper.html) | 2025 | CVPR     | Uses factored latent 3D diffusion for controllable scene generation.               |
| [AnchoredDream](https://arxiv.org/abs/2601.16532)                                                                                                                               | 2026 | arXiv    | Generates 360-degree indoor scenes from a single view through geometric grounding. |
| [Text-Image Conditioned 3D Generation](https://arxiv.org/abs/2603.21295)                                                                                                        | 2026 | arXiv    | Conditions 3D generation on both text and image inputs.                            |

## Agentic and Code-Based Scene Generation

| Title                                                        | Year | Venue        | Desc                                                                                     |
| ------------------------------------------------------------ | ---- | ------------ | ---------------------------------------------------------------------------------------- |
| [Holodeck](https://arxiv.org/abs/2312.09067)                 | 2024 | CVPR         | Generates 3D embodied AI environments from language.                                     |
| [SceneCraft](https://arxiv.org/abs/2403.01248)               | 2024 | arXiv        | Uses an LLM agent to synthesize 3D scenes as Blender code.                               |
| [EnvGen](https://arxiv.org/abs/2403.12014)                   | 2024 | arXiv        | Generates and adapts environments via LLMs for embodied agent training.                  |
| [SceneGenAgent](https://arxiv.org/abs/2410.21909)            | 2025 | arXiv        | Generates precise industrial scenes with a coding agent.                                 |
| [UnrealLLM](https://aclanthology.org/2025.findings-acl.994/) | 2025 | ACL Findings | Connects LLM-powered procedural content generation to controllable UE5 scene generation. |
| [WorldCraft](https://arxiv.org/abs/2502.15601)               | 2025 | arXiv        | Creates and customizes photorealistic 3D worlds with LLM agents.                         |
| [3Dify](https://arxiv.org/abs/2510.04536)                    | 2025 | arXiv        | Builds procedural 3D-CG generation workflows with LLMs, MCP, and RAG.                    |
| [SAGE](https://arxiv.org/abs/2602.10116)                     | 2026 | arXiv        | Scales agentic 3D scene generation for embodied AI.                                      |
| [SceneSmith](https://arxiv.org/abs/2602.09153)               | 2026 | arXiv        | Generates simulation-ready indoor scenes with an agentic pipeline.                       |
| [Code2Worlds](https://arxiv.org/abs/2602.11757)              | 2026 | arXiv        | Empowers coding LLMs for 4D world generation.                                            |
| [AutoUE](https://arxiv.org/abs/2603.07106)                   | 2026 | arXiv        | Automates 3D game generation in Unreal Engine with multi-agent systems.                  |
| [SimWorld Studio](https://arxiv.org/abs/2605.09423)          | 2026 | arXiv        | Generates evolving embodied learning environments with a self-evolving coding agent.     |

## World Generation and World Models

| Title                                                                                                                  | Year | Venue           | Desc                                                                         |
| ---------------------------------------------------------------------------------------------------------------------- | ---- | --------------- | ---------------------------------------------------------------------------- |
| [SceneScape](https://arxiv.org/abs/2302.01133)                                                                         | 2023 | arXiv           | Generates consistent text-driven scenes.                                     |
| [Learning Interactive Real-World Simulators](https://arxiv.org/abs/2310.06114)                                         | 2023 | arXiv           | Studies learned simulators for interactive real-world dynamics.              |
| [LucidDreamer](https://arxiv.org/abs/2311.13384)                                                                       | 2023 | arXiv           | Generates 3D Gaussian Splatting scenes without domain constraints.           |
| [WonderJourney](https://arxiv.org/abs/2312.03884)                                                                      | 2024 | arXiv           | Expands scenes from arbitrary starting points into broader worlds.           |
| [Video Generation Models as World Simulators](https://openai.com/research/video-generation-models-as-world-simulators) | 2024 | OpenAI Research | Frames video generation as a route toward world simulation.                  |
| [Genie](https://arxiv.org/abs/2402.15391)                                                                              | 2024 | ICML            | Learns generative interactive environments.                                  |
| [WonderWorld](https://arxiv.org/abs/2406.09394)                                                                        | 2025 | arXiv           | Supports interactive 3D scene generation from a single image.                |
| [Cosmos World Foundation Model Platform](https://arxiv.org/abs/2501.03575)                                             | 2025 | arXiv           | Provides world foundation models for physical AI.                            |
| [WorldGen](https://github.com/ZiYang-xie/WorldGen#readme)                                                              | 2025 | GitHub          | Generates 3D scenes in seconds.                                              |
| [Agent-World](https://arxiv.org/abs/2604.18292)                                                                        | 2026 | arXiv           | Synthesizes real-world environments for evolving general agent intelligence. |

## Embodied Environments and Robotics

| Title                                                   | Year | Venue    | Desc                                                                                                     |
| ------------------------------------------------------- | ---- | -------- | -------------------------------------------------------------------------------------------------------- |
| [AI2-THOR](https://ai2thor.allenai.org/)                | 2017 | Platform | Provides interactive 3D environments for embodied AI.                                                    |
| [CARLA](https://carla.org/)                             | 2017 | CoRL     | Provides an open simulator for autonomous driving research.                                              |
| [Habitat](https://aihabitat.org/)                       | 2019 | ICCV     | Provides simulation infrastructure for embodied AI.                                                      |
| [iGibson](https://github.com/StanfordVL/iGibson#readme) | 2021 | IROS     | Provides interactive simulated environments for embodied agents.                                         |
| [RoboTHOR](https://arxiv.org/abs/2004.06799)            | 2020 | arXiv    | Connects simulated and real robotic embodied AI evaluation.                                              |
| [MetaUrban](https://arxiv.org/abs/2407.08725)           | 2024 | arXiv    | Simulates urban micromobility for embodied AI.                                                           |
| [LEGENT](https://aclanthology.org/2024.acl-demos.32/)   | 2024 | ACL Demo | Provides an open platform for embodied agents.                                                           |
| [UnrealZoo](https://arxiv.org/abs/2412.20977)           | 2025 | arXiv    | Enriches photorealistic virtual worlds for embodied AI.                                                  |
| [VirtualEnv](https://arxiv.org/abs/2601.07553)          | 2026 | arXiv    | Provides a platform for embodied AI research.                                                            |
| [MolmoSpaces](https://arxiv.org/abs/2602.11337)         | 2026 | arXiv    | Provides a large open ecosystem for robot navigation and manipulation.                                   |
| [SimWorld-Robotics](https://arxiv.org/abs/2512.10046)   | 2026 | arXiv    | Synthesizes photorealistic dynamic urban environments for multimodal robot navigation and collaboration. |

## Tools and Asset Ecosystems

| Title                                                                        | Year | Venue    | Desc                                                                    |
| ---------------------------------------------------------------------------- | ---- | -------- | ----------------------------------------------------------------------- |
| [UnrealCV](https://doi.org/10.1145/3123266.3129396)                          | 2017 | ACM MM   | Connects Unreal Engine virtual worlds to computer vision workflows.     |
| [ThreeDWorld](https://github.com/threedworld-mit/tdw#readme)                 | 2020 | Platform | Provides a platform for interactive multi-modal physical simulation.    |
| [Infinigen](https://arxiv.org/abs/2306.09310)                                | 2023 | CVPR     | Generates infinite photorealistic worlds through procedural generation. |
| [MolmoSpaces Code and Assets](https://github.com/allenai/molmospaces#readme) | 2026 | GitHub   | Provides open assets, scenes, and tooling for robotics simulation.      |

## Related Lists

- [Awesome Embodied AI](https://github.com/haoranD/Awesome-Embodied-AI#readme) - Related list for embodied AI papers, tasks, and platforms.
- [Awesome 3D Generation](https://github.com/justimyhxu/awesome-3D-generation#readme) - Related list for 3D generation papers and resources.

## Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md)
before opening a pull request.
