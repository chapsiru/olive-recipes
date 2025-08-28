# Llama-3.1-8B optimization (NVIDIA TensorRT Model Optimizer)

This folder contains examples of Olive recipes for `Meta-Llama-3.1-8B` optimization.

## INT4 AWQ Quantized Model Generation

The olive recipe `Meta-Llama-3.1-8B_nvmo_int4_awq.json` produces an INT4 AWQ quantized model using NVIDIA's TensorRT Model Optimizer toolkit.

### Setup

1. Install Olive with NVIDIA TensorRT Model Optimizer toolkit

    - Install Olive with TensorRT Model Optimizer.
    ```bash
    pip install olive-ai[nvmo]
    ```

    - If TensorRT Model Optimizer needs to be installed from a local wheel, then follow below steps.

        ```bash
        pip install olive-ai
        pip install <modelopt-wheel>[onnx]
        ```

    - Validate installation
        ```bash
        python -c "from modelopt.onnx.quantization.int4 import quantize as quantize_int4"
        ```

    - Refer TensorRT Model Optimizer documentation for details.

2. Install suitable onnxruntime and onnxruntime-genai packages

    - Install the onnxruntime and onnxruntime-genai packages that have NvTensorRTRTXExecutionProvider support. Ensure only one onnxruntime variant is installed.

3. Install additional requirements.

    ```bash
    pip install -r requirements-nvmo-awq.txt
    ```

### Steps to run

```bash
olive run --config Meta-Llama-3.1-8B_nvmo_int4_awq.json
```
