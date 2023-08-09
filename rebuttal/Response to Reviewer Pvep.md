Thank you for your constructive ideas for our initial manuscript. 

Here is our response in *Methodology*:

- In DIANE, we consider a linear setup to preserve its intrinsic connection with the Ising model framework and
  clearly illustrate the divide-and-conquer (DnC) layout [<sup>1</sup>](#refer-anchor-1). While the current implementation of DIANE focuses
  on linear relationships, it can be extended to address non-linear dependencies under a two-step setup.
  Specifically, we treat the parameter matrix $\mathbf{U} = \mathbf{U}(\mathbf{z})$ as a function of patient-level
  features $\mathbf{z}$ (e.g., gender, race, comorbidities, etc.) and then regress DIANE-based estimator
  $\widehat{\mathbf{U}(\mathbf{z})} \sim \mathbf{z}$ with non-linear approaches.

- Our approach that represents EHR data as multi-dimensional binary vectors not only captures the essential EHR
  patterns, namely the existence of specific EHR codes or CUIs, but also highlights the divide-and-conquer (DnC)
  feature of DIANE, which is a principal contribution of our work. This approach is considered appropriate and
  widely reflected in numerous peer-reviewed publications [<sup>2</sup>](#refer-anchor-2) [<sup>3</sup>](#refer-anchor-3).

- In our original work, we have proposed the joint distribution
  $p(\mathbf{x}, \mathbf{y}) \propto \exp \Big(\mathbf{x}^{\scriptscriptstyle \sf{T}} \mathbf{U}^{\scriptscriptstyle \sf{T}} \mathbf{x} - \frac{1}{2} \mathbf{y}^{\scriptscriptstyle \sf{T}} \mathbf{y} \Big)$,
  where $\mathbf{x}$ is a multi-dimensional binary representation of EHR codes or CUIs, and we assume that the
  patient embedding $\mathbf{y} \in \mathbb{R} ^ d$ is completely latent. To leverage the information embedded
  in other aspects of EHR, such as the lab data, we can fit the model as if a part of $\mathbf{y}$ is visible.
   Moreover, our two-step version of DIANE can be extended to include additional EHR-related information in
  different formalities, including numeric values and free-form text.

Our response in *Application* is listed below:

- We have extended the use of embeddings obtained by DIANE to several more downstream tasks with
  new results in the attachment. The DIANE-based embeddings are now employed to:
  - Detect pairs with pre-existing consensus on the relationship of similarity and/or relatedness
  - Predict risks for patients in the UPMC database
- The performance of DIANE is now measured by comparing it against a range of transformer-based benchmark
  language models, including BERT [<sup>4</sup>](#refer-anchor-4) and its
  variants [<sup>5</sup>](#refer-anchor-5) [<sup>6</sup>](#refer-anchor-6) [<sup>7</sup>](#refer-anchor-7). Our key findings include:
  - DIANE achieves a higher AUC in detecting known-relationship pairs, outperforming BERT and many
    of its variants, as shown in Table 1 in the attachment.
  - For risk prediction, DIANE achieves a lower Birer score than BERT and its variants, indicating
    a higher accuracy, as shown in Table 2 in the attachment.
- The additional results presented in our attachment will be integrated into an updated version of
  our work. A detailed explanation will accompany our updates.

To summarize the contents of our response, we will further elaborate on the potential *modeling limitations*
to our work in the updated version in several aspects:

- We will consider a two-step approach for DIANE and explore the non-linear relationship between
  DIANE-based estimator $\widehat{\mathbf{U}}$ and patient-level features $\mathbf{z}$.
- We will implement DIANE under the scenario such that a proportion of the patient embedding $\mathbf{y}$
  is revealed, which mimics the setup where we have EHR data in formalities beyond mere code/CUI
  co-occurrence patterns.
- We will perform experiments on publicly available EHR cohorts, such as MIMIC, and compare DIANE's
  performance with benchmark methods on multiple tasks to evaluate the utility of DIANE in diverse
  scenarios and ensure reproducibility.

We believe that these additional details address the points mentioned in your comments and further 
demonstrate the validity and significance of our approach.

**Reference**

<div id="refer-anchor-1"></div>
[1] D. M. Witten, R. Tibshirani, and T. Hastie. A penalized matrix decomposition, with applications to
sparse principal components and canonical correlation analysis. Biostatistics, 10(3):515–534, 2009.

<div id="refer-anchor-2"></div>
[2] Chuan Hong, Everett Rush, Molei Liu, Doudou Zhou, Jiehuan Sun, Aaron Sonabend, Victor M Castro,
Petra Schubert, Vidul A Panickan, Tianrun Cai, et al. Clinical knowledge extraction via sparse embedding
regression (keser) with multi-center large scale electronic health record data. NPJ digital medicine,
4(1):151, 2021.

<div id="refer-anchor-3"></div>
[3] Maxime Taquet, Quentin Dercon, Sierra Luciano, John R Geddes, Masud Husain, and Paul J Harrison.
Incidence, co-occurrence, and evolution of long-covid features: A 6-month retrospective cohort study of
273,618 survivors of covid-19. PLoS medicine, 18(9):e1003773, 2021.

<div id="refer-anchor-4"></div>
[4] Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. BERT: pre-training of deep
bidirectional transformers for language understanding. In Proceedings of the 2019 Conference of the North
American Chapter of the Association for Computational Linguistics: Human Language Technologies,
NAACL-HLT, pages 4171–4186, 2019.

<div id="refer-anchor-5"></div>
[5] Yu Gu, Robert Tinn, Hao Cheng, Michael Lucas, Naoto Usuyama, Xiaodong Liu, Tristan Naumann,
Jianfeng Gao, and Hoifung Poon. Domain-specific language model pretraining for biomedical natural
language processing. ACM Transactions on Computing for Healthcare, 3:1–23, 2021.

<div id="refer-anchor-6"></div>
[6] Jinhyuk Lee, Wonjin Yoon, Sungdong Kim, Donghyeon Kim, Sunkyu Kim, Chan Ho So, and Jaewoo
Kang. BioBERT: a pre-trained biomedical language representation model for biomedical text mining.
Bioinformatics, 36(4):1234–1240, 2020.

<div id="refer-anchor-7"></div>
[7] Fangyu Liu, Ehsan Shareghi, Zaiqiao Meng, Marco Basaldella, and Nigel Collier. Self-alignment
pretraining for biomedical entity representations. In Proceedings of the 2021 Conference of the North
American Chapter of the Association for Computational Linguistics: Human Language Technologies,
pages 4228–4238, 2021.

