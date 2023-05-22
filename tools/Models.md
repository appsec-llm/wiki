## tl;dr

Start by determining the maximum size of the model your system can run. For instance, with 16GB RAM, you can operate 13B models (4-bit quantized). With 32GB RAM, you can manage 30B models, and with 64GB, 65B models become feasible.

Take note of the processing speed; llama.cpp generates roughly three tokens per second using 30B models and one token per second when utilizing a 65B model.

To discover new models, visit [HuggingFace](https://huggingface.co/models?sort=modified). Make sure to sort by Recent Activity since new versions are released daily.

While there are several metrics for comparing models, none are perfect. HuggingFace is compiling an LLM leaderboard worth checking, but due to their evaluation queue being weeks long, the results lag behind the release of new models. For more, see the [Open LLM Leaderboard](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard).

### Model Recommendations

Depending on your capacity, here are a few models to consider initially:

#### 13B Models

- [TheBloke/Manticore-13B-GGML](https://huggingface.co/TheBloke/Manticore-13B-GGML)
- [TheBloke/gpt4-x-vicuna-13B-GGML](https://huggingface.co/TheBloke/gpt4-x-vicuna-13B-GGML)

#### 30B Models

- [TheBloke/WizardLM-30B-Uncensored-GGML](https://huggingface.co/TheBloke/WizardLM-30B-Uncensored-GGML)
- [TheBloke/VicUnlocked-30B-LoRA-GGML](https://huggingface.co/TheBloke/VicUnlocked-30B-LoRA-GGML)
- [TheBloke/OpenAssistant-SFT-7-Llama-30B-GGML](https://huggingface.co/TheBloke/OpenAssistant-SFT-7-Llama-30B-GGML)
- [TheBloke/gpt4-alpaca-lora-30B-4bit-GGML](https://huggingface.co/TheBloke/gpt4-alpaca-lora-30B-4bit-GGML)

#### 65B Models

- [TheBloke/gpt4-alpaca-lora_mlp-65B-GGML](https://huggingface.co/TheBloke/gpt4-alpaca-lora_mlp-65B-GGML)
- [TheBloke/alpaca-lora-65B-GGML](https://huggingface.co/TheBloke/alpaca-lora-65B-GGML)

(Yes, TheBloke is amazing)
