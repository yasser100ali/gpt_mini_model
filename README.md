PyTorch GPT Language Model

This repository contains a PyTorch implementation of a GPT-like language model for text generation. Below is a brief overview of the main components and usage.

Key Components

Hyperparameters

	•	batch_size: Number of sequences processed in parallel.
	•	block_size: Maximum context length.
	•	max_iters: Training iterations.
	•	eval_interval: Loss evaluation frequency.
	•	learning_rate: Optimizer learning rate.
	•	device: Training device (cuda or cpu).
	•	eval_iters: Iterations for loss evaluation.
	•	n_embd: Embedding dimension.
	•	n_head: Number of attention heads.
	•	n_layer: Number of transformer layers.
	•	dropout: Dropout rate.

Data Preparation -> Data from a variety of famous literary figues, most notably the greatest writer of all time in Fyodor Dostoevsky!!! ...And some other people like Shakespeare, Herman Melville, etc.

	•	Loads and tokenizes text data.
	•	Splits data into training and validation sets.
	•	get_batch(split) generates data batches.

Model Architecture

	•	Head: Single self-attention head.
	•	MultiHeadAttention: Multiple self-attention heads.
	•	FeedForward: Feedforward network with dropout.
	•	Block: Transformer block combining attention and feedforward layers.
	•	GPTLanguageModel: Main model class with token and positional embeddings, transformer blocks, and output layer.

Training and Evaluation

	•	Trains using AdamW optimizer.
	•	Evaluates loss periodically on training and validation data.
