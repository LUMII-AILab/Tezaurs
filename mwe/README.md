# Multi-Word Expressions (MWE)

Lists of MWE extracted from the [balanced 10M text corpus of Latvian](http://www.korpuss.lv/id/LVK2018).

### Files

- `bigrams.pmiT`: MWE candidates consisting of two consecutive words extracted from the raw text corpus (13,971 candidates)
- `lemmas.pmiT`: lemmatised MWE candidates (12,429 candidates)

### Format

Each line consists of a MWE candidate followed by tab separated values of frequency:
1. `MWE`: *word1*<>*word2*<>
1. `Value 1`: order by T-score
1. `Value 2`: T-score
1. `Value 3`: order by Pointwise Mutual Information
1. `Value 4`: Pointwise Mutual Information
1. `Value 5`: frequency of the whole bigram
1. `Value 6`: frequency of the first word
1. `Value 7`: frequncy of the second word

### Publications

Skadiņa, I. [Looking for a Needle in a Haystack: Semi-automatic Creation of a Latvian Multi-word Dictionary from Small Monolingual Corpora](http://euralex.org/wp-content/themes/euralex/proceedings/Euralex%202018/118-4-2938-1-10-20180820.pdf). Proceedings of the 18th EURALEX International Congress, 2018

### Acknowledgements

This work is supported by European Regional Development Fund under the grant agreement No. 1.1.1.1/16/A/219 ([Full Stack of Language Resources for Natural Language Understanding and Generation in Latvian](https://github.com/LUMII-AILab/FullStack)).

### Licence

This dataset by [AiLab](http://ailab.lv) is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).
