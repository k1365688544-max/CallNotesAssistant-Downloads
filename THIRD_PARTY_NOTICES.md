# 第三方组件与许可说明

本文件说明便携包内的第三方语音模型。它不代表本项目自有源码采用 Apache License 2.0，也不为自有源码另行授予许可证。其他第三方运行库仍适用各自的许可证。

## 离线语音模型

| 便携包目录 | 官方模型来源 | 官方标注的许可证 |
|---|---|---|
| `models/paraformer-zh-onnx` | [ModelScope · iic/speech_paraformer-large_asr_nat-zh-cn-16k-common-vocab8404-onnx](https://modelscope.cn/models/iic/speech_paraformer-large_asr_nat-zh-cn-16k-common-vocab8404-onnx) | Apache License 2.0 |
| `models/fsmn-vad-onnx` | [ModelScope · iic/speech_fsmn_vad_zh-cn-16k-common-onnx](https://modelscope.cn/models/iic/speech_fsmn_vad_zh-cn-16k-common-onnx) | Apache License 2.0 |

上述模型由 FunASR / Alibaba 达摩院相关项目提供，2026-10-15 通过官方 ModelScope 模型元数据核对许可证。便携包使用官方量化 ONNX 权重及所需配置、词表和归一化文件，不包含用户音频或用户训练数据；本项目没有修改这些模型文件。具体文件及校验值见源码 `build-models.json`。

Apache License 2.0 原文随包附于 `licenses/Apache-2.0.txt`，取自 [Apache Software Foundation 官方原文](https://www.apache.org/licenses/LICENSE-2.0.txt)。模型使用说明见 [FunASR](https://github.com/modelscope/FunASR)。

下载、使用或再分发上述模型时，请保留本说明与许可证，并遵守原模型的适用条款。模型许可证不对识别准确率、设备兼容性或使用场景作出保证。


## 加密运行库

媒体解密和项目平台登录加密使用 [cryptography](https://cryptography.io/)。该库按 Apache License 2.0 或 BSD 双重许可分发；其原始许可证随库元数据中的 `cryptography-*.dist-info/licenses/` 一同打包，保留 `LICENSE`、`LICENSE.APACHE` 与 `LICENSE.BSD`。它不提供远端账号，也不会把个人凭据加入发行包。
