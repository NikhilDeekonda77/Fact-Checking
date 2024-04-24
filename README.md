While large language models (LLMs) have revolutionized how we generate text, they also come with a concern: they can generate believable yet false information, often referred to as "hallucinations." This raises serious questions about their responsible use. Our project is all about finding a solution. We're aiming to pioneer a new approach to fact-checking that leverages cross-encoder models.
The Microsoft DeBERTa v3 large language model is an advanced natural language processing model developed by Microsoft. It represents an iteration of the DeBERTa (Decoding-enhanced BERT with disentangled attention) architecture, which introduces several improvements over previous models like BERT and RoBERTa.
DeBERTa improves upon the standard BERT model by using a disentangled attention mechanism. This mechanism separates the representation of words into two vectors—one for content and one for position—allowing the model to understand the influence of word position and word content more effectively.

<img width="924" alt="cross" src="https://github.com/NikhilDeekonda77/Fact-Checking/assets/146599294/843cc824-3274-4948-9a7f-bbd537cd9146">

Our fact-checking model is built upon the CrossEncoder architecture, a powerful neural network model known for its effectiveness in sentence pair classification tasks. Unlike traditional architectures that employ separate encoder networks for each sentence in a pair, the CrossEncoder model processes both sentences simultaneously, facilitating richer semantic understanding and contextualization.
The CrossEncoder model consists of multiple layers of neural network units, including transformer layers, which are pivotal for capturing complex relationships and dependencies within and across sentences. These transformer layers employ self-attention mechanisms, enabling the model to focus on relevant parts of the input sentences while suppressing noise and irrelevant information.
We have opted for a custom training approach for our fact-checking model. Our decision to pursue custom training stems from the unique requirements of fact-checking, which necessitate a model optimized for discerning factual accuracy. We trained the model on Google Cloud Platform with 4vCPUS and 16GB RAM under Tensorflow 2.6 Environment.
Dataset Acquisition and Preprocessing
Our primary datasets for training are
• PAWS(Paraphrase Adversaries from Word Scrambling),
• SNLI(Standard Natural Language Inference),
• MultiNLI (Multi-Genre Natural Language Inference) dataset - benchmark datasets for natural language understanding tasks.
Acquisition
The datasets were obtained from the Hugging Face ‘datasets‘ repository, a comprehensive collection of datasets for NLP research. We utilized the ‘load dataset‘ function to seamlessly access and download these datasets for integration into our training pipeline.
