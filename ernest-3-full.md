# Copyright transfer statement

MEL CHUA hereby irrevocably transfers and assigns to ERNEST W. DURBIN III in perpetuity, all right (whether now known or hereinafter invented), title, and interest, throughout the world, including any copyrights and renewals or extensions thereto, in the attached transcript of the interview recorded between us on OCTOBER 11, 2019 in A LIVE-TRANSCRIBED ONLINE VIDEO CHAT.
 
# License

I, Ernest W. Durbin III, hereby release this work under the following open license: http://creativecommons.org/licenses/by/3.0. Anyone is free to share and remix the work as long as they cite it. I consent to the open publication of this work using my name.

# BEGIN TRANSCRIPT

MEL: I can turn off my video also, so you don’t get backlit Mel all the time. All right. So are you ready to start the third and last interview round?

ERNEST: Absolutely.

MEL: All right. So… Today we’re continuing the saga of PyPI as a case study for sustainability and maintenance of Open Source infrastructure projects.

And there’s a few things that I wanted to do today. One is… Three things. 

One is going back to what everybody said about what sustainability meant to them. The second one is the same thing, but for being well maintained. 

And the third thing was for giving a bit of a preview into some of the patterns and things that we think we’re seeing across the interviews as we start to analyze them, and seeing if you had any thoughts or feedback on that.

ERNEST: Great.

(computer chime)

ERNEST: I’ll be turning that dinging off. There we go.

MEL: Okay.

ERNEST: Computer chime. Perfect.

MEL: Cool. So… I’m actually going to start with the third one. With… Here are some of the patterns and things we seem to be seeing across interviews. I’m gonna start that out with… I’ll just show you an excerpt from Jackie’s first interview. Because she said something that was really interesting, that I think is a good starting point to talking about two distinctions that we’re starting to feel are important here. 

So the first one is: When we think about sustainability and maintainership, it’s important that this is an infrastructure project, versus another kind of project. And then the second half of that is: What difference does it make for it to be an Open Source project, versus a non-Open Source or maybe more typically corporate-developed project?

ERNEST: Sure.

MEL: Okay. And we’re gonna paste the excerpt in here.

> _Source(s): Jackie-1_
>
> JACKIE: As a user of other packages, I never really looked at sustainability because I always looked at it as, well, if this doesn't continue or this somehow fails, I can fork it. In the worst case, I can fork it and fix the things that I need to fix to make it work.

MEL: So that was interesting to me, when I saw it. Because Jackie there was talking about PyPI in particular, but infrastructure in general -- how she felt it was different to think about it, compared to sustainability for other kinds of Open Source software projects.

ERNEST: Yeah. Certainly. I think that reading this excerpt -- it looks like this is in reference to, like, sustainability of a software project. If things just sort of disappear for whatever reason, it’s not that hard to either effectively vendor the code or work from your own fork. Versus infrastructure projects… It’s not necessarily as clear cut. Is that accurate?

MEL: Mm-hm. Yeah. And so… From the perspective of someone who’s very much in charge of keeping the infrastructure up and running, does that feel accurate to you? So Jackie is talking from more of a developer perspective here. But how would you say that translates to your side?

ERNEST: So I mean… I suppose I’m not sure in what context. As a maintainer of PyPI, if PyPI for whatever reason had to shut down, I don’t know what the equivalent would be, necessarily, for users. Right? 

There are other options for hosting package repositories. Most of them are private. And require some form of payment to use. And currently those are mostly focused on hosting your private projects that you don’t really want to be published on PyPI. PyPI serves as a hub, I guess, primarily for everything else. 

So projects that are either privately developed but are published for end user use, or just in the interests of sharing with the community, or public projects that are just built as core parts of sort of the Python ecosystem, and that’s sort of the de facto place to share them… So yeah. 

As far as the equivalent of a software project that you depend on going unmaintained or defunct in some other manner, yeah. It’s a common pattern that’s seen. A fork occurs, and things either pick up from there and move on, or sometimes that fork is just solely for the purpose of them to be able to maintain this thing for their own use, and not necessarily out of interest for the broader community. 

