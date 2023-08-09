Thank you very much for your thorough and insightful comments on our manuscript, which have provided us with valuable perspectives. Below, we outline several key insights and actions we have taken in response to your comments:

- In our most recent experiment, the performance of DIANE is compared with a range of transformer-based benchmark language models, including BERT [1] and its variants [2,3,4], focusing on two downstream tasks:
  - Detecting pairs with pre-existing consensus on the relationship of similarity and/or relatedness; See Table 1 in the attachment.
  - Predicting risks for patients in the UPMC database. See Table 2 in the attachment.
- The performance evaluation for the above tasks is based on ground truth through manual annotation by specialists.
  - The known-relationship pairs are distinguished through manual annotation based on similarity (e.g., codes within the same family) and relatedness (e.g., A *may prevent* B).
  - For risk prediction, we have manually annotated gold-standard labels on whether the patients are diagnosed with Alzheimer's disease (AD) or multiple sclerosis (MS).
- The new results in the attachment have included not only based on the four domains of codified data mentioned in our original work, but on all available EHR codes in the UPMC database, including local codes like ICD-10-CM, local lab codes, and others. Such an update enhances the compatibility of our experiment with real-world applications.
- In our experiment, DIANE achieves a better overall performance than other tested models for both tasks. Our results are provided in Table 1 and Table 2 of our attachment, with explanations presented in our global response.

We believe these changes have strengthened the robustness and contribution of our study. We sincerely hope that our work is now more aligned with the expectations of the conference.

### References

[1] Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. BERT: pre-training of deep
bidirectional transformers for language understanding. In *Proceedings of the 2019 Conference of the North
American Chapter of the Association for Computational Linguistics: Human Language Technologies,
NAACL-HLT*, pages 4171–4186, 2019.

[2] Yu Gu, Robert Tinn, Hao Cheng, Michael Lucas, Naoto Usuyama, Xiaodong Liu, Tristan Naumann,
Jianfeng Gao, and Hoifung Poon. Domain-specific language model pretraining for biomedical natural
language processing. *ACM Transactions on Computing for Healthcare*, 3:1–23, 2021.

[3] Jinhyuk Lee, Wonjin Yoon, Sungdong Kim, Donghyeon Kim, Sunkyu Kim, Chan Ho So, and Jaewoo
Kang. BioBERT: a pre-trained biomedical language representation model for biomedical text mining.
*Bioinformatics*, 36(4):1234–1240, 2020.

[4] Fangyu Liu, Ehsan Shareghi, Zaiqiao Meng, Marco Basaldella, and Nigel Collier. Self-alignment
pretraining for biomedical entity representations. In *Proceedings of the 2021 Conference of the North
American Chapter of the Association for Computational Linguistics: Human Language Technologies*,
pages 4228–4238, 2021.
