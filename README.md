# ML-Semester-Research-Project

Literature Audit — Component D

Semester Research Project | Principles of Machine Learning | Component D: The Literature Audit

This repository contains the literature-audit dataset for Component D, documenting published studies that compare multiple machine-learning classifiers on applied, tabular supervised-classification problems.

The purpose of the audit is to build a transparent evidence base for the broader research question: how often are published classifier comparisons performed on datasets where sample size may be too limited to support reliable winner selection?

Project Objective

Published machine-learning studies frequently compare several classifiers and report a "best" model. However, when datasets are small, the identity of the winning classifier can be unstable and the reported performance of the winner can be optimistic.

This audit records the information needed to connect published classifier comparisons to the project's later simulation and power analysis.

For every qualifying paper, the audit captures:

Sample size

Number of outcome events where available

Class prevalence

Number of classifiers compared

Declared winning classifier

Winner's reported performance

Runner-up performance

Validation/testing protocol

Whether testing or statistical uncertainty was reported

Whether the comparative claim appeared in the abstract

Notes about important methodological or reporting details

Current Dataset

Category

Count

Qualifying papers

20

Rejected/excluded papers documented

5

Total papers currently documented

25

The workbook is organized into two sheets:

20 qualifying papers — papers that passed the current screening criteria.

Rejection Tally — papers screened but excluded, together with the reason for exclusion.

Important: These counts represent the current working dataset and are not the final 400-paper literature audit. The dataset is expected to grow as screening continues.

Screening Criteria

A paper is treated as qualifying when it satisfies the following screening requirements:

Applied machine learning study
The study addresses a real-world applied research question rather than being primarily a methodological benchmark or classifier-comparison paper.

Tabular supervised classification
The prediction task uses structured/tabular data and a categorical outcome.

At least two classifiers compared on the same data
Multiple classification algorithms must be evaluated for the same prediction task/dataset.

Comparative claim / winner identified
The paper must make a comparative claim that identifies one model as the best, highest-performing, or otherwise preferred model.

Sample size reported
The study must report enough information to identify the sample size used for the model analysis.

Publication eligibility
The study must be in English and published in the project's defined date window (currently 2019 or later in the working screening process).

Handling borderline cases

The audit does not silently assume missing information.

When a paper contains ambiguity — for example, different sample sizes for the collected cohort and the final modelling cohort, unclear runner-up scores, or conflicting performance metrics — the issue is recorded in the notes field.

This is intentional: the audit is designed to preserve uncertainty rather than manufacture precision.

Data Dictionary

Field

Description

Paper No.

Internal sequential identifier

paper_id

Identifier used when available

citation

Full bibliographic citation

doi_or_url

DOI or source URL used to access the paper

sample_size

Sample size used for the relevant model analysis

n_events

Number of positive/outcome events, where applicable

prevalence

Outcome prevalence or class distribution information

n_classifiers

Number of classifiers compared

winner

Classifier identified as the winner/best model

winner_score

Reported performance of the winner

runner_up_score

Reported performance of the second-best model when available

protocol

Train/test split, cross-validation, external validation, etc.

test_reported

Whether testing/uncertainty/statistical comparison information was reported

claim_in_abstract

Whether the comparative claim was explicitly present in the abstract

notes

Screening decisions, ambiguities, discrepancies, and methodological observations

Examples of Important Audit Cases

The dataset deliberately retains cases where the published evidence is not perfectly straightforward.

Winner-definition ambiguity

Some papers identify a model as the overall winner even when another classifier has a higher value for a particular metric. These cases are retained with an explanatory note rather than forcing the data into a single simplistic ranking.

Different modelling sample sizes

Some studies begin with one cohort size but use a smaller population after exclusions or missing-data handling. The audit records the sample size relevant to the modelling analysis and documents the original cohort size in the notes where necessary.

Missing runner-up information

Some papers clearly identify a winner but do not report the exact score of the runner-up. In these cases, the runner-up field is recorded as not reported rather than estimated.

Excluded single-classifier studies

A study can be highly relevant to machine learning while still failing this audit. For example, a paper evaluating only one ML classifier does not satisfy the requirement for a comparison of two or more classifiers.

Methodological/benchmark studies

Studies whose primary purpose is to compare algorithms or benchmark datasets rather than answer an applied real-world prediction question are excluded under the applied-study criterion.

Rejection Log

The Rejection Tally sheet currently documents five excluded papers.

Examples of exclusion reasons include:

Primarily methodological or benchmark research

Publication outside the date window

Only one ML classifier evaluated

No single clean same-data winner/runner-up comparison

Other failures of the predefined screening criteria

Keeping rejected papers is important because it makes the screening process auditable rather than showing only the papers that survived.

Audit Workflow

The intended workflow is:

Literature search
      ↓
Initial screening
      ↓
Apply inclusion/exclusion criteria
      ↓
Full-text access
      ↓
Extract standardized fields
      ↓
Record ambiguities
      ↓
Independent coding / agreement check
      ↓
Final literature-audit dataset
      ↓
Map published sample sizes to the project's power surface

The spreadsheet is therefore an audit dataset, not merely a bibliography.

Relationship to the Research Project

Component D supplies the empirical literature layer for the broader project.

The overall research design investigates whether small samples can make classifier winner selection unstable and inflate the apparent performance of the selected winner.

The literature audit contributes the real-world quantities needed to compare published practice with the project's simulation results, particularly:

sample size

number of classifiers

class prevalence

winner/runner-up performance gap

validation protocol

uncertainty/statistical testing practices

The eventual goal is to determine how frequently published classifier comparisons resemble regions of the project's simulated setting where winner selection may be unreliable.

Data Quality Principles

This audit follows several principles:

Do not guess missing values.

Preserve the paper's reported terminology where possible.

Distinguish reported values from calculated values.

Document discrepancies instead of silently correcting them.

Record exclusion reasons explicitly.

Use the modelling sample size when it differs from the originally recruited cohort.

Keep source links for traceability.

Treat the screening rules as fixed criteria rather than deciding eligibility on a paper-by-paper basis.

Current Status

Phase: Literature Audit / Component D
Current qualifying papers: 20
Current documented exclusions: 5
Status: Ongoing — dataset will continue to expand during the literature-screening stage.

Reproducibility and Transparency

The spreadsheet is intended to allow a reviewer or instructor to trace each included paper from:

citation → source → eligibility decision → extracted evidence → coded variables → notes

The repository should therefore be treated as a living research record. Changes to inclusion criteria or previously coded values should be documented through Git commits rather than silently replacing the original information.

Source and Citation

Each paper's DOI or source URL is stored directly in the dataset. The original papers remain the authoritative source for the extracted values.

This repository contains research notes and structured literature-audit data; it does not reproduce the full text of the cited publications.

Team:
Aliraza Mulla
Riya Shingare
Guru Sandeep Mygapula
Vivek Ray

Course: Principles of Machine Learning
Component: Week 1 — Component D: The Literature Audit
Group: Group 3

Add the team members' names and student IDs here before submitting the repository.

License / Academic Use

This repository is intended for academic coursework and research documentation.

The cited publications remain the property of their respective authors and publishers. This repository stores bibliographic information, extracted study-level metadata, screening decisions, and research notes.