So from an infrastructure perspective, again, I’m not strictly sure what the alternative would be. As far as I’m aware, there isn’t really a precedent for the de facto package repository for an Open Source language to go missing. Or shut down. 

It’s not something I’m really interested in seeing occur either. And so honestly, I don’t know that there’s really a whole lot of consideration given to that. So that’s something I’ve spent a whole lot of time thinking about. Yeah. 

Right now, I do know that there are corporations primarily that run either mirrors or caching proxies to PyPI. So that in the event that -- I mean, I think that is primarily oriented towards when PyPI has outages, for whatever reason. But perhaps it is just from a continuity perspective. But these services exist so that if a package is deleted by its author, they still have access to it. Or if they want to publish their own projects internally, in addition to all the PyPI projects, it’s sort of transparent to their users. 

I don’t know necessarily if they’re a good stand-in for if PyPI just turned off. But yeah. I guess… Again, just to sort of circle back a little bit, I don’t think there’s a precedent for core pieces of infrastructure like that sort of permanently disappearing. That I’m aware of, anyway.

MEL: Cool. So… The next bit I wanted to show you… There’s five points I’ll show you one at a time. So far in our analysis we’re playing with a lot of things, but one of the bits that we’re trying to synthesize together is… It’s on that 2x2 grid I was talking about, with infrastructure versus non-infrastructure, and FOSS versus non-FOSS. 

And so far, we have five areas where this seems to be something that is true of infrastructure generally, but maybe not all software projects ever. So the kind of stuff we were talking about are… Yeah. It’s hard to fork infrastructure. And for each of those things, we’ve been going… Okay. This seems to be something that’s different between FOSS and non-FOSS.

ERNEST: Okay.

MEL: So I’ll show you those one at a time. And let you respond to each of those in turn. And some of these -- these are fairly rough notes. We haven’t quite figured out the final phrasing for them yet. And so there might be some where it’s like… This phrasing is awkward. Or this phrasing is from interviews.

ERNEST: Understood.

> _Source(s): notes-11-10-2019.md_
> 
> 1. Infrastructure is “magical plumbing.” FOSS infrastructure lets you look behind the curtain if you so choose; non-FOSS infrastructure likely does not.

MEL: Okay. That’s the first one. What do you think?

ERNEST: In general, this is certainly true. As far as the code and in some circumstances even the tooling used to deploy that code… It is out there and available for looking. Right? 

So one of the most common questions we initially got with Warehouse was: How do I run this myself? And the answer to that generally was: It’s not intended for that. And so there was some confusion, I guess, around, like, okay. There’s a codebase that implements quote-unquote “PyPI”. How do I run my own PyPI? And Warehouse is not that. 

So it’s publicly inspectable. It can be viewed and theoretically it could be reconstituted to some extent. The software itself… Yeah. 

The data clearly not necessarily. Right? We don’t publish -- our database isn’t public. That would be a pretty terrible idea. At least (inaudible) -- a subset of the database is theoretically accessible. But not necessarily something you can just… Okay. We’ll go from this dump and here’s the new PyPI. 

But yeah. There are a lot of things that aren’t necessarily perfectly inspectable. There are processes and procedures, I guess, that either occur in an informal fashion, even in an open infrastructure, that you couldn’t necessarily just find all the records of. They’re imperfect clarity. Right? 

Myself and a handful of the other administrators on PyPI have a private chat that we use to have discussions that are either not of interest or not applicable to the public. Right? 

So these decisions generally -- not generally, nearly always -- manifest as a change to PyPI. And we do our best to summarize the reasoning for it. Sometimes it’s like a security response thing. Right? Or a policy that needs some discussion, but has some other concerns to it. So I don’t know. Yeah. 

It’s a theoretical thing. Right? Theoretically, sure. You can completely reconstitute PyPI minus some data that will never be private. Like users’ hashed passwords and private email addresses. Right? But in reality, I’m not sure whether that’s true. 

So it’s available for inspection. And some people do create really good results, given that. Like, we’ve had certain security reports made based on such inspection. And it offers the community a chance to contribute and be a part of it. 

