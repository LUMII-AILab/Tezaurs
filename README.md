# Tēzaurs

Open data from http://tezaurs.lv/ -- an extensive dictionary and thesaurus of Latvian comprising more than 250,000 entries.

### Available datasets
----------------------

1. Wordlists with metadata
2. Synonym sets (upcoming)
3. Full machine-readable entries (upcoming)

##### Wordlists

See `entries.txt` and `references.txt` under `wordlists`. Entries is a list of headwords of main entries. References is a list of derivatives of the main headwords.
Data format: tab-separated records consisting of 6 fields.
1. Headword.
2. Homonym index (0+).
3. [Universal POS tag](http://universaldependencies.github.io/docs/u/pos/) or `NULL`.
4. Inflectional paradigm (0+) or `NULL`.
5. Comma-separated list of [sources](http://tezaurs.lv/#/avoti) or `NULL`, or `REF` in case of references.

### Acknowledgements
--------------------

This work has been partially supported by Latvian State Research Programmes: Letonika (Project No. 3), NexIT (Project No. 1) and SOPHIS (Project No. 2).

### Licence
-----------

Tēzaurs by [Artificial Intelligence Laboratory](http://ailab.lv/) is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).
