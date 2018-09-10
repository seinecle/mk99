= Preface

== A textbook for managers

The target reader for this book is a manager who needs to clearly understand the business stakes of "data science", "big data", "APIs" and "artificial intelligence" so that they can:

- *leverage* these technologies to improve the efficiency of their current business,
- *innovate* with new products and services

The promise of this book is to bring you from a starting point with no knowledge of these technical concepts, to a point where you understand the concepts *and* you can develop "data centric" business projects: when "data" contributes to creating value for customers and all stakeholders.


== Is this too technical or too easy for you?

This book does not assume any technical pre-requisite. It uses simple terms and a progressive learning curve to lead you to a comprehensive understanding of the topics.

If you are unsure, try this simple test: http://bit.ly/essentials-1-test

-> There are 20 topics. See how you score. If the score is below 12, this volume is for you.

== Online support and material

- An online version of the chapters of this book is available at https://seinecle.github.io/mk99/.
- Blogs, videos, links... are frequently updated to cover emerging topics, and curated on Pinterest: https://www.pinterest.fr/seinecle/
- You are invited to open discussions with the author and readers of the book by using this "issue tracker" system: https://github.com/seinecle/mk99/issues

== Version

This version was last modified: {docdate}





= Chapter 1. Data, a concept with multiple layers
'''

== Definition of data


The English term "data" (1654) originates from  http://www.etymonline.com/index.php?term=data["datum", a Latin word for "a given"].
"Data" is a single factual, a single entity, a single point of matter.
The word "data" to mean "transmittable and storable computer information" was first used in this sense in 1946.
The expression "data processing" was first used in 1954.

[TIP]
====
Thoughts: the etymology suggests that data is "a given". Can you question this?
====

Data represents either a single entity, or a collection of such entities ("data points").
We can speak also of datasets instead of data (so a dataset is a collection of data points).

== The variety of data sets


|===
|||

|A date
|A color
|A grade

|A relation of friendship
|A sound
|A heartbeat

|A user input
|A duration
|A curriculum vitae

|===


|===
|||

|A picture
|A longitude and latitude
|A price

|A number of friends
|A temperature
|A list of favorite movies

|etc...
|etc...
|etc...
|===

These examples are chosen on purpose to be varied and from unexpected places.
They illustrate three principles:

=== a. Think about data in a broad sense

Data is not just numerical, neither is it "what sits in my spreadsheets". You should train in thinking about data in a broader sense:

- pictures are data
- language is data (including slang, lip movements, etc.)
- relations are data: individual A is known, individual B is known, *but the relationship between A and B is data as well*
- preferences, emotional states... are data
- etc. There is no definitive list, you should train yourself looking at business situations and think: "where is the data?"

=== b. metadata is data, too

Metadata is a piece of data describing another data.
Example:
----
The bibliographical reference <1>
describing
a book <2>
----
<1> the metadata
<2> the data

- Data without ((metadata)) can be worthless (imagine a library without a library catalogue)
- Metadata can be informative in its own right, as shown with the ((NSA)) scandal (read this article from the New Yorker about http://www.newyorker.com/news/news-desk/whats-the-matter-with-metadata[NSA and metadata]).


=== c. zoom in, zoom out

We should remember considering that a data point can be itself a collection of data points:

- a person walking into a building is a data point.
- however this person is itself a collection of data points: location data + network relations + subscriber status to services + etc.

It is a good reflex to wonder whether a data point can in fact be "unbundled" (spread into smaller data points / measurements)

== How to describe datasets


=== a. Formats, types, encoding

image::tweet.png[align="center",book="keep"]
{nbsp} +

- This is a digital *medium* (because it's on screen as opposed to analogical, if we had printed the pic on paper)
- The *type* of the data is textual + image
- The text is formatted in *plain text* (meaning, no special formatting), as opposed to *data-interchange formats* which are formatting marks added to the text to facilitate its readability by software (check https://codingislove.com/json-tutorial-indepth/[csv, json and xml]).
- The *encoding* (((data, encoding))) of the text is UTF-8 (one of encodings deriving from the Unicode standard). Encoding deals with the issue: how to represent alphabets, signs (for instance: emojis) and symbols, from different languages, in text? UTF-8 is an encoding which is one of the most universal.
- The tweet is part of a list of tweets. The list represents the *data structure* (((data, structure))) of the dataset, it is the way the data is organized. There are many alternative data structures: arrays, sets, dics, maps...
- The tweet is stored as a picture (png file) on the hard disk. "png" is the *file format*. The data is *persisted* as a file on disk (could have been stored in a database instead).

=== b. Tabular data

*Tabular data* ((( data, tabular))) is a common way to handle datasets, by organizing it in lines and columns:

image::table.png[pdfwidth="100%", align="center", title="tabular data", book="keep"]
{nbsp} +

=== c. First party, second party and third party data

- *First party data* (((data, "first party data"))): the data generated through the activities of your own organization.
Your organization own it, which does not mean that consent from users is not required, when it comes to personal data.
- *Second party data* (((data, "second party data"))) : the data accessed through partnerships.
Without being the generator nor the owner of this data, partners make it available to you through an agreement.
- *Third party data* (((data, "third party data"))): the data acquired via purchase.
This data is acquired through a market transaction. Its uses still comes with conditions, especially for personal data.

=== d. Sociodemo data vs behavior data

- Sociodemogaphic or *sociodemio* (((data, sociodemo))) data refers to information about individuals, describing fundamental attributes of their social identity: age, gender, place of residence, occupation, marital status and number of kids.
- *Behavior data* (((data, behavior))) refers to any digital trace left by the individual in the course of it life: clicks on web pages, likes on Facebook, purchase transactions, comments posted on Tripadvisor...
Sociodemo data is typically well structured or easy to structure.
It has a long history of collection and analysis, basically since census exists.
Behavior data allows to profile individuals much more precisely than sociodemo data alone could do: individuals can be characterized by their acts and tastes, well beyond what an age or marital status could define.

How can behavior data "beat" sociodemo data for precision?
It is hard to predict with great accuracy the political, religious or sexual orientation of a given individual just based on their zip code, gender and age. http://www.pnas.org/content/110/15/5802[A research team could evaluate personal attributes with great precision based on the likes individuals make on Facebook pages and posts]. Political orientation (85% accuracy), sexual orientation (75% to 88% accuracy) and religious orientation (82% accuracy) can be determined for persons who had made 170 likes on average.

But behavior data is typically not well structured, which makes it more costly to collect, in term of technological solution, than it costs to collect sociodemo data. The power and accuracy of prediction that behavior data affords also means that individuals should be protected against the possible invasion of their privacy. There are large differences between countries regarding the legal frameworks protecting individuals rights. We discuss this in the chapter on data privacy and the GDPR.

== Data and size



|===
|||

|1 bit
|
|can store a binary value (yes / no, true / false...)


|8 bits
|1 byte (or octet)
|can store a single character

|~ 1,000 bytes
|1 kilobyte (kb)
|Can store a paragraph of text

|~ 1 million bytes
|1 megabyte (Mb)
|Can store a low res picture.
|===


|===
|||

|~ 1 billion bytes
|1 gigabyte (Gb)
|Can store a movie

|~ 1 trillion bytes
|1 terabyte (Tb)
|Can store 1,000 movies. Size of commercial hard drives in 2017 is 2 Tb.

|~ 1,000 trillion bytes
|1 petabyte (Pb)
|20 Pb = Google Maps in 2013
|===

= Chapter 2. A clarification of big data
'''

== Big data is a mess


image::ariely.png[align="center", title="Facebook post by Dan Ariely in 2013", book="keep"]
{nbsp} +


Jokes aside, defining big data and what it covers needs a bit of precision. Let's bring some clarity.

== The 3 V


Big data is usually described with the "((3 Vs))":

=== *V* for Volume

The size of datasets available today is staggering (ex: ((Facebook)) had 250 billion pics in 2016).

We should also note that the volumes of data are increasing at an *accelerating rate*. According to sources, https://www.sciencedaily.com/releases/2013/05/130522085217.htm[90% of all the data in the world has been generated over the last two years] (statement from 2013) or said differently, https://appdevelopermagazine.com/4773/2016/12/23/more-data-will-be-created-in-2017-than-the-previous-5,000-years-of-humanity-/[more data will be created in 2017 than the previous 5,000 years of humanity].