But I don’t necessarily know that it reaches the same level of… It’s just similar but not equivalent to the fact that a certain library’s code might be Open Source. 

It is significantly better than… As far as from a transparency or openness perspective… Than nearly any private company. I don’t know of any private company whose configuration management is even remotely public. Parts of the tooling they use might be. Or results that they’ve had or methods that they’ve undertaken might be published, either as an Open Source project or as a white paper. Or just as blog posts. But yeah. 

So it is dramatically different between FOSS and non-FOSS. But I think it’s still practically different between libraries and infrastructure.

MEL: Cool. So the second bit… So number two of five…

> _Source(s): notes-11-10-2019.md_
> 
> 2. Infrastructure requires technical effort for operations (as well as development). FOSS infrastructure may begin as a pet project and then “accidentally” go into production; non-FOSS infrastructure is more likely to be deliberately planned with allocated resources and to have project management much earlier on.

ERNEST: I think that is very accurate. So the precursor to PyPI is this thing called the Vaults of Parnassus. I think that spelling is even accurate in the transcript. I’m not positive right off the top of my head. But the Vaults of Parnassus was literally just a web page with links on it. And it was, you know, effectively a pet project. And then that is what spawned PyPI. 

And PyPI did have some thought behind it. But initially, it really is probably best classified -- I mean, at least in its first few months -- as sort of a pet project. Like… Is this something we can do? Is this something we should do? And then as it continued to live on, PyPI itself did grow a bunch of features that were sort of… You know, accidentally going to production. To use the quote. Yeah. So I think I agree a lot with this quote. As far as sort of how things begin.

But by the same token, I’ve seen a lot of -- in corporate settings, I’ve seen similar sorts of things happen. So I don’t think it’s completely unique that pet projects accidentally go to production or are relied on in some manner. But it’s certainly more common in the open space. Yeah. So…

MEL: Huh. Okay. So number three of five…

> _Source(s): notes-11-10-2019.md_
> 
> 3. Infrastructure requires development capacity (people-time). FOSS infrastructure is likely to have some or all of this development capacity come from self-directed volunteers, but that effort is also more likely to fade out during the “last mile.” Non-FOSS infrastructure is more likely to have its development resources known, managed, and allocated in advance.
 
ERNEST: Yeah, certainly. Developing PyPI and building features and such… Sure. It can come and go. I think the most consistent ongoing work, as far as software itself is concerned, is keeping up to date with dependencies and Python versions and security vulnerabilities and such. 

But there is that operational… I guess this quote is mostly about development capacity. But I’m sort of reading it a little bit more along the lines of operational capacity. 

So operations aren’t completely orthogonal to development. They rely on one another, effectively. Better development practices lead to easier to operate software, and well operated software tends to be easier to develop. If the deployment is very simple to go out and also very simple to roll back, then it has… Yeah. It becomes a better environment, overall. 

So yeah. I mean, the last mile thing… Yeah. I mean, I definitely recognize this in being part of that last mile for PyPI for a long time. It’s that people can become very excited about adding a feature and working on something, and then when they hit a blocker sometime, and something becomes difficult or they run out of time, or whatever, we do generally kind of end up picking up that last mile for them. 

Which is logical. Projects or concepts or features can be much larger than anticipated, and as you excitedly set off, you might have a lot of time, and then when you finally realize how much bigger it is or what final little bits like testing you need to undertake, to make it shippable, your situation may have changed, or your motivation may have waned. So yeah. I think it’s very similar. 

And I think the other aspect of this quote that I’m sort of interested in is the non-FOSS infrastructure is most likely to have its development resources known, management allocated in advance… That’s certain. 

Right now, about the only development resource that PyPI has known in advance is… Some limited amount of my time, and then also a handful of projects that we have funding and road maps for. 

Right now, there’s only one of those. We don’t preallocate… We don’t have any idea, necessarily, how much time the other PyPI admins or community will be contributing to this in the future. Yeah. 

So that road mapping is a lot easier when you have a team who is paid on a salary, effectively. Versus… You can develop road maps for an Open Source project or an Open Source infrastructure, but you can’t necessarily guarantee you have the resources to push things along on those road maps. Or necessarily that people’s motivations will be aligned with that road map. 

