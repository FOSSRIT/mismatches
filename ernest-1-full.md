# Copyright transfer statement

MEL CHUA hereby irrevocably transfers and assigns to ERNEST W. DURBIN III in perpetuity, all right (whether now known or hereinafter invented), title, and interest, throughout the world, including any copyrights and renewals or extensions thereto, in the attached transcript of the interview recorded between us on AUGUST 23, 2019 in A LIVE-TRANSCRIBED VIDEO CALL.

# License

I, Ernest W. Durbin III, hereby release this work under the following open license: http://creativecommons.org/licenses/by/3.0. Anyone is free to share and remix the work as long as they cite it. I consent to the open publication of this work using my name. 

# BEGIN TRANSCRIPT

MEL: Okay. Cool. And is it okay to start the transcript point now?

ERNEST: Absolutely it is.

MEL: Okey-dokey. So our first question: How would you like to sort of introduce yourself and your role in -- with the Python community and PyPI, I would say, both of those two things?

ERNEST: Sure. So I started developing with Python about ten years ago. And through the course of my career, I’ve used it more and more. I’ve sort of infected companies I’ve worked with, with Python. And through that time, I also began volunteering a lot with the Python infrastructure. It was… It matched up with what I was doing for my career, and it was… There was a need for it. 

And so starting in, like, 2012 or 2013, I started contributing to, like, Python.org’s infrastructure, PyPI’s infrastructure, et cetera. Over time, that grew and grew, and then in, like, 2016, you know, I began to volunteer more in the community stuff, with PyCon, as the PyCon chair. 

And then actually during that time, there was an opening or a need at the Python Software Foundation, for someone to contribute technically to the organization. Both for the community infrastructure that we run, and also for the systems that the Python Software Foundation uses to operate. So in 2018, in June, I joined the Python Software Foundation full-time. And through that time, I’ve just been doing, I guess, what the needs are. 

So one of the bigger contributions I’ve made over time has definitely been on PyPI. So the Python Package Index is by far and away the largest piece of infrastructure that the Python Software Foundation has a responsibility for. So initially that was taking the existing codebase and taking it to a point where it could even consider scaling to the needs of the community. And then over the past few years, it’s been in helping to maintain the new PyPI, or Warehouse. Yeah. And also overseeing some funded grant work on PyPI since.

MEL: Okay. And could you expand a little bit on your role in PyPI specifically? Or Warehouse?

ERNEST: Sure. So for six years, it was really just as a volunteer. You know, it was constantly breaking, and there was the ability for me to find time to contribute. And so that was… You know, helping the system itself run. So lightly working on the codebase itself, but primarily focusing on the infrastructure behind it. So the databases, the servers, the load balancers, the CDN, all the sort of bits that helped it operate. 

And with Warehouse, so there was a grant funded by Mozilla that allowed Warehouse itself to be -- as a project. 

So briefly, Warehouse is a complete rewrite of -- an implementation of PyPI. And it started many years ago. I mean, almost as long as I’ve been volunteering on the project it’s been sort of in flight. But it never really got over the finish line. 

So there was a funding application put together by a couple people in the packaging space that Mozilla accepted. And that was used to fund getting the Warehouse rewrite across the line. 

So through that project, or through that funded project, my focus was on the infrastructure for the new deployment, and also given my familiarity with the service, I did do a lot of work on the implementation itself.

MEL: Okay. So pausing on the PyPI story for a moment, and we will get back to that later on, I want to ask -- and I’m asking everybody about this, and the next thing we’re gonna do in our second round interview -- is swapping around everybody’s definitions. When you think about Open Source projects and the words “well maintained” and “sustainable”, and some people lump them together and some people don’t… What would your definitions for those two things be? What makes a software project well maintained and/or sustainable, and what kind of criteria do you use to determine whether a project is one or both of those things?

