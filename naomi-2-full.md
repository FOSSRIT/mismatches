# Copyright transfer statement

MEL CHUA hereby irrevocably transfers and assigns to NAOMI CEDER in perpetuity, all right (whether now known or hereinafter invented), title, and interest, throughout the world, including any copyrights and renewals or extensions thereto, in the attached transcript of the interview recorded between us on SEPTEMBER 20, 2019 in A LIVE-TRANSCRIBED ONLINE VIDEO CHAT.

# License

I, Naomi Ceder, hereby release this work under the following open license: http://creativecommons.org/licenses/by/3.0. Anyone is free to share and remix the work as long as they cite it. I consent to the open publication of this work using my name.  

# BEGIN TRANSCRIPT

MEL: Okay to start recording?

NAOMI: Sure.

MEL: All right. The transcript starts now. Thank you again for doing this. I am super excited. We return to our PyPI story. And so I want to start with one of the questions I asked at the end of last time. Which is… What you said you were interested in looking at in the second round. And continuing to the third round. And so I’m gonna put in the transcript right now… Your answer to that question.

> _Source(s): Naomi-1_

> NAOMI: I guess I would be interested, maybe, in knowing a bit more about the issues that they were specifically trying to address... For example... we were having this problem because of overcapacity, X times a week. Or something like that.
>
> [and]what level of success have they had, then, in specifically addressing those particular things? So, you know, now we can do all of this, zero latency, and whatever....
>
> ...I would also be interested in whether or not or how or anything that they’ve considered in terms of some of the things we talked about, in terms of attracting more people to work on this, and maybe an even more inclusive and diverse bunch of people.

MEL: So let me know when you’re done reading that and if you have any responses you want to add before I start showing you bits and pieces.

NAOMI: I’m done. Yeah. I guess I’m fine with that.

MEL: Okay! Let me edit that bit. Okay. So… Today I’m gonna be showing you pieces from the stories of three of our upstream developers. And since I’ll be giving permission for the transcript to be published and everything, we’re gonna actually read some names. So the first one is Donald Stufft, who you know as -- many people consider the developer of PyPI.

NAOMI: Right.

MEL: So here is a little bit about that.

> _Source(s): Donald-1_
>
> DONALD: I’m at least one of the technical leads, if not the technical lead. And I’ve sort of evolved into that position over time, where originally I was just sort of this outsider, trying to contribute to it. And, you know, I got the Commit Bit set, because Richard got tired of me emailing him patches, and then he stepped back and I sort of started to take over at that point. It just kind of evolved from there.
> 
> MEL: And when was that transition? When did you get the Commit Bit, roughly?
> 
> DONALD: I could look it up, but I want to say probably around 2012, 2013.

NAOMI: Okay.

MEL: Okay. And then I’ll give you a little bit more from Donald and how he got involved in PyPI. And if at any point -- this is a little bit of a prelude to the question you’re asking, but we’re starting to get there.

NAOMI: Mm-hm. Okay.

> _Source(s): Donald-1_
> 
> DONALD: So my history with PyPI is a little weird. So my first actual involvement with… My first major involvement with packaging is me getting mad at PyPI and saying: I could do better! And setting up a competing service. So I’ve sort of been trying to rewrite PyPI from the get-go, in some fashion.
> 
> MEL: [Why were you mad?]
> 
> DONALD: Oh, it went down. I believe it was just downtime. And then I spent… I remember, because I joke about it, because it was Christmas Eve. I had bought a domain name and I hacked together a basic hosting service that would just sort of suck in everything from PyPI and rehost it. And be better in ways like… Hey, we have a valid HTTPS certificate. We have a web UI -- just Twitter Bootstrap’s framework, but it looked relatively modern, instead of old PyPI’s horribleness. And things of that nature. 

MEL: And now I think this is the… One of the first answers to the question, the first question you asked, which was: What were the problems they were trying to solve?