So whereas in a corporate environment or in a non-FOSS environment you can just pay people, effectively, to say: “This is what you’re working on!”

MEL: Right.

ERNEST: In the open it’s more of a… Hey, this needs [to get] done. And is somebody interested enough to either do the work themselves or is there a company or a corporation or some other donor who would be interested in funding… Making progress in this aspect?

MEL: So sometimes I’ve heard that characterized as top-down versus bottom-up. I’m not sure if that’s something you’ve seen before or if that seems accurate. Or if there’s a better way of explaining that.

ERNEST: I mean, I think I recognize what those two phrases mean. Like, top-down would be… The direction comes from on high. So does the money. And then you find people to do the work. Bottom-up… The ideas and the work and such lead where things are going. Is that effectively sort of in the ballpark?

MEL: Yeah. I bring that up because I’ve seen it said a bunch to describe Open Source projects. I’m not completely sure of… Personally… That that’s… It’s not inaccurate. But it doesn’t feel to me like it hits like… “Yes, yes. This is a good description. This is the perfect description of what happens.”

ERNEST: Yeah, I agree. It’s not perfect. Because as… Either the administrators of PyPI or as a community, we might all agree that something was a good idea for PyPI. And that might be filed as an issue. It won’t necessarily say: Somebody has to do this! It just says like… Hey, this is where the discussion for this has come from. This is the motivation. And it sort of goes from there. 

Versus… We do fairly regularly see people submitting a change and saying: Hey! This is in my interest. I’ve kind of worked on it. And it’s a good idea, or it’s something that’s not… It doesn’t interfere with other priorities. It doesn’t break something. And then yeah. That’s the more bottom-up. 

And then there are of course a couple of projects we’ve undertaken where we had funding, we had a scope, we had a road map, we had milestones, and we’ve found people to do that work. So it’s a fairly healthy mix, I think, as far as PyPI itself is concerned. I’m not familiar enough with any other similar projects to know how they work. 

But yeah. I can’t really imagine that it would be… I guess I don’t really imagine it would be super productive or welcoming for somebody to be running a project and basically acting as an order. Saying: This is what will happen. Someone must do this. And people falling over themselves. Saying: I’ve got to go do this work! So I don’t know. 

So top-down, bottom-up -- I don’t think it fits perfectly. Because there’s got to be a mix of sort of the approximations that those words have.

MEL: Cool. And then another thing I want to go back to a bit is… You talked about how… So I split up infrastructure projects and technical effort up into two things. One was operations. One was implementation and new feature development. And you talked about how those things were really intertwined. 

So analysis-wise, one of the things I’ve been trying to figure out is: Are they sufficiently intertwined that we need to put them together and have them be one category, technical effort? Or is there something important about the distinction of… Some of this technical effort is operations. Some of this technical effort is implementation and new feature development. 

ERNEST: I don’t think they’re perfectly independent. For a couple reasons. One of the reasons I don’t think they’re perfectly independent is there’s a large overlap in the skills. And so contributions to PyPI that make it operationally better are welcome. And they come through with some regularity. And then the features development tend to be more prolific by far. But yeah. I don’t think they’re independent, and they can’t be perfectly independent. 

But they are different. I think they need to be looked at in a different manner. Development costs… You know, either in people’s time or in money, or however you measure the costs… However you measure the costs, development costs tend to be immediate or sort of one-off. It happens now, and then generally there’s not a whole lot of additional cost. For the development itself. 

Operations, in time or money or credits or donations or however it’s measured… Operations costs are recurring. They can be difficult to predict. 

And so yeah. I mean, it’s a different analysis, in my opinion. Analyzing the sustainability of… Go ahead?

MEL: Okay. Yeah, no, sorry. I’m looking at what you said and nodding, going… You’re right. The way costs are allocated, not the nature of the work, but the way you need to think about resources, is quite different between the two.

ERNEST: Right.

MEL: That’s helpful for me to think about it that way.

