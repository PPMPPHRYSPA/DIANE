Thank you for your constructive ideas for our initial manuscript. 

Here is our response in *Methodology*:

- In DIANE, the reason that we consider a linear setup  with the Ising model framework is for simplicity and to illustrate the most essential idea of the divide-and-conquer (DnC) framework for non-convex optimization. While the current implementation of DIANE focuses on linear relationships, it can be easily  extended to address non-linear dependencies under a two-step setup. Specifically, if the  encoding matrix $\mathbf{U} = \mathbf{U}(\mathbf{z})$ is a nonlinear function of patient-level features $\mathbf{z}$ (e.g., gender, race, comorbidities, etc.), we can first get the DIANE encoding estimator $\widehat{\mathbf{U}}$ and then regress $\widehat{\mathbf{U}} (\mathbf{z}) \sim \mathbf{z}$ with non-linear approaches to estimate the nonlinear effect.
- For your question on considering the continuous variables like the lab measures, in fact, the model considered in our paper has the joint distribution $p(\mathbf{x}, \mathbf{y}) \propto \exp \Big(\mathbf{x}^{\scriptscriptstyle \sf{T}} \mathbf{U}^{\scriptscriptstyle \sf{T}} \mathbf{x} - \frac{1}{2} \mathbf{y}^{\scriptscriptstyle \sf{T}} \mathbf{y} \Big)$, with both the multi-dimensional binary variables  $\mathbf{x}$ and the latent continuous variables $\mathbf{y} \in \mathbb{R} ^ d$. To incorporate the continuous variables as you suggested, we can use the same model but have a part of continuous variables $\mathbf{y}$ visible and the proposed DIANE method can still work.

Our response in *Application* is listed below:

- As you suggested, we have extended the use of embeddings obtained by DIANE to several more downstream tasks with new results in the attachment. The DIANE-based embeddings are now employed to:
  - Detect pairs with pre-existing consensus on the relationship of similarity and/or relatedness. See Table 1 in the attachment.
  - Predict risks for patients in the UPMC database. See Table 2 in the attachment.
- The performance of DIANE is now measured by comparing it against a range of transformer-based benchmark language models, including BERT [<sup>1</sup>](#refer-anchor-1) and its
  variants [<sup>2</sup>](#refer-anchor-2) [<sup>3</sup>](#refer-anchor-3) [<sup>4</sup>](#refer-anchor-4). Our key findings include:
  - DIANE achieves a higher AUC in detecting known-relationship pairs, outperforming BERT and many of its variants, as shown in Table 1 in the attachment.
  - For risk prediction, DIANE achieves a lower Birer score than BERT and its variants, indicating a higher accuracy, as shown in Table 2 in the attachment.
- The additional results presented in our attachment will be integrated into an updated version of our work. A detailed explanation will accompany our updates.

To summarize the contents of our response, we will further elaborate on the potential *modeling limitations* to our work in the updated version in several aspects:

- We will consider a two-step approach for DIANE and explore the non-linear relationship between DIANE-based estimator $\widehat{\mathbf{U}}$ and patient-level features $\mathbf{z}$.
- We will implement DIANE under the scenario such that a proportion of the patient embedding $\mathbf{y}$ is revealed, which mimics the setup where we have EHR data in formalities beyond mere code/CUI co-occurrence patterns.
- We will perform experiments on publicly available EHR cohorts, such as MIMIC, and compare DIANE's performance with benchmark methods on multiple tasks to evaluate the utility of DIANE in diverse scenarios and ensure reproducibility.

We believe that these additional details address the points mentioned in your comments and further 
demonstrate the validity and significance of our approach.

### Reference

<div id="refer-anchor-1"></div>
[1] Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. BERT: pre-training of deep
bidirectional transformers for language understanding. In Proceedings of the 2019 Conference of the North
American Chapter of the Association for Computational Linguistics: Human Language Technologies,
NAACL-HLT, pages 4171–4186, 2019.

<div id="refer-anchor-2"></div>
[2] Yu Gu, Robert Tinn, Hao Cheng, Michael Lucas, Naoto Usuyama, Xiaodong Liu, Tristan Naumann,
Jianfeng Gao, and Hoifung Poon. Domain-specific language model pretraining for biomedical natural
language processing. ACM Transactions on Computing for Healthcare, 3:1–23, 2021.

<div id="refer-anchor-3"></div>
[3] Jinhyuk Lee, Wonjin Yoon, Sungdong Kim, Donghyeon Kim, Sunkyu Kim, Chan Ho So, and Jaewoo
Kang. BioBERT: a pre-trained biomedical language representation model for biomedical text mining.
Bioinformatics, 36(4):1234–1240, 2020.

<div id="refer-anchor-4"></div>
[4] Fangyu Liu, Ehsan Shareghi, Zaiqiao Meng, Marco Basaldella, and Nigel Collier. Self-alignment
pretraining for biomedical entity representations. In Proceedings of the 2021 Conference of the North
American Chapter of the Association for Computational Linguistics: Human Language Technologies,
pages 4228–4238, 2021.