ERNEST: Hm. Sure. So I mean… Well maintained, my definition has sort of come to be a project that new changes are… Can be evaluated effectively, and merged if the maintainers themselves and the community desire the feature. So that’s the approachability of the project, to a newcomer, or to somebody who uses it, and wants to potentially fix a bug, or implement a new feature, so that’s sort of the logistical aspects of it. Like: Is there testing? Are there good definitions of what needs to be done? Or is acceptable or not acceptable? Are the styles for the project available? Et cetera. Not available. Defined, et cetera. 

So the well maintained aspect, to me, mostly comes down to the sort of… I guess the software itself, and the tooling around it that supports its development. Sustainable, you know, is… I think that sustainability sort of relies on maintainability.

MEL: Oh, interesting.

ERNEST: But it also depends a lot on what the software is. Right? So I have a handful of projects that I’ve worked on in the past that I consider very maintainable projects, and super sustainable, because there’s almost no overhead to continuing to have them exist in the world. 

If somebody comes along and says: “Hey, I’d really like to see a change in this library that you wrote dozens of months ago.” It’s not a whole lot of overhead for me to evaluate the change, to make sure the tests pass, that it hasn’t affected the people who might be using the project, et cetera. 

For other projects, such as PyPI, right, sustainability is very much a fiscal issue. PyPI requires some amount of… A significant amount of resources. Currently we pay for very few of them. Most of them are operated via donations. Without those donations, I’m not sure if a project like PyPI, for instance, would necessarily be considered sustainable. There’s just not the funding in place to pay out of pocket, in cash, for what it takes to operate the project. 

For other projects, sustainability might come down to… You know, whether or not there’s any interest in it existing. Or if there are maintainers or users around anymore. When a project loses all of its maintainers and loses all of its users, it’s clearly not sustainable as an effort. As a project. So I think the sustainability word specifically is an interesting one. Because there are sort of two factors. The financial sustainability and also the… You know, I guess project sustainability. Or the existence sustainability.

MEL: So talking about some of the things you said a bit… Sustainability -- you mentioned if a project loses all of its maintainers and its users, it’s not sustainable, but the way that links to what you talked about with well maintained -- so thought experiment. If an Open Source project was beautifully documented, all the stuff is listed in an issue tracker, processes and so on for everything, and then for some reason, an asteroid takes out all of the maintainers and users, but the survivors that are left somehow have internet access… And they don’t care anymore… So the people are gone. So it’s not sustainable. But it’s still, like, pristine, flawless, operating, well documented, everything. Is that still well maintained? Are those two things separable -- is what I’m trying to ask.

ERNEST: I think that’s interesting. It’s a great thought experiment. I will say that… Not necessarily, right? It could be revived. But with the changes in the language it’s implemented for… Right? So if a project is implemented for Python -- so say our theoretical project was written for Python 2.7, and this disaster strikes today, and then in five years, somebody goes to pick it up, at that point, Python 2.7 will no longer be maintained, et cetera. And so the lift to bring the project to, you know, the current Python, whatever it is, might -- it would benefit from that preexisting maintainership, but it wouldn’t necessarily guarantee it, right? The changes could be so dramatic that nobody can just pick it up and run with it. 

And so part of sustainability, I guess, is the continued improvement of that maintainability.

MEL: Oh, okay.

ERNEST: Right? So if you have a project that you just… Only come back to once in a while, and it’s been a very long time, the dependencies you use might have been updated, the runtime that you’re targeting might not be the same, et cetera. And so it takes some… You have to exercise the maintainability in order for it to exist, right? That’s where the sustainability aspect comes from. Is it sustainable, in order to keep it up to date, and again, that depends on maintainability, in my view, anyway.

MEL: So I think what I’m hearing is maybe like… A cost to maintain each kind of project, based on how big it is and how complex it is and how much infrastructure resources it consumes. And so well maintained is -- is this cost paid? And sustainable is: Will it continue to be paid?

ERNEST: I think that’s a really good way to put it, in a nutshell. Thank you for clarifying my thought so well. I think I agree very much with what you just said. Yeah.

MEL: Okay. And another question on what you said about sustainability is: Let’s see… This is the lovely thing about getting the realtime transcription also. I can understand things, and I can scroll back! And all of us can scroll back, in fact.