ERNEST: Right. So the sustainability of a codebase doesn’t necessarily have a monetary… Doesn’t necessarily have a monetary analogy. But the sustainability of the operations of the service -- you can almost come up with a number. Right? You can look at the bills that need to be paid. You can look at the time costs to pay someone to, you know, address production outages. And keep things turning. Right? 

So whereas the sustainability of a software project… Certainly has a fiscal component. You could just pay someone to keep up with a project, somehow. But it’s not necessarily as clean cut.

MEL: Okay. Yeah. That’s very helpful. Let’s see. So we’re on four of five. If we spend a lot of time talking about this, that is also totally okay. I can send you: Here is everyone’s definition of sustainability and being well maintained separately, if need be. But this is great stuff. This is the next one.

> _Source(s): notes-11-10-2019.md_
> 
> 4. Infrastructure requires bureaucratic/organizational work. FOSS infrastructure is likely to have this set up late, during the “last mile” or the “sticking point.” Non-FOSS infrastructure is more likely to have this infrastructure (legal, organizational, financial, managerial, marketing, etc.) be set up early.

MEL: And this is one that we’re still trying to figure out vocabulary for.

ERNEST: I think this is… Ehhhhh… Trying to come up with the bureaucratic/organizational work… I think this is roughly accurate. Huh. Yeah. 

And it’s definitely true in my experience with PyPI, and with other parts of the Python infrastructure that are volunteer-driven, primarily. 

A really good example is the way that we handle in-kind sponsorship or in-kind donations/sponsorships that help us run all of this stuff. It’s very true that most of these things started as sort of informal donations, where somebody is like… Sure! Or somebody saw something they needed, emailed them, and said: Hey, can we use this to run X? Somebody says sure! Of course! Here you go. And then, you know, that’s the way it starts. 

And then we start running into issues where it’s like… Well, what about when it comes time for renewal? 

And when we started looking at the sort of… Like, the size of the liability of… If that just went away, certainly, bureaucratic/organizational work was undertaken to formalize those relationships so that we could have, you know, explicit time frames and amounts that could be relied on in some manner. 

So yeah. I think that it’s definitely accurate. That infrastructure does need some of that work. Because, again, it’s an ongoing thing that requires someone paying attention to keep happening. Whereas yeah… I guess it’s just pretty spot on. Whoever said this is… Whoever sort of brought these points up is pretty insightful.

MEL: So this isn’t an individual person. The things I’m showing you right now are not from interviews. They’re actually our first level synthesis across all of the interviews.

ERNEST: Yeah. Well, again, very insightful. And I appreciate the inspection of… Yeah. You’ve got to have some organization to keep these things moving forward. And it generally isn’t the first priority. And it makes sense too, because a piece of infrastructure might come up. It might be used. It might be important. It might be something that needs to continue. 

And then in that case… It could grow. And then it’s that growth that really requires the bureaucracy, I guess, effectively, to make sure that it can be kept online. 

A small project might be able to run for free in some hosting platform that offers a free tier, until it either proves itself or they realize… Hey, we don’t need this anymore. Or it’s just low enough volume that it can just sit there quietly for a long time with very little concern.

MEL: Okay. So the last one… I’ll just put it out here.

> _Source(s): notes-11-10-2019.md_
> 
> 5. Infrastructure user data and usage patterns are important for determining future resource needs. FOSS infrastructure maintainers are less likely than non-FOSS infrastructure ones to have complete and reliable access to that data because of intentional cultural choices to prioritize user freedom and access over it.

ERNEST: Sure. Gotta think through it, I guess. How some of these words spark things in my head.

MEL: Go for it.

ERNEST: Yeah, I mean… There are sort of two factors, I guess. That I would see underneath… Or I guess in this. One would be… Just the access to that data, those patterns. 

There are two reasons why it might not really exist or be a priority. One might be… Yeah. An intentional choice to say: Well, we’re not going to collect that. Because it sort of violates some freedoms. Or it’s collected, but there’s just no one who has the time or motivation to really analyze it. 

In a corporate or non-FOSS infrastructure, there are marketing departments. And there are people who are very motivated to get access to analyze these things and use them to, you know, better sell the product or increase the value of the product to the users, so that revenue and profit and all that stuff increases, hopefully. 

