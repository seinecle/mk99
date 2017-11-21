= Machine learning, data science and artificial intelligence
Clément Levallois <levallois@em-lyon.com>
2017-11-01

last modified: {docdate}

:icons!:
:iconsfont:   font-awesome
:revnumber: 1.0
:example-caption!:

:title-logo-image: EMLyon_logo_corp.png[width="242" align="center"]

[.stretch]
image::EMLyon_logo_corp.png[width="242" align="center"]


==  'Escape' or 'o' to see all sides, F11 for full screen, 's' for speaker notes


==  1. Explaining machine learning in simple terms

==  !
==== a. A comparison with classic statistics

==  !
Let's https://stats.stackexchange.com/questions/6/the-two-cultures-statistics-vs-machine-learning[compare] machine learning to something we would call "regular statistics":

A basic method in statistics is to compute a regression line to identify a trend from a scatter plot.

==  !
To illustrate, we take some data about marketing budgets and sales figures in the corresponding period:

==  !
++++
<iframe width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vS8dKfwxvgz3ALH8Y1FzxWk9lZtiVBlQdZYUrKJqRXNqBFRjKIP3LUvv29QSIBbGx2-ray5nK8cALMH/pubchart?oid=1075418595&format=interactive"></iframe>
++++


==  !
"Regular statistics" enables, among other things:

