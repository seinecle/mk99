= Machine learning, data science, and artificial intelligence
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


== 1. Explaining machine learning in simple terms
//ST: 1. Explaining machine learning in simple terms

//ST: !
==== a. A comparison with classic statistics

//ST: !
Let's https://stats.stackexchange.com/questions/6/the-two-cultures-statistics-vs-machine-learning[compare] machine learning to something we would call "regular statistics":

A basic method in statistics is to compute a regression line to identify a trend from a scatter plot.

//ST: !
To illustrate, we take some data about marketing budgets and sales figures in the corresponding period:

//ST: !

image::regression-line.png[align="center", title="A linear regression"]
{nbsp} +

//ST: !
"Regular statistics" enables, among other things:

//ST: !
1. to find the numerical relation between the 2 series, based on a pre-established formal model (eg, https://en.wikipedia.org/wiki/Ordinary_least_squares[ordinary least squares]).

-> we see that sales are correlated with marketing spendings. It is likely that more marketing spending causes more sales.

//ST: !
[start=2]
2. to predict, based on this model:

-> by tracing the line further (using the formal model), we can predict the effect of more marketing spending

//ST: !
"Regular statistics" is advanced by scientists who:

1. are highly skilled in mathematics
//ST: !

//ST: !
-> their goal is to find the exact mathematical expression defining the situation at hand, under rigorous conditions

//ST: !
-> a key approach is *inference*: by defining a *sample of the data* of just the correct size, we can reach conclusions which are valid for the entire dataset.

//ST: !
[start=2]
2. have no training in computer science / software engineering

-> they neglect how hard it can be to to run their models on computers, in terms of calculations to perform.
-> since they focus on *sampling* the data, they are not concerned with handling entire datasets with related IT issues.

//ST: !
Machine learning does similar things to statistics, but in a slightly different way:

- there is an emphasis on getting the prediction right, not caring for identifying the underlying mathematical model
- the prediction needs to be achievable in the time available, with the computing resources available
- the data of interest is in a format / in a volume which is not commonly handled by regular statistics package (eg: images, Terabytes)

//ST: !
Machine learning is advanced by scientists who are typically:

- highly skilled in mathematics
- able to work with computer scientists, to take their constraints into account
- working in environments (industry, military, ...) where the operational aspects of the problem are key determinants (unstructured data, limits on computing resources)

//ST: !
(footnote: so machine learning, in my opinion, shares the spirit of "getting things done" as was https://en.wikipedia.org/wiki/Operations_research#Second_World_War[operations research in  the early days])

//ST: !
How does machine learning works, if it does not rely on modelling / sampling the data?

With 3 families of tricks:

//ST: !
==== b. The *unsupervised* learning approach

//ST: !
This designates all the methods which take a fresh dataset and find interesting patterns in it, *without training on previous, similar datasets*.

//ST: !
The analogy is with a person doing a task for the first time:

-> she learns a new thing by applying clever heuristics, without having been training on the task before.

//ST: !
Example: in your wedding, how to sit people with similar interests at the same tables?

//ST: !
The set up:

- a list of 100 guests, and 3 tastes you know they have for each of them
- 10 tables with 10 sits each.

//ST: !
- a measure of similarity between 2 guests: 2 guests have similarity of 0% if they share 0 tastes, 33% if they share 1 taste, 66% with 2 tastes in common, 100% with three matching interests.

//ST: !
- a measure of similarity at the level of a table: the sum of similarities between all pairs of guests at the table (45 pairs possible for a table of 10).

//ST: !
A possible solution using an unsupervised approach:

//ST: !
- on a computer, assign randomly the 100 guests to the 10 tables.

//ST: !
- for each table:
** measure the degree of similarity of tastes for the table
** exchange the sit of 1 person at this table, with the sit of a person at a different table.
** measure again the degree of similarity for the table: if it improves, keep the new sits, if not, revert to before the exchange

And repeat for all tables, many times, until no exchange of sits improves the similarity. When this stage is achieved, we say the model has "*converged*".

//ST: !
image::kmeans.jpg[align=center, title="K-means, an unsupervised learning approach"]
{nbsp} +

//ST: !
==== c. The *supervised* learning approach

//ST: !
Take 50,000 or more observations, or data points, like:

**an image of a cat, with the caption "cat"

**an image of a dog, with the caption "dog"

**another image of a cat, with the caption "cat"

etc....

//ST: !
- you need 50,000 observations of this kind, or more! It is called the *training set*
- this is also called a *labelled dataset*, meaning that we have a label describing each of the observation.

//ST: !
The task is: if we give our computer a new image of a cat without a label, will it be able to guess the label "cat"?

//ST: !
The method:

- take a list of random coefficients (in practice, the list is a vector, or a matrix)

//ST: !
- for each of the 50,000 pictures of dogs and cats:
** apply the coefficients to the picture at hand (let's say we have a dog here)
** If the result is "dog", do nothing, it works!
** If the result is "cat", change slightly the coefficients.
** move to the next picture

//ST: !
- After looping through 50,000 pictures the parameters have hopefully adjusted and fine tuned. This was the *training of the model*.

//ST: !
Now, when you get new pictures (the *fresh set*), applying the trained model should output a correct prediction ("cat" or "dog").

//ST: !
Supervised learning is currently the most popular family of machine learning.

//ST: !
image::kmeans.jpg[align=center, title="A hard test case for supervised learning"]
{nbsp} +

//ST: !
video::4HCE1P-m1l8[youtube]

//ST: !
It is called *supervised* learning because the learning is very much constrained / supervised by the intensive training performed:

-> there is limited or no "unsupervised discovery" of novelty.

//ST: !
Important take away on the supervised approach: *collecting __large__ datasets for training is key*

Without these data, no supervised learning.

//ST: !
==== d. The *reinforcement* learning approach

//ST: !
Take the case of a video game like Super Mario Bros. Goal of the task: collecting gold coins and completing the game.

- Starting point: Mario Bros is standing at the beginning of the game, doing nothing.
- Randomness is introduced: try something ("move right")

//ST: !
- The game ends (Mario moved right, gets hit by a ennemy)
- This negative result is stored somewhere (walking close to an ennemy = not good)
- Game starts over

//ST: !
- Randomness is introduced: try something different ("move right and make random jumps")
- The game ends (Mario moved right, jumped above the ennemy, collected gold coins with the jump, then got hit by a nasty cloud or fire when jumping)

//ST: !
- This new negative result is stored somewhere (walking close to an ennemy = not good, jumps near fire = not good, jumps = more gold coins)

//ST: !
- Game starts over
- Etc...

Note: reinforcement is both positive ("jumps help collect gold coins") and negative ("walking straight to an ennemy ends the game")

//ST: !
video::qv6UVOQ0F44[youtube]

//ST: !
Reinforcement learning is perceived as corresponding to an important side of human learning / human intelligence (goal oriented, "trial and error").


//ST: !
These 3 families are called together *machine learning* because:

//ST: !
- the follow a looping process which is, really, an algorithm made to run on a computer, not a mathematical formula

-> a series of instructions ("do this, then that...") repeated quickly over and over again, which computers are good at performing.

//ST: !
- the solution is not found by applying a mathematical model, but emerges through a *learning process*:

-> the coefficients get better and better at each loop of the algorithm.


== 2. Machine Learning and Data Science
//ST: 2. Machine Learning and Data Science

//ST: !
Machine learning is a step in the longer chain of steps of data science.

"Doing data science" is very much discovering knowledge in data.

//ST: !
The process was formalized as https://en.wikipedia.org/wiki/Data_mining#Process[kdd]: "Knowledge Discovery in Databases":

//ST: !
image::kdd.jpg[align="center", title="KDD - knowledge discovery in databases"]
{nbsp} +

//ST: !
Machine learning is one of the techniques (along with traditional statistics) that intervenes at the step of "Data mining".

//ST: !
What makes data scientists important is that the steps of this kdd are highly interdependent.

//ST: !
You need indviduals or teams who are not just versed in data mining:

-> because the shape of the data at the collection stage has a huge influence on the kind of techniques, and the kind of software, that can be used to discover knowledge.

//ST: !
The skills of a data scientist are often represented as the meeting of three separate domains:

//ST: !
image::conway.png[align="center", title="The Venn diagram of what is a data scientist"]
{nbsp} +

source: http://drewconway.com/zia/2013/3/26/the-data-science-venn-diagram

== 3. Artificial intelligence
//ST: 3. Artificial intelligence

//ST: !
==== a. Weak vs Strong AI

//ST: !
We are currently at the stage of "weak AI", not being sure if "strong AI" will emerge.

//ST: !
Weak AI designates computer programs able to perform better than humans at complex tasks with a narrow focus (playing chess)

//ST: !
Weak AI is typically the results of applying machine learning techniques seen above.

//ST: !
Strong AI is an intelligence that would be general in scope, able to set its own goal, and conscious of itself. Nothing is close to that yet.

//ST: !
So AI is a synonymous with machine learning at the moment.

//ST: !
==== a. Two videos to understand AI further

//ST: !
Laurent Alexandre on the social and economic stakes of AI (in French):

//ST: !
video::rJowm24piM4[youtube]

//ST: !
John Launchbury, the Director of DARPA's Information Innovation Office (I2O) in 2017:

//ST: !
video::-O01G3tSYpU[youtube]

== The end
//ST: The end
//ST: !

Find references for this lesson, and other lessons, https://seinecle.github.io/mk99/[here].

image:round_portrait_mini_150.png[align="center", role="right"]
This course is made by Clement Levallois.

Discover my other courses in data / tech for business: http://www.clementlevallois.net

Or get in touch via Twitter: https://www.twitter.com/seinecle[@seinecle]