=== *V* for Variety

"Variety" refers to the fact that "unstructured" data is considered to be increasingly useful, when before the big data phenoenon only structured data was considered worth storing and exploiting. This calls to explain in more details the distinction between unstructured and structured data.

(((data, structured vs unstructured)))

==== A - Structured data

*Structured data* (((structured data))) refers to data which is formatted and organized according to a well defined set of rules, which makes it *machine readable*. For example, zip codes are a structured dataset because they follow a precise convention regarding the number of letters and digits composing them, making it easy for an optical reader and software to identify and "read" them. Same with license plates, social security numbers...

But these are simple examples.

What about, for instance, a tax form? If each field of the form is well defined, then the data collected through the form can be said to be "structured". By contrast, a form where the user can write free text (think of a comment on a blog post, or a blank space where users can write a feedback) produces unstructured data: data which does not follow a special convention for its size and content. This is typically much harder for software to process, hence to analyze.

To summarize, think of structured data as as anything that can be represented as well organized tables of numbers and short pieces of text with the expected format, size, and conventions of writing: phonebooks, accounting books, governmental statistics...

image::book.png[align="center", title="A book of accounts showing structured data", book="keep"]
{nbsp} +

==== B - Unstructured data

*Unstructured data* (((unstructured data))) refers to datasets made of "unruly" items: text of any length, without proper categorization, encoded in different formats, including possibly pictures, sound, geographical coordinates and what not...

These datasets are much harder to process and analyze, since they are full of exceptions and differences. But they are carry typically rich information: free text, information recorded "in the wild"...

image::unstructured-data.png[align="center", title="Structured vs unstructured data", book="keep"]
{nbsp} +


=== *V* for Velocity

In a nutshell, http://www.zdnet.com/article/volume-velocity-and-variety-understanding-the-three-vs-of-big-data/[the speed of creation and communication of data is accelerating]:

- Facebook hosts 250 billion pics? It receives 900 million more pictures *per day*
- Examining tweets can be done automatically (with computers). If you want to connect to Twitter to receive tweets in real time as they are tweeted, be prepared to receive in excess of 500 million tweets *per day*. Twitter calls this service the http://support.gnip.com/apis/firehose/["Twitter firehose"], which reflects the velocity of the stream of tweets.


- *Sensor data* (((sensor data))) is bound to increase speed as well. While pictures, tweets, individual records... are single item data sent at intervals, more and more sensors can send data *in a continuous stream* (measures of movement, sound, etc.)


So, velocity poses challenges of its own: while a system can handle (store, analyze) say 100Gb of data in a given time (day or month), it might not be able to do it in say, a single second. Big data refers to the problems and solutions raised by the velocity of data.

=== A 4th *V* can be added, for Veracity

Veracity relates to trustworthiness and compliance: is the data authentic? Has it been corrupted at any step of its processing? Does it comply with local and international regulations?

== What is the minimum size to count as "big data"? It's all relative


There is no "threshold" or "minimum size" of a dataset where "data" would turn from "small data" to "big data".

It is more of a *relative* notion: it is big data if current IT systems struggle to cope with the datasets.


"Big data" is a relative notion... how so?


=== a. relative to time

*  what was considered "big data" in the early 2000s would be considered "((small data))" today, because we have better storage and computing power today.
* this is a never ending race: as IT systems improve to deal with "current big data", data gets generated in still larger volumes, which calls for new progress / innovations to handle it.

[start=2]
=== b. relative to the industry

* what is considered "big data" by non tech SMEs (small and medium-sized enterprises) can be considered trivial to handle by tech companies.

[start=3]
=== c. not just about size

* the difficulty for an IT system to cope with a dataset can be related to the size (try analyzing 2 Tb of data on your laptop...), *but also* related to the content of the data.

* For example the analysis of customer reviews in dozens of languages is harder than the analysis of the same number of reviews in just one language.

* So the general rule is: the less the data is structured, the harder it is to use it, even if it's small in size (this relates to the "V" of variety seen above).

[start=4]
=== d. no correlation between size and value

* https://hbr.org/2012/11/data-humans-and-the-new-oil["Big data is often called the new oil"], as if it would flow like oil and would power engines "on demand".

* Actually, big data is *created*: it needs work, conception and design choices to even exist (what do I collect? how do I store it? what structure do I give to it?). The human intervention in creating data determines largely whether data will be of value later.

* Example: Imagine customers can write online reviews of your products. These reviews are data.
But if you store these reviews without an indication of who has authored the review (maybe because reviews can be posted without login oneself), then the reviews become much less valuable.

Simple design decisions about how the data is collected, stored and structured have a huge impact on the value of the data.

