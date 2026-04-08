##  GPT / Decoder-Only Transformers — генерация, sampling и RAG

### О чём пара

Практически и концептуально разбираем **decoder-only Transformer (GPT-класс)**:

* как работает **авторегрессивная генерация** (next-token prediction)
* почему нужен **causal mask** и как ускоряет генерацию **KV-cache**
* как разные стратегии decoding влияют на качество: **greedy, beam search, top-k, top-p (nucleus), temperature**
* зачем нужен **RAG** (retrieval-augmented generation): поиск знаний → добавление контекста в prompt → ответ

### Ключевые ссылки (must-read)

**База по трансформерам**

* *Attention Is All You Need* (Transformer): ([arXiv][1])
* Визуальное объяснение: *The Illustrated Transformer* (Jay Alammar): ([jalammar.github.io][2])

**GPT и instruction-tuning**

* GPT-2 paper (PDF): ([cdn.openai.com][3])
* GPT-3 paper (arXiv): ([arXiv][4])
* InstructGPT / RLHF (arXiv): ([arXiv][5])

**Sampling / decoding (top-k, top-p)**

* *The Curious Case of Neural Text Degeneration* — вводит **nucleus sampling (top-p)**: ([arXiv][6])

**RAG**

* *Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks*: ([arXiv][7])

### Инструменты/библиотеки (для практики)

* Hugging Face generation docs (параметры/стратегии): ([arXiv][6])
* FAISS (векторный поиск): ([GitHub][8])
* Sentence-Transformers (эмбеддинги): ([GitHub][9])
* Multilingual E5 embeddings (тех. отчёт): ([arXiv][10])

### Дополнительно (если хочется “с нуля”)

* Karpathy: *build-nanoGPT* (пошагово собрать GPT-2-уровня): ([GitHub][11])

[1]: https://arxiv.org/abs/1706.03762?utm_source=chatgpt.com "Attention Is All You Need"
[2]: https://jalammar.github.io/illustrated-transformer/?utm_source=chatgpt.com "The Illustrated Transformer – Jay Alammar – Visualizing machine ..."
[3]: https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf?utm_source=chatgpt.com "Language Models are Unsupervised Multitask Learners - OpenAI"
[4]: https://arxiv.org/abs/2005.14165?utm_source=chatgpt.com "[2005.14165] Language Models are Few-Shot Learners - arXiv.org"
[5]: https://arxiv.org/abs/2203.02155?utm_source=chatgpt.com "Training language models to follow instructions with human feedback"
[6]: https://arxiv.org/abs/1904.09751?utm_source=chatgpt.com "The Curious Case of Neural Text Degeneration"
[7]: https://arxiv.org/abs/2005.11401?utm_source=chatgpt.com "Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks"
[8]: https://github.com/facebookresearch/faiss?utm_source=chatgpt.com "GitHub - facebookresearch/faiss: A library for efficient similarity ..."
[9]: https://github.com/huggingface/sentence-transformers?utm_source=chatgpt.com "GitHub - huggingface/sentence-transformers: State-of-the-Art Text ..."
[10]: https://arxiv.org/abs/2402.05672?utm_source=chatgpt.com "Multilingual E5 Text Embeddings: A Technical Report"
[11]: https://github.com/karpathy/build-nanogpt?utm_source=chatgpt.com "GitHub - karpathy/build-nanogpt: Video+code lecture on building nanoGPT ..."