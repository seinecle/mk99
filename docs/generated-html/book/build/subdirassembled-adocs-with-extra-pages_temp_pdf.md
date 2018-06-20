= Topics in Data Science for business: Volume 1 - Fundamentals
Clément Levallois <levallois@em-lyon.com>
v1.0, April 2018
:icons!:
:iconsfont:   font-awesome
:revnumber: 1.0
:example-caption!:
:sourcedir: ../../../main/java
= Preface

== A textbook for managers

The target reader for this book is a manager who needs to clearly understand what "data science", "big data", "artificial intelligence" so that they can:

- *leverage* these technologies to improve the efficiency of  their existing business,
- *innovate* with new products and services and develop new business guidelines

The promise of this book is to bring you from a starting point with no knowledge of these technical concepts, to a point where you understand the concepts *and* you can develop "data centric" business projects: when "data" contributes to creating value for the customer and all stakeholders.


=== Is this textbook too technical or too easy for me?

If you are unsure, try this simple test: http://bit.ly/essentials-1-test

-> There are 20 topics you should be comfortable answering. See how you score. If the score is low, you should read first the introductory volume to this series:

"Essentials of data science for managers: Volume 1, from big data to APIs"



<<<

= Machine learning, data science and artificial intelligence

== 1. Explaining machine learning in simple terms

=== a. A comparison with classic statistics

Let's https://stats.stackexchange.com/questions/6/the-two-cultures-statistics-vs-machine-learning[compare] machine learning to something we would call "regular statistics":

A basic method in statistics is to compute a regression line to identify a trend from a scatter plot.

To illustrate, we take some data about marketing budgets and sales figures in the corresponding period:


image::regression-line.png[align="center", title="A linear regression"]
{nbsp} +

"Regular statistics" enables, among other things:

