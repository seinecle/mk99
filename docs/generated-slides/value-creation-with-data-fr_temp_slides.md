= Seven roads to data-driven value creation
== !
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
Ceci n'est ni une liste exhaustive, ni une recette!
Ce sont plutôt des pistes de réflexion sur la façon dont la donnée contribue à réaliser un service à valeur ajoutée.
====

== 1. Prédire
== !
[.stretch]
image::prediction.jpg[pdfwidth="25%", align="center",title="prediction"]
== !


==== a. Entreprises qui créent des services sur cette base
== !
1. Prédire les délits image:predpol.png[pdfwidth="100", width="100", book="keep"]
2. Prédire qu'un deal va se faire image:tilkee.png[pdfwidth="100", width="100", book="keep"]
3. Maintenance prédictive image:cat.jpg[pdfwidth="100", width="100", book="keep"]

== !
==== b. Le rôle de la prédiction dans une plateforme
== !

La prédiction permet de fournir un meilleur service au client final et d'optimiser les coûts de transaction.

C'est un facteur clé de succès des plateformes car ce faisant, elles peuvent battre les marchés et organisations existantes sur le coût et la qualité.

1. Uber prédit à quelle minute votre taxi arrive, tout en assurant un service où les offreurs et demandeurs sont dispersés et non coordonnés.
2. Booking prédit le meilleur prix pour une chambre, malgré la diversité des chaînes d'hôtel
3. Amazon prédit une gestion de stocks optimale, malgré la diversité des fournisseurs

== !
==== c. Obstacles et difficultés
== !
1. Le https://indatalabs.com/blog/data-science/cold-start-problem-in-recommender-systems[((cold start problem))]
2. Risque de manquer la ((long tail)), ((algorithmic discrimination)), ((stereotyping))
3. Négligence de la nouveauté radicale

== 2. Suggérer
== !
[.stretch]
image::suggestion.jpg[pdfwidth="25%", align="center"]
== !


==== a. Entreprises qui créent des services sur cette base
== !
1. Amazon’s product recommendation system image:amazon.jpg[pdfwidth="100", width="100", book="keep"]
2. Google’s “Related searches…” image:google.jpg[pdfwidth="100", width="100", book="keep"]
3. Les recommendations de produits personnalisées sur les tickets de caisse image:auchan.jpg[pdfwidth="100", width="100", book="keep"]

== !
==== c. Le rôle de la suggestion dans une plateforme
== !

La suggestion permet aux utilisateurs finaux d'explorer la richesse du catalogue d'offre.
Cela vient donc améliorer la coordination des acteurs en abaissant les coûts de découverte / d'être découvert.

1. Amazon fait des suggestions de produits, ce qui met en avant la richesse du catalogue
2. Booking suggère des hôtels similaires sur les mêmes zones, à critères comparables


== !
==== b. Obstacles et difficultés
== !
1. Le ((cold start problem)), gérer la https://doi.org/10.1016/j.knosys.2016.08.014[((sérendipité))] et les http://wwwconference.org/proceedings/www2014/proceedings/p677.pdf[((effets de bulle))].


== 3. Curation
== !
[.stretch]
image::curation.jpg[pdfwidth="25%", align="center"]
== !


==== a. Entreprises qui créent des services sur cette base
== !

Il est intéressant de noter que *tous les exemples suivants sont proches d'un modèle de plateforme*, ce qui indique que la curation serait au coeur de la notion de plateforme.

1. ((Clarivate Analytics)) curating metadata(((data, data curation))) from scientific publishing image:crv_logo_rgb_rev.png[pdfwidth="100", width="100", book="keep"]
2. ((Nielsen)) and IRI curating and selling retail data image:nielsen.jpg[width="100"] image:iri.jpg[pdfwidth="100", width="100", book="keep"]
3. ImDB curating and selling movie data image:imdb.jpg[pdfwidth="100", width="100", book="keep"]
4. NomadList providing practical info on global cities for nomad workers image:nomadlist.jpg[pdfwidth="100", width="100", book="keep"]

== !
==== b. Obstacles et difficultés
== !
1. Progrès lent : la curation demande d'organiser un travail sur tâches simples. Les plateformes de crowd working fournissent ce service.
2.La continuité peut être essentielle : rater un jour, mois ou année de collecte et curation de donnée peut faire baisser la valeur de tout le reste du jeu de données.
3. Contrôle qualité


== 4. Enrichissement
== !
[.stretch]
image::enrich.jpg[pdfwidth="25%", align="center",width="500"]
== !


==== a. Entreprises qui créent des services sur cette base
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
4. https://deepart.io/[Image generation] image:deepart.png[pdfwidth="100", width="100", book="keep"](((image generation)))

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

image:round_portrait_mini_150.png[align="center", role="right"]
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
