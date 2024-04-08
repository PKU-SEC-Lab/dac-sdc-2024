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

Average Hausdorff Distance is used as the segmentation performance metric. 

<del>The minimum accuracy should be **TBD**, otherwise a penalty is applied.</del>

### THROUGHPUT
Throughput is measured in FPS.  The time to read images from the SD card is not included.

<del>The design should achieve at least 5 FPS (**subject to change**), otherwise a penatly is applied.</del>

### SCORING FUNCTION
The score for a team is calculated as follows **(Subject to change)**:

team score = F1-score^2 * fps


### Scoring Script

A <del>[score.py](https://github.com/dac-sdc/fpga_starter_2023/blob/main/scripts/score.py) </del> [score.py](./score.py)script is provided that will provide f1-score and fps.
