# YOLOv8 Inference Framework Comparison

This project investigates the effects of converting a YOLOv8 model across different inference frameworks: PyTorch, ONNX, and TensorRT. The goal is to analyze performance differences in terms of latency, stability, and throughput while ensuring prediction consistency after conversion.

## Objectives

- Compare inference latency between PyTorch and ONNX
- Verify model parity after conversion
- Benchmark pure forward-pass performance
- Evaluate TensorRT as an optimized deployment framework

## Experiments

### 1. Latency and Stability Test

- Dataset: 10 images from the COCO dataset
- Image size: 640x640
- Metrics:
  - Mean latency
  - p50 latency
  - p95 latency
  - FPS

Results showed that ONNX improved latency stability compared to PyTorch, particularly in p95 values.

### 2. Pure Inference Benchmark

- Setup: 1 image processed 1000 times
- Environment: Google Colab (NVIDIA T4 GPU)
- Repeated 5 times for reliability
- Frameworks compared:
  - PyTorch
  - ONNX (CUDA)
  - TensorRT (FP16)

TensorRT consistently achieved the highest FPS and lowest inference time.

## Key Findings

- Model conversion preserved prediction consistency.
- ONNX improved latency stability.
- TensorRT provided the best inference performance.
- Performance ranking remained consistent across multiple runs:
  
  TensorRT > ONNX > PyTorch

## Conclusion

Model optimization can significantly improve inference speed without sacrificing detection accuracy. Proper evaluation using both parity and latency metrics is essential for reliable deployment.
