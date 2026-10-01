Transparent static-analysis scoring for software sustainability, grounded in the Green Software Foundation SCI specification.
green-software
sustainability
software-carbon-intensity
carbon-aware-computing
static-analysis
python
developer-tools
cloud-efficiency
https://sci.greensoftware.foundation/

# sustainability-score

Measure Software Sustainability. Identify Opportunities. Build Greener Software.

Sustainability Score is a Python-based static-analysis tool designed to help developers evaluate software sustainability practices across source code, cloud infrastructure, containerization, CI/CD pipelines, and SRE/operations.

As software systems grow, their resource consumption and environmental impact become increasingly important. Sustainability Score aims to help developers identify potential improvement opportunities and make more informed engineering decisions.

# Why Sustainability Score?

Traditional code analysis often focuses on correctness, security, and maintainability. Sustainability Score adds another perspective: how software engineering practices may influence resource efficiency and environmental sustainability.

It reads only what is in the repository (source, Dockerfiles, CI workflows,
Terraform, Kubernetes manifests, dependency files). It never runs the code and
never measures live infrastructure, so it is **honest about confidence**: every
finding is stamped with a data-quality tier, and the report says plainly that
the score is directional, not a measurement.

# Key Areas of Analysis

Code Efficiency: Examine code patterns that may affect computational efficiency.
Cloud Infrastructure: Evaluate infrastructure configurations for potential efficiency improvements.
Containerization: Review container-related practices that may influence resource utilization.
CI/CD Pipelines: Identify opportunities to improve pipeline efficiency.
SRE & Operations: Assess operational practices related to reliability and resource management.
Sustainability Scoring: Use sustainability focused insights to guide improvement efforts.

The availability and depth of each analysis depend on the implemented rules and supported file types.

# Who Is It For?
- Python developers
- DevOps and platform engineers
- Cloud infrastructure engineers
- SRE teams
- Green software advocates
- Open source maintainers
- Researchers exploring software sustainability

# Getting Started

Clone the repository:

git clone https://github.com/srinathgopinath-code/sustainability-score.git

cd sustainability score

Install the project in editable mode, following the repository's dependency instructions:

pip install -e .

Run the analyzer:

sustainability-score /path/to/repo

Replace /path/to/repo with the directory you want to analyze. Confirm the supported installation steps and CLI options in the project documentation.


## How scoring works

Each applicable pillar starts at 100 and loses points per finding by severity
(high 20 / medium 10 / low 4 / info 0), floored at 0. The composite is the
weighted mean over **applicable** pillars only — a pillar with no relevant
artifacts (e.g. no Dockerfile) is marked *not applicable* and its weight is
renormalized away rather than counted as a free 100.

## Tests

```bash
python -m pytest
```
# Contributing

Contributions, feedback, bug reports, documentation improvements, and new analysis rules are welcome.
- Fork this repository.
- Create a feature branch.
- Make your changes and test them.
- Submit a pull request describing your contribution.
- Please open an issue to discuss significant changes before starting work.

# Support the Project

If you find Sustainability Score useful, consider starring the repository, sharing it with developers interested in green software, trying it on a sample project, or contributing an improvement.

Every constructive contribution helps the project grow.

## License

MIT. See [LICENSE](LICENSE).


