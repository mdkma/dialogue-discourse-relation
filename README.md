# Implicit Discourse Relation Identification for Open-domain Dialogues

## Dataset

Original self-dialogue corpus Edina can be obtained [here](https://github.com/jfainberg/self_dialogue_corpus).

The new proposed dataset are in the `Edina-DR` directory. The three folders under it are for:

* `Edina-DR`: Argument pairs extracted from Edina dataset
* `Edina-DR_NLU`: Argument pairs and dialogue features extracted Natural Language Understanding modules
* `Edina-DR_NLU_human-annotation`: 400 samples selected from the samples in `Edina-DR_NLU` and annotated by human

The column names across all files in `Edina-DR` and `Edina-DR_NLU` stands for:

* `arg1`: the first arugment
* `arg2`: the second argument
* `relation`: the annotated discourse relation
* `connective`: the connective word originally lies between `arg1` and `arg2`
* `type`: whether the connective originally is at the beginning (`begin`) of a utterance or middle (`mid`) of a utterance
* `original_utt`: orginal full utterance where this argument pairs and discourse relation are extracted from
* `original_utt_prev`: the previous utterance of `original_utt`. If the connective is `begin`, then the first argument is extracted from the previous utternace
* `arg*_{dialogue_act, sentiment, topic, cobot_topics, intents}`: values for the names dialogue features
* `arg*_gnode_entities`: entities and their related properties using the entity detector
* `arg*_{gkg_entities, gkg_keywords, gkg_etype_list}`: the same information as in `arg*_gnode_entities` but separated according whether it's entities themselves, keywords or types
* `arg*_flow_topics`: topics detected by seperated topic classifier originally designed for invoking certain dialogue flows

The human annotation include:

* Discourse relation identified by expert annotater (`relation_human` field)
* Whether this pair of arugments do not hold a discourse relation due to grammar error (`error_human` field is `y`)

## Cite

```
@inproceedings{ma2019implicit,
  title={Implicit Discourse Relation Identification for Open-domain Dialogues},
  author={Ma, Mingyu Derek and Bowden, Kevin and Wu, Jiaqi and Cui, Wen and Walker, Marilyn},
  booktitle={Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics (ACL)},
  year={2019}
}

@article{fainberg2018talking,
  title={Talking to myself: self-dialogues as data for conversational agents},
  author={Fainberg, Joachim and Krause, Ben and Dobre, Mihai and Damonte, Marco and Kahembwe, Emmanuel and Duma, Daniel and Webber, Bonnie and Fancellu, Federico},
  journal={arXiv preprint arXiv:1809.06641},
  year={2018}
}

@article{krause2017edina,
  title={Edina: Building an Open Domain Socialbot with Self-dialogues},
  author={Krause, Ben and Damonte, Marco and Dobre, Mihai and Duma, Daniel and Fainberg, Joachim and Fancellu, Federico and Kahembwe, Emmanuel and Cheng, Jianpeng and Webber, Bonnie},
  journal={Alexa Prize Proceedings},
  year={2017}
}
```