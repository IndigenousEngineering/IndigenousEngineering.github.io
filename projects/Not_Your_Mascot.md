# not your mascot

*opinions vs data*

**Content Note: This post contains references to anti-Indigenous slurs & other racism.**

## Background

Although [extensive peer-reviewed research](https://www.apa.org/pi/oema/resources/indian-mascots) has been conducted into the harm Native mascots cause Indigeous people, both individual [team owners](https://www.usatoday.com/story/sports/nfl/redskins/2013/05/09/washington-redskins-daniel-snyder/2148127/) and the [NFL itself](https://www.espn.com/nfl/story/_/id/22263384/nfl-commissioner-roger-goodell-see-change-washington-redskins-nickname) refuse to take action on changing the names of these teams.

The NFL & its teams claim that they are honoring Natives. Leading Native organizations [say otherwise](http://www.ncai.org/proudtobe).

The team owners strong sentiment against changing the names--despite their [documented harm ](https://www.changethemascot.org/wp-content/uploads/2013/10/DrFriedmanReport.pdf)--is echoed in the public sphere by fans: [USA Today](https://www.usatoday.com/story/sports/columnist/erik-brady/2018/05/09/dan-snyder-redskins-mascot-never-five-years-later/596491002/) identified the word 'NEVER', rendered in all capital letters, as "*a two-syllable rallying cry courtesy of the franchise’s owner on when he will change his club’s embattled team name*" asserting that "*Fans of Washington’s NFL team know precisely what that word means...*"

Is it really possible that R-dskins & Chiefs fans are so intensely passionate about "honoring" Natives?

Or are these teams' names linked to a darker tradition of celebrating American conquest over the Indigenous people on whose stolen land the US was founded?

#### Inspiration

Natives on twitter have articulated the reasons these names are harmful time and time again.

Recently, Mohawk journalist [Vincent Schilling](https://twitter.com/VinceSchilling) [discussed](https://twitter.com/VinceSchilling/status/1219280045736415232?s=20) the names from his perspective as a Native sports editor:

[<img src="https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/Vincent_Schilling_tweet.png" alt="V Schilling tweet" width="500"/>](https://twitter.com/VinceSchilling/status/1219280045736415232?s=20)

Schilling succinctly & eloquently lays out a compelling case for re-examining these names.

The methodology for this project was inspired by twitter user [@EaglesElatis](https://twitter.com/EaglesElatis), who was able to search twitter & [handily deliver a list of racist usages](https://twitter.com/EaglesElatis/status/1219785305106059269?s=20) to another person tweeting in defense of the names:

[<img src="https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/EaglesElatis_tweet.png" alt="@EaglesElatis tweet" width="500"/>](https://twitter.com/EaglesElatis/status/1219785305106059269?s=20)

The team's defender insisted that the terms were no longer in offensive use, however @EaglesElatis was able to quickly & easily demonstrate otherwise. This gave me an idea--why not try the same thing on a much larger scale, working directly with the Twitter API?

My hope is that with a large amount of data showing how these words are used online, the position advocated for by countless Native academics, activists, and organizations--that Native mascots are harmful and should be changed--cannot be ignored.



### Methods

I tested a total of 26 terms, selected because of their negative association with Natives.

It's arguable that some of these terms could be used primarily in the context of so-called sports "trash talk" or have other meanings altogether. So I decided to include some words as controls.

As an example, "dirty r-dskin" is a familiar use of this slur to many Natives, so it was natural to search for this combination of terms. However the word "dirty" has connotations of its own in sports vernacular. One immediate usage that comes to mind refers to sportsmanship--a team can be accused of "playing dirty" etc.

To control for this, I added "filthy", a synonym for "dirty". And indeed it's easy to see that the negative connotations of both these words are in practice strongly associated with the r-dskin slur.

Another example is the word "killed". Natives are familiar with the use of this word in conjunction with the r-dskin slur, frequently in celebration of what is assumed to be Native extinction. However it's easy to imagine a variety of "trash talk" applications for this word--so to help sort typical football discourse from more overt anti-Indigenous hostility, I added words that were strongly correlated with Native American subjects, including the relatively benign "reservation" to the outright offensive (yet often-used) "firewater".

Besides insults, many of the other words I selected based on their tendency to be used in celebrating Native genocide. These also help to act as controls for sports vernacular: while it's possible & even likely a fan might tweet their hope that an opposing team gets "killed" in an upcoming game, it seems considerably less likely that fans would tweet using the words "exterminate" or "extinct".

The words & phrases I have selected do not constitute a comprehensive list; however they will likely be familiar to many Natives as anti-Indigenous insults they encounter on a regular basis.

Words & phrases I tested: *'dirty', 'filthy', 'stupid', 'ugly', 'Indian', 'blood', 'scalp', 'savage', 'dead', 'killed', 'sexy', 'Indian blood', 'drunk', 'injun', 'exterminate', 'extinct', 'firewater', 'reservation', 'smallpox', 'ignorant', 'raped', 'die', 'dumb', 'backwards', 'inbred', 'died'*

### Results

#### Over 170,000 offensive words & phrases

I was able to find a total of instances of 172,768 offensive terms & phrases used in conjunction with racist team names like the R-dskins & the Chiefs in the week leading up to Super Bowl 2020.

The NFL, team owners, & fans claiming that Washington's use of a slur as its team name is not offensive will need to explain away over 45,000 tweets containing violent and/or offensive imagery. This dataset is a resounding counter to the claim that the slur "r-dskins" is no longer used offensively.

The two teams in the 2020 Super Bowl provide the most telling comparison, since these teams could be expected to share a relatively similar amount of "trash talk" in the days leading up to the game.

However that is not what the data show, and the difference could not be more stark: while the San Francisco 49ers team name is itself problematic with deep anti-Indigenous connotations, as demonstrated by over 44,000 rows of tweets containing offensive words & imagery, **the Kansas City Chiefs dataset is nearly twice as long, at *82,386* tweets.**

#### Chiefs vs R-dskins: a Nearly Two-Fold Difference

In a time period where one of these teams is not playing in the Super Bowl--the most famous & well-publicized event in American football--one might expect the slur "r-dskins" to garner the most offensive & hate speech.

However these datasets were prepared from fresh tweets in the week leading up to Super Bowl 2020, featuring the Chiefs vs 49ers--a time when increased visibility focuses on both teams--and offensive term occurrences in the Chiefs corpus are *nearly double* those in the R-dskins corpus. It seems likely that this increased visibility is the cause of the difference between the Chiefs & R-dskins.

Comparing the Chiefs dataset to the 49ers is a useful control due to their 2020 Super Bowl matchup. With nearly twice the occurrences of offensive words & imagery in the Chiefs dataset versus the 49ers, it's clear that increased visibility alone is not responsible for the increased vitriol: the offensive & hate speech is also demonstrably tied to race.

This fact, combined with the frequencies of terms directly linked to Indigenous stereotypes etc & their differentials within the datasets, constitutes strong evidence that mascots evoking Natives are directly linked to an increase of anti-Indigenous hate speech.


#### Offensive Speech Tied to Mascots Hurts Indigenous People

If an increase in visibility results in a measurable two-fold difference in offensive, race-related speech online, it seems reasonable to infer that the visibility of teams like the R-dskins and the Chiefs results in an increase of offensive & outright hate speech directed at Natives. Personal accounts suggest exactly that.

### Term-by-Term: 49ers vs Chiefs

While the trend of increased racially-associated negative speech is clearly visible when Native mascots are grouped together, the differences come into even sharper focus when we directly compare terms by team.

To do this, I created a dataframe containing only two corpora: the Chiefs and the 49ers.

At over 126,000 rows containing offensive words and phrases, this 49ers-vs-Chiefs matchup contains a Super Bowl-sized cache of data.

#### Six Figures of Violence, Insults & Hate

The 49ers & Chiefs corpus contains 126,890 rows with at least 1 negative/offensive term tested.

These tweets were all gathered from the week prior to Super Bowl 2020.

#### Trends Across Terms: Native Mascots Linked to Hate

With a side-by-side comparison of all terms tested, grouped by the two teams contending for Super Bowl 2020, clear trends emerge.

The group of bars on the left correspond to terms within the 49ers corpus. The bars on the right represent terms from the Chiefs corpus.

[![all terms by team](https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/NYM_all_terms_by_team.png)](https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/Not_Your_Mascot_dataviz.ipynb)

The occurrence of negative-to-hate speech is markedly higher in the Chiefs corpus vs. the 49ers.

In addition, the tail of the Chiefs chart is considerably longer, representing the increased frequencies of rarer words that are more closely associated with anti-Native discriminatory speech.

#### Top 10 Most Frequently Appearing Terms by Team

All of the top 5 most frequently appearing terms--and seven of the top 10--come from the Chiefs dataset:

[![top 10 terms and teams](https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/top_10_terms_and_teams.png)](https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/Not_Your_Mascot_dataviz.ipynb)

### Terms Side-by-Side

Examining individual terms, we can see an even more compelling case for the link between Native mascots & hate speech.

The Chiefs lead the 49ers *dramatically* in occurences for nearly every negative term or phrase tested.

[![individual terms by team](https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/indiv_terms_by_team_pivot_all.png)](https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/Not_Your_Mascot_dataviz.ipynb)

#### Offensive Words & Associations: "Indian", "Inbred", "Firewater", "Scalp"

A number of offensive words & associations appear at a much higher frequency within the Chiefs dataset, vs the 49ers.

While it's possible that *some* instances of *some* words could be attributed to football trash-talk & not outright racism, it is difficult to argue that the word "scalp", even used in this context, is part of the typical sports vernacular. Such use is blatantly racist.

Similar arguments could be made for terms like "inbred" and "injun".

Additionally, there is no realistic context easily imaginable for the use of terms like "smallpox" and "firewater" within this dataset having anything other than racist overtones.

#### "Firewater"

[<img src="https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/firewater.png" alt="drawing" width="500"/>](https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/Not_Your_Mascot_dataviz.ipynb)

#### "Inbred"

[<img src="https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/inbred.png" alt="drawing" width="700"/>](https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/Not_Your_Mascot_dataviz.ipynb)

#### "Injun"

[<img src="https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/injun.png" alt="drawing" width="700"/>](https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/Not_Your_Mascot_dataviz.ipynb)

#### "Smallpox"

[<img src="https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/smallpox.png" alt="drawing" width="700"/>](https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/Not_Your_Mascot_dataviz.ipynb)

#### "Scalp"

[<img src="https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/scalp.png" alt="drawing" width="700"/>](https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/Not_Your_Mascot_dataviz.ipynb)

#### Violent Imagery Takes On New, Hateful Dimensions

Some of the imagery evoked by these terms is particularly violent. Moreover, it is difficult to explain away occurrences within the Chiefs dataset of words like "exterminate" as simple "trash talk"--particularly given the term's absence from 49ers discourse.

According to the [US Department of Justice](https://www.bjs.gov/content/pub/pdf/aic.pdf):

**_“American Indians are more likely than people of other races to experience violence at the hands of someone of a different race.”_**

Given the demonstrable racial overtones of this data and [epidemic of violence against Native womxn](https://www.theguardian.com/commentisfree/2019/may/02/missing-murdered-indigenous-women-deb-haaland), **it is difficult not to find these corpora concerning:**

#### "Raped"

[<img src="https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/raped.png" alt="drawing" width="700"/>](https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/Not_Your_Mascot_dataviz.ipynb)

#### "Exterminate"

[<img src="https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/exterminate.png" alt="drawing" width="700"/>](https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/Not_Your_Mascot_dataviz.ipynb)

#### "Die"

[<img src="https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/die.png" alt="drawing" width="700"/>](https://github.com/IndigenousEngineering/Not_Your_Mascot/blob/master/dataviz/Not_Your_Mascot_dataviz.ipynb)


## Conclusion

Despite documented harm from Native mascots, & [repeated requests for change from Natives](http://www.ncai.org/attachments/PolicyPaper_mijApMoUWDbjqFtjAYzQWlqLdrwZvsYfakBwTHpMATcOroYolpN_NCAI_Harmful_Mascots_Report_Ending_the_Legacy_of_Racism_10_2013.pdf) both team owners and the NFL refuse to take action to change the names, citing, among other reasons, both the words' shift in contemporary usage & an intent to "honor" Natives.

But these arguments don't hold water in the face of over *one hundred seventy-two thousand*  (172,768 to be precise) instances of negative- to outright hate speech used in conjunction with these team names in the week leading up to the Super Bowl. Comparing tweets containing the team name "Chiefs" with those containing "49ers" provides a useful control both for Native mascots and Super Bowl spotlight; the results demonstrate a marked increase in negative & violent speech associated with the Chiefs.

Given the clear & demonstrable racial correlation, the dramatic increases of violent & hateful rhetoric around the Native-named Chiefs--particularly in light of the epidemic of violence against Indigenous womxn and girls, and high rates of Native victimization by non-Natives--should give anyone still arguing that these names aren't harmful extreme pause.

Advocates for changing the names now have contemporary (English) natural language data, on a large scale, to back up their anecdotal evidence that these words are still used in hateful ways against Natives online. Datasets are freely available for research use [here](https://github.com/IndigenousEngineering/Not_Your_Mascot-build/tree/master/datasets). A CSV containing all tweets, including terms & team info, is available [here](https://github.com/IndigenousEngineering/Not_Your_Mascot-build/blob/master/datasets/Not_Your_Mascot_Full_DF.zip). A Jupyter notebook containing all code is available [here](https://github.com/IndigenousEngineering/Not_Your_Mascot-build/blob/master/Not_Your_Mascot_full.ipynb).

Natives [have spoken](https://www.changethemascot.org/supporters-of-change/).

The data has now spoken.

Will the NFL finally listen?
