= Big data and marketing
Clément Levallois <levallois@em-lyon.com>
2017-16-10

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
Enthusiasm, disappointment, bad buzz, worries, debates, promises... the discourse about AI will grow. AI is fed on data, so the future of big data will intersect with what AI becomes.

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


== 6. Definition of CRM
//ST: 6. Definition of CRM

CRM: acronym for "Customer Relationship Management"

A CRM is a software used to manage the commercial relationship between a company and its clients.

//ST: !
A CRM is part of the *information system* (IS) of the firm. The information system designates all software, human resources and procedures devoted to keep track of all info necessary to the business of the firm - from sales to production, etc.

//ST: !

The information system of a firm comprises many other blocks, besides the CRM:

//ST: !

image::How-a-CRM-integrates-in-the-information-system-of-a-firm.png[align="center",title="How a CRM integrates in the information system of a firm"]
{nbsp} +

//ST: !

Large companies often integrate these different blocks into an *ERP* ("Enterprise Resource Planning"), which is an even larger software able to plug different parts together.

//ST: !

The role of CRMs is evolving, and in this lecture *we make the case that "big data" has transformed CRMs radically*.

To illustrate, we will compare (and caricature a bit) a CRM from 2000 with a CRM of today:

== 7. CRMs - before
//ST: 7. CRMs - before

//ST: !
The name of the CRM - Customer *Relationship* Management suggests a kind of rich, personalized and human touch.

In practice, CRMs where used for more practical purposes:

//ST: !
image::CRMs-before-the-data-revolution.png[align="center", title="CRMs before the data revolution"]
{nbsp} +

//ST: !
We must imagine the CRM software as a tool which *supported the management of sales*, performing these 3 essential functions:

//ST: !
- measuring revenues, through the recording of sales transactions.
- controlling the performance of the sales persons, by registering which cashier, which employee performed the sale, or at least at which location the sale took place.
- recording the VAT ("Value-added tax") collected through sales, which is a legal obligation for tax declaration purposes.

//ST: !
Do you see the customer being catered for in the functions described above? No? Me neither.

//ST: !
The customer was not completely forgotten: CRM are used to run loyalty programs and campaigns:

//ST: !
==== a) loyalty programs

//ST: !
Loyalty programs afford discounts and special offers to its members.

They increase the share-of-wallet of the company implementing them: the amount of the customer's total spending that a business captures in the products and services that it offers.

//ST: !
A study performed on the loyalty programs run by 7 major supermarket chains in the Netherlands has found that it increased revenues for the supermarket running it:

//ST: !
[quote]
On average, a loyalty program enhances the net yearly revenues of a customer by € 163, but the effects vary between € 91 and € 236

source: http://www.sciencedirect.com/science/article/pii/S016781160600084X[Leenheer et al. (2007)].

//ST: !
Loyalty programs create extra value for the customer as well through the discounts and special offers they bring. But they tend to be limited in their personalization: typically, every customer can enjoy the same offers, even if many of them are irrelevant (discounts on diapers when you don't have a child etc.).

//ST: !
==== b) Direct mails and coupons

//ST: !
Customers registered in a CRM with their postal address (after joining a loyalty program) can be sent promotional material and coupons.

Using printed material prohibits the customization to the personal needs of the customers, since a printed catalogue is the same for every recipient.

This decreases the efficiency of direct mail campaigns.

== 8. The digital transformation, 2006-2015
//ST: 8. The digital transformation, 2006-2015

Changes occurring in the past decade have transformed the landscape of the customer relationship.
We should realize that:

//ST: !
==== a) Until 2006 only half of US and EU households, and 10% of the Chinese population, had Internet broadband access at home:

//ST: !
++++
<iframe src="http://www.pewinternet.org/chart/home-broadband-use/iframe/" id="pew17070" scrolling="no" width="100%" height="100px" frameborder="0"></iframe>

