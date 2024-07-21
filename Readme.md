
# Chinese Spelling Correction (CSC) Improvement Project

This repository is dedicated to the refinement and improvement of Chinese Spelling Correction (CSC) models. The project addresses two key issues in the current CSC research and provides a solution that enhances the performance of existing models.

## Overview

- **Issue 1**: Commonly used benchmark datasets (SIGHAN13, SIGHAN14, and SIGHAN15) contain mistakes that affect the accuracy of model evaluations.
- **Issue 2**: Existing models have reached a performance bottleneck with minimal and unstable improvements.

## Models Evaluated

- PLOME (Liu et al., 2021)
- REALISE (Xu et al., 2021)
- LEAD (Li et al., 2022b)
- SCOPE (Li et al., 2022a)

These models were chosen due to their strong performance and availability of source code for reproduction and training.

## Refinement Solution

Using ChineseBERT, our refinement solution masks problematic characters and infers the correct character based on contextual information. It measures the phonological distance and retains the inferred character if below a certain threshold.

## Results

The refinement process resulted in notable improvements in detection (D-P), detection recall (D-R), detection F1 (D-F), correction precision (C-P), correction recall (C-R), and correction F1 (C-F) for all evaluated models.

![image](https://github.com/user-attachments/assets/019acc34-5b65-4984-b6bd-9d08e1c99e0d)