> _Source(s): Donald-1_
>
> DONALD: So the history of PyPI is that PyPI pre-dates every modern web framework in Python. So… It pre-dates WSGI. Sorry, I think it is a contemporary of WSGI. If I’m going back in my history. But… So PyPI originally was not a WSGI service. It has no web framework whatsoever. 
> 
> It just sort of is proof of concept that Richard wrote one evening. Or one weekend. That then eventually came on to be production for every Python programmer. 
> 
> But so… Basically nobody knows how to contribute to PyPI, until you spend a significant amount of time digging into PyPI’s codebase. And that codebase was not very good. Again, this pre-dates modern practices and thoughts on unit testing and code structure and what-not. So PyPI was roughly… The bulk of PyPI was contained in two files. Each of them were about 3,000 to 4,000 lines long. And it had almost no unit testing or testing whatsoever.
> 
> And at some points in its time, you have to -- to run it locally, you had to actually comment out bulks of -- parts of the code to make it run locally. So at that time, this is where test PyPI came from. The way you worked on PyPI is you just sort of committed code. Pushed it to test PyPI, to see if it broke. And then if it didn’t, you would push it to PyPI and hope that PyPI and test PyPI’s production environments had not drifted enough apart that now it would now break in PyPI. Which did happen. Or just that the amount of traffic and varying traffic PyPI got was different, and would also break it. 
> 
> So when I sort of stepped into the project, and got involved, I figured out how to -- you know, I figured out the whole mess of the codebase. And at that time, there were approximately two people on the planet who understood PyPI. Me and Richard. Three, I guess. If you count Martin. But he wasn’t involved, really, anymore. So there were two to three people on the planet who currently understood PyPI. 
> 
> ....I concluded that the codebase was just so bad that there was no salvaging it. Like, trying to do anything effectively was rewriting the whole thing anyways. And we had no unit tests. So any change we made broke things every time we deployed, basically. 
> 
> So I was like… Okay. We’re gonna start this over from scratch. Taking what we’ve learned here, and really focus on making it something that is significantly easier to both get new contributors on board -- because bringing in new blood, I believe is… I forget if I mentioned that. But it’s part of sustainability. Being able to attract new people. And making it easier to maintain. And sort of solving these best practices problems. And also just making it possible to run it locally, without commenting out code, would have been nice. 
 
NAOMI: Okay. Makes sense.

MEL: So one of the answers I found was -- actually, people being unable to contribute was a big problem that you’re trying to fix.

NAOMI: Right. And that certainly makes sense to me. And is consistent, I guess, with things I know about how such things develop. So the whole scenario of writing a proof of concept in a weekend that months later has become production, and then runs for years is… Yeah. It’s a thing.

MEL: And one of the things that I’ve been talking about with some of the other participants in this study is: How that model is in Open Source projects, versus a piece of software that would be started off and… Okay. What we want the SLA to be, what -- it doesn’t start as a side project. It starts as a corporate project at some point.

NAOMI: Yeah. I mean… That’s true. Although I’m not sure the distinction is just corporate versus Open Source versus the size and the amount of hierarchy in the organization. I worked as a tech director in a private school for a long time. And more than one of the things I did just to see if they would work then ended up running for years. And kind of becoming a curse that way. And I’ve run across that even in smaller business environments as well. So yeah, if you’ve got a hierarchy around the development of software, this would be less likely to fly. But I think that’s really the case. It’s that kind of built-in hierarchy, whether it’s business, not for profit, I mean, of course, Open Source projects are very unlikely to have that kind of hierarchy. But yeah.

MEL: Well, even something as large as the Python community, PSF, is pretty substantial in terms of relative to the size and scope of other Open Source projects and communities.

NAOMI: Right. But… We don’t have… We’ve never really had any sort of hierarchy, because we’ve never had any paid developers in any long-term sense of the word. So it’s very difficult with a volunteer organization to impose that sort of hierarchy. I know that people sometimes expect that somehow the PSF should take care of it. And yet… How? People will just leave if you tell them to do something they don’t want to do.

MEL: Right. And I think that one of the things that’s sort of an interesting situation for places like the Python community is… A really large community. A super small paid technical staff base.

NAOMI: Mm-hm.

MEL: And then that space of people whose jobs pay them to contribute to Python but don’t work for the PSF.

NAOMI: Right. And I don’t know… I don’t even know how we get a handle on how many people are in that space.

MEL: Yeah. Which, again, when you talk about sustainability, and being well maintained, a lot of people said similar things. And that’s something I’m gonna come back to in the third round, of: What were people’s definitions of sustainability and well maintained stuff? Pretty much everybody talked about: Being well maintained needed people to contribute. Because of that volunteer emphasis.

NAOMI: Mm-hm.

MEL: Any other immediate thoughts, comments, on Donald’s bits here? And why the Warehouse rewrite happened?

NAOMI: Um… It’s not surprising, I suppose, in a way. It kind of fits one of the classic narratives around Open Source projects, where you’re so bothered by a problem that you feel compelled to fix it, and then contribute that fix back.

MEL: Yeah. Okay. And this will build as well. So the second person that we had from upstream was Ernest, who is one of the very few full-time PSF employees. And focuses on infrastructure. And so this is what he said about why… What problems with the Warehouse rewrite they were trying to solve.

