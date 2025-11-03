# Introduction
To Evaluate a RAG system first we need to know how they work. RAG or Retrieval Augmented Generation works justl like an LLM but with extra infromation about a subject which is provided before user interacts with it. To evaluate a RAG application we need to have or do these things:
1. Have or create a dataset to test with
2. Run the RAG application on the created dataset
3. Measure it's performance usiing different evaluation metrics

# Tools, Metrics and Methods for Evaluation

## Metrics 
While it seems normal metrics are not the best fro this type of testing it still seems like a solid starting point for it. Some of the more effective ones are:
* Precision@k: proportion of top-k retrieved docs that are relevant.
* Recall@k: proportion of all relevant docs that appear in top-k.
* Mean Average Precision (MAP): balances precision and recall.
* nDCG (normalized Discounted Cumulative Gain): rewards correct ranking order.

As you probably noticed these are mostly for reterival part of the RAG application and not the generation and for that we can use teh following datasets:
* MS MARCO(https://microsoft.github.io/msmarco/)
* Natural Questions(https://ai.google.com/research/NaturalQuestions)
* HotpotQA(https://hotpotqa.github.io/)

### Interpret Results
* High Recall, Low Precision → retriever finds all relevant docs but also a lot of irrelevant noise.
* Low Recall, High Precision → retriever misses some relevant docs but those it finds are good.
* Low nDCG → relevant docs are buried deep in the ranking.
* Good MAP → your ranking is balanced and consistent.

## Methods
These ones are more tailored to test out the Generation part of the RAG application and which happens after retrival in thsi fashion:                  
* Query + Retrieved Documents → Generated Answer 

Metrics for this part are:
* Faithfulness / Groundedness: does it stay true to retrieved sources?
* Relevance: is the answer actually about the user’s question? 
* Fluency: is it well-written and coherent? Normally no problems here
* Factuality: does it contain hallucinations? even if the retrived documents are wrong, the model should not hallucinate and at least should say so. 

and testing methods for these are:
* ROUGE / BLEU / METEOR: lexical overlap (good for short answers).
<img width="580" height="177" alt="image" src="https://github.com/user-attachments/assets/7b35595e-1711-477a-a426-11cc72a15b05" />

* BERTScore / MoverScore: semantic similarity.
<img width="552" height="110" alt="image" src="https://github.com/user-attachments/assets/2ece8f09-bee3-4597-9e3f-a144ea6d825f" />

* GPT-based evaluation: use an evaluator LLM to rate correctness, faithfulness, etc.

# Sources
* https://docs.langchain.com/langsmith/evaluate-rag-tutorial#type-1-reference-answer
* https://github.com/docugami/KG-RAG-datasets/tree/main
* https://huggingface.co/datasets/rag-datasets/rag-mini-wikipedia
* https://www.reddit.com/r/Rag/comments/1ldhcly/are_there_any_good_rag_evaluation_metrics_or/
* https://docs.ragas.io/en/stable/getstarted/evals/
* https://www.youtube.com/watch?v=lTfhw_9cJqc
* https://www.youtube.com/watch?v=IlNglM9bKLw
* https://huggingface.co/learn/cookbook/en/rag_evaluation
