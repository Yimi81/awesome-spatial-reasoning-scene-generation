# Source Notes

These notes explain how the initial list was seeded from local material in this
workspace. They are not a substitute for canonical paper links.

## Title Choice

The recommended project title is **Awesome Spatial Reasoning and Scene
Generation**.

This is more explicit than `awesome-spatial-reason-gen`: it keeps the standard
awesome-list pattern while avoiding the ambiguous `gen` abbreviation. "Scene
Generation" also leaves room for indoor scenes, outdoor worlds, simulation-ready
environments, game worlds, and embodied AI training environments.

## Seed Sources

- `amara_whitepaper_summary.md`
- `spatial-reason-survey.pdf`
- `simworld-studio.pdf`
- `molmospaces.pdf`
- `Spatial-reason-gen/SimWorld-Studio/references.bib`

## Taxonomy Used

The first README structure follows four linked layers:

- Spatial representation and reasoning: cognitive maps, object-centric state,
  scene graphs, metric maps, relational maps, and persistent spatial memory.
- Evaluation: spatial relation benchmarks, semantic coherence metrics, and
  world generation quality benchmarks.
- Controllable generation: text-to-scene, graph-to-scene, diffusion-based
  layouts, agentic scene construction, and code-based generation.
- Embodied environments: generated or diverse simulators that expose tasks,
  rewards, actions, observations, and agent feedback loops.

## Amara Whitepaper Summary

The local Amara summary frames the problem as a reasoning gap rather than a
tooling gap. The key filter it suggests for this awesome list is whether a work
helps a system maintain or generate spatially coherent worlds through:

- Object positions and bounding volumes.
- Collision, support, adjacency, alignment, and clearance constraints.
- Constraint graphs or structured spatial state.
- Asset retrieval or generation with semantic metadata.
- Scene-level and object-level ground truth.
- Feedback loops that improve spatial reasoning or generated scenes over time.

## Spatial Survey Summary

The survey PDF, "Spatial Intelligence from a Cognitive Map Perspective: A
Survey", organizes spatial intelligence around cognitive maps:

- Perception constructs internal spatial representations.
- Reasoning performs inference with those representations.
- Generation realizes those representations as external spatial forms.

The README uses this as the backbone for its sections.

## SimWorld Studio Summary

`simworld-studio.pdf` motivates the difference between static scene generation
and deployable embodied environment generation. Its main inclusion criteria for
this list are:

- Generated scenes should be physically grounded.
- Generated worlds should support tasks, rewards, observations, and actions.
- Agent feedback can steer future environment generation.
- Verification can include rule-based checks, physics checks, and VLM critiques.

## MolmoSpaces Summary

`molmospaces.pdf` contributes the robotics side of the list:

- Large-scale scene and object diversity.
- Rich object metadata and grasp annotations.
- Simulator-agnostic environments.
- Benchmarks for navigation, manipulation, and long-horizon tasks.
- Simulation-to-real correlation as an evaluation signal.

## Open Items to Verify

These names appeared in the local notes or BibTeX but should get canonical links
before being promoted into the main README as regular entries:

- Spatial-DISE.
- SpatialBench.
- PLATO.
- SceneEval.
- SenseNova SI.
- Amara.