> _Source(s): Ernest-1_
>
> ERNEST: PyPI is, as a service, something like 17 years old. And the Warehouse is the second, you know, sort of imagination of the project. The project started, you know, well in the history of Python -- like, as a web language. And when it was originally written, there weren’t any of the fancy modern day web frameworks.
> 
> Testing was known and something people definitely did, but wasn’t necessarily as highly valued for, you know, what was effectively a pet project at the time. It was… Hey, can we do this? And then they went for it, right? You know, over time, PyPI grew sort of… Exponentially.
> 
> ...And so somewhere around 2012 or 2013, PyPI was starting to really show its age as a service. There were a lot of regular outages. There were sort of… It was common, I guess, for changes to go out that broke things unexpectedly. There were, like, two working tests for the service... It had features like an oauth consumer and an oauth provider that were in very, very low use. But caused a lot of headaches. It had features like SSH for uploads to bypass the fact that, you know, it didn’t have TLS for a really long time.
> 
> And so over time, also it didn’t really have any in-depth monitoring. Sort of the best monitoring that it had was: Is PyPI working or not? Like, can I get to it? And so over time…
> 
> MEL: Literally can you go to the web page and see it?
> 
> ERNEST: Yeah, effectively... basically just uptime monitoring. Is the service responding?
> 
> ...there wasn’t a good open door that any developer could sort of walk in and do anything with PyPI. It was very difficult to run locally, to sort of make changes and play around. Again, since there weren’t tests, it was really hard to verify that you hadn’t completely screwed up some other feature that you didn’t realize...

MEL: There you go.

NAOMI: Right.

MEL: So any thoughts or responses to this? Is anything here new or surprising?

NAOMI: No, I don’t think so. I would say this reflects the same thing that Donald was describing, but perhaps from a slightly different perspective, given that he’s now somebody in charge of keeping the infrastructure up. It reads to me as somebody who has those concerns, much more. So yeah, I would say it makes sense.

MEL: Okay. And then the third person… Is Nick Coghlan. Who is one of the Python core developers. And also involved in getting the Mozilla grant that was part of how Warehouse was funded. There’s two parts to this. This is the first one.

> _Source(s): Nick-1_
>
> NICK: Anyway, one of the things that came alongside those membership changes was the working group structure... And so, we formed the packaging working group. I'd have to look up myself exactly who the founding members were, but it was essentially so that the PSF could accept money that we would then spend to complete packaging projects,
> 
> And the specific project we had in mind when we started was finally getting the legacy PyPI replaced by the new one because Donald had got the new one to the point where it was there and you could opt-in to using it, if you wanted to. A lot of folks opted into using it for uploads because they were much more reliable uploads. So essentially, you could use either one. They went to the same database. They showed you all the same files. Everything was fine.
> 
> The issue was there was an unclear amount of additional work before the old one could actually be switched off because there were a few things that the new one didn't do yet. Mostly related to the web interface. There was still some tasks where you would have to go back to legacy PyPI if you wanted to do things. It was just the main package upload and package install flows that the new service had implemented.
 

NAOMI: Okay.

MEL: And so one of the differences here is that Nick is talking to us about… Not that Donald or Ernest were talking about the super technical side of things. I personally think it’s really interesting that both of them start off talking about “no one can contribute to this”. But Nick was almost taking a step back and going: Organizationally… The PSF… And so this is… A little bit not directly at your question, but…

> _Source(s): Nick-1_
>
> NICK: There was one [bid for a Python grant] where essentially the quality of the prework that had gone in was spectacular, but the operational proposal for actually getting the job done we didn't think would fit in with the PSF's nature as an all-volunteer organization. It was clearly structured around working with a full-time project manager on the client side, and so, what actually happened was the pre-work from that, the PSF paid [to] outright transfer the IP for that to the PSF.
> 
> Then there was another -- the winning bid was one where the pre-work wasn't as strong but the operational proposal was a lot better. Or a lot more suited to the nature of the PSF as a client. And so -- then out of that hybrid is essentially the Python.org that we have today.
>
> However, that was a project where the management on the PSF side was completely volunteer run. And so, when we're reviewing the bids, one of our comments was [that] the weak link here is not the contractor. It's management on the PSF side because this is a big project. It's a complicated project. Trying to do it with all-volunteer management is going to be tough.
> 
> Now, one of the mitigating factors was the winning bidder had a very well-known profile community member working for them. Okay. They should be able to step in and make up the difference if the PSF project management isn't up to the task. They got a really, really good job offer in San Francisco and took it, so they weren't involved anymore because they'd gone to a new job.
> 
> The project lead on the PSF side had life happen. It was a case of -- so essentially, that project stalled for a long time. Eventually, some folks were able to step in and say let's actually get this done. Let's get this deployed. It did become the Python.org web presence, but it was not a smooth journey.
> 
I think that was one of the factors that led to when the Mozilla grant for PyPI was sent, the grant said “we will pay a professional project manager to actually be part of this process and actually be the PSF's ongoing management”.