ERNEST: Yeah, I’m very much enjoying the transcription, by the way.

(laughter)

MEL: So… Here we go. Ah, okay. So you’re talking about PyPI requiring a significant amount of resources. Could you talk a little bit about what different kinds of resources it requires?

ERNEST: Certainly. So the largest ongoing cost to operating PyPI is just the infrastructure -- the technical infrastructure that it takes to operate the service at this scale. So currently that is, you know, a decent-sized postgres database, a decent-sized Redis database. Somewhere on the order of like… 6 mid-sized servers. Load balancer infrastructure. Which currently is provided by Amazon. So that’s sort of everything in the core hosting of it. Right? Just operating the services that run the code. 

And then we’re very dependent upon our CDN, our content delivery network. Fastly has been providing free CDN service to PyPI for… I think since 2013 or so. And we’re absolutely dependent on that to serve all of the files. I mean, the amount of bandwidth and the number of requests that are terminated at the CDN and never have to go to the backends… Is immense. Something like 99 -- over 99% of the requests that come into PyPI.

MEL: Oh, wow!

ERNEST: Don’t actually have to talk to the backend. That’s not saying that the backend is doing nothing. You know, I don’t have numbers at hand. If you’re interested, I could pull them up pretty quickly. But, you know, it’s something like 100-ish requests per second are making it back to the backend. And so that’s a decent amount of traffic that the backends have to handle. And some of those are slow and fast, et cetera. So it’s a good mix. But the vast majority of it is dependent upon that CDN. 

So from a technical aspect, you know, it’s on the order of like… I forget. I don’t want to pull a number from the air, and be incorrect. But our hosting bill itself would be, if we paid for it, somewhere around, you know, $9,000 to $11,000 a month, US. And our CDN bill is almost… I think -- again, this is where I want to be careful not to over or understate it, but it’s significant. On the order of a million or more a year, I think. If we were to pay for the CDN.

MEL: Wow! And from a sustainability standpoint, thinking about the definition of continuing to provide it, Amazon and Fastly are donating these?

ERNEST: Yeah, that’s correct. Amazon sponsors the PSF and PyPI with an in-kind donation. And similarly, Fastly provides CDN service at no cost. And that’s not just for Python. I mean, Fastly provides that same service to a number of Open Source -- like the Debian archives and a handful of other package repositories.

MEL: And if you were gonna compare that way of getting these services provided to, say, what might happen if this was a corporate project, and they had a contract with Amazon to deliver those services and were paying for it, do you see the sustainability as any different between those sorts of scenarios?

ERNEST: Sure. I mean… I think one of the biggest differences would be that we probably would have to charge for PyPI. Right? There probably would be some usage-based charge that’s commensurate with either hosting a project there or for accessing it. 

I also probably think we would be a little bit more persnickety about some tuning things. Right? We might have to find more optimizations throughout the entire stack. We might have to enforce rate limits, et cetera, to manage that cost. We do a lot of that, but we’re definitely not as fine-toothed as I’ve been in my career with some services I’ve helped -- I’ve been paid to operate. In that corporate-type environment, where we really did spend a lot of time sort of going through, piece by piece, trying to find out where we can reduce costs. We keep an eye on this stuff, and we try to be good stewards of these donations. But since so much of the work is provided by volunteers, it is beneficial to not have to worry about it as closely. Right?

MEL: Mm-hm. So not having to do that kind of level of optimization and tuning, or maybe a better way of phrasing this question is: What would change about the way that PyPI runs or what developers might do with it, in terms of being able to allocate your resources and attention and so forth? What would change if PyPI had to make that kind of shift? Does that make sense?

ERNEST: Um… I mean… Yeah. I think… I’m not sure. So you’re saying if PyPI suddenly was a company…

MEL: Well, so… So it sounds like, from the description, that one of the things that Amazon and Fastly and those donations are enabling you to do is to essentially not worry about those resources, and not worry about pinching every single penny, because oh, no, we’re gonna run out of money. And so being able to not worry about that lets you do other things. Rather than having to be like… Oh, first and foremost, we have to always optimize for this forever.

