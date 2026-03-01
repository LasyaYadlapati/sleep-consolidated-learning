# Sleep-Consolidated Learning and Plasticity Decay
## Introduction
Language Models (LMs), while powerful, are extremely resource-intensive to train. 
Effective LMs require hundreds of times more data to build an understanding of language than human children, often more text than a human will ever be exposed to in their entire lifetime. 
For example, ELMo and BERT were both trained on billions of words, RoBERTa was trained on 30 billion words, and Meta AI’s Llama 4 was trained on around 30 trillion words<sup>11</sup>,<sup>1</sup>.
In comparison,<sup>3</sup> estimate that human children are exposed to about 3 million to 11 million words per year.
That means in order to acquire and use language in a meaningful way, LMs see hundreds to millions of years’ worth of linguistic content<sup>11</sup>.
The resource requirements to build an effective language model from random initialization (also known as pre-training) restrict language model research to larger organizations with lots of funding, making academic research of LM pre-training difficult and costly.

Most neural language models are also trained on data over multiple epochs.
This means that over the course of a training run, the model will see the same dataset anywhere from hundreds to thousands of times.
This is entirely different from how humans acquire language: we live through every day once, and experience everything only once.
In addition to not being cognitively plausible, epoch training also potentially wastes computational resources.
Different samples of the data will have different difficulty levels that determine how easily the model can learn their patterns.
Epoch training means that even after the model has mastered easier samples, it is still re-trained on those same samples in the same contexts as before, leading to overfitting and shortcut learning, where the model picks up on spurious relationships rather than learning real semantic content<sup>13</sup>.
This disconnect between the training schedules of LMs and human language acquisition not only could contribute to their inefficiency, but also means that there are strong limitations in the use and interpretation of LMs as cognitive models.

Humans, however, do revisit experiences in a critical stage for cognitive development: sleep.
Neuroscience research has shown that sleep is not just a period of rest, but critical for developing memories.
While the waking brain is optimized for encoding new experiences into memory, during sleep, the brain undergoes a process called *memory consolidation*, where they are stabilized and integrated into pre-existing synaptic networks rasch2013sleep.
This two-stage process for memory formation assumes that, because long-term memory stores take longer to train and short-term memory is easily overwritten by new experiences, sleep provides an essential off-line environment, where recent experiences are revisited repeatedly to gradually integrate into long-term stores without overwriting older memories<sup>5</sup>.
By consolidating abstract representations of our memories in sleeping periods, humans also retain world knowledge and episodic memory of recent events (declarative memory) as well as intuition and unconscious long-term memories that influence their behavior (non-declarative memory), both of which are important for learning complex skills such as language rasch2013sleep.

Another process that happens during sleep as a part of *memory consolidation* is *synaptic homeostasis*.
During waking hours, synapses are constantly strengthening and firing strongly, making it easier to learn and encode new information.
However, this comes with a high resource cost; stronger synaptic connections need more energy and place extra stress on neurons<sup>10</sup>.
Additionally, neurons with stronger synaptic connections may fire for random chance, effectively wasting resources<sup>2</sup>.
Thus, during sleep, synapses renormalize through a down-selection process.
As memories are revisited, synapses that consistently fire strongly are kept, whereas synapses that do not fire as strongly are downscaled.
This has the effect that important synapses with strong signals are strengthened and consolidated, becoming more resistant to decay, while less important connections are reduced or even pruned to reduce resource costs<sup>10</sup>.

It is clear that sleep is a process of utmost importance for cognitive development, and contributes to how humans are able to quickly encode and retain information from recent experiences without truly experiencing them more than once. In this project, will explore sleep-inspired, cognitively-plausible training schedules for language models in the hopes of producing data-efficient training paradigms that diverge from standard multi-epoch conventions.
## Methods

## Results

## Conclusion

## Limitations and Future Work

