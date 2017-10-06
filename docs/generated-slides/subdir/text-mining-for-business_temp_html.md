= A primer on text mining for business
Clément Levallois <levallois@em-lyon.com>
2017-12-08

last modified: {docdate}

:icons!:
:iconsfont:   font-awesome
:revnumber: 1.0
:example-caption!:
:sourcedir: ../../../main/java

:title-logo-image: EMLyon_logo_corp.png[width="242" align="center"]

image::EMLyon_logo_corp.png[width="242" align="center"]
{nbsp} +

//ST: 'Escape' or 'o' to see all sides, F11 for full screen, 's' for speaker notes


== 1. Definitions
//ST: 1. Definitions

//ST: !
"Text mining" refers to using computational methods to find interesting information in texts.

//ST: !
Quasi synonyms:

//ST: !
- natural language processing (abbreviated in NLP)

-> "Natural language" insists on the fact that we deal with "everyday language" (possibly with slang, grammar and spelling errors, etc.)

//ST: !
- computational linguistics (name of a scientific discipline)

-> this expression shows that of course, text mining is practised by computer scientists but linguists as well.
Some approaches to text mining put a heavy emphasis on grammatical notions (structure of sentences etc.), while other methods ignore grammar and syntax completly and still get good results.

//ST: !
A "corpus" is a collection of documents. The plural form exists: corpora. So data scientists doing text mining refer to their "dataset" or "corpus".

== 2. What kind of text?
//ST: 2. What kind of text?

//ST: !
- Books
- Tweets
- Product reviews on Amazon

//ST: !
- LinkedIn profiles
- The whole Wikipedia
- Free text answers in the results of a survey

//ST: !
- Tenders, contracts, laws, …
- Print and online media
- Archival material

//ST: !
The list above is to convey that "text" is virtually everywhere, and as obvious as it seems we should not forget about this diversity of sources.


== 2. What can be done with text mining?
//ST: 2. What can be done with text mining?

//ST: !
[start=1]
==== a. Sentiment analysis

//ST: !
Is this piece of text of a positive or negative tone? This type of text mining is useful to filter a large number of documents and retain only those that need action (eg, addressing negative comments).

Companies are typically interested in sentiment analysis in conjuction with topic modeling: they need to identify which *topic* elates negative sentiments.

For a review of methods for sentiment analysis, see https://arxiv.org/abs/1512.01818[this review article].

//ST: !
[start=2]
==== b. Topic modeling / topic detection

//ST: !
This type of tool aims at discovering the main topic or the multiple topics of a corpus. This is an essential function for:

//ST: !
- exploratory analysis: what is this corpus about?
- categorization: is this document about this or that?
- detection / monitoring: send an alert when a document matching this topic is published
- etc.

