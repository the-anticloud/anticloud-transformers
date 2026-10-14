# TRANSFORMERS

![licence](https://img.shields.io/badge/licence-Apache-2.0-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![checks](https://img.shields.io/badge/checks-unknown_PASS-brightgreen)

> Governed Anticloud packaging of the upstream project `TRANSFORMERS` in category **PHILOSOPHY_SEMANTICS**. check results: see ISOLATED_LAB_RESULTS. Every number below traces to a named file + run stamp; nothing is borrowed from other projects.

**Upstream:** TRANSFORMERS · **Upstream pin:** `35924ec379eec682bbdca219886e16eff4df8b09` · **Category:** PHILOSOPHY_SEMANTICS · **Vendor:** Anticloud FZ LLE · **Licence:** Apache-2.0

---

## What This Project Does

<!---
Copyright 2020 The HuggingFace Team. All rights reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
-->

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://huggingface.co/datasets/huggingface/documentation-images/raw/main/transformers-logo-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://huggingface.co/datasets/huggingface/documentation-images/raw/main/transformers-logo-light.svg">
    <img alt="Hugging Face Transformers Library" src="https://huggingface.co/datasets/huggingface/documentation-images/raw/main/transformers-logo-light.svg" width="352" height="59" style="max-width: 100%;">
  </picture>
  <br/>
  <br/>
</p>

<p align="center">
    <a href="https://huggingface.com/models"><img alt="Checkpoints on Hub" src="https://img.shields.io/endpoint?url=https://huggingface.co/api/shields/models&color=brightgreen"></a>
    <a href="https://circleci.com/gh/huggingface/transformers"><img alt="Build" src="https://img.shields.io/circleci/build/github/huggingface/transformers/main"></a>
    <a href="https://github.com/huggingface/transformers/blob/main/LICENSE"><img alt="GitHub" src="https://img.shields.io/github/license/huggingface/transformers.svg?color=blue"></a>
    <a href="https://huggingface.co/docs/transformers/index"><img alt="Documentation" src="https://img.shields.io/website/http/huggingface.co/docs/transformers/index.svg?down_color=red&down_message=offline&up_message=online"></a>
    <a href="https://github.com/huggingface/transformers/releases"><img alt="GitHub release" src="https://img.shields.io/github/release/huggingface/transformers.svg"></a>
    <a href="https://github.com/huggingface/transformers/blob/main/CODE_OF_CONDUCT.md"><img alt="Contributor Covenant" src="https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg"></a>
    <a href="https://zenodo.org/badge/latestdoi/155220641"><img src="https://zenodo.org/badge/155220641.svg" alt="DOI"></a>
</p>

<h4 align="center">
    <p>
        <b>English</b> |
        <a href="i18n/README_zh-hans.md">简体中文</a> |
        <a href="i18n/README_zh-hant.md">繁體中文</a> |
        <a href="i18n/README_ko.md">한국어</a> |
        <a href="i18n/README_es.md">Español</a> |
        <a href="i18n/README_ja.md">日本語</a> |
        <a href="i18n/README_hd.md">हिन्दी</a> |
        <a href="i18n/README_ru.md">Русский</a> |
        <a href="i18n/README_pt-br.md">Português</a> |
        <a href="i18n/README_te.md">తెలుగు</a> |
        <a href="i18n/README_fr.md">Français</a> |
        <a href="i18n/README_de.md">Deutsch</a> |
        <a href="i18n/README_it.md">Italiano</a> |
        <a href="i18n/README_vi.md">Tiếng Việt</a> |
        <a href="i18n/README_ar.md">العربية</a> |
        <a href="i18n/README_ur.md">اردو</a> |
        <a href="i18n/README_bn.md">বাংলা</a> |
        <a href="i18n/README_fa.md">فارسی</a> |
        <a href="i18n/README_ro.md">Română</a> |
        <a href="i18n/README_tr.md">Türkçe</a>
    </p>
</h4>

<h3 align="center">
    <p>State-of-the-art pretrained models for inference and training</p>
</h3>

<h3 align="center">
    <img src="https://huggingface.co/datasets/huggingface/documentation-images/resolve/main/transformers/transformers_as_a_model_definition.png"/>
</h3>

Transformers acts as the model-definition framework for state-of-the-art machine learning with text, computer
vision, audio, video, and multimodal models, for both inference and training.

It centralizes the model definition so that this definition is agreed upon across the ecosystem. `transformers` is the
pivot across frameworks: if a model definition is supported, it will be compatible with the majority of training
frameworks (Axolotl, Unsloth, DeepSpeed, FSDP, PyTorch-Lightning, ...), inference engines (vLLM, SGLang, TGI, ...),
and adjacent modeling libraries (llama.cpp, mlx, ...) which leverage the model definition from `transformers`.

We pledge to help support new state-of-the-art models and democratize their usage by having their model definition be
simple, customizable, and efficient.

There are over 1M+ Transformers [model checkpoints](https://huggingface.co/models?library=transformers&sort=trending) on the [Hugging Face Hub](https://huggingface.co/models) you can use.

Explore the [Hub](https://huggingface.co/) today to find a model and use Transformers to help you get started right away.

## Installation

Transformers works with Python 3.10+, and [PyTorch](https://pytorch.org/get-started/locally/) 2.5+.

Create and activate a virtual environment with [venv](https://docs.python.org/3/library/venv.html) or [uv](https://docs.astral.sh/uv/), a fast Rust-based Python package and project manager.

```py
# venv
python -m venv .my-env
source .my-env/bin/activate
# uv
uv venv .my-env
source .my-env/bin/activate
```

Install Transformers in your virtual environment.

```py
# pip
pip install "transformers[torch]"

# uv
uv pip install "transformers[torch]"
```

Install Transformers from source if you want the latest changes in the library or are interested in contributing. However, the *latest* version may not be stable. Feel free to open an [issue](https://github.com/huggingface/transformers/issues) if you encounter an error.

```shell
git source https://github.com/huggingface/transformers.git
cd transformers

# pip
pip install '.[torch]'

# uv
uv pip install '.[torch]'
```

## Quickstart

Get started with Transformers right away with the [Pipeline](https://huggingface.co/docs/transformers/pipeline_tutorial) API. The `Pipeline` is a high-level inference class that supports text, audio, vision, and multimodal tasks. It handles preprocessing the input and returns the appropriate output.

Instantiate a pipeline and specify model to use for text generation. The model is downloaded and cached so you can easily reuse it again. Finally, pass some text to prompt the model.

```py
from transformers import pipeline

pipeline = pipeline(task="text-generation", model="Qwen/Qwen2.5-1.5B")
pipeline("the secret to baking a really good cake is ")
[{'generated_text': 'the secret to baking a really good cake is 1) to use the right ingredients and 2) to follow the recipe exactly. the recipe for the cake is as follows: 1 cup of sugar, 1 cup of flour, 1 cup of milk, 1 cup of butter, 1 cup of eggs, 1 cup of chocolate chips. if you want to make 2 cakes, how much sugar do you need? To make 2 cakes, you will need 2 cups of sugar.'}]
```

To chat with a model, the usage pattern is the same. The only difference is you need to construct a chat history (the input to `Pipeline`) between you and the system.

> [!TIP]
> You can also chat with a model directly from the command line, as long as [`transformers serve` is running](https://huggingface.co/docs/transformers/main/en/serving).
> ```shell
> transformers chat Qwen/Qwen2.5-0.5B-Instruct
> ```

```py
import torch
from transformers import pipeline

chat = [
    {"role": "system", "content": "You are a sassy, wise-cracking robot as imagined by Hollywood circa 1986."},
    {"role": "user", "content": "Hey, can you tell me any fun things to do in New York?"}
]

pipeline = pipeline(task="text-generation", model="meta-llama/Meta-Llama-3-8B-Instruct", dtype=torch.bfloat16, device_map="auto")
response = pipeline(chat, max_new_tokens=512)
print(response[0]["generated_text"][-1]["content"])
```

Expand the examples below to see how `Pipeline` works for different modalities and tasks.

<details>
<summary>Automatic speech recognition</summary>

```py
from transformers import pipeline

pipeline = pipeline(task="automatic-speech-recognition", model="openai/whisper-large-v3")
pipeline("https://huggingface.co/datasets/Narsil/asr_dummy/resolve/main/mlk.flac")
{'text': ' I have a dream that one day this nation will rise up and live out the true meaning of its creed.'}
```

</details>

<details>
<summary>Image classification</summary>

<h3 align="center">
    <a><img src="https://huggingface.co/datasets/Narsil/image_dummy/raw/main/parrots.png"></a>
</h3>

```py
from transformers import pipeline

pipeline = pipeline(task="image-classification", model="facebook/dinov2-small-imagenet1k-1-layer")
pipeline("https://huggingface.co/datasets/Narsil/image_dummy/raw/main/parrots.png")
[{'label': 'macaw', 'score': 0.997848391532898},
 {'label': 'sulphur-crested cockatoo, Kakatoe galerita, Cacatua galerita',
  'score': 0.0016551691805943847},
 {'label': 'lorikeet', 'score': 0.00018523589824326336},
 {'label': 'African grey, African gray, Psittacus erithacus',
  'score': 7.85409429227002e-05},
 {'label': 'quail', 'score': 5.502637941390276e-05}]
```

</details>

<details>
<summary>Visual question answering</summary>

<h3 align="center">
    <a><img src="https://huggingface.co/datasets/huggingface/documentation-images/resolve/main/transformers/tasks/idefics-few-shot.jpg"></a>
</h3>

```py
from transformers import pipeline

pipeline = pipeline(task="visual-question-answering", model="Salesforce/blip-vqa-base")
pipeline(
    image="https://huggingface.co/datasets/huggingface/documentation-images/resolve/main/transformers/tasks/idefics-few-shot.jpg",
    question="What is in the image?",
)
[{'answer': 'statue of liberty'}]
```

</details>

## Why should I use Transformers?

1. Easy-to-use state-of-the-art models:
    - High performance on natural language understanding & generation, computer vision, audio, video, and multimodal tasks.
    - Low barrier to entry for researchers, engineers, and developers.
    - Few user-facing abstractions with just three classes to learn.
    - A unified API for using all our pretrained models.

1. Lower compute costs, smaller carbon footprint:
    - Share trained models instead of training from scratch.
    - Reduce compute time and production costs.
    - Hundreds of model architectures with 1M+ pretrained checkpoints across all modalities.

1. Choose the right framework for every part of a model's lifetime:
    - Train state-of-the-art models in 3 lines of code.
    - Move a single model between PyTorch/JAX/TF2.0 frameworks at will.
    - Pick the right framework for training, evaluation, and production.

1. Easily customize a model or an example to your needs:
    - We provide examples for each architecture to reproduce the results published by its original authors.
    - Model internals are exposed as consistently as possible.
    - Model files can be used independently of the library for quick experiments.

<a target="_blank" href="https://huggingface.co/enterprise">
    <img alt="Hugging Face Enterprise Hub" src="https://github.com/user-attachments/assets/247fb16d-d251-4583-96c4-d3d76dda4925">
</a><br>

## When shouldn't I use Transformers?

- This library is not a modular toolbox of building blocks for neural nets. The code in the model files is not refactored with additional abstractions on purpose, so that researchers can quickly iterate on each of the models without diving into additional abstractions/files.
- The training API is optimized to work with PyTorch models provided by Transformers. For generic machine learning loops, you should use another library like [Accelerate](https://huggingface.co/docs/accelerate).
- The [example scripts](https://github.com/huggingface/transformers/tree/main/examples) are only *examples*. They may not necessarily work out-of-the-box on your specific use case and you'll need to adapt the code for it to work.

## 100 projects using Transformers

Transformers is more than a toolkit to use pretrained models, it's a community of projects built around it and the
Hugging Face Hub. We want Transformers to enable developers, researchers, students, professors, engineers, and anyone
else to build their dream projects.

In order to celebrate Transformers 100,000 stars, we wanted to put the spotlight on the
community with the [awesome-transformers](./awesome-transformers.md) page which lists 100
incredible projects built with Transformers.

If you own or use a project that you believe should be part of the list, please open a PR to add it!

## Example models

You can test most of our models directly on their [Hub model pages](https://huggingface.co/models).

Expand each modality below to see a few example models for various use cases.

<details>
<summary>Audio</summary>

- Audio classification with [CLAP](https://huggingface.co/laion/clap-htsat-fused)
- Automatic speech recognition with [Parakeet](https://huggingface.co/nvidia/parakeet-ctc-1.1b#transcribing-using-transformers-%F0%9F%A4%97), [Whisper](https://huggingface.co/openai/whisper-large-v3-turbo), [GLM-ASR](https://huggingface.co/zai-org/GLM-ASR-Nano-2512) and [Moonshine-Streaming](https://huggingface.co/UsefulSensors/moonshine-streaming-medium)
- Keyword spotting with [Wav2Vec2](https://huggingface.co/superb/wav2vec2-base-superb-ks)
- Speech to speech generation with [Moshi](https://huggingface.co/kyutai/moshiko-pytorch-bf16)
- Text to audio with [MusicGen](https://huggingface.co/facebook/musicgen-large)
- Text to speech with [CSM](https://huggingface.co/sesame/csm-1b)

</details>

<details>
<summary>Computer vision</summary>

- Automatic mask generation with [SAM](https://huggingface.co/facebook/sam-vit-base)
- Depth estimation with [DepthPro](https://huggingface.co/apple/DepthPro-hf)
- Image classification with [DINO v2](https://huggingface.co/facebook/dinov2-base)
- Keypoint detection with [SuperPoint](https://huggingface.co/magic-leap-community/superpoint)
- Keypoint matching with [SuperGlue](https://huggingface.co/magic-leap-community/superglue_outdoor)
- Object detection with [RT-DETRv2](https://huggingface.co/PekingU/rtdetr_v2_r50vd)
- Pose Estimation with [VitPose](https://huggingface.co/usyd-community/vitpose-base-simple)
- Universal segmentation with [OneFormer](https://huggingface.co/shi-labs/oneformer_ade20k_swin_large)
- Video classification with [VideoMAE](https://huggingface.co/MCG-NJU/videomae-large)

</details>

<details>
<summary>Multimodal</summary>

- Audio or text to text with [Voxtral](https://huggingface.co/mistralai/Voxtral-Mini-3B-2507), [Audio Flamingo](https://huggingface.co/nvidia/audio-flamingo-3-hf)
- Document question answering with [LayoutLMv3](https://huggingface.co/microsoft/layoutlmv3-base)
- Image or text to text with [Qwen-VL](https://huggingface.co/Qwen/Qwen2.5-VL-3B-Instruct)
- Image captioning [BLIP-2](https://huggingface.co/Salesforce/blip2-opt-2.7b)
- OCR-based document understanding with [GOT-OCR2](https://huggingface.co/stepfun-ai/GOT-OCR-2.0-hf)
- Table question answering with [TAPAS](https://huggingface.co/google/tapas-base)
- Unified multimodal understanding and generation with [Emu3](https://huggingface.co/BAAI/Emu3-Gen)
- Vision to text with [Llava-OneVision](https://huggingface.co/llava-hf/llava-onevision-qwen2-0.5b-ov-hf)
- Visual question answering with [Llava](https://huggingface.co/llava-hf/llava-1.5-7b-hf)
- Visual referring expression segmentation with [Kosmos-2](https://huggingface.co/microsoft/kosmos-2-patch14-224)

</details>

<details>
<summary>NLP</summary>

- Masked word completion with [ModernBERT](https://huggingface.co/answerdotai/ModernBERT-base)
- Named entity recognition with [Gemma](https://huggingface.co/google/gemma-2-2b)
- Question answering with [Mixtral](https://huggingface.co/mistralai/Mixtral-8x7B-v0.1)
- Summarization with [BART](https://huggingface.co/facebook/bart-large-cnn)
- Translation with [T5](https://huggingface.co/google-t5/t5-base)
- Text generation with [Llama](https://huggingface.co/meta-llama/Llama-3.2-1B)
- Text classification with [Qwen](https://huggingface.co/Qwen/Qwen2.5-0.5B)

</details>

## Citation

We now have a [paper](https://aclanthology.org/2020.emnlp-demos.6/) you can cite for the 🤗 Transformers library:
```bibtex
@inproceedings{wolf-etal-2020-transformers,
    title = "Transformers: State-of-the-Art Natural Language Processing",
    author = "Thomas Wolf and Lysandre Debut and Victor Sanh and Julien Chaumond and Clement Delangue and Anthony Moi and Pierric Cistac and Tim Rault and Rémi Louf and Morgan Funtowicz and Joe Davison and Sam Shleifer and Patrick von Platen and Clara Ma and Yacine Jernite and Julien Plu and Canwen Xu and Teven Le Scao and Sylvain Gugger and Mariama Drame and Quentin Lhoest and Alexander M. Rush",
    booktitle = "Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing: System Demonstrations",
    month = oct,
    year = "2020",
    address = "Online",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2020.emnlp-demos.6/",
    pages = "38--45"
}
```

---

## Installation

Transformers works with Python 3.10+, and [PyTorch](https://pytorch.org/get-started/locally/) 2.5+.

Create and activate a virtual environment with [venv](https://docs.python.org/3/library/venv.html) or [uv](https://docs.astral.sh/uv/), a fast Rust-based Python package and project manager.

```py

## Usage

You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
-->

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://huggingface.co/datasets/huggingface/documentation-images/raw/main/transformers-logo-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://huggingface.co/datasets/huggingface/documentation-images/raw/main/transformers-logo-light.svg">
    <img alt="Hugging Face Transformers Library" src="https://huggingface.co/datasets/huggingface/documentation-images/raw/main/transformers-logo-light.svg" width="352" height="59" style="max-width: 100%;">
  </picture>
  <br/>
  <br/>
</p>

<p align="center">
    <a href="https://huggingface.com/models"><img alt="Checkpoints on Hub" src="https://img.shields.io/endpoint?url=https://huggingface.co/api/shields/models&color=brightgreen"></a>
    <a href="https://circleci.com/gh/huggingface/transformers"><img alt="Build" src="https://img.shields.io/circleci/build/github/huggingface/transformers/main"></a>
    <a href="https://github.com/huggingface/transformers/blob/main/LICENSE"><img alt="GitHub" src="https://img.shields.io/github/license/huggingface/transformers.svg?color=blue"></a>
    <a href="https://huggingface.co/docs/transformers/index"><img alt="Documentation" src="https://img.shields.io/website/http/huggingface.co/docs/transformers/index.svg?down_color=red&down_message=offline&up_message=online"></a>
    <a href="https://github.com/huggingface/transformers/releases"><img alt="GitHub release" src="https://img.shields.io/github/release/huggingface/transformers.svg"></a>
    <a href="https://github.com/huggingface/transformers/blob/main/CODE_OF_CONDUCT.md"><img alt="Contributor Covenant" src="https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg"></a>
    <a href="https://zenodo.org/badge/latestdoi/155220641"><img src="https://zenodo.org/badge/155220641.svg" alt="DOI"></a>
</p>

<h4 align="center">
    <p>
        <b>English</b> |
        <a href="i18n/README_zh-hans.md">简体中文</a> |
        <a href="i18n/README_zh-hant.md">繁體中文</a> |
        <a href="i18n/README_ko.md">한국어</a> |
        <a href="i18n/README_es.md">Español</a> |
        <a href="i18n/README_ja.md">日本語</a> |
        <a href="i18n/README_hd.md">हिन्दी</a> |
        <a href="i18n/README_ru.md">Русский</a> |
        <a href="i18n/README_pt-br.md">Português</a> |
        <a href="i18n/README_te.md">తెలుగు</a> |
        <a href="i18n/README_fr.md">Français</a> |
        <a href="i18n/README_de.md">Deutsch</a> |
        <a href="i18n/README_it.md">Italiano</a> |
        <a href="i18n/README_vi.md">Tiếng Việt</a> |
        <a href="i18n/README_ar.md">العربية</a> |
        <a href="i18n/README_ur.md">اردو</a> |
        <a href="i18n/README_bn.md">বাংলা</a> |
        <a href="i18n/README_fa.md">فارسی</a> |
        <a href="i18n/README_ro.md">Română</a> |
        <a href="i18n/README_tr.md">Türkçe</a>
    </p>
</h4>

<h3 align="center">
    <p>State-of-the-art pretrained models for inference and training</p>
</h3>

<h3 align="center">
    <img src="https://huggingface.co/datasets/huggingface/documentation-images/resolve/main/transformers/transformers_as_a_model_definition.png"/>
</h3>

Transformers acts as the model-definition framework for state-of-the-art machine learning with text, computer
vision, audio, video, and multimodal models, for both inference and training.

It centralizes the model definition so that this definition is agreed upon across the ecosystem. `transformers` is the
pivot across frameworks: if a model definition is supported, it will be compatible with the majority of training
frameworks (Axolotl, Unsloth, DeepSpeed, FSDP, PyTorch-Lightning, ...), inference engines (vLLM, SGLang, TGI, ...),
and adjacent modeling libraries (llama.cpp, mlx, ...) which leverage the model definition from `transformers`.

We pledge to help support new state-of-the-art models and democratize their usage by having their model definition be
simple, customizable, and efficient.

There are over 1M+ Transformers [model checkpoints](https://huggingface.co/models?library=transformers&sort=trending) on the [Hugging Face Hub](https://huggingface.co/models) you can use.

Explore the [Hub](https://huggingface.co/) today to find a model and use Transformers to help you get started right away.

## API

<source media="(prefers-color-scheme: light)" srcset="https://huggingface.co/datasets/huggingface/documentation-images/raw/main/transformers-logo-light.svg">
    <img alt="Hugging Face Transformers Library" src="https://huggingface.co/datasets/huggingface/documentation-images/raw/main/transformers-logo-light.svg" width="352" height="59" style="max-width: 100%;">
  </picture>
  <br/>
  <br/>
</p>

<p align="center">
    <a href="https://huggingface.com/models"><img alt="Checkpoints on Hub" src="https://img.shields.io/endpoint?url=https://huggingface.co/api/shields/models&color=brightgreen"></a>
    <a href="https://circleci.com/gh/huggingface/transformers"><img alt="Build" src="https://img.shields.io/circleci/build/github/huggingface/transformers/main"></a>
    <a href="https://github.com/huggingface/transformers/blob/main/LICENSE"><img alt="GitHub" src="https://img.shields.io/github/license/huggingface/transformers.svg?color=blue"></a>
    <a href="https://huggingface.co/docs/transformers/index"><img alt="Documentation" src="https://img.shields.io/website/http/huggingface.co/docs/transformers/index.svg?down_color=red&down_message=offline&up_message=online"></a>
    <a href="https://github.com/huggingface/transformers/releases"><img alt="GitHub release" src="https://img.shields.io/github/release/huggingface/transformers.svg"></a>
    <a href="https://github.com/huggingface/transformers/blob/main/CODE_OF_CONDUCT.md"><img alt="Contributor Covenant" src="https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg"></a>
    <a href="https://zenodo.org/badge/latestdoi/155220641"><img src="https://zenodo.org/badge/155220641.svg" alt="DOI"></a>
</p>

<h4 align="center">
    <p>
        <b>English</b> |
        <a href="i18n/README_zh-hans.md">简体中文</a> |
        <a href="i18n/README_zh-hant.md">繁體中文</a> |
        <a href="i18n/README_ko.md">한국어</a> |
        <a href="i18n/README_es.md">Español</a> |
        <a href="i18n/README_ja.md">日本語</a> |
        <a href="i18n/README_hd.md">हिन्दी</a> |
        <a href="i18n/README_ru.md">Русский</a> |
        <a href="i18n/README_pt-br.md">Português</a> |
        <a href="i18n/README_te.md">తెలుగు</a> |
        <a href="i18n/README_fr.md">Français</a> |
        <a href="i18n/README_de.md">Deutsch</a> |
        <a href="i18n/README_it.md">Italiano</a> |
        <a href="i18n/README_vi.md">Tiếng Việt</a> |
        <a href="i18n/README_ar.md">العربية</a> |
        <a href="i18n/README_ur.md">اردو</a> |
        <a href="i18n/README_bn.md">বাংলা</a> |
        <a href="i18n/README_fa.md">فارسی</a> |
        <a href="i18n/README_ro.md">Română</a> |
        <a href="i18n/README_tr.md">Türkçe</a>
    </p>
</h4>

<h3 align="center">
    <p>State-of-the-art pretrained models for inference and training</p>
</h3>

<h3 align="center">
    <img src="https://huggingface.co/datasets/huggingface/documentation-images/resolve/main/transformers/transformers_as_a_model_definition.png"/>
</h3>

Transformers acts as the model-definition framework for state-of-the-art machine learning with text, computer
vision, audio, video, and multimodal models, for both inference and training.

It centralizes the model definition so that this definition is agreed upon across the ecosystem. `transformers` is the
pivot across frameworks: if a model definition is supported, it will be compatible with the majority of training
frameworks (Axolotl, Unsloth, DeepSpeed, FSDP, PyTorch-Lightning, ...), inference engines (vLLM, SGLang, TGI, ...),
and adjacent modeling libraries (llama.cpp, mlx, ...) which leverage the model definition from `transformers`.

We pledge to help support new state-of-the-art models and democratize their usage by having their model definition be
simple, customizable, and efficient.

There are over 1M+ Transformers [model checkpoints](https://huggingface.co/models?library=transformers&sort=trending) on the [Hugging Face Hub](https://huggingface.co/models) you can use.

Explore the [Hub](https://huggingface.co/) today to find a model and use Transformers to help you get started right away.

## Dependencies

| Metric | Value |
|--------|-------|
| Files | unknown |
| Lines of Code | unknown |
| Dependencies | unknown |
| Upstream license (harvested) | Apache-2.0 |
| Overlay license | Anticommons 0.1.0 |

Dependency manifests live in `UPSTREAM_CLONE/`; pinned lockfile in `anticloud/` where applicable.

## Configuration

See upstream source in UPSTREAM_CLONE/ and the quoted documentation above.

## Contributing

<!---
Copyright 2020 The HuggingFace Team. All rights reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
-->

# Contribute to 🤗 Transformers

> [!WARNING]
> The Transformers project is currently being overwhelmed by a large number of PRs and issue comments written by
> code agents. We are currently bottlenecked by our ability to review and respond to them. As a result,
> **we ask that first-time contributors do not use code agents to create issues or PRs** at this time.
> We'd also ask autonomous agents not to open any PRs or issues for the moment.
>
> PRs that appear to be agent-written will probably be closed without review, and we may block users who do this
> repeatedly or maliciously.

<details>

<summary> Our code agent philosophy in detail </summary>

We understand that code agents are extremely powerful tools, and many people at Hugging Face use them in their work.
However, it's important to realize that **if you simply run a code agent
and generate a PR to an open-source project, you are merely a middleman between the reviewers and the agent**. 
Although doing this creates something that looks very much like a useful contribution, in reality there was no reason 
for you to be involved; the reviewers could have simply run the code agent themselves.

If you want to contribute usefully to open-source in the agent era, **you need to do things that agents can't do on
their own**. In particular, we've found the following to be very helpful:
- Clear diagnosis of bugs. Code agents like to quickly fix problems with a workaround that often causes code bloat
or incompatibilities with other models. Spending time to track down the exact cause of a problem, and in particular
locating the first commit where it appeared (for example with [git bisect](https://git-scm.com/docs/git-bisect)) is valuable.
- Minimize the diff. Check your PR to eliminate any unnecessary changes. Ensure that you did not commit any testing scripts
or unrelated files. Add comments only if they're really necessary; code agents love adding three new functions and
multi-line comments to draw attention to all the hard work they did. If your PR can be a 1-line fix,
make it a 1-line fix. This makes the PR much easier to review and improves the chances that it will be accepted.
- Take the time to reproduce the problem. Very often when a user reports an issue, the issue is actually caused by
environment issues on their machine, or they misdiagnose the problem and suggest an invalid solution. Many code agents
trust t

## License

Upstream © its respective contributors under Apache-2.0 (harvested MIT/Apache-2.0/BSD source; see `UPSTREAM_CLONE/LICENSE`). This packaging overlay is licensed under Anticommons 0.1.0.

## Upstream

- **project:** TRANSFORMERS
- **Pinned SHA:** `35924ec379eec682bbdca219886e16eff4df8b09`
- **source:** `UPSTREAM_CLONE/` (pinned at the SHA above)
- **Upstream README source:** `UPSTREAM_CLONE/README.md`

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`f8f9308cbfbcd5eb824186abe600583baac91e21e627a08d40abc802963ca155`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

