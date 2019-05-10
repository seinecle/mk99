= The headache of data integration
Clément Levallois <levallois@em-lyon.com>
2017-31-07

last modified: {docdate}

:icons!:
:iconsfont:   font-awesome
:revnumber: 1.0
:example-caption!:
:sourcedir: ../../../main/java

:title-logo-image: EMLyon_logo_corp.png[width="242" align="center"]

image::EMLyon_logo_corp.png[width="242", align="center"]
{nbsp} +

//ST: 'Escape' or 'o' to see all sides, F11 for full screen, 's' for speaker notes

//ST: !

== 1. Data: you don't get in on tap

//ST: !

A naive vision of data would get that it's all fluid. Don't we talk about "data streams"?
Working with data would be as simple as opening a tap and "getting customer data", for instance.

//ST: !

image::tap.jpg[align="center", title="Data streams, as fluid as water on tap?"]
{nbsp} +

//ST: !

Actually, data is more like a complex patchwork: many different pieces which must be stitched together - and this is hard.

//ST: !

image::patchwork.jpg[align="center", title="Data streams make a patchwork"]
{nbsp} +

//ST: !

Take customer data.

It is not a given. Instead, this is a design made of multiple primary data sources:

//ST: !

image::Multiple-sources-of-customer-data.png[align="center", title="Multiple sources of customer data", book="keep"]
{nbsp} +

//ST: !
> Analysts often spend 50-80% of their time preparing and transforming data sets before they begin more formal analysis work.

Garrett Grolemund, http://shop.oreilly.com/product/0636920035992.do[Data Scientist and Master Instructor at RStudio]


//ST: !

Take away: Data is fragmented by nature. It comes from different sources and presented in different formats.
*You* (the marketer in collaboration with data scientists) wrangle to __construct__ customer profiles by joining and assembling different sources of data into a meaningful synthesis.

//ST: !

Data scientists actually have entire books devoted to the subject of wrangling with the complexity of integrating different data sources.

image::wrangling.jpg[align="center", title="Data wrangling"]
{nbsp} +

//ST: !

== 2. Sources of fragmentation

//ST: !

=== a. Channels keep diversifying

//ST: !

Point of sale, print, TV, radio, outdoor posters, mobile apps, mobile sites, emails, SMS, APIs, social networks, search engines, e-commerce platforms, e-commerce websites, blogs, content channels, …

-> all these channels can provide relevant data.

//ST: !

=== b. Connections between these channels intensify and complexify

//ST: !

- Social TV is TV delivered with Internet services,

- User profiles created on one platform are imported on another

//ST: !

- Orders taken online can be picked up on a variety of point of sales

- Ads circulating through one channel replicate on other channels, ...

//ST: !

-> It is very complex to trace the "customer journey" on all these channels and to keep an updated view of a customer profile.

It is even more difficult to explore causality (which action on which channel caused which subsequent action by the user?)

//ST: !

=== c. Underlying technologies fragment and keep evolving, across channels

//ST: !

Browsers, Cookies, APIs, mobile OS (Android or iOS?), etc... All these different techs evolve and need continuous effort and expertise to integrate.

//ST: !

Example: *did you notice* that on a mobile device, the url of the pages you visit can now start with an https://www.ampproject.org/latest/blog/whats-in-an-amp-url/[AMP url]?

Like, to visit the page of the New York Times the url should be http://www.nyt.com but it looks like: *http://google.com/amp/www.nyt.com*

This *http://google.com/amp* prefix is a new tech by Google to accelerate the display of web pages on mobiles. Fine.
But then, as a marketing data analyst, how to count visits to:

//ST: !

http://google.com/amp/www.nyt.com

and

http://www.nyt.com

-> It is important to count visits to these two urls as a visit *to the same page*.

//ST: !

In September 2017 major services of ((web analytics)) were still struggling with this  http://searchengineland.com/google-amp-cache-unified-users-analytics-282069[issue of page counts in web analytics].

This illustrates that to just count visits to a web page (something which should be classic and robust) and integrate this data to a larger analysis, big issues can arise and be hard to fix even in 2017, because of the evolution of techs and standards.

//ST: !

=== d. In the meantime, customers have growing expectations about the quality of service

//ST: !

Difficulties posed by data integration do not slow or decrease customer expectations.
To the contrary, we see an elevation of expectations.
Customers increasingly expect:

- realtime contact
- two-ways interaction (they want to be able to voice their opinion, and get a response)
- seamless experience (no glitch, modern ((user interface)), consistence of the ((user experience)) across channels)
- personalized experience (customization of the message they receive)

//ST: !

=== e. Example: A French bank going through the 2010s

//ST: !

image::Before---a-couple-of-data-sources-across-a-few-channels.png[pdfwidth="80%", align="center", title="Before - a couple of data sources across a few channels", book="keep"]
{nbsp} +

//ST: !

image::Now---many-data-sources-across-a-variety-of-channels.png[pdfwidth="80%", align="center", title="Now - many data sources across a variety of channels", book="keep"]
{nbsp} +

//ST: !


== 3. Tools for data integration: DMPs and more


=== a. Data Management Platform (DMP)

//ST: !

In 2015/2016 a new acronym started to trend: "DMP", standing for *"Data Management Platform"*.

Basically a *DMP*(((DMP - data management platform))) is an information system dedicated to solving the issues of data integration:

//ST: !

- it can store a large amount of data
- it can receive data from a variety of sources, in a variety of formats

//ST: !

- it offers functions to reconcile records from different data sources and generate a unique identifier for each reconciled entry.
- it offers segmentation / classification functions

//ST: !

- it provides security and analytics capabilities on the data
- it makes this data available for execution by other software.


//ST: !
=== b. DMP in relation to other components of the information system

//ST: !
*DMPs*(((DMP - data management platform))) are relatively new. They integrate with 3 other information systems in the firm:

//ST: !
- CRM(((CRM - Customer Relationship Management)))
** This is the software *gathering* data related to customers and sales. It is a major source of *input data* for a DMP.

//ST: !
- ERP(((ERP - Enterprise Resource Planning)))
** Large software synchronizing information systems from finance, sales, logistics and more. The CRM can be independent or part of the ERP.

//ST: !
- DSP(((DSP - Demand Side Platform)))
** https://digiday.com/media/wtf-demand-side-platform/[Piece of software automatizing ad buying]. The audiences identified in the DMP could be served corresponding ads with a DSP.

//ST: !
- Data lake(((data lake)))
** Data lakes are databases specializing in storing large amounts of unstructured data. They respond to the need of "storing today, for future use". A data lake is not meant to be optimized for queries. They are meant to store everything we collect today, in the case this data will serve future usages. When this happens, data can be extracted from the data lake and put in a database, in a form which makes it convenient to query and analyze.

//ST: !
How can data circulate across these software and with the external world? The next chapter is devoted to APIs, another essential concept.

== The end
//ST: !

Find references for this lesson, and other lessons, https://seinecle.github.io/mk99/[here].

image:round_portrait_mini_150.png[align="center", role="right"]
This course is made by Clement Levallois.

Discover my other courses in data / tech for business: https://www.clementlevallois.net

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
