We sincerely appreciate the reviewers' time and effort in providing feedback on our manuscript. We are grateful for the insightful comments and suggestions that have undoubtedly enriched the quality of our work.

We have deployed the proposed algorithm, DIANE, on a new dataset from the University of Pittsburgh Medical Center (UPMC) between 2011-2021, which includes the EHR data for $15,906$ patients with multiple sclerosis (MS) diagnosis, $1,508$ patients with Alzheimer's Disease (AD) diagnosis and $7$ patients with both MS and AD. We collect all codified codes that are presented on more than $10\%$ patients, resulting in a total of $2,928$ features, including $705$ PheCode codes, $153$ CCS codes, $772$ LOINC codes, $539$ RxNorm codes, and $759$ other local codes like ICD-10-CM, local labs codes. To evaluate the performance of DIANE, we apply our algorithms on the following downstream tasks: (1) known relationship detecting, (2) risk prediction, and (3) patient phenotyping. We also compare the results based on our algorithms with that based on existing methods, including pretrained language model (PLM) embeddings based on BERT [1] and its variants [2,3,4]. We refer to the numerical results for the above tasks in the attachment.

In addition, our model and method can be easily generalized to take the temporal effect and nonlinear confounding effect into account. With the encoder estimator $\hat{\mathbf{U}}$ obtained by DIANE, it can be further regressed by the time or other continuous variables. 

### References

[1] Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. BERT: pre-training of deep
bidirectional transformers for language understanding. In *Proceedings of the 2019 Conference of the North
American Chapter of the Association for Computational Linguistics: Human Language Technologies*,
NAACL-HLT, pages 4171–4186, 2019.

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
