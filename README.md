# TidyRModelling

A comprehensive Claude Code plugin for enterprise-scale R data science, data analysis, and biostatistics. This plugin provides specialized AI agents that act like the most experienced R data scientist in the world.

## Features

- **10 Specialized Agents**: Expert AI assistants for different aspects of R data science
- **23 Knowledge Skills**: Deep domain knowledge in tidymodels, biostatistics, and more
- **7 Workflow Commands**: End-to-end analysis workflows for common tasks
- **TMwR Code Review**: Anti-pattern detection for tidymodels workflows
- **Safe by Design**: All generated code goes to output folders - your existing code is never modified

## Installation

Add this plugin to your Claude Code configuration:

```bash
# Clone the repository
git clone https://github.com/yourusername/TidyRModelling.git

# Add to your Claude Code plugins directory
# (Follow Claude Code plugin installation instructions)
```

## Agents

### Data Science Core

| Agent | Model | Description |
|-------|-------|-------------|
| **r-data-architect** | Opus | Master strategist for R project architecture, pipeline design, and technology decisions |
| **data-wrangler** | Sonnet | Expert in dplyr, tidyr, and data transformation |
| **feature-engineer** | Sonnet | Specialist in recipes-based feature engineering and preprocessing |
| **tidymodels-engineer** | Sonnet | Model building with parsnip, workflows, tune, and stacks |

### Biostatistics

| Agent | Model | Description |
|-------|-------|-------------|
| **biostatistician** | Sonnet | Clinical trials, survival analysis, epidemiology, and regulatory statistics |

### Visualization & Reporting

| Agent | Model | Description |
|-------|-------|-------------|
| **viz-specialist** | Sonnet | Publication-quality graphics with ggplot2 and extensions |
| **reporting-engineer** | Sonnet | Quarto, RMarkdown, Shiny dashboards, and automated reports |

### Quality & Documentation

| Agent | Model | Description |
|-------|-------|-------------|
| **r-code-reviewer** | Opus | Code quality, tidyverse style, TMwR compliance, performance optimization |
| **r-docs-architect** | Sonnet | Package documentation, pkgdown sites, roxygen2 |
| **r-tutorial-engineer** | Sonnet | Tutorial creation, learnr apps, educational content |

## Skills (Knowledge Modules)

### tidymodels Ecosystem
- `tidymodels-workflow` - Complete modeling pipelines
- `recipes-patterns` - Feature engineering patterns
- `resampling-strategies` - Cross-validation and bootstrapping
- `model-tuning` - Hyperparameter optimization
- `model-evaluation` - Metrics and calibration
- `tidymodels-review-patterns` - **TMwR anti-pattern detection and compliance scoring**

### Biostatistics - Core
- `survival-analysis` - Time-to-event methods (KM, Cox, competing risks, RMST)
- `clinical-trials` - Trial design and analysis (group sequential, adaptive)
- `bayesian-modeling` - brms, rstanarm, Stan
- `epidemiology-methods` - Observational study methods, propensity scores
- `genomics-analysis` - Bioconductor and RNA-seq

### Biostatistics - Meta-Analysis
- `meta-analysis` - **Pairwise meta-analysis (meta, metafor)**
- `network-meta-analysis` - **NMA, SUCRA, consistency (netmeta, gemtc)**
- `ipd-meta-analysis` - **IPD-MA one-stage and two-stage methods**

### Biostatistics - Specialty Methods
- `diagnostic-accuracy` - **ROC curves, DCA, calibration (pROC, dcurves)**
- `pharmacokinetics` - **NCA, PopPK, bioequivalence (PKNCA, nlmixr2)**
- `health-economics` - **CEA, Markov models, PSA (BCEA, heemod, hesim)**
- `mendelian-randomization` - **Two-sample MR, sensitivity analyses (TwoSampleMR)**
- `causal-mediation` - **Mediation analysis (mediation, CMAverse)**
- `real-world-evidence` - **Target trial emulation, IPTW (TrialEmulation)**
- `advanced-adaptive-trials` - **Platform, basket, MAMS trials (adaptr, rpact)**

### Documentation
- `r-documentation-patterns` - Documentation best practices
- `roxygen2-pkgdown` - Package documentation tools

