# Statistical Inference on Aspirin: International Stroke Trial

Statistical analysis of aspirin allocation and six-month mortality using data from the International Stroke Trial (IST), a large randomised trial of patients with acute ischaemic stroke.

## Overview

This project investigates whether allocation to aspirin was associated with mortality at six months in the International Stroke Trial. The IST evaluated aspirin, subcutaneous heparin, both treatments, or neither among 19,435 patients with acute ischaemic stroke.

The analysis focuses on the aspirin randomisation and uses patients with complete outcome data. It examines baseline balance between treatment groups, models six-month mortality, assesses model calibration, and uses simulation to evaluate the trial's ability to detect treatment effects of different sizes.

## Method

The analysis was completed in **R** using packages from the tidyverse, including `dplyr` and `ggplot2`.

The workflow includes:

- Baseline descriptive statistics and visual comparisons of age, systolic blood pressure, sex, and consciousness state across aspirin groups.
- A binomial logistic-regression model for death at six months, with age, sex, systolic blood pressure, consciousness state at randomisation, and aspirin allocation as covariates.
- Odds-ratio estimates with normal-theory and bootstrap 95% confidence intervals.
- Calibration assessment comparing predicted six-month mortality probabilities with observed mortality proportions.
- A simulation-based power analysis across a range of assumed aspirin treatment effects.

## Results

The aspirin and no-aspirin groups were well balanced at baseline, consistent with the trial's randomised design.

After adjustment for the included covariates, aspirin allocation was associated with a small estimated reduction in the odds of death at six months. This effect did not reach conventional statistical significance in this analysis. Age, systolic blood pressure, and consciousness state at randomisation were important predictors of mortality.

The model's predicted probabilities were well calibrated overall. The power simulation suggested that the trial had high power to detect moderate treatment effects but lower power for small effects.

## Report

The full mathematical methodology, results and discussion are available in the project report:

[Project Report](statistical_inference_on_aspirin.pdf)