//ST: !
(want to know more about topic modelling? Again, the digital humanities are a good starting point. Check http://www.scottbot.net/HIAL/index.html@p=221.html[there], http://www.matthewjockers.net/2013/04/12/secret-recipe-for-topic-modeling-themes/[there] or https://tedunderwood.com/2012/04/07/topic-modeling-made-just-simple-enough/[there].)


//ST: !
[start=3]
==== c. Semantic disambiguation and Named Entity Recognition

//ST: !
How can a software "understand" the difference between "Paris Hilton" and "Hilton Hotel, in Paris"?

//ST: !
Named Entity Recognition (NER) consists in matching an expression with the proper definition, given the context of use. Clever techniques and data sources (like http://wiki.dbpedia.org/[DBPedia]) are used to achieve good results.

//ST: !
Semantic disambiguation or "Word sense disambiguation" consists in finding the meaning of an expression when multiple meanings are possible.

//ST: !
[start=4]
==== d. Automated translation / live translation

//ST: !
See Google translate but also the https://www.skype.com/en/features/skype-translator/[Skype Translator].

//ST: !
[start=5]
==== e. Summarizing

//ST: !
Shortening a text while keeping its core message intact. See https://arxiv.org/abs/1707.02268[this reference] for a short, technical review.


== 3. Ok, amaze me
//ST: 3. Ok, amaze me

//ST: !
[start=1]
==== a. Named Entity Recognition

//ST: !
A demo for Named Entity Recognition (the demo is for a service delivered as an API):

https://dandelion.eu/semantic-text/entity-extraction-demo/

//ST: !
On the website above, try first:

----
Paris Hilton was visiting Paris.
She was interested in books by Jack London, who has written a book about hobboes in London.
----

Then:

 London is bigger than Paris

//ST: !
[start=2]
==== b. A demo of sentiment analysis by a research team at Stanford:

//ST: !

Visit this page and try writing a sentence with a negative or positive emotion / sentiment:

http://nlp.stanford.edu:8080/sentiment/rntnDemo.html


== 4. Frontier of text mining: what works, what is hard, what does not work.
//ST: 4. Frontier of text mining: what works, what is hard, what does not work.

//ST: !
==== a. What works: Profiling of individuals on psycho / political / social dimensions

//ST: !
The current state of text mining  makes it *easy* to profile individuals, based on the texts they write on social networks.

//ST: !
Without text mining, we have access to “external”, “cold” states of the individual:

- behavior (eg, clicks on websites, purchases, subscriptions)
- sociodemo attributes (address, gender)
- social networks (but relatively cold ones)

//ST: !
With text mining, there is access to “internal”, “hot” cognitive states of individuals:

//ST: !
- opinions
- intentions
- preferences

//ST: !
- degree of consensus
- social networks (who mentions whom: how, in which context)
- implicit and very private attributes of the author (eg, sexual orientation)

//ST: !
See these following studies:

//ST: !
http://cnets.indiana.edu/wp-content/uploads/conover_prediction_socialcom_pdfexpress_ok_version.pdf[“Predicting the Political Alignment of Twitter Users” by Conover et al. (2011)].

//ST: !
http://anthology.aclweb.org/C/C14/C14-1019.pdf[“Political Tendency Identification in Twitter using Sentiment Analysis Techniques”
by Pla and Hurtado (2014)].

//ST: !
http://www.pnas.org/content/110/15/5802.abstract[“Private traits and attributes are predictable from digital records of human behavior”
by Kosinski et al. (2013)].

??ST: !
See this article in the New York Times examining the role of https://cambridgeanalytica.org/[Cambridge Analytica] in profiling voters at the service of Donal Trump's campaign in 2016:

https://www.nytimes.com/2017/03/06/us/politics/cambridge-analytica.html

//ST: !
These text mining techniques get even more precise when mixed  with network analysis and machine learning.


//ST: !
[start=2]
==== b. Printed form (or even pdf) is hard

//ST: !
Printed text is typically harder and slower to analyze, because it needs to be scanned first (the technical term is "https://en.wikipedia.org/wiki/Optical_character_recognition[OCR]"). The process of OCR introduces errors.

Check http://www.digitalhumanities.org/dhq/vol/8/1/000168/000168.html[this paper in the Digital Humanities Quarterly] for a deeper look into this issue, in the context of historical research.

//ST: !
And even when the text is in a digital form, it can be hard to use: extracting text from a pdf is not trivial at all, and this is part of https://dss.iq.harvard.edu/blog/extracting-content-pdf-files[the toolchain of data science].

//ST: !
[start=3]
==== c. Multilingual

//ST: !
Many operations in text mining will break when the language changes.

For example, the German language capitalizes nouns. It can be confusing to an algorithm trained on a corpus in English where only names are capitalized: simple nouns could be tagged as first names or family names.

This is just one of many examples. Text mining applications often break, are less efficient and / or are more costly when they handle multiple languages.

//ST: !
[start=4]
==== d. Very informal / colloquial speech

//ST: !
Text mining applications will have a relatively easy time on text published by Reuters news, because it is written in a formal style.

It will have a harder time on a Facebook message written by a teenager, peppered with slang, emojis and spelling shortcuts.


//ST: !
[start=5]
==== e. Detection of irony and sarcasm: progresses but not there yet

//ST: !
This project tries to crack the challenge of detecting irony in short texts: https://deepmoji.mit.edu/

Not working perfectly. Irony is hard because it needs contextual knowledge to guess that the real meaning is different from the literal meaning.

//ST: !
[start=6]
==== f. Robust translation

//ST: !
Translation remains very imperfect.
Again, because the meaning of a sentence or paragraph is crafted from the terms used but also from with the contribution of subtle cues (punctuation, phrasing) which are ignored by current algorithms.

//ST: !
[start=7]
==== g. Reasoning beyond Q&As

//ST: !
IBM Watson is a software which beat human players at the TV Game "Geopardy" (and that was in __2011__)

//ST: !
video::WFR3lOm_xhE[youtube]

