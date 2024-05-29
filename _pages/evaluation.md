---
layout: page
toc: false
title: Evaluation
sidebar: true
icon: fas fa-sort-numeric-down
order: 4
---

The design is evaluated based on accuracy and throughput.

### ACCURACY

Accuracy is measured using the [F1-score](https://en.wikipedia.org/wiki/F-score), where:

F1-score = (2 * precision * recall) / (precision + recall)

precision = global_true_positives / (global_true_positives + global_false_positives)

recall = global_true_positives / (global_true_positives + global_false_negatives)

True positives are when a reported object matches the type and location (IoU > 0.5) of an object from the golden data.

**mIoU** is used to measure the **segmentation** performance. 

<del>The minimum accuracy should be **TBD**, otherwise a penalty is applied.</del>

### THROUGHPUT
Throughput is measured in FPS.  The time to read images from the SD card is not included.

<del>The design should achieve at least 5 FPS (**subject to change**), otherwise a penatly is applied.</del>

### SCORING FUNCTION
The score for a team is calculated as follows **(Subject to change)**:

<del>team score = F1-score^2 * fps </del>

team score = (F1-score^2 + mIoU^2) * fps

**Note** that for fairness, all valid submissions must meet the requirements: F1 >= 0.25, mIoU >= 0.15. 

### Scoring Script

A [score_miou.py](https://github.com/PKU-SEC-Lab/dac-sdc-2024/tree/main/media/score_miou.py) script is provided that will provide f1-score, mIoU and fps.
