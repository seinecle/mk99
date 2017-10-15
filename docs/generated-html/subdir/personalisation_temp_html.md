= Personalization and value creation
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


== 1. From segmentation to personalization
//ST: 1. From segmentation to personalization

//ST: !
Segmentation helps refine the picture from a mass of data to meaningful subgroups of data points.

Why not go down to extreme segmentation: segments the size of an individual?

//ST: !
Major websites do it (Amazon, Yahoo!, Netflix, etc.)
Ads providers do it (Facebook)
News feed do it (Prismatic, Pulse)

//ST: !
Advantages: pinpoint accuracy and relevance
Inconvenient: operational complexity

//ST: !
image::amazon-personalization.png[align="center", title="How is an Amazon page (old version!) personalized"]
{nbsp} +

== 2. Beyond behavior: tracking individual bodies
//ST: 2. Beyond behavior: tracking individual bodies

//ST: !
image::The-relation-between-connected-objects-and-personalization.png[aling="center",title="The relation between connected objects and personalization"]
{nbsp} +

//ST: !
A list of bodily aspects being measured with examples:

//ST: !
.Location
[cols="a,a,a,a,a",options="header"]
|==========================
|Bodily Measurement       |Device         |Company              |Product  |Picture
|Location                 |Mobile phone   |Samsung, Apple, etc. |Phone    |image::gmap-location-history.png[align="center",width=120]
|==========================


//ST: !
.Movement
[cols="a,a,a,a,a",options="header"]
|==========================
|Bodily Measurement       |Device         |Company              |Product     |Picture
|Movement                 |Wrist band     |Nike                 |Fuelband    |image::fuelband.jpg[align="center",width=120]
|==========================

//ST: !
.Gesture
[cols="a,a,a,a,a",options="header"]
|==========================
|Bodily Measurement       |Device         |Company              |Product     |Picture
|Gesture                  |Arm band       |Thalmic Labs         |Myo         |image::myo.png[align="center",width=120]
|==========================

//ST: !
.Weight, heart rate
[cols="a,a,a,a,a",options="header"]
|==========================
|Bodily Measurement       |Device         |Company              |Product              |Picture
|Weight, heart rate               |Body scale     |Nokia                |https://support.health.nokia.com/hc/en-us/categories/200118207-Smart-Body-Analyzer-WS-50-[Smart Body Analyzer]   |image::withings.png[align="center",width=120]
|==========================

//ST: !
.Sleep
[cols="a,a,a,a,a",options="header"]
|==========================
|Bodily Measurement       |Device         |Company              |Product              |Picture
|Sleep                    |Undermat       |Nokia                |https://support.health.nokia.com/hc/en-us/categories/200189426-Withings-Aura[Aura]                 |image::aura.jpg[align="center",width=120]
|==========================

//ST: !
.Fingerprint
[cols="a,a,a,a,a",options="header"]
|==========================
|Bodily Measurement       |Device         |Company              |Product              |Picture
|Fingerprint              |Mobile Phone   |Apple                |iPhone 5             |image::fingerprint.jpg[align="center",width=120]
|==========================

//ST: !
.Facial recognition
[cols="a,a,a,a,a",options="header"]
|==========================
|Bodily Measurement       |Device         |Company              |Product              |Picture
|Facial recognition       |Mobile Phone   |Apple                |iPhone 8             |image::facial-recognition.jpg[align="center",width=120]
|==========================

//ST: !
.Emotions
[cols="a,a,a,a,a",options="header"]
|==========================
|Bodily Measurement       |Device         |Company              |Product              |Picture
|Emotions                 |Camera         |SightCorp            |http://sightcorp.com/crowdsight/[CrowdSight SDK]       |image::crowdsight.png[align="center",width=120]
|==========================

//ST: !
video::7V8jrdH5tAQ[youtube]

//ST: !
.Behavior in public places
[cols="a,a,a,a,a",options="header"]
|==========================
|Bodily Measurement       |Device             |Company                  |Product                          |Picture
|Behavior in public areas |Multiple devices   |AGT International        |https://www.agtinternational.com/analytics/iot-analytics/crowd-analytics/[Mega Events Management Solution]  |image::agt.png[align="center",width=120]
|==========================

