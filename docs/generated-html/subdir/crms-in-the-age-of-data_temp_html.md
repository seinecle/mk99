= CRMs in the age of data
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


== 1. Definition of CRM
//ST: 1. Definition of CRM

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

== 2. CRMs - before
//ST: 2. CRMs - before

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

== 3. The digital transformation, 2006-2015
//ST: 3. The digital transformation, 2006-2015

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


== 4. Consequence of this digital transformation: the customer relationship and CRMs have evolved
//ST: 4. Consequence of this digital transformation: the customer relationship and CRMs have evolved

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

-> it becomes increasingly hard to record customers actions (is this customer in my shop the same that clicked on this web page 2 minutes ago?): "click and collect" for example, one example of the broader trend called "https://www.seo.com/blog/phygital-marketing-where-the-physical-and-digital-worlds-converge/[phygital marketing]".

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
iii. Personalizing the customer relationship, even when effective, is not inherently a good thing. It has been shown that the Coca-Cola #ShareaCoke campaign is effective at making more children choose a soda with a label to their name, over a healthy drink (paying version of the study http://onlinelibrary.wiley.com/doi/10.1111/ijpo.12193/abstract[here], free version not available).

//ST: !
iv. Personalization through smart CRMs? Companies rated with the best customer service do personalization differently: with humans.

//ST: !
See how Zappos offers a great service to their customers:

video::vApoQPISmvs[youtube]

(https://www.youtube.com/watch?v=IwE1zb9fiVs[another impactful version here])

//ST: !
or see (in French) how https://medium.com/@djo/obsession-service-client-captain-train-cb0b91467fd9[Trainline makes its customers happy].


== 5. Todays's CRMs must be data-driven
//ST: 5. Todays's CRMs must be data-driven

//ST: !
Explaining the expression "data-driven CRMs":

-> CRMs must turn from a system "supporting the firm's administration needs" to a a system tuned to "plug, host, analyze and push actions from multiple data sources".

//ST: !
To get such a CRM to run in an organization, the right resources must be gathered:

//ST: !
a. Adequate software:

- the CRM itself - recent enough that it can plug and play with a DMP and a large variety of data sources.
- a Data Management Platform (*DMP*) as well. The DMP is the software specializing in receiving data streams from a variety of sources and in a variety of formats, and reconciling them (see the lecture on Data Integration).
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
