# Tēzaurs

Open data from http://tezaurs.lv -- an extensive dictionary and thesaurus of Latvian, comprising more than 275,000 lexical entries.

### Available datasets

1. Wordlists with metadata.
2. Synonym sets (upcoming).
3. Full machine-readable entries (upcoming).

##### Wordlists

See `entries.txt` and `references.txt` under `wordlists`. Entries is a list of main headwords. References is a list of derivatives of the main headwords. Acronyms, abbreviations, prefixes, etc. are currently not included. They will be added later as a separate wordlist.

Data format: tab-separated records consisting of 9 fields:

1. Headword.
1. Homonym / homograph index (0\.\.N).
1. [Universal POS tag](http://universaldependencies.github.io/docs/u/pos/), or `NULL`.
1. Inflectional paradigm\* (0\.\.N), or `NULL`.
1. Infinitive stem\* (if the paradigm is 15 or 18), or `NULL`.
1. Comma-separated present stems\* (if the paradigm is 15 or 18), or `NULL`.
1. Comma-separated past stems\* (if the paradigm is 15 or 18), or `NULL`.
1. Verb prefix\*\* (if the paradigm is 15 or 18), or `NULL`.
1. Comma-separated list of [sources](http://tezaurs.lv/#/avoti), or `NULL`, or `REF` in case of references.

\* Used by [http://api.tezaurs.lv/v1/inflections/{word}](http://api.tezaurs.lv/) as [http://api.tezaurs.lv/v1/inflections/{word}?paradigm={inflectional_paradigm}&stem1={infinitive_stem}&stem2={present_stem}&stem3={past_stem}](http://api.tezaurs.lv/v1/inflections/rakt?paradigm=15&stem1=rak&stem2=rok&stem3=rak) if for paradigms 15, 18 and [http://api.tezaurs.lv/v1/inflections/{word}?paradigm={inflectional_paradigm}](http://api.tezaurs.lv/v1/inflections/aita?paradigm=7) for other paradigms.

\*\* To be used by [http://api.tezaurs.lv/v1/transcriptions/{word}](http://api.tezaurs.lv/v1/transcriptions/doma?encoding=ipa)

### Publications

Spektors, A., Auziņa, I., Darģis, R., Grūzītis, N., Paikens, P., Pretkalniņa, L., Rituma, L. and Saulīte, B. [Tezaurs.lv: the largest open lexical database for Latvian](http://www.lrec-conf.org/proceedings/lrec2016/pdf/1095_Paper.pdf). Proceedings of the 10th International Conference on Language Resources and Evaluation (LREC), 2016, pp. 2568-2571

### Acknowledgements

This work has been partially supported by Latvian State Research Programmes: Letonika (Project No. 3), NexIT (Project No. 1) and SOPHIS (Project No. 2).

### Licence

Tēzaurs by [AiLab](http://ailab.lv/en/) is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).
