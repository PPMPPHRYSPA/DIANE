We appreciate your valuable comments and constructive suggestions on our manuscript.

For your questions in *Methodology*:

- We recognize and appreciate the concern you highlighted in your comments that our 30-day sliding window approach in EHR collection for each patient might overlook the long-term effects among different windows. In fact, integrating the temporal information within the DIANE framework is indeed feasible. Specifically, we treat the parameter matrix $\mathbf{U} = \mathbf{U} (t)$ as time-dependent. In this scenario, we estimate $\widehat {\mathbf{U}(t)}$ for some specific time $t \in \mathcal{T}$ and apply kernel smoothing across the timeframe $\mathcal{T}$ [<sup>1</sup>](#refer-anchor-1) [<sup>2</sup>](#refer-anchor-2) [<sup>3</sup>](#refer-anchor-3)

For your questions in *Application*:

- Despite being collected within a single healthcare system, it is common that the real-world EHR databases reside in different sites (e.g., locations, departments) within the system. Furthermore, the EHR data is usually massive even if stored in a single site, and chances are that it is necessary to distribute the data prior to analysis. Finding a universal approach to analyze EHR data under such a distributed setup remains an active research field [<sup>4</sup>](#refer-anchor-4) [<sup>5</sup>](#refer-anchor-5). Our experiments treat randomly distributed patient subgroups as if collected from different sites, which reflects a real-world distributed learning scenario.
- We have recently extended the application of DIANE to a new dataset of $17,421$ patients, involving both Alzheimer's Disease and multiple sclerosis (MS) cohorts in the UPMC system. A knowledge network corresponding to the larger-scale dataset is posted in Figure 1 of the attachment.
- We compared the embeddings obtained by DIANE and several benchmark language models, focusing on two main tasks: (1) detecting known-relationship pairs and (2) risk prediction on a large-scale dataset described above. DIANE shows superior performance in both tasks over existing methods, as evidenced by a higher AUC in detecting known relationship pairs and a lower Brier score (i.e., higher accuracy) for risk prediction. The results are posted in Table 1 and Table 2 in the attachment respectively.
- In the future, we will deploy DIANE on publicly available EHR cohorts, including MIMIC, to demonstrate the reproducibility of our work. Our code, along with the hyperparameter setup and other potentially publishable items, are available on GitHub.

We hope that these clarifications adequately address your comments. We are grateful for your feedback, 
which aids in refining and improving our work.

### References

<div id="refer-anchor-1"></div>
[1] Edward James Hannan and Laimonis Kavalieris. Regression, autoregression models. Journal of Time Series Analysis, 7(1):27–49, 1986.
<div id="refer-anchor-2"></div>
[2] Wim Meeus. Adolescent psychosocial development: A review of longitudinal models and research. Developmental Psychology, 52(12):1969, 2016.
<div id="refer-anchor-3"></div>
[3] Matt P Wand and M Chris Jones. Kernel smoothing. CRC press, 1994.
<div id="refer-anchor-4"></div>
[4] Bernd Blobel. Trustworthiness in distributed electronic healthcare records-basis for shared care. In
Seventeenth Annual Computer Security Applications Conference, pages 433–441. IEEE, 2001.
<div id="refer-anchor-5"></div>
[5] Jane Grimson, William Grimson, Damon Berry, Gaye Stephens, Eoghan Felton, Dipak Kalra, Pieter
Toussaint, and Onno W Weier. A corba-based integration of distributed electronic healthcare records
using the synapses approach. IEEE Transactions on information technology in biomedicine, 2(3):124–138,
1998.