ERNEST: Oh, sure. I mean, it makes… It basically frees up the volunteer time that exists to look toward the future and implement new features. Right? If we had… If everything changed suddenly, we would have to do an immediate focus on optimizing costs, for sure. And that would detract, I’m fairly certain, from other endeavors. To add new features or refine existing features. Right?

MEL: Mm-hm. And so with the… Are there other kinds of resources? Sorry that I sort of interrupted you on that. You were talking about -- with the infrastructure stuff. With the CDN. And the hosting. Are there other kinds of resources? Like people time, or marketing donations? What would you call the rest of the infrastructure that PyPI needs to operate the project?

ERNEST: Yeah. So I mean… Certainly volunteers who are fixing bugs or helping us discover bugs… I mean, that’s a huge part of operating it. Right? Everyone has new use cases, more interesting use cases. 

A specific example, for instance, that’s sort of on top of mind right now is: There’s a lot of interest in better license specifications on PyPI. And so the PyPI administrators/maintainers, of which there are three, we don’t have a full view and a full understanding of the intricacies of license specifications for Open Source projects. And so a lot of the discussions in the community -- those are occurring both on discuss.python.org and also in PyPI’s issue tracker itself. 

You know, I guess the community infrastructure, if you will, is really… The people, the depth of expertise, and all the varying use cases that people have… And then in a similar facet, a lot of the changes that aren’t big enough to fund are being made by people in their volunteer time. And so, again, that’s effectively community infrastructure. There are a number of people who find some time now and again to contribute for free to the service.

MEL: Okay. So… Transitioning back to PyPI’s story here, thinking about the definitions that we’ve been talking about, about the projects being well maintained and projects being sustainable, how would you evaluate PyPI as a project on those two fronts? And if you were gonna tell the story about PyPI as a project, as you experienced it, and its well maintainedness and sustainability over time, what would that arc be? What would that graph look like, and why?

ERNEST: Oh, sure. So let me just… I guess start with the current picture. And so the current picture for the project is that it is, in my opinion, one of the better -- one of the better maintainable… Let’s see. It ranks pretty high on maintainability from a development perspective. 

There is extensive test coverage. 

There is good documentation for a lot of the common operations a developer has to undertake. 

There’s a very big issue tracker. It’s well classified. That allows people who are looking to contribute or looking for high priority issues to identify them. 

There are good automated integration tests, and there are also -- I’m sorry. Not integration tests. But good automated tests. 

And good specifications for what the service is supposed to do. 

So with that, it provides the ability for nearly anyone who has the basic skills to contribute to the project. Without having to think too much about breaking some other feature they didn’t intend to, without realizing it, right?

MEL: Mm-hm.

ERNEST: So from that perspective, it’s very maintainable. 

Also, we have a continuous deployment pipeline that gets changes out to production on a very regular basis. I think we’re well over 1200 deployments since PyPI launched two years ago, or more. I can’t remember at this point. We passed the 1,000 deployment mark, I think, a little bit after it had been deployed for a year. 

So it’s reliable, it has good metrics as a service, which helps for maintainability as well, from an infrastructure administration, sysadmin-type perspective. And so we’re able to keep tabs on it really well.

MEL: Mm-hm.

ERNEST: So that’s now. In the past, it was different. So PyPI is, as a service, something like 17 years old. And the Warehouse is the second, you know, sort of imagination of the project. The project started, you know, well in the history of Python -- like, as a web language. And when it was originally written, there weren’t any of the fancy modern day web frameworks.

MEL: Right.

ERNEST: Testing was known and something people definitely did, but wasn’t necessarily as highly valued for, you know, what was effectively a pet project at the time. It was… Hey, can we do this? And then they went for it, right? You know, over time, PyPI grew sort of… Exponentially. 

And, you know, it evolved to keep up, but also, along the same lines, it started to grow new features, and features that weren’t necessarily core to what it needed to be doing. And so somewhere around 2012 or 2013, PyPI was starting to really show its age as a service.

