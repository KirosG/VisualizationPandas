## [Big Data Foundations: Techniques and Concepts](https://www.linkedin.com/learning/big-data-foundations-techniques-and-concepts)

## Course details

2h 12mBeginnerReleased: October 22, 2014**8 chapter quizzes**

Big data is big news. But what is big data, and how do we use it? Simply put, big data is data that, by virtue of its velocity, volume, or variety (the three Vs), cannot be easily stored or analyzed with traditional methods. Spreadsheets and relational databases just don't cut it with big data. In this course, Barton Poulson tells you the methods that do work, introducing all the techniques and concepts involved in capturing, storing, manipulating, and analyzing big data, including data mining and predictive analytics. He explains big data's relationship to data science, statistics, and programing; its uses in marketing, scientific research, and tools like Amazon's recommendation engine; and the ethical issues that lie behind its use.  

Lynda.com is a PMI Registered Education Provider. This course qualifies for professional development units (PDUs). To view the activity and PDU details for this course, click[here](https://ccrs.pmi.org/search/Activity/220314).  
![](http://files.lynda.com/files/course_description_images/REP_color.jpg)  
The PMI Registered Education Provider logo is a registered mark of the Project Management Institute, Inc.



# Introduction

### Welcome

Techniques and Concepts of Big Data.Big Data refers to data that because of its size,speed or format, that is, its volume, velocity or variety,cannot be easily stored, manipulated or analyzedwith traditional methods like spreadsheets,relational databases or common statistical software.We'll take a look at a practical definition of Big Data,how it relates to fields like data science,statistics and programming and the variety ofpeople and skills involved with Big Data.We'll also discuss how Big Data has been used in fieldssuch as marketing and scientific research, how Big Datainfluences customer services like recommendation enginesand the ethical issues raised by Big Data.

Finally, we'll go over common methods for generatingor capturing Big Data, storing and manipulating Big Dataand analyzing and visualizing Big Data,including data mining and predictive analytics.The applications of Big Data have been extraordinaryand its possibilities are immense.This overview should help you get excitedabout what big data can do for you.And with that in mind,let's get started with Techniques and Concepts of Big Data.

## What Is Big Data?

### The three Vs of big data

- Big data is an ambiguous and relative term.It may be best to define it by what it is not.It's not regular data.It's not business as usual.It's not something that an experienceddata analyst may be ready to deal with.To put it another way, big data is data thatdoesn't fit well into a familiar analytic paradigm.It won't fit into the rows and columnsof an Excel spreadsheet.It can't be analyzed with conventional multiple regression,and it probably won't fit on yournormal computer's hard drive anyhow.On the other hand, one way of describing big datais by looking at the three V'sof volume, velocity, and variety.

These come from an article written by Doug Laney in 2001,and they're taken as the most common characteristicsof big data, but they're certainly not the only ones.We'll talk about some other possible V's to considerin big data later in this course.Let's start by looking at thefirst of the three V's, volume.

### Volume

In its simplest possible definition,big data is data that's just too bigto work on your computer.Obviously this is a relative definition.What's big for one system at one timeis common place for another systemat another time.That's the general point of Moore's Law,a well known observation in computer sciencethat physical capacity and performanceof computers double about every two years.So for example, my Mac Classic two,which got me through graduate school,had two megabytes of ram and an 80 megabyte hard driveand so as far as it was concerned,big data is something that would fit ontoa one dollar flash drive right now.

![Image result for Moore's law](https://upload.wikimedia.org/wikipedia/commons/thumb/9/9d/Moore%27s_Law_Transistor_Count_1971-2016.png/1200px-Moore%27s_Law_Transistor_Count_1971-2016.png)

![Image result for Moore's law](https://i-cdn.phonearena.com//images/articles/115059-thumb/000192-00.png)

On the other hand, in Excelthe maximum number of rowsthat you could have in a single spreadsheethas changed over time.Previously it was 65,000.Now it's over a million,which seems like a lot,but if you're logging internet activitywhere something can occur hundreds or thousandsof times per second,you'll reach your million rows very, very quickly.On the other hand, if you're looking atphotos or video and you need to haveall of the information in memory at once,you have an entirely different issue.

Even my iPhone takes photosat two or three megabytes per photoand video at about 18 megabytes per minute,or one gigabyte per hour.That's on my iPhone.And if you have a Red Epic video camerayou could do up to 18 gigabytes per minute.And instantly you have very big data.Now, some people call this lots of data,meaning it's the same idea of the datathat we're generally used to,there's just a lot more of it.And that gets into the issues ofvelocity and variety.

We'll talk about velocity next.

### Velocity

So for velocity, this is when data is coming in very fast.In conventional scientific research,it could take months to gather data from 100 cases,weeks to analyze the data,and years to get that research published.Not only is this kind of data time consuming to gather,it's generally static once it's entered,that is, it doesn't change.As an example, perhaps the most familiar data set for teaching the statistical procedure, cluster analysis,is the Iris data collected by Edgar Andersonand analyzed by Ronald Fisher,both of whom published their papers in 1936.

This data set contains four measurements:The widths and lengths of the petals and sepalsfor three species of Iris.It's got about 150 cases,and this data set is used everyday.It's one of the built in data setsin the statistical programming language, R,and it hasn't changed in nearly 80 years.At the other end of the scale,if you're interested in using datafrom a social media platform, like Twitter,you may have to deal with the so-called "fire hose".In fact, right now they're processingabout 6,000 tweets globally per second.

![Related image](https://upload.wikimedia.org/wikipedia/commons/thumb/1/10/Iris_Flowers_Clustering_kMeans.svg/2000px-Iris_Flowers_Clustering_kMeans.svg.png)

That works out to 500,000,000 tweets per dayand about 200,000,000,000 tweets per year.In fact, a neat way to see thisis with a live counter on the web.At Internet Live Stats, it's showing usthat there are about 341,000,000 tweetsthat have been sent so far today,and they're updating extremely quickly.

![36](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 02.38.36.png)

![07](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 02.41.07.png)

Even a simple temperature sensorhooked up to an Arduino microprocessorthrough a serial connection,and is sending just one bit of data a time,that can eventually overwhelm a computerif left running long enough.

Now, this kind of constant influx of data,better known as streaming data,presents special challenges for analysis,because the data set, itself, is a moving target.If you're accustomed to working with static data sets,in a program like SPSS or R,the demands and complexities of streaming datacan be very daunting, to say the least.

### Variety

And now we get to the third aspect of big data, variety.What we mean here is that it's not justthe rows and columns of a nicely formatteddata set in a spread sheet, for instance.Instead you can have many data sheetsin many different formats.You can have unstructured text,like books and blog postsand comments on news articles and tweets.One researcher has estimated that 80 percentof enterprise data may be unstructured,so it's the majority as the common case.This can also include photos and videos and audio.

![Image result for unstructured text](https://www.datamation.com/imagesvr_ce/8800/structured-unstructured.jpg)

![Image result for unstructured text](https://lh4.googleusercontent.com/s63d2T5cWBYBQuKQUiMI5GEZBmwAD_EM7KZNKYkvUHSkeWG1hZ7c5YoQoQSpyApjbyHqx_fO77GjpIZG_6qs9WtGxXlEumd1W1VbN1bDk2fa0fgKHCFDPldyhVXpi0A8Wmi7aky172Ff)

Similarly, data sets that include thingslike networked graph data,that's social connections data.Or if you're dealing with data setsin what is called noSQL databases,so you may have graphs of social connections.

![10](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 02.46.10.png)

you may have hierarchicalstructures and documents.Any number of data formats that don't fit wellinto the rows and columns of a conventionalrelational database or a spreadsheet,then you can have some veryserious analytical challenges.

In fact, a recent study by Forester Researchshows that variety is the biggest factorthat's leading companies to big data solutions.In fact, variety was mentioned over four timesas often as data volume.

### Does big data need all three?

- Now, the final question here is,"Do you have to have all three V's-- volume, velocity,and variety-- at once, or just one, to have Big Data?It may be true that if you have all three V's at once,then you have Big Data, but any one of them can betoo much for your standard approach to data.And really, what Big Data means isthat you can't use your standard approach with it.As a result, Big Data can present a numberof special challenges.We'll be discussing those later, but first,let's take a look at how Big Data is used and some of the amazing things that are already being accomplished by using Big Datafor research, for business, and even for the casual consumer.

## Chapter Quiz

- ###### Question 1 of 4

##### Big Data means that you cannot use your computer's standard approach to analyze data.

  **TRUE**

- FALSE

###### Question 2 of 4

##### Moore's Law suggests that physical capacity and performance of computers doubles every two years.

- **TRUE**
- FALSE

###### Question 3 of 4

##### What are the three V's of big data?

- Variety, Variety, and Variety
- Value, Velocity, and Variance
- **Volume, Velocity, and Variety**
- Variance, Volume, and Value

###### Question 4 of 4

##### Velocity is a part of big data since it includes _____ from more than 18 billion networks.

- **streaming data**
- voluminous data
- consistent data
- dynamic data

  ### 2. How Is Big Data used?

### Understanding big data for consumers

  Most of the time when you hear people talkabout big data, they're talking about it withinthe commercial setting about how businesses can usebig data in advertising or marketing strategies.But one really important place that big datais also used is for consumers, and what's funnyabout this is that while the data is thereand the algorithms are there and as incrediblysophisticated processing it's nearly invisible.The results are so clean they give you just alittle piece of information, but exactly what you need.What I want to do is show you some commonapplications of big data for consumersthat you may be using already withoutbeing aware of the sophistication ofthe big data analysis that's going into it.

  The first one is if you have an Apple iPhoneor iPad is what Siri can do.So for instance, aside from saying what'sthe weather like, and Siri actually knowswhat it is you mean, and where you are,and what time you're talking about, it can do thingslike look for restaurants of a particular kindof food and see if they have reservations available.It can do an enormous amount of things that requires the recommendation of other people,awareness of your locations, awareness ofthe changes over time of whatis most preferable for people.

  ![00](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 02.54.00.png)

  Another one is Yelp.A lot of people use this to find a restaurant,and again, it draws on millions and millionsof reviews from users and from other sourcesto make a very small recommendation.Here I'm searching for Thai food in Carpinteria,California, which is where Lynda.com is located.I've got Siam Elephant and Your Place Restaurantas my first two hits.The next one, you might be familiarwith recommendation engines.This is an idea of software that is able to makea specific suggestion to you.

  ![50](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 02.53.50.png)

  Yelp is an example, but people are more familiarwith things like movies, and books, and music.Here's my Spotify account, and Spotify knows whatI listen to when I'm on Spotify, and what I listento all the way through, what I add to my list,what I skip through, and it's able to make specificsuggestions to help me find new artiststhat I wouldn't otherwise know about.I love some of the stuff that Spotify comes up with.

  ![45](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 10.39.45.png)

  Similarly, Amazon.com makesrecommendations for books.For instance, here's a book, Principles of Big Data,one of my favorites, by Jules Berman,and if you scroll down you'll see that theyhave a list of other books that are recommended.

  ![03](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 10.41.03.png)

  This is generated by Amazon's recommendationengine, and you see several other bookson big data, and in fact, it's a great list,I own about half of them.It's the same general principle here.

  ![57](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 10.42.57.png)

  A lot of people use Netflix to get movies.Netflix makes specific suggestionsfor other movies you might like.

  ![07](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 10.44.07.png)

  What's interesting is that a few years agothey had a major contest called the Netflix Prizewhere they wanted to see if anybody could improvethe accuracy of their predictions,meaning would you actually like this.

  If they could improve those predictions by 10%it was a million dollar prize and it wasincredibly sophisticated analysis that wentinto this, but the end result againis a very simple thing, you get recommendeda hand full of movies, and usuallyyou pick one and you like it.In another context there's the app calledNeighborland, which is designed to help youcollaborate with people to make your citywork a little bit better.

  ![18](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 10.45.18.png)

  That's a simple goal, but what Neighborlanduses is photos, and data, and APIs from Twitter,and Google Maps, and Instagram, and agenciesthat report on real estate parcels, it usestransit systems, it uses three one one complaints,an enormous set of data that really highlightsthe variety of big data.

  The other ones, for instance, with Spotify and Yelp,show the volume, but this one shows the varietyof integrating data from so many different placesand so many different formats to help peoplecollaborate on something simple about workingtogether to improve their neighborhood.Finally, the last one I want to show youis Google Now, and what Google Now does is itactually makes recommendations before you askfor them, especially when it's linked up to yourcalendar and it's linked up to the locationsensing on your phone.

  ![49](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 10.57.49.png)

  It knows where you are, it knows where you needto be, and it can tell you about things liketraffic or the weather before you even ask for it,and this is based on, again, an enormous amountof information about the kinds of informationpeople search for, and it provides itin a sort of preemptive manner.So for consumers, big data plays an enormous rolein providing valuable services, but again,with the irony that it operates invisiblyby taking a huge amount of information fromseveral different sources and distilling itinto just two or three thingsthat give you what you need.

### Understanding big data for business

We saw in the last movie that big datacan provide important conveniencesand functinality for consumers,but for the business world,big data is revolutionizing the way people do commerce.In this movie, I want to look at a few particular placeswhere big data has proven to be particularly useful,or unusual and interesting.The first thing we're going to do is look at the placewhere most people have encountered big data in commerce,and that's in the results for Google ad searches.Whenever you search for something on Googleor any other search engine,you type in your term.

![41](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 10.59.41.png)

You're going to get the results that you want,but you're also going to get ads.You see here, for instance, on the topI'm searching for big data.I have three ads on the top,and I have a series of ads down the right side.Those ads are not placed at random.They're placed there because they are basedfirst on the thing that I am currently searching for,but also based on what Google knows about me.You can see in the top rightthat I am logged in to my own account,so Google is drawing on all of the thingsthat I've searched for, and the other informationit has about me, to try to place adsthat it thinks I would be most likely to respond to.That's something it gets by havinga very large amount of data available,to tailor things to be most applicable to the consumer.

Another interesting place is what's called predictive marketing.This is when big data is used to help decidewho the audience would be for somethingbefore they actually get there.This is trying to predict, for example,major life events, like for instancegraduating, or getting married, or getting a new job,or having a child, or any number of eventsthat are often associated with a whole seriesof commercial transactions.

![15](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.03.15.png)

To do this, these companies can look at consumer behavior.They can look at how often you log onto their website.They can look at what credit cards you use.They can look at how often you look at particular itemsbefore moving on to something else.They can look at whether you've appliedfor an account at their organization.They can make a huge amount of informationthat they already have available to them.Similarly, they can use demographic information.This can include things like your age,your marital status, the number of children you have,your home address, how far you live from their store,your estimated salary, if you've moved recently,what credit cards you have, what websites you visit.

All of this information is potentially availablein one form or another,to the company that's trying to make these predictions.Similarly, they can rely on additional purchased data.It's possible for the company to get informationabout your ethnicity, your job history,your magazine subscriptions,whether you've declared bankruptcy or been divorced,whether you've attended college,the kind of things you talk about online, and so on.There's an enormous amount of information herethat again is potentially available.Now, this is going to lead into an important discussion.

In fact, we have an entire series of movieson ethics and big data,so that's going to come up on this one.But using this kind of information,it is possible for a company to predictthat you're about to buy a new house,and that when you buy a new houseyou make an enormous number of purchases,and so they can link in to youbefore you start making the commitments to those.Another place we want to talk about big datais trying to predict trends.One of the really fascinating places for this is in fashion.The company Editd has actually received awardsfor their use of big data in predicting fashion trends.

![53](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.04.53.png)

So they can actually tell retailerswhat the most popular colors and stylesand brands are going to be,when they're going to be popular,and they can help them price them.Obviously, this kind of informationis enormously important to the companiesthat are going to be selling these products,and Editd is able to do thisthrough their reliance on big data.A final thing I want to mention about the useof big data in commerce is for fraud detection.Now it turns out that fraud is an enormous industry,that online retailers lose about $3.5 billion dollarseach year to online fraud,and insurance fraud, not counting health insurance,is estimated to be more than $40 billion dollars per year.

So fraud is a big issue.It turns out that there's a number of thingsthat companies can do to lessen the prevalence of fraud,especially through online transactions.They can look at the point of sale.That specifically means, how are you making the purchase?Are you online, and what website are you using?They can use geolocation.Where are you physically located in the world?They can look at the IP address.What computer are you using to access the website.They can look at the log in time.

![16](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.07.16.png)

So are you somehow making a purchase at 4:00 a.m.,when you've never before done anything after 11:00 p.m.Interestingly, they can also look at things like biometrics.I was talking with a colleaguewho works in computer security,and says that, for instance,the way that people move their mouse,or the time they take between pressing keys on the computer,are distinctive measurements of people.When you hold your cell phone and you're looking at it,people of different heights hold the cell phonesat different angles, as measuredby the accelerometer in the phone.

All this can be used to determine whether the personwho is making the purchase is who they say they are.I've been saved by this.I remember a few years ago, American Express called me,and asked me if I had just booked $4,000 of hotel roomsin the Middle East.No, I had not.It turned out that there were a seriesof other small purchases that were not in the Middle Eastthat showed my account had been compromised.Fortunately, American Express was ableto stop these charges beforehand,and they were able to help solve the problemsand get things taken care of.

But a lot of it was because of these particular detailsand the patterns that they havein their extraordinarily large data set,let them recognize these anomaliesas potential fraud, which in this case,they actually were.

### Understanding big data for research

In the previous movies we lookedat the role that big data can playin individual people's lives as well as in businesses.We also want to look very quickly at howbig data has been revolutionizingaspects of scholarship and research.I want to show you a few interesting examplesof where big data has influenced scientific progress.The first one we want to look at isGoogle flu trends where they were able to find thatsearch patterns for flu related words wereactually able to identify outbreaks of the fluin the United States much faster than theresearch that the Center for Disease Control could do.

![04](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.10.04.png)

Similarly, a more recent project found that Wikipediasearches could identify them with even greater accuracy.

![57](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.10.57.png)

![38](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.11.38.png)

The National Institutes of Health created theBrain Initiative as a way of taking enormous numbers ofbrain scans to create a full map of brain functioning.Additionally, NASA'`s Kepler space telescopehas been on a mission to find exoplanets, orplanets outside of our solar system.

![31](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.12.31.png)

As you can see over here so farit's identified nearly 1000 confirmedplanets with over 4000 candidates.Closer to home, psychological research has alsobeen influenced through big data.Just last year, a paper published aboutpersonalities in the United Stateswas able to identify clusters of personalities,in regions where we have the mid-westernfriendly and conventional region,the western relaxed and creative region,and a northeastern and somewhat southerntemperamental and uninhibited region.

![16](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.13.16.png)

![15](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.14.15.png)

Now, I'd like to say that this is not based onsimply how do you feel about the places,but this is published in a journal from theAmerican Psychological Association, avery high quality psychological research.Similiarly, another group of reseachers created anapplication on Facebook that used ascientifically valid measure of personality.

![27](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.16.27.png)

They got data several hundred thousand respondents andby combining those with the patterns of likes thateach of those people had on Facebook, theyfound they were able to create a single question app,that really just asked for access to your likes that'sable to give a surprisingly accurate evaluationof what your personality would beif you took the entire questionnaire.

Finally, the Google Books project.For the last few years, Google has been scanningbooks that were published over the last few hundred years.

![31](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.17.31.png)

They currently have over 30 million booksthat they have scanned, they make themdigitally accessible, and that allows peoplein Digital Humanitites to look at thechanges in word usage over time.There's some interesting things, so for instance here,we have the last 208 years of the prevalence of the word,'math' and 'arithmetic' and 'algebra' where'arithmetic' shows a strong spike in the 20s and 30s,but it decreases over time, whereas the word 'math'has increased over the last 50 to 60 yearswith a peak right around 2000.

Now this is just one possible example of what can be done,but the idea here is that big datawith both the volume of information that's available,the variety of information that's able to be combined,and with the velocity, especially with things like theflu trends where things are changing constantly,all of these are able to make good use of big datafor scientific research and advancement.It's an exciting time to see what's happening,And to see what will happen in the near future.

###### Chapter Quiz

###### Question 1 of 2

##### Which of the following uses multiple sources of data to provide a simple result to consumers?

- Neighborland
- Siri
- Google Now
- **all of these answers:- Each of these leverages data from multiple sources to provide a simple solution to the consumer.**

###### Question 2 of 2

##### By using big data, companies can predict future market trends and price their goods accordingly. This has been useful in the _____ industry.

- housing
- automobile
- food
- **fashion** The company Editd has used big data to predict popular colors, styles, trend timing, and prices.

## 3. Big Data and Data Science

### Ten ways big data is different from small data

Big data can be characterized by more thanthe three Vs that we mentioned in the previous movie.Those were volume, velocity, and variety.There are several practical differences as well.Jules Berman has a book called Principlesof Big Data: Preparing, Sharing,and Analyzing Complex Information.He lists 10 ways that big data's differentfrom small data, and I want to go throughsome of those points here.The first is goals.Small data is usually gathered for a specific goal.Big data on the other hand may have a goalin mind when it's first started, but thingscan evolve or take unexpected directions.![13](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.23.13.png)

The second is location.Small data is usually in one place, and oftenin a single computer file.Big data on the other hand can be in multiple filesin multiple servers on computersin different geographic locations.![15](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.24.15.png)

Third, the data structure and content.Small data is usually highly structured likean Excel spreadsheet, and it's got rowsand columns of data.Big data on the other hand can be unstructured,it can have many formats in files involvedacross disciplines, and may link to other resources.![12](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.25.12.png)

Fourth, data preparation.Small data is usually prepared by the end userfor their own purposes, but with big datathe data is often prepared by one group of people,analyzed by a second group of people,and then used by a third group of people,and they may have different purposes,and they may have different disciplines.

![49](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.30.49.png)

Fifth, longevity.Small data is usually kept for a specific amountof time after the project is overbecause there's a clear ending point.In the academic world it's maybe five or sevenyears and then you can throw it away,but with big data each data project, because itoften comes at a great cost, gets continuedinto others, and so you have data in perpetuity,and things are going to stay therefor a very long time.![47](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.31.47.png)

They may be added on to in terms of new dataat the front, or contextual data of thingsthat occurred beforehand, or additional variables,or linking up with different files.So it has a much longer and really uncertainlifespan compared to a small data set.

The sixth is measurements.Small data is typically measured with a singleprotocol using set units and it's usually doneat the same time.With big data on the other hand, because you canhave people in very different places, in verydifferent times, different organizations, and countries,you may be measuring things using differentprotocols, and you may have to do a fair amountof conversion to get things consistent.

![03](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.33.03.png)

Number seven is reproducibility.Small data sets can usually be reproduced in theirentirety if something goes wrong in the process.Big data sets on the other hand, because they comein so many forms and from different directions,it may not be possible to start over againif something's gone wrong.Usually the best you can hope to do is to at leastidentify which parts of the data projectare problematic and keep those in mindas you work around them.

![08](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 11.34.08.png)

Number eight is stakes.On small data, if things go wrong the costsare limited, it's not an enormous problem,but with big data, projects can cost hundredsof millions of dollars, and losing the dataor corrupting the data can doom the project,possibly even the researcher's careeror the organization's existence.

![52](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 12.28.52.png)

The ninth is what's called introspection,and what this means is that the datadescribes itself in an important way.With small data, the ideal for instance is what'scalled a triple that's used in severalprogramming languages where you say, first off,the object that is being measured.

![17](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 12.30.17.png)

Here, I say Salt Lake City, Utah, USA,that's where I'm from.Second, you say what is being measured,a descriptor for the data value.In this case, average elevation in feet.Then third, you give the data value itself,4,226 feet above sea level.In a small data set, things tend to be well-organized,individual data points can be identified,and it's usually clear what things mean.In a big data set however, because things can beso complex with many files and many formats,you may end up with information thatis unidentifiable, unlocatable, or meaningless. Obviously, that compromises the utilityof big data in those situations.

The final characteristic is analysis.With small data it's usually possible to analyzeall of the data at once in a single procedurefrom a single computer file.With big data however, because things areso enormous and they're spread across lotsof different files and servers, you may haveto go through extraction, reviewing, reduction,normalization, transformation, and other stepsand deal with one part of the data at a timeto make it more manageable, and then eventuallyaggregate your results.![56](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 12.30.56.png)

So it becomes clear from this that there'smore than just volume, and velocity, and variety.There are a number of practical issues that canmake things more complex with big datathan with small data.On the other hand, as we go through this coursewe're going to talk about some of the general waysof dealing with these issues to get the added benefitof big data and avoiding some of the headaches.

### The three facets of data science

When people talk about big data,they nearly always talk aboutdata science, and data scientists, as well.Now, just as the definition of big data is still debated,the same is true for the definition of data science.To some people, the term's just a fancierway of saying statistics and statisticians.On the other hand, other people argue thatdata science is a distinct field.It has different training, techniques,tools and goals than statistics typically has.Now, that's what we're going to talkabout in this movie.The first thing that we want to do, is we want tolook at what's called the data science venn diagram.![Image result for data science](https://images.click.in/classifieds/images/72/20_05_2018_23_39_58_b6068943642cde764518e6570be715d2_9q1th3bfvi.png)

This is a chart that was created by Drew Conwayin 2010, and what he's arguing hereis that data science involves acombination of three different skills.The first is statistics.That's on the top right.The second, on the bottom, is domain knowledgethat you actually know, for instance, aboutmanagement or advertising or about sports recruiting.And the one on the top left is coding,or being able to program computers,and he's arguing that really, to get data science,a person needs to be able to do all three of these,so we're going to talk about each of these facetsone at a time and in combination with each other.

The first component of data science is statistics,which shouldn't be surprising because we'retalking about data science.The trick here is that a lot of thingsthat go into statistics and mathematicscan be really counterintuitive, and if you don'thave the specific formal training,you can make some really big mistakes.An easy example of this is what's called the birthday problem in probability.That's simply trying to figure out what's theprobability that two people in a room have the same birthday, month and day,and intuition suggests that to have a 50% chanceof a match, you should have over 180 people in the group, because that's about half as many people as there are days.

On the other hand, the correct answeris a lot smaller than that.It's in the 20s, and that's all you need to have a 50% chance of a match,and because data scientists often are going to be looking for matches and associations,being able to get these probabilities correct is a really important part.That's why mathematical training isan important part of data science.The second element of data science is domainknowledge, and the idea here is that a researchershould know about the topic area that they'reworking in, so if you're working in, say for instance,marketing, you need to understand how marketingworks, and that makes it so you can have moreinsight and better direct your analyses andyour procedures to match the questionsthat you might have.

![36](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 12.36.36.png)

For instance, there's a wonderful blog postby Svetlana Sicular of Gartner Ink, where she writes,"Organizations already have people who know their"own data better than mystical data scientists -"this is a key."The internal people already gained experience"and ability to model, research, and analyze."Learning Hadoop, (and that's a common software"(framework for dealing with big data), learning"Hadoop is easier than learning"a company's business."And that really underscores the importanceof domain knowledge in data science.The third element of Drew Conway's data sciencediagram is coding, and this refers tocomputer programming ability.

Now, it doesn't need to be complicated.You don't have to have a PhD in computer science.A little bit of Python programmingcan go a very long way.It's because this allows for the creativeexploration and manipulation of data sets,and especially when you considerthe variety of data that's part of big data.The ability to combine data that comes in differentformats can be a really important thing,and that often requires some coding ability.It also helps to develop algorithmic thinking,or thinking in linear steps by steps by stepsto get through a problem.

Fortunately, Lynda.com has a great set of tutorialson both Python and in working through thecommand line, which are listed in thelast video of this course.Next, we'll talk about combinationsof two of these elements at a time.The first one is statistics anddomain knowledge without coding.Now, this is what Conway calls traditional research,and this is where a researcher works withintheir field of expertise, uses common toolsfor working with familiar data formats.It's extremely productive, and nearly all existingresearch has been conducted this way.

The American Psychological Association,that's in my field, specifically directs researchers,for example, to use the simplest methods possiblethat will adequately address their research questions.That's what they call a minimally sufficient analysis.So, these traditional methods are extremelyimportant, but they aren't sufficient for workingwith big data, and we'll talk more about that.The second combination is statisticsand coding without substantive expertise.This is what Conway refers to as machine learning,and now, that's not to be confused with data mining.

Machine learning is where an algorithm or aprogram updates itself and evolves to performa specific analytical task.The most familiar example of this is spam filtersin email, in which the user or a whole large groupof users identify messages as spam or not spam,and the formula that the program uses to determinewhether something is spam updates with each newpiece of information to have increased accuracythe more you use it.Now, a risk with machine learning is thatyou get the idea of a mystical black box.

You don't actually know how the programis doing what it's doing.On the other hand, if what you're looking foris prediction only, this can be a very effective method.On the other hand, with Conway's model,it's not enough to constitute data sciencewithout an important element of substantiveor domain knowledge.The third combination here is domainknowledge and coding without statistics.Now, Conway labels this a danger zone,with the idea being that you have enoughknowledge to be dangerous.While there are problems with this,I'll mention two things.

First, Conway himself mentions thatit seems very unlikely that a personcould develop both programmingexpertise and substantive knowledgewithout also learning some math and statistics,so he says it would be a sparsely populatedcategory, and I believe that's true.On the other hand, there's some really importantdata science contributions that come out of thiscombination, including, for instance, what arecalled word counts, which we'll talk about later.It's simple stuff.These are procedures that do not requiresophisticated statistics.You're just counting how often things occur,and you can get important insights out of that,so I wouldn't write this one off completely.

![30](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 12.47.30.png)

I would say, though, that like Conway,it's not likely that a person could developexpertise in both coding and their domain without getting the math and statistics as well.And finally, of course,there's all three of these things,statistics, domain knowledge, and coding, at once,and that is the most commondefinition of data science.

### Types and skills in data science

When people talk about big data in newspaper articlesor professional conferences, it's easy to get the ideathat data scientists are not just peoplewho have domain expertise,who understand statistics and can program.Instead, they often start to sound like omnicientand omnipotent super humans who can do anythingand do it instantly and effortlessly.Of course, it's not the real picture.As with any other domain there is a large range of skillsinvolved in data science beyond the three mentioned earlier.A great report called, **"Analyzing the Analyzers:"An Introspective Survey of Data Scientists and Their Work"** goes over this in detail.

It's a short 40-page book by Harlan Harris, Sean Murphyand Marck Vaisman that was publishedby O'Reilly Media in 2013.It's available in print or as a free e-bookfrom O'Reilly or Amazon.In it, the authors surveyed about 250 data science practitioners.They asked them how they identified themselvesand how they clustered skillsthat are relevant to data science.Each of these classifications was then subject tocluster analysis and then to a cross-classification.What they found is expected is that there's a high levelof heterogeneity among the people in big data,not everyone is the same.

![46](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 12.54.46.png)

The respondents rated themselves in terms of 11possible professional identities.In alphabetical order, they were artist and business person,developer, engineer, entrepreneur, hacker,jack of all trades, leader, researcher,scientist and statistician.This table shows how those 11 identities clusteredbased on the individual's responses.They fell into four basic categories:The data developer, that's developer and engineer,the data researcher, that's researcher,scientist and statistician,the data creative, that's the jack of all trades,the artist and the hacker,and the data business person is leader,businessperson and entrepreneur.

![24](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 12.56.24.png)

Next the respondents ranked themselveson a list of 22 possible skills, such as algorithms,visualization, product developmentand systems administration.![45](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 12.55.45.png)

These skills sorted into five general categoriesrelevant to data science,business, machine learning or big data, that's ML,math or operations research, programming and statistics.Now what's important here is you see that the skillsare not the same for all of them so for example,in the business category on the far left,we have product development in businesswhereas on programming near the rightwe have systems administration and back-end programming.

Not everybody needs to be able to do all of the same things.In fact, when the researchers crossed the self-identification categories with the skillsthey got rough profiles of the skills associatedwith each category of data science practitioner.![50](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 13.10.50.png)

Not surprisingly, the data business personis a person who has skill in working with databut views themselves primarily as a business personor a leader and entrepreneur.The data creative is interesting for being the onewhere the skills are most evenly distributed.On the far right, for example, the data researchersees their skills as lying primarilywith statistical analysis.

The most obvious thing here is again,that not everybody's the same.Each group had at least some skill in each areabut the distributions differed dramatically.What this makes clear is that there's roomfor substantial variation in personal interestand skill sets within data science and,by extension, within big data.It's helpful for everybody to know at leasta little bit about each of the five skill categoriesthat the researchers mentioned,but diversity is really the name of the game here.I encourage you to download the free reportand take a closer look at what they foundbecause it helps reduce some of the perceived barriersand self-imposed limitations to engaging in data scienceand working with big data.

### Data science without big data

If you argue that big data requiresall of the three V's:volume, velocity and variety at onceto count as big data properthen it's entirely possible to be a data scientist.A person with domain expertiseand statistical knowledge and encoding skillswithout touching big data.We'll look at a few of these possibilities.First, let's review our Venn diagram of data science.This again shows on the top right we have statistics,on the bottom we have domain knowledgeand on the top we have coding.![Image result for data science](https://ion.icaew.com/cfs-file/__key/communityserver-blogs-components-weblogfiles/00-00-00-00-05/0143.Venn.png)

![Related image](https://cdn-images-1.medium.com/max/1600/1*rHnEr1VuZ3pFA5xctXUagA.png)

Taken together those class to data science.We also have a Venn diagram for big data.Where we have volume and velocity and variety,and again, depending on who you askyou need to have all three of them at onceto have big data.So let's take a look at data sciencefor just one V at a time.So we're talking about statisticsand domain knowledge encodingbut with just velocity or variety or volume. ![37](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 13.17.37.png)The first example we want to look at isvolume of datawithout any remarkable velocity or variety.

So, this would mean a very large and static data set with a consistent format.The data would generally be structured as wellso we're not gonna have free text.A good example of this is genetics data as I'm showing right here from Nature Reviews. ![51](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 13.18.51.png)Genetics data is huge.It's enormous but it follows a well-understood structureand now there's an enormous amountthat you have to do to work through itbut it's consistent in that way.Another good example would bemany instances of data miningor predictive analytics.

In the latter case you may be trying to predicta single outcome like whether a personwill click on an ad or a web page.In this case you might have a data setwith thousands of variablesand maybe even billions of casesbut all of the data is in the consistent format.The size of the datamakes many common approaches impossibleso the coding skills of a data scientist may be essentialalong with a statistical knowledgeand domain knowledge.Next is data science for velocitywithout volume or variety.So, this is referring primarilyto streaming data with a consistent structure.

Now by streaming datawe mean that data is coming in consistentlyand very often you're not holding on to the data.You're just keeping a small window of it open.One interesting example is theearthquake detection systemsof the United States Geological Survey. ![23](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 13.23.23.png)This is the Advanced National Seismic Systemwhich is simply looking to seewhether there are earthquakes that are happeningor really about to happen.And you don't necessarily need to hold onto all the data if what you're trying to do istrigger a responseso that if an earthquake is imminentor if it's just starting,people may have enough time to respond to it.

Another term for this kind of data where it's coming in very fast but you're not necessarily keeping it,so it's relatively low in volume,and it may have a very consistent structure so it's low on variety.This can also be called data stream mining.And one possible example is what's called real time classification of string and sensor data.Finally, for one V at a time,let's talk about data sciencefor a data that has variety.So a lot of different formatswithout velocity or volume.This is where you have a complexbut small or static or relatively static data set.

A couple of examples could include facial recognitionand personal photo collection,so, you don't have an enormous number of photos but you do have a lot of variety visual datais almost always very high in variety,and it may be staticbecause you don't add to it constantly. ![56](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 13.25.56.png)Or you can talk about the data visualizationof complex data sets.One of my favorite examplesis from the site Visually.And we have here an exercise that shows892 unique ways to partition a three by four grid.And this is somethingthat you would not want to create by hand,but they would show a fair amount of codingto create the diagram.

Now these are examples of data sciencewhich again means statisticsand it can mean domain expertiseand it can mean coding,or you're doing just one of the V's of data at a time.You can also do two V's at a time.So for instance you may talk about data sciencefor data where you have volume and velocitybut not a lot of variety.So for instance, a lot of data is coming in very fastbut it's in the same format.You can include for instance stock market dataor here's an interesting one.It has to do with jet engines.And a surprising statistic herecomes from this chart.

Now there's a little bit of math herebut I think they may be multiplyingmore than they need to,but they say that a jet engine has sensors on itthat generate 20 terabytes of information each hour.That's an enormous amount of information. ![52](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 13.27.52.png)So 20 terabytes per engine per hourthen it says times two engines,times six hours cross country flight,plus 28,000 flights,although I don't think they're allcross country flights,and 365 days a year.What they're saying here is they haveover 2 1/2 billion terabytes of data per yearjust from jet engines if all that math is correct.

But the point here is it's a lot of dataand you would want to hold on to thatbecause the failure of a jet engineis an extraordinarily important thing,and so you want to be ableto find the patterns in it fully.Another possibility is data scienceapplied to data that has velocity.So it's coming in fastand there's a lot of variety but not a lot of volume.So again, this is streaming data where you're not necessarily holding on to everything. ![03](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 13.31.03.png)One interesting example of this is surveillance video.Again, we could go ahead to the next chapterwhere we talk about ethics,but there is a lot of surveillance video.

And in fact if you look at the endof the second paragraph here,it says, "According to the International Data Corporation's"recent report that Digital Universe in 2020"half of global big data,"the valuable matter for analysis in the digital universe"was surveillance video in 2012"and the percentage is set to increase to 65%,"2/3 of it by 2015."And that's because surveillance videois moving into high definitionas opposed to the normal really low res stuffthat you often see.Now, if you're saving all the datathen that's an enormous volume.

On the other hand,if you're not saving it but you're streaming it in,it's very fastbecause the information comes in very quickly. Maybe 20, 30 frames per second and it has a lot of variety because it's visual information.But if you're simply wanting to seedoes a person come throughfor instance, who's carrying a weapon,or does a particular event occur?You use a streamand you're just trying to triggerwhen something happens.Finally, let's talk about data sciencefor volume and variety without velocity,and this can be any large historical data setthat uses multiple formatsor includes visual data.

A really good example of this is Google Books. ![25](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 13.33.25.png)We've looked at this before.Where they have 30 million books that they've scannedand they've digitized them,and you're dealing with a really complex information here.This is one of my favorites.It's a book called The Anatomy of Melancholyand I actually have the hard copy version of this as wellbut I love seeing it online.Similar examples include the Twitter archiveswhere every single tweetthat's ever been written has been saved.That's an enormous amount of informationbecause its text is complexbut because it's not updated constantly,it doesn't have the velocity.

Now what this examples show is thatdespite the strong associationbetween big data and data science,the skills of data science,the statistical knowledge and domain expertiseor knowledge encoding skills.Those apply even when thethree major aspects of big dataaren't all present at the same time.In the next movie we'll look atthe flip side of all this.How to work with big datawithout requiring the full data science skill set.

### Big data without data science

In the last movie we talked about data sciencewithout actually having Big Data.In this movie, we'll take the compliment of that.We'll look at scenarios in which a person works withBig Data, but doesn't requirethe full data science skill set.As a way of reminding ourselves, Big Data usually involves unusual volume, and velocity, and variety in the data. ![24](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 13.36.24.png)Data Science also has this little diagram.It involves statistical skills,and domain knowledge, and coding ding ability.

And the three of them together gets data science.Now let's take a look at, can you do Big Datawith just two of the data science skills?How about with just statistics and with coding?The answer of course is yes.Because that's where we have machine learning. ![06](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 13.44.06.png)Machine learning is a very important area of data science and this is where a computer program learnsto adapt to new information as it comes in.The two most familiar examples are spam filters,where the computer program learns that a particularkind of email is spam or not based on your own individualresponses and based on the responses of millions of otherpeople who use the same email program, like Gmail.

Or, facial recognition and photographs where yourcomputer program learns what face belongs to whom.Now here's an article from Nature that talks aboutartificial intelligence and machine learning in general.![06](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 13.53.06.png)

And actually if we scroll down a little bit it talksspecifically about the problem of facial recognitionand how the computers can learn to identify face.It's funny, it's something that's very easy for humansto do, but much harder for a computer.So machine learning is a good example of workingwith Big Data because it can have volume,it can have velocity, it can have variety, but you don'tnecessarily need to have domain knowledge becausethe computer is working without any knowledge whatsoever,simply, did it get it or did it not.

Another possibility is what Drew Conway,who created this Venn Diagram, originally calledthe Data Zone, that's the combination of coding,and domain knowledge without statistics.Now he says, "danger" here, but there are somevery good examples of data science herethat do not involve statistical knowledge.The most common of which are word countsand just parsing of natural language. ![24](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 13.54.24.png)The most common tool used for this is what's called,the natural language tool kit.This is a package that's used inPython, the programming language.

![09](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 13.56.09.png)

![36](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 13.57.36.png)

And it will ask people to do all sorts of amazing things.You can do things like word counts.The best known word count was the one that was usedactually a few decades ago to identifyauthorship of the Federalist lettersin American historical political science,all the way up to the things like,comparing vocabulary sizes of various Hip-Hop singers.And so, there's amazing things that can be donewith natural language by simply countinghow often the words occur, without requirngany statistical knowledge per se, because there'sno influential procedure that goes into it.

And now those are two of the combinations of data scienceskills that we have two at a time without Big Data.That leaves a third one here, and that'sstatistics and substantive or domain expertise.And this traditional research, unfortunately as much as Ipersonally value traditional research, I'm trained asan experimental social psychologist,you're not able to work with Big Data.Without the coding skills, you're not going tobe able to deal with the volume, the velocity,or the variety of data that characterizes Big Data.Tremendous things are accomplished in traditional research,but Big Data is not one of them.

And then, it also goes to say that as far as I can tell,unless you have at least two ofthese, it's just a non-starter.You simply can not work with Big Data if you havejust statistical knowledge, or just codingskills, or just domain knowledge.Instead, what you would have to do in that situationis collaborate with people who have that information.In fact, collaboration really is the rulein data science, as opposed to an exception.Because there is such a broad range of skillsthat are necessary, nobody is usually able tobring all of to it, but they have to work together.

And that actually is one of the wonderful thingsbecause I think that most of the interesting developmentscome about through collaboration.And that's something that data science encourages strongly.And so, when you look at the relationship between datascience and Big Data, the situation isn't exactly even.It's possible to do data science with an incompleteversion of Big Data, but it's much more difficultto do Big Data work without thetriumvirate of data science skills.We'll get more into the specifics of workingwith Big Data in later movies, but first we needto talk about ethics and Big Data.

And that's what we're going to do in the next chapter.

##### Chapter Quiz

###### Question 1 of 1

###### The three facets of data science are:

- coding fast, knowledge, and statistics
- **domain knowledge, coding, and statistics** Each of these is part of the Venn diagram of data science.
- people skills, volume, and accounting
- intrinsic motivation, statistics, and curiosity

## 4. Ethics in Big Data

### Challenges with anonymity

We've discussed some amazing thingsthat can be done with big dataespecially when an individual's information is comparedto a massive data set.Some of those examples however, can feel likethey've crossed the line that separates the impressivefrom the creepy.That's because privacy is an important issueand a lot of these examples feel likethey may have crossed the line into private informationthat people did not expect to have divulged.People don't want their personal information to be publicand over the last several yearsthere have been severe consequences to breaches of privacyeither accidental or intentional.

On the other hand people do want to have quality serviceand need to have good research, there's the rub.One possible solution is to anonymize datato make it anonymous.By removing identifiers like names, addresses,and other obvious bits of personallyidentifiable information.But many such attempts have failed dramatically.One of the major challenges of working with big datais that even when a person attemptsto make the data anonymousby removing obvious identifiers,it's actually not impossible to de-anonymize the data.

A really telling example of this came a few years agoduring the Netflix Prize,when Netflix provided people with an anonymized data setof user ratings on movies. ![51](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 15.20.51.png)Two researchers Arvind Narayanan and Vitaly Shmatikovwere then able to take that informationand compare it with identified user ratingson the internet movie database, IMDb.They were then able to match peoplewho are identified by name on IMDbwith anonymized ratings on Netflixand connected two data sets.![50](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 15.22.50.png)

A bigger challenge, there was another contestthat looked at social networks,and what this is, is the contest included informationthat said, this person who was identifiedjust by a random number is connected to this personand this person, and this person, and this person.From that you get a **social network graph**. ![29](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 15.24.29.png)That's a picture that we've shown beforewhere each circle here represents an individualand the lines are nodes that connect themwith other individuals.What the researcher was able to do in this casewas again, send out a computer crawlergo through several social network sitesthat were publicly availableand they were able to find simply by matching shapes,they had no other information aside from the shapewith a diagram.

They were able to identify a social networkwhich actually came from Flickr, the photo sharing site.They were able to identify shapesin the Flickr social network that matched the datain the contest data, and they were able to thensort of de-anonymize that data set as well.Simply by matching by geometry.Now, even more dramatic example and researcherLatanya Sweeney, showed that she was able to purchasevoter records for Cambridge, Massachusetts.

![36](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 15.26.36.png)

 What this included on the left is the name and address,date registered, party affiliation, and date last votedalong with the zip code, birthdate, and sexfor each person in that voter list.

![00](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 15.28.00.png)

Now on it's own that's not horrible informationexcept you do find out the party affiliationwhen they voted.But what she also found is that with just threeof those pieces of information:the zip code, the birth date, and the person's sexand that's it,she was then able to go to medical recordsthat were publicly available and matched them upand find the person's ethnicity, their visit date,their diagnosis, their procedure, their medication,and their total charge.In fact, she was able to identifythe governor of Massachusettsfrom that data set, and get his medical informationthrough this round about procedure.

Now, this wasn't done as a way of showingthat there, she wasn't trying to dig up any dirt on anybodybut what she was trying to showthat small pieces of readily available informationzip code, birthdate, and sex.She was able to correctly identify 97% of the individualsin the medical data.Now this was done about 20 years agoand the nice thing is that regulations had changedsince then, about the kind of information that's available.Now we have the health insurance portabilityand accountability actbetter knows as HIPAAwhich has a lot to dowith privacy regulations in medicine.![23](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 15.29.23.png)

HIPAA requires that a lot of different information,about 17 major variables need to be anonymizedor aggregated.For instance, you can't report a person's age,or you can't give their birthdate,you can simply say how many years old they are.If they're over 89, you just have to say they're over 89.You can't give the zip code, you can only give the stateand so it becomes much larger groupsand much harder to identify people.Other research by Latanya Sweeney has showedthat when you remove the HIPAA-protected information,and so that's only four one hundredth of a percentof the people.

For comparison purposes, the probabilityof getting strucked by a lightning is about oneout of 10,000,so it's in the same vicinity as that at risk.Similarly, law professor Paul Ohm has shownthat re-identifying people in anonymized data setis enormously difficult.![47](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 15.30.47.png) It requires, what he calls massive statisticaland data management skills.The point here is while it can be done,it's very hard to do it.As Professor Sweeney has shown,if the information is properly anonymized,it's nearly impossible to identify people.

The point of these examples is not to encourage paranoiabut rather to point out that care needs to be takenwhen we're working with big data,especially when personally identifiable informationis present, in order to ensure privacy.Anonymization is a start but it requires some thoughtand care to be done well,and if it is done well, it is still possible to provideservices and conduct research without crossing the lineinto creepiness or into legal trouble.

### Challenges with confidentiality

In our last movie, we talked about the imporanceand the difficulty of protecting personally identifiableinformation through anonymity in big data.Now, anonymity means that individuals cannot be identified.Another important element of privacy, however,is confidentiality for what's called nonpublic information.![45](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 15.32.45.png)

In its simplest form, confidentiality means thatregardless of whether individuals can be identifiedwithin the data, their data will not be sharedwith people they did not specifically allow to see it.Confidentiality's an issue of trustthat makes interactions possible.

For instance, I have given my credit card informationto several online companies because one,it makes interactions with them much easierif that information is already stored,and two, I feel confident that they'llkeep that information private.There are several exceptions and limits to confidentiality,however, that need to be discussed.The first is that in conducting transactions,companies do share limited amounts of informationwith third parties.For example, if a person goes to make a large purchase,it's not uncommon for the vendor to call the bankand ask whether the person has enough moneyin the bank to make that purchase.![35](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 15.40.35.png)

They're just checking for what's called sufficient funds.And all the bank does is tell them yes or no.And so there's a sharing of a very smallamount of information, but the bank does not pass alongthe person's account numbers, their ID information,doesn't give them their actual balance;just says whether they have enoughto cover a particular transaction.On the other hand, it is also sometimes the casethat information is stolen from companies.Several companies have had their data stolen,including credit card information, addresses,and other important personal information.

And in some cases, companies have lost hundreds of millions of dollars in business because consumers were no longer confident that their information would be safe.Similarly, another limitation to confidentialityis that companies sometimes had to give their informationto courts or government regulatorsas part of law suits that could've put themout of business completely if they did notprovide the information.It's a very awkward situation,but it does come up occasionally.The trick with that one is while it is a legal process,it is not something that the users originally agreed to,and so there is a violation of trusteven if what's happening is technically a legal process.

Now these exceptions don't call fora complete lockdown on data because the datadoes provide very important services,but it does call for more care and attention.So for example, the National Science Foundationand the National Institutes of Healthhave instituted policies that researchers have topresent a plan to provide access to their datathey use in their studies.Additionally, there are insurance companiesthat now provide insurance for the cost of data breachesand companies should consider whether they wantto purchase that kind of insurance.

It's still relatively uncommon,but it is available. ![47](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 15.44.47.png)And finally, companies should very carefully consider whether they even need to havethe confidential information in the first place.The point here is, you can't lose somethingif you don't have it to begin with.And so a company should consider the actual servicesthey provide and whether that information's important.I can example a scenario, for instance,in which a new life insurance companymay want the access to medical records, maybe.But it's much harder to imagine a scenarioin which it would be appropriate for a credit card companyto have that kind of information.

And so it's clear that things can, and occasionally do,go very wrong when data is supposed to be confidential.But again, this doesn't call for a complete avoidance of data with non-public information in it.After all, that's what makes things likerestaurant and movie recommendations work so well,and it's certainly important for using big datato make medical discoveries.Some of these benefits are of personal conveniencesand could theoretically be forgone,but others have life and death consequencesand deserve to be maintained.For these reasons, it's important for companies to considerhow they're going to deal with non-public information.

That way, the trust of regular people,who are the consumers and people who benefitfrom big data research,the trust can be maintained and big datacan provide its full benefits.

##### Chapter Quiz

###### Question 1 of 1

###### Although people want access to quality research, what is it that people do not want?

- People do not want their families to know.
- People do not want to know any of this.
- People do not want to read data for a long time.
- **People do not want their private information to become public.** Over the last several years, there have been severe consequences to breaches of privacy, whether accidental or intentional.

## 5. Sources and Structures of Big Data

### Human-generated data

Big data can come from several different sources.Now, one way to think about it is whetherthe data was produced by a humanor whether it was produced by a machine.We humans generate a lot of datawhether we mean to or not.That's what we're going to cover in this movie.This first thing I want to talk about is intentional data.This is data that you know you are creating,so for instance, if you take photos, videos,or record audio or put text on a social network,you know you're doing it.You can also click "like" if you're on Facebook.When you do web searches, a record of theweb pages that you have viewed are bookmarked.![08](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 15.52.08.png)

![28](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 15.53.28.png)

Your emails and your text messages.Your cell phone calls.If you read an eBook, the highlights, the notesin the bookmarks and online purchases.All of these are kinds of data that do not existuntil the person deliberately makes them happen,so these are records of human actions.What's interesting about it is, in addition to theseintentional pieces of information,there's also meta data.Now, meta data is data about data.You might call this second orderhuman generated data.![05](../Desktop/Screen Shot 2018-09-19 at 15.58.05.png)

![05](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-19 at 15.58.05.png)

Now, that's my own term.I made that one up.But the idea here is this is data that accompaniesthe things that you do,and you may not be aware of it.What's funny is that the meta data, first off,can be enormous, sometimes larger than the actualpiece of data you created, and most significantlyfor the big data world, meta data, because it'scomputer generated, is alreadymachine readable and searchable.I want to show you some of the things that showup in meta data and what can be done with it.

A really simple one is in photographs.So, for instance, if you take apicture with your phone, you not only getthe picture, you also getwhat's called the **EXIF data.That stands for exchangeable image file format**,and this is the meta data that comes froma picture on an iPhone.![05](../Desktop/Screen Shot 2018-09-19 at 16.00.05.png)Now, aside from the name of the file whichyou see at the top left and that it's 3.1 megabytes,and the time that it was taken, near the bottomon the right side, you see the GPS altitude, latitude,longitude and position, or partway up from that,you'll even see the GPS image direction.

It knows which way you're holding the camera.This is an enormous amount of informationthat accompanies the photo that you get.Another interesting thing is cell phone meta data. Now, this is information that is not normallypublicly available, and so this reallyis talking about sort of an academic interest here,but the idea is that there's a lot of informationthat accompanies your phone call,and without even knowing who you're callingor what you said on the phone call, two pieces of information: knowing the time ofthe phone call and the location.

![51](../Desktop/Screen Shot 2018-09-19 at 16.01.51.png)

What's interesting is that with four of thesepieces of data, or rather, four calls where youknow the time and the position,in an anonymized data set, that's enough informationto identify 95% of individuals.Again, I'd like to emphasize that this isinformation that is not publicly available,but the point here is, is that it's possible to tella lot about people by the meta data.Another one is email meta data.Now, there's a lot of information that accompanieseach email, but four very common pieces are:who's it from, who's it going to,did they CC anybody, carbon copy anybody,and the time that it was sent.![30](../Desktop/Screen Shot 2018-09-19 at 16.03.30.png)

Now, one really interesting thing about thisthat you can do for yourself is that MIThas created a web app called Immersionthat allows you to do a quick analysisof your own social network via your email account.I'm going to show you the Immersion website. ![08](../Desktop/Screen Shot 2018-09-19 at 16.04.08.png)It's immersion dot media dot mit dot edu,and what it does is, it takes those four piecesof information about your emails and it putstogether an image of the network,and I've done this for myself,and it's absolutely fascinating.

It takes a few minutes and you have to refreshit to get it up to date, but what I'm going to dofor this example, is I'm going to come down hereto the Immersion demo, so this is fictional data,but this is what yours would look like if you did it.Tony Stark is not at MIT.What here we have is a fictionalized analysisof what his information would look like withsix years of emails, 20,000 emails to159 collaborators, and what you can seeis who is in his group.We have more to Travis than anybody else.

It looks like Travis is connected with Tabitha,and you can change, for instance, how things are distributed over here.The number of notes that show, now we have moreand more people showing up. ![49](../Desktop/Screen Shot 2018-09-19 at 21.16.49.png)We can make that a little bit smaller,and the strength of the links between them, see,so now nobody's connected,and now everybody is connected,but what's interesting about it is,I know, for instance, when I do it,I have a distinct group that shows for my family.I have another distinct groupthat shows up for my job.I have another distinct group that shows upfor the people I work with here at Lynda.com,another group for a nonprofit I worked with,and it's funny to see, for instance,that there are sometimes people who connectseveral of those groups at once,but the interesting thing again,this is just based on who you sent it to,who it was from, the CCs, the time and the date,and that's how it's able to reconstructyour own personal social network.![12](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 00.09.12.png)

The last thing I want to show youis about Twitter.Now, one of the interesting things about Twitter,aside from the fact it's a very popular social networkis, tweets are very small. ![28](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 00.09.28.png)They're limited to 140 characters.What's interesting about this from a researchpoint of view, is there's an enormous amount ofmeta data that accompanies each tweet,so I'm going to go to an article here called"What's (technically in your tweets?",and scroll down a little bit,and I'm going to zoom in on this image. ![38](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 00.09.38.png)Now, this was put together by anemployee at Twitter, Raffi Krikorian.I'm going to make that a little bigger here.

Let's go up to the top here.This information in the red,that is the content of the tweet.That's the stuff that you meant to put there,but look at all this otherinformation that accompanies itin terms of whether there was a reply,a truncated version, the author's screen nameand URL, the location, I like this renderinginformation, the creation data, the account,the number of followers, the time zone,their language, whether they have a verified badge,the place ID, the URL, the country,the bounding box, the application they sent it.

It's an enormous amount of information.Several times, the meta data in this case is severaltimes greater than the actual content that it's about.This is one of the most interesting things,and this is why Twitter in particular is a veryrich data set for people who are doing marketingresearch or social connection research.Anyhow, the point of this is that theseare all sources of big data, and one of the interestingthings about it is that the meta data in particulardoes not have to be processed.It's already computer readable.

It's searchable.It's mindable, and you can startto get information about it immediatelyto reach your big data analysis purposes.

### Machine-generated data

In T.S. Eliot's poem, The Love Songof J. Alfred Prufrock, he has the lineI have heard the mermaid singing,each to each, I do not think they will sing to me.I bring this up because it has been estimatedthat as much as 95 percent of the world's datawill never be seen by human eyes.Much of this unseen data is calledM to M data or machine to machine.The machines are talking to eachother not to be heard by the humans.Just like Prufrock's mermaids.Now, let me talk about some of thesources of machine generated data.There's a very long list, thisis not meant to be comprehensive,but things like when the cell phonesping to the cell towers to check where they are,when the satellite radio and the GPS connectto locate the car or your phone, the RFIDor radio frequency identification tag readingson billions of small objects, readings frommedical devices and web crawlers and spam bots.![31](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 00.14.31.png)

It's especially fun to think about theelectronic spam bots being stopped by theelectronic spam filters, each working against another.Perhaps the most interesting part of themachine to machine communications fallsunder the rubric of the **Internet of Things,sometimes just called IoT**.Now, it's estimated that by 2020,which is only a few years from now,as many as 30 billion uniquely identifiabledevices may be connected to the internet.This actually requires a major change inhow the internet works it's addressing systemfor all of these things to fit, but basically,everything will have a chip and it will beconnected to the internet and they'll betalking to each other, sharing information.![55](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 00.16.55.png)

So when you hear people talk about smart sensors,in your home or in your city or on yourair conditioning or the smart home,which knows when to turn lights onor change the temperature, or the smart gridswhere the city generates and sends out the electricityor the smart city itself which coordinatesall of the traffic and the utilitiesas a way of being more efficient and moreeconomical in providing better service.All of this would be enabled bysmall objects communicating one with anotherin the internet of things, they communicatedirectly and not with a human an intermediary.

Some of the uses for this can includeputting sensors on production linesto monitor systems for when they need maintenance,or the smart meters on utility systemsto shut them off at peek times, if theycan do it without interrupting service.![30](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 11.01.30.png)

My dog has a little chip and it's underit's skin as a way of identifying pets,also for farm animals, tracking them through systems,thermostats and light bulbs, you can actuallyget your iPhone controlled light bulbs now,or just environmental monitoring,that can include things like air and water quality,atmospheric or soil conditions, movements of wildlife,earth quakes and tsunami early warning systems.![59](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 11.02.59.png)

Also things like infrastructure management,that talks about control and monitoringof bridges, railways, wind farms, traffic systems.Industrial applications like manufacturingprocess controls, supply chain network,having predictive maintenance or integrationwith a smart grid to optimize energy consumption.There's energy management, that's the switchesand outlets and bulbs and TVs and screensand heating systems, controllingovens, changing lighting conditions.And then, medical and healthcare systems.

Building and home automation, transport sytems.Basically anything that's mechanicalcan be eventually hooked up andcommunicating through the internet of things.All of which generates an enormousamount of data as they talk one toanother and coordinate their own activities.So, in looking at the differences betweenmachine generated data and human generated data,which we talked about in the last movie,the most obvious difference is that the machinesdon't generally post selfies on Facebook,they don't make silly videos on YouTube,they don't write job applications andput them on LinkedIn, and so, the contentis different, but what is interesting is that contentmay not be the most important difference.

Instead, the most important distinguishing featureof machine generated data may be that all of themachine generated data is machine readable.It can be immediately searched and read and mined.It's high on volume and velocity,two of the characteristics of big data,but low on variety, which makes iteasier for machines to deal with it.And that brings up the important distinctionbetween what's called structured, unstructuredand semi-structured data, and that'swhat we'll discuss in the next set of videos.

### Structured data

Data is said to be structuredwhen it's placed in a file with fixed fields or variables.The most familiar example of this kind of structureddatabase is a spreadsheet. ![09](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 11.05.09.png)Where every column is a variableand every row is a case or observation.In the business world however,large data sets are usually stored in databases.Relational databases to be specific,which share some characteristics with spreadsheetssuch as rows and columns,but allow for much larger data sets,more flexibility, and more constancy.A recent survey of database users found thatnearly 80 percent use some form of relational databasewith Microsoft SQL server, MySQL, and Oracleas the most common options.

Now, before I say anymore,I need to give you a very brief history of SQL databases. In the early 70's researchers at IBMwrote a paper describing theStructured English Query Languageor SQL written as the word.Name was later changed to SQL because of a copyright issue,but it's still generally pronounced “sequel”. ![29](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 11.07.29.png)IBM however did not commercially launch SQL.That happened in the late 70's by a relational software inc,which later became Oracle,which is still one of the biggest providersof database software in the world.

Oracle is also well known for making one of it's co-foundersLarry Ellison, one of the richest people in the world.Now, what SQL does,is it makes it easy to extract, count and sort data,create unions in the intersection between sets.It's also used to add, update and delete data.And it does this all in a language that's mucheasier to manage than the mouse-driven clicks and selections of a spreadsheet.For example, if a university has a database of student information, than a SQL command to get the gender, college, department and major of the students might be written this way,Select, that's a function, and then you say the four fields or variables that you want, gender,college, department and major.  **SQL SELECT STATEMENT 1** **SELECT gender,college,department,majorFROM Students;** ![45](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 11.11.45.png)

And from, another function,is coming from a table called students.If you want to make it slightly more elaborate,you can specify students over the age of 25using the where statement or command.So again, we have a single sentence here.Select, these four fields, gender, college, department,major, from the table students, where the value in thefield age is greater than 25. ![53](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 11.12.53.png)And again finish with a semicolon.Now there's a whole lot more that can be saidabout structured data and SQL databases,but it'd be better to direct you towards some of theexcellent courses that lynda.com has on these topics.

These include, Foundations of Programming Databases,Foundations of Programming Data Structures,SQL Essential Training and MySQL Essential Training.And with that, we'll turn to the compliments ofstructured data and SQL,unstructured and semi-structured data,and no SQL databases.

### Unstructured data

In the last movie, we talked about structured data,which usually means data that's placed in a filewith fixed fields, such as a spreadsheetor relational database.For example, here's a table with basic dataabout a few sports teams. ![03](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 11.14.03.png)We have a column to indicate the sport,and we have a second columnto indicate the name of the team,and each team gets one row.This is just like you would get out of an Excel spreadsheet.In fact, I copied and pasted it out of there,and that's how you would format it.Easy to deal with.On the other hand,there's also unstructured data or text.If you were to write this in a report,you might say something like,"Two prominent soccer teams in Europe"are Manchester United and FC Barcelona."And "Two NFL football teams in America"are the Oakland Raiders and the Tennessee Titans." ![01](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 11.15.01.png)Now, while this data is easy for a person to understand,it's much more difficult for a machine to understand.

It's not easy to sort this kind of data.It's hard to rearrange it.It's hard to count the values,and it's hard to add more observations.So this is an example of unstructured data,that's data that's not in fixed fields and text documents,presentations, images, video, audio, PDFs,what have you, all go into this.And it may be the majority of data in business settings.I've seen estimates anywhere from about 45 percentup to as much as 80 percentof business data may be unstructured.

It's a little hard to deal with. ![40](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 11.16.40.png)You may have to convert it to textand then use a text-mining program to try to get structureout of the sentences of data,but that's difficult, and it's time consuming to do.On the other hand, data doesn’t have to beeither structured in a spreadsheet or unstructured in text.A third option is available,and that's semi-structured data.Now, semi-structured data is datathat's not in fixed fields.So it's not the rows and columns of a spreadsheet,but the fields are still marked,and the data are still identifiable.

Now two common formats for semi-structured data,they're not the only ones, but the most commonare XML, which stands for Extensible Markup Language,and JSON for Javascript Object Notation.![53](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 11.17.53.png)Let me show you what the sports data would look like in XML.What we need to do is have a series of bracketsthat indicate what information is being shown at the moment.![39](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 11.18.39.png)The first set of brackets indicatesthat we're gonna talk about sports.And then the value in that field is soccer,and then we're going to break it down to two teamsin which we would have an opening bracketfor each one that says team,and then a closing bracket with the slashto indicate we're done talking about that team.

And if you've seen HTML, it looks similar.And it goes through sort in a nesting and winding format.What this shows is that the semi-structured data formatof XML or others is really good for nested dataor hierarchical structures,whereas trying to show it in a spreadsheet,you end up having to repeat a lot of the information.This avoids the repetition,and so it's actually more efficient in that sense.On the other hand, XML is a slightly older format,and it's a little wordy.

A more recent development is JSON,or the JavaScript Object Notation,and JSON has a similar feel to it,but there's not as much text.![03](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 11.20.03.png)We still have the brackets.We have curly brackets to start our thing,and then we put the names of the fieldsand the values in quotes,but you can see the same kind of in-and-out structurethat we had before.Now, a nice thing about this is you can also write it as a single line.![49](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 11.20.49.png)And now you can see that it's more compact,and this allows you to indicate, again,the hierarchical or nested nature of the data,without having to repeat informationthe way that we did in the original spreadsheet.

The next thing we wanna talk about,once we've discussed unstructured and semi-structured data,is the databases that you can store the information in,as opposed to the SQL databases that are usedfor structured data with rows and columns.Semi-structured and unstructured datausually go into go into what are called NoSQL databases.That used to mean not SQL,but now it means not only SQL,because NoSQL databases are extremely flexibleand can handle a wide range of data formats.So most of them use a semi-structured format.

For instance, the most common NoSQL databaseis MongoDB that uses JSON.It's nice because it's a flexible structure,and for certain tasks, a NoSQL databasecan be much faster than a SQL database. ![00](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 14.25.00.png)On the other hand, they haven't been adopted as widelyas relational databases.For instance, the survey that I mentioned in the last moviesaid that about 79 percentof companies had used relational databases.Whereas only about 16 percent hadadopted NoSQL databases.

On the other hand, if you're lookingat the sheer volume,because Hadoop, which we'll mention a little bit later,is a NoSQL database,and almost all big data is installedin Hadoop or Mongo database.Even though there's fewer by head count,an enormous amount of data is installed in that format.Now one of the big problems is thatwhereas the SQL databases all useat least relatively standardized versionsof the SQL query language,there is no standardized query languagefor NoSQL databases, and it means as you switch from oneto the other, you may have to learn all over againhow to work with it.

That's a problem,but on the other hand, the NoSQL databasesare an area of huge development,and I imagine that will get resolved pretty quickly.In the mean time,if you'd like to learn more aboutunstructured or semi-structured data or NoSQL databases,**lynda.com has a great set of courses you can work with.Up and Running with NoSQL Databases,XML Essential Training,Working with Data on the Web,Real-World XML,and JavaScript and JSON**And those will give you a good feelfor what's possible with these more flexibleand more recently developed formats,especially as you can apply them to web data and big data.

###### Chapter Quiz

###### Question 1 of 2

##### Human-generated data may be _____ than the computer-generated metadata that accompanies it.

- **smaller**
- faster
- larger
- prettier

##### Question 2 of 2

###### As much as _____% of the world's data will never be seen by human eyes.

- 25
- 15
- 40
- **95**

### 6. Storing Big Data

### Distributed storage and the cloud

Big data is defined byvolume, velocity, and variety.The first of these characteristics, volume,makes it difficult to store data on a single drive.As a result, distributed storage,which means storing data across more than one computer,has become a necessity.In a traditional storage system,data on a disk is stored in blocks.Each block contains the 0's and 1'sthat make the bytes of letters and numbers.Storage data also includes error correction code,which you use to verify the integrity of storage data.If your data set's become too large for your computer drive,then adding an extra drive is an easy solution.

For example, I have four external drivesroutinely hooked up to my laptop,each of which gives me extra space,and each of which serves a particular function.While this approach can work to a certain extent,it has limitations.A) They're only attached to your computer.B) They're all in the same physical space,so if your house burns down you lose everything at once.C) There's usually only one copy,that is, the information is not necessarily redundant.And D) it doesn't do anything aboutsharing the documents with other people.Also, if a drive goes bad,like my main backup drive did last month,then it can stop everything for a whilewhile you sort it out.

As a result, simply adding external drivesto your own computer is not the ideal solution.For many years, the best solutionto the one computer problem,was to create a storage area network,or S-A-N, or SAN.![Image result for SAN](http://tvmlogic.com/images/SAN.jpg)

SANs are large and expensive collectionsof disk drives on racks.They have a lot of nice features, though.They can be spread out across a large geographical area.They include redundancy, so informationis always written onto more than one drive,and they're relatively easy to service,by allowing you to replace a faulty drivewithout shutting the whole thing off.

On the other hand, SANs can be very expensive to set up,and can take a lot of skilled labor to maintain.As a result, many companies have lookedfor workable alternatives.Over the last few years, cloud storage,or storage over the internet,has become not just a viable option,but the preferred method.Cloud storage is attractive, especially for big data,because the storage space is scalable.That is, it can be rented on an as-needed basis.There's no real up-front costfor installation or maintenance,and the level of redundancy that cloud providers can offermakes data nearly impossible to lose or damage. ![32](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 14.50.32.png)

You can think of it as an industrial-strength versionof services such as Box or Dropbox or Google Drive.Now, perhaps the most popular cloud storage vendor,but far from the only one, is Amazon,and they have the Simple Storage Service,better known as Amazon S3.With services like Amazon's, it's possible to storeessentially an unlimited amount of data.For instance, that's where Netflixstores all of their movies.It's also possible to tailor cloud storagefor things like scalability, how much storage do you need;redundancy, how many backup copies do you want to havein case something goes wrong;or speed, how fast you want to be ableto pull the information out.

That can include, for instance, whether it's storedon hard disk drives, or whether it's storedon solid state drives.Obviously, faster, more secure, means more money.On the other hand, research has also shownthat most data, once it's written,is never accessed again,and this makes some of the moreeconomical strategies attractive.For instance, there are deep freeze solutions.Amazon has something called Glacier.Other people have similar programsthat are much cheaper, but the data needsa few hours notice before it can be pulled out.Now, the point of this is that as data growsfrom conventional formats to become big data,the storage problems multiply.

It becomes necessary to store the dataacross multiple drives, multiple computers,as well as to work to make the data secure.The costs and physical trouble can become overwhelming.So big data companies have turned to cloud storage providersto solve these problems.What's interesting is that cloud providersare able to do more than just provide storage,and that's what we'll look at in the next movie.

### Cloud computing: IaaS, PaaS, SaaS, and DaaS

- Cloud computing means, computer servicesthat are delivered over the internetinstead of on your own computer.The most common services in cloud computingare infrastructure as a service, or IaaS,platform as a service, PaaS, software as a service, Saas.And because this course is about Big Data,I will also mention data as a service, or Daas.Infrastructure as a service is an online versionof the physical hardware of computer, which is whyit's also sometimes called hardware as service,It can be thought of as the hosting layer.It includes the disk drive, servers,memory and network connections.

For example, in the last moviewe talked about online storage.And that would be one element of IaaSOn the other hand, that part where we discussed storagedidn't include the availability of computer chips, or RAM.If you need access to hundreds ofterabytes of storage space, hundreds of gigabytes of RAM,and super high speed network connections,then an IaaS service would be a great way to go.This can save an organization an immense amountof money and time on purchasingand maintaining their own machines.What makes IaaS possible is virtualization,that is software that allows one computerto run multiple operating systems at the same time,similar to how software like Parallels Desktop makes itpossible for me to run Windows and Linux on my Mac.

These are called virtual machines.Amazon, Microsoft, VMWare, Rackspace, Red Hat, those arethe biggest players in infrastructure as a service.The next step us from this isPaaS, or platform as a service.This can be thought of as the building layerbecause this is something that developers useto build applications that run on the web.PaaS includes the middle layer software,like the operating system, and the other componentslike the Java run time in the middleware, that allowhigher level software to run, like web basedapplications that use the dot net,that's the Microsoft program, or the Java.

PaaS also gives access to databases like Oracle,Hadoop, and application servers like,Web Logic, Microsoft IIS, and Tomcat.Force.com, which supports sales force, a verycommon sales application, and Google's App Engineare well known examples of PaaS.PaaS is a low-cost way to get started, plus itprovides for limitless growth for a new company,or an existing company as it ramps it's application upwithout having to buy their own hardwareor pay software vendor licenses.It is however, a level of computingthat most users will never touch.

The next step up from that is SaaS, or software as service.This is the top layer for most people.It can be thought of as the consumer layer of crowd computing.It includes web applications that runentirely through the browser like Gmailand Google Driver Docs, Office 365, Salesforce,Quicken.com, and Mint.com, and so on.The point with this market is that it's easier to useSaaS, which is ready to go, than install your own software,which could take hours, days, or even longer.![51](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 15.16.51.png)

It also makes it possible to use cheap netbookslike Chromebooks, where everything's done over the web.I have a couple of Chromebooks.I love them.The next thing I want to talk aboutis DaaS, or data as a service.This is the final layer of cloud computingthat we'll discuss in this movie.Please note, it's not to be confused withdesktop as a service, which is another more common SaaS.Data as a service is an online service like the others,except instead of providing online accessto computing hardware, operating systems,or applications, it provides access to data.For this reason, DaaS providers are similarto what are called data market places or data marts.

And the idea is that DaaS providers can provideimportant services by allowing customersto get access to data quickly and affordably,while assuring data quality.For instance, in the previous movie I talked abouthow market researchers can buy demographic informationabout their clientele and match it up withwhat they have in their own records.That's an example of DaaS.Or for instance, there are companies that have a recordof every tweet ever sent and you can buy access to that.That's another example of DaaS.

Other companies include for instance, Factual.com,and Infochimps, are in the same market,although it still looks like the market's kind of wide openin terms of what is available and what can be provided.The collection of cloud computing services that wediscussed in this movie, infrastructure as a service,platform as a service, software as a service,and data as a service, they can all playimportant roles in Big Data projects.Either by providing the physical resources necessaryto store and process the data, the software to interactwith the data, or even the data itself.

What they all have in common is the ability to shiftthe load off the consumer business and allow theminstead to dedicate their own resources, their money,space, time and energy, to working with the dataand getting the insight they needfor their own projects and progress.

### A brief introduction to Hadoop

Any discussion of big data willinvariably lead to a mention of Hadoop.Hadoop's a very common, a very powerful platformfor working with data, but it can be a little hardto get a grip exactly on what it is and what it does.This movie is designed to give the briefest possibleintroduction to Hadoop, which could benefitfrom several courses all on its own,and with that, here is the bare minimum on Hadoop.The very first question is, what is Hadoop?It sounds like it's a untranslatable word forbig data or for transformative business practice.Instead, Hadoop was the name for the stuffedanimal that belonged to the sonof one of the developers.

It was a stuffed elephant,which explains the logo as well.But what is Hadoop, and what does it do?![53](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 15.49.53.png)Most significantly, Hadoop is not a single thing.It's a collection of software applications thatare used to work with big data.It's a framework or platform that consistsof several different modules.Perhaps the most important part of **Hadoop is theHadoop distributed file system, or HDFS,and what this does, is it takes a piece of information,it takes a collection of information, and spreadsit across a bunch of computers.**

It can be dozens or hundredsor tens of thousands, in certain cases,so, it's not a database, because a database usuallyimplies a single file, especially if you're talkingabout a relational database,it's a single file with rows and columns.Hadoop can have hundreds or millions ofseparate files that are spread acrossthese computers and all connected throughthe software to each other.MapReduce is another critical part of Hadoop.![04](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 15.53.04.png)What this is, is it's a process consisting of mappingand reducing, and it's a little counterintuitive,but here's how it works.

Map means to take a task and to take the dataand to split it into many pieces,and you do that because you want to send it outto various computers and each one can onlyhandle so much information, so let's say you have100 gigabytes of information and each of yourcomputers has 16 gigabytes of RAM, you're goingto need to split it up into 60 or 70 different pieces,and send it out to each of those differentcomputers that you're renting from AmazonWeb Services or wherever.Map splits it up and sends it out to workin parallel on these different computers.

The reduce process takes the results of thoseanalyses that you've done on each of these dozensof different computers and combines the outputto give a singe result.Now, the original MapReduce program has beenreplaced by a patchy Hadoop YARN,which stands for Yet Another Resource Negotiator.Sometimes people just call it MapReduce two,and YARN allows a lot of thingsthat the original MapReduce couldn't do.The original MapReduce did batch processing,which meant you had to get everything togetherat once, you split it out at once, you waiteduntil it was done, and then you got your result.

YARN can do batch processing,but it also can do stream processing,which means things are coming inas fast as possible and going out simultaneously,and it can also do graph processing,which is social network connections.That's a special kind of data.Next is Pig.Pig is a platform in Hadoop that's usedto write MapReduce programs,the process by which you split things upand then gather back the results and combine them.It uses its own language.It's called the Pig Latin Programming Language.Probably the fourth major component of Hadoopthat is most frequently used is called Hive,and Hive summarizes queries and analyzesthe data that's in Hadoop.

It uses a SQL-like language called HiveQLfor query language, and this is the one that mostpeople are going to use in terms of how to actuallywork with the data, so between the Hadoopdistributed file system and the MapReduce or YARN,and Pig and Hive, you've covered most of whatpeople use when they're using Hadoop.On the other hand, there are othercomponents that are available.For instance, HBase is a no SQL database,so a nonrelational database, or not onlySQL database for Hadoop.

Storm allows the processing ofstreaming data in Hadoop.Spark allows in memory processing.This is actually a big deal becauseit means you're taking things off of the harddrive and putting them into the RAM ofyour computer, which is much, much faster.In fact, in memory processing can be a hundredtimes faster than on disk processing,although you do have to get through the processof putting the information into the RAM,which usually isn't countedwhen people are doing these statistics.Spark is often used with Shark,something that enables the in memory processing.

And then there's Giraph, spelled like graphwith an i, which is used for analyzing thegraph for the social network data.Now, there are maybe 150 different projectsthat can all relate to Hadoop.These are just some of the major players.So the question also is, where does Hadoop go?It can be installed in any computer.You can put it on your laptop if you want.In fact, a lot of people do so they cansort of practice with it and get things set up,and then send it out to the cloud computing platform,and in fact, that's where it usually is.

Cloud computing providers, Amazon Web Services isthe most common, but Microsoft Azure hasa form of Hadoop that they use, and there area lot of other providers that allow you to installHadoop and run it on their computer systems.Who uses Hadoop?Basically anybody with big data.Yahoo!, not surprisingly, because they developedit, is the single biggest user of Hadoop.They have over 42,000 nodes running Hadoop,which is sort of mind-bogglingly huge.LinkedIn uses a huge amount.

Facebook uses a bunch,and Quantcast, which is an online marketinganalysis company, has a huge installation as well,and there's a lot of others.Finally, it's worth pointing out that **Hadoop is open source.While it was developed by engineers at Yahoo!,it's now an open source project from Apache.So you'll often hear it called Apache Hadoop,or Apache Hive, or Apache Pig.One of the things about open sourceprojects like this is it's free, which explainsin part its popularity.Also, anyone can download the source codeand can modify it, which explains so manyof the modifications or the extensionsor the programs that work along with Hadoopthat make the most of its capabilities**

The takeaway message of this presentation isHadoop is not just one thing, but a collectionof things that collectively make it much easierto work with big data, especially when its usedon a cloud computing setup.Hadoop is extremely popular in the big data world,and there's very, very active development for Hadoop,but there's also very stiff competition for the market.Not everybody is just willing to stand byand let Hadoop have everything.This should make it a very exciting situationfor companies and consumers who wantthe best tools for working with theirbig data projects.

###### Chapter Quiz

###### Question 1 of 1

##### Cloud storage is _____. This means it can be rented on an as-needed basis, without up-front costs for installation or maintenance.

- free
- **scalable**
- cloudy
- confusing

## 7. Preparing Data for Analysis

### Challenges with data quality

In any data project the quality ofthe data play a critical role.In big data, however, quality is even harder todeal with because the data often originated outsideof the immediate project and willhave a life of its own beyond it.The researcher doesn't have complete control overthe data in the same way that they wouldwith a standard small data project.Consider for a moment that much of the data thatgoes into a big data project mayhave once come from spreadsheets.Some researchers have found that **nearly 95% of spreadsheets they examined had errors in them.** And it falls back on the familiar expression fromcomputer science GIGO, for garbage in, garbage out.

Data can have these problems, and even if youhave Hadoop, even if you've got this tremendouslysophisticated analysis, if you're starting withbad data you're going to end up with bad results.Now, this gets back to our concept.We want to make sure we have good data to start withso we can have a defensible and informative result.Let me go over very quickly some of the things thatcould be challenges in terms of the quality of the data.

The first is **incomplete or corrupted data records.** This can lead to what's called NULL pointerswhere the computer is pointing or lookingin a space where there's nothing there.The first is incomplete or corrupted data records.This can lead to what are called NULL pointersin which the expected information isn't thereor it can lead to attempts to divide by zero,which can actually cause the computer to crash.

You can have **duplicate records**, which means the same person, for example, is appearing in more than one place and that explains why I get three postcards from the same organization each time they do a mailing.

You can have **typographical errors in text and numbers.** So for instance, you may accidentally enter a numberincorrectly with the wrong number of zeros,too many or too few and it canthrow things off dramatically.

You can have **data that'ss missing context or ismissing measurement information,such as the units of measurement.** You may recall the Mars climate orbiter that NASA launched back in 1998 at a cost of nearly $300 millionand it crashed when it approached Mars a year later because some of the flight programming data had not been converted to metric units. so very embarrassing to not accurately specify the units that you're dealing with and can avoid very costly and time consuming errors.

And there's also **the issue of  incomplete transformations of data**Some of the information may have, for instance,I know in psychology sometimes we reverse codeinformation if people are answering it manually.You flip it around, but it's not always indicatedwhether it got flipped around and that's a horriblemess because then you usually have to throw outthe data and that's something that you usuallycannot afford to do in a big data project.Now all of these issues are problems in a smalldata project, but they become evenbigger in a big data project.

They become qualitatively different animals.Now part of the problem with big data is that **normal methods for checking the accuracy of the data may not be present** because, for instance, the person who gathered the data isn't the same person who's analyzing or presenting it.Also **if the data stays in Hadoop the whole time,it may not need to be pulled out and converted.** We're going to talk about that in the next movie.And **if it's not converted, it may not be examined,and so there's a potential of a space that gets missed in terms of what you're looking for**.All of these issues are problems in a small data project,but they become much more significant in big data.

And what all of this leads us to is the importanceof carefully examining the data at each step,especially if you're bringing any of it out andtransforming it, which leads us to the extraction, transformand load step which we'll talk about in the next movie.

### ETL: Extract, transform, load

**ETL stands for extract, transform and load.** This is a term that developed from data warehousing,where data typically resided in one or more large storage systems or data warehouses,but wasn't analyzed there.Instead, the data had to be pulled out of storage,that's the extract stage, and then it had to be converted to the appropriate format for analyses and especially if you're pulling data from several different sources, which may be in different formats,so you transform it.And then once it's ready, you then have to load itas a separate step into the analyses software. **Etract :- the process of pulling data from storage such as data base**     **Transform:- The process of putting all data in to a common format** **Load:- the process of loading data in to software for analysis**

Each of these steps involve significant time.In fact there are several software vendorswho made most of their money from selling softwarethat facilitated the ETL process,when dealing with data warehouses.And just think for a second of documents that maybe stored in several different formats.So for instance, if you're looking at text documents,they can be in Microsoft Word files,they can be in HTML webpages, they can be in e-mails,or PDF's, or any number of formats that you get. ![09](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-21 at 22.15.09.png)What you might have to do though is if you want to dealwith the text, is you have to transform all of theminto a single common format so you can do all your workon them simultaneously.

So for instance, one common one with textis to convert it to plain text, a dot txt file.That's wonderful because basicallyanything in the world can read a text file.But the problem is that you lose all the formatting,and formatting sometimes carries important information.Let alone the fact that you lose picturesand things like that.So you may want to use a different format.Markdown formatting which is based on text but hascodes or indicators for formatting,may be an acceptable alternative.But is something that you just have to considerhow are you going to combine things,what information is vital to keep and what informationcan you afford to lose in the process?Now the funny thing about Big Datais the ETL extract, transform and load processjust works differently in Big Data.

And this has to do with the effect of Hadoop.Because the data, for instance, starts and ends in Hadoop.It is not taken from one system to another.It's always in the same system.Now it's true that you're moving it from one sort ofpart of the system to another,but the fact that it is staying in the same general system,really changes the extracting and loading process.Moreover, Hadoop can handle different data formats.It can handle unstructured datain a lot of different sources.

And so the transformation process,is also very different when dealing with Hadoop.Now, a funny thing about this,aside from the fact that it makes life a lot easier,is that when you're dealing with Hadoop,you don't have to be so aware of the extract,transform, load process because it doesn't really happen in quite the same way. ![41](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-22 at 00.48.41.png)So there's not so much inspection of the data,you don't have to think about it so deliberatelyto solve these problems.It doesn't force you to think about it.On the other hand, what's funny about that isyou really miss some opportunities to better understandyour data and to check for errors along the way.

And so Hadoop has the ironic situation of making your lifemuch easier, but sometimes you need to make your lifea little harder and make it a point to deliberatelychoose to inspect the data for qualityand make sure you understand what's going into it.Hopefully, Big Data users will take that opportunityand will audit their data for quality using someof the criterion that we'll talk about in the next movie.

### Additional Vs of big data

At the beginning of this course, I mentioned thatbig data is typically defined by three V's.And those are volume, velocity, and variety.So volume meaning a very large amount of data,velocity meaning it's often coming in quickly,might be streaming data, and variety meansa lot of different formats and especially notin the regularly structured rows and columnsof a spreadsheet or a relational database.On the other hand, there have been a seriesof other V's proposed.

Now the thing is we kind of got the V's rolling andpeople are throwing everything they can in it like volcanic and verisimilitudeness and who knows what else.But the point here is the V's that I'm going to listall do have a legitimate reason for being discussedeven if the V word itself is a bit of a stretch.But these are all factors to considerwith big data research.The ones I'm going to mention here are **veracity**.Now, **veracity means will it give you insights in to the truth about your research questions**?It really has to do with does the data that you have contain enough information at a sufficiently micro level for you to be able to make accurate conclusions about larger groups of people?Also, **validity**, is the data clean?Is it well managed, does it meet the requirements,is it up to the standards of the discipline?Does it have **value**?And **in a business setting that's going to specificallytrnaslate to the ROI or return on investment**.

Is it worth your time to engage in a big data project? Because you know what?It's not always going to be.Big data is still an expensive, time consuming,major undertaking in most situations.It's getting better, but for right now you need to thinkabout whether that particular analysis really is going tofurther your organizational goal.Number seven is **variability**.And the **idea here is that the data can change over timeand you can usually analyze that.It can also change over a place.**

And there's a lot of uncontrolled factors that mayintroduce noise into your data unless youspecifically measure and account for them.A few more V's are eight, **venue**.And this means **where's the data located and howdoes that affect access to the data and how doesthat affect its formatting?** Number nine is **vocabulary.And this refers to the metadata that's used todescribe the data, especially when you're combining data from very different sources**.When they're talking about the same variable, thes ame kind of information, they may be using very different terms to describe it.

It may not be clear that what's going on there isthe same thing and so that becomes one of the challenges in combining data sources in a big data project.And the number ten and last one we're going to talk aboutis kind of a funny one, it's **vagueness.And that really is, do you know what in fact you're talking about**?What do you mean by big data?What are your goals?What are you trying to accomplish?Because you have to have clarity of purpose oryou have the potential of wasting an enormousamount of time and energy chasing the wrong thing.Big data is there to serve a purpose.

It's there to give you insight that you cannot getotherwise and that gives you an ability to functionmuch more efficiently and intelligently, but you needto be clear about what you're doing or yourtime might be wasted.So having big data does not automatically solveorganizational questions or overcome research challenges.You can have Hadoop, but that doesn't mean you'regoing to understand what's going into it.You may have the most sophisticated predicitiveanalytics equation, but if it's based on something that'sirrelevant, you've wasted your time.

If anything, big data introduces more things to beaware of because there's more places for thingsto go wrong or to be confused.And responsibilities tend to be spread out in abig data project.What that is is you usually have different groups ofpeople who prepare the data, who analyze it, whovisualize it, who apply it, who form the new setsof questions, find other information to bring in.Because you can have hundreds or even thousandsof people involved in a single big data project.No one person's overlooking everything.

And so the responsibilities to answer these questionsabout things like value and vagueness,they become incumbent on everybody understanding what's going on.There's a greater need to think about the quality because there's so many more opportunities tolet things slip through the crack.And there's a greater need to think about the meaningof the project as you go through it.If you do that, then you're going to be in a muchbetter situation.And if we assume, also, that the quality of the datain the project has been verified, then our nextstep is the actual analysis of big data,which is where we'll turn in our next chapter.

**Special challenges with Big data**  **1.Responsibilities are spread out, 2. Different people prepare, analyze and apply the data, 3. There is greater need to think about quality, 4.There's a greater need to think about the meaning**

###### Chapter Quiz

###### Question 1 of 2

###### Access to big data means that you can automatically solve organizational questions.

- TRUE
- **FALSE**

##### Question 2 of 2

###### The process of loading data into software for analysis is called _____.

- import
- jacking in
- **load** After extracting the data from storage, and converting it for analysis, you can load it into the analysis software.
- unload

## 8.Big Data Analysis

### Monitoring and anomaly detection

Big data can be helpful for letting people knowwhen unusual things happenor possibly, when they're about to happen.These kinds of notifications can fallinto two general categories,although there are other systemsfor describing notifications.They are monitoring and anomaly detection.At the risk of making the differencesbetween these two procedures sound bigger than it is,here's how I describe each one:Monitoring can be very helpfulwhen you know what you're looking forand you need a notification when that thing occurs.It detects when a specific event occurs.

So you need to be able to specify the criterion in advance.For example, a manufacturer needs to know when one of their machines need maintenance,so they may look at temperatures.They may look at vibration levels.They may look at a number of factorsthat let them know that breakdown is imminent.Take care of it now.A doctor or nurse needs to knowwhen one of their patients' is sick.They may be monitoring, for instance,for temperature and pulse, and, if possible,for white-cell counts to indicate infection,and a credit-card company needs to knowwhen a charge is potentially fraudulent.![47](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-22 at 01.12.47.png)

In these cases, it may be possible for a user to specify the particular criteria they needin order to trigger the event,and what's interesting about it iswith the monitoring, because you can be very specific,it may even be possible in certain situations,to set up an automatic response that really says,"If X occurs, then Y results,"and we take care of it automatically.And so, monitoring is a specific thing.You know what you're looking for.You're waiting for it happen,and possibly, even an automatic response.Anomaly detection, on the other hand,can describe a situation in which the userwants to know when something unusual happens.![57](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-22 at 01.14.57.png)

They're looking for a notification of unusual activitywithout necessarily knowing in advancewhat that something might be.As a result, it needs to be based on flexible criteria,and it says, "Let me know when something"that is out of the ordinary happens,"maybe not just on one factor,"but, like, on a combination of several different factors."And the flexible criteria usually existsto draw a person's attention to something.So, for instance, in security cameras,they might be able to say,"Look, we don’t know what's going on here,"but we do know that it's out of the ordinary."Or in a stock-trading situation, they might say,"We don’t know what's going on here,"but it needs to be examined."And so it does usually trigger an automatic response,but instead, it invites inspection.

But anomaly detection can notice patterns that,for instance, may be too far spread apart in big dataor may be too fine for humans to notice on their own.What big data allows here is notthat these things can occur,because monitoring anomaly detectionhave occurred for forever.Now both of these approaches,monitoring and anomaly detection,are common practices and predate not just big databut computers as well.What big data adds to them though is the possibilityto watch for extremely rare eventsor combinations of factors.

So, for instance, **if you have an event that's a one-in-a-million.** It only occurs one time out of a million observations,that could be really hard to spot if you're doing it by hand or if you're doing it, for instance,even a hundred cases at a time,but if you have ten billion cases that you're sorting through,this one in a million event is going to occur 10,000 times.And suddenly, that's not a small a number. ![56](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-22 at 02.48.56.png)It's not so rare.In fact, 10,000 is a pretty large number,and it allows you to do statistical modeling.It allows you to break it down by sub-categories.

It allows you to figure out exactlywhat's associated with it and what's causing it.As for anomaly detection,the big data advantage is similar,especially when you lookfor rare combinations of events.That is, it may be possible to measurea thousand different things at onceinstead of just, you know, 10 or 12.This allows the machine learning algorithmthat identifies anomalous casesto become much more specific and have a much better chanceat avoiding both false positives and false negatives.To take a relatively trivial example of this,let's look at email spam filters.

Now spam is a tricky situationbecause spam is a very fast-evolvingsort of virus-like mechanism.It's never the same.It has to change all the timebecause there's this little arms racebetween spam and spam filter.So you can't just write a single rule that says,"This is spam," because the spam will adaptto circumvent that rule,and so we have this very quick evolution,and so you can't give clear rules for spam,or it's very hard to do. ![22](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-22 at 02.50.22.png)And what you find is thatif you have a spam filter that looks only at your emailand what you say, "This is spam; this is not,"you get a lot of false results.

You get false positives.You get false negatives.And I remember when I first started with email,that was the case.I used an email client,and I had to indicate what was spam.And I have to admit, it was semi-useless.It didn’t work very well.On the other hand, when you hook upto a big data collection,when you're not categorizing spam just on your own,but when you combine the data from millionsor hundreds of millions of users,like, for instance, if you use Gmail or Hotmail or Yahoo,then it combines the collective wisdom of the crowdto determine what is spam and what's.

I've gotta say, my Gmail filter is superat identifying spam,and that's because we're going onto big data,and millions, or truthfully, billions of emailsthat are sent every day.So big data makes it possibleto perform these two kinds of watching,the more specific monitoringand the more flexible anomaly detectionwith much greater power,by being able to sort through much larger data setsand to look for more diagnostic signs at each point.

### Data mining and text analytics

One of the most powerful and common applicationsof big data is in Data Mining andit's close cousin Text Analytics. Data Mining covers a large and diverse fieldof activities but the most basic idea is this,use statistical procedures to findunexpected patterns in data.Those patterns might include unexpectedassociations between variables or people whocluster together in unanticipated ways.![56](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-22 at 02.52.56.png)For example, managers in a supermarket teammight find that people who visit their storesin a particular region, on a particular nightof the week are generally different from peoplewho come at other times and places.

The market can then change where couponsare displayed, or if at all, and they can changewhere certain items are found from day to dayto build on those differences.Or an investment company may find that whencertain stocks move up together but certain othersgo down, then a particular stock will generally follow.And that allows them to investin that one and hopefully make a profit.Or a medical researcher may find that patientswho exhibit a very particular pattern of symptomsat one time, even if they don't meet the criteriafor a diagnosed illness, are more likely to check intothe hospital in the next six weeks, for example.

Perhaps the most common application of this kind of Data Mining is with online advertisingbecause the data base is so largeand because it's so easy to adaptthe results for each specific viewer. ![32](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-22 at 02.54.32.png)In fact, that's one of the biggest promises ofData Mining, the ability to tailor servicesto the preferences and behaviors of each individualperson once enough data has been gathered.Text Analytics is closely related to the standardkind of Data Mining that deals exclusivelywith numbers, however Text Analytics issufficiently distinct to be it's own field.The goal here is to take the actual contentof Text data, such as tweets orcustomer reviews and find meaningand pattern in the words.

This is different from the Meta Data Research that we discussed earlier because that researchwhich can be shockingly informative,dealt just with the numerical informationthat the computers created on their ownand didn't even need to deal withthe content of the information.When researchers look at the text itselfthe interpretive and computational problemsbecome really enormous and that's becausehuman language is so flexible and subtle.Where phrases that sound very similarcan have very different meanings,as in the familiar joke, time flieslike an arrow, fruit flies like a banana.

It's attributed to Groucho Marx sometimes.Now, this is a difficult phrasefor humans to understand immediately.It's nearly for possible for computers to understandand explains why the field that's calledNatural Language Processing, has had,you know, so many challenges to overcome,and why it's such an active area of research.But perhaps in Text Analytics, the most commontask is probably what they callsentiment analysis, or determininghow people feel about something.That makes sense if you're thinking about advertising or marketing point of view,you definitely want to know if people feelgood or bad about your particular product.

The most basic task in sentiment analysis isdetermining if a person's feelings are positive or negative.This is referred to as Polarity, in the Text Analytics world.![36](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-22 at 03.08.36.png)Now, in, in my field, Social Psychology we call it valence. Fortunately, because this distinctionis such a common task, there are many programsand packages that you can use in familiarlanguages like Python or R, thathave been developed to help with this.Of course, Sentiment Analysis and Text Analyticsare generally much, much more sophisticatedthan just good, bad, but this gives you the basic idea.

Now, there's much, much more that could be saidabout these topics, but I hope to make it clearthat Data Mining and Text Analyticswork best when they have very largeand diverse data sets to work with.And that's what big data does best.As researchers continue to develop and refinemethods for Data Mining and Text Analytics,the ability to find patterns in numerical dataand derive meaning from textual data,they'll become faster, simpler and more nuanced.

### Predictive analytics

**Predictive analytics is the crystal ball of big data**.That is, it represents a range of techniques that are adapted to work with big data to try to predict future events based on past observations. ![32](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-22 at 03.10.32.png)And while people have been trying to predict the futureever since there have been people,the raw resources of big dataand the sophistication of modern predictive modelinghave fundamentally changed the waythat we look into the future.In the popular world, there are a few well-knownexamples of predictive analytics.The first is in baseball,as shown in the book and the movie, Moneyball,where statistical analysis is used to assist to identifyan offensive player's scoring ability.

And the standard criteria that have been usedby people for a hundred years in baseballis to look at things like batting averages and RBIs or runs batted in, stolen bases, and what happened is,baseball has an enormous data set,because it's very easy to count discrete events that occur,and so, you're able to go back and deal withan extraordinarily large data set for sports. ![15](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-22 at 03.12.15.png)And researchers found that no,the batting averages and RBIs are not the best predictorsbut on-base percentage, because you can get on baseby getting a hit or getting walkedor getting hit by a ball or any number of ways,and slugging percentage, which has to do withhow many bases you get, are better predictors.

The second example is from Nate Silver'sremarkable accuracy predicting the resultsfor every single state in the2012 U.S. Presidential election. ![49](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-22 at 03.13.49.png)Now, what Nate did here is, he has a blog calledFiveThirtyEight, which has to do withthe number of representatives in congress.He took data from a wide range of polls,combined that data, and weighted them by their reliability,and he was able to come up with an accurate predictionfor every single state in the election.

It was remarkable.Now, I just want to show you.He has a website, FiveThirtyEight.The other thing that Nate Silver does is sports statistics.In fact, he's better known for most peoplefor his baseball statistics, like Moneyball,and his website, FiveThirtyEight,which used to be primarily political,has been purchased by ESPN,so here's his current website,and there's Nate down in the bottom right corner,where he is doing all sorts of predictions.Also his site, FiveThirtyEight, is very well knownfor its college basketball brackets,when you get to the playoffs.

The next thing I've brought up before is the Netflix Prize.This is from a few years ago,when Netflix provided a million dollar prizeto anybody who could improve the qualityof their recommendations by 10%using an anonymized data set that they had provided.Now what's happened with that oneis there were some really remarkablestatistical analyses that came out of it.Perhaps the biggest thing that came out of the Netflix prizewas the efficacy of what are called ensemble models,and the idea here is,you don't build a single predictive model.

You don't try to say, well these are--this is our regression equationor this is our random forest model to predict.You build as many different predictive modelsas you possibly can, and then you basicallyaverage the results of them.Because it turns out that when it comes to predictions,the average prediction is usually more accuratethan any one individual prediction.It actually comes from a thing aboutguess the number of jelly beans in a large jar.If you take everybody's predictions and average them,that's usually going to be closer to the real numberthan any one individual's actual guess.

Now, a place that has taken up on this,and the Netflix Prize was a few years ago,but there's a website now called kaggle.com,which is for hosting similar kinds ofpredictive analytics competitions.I'm going to show you their website for a moment.Kaggle.com, if we come down here,you can see, for instance,right now they're having a machine learning challengeon identifying the Higgs boson.It's an amazing thing.Let's go back up to the competition,and right now you can see they're hostinga number of competitions from companies that have data,and they're looking to find good predictive models,and they're paying prizes here of up to $25,000.

Now, in the past they've had prizes of half million dollarsfor what they're doing,and they also have a number of free onesthat are actually there to teach youhow to do predictive analytics.So, for instance, these ones down here on the bottom,the Titanic is an educational oneabout how to do machine learningin Python and R and other things.So, Kaggle is a fabulous source for what's available.Predictive analytics is an enormous area of interestbecause, especially if you're in the business world,trying to predict what is going to happenand having a little bit of foreknowledgecan get you a huge competitive advantage.

It's an area of incredible growth, and it really isone of the most fascinating things about statistics,because there's always a very clear criterion,which is something that's often lacking.You can tell, if you wait just a little bit,you can tell whether your model is goodor whether it wasn't,and the progress in the field makes it possibleto learn more and more,and especially with the raw material from big data,there's so much more to work with to build more new ones,more refined models, and to get better predictive abilitiesfor more competitive advantage.

### Big Data Visualization

Up to this point,we've been talking about big data,and the things that the computersare able to do for the humans.On the other hand, it turns out there are certain thingsthat humans still do better than computers,and visualization is one of them.Humans are visual animals.![53](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-22 at 03.39.53.png)We work on sight, and we geta huge amount of information that way.Computers are very good at spotting certain patterns.They're also very good at calculatingpredictive models and doing data miningin a way that humans would have a hard timedoing in a thousand lifetimes.But, humans perceive and interpret patternsmuch better than computers do,and so human vision still playsan important role in big data.

Humans can see the patterns,and they can see the exceptions to the patternsor the anomalies very quickly.They can also see those patterns acrossmultiple variables and groups.They're also much better at interpretingthe content of images than computers are.So for instance, here are some familiar examplesfrom what's called Gestalt patterns.It's a German word meaning a pattern or a whole.![57](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-22 at 03.40.57.png)What you see here for instance,is in the top left the three circles or the three arcs,that together suggest, imply a triangle in the middle.

The triangle is not there.It's created by the absence.It's very easy for humans to see this,because we're looking at something that is suggestedthrough negative space.It would be much harder for a computer to see it.Similarly, the arrangement of circles and squaresis easy for people to follow that on the top right.On the bottom left, we see four squares separately.Then we see squares arranged in pairs,and then squares all arranged as a single line.Easy for humans to perceive and interpret.Hard for computers to make sense of.

In the bottom right in D,it's easy to see rows of dots,and then columns of dots,because humans are built for this kind of visual processing,and it's very hard to describe to a computer how to do it.Now, I want to show you an interesting examplefrom the National Science Foundation,who has their Vizzies.![50](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-22 at 03.42.50.png)Even though it says the most beautiful visualizations,these are also very informative ones.I'm going to scroll down just a little bit here,and look at the one on the right, which is about video.I will look at the 2013 winners,and I'll click on the first one here.

Now, this is a still frame from a video visualization.What it's showing is weather datafrom satellites about the earth.What's clear here is that theseare circulation patterns of the ocean and the wind,and it's really easy for humans to see the patternsof the swirling shapes that form a continuous flow,and also the circles.Humans can see these very easily,and this is based on an enormous data set.It's absolutely big data.But it's very hard for the computers to see it.

Now, I do need to bring something up.Because visualization is important,a person should not assume that anything goes.There's a lot of things that don't work well.When I look at visualization on the web,most of the examples I get are very pretty,visually arresting pictures, but to me they're not very informative.The important thing here is thata **pretty graph is not always better**.It gets back to the rules from Excel.Never use a false third dimension.Don't separate things from the axis.You've got to be able to read them clearly.

Also, in many situations, **animated or interactive graphs,they can be more informative,but they can also sometimes just be distracting,and a person starts messing around with it,instead of understanding exactly what the message is**.So you've got to think very carefullyabout whether you're going to include those.**The goal of data visualization in any kind of graphics is insight.** You want to get to the insightas quickly and clearly as possible,and anything that distracts from that,or heaven forbid, gives a person the wrong impression,is a mistake and should be eliminated.

So data visualization is still an areawhere humans can make an important contributionto big data analysis,and the computers can contributeall of the other models that we've talked about so far.So it's important to remember this human elementwhen planning a big data project,that there is still a need for the human perceptionand interpretation to make sense of the datain addition to what the computer is able to provide.

### The role of Excel in big data

Before we leave our discussion of big data analytics,I want to talk about the role of Excel.Now this is important because a lot of people think that to do big data you have to use rocketscience equipment all the way through, and thatExcel because it's installed on every computerin the whole entire world certainly isn'tspecial enough and doesn't qualify.That's not true at all.There's a few things about Excel.First off, is as a general principle you want to go to where the people are.The analysis is there to serve a purpose,it's there to inform other people.And even if you have to store the data and dupeand you've got to use other programs to access it there,Excel is still going to be a really good way to share itbecause it's where people know how to work.

Far and away the most common data tool.There are hundreds of millions, perhaps billions,of copies of Excel floating in the world.Millions of people use it on a daily basis.Even professional data miners use it.I saw a recent survey of data miner software.The third most common application that data minersuse in their professional projects is Excel.Now big data and data science havean interesting connection with Excel.For one thing, Excel, entirely on its own,just the application, is able to do real data science.**The best presentation of this is in the bookData Smart: Using Data Science to TransformInformation into Insight by John W. Foreman.** ![28](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-22 at 21.29.28.png)

And he goes all the way through the really advancedcapabilities of Excel that make it possible toexplore and manipulate data in ways that youprobably never thought were possible.But more interestingly using what are calledopen database connectivity interfaces or ODBC interfaces,you can hook Excel directly to Hadoop and doqueries and analyses from the Excel interface.Let me just go to Excel for a moment.Here I am and we've got the home.If you come over here to data and bring up that menu,and then go to from other sources, you'll see that ourvery first thing is from a SQL Server,which is a relational database and a lot ofinformation is going to be there,but you can go down to the Windows Azure Marketplace,so that's going to connect you up with Hadoopand these, the data connectivity wizard and the queriesand the Odata, these are methods for connecting to big data.

And now Microsoft has their own solutions and othervendors have other ways of hooking up Excel intobig data and to Hadoop to make it possible to controlthe analysis, or at least do the queries and the sortings,right here from the single most familiarinterface for working with data.Finally, I want to mention that Excel is also a greatway for sharing the results of the analysis.You can make interactive PivotTables, a great wayfor exploring the complexities of the data and peopleknow how to work these, and sortable worksheetsand the graphics and charts are familiar, they communicate,they're clear, it's a great way to go.

In fact, I would say that putting the final resultsinto Excel, which provides a degree of explorationand manipulation to your viewers, is probably themost democratic way of sharing theresults of a big data analysis.And again, the point of any analysis is to provideinsight that people can work on, that is actionable,that they can use to improve their ownbusinesses and their own projects.

##### Chapter Quiz

###### Question 1 of 4

###### Computers are far better at visualization than humans.

- TRUE
- **FALSE**

###### Question 2 of 4

###### When many predictions are averaged, the result will be close to the real number.

- **TRUE**
- FALSE

##### Question 3 of 4

###### What is the most common application of data mining?

- predicting illness
- **online advertising** It's easy for advertising to utilize the large data base and adapt the results for each specific viewer.
- government surveillance
- forecasting weather

###### Question 4 of 4

###### Excel is the _____ most common application that data miners use.

- **third** According to a recent survey, the third most common application that data miners use in their professional projects is Excel.
- first
- unexpected
- last

### Next steps

And so we've come all the way aroundand we're at the final videofor techniques and concepts of big data.Before we leave,I wanted to give you some ideas for further learning.We're going to base thison the data science Venn diagramthat we talked about earlier,which talks about codingand statistics and domain knowledge.At Lynda.com you can finda really wide range of coding courses.If you're new to coding,a really nice way to do thismight be either with Bash Scriptingthrough the command line or with Python.Similarly, statistics,there's a range of courses available at Lynda,these are actually on my coursesabout using the programming language R,which is for statistics,or processing for data visualization.![24](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-22 at 21.38.24.png)

I also have courses on SPSS,another statistical package.Although it's not explicitly partof the data science Venn diagram,databases are absolutely centralin this sort of split between coding and statisticsand there's a great selectionof database courses at Lynda.com,such as the foundations coursesand the SQL and MySQLand Up and Running with NoSQL Databases. ![44](/Users/kirosgebremariam/Desktop/Screen Shot 2018-09-22 at 21.40.44.png)As far as domain knowledge goesthat's going to of course dependon what your specific interests are.

For that I'm just going to goto the Lynda.com website.If you go to Browse the Libraryyou see of course that there are hundredsand hundreds of choices.For instance, I'll just scroll down a little bit hereto let you see that if you're lookingat business in general there are 555 coursesthat are of interest on Lynda.com.You can find very specificmarketing and advertising segments,you can also find app developmentand web design and education.There's a huge range of choices herethat can give you the specificdomain knowledge that you needto combine with your statistical knowledgeand your coding skills.

And then you can start implementingyour own big data solutions in your field.Thanks for joining me and good luck.

#### EXAM

###### Question 1 of 13

##### Examples of variety of big data include _____ such as books, blogs, news articles, photos, tweets, as well as video and audio files.

#### Select an answer:

- structured data
- static data
- never-ending data
- unstructured data**

Question 2 of 13

### Big data algorithms are so sophisticated that the processes are almost _____ to consumers.

#### Select an answer:

- complex
- visible
- invisible**
- continual

Question 3 of 13

### An good example of big data that influences science is Google _____.

#### Select an answer:

- ad words
- **flu trends**
- user demographics**
- blog circles

Question 4 of 13

### One of the ways big data differs from small data is that if something goes wrong in the process, it is not easy to start the dataset again. This is referred to as _____.

#### Select an answer:

- difficult
- non-verifiable**
- **reproducibility**
- errors

Question 5 of 13

### For those in big data, there is a high level of _____ among practitioners.

#### Select an answer:

- complexity
- heterogeneity**
- humans
- largeness

Question 6 of 13

### A very large and static data set with a consistent format is an example of _____.

#### Select an answer:

- vectors
- variation
- vacancies
- volume**

Question 7 of 13

### What is the definition of confidentiality of data?

#### Select an answer:

- If individuals are identified within the data, they will regret it.
- If individuals are identified within the data, they may use their avatar names.
- If individuals are identified in data, their data will not be shared with people they do not specifically allow to see it.**
- If individuals are identified within the data, they can just say, It's not me.""

Question 8 of 13

### Nearly 80% of database users use some form of _____.

#### Select an answer:

- word processing
- relational databases**
- help resources
- headache medicine

Question 9 of 13

### What are two common formats for semi-structured data?

#### Select an answer:

- XML and JSON**
- YING and YANG
- R and PYTHON
- PDF and DOC

Question 10 of 13

### _____ is thought of as the consumer layer of crowd computing and includes web applications that run entirely through the browser.

#### Select an answer:

- SaaS**
- PaaS
- SaaP
- PaaP

Question 11 of 13

### What is Hadoop?

#### Select an answer:

- a complex theory of big data
- a collection of software applications used to work with big data**
- a data protocol derived from NASA's Apollo engineering program
- a plug-in

Question 12 of 13

### What is one challenge of big data quality?

#### Select an answer:

- Data often originates outside of a project and could introduce errors.**
- The quantity/quality balance suffers.
- The volume interferes with quality.
- Data often comes from foreign sources.

Question 13 of 13

### Use _____ detection when you need to know if something unusual happens and _____ when you know what you are looking for.

#### Select an answer:

- monitoring; anomaly

- anomaly; monitoring**

- camera; monitoring

- data; monitoring

- Show wrong only

- ### Question 1 of 13

  #### Examples of variety of big data include _____ such as books, blogs, news articles, photos, tweets, as well as video and audio files.

- ### Question 2 of 13

  #### Big data algorithms are so sophisticated that the processes are almost _____ to consumers.

- ### Question 3 of 13

  #### An good example of big data that influences science is Google _____.

- ### Question 4 of 13

  #### One of the ways big data differs from small data is that if something goes wrong in the process, it is not easy to start the dataset again. This is referred to as _____.

- ### Question 5 of 13

  #### For those in big data, there is a high level of _____ among practitioners.

- ### Question 6 of 13

  #### A very large and static data set with a consistent format is an example of _____.

- ### Question 7 of 13

  #### What is the definition of confidentiality of data?

- ### Question 8 of 13

  #### Nearly 80% of database users use some form of _____.

- ### Question 9 of 13

  #### What are two common formats for semi-structured data?

- ### Question 10 of 13

  #### _____ is thought of as the consumer layer of crowd computing and includes web applications that run entirely through the browser.

- ### Question 11 of 13

  #### What is Hadoop?

- ### Question 12 of 13

  #### What is one challenge of big data quality?

- ### Question 13 of 13

  #### Use _____ detection when you need to know if something unusual happens and _____ when you know what you are looking for.
