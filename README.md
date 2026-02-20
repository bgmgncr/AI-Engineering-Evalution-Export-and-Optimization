# YOLOv8 Inference Framework Comparison

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