In the FOSS infrastructure world, I mean, my experience has been: We have been really diligent about trying to collect the bare minimum of information that is reasonable and store it. 

So a good example would be, like, PyPI has public data available on the project download stats. So how often a file has downloaded for a certain project in release. And that stuff is publicly accessible. But it’s very sanitized. And we don’t really hold on to the unsanitized data for longer than necessary. To get it into that public dataset.

So it exists. And it’s used for, like, a couple things, you know, to look at trending projects on PyPI, so that it can be displayed on the homepage, and we use it for analysis occasionally, to determine usage patterns that are problematic for us. So maybe to look at and see how often a really big project is downloaded, and what that might be costing us in bandwidth or something. 

But it’s not used extensively by us for any specific purpose. And there are a ton of people who use it for other things. But there’s no centralized authority that’s governing how it’s decided that it would be used. 

So yeah. It’s a matter of time and requirements. We don’t have anyone who’s spending -- we don’t have anyone who’s got the time to spend a lot of resources digging through stuff, just to find new insights. 

And we also don’t have a great way of communicating directly with anyone in particular about how they’re using PyPI to verify this stuff. 

And we sort of discussed in previous interviews -- like, we don’t have a great way of, you know, getting contact with a bunch of PyPI users to get information for how they’re using it. Once again, to verify if any of the insights that could have been made from that dataset are accurate.

MEL: So part of this actually came from the three of you as the PyPI upstream maintainers. They all talked about the challenges of not having that data, not having that insight. 

And Nick also told me a little bit about the lengths to which some of you had to go to get contact information for people. 

But then on the flip side, I believe it was Jackie’s second interview… When she was talking about… You know, “I’m really glad we don’t collect that information. I’m really glad it’s not required. Because from a privacy standpoint, both from a personal standpoint and also thinking about a corporate standpoint, it’s really nice to not have this. It’s really nice to know the information is not gonna be out there. It’s really nice to have that be a barrier to entry that doesn’t exist.”

ERNEST: Yeah. There’s a big liability in storing much personal identifiable information. I’m not a fan of doing anything that we don’t necessarily need to. 

So GDPR, for instance, the European privacy standard… I think we meet or exceed that, and we did that before it existed. Right? 

There’s not… I guess there’s not a benefit in just sitting on all of that data and waiting for it to become a liability or a leak. Right?

MEL: Mm-hm. So any other thoughts on sort of those five chunks of analysis I’ve served to you so far?

ERNEST: No. I think as far as how you differentiate the terms “sustainability” and “maintainability”, I think they all have fairly good insight into what those differences are. So yeah. I mean, particularly… Yeah. I think that they’re just good insights. So I find them interesting, and I’m kind of excited to see where they go.

MEL: Cool! So now I’m gonna show you the sort of aggregated version of what are people’s definitions of “well maintained”, and then, if we have time, “sustainable”. So this is the “well maintained” list.

> _Source(s): notes-11-10-2019.md_
> 
> 1. There are people there to triage and address issues that come up in a timely manner.
> 1. There are people to make sure a project is keeping up with changes in the ecosystem (ex: maintaining compatibility when dependencies are updated, etc.)
> 1. The project is following best practices regarding software development (tools, code style, tests, etc.)
> 1. The project cares about backwards compatibility.
> 1. The review process is clear. New changes can be evaluated effectively and merged if appropriate, and standards/expectations are clear to contributors.
> 1. The review process is pleasant; maintainers are friendly when contacted.
> 1. The project values inclusion and is visibly trying to be welcoming to a wide variety of contributors.
> 1. The project is regularly updated and has activity happening, AND this activity is fully and easily visible to outsiders.
 
MEL: Let me make that numbers instead of bullet points. There we go.

ERNEST: I like it. I mean, I think that it aligns fairly well with my assessment. A little higher level, I guess, than I generally think about it. 

And so I kind of like that these all sort of… You know, they’re not specifically calling out this kind of test or that kind of code style. No. 

