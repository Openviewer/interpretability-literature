# Notes on interpretability 

## Overviews 

Miller. [Explanation in Artificial Intelligence: Insights from the Social Sciences](https://arxiv.org/abs/1706.07269). In *AIJ 2018*.

Molnar. [Interpretable machine learning. A Guide for Making Black Box Models Explainable](https://christophm.github.io/interpretable-ml-book/). 2019.

Murdoch et al. [Interpretable machine learning: definitions, methods, and applications](https://arxiv.org/abs/1901.04592). arxiv 2019. 

## Perspectives 

Rudin. [Stop explaining black box machine learning models for high stakes decisions and use interpretable models instead](https://www.nature.com/articles/s42256-019-0048-x.epdf?author_access_token=SU_TpOb-H5d3uy5KF-dedtRgN0jAjWel9jnR3ZoTv0M3t8uDwhDckroSbUOOygdba5KNHQMo_Ji2D1_SdDjVr6hjgxJXc-7jt5FQZuPTQKIAkZsBoTI4uqjwnzbltD01Z8QwhwKsbvwh-z1xL8bAcg%3D%3D). In *Nature 2019*.

Doshi-Velez and Kim. [Towards A Rigorous Science of Interpretable Machine Learning](https://arxiv.org/abs/1702.08608). arxiv 2017. 

Lipton. [The Mythos of Model Interpretability](https://arxiv.org/abs/1606.03490). In *WHI 2016*.

* The umbrella term "Explainable AI" encompasses at least three distinct notions : **transparency**, **explainability**, and **interpretability**.

Goodman and Flaxman. [European Union regulations on algorithmic decision-making and a "right to explanation"](https://arxiv.org/abs/1606.08813). In *WHI 2016*.

## Impact of explanations  

Strout et al. [Do Human Rationales Improve Machine Explanations?](https://www.aclweb.org/anthology/W19-4807/). In *ACL 2019*. 

* This paper shows that learning with rationales can also improve the quality of the machine's explanations as evaluated by human judges.

Ray et al. [Can You Explain That? Lucid Explanations Help Human-AI Collaborative Image Retrieval](https://arxiv.org/abs/1904.03285). In *AAAI 2019*.

## Evaluation critera and pitfalls of explanatory methods

Heo et al. [Fooling Neural Network Interpretations via Adversarial Model Manipulation](https://arxiv.org/abs/1902.02041). In *NeurIPS 2019*. 

* Saliency interpretation methods can be fooled via adversarial model manipulation---a model finetuning step that aims to radically alter the explanation without hurting the accuracy of the original model. 

* Similar work: 

    * Zheng et al. [Analyzing the Interpretability Robustness of Self-Explaining Models](https://arxiv.org/abs/1905.12429). In ICML 2019 Security and Privacy of Machine Learning Workshop. 

Wiegreffe and Pinter. [Attention is not not Explanation](https://arxiv.org/abs/1908.04626). In *EMNLP 2019*.

* Deteching the attention scores obtained by parts of the model degredes the model itself. A reliable adversary must also be trained. 
* Attention scores are used as poviding an explanation; not the explanation.

Serrano and Smith. [Is Attention Interpretable?](https://www.aclweb.org/anthology/P19-1282/). In *ACL 2019*.

Jain and Wallace. [Attention is not Explanation](https://www.aclweb.org/anthology/N19-1357/). In *NAACL 2019*.

> Attention provides an important way to explain the workings of neural models. 
> Implicit in this is the assumption that the inputs (e.g., words) accorded high attention weights are responsible for model output. 

* Attention is not strongly correlated with other, well-grounded feature-importance metrics.  
* Alternative distributions exist for which the model outputs near-identical prediction scores. 

Aïvodji et al. [Fairwashing: the risk of rationalization](https://arxiv.org/abs/1901.09749). In *ICML 2019*. 

* **Fairwashing** is prooting the false perception that a machine learning model respects some ethical values. 
* This paper shows that tt is possible to forge a fairer explanation from a truly unfair black box trough a process that the authors coin as **rationalization**.

Mittelstadt et al. [Explaining Explanations in AI]. In *FAT 2019*.

Adebayo et al. [Sanity Checks for Saliency Maps](https://arxiv.org/abs/1810.03292). In *NeurIPS 2018*.

Chandrasekaran et al. [Do explanations make VQA models more predictable to a human?](https://www.aclweb.org/anthology/D18-1128/). In *EMNLP 2018*.

* This paper measures how well a human "understands" a VQA model. The paper shows that people get better at predicting VQA model's behaviour using a few "training" examples, but that exisiting explanation modalities do not help make its failures or responses more predictable. 

Kindermans et al. [The (Un)reliability of saliency methods](https://arxiv.org/abs/1711.00867). In *ICLR 2018*.
 
 > Evaluating the reliability of saliency methods is complicated by a lack of ground truth, as ground truth would depend upon full transparency into how a model arrives at a decision---the very problem we are trying to solve for in the first place.
 
 *  A new evaluation criterion, **input invariance**, requires that the saliency method mirrors the sensitivity of model with respect to transformations of the input. Input transformations that do not change network's prediction, should not change the attribution either. 

Feng et al. [Pathologies of Neural Models Make Interpretations Difficult](https://www.aclweb.org/anthology/D18-1407/). In *EMNLP 2018*.

 * Input reduction iteratively removes the least important word from the input.    
 * The remaining words appear nonsensical to humans and are not the ones determined as important by interpretation method.
 
 Poerner et al. [Evaluating neural network explanation methods using hybrid documents and morphosyntactic agreement](https://www.aclweb.org/anthology/P18-1032/). In *ACL 2018*.

  * Important characterization of explanation:   
  > A good explanation method should not reflect what humans attend to, but what task methods attend to.  
  * Interpretability differs between *small contexts* NLP tasks and *large context* tasks. 
  
 Sundararajan et al. [Axiomatic Attribution for Deep Networks](https://arxiv.org/abs/1703.01365). In *ICML 2017*.  
 
* **Implementation invariance**: the attributions should be identical for two functionally equivalent networks (their outputs are equal for all inputs, despite having very different implementations). 

* **Sensitivity**: if network assigns different predictions to two examples that differ in only one feature then the differing feature should be given a non-zero attribution.
 
 Das et al. [Human Attention in Visual Question Answering: Do Humans and Deep Networks look at the same regions?](https://www.aclweb.org/anthology/D16-1092/). In *EMNLP 2016*.
 
 * Current attention models in VQA do not seem to be looking at the same regions as humans.     

## Self-explanatory models / Model-based intepretability 


## Textual explanations generation 

Ehsan et al. [Computer Science > Artificial Intelligence
Automated Rationale Generation: A Technique for Explainable AI and its Effects on Human Perceptions](https://arxiv.org/abs/1901.03729). in *ACM IUI 2019*.

Kim et al. [Textual Explanations for Self-Driving Vehicles](https://arxiv.org/abs/1807.11546). In *ECCV 2018*.

Hendricks et al. [Generating Counterfactual Explanations with Natural Language](https://arxiv.org/abs/1806.09809). In *WHI 2018*. 

## Lectures 

[Interpretability and Explainability in Machine Learning at Harvard University](https://interpretable-ml-class.github.io/)

## Tutorials 

[Introduction to Interpretable Machine Learning by Been Kim @ MLSS 2018](https://beenkim.github.io/slides/DLSS2018Vector_Been.pdf)

