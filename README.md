Medical Keyword Extraction Pipeline: A Comparative Analysis
This project develops and evaluates a pipeline to automatically extract keywords from a large corpus of medical transcriptions. The core of the project is a comparative analysis of three distinct NLP methodologies to determine the most effective approach for this specialized domain.

The final, high-performing model is a fine-tuned T5-base Transformer, which learns to generate keywords in a sequence-to-sequence fashion.

🚀 Project Goal
The primary objective is to build a system that can accurately extract relevant keywords from medical reports. This aids in content summarization, improves data searchability, and facilitates better information retrieval in the medical field. The project scientifically evaluates the performance of the following approaches:

Statistical Baseline: A non-AI, statistical method (YAKE).

Pre-trained AI Baseline: An "off-the-shelf" semantic model (KeyBERT with a specialized BioBERT brain).

Fine-Tuned AI Solution: A T5-base model fine-tuned on the specific dataset.

🛠️ Methodology & Algorithms
The project followed a three-tiered approach to progressively build a more sophisticated and accurate solution.

1. Baseline 1: YAKE (Statistical Approach)
Algorithm: YAKE (Yet Another Keyword Extractor) is an unsupervised statistical algorithm.

Reasoning: Chosen to establish a strong, non-AI baseline. It answers the question: "How well can we do with a fast, purely statistical method?" This provides a crucial benchmark to justify the use of more complex models.

2. Baseline 2: KeyBERT (Pre-trained Semantic Approach)
Algorithm: KeyBERT utilizes a pre-trained SentenceTransformer model (pritamdeka/S-BioBert-snli-multinli-stsb) to find keywords based on semantic similarity between candidate phrases and the entire document.

Reasoning: This represents a powerful, "off-the-shelf" AI baseline using a model already specialized in biomedical text. It tests the effectiveness of a general pre-trained semantic understanding.

3. Advanced Solution: Fine-Tuning T5 (Generative Approach)
Algorithm: This approach reframes keyword extraction as a sequence-to-sequence task. We used the stable, official t5-base model from Google and fine-tuned it on our specific dataset.

Reasoning: This was the core experiment. The hypothesis was that by training the model on our specific data, it would learn not only the relevant medical concepts but also the specific style and structure of the desired keyword output, leading to superior performance.
