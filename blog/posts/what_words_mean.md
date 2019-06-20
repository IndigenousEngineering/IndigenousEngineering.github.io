# what words mean
*towards a multidisciplinary approach to bias in nlp*

In 2009 a researcher named Fei-Fei Lee, after [much perseverance](https://qz.com/1034972/the-data-that-changed-the-direction-of-ai-research-and-possibly-the-world/), published the now-famous [ImageNet paper](http://www.image-net.org/papers/imagenet_cvpr09.pdf)--along with a massive [dataset](http://www.image-net.org/) of curated and labeled images for supervised computer vision training. Lee had started the project on the intuition that more data would significantly improve the performance of still-nascent neural nets, particularly in computer vision. Lee was right, in a way that is difficult to overstate--not only did ImageNet & its corresponding [competition](http://image-net.org/challenges/LSVRC/) spawn a new wave of deep learning innovation & improve computer vision model performance on the dataset itself, but neural nets trained using ImageNet showed significant improvement in skill on novel data and tasks as well. ImageNet didn’t just make the models better at classification, it made them better at *learning*.

\***

Unlike computer vision, natural language processing doesn’t have an easy animal-brain metaphor. The convolutional layers invoked in a computer vision CNN mimic the animal visual processing cortex; but there isn’t any one single spot in the brain for language from which researchers can draw structural cues. 

While we still know relatively little about the precise mechanisms by which language information is processed in the human brain, advances in neuroimaging have provided greater context to understand the overlap of physical processing centers as linguistic requirements become more complex. Nevertheless, our best current systems for understanding language computationally are often mathematical models of the persistence of memory: RNNs and specifically LSTMs, networks that are [deep in both space and time](http://colah.github.io/posts/2015-08-Understanding-LSTMs/). 

Models need numerical data to learn from. This means that human-ready inputs like pictures or sentences must be transformed into something a model can understand. Processes for doing so effectively have evolved throughout NLP’s history, with major advances in the field at large often tied to novel vectorization techniques. Since 2013, word2vec ([paper](https://arxiv.org/pdf/1301.3781.pdf), [paper](https://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and-their-compositionality.pdf), [paper](http://www.aclweb.org/anthology/N13-1090), [code](https://code.google.com/archive/p/word2vec/source/default/source)) and GloVe ([paper](https://nlp.stanford.edu/pubs/glove.pdf), [code](https://nlp.stanford.edu/projects/glove/)) have been two of the most successful--and widely deployed--encoding frameworks in the history of the discipline.

In contrast to the deeper networks they often feed, word embeddings like GloVe and word2vec are shallow, the product of two-layer feedforward networks tuned to create numerical representations of words. It is on these representations that machines can perform the math that ultimately trains a downstream network. The need to convert text data to something quantifiable is at root of all encoding: after all is said and done, models are only as smart and capable as the data we provide them. But while pixel encoding and back-propogating work surprisingly well for computer vision models, converting human language--with all its nuance--to model-ready encodings proves to be a different kind of challenge. 

When human brains process language, they are encoding information along many vectors of meaning simultaneously. Simple numeric representations can’t possibly capture all that dimensionality.

Machines are, of course, not engaging in patterns of neurotransmitter discharge and uptake. The conditions under which their neurons pass information along are numerical, and not electro-chemical; they are differentials gating another type of electric potential altogether. But in the mapping of tokens to vector space, machines can manage to capture some of the complexities of language--both syntactic and semantic--that our brains seem to manage with ease.

That machine vectorization manages to capture semantic and syntactic information is in itself already impressive. The fact that it does so with little to no supervision is nothing short of amazing.

\***

Natural Language Processing owes much of its intellectual heritage to thinkers in the field of linguistics. And linguists have been thinking about the deep, often inscrutable, culturally- and personally-specific relationships between words and their meanings for a very long time.

In the 19th century, Swiss-born Ferdinand de Saussure began looking at ways to reform and codify the terminology of linguistics as a way to facilitate academic progress. In doing so, Saussure proposed a series of dichotomies to describe facets of language, one of the most powerful being that of signifier and signified. In doing so, Saussure effectively founded a field that would come to be known as [structural linguistics](https://www.encyclopediaofmath.org/index.php/Structural_linguistics).

The structuralist school of linguistics has informed modern cognitive neuroscience, psycholinguistics, and even sociological paradigms in a multitude of ways. And it is arguably interwoven into our current efforts to teach machines how we talk. 

Saussure believed that language has no teleology; its evolution is driven by the need to differentiate ideas from one another. It followed logically, Saussure posited, that words would have no truly “positive” relationships to each other; language depends entirely on contrasts to derive meaning.

Words--Saussure’s signifiers--only possess meaning in relationship to other signifiers. They are defined by their differences of meaning, relative to one another. Their signified concepts are arbitrary. 

If the relationship between signifier and signified is a purely arbitrary one, then the most critical mechanism of transferring meaning in any language becomes the differences among signifiers themselves--rather than any inherent similarities between words and their signified concepts.

Language, the culturally-specific cumulation of words and their associations, can be represented as a network of differentiable signifiers suspended in some space of meaning, relative to one another. To locate a word and its meaning, we need only find the words around it.

Current widely used methods in natural language processing arguably model these mechanisms in two ways: word vectors/embeddings, and intracellular memory. Persistent memory within the cells of recurrent neural networks models sequences and syntax well. But in modern NLP, a large chunk of semantic meaning is encoded in the vectorization process, before the data ever see an LSTM’s forget gate.

In vector space, conceptual distance becomes quantifiable distance. 

\***

Back in July, Sebastian Ruder wrote a post arguing that [“NLP’s ImageNet Moment Has Arrived”](http://ruder.io/nlp-imagenet/). In it, Ruder analogizes the potential of new, deeper, pretrained models like [ULMFiT](https://arxiv.org/abs/1801.06146), the [OpenAI Transformer](https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/language-unsupervised/language_understanding_paper.pdf), and [ELMo](https://arxiv.org/pdf/1802.05365.pdf) to the revolutionizing impact of pretrained computer vision models via the ImageNet breakthrough. But while celebrating the possibilities in these newer, deep contextualized vectors, it’s worth taking a moment to look at what made the shallower models like word2vec and GloVe so powerful--and what contributes to their weaknesses.

Word embeddings like word2vec and GloVe are, in many ways, almost magical. For the price of a few hundred dimensions--much smaller and computationally less expensive than traditional, more sparse representations--it becomes possible to capture a much greater depth of meaning than any decontextualized bag-of-words model ever could. These gains come through examining words in their contexts--in “the company they keep.”

Projected into vector space, words are represented as points. The higher the likelihood that two words might appear in each others’ contexts (based on whatever data the model has trained on), the closer their points will be in vector space.

With hundreds of dimensions, these word associations would be difficult to visualize accurately. However, using [principal component analysis (PCA)](https://www.utdallas.edu/~herve/abdi-awPCA2010.pdf), it’s possible to project their large dimensionality onto a more human-readable two dimensions. Applying PCA (via [Gensim](https://radimrehurek.com/gensim/)) to the vectors learned by a pre-trained GloVe model, true-to-usage relationships begin to emerge. These relationships also make possible neat little bits of math--arithmetic on word vectors to find relationships among words. With similar calculations, it’s possible to find and measure a multitude of relationships in word2vec and GloVe embeddings.

The ability to learn and map complex relationships and their representations is stunning, really. Models went from measuring the statistical usage of language to something more resembling an understanding of language. They were learning--and encoding into models further down the pipeline--subtleties of both syntax and semantics, and possibly even something about the ways in which these two fundamental components of language interplay.

But what if the models were also learning society’s unconscious biases? What if, in addition to innocuous-to-useful word-pair relationships, there existed uglier associations that were racist, sexist, or otherwise offensively skewed?

Two recent groundbreaking papers have shown exactly that. 

\***

The conversation around bias in word embeddings is emergent, and moving quickly.

In 2016 Bolukbasi et al. published [“Man is To Computer Programmer as Woman is to Homemaker? Debiasing Word Embeddings”](https://arxiv.org/abs/1607.06520). The paper showed that using matrix arithmetic operations like the ones above, it was easy to find stereotypical and offensive relationships encoded in popular word embeddings; for example the relationship *man - woman* is roughly equal to *computer programmer - homemaker*. 

In 2017, [Caliskan et al.](https://purehost.bath.ac.uk/ws/portalfiles/portal/168480066/CaliskanEtAl_authors_full.pdf) proposed the Word Embedding Association Test (WEAT) as a means to quantify--or at least begin to get a handle on--bias in word embeddings. The test borrows from the [Implicit Association Test (IAT)](https://www.projectimplicit.net/nosek/iat/), which explores concepts around identity, bias, and their measurement. The WEAT framework uses cosine similarity as a metaphor for distance and stand-in for the IAT’s response-time metric.

Unsurprisingly, the researchers found that biases were not only measurable, but in some cases correspond with measurable social phenomena: the researchers found that the word relationships encoded in GloVe embeddings around gender and career correlated strongly with actual US Department of Labor Statistics data.

On a more optimistic note, one exciting moment of the paper comes when the authors, qualifying carefully that preliminary testing is yet to be done, introduce the prospect of applying the framework to historic corpora for the purpose of analyzing past societies:

>*Similarly, our methods could be used to quickly find differences in bias between demographic groups, given large corpora authored by members of the respective groups. If substantiated through testing and replication, WEAT may also give us access to implicit associations of groups not available for testing, such as historic populations.*

Imagine being able to sample the biases and deeper sociolinguistic cues of long-gone historic populations! However,  the prospect of research should give us pause, as it introduces the question of how large a corpus would be necessary for a task like this--and given the bias of historic preservation toward white, western corpora, whether we could ever leverage this technology to learn from historic non-white & non-western voices at the same scale.

Linguistic and cultural bias are self-replicating.

What the authors repeatedly make clear is that the bias in popular, readily available, and widely-deployed embeddings was significant, measurable, and largely consistent. Even working with data prepared by journalists--communications professionals who are trained to represent reality without bias--the models would learn prevalent social biases from the data itself:

>*We stress that we replicated every association documented via the IAT that we tested. The
number, variety, and substantive significance of our results raise the possibility that all implicit
human biases are reflected in the statistical properties of language.*

The WEAT paper's demonstration of sexist associations and negative reactions to black american (vs european american) names echoed computer vision’s recent bias fiascos. Harmful user experiences, such as facial recognition models’ [inability to recognize people of color](https://www.theguardian.com/technology/2017/dec/04/racist-facial-recognition-white-coders-black-people-police) and google’s photo-tagging suite that [offensively mis-identified black folks](https://www.theguardian.com/technology/2018/jan/12/google-racism-ban-gorilla-black-people) in photos, made headlines as AI bias moved more into the mainstream consciousness. Developers working on these systems scrambled to get better data and find ways to mitigate bias, or else risk not only amplifying existing social prejudices, but leaving their product unusable by significant portions of the population--groups that have traditionally been denied access to unequally distributed social resources in the past. 

Both computer vision and NLP clearly have progress to make before becoming the kinds of democratizing technologies that Silicon Valley loves to espouse. Given computer vision’s well-established problems with implicitly learned racism, it might have been foreseen that NLP models trained on human generated data could learn the same social cues.

If the promise of ImageNet’s portability and wide application is just now arriving for NLP, its biases were almost certainly already here.

\***

There are, of course, many more sources of bias for NLP models than just word embeddings, and even more potential solutions, from emergent data gathering and preparation protocols, to a variety of methods to train out the biasing noise. Additionally there are suggestions that given enough data, learned biases in word2vec and GloVe can be mitigated--although “throw more data at it” seems to solve nearly every modern machine learning problem in a way that becomes slightly suspect when the data is itself the problem.

The data-mitigation-by-data-mass approach also highlights once again the uneven representation of certain voices within the machine-trainable corpora; even if all other potential biases could be magically removed, due to long-standing [academic eurocentrism](https://tinyurl.com/ycehwqou) the probability that white and western voices will be amplified remains high given the nature of the available texts. If models simply reflect biases already encoded in the data, more data won’t necessarily ensure more even representation. 

Working around issues like these, and towards more representative corpora in the future, depends on a multidisciplinary partnership among historians, linguists, statisticians, social scientists, and NLP practitioners. The statistical associations of words could potentially provide a rich source of cultural information--if we care enough to seek the corpora out, preserve them, and train our models to recognize them.

Whether deeper embeddings like the OpenAI Transformer, ULMfit, and ELMo will significantly impact the bias of the systems they help train remains to be seen. If the hypothesis that cultural biases are encoded and transmitted via the statistical relationships among words proves true, it seems likely that these deeper contextual representations will reflect our social biases back to us in much the same way their predecessors have. This require awareness and sensitivity, as well as a constant, rigorous self-examination of what our algorithms say about us.

\***

Saussure’s nineteenth-century structuralism paved the way for the American relativists of the twentieth century, who began to assert the personal and cultural specificity of language as primary--if not the only valid--mechanism for linguistic study. It was from these early descriptivists that the Sapir-Whorf hypothesis was born: that not only is language a highly personal and culturally specific endeavor, but that the language(s) we speak shape our perception of the world around us.

Towards the end of the WEAT paper, Caliskan et al. also reference the complex interplay of language and social values:

>*Our results also suggest a null hypothesis for explaining origins of prejudicial behavior in
humans, namely, the implicit transmission of ingroup/outgroup identity information through
language. That is, before providing an explicit or institutional explanation for why individuals make prejudiced decisions, one must show that it was not a simple outcome of unthinking reproduction of statistical regularities absorbed with language.*

The “simple outcome” of “unthinking reproduction of statistical regularities” can be a powerful thing when applied across institutions--or amplified via widespread machine learning applications. If all our institutions are at root human, and thus based on communication, and thusly based on language, can the biases we encode in and through our very words really be separated from the institutions--and algorithms-- we build?

What if we are, in some sense, back to the descriptivist model of language as a shaper of culture? And what if, in this unique moment in technological history, we have the power to shape the discourse? 

We know that social biases exist, and that machines implicitly learn them. How we choose to work around these biases as our models evolve will shape NLP research well into the future. 

We should strive to make sure our algorithmic choices are rigorously transparent, and perpetually open to challenge from not only fellow engineers and machine learning practitioners, but from the social sciences, arts and humanities as well. We need interested experts in fields outside of science to help us tackle questions that can’t be readily translated with code, since, as recent experience has demonstrated, ignoring these questions is no longer feasible. We are rapidly learning that model performance matters little if what we build isn’t moral. In applying the new deep embeddings, NLP practitioners would be wise to partner with outside disciplines to remain vigilant for new ways of evaluating and mitigating bias. 

If computer vision’s “ImageNet moment” can teach NLP practitioners anything right now, it’s that waiting for bias to make itself apparent is not a viable option.


\***

[Indigenous Engineering blog](https://www.diverge.ai/#blog)
