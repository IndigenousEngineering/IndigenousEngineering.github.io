# What is Normalization in Natural Language Processing?

_2020-05-11_

If Stack Overflow’s [list of questions tagged ‘string’ - at over 150,000 entries -](https://stackoverflow.com/questions/tagged/string) is any guide, a lot of coders working with strings have run into some unusual edge-case behavior (and maybe even employed some [ugly regex](https://blog.codinghorror.com/regex-use-vs-regex-abuse/) to get the job done). _Normalization_ describes [processes](https://www.kdnuggets.com/2019/04/text-preprocessing-nlp-machine-learning.html) for getting words to their most universally useful form, and anyone who works with strings or text data will need to employ it at some point.

Normalization can cover a range of strategies from [lowercasing](https://nlp.stanford.edu/IR-book/html/htmledition/capitalizationcase-folding-1.html) to [stemming](https://nlp.stanford.edu/IR-book/html/htmledition/stemming-and-lemmatization-1.html) to more advanced processes like [lemmatization](https://nlp.stanford.edu/IR-book/html/htmledition/stemming-and-lemmatization-1.html). Stemming & lemmatization are methods based on word forms; normalization can also include phonetic methods, and converting non-latin characters or non-standard abbreviations.   Natural language processing, with its focus on [unstructured text data](https://en.wikipedia.org/wiki/Unstructured_data), includes some form of normalization as part of the normal workflow for almost any project.

It’s important to remember that no one normalization method is universal; the combination of methods depends on the task at hand. For sentiment analysis, emojis can be a particularly rich source of information. For another application, they might just be noise. There are a number of use-cases where lowercasing makes sense, but in searches where case matters, converting all the text to lowercase won’t yield very good results.

I recently had a model performing poorly on a sentiment classification task. It turned out the problem wasn’t my model, it was my text pre-processing: I had written code that removed high-value abbreviations from my text before the model even saw it. In this case it turned out that what might have been noise in another project was critical information the model needed to perform.

Nothing is foolproof, but investing time to think about what type(s) of text normalization is/are appropriate for the task at hand can yield improved analysis & model performance down the road.