//ST: !
image::agt-2.png[align="center", title="source: https://www.agtinternational.com/wp-content/uploads/2014/10/AGT_AAG_MegaEvent-02Oct2014-2.pdf]
{nbsp} +

== 3. The case of Nicholas Felton: constant data monitoring
// 3. The case of Nicholas Felton: constant data monitoring


//ST: !
==== a. The Feltron reports

//ST: !
image::nicholas_felton3.jpg[align="center", title="Nicholas Felton"]
{nbsp} +

//ST: !
http://feltron.com/[Nicholas Felton] is a designer and data artist who produced printed annual reports from 2005 to 2014.

Reports on what?

//ST: !
Reports on his bodily data and social life, which he measures __constantly__

//ST: !
video::145332585[vimeo]

//ST: !
==== b. Not just Feltron

//ST: !
Insurance companies are interested in boosting individual health, using connected objects as monitoring devices

//ST: !
http://www.forbes.com/sites/parmyolson/2014/06/19/wearable-tech-health-insurance/[image:autodesk.jpg[align="center",title="Employee at Autodeck wearing a Jawbone as part of a company challenge"]]

//ST: !
Companies are looking to provide a 360 degree solution to health and well being through constant monitoring:

//ST: !
video::E9jq6XpZjGo[youtube]

//ST: !
Monitoring on health is also a B2B market to achieve "corporate welfare". See link:resources/corporate_wellness_smartdata_nokia.pdf[Nokia's brochure] on the topic.

== 4. Issues, limits
// 4. Issues, limits

//ST: !
These technologies open a vast number of issues: from data privacy to the redefinition of well-being, and the grey boundary between monitoring and surveillance.

//ST: !
A full session of this series is devoted to discussing these issues.

//ST: !
For the moment, let us just repeat cautionary remarks already mentioned in a different session:

//ST: !
==== a. "personalization" has been blamed for reinforcing "bubbles" or "tribes" views of the world (http://pubsonline.informs.org/doi/pdf/10.1287/mnsc.2013.1808[paying version] of the paper, free version https://www.researchgate.net/profile/Kartik_Hosanagar/publication/228233814_Will_the_Global_Village_Fracture_Into_Tribes_Recommender_Systems_and_Their_Effects_on_Consumer_Fragmentation/links/0046352960e0b2e12c000000/Will-the-Global-Village-Fracture-Into-Tribes-Recommender-Systems-and-Their-Effects-on-Consumer-Fragmentation.pdf[here]).

//ST: !
Content personalization is also blamed for favoring political polarization via an "echo chamber effect": social media tend to show me content I already agree with (paying version of the paper http://www.sciencedirect.com/science/article/pii/S0740624X16300375[here], free version https://www.academia.edu/24798528/Political_Polarization_on_Twitter_Implications_for_the_Use_of_Social_Media_in_Digital_Governments?auto=download[here]).

//ST: !
==== b. Personalizing the customer relationship, even when effective, is not inherently a good thing.

//ST: !
It has been shown that the http://www.coca-colacompany.com/stories/summer-of-sharing-share-a-coke-campaign-rolls-out-in-the-us[Coca-Cola #ShareaCoke campaign] is effective at making more children choose a soda with a label to their name, over a healthy drink (paying version of the study http://onlinelibrary.wiley.com/doi/10.1111/ijpo.12193/abstract[here], free version not available).

//ST: !
==== c. Personalization through technology? Companies rated with the best customer service do personalization differently: with humans.

//ST: !
See how Zappos offers a great service to their customers:

video::vApoQPISmvs[youtube]

(https://www.youtube.com/watch?v=IwE1zb9fiVs[another impactful version here])

//ST: !
or see (in French) how https://medium.com/@djo/obsession-service-client-captain-train-cb0b91467fd9[Trainline makes its customers happy].


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
