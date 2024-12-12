
Zero-Shot Image Captioning

Project Overview

This project focuses on developing a model that generates captions for images in languages it has never been trained on. The model leverages linguistic structure inferred from a few text examples in the target language and visual context extracted from the image. The goal is to achieve semantic and contextual correctness without direct training on the target language.

Features

Zero-shot learning for generating captions in unseen languages.

Multimodal architecture combining visual and language models.

Few-shot adaptation using text examples in the target language.

Focus on contextual and semantic alignment between image and language.

Architecture

Visual Encoder

CLIP (Contrastive Language-Image Pretraining)

Extracts image embeddings.

Provides a shared embedding space for vision and text.

Multilingual Text Decoder

Transformer-based decoder (e.g., mBART or XLM-R):

Processes text examples in the target language.

Infers syntactic and semantic structure.

Cross-Modal Alignment

Cross-attention mechanism aligns visual and linguistic embeddings.

Text examples guide language-specific adaptation.

Caption Generation

Combines visual embeddings and linguistic patterns to produce captions.
