This notebook implements a Supervised Fine-Tuning (SFT) pipeline:
The LLM: It uses Mistral 7B (mistralai/Mistral-7B-v0.1), a powerful open-source Large Language Model.

We load it in 4-bit mode so it fits on the A100 High RAM

The Dataset: It takes your small, custom dataset (dataset.json) containing specific examples (Instructions → Outputs) for your chosen task.

The Method: It uses LoRA (Low-Rank Adaptation). Instead of retraining the huge model from scratch (which is impossible on Colab), it freezes the main model and trains tiny "adapter" layers to learn your specific task.
