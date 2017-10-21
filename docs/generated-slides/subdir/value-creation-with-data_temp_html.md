= 7 roads to data-driven value creation
Clément Levallois <levallois@em-lyon.com>
2017-09-10

last modified: {docdate}

:icons!:
:iconsfont:   font-awesome
:revnumber: 1.0
:example-caption!:
:sourcedir: ../../../main/java

:title-logo-image: EMLyon_logo_corp.png[align="center"]

image::EMLyon_logo_corp.png[align="center"]
{nbsp} +

//ST: 'Escape' or 'o' to see all sides, F11 for full screen, 's' for speaker notes


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

image::enrich.jpg[align="center",width="500"]
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

image::rank.jpg[align="center",width="500"]
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

image::muffin.jpg[align="center",width="500"]
{nbsp} +

//ST: !
==== Segmenting / classifying: The ones doing it

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

[cols="a"]
|===

|1. Intelligent BI https://www.aiden.ai/[image:aiden.png[width="100"]]

|2. wit.ai, the chatbot by FB https://wit.ai/[image:wit.png[width="100"]]

|3. Virtual assistants https://www.cxcompany.com/digitalcx/[image:cx.jpg[width="100"]]

|4. Image generation https://deepart.io/[image:deepart.png[width="100"]]

|5. Close-to-real-life speech synthesis https://deepmind.com/blog/wavenet-generative-model-raw-audio/[image:google.jpg[width="100"]]

|===

[cols="a,a"]
|===
|6. Generating realistic car models from a few parameters: https://www.autodeskresearch.com/publications/exploring_generative_3d_shapes[image:autodesk.png[width="100", title="Autodesk"]]

|===

//ST: !
A video on the generation of car models:

//ST: !
video::25xQs0Hs1z0[youtube]

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
