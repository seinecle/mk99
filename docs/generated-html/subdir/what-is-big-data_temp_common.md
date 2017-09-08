= What is big data?
Clément Levallois <levallois@em-lyon.com>
2017-31-07

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

//ST: !

== Reading list
Find the reading list for this session on Pinterest:
https://fr.pinterest.com/seinecle/what-is-data-what-is-big-data/

== 1. Big data is a mess
//ST: 1. Big data is a mess

image::ariely.png[align="center", title="Facebook post by Dan Ariely in 2013"]
{nbsp} +

//ST: !

Jokes aside, defining big data and what it covers needs a bit of precision. Let's bring some clarity.

== 2. The 3 V
//ST: 2. The 3 V

Big data is usually described with the "3 Vs":

//ST: !
==== *V* for Volume
//ST: !

The size of datasets available today is staggering (ex: Facebook had 250 billion pics in 2016).

We should also note that the volumes of data are increasing at an *accelerating rate*. According to sources, https://www.sciencedaily.com/releases/2013/05/130522085217.htm["90% of all the data in the world has been generated over the last two years"] (statement from 2013) or said differently, https://appdevelopermagazine.com/4773/2016/12/23/more-data-will-be-created-in-2017-than-the-previous-5,000-years-of-humanity-/["More data will be created in 2017 than the previous 5,000 years of humanity"]

//ST: !
==== *V* for Variety
//ST: !

This is a bit less intuitive. "Variety" means here that data is increasingly unstructured and messy, and this is an important characteristic of the "big data" phenomenon. To carictature a bit, try to picture a shift from A to B:

//ST: !

*A - Structured data*:

phonebooks, accounting books, governmental statistics... anything that can be represented as well organized tables of numbers and short pieces of text with the expected format, size, and conventions of writing.

image::book.png[align="center", title="A book of accounts showing structured data"]
{nbsp} +

//ST: !
*B - Unstructured data*:

datasets made of "unruly" items: text of any length, without proper categorization, encoded in different formats, including possibly pictures, sound, geographical coordinates and what not...

//ST: !

image::unstructured-data.png[align="center", title="Structured vs unstructured data"]
{nbsp} +

//ST: !
==== *V* for Velocity
//ST: !