MEL: Mm-hm.

ERNEST: There were a lot of regular outages. There were sort of… It was common, I guess, for changes to go out that broke things unexpectedly. There were, like, two working tests for the service.

MEL: (laughing)

ERNEST: Yeah. It had features like an oauth consumer and an oauth provider that were in very, very low use. But caused a lot of headaches. It had features like SSH for uploads to bypass the fact that, you know, it didn’t have TLS for a really long time. 

And so over time, also it didn’t really have any in-depth monitoring. Sort of the best monitoring that it had was: Is PyPI working or not? Like, can I get to it? And so over time…

MEL: Literally can you go to the web page and see it?

ERNEST: Yeah, effectively.

MEL: Dang.

ERNEST: Like, basically just uptime monitoring. Is the service responding? 

So… With time, you know, we were able to implement a lot of additional -- we were able to resolve a lot of those things slowly. There was an effort by myself and Donald Stufft, who at that point were basically the only people contributing to the service, to implement some monitoring, to improve the reliability of the service, to improve the underlying infrastructure that it runs on. And all at the same time to make some progress towards, you know, the specifications and desires of the community for the service. 

So it wasn’t all bad, but there wasn’t a good open door that any developer could sort of walk in and do anything with PyPI. It was very difficult to run locally, to sort of make changes and play around. Again, since there weren’t tests, it was really hard to verify that you hadn’t completely screwed up some other feature that you didn’t realize. And so, you know, again, it was just sort of showing its age. 

So I think with enough time the existing PyPI implementation could have been somehow evolved, very slowly, and with lots of effort, into where we’re at now. 

But there was really good work put in on Warehouse already by Donald Stufft over years, towards that goal. And so Donald I think was really guided by all of the sort of negative things, I guess, I just sort of said. Right? Guided by all of those things to implement Warehouse initially with those in mind. So things like monitoring were sort of built in from the beginning. Tests and test coverage and making those tests easy to run was sort of there to begin with. Et cetera. 

So yeah. I think the arc honestly probably… If I had to draw it… I’m gonna see if I can try to explain a graph. But I guess if we were on a scale of one to ten, I think when it first showed up on the scene, it was probably somewhere in the five and six range. It was a small service. It wasn’t doing a whole lot. I mean, at that point, it didn’t even actually host packages. It was literally just an index. 

And so it probably started as a five or six, and slowly, over nearly ten years, sort of degraded to like a one or a two, if that. On maintainability. 

And then slowly sort of crept… It begrudgingly climbed back up to like a three or a four, maybe. Just as we sort of kept PyPI -- the initial implementation -- on life support, effectively, awaiting Warehouse. 

And then when Warehouse deployed, I would say it rose to what I would consider a nine or a ten. You know, basically with the deployment of that service and the turning off of the old servers. 

And we’ve kept that. The project continues to be maintained. It continues to stay up to date. And we haven’t given up on any of the goals around testing and automation, et cetera.

MEL: Wow. And is that graph for well maintainedness, sustainability, or both?

ERNEST: I would definitely say that that is specifically for maintainability.

MEL: Okay.

ERNEST: Sustainability is sort of a different graph. I mean… I think there’s the theoretical sustainability, which is… You know, PyPI can’t really, quote-unquote, “go away”, and so I think that it will remain sustainable, because there will always be people interested in making sure that it is around. Not always, but for the foreseeable future, people will always be interested in seeing it stay around. And so if we ever needed help or assistance in some way, I’m sure that we could bring that together. 

I will say that the current way that it’s sustained is somewhat fragile. From a financial aspect. You know, it’s sustained via donations, and if one of those big donations went away, it would be a little bit of a scramble to either come up with the funds to pay for it out of pocket by the PSF or to fundraise from the community to do so, or to find someone… Some other company willing to make a similar donation. So from that perspective, it’s somewhat fragile. Right? 

And the paradigm shift from going from in-kind donations from companies to try to fund it from a more grassroots effort would be a significant change. And something that would be… Not necessarily difficult, but slow. Certainly slow. And I don’t know what… How that would impact the service in the mean time. Or during that transition. 