1. to find the numerical relation between the 2 series, based on a pre-established formal model (eg, https://en.wikipedia.org/wiki/Ordinary_least_squares[ordinary least squares]).

-> we see that sales are correlated with marketing spendings. It is likely that more marketing spending causes more sales.

[start=2]
2. to predict, based on this model:

-> by tracing the line further (using the formal model), we can predict the effect of more marketing spending

"Regular statistics" is advanced by scientists who:

1. are highly skilled in mathematics

-> their goal is to find the exact mathematical expression defining the situation at hand, under rigorous conditions

-> a key approach is *inference*: by defining a *sample of the data* of just the correct size, we can reach conclusions which are valid for the entire dataset.

[start=2]
2. have no training in computer science / software engineering

-> they neglect how hard it can be to to run their models on computers, in terms of calculations to perform.

-> since they focus on *sampling* the data, they are not concerned with handling entire datasets with related IT issues.

Machine learning does similar things to statistics, but in a slightly different way:

- there is an emphasis on getting the prediction right, not caring for identifying the underlying mathematical model
- the prediction needs to be achievable in the time available, with the computing resources available
- the data of interest is in a format / in a volume which is not commonly handled by regular statistics package (eg: images, observations with hundreds of features)

Machine learning is advanced by scientists who are typically:

[start=1]
1. highly skilled in statistics (the "classic" statistics we have seen above)

[start=2]
2. with a training or exeprience in computer science, familiar with working with unstructured / big data

[start=3]
3. working in environments (industry, military, ...) where the operational aspects of the problem are key determinants (unstructured data, limits on computing resources)

Machine learning puts a premium on techniques which are "computationally adequate":

- which need the minimum / the simplest algebric operations to run: the best technique is worthless if it's too long or expensive to compute.
- which can be run in such a way that multiple computers work in parallel (simultaneously) to solve it.

(footnote: so machine learning, in my opinion, shares the spirit of "getting things done" as was https://en.wikipedia.org/wiki/Operations_research#Second_World_War[operations research in  the early days])

The pursuit of improved models in traditional statistics is not immune to the notion of computational efficiency - it does count as a desirable property - but in machine learning this is largely a pre-requisite.

=== b. An illustration: the case of GPUs

A key illustration of the difference between statistics and machine learning can be provided with the use of graphic cards.

Graphic cards are these electronic boards full of chips found inside a computer, which are used for the display of images and videos on computer screens:

image::gpu.jpg[align="center", title="A graphic card sold by NVidia, a leading manufacturer", width="300"]
{nbsp} +

In the 1990s, video gaming developed a lot from arcades to desktop computers. Game developers created computer games showing more and more complex scenes and animations. (see https://youtu.be/3UTdxI2IEp0[an evolution of graphics], and https://www.youtube.com/watch?v=Rywkv7PCYDM[advanced graphics games in 2017]).

These video games need powerful video cards (aka https://en.wikipedia.org/wiki/Graphics_processing_unit[GPUs]) to render complex scenes in full details - with calculations on light effects and animations *made in real time*.

This pushed for the development of ever more powerful GPUs. Their characteristics is that they can compute simple operations to change pixel colors, *for each of the millions of pixels of the screen in parallel*, so that the next frame of the picture can be rendered in milliseconds.

Millions of simple operations run in parallel for the price of a GPU (a couple of hundreds of dollars), not the price of dozens of computers running in parallel (can be dozens of thousands of dollars)? This is interesting for computations on big data!

If a statistical problem for prediction can be broken down into simple operations which can be run on a GPU, then a large dataset can be analyzed in seconds or minutes on a laptop, instead of  cluster of computers.

To illustrate the difference in speed between a mathematical operation run without / with a GPU:

video::-P28LKWTzrI[youtube, width= 500, height=400]

The issue is: to use a GPU for calculations, you need to conceptualize the problem at hand as one that can be:

- broken into a very large series
- of very simple operations (basically, sums or multiplications, nothing complex like square roots or polynomials)
- which can run independently from each other.

Machine learning tyically pays attention to this dimension of the problem right from the design phase of models and techniques, where statistics would typically not consider the issue, or only downstream: not at the design phase but at the implementation phase.

Now that we have seen how statistics and machine learning differ in their approach, we still need to understand how does machine learning get good results, if it does not rely on modelling / sampling the data like statistics does?


Machine learning can be categorized in 3 families of tricks:

== 2. Three families of machine learning


=== a. The *unsupervised* learning approach

This designates all the methods which take a fresh dataset and find interesting patterns in it, *without training on previous, similar datasets*.

The analogy is with a person doing a task for the first time:

-> she learns a new thing by applying clever heuristics, without having been training on the task before.

Example: in your wedding, how to sit people with similar interests at the same tables?

The set up:

- a list of 100 guests, and 3 tastes you know they have for each of them
- 10 tables with 10 sits each.

- a measure of similarity between 2 guests: 2 guests have similarity of 0% if they share 0 tastes, 33% if they share 1 taste, 66% with 2 tastes in common, 100% with three matching interests.

- a measure of similarity at the level of a table: the sum of similarities between all pairs of guests at the table (45 pairs possible for a table of 10).

A possible solution using an unsupervised approach:

- on a computer, assign randomly the 100 guests to the 10 tables.

- for each table:
** measure the degree of similarity of tastes for the table
** exchange the sit of 1 person at this table, with the sit of a person at a different table.
** measure again the degree of similarity for the table: if it improves, keep the new sits, if not, revert to before the exchange

And repeat for all tables, many times, until no exchange of sits improves the similarity. When this stage is achieved, we say the model has "*converged*".

image::kmeans.jpg[align="center", title="K-means, an unsupervised learning approach", width= 300]
{nbsp} +

=== b. The *supervised* learning approach

Take 50,000 or more observations, or data points, like:

**an image of a cat, with the caption "cat"

**an image of a dog, with the caption "dog"

**another image of a cat, with the caption "cat"

etc....

- you need 50,000 observations of this kind, or more! It is called the *training set*
- this is also called a *labelled dataset*, meaning that we have a label describing each of the observation.

The task is: if we give our computer a new image of a cat without a label, will it be able to guess the label "cat"?

The method:

- take a list of random coefficients (in practice, the list is a vector, or a matrix)

- for each of the 50,000 pictures of dogs and cats:
** apply the coefficients to the picture at hand (let's say we have a dog here)
** If the result is "dog", do nothing, it works!
** If the result is "cat", change slightly the coefficients.
** move to the next picture

- After looping through 50,000 pictures the parameters have hopefully adjusted and fine tuned. This was the *training of the model*.

Now, when you get new pictures (the *fresh set*), applying the trained model should output a correct prediction ("cat" or "dog").

Supervised learning is currently the most popular family of machine learning.

image::muffin.jpg[align="center", title="A hard test case for supervised learning", width=400]
{nbsp} +

It is called *supervised* learning because the learning is very much constrained / supervised by the intensive training performed:

-> there is limited or no "unsupervised discovery" of novelty.

video::4HCE1P-m1l8[youtube, width=500, height=400]

Important take away on the supervised approach:

- *collecting __large__ datasets for training is key*. Without these data, no supervised learning.
- supervised learning is not good at analyzing situations entirely different from what is in the training set.


=== c. The *reinforcement* learning approach

To understand reinforcement learning in an intuitive sense, we can think of how animals can learn quickly by *ignoring* undesirable behavior and rewarding desirable behavior.

This is easy and takes just seconds. The following video shows B.F. Skinner, main figure in psychology in the 1950s-1970s:

video::TtfQlkGwE2U[youtube, width=500, height=400]

Footnote: how does this apply to learning in humans? On the topic of learning and decision making, I warmly recommend https://global.oup.com/academic/product/foundations-of-neuroeconomic-analysis-9780199744251?cc=us&lang=en&[this book by Paul Glimcher], professor of neuroscience, psychology and economics at NYU:

(this is a very hard book to read as it covers three disciplines in depth. The biological mechanisms of decision making it describes can be inspiring to design new computanional approaches.)

image::glimcher.jpg[align="center",title="Foundations of Neuroeconomics, Paul Glimcher, 2010", width="250"]
{nbsp} +

Besides pigeons, reinforcement learning can be applied to any kind of "expert agents".

Take the case of a video game like Super Mario Bros:

image::mario.jpg[align="center",title="Mario Bros, a popular video game"]
{nbsp} +


Struture of the game / the task:

- Goal of the task: Mario should collect gold coins and complete the game by reaching the far right of the screen.
- Negative outcome to be avoided: Mario getting killed by ennemies or falling in holes.

- Starting point: Mario Bros is standing at the beginning of the game, doing nothing.
- Possible actions: move right, jump, stand & do nothing, shoot ahead.


Reinforcement learning works by:

1. Making Mario do a new random action ("try something"), for example: "move right"
2. The game ends (Mario moved right, gets hit by a ennemy)

[start=3]
3. This result is stored somewhere:
** move right = good (progress towards the goal of the game)
** walking close to an ennemy and getting hit by it = bad

[start=4]
4. Game starts over (back to step 1) with a a combination of
** continue doing actions recorded as positive
** try something new (jump, shoot?) when close to a situation associated with a negative outcome

After looping from 1. to 4. thousands of times, Mario completes the game, without any human player:

video::qv6UVOQ0F44[youtube, width=500, height=400]

Reinforcement learning is perceived as corresponding to an important side of human learning / human intelligence (goal oriented, "trial and error").


=== d. When is machine learning useful?

Using machine learning can be a waste of resource, when well known statistics could be easily applied.

Hints that "classic" statistical modelling (maybe as simple as a linear regression) should be enough:

- The dataset is not large (below 50k observations), supervised learning is not going to work
- The data is perfectly structured (tabular data)
- The data points have few features

Cases when "classic" statistics modelling is *necessary*:

- The question is about the relative contribution of independent variables to the determination of an outcome

== 3. Machine Learning and Data Science

Machine learning is a step in the longer chain of steps of data science.

The process was formalized as https://en.wikipedia.org/wiki/Data_mining#Process[kdd]: "Knowledge Discovery in Databases":

image::kdd.png[align="center", title="KDD - knowledge discovery in databases", width=500]
{nbsp} +

More recent representations of the steps in data processing have been suggested, making room for the role of data visualization (see the lecture on the topic):

-> see https://image.slidesharecdn.com/datavisualizationforbusiness-141017095602-conversion-gate01/95/data-visualization-for-business-13-638.jpg?cb=1414060400[the version by Ben Fry] (http://benfry.com/phd/[source]) and this one by Moritz Stefaner:

image::stefaner.png[align="center", title="data visualization workflow by Moritz Stefaner", width=500]
{nbsp} +

(http://blogger.ghostweather.com/2013/11/data-vis-consulting-advice-for-newbies.html[source])

Machine learning is one of the techniques (along with traditional statistics) that intervenes at the step of "Data mining".

What makes data scientists important is that the steps of this kdd are highly interdependent.

You need indviduals or teams who are not just versed in data mining:

-> because the shape of the data at the collection stage has a huge influence on the kind of techniques, and the kind of software, that can be used to discover knowledge.

The skills of a data scientist are often represented as the meeting of three separate domains:

image::conway.png[align="center", title="The Venn diagram of what is a data scientist"]
{nbsp} +

source: http://drewconway.com/zia/2013/3/26/the-data-science-venn-diagram

== 4. Artificial intelligence

=== a. Weak vs Strong AI

Weak AI designates computer programs able to outperform humans at complex tasks with a narrow focus (playing chess)

Weak AI is typically the result of applying expert systems or machine learning techniques seen above.

Strong AI is an intelligence that would be general in scope, able to set its own goal, and conscious of itself. Nothing is close to that yet.

So AI is a synonymous with weak AI at the moment.

=== b. Two videos to understand AI further

Laurent Alexandre on the social and economic stakes of AI (in French):

video::rJowm24piM4[youtube, width= 500, height=400]

John Launchbury, the Director of DARPA's Information Innovation Office (I2O) in 2017:

video::-O01G3tSYpU[youtube, width= 500, height=400]


<<<

= 7 roads to data-driven value creation

== 7 roads to data-driven value creation

[IMPORTANT]
===
Not a closed list, not a recipe!

Rather, these are essential building blocks for a strategy of value creation based on data.
===

== 1. PREDICT

image::prediction.jpg[align="center"]
{nbsp} +

=== Prediction: The ones doing it

|===

1. Predictive churn / default / ... (banks / telco)

2. Predicting crime image:predpol.png[width="100"]

3. Predicting deals image:tilkee.png[width="100"]

4. Predictive maintenance image:cat.jpg[width="100"]

|===

=== Prediction: the hard part


|===

1. Collecting data (https://indatalabs.com/blog/data-science/cold-start-problem-in-recommender-systems[cold start problem])

2. Risk missing the long tail, algorithmic discrimination, stereotyping

3. Neglect of novelty
|===


== 2. SUGGEST

image::suggestion.jpg[align="center"]
{nbsp} +

=== Suggestion: The ones doing it

|===


1. Amazon’s product recommendation system image:amazon.jpg[width="100"]

2. Google’s “Related searches…” image:google.jpg[width="100"]

3. Retailer’s personalized recommendations image:auchan.jpg[width="100"]

|===

=== Suggestion: the hard part

|===

1. The https://indatalabs.com/blog/data-science/cold-start-problem-in-recommender-systems[cold start problem], managing serendipity (see review: https://doi.org/10.1016/j.knosys.2016.08.014[paying version], free version not available) and "filter bubble" effects (review: https://doi.org/10.1145/2566486.2568012[paying version], http://wwwconference.org/proceedings/www2014/proceedings/p677.pdf[free version here]).

2. Finding the value proposition which goes beyond the simple “you purchased this, you’ll like that”

|===


== 3. CURATE

image::curation.jpg[align="center"]
{nbsp} +

=== Curation: The ones doing it

|===

1. Clarivate Analytics curating metadata from scientific publishing image:crv_logo_rgb_rev.png[width="100"]

2. Nielsen and IRI curating and selling retail data image:nielsen.jpg[width="100"] image:iri.jpg[width="100"]

3. ImDB curating and selling movie data image:imdb.jpg[width="100"]

|===

=== Curation: the hard part

|===

1. Slow progress: curation needs human labor to insure high accuracy, it does not scale the way a computerized process would.

2. Must maintain continuity: missing a single year or month hurts the value of the overall dataset disproportionally.

3. Scaling up / right incentives for the workforce: the workforce doing the curation should be paid fairly, which is https://www.wired.com/story/amazons-turker-crowd-has-had-enough/[not the case yet].

4. Quality control

|===


== 4. ENRICH

image::enrich.jpg[align="center",width="500"]
{nbsp} +

=== Enrichment: The ones doing it

|===

1. Selling methods and tools to enrich datasets image:watson.png[width="100"]

2. Selling aggregated indicators image:edf.jpg[width="100"]

3. Selling credit scores

|===

=== Enrichment: the hard part

|===

1. Knowing which cocktail of data is valued by the market

2. Limit replicability

3. Establish legitimacy

|===


== 5. RANK / MATCH / COMPARE

image::rank.jpg[align="center",width="500"]
{nbsp} +

=== Ranking / matching / comparing: The ones doing it

|===

1. Search engines ranking results image:google.jpg[width="100"]

2. Yelp, Tripadvisor, etc… which rank places image:tripadvisor.jpg[width="100"]

3. Any system that needs to filter out best quality entities among a crowd of candidates

|===

=== Ranking / matching / comparing: the hard part

|===

1. Finding emergent, implicit attributes (imagine: if you rank things based on just one public feature: not interesting nor valuable)

2. Insuring consistency of the ranking (many rankings are less straightforward than they appear)

3. Avoid gaming of the system by the users (for instance, http://www.nytimes.com/2011/02/13/business/13search.html[companies try to play Google's ranking of search results at their advantage])

|===


== 6. SEGMENT / CLASSIFY

image::muffin.jpg[align="center",width="500"]
{nbsp} +

=== Segmenting / classifying: The ones doing it

|===

1. Tools for discovery / exploratory analysis by segmentation

2. Diagnostic tools (spam or not? buy, hold or sell? healthy or not?) image:medimsight.png[width="100"]

|===

=== Segmenting / classifying: the hard part

|===

1. Evaluating the quality of the comparison

2. Dealing with boundary cases

3. Choosing between a pre-determined number of segments (like in the k-means) or letting the number of segments emerge

|===


== 7. GENERATE / SYNTHETIZE(experimental!)

image::generate.jpg[align="center"]
{nbsp} +

=== Generating: The ones doing it

(click on the logos to get to the relevant web page)


[cols="a"]
|===

|[start=1]
1. Intelligent BI with https://www.aiden.ai/[Aiden] image:aiden.png[width="100"]

|[start=2]
2. https://wit.ai/[wit.ai], the chatbot by FB image:wit.png[width="100"]

|[start=3]
3. https://www.cxcompany.com/digitalcx/[Virtual assistants] image:cx.jpg[width="100"]

|[start=4]
4. https://deepart.io/[Image generation] image:deepart.png[width="100"]

|[start=5]
5. Close-to-real-life https://deepmind.com/blog/wavenet-generative-model-raw-audio/[speech synthesis] image:google.jpg[width="100"]

|===

[cols="a"]
|===
|[start=6]
6. Generating realistic car models from a few parameters by https://www.autodeskresearch.com/publications/exploring_generative_3d_shapes[Autodesk]: image:autodesk.png[width="100", title="Autodesk"]

|===

A video on the generation of car models by Autodesk:

video::25xQs0Hs1z0[youtube]

=== Generating: the hard part

|===

1. Should not create a failed product / false expectations

2. Both classic (think of image:clippy.jpg[width="50"]) and frontier science: not sure where it’s going

|===


== Combos!


image::data-driven-value-creation.png[align="center", title="Combinations"]
{nbsp} +



<<<


[Index]
= Index


image::datacenter.jpg[align="center",title="A data center"]
{nbsp} +

Look at this video showing a tour of a data center at Google:

video::XZmGGAbHqa0[youtube]

Usually, until 2005 roughly, companies had two options:

- buying their own servers and using them on their premises (at their location).
- paying the services of companies specializing in managing data centers.

Then the "cloud" changed this.

== 2. The cloud

The term "cloud" was made popular by Amazon with their service “Amazon Elastic Compute Cloud” (Amazon EC2) launched in 2006.

This service was new in many ways:

- you can rent servers owned by Amazon, at a distance, when you need them, for a duration that you choose.

- there is an emphasis on ease of use: no need to know the technical details of these servers (how they are plugged, how they are configured…)

- you are just given a login + password and you can start using these servers for your needs.

- it's "elastic": if you need more servers, or more powerful servers, it's just possible. No need for signing a new contract or to evaluate whether Amazon has the capacity... it's dimensioned to be possible.

Let's compare a situation with or without the cloud:


[width="100%"]
|=====
|*Without the cloud* |*With the cloud*
|You make a market study for which server to buy


Get the approval by your finance department to buy it (that’s a fixed asset!)

Wait for the server to ship

Install it and configure it

Maintain it (security, etc.)

When the job is over: what do you do with your server? That’s a sunk cost.

If the job happens to need more computing capacity than your server offers: you are stuck with your too-small-server!

|On https://aws.amazon.com/ec2/?nc1=h_ls[Amazon’ EC2 website], you click to choose a server among those on offer: it is *on demand*

You run your job on it. Costs are metered precisely.

When your job is over, you stop the server with a click and pay the bill.

If the job happens to need more computing capacity, you switch to a bigger server with a single click, or it can be done for you automatically: it is *elastic*.
|It is a capex|It is an opex
|=====

The cloud can fit in the budget as an operational expense instead of a capital expenditure.
Opex are not inherently a better or cheaper option than a capex, but they are easier for a project team or business unit to fit in their budget.
See http://gevaperry.typepad.com/main/2009/01/accounting-for-clouds-stop-saying-capex-vs-opex.html[this blog post], especially the critical comments below the post, to continue this discussion.

== 3. IaaS, PaaS, Saas ... ??



What a company can do with the cloud?

They can use it to run elementary operations, up to more complex ones:


*Infrastructure as a service* (IaaS)

You use servers in the cloud for basic capabilities like storing data, or computing operations.


*Platform as a Service* (Paas)

The cloud is used to provide building blocks of a service: to manage a messenging system, to host apps, ...


*Software as a Service* (Saas)

The cloud is used to host a full software accessible "on demand" through the browser: like Google Drive, https://www.d2l.com/products/learning-environment/[Brightspace] or https://www.salesforce.com/fr/?ir=1[SalesForce].

== 4. Private or public cloud? Hybrid cloud?

- Amazon EC2 is an example of a *public cloud*: it is publicly accessible to any customer. Of course, this does not mean that every customer can see what the others are doing on the cloud! Each customer have their private spaces on the cloud.


- Many companies have security requirements which prevent them from accessing public clouds.
They need to have their servers on premises.
In this case, they can build their own *private cloud*: it is a cloud just like Amazon EC2, except that it is owned, managed and used by the company exclusively - it is not accessible to third parties.
But even private, it keeps the basic characteristics of a cloud: on-demand and elastic in particular.

- *Hybrid clouds* are a variety of private clouds: it is a private cloud where some forms of operations can be delegated to a public cloud.
For example, operations which are not security sensitive and which need a capacity of computing in excess of what the private cloud of the company can provide.



<<<

= The headache of data integration

== 1. Data: you don't get in on tap


A naive vision of data would get that it's all fluid. Don't we talk about "data streams"?
Working with data would be as simple as opening a tap and "getting customer data", for instance.


image::tap.jpg[align="center", title="Data streams, as fluid as water on tap?"]
{nbsp} +


Actually, data is more like a complex patchwork: many different pieces which must be stiched together - and this is hard.


image::patchwork.jpg[align="center", title="Data streams make a patchwork"]
{nbsp} +


Take customer data.

It is not a given. Instead, this is a design made of multiple primary data sources:


image::Multiple-sources-of-customer-data.png[align="center", title="Multiple sources of customer data"]
{nbsp} +

> Analysts often spend 50-80% of their time preparing and transforming data sets before they begin more formal analysis work.

Garrett Grolemund, http://shop.oreilly.com/product/0636920035992.do[Data Scientist and Master Instructor at RStudio]



Take away: Data is fragmented by nature. It comes from different sources and presented in different formats.
*You* (the marketer in collaboration with data scientists) wrangle to __construct__ customer profiles by joining and assembling different sources of data into a meaningful synthesis.


(if you are interested, data scientists actually have whole books on the subject of wrangling with the mess of different data sources)

image::wrangling.jpg[align="center", title="Data wrangling"]
{nbsp} +


== 2. Sources of fragmentation


=== a. Channels keep diversifying


Point of sale, print, TV, radio, outdoor posters, mobile apps, mobile sites, emails, SMS, APIs, social networks, search engines, e-commerce platforms, e-commerce websites, blogs, content channels, …

-> all these channels can provide relevant data.


=== b. Connections between these channels intensify and complexify


- Social TV is TV delivered with Internet services,

- User profiles created on one platform are imported on another


- Orders taken online can be picked up on a variety of point of sales

- Ads circulating through one channel replicate on other channels, ...


-> It is very complex to trace the "customer journey" on all these channels and to keep an updated view of a customer profile.

It is even more difficult to explore causality (which action on which channel caused which subsequent action by the user?)


=== c. Underlying technologies fragment and keep evolving, across channels


Browsers, Cookies, APIs, mobile OS (Android or iOS?), etc... All these different techs evolve and need continuous effort and expertise to integrate.


Example: *did you notice* that on a mobile device, the url of the pages you visit can now start with an https://www.ampproject.org/latest/blog/whats-in-an-amp-url/[AMP url]?

Like, to visit the page of the New York Times the url should be http://www.nyt.com but it looks like: *http://google.com/amp/www.nyt.com*

This *http://google.com/amp* prefix is a new tech by Google to accelerate the display of web pages on mobiles. Fine.
But then, as a marketing data analyst, how to count visits to:


http://google.com/amp/www.nyt.com

and

http://www.nyt.com/etc

-> It is important to count visits to these two urls as a visit *to the same page*.


In Sept 2017 major services of web data analytics were http://searchengineland.com/google-amp-cache-unified-users-analytics-282069[still struggling with this issue].

This illustrates that to just count visits to a web page (something which should be classic and robust) and integrate this data to a larger analysis, big issues can arise and be hard to fix even in 2017, because of the evolution of techs and standards.


=== d. In the meantime, customers have growing expectations about the quality of service


Difficulties posed by data integration do not slow or decrease customers expectations.
To the contrary, we see an elevation of expectations.
Customers increasingly expect:

- realtime contact
- two-ways interaction (they want to be able to voice their opinion, and get a response)
- seamless experience (no glitch, modern UI, consistence of the UX across channels)
- personalized experience (customization of the message they receive)


=== e. Example: A French bank going through the 2010s


image::Before---a-couple-of-data-sources-across-a-few-channels.png[align="center", title="Before - a couple of data sources across a few channels"]
{nbsp} +


image::Now---many-data-sources-across-a-variety-of-channels.png[align="center", title="Now - many data sources across a variety of channels"]
{nbsp} +



== 3. Tools for data integration: DMPs and more


=== a. Data Management Platform (DMP)


In 2015/2016 a new acronym started to trend: "DMP", standing for *"Data Management Platform"*.

Basically a DMP is an information system dedicated to solving the issues of data integration:


- it can store a large amount of data
- it can receive data from a variety of sources, in a variety of formats


- it offers functions to reconcile records from different data sources and generate a unique identifier for each reconciled entry.
- it offers segmentation / classification functions


- it provides security and analytics capabilities on the data
- it makes this data available for execution by other software.


=== b. DMP in relation to other components of the information system


DMPs are relatively new. They integrate with 3 other information systems in the firm:


- CRM (Customer Relationship Management)
** This is the software *gathering* data related to customers and sales. It is a major source of *input data* for a DMP.


- ERP (Enterprise Resource Planning)
** Large software synchronizing information systems from finance, sales, logistics and more. The CRM can be independent or part of the ERP.


- DSP (Demand Side Platform)
** https://digiday.com/media/wtf-demand-side-platform/[piece of software automatizing ad buying]. So, the audiences identified in the DMP could be served corresponding ads automatically with a DSP.


How can data circulate across these software and with the external world? The next lesson is devoted to APIs, another important concept.

== Reading list
Find the reading list for this chapter on Pinterest:
https://fr.pinterest.com/seinecle/what-is-the-cloud/



<<<

= APIs and their business relevance

== 1. Definition of API

API: acronym for "Application Programming Interface"

An API is the way to make software programs “easy to plug and share” with other programs.

Ok so... APIs are a cable? A computer? A USB connection? No.

An API is simply a group of rules (you can also call it a convention, or an agreement...) which programmers follow when writing the part of their code which is in charge of communicating with other software.

These rules are then published (on a webpage for example), so that anyone who needs to connect to the program can learn what rules to follow.
That's it.

So, an API is simply a way to write code to make it easy to interface with other programs?
Yes.

Why the fuss then?

Having conventions on how to write a software so that somebody can plug it to its own software is one thing.
APIs of this sort are a https://dzone.com/articles/how-design-good-regular-api[classic topic in computer science] but we are not concerned with this here.

APIs we are going to discuss are about communication between distant computers, in a business context.

Let's do a bit of history:

== 2. The origin of APIs

Companies which need to exchange data is nothing new.
Manufacturers, retailers, banks, ... they need to exchange information at regular interval.

Sending invoices, receiving receipts for merchandise, and many other administrative records generated in the course of business.

These receipts, invoices... can be printed and mailed (this solution still exists of course).

With informatics developing in the 1970s and 1980s, a new system emerged: the exchange of information via computers: https://en.wikipedia.org/wiki/Electronic_data_interchange[Electronic Data Interchange] (EDI)

=== a. EDI: Electronic Data Interchange

EDI is not an exchange of file attachments in emails or via a file transfer on a website, because emails and websites did not exist yet! (emails and the Web were adopted by firms in the late 1990s).

Instead, exchanging data via EDI consisted in using complex electronic tools (like the fax but even more complicated) because:

- each industry has its own protocol to exchange data (one protocol for logistics, one for payments, one for this or that retailer chain, etc.)
- you need a dedicated device or software for each EDI protocol, and these are not given for free

- EDI protocols can vary from one country to another
- EDI protocols are controlled by industry associations which do not adopt innovation quickly

and finally, EDI protocols created "closed systems": a company A can connect to company B via an EDI only if the two have a pre-agreement to use this EDI.

So EDIs are fragmented, complicated to implement, slow to evolve, not cheap and restricts the communication to a "club" of partners who agreed to use it.

EDIs still exist, especially in large B2B industries like transportation (http://cerasis.com/2014/12/11/edi-in-transportation/[check here]), but it lost in popularity in the wider economy because...  APIs have arrived.

=== b. The emergence of web APIs

In the late 1990s and early 2000s, Internet and the World Wide Web expanded a lot.

More and more servers in different parts of the world needed to be interfaced with each other to exchange data.

It became increasingly convenient to define simple and universal conventions that everyone could learn and follow to standardize these exchanges, for free and easily.

That's what *web APIs* do. They are also often called:

- "*API*" for short
- "*web services*"
- "*REST* API" (see below for that last one).

A web API extends the logic of the APIs we have seen in the beginning of this document, to software communicating via the web.

To recall, an API is a convention followed when writing a software, making this software available to other software.

NOTE:: Example: the API of Microsoft PowerPoint enables the import of Excel tables in pptx documents, because the API of Powerpoint plugs to the API of Excel. In this example Excel and Powerpoint are suposed to be installed on the same computer of course!

*Web* APIs are APIs which enable two pieces of software to communicate, via Internet. *They don't need to be installed on the same computer.*

=== c. The benefits of a web API compared to an EDI

Unlike EDI, web APIs drop any industry-specific concern. Web APIs are just a convention to send and receive data over the Internet, without any saying on the content of the data.

The data sent and received can be invoices, webpages, train schedules, audio, video... whatever.

Contrary to EDIs, a company creating a web API can choose to leave its access open (remember that EDIs need the two parties to have a pre-established agreement).

So that a potential client interested in using the web API of a company can set it up in a couple of clicks, instead of waiting weeks or months before a contract is signed and the EDI is setup.

WARNING:: Saying that APIs are open does not mean an absence of security: communication through APIs can easily be identified and encrypted, as needed.

=== d. REST API?

Two popular web API conventions emerged in the 1990s and competed for popularity:

- SOAP (https://en.wikipedia.org/wiki/SOAP[Simple Object Access Protocol])
- REST (https://en.wikipedia.org/wiki/Representational_state_transfer[Representational State Transfer])

REST became ultimately the most widely adopted, because it uses the same simple principles that webpages use to be transferred over the Internet (the "http" protocol that you see in web page addresses).
This is why APIs are often called https://www.youtube.com/watch?v=7YcW25PHnAA["REST APIs"].

In 2000-2010, it became increasingly easy and natural to adopt the REST convention to make one's software and data available to another computer.
This simple evolution to ease interoperability had *immense effects*:

== 3. Business consequences of APIs
=== a. APIs *opened* software to the world

An API transforms a closed software into something that can be plugged to anything other computer or object, as long as it is connected to the Internet.

For instance, APIs were a key factor of success for https://en.wikipedia.org/wiki/Salesforce.com[SalesForce] in the early 2000s. SalesForce, created in 1999, has a revenue of US$8.39 billion in 2017:

- SalesForce developed a CRM as a SaaS where features of the CRM were *exposed as APIs* (meaning, these features could be plugged to external apps via the REST protocol).

- SalesForce created a PaaS to host apps that could plug to the SalesForce CRM via the APIs developed by SalesForce.

This platform is called https://www.salesforce.com/products/platform/products/force/[Force.com] and external developers can put their apps there, as long as they are compatible with the SalesForce API.

SalesForce takes a commission on the sales made by these third party apps hosted on Force.com, but more importantly, the platform creates an *ecosystem* of apps and developers around the SalesForce products which makes it hard for a customer company to switch to a different product.

=== b. APIs *accelerated* software innovation


Thanks to API it became easy to add software blocks together and create new apps, even if the app developers where from different countries, industries, or big and small. https://medium.freecodecamp.org/how-i-replicated-an-86-million-project-in-57-lines-of-code-277031330ee9[Check this amazing story].

=== c. APIs *opened* data

Companies and public organization own many datasets of great business interest.
The use of these datasets can be free (for small projects and NGOs) or monetized if the user is an entreprise.

Without APIs, datasets can be made publicly available as docs (eg, Excel spreadsheets) to download but this is not practical (try downloading something like `all_train_schedules_2000_to_2017.xls` ! 😓).

So, imagine a transportation company like French SNCF which finds it interesting to publish station names, train schedules, etc. because it could be used by other companies to build new services : how can it do it?

The data is on a server of SNCF. Then SNCF adds https://data.sncf.com/api/en[an API and its documentation], making the data available to anyone who knows about REST APIs (and https://youtu.be/7YcW25PHnAA[this is trivial]).

Entrepreneurs and programmers in general will be able to access the data via the API and use it, possibly to create new services based on this train information.

== 4. The ecosystem of APIs
=== a. A wealth of APIs

To discover new APIs, or to make your APIs easier to discover, the most well known place is the website "Programmable Web": https://www.programmableweb.com/

Searching on this website, you will find APIs ranging from the most https://www.programmableweb.com/api/coca-cola-enterprises[business-y] use case, to APIs of a https://www.programmableweb.com/api/itsthisforthat[more fun and odd sort].


Still, many APIs are not listed on this website, and a google search for "info I need + API" is also a good way to find if the API you'd need exists. Interested in whale sightings? http://hotline.whalemuseum.org/api[There is an API for that].


=== b. APIs: a business world of its own

APIs have become central to the economy. As a result, a large number of services associated to APIs have developed to cater for all the needs of companies that use them.

How to create an API, how to manage the documentation of a large number of APIs, how to connect a wide variety of APIs, how to manage the security of APIs, how to monetize and API...

-> Many large firms and startups now specialize in all these different issues.
Here is the 2017 landscape of the main companies active in the API industry:

image::api-landscape-2017.jpg[align="center", title="The API landscape in 2017"]
{nbsp} +


<<<

= Essential notions on privacy and data protection

== 1. Privacy: just one aspect of data protection

image::Defining-data-protection.png[align="center", title="Defining data protection"]
{nbsp} +

== 2. When is personal information considered "data"?

At the most basic level, anything could count as "data" with possibly a personal character to it, including comments written about somebody in a personal notbook.

In practice, "data" starts to to be considered as such when:

This is information capable of being processed *automatically*

-> Hint: data on computers, not unstructured written notes

*Or* information intended to be processed automatically

-> Hint: paper records to be fed in a computer (eg, via scanning), not any pile of paper on your desk.

Or *structured information* that can be used to facilitate the retrieval of specific information on specific individuals

-> Hint: paper records, filing systems, databases

== 3. Personal data matters because of privacy

[quote, CNIL (French Independent Administrative Authority),https://www.cnil.fr/en/personal-data-definition]
____
Personal data are any anonymous data that can be double checked to identify a specific individual (e.g. fingerprints, DNA, or information such as “the son of the doctor living at 11 Belleville St. in Montpellier does not perform well at school”).
____

Personal data is data that an individual has the right to keep private. *How and why is privacy an issue*?

Privacy is mentioned in the Article 12 of the http://www.un.org/en/universal-declaration-human-rights/index.html[1948 Universal Declaration of Human Rights]:

[quote,Universal Declaration of Human Rights]
____
No one shall be subjected to arbitrary interference with his privacy, family, home or correspondence, nor to attacks upon his honor and reputation. Everyone has the right to the protection of the law against such interference or attacks.
____

This article from the Declaration is found in similar forms in most of the conventions on human rights in the world.

This right to privacy enables individuals to define their identity in relation to the world, by giving each individual the power to control what to keep for themselves, and what to reveal / share with the world.

In 2005, a report on https://books.google.fr/books?id=yeVRrrJw-zAC&pg=PA1&dq=right+to+privacy+tel+aviv&hl=en&ei=T0IhTaWhEI-msQOizMWZCg&sa=X&oi=book_result&ct=result&redir_esc=y#v=onepage&q=right%20to%20privacy%20tel%20aviv&f=false[Privacy in the Digital Environment] by the Haifa Center of Law & Technology develops:

____
The right to privacy is our right to keep a domain around us, which includes all those things that are part of us, such as our body, home, property, thoughts, feelings, secrets and identity.
____

____
The right to privacy gives us the ability to choose which parts in this domain can be accessed by others, and to control the extent, manner and timing of the use of those parts we choose to disclose.
____

In addition to shaping an individual's own personal sphere and identity, privacy also underpins the development of a relation between the individual and the society she is part of:

-> when an individual's privacy is secured, they don't have to fear that their personal opinions and activities (as simple as reading a newspaper) will endanger them as citizens.

-> this gives liberty to individuals to develop political expressions which do not necessarily conform with the power structure in place. This would be much harder if everyone's political opinions could not be kept private.

== 4. Evolution of privacy

Privacy is a social norm which transforms as societies evolve. Since the 2000s, a couple of tendencies can be identified:

- increasing tracking of the digital traces left by individuals by companies which use these traces for ad targeting and data reselling

- increasing state surveillance through digital means, against security threats and unspecified goals.

- broader public acceptance of new forms of violations to privacy.

For example, https://en.wikipedia.org/wiki/Reality_television[TV shows] where participants are filmed 24/24 and where they reveal their (real or supposed) intimacy, dates back only from the late 1990s.

[link=http://www.imdb.com/title/tt0120382/]
image::truman.jpg[align="center", title="The Truman Show, 1998"]
{nbsp} +

== 5. Privacy of the consumer and privacy of citizens: the relations between the two

Thanks to whistleblowers like https://en.wikipedia.org/wiki/Edward_Snowden[Edward Snowden], the extent of privacy breaches by governmental agencies is now better known:

video::108771171[vimeo]

Journalists, academics, activists and NGOs such as the https://www.eff.org/[Electronic Frontier Foundation] make the case that:

- consumers are insufficiently aware and sensitive of how much information is captured in the normal conduct of their lives, just by using mobile phones and apps, web browsing, and increasingly in public places.

- citizens are insufficiently aware and sensitive of the breach of their privacy by security agencies of their own country of residence, and by other countries.

Many citizens consider that if they don't break the law, then they have "nothing to hide".

Similarly, consumers might find that bargaining their private data against a free service and some targeted ads, is a good deal.


Sociologist of technology http://technosociology.org/[Zeynep Tufekci] goes further:

Her argument is that besides "surveillance" and "lack of privacy", companies like Google and Facebook developing a business model based on ad targeting by analytics on personal data, design a *persuasion architecture* which can be used / highjacked for political purposes.

Tufeckci does not argue that Google, Facebook or the likes inherently have anti-democratic purposes, but that:

- they develop of an information architecture which has the potential to shape opinions of crowds,
- they do so without transparency

- some past experiments on voting in the US, and current developments on electronic surveillance in China, show that the power of these technologies has already consequences in the real world.


https://www.ted.com/talks/zeynep_tufekci_we_re_building_a_dystopia_just_to_make_people_click_on_ads[link to the TEDx conference by Zeynep Tufekci]
{empty} +


== 6. Conclusion: data protection in business, more than an regulatory obligation

The collection and treatment of personal data by businesses has far reaching implication, and should not be considered merely from a legal standpoint by firms.

The topic engages the https://en.wikipedia.org/wiki/Corporate_social_responsibility[Corporate social responsibility] of the firm.

The nature of the business model itself - profiling consumers in the most specific way - has profound consequences on the design of the environment surrounding individuals.

What are the next steps? Several trends can be identified:

1. some voices question the business model: are personalized ads based on personal data as effective as the market valuation of Facebook suggests? How much is just scam? Some voices warn against the extent of the fraud, as the video below shows (see also https://digiday.com/media/ft-warns-advertisers-discovering-high-levels-of-domain-spoofing/[here], or https://digiday.com/media/ft-warns-advertisers-discovering-high-levels-of-domain-spoofing/[here]):

video::oVfHeWTKjag[youtube]

[start=2]
2. legislation by political authorities to protect the public interest, especially via an obligation for transparency, in the face of more personal data being collected, for a larger variety of purposes. See our related lecture on the GDPR.

[start=3]
3. a deepening of the current model with more personal data being collected, in private spaces (homes) and behavior in relation to the public (crowd management in streets, stadiums, etc.):

image::amazon-echo.jpg[align="center",title= "Echo Alexa, a home assistant collecting personal data"]
{nbsp} +



<<<


[Index]
= Index
