## oobabooga/text-generation-webui

https://github.com/oobabooga/text-generation-webui

One of the best frontends so far, recommended for beginners. It supports multiple engines and comes preconfigured to work with virtually all notable models. Includes Web UI and REST API.

### Installation

While there are [one-click installers](https://github.com/oobabooga/text-generation-webui#one-click-installers), these can force you to use hardcoded dependencies. As a result, it's better to install textgen into a virtual environment. The repository's Readme only mentions Conda as it's simpler to install on Windows, but it's not strictly required. A basic virtual environment will suffice:

```bash
git clone https://github.com/oobabooga/text-generation-webui
python -m venv venv
. ./venv/bin/activate
pip install -r requirements.txt
```

Update pytorch and llama-cpp-python:

```bash
pip install -U --pre torch torchvision -f https://download.pytorch.org/whl/nightly/cpu/torch_nightly.html
pip install -U llama-cpp-python
```

The final command is especially useful when llama.cpp breaks compatibility for the nth time, and textgen devs take their time to update dependencies.

### Adding models

The User Interface provides an option to download models directly from HuggingFace. Be aware that it will clone the entire repository, which at times includes over 100GB of unrelated files (such as unnecessary checkpoints, training sets, alternative quantizations).

Alternatively, you can place model files within the `models/` directory.

## llama.cpp

https://github.com/ggerganov/llama.cpp

Currently, llama.cpp is the state-of-the-art tool for running inference on a CPU. It features its unique format (GGML) and several quantization strategies. Recently, it has introduced limited GPU support.

However, the developers don't seem concerned about backward compatibility, frequently introducing breaking changes. On a few occasions this lack of stability has necessitated the re-download of quantized models.

## PyTorch

PyTorch is technically the most versatile engine and is certain to support any model you need. It's primarily used by academic researchers.

Designed for training rather than inference, PyTorch performs best with one or more CUDA GPUs. However, it's not optimized for budget hardware.