In a nutshell, the speed of creation and communication of data is accelerating (http://www.zdnet.com/article/volume-velocity-and-variety-understanding-the-three-vs-of-big-data/[examples taken from here]):

//ST: !

- Facebook hosts 250 billion pics? It receives 900 million more pictures *per day*
- Examining tweets can be done automatically (with computers). If you want to connect to Twitter to receive tweets in real time as they are tweeted, be prepared to receive in excess of 500 million tweets *per day*. Twitter calls this service the http://support.gnip.com/apis/firehose/["firehose"], which reflects the velocity of the stream of tweets.

//ST: !
image::firehose.jpg[align="center", title="The Twitter Firehose"]
{nbsp} +
//ST: !

- Sensor data is bound to increase speed as well. While pictures, tweets, individual records... are single item data sent at intervals, more and more sensors can send data *in a continuous stream* (measures of movement, sound, etc.)

//ST: !

So, velocity poses challenges of its own: while a system can handle (store, analyze) say 100Gb of data in a given time (day or month), it might not be able to do it in say, a single second. Big data refers to the problems and solutions raised by the velocity of data.

//ST: !
==== A 4th *V* can be added, for Veracity
//ST: !

Veracity relates to trustworthiness and compliance: is the data authentic? Has it been corrupted at any step of its processing?

We will devote a session of this course to data compliance, which is a broad topic covering data privacy, cybersecurity, and the societal impacts of data.

https://fr.pinterest.com/seinecle/data-compliance/[You can start reading the documents for this course here]

== 3. What is the minimum size to count as "big data"? It's all relative
//ST: 3. What is the minimum size to count as "big data"? It's all relative

//ST: !

There is no "threshold" or "minimum size" of a dataset where "data" would turn from "small data" to "big data".

It is more of a *relative* notion: it is big data if current IT systems struggle to cope with the datasets.

(see https://en.wikipedia.org/wiki/Big_data[Wikipedia definition] developing on this.)

//ST: !

"Big data" is a relative notion... how so?

//ST: !

==== 1. relative to time
//ST: !

*  what was considered "big data" in the early 2000s would be considered "small data" today, because we have better storage and computing power today.
* this is a never ending race: as IT systems improve to deal with "current big data", data gets generated in still larger volumes, which calls for new progress / innovations to handle it.

//ST: !
[start=2]
==== 2. relative to the industry
//ST: !

* what is considered "big data" by non tech SMEs (small and medium-sized entreprises) can be considered trivial to handle by tech companies.

//ST: !
[start=3]
==== 3. not just about size
//ST: !

* the difficulty for an IT system to cope with a dataset can be related to the size (try analyzing 2 Tb of data on your laptop...), *but also* related to the content of the data.

//ST: !
* For example the analysis of customer reviews in dozens of languages is harder than the analysis of the same number of reviews in just one language.

//ST: !
* So the general rule is: the less the data is structured, the harder it is to use it, even if it's small in size (this relates to the "V" of variety seen above).

//ST: !
[start=4]
==== 4. no correlation between size and value
//ST: !

* Big data is often called https://hbr.org/2012/11/data-humans-and-the-new-oil["the new oil"], as if it would flow like oil and would power engines "on demand".

//ST: !

* Actually, big data is *created*: it needs work, conception and design choices to even exist (what do I collect? how do I store it? what structure do I give to it?). The human intervention in creating data determines largely whether data will be of value later.

//ST: !

* Example: Imagine customers can write online reviews of your products. These reviews are data.
But if you store these reviews without an indication of who has authored the review (maybe because reviews can be posted without login oneself), then the reviews become much less valuable.
Simple design decisions about how the data is collected, stored and structured have a huge impact on the value of the data.

//ST: !
So, in reaction to large, unstructured and badly curated datasets with low value at the end, a notion of "smart data" is sometimes put forward: data which can be small in size but which is well curated and annotated, enhancing its value (see also https://www.quora.com/After-Big-Data-Smart-Data-is-a-trend-in-2013-So-what-is-Smart-Data-Have-any-clear-definition[here]).

//ST: !
[start=5]
==== 5. as an expression, "big data" is evolving
//ST: !

* It is interesting to note that "hot" expressions, like "big data", tend to wear out fast. They are too hyped, used in all circumstances, become vague and over sold.
For big data, we observe that it is peaking in 2017, while new terms appear:

//ST: !
pass:[<iframe scrolling="no" style="border:none;" width="640" height="600" src="https://www.google.com/trends/fetchComponent?hl=en-US&amp;q=big data,machine learning,artificial intelligence%20&amp;content=1&amp;cid=TIMESERIES_GRAPH_0&amp;export=5&amp;w=640&amp;h=600"></iframe> ]

image::gtrends.png[align="center", title="Google searches for big data, machine learning and AI"]
{nbsp} +

//ST: !

What are the differences between these terms?

* "Big data" is by now a generic term

* "Machine learning" puts the focus on the scientific and software engineering capabilities enabling to do something useful with the data (predict, categorize, score...)

//ST: !

* "Artificial intelligence" puts the emphasis on human-like possibilities afforded by machine learning. Often used interchangeably with machine learning.

* And "data science"? This is a broad term encompassing machine learning, statistics, ... and any analytical methods to work with data and interpret it. Often used interchangeably with machine learning. "Data scientist" is a common job description in the field.

== 4. Where did big data come from?
//ST: 4. Where did big data come from?
//ST: !

[start=1]
==== 1. Data got generated in bigger volumes because of the digitalization of the economy
//ST: !

image::Movie-theater-vs-Netflix.png[align=center, title="Movie theater vs Netflix"]
{nbsp} +

//ST: !
[start=2]
==== 2. Computers became more powerful
//ST: !

image::Moore's-law.png[align=center, title="Moore's law"]
{nbsp} +


//ST: !
[start=3]
==== 3. Storing data became cheaper every year
//ST: !

image::Decreasing-costs-of-data-storage.png[align=center, title="Decreasing costs of data storage"]
{nbsp} +

//ST: !
[start=4]
==== 4. The mindset changed as to what "counts" as data
//ST: !

* Unstructured (see above for definition of "unstructured") textual data was usually not stored: it takes a lot space, and software to query it was not sufficiently developped.

//ST: !
* Network data (also known as graphs) (who is friend with whom, who likes the same things as whom, etc.) was usually neglected as "not true observation", and hard to query. Social networks like Facebook made a lot to make businesses aware of the value of graphs (especially https://en.wikipedia.org/wiki/Social_graph[social graphs]).

//ST: !
* Geographical data has democratized: specific (and expensive) databases existed for a long time to store and query "place data" (regions, distances, proximity info...) but easy-to-use solutions have multiplied recently.


//ST: !
[start=5]
==== 5. With open source software, the rate of innovation accelerated
//ST: !

In the late 1990s, a rapid shift in the habits of software developers kicked in: they tended to use more and more open source software, and to release their software as open source.
Until then, most of the software was "closed source": you buy a software *without the possibility* to reuse / modify / augment its source code. Just use it as is.

//ST: !

Open source software made it easy to get access to software built by others and use it to develop new things. Today, all the most popular software in machine learning are free and open source.

See the Wikipedia article for a developed history of open source software: https://en.wikipedia.org/wiki/History_of_free_and_open-source_software

//ST: !
[start=6]
==== 6. Hype kicked in
//ST: !

The http://www.gartner.com/technology/research/methodologies/hype-cycle.jsp[Gartner hype cycle] is a tool measuring the maturity of a technology, differentiating expectations from actual returns:

//ST: !

image::Gartner-Hype-Cycle-for-2014.png[align=center, title="Gartner Hype Cycle for 2014"]
{nbsp} +

//ST: !

This graph shows the pattern that all technologies follow along their lifetime:

//ST: !

- at the beginning (left of the graph), an invention or discovery is made in a research lab, somewhere. Some news reporting is done about it, but with not much noise.
- then, the technology starts picking the interest of journalists, consultant, professors, industries... expectations grow about the possibilities and promises of the tech. "With it we will be able to [insert amazing thing here]"

//ST: !

- the top of the bump is the "peak of inflated expectations". All techs tend to be hyped and even over hyped. This means the tech is expected to deliver more than it surely will, in actuality. People get overdrawn.
- then follows the "Trough of Disillusionment". Doubt sets in. People realize the tech is not as powerful, easy, cheap or quick to implement as it first seemed. Newspapers start reporting depressing news about the tech, some bad buzz spreads.

//ST: !

- then: slope of Enlightenment. Heads get colder, expectations get in line with what the tech can actually deliver. Markets stabilize and consolidate: some firms close and key actors continue to grow.
- then: plateau of productivity. The tech is now mainstream.

//ST: !
(all technology can "die" - fall into disuse - before reaching the right side of the graph of course).

In 2014, big data was near the top of the curve: it was getting a lot of attention but its practical use in 5 to 10 years were still uncertain. There were "great expectations" about its future, and these expectations drive investment, research and business in big data.


//ST: !

In 2017, "big data" is still on top of hyped technologies, but is broken down in "deep learning" and "machine learning". Note also the "Artificial General Intelligence" category:

//ST: !

image::Gartner-Hype-Cycle-for-2017.png[align=center, title="Gartner Hype Cycle for 2017"]
{nbsp} +


//ST: !
[start=7]
==== 6. Big data transforms industries, and has become an industry in itself
//ST: !

Firms active in "Big data" divide in many subdomains: the industry to manage the IT infrastructure for big data, the consulting firms, software providers, industry-specific applications, etc...

-> the field is huge.

//ST: !
Matt Turck, https://twitter.com/mattturck[VC at FirstMarkCap], creates every year a sheet to visualize the main firms active in these subdomains.
This is the 2017 version:

//ST: !
image::Matt-Turck-FirstMark-2017-Big-Data-Landscape.png[align=center, title="Big data landscape for 2017"]
{nbsp} +

//ST: !

You can find a high res version of this pic, an Excel sheet version, and a very interesting comment https://mattturck.com/bigdata2017/[all here].

== 5. What is the future of big data?
//ST: 5. What is the future of big data?
//ST: !

[start=1]
==== 1. More data is coming
//ST: !

The Internet of things (IoT) designates the extension of Internet to objects, not just web pages and emails (https://seinecle.github.io/IoT4Entrepreneurs/[see here for details]).

//ST: !

These connected objects are used to *do* things (display stuff on screen, pilote robots, etc.) but also very much to *collect data* in their environments (through sensors).

The development of connected objects will lead to a tremendous increase in the volume of data collected.

We have a session devoted to IoT later in this course. You can already starting reading the documents for this session:

- https://fr.pinterest.com/seinecle/internet-of-things/[Internet of things]

//ST: !
[start=2]
==== 2. Discussions about big data will fuse with AI
//ST: !
Enthusiasm, disappointment, bad buzz worries, debates, promises... the discourse about AI will grow. AI is fed on data, so the future of big data will intersect with what AI becomes.

//ST: !
We have a session devoted to data science / machine learning / AI later in this course. You can already start reading the documents for this course:

- https://fr.pinterest.com/seinecle/what-is-data-science/[What is data science?]
- https://fr.pinterest.com/seinecle/ai-applications-in-business/[AI applications in business]

//ST: !
[start=3]
==== 3. Regulatory frameworks will grow in complexity

//ST: !
Societal impacts of big data and AI are not trivial, ranging from racial, financial and medical discrimination to giant data leaks, or economic (un)stability in the age of robots and AI in the workplace.

//ST: !
Public regulations at the national and international levels are trying to catch up with these challenges. As technology evolves quickly, we can anticipate that societal impacts of big data will take center stage.

//ST: !
We have a session devoted to data compliance in this course. You can already start reading the documents for this course:

- https://fr.pinterest.com/seinecle/data-compliance/[Data compliance]

//ST: !

== The end
//ST: The end
//ST: !

Find references for this lesson, and other lessons, https://seinecle.github.io/mk99/[here].

image:round_portrait_mini_150.png[align="center", role="right"]
This course is made by Clement Levallois.

Discover my other courses in data / tech for business: http://www.clementlevallois.net

Or get in touch via Twitter: https://www.twitter.com/seinecle[@seinecle]
