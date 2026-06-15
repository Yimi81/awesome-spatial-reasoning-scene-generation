# Contribution Guidelines

Thanks for helping improve this list.

## Scope

This list focuses on work that connects at least one of these themes:

- Spatial reasoning over objects, geometry, relations, constraints, maps, or
  embodied state.
- Controllable 3D scene, environment, or world generation.
- Benchmarks and evaluation for spatial relations, world generation, or scene
  coherence.
- Embodied simulation infrastructure where generated or richly varied
  environments matter for agent learning.

Prefer papers, datasets, benchmarks, systems, and codebases with public links.
Company notes, whitepapers, and product claims can be useful, but they should be
placed in source notes unless there is enough technical detail to make them a
stable research resource.

## Entry Format

Use this format:

```markdown
- [Name](https://example.com) (YYYY) - One factual sentence about what it contributes.
```

Keep descriptions short, neutral, and specific. Avoid marketing language.

## Quality Bar

- Check that links work.
- Avoid duplicate entries.
- Put the item in the most specific section.
- Prefer the paper, project page, or official repository over secondary posts.
- For GitHub repositories, append `#readme` when the README is the target.
- Use ASCII punctuation and normal hyphens.

## Pull Request Checklist

- [ ] The entry is in scope.
- [ ] The link is stable and canonical.
- [ ] The description is factual and concise.
- [ ] The README table of contents still matches section headings.
- [ ] `npm run lint` passes, if Node.js is available.
