
# Chinese Spelling Correction (CSC) Improvement Project
# Two Issues with Chinese Spelling Correction and A Refinement Solution

This repository is dedicated to the refinement and improvement of Chinese Spelling Correction (CSC) models. The project addresses two key issues in the current CSC research and provides a solution that enhances the performance of existing models.

## Overview

This repository is based on our paper: [**Two Issues with Chinese Spelling Correction and A Refinement Solution**](https://aclanthology.org/2024.acl-short.19) (Sun et al., ACL 2024). 

- **Issue 1**: Commonly used benchmark datasets (SIGHAN13, SIGHAN14, and SIGHAN15) contain mistakes that affect the accuracy of model evaluations.
- **Issue 2**: Existing models have reached a performance bottleneck with minimal and unstable improvements.

## Contributions

1. **Dataset Refinement**: We manually corrected the mistakes in the SIGHAN datasets and re-evaluated four representative CSC models using the fixed datasets. You can get the refined SIGHAN dataset from the following link:  
   [Refined SIGHAN Dataset](https://drive.google.com/drive/folders/1lmsPxmRmFrYnrrhQLKC4zGXCUtiyp-08?usp=drive_link)
   
2. **Performance Improvement**: We proposed a simple yet effective refinement solution, which significantly improved the models' performance across all metrics without additional training.

## Models Evaluated

- PLOME (Liu et al., 2021)
- REALISE (Xu et al., 2021)
- LEAD (Li et al., 2022b)
- SCOPE (Li et al., 2022a)

These models were chosen due to their strong performance and availability of source code for reproduction and training.

## Refinement Solution

Using **ChineseBERT**, our refinement solution identifies and masks problematic characters. It then infers the correct character based on contextual information and measures the phonological distance. If the distance is below a predefined threshold, the inferred character is retained.

## Results

The refinement process resulted in notable improvements in the following metrics for all evaluated models:  
- Detection Precision (D-P)  
- Detection Recall (D-R)  
- Detection F1 Score (D-F)  
- Correction Precision (C-P)  
- Correction Recall (C-R)  
- Correction F1 Score (C-F)

![image](https://github.com/user-attachments/assets/019acc34-5b65-4984-b6bd-9d08e1c99e0d)
