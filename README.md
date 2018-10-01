# Tēzaurs

Open data from http://tezaurs.lv - an extensive dictionary and thesaurus of Latvian, comprising more than 300,000 lexical entries.

### Available datasets

1. Wordlists with metadata.
2. Synonym sets (upcoming).
3. Glosses (upcoming).

##### Wordlists

See `entries.txt` and `references.txt` under `wordlists`. Entries is a list of main headwords. References is a list of derivatives of the main headwords. Named entities, acronyms, abbreviations, prefixes, etc. are not included.

Data format: tab-separated records consisting of 9 fields:

1. Headword.
1. Homonym / homograph index (0\.\.N).
1. [Universal POS tag](http://universaldependencies.github.io/docs/u/pos/), or `NULL`.
1. Inflectional paradigm<sup>1</sup> (0\.\.N), or `NULL`.
1. Infinitive stem<sup>1</sup> (if the paradigm is 15 or 18), or `NULL`.
1. Comma-separated present stems<sup>1</sup> (if the paradigm is 15 or 18), or `NULL`.
1. Comma-separated past stems<sup>1</sup> (if the paradigm is 15 or 18), or `NULL`.
1. Verb prefix<sup>2</sup> (if the paradigm is 15 or 18), or `NULL`.
1. Comma-separated list of [sources](http://tezaurs.lv/#/avoti), or `NULL`, or `REF` in case of references.

<sup>1</sup> Used by Tēzaurs' inflection service with the following parameters:
* [http://api.tezaurs.lv/v1/inflections/{word}?paradigm={inflectionalParadigm}&stem1={infinitiveStem}&stem2={presentStem}&stem3={pastStem}](http://api.tezaurs.lv/v1/inflections/rakt?paradigm=15&stem1=rak&stem2=rok&stem3=rak) for the paradigms 15 and 18;
* [http://api.tezaurs.lv/v1/inflections/{word}?paradigm={inflectionalParadigm}](http://api.tezaurs.lv/v1/inflections/aita?paradigm=7) for other paradigms;
* or no parameters - [http://api.tezaurs.lv/v1/inflections/{word}](http://api.tezaurs.lv/v1/inflections/aita) - if you feel lucky.

<sup>2</sup> To be used by [http://api.tezaurs.lv/v1/transcriptions/{word}](http://api.tezaurs.lv/v1/transcriptions/doma?encoding=ipa)

### Publications

Spektors, A., Auziņa, I., Darģis, R., Grūzītis, N., Paikens, P., Pretkalniņa, L., Rituma, L., Saulīte, B. [Tezaurs.lv: the largest open lexical database for Latvian](http://www.lrec-conf.org/proceedings/lrec2016/pdf/1095_Paper.pdf). Proceedings of the 10th International Conference on Language Resources and Evaluation (LREC), 2016

Pretkalniņa, L., Paikens, P. [Extending Tēzaurs.lv Online Dictionary into a Morphological Lexicon](http://ebooks.iospress.nl/volumearticle/50312). Human Language Technologies - The Baltic Perspective. Frontiers in Artificial Intelligence and Applications, vol. 307, IOS Press, 2018

### Acknowledgements

This work is partially supported by the Latvian State research programmes: Letonika (Project No. 3), NexIT (Project No. 1) and SOPHIS (Project No. 2). The latest development is supported by European Regional Development Fund under the grant agreement No. 1.1.1.1/16/A/219 ([Full Stack of Language Resources for Natural Language Understanding and Generation in Latvian](https://github.com/LUMII-AILab/FullStack)).

### Licence

Tēzaurs by [AiLab](http://ailab.lv) is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).