NAOMI: Okay.

MEL: So I think some of the context around this is -- Nick was talking a lot about how the sort of large infrastructure change that was needed to get the PyPI Warehouse negotiation going was something that PSF and Python community also needed to grow into. Organizationally and structurally.

NAOMI: Yes.

MEL: So the context of that is: Oh, jeez. This technical work requires multiple humans working on it and getting paid. Okay. Shoot. How do we get the money to pay them? How do we set up the infrastructure to pay them? Do we have the capacity to handle the money to pay them and so that story of organizations, how did Python grow into being able to do that.

NAOMI: Right.

MEL: And again, is there anything… Surprising here? From your vantage point, that’s like -- oh yeah. Of course. Knew this.

NAOMI: Um… Having been on the PSF board for probably the last, say, two thirds of that history, I wasn’t there at the very beginning, but… I’m not surprised. I think it captures very well the sort of dilemma that we as the PSF faced, as we basically came to terms that the old ways that the PSF had had of managing things were not up to a lot of the challenges that the PSF was coming to face. 

So… This is a classic example, and I think it’s actually one of our signs, I hope, of emerging wisdom, that we were smart enough to adapt to -- come around to the decision that we needed to pay for project management, as something we considered before paying for developers. Since most of us are developers, thinking that way was not a natural thing to do, I don’t think. But in fact, there’s more leverage in paying for the project manager than in paying for a developer. Ideally we would like to be able to do more of both. But I think that was kind of a key thing.

MEL: Can you expand on that a little bit? Why do you say there’s more leverage in paying for the project manager?

NAOMI: Well, because… I mean, coming back to the whole fact of making it easy for people to contribute, you know, it’s my impression if you talk to people maintaining projects, particularly where there’s a lot of activity, they tend to get bogged down… What should I say? They will say that code reviews are their problem, but when you actually talk about a lot of what they do, it sounds like… Yes. Code reviews take up time. But the real burden is the same burden that any leader of a software team kind of faces. Any project manager faces. And that is: Finding the right things for people to do when they are available to do them. That’s not really a development task. That’s a management task.

MEL: Huh. And it’s… Is that the kind of thing that is harder to get unpaid, at that level that you need?

NAOMI: I think it is. Because I think most of the people that we normally attract to volunteering don’t come in asking: How can I help manage a project? They come in saying: How can I get my patch accepted?

MEL: And I wonder… When we were talking about attracting contributors to the project, we talked about diversity of different types of people. And I don’t know if we specifically talked about diversity of type of contribution people want to make, but there’s been that discussion in the Open Source world for a while, about… Do we overvalue “technical”, quote-unquote, contributions, over…

NAOMI: Right. Yeah. I don’t know. I don’t think we really discussed that. I mean, certainly it’s been common to say… Oh, we would love to have you come in and write documentation, if you’re not technical. But I cannot recall any project saying: Hey, we really have a lot of tasks to juggle. Anybody with a project management background or skills -- we would love to have you come in and tell us what to do. I just… I can’t remember ever seeing that.

MEL: Yeah. That does sound like an unusual… Also, I’m also going… Yeah. I can’t remember this either. I’ve seen calls for it. We need artists! We need testers! But that’s technical-ish also. Or technical (inaudible) at least. Huh. So I’m going to put in what Nick and Donald Ernest thought about: So how did this all work? What did they consider the successes? Or the closest thing they had to those answers. And then spend the rest of the time asking… Let’s see… I’ve got Ernest here.

