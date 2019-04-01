# Alexa Contextual Query Rewrite Dataset

![CQR](https://github.com/alexa/alexa-dataset-contextual-query-rewrite/blob/master/dialog2-crop.png)

## Motivation
Dialogue assistants are used by millions of people today to fulfill a variety of tasks.  Such assistants also serve as a digital marketplace where any developer can build a domain-specific, task-oriented, dialogue agent offering a service such as booking cabs, ordering food, listening to music, shopping etc. Also, these agents may interact with each other, when completing a task on behalf of the user. Accomplishing this task requires understanding the context of a dialogue, communicating the conversational state to multiple agents and updating the state as the conversation proceeds. However, this is challenging given that different agents use their own domain specific schemas and meaning representations. In this dataset, we explore using natural language as an API for communicating across agents, thereby eliminating the need to learn or adapt to schema mappings. Instead, we show how one can leverage the syntactic/semantic regularities imposed by the language itself as a way to track the dialogue state. 

This work is detailed in the following [paper](https://arxiv.org/pdf/1903.05164.pdf)
```shell
@inproceedings{rastogi2019scaling,
  title={Scaling Multi-Domain Dialogue State Tracking via Query Reformulation},
  author={Rastogi, Pushpendre and Gupta, Arpit and Chen, Tongfei and Mathias, Lambert},
  booktitle={Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics},
  year={2019},
  publisher={Association for Computational Linguistics},
}
```

## Citation
When using this dataset, please cite
```shell
@inproceedings{Regan2019ADF,
  title={A dataset for resolving referring expressions in spoken dialogue via contextual query rewrites (CQR)},
  author={Michael Regan and Pushpendre Rastogi and Arpit Gupta. Lambert Mathias},
  year={2019}
}
```

This data itself is a modification of the original [Stanford Dialogue Corpus](https://nlp.stanford.edu/blog/a-new-multi-turn-multi-domain-task-oriented-dialogue-dataset/). It contains crowd-sourced rewrites to facilitate research in dialogue state tracking using natural language as the interface. For details of the contextual query rewrite dataset creation please refer to this [paper](https://arxiv.org/pdf/1903.11783.pdf)

## Format
The dataset is in JSON format, where each line is a JSON record. The JSON key 'reformulation' contains the additions made in this dataset. The ```refomulation``` are created at the end of each dialogue defined as ```"end_dialogue": true``` The structure under ```reformulation``` contains the following keys:
1. ```base_utt_idx``` - this is the index of the utterances in the original dialogue that is selected for rewrite.
2. ```flag``` - indicating the categories of referring expressions.
3. ```gold_slots``` - the gold standard slots to be used in the rewrite.
4. ```mturk_reformulations``` -  a list of crowd-sourced rewrites from MTurk.
5. ```reformulated_utt``` - gold rewrites.

## License Summary

This sample code is made available under a modified MIT license. See the LICENSE file.
