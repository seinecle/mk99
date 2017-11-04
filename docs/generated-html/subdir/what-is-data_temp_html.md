= What is data?
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
{nbsp} +

//ST: 'Escape' or 'o' to see all sides, F11 for full screen, 's' for speaker notes

== 1. Definition of data
//ST: 1. Definition of data
//ST: !

The English term "data" (1654) originates from “datum”, a Latin word for "a given".footnote:[http://www.etymonline.com/index.php?term=data]
"Data" is a single factual, a single entity, a single point of matter.

//ST: !
Using the word "data" to mean "transmittable and storable computer information" was first done in 1946.
The expression "data processing" was first used in 1954.footnote:[http://www.etymonline.com/index.php?term=data]

//ST: !
=====
Thoughts: the etymology suggests that data is "a given". Can you question this?
=====

//ST: !
Data represents either a single entity, or a collection of such entitities ("data points").
We can speak also of datasets instead of data (so a dataset is a collection of data points).

== 2. Examples!
//ST: 2. Examples!
//ST: !


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

//ST: !


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
//ST: 3. Three take aways from the examples
//ST: !

==== a. Think about data in a broad sense
//ST: !

Data is not just text and figures. You should train in thinking about data in a broader sense:

- pictures are data
- language is data (including slang, lip movements, etc.)

//ST: !
- relations are data (you know individual A, you know individual B, but the relationship between A and B is data as well)
- preferences, emotional states... are data
- etc. There is no definitive list, you should train yourself looking at buisness situations and think: "where is the data?"

//ST: !

==== b. metadata is data, too
//ST: !

Metadata: this is some data describing some other data.

Example:
----
The bibliographical reference <1>
describing
a book <2>
----
<1> the metadata
<2> the data

//ST: !

-> Data without metadata can be worthless (imagine a library without a library catalogue)

-> Metadata can be informative in its own right, as shown with the NSA scandal: footnote:[http://www.newyorker.com/news/news-desk/whats-the-matter-with-metadata]

image:metadata.png["The trouble with metadata"]

//ST: !
==== c. zoom in, zoom out
//ST: !

We should remember considering that a data point can be itself a collection of data points:

- a person walking into a building is a data point.
- however this person is itself a collection of data points: location data + network relations + subscriber status to services + etc.

So it is a good habit to wonder whether a data point can in fact be "unbundled" (spread into smaller data points / measurements)

== 4. Some essential vocabulary to discuss data
//ST: 4. Some essential vocabulary to discuss data

//ST: !
==== a. Formats, types, encoding
//ST: !


//ST: !

image:tweet.png[width="500" align="center"]

//ST: !
- This is a digital *medium* (because it's on screen as opposed to analogic, if we had printed the pic on paper)
- The *type* of the data is textual + image

//ST: !
- The text is *formatted* in plain text (meaning, no special formatting), as opposed to more structured data-interchange formats (https://codingislove.com/json-tutorial-indepth/[check json or xml]).
- The *encoding* of the text is UTF-8. Encoding has to do with the issue: how to represent alphabets and signs from different languages in text? (not even mentioning emojis?). UTF-8 is an encoding which is one of the most universal.

//ST: !
- The tweet is part of a list of tweets. The list represents the *data structure* of my dataset, it is the way my data is organized. There are many alternative data structures: arrays, sets, dics, maps...
- The tweet is stored as a picture (png file) on my hard disk. "png" is the *file format*. The data is *persisted* as a file on disk (could have been stored in a database instead).


//ST: !
==== b. Data presented as a table
//ST: !

image::table.png[table]
{nbsp} +
{nbsp} +

//ST: !
==== c. Data according to who owns it

//ST: !
- First party data: the data generated through the activities of your own organization.
Your organization own it, which does not mean that consent from users is not required, when it comes to personal data.

//ST: !
- Second party data: the data accessed through partnerships.
Without being the generator nor the owner of this data, partners make it available to you through an agreement.

//ST: !
- Third party data: the data acquired via purchase
This data is acquired through a market transaction. Its uses still comes with conditions, especially for personal data.

//ST: !
==== d. Data: "sociodemo" or "behavior"?

//ST: !
- Sociodemogaphic or "sociodemio" data refers to information about individuals, describing fundamental attributes of their social identity: age, gender, place of residence, occupation, marital status and number of kids.

//ST: !
- Behavior data refers to any digital trace left by the individual in the course of it life: clicks on web pages, likes on Facebook, purchase transactions, comments posted on Tripadvisor...

//ST: !
Sociodemo data is typically well structured or easy to structure. It has a long history of collection and analysis, basically since census exists.

//ST: !
Behavior data allows to go further than sociodemo data: each individual can be characterized by its acts and tastes, well beyond what an age or marital status could define.

But behavior data is typically not well structured and harder to collect.


== 5. Finally: data and size
//ST: 5. data and size
//ST: !

image:russian_dolls.jpg[Data sizes]

//ST: !


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

//ST: !

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