> _Source(s): Ernest-1_
> 
> ERNEST: I think that overall the service has been far more reliable. To the community. As a result of this.
> 
> And then, you know, I think generally it was sort of a morale boost, I think, for both the people working on the service and for the community as a whole. You know, there was a lot of excitement around the new PyPI, et cetera... we even tried to juice that [morale boosting] a little bit. During the last few months of the Moz Grant and a little bit after, you know, we had stickers printed up that -- I think I mailed stickers to, like, 10 or 15 different countries. For new contributors to PyPI. Or first time contributors. So it was. I mean, it was really impactful. I agree. I think you do a good job, again, of putting a fine point on how important it was that people were excited, and not just excited. Capable.
> 
> Because I think there was always a lot of excitement at the opportunity to contribute to PyPI. But it wasn’t necessarily something you could just do. Right? You couldn’t take your skills and apply them immediately. There was a lot of… There were barriers that didn’t need to exist and shouldn’t have existed to that. And so the combination of that -- yeah. I mean, it built on new excitement and it enabled a lot of existing excitement, if that makes sense.
> 
And in a way, it also has a snowball effect. Where the more maintainers you add and the more maintainable the project is, the more maintainable it becomes, because more people are attracted to it. They come in and they sort of share their pain points or the problems they had, and then if you address those, then you improve the maintainability. If you don’t, it stays the same. But you won’t necessarily attract maintainers from that perspective. 

NAOMI: Okay.

MEL: Any thoughts or responses to that bit? Or I can also just put Donald’s and Nick’s and you can talk about them all together.

NAOMI: Yeah, let’s do that.

MEL: Okay.

> _Source(s): Nick-1, Donald-1_
>
> NICK: So, one of the biggest things was on the sustainability front, the PSF taking straight up responsibility for this as a service that the PSF provides and will make sure is functional. That's kind of the sustainability backing there, coming from the PSF.
> 
> A lot of the actual work is still very volunteer driven, and so, there's -- it's not like the PSF is in a position to say we have this person working full time on making PyPI better. It is still grant driven, but at the same time, we have partial contributions from folks' employers to say this person has a certain amount of time to work on PyPI community stuff. At the moment, there's a reasonable amount of that going on, so there's still possible improvements to be made, but it is in a lot better place than a lot of projects and services.
> 
> DONALD: Right. And one of the things that I… That has made me the happiest about the state of PyPI today is that there are major features added to PyPI that I know nothing about. I’ve touched them zero amount. I don’t know anything about them. There are parts of the codebase that I don’t know… That I don’t have in my head, because I’ve never looked at them. And, you know, that sounds weird. But the fact that other people are able to get in there and work on it and become experts on their own part of the codebase, and are able to implement these features without my fingers having to be in all those pies… Makes me feel like -- on the sustainable side of things -- that the sustainability goals of Warehouse were a success.

MEL: Actually, I’ve got a little bit from Ernest here that was from right before what he just said. So I’m gonna put that in.

> _Source(s): Ernest-1_
> 
> MEL: Would it cost less to run the new version of PyPI than the five years ago version?
> 
> ERNEST: It was kind of a wash, truthfully. The new implementation is… Well, the new implementation runs as a composition of a handful of services. Not just one little service running. Right?
> 
> ...And so that increases the complexity a little bit, which increases -- there’s basically an overhead cost to running multiple services, versus one. And so I think it’s about equivalent. Even though the new service is a little bit more efficient. We also are running a handful more services in combination. So I think it’s, again… I would probably estimate it to be about equivalent.
> 
> MEL: Yeah. And it’s also hard to compare, because over time, the demand on PyPI would increase, and more people are using it, so…
> 
> ERNEST: Indeed.
> 
> MEL: So from an infrastructure perspective, and a sustainability perspective, what did the move to Warehouse get you? So you mentioned already ease of contribution and people being able to work on it, even Donald. What else did that get you?
> 
> ERNEST: I mean, a lot of safety. Right? When tests fail, we know to look for something that might…
> 
> MEL: Mmm.
> 
> ERNEST: Something else might have broken. So I think that overall the service has been far more reliable. To the community. As a result of this.

NAOMI: Okay. Makes sense.

MEL: So going back to the questions you asked in the last interview, about what were specific issues they were having… None of the core developers, I think, surprisingly, talked about that as much, in that sense. Donald got closest when he was talking about things being unreliable and dropping out. But pretty much no one was like… Ah, yes. We were having outages once a week. That was the issue. And so I thought that was really interesting. And most folks… Again, we got three. So “most” is… But they were talking about the second bit you asked me about, which is: How do you think about attracting new contributors to this? 

So I thought… Oh, that’s fascinating. It’s a technical improvement. That’s in some ways focused on a human onboarding problem.

NAOMI: Yeah. I think that’s probably true. I mean, I think there were hints in what… Certainly what Ernest said, somewhat. Maybe less in Nick said about reliability and testability. But I guess I would agree. Their focus in raising those things was more on how that made it difficult for people to get started contributing than the inconvenience, maybe, to the community. Even though they all acknowledged that, I think. But yeah. That, I think, is… Is a little bit surprising. But again, that may also kind of reflect a volunteer, Open Source-type organization, where there isn’t, again, a hierarchy demanding cost estimates and justifications, return on investment, any of those things.