==  !
1. to find the numerical relation between the 2 series, based on a pre-established formal model (eg, https://en.wikipedia.org/wiki/Ordinary_least_squares[ordinary least squares]).

-> we see that sales are correlated with marketing spendings. It is likely that more marketing spending causes more sales.

==  !
[start=2]
2. to predict, based on this model:

-> by tracing the line further (using the formal model), we can predict the effect of more marketing spending

==  !
"Regular statistics" is advanced by scientists who:

1. are highly skilled in mathematics
==  !

==  !
-> their goal is to find the exact mathematical expression defining the situation at hand, under rigorous conditions

==  !
-> a key approach is *inference*: by defining a *sample of the data* of just the correct size, we can reach conclusions which are valid for the entire dataset.

==  !
[start=2]
2. have no training in computer science / software engineering

-> they neglect how hard it can be to to run their models on computers, in terms of calculations to perform.

-> since they focus on *sampling* the data, they are not concerned with handling entire datasets with related IT issues.

==  !
Machine learning does similar things to statistics, but in a slightly different way:

- there is an emphasis on getting the prediction right, not caring for identifying the underlying mathematical model
- the prediction needs to be achievable in the time available, with the computing resources available
- the data of interest is in a format / in a volume which is not commonly handled by regular statistics package (eg: images, observations with hundreds of features)

==  !
Machine learning is advanced by scientists who are typically:

==  !
[start=1]
1. highly skilled in statistics (the "classic" statistics we have seen above)

==  !
[start=2]
2. with a training or exeprience in computer science, familiar with working with unstructured / big data

==  !
[start=3]
3. working in environments (industry, military, ...) where the operational aspects of the problem are key determinants (unstructured data, limits on computing resources)

==  !
Machine learning puts a premium on techniques which are "computationally adequate":

==  !
- which need the minimum / the simplest algebric operations to run: the best technique is worthless if it's too long or expensive to compute.
- which can be run in such a way that multiple computers work in parallel (simultaneously) to solve it.

==  !
(footnote: so machine learning, in my opinion, shares the spirit of "getting things done" as was https://en.wikipedia.org/wiki/Operations_research#Second_World_War[operations research in  the early days])

==  !
The pursuit of improved models in traditional statistics is not immune to the notion of computational efficiency - it does count as a desirable property - but in machine learning this is largely a pre-requisite.

==  !
==== b. An illustration: the case of GPUs

==  !
A key illustration of the difference between statistics and machine learning can be provided with the use of graphic cards.

==  !
Graphic cards are these electronic boards full of chips found inside a computer, which are used for the display of images and videos on computer screens:

==  !
[.stretch]
image::gpu.jpg[align="center", title="A graphic card sold by NVidia, a leading manufacturer", width="300"]


==  !
In the 1990s, video gaming developed a lot from arcades to desktop computers. Game developers created computer games showing more and more complex scenes and animations. (see https://youtu.be/3UTdxI2IEp0[an evolution of graphics], and https://www.youtube.com/watch?v=Rywkv7PCYDM[advanced graphics games in 2017]).

==  !
These video games need powerful video cards (aka https://en.wikipedia.org/wiki/Graphics_processing_unit[GPUs]) to render complex scenes in full details - with calculations on light effects and animations *made in real time*.

==  !
This pushed for the development of ever more powerful GPUs. Their characteristics is that they can compute simple operations to change pixel colors, *for each of the millions of pixels of the screen in parallel*, so that the next frame of the picture can be rendered in milliseconds.

==  !
Millions of simple operations run in parallel for the price of a GPU (a couple of hundreds of dollars), not the price of dozens of computers running in parallel (can be dozens of thousands of dollars)? This is interesting for computations on big data!

==  !
If a statistical problem for prediction can be broken down into simple operations which can be run on a GPU, then a large dataset can be analyzed in seconds or minutes on a laptop, instead of  cluster of computers.

==  !
To illustrate the difference in speed between a mathematical operation run without / with a GPU:

==  !
video::-P28LKWTzrI[youtube, width= 500, height=400]

==  !
The issue is: to use a GPU for calculations, you need to conceptualize the problem at hand as one that can be:

- broken into a very large series
- of very simple operations (basically, sums or multiplications, nothing complex like square roots or polynomials)
- which can run independently from each other.

==  !
Machine learning tyically pays attention to this dimension of the problem right from the design phase of models and techniques, where statistics would typically not consider the issue, or only downstream: not at the design phase but at the implementation phase.

==  !
Now that we have seen how statistics and machine learning differ in their approach, we still need to understand how does machine learning get good results, if it does not rely on modelling / sampling the data like statistics does?


Machine learning can be categorized in 3 families of tricks:

==  2. Three families of machine learning


==  !
==== a. The *unsupervised* learning approach

==  !
This designates all the methods which take a fresh dataset and find interesting patterns in it, *without training on previous, similar datasets*.

==  !
The analogy is with a person doing a task for the first time:

-> she learns a new thing by applying clever heuristics, without having been training on the task before.

==  !
Example: in your wedding, how to sit people with similar interests at the same tables?

==  !
The set up:

- a list of 100 guests, and 3 tastes you know they have for each of them
- 10 tables with 10 sits each.

==  !
- a measure of similarity between 2 guests: 2 guests have similarity of 0% if they share 0 tastes, 33% if they share 1 taste, 66% with 2 tastes in common, 100% with three matching interests.

==  !
- a measure of similarity at the level of a table: the sum of similarities between all pairs of guests at the table (45 pairs possible for a table of 10).

==  !
A possible solution using an unsupervised approach:

==  !
- on a computer, assign randomly the 100 guests to the 10 tables.

==  !
- for each table:
** measure the degree of similarity of tastes for the table
** exchange the sit of 1 person at this table, with the sit of a person at a different table.
** measure again the degree of similarity for the table: if it improves, keep the new sits, if not, revert to before the exchange

And repeat for all tables, many times, until no exchange of sits improves the similarity. When this stage is achieved, we say the model has "*converged*".

==  !
[.stretch]
image::kmeans.jpg[align=center, title="K-means, an unsupervised learning approach", width= 300]


==  !
==== b. The *supervised* learning approach

==  !
Take 50,000 or more observations, or data points, like:

**an image of a cat, with the caption "cat"

**an image of a dog, with the caption "dog"

**another image of a cat, with the caption "cat"

etc....

==  !
- you need 50,000 observations of this kind, or more! It is called the *training set*
- this is also called a *labelled dataset*, meaning that we have a label describing each of the observation.

==  !
The task is: if we give our computer a new image of a cat without a label, will it be able to guess the label "cat"?

==  !
The method:

- take a list of random coefficients (in practice, the list is a vector, or a matrix)

==  !
- for each of the 50,000 pictures of dogs and cats:
** apply the coefficients to the picture at hand (let's say we have a dog here)
** If the result is "dog", do nothing, it works!
** If the result is "cat", change slightly the coefficients.
** move to the next picture

==  !
- After looping through 50,000 pictures the parameters have hopefully adjusted and fine tuned. This was the *training of the model*.

==  !
Now, when you get new pictures (the *fresh set*), applying the trained model should output a correct prediction ("cat" or "dog").

==  !
Supervised learning is currently the most popular family of machine learning.

==  !
[.stretch]
image::muffin.jpg[align=center, title="A hard test case for supervised learning", width=400]


==  !
It is called *supervised* learning because the learning is very much constrained / supervised by the intensive training performed:

-> there is limited or no "unsupervised discovery" of novelty.

==  !
video::4HCE1P-m1l8[youtube, width=500, height=400]

==  !
Important take away on the supervised approach:

- *collecting __large__ datasets for training is key*. Without these data, no supervised learning.
- supervised learning is not good at analyzing situations entirely different from what is in the training set.


==  !
==== c. The *reinforcement* learning approach

==  !
To understand reinforcement learning in an intuitive sense, we can think of how animals can learn quickly by *ignoring* undesirable behavior and rewarding desirable behavior.

This is easy and takes just seconds. The following video shows B.F. Skinner, main figure in psychology in the 1950s-1970s:

==  !
video::TtfQlkGwE2U[youtube, width=500, height=400]

==  !
Footnote: how does this apply to learning in humans? On the topic of learning and decision making, I warmly recommend https://global.oup.com/academic/product/foundations-of-neuroeconomic-analysis-9780199744251?cc=us&lang=en&[this book by Paul Glimcher], professor of neuroscience, psychology and economics at NYU:

(this is a very hard book to read as it covers three disciplines in depth. The biological mechanisms of decision making it describes can be inspiring to design new computanional approaches.)

==  !
[.stretch]
image::glimcher.jpg[align="center",title="Foundations of Neuroeconomics, Paul Glimcher, 2010", width="250"]


==  !
Besides pigeons, reinforcement learning can be applied to any kind of "expert agents".

Take the case of a video game like Super Mario Bros:

==  !
[.stretch]
image::mario.jpg[align="center",title="Mario Bros, a popular video game"]



==  !
Struture of the game / the task:

- Goal of the task: Mario should collect gold coins and complete the game by reaching the far right of the screen.
- Negative outcome to be avoided: Mario getting killed by ennemies or falling in holes.

==  !
- Starting point: Mario Bros is standing at the beginning of the game, doing nothing.
- Possible actions: move right, jump, stand & do nothing, shoot ahead.


==  !
Reinforcement learning works by:

1. Making Mario do a new random action ("try something"), for example: "move right"
2. The game ends (Mario moved right, gets hit by a ennemy)

==  !
[start=3]
3. This result is stored somewhere:
** move right = good (progress towards the goal of the game)
** walking close to an ennemy and getting hit by it = bad

==  !
[start=4]
4. Game starts over (back to step 1) with a a combination of
** continue doing actions recorded as positive
** try something new (jump, shoot?) when close to a situation associated with a negative outcome

==  !
After looping from 1. to 4. thousands of times, Mario completes the game, without any human player:

==  !
video::qv6UVOQ0F44[youtube, width=500, height=400]

==  !
Reinforcement learning is perceived as corresponding to an important side of human learning / human intelligence (goal oriented, "trial and error").


==  !
==== d. When is machine learning useful?

==  !
Using machine learning can be a waste of resource, when well known statistics could be easily applied.

==  !
Hints that "classic" statistical modelling (maybe as simple as a linear regression) should be enough:

==  !
- The dataset is not large (below 50k observations), supervised learning is not going to work
- The data is perfectly structured (tabular data)
- The data points have few features

==  !
Cases when "classic" statistics modelling is *necessary*:

- The question is about the relative contribution of independent variables to the determination of an outcome

==  3. Machine Learning and Data Science

==  !
Machine learning is a step in the longer chain of steps of data science.

==  !
The process was formalized as https://en.wikipedia.org/wiki/Data_mining#Process[kdd]: "Knowledge Discovery in Databases":

==  !
[.stretch]
image::kdd.png[align="center", title="KDD - knowledge discovery in databases", width=500]


==  !
More recent representations of the steps in data processing have been suggested, making room for the role of data visualization (see the lecture on the topic):

-> see https://image.slidesharecdn.com/datavisualizationforbusiness-141017095602-conversion-gate01/95/data-visualization-for-business-13-638.jpg?cb=1414060400[the version by Ben Fry] (http://benfry.com/phd/[source]) and this one by Moritz Stefaner:

==  !
[.stretch]
image::stefaner.png[align="center", title="data visualization workflow by Moritz Stefaner", width=500]


(http://blogger.ghostweather.com/2013/11/data-vis-consulting-advice-for-newbies.html[source])

==  !
Machine learning is one of the techniques (along with traditional statistics) that intervenes at the step of "Data mining".

==  !
What makes data scientists important is that the steps of this kdd are highly interdependent.

==  !
You need indviduals or teams who are not just versed in data mining:

-> because the shape of the data at the collection stage has a huge influence on the kind of techniques, and the kind of software, that can be used to discover knowledge.

==  !
The skills of a data scientist are often represented as the meeting of three separate domains:

==  !
[.stretch]
image::conway.png[align="center", title="The Venn diagram of what is a data scientist"]


source: http://drewconway.com/zia/2013/3/26/the-data-science-venn-diagram

==  4. Artificial intelligence

==  !
==== a. Weak vs Strong AI

==  !
Weak AI designates computer programs able to outperform humans at complex tasks with a narrow focus (playing chess)

==  !
Weak AI is typically the result of applying expert systems or machine learning techniques seen above.

==  !
Strong AI is an intelligence that would be general in scope, able to set its own goal, and conscious of itself. Nothing is close to that yet.

==  !
So AI is a synonymous with weak AI at the moment.

==  !
==== b. Two videos to understand AI further

==  !
Laurent Alexandre on the social and economic stakes of AI (in French):

==  !
video::rJowm24piM4[youtube, width= 500, height=400]

==  !
John Launchbury, the Director of DARPA's Information Innovation Office (I2O) in 2017:

==  !
video::-O01G3tSYpU[youtube, width= 500, height=400]

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
