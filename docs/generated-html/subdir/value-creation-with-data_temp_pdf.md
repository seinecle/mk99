= Big data for business: Value creation with data
Clément Levallois <levallois@em-lyon.com>
2017-09-10

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


== Seven roads to data-driven value creation
//ST: Seven roads to data-driven value creation
//ST: !

//ST: !
[IMPORTANT]
====
Not a closed list, not a recipe!

Rather, these are essential building blocks for a strategy of value creation based on data.
====

== 1. PREDICT
//ST: 1. PREDICT
//ST: !

.Predict
|===
| *The data you need* | *The hard part*

|

1. Domain specific historical data

2. Data mashups

3. Feedback mechanism on the accuracy

|

1. Collecting data ("cold start problem")

2. Risk missing the long tail, algorithmic discrimination, stereotyping

3. Neglect of novelty


| *The people you need* | *The ones doing it*

|

1. Data scientists

2. Domain specialists

|

1. Predictive churn / default / ... (banks / telco)

2. Predicting crime image:predpol.png[width="100"]

3. Predicting deals image:tilkee.png[width="100"]

4. Predictive maintenance image:cat.jpg[width="100"]

|===

== 2. SUGGEST
//ST: 1. SUGGEST
//ST: !

.Suggest
|===
| *The data you need* | *The hard part*

|

1. A rich dataset and / or historical data on past transactions

2. A feedback mechanism providing data to improve on the suggestion procedure

|

1. Managing serendipity and bubble effects

2. Finding the value proposition which goes beyond the simple “you purchased this, you’ll like that”



| *The people you need* | *The ones doing it*

|

1. Data scientists

2. Domain specialists for insights into the suggestion logic

|

1. Amazon’s product recommendation system image:amazon.jpg[width="100"]

2. Google’s “Related searches…” image:google.jpg[width="100"]

3. Retailer’s personalized recommendations image:auchan.jpg[width="100"]

|===


== 3. CURATE
//ST: 1. CURATE
//ST: !

.Curate
|===
| *The data you need* | *The hard part*

|

1. Dirty (inaccuracies, missing values, bad formatting)

2. Cheap but hard to collect

3. Preferably unstructured

|

1. Slow progress

2. Must maintain continuity

3. Scaling up / right incentives for the workforce

4. Quality control



| *The people you need* | *The ones doing it*

|

Large workforce ("digital labor") to manually inspect the data

Data scientists used to work with crowd sourced data.


|

1. Clarivate Analytics curating metadata from scientific publishing image:clarivate-analytics.png[width="100"]

2. Nielsen and IRI curating and selling retail data image:nielsen.jpg[width="100"] image:iri.jpg[width="100"]

3. ImDB curating and selling movie data image:imdb.jpg[width="100"]

|===


== 4. ENRICH
//ST: 4. ENRICH
//ST: !

.Enrich
|===
| *The data you need* | *The hard part*

|

1. Clean

2. Diverse

|

1. Knowing which cocktail of data is valued by the market

2. Limit replicability

3. Establish legitimacy


| *The people you need* | *The ones doing it*

|

1. Specialists of APIs / data mashups / data integration

2. Possibly: specialists of linked data

3. Domain specialists for market research


|

Selling methods and tools to enrich datasets image:watson.png[width="100"]

Selling aggregated indicators image:edf.jpg[width="100"]

Selling credit scores

|===

== 5. RANK / MATCH / COMPARE
//ST: 5. RANK / MATCH / COMPARE
//ST: !

.Rank / Match / Compare
|===
| *The data you need* | *The hard part*

|

Lots of data:

a. with many features

b. large dispersion values

c. in large volumes

|

1. Finding emergent, implicit attributes

2. Insuring consistency of the ranking

3. Avoid gaming of the system by the users


| *The people you need* | *The ones doing it*

|

1. Data scientists

2. Hacker mentality to imagine how unstructured data can contribute to ranking

3. Domain specialists for quality control


|

1. Search engines ranking results image:google.jpg[width="100"]

2. Yelp, Tripadvisor, etc… which rank places image:tripadvisor.jpg[width="100"]

3. Any system that needs to filter out best quality entities among a crowd of candidates

|===


== 6. SEGMENT / CLASSIFY
//ST: 5. SEGMENT / CLASSIFY
//ST: !

.Segment / classify
|===
| *The data you need* | *The hard part*

|

1. Any dataset, the richer the better

2. A feedback mechanism providing data to improve on the classification procedure

|

1. Evaluating the quality of the comparison

2. Dealing with boundary cases

3. Choosing between a supervised and unsupervised approach (how many categories?)


| *The people you need* | *The ones doing it*

|

1. Data scientists

2. Domain specialists for insights into the classification logic


|

1. Tools for discovery / exploratory analysis by segmentation

2. Diagnostic tools (spam or not? buy, hold or sell? healthy or not?) image:medimsight.png[width="100"]


|===


== 7. GENERATE (experimental!)
//ST: 7. GENERATE (experimental!)
//ST: !

.Generate (experimental!)
|===
| *The data you need* | *The hard part*

|

1. Unstructured data is more challenging but more interesting (pictures, sound, natural language...)

|

1. Should not create a failed product / false expectations

2. Both classic (think of image:clippy.jpg[width="50"]) and frontier science: not sure where it’s going


| *The people you need* | *The ones doing it*

|

1. Data scientists + academics

2. Excellent intrapreneurs to pilote this risky project


|

1. Intelligent BI image:aiden.png[witdth="100"]

2. wit.ai, the chatbot by FB image:wit.png[witdth="100"]

3. Virtual assistants image:cx.jpg[witdth="100"]

4. Image generation image:deepart.png[witdth="100"]


|===

== Combos!
//ST: Combos!
//ST: !

//ST: !

image::data-driven-value-creation.png[align="center", title="Combinations"]
{nbsp} +


== The end
//ST: The end
//ST: !

Find references for this lesson, and other lessons, https://seinecle.github.io/mk99/[here].

image:round_portrait_mini_150.png[align="center", role="right"]
This course is made by Clement Levallois.

Discover my other courses in data / tech for business: http://www.clementlevallois.net

Or get in touch via Twitter: https://www.twitter.com/seinecle[@seinecle]
