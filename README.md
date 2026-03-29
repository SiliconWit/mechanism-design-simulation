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

Hands-on engineering experiments using interactive browser-based mechanism simulators. Each lesson provides structured lab exercises with data collection, Python analysis scripts, and design insight questions.

## Lessons

| # | Title | Simulator |
|---|-------|-----------|
| 1 | Crank-Slider Mechanism Experiments (8 experiments) | [Crank-Slider Simulator](https://siliconwit.com/product-development/crank-slider-mechanism-simulator/) |
| 2 | Four-Bar Linkage Experiments (9 experiments) | [Four-Bar Linkage Simulator](https://siliconwit.com/product-development/four-bar-linkage-simulator/) |
| 3 | Scissor Lift Experiments (9 experiments) | [Scissor Lift Simulator](https://siliconwit.com/product-development/scissor-lift-mechanism-simulator/) |

## File Structure

```
mechanism-design-simulation/
├── index.mdx
├── crank-slider-experiments.mdx
├── four-bar-linkage-experiments.mdx
├── scissor-lift-experiments.mdx
└── README.md
```

## How to Contribute

All commands below work on Linux, macOS, and Windows (using Git Bash, PowerShell, or Command Prompt with Git installed).

### For Team Members (with push access)

**First time setup (clone the repo once):**

```bash
git clone https://github.com/SiliconWit/mechanism-design-simulation.git
cd mechanism-design-simulation
```

**Every time you start working:**

```bash
git pull origin main
```

Always pull before making changes. This avoids conflicts with other contributors.

**After making your changes:**

```bash
git add .
git commit -m "Brief description of what you changed"
git push origin main
```

**If you get a push error** (someone pushed before you):

```bash
git pull origin main
```

Git will merge the changes automatically in most cases. If there is a conflict, Git will mark the conflicting lines in the file. Open the file, choose which version to keep, then:

```bash
git add .
git commit -m "Resolve merge conflict"
git push origin main
```

**Tips to avoid conflicts:**

- Always `git pull origin main` before you start working
- Push your changes as soon as you are done, do not hold onto uncommitted work for long
- Coordinate with other contributors so two people are not editing the same file at the same time

### For External Contributors (without push access)

1. Fork the repository: [SiliconWit/mechanism-design-simulation](https://github.com/SiliconWit/mechanism-design-simulation)
2. Clone your fork:
   ```bash
   git clone https://github.com/YOUR-USERNAME/mechanism-design-simulation.git
   cd mechanism-design-simulation
   ```
3. Make your changes and commit:
   ```bash
   git add .
   git commit -m "Brief description of what you changed"
   git push origin main
   ```
4. Open a Pull Request against `main` on the original repository
5. Describe what you changed and why in the PR description

## Content Standards

- All lesson files use `.mdx` format
- Each experiment must include: objective, setup instructions, data collection table, Python script, expected results, and design question
- Code blocks should include a title attribute:
  ````mdx
  ```python title="analyze_velocity.py"
  import numpy as np
  import matplotlib.pyplot as plt
  ```
  ````
- Use Starlight components (`<Tabs>`, `<TabItem>`, `<Steps>`, `<Card>`) where appropriate
- Python scripts must work with CSV files exported from the simulators
- Experiments should progress from basic observation to quantitative analysis

## Local Development

To preview the full site locally, clone the main site repository and initialize submodules:

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