I think I agree with all of them. I’m trying to think if there’s anything that isn’t missing.

MEL: Yeah. I’m curious about that. If there’s anything that you feel is not in this. Or also in the five chunks of analysis, if it’s like… These seem right, but there’s this really important factor of analysis you completely missed.

ERNEST: I mean, one thing that I do think is maybe missing would be something along the lines… I think point 7 sort of captures it. The project values inclusion and visibly being welcome to a wide variety of contributors is one level of it. 

And then the next level is: It’s clear how someone new could contribute. Which… Or there are good places for someone new to contribute. They’re well specified. 

I think it’s a requirement for 7, but I think being a little bit more explicit about… Not only is it welcoming. Just, I guess, I can feel welcome somewhere, but still not feel like I have a purpose there, I guess. You can come in the door and say… Oh, wow! This looks so good. But I have no idea what to do. And that I think would be a fairly deflating experience. Or could be. 

So I think, again, it’s part of part 7, but doesn’t necessarily get called out specifically to say… Not only is it welcoming. Once you’re attracted and in there, you actually find some way to be helpful or contribute.

MEL: Okay. And is there a way that you would edit or extend that specifically? Welcoming… I’m trying to figure out how I would edit number 7 to reflect what you just said. Do you have any ideas?

ERNEST: No. Again, I think part of visibly trying to be welcoming is making those issues available. Making those things clear. So again, I think it exists in that statement. It’s just not necessarily explicit. I don’t have a good edit for it, right off the top of my head.

MEL: I’m gonna try writing up a version of it. See what you think. This is a rough one. But...
The project has clear entry points for new contributors so they know how to get started.

ERNEST: Oh, sure! I think in addition to 7, or integrated into that statement somehow… “clear entry points” is fairly clear!

MEL: Okay. So this is the aggregated list across all the interviews. We’re still trying to wordsmith a little bit. I will put that on the list and show it to other people down the line and see what they make of it. 

Oh, look. We have just enough time for this. That was “well maintained.” This is “sustainable.” The sustainable one was much more all over the map.

> _Source(s): notes-11-10-2019.md_
> 
> 1. There are resources (donated services or money to pay directly) for ongoing operating costs, including computing resources, people for operations, people for development, and people for “management.”
> 1. Will the resources needed for the project continue to be provided in the future?
> 1. The “bus factor” is high.
> 1. Sustainability relies on maintainability; what is the overhead to the project continuing to exist in the world?
> 1. Continued improvement of maintainabilty; keeping a project “up to date”
> 1. Computing resources, either donated or via the fiscal means to afford them
> 1. Interest in its existence from users (“existence sustainability”)
> 1. Sustainability is a sort of artifact of people and an extension of their time; do people have enough time to dedicate to this, or are they spread too thin?
> 1. Are there new people onboarding?
> 1. Are there entryways for people to onboard?
> 1. Are maintainers burning out in silence?
> 1. Are contributions bottlenecked at one person, a single point of failure, with no clear pathway to engage the community otherwise?
> 1. Are various people taking on roles, or is it just one person?
> 1. Sustainability is hard to define with numerical metrics; you can try to count how many PRs there are, or average time for an issue to get fixed, but there are always more complicated reasons than that. 

ERNEST: Oh yeah. All over the map.

It looks like point 10 sort of captures what I was saying previously, on the last list.

MEL: Yeah. And one of the interesting bits is how various people started talking about the relationship between being well maintained and being sustainable. Because clearly they’re related in some way. And people talk about them being related in a slightly different way. And we’re still working on what to do with that.

ERNEST: Yeah. Yeah. Just frankly… I think one of the reasons why this is all over the map, as you said, or really fuzzy, is… It’s not clear that there’s necessarily a consensus anywhere on much of the sustainability aspect. 

I mean, there are people who have pulled it off. But I think that there’s been a lot less generalized discussion around it. 

There are people I’m aware of, who think about and talk about this a lot. Like, Eric Holscher has been very public about discussing the sustainability. Like Read the Docs. I think that’s a really good resource. Some of the things that Eric has written. As far as I’m aware, one of the better documented paths on that. But it’s just not the same for every project either, necessarily. 

