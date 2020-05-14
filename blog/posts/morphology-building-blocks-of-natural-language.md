# morphology: the building blocks of natural language

_2020-05-14_

Morphology is the study of change.

In linguistics, morphology looks at how words are formed--their structure, stems, suffixes, prefixes, and roots--and how those meanings change and shift when reconstructed. Morphology is also concerned with how words relate to each other through parts of speech, & _context._ These are all critical ingredients to understanding how words, their constituent properties, and their meanings change in relationship to one another.

These are also important to almost any Natural Language processing task. 

When linguists study language, they break it down into its most fundamental parts. Words are considered the smallest _independent_ unit of language: they can change position, they are separate units & not dependent on other words.

Morphology takes this breakdown to fundamental components a step further. _Morphemes_, the smallest meaning-bearing unit of language, are the building blocks of words. 

Consider the distinction between _free_ and _bound_ morphemes. Free morphemes are words themselves, which cannot be broken down any further into constituent concepts. Examples of free morphemes are words like _chair_,  _coat_, and _love_.  These words carry 1 single concept and do not require additional morphemes to convey their meaning.

Bound morphemes, on the other hand, require a kind of synergy to deliver their full ideological punch. These words consist of a morpheme that conveys the root meaning, combined with additional units of meaning that enhance or add detail/context. The words they create are referred to as _complex words_. They consist of a base and one or more affixes that add to the base morpheme’s meaning. An example of a complex word is _runner_, consisting of the verb ‘run’ and the affix ‘er’, which transforms the word _run_ into the *idea* of _a person who runs_.

Complex words whose meanings are evident from their morpheme structure are said to be _semantically transparent_: the word ‘unkindness’ builds from the base ‘kind’ by adding ‘un’ and ‘ness’ to structure a meaning that is near the opposite of the original base. It is semantically transparent because we can parse every morpheme to derive meaning. 

Semantically opaque words, on the other hand, are complex words consisting of a base morpheme and one or more affixes whose meaning is not easily parsed piecewise. Most of us know what a dentist is, but the word _dentist_ does not easily break down into clear morphological building blocks (unless you happen to be a student of latin).


There is a linguistic [Principle of Compositionality](https://plato.stanford.edu/entries/compositionality/) that describes the hierarchical relationship among the constituent properties--the morphemes--of any word. Simply put the word’s meaning is the sum of its parts, and the composition of these parts is determined by rules within the language. There are rules around which morphemes can be combined, and how--the order in which morphemes are affixed to a base matters too, hence the hierarchy.

When we begin to think of morphology as the study of the building blocks of words & ideas, its application in natural language processing becomes apparent. NLP text processing for almost any task requires a working understanding of morphology. Whether it is introduced in the form of complex human-designed rule-based work, normalization in preprocessing to simplify language for a machine learning model, or a model that learns to intuit common morphological rules from massive amounts of data (such as deep learning), the basic structure and building blocks of words is crucial domain knowledge for building successful natural language processing applications. 