MEL: So… I’m gonna put on my… Unpack for people who might not be as familiar with Open Source hat. Oh, no, that actually is super surprising. Why is it not surprising to you? What about the Open Source volunteer culture makes it like… Oh! Well, yes, of course, we would focus on this.

NAOMI: Well, I think… I guess I would say… That it may not have always been the focus, but you can tell for all of them, they’re very interested in getting new people involved, which is one of the keys to a sustainable Open Source project. 

When I first started being involved in Open Source projects, which is now embarrassingly close to 20 years ago, or at least 15 years ago, there hadn’t been enough of them lasting long enough for us to really be aware that was a problem. Somehow, when people started a project and it was successful, there was an assumption it would just go on forever. Nobody thought about it. 

Now we have seen various projects come, go. Somethings are vital, but sort of end up going dormant, and that being an issue. And the various struggles. So I think that’s probably much more top of mind. 

But I also think in Open Source culture, generally, and I would say probably even more so in Python, a strict return on investment, strict performance, those sorts of metrics, have not always been the things driving things. You know, even to go back to: Why do we have Linux? Well, according to the creator himself, problematic though he may be, it was just for fun! It wasn’t to solve a grand problem. Same thing with Python itself. There was no intimation that it was going to be more performant, more this, more that. It was an interesting idea that was fun. So that’s kind of at the heart of the Open Source ethos. I would say. So I think that kind of gets at it.

MEL: Yeah. And I think that also ties into… When Ernest was talking about -- what did we do after? We sent stickers to people! Like… Okay.

NAOMI: And I know from experience in Open Source communities… Stickers are a big deal. So wherever I go in the world, even the sort of most seasoned, hardened, gruff old guys want a sticker.

MEL: And so I’m thinking that… What kinds of implications does this have for Open Source projects? And also foundations or industry partners and corporate sponsors that want to make things like Python more sustainable? I mean, give us stickers. It will make us happy.

NAOMI: Yes. Well… It kind of, I think, gets at a little bit of… I don’t know exactly. Paradox. A dilemma, at least, in Open Source communities. Which is, as we’ve kind of mentioned, technical skills tend to be highly valued. And yet the thing that actually drives these projects and makes these things work really comes down to much more sort of emotional and soft skill and human skill-type things. So…

MEL: And do you think that’s because the technical literacy, maybe, is one way to phrase it… Is already a given for enough people? It’s like… Well, of course we all have technical skills or fluency of some kind. I’m trying to figure out how that fits in there.

NAOMI: I’m not sure. I think part of it is that demonstrating technical skills is a… Is an easy to understand way to compete. And not wanting to go too far down this path, but at least kind of nod in this direction, I think that particularly historically we have had a lot of kind of male-driven competition behind some of those things. And I think… My feeling is, if you go back and read things about Open Source, as it was emerging, I can recall all sorts of things where this was kind of even not so terribly veiled as people talk about it. You know, being able to make the most patches is a way to prove you’re the best guy. And so I think that may be behind that. But as I say, it’s kind of a paradox that in fact… That is not one of the things that tends to make projects sustainable.

MEL: That’s fascinating. And hopping back to something you said a little while ago, about… You know, 15, 20 years ago, people were not thinking about this quite as much. Sustainability. Because Open Source hadn’t been around that long. Were there conversations where people were going… No, we need to think about sustainability. Down the road -- I’ve been in software for X years, and we need to be seeing this in the future? Do you recall any of that?

NAOMI: I don’t. I don’t recall that, in terms of reading things that were being written and talking to people. I think there was a certain feeling of… I don’t know. Exceptionalism, something like that. We’ve invented a completely new paradigm, new way of doing things, and the old rules don’t apply. You know, the rules of business don’t apply. Things like that. One of the first couple of conferences I went to, 2001-2002, Linux World… I know 2002, it was held in the Moscone Center. It wasn’t a tiny conference. But people were starting to complain that the presence of business in suits was ruining the Open Source vibe even then. So… Yeah.

MEL: And yeah. So I got involved, I would say, 2006-2007. And the paradigm shift framing is something I also recall very strongly. In thinking about sustainability of Open Source projects, as Open Source has become more popular, more widely used, more major projects, the way that we think about sustainability within Open Source software projects, and infrastructure projects specifically… And the way that people outside of Open Source think about the sustainability of digital infrastructure… Do you feel like the difference between the two has changed over time? 

