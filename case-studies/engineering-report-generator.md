# Case Study: Engineering Report Generator

## 1. Problem

Engineering reports often require combining measurements, specifications, observations, investigation notes, and procedure details into a consistent technical format.

This is repetitive work, but it also requires engineering judgment. A poor automation workflow can create risks by:

* missing assumptions,
* hiding data-quality issues,
* over-interpreting statistical results,
* exposing sensitive production data,
* relying too much on AI-generated text.

## 2. Context

This project was built as part of an industrial AI career portfolio focused on process engineering, automation, and applied AI.

The goal was to create a realistic engineering automation project that demonstrates Python skills and responsible AI workflow design.

## 3. Approach

The project uses a modular Python architecture.

The main workflow is:

```text
Input manifest
  ↓
Input preparation report
  ↓
Privacy and sensitivity screening
  ↓
Engineering calculation or structured parsing
  ↓
Internal technical report
  ↓
AI review prompt
  ↓
External pseudonymized report
  ↓
Human engineering review
```

## 4. Implemented Modules

### Process Capability

Generates a Process Capability report with:

* Cp/Cpk calculations,
* Shapiro-Wilk normality screening,
* histogram,
* run chart,
* human review checklist.

### MSA / Gauge R&R

Generates an MSA report with:

* balanced crossed Gauge R&R validation,
* ANOVA-style variance component calculations,
* %GRR,
* number of distinct categories,
* MSA charts.

### RCA

Generates a Root Cause Analysis report from structured notes with:

* problem statement,
* containment actions,
* observations,
* evidence,
* root cause identification,
* corrective actions,
* verification of effectiveness.

### SOP

Generates a Standard Operating Procedure draft with:

* purpose,
* scope,
* safety precautions,
* PPE,
* procedure steps,
* quality checks,
* records,
* human review checklist.

## 5. Tools

* Python
* Pandas
* NumPy
* SciPy
* Matplotlib
* Typer
* Pytest
* Markdown
* GitHub Actions

## 6. Results

Milestone 1 delivered a working MVP with four report workflows and a root-level runner file for easier use in VS Code.

Validation:

```text
33 tests passed
```

The project can be run with:

```bash
python run_report.py --report-type all
```

## 7. Engineering Interpretation

The project shows that AI-assisted reporting should not start by sending raw data to an AI tool.

A safer workflow is:

1. structure the input,
2. validate required files,
3. screen for sensitive information,
4. calculate or parse locally,
5. create an internal report,
6. create a pseudonymized external report,
7. use AI only for review support,
8. keep final engineering responsibility with a human.

## 8. Limitations

* Synthetic data only.
* Not a validated quality-management tool.
* Statistical calculations need professional review before production use.
* Privacy detection is rule-based.
* Pseudonymization does not guarantee full anonymization.
* SOP drafts require HSE and quality approval before use.

## 9. Next Steps

* Add Streamlit user interface.
* Improve charts and visual summaries.
* Add report export options.
* Improve privacy detection.
* Add more realistic synthetic datasets.
* Add GitHub Pages portfolio presentation.
