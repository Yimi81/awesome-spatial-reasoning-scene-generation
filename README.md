# Awesome Spatial Reasoning and Scene Generation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Curated papers, datasets, benchmarks, and systems for spatial reasoning,
> spatial intelligence, and controllable 3D scene or world generation.

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

- [Spatial Intelligence from a Cognitive Map Perspective: A Survey](https://github.com/Klingsor-tyx/Awesome-Spatial-Cognitive-Map#readme) (2026) - Organizes spatial intelligence as cognitive-map construction, inference, and realization.

## Spatial Reasoning and Cognitive Maps

- [Visual Spatial Reasoning](https://arxiv.org/abs/2205.00363) (2023) - Studies spatial relation verification in natural images.
- [LayoutGPT](https://arxiv.org/abs/2305.15393) (2023) - Uses LLMs for compositional visual planning and layout generation.
- [InstructScene](https://arxiv.org/abs/2402.04717) (2024) - Generates 3D indoor scenes from instructions with semantic graph priors.
- [RelScene](https://doi.org/10.1145/3664647.3681653) (2024) - Benchmarks spatial relations in text-driven 3D scene generation.
- [VULCAN](https://arxiv.org/abs/2512.22351) (2026) - Uses tool-augmented multi-agent iteration for 3D object arrangement.

## Benchmarks and Evaluation

- [WorldScore](https://arxiv.org/abs/2504.00983) (2025) - Provides a unified benchmark for evaluating world generation.
- [WorldLens](https://arxiv.org/abs/2512.10958) (2025) - Evaluates driving world models across real-world dimensions.
- [Benchmarking and Learning Multi-Dimensional Quality Evaluator for Text-to-3D Generation](https://arxiv.org/abs/2412.11170) (2025) - Studies quality assessment for text-to-3D generation.

## Indoor Scene Synthesis and Layout

- [GRAINS](https://arxiv.org/abs/1807.09193) (2019) - Uses generative recursive autoencoders for indoor scenes.
- [PlanIT](https://doi.org/10.1145/3306346.3322941) (2019) - Plans and instantiates indoor scenes with relation graphs and spatial priors.
- [ATISS](https://arxiv.org/abs/2110.03675) (2021) - Applies autoregressive transformers to indoor scene synthesis.
- [Text2Room](https://arxiv.org/abs/2303.11989) (2023) - Extracts textured 3D room meshes from 2D text-to-image models.
- [CommonScenes](https://arxiv.org/abs/2305.16283) (2023) - Generates commonsense 3D indoor scenes with scene graph diffusion.
- [SceneWiz3D](https://arxiv.org/abs/2312.08885) (2023) - Moves toward text-guided 3D scene composition.
- [AnyHome](https://arxiv.org/abs/2312.06644) (2024) - Generates structured and textured 3D homes with open vocabulary prompts.
- [DiffuScene](https://openaccess.thecvf.com/content/CVPR2024/html/Tang_DiffuScene_Denoising_Diffusion_Models_for_Generative_Indoor_Scene_Synthesis_CVPR_2024_paper.html) (2024) - Uses denoising diffusion models for generative indoor scene synthesis.
- [ArtiScene](https://arxiv.org/abs/2506.00742) (2025) - Generates artistic 3D scenes through image intermediaries.
- [SceneFactor](https://openaccess.thecvf.com/content/CVPR2025/html/Bokhovkin_SceneFactor_Factored_Latent_3D_Diffusion_for_Controllable_3D_Scene_Generation_CVPR_2025_paper.html) (2025) - Uses factored latent 3D diffusion for controllable scene generation.
- [AnchoredDream](https://arxiv.org/abs/2601.16532) (2026) - Generates 360-degree indoor scenes from a single view through geometric grounding.
- [Text-Image Conditioned 3D Generation](https://arxiv.org/abs/2603.21295) (2026) - Conditions 3D generation on both text and image inputs.

## Agentic and Code-Based Scene Generation

- [Holodeck](https://arxiv.org/abs/2312.09067) (2024) - Generates 3D embodied AI environments from language.
- [SceneCraft](https://arxiv.org/abs/2403.01248) (2024) - Uses an LLM agent to synthesize 3D scenes as Blender code.
- [EnvGen](https://arxiv.org/abs/2403.12014) (2024) - Generates and adapts environments via LLMs for embodied agent training.
- [SceneGenAgent](https://arxiv.org/abs/2410.21909) (2025) - Generates precise industrial scenes with a coding agent.
- [UnrealLLM](https://aclanthology.org/2025.findings-acl.994/) (2025) - Connects LLM-powered procedural content generation to controllable UE5 scene generation.
- [WorldCraft](https://arxiv.org/abs/2502.15601) (2025) - Creates and customizes photorealistic 3D worlds with LLM agents.
- [3Dify](https://arxiv.org/abs/2510.04536) (2025) - Builds procedural 3D-CG generation workflows with LLMs, MCP, and RAG.
- [SAGE](https://arxiv.org/abs/2602.10116) (2026) - Scales agentic 3D scene generation for embodied AI.
- [SceneSmith](https://arxiv.org/abs/2602.09153) (2026) - Generates simulation-ready indoor scenes with an agentic pipeline.
- [Code2Worlds](https://arxiv.org/abs/2602.11757) (2026) - Empowers coding LLMs for 4D world generation.
- [AutoUE](https://arxiv.org/abs/2603.07106) (2026) - Automates 3D game generation in Unreal Engine with multi-agent systems.
- [SimWorld Studio](https://arxiv.org/abs/2605.09423) (2026) - Generates evolving embodied learning environments with a self-evolving coding agent.

## World Generation and World Models

- [SceneScape](https://arxiv.org/abs/2302.01133) (2023) - Generates consistent text-driven scenes.
- [Learning Interactive Real-World Simulators](https://arxiv.org/abs/2310.06114) (2023) - Studies learned simulators for interactive real-world dynamics.
- [LucidDreamer](https://arxiv.org/abs/2311.13384) (2023) - Generates 3D Gaussian Splatting scenes without domain constraints.
- [WonderJourney](https://arxiv.org/abs/2312.03884) (2024) - Expands scenes from arbitrary starting points into broader worlds.
- [Video Generation Models as World Simulators](https://openai.com/research/video-generation-models-as-world-simulators) (2024) - Frames video generation as a route toward world simulation.
- [Genie](https://arxiv.org/abs/2402.15391) (2024) - Learns generative interactive environments.
- [WonderWorld](https://arxiv.org/abs/2406.09394) (2025) - Supports interactive 3D scene generation from a single image.
- [Cosmos World Foundation Model Platform](https://arxiv.org/abs/2501.03575) (2025) - Provides world foundation models for physical AI.
- [Agent-World](https://arxiv.org/abs/2604.18292) (2026) - Synthesizes real-world environments for evolving general agent intelligence.
- [WorldGen](https://github.com/ZiYang-xie/WorldGen#readme) (2025) - Generates 3D scenes in seconds.

## Embodied Environments and Robotics

- [AI2-THOR](https://ai2thor.allenai.org/) - Provides interactive 3D environments for embodied AI.
- [CARLA](https://carla.org/) - Provides an open simulator for autonomous driving research.
- [Habitat](https://aihabitat.org/) - Provides simulation infrastructure for embodied AI.
- [iGibson](https://github.com/StanfordVL/iGibson#readme) - Provides interactive simulated environments for embodied agents.
- [RoboTHOR](https://arxiv.org/abs/2004.06799) (2020) - Connects simulated and real robotic embodied AI evaluation.
- [MetaUrban](https://arxiv.org/abs/2407.08725) (2024) - Simulates urban micromobility for embodied AI.
- [LEGENT](https://aclanthology.org/2024.acl-demos.32/) (2024) - Provides an open platform for embodied agents.
- [UnrealZoo](https://arxiv.org/abs/2412.20977) (2025) - Enriches photorealistic virtual worlds for embodied AI.
- [VirtualEnv](https://arxiv.org/abs/2601.07553) (2026) - Provides a platform for embodied AI research.
- [MolmoSpaces](https://arxiv.org/abs/2602.11337) (2026) - Provides a large open ecosystem for robot navigation and manipulation.
- [SimWorld-Robotics](https://arxiv.org/abs/2512.10046) (2026) - Synthesizes photorealistic dynamic urban environments for multimodal robot navigation and collaboration.

## Tools and Asset Ecosystems

- [UnrealCV](https://doi.org/10.1145/3123266.3129396) (2017) - Connects Unreal Engine virtual worlds to computer vision workflows.
- [ThreeDWorld](https://github.com/threedworld-mit/tdw#readme) - Provides a platform for interactive multi-modal physical simulation.
- [Infinigen](https://arxiv.org/abs/2306.09310) (2023) - Generates infinite photorealistic worlds through procedural generation.
- [MolmoSpaces Code and Assets](https://github.com/allenai/molmospaces#readme) - Provides open assets, scenes, and tooling for robotics simulation.

## Related Lists

- [Awesome Embodied AI](https://github.com/haoranD/Awesome-Embodied-AI#readme) - Related list for embodied AI papers, tasks, and platforms.
- [Awesome 3D Generation](https://github.com/justimyhxu/awesome-3D-generation#readme) - Related list for 3D generation papers and resources.

## Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md)
before opening a pull request.
