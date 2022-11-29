# Occupational Biases in Norwegian and Multilingual Language Models

This repository contains the bias probes amd codes used and described in the paper ["*Occupational Biases in Norwegian and Multilingual Language Models*"](https://aclanthology.org/2022.gebnlp-1.21/) by Samia Touileb, Lilja Øvrelid, and Erik Velldal. Published in the proceedings of the 4th Workshop on Gender Bias in Natural Language Processing (GeBNLP), collocated with NAACL 2022, Seattle.


# Abstract of the paper

In this paper we explore how a demographic distribution of occupations, along gender dimensions, is reflected in pre-trained language models. We give a descriptive assessment of the distribution of occupations, and investigate to what extent these are reflected in four Norwegian and two multilingual models. To this end, we introduce a set of simple bias probes, and perform five different tasks combining gendered pronouns, first names, and a set of occupations from the Norwegian statistics bureau. We show that language specific models obtain more accurate results, and are much closer to the real-world distribution of clearly gendered occupations. However, we see that none of the models have correct representations of the occupations that are demographically balanced between genders. We also discuss the importance of the training data on which the models were trained on, and argue that template-based bias probes can sometimes be fragile, and a simple alteration in a template can change a model’s behavior.

# Usage

To run the code: 

```
python compute_scores.py --task occupation --template_file templates_er.txt --lm_model norbert --output_file test_NorBERT.csv
```

Where:

- "--task" is of ``type=str'', and can only be "occupation" for now.
- "--template_file", is of "type=str", and should provide the path to the template file.
- "--lm_model", is of "type=str",  and referes to the pretrained language models to use (options: "norbert", "nbbert", "mbert", "roberta", "nbbertLarge", "nbroberta", "norbert2").
- "--output_file", is of "type=str", and should provide the path to output file with sentence scores")

# Cite

If you use these probes, codes, or the results associated with our work, please cite the following paper:

```
@inproceedings{touileb-etal-2022-occupational,
    title = "Occupational Biases in {N}orwegian and Multilingual Language Models",
    author = "Touileb, Samia  and
      {\O}vrelid, Lilja  and
      Velldal, Erik",
    booktitle = "Proceedings of the 4th Workshop on Gender Bias in Natural Language Processing (GeBNLP)",
    month = jul,
    year = "2022",
    address = "Seattle, Washington",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2022.gebnlp-1.21",
    doi = "10.18653/v1/2022.gebnlp-1.21",
    pages = "200--211",
}
```