And that was not a very clearly phrased question. But the difference between… How do we think about digital infrastructure sustainability inside the Open Source community and outside the Open Source community? Do you see… First of all, do you see a difference in the way those things are discussed right now? And whether there is or isn’t a difference, has that difference between the two spaces changed? In the history that you’ve experienced?

NAOMI: Well… So I think… I think it gets at what you’re saying. It’s just… There has been a slow and gradual shift, and it’s probably lagged behind reality. To understand on both sides in the… Let’s say for shorthand, for non-Open Source, let’s say business or commercial world. And the Open Source world. 

So the business world is slowly waking up to the fact that almost while they weren’t watching, they started using a large, large, large amount of Open Source software. And I know this, because I had to explain in 2011, I had to spend a lot of time explaining to corporate lawyers what Open Source even was. And I had to fill out documents saying where we got support, how we got the license, and all sorts of things like that. 

And these are now companies… You know, the company I’m thinking of now uses lots of Open Source. But even at that point, they were starting to use it. They just weren’t aware of it, at a corporate level. As the technical people made the best decisions, they thought, they were using more and more of that. Now they are starting to be aware of this. And consequently, they’re starting to wonder about questions of: How do we make sure these resources we’re using stay available? And how do we exert some control over them? 

And I think the flip side is kind of true in Open Source communities. We were all slyly happy that this was going on. We thought we were pulling off a great trick. But in fact… As it grows and becomes more popular, it then becomes something different than what it was 15 years ago. And I think we’re also slowly becoming aware that we cannot completely ignore and pretend that we’re not connected to all of those many businesses, commercial enterprises, et cetera, that are using Open Source. Sometimes in ways that… Many of us aren’t totally happy with. So… I think that’s getting at your question, in a way. Both sides are struggling with: How do we actually come to a model where these projects that have become vital can be maintained? And on the other side, how do we as a project that’s Open Source come to terms with a way that we can accept those resources and be happy?

MEL: Yeah. And then what does that mean for us, not just technically, but as Nick was talking about, organizationally. Structurally.

NAOMI: Right.

MEL: And what does it mean for a culture who talked about… A lot of that paradigm shift rhetoric was like… Anarchy. Maybe not using that word, but… No hierarchy. You do things. So in terms of thinking about, again, the sustainability of these Open Source digital infrastructure projects, these non-Open Source entities, corporations, et cetera, are going -- oh, shoot. We’re using this. We’d like to help it keep going. What can we offer?

NAOMI: Right.

MEL: What would be most helpful?

NAOMI: But… But I think, to interrupt on that, that that’s only part of what they’re asking themselves. Of course, they’re not doing it from a purely altruistic sense. So it’s also: How can we control this? How can we be sure that we’re ensuring what we need?

MEL: Uh-huh. So from the Open Source community perspective, thinking about your experiences, thinking about what the PyPI developers have talked about, why they did this and what happened… What kinds of things would you say or have you said to the corporations, saying… We use Python. We’d like you to be around. What can we do?

NAOMI: (laughing) Um… So there are… From what I’ve seen, there are a couple of different things that we can do. One of them is that you can approach corporations and have this almost be an exchange on, say, the engineering level, or coming from the engineering budget. You know. We are providing, say, PyPI. And we could say… Okay. Large corporation. You want extra services. Extra something. Special abilities. Whatever it is they might want. If you’re willing to give us X amount of dollars, in exchange, we can do that. We can make that kind of arrangement, almost as a sale of services. 

And we have not done that at this point with PyPI. We’ve talked about it a lot. I think… Like, Read the Docs kind of works on that model in some cases. And there are, for a non-profit entity like the PSF, there are issues with that, in that -- that no longer becomes non-taxable income. That becomes taxable income that the organization then has to handle differently.

And so that is a challenge, maybe, that the PSF isn’t up to. The other approach you can take, of course, is to say: We do this variety of things. And we’re not gonna give you anything particularly, other than our public thanks. But you can give us money to keep on doing these things, which is what we have done. And actually have gotten a certain amount of support for. And maybe it is earmarked. Some donations we’ve gotten, it’s earmarked for supporting PyPI. Okay. We can do that. And I guess… Actually, there is a third category as well, which is getting services in kind. So a lot of the infrastructure that, say, PyPI runs on is donated. And if, in fact, we were to lose these donations, this would put the PSF and the Python community in a considerable quandary. Because we’re talking about a large amount of money now that would be taken to pay for those things sort of regularly available. So I’m not sure I answered your question, honestly. But those are the things kind of floating around, in terms of what we might do.

