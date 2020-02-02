# Tēzaurs

Open data from https://tezaurs.lv - an extensive dictionary and thesaurus of Latvian, comprising more than 315,000 lexical entries.

### Available datasets

1. Wordlists with metadata (under `wordlists`).
1. Synonymic references (under `wordlists`).
1. Glosses, etc. (under `entries`).

### Additional datasets

1. Multi-word expressions (extraced from a balanced 10M text corpus of Latvian) - under `mwe`.
1. Mapping of Tēzaurs entries to core WordNet synsets (experimental) - under `wordnet`.

## Wordlists

### Morphology and other metadata

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

<sup>1</sup> Used by Tēzaurs inflection service with the following parameters:
* [http://api.tezaurs.lv/v1/inflections/{word}?paradigm={inflectionalParadigm}&stem1={infinitiveStem}&stem2={presentStem}&stem3={pastStem}](http://api.tezaurs.lv/v1/inflections/rakt?paradigm=15&stem1=rak&stem2=rok&stem3=rak) for the paradigms 15 and 18;
* [http://api.tezaurs.lv/v1/inflections/{word}?paradigm={inflectionalParadigm}](http://api.tezaurs.lv/v1/inflections/aita?paradigm=7) for other paradigms;
* or no parameters - [http://api.tezaurs.lv/v1/inflections/{word}](http://api.tezaurs.lv/v1/inflections/aita) - if you feel lucky.

<sup>2</sup> To be used by [http://api.tezaurs.lv/v1/transcriptions/{word}](http://api.tezaurs.lv/v1/transcriptions/doma?encoding=ipa)

### Synonyms

See `synonyms.txt` under `wordlists`.

Data format: tab-separated records consisting of 2 fields:

1. Headword.
1. Comma-separated synonymic references.

## Publications

Spektors, A., Auziņa, I., Darģis, R., Grūzītis, N., Paikens, P., Pretkalniņa, L., Rituma, L., Saulīte, B. [Tezaurs.lv: the largest open lexical database for Latvian](http://www.lrec-conf.org/proceedings/lrec2016/pdf/1095_Paper.pdf). Proceedings of the 10th International Conference on Language Resources and Evaluation (LREC), 2016

Pretkalniņa, L., Paikens, P. [Extending Tēzaurs.lv Online Dictionary into a Morphological Lexicon](http://ebooks.iospress.nl/volumearticle/50312). Human Language Technologies - The Baltic Perspective. Frontiers in Artificial Intelligence and Applications, vol. 307, IOS Press, 2018

Paikens, P., Grūzītis, N., Rituma, L., Nešpore, G., Lipskis, V., Pretkalniņa, L., Spektors, A. [Enriching an Explanatory Dictionary with FrameNet and PropBank Corpus Examples](https://elex.link/elex2019/wp-content/uploads/2019/09/eLex_2019_52.pdf). Proceedings of the 6th Biennial Conference on Electronic Lexicography (eLex), 2019

## Related work

- [Tēzaurs API](https://api.tezaurs.lv)
- [NLP-PIPE: Latvian NLP Tool Pipeline](https://github.com/LUMII-AILab/nlp-pipe)
- [Full Stack of Latvian Language Resources for NLU and NLG](https://github.com/LUMII-AILab/FullStack)

## Acknowledgements

This work is partially supported by the Latvian State research programmes: Letonika (Project No. 3), NexIT (Project No. 1) and SOPHIS (Project No. 2). The latest development is supported by European Regional Development Fund under the grant agreement No. 1.1.1.1/16/A/219 ([Full Stack of Language Resources for Natural Language Understanding and Generation in Latvian](https://github.com/LUMII-AILab/FullStack)) and by the Latvian State research programme Latvian Language (VPP-IZM-2018/2-0002).

## Licence

Tēzaurs data sets by [AiLab](http://ailab.lv) are licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

Please, cite the relevant [publications](https://github.com/LUMII-AILab/Tezaurs#publications) if you use Tēzaurs data or API in your research. Please, [let us know](mailto:tezaurs@ailab.lv) if you use Tēzaurs data or API in your products or services. Your citations and feedback are important to secure funding for the further development of Tēzaurs data sets and API.

## Contacts

Project coordinator: [Andrejs Spektors](http://ailab.mii.lu.lv/aspekt/cv.htm), `tezaurs@ailab.lv`

Team members: Ilze Auziņa, Guntis Bārzdiņš, Roberts Darģis, Mikus Grasmanis, Normunds Grūzītis, Gunta Nešpore-Bērzkalne, Pēteris Paikens, Ilmārs Poikāns, Lauma Pretkalniņa, Laura Rituma, Baiba Valkovska (Saulīte), Artūrs Znotiņš
