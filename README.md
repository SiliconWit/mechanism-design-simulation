---
title: "Mechanism Design and Simulation - Collaboration Guide"
description: "Contributing guide for Mechanism Design and Simulation course content"
tableOfContents: true
sidebar:
  order: 999
---

# Mechanism Design and Simulation

![Build](https://img.shields.io/badge/build-passing-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)
![Contributors Welcome](https://img.shields.io/badge/contributors-welcome-orange)

**Read this course at:** [https://siliconwit.com/education/mechanism-design-simulation/](https://siliconwit.com/education/mechanism-design-simulation/)

Hands-on engineering experiments using interactive browser-based mechanism simulators. Each lesson provides structured lab exercises with data collection, Python analysis scripts, and design insight questions. Covers crank-slider mechanisms, with future lessons planned for four-bar linkages, Geneva mechanisms, and other planar mechanisms.

## Lessons

| # | Title | Simulator |
|---|-------|-----------|
| 1 | Crank-Slider Mechanism Experiments | [Crank-Slider Simulator](https://siliconwit.com/product-development/crank-slider-mechanism-simulator/) |

## File Structure

```
mechanism-design-simulation/
├── index.mdx
├── crank-slider-experiments.mdx
└── README.md
```

## How to Contribute

1. Fork the repository: [SiliconWit/mechanism-design-simulation](https://github.com/SiliconWit/mechanism-design-simulation)
2. Create a feature branch: `git checkout -b feature/your-topic`
3. Make your changes and commit with a clear message
4. Push to your fork and open a Pull Request against `main`
5. Describe what you changed and why in the PR description

## Content Standards

- All lesson files use `.mdx` format
- Each experiment must include: objective, setup instructions, data collection table, analysis questions, Python script, and expected results
- Code blocks should include a title attribute:
  ````mdx
  ```python title="analyze_velocity.py"
  import numpy as np
  import matplotlib.pyplot as plt
  ```
  ````
- Use Starlight components (`<Tabs>`, `<TabItem>`, `<Steps>`, `<Card>`) where appropriate
- Python scripts must work with CSV files exported from the simulators
- Mathematical notation uses LaTeX in MDX
- Experiments should progress from basic observation to quantitative analysis

## Local Development

Clone the main site repository and initialize submodules:

```bash
git clone --recurse-submodules <main-repo-url>
cd siliconwit-com
npm install
npm run dev
```

To test a production build:

```bash
npm run build
```

## License

This course content is released under the [MIT License](LICENSE).