MEL: Yeah, no. That was a great answer to the question. And Ernest also mentioned the hundreds of thousands -- millions of dollars -- of donated infrastructure for PyPI alone, between Amazon and Fastly. And how much it would cost to do the CDN if it wasn’t donated.

NAOMI: Right.

MEL: And one of the things I was asking him, also, I wanted to run by you, in terms of… How robust is that? How much lead time… So let’s say… I don’t think Amazon is gonna go away any time soon. But if suddenly you have to deal with all the infrastructure… How big of an issue is that? Do you feel like… Oh, no, we’ll always have enough lead time. There’s always gonna be a way to handle that. How tenuous does that feel?

NAOMI: Um… I think in general it’s a reasonably safe assumption that there will be a fair amount of lead time. We’ve had in-kind sponsorship things go away like that in the past, and we have usually had several months to resolve that. And I would say probably from a technical standpoint that’s not so much at the issue as it is just the negotiating and finding other sponsors and being able to have a way forward that is more of the issue. But I don’t know that any company really would like to be known as the ones who pulled the plug on PyPI. So I don’t think that is a huge risk.

MEL: And then also going back to what we were discussing earlier… Paying project management versus paying developers. I’m curious about the kind of implications that sort of statement has for people saying: How do we support this stuff? How do we make this stuff more sustainable?

NAOMI: Well, I think if it is framed the right way, and I think that sort of framing will become easier, as we start having more successes on this… It does two things. First of all, it provides an obvious destination for donor support. Probably one that they understand. So if we’re to go to a large company and say: We have a project, and we have found that in order to make this project work, we need to give it proper project management support… I think most entities will understand that, based on their own experience. 

I think it also, in addition to making it perhaps a better experience for volunteers, it may also make it more palatable for organizations who have hired someone that they, as we mentioned before, are going to release to work on a Python project or a community project for a particular amount each week. It may actually give them assurance, then, that that time will actually be reasonably well spent. It’s like… Yes, we actually do pay for management on this. So if you’re going to contribute your developer resources, we have some assurance that we’re going to be using them for what we say we are.

MEL: So we have a lot of examples of companies releasing worker time specifically to contribute. That’s Donald Stufft. He was describing it. Right now, his employer gives him X% of the week to work on Python things. And a lot of people have that. If a company wanted to -- instead of donating a developer or part of a developer -- if they wanted to donate a project manager instead, what kind of… Because that gets into, also, the corporate control bit of it.

NAOMI: Right. Right, right. I’m… I think that such an arrangement would be possible. It’s not something that we have seriously contemplated, as to the parameters, the controls, the terms of such a release. Might be a little bit more slippery to work out, than in terms of a developer. But I also think it’s something that… My sense is it’s something that would be considered seriously, if that were ever to come about.

MEL: What makes it more slippery to look at? What’s the difference between development and project management that makes it more challenging?

NAOMI: I think it is… I guess to my mind… It would be… There are a couple of things. One of them is… The implicit ability to shape directions of projects that I think we might want to be a little bit careful about. Whoever is doing the project management can control the evolution, the development, of a project, in lots of subtle ways, as well as very overt ways. So I think that might be part of it. 

I think from my experience working with and sharing project managers across teams, the other one would be whether or not you’re really going to have this person for X amount of time or not. I’ve certainly had that experience where… Yes, yes, yes. You can have a share of the project manager for your project for 15 hours a week. And in fact… Other things come up. More important projects take precedence, whatever. And you end up getting -- the person maybe rushed and in a hurry for 2 hours a week. So that, I think, might be the other thing that I would, just from my experience, I would wonder about.

MEL: And I’m thinking about the way that -- people who have done project management professionally in Open Source communities… How that has been set up. And I can remember some -- like, PyPI hired Sumana.

NAOMI: Right.

MEL: And places like Mozilla, Red Hat, who have their own in-house…

NAOMI: Right.

MEL: I’m also looking at the time. There’s a lot to think about here. Any other thoughts or closing comments from any of this?

NAOMI: Um… No. I can’t think of any.

MEL: Okay. So same process is gonna happen. I’ll send you a transcript to look over and open license, like before. And in the third round, we’re gonna bring back everybody’s definitions of sustainability, both upstream and users of PyPI like yourself, and then also some of the other things that the other users of PyPI said about it in the first round. So that’s the game plan for the third round. And Heather will probably email you about scheduling for next month, once everyone gets through their piece.

NAOMI: Sounds good.

MEL: Thank you again so much for doing this.

NAOMI: My pleasure.

MEL: Okay! Have a lovely weekend.

NAOMI: Okay. You too!

MEL: Will do.
