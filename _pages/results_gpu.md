---
layout: page
toc: false
title: Results (GPU)
sidebar: true
icon: fas fa-medal
order: 6
---

## Final Results

## Prelim \#1

Did not run successfully:
* SEU AIC Lab: Batch size is not equal to 1. 

## Prelim #2

| RANK | TEAM NAME | **PRECISION** | RECALL | **F1-SCORE** | FPS  | mIoU   | TOTAL SCORE |
| ---- | --------- | ------------- | ------ | ------------ | ---- | ------ | ----------- |
| 1    | GO3       | 0.714         | 0.552  | 0.623        | 9.87 | 0.2086 | 4.2601      |
| 2    | T-IMI     | 0.016         | 0.007  | 0.010        | 2.42 | 0.0000 | 0.0002      |

## Prelim #3

| RANK | TEAM NAME     | **PRECISION** | RECALL | **F1-SCORE** | FPS   | mIoU   | TOTAL SCORE |
| ---- | ------------- | ------------- | ------ | ------------ | ----- | ------ | ----------- |
| 1    | GO3           | 0.582         | 0.637  | 0.608        | 34.62 | 0.1937 | 14.0993     |
| 2    | SEU_AIC_Lab   | 0.640         | 0.336  | 0.441        | 35.39 | 0.2376 | 8.8677      |
| 3    | SKKU_IRIS_GPU | 0.740         | 0.589  | 0.656        | 3.79  | 0.2596 | 1.8837      |
| 4    | AlphaChip     | 0.733         | 0.785  | 0.758        | 1.10  | 0.4264 | 0.8316      |
| 5    | FSBIN         | 0.000         | 0.0    | 0            | 7.94  | 0.2045 | 0.3318      |
| 6    | Redbrain      | 0.247         | 0.006  | 0.013        | 8.17  | 0.0000 | 0.0013      |

#### Bug

1. T-IMI

   ```
   Fail: [ONNXRuntimeError] : 1 : FAIL : Load model from ./prune.onnx failed:/onnxruntime_src/onnxruntime/core/graph/model_load_utils.h:47 void onnxruntime::model_load_utils::ValidateOpsetForDomain(const std::unordered_map<std::basic_string<char>, int>&, const onnxruntime::logging::Logger&, bool, const string&, int) ONNX Runtime only *guarantees* support for models stamped with official released onnx opset versions. Opset 17 is under development and support for this is limited. The operator schemas and or other functionality may change before next ONNX release and in this case ONNX Runtime will not guarantee backward compatibility. Current official support for domain ai.onnx is till opset 15.
   ```