So I would say it is fairly sustainable, and it feels like it’s getting more sustainable regularly. You know, we’ve made an effort, in making it very maintainable, to hopefully having that impact the sustainability. And so we have more contributors than ever, who have contributed to the project recently. I mean, it’s literally more than two, which is a really good start. And it is, in reality, it’s significantly more than that. It’s probably something like 50 to 100 people have contributed to the project, whereas previously, for a long time, it was really just a handful.

And so from that perspective, it’s getting more sustainable, and also some of the funding projects that we’ve undertaken -- funded projects that we’ve undertaken -- have really contributed to the financial sustainability of it, in that as we have success with a funded project to launch Warehouse, it makes it easier to seek funding to improve Warehouse. 

So after the Moz Grant, we have also had a Carryon-funded project by the OTF, the Open Technology Fund, to improve the security of PyPI, and also the internationalization and localization for… And accessibility for the service. So having that story of the successful Moz Grant was impactful for, you know, seeking additional funding.

MEL: Mm-hm.

ERNEST: So from that perspective, again, the sustainability feels fairly fragile, but I don’t think that it’s… You know, I don’t think that it’s in danger, necessarily. Right?

MEL: How much of a runway would you have, if funding abruptly stopped, for some reason? How many months would you be able to keep on doing what you’re doing, before you would be like… And we’re gonna run out of money on this day!

ERNEST: It certainly depends on which donation it is. That’s really hard to say. And I don’t… If all of our sponsors pulled out in one fell swoop, I think that PyPI would probably just have to turn off more or less immediately. Versus have to pay all of the bills that moment. Right? If we had notice from a sponsor that they were like… Hey, we can’t do this for you anymore, and we’re gonna turn you off in a few months… Which has happened… With that, we can seek a different sponsor, or prepare for paying it. Right? 

But at its current cost, no, I mean, just the CDN bill alone would probably be significant enough that it would be fiscally irresponsible for the PSF to try to pay for that, since it would… I mean, the PSF has a general fund that backs it up for its operation. Right? That’s paying… It’s the fiscal outlay for PyCon, for paying employees, for the grants, et cetera, that the non-profit performs. There’s a small reserve fund for infrastructure concerns. But it’s not significant enough that we could, you know, pay for PyPI indefinitely. You know. Or not knowing exactly how much even that first month would cost. Right? I mean, it’s somewhere on the order of hundreds of thousands of dollars, theoretically, right?

MEL: Yeah. The numbers you were quoting earlier were like… Oh my gosh.

ERNEST: Right. So we have had sponsors pull out in the past. They’ve always been really generous in what they’ve provided for us. And then when they let us know that they no longer are able or willing or whatever to make that donation continue, they’ve always been really responsible and kind to us, to give us -- to let us know when it’s gonna terminate, and give us some time to figure out… 

You know, we recently went through this for the more general Python Software Foundation infrastructure, for the hosting provider who had been providing all of the various services since 2012 or so. So you know, six and a half, seven years of providing that -- they gave us a termination date. We figured out where we would go. We worked on migrating. And it was more or less seamless. Most people probably didn’t notice it happened. And that’s because we had a decent amount of -- we knew when it was gonna be. And we could make plans. If there was a more immediate change, I’m not sure exactly what it would look like.

MEL: So I’m curious about the… Talking about financial sustainability here, and the cost it would take to operate the infrastructure resources… The rewrite of PyPI to become Warehouse… How much did that change the infrastructure costs? So would it cost less to run the new version of PyPI than the five years ago version?

ERNEST: It was kind of a wash, truthfully. The new implementation is… Well, the new implementation runs as a composition of a handful of services. Not just one little service running. Right?

MEL: Mm-hm.

ERNEST: And so that increases the complexity a little bit, which increases -- there’s basically an overhead cost to running multiple services, versus one. And so I think it’s about equivalent. Even though the new service is a little bit more efficient. We also are running a handful more services in combination. So I think it’s, again… I would probably estimate it to be about equivalent.

