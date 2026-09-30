# callai-models

On-device speech recognition models used by the Call AI app. Model files are published as
GitHub Release assets and verified by SHA-256 in the app.

## SenseVoiceSmall-callai-ko-exp9 (int8, sherpa-onnx)

Korean telephone-call fine-tune of SenseVoiceSmall.

| File | Size (bytes) | SHA-256 |
|---|---|---|
| model.int8.onnx | 239,233,841 | `0ecad17a8fc861d23a17a4c606ff51039a4b83de2188ef94081f98795aa18231` |
| tokens.txt | 315,894 | `f449eb28dc567533d7fa59be34e2abca8784f771850c78a47fb731a31429a1dc` |

Evaluation (28 user-corrected phone calls, character error rate, same windowing as the app):
base SenseVoiceSmall 28.5% → exp9 21.7%.

## Attribution and licenses

- Base model: **SenseVoiceSmall** by **Alibaba Group** (FunAudioLLM / iic/SenseVoiceSmall),
  licensed under the **FunASR Model License v1.1**. This derivative keeps the SenseVoice name.
- Fine-tuning data includes datasets from **AI Hub (aihub.or.kr)**:
  - 저음질 전화망 음성인식 데이터 (Low-quality telephone network speech recognition data)
  - 한국어 대화 음성 (Korean conversational speech)

  The original AI Hub data is not redistributed here.
- ONNX export uses scripts from k2-fsa/sherpa-onnx.