## References
1. Aaron Grattafiori et al.. 2024. “The Llama 3 Herd of Models.” [Link](https://arxiv.org/abs/2407.21783)
2. Balduzzi, D., and G. Tononi. 2013. “What can neurons do for their brain? Communicate selectivity with bursts.” Theory Biosci 132(1): 27–39. [Link](https://pubmed.ncbi.nlm.nih.gov/22956291/)
3. Hart, Betty, and Todd R. Risley. 1992. “American Parenting of Language-Learning Children: Persisting Differences in Family-Child Interactions Observed in Natural Home Environments..” Developmental Psychology 28: 1096–1105. [Link](https://api.semanticscholar.org/CorpusID:143528292)
4. Hu, Michael Y., Aaron Mueller, Candace Ross, Adina Williams, Tal Linzen, Chengxu Zhuang, Ryan Cotterell, Leshem Choshen, Alex Warstadt, and Ethan Gotlieb Wilcox. 2024. “Findings of the Second BabyLM Challenge: Sample-Efficient Pretraining on Developmentally Plausible Corpora.” [Link](https://arxiv.org/abs/2412.05149)
5. Marr, D. 1971. “Simple memory: a theory for archicortex.” Philosophical Transactions of the Royal Society of London. B, Biological Sciences 262(841): 23–81. [Link](https://doi.org/10.1098/rstb.1971.0078)
6. Ott, Myle, Sergey Edunov, Alexei Baevski, Angela Fan, Sam Gross, Nathan Ng, David Grangier, and Michael Auli. 2019. “fairseq: A Fast, Extensible Toolkit for Sequence Modeling.” In Proceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics (Demonstrations). Minneapolis, Minnesota Association for Computational Linguistics. [Link](https://aclanthology.org/N19-4009/)
7. Oudiette, Delphine, and Ken A. Paller. 2013. “Upgrading the sleeping brain with targeted memory reactivation.” Trends in Cognitive Sciences 17(3): 142–149. [Link](https://www.sciencedirect.com/science/article/pii/S136466131300020X)
8. Rasch, Björn, and Jan Born. 2013. “About Sleep’s Role in Memory.” Physiological Reviews 93(2): 681–766. [Link](https://doi.org/10.1152/physrev.00032.2012)
9. Tadros, Timothy, Giri P. Krishnan, Ramyaa Ramyaa, and Maxim Bazhenov. 2022. “Sleep-like unsupervised replay reduces catastrophic forgetting in artificial neural networks.” Nature Communications 13(1), p. 7742. [Link](https://doi.org/10.1038/s41467-022-34938-7)
10. Tononi, Giulio, and Chiara Cirelli. 2014. “Sleep and the Price of Plasticity: From Synaptic and Cellular Homeostasis to Memory Consolidation and Integration.” Neuron 81(1): 12–34. [Link](https://doi.org/10.1016/j.neuron.2013.12.025)
11. Warstadt, Alex, and Samuel R. Bowman. 2024. “What Artificial Neural Networks Can Tell Us About Human Language Acquisition.” [Link](https://arxiv.org/abs/2208.07998)
12. Warstadt, Alex, Aaron Mueller, Leshem Choshen, Ethan Wilcox, Chengxu Zhuang, Juan Ciro, Rafael Mosquera, Bhargavi Paranjabe, Adina Williams, Tal Linzen, and Ryan Cotterell. 2023. “Findings of the BabyLM Challenge: Sample-Efficient Pretraining on Developmentally Plausible Corpora.” In Proceedings of the BabyLM Challenge at the 27th Conference on Computational Natural Language Learning. Association for Computational Linguistics. [Link](http://dx.doi.org/10.18653/v1/2023.conll-babylm.1)
13. Xiao, Chenghao, G Thomas Hudson, and Noura Al Moubayed. 2023. “Towards more Human-like Language Models based on Contextualizer Pretraining Strategy.” In Proceedings of the BabyLM Challenge at the 27th Conference on Computational Natural Language Learning. Singapore Association for Computational Linguistics. [Link](https://aclanthology.org/2023.conll-babylm.28/)