So, in reaction to large, unstructured and badly curated datasets with low value at the end, a notion of "smart data" is sometimes put forward: data which can be small in size but which is well curated and annotated, enhancing its value (see also https://www.quora.com/After-Big-Data-Smart-Data-is-a-trend-in-2013-So-what-is-Smart-Data-Have-any-clear-definition[here]).

== Where did big data come from?


[start=1]
=== a. Data got generated in bigger volumes because of the digitalization of the economy

image::Movie-theater-vs-Netflix.png[align="center", title="Movie theater vs Netflix", book="keep"]
{nbsp} +

[start=2]
=== b. Computers became more powerful

image::Moore's-law.png[align="center", title="Moore's law", book="keep"]
{nbsp} +


[start=3]
=== c. Storing data became cheaper every year

image::Decreasing-costs-of-data-storage.png[align="center", title="Decreasing costs of data storage", book="keep"]
{nbsp} +

[start=4]
=== d. The mindset changed as to what "counts" as data

* Unstructured data (see above for definition of "unstructured") was usually not stored: it takes a lot space, and software to query it was not sufficiently developped.

* Network data (also known as graphs) (who is friend with whom, who likes the same things as whom, etc.) was usually neglected as "not true observation", and hard to query. Social networks like Facebook made a lot to make businesses aware of the value of graphs (especially https://en.wikipedia.org/wiki/Social_graph[social graphs]).

* Geographical data has democratized: specific (and expensive) databases existed for a long time to store and query "place data" (regions, distances, proximity info...) but easy-to-use solutions have multiplied recently.


[start=5]
=== e. With open source software, the rate of innovation accelerated

In the late 1990s, a rapid shift in the habits of software developers kicked in: they tended to use more and more open source software, and to release their software as open source.
Until then, most of the software was "closed source": you buy a software *without the possibility* to reuse / modify / augment its source code. Just use it as is.


*Open source* (((open source))) software made it easy to get access to software built by others and use it to develop new things. Today, all the most popular software in machine learning are free and open source.

See the Wikipedia article for a developed history of open source software: https://en.wikipedia.org/wiki/History_of_free_and_open-source_software

[start=6]
=== f. Hype kicked in

The http://www.gartner.com/technology/research/methodologies/hype-cycle.jsp[((Gartner hype cycle))] is a tool measuring the maturity of a technology, differentiating expectations from actual returns:


image::Gartner-Hype-Cycle-for-2014.png[align="center", title="Gartner Hype Cycle for 2014", book="keep"]
{nbsp} +


This graph shows the pattern that all technologies follow along their lifetime:


- at the beginning (left of the graph), an invention or discovery is made in a research lab, somewhere. Some news reporting is done about it, but with not much noise.
- then, the technology starts picking the interest of journalists, consultant, professors, industries... expectations grow about the possibilities and promises of the tech. "With it we will be able to [insert amazing thing here]"


- the top of the bump is the "peak of inflated expectations". All techs tend to be hyped and even over hyped. This means the tech is expected to deliver more than it surely will, in actuality. People get overdrawn.
- then follows the "Trough of Disillusionment". Doubt sets in. People realize the tech is not as powerful, easy, cheap or quick to implement as it first seemed. Newspapers start reporting depressing news about the tech, some bad buzz spreads.


- then: slope of Enlightenment. Heads get colder, expectations get in line with what the tech can actually deliver. Markets stabilize and consolidate: some firms close and key actors continue to grow.
- then: plateau of productivity. The tech is now mainstream.

(all technology can "die" - fall into disuse - before reaching the right side of the graph of course).

In 2014, big data was near the top of the curve: it was getting a lot of attention but its practical use in 5 to 10 years were still uncertain. There were "great expectations" about its future, and these expectations drive investment, research and business in big data.



In 2017, "big data" is still on top of hyped technologies, but is broken down in "deep learning" and "machine learning". Note also the "Artificial General Intelligence" category:


image::Gartner-Hype-Cycle-for-2017.png[align="center", title="Gartner Hype Cycle for 2017", book="keep"]
{nbsp} +


[start=7]
=== g. Big data transforms industries, and has become an industry in itself

Firms active in "Big data" divide in many sub-domains: the industry to manage the IT infrastructure for big data, the consulting firms, software providers, industry-specific applications, etc...

https://twitter.com/mattturck[Matt Turck, VC at FirstMarkCap], creates every year a sheet to visualize the main firms active in these subdomains.

This is the 2017 version:

<<<<

image::Matt-Turck-FirstMark-2017-Big-Data-Landscape_panorama.png[pdfwidth="100%", align="center", title="Big data landscape for 2017", book="keep"]
{nbsp} +

You can find a https://mattturck.com/bigdata2017/[high res version of the Big data panorama], an Excel sheet version, and a very interesting comment on this website: https://mattturck.com/bigdata2017/

== What is the future of big data?



=== a. More data is coming

The *Internet of things* (((IoT - Internet of things))) designates the https://seinecle.github.io/IoT4Entrepreneurs/[extension of Internet to objects beyond web pages or emails].

The *IoT* (((IoT - Internet of things))) is used to *do* things (display information on screen, pilote robots, etc.) but also very much to *collect data* in their environments, through sensors.

Hence, the development of *connected objects* (((IoT - Internet of things))) will lead to a tremendous increase in the volume of data collected.

=== b. Regulatory frameworks will grow in complexity

Societal impacts of big data and AI are not trivial, ranging from racial, financial and medical discrimination to giant data leaks, or economic (un)stability in the age of robots and AI in the workplace.

Public regulations at the national and international levels are trying to catch up with these challenges. As technology evolves quickly, we can anticipate that societal impacts of big data will take center stage.

=== c. as an expression, "big data" is evolving

* It is interesting to note that "hot" expressions, like "big data", tend to wear out fast. They are too hyped, used in all circumstances, become vague and over sold.
For big data, we observe that it is peaking in 2017, while new terms appear:



image::gtrends.png[pdfwidth="100%", align="center", title="Google searches for big data, machine learning and AI", book="keep"]
{nbsp} +


What are the differences between these terms?

* "Big data" is by now a generic term

* *Machine learning* (((machine learning))) puts the focus on the scientific and software engineering capabilities enabling to do something useful with the data (predict, categorize, score...)


* *Artificial intelligence* (((artificial intelligence))) puts the emphasis on human-like possibilities afforded by machine learning. Often used interchangeably with machine learning. AI is fed on data, so the future of big data will intersect with what AI becomes.

* And *data science* (((data science)))? This is a broad term encompassing machine learning, statistics, and many analytical methods to work with data and interpret it. Often used interchangeably with machine learning. *Data scientist* (((data scientist))) is a common job description in the field.


= Chapter 3. The cloud
'''

== Note on the terminology: what is a server?


To understand the ((cloud)) precisely, We need first to have a clear vision of what a ((server)) is. A server is simply a computer stripped of everything unessential (screen, mouse, graphic card, sound card, keyboard)...


To illustrate: when Google is calculating what the best results are for your search "what are cheap and delicious restaurants in Lyon", this calculation must be done on a computer, right?

The kind of computer used to do this calculation is *not* this one:


image::desktop.jpg[align="center",title="A desktop computer", book="keep"]
{nbsp} +

The reason is, we don't need a screen, mouse, desktop, and not even the big box containing the computer itself.
They take too much space, consume energy, and there is no need for them.

So when all the unnecessary parts are removed, the computer looks like this, and is called a "server":

.https://www.oracle.com/servers/sparc/s7-2/index.html[A server]
image::server.jpg[align="center", book="keep"]
{nbsp} +

Take a look at the shape: rectangular and very slim.
This makes it easy to stack up servers one on the other.
Because for Google and other companies crunching data for their business, a lot of servers are needed, so gaining on space is a real issue.

When many servers are piled up together and put in a big tall box, this is called a *rack* (((server, rack of))) of servers, and look like this:

image::rack.jpg[align="center",title="A rack of servers", book="keep"]
{nbsp} +

When all the racks of servers are put in the same room, this is called a *data center* (((server, data center))) and looks like this:

image::datacenter.jpg[align="center",title="A data center", book="keep"]
{nbsp} +

To get a sens of how "the cloud" is actually a physical space, watch this video showing a tour of a data center at Google:

video::XZmGGAbHqa0[youtube]

Usually, until 2005 roughly, companies had two options:

- buying their own servers and using them on their premises (at their location).
- paying the services of companies specializing in managing data centers.

Then the "cloud" changed this.

== The cloud


The term *cloud* (((cloud, definition))) was made popular by ((Amazon)) with their service “Amazon Elastic Compute Cloud”: *Amazon EC2* (((Amazon, EC2))) launched in 2006.

This service was new in many ways:

- you can rent servers owned by Amazon, at a distance, when you need them, for a duration that you choose.

- there is an emphasis on ease of use: no need to know the technical details of these servers (how they are plugged, how they are configured…)

- you are just given a login + password and you can start using these servers for your needs.

- it's "elastic": if you need more servers, or more powerful servers, it's just possible. No need for signing a new contract or to evaluate whether Amazon has the capacity... it's dimensioned to be possible.

Let's compare a situation with or without the ((cloud)):


[width="100%"]
|=====
|*Without the cloud* |*With the cloud*
|You make a market study for which server to buy

Get the approval by your finance department to buy it (that’s a fixed asset!)

Wait for the server to ship

Install it and configure it

Maintain it (security, etc.)

When the job is over: what do you do with your server? That’s a sunk cost.

If the job happens to need more computing capacity than your server offers: you are stuck with your too-small-server!

|On https://aws.amazon.com/ec2/?nc1=h_ls[Amazon’ EC2 website], you click to choose a server among those on offer: it is *on demand*

You run your job on it. Costs are metered precisely.

When your job is over, you stop the server with a click and pay the bill.

If the job happens to need more computing capacity, you switch to a bigger server with a single click, or it can be done for you automatically: it is *elastic*.
|It is a capex|It is an opex
|=====

The cloud can fit in the budget as an operational expense instead of a capital expenditure.
Opex are not inherently a better or cheaper option than a Capex, but they are easier for a project team or business unit to fit in their budget.
See this blog post discussing  http://gevaperry.typepad.com/main/2009/01/accounting-for-clouds-stop-saying-capex-vs-opex.html[opex and capex in the context of the cloud], especially the critical comments in response, to continue this discussion.

== IaaS, PaaS, Saas


What is the use of the cloud?

Companies can use it to run elementary operations, up to more complex ones:

*Infrastructure as a service* (IaaS)

The cloud is used to replace the company's local IT infrastructure needs such storing data, or computing operations.

*Platform as a Service* (Paas)

The cloud is used to run the building blocks of a service: to manage a messaging system, to host apps, ...

*Software as a Service* (Saas)

The cloud is used to host a full software accessible "on demand" through the browser.
Popular examples are Google Drive, https://www.d2l.com/products/learning-environment/[Brightspace] or https://www.salesforce.com/fr/?ir=1[SalesForce].

== Private or public cloud? Hybrid cloud?


- Amazon EC2 (((Amazon, EC2))) is an example of a *public cloud*: it is publicly accessible to any customer. Of course, this does not mean that every customer can see what the others are doing on the cloud! Each customer have their private spaces on the cloud.

- Many companies have security requirements which prevent them from accessing public clouds.
They need to have their servers on premises.

In this case, they can build their own *private cloud*: it is a cloud just like Amazon EC2, except that it is owned, managed and used by the company exclusively - it is not accessible to third parties.

But even private, the cloud keeps the basic characteristics of a cloud: on-demand and elastic in particular.

- *Hybrid clouds* are a variety of private clouds: it is a private cloud where some forms of operations can be delegated to a public cloud.

For example, operations which are not security sensitive and which need a capacity of computing in excess of what the private cloud of the company can provide.


= Chapter 4. The headache of data integration
'''

== Data: you don't get in on tap



A naive vision of data would get that it's all fluid. Don't we talk about "data streams"?
Working with data would be as simple as opening a tap and "getting customer data", for instance.




Actually, data is more like a complex patchwork: many different pieces which must be stitched together - and this is hard.




Take customer data.

It is not a given. Instead, this is a design made of multiple primary data sources:


image::Multiple-sources-of-customer-data.png[align="center", title="Multiple sources of customer data", book="keep"]
{nbsp} +

> Analysts often spend 50-80% of their time preparing and transforming data sets before they begin more formal analysis work.

Garrett Grolemund, http://shop.oreilly.com/product/0636920035992.do[Data Scientist and Master Instructor at RStudio]



Take away: Data is fragmented by nature. It comes from different sources and presented in different formats.
*You* (the marketer in collaboration with data scientists) wrangle to __construct__ customer profiles by joining and assembling different sources of data into a meaningful synthesis.


Data scientists actually have entire books devoted to the subject of wrangling with the complexity of integrating different data sources.



== Sources of fragmentation



=== a. Channels keep diversifying


Point of sale, print, TV, radio, outdoor posters, mobile apps, mobile sites, emails, SMS, APIs, social networks, search engines, e-commerce platforms, e-commerce websites, blogs, content channels, …

-> all these channels can provide relevant data.


=== b. Connections between these channels intensify and complexify


- Social TV is TV delivered with Internet services,

- User profiles created on one platform are imported on another


- Orders taken online can be picked up on a variety of point of sales

- Ads circulating through one channel replicate on other channels, ...


-> It is very complex to trace the "customer journey" on all these channels and to keep an updated view of a customer profile.

It is even more difficult to explore causality (which action on which channel caused which subsequent action by the user?)


=== c. Underlying technologies fragment and keep evolving, across channels


Browsers, Cookies, APIs, mobile OS (Android or iOS?), etc... All these different techs evolve and need continuous effort and expertise to integrate.


Example: *did you notice* that on a mobile device, the url of the pages you visit can now start with an https://www.ampproject.org/latest/blog/whats-in-an-amp-url/[AMP url]?

Like, to visit the page of the New York Times the url should be http://www.nyt.com but it looks like: *http://google.com/amp/www.nyt.com*

This *http://google.com/amp* prefix is a new tech by Google to accelerate the display of web pages on mobiles. Fine.
But then, as a marketing data analyst, how to count visits to:


http://google.com/amp/www.nyt.com

and

http://www.nyt.com

-> It is important to count visits to these two urls as a visit *to the same page*.


In September 2017 major services of ((web analytics)) were still struggling with this  http://searchengineland.com/google-amp-cache-unified-users-analytics-282069[issue of page counts in web analytics].

This illustrates that to just count visits to a web page (something which should be classic and robust) and integrate this data to a larger analysis, big issues can arise and be hard to fix even in 2017, because of the evolution of techs and standards.


=== d. In the meantime, customers have growing expectations about the quality of service


Difficulties posed by data integration do not slow or decrease customer expectations.
To the contrary, we see an elevation of expectations.
Customers increasingly expect:

- realtime contact
- two-ways interaction (they want to be able to voice their opinion, and get a response)
- seamless experience (no glitch, modern ((user interface)), consistence of the ((user experience)) across channels)
- personalized experience (customization of the message they receive)


=== e. Example: A French bank going through the 2010s


image::Before---a-couple-of-data-sources-across-a-few-channels.png[pdfwidth="80%", align="center", title="Before - a couple of data sources across a few channels", book="keep"]
{nbsp} +


image::Now---many-data-sources-across-a-variety-of-channels.png[pdfwidth="80%", align="center", title="Now - many data sources across a variety of channels", book="keep"]
{nbsp} +



== Tools for data integration: DMPs and more



=== a. Data Management Platform (DMP)


In 2015/2016 a new acronym started to trend: "DMP", standing for *"Data Management Platform"*.

Basically a *DMP* (((DMP - data management platform))) is an information system dedicated to solving the issues of data integration:


- it can store a large amount of data
- it can receive data from a variety of sources, in a variety of formats


- it offers functions to reconcile records from different data sources and generate a unique identifier for each reconciled entry.
- it offers segmentation / classification functions


- it provides security and analytics capabilities on the data
- it makes this data available for execution by other software.


=== b. DMP in relation to other components of the information system

*DMPs* (((DMP - data management platform))) are relatively new. They integrate with 3 other information systems in the firm:

- CRM (((CRM - Customer Relationship Management)))
** This is the software *gathering* data related to customers and sales. It is a major source of *input data* for a DMP.

- ERP (((ERP - Enterprise Resource Planning)))
** Large software synchronizing information systems from finance, sales, logistics and more. The CRM can be independent or part of the ERP.

- DSP (((DSP - Demand Side Platform)))
** https://digiday.com/media/wtf-demand-side-platform/[Piece of software automatizing ad buying]. The audiences identified in the DMP could be served corresponding ads with a DSP.

- Data lake (((data lake)))
** Data lakes are databases specializing in storing large amounts of unstructured data. They respond to the need of "storing today, for future use". A data lake is not meant to be optimized for queries. They are meant to store everything we collect today, in the case this data will serve future usages. When this happens, data can be extracted from the data lake and put in a database, in a form which makes it convenient to query and analyze.

How can data circulate across these software and with the external world? The next chapter is devoted to APIs, another essential concept.

= Chapter 5. APIs and their business relevance
'''

== Definition of API


API: acronym for *Application Programming Interface* (((API, definition)))

An ((API)) is the way to make software programs “easy to plug and share” with other programs.

An API is simply a group of rules (you can also call it a convention, or an agreement...) which programmers follow when writing the part of their code which is in charge of communicating with other software.

These rules are then published (on a webpage for example), so that anyone who needs to connect to the program can learn what rules to follow.

So, an API is simply a way to write code to make it easy to interface with other programs? Yes. Why the fuss then?

Having conventions on how to write a software so that somebody can plug it to its own software is one thing.
https://dzone.com/articles/how-design-good-regular-api[APIs as an aspect of software design] is a classic topic in computer science, but we are not concerned with this here.

APIs we are going to discuss are about communication between distant computers, in a business context.

Let's do a bit of history:

== The origin of APIs


Companies which need to exchange data is nothing new.
Manufacturers, retailers, banks, ... they need to exchange information at regular interval.

Sending invoices, receiving receipts for merchandise, and many other administrative records generated in the course of business.

These receipts, invoices... can be printed and mailed (this solution still exists of course).

With informatics developing in the 1970s and 1980s, a new system emerged: the exchange of information via computers: https://en.wikipedia.org/wiki/Electronic_data_interchange[Electronic Data Interchange] (EDI)

=== a. EDI: Electronic Data Interchange

EDI is not an exchange of file attachments in emails or via a file transfer on a website, because emails and websites did not exist yet! (emails and the Web were adopted by firms in the late 1990s).

Instead, exchanging data via EDI consisted in using complex electronic tools (like the fax but even more complicated) because:

- each industry has its own protocol to exchange data (one protocol for logistics, one for payments, one for this or that retailer chain, etc.)
- you need a dedicated device or software for each EDI protocol, and these are not given for free

- EDI protocols can vary from one country to another
- EDI protocols are controlled by industry associations which do not adopt innovation quickly

and finally, EDI protocols created "closed systems": a company A can connect to company B via an EDI only if the two have a pre-agreement to use this EDI.

So EDIs are fragmented, complicated to implement, slow to evolve, not cheap and restricts the communication to a "club" of partners who agreed to use it.

http://cerasis.com/2014/12/11/edi-in-transportation/[EDIs still exist], especially in large B2B industries like transportation, but it lost in popularity in the wider economy because...  APIs have arrived.

=== b. The emergence of web APIs

In the late 1990s and early 2000s, Internet and the ((World Wide Web)) expanded dramatically.

More and more servers in different parts of the world needed to be interfaced with each other to exchange data.

It became increasingly convenient to define simple and universal conventions that everyone could learn and follow to standardize these exchanges, for free and easily.

That's what *web APIs* do. They are also often called:

- *API* for short
- *web services* (((API, web service)))
- *REST* API (see below for this last one).

A *web API* (((API, web service))) extends the logic of the APIs we have seen in the beginning of this document, to software communicating via the web.

To recall, an API is a convention followed when writing a software, making this software available to other software.

NOTE:: Example: the API of Microsoft PowerPoint enables the import of Excel tables in pptx documents, because the API of Powerpoint plugs to the API of Excel. In this example Excel and Powerpoint are suposed to be installed on the same computer of course!

A Web API is an API which enables two pieces of software to communicate, via Internet. *They don't need to be installed on the same computer.*

=== c. The benefits of a web API compared to an EDI

Unlike an *EDI* (((API, difference with EDIs))), a web API drops any industry-specific concern. Web APIs are just a convention to send and receive data over the Internet, without any saying on the content of the data.

The data sent and received can be invoices, webpages, train schedules, audio, video... whatever.

Contrary to an EDI, a company creating a web API can choose to leave its access open (remember that EDIs need the two parties to have a pre-established agreement).

So that a potential client interested in using the web API of a company can set it up in a couple of clicks, instead of waiting weeks or months before a contract is signed and the EDI is setup.

[WARNING]
====
Saying that APIs are open does not mean an absence of security (((API, security of))): communication through APIs can easily be identified and encrypted, as needed.
====

=== d. REST API?

Two popular web API conventions emerged in the 1990s and competed for popularity:

- SOAP (https://en.wikipedia.org/wiki/SOAP[Simple Object Access Protocol])
- REST (https://en.wikipedia.org/wiki/Representational_state_transfer[Representational State Transfer])

*REST APIs* (((API, REST protocol))) became ultimately the most widely adopted, because it uses the same simple principles that webpages use to be transferred over the Internet (the "http" protocol that you see in web page addresses).
This is why APIs are often called https://www.youtube.com/watch?v=7YcW25PHnAA["REST APIs, presented in this pedagogical video"].

In 2000-2010, it became increasingly easy and natural to adopt the REST convention to make one's software and data available to another computer.
This simple evolution to ease interoperability had *immense effects*:

== Business consequences of APIs

=== a. APIs *opened* software to the world

An API transforms a closed software into something that can be plugged to anything other computer or object, as long as it is connected to the Internet.

For instance, APIs were a key factor of success for https://en.wikipedia.org/wiki/Salesforce.com[SalesForce] in the early 2000s. SalesForce, created in 1999, has a revenue of US$8.39 billion in 2017:

- ((SalesForce)) developed a CRM as a SaaS where features of the CRM were *exposed as APIs* (meaning, these features could be plugged to external apps via the REST protocol).

- SalesForce created a ((PaaS)) to host apps that could plug to the SalesForce CRM via the APIs developed by SalesForce.

This platform is called https://www.salesforce.com/products/platform/products/force/[Force.com] and external developers can put their apps there, as long as they are compatible with the SalesForce API.

SalesForce takes a commission on the sales made by these third party apps hosted on Force.com, but more importantly, the platform creates an *ecosystem* of apps and developers around the SalesForce products which makes it hard for a customer company to switch to a different product.

=== b. APIs *accelerated* software innovation

Thanks to API it is now easier to add software blocks together and create new apps, even if these software blocks originate from different countries, industries, big and small.

As an extreme example: the Australian Victoria Police deployed a project for the recognition of stolen vehicles through the video recognition of licence plates on cars passing in the street (stolen vehicles get their license plates immediately recognized). This is a $86,000,000 project. An individual actually replicated this https://medium.freecodecamp.org/how-i-replicated-an-86-million-project-in-57-lines-of-code-277031330ee9[project with just 57 lines of code and a dashcam]. How so? Just because he could use existing software for licence plate recognition, available as an API, instead of re-developing this by himself. [Check this amazing story].

=== c. APIs *opened* data

Companies and public organization own many datasets of great business interest.
The use of these datasets can be free (for small projects and NGOs) or monetized if the user is an enterprise.

Without APIs, datasets can be made publicly available as docs (eg, Excel spreadsheets) to download but this is not practical (try downloading something like `all_train_schedules_2000_to_2017.xls` !).

So, imagine a transportation company like French SNCF which finds it interesting to publish station names, train schedules, etc. because it could be used by other companies to build new services : how can it do it?

The data is on a server of SNCF. Then SNCF adds https://data.sncf.com/api/en[an API and its documentation], making the data available to developers able to https://youtu.be/7YcW25PHnAA[connect to APIs, which is a basic skill in software development].

Entrepreneurs and programmers in general will be able to access the data via the API and use it, possibly to create new services based on this train information.
*Open data* (((open data))) designates this movement to make datasets available to a broad audience, and web APIs have been a key technological ingredient in this movement.

== The ecosystem of APIs


=== a. A wealth of APIs

To discover new APIs, or to make your APIs easier to discover, the most well known place is https://www.programmableweb.com/[the website "Programmable Web"] (see also http://apis.io/[apis.io]):

Searching on this website, you will find  https://www.programmableweb.com/api/coca-cola-enterprises[APIs providing business services], or   https://www.programmableweb.com/api/itsthisforthat[APIs of a fun and odd sort].

Still, many APIs are not listed on this website, and a google search for "info I need + API" is also a good way to find if the API you'd need exists. http://hotline.whalemuseum.org/api[Interested in whale sightings? There is an API for that].

=== b. APIs: a business world of its own

*APIs* (((API))) have become central to the economy.
As a result, a large number of services associated to APIs have developed to cater for all the needs of companies that use them:

- how to create an API
- how to manage the documentation of a large number of APIs
- how to connect a wide variety of APIs
- how to control and audit the security of APIs
- how to monetize and API...

-> Many large firms and startups now specialize in all these different issues.
Here is the https://twitter.com/medjawii?lang=en[landscape of the main companies active in the API industry]:

<<<<

image::api-landscape-2017_panorama.jpg[pdfwidth="90%", align="center", title="The API landscape in 2017 by Mehdi Medjaoui", book="keep"]
{nbsp} +

= Chapter 6. Essential notions on privacy and data protection
'''

== Privacy: just one aspect of data protection


image::Defining-data-protection.png[align="center", title="Defining data protection", book="keep"]
{nbsp} +

== When is personal information considered "data"?


At the most basic level, anything could count as "data" with possibly a personal character to it, including comments written about somebody in a personal notebook.

In practice, "data" starts to to be considered as such when:

This is information capable of being processed *automatically*

-> Hint: data on computers, not unstructured written notes

*Or* information intended to be processed automatically

-> Hint: paper records to be fed in a computer (eg, via scanning), not any pile of paper on your desk.

Or *structured information* that can be used to facilitate the retrieval of specific information on specific individuals

-> Hint: paper records, filing systems, databases

== Personal data matters because of privacy


https://www.cnil.fr/en/personal-data-definition[Definition of personal data]:

[quote, CNIL (French Independent Administrative Authority)]
____
Personal data are any anonymous data that can be double checked to identify a specific individual (e.g. fingerprints, DNA, or information such as “the son of the doctor living at 11 Belleville St. in Montpellier does not perform well at school”).
____

Personal data is data that an individual has the right to keep private. *How and why is privacy an issue*?

Privacy is mentioned in the Article 12 of the http://www.un.org/en/universal-declaration-human-rights/index.html[1948 Universal Declaration of Human Rights]:

[quote,Universal Declaration of Human Rights]
____
No one shall be subjected to arbitrary interference with his privacy, family, home or correspondence, nor to attacks upon his honor and reputation. Everyone has the right to the protection of the law against such interference or attacks.
____

This article from the Declaration is found in similar forms in most of the conventions on human rights in the world.

This *right to privacy* (((privacy, right to privacy))) enables individuals to define their identity in relation to the world, by giving each individual the power to control what to keep for themselves, and what to reveal / share with the world.

In 2005, a report on https://books.google.fr/books?id=yeVRrrJw-zAC&pg=PA1&dq=right+to+privacy+tel+aviv&hl=en&ei=T0IhTaWhEI-msQOizMWZCg&sa=X&oi=book_result&ct=result&redir_esc=y#v=onepage&q=right%20to%20privacy%20tel%20aviv&f=false[Privacy in the Digital Environment] by the Haifa Center of Law & Technology develops:

____
The right to privacy is our right to keep a domain around us, which includes all those things that are part of us, such as our body, home, property, thoughts, feelings, secrets and identity.
____

____
The right to privacy gives us the ability to choose which parts in this domain can be accessed by others, and to control the extent, manner and timing of the use of those parts we choose to disclose.
____

In addition to shaping an individual's own personal sphere and identity, privacy also underpins the development of a relation between the individual and the society she is part of:

-> when an individual's privacy is secured, they don't have to fear that their personal opinions and activities (as simple as reading a newspaper) will endanger them as citizens.

-> this gives liberty to individuals to develop political expressions which do not necessarily conform with the power structure in place. This would be much harder if everyone's political opinions could not be kept private.

== Evolution of privacy


Privacy is a social norm which transforms as societies evolve. Since the 2000s, a couple of tendencies can be identified:

- increasing tracking of the digital traces left by individuals by companies which use these traces for ad targeting and data reselling.

- increasing ((state surveillance)) through digital means, against security threats and unspecified goals.

- broader public acceptance of new forms of violations to privacy.

For example, https://en.wikipedia.org/wiki/Reality_television[TV shows where participants are filmed 24/24] and where they reveal their (real or supposed) intimacy, dates back only from the late 1990s.

[link=http://www.imdb.com/title/tt0120382/]
image::truman.jpg[align="center", title="The Truman Show, 1998", book="keep"]
{nbsp} +

== Privacy of the consumer and privacy of citizens: the relations between the two


Thanks to whistleblowers like https://en.wikipedia.org/wiki/Edward_Snowden[Edward Snowden], ((("Snowden, Edward"))) a former contractor for the National Security Agency - NSA, the extent of privacy breaches by governmental agencies is now better known.

This trailer for "CitizenFour" gives a sense of the dangers whistleblowers face when revealing how governmental agencies spy on their citizens:

video::108771171[vimeo]

Journalists, academics, activists and NGOs such as the https://www.eff.org/[Electronic Frontier Foundation] make the case that:

- consumers are insufficiently aware and sensitive of how much information is captured in the normal conduct of their lives, just by using mobile phones and apps, web browsing, and increasingly in public places.

- citizens are insufficiently aware and sensitive of the breach of their privacy by security agencies of their own country of residence, and by other countries.

Many citizens consider that if they don't break the law, then they have "nothing to hide".

Similarly, consumers might find that bargaining their private data against a free service and some targeted ads, is a good deal.


Sociologist of technology http://technosociology.org/[Zeynep Tufekci] goes further:

Her argument is that besides "surveillance" and "lack of privacy", companies like Google and Facebook developing a business model based on ad targeting by analytics on personal data, design a *persuasion architecture* which can be used / highjacked for political purposes.

*Tufekci* ((("Tufekci, Zeynep"))) does not argue that Google, Facebook or the likes inherently have anti-democratic purposes, but that:

- they develop of an information architecture which has the potential to shape opinions of crowds,
- they do so without transparency

- some past experiments on voting in the US, and current developments on electronic ((surveillance)) in ((China)), show that the power of these technologies has already consequences in the real world:

video::iFTWM7HV2UI[youtube]

== Conclusion: data protection in business, more than an regulatory obligation


The collection and treatment of personal data by businesses has far reaching implication, and should not be considered merely from a legal standpoint by firms.

The topic engages the https://en.wikipedia.org/wiki/Corporate_social_responsibility[Corporate social responsibility] of the firm.

The nature of the *business model* (((business model, based on consumer profiling))) itself - profiling consumers in the most specific way - has profound consequences on the design of the environment surrounding individuals.

What are the next steps? Several trends can be identified:

1. Some voices question the business model: are ((personalized ads)) based on personal data as effective as the market valuation of Facebook suggests? How much is just scam? Some voices warn against https://digiday.com/media/ft-warns-advertisers-discovering-high-levels-of-domain-spoofing/[the extent of the fraud in digital ads], as the video below shows:

video::oVfHeWTKjag[youtube]

[start=2]
2. Legislation by political authorities to protect the public interest, especially via an obligation for transparency, in the face of more personal data being collected, for a larger variety of purposes.

[start=3]
3. A deepening of the current model with more personal data being collected, in private spaces (homes) and behavior in public places (crowd management in streets, stadiums, etc.):

image::amazon-echo.jpg[align="center", title="Echo Alexa", book="keep"]
{nbsp} +

*Echo Alexa* (((Amazon, Echo Alexa))) is a home assistant with a conversational interface, providing services personalized with the data provided by the user.

= Chapter 7. GDPR and data protection globally
'''

== Evolution of data protection regulations in the EU


=== a. The Directive on Data Protection by the EU in 1995

This Directive derives from earlier guidelines adopted by the OECD as far back as 1980 on http://www.oecd.org/internet/ieconomy/oecdguidelinesontheprotectionofprivacyandtransborderflowsofpersonaldata.htm[the Protection of Privacy and Transborder Flows of Personal Data].

These guidelines were adopted by OECD members but were non binding: for instance, https://en.wikipedia.org/wiki/Data_Protection_Directive#Context[the US did not translate the OECD guidelines on the protection of privacy into their legislation]. In contrast, these guidelines were turned into a Directive in the EU, in 1995.

- http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=CELEX:31995L0046:en:HTML[full text of the EU Directive on Data Protection]
- https://en.wikipedia.org/wiki/Data_Protection_Directive[Wikipedia presentation of the EU Directive on Data Protection on]

This Directive guarantees and facilitates the free movement of personal data across EU States, by providing a framework valid for all member States for the protection of personal data of EU citizens.

How is handled the issue of EU data owned by non EU companies? For example, what is the level of protection for the personal data of a French individual, owned by a US company on a server located in the US?

-> According to the 1995 Directive, th rule was simple: *it is forbidden to export personal data to a non EU-country with a lower level of personal data protection.*


=== b. The case of EU citizen data hosted by US-based companies

The case is important as major providers of services involving personal data (google search, gmail, gmaps, facebook, etc.) is hosted in the US.

The question is: what it the level of data protection in this case? US-level of protection or EU?

It should not be possible to host EU citizen personal data in the US because the US have much less stringent regulations in these matters. Indeed, in the US:

- There is a regulatory framework on data protection for data collected or held by the Federal government

- But there is no general framework on data protection outside the Federal government (states level).

To remedy this situation, the ((Safe Harbor)) principles is an international agreement between the USA and EU which was put in place in 2000.

The https://en.wikipedia.org/wiki/International_Safe_Harbor_Privacy_Principles[Safe Harbor principles] are a series of regulations which US companies can agree to follow if they want to host EU personal data outside the EU. These rules provide a level of data protection equivalent to the one guaranteed by the 1995 Data Protection Directive in the EU.

In October 2015, https://en.wikipedia.org/wiki/Max_Schrems[Maximillian Schrems] (a student in law in Austria) ((("Schrems, Max"))) launched a lawsuit against Facebook for failure to protect his personal data against the spying of the NSA in the USA.

The defense of Facebook was to argue that it complied with the Safe Harbor Act. The lawsuit went to the European Court of Justice which ended up *declaring the Safe Harbor Act invalid* because:

"legislation permitting the public authorities to have access on a generalized basis to the content of electronic communications must be regarded as compromising the essence of the fundamental right to respect for private life"."

The following months were a state of legal uncertainty as the EU data hosted on US servers were so under no legal conditions.

On 2nd February 2016, the EU and the US created a new legal agreement known as the https://en.wikipedia.org/wiki/EU-US_Privacy_Shield[EU-US Privacy Shield]. The https://www.scmagazineuk.com/how-will-the-new-eu-us-privacy-shield-fit-with-the-upcoming-general-data-protection-regulation/article/531527/[the ((Privacy Shield)) differs from the Safe Harbor Act] in the following:

1. Stronger obligations on companies in the US to protect the personal data of Europeans' and stronger monitoring and enforcement by the US Department of Commerce and Federal Trade Commission.

[start=2]
2. Access to personal data transferred under the new arrangement by public authorities on the US was scheduled to be subject to clear conditions, limitations and oversight, preventing generalized access by state surveillance organizations.

[start=3]
3. Effective protection of EU citizens' rights with several redress possibilities.

[start=4]
4. An annual joint review mechanism between the EU and the US.

=== c. GDPR, a new legal framework

The handling of EU citizen data outside of the EU is of a great legal complexity, as evidenced by the fragility of the EU-US legal agreements. Should the EU create special legal agreements with each and every country wishing for their companies to be able to host EU personal data? This seems like a bureaucratic nightmare (or a lawyer's dream).

Instead, the EU has designed *a new legal principle* applying to all countries holding EU personal data, without the need for bilateral agreements. *This is the GDPR*.

The *GDPR: General Data Protection Regulation* is a legal framework coming into place in 2018, replacing the 1995 Directive by a new, simple rule: EU citizen data must be handled according to the rules stated by the EU, *wherever these data are stored or processed*.

Before examining the GDPR in more details, we define the legal terms used in it:


== Key definitions


Source for these key definitions : a synthetic https://github.com/seinecle/mk99/blob/master/src/main/asciidoc/resources/DATAIKU-WP-DATA-GDPR.pdf[whitepaper on the GDPR by Dataiku]. (((Dataiku)))

=== a. Personal data

Personal data (((data, personal data))) is any information related to a human being (or data subject) that can be used to directly or indirectly identify that person.

For example: name, photos, email addresses, bank details, posts on social networking websites, medical information, IP addresses, etc.

=== b. Sensitive data

Sensitive data (((data, sensitive data))) is a special category of personal data (including personal data revealing racial or ethnic origin, political opinions, religious or philosophical beliefs, trade-union membership, and data concerning health or sex life) to which additional protections apply.

=== c. Data subject

A ((data subject)) is a human being on whom personal data is being collected.

=== d. Data controller (DC)

A ((data controller)) is an entity that determines the purposes, conditions, and means of the processing of personal data. When the organization is large enough, a dedicated position of "Data Controller" can be created.

Ex: in France, the DC is in charge of declaring the personal data being processed to the https://www.cnil.fr/en/home[CNIL].

=== e. Data processor (DP)

A ((data processor)) An entity that processes personal data on behalf of the controller (e.g., cloud and data center providers).

Until 2017, it was considered that the data processor is just "executing" the mission given by the DC:

- the DP is in charge of proper security measures to ensure data protection against breach, loss...
- but the DP is not liable for the improper collection procedures of personal data set up by the data controller.

Starting in 2018 with the ((GDPR)) (see next), the DP is co-responsible with the DC in case of a data breach compromising the personal data of subjects.


== Four key principles for the rightful processing of personal data


=== a. Prior consent

Prior consent (((prior consent))) is required before collecting personal data in view of processing it:

- Data collection policy should be made clearly available to users
- Opt out should be possible
- Consent should be presented clearly

=== b. Adequacy / legitimate purpose

The data collected should be exactly necessary to run the service, not more.

Time out: information should be deleted when service stops. In France, there is a 13 month limit after which consent must be renewed.

=== c. Portability

-> Information should be available on request (((data, portability of)))

In 2011 Max Schrems requested all his Facebook data. He received 1,200 pages of it.

Thanks to his efforts, now most of social media offer a one-click download of your personal data.

Portability also covers the "right to be forgotten", detailed http://ec.europa.eu/justice/data-protection/files/factsheets/factsheet_data_protection_en.pdf[in this factsheet by the EU].


=== d. Safety

All reasonable precautions should be taken against data breaches.

Precautions taken should be scaled to the damage which would result from a breach in security.

Basics: define and manage access rights to each relevant aspects of the data.

Users should be told about security breaches potentially affecting their data

== In 2018: the GDPR and what it changes


GDPR stands for "General Data Protection Regulation". It was adopted by the EU on April 14, 2016 and is enforced on *May 25, 2018*.

Its key novelties, compared to the EU Data Protection Directive, are:

=== a. Application

The GDPR applies to any company (regardless of their location, size, and sector) processing the personal data of people residing in the EU.

For example, a US-based company processing the personal data within the United States of EU citizens is required to comply.

=== b. Responsibility

Under the GDPR, both the ((data controller)) and the ((data processor)) must comply with the legislation. Under the previous/current Data Protection Directive, only data controllers were held liable for data protection compliance, not data processors.

=== c. Penalties

With a maximum fine of up to 4 percent of annual global turnover or €20 million (whichever is greater), penalties for non-compliance are steep.

=== d. Consent

Under the ((GDPR)), companies will no longer be able to use long, illegible terms and conditions full of legalese; consent for collection and use of personal data must be in plain language and detail the purpose of data processing.

=== e. Data breaches

Increased regulation surrounding the disclosure of *data breaches* (((data, data breaches))); specifically, much quicker reporting is required (within 72 hours).

=== f. Data Subjects’ Rights

EU data subjects have expanded rights when it comes to data protection, including:

- the *right to be forgotten* (((right to be forgotten))) (have their data erased),
- the right to access (obtain information about exactly what data is being processed where and for what purpose),
- and the right to data portability (receive a copy of the personal data concerning them).

Citizens now also have the right to question and fight decisions that affect them that have been made on a purely algorithmic basis.

=== g. Privacy by design

*Privacy by design* (((privacy, privacy by design))) is a legal requirement to consider data privacy on the onset of all projects and initiatives, not as an afterthought.


=== h. Data Protection Officer (DPO) Appointment

Controllers and processors whose core business is regular and systematic monitoring of data
subjects on a large scale or who deal with special categories of data will be required to appoint a DPO. The DPO may be appointed from within, hired, or contracted, but (among other specific requirements) (s)he must be an expert on data protection law and practices.

== Data protection: a quick view outside the EU


=== a. U.S.A.

-> Framework on data protection for data collected / held by the Federal government

-> But no general framework on data protection outside the Fed. gov

=== b. India

IT Act of 2000 + http://www.wipo.int/wipolex/en/details.jsp?id=15063[IT Rules 2011]

-> Focus on *sensitive* personal information:

Passwords, financial information, health condition, sexual orientation, biometric information

-> No need to declare data processing activities to an authority

=== c. China

(((China)))

In China, data protection is not enacted in a single piece of legislation, except for laws of a broader scope: National People’s Congress Standing Committee http://tinyurl.com/npcdecision[Decision concerning Strengthening Network Information Protection].

Rather, China has sector based pieces of legislation, such as the Regulation on Personal Information Protection of Telecom and Internet Users (http://tinyurl.com/miitdecision[MIIT Regulation]).

==== d. Legislation for the protection of personal data in other countries

To have a https://uk.practicallaw.thomsonreuters.com/Browse/Home/International/DataProtectionGlobalGuide?__lrTS=20171113205355950&transitionType=Default&contextData=(sc.Default)&firstPage=true&bhcp=1[synthetic view of data protection laws in other countries, visit this website by Thomson Reuters].

= Chapter 8. The method
'''

== Step 1: Restating the strategic objectives of the organisation

=== 1. What you accomplish at this step

Designing a business project can lead to results of great interest, except that it does not fit with the goals of the organisation.

*In step 1, we help you state what are the goals of your organisation*, so that it becomes clear what type of project will contribute to these goals. We call these goals “strategic objectives”.

The strategic objectives of an organisation are the key guiding principles defined by its executives. They define the priorities an organisation must concentrate on to accomplish its vision.

How to identify the strategic objectives of your organisation?

-> They are typically openly stated by the CEO or top management of your organisation.

=== 2. How to use the canvas

Use this canvas to explain in your terms

=== 3. Example: Gym Sports

. Illustration: the case “Sports Gym”
[cols="asciidoc"]
|=======
| “Sports Gym” is a 30-year company owned by an investor with an objective of increasing the profitability of this asset, on a constant business perimeter. Sport Gym manages 123 fitness centers across the country. Each fitness center is a place where gym goers can exercise with machines, group activities and other equipments. There are three types of customers: members with a year-long subscription (350€ / year), members on a monthly plan (41€ / month), and visitors for the day (15€ / day). Its yearly revenue is 57 millions €.

Sports Gym’s revenues make it a sustainable business in the short to middle term, but several factors threaten its profitability:
Low level of customer loyalty. Customers visit their Sports Gym club because it is close but they would easily switch to a fitness center with lower prices and a convenient location.
Lack of brand attachment. Surveys have shown that customers and prospects do not perceive Sports Gym as a unique, specific brand. They tend to associate it with any other fitness club, including competitors with lower prices.
Lack of scalability within each fitness center due to 1) cost structure: personalized coaching by certified experts is limited by HR costs, 2) difficulty with capacity management: fitness machines and group activities are alternatively overcrowded or not used at all.


|=======

<<<<

== Step 2: Identifying the target user
#2 - What it is used for
#2 - How to use the canvas
#2 - Example: Gym Sports.


<<<<

== Step 3: Profiling the avatar of the target user
#3 - What it is used for
#3 - How to use the canvas
#3 - Example: Gym Sports.
<<<<

== Step 4: Mapping the needs of the target user
#4 - What it is used for
#4 - How to use the canvas
#4 - Example: Gym Sports.
<<<<

== Step 5: Listing the data sources available
#5 - What it is used for
#5 - How to use the canvas
#5 - Example: Gym Sports.
<<<<

== Step 6: Selecting up to 3 data sources
This index term should also appear in the index.
#6 - What it is used for

Now that you have listed the data sources at your disposition, the next step consists in identifying those that will provide the highest value at the lowest cost. This canvas helps you rank your data sources along key dimensions like machine readability, data completion, etc.
#6 - How to use the canvas

Select the 3 data sets which you think will provide most value for your project, and for each dataset, assign a mark between 1 and 5, 1 being the hardest and 5 the easiest for the following dimensions :
Machine readable: data that exists in a database or a comma-separated value (.csv) file is easier to read than if it is stored in a Word document or a .pdf.
Structured or not: Free text is harder to use than structured data stored in a database
Follows universal categories or is company-specific: data that follows standard categorization, like the ones provided by national and international statistics organizations (e.g. Eurostat) is easier to analyze than if the categorization is specific to your company
Time series: data that is collected regularly across time will provide better results in the long term than punctual data
Personal and sensitive data: The more personal and sensitive data is, the more constraints it generates (GDPR, etc.), and therefore the harder it is to use
Complete: the more complete the data, the easier it is to use

#6 - Example: Gym Sports.
<<<<

== Step 7: Brainstorming on data x the need of the target user
This Index term should also appear.

#7 - What it is used for
In this step, you will put the datasets you have selected to the test: do they really contribute to providing a service meeting the needs of your target user? Is the solution still aligned with your company’s strategic objectives ?
#7 - How to use the canvas
Follow this iterative process:
Pick one of the datasets
Define how the selected dataset contributes to a service meeting the needs of your target users
Challenge the results:
Is the solution still aligned with your company’s strategic objectives ?
Is the user really gaining value from the solution ?
If the dataset stands the challenge, you can keep it and move on to the next one. If it doesn’t, discard it and replace it.
#7 - Example: Gym Sports.
<<<<


== Step 8: Formalizing the value proposition
#8 - What it is used for
In this step, you will summarize the value proposition of the solution you have identified, based on the datasets you have selected. The objective is to list the key features of the solution, as well as describe how it helps solve the target user’s problems and how it creates value for the target user.
#8 - How to use the canvas
The canvas is split in three areas:
Products and services:
Pain relievers:
Gain creators:
#8 - Example: Gym Sports.
<<<<

== Step 9: Graphical synthesis
#9 - What it is used for
#9- How to use the canvas
#9 - Example: Gym Sports.
<<<<

== Step 10: Memo synthesis
#10 - What it is used for
#10 - How to use the canvas
#10 - Example: Gym Sports.

<<<<
= Chapter 9. Seven roads to data-driven value creation
'''

====
Not a closed list, not a recipe!
Rather, these are essential building blocks for a strategy of value creation based on data.
====

== Predict



=== Examples of companies

1. Predicting crime image:predpol.png[pdfwidth="100", width="100", book="keep"]

2. Predicting deals image:tilkee.png[pdfwidth="100", width="100", book="keep"]

3. Predictive maintenance image:cat.jpg[pdfwidth="100", width="100", book="keep"]

=== Obstacles and difficulties

1. The https://indatalabs.com/blog/data-science/cold-start-problem-in-recommender-systems[((cold start problem))]

2. Risk missing the ((long tail)), ((algorithmic discrimination)), ((stereotyping))

3. Neglect of novelty


== Suggest



=== Examples of companies

1. Amazon’s product recommendation system image:amazon.jpg[pdfwidth="100", width="100", book="keep"]

2. Google’s “Related searches…” image:google.jpg[pdfwidth="100", width="100", book="keep"]

3. Retailer’s personalized recommendations image:auchan.jpg[pdfwidth="100", width="100", book="keep"]

=== Obstacles and difficulties

1. The ((cold start problem)), managing https://doi.org/10.1016/j.knosys.2016.08.014[((serendipity))] and http://wwwconference.org/proceedings/www2014/proceedings/p677.pdf[((filter bubble effects))].

2. Finding the ((value proposition)) which goes beyond the simple “you purchased this, you’ll like that”


== Curate



=== Examples of companies

(((data, data curation)))

1. ((Clarivate Analytics)) curating metadata from scientific publishing image:crv_logo_rgb_rev.png[pdfwidth="100", width="100", book="keep"]

2. Nielsen and IRI curating and selling retail data image:nielsen.jpg[width="100"] image:iri.jpg[pdfwidth="100", width="100", book="keep"]

3. ImDB curating and selling movie data image:imdb.jpg[pdfwidth="100", width="100", book="keep"]

=== Obstacles and difficulties

1. Slow progress: curation needs ((human labor)) to insure high accuracy, it does not scale the way a computerized process would.

2. Must maintain continuity: missing a single year or month hurts the value of the overall dataset.

3. Scaling up / right incentives for the workforce: https://www.wired.com/story/amazons-turker-crowd-has-had-enough/[the workforce doing the digital labor of curation should be paid fairly], which is not the case yet.

4. Quality control


== Enrich



=== Examples of companies

1. Selling methods and tools to enrich datasets image:watson.png[pdfwidth="100", width="100", book="keep"]

2. Selling aggregated indicators image:edf.jpg[pdfwidth="100", width="100", book="keep"]

3. Selling credit scores

=== Obstacles and difficulties

1. Knowing which cocktail of data is valued by the market

2. Limit duplicability

3. Establish legitimacy

== Rank / match / compare



=== Examples of companies

1. Search engines ranking results image:google.jpg[pdfwidth="100", width="100", book="keep"]

2. Yelp, Tripadvisor, etc… which rank places image:tripadvisor.jpg[pdfwidth="100", width="100", book="keep"]

3. Any system that needs to filter out best quality entities among a crowd of candidates

=== Obstacles and difficulties

1. Finding emergent, implicit attributes (imagine: if you rank things based on just one public feature: not interesting nor valuable)

2. Insuring consistency of the ranking (many rankings are less straightforward than they appear)

3. Avoid gaming of the system by the users (for instance, http://www.nytimes.com/2011/02/13/business/13search.html[companies try to play Google's ranking of search results at their advantage])

== Segment / classify



=== Examples of companies

1. Tools for discovery / exploratory analysis by ((segmentation))

2. Diagnostic tools (spam or not? buy, hold or sell? healthy or not?) image:medimsight.png[pdfwidth="100", width="100", book="keep"]

=== Obstacles and difficulties

1. Evaluating the quality of the comparison

2. Dealing with boundary cases

3. Choosing between a pre-determined number of segments (like in the k-means) or letting the number of segments emerge

== Generate / synthesize (experimental!)



=== Examples of companies

1. Intelligent BI with https://www.aiden.ai/[Aiden] image:aiden.png[pdfwidth="100", width="100", book="keep"]

2. https://wit.ai/[wit.ai], the ((chatbot)) by FB image:wit.png[pdfwidth="100", width="100", book="keep"]

3. https://www.cxcompany.com/digitalcx/[Virtual assistants] image:cx.jpg[pdfwidth="100", width="100", book="keep"]

4. https://deepart.io/[Image generation] image:deepart.png[pdfwidth="100", width="100", book="keep"] (((image generation)))

5. Close-to-real-life https://deepmind.com/blog/wavenet-generative-model-raw-audio/[((speech synthesis))] image:google.jpg[pdfwidth="100", width="100", book="keep"]

6. Generating realistic car models from a few parameters by https://www.autodeskresearch.com/publications/exploring_generative_3d_shapes[Autodesk]: image:autodesk.png[pdfwidth="100", width="100", title="Autodesk", book="keep"]

A video on the generation of car models by Autodesk:

video::25xQs0Hs1z0[youtube]

=== Obstacles and difficulties

1. Should not create a failed product / false expectations

2. Both classic (think of image:clippy.jpg[pdfwidth="50", width="50", book="keep"]) and frontier science: not sure where it’s going


== Combos


image::data-driven-value-creation.png[pdfwidth="100%", align="center", title="Combinations", book="keep"]
{nbsp} +