//ST: !
Yet, mining text to produce new "reasoning" in general situations by machines has not made much progresses yet.

This topic (reasoning beyond special tasks) is discussed further in the presentation on artificical intelligence.

== 5. Basic operations in text mining - essential vocabulary
//ST: 5. Basic operations in text mining - essential vocabulary

//ST: !
[start=1]
==== a. Tokenization

//ST: !
Tokenization is finding terms in a sentence. For example, "I am Dutch" is tokenized into "I", "am", "Dutch".

Trivial? Not so much. Try tokenizing a sentence in Mandarin!

//ST: !
[start=2]
==== b. Stemming

//ST: !
With stemming, “liked” and “like” will be reduced to their stem “lik” to facilitate further operations

//ST: !
[start=3]
==== c. Lemmatizing

//ST: !
With lemmatizing, “liked”, “like” and “likes” will be grouped to count them as one basic semantic unit

//ST: !
[start=4]
==== d. Part-of-Speech tagging (aka POS tagging)

//ST: !
POS detects the grammatical function of the terms used in a sentence, to facilitate translation or other tasks.

See for example http://nlp.stanford.edu:8080/sentiment/rntnDemo.html[the online demo by the Stanford team] shown above: POS tagging is used to decompose the sentence.

//ST: !
[start=5]
==== e. Bag-of-words model

//ST: !
“Starting the text analysis with a bag-of-words model” means just listing and counting all different words in the text, as a first approach.

//ST: !
[start=6]
==== f. N-grams

//ST: !
The text “I am Dutch” is made of 3 words: I, am, Dutch.

But it can also be interesting to look at bigrams in the text: “I am”, “am Dutch”. Or trigrams: “I am Dutch”.

//ST: !
N-Grams is the general approach of considering groups of n terms in a document.

This can reveal interesting things about frequent expressions used in the text.

//ST: !
A good example of how useful n-grams can be: visit the Ngram Viewer by Google: https://books.google.com/ngrams

== 6. Types of use of text mining for business
//ST: 6. Types of use of text mining for business

//ST: !
Three types of use:

- for market facing activities
- for business management
- for business development


//ST: !
[start=1]
==== a. for market facing activities

//ST: !
- Refined scoring: propensity scores (including churn), scoring of prospects
- Refined individualization of campaigns:  personalized ads, email campaigns, coupons, etc.
- Better community management: getting a clear and precise picture of how customers and prospects perceive, talk about, and engage with your brand / product / industry

//ST: !
[start=2]
==== b. for business management

//ST: !
- Organizational mapping: getting a view of the organization through text flows.

Example: getting a view on the activity of a business school through a map of its scientific publications.

- HRM: finding talents in niche industries, based on the mining of profiles
- Marketing research: refined segmentation + targeting + positioning, measuring customer satisfaction, perceptual mapping.

//ST: !
[start=3]
==== c. for business development

//ST: !
- Developing adjunct services:
* product recommendation systems (eg, Amazon’s)
* detection and matching of needs (eg, detection of complaints / mood changes)
* product enhancements (eg, content enrichment through localization/personalization)

//ST: !
- Developing new products entirely, based on
* different search engines
* innovative alert systems / automated systems based on smart monitoring of textual input
* knowledge databases
* new forms of content curation / high value info creation + delivery


== The end
//ST: The end
//ST: !

Find references for this lesson, and other lessons, https://seinecle.github.io/mk99/[here].

image:round_portrait_mini_150.png[align="center", role="right"]
This course is made by Clement Levallois.

Discover my other courses in data / tech for business: http://www.clementlevallois.net

Or get in touch via Twitter: https://www.twitter.com/seinecle[@seinecle]
pass:[    <!-- Start of StatCounter Code for Default Guide -->
    <script type="text/javascript">
        var sc_project = 11411204;
        var sc_invisible = 1;
        var sc_security = "7b86ca26";
        var scJsHost = (("https:" == document.location.protocol) ?
            "https://secure." : "http://www.");
        document.write("<sc" + "ript type='text/javascript' src='" +
            scJsHost +
            "statcounter.com/counter/counter.js'></" + "script>");
    </script>
    <noscript><div class="statcounter"><a title="site stats"
    href="http://statcounter.com/" target="_blank"><img
    class="statcounter"
    src="//c.statcounter.com/11411204/0/7b86ca26/1/" alt="site
    stats"></a></div></noscript>
    <!-- End of StatCounter Code for Default Guide -->]
