# in reply: Natives, suicide, and online hostility

_Did hostility to Natives really increase since the 2016 election cycle? Does it matter?_

[<img src="https://raw.githubusercontent.com/IndigenousEngineering/In-Reply/master/dataviz/Mickey_Barrett_graphic.jpeg" alt="a lone figure sits wrapped in a hoodie with anti-Indigenous slurs and suicide references written on it, in front of a night sky with more insults & slurs written across. click for resources. Graphic by Mickey Barrett" width="500"/>](#Resources)

**_Content Note: This project contains references to physical violence, sexual assault, anti-Indigenous slurs, suicide, & self harm._**

**_If you are experiencing suicidal thoughts, there is help. You are not alone. Please [*click here*](#Resources) for resources._**

**_Dedicated to the family members we have lost, and those fighting to survive. You are sacred and loved._**

In recent years the number of deaths by suicide in the US has increased across all ethnicities by [more than one third](https://www.cdc.gov/nchs/data/databriefs/db330-h.pdf). However within this dramatic increase, Indigenous peoples are [disproportionately affected](https://www.cdc.gov/nchs/data/hestat/suicide/rates_1999_2017.htm). Suicide rates for Native men have increased by 71% since 1999, more than _double_ the rate for the US as a whole. For Native womxn, deaths by suicide have [increased by _one hundred thirty nine percent_  (139%)](https://indiancountrytoday.com/news/centers-for-disease-control-release-suicide-stats-native-american-women-top-the-list-with-139-percent-increase-ivpVozlnc0eKs3iHX44V4Q).

The Centers for Disease Control and Prevention reports that _”American Indian/Alaska Natives (AI/AN) have the highest rates of suicide of any racial/ethnic group in the United States”_, with [rates steadily increasing since 2003](https://www.cdc.gov/mmwr/volumes/67/wr/mm6708a1.htm). Data from the 18 states participating in the National Violent Death Reporting System (NVDRS) showed that overall, suicide rates for Natives were more than 3.5 times higher than those among racial/ethnic groups with the lowest rates

Even more disturbing, according to the same CDC report more than one third (35.7%) of American Indian/Alaska Native suicides occurred among youths aged 10–24 years (vs only 11% of non-Native whites). Heartbreakingly, Natives had 2.4 times the odds of a suicide of a friend or family member affecting their death, demonstrating the ripple effects of suicide throughout Indigenous communities. Suicide is in fact the [eighth leading cause of death for Natives of all ages](https://www.nicoa.org/national-american-indian-and-alaska-native-hope-for-life-day/).

Natives experience serious psychological distress more than the general population, and Indigenous people experience post traumatic stress disorder (PTSD) more than twice as often as non-Natives, according to the [Substance Abuse and Mental Health Services Administration (SAMHSA)](https://www.integration.samhsa.gov/workforce/mental_health_disparities_american_indian_and_alaskan_natives.pdf).

While suicide is a complex topic affected by many interconnected factors, there is strong evidence that experiencing violence is a major risk factor for death by suicide. Physical and sexual violence have lasting after-effects often including anxiety, depression, and PTSD.

The CDC also [reported](https://www.cdc.gov/mmwr/volumes/67/wr/mm6708a1.htm) that _“although intimate partner problems were a common precipitating circumstance [for death by suicide] for both Natives (39.1%) and non-Native whites (29.4%), Natives had significantly higher odds of experiencing this circumstance”._

According to a 2016 report from the National Institute of Justice, over 84% of Native womxn and 81% of Native men--more than 4 out of 5--[experience physical violence in their lifetimes](https://nij.ojp.gov/topics/articles/violence-against-american-indian-and-alaska-native-women-and-men). This includes 27.5% of Native men who experience sexual violence, and more than 55% of Native womxn.

Survivors of sexual assault are 10 times more likely to attempt suicide than those who haven’t experienced sexual assault, as reported by the [National Sexual Violence Resource Center](https://www.nsvrc.org/blogs/what-puts-survivors-increased-risk-suicide-and-how-help). The NSVRC also reports research showing _“over a third of womxn rape survivors have contemplated suicide at some point after their assault, and 13% had attempted suicide.”_

Other acts of violence, such as stalking, disproportionately affect Natives as well: [48.8% of Native womxn had been stalked](https://nij.ojp.gov/topics/articles/violence-against-american-indian-and-alaska-native-women-and-men), compared with 26.8% of white womxn.

Given the high rates of violence against Native communities, it is not difficult to imagine how such significant traumas & psychological stressors might contribute to what could be described as a suicide epidemic. Unfortunately many of these real-world stressors are replicated in online social spaces. The link between online bullying and suicide/self-harm are well established: research shows that people who experienced bullying online were [more than twice as likely](https://www.jmir.org/2018/4/e129/) to self-harm, experience suicidal thoughts, or attempt suicide. [Another study](https://www.researchgate.net/publication/327167587_Connecting_Adolescent_Suicide_to_the_Severity_of_Bullying_and_Cyberbullying) found similar numbers replicated among adolescents: teens were more than twice as likely to attempt suicide after experiencing online harassment.

However while at least [34% of students say they’ve experienced cyber bullying](https://cyberbullying.org/cyberbullying-fact-sheet-identification-prevention-and-response), it appears no specific data currently exist on the frequency with which Natives experience harassment online. I wanted to change this.

In my project [“Not Your Mascot: Opinions vs Data”](https://indigenous.engineering/projects/Not_Your_Mascot.html) I explored the connection between Native mascots and anti-Indigenous hate speech online. I was easily able to find well over one 150,000 tweets containing offensive words or phrases. I also explored how false claims of Cherokee heritage measurably take up cultural & linguistic space from actual Indigenous peoples in [“What Does it Mean to be Cherokee Online?”](https://indigenous.engineering/projects/Cherokee-Online.html). What I had not yet explored was sentiment towards Indigenous people. 

Anecdotal evidence suggests that anti-Indigenous hostility online has increased since the 2016 election cycle. I wanted to see if this was true.

### Methods

Beginning this project, I had three questions in mind. First, how often do Natives experience harassment online? Second, is there a way to quantify the overall tone of the discourse for Indigenous people in online spaces? Third, has there been measurable change in the tone since the 2016 election cycle? To explore these questions, I employed several natural language processing & machine learning techniques.

#### Building Corpora

I first gathered tweets from a curated list of fairly well-known Native accounts via Twitter’s searchtweets API for historical tweets. I tried to include as many accounts belonging to Black Natives as possible for accuracy in representation. 

To measure how Natives are _spoken to_ online, my dataset included only _replies_ to these accounts, not original posts from the accounts themselves. While this does not ensure that every tweet counted is from an outside/non-Native party, it vastly increases the chances that a particular tweet in the dataset will be an independent part of the conversation (and thus useful for measuring tone).

#### Targeted Searches

Next I searched for particular phrases within the tweets’ text. These phrases were selected based on their likelihood of appearing in anti-Indigenous threats and/or hate speech. To keep results brief & focused I included only twelve phrases in my initial search, with a focus several common insults, & specific references to suicide & variants: _'ugly', 'kill', 'die', 'kys', 'kill yourself', 'kill urself', 'kill ur self', 'shut up', 'stupid', 'dumb', 'Pocahontas', & 'sq**w'_.

Preliminary searches revealed a significant increase in negative speech towards Natives online post-2016.
 
Despite the fact that the 2007-2016 corpus covers more than twice the time span, initial explorations revealed a nearly 50% increase in the terms tested in the 2016-2020 corpus (641 phrases found in 30,658 pre- July 2016 tweets, ~2.0% versus 1,435 phrases found in tweets during & after July of 2016, or 2.9%).

With these results, I decided to gather a larger sample focused on a shorter list of Native accounts that had notoriety for discussing tribal sovereignty, DNA testing, missing & murdered Indigenous womxn (MMIW), and/or Elizabeth Warren's claims specifically due to anecdotal reports from Natives online regarding increased harassment around Warren’s candidacy: [@DelSchilling](https://twitter.com/DelSchilling), [@rebeccanagle](https://twitter.com/rebeccanagle), [@pollysgdaughter](https://twitter.com/pollysgdaughter), [@KimTallBear](https://twitter.com/KimTallBear), [@NativeApprops](https://twitter.com/NativeApprops), [@justicedanielh](https://twitter.com/justicedanielh), & [@PepePierce](https://twitter.com/PepePierce).

I wanted to see whether the tone of the conversation had shifted differently for these accounts in and after the 2016 election cycle.

I also expanded the search range slightly, resetting the end date from January 28th 2020 to extend through March 6th, 2020--the day after Warren [ended her presidential campaign](https://www.cnn.com/2020/03/05/politics/elizabeth-warren-drops-out/index.html).

Within this larger and more focused dataset, I was able to quickly find just under 2,000 potentially offensive tweets containing words/phrases associated with anti-Indigenous violence. With 1,999 such tweets from a corpus of 52,634 documents, or 3.79%, this set contained the largest number of any group/time period I tested. Versus the general post- July 2016 Native group, Native accounts focused on these Native-specific issues received nearly one third more negatively associated phrases among the short list I tested.

[<img src="https://raw.githubusercontent.com/IndigenousEngineering/In-Reply/master/dataviz/hostile_terms_and_death_refs_2016_and_2020.png" alt="There has been a marked increase in hateful & anti-Indigenous terms, as well as references to death & suicide, since the 2016 election cycle" width="500"/>](https://github.com/IndigenousEngineering/In-Reply/in_reply_1.ipynb)

It should be noted that this short list of only twelve word/phrases--including several variants of “kill yourself”, a frequently used insult in online spaces that specifically references suicide--is incomplete & non-exhaustive. The stark increases in tweets potentially containing hate speech directed at these accounts warrants further investigation with more detailed search strings & analysis.

Finding offensive phrases was relatively quick and easy across all focus accounts. However I wanted to model a more objective measure of tone towards Natives online.

#### Sentiment Analysis

Searching for particular words & phrases is an intuitive approach to examining sentiments present in the data. While it can be illuminating, this type of analysis can be difficult to scale.

Another tool for understanding unstructured text data is sentiment analysis, where a model is trained to recognize whether the emotions expressed in a particular document are generally positive, or negative. For this task I chose to use a Naive Bayes Classifier. Bayesian classifiers (and specifically the Native Bayes model) have proven to be both simple & powerful for a variety of text classification applications.

Using the scikit-learn library, I trained a Naive Bayes classifier on the NLTK dataset of sentiment-labeled tweets, setting up a binary classification task in which the model would differentiate between tweets with either overall positive or negative sentiment. The NLTK corpus includes 5,000 tweets with positive sentiment, and 5,000 tweets labeled as having negative sentiment. Since my model would be working with tweet text(s), training on a corpus of tweets made intuitive sense. My Naive Bayes model achieved 99.6% accuracy out-of-the-box on the NLTK corpus test split.

I applied minimal text processing: I removed tweet artifacts & low-value stopwords, then normalized tweet texts using lemmatization. Lemmatization is a process of algorithmically applying morphological analysis to the structure of words in order to determine the most basic & meaningful form. Although it is a slower normalization method due to the processing involved, it can often produce very good results. For sentiment analysis, emoticons can be high-value indicators of a document’s tone, so I let non-alpha characters remain.

### Results

#### Pre- vs Post 2016 Election Cycle

Sentiment analysis on the pre- election cycle (2006-July 2016) corpus of over 30,000 tweets showed Natives receiving slightly more positivity than not, at 63.14%. This corpus contained a mix of larger (several thousand or more) and smaller accounts.

Post July 2016 data show a downward shift in sentiment in replies to the mixed-size group: across more than 49,000 tweets, positive responses went down to 57.23%, a nearly six-point downward shift.

The 2016 election cycle marks a measurable increase in negativity directed towards Indigenous accounts:

[<img src="https://raw.githubusercontent.com/IndigenousEngineering/In-Reply/master/dataviz/gen_group_neg_replies_by_date.png" alt="Negative sentiment in replies towards Natives has increased measurably since the 2016 election cycle" width="500"/>](https://github.com/IndigenousEngineering/In-Reply/in_reply_1.ipynb)

Larger Native accounts fared only slightly better during and after the election cycle, with positive tweets making up 59.55% of all replies tested. To get a better sense of potential differences within this group, I created a corpus of replies to each account & tested their sentiment individually.

#### Tribal Sovereignty & DNA

From the focused list of larger Native accounts, two users in particular scored similarly lower than the rest. At only 58.88% and 58.39% positive responses respectively, [@KimTallBear](https://twitter.com/KimTallBear) & [@pollysgdaughter](https://twitter.com/pollysgdaughter) stood out for their similar scores & related content. 

Both accounts are known for their writing on tribal sovereignty, DNA & false Native heritage claims. Given that these remain highly contested issues by non-Natives on both sides of the political spectrum, it is perhaps not surprising to see that these accounts attracted the most  negative comments out of the group.

#### Black Natives

Out of all groups tested, Black Natives received the most negativity & the lowest numbers of positive replies to their tweets. While in most tests, larger accounts tended to receive less negative feedback, for Black Natives the opposite trend emerged. 

In fact the largest account I tested from this group, with over 9,000 followers at the time, received the _most_ negative responses to tweets out of all individual accounts I checked: only 54.6% positive responses. Given these results it seems reasonable to infer that increased visibility for Black Natives online can lead to increased harassment. (For this reason I have chosen not to publish the handles of these accounts here.)

[<img src="https://raw.githubusercontent.com/IndigenousEngineering/In-Reply/master/dataviz/neg_responses_vs_followers_Black_Native_accounts.png" alt="As Black Native accounts attract more followers, they also receive an increase in hostile responses." width="500"/>](https://github.com/IndigenousEngineering/In-Reply/in_reply_1.ipynb)

### Results At-A-Glance

#### Sentiment Shift Towards Natives Since 2016 Election:


| date range | total replies | negative replies| % negative|
|:----------:|:-------------:|:---------------:|:---------:|
| 2006 - July 2016 | 30,658 | 11,298 | 36.86 % |
| July 2016 - 2020 | 49,391 | 21,121 | 42.77 % |

####  Increase in Hostile Terms & Suicide References:

| group | replies | hostile/suicide reference | % hostile |
|:----------:|:-------------:|:---------------:|:---------:|
| general pre - 2016 | 30,658 | 641 | 2.0 % |
| general post - 2016 | 49,391 | 1,435 | 2.9 % |
| focused list post - 2016 | 52,634 | 1,999 | 3.79 % |

#### Black Native Accounts Receive the Most Negativity:

| account | followers | replies | negative replies | % negative |
|:--------:|:-----:|:---------------:|:---------:|:----------:|
| Account 1 | 2,076 | 866 | 357 | 41.2 % |
| Account 2 | 2,395 | 1,000 | 412 | 41.2 % |
| Account 3 | 4,575 | 1,000 | 444 | 44.4 % |
| Account 4 | 9,197 | 1,000 | 454 | 45.4 % |

### Conclusion

Anecdotal evidence suggests that the 2016 election cycle unleashed increased negativity and outright harassment against Indigenous people online. My models support this conclusion. Even without tuning, the model was able to find measurable differences in the pre- vs- post election cycle conversation. 

My model also provides evidence that accounts dealing with tribal sovereignty & false heritage claims fare worse overall in terms of positive responses. This matches Natives’ reported experience with increased vitriol during and since the 2016 election.

Finally, Black Natives have long spoken about inequities they experience in online spaces & particularly when participating in the “Native Twitter” community.  My model shows that for the accounts I tested these experiences are more than perception; they are a reality that a Naive Bayes classifier can quantify. Further investigation is warranted into ways the community can better support & protect Black Natives online.

Participating in social media can be a double-edged sword for Indigenous people. While many Natives find lifesaving community, connection, and a voice online, online presence can also open them to increased harassment. The 2016 election cycle appears to have measurably increased negativity in replies to Natives; this is sobering information given the well-documented links between online harassment and mental health issues/suicide, and the CDC’s 2019 report showing an increase in death by suicide for Native womxn and men far outpacing any other group, at 139% and 71% repsectively. 

Social media companies should take note, and then take action: with vast data & computing resources at their disposal, they should be leading, not lagging, in recognizing & discouraging destructive/hate speech on their platforms. It is imperative, and--armed with data--*very possible* for us to innovate in protecting the most vulnerable members of our communities.


_All code for this project is available in [this repo](https://github.com/IndigenousEngineering/In-Reply/blob/master/in_reply_1.ipynb)._


_If you are struggling with suicidal thoughts there is hope & support. Please reach out._

### Resources

**ONLINE**

[Suicide prevention: Indian Health Service](https://www.ihs.gov/suicideprevention/)

[**We R Native**](https://www.wernative.org/articles/wanting-to-end-your-life)

[**National Suicide Prevention Lifeline: for Native Americans**](https://suicidepreventionlifeline.org/help-yourself/native-americans/)

[**National Suicide Prevention Lifeline Main Site**](https://suicidepreventionlifeline.org/)

[**Online chat:**](https://suicidepreventionlifeline.org/chat/) https://suicidepreventionlifeline.org/chat/

**BY PHONE**

**English: 1-800-273-8255**

**Spanish: 1-888-628-9454**

**Hearing impaired/Deaf: 1-800-799-4889**

**Crisis Text Line: Text HOME to 741741**