MEL: Yeah. And it’s also hard to compare, because over time, the demand on PyPI would increase, and more people are using it, so…

ERNEST: Indeed.

MEL: So from an infrastructure perspective, and a sustainability perspective, what did the move to Warehouse get you? So you mentioned already ease of contribution and people being able to work on it, even Donald. What else did that get you?

ERNEST: I mean, a lot of safety. Right? When tests fail, we know to look for something that might…

MEL: Mmm.

ERNEST: Something else might have broken. So I think that overall the service has been far more reliable. To the community. As a result of this. 

And then, you know, I think generally it was sort of a morale boost, I think, for both the people working on the service and for the community as a whole. You know, there was a lot of excitement around the new PyPI, et cetera. Which I think was beneficial. Right? It’s just positive. It was a nice injection of happiness and excitement into the community. Let’s see. What else? I mean… Realistically, it’s hard to say, right? I don’t have the best visibility, globally. As far as just all of the different facets. 

But from an infrastructure perspective specifically, it has been really beneficial, just in having a much better understanding of the service and what it takes to run and how we run it. And yeah. I mean… The codebase being a little bit better documented and all of that really has helped just in the maintenance as well.

MEL: And also -- the morale boosting -- I don’t want to understate that. If you’re describing contributors and volunteer time as being absolutely crucial to this, then things that get people excited and more energized about things is a huge increase in this vital resource for keeping up the project.

ERNEST: Oh, absolutely. And so we even tried to juice that a little bit. During the last few months of the Moz Grant and a little bit after, you know, we had stickers printed up that -- I think I mailed stickers to, like, 10 or 15 different countries. For new contributors to PyPI. Or first time contributors. So it was. I mean, it was really impactful. I agree. I think you do a good job, again, of putting a fine point on how important it was that people were excited, and not just excited. Capable. 

Because I think there was always a lot of excitement at the opportunity to contribute to PyPI. But it wasn’t necessarily something you could just do. Right? You couldn’t take your skills and apply them immediately. There was a lot of… There were barriers that didn’t need to exist and shouldn’t have existed to that. And so the combination of that -- yeah. I mean, it built on new excitement and it enabled a lot of existing excitement, if that makes sense.

MEL: Yeah! So… Looking through… And I’m curious about… So you were describing the graph, where it started at five and kind of went down to a one and now it’s up around nine or ten. Could you help me get a better sense of what those levels mean? So a level one is… This is happening, that is happening. A five is this is happening, that is happening. So what does the project look like at either of these levels?

ERNEST: Okay. So at a one, it’s sort of dangerous or spooky or scary to make a change to the service, right? Like… The changes come with high risk. Honestly, maybe perhaps it’s worth saying that these levels are sort of the inverse of the risk of a change. Or the complexity or the danger of making a change. Right? And so at a one or so, the risk is very high. And at a nine or a ten, the risk is very low. I guess at ten there would be no risk. 

So maybe we’re not at a ten, because there’s still some ways that we’ve… Excuse me… Shipped changes to PyPI that have, you know, broken people. But it’s a lot less common than it used to be.

MEL: Hm. And… I’m scrolling up through the transcript. And so that being… Since the graph is maintainability, that implies that maintainability is the inverse of “Oh my gosh, will changes break this?” 

ERNEST: Maybe. I think that that’s a pretty good proxy, anyway. 

You know, aside from just the risk of a change, there is also the developer experience. Right? So the people who actually want to do the work or are attempting to do the work -- you know, those numbers sort of, again, are the… A good proxy. Right? 

So at a one or a two, there are barriers. It’s kind of annoying. You’re not sure exactly what to do or how to do it. And at a nine or a ten, you have a pretty good direction or an idea of… Oh, this is pretty straightforward. At least where I need to start thinking about this in the codebase, or how I would go about implementing. Right?

MEL: Oh, huh. So what you’re saying is: Maintainability is not just from the perspective of, like, really experienced maintainers, but there’s also an angle for new maintainers here.

ERNEST: Sure. And that’s, again, sort of why I see sustainability as being dependent upon maintainability.

