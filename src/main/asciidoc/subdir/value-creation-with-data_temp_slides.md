= Seven roads to data-driven value creation
Clément Levallois <levallois@em-lyon.com>
2017-09-10

last modified: {docdate}

:icons!:
:iconsfont:   font-awesome
:revnumber: 1.0
:example-caption!:

:title-logo-image: EMLyon_logo_corp.png[align="center"]

== !
[.stretch]
image::EMLyon_logo_corp.png[align="center"]
== !


//ST: 'Escape' or 'o' to see all sides, F11 for full screen, 's' for speaker notes

[TIP]
====
Not a closed list, not a recipe!
Rather, these are essential building blocks for a strategy of value creation based on data.
====

== 1. Predict
== !
[.stretch]
image::prediction.jpg[pdfwidth="25%", align="center",title="prediction"]
== !


==== a. Examples of companies
== !
1. Predicting crime image:predpol.png[pdfwidth="100", width="100", book="keep"]
2. Predicting deals image:tilkee.png[pdfwidth="100", width="100", book="keep"]
3. Predictive maintenance image:cat.jpg[pdfwidth="100", width="100", book="keep"]

== !
==== b. Obstacles and difficulties
== !
1. The https://indatalabs.com/blog/data-science/cold-start-problem-in-recommender-systems[((cold start problem))]
2. Risk missing the ((long tail)), ((algorithmic discrimination)), ((stereotyping))
3. Neglect of novelty

== 2. Suggest
== !
[.stretch]
image::suggestion.jpg[pdfwidth="25%", align="center"]
== !


==== a. Examples of companies
== !
1. Amazon’s product recommendation system image:amazon.jpg[pdfwidth="100", width="100", book="keep"]
2. Google’s “Related searches…” image:google.jpg[pdfwidth="100", width="100", book="keep"]
3. Retailer’s personalized recommendations image:auchan.jpg[pdfwidth="100", width="100", book="keep"]

== !
==== b. Obstacles and difficulties
== !
1. The ((cold start problem)), managing https://doi.org/10.1016/j.knosys.2016.08.014[((serendipity))] and http://wwwconference.org/proceedings/www2014/proceedings/p677.pdf[((filter bubble effects))].
2. Finding the ((value proposition)) which goes beyond the simple “you purchased this, you’ll like that”

== 3. Curate
== !
[.stretch]
image::curation.jpg[pdfwidth="25%", align="center"]
== !


==== a. Examples of companies
== !
1. ((Clarivate Analytics)) curating metadata (((data, data curation))) from scientific publishing image:crv_logo_rgb_rev.png[pdfwidth="100", width="100", book="keep"]
2. ((Nielsen)) and IRI curating and selling retail data image:nielsen.jpg[width="100"] image:iri.jpg[pdfwidth="100", width="100", book="keep"]
3. ImDB curating and selling movie data image:imdb.jpg[pdfwidth="100", width="100", book="keep"]
4. NomadList providing practical info on global cities for nomad workers image:nomadlist.jpg[pdfwidth="100", width="100", book="keep"]

== !
==== b. Obstacles and difficulties
== !
1. Slow progress: curation needs ((human labor)) to insure high accuracy, it does not scale the way a computerized process would.
2. Must maintain continuity: missing a single year or month hurts the value of the overall dataset.
3. Scaling up / right incentives for the workforce: https://www.wired.com/story/amazons-turker-crowd-has-had-enough/[the workforce doing the digital labor of curation should be paid fairly], which is not the case yet.
4. Quality control


== 4. Enrich
== !
[.stretch]
image::enrich.jpg[pdfwidth="25%", align="center",width="500"]
== !


==== Examples of companies
== !
1. Selling methods and tools to enrich datasets image:watson.png[pdfwidth="100", width="100", book="keep"]
2. Selling aggregated indicators image:edf.jpg[pdfwidth="100", width="100", book="keep"]
3. Selling credit scores

== !
==== Obstacles and difficulties
== !
1. Knowing which cocktail of data is valued by the market
2. Limit duplicability
3. Establish legitimacy

== 5. Rank / match / compare
== !
[.stretch]
image::rank.jpg[pdfwidth="25%", align="center",width="500"]
== !


==== Examples of companies
== !
1. Search engines ranking results image:google.jpg[pdfwidth="100", width="100", book="keep"]
2. Yelp, Tripadvisor, etc… which rank places image:tripadvisor.jpg[pdfwidth="100", width="100", book="keep"]
3. Any system that needs to filter out best quality entities among a crowd of candidates

== !
==== Obstacles and difficulties
== !
1. Finding emergent, implicit attributes (imagine: if you rank things based on just one public feature: not interesting nor valuable)
2. Insuring consistency of the ranking (many rankings are less straightforward than they appear)
3. Avoid gaming of the system by the users (for instance, http://www.nytimes.com/2011/02/13/business/13search.html[companies try to play Google's ranking of search results at their advantage])

== 6. Segment / classify
== !
[.stretch]
image::muffin.jpg[pdfwidth="25%", align="center",width="500"]
== !


==== Examples of companies
== !
1. Tools for discovery / exploratory analysis by ((segmentation))
2. Diagnostic tools (spam or not? buy, hold or sell? healthy or not?) image:medimsight.png[pdfwidth="100", width="100", book="keep"]

== !
==== Obstacles and difficulties
== !
1. Evaluating the quality of the comparison
2. Dealing with boundary cases
3. Choosing between a pre-determined number of segments (like in the k-means) or letting the number of segments emerge

== 7. Generate / synthesize (experimental!)
== !
[.stretch]
image::generate.jpg[pdfwidth="25%", align="center"]
== !


==== Examples of companies
== !
1. Intelligent BI with https://www.aiden.ai/[Aiden] image:aiden.png[pdfwidth="100", width="100", book="keep"]
2. https://wit.ai/[wit.ai], the ((chatbot)) by FB image:wit.png[pdfwidth="100", width="100", book="keep"]

== !
3. https://www.cxcompany.com/digitalcx/[Virtual assistants] image:cx.jpg[pdfwidth="100", width="100", book="keep"]
4. https://deepart.io/[Image generation] image:deepart.png[pdfwidth="100", width="100", book="keep"] (((image generation)))

== !
5. Close-to-real-life https://deepmind.com/blog/wavenet-generative-model-raw-audio/[((speech synthesis))] image:google.jpg[pdfwidth="100", width="100", book="keep"]
6. Generating realistic car models from a few parameters by https://www.autodeskresearch.com/publications/exploring_generative_3d_shapes[Autodesk]: image:autodesk.png[pdfwidth="100", width="100", title="Autodesk", book="keep"]


== !
A video on the generation of car models by Autodesk:

== !
[.stretch]
video::25xQs0Hs1z0[youtube]
== !

==== Obstacles and difficulties
== !
1. Should not create a failed product / false expectations
2. Both classic (think of image:clippy.jpg[pdfwidth="50", width="50", book="keep"]) and frontier science: not sure where it’s going

== Combos
== !


== !
[.stretch]
image::Combinations.png[align="center", "title="Combinations"]
== !




== The end
== !
Find references for this lesson, and other lessons, https://seinecle.github.io/mk99/[here].

image:round_portrait_mini_150.png[align="center", role="right"][align="center", role="right"]
This course is made by Clement Levallois.

Discover my other courses in data / tech for business: https://www.clementlevallois.net

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