Whereas I think from the maintainability aspect, there are expectations and a lot of experience in approaching the maintainability of a codebase. Because there are so many more codebases than there are services. Right?

MEL: Yeah.

ERNEST: And so… Again, I just think there’s a poorly understood… Generally understood. I think there are some people who have good grasps on it. You know, again, like Eric. 

But generally it’s not something that’s discussed nearly as much. And it’s not something that as many people have experience with. And that as a result leads to, again, it not being a quote-unquote “solved problem”. 

Not that I think maintainability is solved. But I think it’s much more discussed, and there are better standards and practices as a result, again, of just exposure.

MEL: And the scope of… When you talk about it being a more solved problem or there’s not a consensus… The group of people you’re referring to -- is this software in general? Is this Open Source specifically? But corporate projects have this figured out in their own way? Or…?

ERNEST: From a sustainability perspective, I think a corporate project generally will have much better guardrails. 

If your operating costs are outpacing your… If the operating costs of your infrastructure are outpacing your revenue, you can draw that line and very quickly realize… Oh, well, we’re not sustainable at this current juncture. We have to make a change. Or we’re gonna go out of business. 

So I don’t think there are a whole lot of corporate projects where, if they realized that, and reached out to new beneficiaries that they would necessarily have as much luck with somebody saying… Oh, sure. You can just have a discount on this, or run this for free in the meantime. So… 

Not to say that we necessarily have a 100% hit rate on that either. It’s not necessarily easy to forecast our needs as well. But we also have a benefit of, you know, we’re running this service as a benefit to the community. And there are a lot of companies that are part of that community. And either rely on the service or rely on the community. 

And so the value proposition is a lot higher. When it comes time for us to ask for, you know, what we need. So yeah. 

Again, if that list is specific to Open Source infrastructure projects or free Open Source infrastructure projects, then yeah. It makes a ton of sense that it’s all over the place. Because it’s something that requires more work. And it sounds like y’all are doing that work. So that’s really cool. But yeah. Again, it strikes me as reasonable that it would be… All over the place.

MEL: Cool! That is all I had. Is there anything else on sustainability, PyPI, maintainership, that you’d like to… That I haven’t asked or that you want to make sure gets mentioned before we wrap up?

ERNEST: I do not have anything off the top of my head.

MEL: Okay! And I have one last question. Sort of shifting that… What has it been like for you, participating in this research project? Has there been anything that’s been surprising or particularly interesting? And the reason I ask is that: If we do any other versions of this in the future, with other Open Source communities, or other people from Python, is there anything that we should be thinking about changing or adapting or doing? I’m curious about what the experience of participating in the project has been like.

ERNEST: Well, I mean, just the logistics of it have been really pleasant. So I think logistically, it’s been nice. There haven’t been any concerns there. 

As far as surprising goes, it’s been really interesting to hear… I guess at the distance between myself and these other people who I’m familiar with and have had discussions with… It’s interesting to hear their perspective on it through the lens of a similar interview. So it’s been really nice to hear those things. 

And also to be able to see the transcripts out in the open and look through them and just sort of get a feel for… You know, the ways that other people are viewing us. In explicit terms. Right? And in a similar format. 

So I’ve really appreciated it from that perspective. It’s been really nice to just spend some time even just in this format, just spend some time thinking about this stuff. And yeah. 

So I mean… It’s been enjoyable. It certainly hasn’t been a negative experience, by any means. I’ve really found it great.

MEL: Sure. And it’s been really helpful to talk with you as well. Thank you so much for all of your time, for being willing to participate, and then I’ll have Heather get in touch with you about… We have a little thank you stipend for people who participated. And we’re still figuring out the logistics of how to get that to you.

ERNEST: Thank you so much and thank you to the translator whose name I didn’t catch. Or the…

MEL: Mirabai.

ERNEST: Thank you so much to both of you.

MEL: Yay! Thanks, Ernest.

ERNEST: All right. Bye-bye.

MEL: I’ll see you at PyCon next year.

ERNEST: I’ll be there! Bye-bye.

MEL: All right, bye.
