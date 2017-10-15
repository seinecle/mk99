= Localization and value creation

Clément Levallois <levallois@em-lyon.com>
2017-31-07

last modified: {docdate}

:icons!:
:iconsfont:   font-awesome
:revnumber: 1.0
:example-caption!:

:title-logo-image: EMLyon_logo_corp.png[width="242" align="center"]

[.stretch]
image::EMLyon_logo_corp.png[width="242" align="center"]


==  'Escape' or 'o' to see all sides, F11 for full screen, 's' for speaker notes


==  1. Localization brings interesting new dimensions

==  !
Localization relates activities to physical space, in at least 4 different ways:

==  !
Place: Where is this activity happening?

==  !
Distance: Are these two agents neighbors?

==  !
Movement: Is this agent travelling?

(together with *speed* and *acceleration*)

==  !
Structure: How are these agents and activities *configured* in space?


==  !
==== a. Example - Facebook Local Awareness Feature

==  !
[.stretch]
image::fb-aware.png[align"center", title="Facebook Local Awareness Ad Feature"]


==  !
“Helping Local Businesses Reach More Customers”:

- Target ads to people living in a radius around your store.
- Can also target people who have been recently in this radius.

-> https://www.facebook.com/business/learn/facebook-create-ad-reach-ads

==  !
video::-YE90ygswoU[youtube]


==  !
==== b. Example - Data @GrandLyon

==  !
https://data.grandlyon.com/[
image:logo-smart-data-grand-lyon.png[align"center", title="Grand Lyon Data"]]

==  !
An initiative by the city of Lyon

-> Making data open to foster innovation for citizens and businesses

-> Includes many datasets with geographical relevance

==  !
Similar initiatives in large cities:

https://data.amsterdam.nl/[image:amsterdam.gif[width=150]]
https://www.beijingcitylab.com/[image:bjcitylab.jpg[width=150]]
http://www.milanosmartcity.org/joomla/[image:milano.jpg[width=150]]
http://smartcity.jakarta.go.id/[image:jakarta.png[width=150]]
http://smartcityinnovationlab.com/[image:lisboa.png[width=150]]

==  2. The visual power of maps

==  !
==== a. Map: useful metaphors with a political dimension

==  !
- The visual metaphor of the map is widely understood

- Makes exploration easy: all visible at once, while zoom allows for details as well

- Multiple information cues (colors, symbols, shapes, layers, etc.)


==  !
- Keep in mind: maps are always *political*

- Watch this extract from the TV series "The West Wing“, Season 2, Episode 16:

==  !
video::vVX-PrBRtTY[youtube]

==  !
==== b. Example: how to explore the real estate market in the Netherlands

==  !
- Every single building of the Netherlands on a map
- Colored by year of construction
- With role (retail or housing?) and surface highlighted
- Zoomable and draggable

==  !
http://code.waag.org/buildings/[image:waag.png[align"center", title="Visual exploration of real estate in NL"]]

==  !
==== c. Key resources to work with maps

==  !
[.stretch]
image::stamen.jpg[align="center", title="Stamen Design"]


- Agency based in San Francisco
- Famous for cutting research in map design

==  !
[.stretch]
image::mapbox.png[align="center", title="MapBox"]


- Mapbox.com
- SaaS to create interactive maps in web pages and mobile apps.

==  !
[.stretch]
image::openstreetmap.png[align="center", title="Openstreetmap"]


- OpenStreetMap
- A crowd sourced open source map of the world. Available through API.


==  3. How to represent “space” in data format?

==  !
==== a. The specifity of geospatial data
==  !

Data is traditionally stored in tables in relational databases, taking this form:

[.stretch]
image::table-example.png[align="center", title="A table with two entries"]


==  !
A table can have millions of rows. How to retrieve information such as "get all customers living in Rotterdam"?

"SQL" (Structured Query Language) is a system to express these kinds of queries.

==  !
In the table shown above, a query written in SQL look in the "Address" column and inspect all the text to find if "Rotterdam" is present or not.

==  !
This is highly inefficient (slow), and more complex queries would not work.

For example, the table above could not be queried for "get all customers living in a 10 miles radius around Rotterdam".

==  !
So how to store geospatial data in a way that makes it easy to retrieve?

==  !
==== b. Solutions to store and retrieve geospatial data
==  !


1. SQL solutions

Even if SQL does not perform well on geospatial data "out of the box", extra modules have been developed to deal with it.

==  !
Microsoft SQL server since 2008:

- Possible to store and query “geometric” and “geographic” objects
- Possible to use complex queries on these objects

==  !
[start=2]
2. NoSQL solutions

Since ~ 2005, new types of databases have been developed, which don't follow a table structure in order to facilitate the query of special kinds of data, like geospatial data or network data.