## Commands (Workflows)

| Command | Description |
|---------|-------------|
| `/r-analysis` | End-to-end data analysis workflow |
| `/r-code-review` | Comprehensive code quality review (includes TMwR compliance) |
| `/r-model-comparison` | Systematic model comparison with workflow sets |
| `/r-clinical-analysis` | Regulatory-compliant clinical trial analysis |
| `/r-project-setup` | Initialize new R project with best practices |
| `/r-doc-generate` | Generate comprehensive documentation |
| `/r-tutorial-create` | Create tutorials from code |

### Code Review Types

The `/r-code-review` command supports specialized review types:

| Type | Description |
|------|-------------|
| `full` | All review types including TMwR |
| `style` | Tidyverse style guide compliance |
| `performance` | Vectorization, memory, speed |
| `security` | Input validation, credentials |
| `tests` | Test coverage and quality |
| `tmwr` | **Tidymodels workflow review (data leakage, resampling, evaluation)** |

## Safety Features

All agents follow strict safety protocols:

- **Never modify existing code** - All generated code, reports, and documentation are written to the `output/` directory
- **Preserve original files** - Your data and code remain untouched
- **Review before integrating** - Generated content can be reviewed before use

### Default Output Structure

```
output/
├── code/           # Generated R scripts
├── reports/        # Quarto/RMarkdown documents
├── documentation/  # Package docs, README, vignettes
├── tutorials/      # Learning materials
├── models/         # Saved model objects (.rds)
└── figures/        # Generated plots
```

## Usage Examples

### Data Analysis
```
# Perform survival analysis on patient data
/r-analysis data/patients.csv survival html
```

### Code Review
```
# Review all R code in the R/ directory
/r-code-review R/ full
```

### Model Comparison
```
# Compare ML models for classification
/r-model-comparison data/credit.csv default classification rf,xgb,glmnet
```

### Clinical Analysis
```
# Full clinical study analysis
/r-clinical-analysis data/adsl.sas7bdat,data/adae.sas7bdat full rtf
```

### Documentation
```
# Generate complete package documentation
/r-doc-generate my_package full
```

## Package Coverage

This plugin has expertise in the complete tidyverse and tidymodels ecosystem:

### Core tidyverse
dplyr, tidyr, ggplot2, readr, purrr, tibble, stringr, forcats, lubridate

### tidymodels
parsnip, recipes, workflows, tune, rsample, yardstick, broom, workflowsets, stacks, probably, censored

### Biostatistics - Core
survival, survminer, cmprsk, flexsurv, mstate, rstpm2, brms, rstanarm, mmrm, gsDesign, rpact

### Meta-Analysis
meta, metafor, dmetar, metasens, netmeta, gemtc, multinma, mada, robumeta

### Pharmacokinetics & Health Economics
PKNCA, mrgsolve, nlmixr2, rxode2, BE, BCEA, heemod, hesim, dampack

### Causal Inference & Epidemiology
MatchIt, WeightIt, cobalt, dagitty, ggdag, EValue, ivreg, tipr, adjustedCurves, TrialEmulation

### Mendelian Randomization
TwoSampleMR, MendelianRandomization, MRPRESSO, mr.raps

### Mediation Analysis
mediation, medflex, CMAverse, intmed

### Adaptive Trials
adaptr, basket, MAMS, RBesT, gMCPLite

### Diagnostic Accuracy
pROC, cutpointr, OptimalCutpoints, dcurves, irr

### Visualization
ggplot2, patchwork, cowplot, ggpubr, ggrepel, ggforce, gganimate, plotly, gt, gtsummary

### Bioconductor
DESeq2, edgeR, limma, clusterProfiler, ComplexHeatmap, Seurat

### Reporting
quarto, rmarkdown, shiny, flexdashboard, pkgdown, roxygen2

## Contributing

Contributions are welcome! Please feel free to submit issues and pull requests.

## License

MIT License - see LICENSE file for details.

## Acknowledgments

- Built following tidy modeling principles from [Tidy Modeling with R](https://www.tmwr.org/)
- Agent architecture inspired by enterprise data science workflows
- Biostatistics patterns based on regulatory best practices
