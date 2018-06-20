= Topics in Data Science for business: Volume 1 - Fundamentals
Clément Levallois <levallois@em-lyon.com>
v1.0, April 2018
:icons!:
:iconsfont:   font-awesome
:revnumber: 1.0
:example-caption!:
:sourcedir: ../../../main/java
= What is data?

== 1. Definition of data

The English term "data" (1654) originates from “datum”, a Latin word for "a given".footnote:[http://www.etymonline.com/index.php?term=data]
"Data" is a single factual, a single entity, a single point of matter.

Using the word "data" to mean "transmittable and storable computer information" was first done in 1946.
The expression "data processing" was first used in 1954.footnote:[http://www.etymonline.com/index.php?term=data]

===
Thoughts: the etymology suggests that data is "a given". Can you question this?
===

Data represents either a single entity, or a collection of such entitities ("data points").
We can speak also of datasets instead of data (so a dataset is a collection of data points).

== 2. Examples!


|===
|||

|A date
|A color
|A grade

|A relation of friendship
|A sound
|A hearbeat

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



== 3. Three take aways from the examples

=== a. Think about data in a broad sense

Data is not just text and figures. You should train in thinking about data in a broader sense:

- pictures are data
- language is data (including slang, lip movements, etc.)

- relations are data (you know individual A, you know individual B, but the relationship between A and B is data as well)
- preferences, emotional states... are data
- etc. There is no definitive list, you should train yourself looking at buisness situations and think: "where is the data?"


=== b. metadata is data, too

Metadata: this is some data describing some other data.

Example:
----
The bibliographical reference <1>
describing
a book <2>
----
<1> the metadata
<2> the data


-> Data without metadata can be worthless (imagine a library without a library catalogue)

-> Metadata can be informative in its own right, as shown with the NSA scandal: footnote:[http://www.newyorker.com/news/news-desk/whats-the-matter-with-metadata]

image:metadata.png["The trouble with metadata"]

=== c. zoom in, zoom out

We should remember considering that a data point can be itself a collection of data points:

- a person walking into a building is a data point.
- however this person is itself a collection of data points: location data + network relations + subscriber status to services + etc.

So it is a good habit to wonder whether a data point can in fact be "unbundled" (spread into smaller data points / measurements)

== 4. Some essential vocabulary to discuss data

=== a. Formats, types, encoding



image:tweet.png[width="500" align="center"]

- This is a digital *medium* (because it's on screen as opposed to analogic, if we had printed the pic on paper)
- The *type* of the data is textual + image

- The text is *formatted* in plain text (meaning, no special formatting), as opposed to more structured data-interchange formats (https://codingislove.com/json-tutorial-indepth/[check json or xml]).
- The *encoding* of the text is UTF-8. Encoding has to do with the issue: how to represent alphabets and signs from different languages in text? (not even mentioning emojis?). UTF-8 is an encoding which is one of the most universal.

- The tweet is part of a list of tweets. The list represents the *data structure* of my dataset, it is the way my data is organized. There are many alternative data structures: arrays, sets, dics, maps...
- The tweet is stored as a picture (png file) on my hard disk. "png" is the *file format*. The data is *persisted* as a file on disk (could have been stored in a database instead).


=== b. Data presented as a table

image::table.png[table]
{nbsp} +
{nbsp} +

=== c. Data according to who owns it

- First party data: the data generated through the activities of your own organization.
Your organization own it, which does not mean that consent from users is not required, when it comes to personal data.

- Second party data: the data accessed through partnerships.
Without being the generator nor the owner of this data, partners make it available to you through an agreement.

- Third party data: the data acquired via purchase
This data is acquired through a market transaction. Its uses still comes with conditions, especially for personal data.

=== d. Data: "sociodemo" or "behavior"?

- Sociodemogaphic or "sociodemio" data refers to information about individuals, describing fundamental attributes of their social identity: age, gender, place of residence, occupation, marital status and number of kids.

- Behavior data refers to any digital trace left by the individual in the course of it life: clicks on web pages, likes on Facebook, purchase transactions, comments posted on Tripadvisor...

Sociodemo data is typically well structured or easy to structure. It has a long history of collection and analysis, basically since census exists.

Behavior data allows to go further than sociodemo data: each individual can be characterized by its acts and tastes, well beyond what an age or marital status could define.

But behavior data is typically not well structured and harder to collect.


== 5. Finally: data and size

image:russian_dolls.jpg[Data sizes]



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


<<<

= What is big data?

== 1. Big data is a mess

image::ariely.png[align="center", title="Facebook post by Dan Ariely in 2013"]
{nbsp} +


Jokes aside, defining big data and what it covers needs a bit of precision. Let's bring some clarity.

== 2. The 3 V

Big data is usually described with the "3 Vs":

=== *V* for Volume

The size of datasets available today is staggering (ex: Facebook had 250 billion pics in 2016).

We should also note that the volumes of data are increasing at an *accelerating rate*. According to sources, https://www.sciencedaily.com/releases/2013/05/130522085217.htm["90% of all the data in the world has been generated over the last two years"] (statement from 2013) or said differently, https://appdevelopermagazine.com/4773/2016/12/23/more-data-will-be-created-in-2017-than-the-previous-5,000-years-of-humanity-/["More data will be created in 2017 than the previous 5,000 years of humanity"]

=== *V* for Variety

This is a bit less intuitive. "Variety" means here that data is increasingly unstructured and messy, and this is an important characteristic of the "big data" phenomenon. To carictature a bit, try to picture a shift from A to B:


*A - Structured data*:

phonebooks, accounting books, governmental statistics... anything that can be represented as well organized tables of numbers and short pieces of text with the expected format, size, and conventions of writing.

image::book.png[align="center", title="A book of accounts showing structured data"]
{nbsp} +

*B - Unstructured data*:

datasets made of "unruly" items: text of any length, without proper categorization, encoded in different formats, including possibly pictures, sound, geographical coordinates and what not...


image::unstructured-data.png[align="center", title="Structured vs unstructured data"]
{nbsp} +

=== *V* for Velocity

In a nutshell, the speed of creation and communication of data is accelerating (http://www.zdnet.com/article/volume-velocity-and-variety-understanding-the-three-vs-of-big-data/[examples taken from here]):


- Facebook hosts 250 billion pics? It receives 900 million more pictures *per day*
- Examining tweets can be done automatically (with computers). If you want to connect to Twitter to receive tweets in real time as they are tweeted, be prepared to receive in excess of 500 million tweets *per day*. Twitter calls this service the http://support.gnip.com/apis/firehose/["firehose"], which reflects the velocity of the stream of tweets.

image::firehose.jpg[align="center", title="The Twitter Firehose"]
{nbsp} +

- Sensor data is bound to increase speed as well. While pictures, tweets, individual records... are single item data sent at intervals, more and more sensors can send data *in a continuous stream* (measures of movement, sound, etc.)


So, velocity poses challenges of its own: while a system can handle (store, analyze) say 100Gb of data in a given time (day or month), it might not be able to do it in say, a single second. Big data refers to the problems and solutions raised by the velocity of data.

=== A 4th *V* can be added, for Veracity

Veracity relates to trustworthiness and compliance: is the data authentic? Has it been corrupted at any step of its processing?

We will devote a session of this course to data compliance, which is a broad topic covering data privacy, cybersecurity, and the societal impacts of data.

https://fr.pinterest.com/seinecle/data-compliance/[You can start reading the documents for this course here]

== 3. What is the minimum size to count as "big data"? It's all relative


There is no "threshold" or "minimum size" of a dataset where "data" would turn from "small data" to "big data".

It is more of a *relative* notion: it is big data if current IT systems struggle to cope with the datasets.

(see https://en.wikipedia.org/wiki/Big_data[Wikipedia definition] developing on this.)


"Big data" is a relative notion... how so?


=== a. relative to time

*  what was considered "big data" in the early 2000s would be considered "small data" today, because we have better storage and computing power today.
* this is a never ending race: as IT systems improve to deal with "current big data", data gets generated in still larger volumes, which calls for new progress / innovations to handle it.

[start=2]
=== b. relative to the industry

* what is considered "big data" by non tech SMEs (small and medium-sized entreprises) can be considered trivial to handle by tech companies.

[start=3]
=== c. not just about size

* the difficulty for an IT system to cope with a dataset can be related to the size (try analyzing 2 Tb of data on your laptop...), *but also* related to the content of the data.

* For example the analysis of customer reviews in dozens of languages is harder than the analysis of the same number of reviews in just one language.

* So the general rule is: the less the data is structured, the harder it is to use it, even if it's small in size (this relates to the "V" of variety seen above).

[start=4]
=== d. no correlation between size and value

* Big data is often called https://hbr.org/2012/11/data-humans-and-the-new-oil["the new oil"], as if it would flow like oil and would power engines "on demand".


* Actually, big data is *created*: it needs work, conception and design choices to even exist (what do I collect? how do I store it? what structure do I give to it?). The human intervention in creating data determines largely whether data will be of value later.


* Example: Imagine customers can write online reviews of your products. These reviews are data.
But if you store these reviews without an indication of who has authored the review (maybe because reviews can be posted without login oneself), then the reviews become much less valuable.
Simple design decisions about how the data is collected, stored and structured have a huge impact on the value of the data.

So, in reaction to large, unstructured and badly curated datasets with low value at the end, a notion of "smart data" is sometimes put forward: data which can be small in size but which is well curated and annotated, enhancing its value (see also https://www.quora.com/After-Big-Data-Smart-Data-is-a-trend-in-2013-So-what-is-Smart-Data-Have-any-clear-definition[here]).

[start=5]
=== e. as an expression, "big data" is evolving

* It is interesting to note that "hot" expressions, like "big data", tend to wear out fast. They are too hyped, used in all circumstances, become vague and over sold.
For big data, we observe that it is peaking in 2017, while new terms appear:



image::gtrends.png[align="center", title="Google searches for big data, machine learning and AI"]
{nbsp} +


What are the differences between these terms?

* "Big data" is by now a generic term

* "Machine learning" puts the focus on the scientific and software engineering capabilities enabling to do something useful with the data (predict, categorize, score...)


* "Artificial intelligence" puts the emphasis on human-like possibilities afforded by machine learning. Often used interchangeably with machine learning.

* And "data science"? This is a broad term encompassing machine learning, statistics, ... and any analytical methods to work with data and interpret it. Often used interchangeably with machine learning. "Data scientist" is a common job description in the field.

== 4. Where did big data come from?

[start=1]
=== a. Data got generated in bigger volumes because of the digitalization of the economy

image::Movie-theater-vs-Netflix.png[align="center", title="Movie theater vs Netflix"]
{nbsp} +

[start=2]
=== b. Computers became more powerful

image::Moore's-law.png[align="center", title="Moore's law"]
{nbsp} +


[start=3]
=== c. Storing data became cheaper every year

image::Decreasing-costs-of-data-storage.png[align="center", title="Decreasing costs of data storage"]
{nbsp} +

[start=4]
=== d. The mindset changed as to what "counts" as data

* Unstructured (see above for definition of "unstructured") textual data was usually not stored: it takes a lot space, and software to query it was not sufficiently developped.

* Network data (also known as graphs) (who is friend with whom, who likes the same things as whom, etc.) was usually neglected as "not true observation", and hard to query. Social networks like Facebook made a lot to make businesses aware of the value of graphs (especially https://en.wikipedia.org/wiki/Social_graph[social graphs]).

* Geographical data has democratized: specific (and expensive) databases existed for a long time to store and query "place data" (regions, distances, proximity info...) but easy-to-use solutions have multiplied recently.


[start=5]
=== e. With open source software, the rate of innovation accelerated

In the late 1990s, a rapid shift in the habits of software developers kicked in: they tended to use more and more open source software, and to release their software as open source.
Until then, most of the software was "closed source": you buy a software *without the possibility* to reuse / modify / augment its source code. Just use it as is.


Open source software made it easy to get access to software built by others and use it to develop new things. Today, all the most popular software in machine learning are free and open source.

See the Wikipedia article for a developed history of open source software: https://en.wikipedia.org/wiki/History_of_free_and_open-source_software

[start=6]
=== f. Hype kicked in

The http://www.gartner.com/technology/research/methodologies/hype-cycle.jsp[((Gartner hype cycle))] is a tool measuring the maturity of a technology, differentiating expectations from actual returns:


image::Gartner-Hype-Cycle-for-2014.png[align="center", title="Gartner Hype Cycle for 2014"]
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


image::Gartner-Hype-Cycle-for-2017.png[align="center", title="Gartner Hype Cycle for 2017"]
{nbsp} +


[start=7]
=== g. Big data transforms industries, and has become an industry in itself

Firms active in "Big data" divide in many subdomains: the industry to manage the IT infrastructure for big data, the consulting firms, software providers, industry-specific applications, etc...

-> the field is huge.

Matt Turck, https://twitter.com/mattturck[VC at FirstMarkCap], creates every year a sheet to visualize the main firms active in these subdomains.
This is the 2017 version:

image::Matt-Turck-FirstMark-2017-Big-Data-Landscape.png[align="center", title="Big data landscape for 2017"]
{nbsp} +


You can find a high res version of this pic, an Excel sheet version, and a very interesting comment https://mattturck.com/bigdata2017/[all here].

== 5. What is the future of big data?

[start=1]
=== 1. More data is coming

The Internet of things (IoT) designates the extension of Internet to objects, not just web pages and emails (https://seinecle.github.io/IoT4Entrepreneurs/[see here for details]).


These connected objects are used to *do* things (display stuff on screen, pilote robots, etc.) but also very much to *collect data* in their environments (through sensors).

The development of connected objects will lead to a tremendous increase in the volume of data collected.

We have a session devoted to IoT later in this course. You can already starting reading the documents for this session:

- https://fr.pinterest.com/seinecle/internet-of-things/[Internet of things]

[start=2]
=== 2. Discussions about big data will fuse with AI
Enthusiasm, disappointment, bad buzz, worries, debates, promises... the discourse about AI will grow. AI is fed on data, so the future of big data will intersect with what AI becomes.

We have a session devoted to data science / machine learning / AI later in this course. You can already start reading the documents for this course:

- https://fr.pinterest.com/seinecle/what-is-data-science/[What is data science?]
- https://fr.pinterest.com/seinecle/ai-applications-in-business/[AI applications in business]

[start=3]
=== 3. Regulatory frameworks will grow in complexity

Societal impacts of big data and AI are not trivial, ranging from racial, financial and medical discrimination to giant data leaks, or economic (un)stability in the age of robots and AI in the workplace.

Public regulations at the national and international levels are trying to catch up with these challenges. As technology evolves quickly, we can anticipate that societal impacts of big data will take center stage.

We have a session devoted to data compliance in this course. You can already start reading the documents for this course:

- https://fr.pinterest.com/seinecle/data-compliance/[Data compliance]



<<<

= What is "the cloud"?

== 1. Note on the terminology: what is a server?

For this topic, you need to know what a "server" is. A server is simply a computer stripped of everything unessential (screen, mouse, graphic card, sound card, keyboard)...


To illustrate: when Google is calculating what the best results are for your search "what are cheap and delicious restaurants in Lyon", this calculation must be done on a computer, right?

The kind of computer used to do this calculation is *not* this one:


image::desktop.jpg[align="center",title="A desktop computer"]
{nbsp} +

The reason is, we don't need a screen, mouse, desktop, and not even the big box containing the computer itself.
They take too much space, consume energy, and there is no need for them.

So when all the unecessary parts are removed, the computer looks like this, and is called a "server":


image::server.jpg[align="center",title="A server"]
{nbsp} +

source: https://www.oracle.com/servers/sparc/s7-2/index.html

Take a look at the shape: rectangular and very slim.
This makes it easy to stack up servers one on the other.
Because for Google and other companies crunching data for their business, a lot of servers are needed, so gaining on space is a real issue.

When many servers are piled up together and put in a big tall box, this is called a *rack* of servers, and look like this:

image::rack.jpg[align="center",title="A rack of servers"]
{nbsp} +

When all the racks of servers are put in the same room, this is called a "data center" and looks like this:

image::datacenter.jpg[align="center",title="A data center"]
{nbsp} +

Look at this video showing a tour of a data center at Google:

video::XZmGGAbHqa0[youtube]

Usually, until 2005 roughly, companies had two options:

- buying their own servers and using them on their premises (at their location).
- paying the services of companies specializing in managing data centers.

Then the "cloud" changed this.

== 2. The cloud

The term "cloud" was made popular by Amazon with their service “Amazon Elastic Compute Cloud” (Amazon EC2) launched in 2006.

This service was new in many ways:

- you can rent servers owned by Amazon, at a distance, when you need them, for a duration that you choose.

- there is an emphasis on ease of use: no need to know the technical details of these servers (how they are plugged, how they are configured…)

- you are just given a login + password and you can start using these servers for your needs.

- it's "elastic": if you need more servers, or more powerful servers, it's just possible. No need for signing a new contract or to evaluate whether Amazon has the capacity... it's dimensioned to be possible.

Let's compare a situation with or without the cloud:


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
Opex are not inherently a better or cheaper option than a capex, but they are easier for a project team or business unit to fit in their budget.
See http://gevaperry.typepad.com/main/2009/01/accounting-for-clouds-stop-saying-capex-vs-opex.html[this blog post], especially the critical comments below the post, to continue this discussion.

== 3. IaaS, PaaS, Saas ... ??



What a company can do with the cloud?

They can use it to run elementary operations, up to more complex ones:


*Infrastructure as a service* (IaaS)

You use servers in the cloud for basic capabilities like storing data, or computing operations.


*Platform as a Service* (Paas)

The cloud is used to provide building blocks of a service: to manage a messenging system, to host apps, ...


*Software as a Service* (Saas)

The cloud is used to host a full software accessible "on demand" through the browser: like Google Drive, https://www.d2l.com/products/learning-environment/[Brightspace] or https://www.salesforce.com/fr/?ir=1[SalesForce].

== 4. Private or public cloud? Hybrid cloud?

- Amazon EC2 is an example of a *public cloud*: it is publicly accessible to any customer. Of course, this does not mean that every customer can see what the others are doing on the cloud! Each customer have their private spaces on the cloud.


- Many companies have security requirements which prevent them from accessing public clouds.
They need to have their servers on premises.
In this case, they can build their own *private cloud*: it is a cloud just like Amazon EC2, except that it is owned, managed and used by the company exclusively - it is not accessible to third parties.
But even private, it keeps the basic characteristics of a cloud: on-demand and elastic in particular.

- *Hybrid clouds* are a variety of private clouds: it is a private cloud where some forms of operations can be delegated to a public cloud.
For example, operations which are not security sensitive and which need a capacity of computing in excess of what the private cloud of the company can provide.



<<<

= The headache of data integration

== Reading list
Find the reading list for this session on Pinterest:
https://fr.pinterest.com/seinecle/what-is-the-cloud/

== 1. Data: you don't get in on tap


A naive vision of data would get that it's all fluid. Don't we talk about "data streams"?
Working with data would be as simple as opening a tap and "getting customer data", for instance.


image::tap.jpg[align="center", title="Data streams, as fluid as water on tap?"]
{nbsp} +


Actually, data is more like a complex patchwork: many different pieces which must be stiched together - and this is hard.


image::patchwork.jpg[align="center", title="Data streams make a patchwork"]
{nbsp} +


Take customer data.

It is not a given. Instead, this is a design made of multiple primary data sources:


image::Multiple-sources-of-customer-data.png[align="center", title="Multiple sources of customer data"]
{nbsp} +

> Analysts often spend 50-80% of their time preparing and transforming data sets before they begin more formal analysis work.

Garrett Grolemund, http://shop.oreilly.com/product/0636920035992.do[Data Scientist and Master Instructor at RStudio]



Take away: Data is fragmented by nature. It comes from different sources and presented in different formats.
*You* (the marketer in collaboration with data scientists) wrangle to __construct__ customer profiles by joining and assembling different sources of data into a meaningful synthesis.


(if you are interested, data scientists actually have whole books on the subject of wrangling with the mess of different data sources)

image::wrangling.jpg[align="center", title="Data wrangling"]
{nbsp} +


== 2. Sources of fragmentation


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

http://www.nyt.com/etc

-> It is important to count visits to these two urls as a visit *to the same page*.


In Sept 2017 major services of web data analytics were http://searchengineland.com/google-amp-cache-unified-users-analytics-282069[still struggling with this issue].

This illustrates that to just count visits to a web page (something which should be classic and robust) and integrate this data to a larger analysis, big issues can arise and be hard to fix even in 2017, because of the evolution of techs and standards.


=== d. In the meantime, customers have growing expectations about the quality of service


Difficulties posed by data integration do not slow or decrease customers expectations.
To the contrary, we see an elevation of expectations.
Customers increasingly expect:

- realtime contact
- two-ways interaction (they want to be able to voice their opinion, and get a response)
- seamless experience (no glitch, modern UI, consistence of the UX across channels)
- personalized experience (customization of the message they receive)


=== e. Example: A French bank going through the 2010s


image::Before---a-couple-of-data-sources-across-a-few-channels.png[align="center", title="Before - a couple of data sources across a few channels"]
{nbsp} +


image::Now---many-data-sources-across-a-variety-of-channels.png[align="center", title="Now - many data sources across a variety of channels"]
{nbsp} +



== 3. Tools for data integration: DMPs and more


=== a. Data Management Platform (DMP)


In 2015/2016 a new acronym started to trend: "DMP", standing for *"Data Management Platform"*.

Basically a DMP is an information system dedicated to solving the issues of data integration:


- it can store a large amount of data
- it can receive data from a variety of sources, in a variety of formats


- it offers functions to reconcile records from different data sources and generate a unique identifier for each reconciled entry.
- it offers segmentation / classification functions


- it provides security and analytics capabilities on the data
- it makes this data available for execution by other software.


=== b. DMP in relation to other information systems


DMPs are relatively new. They integrate with 3 other information systems in the firm:


- CRM (Customer Relationship Management)
** This is the software *gathering* data related to customers and sales. It is a major source of *input data* for a DMP.


- ERP (Enterprise Resource Planning)
** Large software synchronizing information systems from finance, sales, logistics and more. The CRM can be independent or part of the ERP.


- DSP (Demand Side Platform)
** https://digiday.com/media/wtf-demand-side-platform/[piece of software automatizing ad buying]. So, the audiences identified in the DMP could be served corresponding ads automatically with a DSP.


How can data circulate across these software and with the external world? The next lesson is devoted to APIs, another important concept.


<<<

= APIs and their business relevance

== 1. Definition of API

API: acronym for "Application Programming Interface"

An API is the way to make software programs “easy to plug and share” with other programs.

Ok so... APIs are a cable? A computer? A USB connection? No.

An API is simply a group of rules (you can also call it a convention, or an agreement...) which programmers follow when writing the part of their code which is in charge of communicating with other software.

These rules are then published (on a webpage for example), so that anyone who needs to connect to the program can learn what rules to follow.
That's it.

So, an API is simply a way to write code to make it easy to interface with other programs?
Yes.

Why the fuss then?

Having conventions on how to write a software so that somebody can plug it to its own software is one thing.
APIs of this sort are a https://dzone.com/articles/how-design-good-regular-api[classic topic in computer science] but we are not concerned with this here.

APIs we are going to discuss are about communication between distant computers, in a business context.

Let's do a bit of history:

== 2. The origin of APIs

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

EDIs still exist, especially in large B2B industries like transportation (http://cerasis.com/2014/12/11/edi-in-transportation/[check here]), but it lost in popularity in the wider economy because...  APIs have arrived.

=== b. The emergence of web APIs

In the late 1990s and early 2000s, Internet and the World Wide Web expanded a lot.

More and more servers in different parts of the world needed to be interfaced with each other to exchange data.

It became increasingly convenient to define simple and universal conventions that everyone could learn and follow to standardize these exchanges, for free and easily.

That's what *web APIs* do. They are also often called:

- "*API*" for short
- "*web services*"
- "*REST* API" (see below for that last one).

A web API extends the logic of the APIs we have seen in the beginning of this document, to software communicating via the web.

To recall, an API is a convention followed when writing a software, making this software available to other software.

NOTE:: Example: the API of Microsoft PowerPoint enables the import of Excel tables in pptx documents, because the API of Powerpoint plugs to the API of Excel. In this example Excel and Powerpoint are suposed to be installed on the same computer of course!

*Web* APIs are APIs which enable two pieces of software to communicate, via Internet. *They don't need to be installed on the same computer.*

=== c. The benefits of a web API compared to an EDI

Unlike EDI, web APIs drop any industry-specific concern. Web APIs are just a convention to send and receive data over the Internet, without any saying on the content of the data.

The data sent and received can be invoices, webpages, train schedules, audio, video... whatever.

Contrary to EDIs, a company creating a web API can choose to leave its access open (remember that EDIs need the two parties to have a pre-established agreement).

So that a potential client interested in using the web API of a company can set it up in a couple of clicks, instead of waiting weeks or months before a contract is signed and the EDI is setup.

WARNING:: Saying that APIs are open does not mean an absence of security: communication through APIs can easily be identified and encrypted, as needed.

=== d. REST API?

Two popular web API conventions emerged in the 1990s and competed for popularity:

- SOAP (https://en.wikipedia.org/wiki/SOAP[Simple Object Access Protocol])
- REST (https://en.wikipedia.org/wiki/Representational_state_transfer[Representational State Transfer])

REST became ultimately the most widely adopted, because it uses the same simple principles that webpages use to be transferred over the Internet (the "http" protocol that you see in web page addresses).
This is why APIs are often called https://www.youtube.com/watch?v=7YcW25PHnAA["REST APIs"].

In 2000-2010, it became increasingly easy and natural to adopt the REST convention to make one's software and data available to another computer.
This simple evolution to ease interoperability had *immense effects*:

== 3. Business consequences of APIs
=== a. APIs *opened* software to the world

An API transforms a closed software into something that can be plugged to anything other computer or object, as long as it is connected to the Internet.

For instance, APIs were a key factor of success for https://en.wikipedia.org/wiki/Salesforce.com[SalesForce] in the early 2000s. SalesForce, created in 1999, has a revenue of US$8.39 billion in 2017:

- SalesForce developed a CRM as a SaaS where features of the CRM were *exposed as APIs* (meaning, these features could be plugged to external apps via the REST protocol).

- SalesForce created a PaaS to host apps that could plug to the SalesForce CRM via the APIs developed by SalesForce.

This platform is called https://www.salesforce.com/products/platform/products/force/[Force.com] and external developers can put their apps there, as long as they are compatible with the SalesForce API.

SalesForce takes a commission on the sales made by these third party apps hosted on Force.com, but more importantly, the platform creates an *ecosystem* of apps and developers around the SalesForce products which makes it hard for a customer company to switch to a different product.

=== b. APIs *accelerated* software innovation


Thanks to API it became easy to add software blocks together and create new apps, even if the app developers where from different countries, industries, or big and small. https://medium.freecodecamp.org/how-i-replicated-an-86-million-project-in-57-lines-of-code-277031330ee9[Check this amazing story].

=== c. APIs *opened* data

Companies and public organization own many datasets of great business interest.
The use of these datasets can be free (for small projects and NGOs) or monetized if the user is an entreprise.

Without APIs, datasets can be made publicly available as docs (eg, Excel spreadsheets) to download but this is not practical (try downloading something like `all_train_schedules_2000_to_2017.xls` ! 😓).

So, imagine a transportation company like French SNCF which finds it interesting to publish station names, train schedules, etc. because it could be used by other companies to build new services : how can it do it?

The data is on a server of SNCF. Then SNCF adds https://data.sncf.com/api/en[an API and its documentation], making the data available to anyone who knows about REST APIs (and https://youtu.be/7YcW25PHnAA[this is trivial]).

Entrepreneurs and programmers in general will be able to access the data via the API and use it, possibly to create new services based on this train information.

== 4. The ecosystem of APIs
=== a. A wealth of APIs

To discover new APIs, or to make your APIs easier to discover, the most well known place is the website "Programmable Web": https://www.programmableweb.com/

Searching on this website, you will find APIs ranging from the most https://www.programmableweb.com/api/coca-cola-enterprises[business-y] use case, to APIs of a https://www.programmableweb.com/api/itsthisforthat[more fun and odd sort].


Still, many APIs are not listed on this website, and a google search for "info I need + API" is also a good way to find if the API you'd need exists. Interested in whale sightings? http://hotline.whalemuseum.org/api[There is an API for that].


=== b. APIs: a business world of its own

APIs have become central to the economy. As a result, a large number of services associated to APIs have developed to cater for all the needs of companies that use them.

How to create an API, how to manage the documentation of a large number of APIs, how to connect a wide variety of APIs, how to manage the security of APIs, how to monetize and API...

-> Many large firms and startups now specialize in all these different issues.
Here is the 2017 landscape of the main companies active in the API industry:

image::api-landscape-2017.jpg[align="center", title="The API landscape in 2017"]
{nbsp} +


<<<

= Essential notions on privacy and data protection

== 1. Privacy: just one aspect of data protection

image::Defining-data-protection.png[align="center", title="Defining data protection"]
{nbsp} +

== 2. When is personal information considered "data"?

At the most basic level, anything could count as "data" with possibly a personal character to it, including comments written about somebody in a personal notbook.

In practice, "data" starts to to be considered as such when:

This is information capable of being processed *automatically*

-> Hint: data on computers, not unstructured written notes

*Or* infomation intended to be processed automatically

-> Hint: paper records to be fed in a computer (eg, via scanning), not any pile of paper on your desk.

Or *structured information* that can be used to facilitate the retrieval of specific information on specific individuals

-> Hint: paper records, filing systems, databases

== 3. Personal data matters because of privacy

[quote, CNIL (French Independent Administrative Authority),https://www.cnil.fr/en/personal-data-definition]
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

This right to privacy enables individuals to define their identity in relation to the world, by giving each individual the power to control what to keep for themselves, and what to reveal / share with the world.

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

== 4. Evolution of privacy

Privacy is a social norm which transforms as societies evolve. Since the 2000s, a couple of tendencies can be identified:

- increasing tracking of the digital traces left by individuals by companies which use these traces for ad targeting and data reselling

- increasing state surveillance through digital means, against security threats and unspecified goals.

- broader public acceptance of new forms of violations to privacy.

For example, https://en.wikipedia.org/wiki/Reality_television[TV shows] where participants are filmed 24/24 and where they reveal their (real or supposed) intimacy, dates back only from the late 1990s.

[link=http://www.imdb.com/title/tt0120382/]
image::truman.jpg[align="center", title="The Truman Show, 1998"]
{nbsp} +

== 5. Privacy of the consumer and privacy of citizens: the relations between the two

Thanks to whistleblowers like https://en.wikipedia.org/wiki/Edward_Snowden[Edward Snowden], the extent of privacy breaches by governmental agencies is now better known:

video::108771171[vimeo]

Journalists, academics, activists and NGOs such as the https://www.eff.org/[Electronic Frontier Foundation] make the case that:

- consumers are insufficently aware and sensitive of how much information is captured in the normal conduct of their lives, just by using mobile phones and apps, web browsing, and increasingly in public places.

- citizens are insufficently aware and sensitive of the breach of their privacy by security agencies of their own country of residence, and by other countries.

Many citizens consider that if they don't break the law, then they have "nothing to hide".

Similarly, consumers might find that bargaining their private data against a free service and some targeted ads, is a good deal.


Sociologist of technology http://technosociology.org/[Zeynep Tufekci] goes further:

Her argument is that besides "surveillance" and "lack of privacy", companies like Google and Facebook developing a business model based on ad targeting by analytics on personal data, design a *persuasion architecture* which can be used / highjacked for political purposes.

Tufeckci does not argue that Google, Facebook or the likes inherently have anti-democratic purposes, but that:

- they develop of an information architecture which has the potential to shape opinions of crowds,
- they do so without transparency

- some past experiments on voting in the US, and current developments on electronic surveillance in China, show that the power of these technologies has already consequences in the real world.


https://www.ted.com/talks/zeynep_tufekci_we_re_building_a_dystopia_just_to_make_people_click_on_ads[link to the TEDx conference by Zeynep Tufekci]
{empty} +


== 6. Conclusion: data protection in business, more than an regulatory obligation

The collection and treatment of personnal data by businesses has far reaching implication, and should not be considered merely from a legal standpoint by firms.

The topic engages the https://en.wikipedia.org/wiki/Corporate_social_responsibility[Corporate social responsibility] of the firm.

The nature of the business model itself - profiling consumers in the most specific way - has profound consequences on the design of the environment surrounding individuals.

What are the next steps? Several trends can be identified:

1. some voices question the business model: are personalized ads based on personal data as effective as the market valuation of Facebook suggests? How much is just scam? Some voices warn against the extent of the fraud, as the video below shows (see also https://digiday.com/media/ft-warns-advertisers-discovering-high-levels-of-domain-spoofing/[here], or https://digiday.com/media/ft-warns-advertisers-discovering-high-levels-of-domain-spoofing/[here]):

video::oVfHeWTKjag[youtube]

[start=2]
2. legislation by political authorities to protect the public interest, especially via an obligation for transparency, in the face of more personal data being collected, for a larger variety of purposes. See our related lecture on the GDPR.

[start=3]
3. a deepening of the current model with more personal data being collected, in private spaces (homes) and behavior in relation to the public (crowd management in streets, stadiums, etc.):

image::amazon-echo.jpg[align="center",title= "Echo Alexa, a home assistant collecting personal data"]
{nbsp} +



<<<


[Index]
= Index
related lecture on the GDPR.

[start=3]
3. a deepening of the current model with more personal data being collected, in private spaces (homes) and behavior in relation to the public (crowd management in streets, stadiums, etc.):

image::amazon-echo.jpg[align="center",title= "Echo Alexa, a home assistant collecting personal data"]
{nbsp} +



<<<


[Index]
= Index