These new databases are called "NoSQL databases"

==  !
[.stretch]
image::carto.png[align="center", title="the Carto Platform"]


https://carto.com/[Carto (ex CartoDB)]: specializing in geospatial data + mapping.

==  !
[.stretch]
image::neo4j.png[align="center", title="Neo4J, a database for networks"]


http://neo4j-contrib.github.io/spatial/[Neo4J Spatial] enables to mix the logics of networks with places in the data, so that you can make such queries on your data:

"Select all streets in the Municipality of NYC where at least 2 of my friends are walking right now."

==  !
[.stretch]
image::topojson.png[align="center", title="GeoJSon and TopoJSon are derivations of the json formats for geospatial data"]


GeoJSon and TopoJSon: 2 data formats to represent geometric and geographic data developed for Javascript applications – and beyond.

==  4. Two friends for localization: personalization and real-time

==  !
Knowing the person, its location, at a precise time unlocks meaningful push notifications

==  !
Push notifications are these alerts sent by an app on your mobile, visible as transient icons.

==  !
Gets “push marketing” back on solid foundations:

Push marketing actions only to the right person, at the right place, at the right time (and at the right frequency!)

==  5. Ending with a provocation: Challenging the usefulness of location

==  !
==== a. Localization is about people and __territories__
==  !
- Data is a fungible and universal material (just 0s and 1s)

- Geographical coordinates are perfectly universal (just need a longitude and latitude)

and yet …

==  !
The logic of territories is shaping data: there is a geography of data.

Cultural, social, political, linguistic, economic dimensions to data.

-> representations with a supposedly universal and transparent coordinate system blinds us to this fact.

==  !
This argument is made by Frederic Martel in his book "Smart": Internet does not flatten everything into one big model. There are several Internets with their geography, politics and sociology.

==  !
https://www.amazon.com/s/ref=nb_sb_noss?url=search-alias%3Daps&field-keywords=smart+frederic+martel&rh=i%3Aaps%2Ck%3Asmart+frederic+martel[image:smart.jpg[align="center", title="Smart by Frederic Martel"]]

==  !
- Data protection: http://www.darkreading.com/cloud/privacy-security-and-the-geography-of-data-protection-/a/d-id/1315480[not all countries are equal]

==  !
- Data handling devices

India and Africa  have ++ share of mobile devices

==  !
- Data production

Amazon Mechanical Turk is a service of data production through the hiring of a distributed crowd of workers. Tends to "erase distance".

Yet, the geographical distribution of workers on Amazon Mechanical Turk is far from even. The following figure is taken  http://aclweb.org/anthology/Q14-1007[from this study]:

==  !
[.stretch]
image::amt-distribution.png[align="center", title="Distribution of Amazon Mechanical Turk workers"]



==  !
==== b. Distributed systems – the end of territories?

==  !
The libertarian dream of the cypher-punks: individuals transact without consideration for their nationality, currency, legal system, political regime.

==  !
Organizations, banking, voting systems, … any aggregated human activity could emerge without reference to local territories or institutions. Just groups of individuals transacting voluntarily and securely, without a notion of place or distance.

==  !
- Bitcoin: the currency for these transactions?
- Torrent: The exchange platform for numeric goods?
- Etherum: the platform where contracts are made and executed?

==  !
https://www.amazon.com/This-Machine-Kills-Secrets-Whistleblowers/dp/0142180491/ref=sr_1_1?ie=UTF8&qid=1508079962&sr=8-1&keywords=this+machine+kills+secrets[image:cypherpunks.png[align="center",title="This machine kills secrets by Andy Greenberg"]]

==  The end
==  !

Find references for this lesson, and other lessons, https://seinecle.github.io/mk99/[here].

image:round_portrait_mini_150.png[align="center", role="right"]
This course is made by Clement Levallois.

Discover my other courses in data / tech for business: http://www.clementlevallois.net

Or get in touch via Twitter: https://www.twitter.com/seinecle[@seinecle]
pass:[    <!-- Start of StatCounter Code for Default Guide -->
    <script type="text/javascript">
        var sc_project = 11411204;
        var sc_invisible = 1;
        var sc_security = "11411204";
        var scJsHost = (("https:" == document.location.protocol) ?
            "https://secure." : "http://www.");
        document.write("<sc" + "ript type='text/javascript' src='" +
            scJsHost +
            "statcounter.com/counter/counter.js'></" + "script>");
    </script>
    <noscript><div class="statcounter"><a title="site stats"
    href="http://statcounter.com/" target="_blank"><img
    class="statcounter"
    src="//c.statcounter.com/11411204/0/11411204/1/" alt="site
    stats"></a></div></noscript>
    <!-- End of StatCounter Code for Default Guide -->]
