# An Evaluation of Lightweight LLM Approaches to Enhancing Pre-Consultation Patient Questioning

Full write-ups and presentations in the WriteUp folder

## Introduction

As artificial intelligence has become prevalent in modern society, its presence in the medical field has been closely looked at as errors and incorrect diagnosis have the potential to result in great harm to someone. In this project, I looked at one aspect of the medical field where artificial intelligence has the possibility in our current state of development to help without the potential for large negative consequences—that of follow-up questions instead of diagnoses. The project looks at language learning model’s capability to prompt a person seeking medical answers for more relevant information to diminish the potential back and forth between a patient and a medical provider—effectively streamlining the pre-consultation phase and supporting better clinical decision-making.


Looking at related studies, the MediQ framework employs a dual-system that alternates between patient queries and expert evaluation to guide follow-up questions, illustrating the value of structured information gathering in clinical settings (Li et al., 2024). Additionally, research on patient messaging emphasizes how efficient communication can alleviate provider burnout, reinforcing the need for streamlined, targeted inquiries (Huang et al., 2022). While these studies often focus on diagnostic decision-making or extensive multi-turn dialogues, my approach diverges by utilizing a lightweight, single-response model solely aimed at prompting patients for critical information, thereby complementing and extending current methodologies in medical dialogue systems.


I approached the problem by first building a comprehensive database from the r/AskDocs subreddit, compiling a list of titles and posts with corresponding follow-up questions asked by verified medical professionals. I then fine-tuned LLMs on this data and asked them to generate questions based on posts. Then, I took the generated follow-ups as well as my baseline follow-ups of GPT 4o-mini’s questions, and had GPT 4o-mini-2024-07-18 evaluate the strength of the generated responses on four different axes (Utility, Necessity, Completeness, and Clarity) using a five-point Likert scale, where one is minimally embodying that feature and five is greatly embodying that feature.


While fine-tuning improved performance, model size was the primary factor in generating high-quality follow-up questions. Smaller models, even when trained, lagged behind GPT-4o-mini, which consistently outperformed them across all metrics. Fine-tuning provided slight gains, but large models remained significantly superior for this task.


Key Contributions
* Lightweight LLM exploration for cost-effective medical follow-up question generation.
* Fine-tuning on r/AskDocs data, leveraging real patient-provider interactions.
* Comprehensive evaluation framework using GPT-4o-mini for multi-metric assessment.
* Trade-off insights between model size and fine-tuning, highlighting large models' superiority.


## Conclusion
This study explored the feasibility of using lightweight, fine-tuned LLMs to generate follow-up medical questions, aiming to streamline patient-provider communication. By training models on a dataset of r/AskDocs posts and evaluating their performance across utility,
necessity, completeness, and clarity, we assessed their effectiveness compared to GPT-4o mini.


Results showed that while fine-tuning improved question generation, model size remained the most significant factor in performance. Larger models consistently outperformed smaller ones, highlighting the limitations of parameter-constrained LLMs for this task. These findings suggest that while fine-tuning enhances specialized capabilities, robust question generation in medical contexts still demands larger-scale architectures. Future work could explore refining training methodologies and leveraging multimodal data to improve performance in real-world applications.
