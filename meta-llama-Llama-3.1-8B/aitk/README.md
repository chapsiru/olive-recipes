# Meta-Llama-3.1-8B Model Optimization

This folder mirrors the Llama-3.2-1B-Instruct AITK flows adapted for Meta-Llama-3.1-8B.

Workflows included:
- QDQ for AMD NPU (VitisAI)
- PTQ + AOT for QNN NPU
- OpenVINO for Intel NPU
- DML for general GPU

Update the QNN python environment path in `llama3_1_qnn_config.json` before running.