MEL: Yeah. That makes sense.

ERNEST: Yeah. Because if you can’t attract new people to your project, eventually just by attrition, you will end up with fewer and fewer people who either are capable or desiring to maintain something. Right?

MEL: Yeah. So that would imply, with maintainability, then, if there was a project that had, you know, one maintainer who was amazing and on top of all the things, but there was no documentation and absolutely nothing… If that person, the bus factor would be really low. If that person left or vanished… No one else would know how to take over -- so it’s basically the “Works for me!” Is not… Does not mean something is maintainable. If the current maintainers are like… Oh, this is fine! But no one else can get configuration up or figure out how to do it, that project is not well maintained?

ERNEST: Yeah. I mean, absolutely. And in a way, it also has a snowball effect. Where the more maintainers you add and the more maintainable the project is, the more maintainable it becomes, because more people are attracted to it. They come in and they sort of share their pain points or the problems they had, and then if you address those, then you improve the maintainability. If you don’t, it stays the same. But you won’t necessarily attract maintainers from that perspective. 

And so there’s… There have been a lot of improvements to PyPI’s maintainability since it launched, just from more contributors coming in and saying… “Hey! This isn’t working for me.” Or, “I was confused by this. Here was some friction I came up against.”

MEL: And so you’re talking about the pain points and problems they had, becoming contributors, as separate from: Here’s the bug I want to fix in PyPI itself? 

ERNEST: Yeah, but I think it sort of comes hand in hand. There have been a handful of situations I’m very aware of where somebody was able to get everything up and running and going, but there wasn’t enough information, necessarily, to, like, carry forward to complete the thing they wanted to. Right?

MEL: Yeah, yeah.

ERNEST: But that’s sort of a generic problem that -- any service or piece of software might have. Where if the answer is not known, just because something is implemented doesn’t mean that it would be merged or that it would be, you know, acceptable. Right?

MEL: Right. Okay. Is there anything else? The first round story of: PyPI, the maintainability, sustainability story arc here… Is there anything else in the story that you feel is important to get out now that you want people to know, this first round? And you’ll have opportunities to come back around to it and tell us again.

ERNEST: No, I think this has been good. I’m actually looking forward to reviewing this again myself. This was a really good exploration, and I think you did a good job of guiding it.

MEL: And… So for the second and third rounds, what we’re gonna be doing is getting -- once everyone’s transcript is up and open licensed, then that means I’m gonna be able to show you what other people said and pull together pieces of like -- oh, here’s what they said about sustainability. And here’s what they think the backstory of PyPI maintainership was. Or maybe they said they didn’t know anything about it. And that’s important to know also. Is there anything that you would be curious about finding from other people’s perspectives? And so we’re gonna be interviewing two other people that were deeply involved in PyPI to Warehouse’s transition, and then three people who were really active in the Python community, but not involved in PyPI specifically. As users of PyPI. Is there anything from that perspective that you would like to see, so I can make sure to pull it out for the next time we talk?

ERNEST: This is a really good question. Can I get back to you on that?

MEL: Absolutely, yeah. 

ERNEST: Yeah. If I think of anything, I’ll send you an email. Hello? Still there? 

MEL, TYPING: Still here, did audio cut out on my end?

ERNEST: Heh. Oh, okay. If I think of anything, I’ll send you an email.

MEL, TYPING: Ok! That sounds great. Sorry for the infrastructure weirdness. 

MIRABAI: I can hear Ernest, but not you.

ERNEST: I’m not getting audio from your end anymore, Mel. Well, I guess that’s good timing for the… The audio to cut out! 

MEL, TYPING: Yep. Sorry about that - let's wrap up and then I'll email the transcript probably later today. Thanks so much! (waves) 

ERNEST: I really appreciate your time. And again, the questions you asked were really solid. So… I look forward to future conversations! All right. Thanks. Bye-bye!

MEL, TYPING: Thanks, Mirabai.

ERNEST: Indeed! Excellent job!

MEL, TYPING: No idea what… Thank goodness for transcripts.
