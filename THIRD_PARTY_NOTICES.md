# 第三方模型与许可说明

本文件说明便携包内的第三方语音模型。它不代表本项目自有源码采用 Apache License 2.0，也不为自有源码另行授予许可证。其他第三方运行库仍适用各自的许可证。

## 离线语音模型

| 便携包目录 | 官方模型来源 | 官方标注的许可证 |
|---|---|---|
| `models/paraformer-zh-onnx` | [ModelScope · iic/speech_paraformer-large_asr_nat-zh-cn-16k-common-vocab8404-onnx](https://modelscope.cn/models/iic/speech_paraformer-large_asr_nat-zh-cn-16k-common-vocab8404-onnx) | Apache License 2.0 |
| `models/fsmn-vad-onnx` | [ModelScope · iic/speech_fsmn_vad_zh-cn-16k-common-onnx](https://modelscope.cn/models/iic/speech_fsmn_vad_zh-cn-16k-common-onnx) | Apache License 2.0 |

上述模型由 FunASR / Alibaba 达摩院相关项目提供，2026-10-15 通过官方 ModelScope 模型元数据核对许可证。便携包使用官方量化 ONNX 权重及所需配置、词表和归一化文件，不包含用户音频或用户训练数据；本项目没有修改这些模型文件。安装包已按固定模型清单逐项校验，结果见每版附带的验证报告。

Apache License 2.0 原文随包附于 `licenses/Apache-2.0.txt`，取自 [Apache Software Foundation 官方原文](https://www.apache.org/licenses/LICENSE-2.0.txt)。模型使用说明见 [FunASR](https://github.com/modelscope/FunASR)。

下载、使用或再分发上述模型时，请保留本说明与许可证，并遵守原模型的适用条款。模型许可证不对识别准确率、设备兼容性或使用场景作出保证。