<script type='text/javascript'id='pew-iframe'>(function(){function async_load(){var s=document.createElement('script');s.type='text/javascript';s.async=true;s.src='http://www.pewinternet.org/wp-content/plugins/pew-scripts/js/iframeResizer.min.js';s.onload=s.onreadystatechange=function(){var rs=this.readyState;try{iFrameResize([],'iframe#pew17070')}catch(e){}};var embedder=document.getElementById('pew-iframe');embedder.parentNode.insertBefore(s,embedder)}if(window.attachEvent)window.attachEvent('onload',async_load);else window.addEventListener('load',async_load,false)})();</script>
++++


//ST: !

image::eu-broadband.png[align="center", title="Households with internet access and with broadband connection EU-28, 2007-2016"]
{nbsp} +

source: http://ec.europa.eu/eurostat/statistics-explained/index.php/E-commerce_statistics_for_individuals[Eurostat]

//ST: !

image::china-internet.png[align="center", title="China Internet Users, 2000-2016"]
{nbsp} +

source: http://www.internetlivestats.com/internet-users/china/[Internetlivestats.com]


//ST: !
==== b) Smartphones as we know them appeared just in 2007

//ST: !
image::first-iphone.jpg[align="center", title="Steve Jobs presenting the iPhone in 2007"]
{nbsp} +

//ST: !
==== c) Until 2009 social media was just taking off

//ST: !
++++
<iframe width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vR4Kh6Sf0XDOZf1-FU4VznSydrxIRm3NRJfJHIq4KYKGV2_TAtbqoI634NSu9SR0LYk3UihYLvrlHhs/pubchart?oid=412747728&amp;format=interactive"></iframe>
++++


//ST: !
==== d) Online retail is growing at a steady pace

//ST: !
Together, Alibaba and Amazon have tripled customers in 5 years, nearing 900 million customers in 2017:

//ST: !
image::alibaba-users.png[align="center",title="Active consumers on Alibaba, 2012-2017"]
{nbsp} +

//ST: !
image::amazon-users.png[align="center",title="Active consumers on Amazon, 2012-2016"]
{nbsp} +

//ST: !
==== e) The technoloy for ad campaigns has transformed

//ST: !
Three key aspects for ad buying and selling:

//ST: !
- It became programmatic: ad space and ad inventories are bought and sold through automated market places (through https://digiday.com/media/wtf-supply-side-platform/[SSP], http://adage.com/lookbook/article/dsp/demand-side-platforms-work/299456/[DSP] and http://adage.com/lookbook/article/ad-exchange/needed-ad-exchanges-work/298394/[Ad exchanges]).

//ST: !
- Ads are displayed across many channels (with https://en.wikipedia.org/wiki/Site_retargeting[retargeting])

//ST: !
- Ads are personalized (started with Search Engine Advertising showing ads matching search queries, then cookies, then browser fingerprinting (see https://panopticlick.eff.org/[here]) and https://www.theguardian.com/technology/2017/jul/03/facebook-track-browsing-history-california-lawsuit[other techniques])


== 9. Consequence of this digital transformation: the customer relationship and CRMs have evolved
//ST: 9. Consequence of this digital transformation: the customer relationship and CRMs have evolved

//ST: !
==== a) CRMs must handle multiple channels (distribution and communication)

//ST: !
Distribution and communication channels have multiplied and fragmented, and each have their different rules for content generation, data streams and communication modes.

//ST: !
Distribution channels:

- retail stores (as usual)
- ecommerce websites (since 2000s) and mobile apps (since 2010s)

//ST: !
- third party platforms (such as Amazon and Alibaba, taking off since 2010s)
- resellers becoming primary sellers (eg, http://leboncoin.fr[leboncoin.fr] or http://marktplaats.nl[marktplaats.nl] selling cars, housing and jobs) - since 2010s.

//ST: !
Multiplication of distribution channels

-> it becomes increasingly hard to record customers actions (is this customer in my shop the same that clicked on this web page 2 minutes ago?): "click and collect" for example, one example of the broader trend called " https://www.seo.com/blog/phygital-marketing-where-the-physical-and-digital-worlds-converge/[phygital marketing] ".

//ST: !
Note how traditional CRMs are unequipped to command and control this variety of distribution channels.

//ST: !
Communication channels:

From brick and mortar + call centers + sms + emails to ...

-> Live chat in websites + Facebook + Twitter + Instagram


//ST: !
==== b) CRMs must handle complex communication patterns, not just "push campaigns"

//ST: !
Communication used to be mainly "outbound" (company pushing campaigns to customers) and occasionally inbound (customers calling or emailing back).

//ST: !
Three evolutions:

//ST: !
- customers expect their point of view to be heard, without being prompted for it.
- cross customer conversation has spread (without the intervention of companies and brands)
- The high cost of pushing content through ads incentivizes firms to develop inbound communication - this is https://www.hubspot.com/inbound-marketing["inbound marketing"].

//ST: !
==== c) CRMs must accomodate multiple, fragmented touchpoints
//ST: !

- TV, radio, outdoor advertising, in store and outdoor displays: it continues
- mobile phones: operating systems with constantly evolving techs and rules of play (http://fortune.com/2017/06/22/apple-app-store-removals/[1], https://arstechnica.com/gadgets/2017/01/future-ios-release-will-soon-end-support-for-unmaintained-32-bit-apps/[2])
- desktops, tablets, social TVs, but also... watches? cars? homes?

//ST: !
==== d) CRMs must handle personalized content

//ST: !
- The expectations of customers have elevated: if your company has a Facebook page, it should not just display a catalogue. It should engage (converse) with customers.
- Same with all steps of the customer journey: a CRM should adapt the product (or service) to the profile of the customer.

//ST: !
Several remarks on personalization:

//ST: !
i. "personalization" is the extreme end: one different view for each different customer or prospect.

*Micro-segmentation* is the step just before: identifying very precise, tiny segments in the population of customers and prospects.

//ST: !
ii. "personalization" has been blamed for reinforcing "bubbles" or "tribes" views of the world (http://pubsonline.informs.org/doi/pdf/10.1287/mnsc.2013.1808[paying version] of the paper, free version https://www.researchgate.net/profile/Kartik_Hosanagar/publication/228233814_Will_the_Global_Village_Fracture_Into_Tribes_Recommender_Systems_and_Their_Effects_on_Consumer_Fragmentation/links/0046352960e0b2e12c000000/Will-the-Global-Village-Fracture-Into-Tribes-Recommender-Systems-and-Their-Effects-on-Consumer-Fragmentation.pdf[here]).

//ST: !
Content personalization is also blamed for favoring political polarization via an "echo chamber effect": social media tend to show me content I already agree with (paying version of the paper http://www.sciencedirect.com/science/article/pii/S0740624X16300375[here], free version https://www.academia.edu/24798528/Political_Polarization_on_Twitter_Implications_for_the_Use_of_Social_Media_in_Digital_Governments?auto=download[here]).

//ST: !
iii. Personalizing the customer relationship, even when effective, is not inherently a good thing. It has been shown that the http://www.coca-colacompany.com/stories/summer-of-sharing-share-a-coke-campaign-rolls-out-in-the-us[Coca-Cola #ShareaCoke campaign] is effective at making more children choose a soda with a label to their name, over a healthy drink (paying version of the study http://onlinelibrary.wiley.com/doi/10.1111/ijpo.12193/abstract[here], free version not available).

//ST: !
iv. Personalization through smart CRMs? Companies rated with the best customer service do personalization differently: with humans.

//ST: !
See how Zappos offers a great service to their customers:

video::vApoQPISmvs[youtube]

(https://www.youtube.com/watch?v=IwE1zb9fiVs[another impactful version here])

//ST: !
or see (in French) how https://medium.com/@djo/obsession-service-client-captain-train-cb0b91467fd9[Trainline makes its customers happy].


== 10. Todays's CRMs must be data-driven
//ST: 10. Todays's CRMs must be data-driven

//ST: !
Explaining the expression "data-driven CRMs":

-> CRMs must turn from a system "supporting the firm's administration needs" to a a system tuned to "plug, host, analyze and push actions from multiple data sources".

//ST: !
To get such a CRM to run in an organization, the right resources must be gathered:

//ST: !
a. Adequate software:

- the CRM itself - recent enough that it can plug and play with a DMP and a large variety of data sources.
- a Data Management Platform (*DMP*) as well. The DMP is the software specializing in receiving data streams from a variety of sources and in a variety of formats, and reconciling them.

//ST: !
- a Data Lake to store and query data.
- software bricks for additional analysis, as needed. For example, Dataiku's https://www.dataiku.com/learn/[DSS platform].

//ST: !
[start  = 2]
b. Adequate human resources:

- product managers with a tech culture (you), able to design and deploy a marketing strategy in a data intensive environment.
- data scientists who will implement the strategy.
- IT engineers to run the pumblery of the software.

//ST: !
[start  = 3]
c. Adequate organizational culture:

- This is probably the hardest part: making the top management, and the rest of the organization pay attention and believe in the possibilities afforded by these new way to manage customer relationships.
- The organization needs to invest and devote enough operational resources to stop doing "business as usual" and develop a data-driven CRM.

== 11. The role of segmentation in marketing
//ST: 11. The role of segmentation in marketing

//ST: !
==== a. The need for a market fit

//ST: !
How to market the right product to the right people?

//ST: !
image::A-product-cannot-fit-everybody's-expectations.png[align="center", "title="A product cannot fit everybody's expectations"]
{nbsp} +


//ST: !
A product cannot have every feature: adding a new feature can conflict with existing features or just hurt the need for simplicity.

//ST: !
Customers have diverging expectations: what is preferred by one customer is considered a nuisance by another.

//ST: !
Firms have limited resources: they cannot create and sell every variety of a product with every feature. They must allocate their scarce resources in the best way possible.

//ST: !
A *market fit* is achieved when there is an alignment between the product, the customers needs and the firms capabilities to deliver.

How to achieve a market fit?

//ST: !
This question is a classic field of study in marketing, and is called "market research". A market fit can be explored and found with the "STP" approach:

//ST: !
==== b. Segmentation and STP

//ST: !
STP stands for: *Segmentation → Targeting → Positioning*

This a strategy to arrive at a market fit.

Once defined, this strategy will be implemented following a *marketing plan* (for example, following the famous http://www.smartinsights.com/digital-marketing-strategy/customer-segmentation-targeting/segmentation-targeting-and-positioning/["4Ps"]).

//ST: !
Let's have a closer look at the "STP":

//ST: !
- SEGMENTATION

First, cut the crowd into segments of customers with similar characteristics / expectations / needs

//ST: !
- TARGETING

Then, evaluate each segment, and select the most attractive one.

//ST: !
- POSITIONING

Creating an offer (a value proposition) corresponding to the segment we target

//ST: !
"Segmenting a market" is the first step of this STP strategy.

It is the key operation where the "anonymous crowd of potential buyers" is analyzed and cut into distinct groups which can be interested in the same kind of product or service.

== 12. How to segment, in practice?
//ST: 12. How to proceed to segment, in practice?

//ST: !
==== a. Quantitative vs qualitative methods

//ST: !
Qualitative and quantitative methods can be used for segmentation.

//ST: !
Qualitative methods include surveys, ethnographic observation (online or offline), literature reviews on socio cultural trends, text analysis, interviews, focus groups, and more.

//ST: !
The point of these qualitative methods is to identify typical *usages* and *attitudes* towards the product (aka, *use cases*) among potential customers.
Each of these use cases is a potential segment to address.

//ST: !
Qualitative methods are strong at *identifying* segments, and also strong at *understanding* and *explaining* them: we understand better *why* people make their choices.

//ST: !
Qualitative methods are not strong at evaluating the *size* and at *generalizing* beyond the circumstances of the observations made.

//ST: !
In comparison, quantitative methods are relatively stronger at *measuring*, *comparing* and *generalizing*.

//ST: !
Quantitative methods put numbers on things, allowing for an estimation of absolute and relative mangitudes: is this segment a large one? The largest?

//ST: !
And contrary to qualitative methods, quantitative methods are good at projecting a small sample to a larger situation, all while measuring by how much we can be off - that's what statistics do.

//ST: !
But let's not forget about 2 relative weaknesses of quantitative studies compared to qualitative ones:

//ST: !
- correlations are easy to find, *causality* is harder to prove.
- *explanations* (causality + motives -> the why?? question) are also hard to establish.

-> we detail *some* of these quantitative methods below.


//ST: !
==== b. Methods for segmentation in data science: "clustering"

//ST: !
(we use "data science methods" here, but that's very close to "machine learning techniques")

//ST: !
Many overviews of ML techniques tend to have a special category for "clustering techniques" (http://scikit-learn.org/stable/tutorial/machine_learning_map/[1], https://www.pinterest.fr/pin/440367669799815280/[2], https://s3-ap-south-1.amazonaws.com/av-blog-media/wp-content/uploads/2017/02/17090804/microsoft-machine-learning-algorithm-cheat-sheet-v6.pdf[3]).

For example at the bottom right of this chart:

//ST: !
image::ds_techniques_cheatsheet_1.png[align="center", title="data science techniques grouped in families"]
{nbsp} +

source: https://machinelearningmastery.com/a-tour-of-machine-learning-algorithms/[machinelearningmastery.com]

//ST: !
Clustering means "finding groups" in the data. This is analogous to "segmenting" in marketing. So the clustering techniques from machine learning can be used for segmentation.

//ST: !
Does it mean that the other methods shown on the chart above are useless for segmentation?

-> *NO*

//ST: !
For example, Principal Component Analysis (PCA) is classified in the chart as a technique for "dimensionality reduction" (we'll explain this term in an other course), even if it has been used for a long time in marketing (and elsewhere) to segment a dataset (see a great example and tutorial http://www.business-science.io/business/2016/09/04/CustomerSegmentationPt2.html[here]).

//ST: !
==== c. Two classic clustering methods: k-means and hierarchical clustering

//ST: !
IMPORTANT: just to remind you that the goal of this course is to make you familiar and knowledgeable about *what it means to do data science in a business context*, not to turn you in data scientists. Knowing the general principles of k-means and hierarchical clustering is useful if you want to work productively as a business person with data scientists.

//ST: !
The general approach for clustering is:

//ST: !
1. Get data

For example, data on car drivers from consumer panel providing info on their demographics, tastes in car size and design, and pricing preferences

//ST: !
[start =2]
2. Develop measures of association

This means creating a measure of “which customer is similar to which” in terms of their features

//ST: !
For example, families with young children will be roughly similar in terms of demographics, needs and budget.

//ST: !
[start =3]
3. Deal with outliers

Removing car drivers that have extreme values? (the one car driver that needs a race car, etc.)

//ST: !
[start =4]
4. Form segments

Use analytical techniques to create groups of car drivers based on their associations. Also called “clusters” or “communities”.

//ST: !
[start =5]
5. Profile segments and interpret results

Groups have now been found automatically. Identify what these groups mean and how they show a path for action.


//ST: !
==== d. hierarchical clustering

//ST: !
image::Hierarchical-clustering.png[align="center", title="Hierarchical clustering"]
{nbsp} +

//ST: !
==== e. k-means clustering

//ST: !
image::k-means-clustering.png[align="center", title="k-means clustering"]
{nbsp} +

//ST: !
==== f. clustering using community detection - via network analysis

//ST: !
This last example of a clustering technique is a bit fancy - not usually represented in ML cheatsheets.

See the lesson on "Network analysis and text mining" for an example of how it can be practised in http://www.gephi.org[Gephi].

//ST: !
image::community-detection.png[align="center", title="community detection"]
{nbsp} +

//ST: !
This clustering example is particularly interesting because the number of clusters found in the dataset is not specified in advance: it "emerges" through the analysis.

(contrary to k-means where the number of clusters is set by the analyst: it is the "k" parameter).

== 13. Last notes: clustering, useful beyond segmenting in marketing
//ST: 13. Last notes: clustering, useful beyond segmenting in marketing

//ST: !
-> It reveals groups, relations between groups

-> With the network approach, it can even point to the position of single individuals in each group (are they central? Do they bridge to other segments?)

-> Useful for operational marketing (ex: email campaigns), not just strategic product launch!

== 7 roads to data-driven value creation
//ST: 7 roads to data-driven value creation
//ST: !

[IMPORTANT]
====
Not a closed list, not a recipe!

Rather, these are essential building blocks for a strategy of value creation based on data.
====

== 1. PREDICT
//ST: 1. PREDICT

//ST: !
image::prediction.jpg[align="center"]
{nbsp} +

//ST: !
==== Prediction: The ones doing it

//ST: !
|===

1. Predictive churn / default / ... (banks / telco)

2. Predicting crime image:predpol.png[width="100"]

3. Predicting deals image:tilkee.png[width="100"]

4. Predictive maintenance image:cat.jpg[width="100"]

|===

//ST: !
==== Prediction: the hard part

//ST: !

|===

1. Collecting data (https://indatalabs.com/blog/data-science/cold-start-problem-in-recommender-systems[cold start problem])

2. Risk missing the long tail, algorithmic discrimination, stereotyping

3. Neglect of novelty
|===


== 2. SUGGEST
//ST: 2. SUGGEST
//ST: !

image::suggestion.jpg[align="center"]
{nbsp} +

//ST: !
==== Suggestion: The ones doing it

//ST: !
|===


1. Amazon’s product recommendation system image:amazon.jpg[width="100"]

2. Google’s “Related searches…” image:google.jpg[width="100"]

3. Retailer’s personalized recommendations image:auchan.jpg[width="100"]

|===

//ST: !
==== Suggestion: the hard part

//ST: !
|===

1. The https://indatalabs.com/blog/data-science/cold-start-problem-in-recommender-systems[cold start problem], managing serendipity (see review: https://doi.org/10.1016/j.knosys.2016.08.014[paying version], free version not available) and "filter bubble" effects (review: https://doi.org/10.1145/2566486.2568012[paying version], http://wwwconference.org/proceedings/www2014/proceedings/p677.pdf[free version here]).

2. Finding the value proposition which goes beyond the simple “you purchased this, you’ll like that”

|===


== 3. CURATE
//ST: 3. CURATE
//ST: !

image::curation.jpg[align="center"]
{nbsp} +

//ST: !
==== Curation: The ones doing it

//ST: !
|===

1. Clarivate Analytics curating metadata from scientific publishing image:crv_logo_rgb_rev.png[width="100"]

2. Nielsen and IRI curating and selling retail data image:nielsen.jpg[width="100"] image:iri.jpg[width="100"]

3. ImDB curating and selling movie data image:imdb.jpg[width="100"]

|===

//ST: !
==== Curation: the hard part

//ST: !
|===

1. Slow progress: curation needs human labor to insure high accuracy, it does not scale the way a computerized process would.

2. Must maintain continuity: missing a single year or month hurts the value of the overall dataset disproportionally.

3. Scaling up / right incentives for the workforce: the workforce doing the curation should be paid fairly, which is https://www.wired.com/story/amazons-turker-crowd-has-had-enough/[not the case yet].

4. Quality control

|===


== 4. ENRICH
//ST: 4. ENRICH
//ST: !

image::enrich.jpg[align="center"]
{nbsp} +

//ST: !
==== Enrichment: The ones doing it

//ST: !
|===

1. Selling methods and tools to enrich datasets image:watson.png[width="100"]

2. Selling aggregated indicators image:edf.jpg[width="100"]

3. Selling credit scores

|===

//ST: !
==== Enrichment: the hard part

//ST: !
|===

1. Knowing which cocktail of data is valued by the market

2. Limit replicability

3. Establish legitimacy

|===


== 5. RANK / MATCH / COMPARE
//ST: 5. RANK / MATCH / COMPARE
//ST: !

image::rank.jpg[align="center"]
{nbsp} +

//ST: !
==== Ranking / matching / comparing: The ones doing it

//ST: !
|===

1. Search engines ranking results image:google.jpg[width="100"]

2. Yelp, Tripadvisor, etc… which rank places image:tripadvisor.jpg[width="100"]

3. Any system that needs to filter out best quality entities among a crowd of candidates

|===

//ST: !
==== Ranking / matching / comparing: the hard part

//ST: !
|===

1. Finding emergent, implicit attributes (imagine: if you rank things based on just one public feature: not interesting nor valuable)

2. Insuring consistency of the ranking (many rankings are less straightforward than they appear)

3. Avoid gaming of the system by the users (for instance, http://www.nytimes.com/2011/02/13/business/13search.html[companies try to play Google's ranking of search results at their advantage])

|===


== 6. SEGMENT / CLASSIFY
//ST: 6. SEGMENT / CLASSIFY
//ST: !

image::muffin.jpg[align="center"]
{nbsp} +

//ST: !
==== Generating: The ones doing it

//ST: !
|===

1. Tools for discovery / exploratory analysis by segmentation

2. Diagnostic tools (spam or not? buy, hold or sell? healthy or not?) image:medimsight.png[width="100"]

|===

//ST: !
==== Segmenting / classifying: the hard part

//ST: !
|===

1. Evaluating the quality of the comparison

2. Dealing with boundary cases

3. Choosing between a pre-determined number of segments (like in the k-means) or letting the number of segments emerge

|===


== 7. GENERATE / SYNTHETIZE(experimental!)
//ST: 7. GENERATE / SYNTHETIZE (experimental!)
//ST: !

image::generate.jpg[align="center"]
{nbsp} +

//ST: !
==== Generating: The ones doing it

//ST: !
(click on the logos to get to the relevant web page)

//ST: !


|===

1. Intelligent BI https://www.aiden.ai/[image:aiden.png[witdth="100"]]

2. wit.ai, the chatbot by FB https://wit.ai/[image:wit.png[witdth="100"]]

3. Virtual assistants https://www.cxcompany.com/digitalcx/[image:cx.jpg[witdth="100"]]

4. Image generation https://deepart.io/[image:deepart.png[witdth="100"]]

5. Close-to-real-life speech synthesis https://deepmind.com/blog/wavenet-generative-model-raw-audio/[image:google.jpg[witdth="100"]]
|===

//ST: !
==== Generating: the hard part

//ST: !
|===

1. Should not create a failed product / false expectations

2. Both classic (think of image:clippy.jpg[width="50"]) and frontier science: not sure where it’s going

|===

//ST: !

== Combos!
//ST: Combos!

//ST: !
image::Combinations.png[align="center", "title="Combinations"]
{nbsp} +



== The end
//ST: The end
//ST: !

Find references for this lesson, and other lessons, https://seinecle.github.io/mk99/[here].

image:round_portrait_mini_150.png[align="center", role="right"]
This course is made by Clement Levallois.

Discover my other courses in data / tech for business: http://www.clementlevallois.net

Or get in touch via Twitter: https://www.twitter.com/seinecle[@seinecle]
