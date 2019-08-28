# Copyright transfer statement

MEL CHUA hereby irrevocably transfers and assigns to NICK COGHLAN in perpetuity, all right (whether now known or hereinafter invented), title, and interest, throughout the world, including any copyrights and renewals or extensions thereto, in the attached transcript of the interview recorded between us on JULY 31, 2019 in A LIVE-TRANSCRIBED ONLINE VIDEO CHAT.

# License

I, Nick Coghlan hereby release this work under the following open license: http://creativecommons.org/licenses/by/3.0. Anyone is free to share and remix the work as long as they cite it. I consent to the open publication of this work using my name.  

# BEGIN TRANSCRIPT

MEL: I need to have some sort of clean line -- it is okay for the official transcript to start here, and then everything before that we'll delete. Ready to start official transcript time? 

NICK: Yeah, absolutely. 

MEL: Sweet. To start out, I'm asking everyone this. How would you like to be identified in the project? What name do you like to go by? 

NICK: Oh, Nick Coghlan. 

MEL: Got that. And how would you describe your involvement with the PyPI thing and what would you call that? 

NICK: When I originally got involved in PyPI, I thought of it as my “keep Daniel [Holth], and Donald [Stufft] from burning out” project because Daniel had done some excellent work around the wheel packaging format, and Donald had essentially written a proof of concept of what PyPI could be. 

Both of them had a common problem. There wasn't anybody that could actually say yes to what they wanted to do, and so, they were just getting lost in the weeds of details and both just clearly heading towards burning out completely and giving up. 

And so, back in 2013, I think it was, at the language summit that year, I basically pitched the idea of a couple of standing BDFL delegations to Richard Jones for Python packaging index-related stuff and to me for Python packaging interoperability-related stuff, so it fit the format at the time. Guido [van Rossum] was amenable to that idea. We organized a packaging mini-summit at the following PyCon, and I gave a few talks, attended some conferences about it and what we were doing. 

This actually then built on top of previous work, which is actually written up in the [book titled] The Architecture of Open Source Applications - (NOTE FROM NICK: Tarek's chapter is here: https://aosabook.org/en/packaging.html.) the details for the project and essentially the kind of genesis - the precursor to this round of updates -

NICK: I think it was Éric Araujogoing, “this stuff is not ready to ship. Take it out of Python 3.3.” That was kind of what drew the line in the sand of the previous attempt to improve things. I said, “This hasn't worked. Let's stop and reconsider where we're doing.” Then that was where this latest effort really got started was after that. And basically going, okay, what didn't work last time, what have we learned, what are we going to do differently this time. We did a bunch of things differently, and we got a different outcome. (Laughter). 

MEL: The latest effort getting started, about when would you say that was? About what year? What time? 

NICK: Pretty much when Daniel and Donald got involved, which would have been just before that 2013 language summit. I don't remember exactly when it was, but if you look at the dates onPEPs 425, 426, and 427, the original dates on those was around where it all started to happen. 

Again, there were like the two most obvious user-facing outcomes of that, which is we eventually got the wheel format standardized and wheels became a routine thing for people to publish, which meant it was far less likely that end users would need a compiler on the computer, which was an especially high barrier to entry on Windows. 

The other big thing was what eventually became PyPI.org. It's one thing to write the proof of concept of “this is what PyPI could be” and something else entirely to write an [actual replacement service].

After that, after that initial organization work, I was reasonably hands-off. It was just the case of I got myself into the position where these folks, who had good ideas but didn't have a way to get them accepted and say, “yes, this is what we're going to do,” that was what Richard and I -- “Okay, so we can say yes now.” 

On the wheel side, we were able to say, yes, that's gone in. PyPI was able to accept uploads of Microsoft Windows and Mac OS X wheels -- the Linux wheel took a lot longer, and that was mostly Nathaniel Smith (NOTE FROM NICK: Robert McGibbon co-drafted the original manylinux specification with Nathaniel). He was certainly a major player. People were able to actually make changes and see benefits. Once you start getting benefits, it is easier for people to get going as opposed to spinning their wheels. No pun intended. 

MEL: How would you describe your position in the Python community? Why were you able to step in and make these connections and help things happen? 

NICK: By that point, I'd been a Python core developer for like eight or ten years and had -- 
probably eight. And so, the key thing was that the core developers trusted me. Guido [van Rossum] was willing to say, okay, you can take care of this. (Correcting captioner spelling error for “Guido”)

But then I was also able to listen to the different groups and reflect back what they were saying and say, actually, you all want different things. One of the ways I would describe it, I was able to convince people if they wanted to be mad at somebody, be mad at me, not at each other, which made it much easier for them to collaborate. 

MEL: (laughs) That works. 

NICK: But yeah, a big part of it was just being able to say yes to things and make it stick.
That was having the right context, I think. Core development. I forget the exact timeline, but Marcus Smith had the Python packaging user guide. Said, “wouldn't it be cool if this was a Python.org thing?” That's where the packaging user guide is now. 

Yes, just generally lots of little administrative things to just say, “no, no, no, the Python Packaging Authority is a real thing. It actually does get to define what the default practices are.”

MEL: Cool. So, stepping back a little bit before we advance into the saga of the recent big PyPI project, what does it mean to you for an open-source project to be well maintained and sustainable? If those are two separate things, that's cool. If you lump them together, that's also cool, but what is the definition and indicators for you to say this project is well maintained and this project is sustainable? 

NICK: I think they are two separate things. 

Well maintained is basically you have release notes. You have pre-release testing, where you have automated testingYou actually care about backwards compatibility, you don't just change stuff because you feel like it. You have a reason. 

There's no requirement for the project to be well maintained. Sometimes projects are just people's fun side project that they can do whatever they want with. All you can reasonably ask from in that case is - 

(audio issues)
(resolving audio issues)

MEL: Okay, cool. Sorry, Nick. You were talking about sometimes things are just people's fun side projects. 

NICK: If it is someone's fun side project, all you can reasonably ask is that they clearly label it as such. There's a thing called “unmaintained.tech”, saying like, look, don't use this for anything serious. If you do, that's on you, not on me. Make a copy of it. 

Whereas, sustainable, it's the case of doing things in your spare time is all well and good.
Life happens. Job changes happen. One of my favorite comments about bus factor in open source is the bus doesn't have to hit anyone. It can just pick them up and take them to a new job. 

So anyways, the issue there is if a project is basically maintained by one person and that person isn't specifically employed by anyone to say, hey, make sure this thing keeps existing, make sure it keeps up to date with the changing environment around it, then you've got a sustainability problem. 

There are lots of projects, in fact, that [have sustainability] problems. Even the core reference interpreter itself. It's in a much better place than a lot of other projects, but relative to the degree with which it is used, the level of investment is disturbingly low. 

For a long time, PyPI, it started life as something Richard Jones put together as a proof of concept for what a Python packaging index could be. Then that became the real production implementation of PyPI and was the implementation for more than ten years. (Laughter). 

Yeah, that's just the reality of -- people will be able to tell you lots of stories of that happening inside of companies. Not just in open source. 

MEL: Was there ever a moment where it was, okay, now this is officially production? Was there ever like a blessing or process by which people went, oh, geez, this can't just be someone's side project? 

NICK: That was kind of before my time. Yeah, you need to talk to some of the folks that know more about the history of PSF infrastructure, so like Thomas [Wouters] and those folks. Yeah, or Richard himself for that matter, but no. 

I think it was a case of they ran up the proof of concept. The PSF put it on a server and said, here's this thing. Then people started putting more and more projects on it. Then it was like, oh, well, people are actually using this thing for real. (Laughter) I guess we better keep it working. Yeah. Because the very, very visible thing was the final cut-over to the new app. 

After Donald got involved, he drove a lot of improvements to PyPI. The biggest one being the production of the CDN because that -- basically, because the original PyPI was a relatively -- essentially, it predated a lot of the modern Python framework, so the way it was written is not the way you would put together a web app today. You would get a bunch of PyPI failure found within the PyPI application itself rather than anything in the infrastructure. 

When Fastly got involved, what that actually provided was -- they just put their content distribution network in front of PyPI. 

And the thing is, because of the nature of our package index, it caches really well. Because once old releases go up, they don't change. And so, you put all those into the cache. 

The numbers I remember when the CDN went in: traffic to the main PyPI app dropped by 95%. The vast majority of hits started getting served out of the cache. It also meant if the app did go down, all that stuff that was in the cache could still be served. The app could fall over, and people's installs still worked most of the time. They couldn't publish new releases. That absolutely had to go to the primary application. 

Yeah, that was kind of one of those things where there was some work in the application to actually properly integrate the CDN, which Donald did in his spare time, but it was a case of just the donation of that service was probably one of the single biggest reliability improvements in the history of the package index. That's still there. It's still in front of the new PyPI, and it is still keeping most of the traffic from hitting the backend. 

Eventually, that got recognized as an in-kind sponsorship. Properly recognized as one of the PSF's biggest sponsors because the bandwidth bill for the package index is not small. (Laughter)

MEL: Can you give me the back story on how that got recognized by the PSF? 

NICK: Oh. Actually, that fits into the story as well because the whole other side of what brought us to the Mozilla grant in finally making the warehouse migration is the PSF side of the story. 

I do not remember the timing of this at all. I think it was around the same time as the packaging -- as I was getting involved in the packaging stuff. 

There was a project to do a refresh of the Python.org web presence. That is the web app that is still running today. The PSF put out a request for proposals, and there was a few of us on essentially the volunteer review team reviewing the proposals. And there were a couple of very, very strong proposals that came in. 

There was one where essentially the quality of the prework that had gone in was spectacular, but the operational proposal for actually getting the job done we didn't think would fit in with the PSF's nature as an all-volunteer organization. It was clearly structured around working with a full-time project manager on the client side, and so, what actually happened was the pre-work from that, the PSF paid [to] outright transfer the IP for that to the PSF. 

Then there was another -- the winning bid was one where the pre-work wasn't as strong but the operational proposal was a lot better. Or a lot more suited to the nature of the PSF as a client. And so -- then out of that hybrid is essentially the Python.org that we have today.

However, that was a project where the management on the PSF side was completely volunteer run. And so, when we're reviewing the bids, one of our comments was [that] the weak link here is not the contractor. It's management on the PSF side because this is a big project. It's a complicated project. Trying to do it with all-volunteer management is going to be tough. 

Now, one of the mitigating factors was the winning bidder had a very well-known profile community member working for them. Okay. They should be able to step in and make up the difference if the PSF project management isn't up to the task. They got a really, really good job offer in San Francisco and took it, so they weren't involved anymore because they'd gone to a new job. 

The project lead on the PSF side had life happen. It was a case of -- so essentially, that project stalled for a long time. Eventually, some folks were able to step in and say let's actually get this done. Let's get this deployed. It did become the Python.org web presence, but it was not a smooth journey. 

I think that was one of the factors that led to when the Mozilla grant for PyPI was sent, the grant said “we will pay a professional project manager to actually be part of this process and actually be the PSF's ongoing management”.

The other thing that happened on the PSF side between when that Python.org bid happened and when the Mozilla grant happened was just general professionalization of the PSF in general. 

Yeah, it was basically when Ewa [Jodlowska] first joined the PSF as secretary. I think that was either the only paid position -- actually, I think she joined as events coordinator and served as secretary of the board. Anyway, it was something along those lines. I think Kurt [Kaiser] may have been paid part time as treasurer, but it was certainly - yeah, there just wasn't a lot of full-time permanent structure there, and so, a lot of things were very, very dependent on board members volunteering time. And that is just a tricky thing if you want to deal effectively with contractors. 

Anyway, from that point, again around the 2013-2014 mark, I was on the board from -- which years was I on there? Definitely 2015, 2016. I think I joined the board in 2014. I was there for two years, finishing up in 2016. 

Anyway, during that time, Ewa was promoted to director of operations. We hired an infrastructure manager. And then since then, Ewa has become executive director. There's now an events manager, financial controller, infrastructure manager. There's just a much stronger professional core inside the PSF to help with project management and so on and so forth. 

That brings us to the point where these two streams come together, which is the formation of the packaging working group. 

I actually forget how that discussion started because one of those things is it can actually be -- it's one thing saying money will help. Because if people start giving you money, you have to figure out how to spend it effectively. The problem with the PSF is the PSF could potentially collect money, but how would they know how to spend it? 

And on the Python packaging authority side, while that sounds like a very cohesive name, it's not a cohesive group. The design delegations are actually to specific people. Currently, Paul Moore and Donald Stufft for the packaging index. It just so happens that those people consider themselves part of this collective called the Python packaging authority. 

That means that even if people want to give money to Python packaging, how do you decide what's a good use of that money? 

Alongside all of this, in 2016, the PSF changed its membership structure and went to the open membership model because that was one of the other things going alongside all of this. The PSF was a very closed organization, very opaque to a lot of people. Van Lindberg drove a lot of stuff to open it up and make it an open membership organization so people could vote in board elections and just make it genuinely more representative of the Python community as a whole. 

Anyway, one of the things that came alongside those membership changes was the working group structure. The working group structure basically let the PSF set up a group of volunteers with board oversight that had the authority to spend the PSF's money. And that had the authority to spend earmarked money that was going to the PSF to say this money is specifically for that working group. 

And so, we formed the packaging working group. I'd have to look up myself exactly who the founding members were, but it was essentially so that the PSF could accept money that we would then spend to complete packaging projects, 

And the specific project we had in mind when we started was finally getting the legacy PyPI replaced by the new one because Donald had got the new one to the point where it was there and you could opt-in to using it, if you wanted to. 

A lot of folks opted into using it for uploads because they were much more reliable uploads. So essentially, you could use either one. They went to the same database. They showed you all the same files. Everything was fine. 

The issue was there was an unclear amount of additional work before the old one could actually be switched off because there were a few things that the new one didn't do yet. Mostly related to the web interface. There was still some tasks where you would have to go back to legacy PyPI if you wanted to do things. It was just the main package upload and package install flows that the new service had implemented. 

That's basically where the Mozilla grant comes into it. The packaging work group had formed, I think. The packaging working group had formed. 

The grant proposal -- I'd have to look up exactly who drove the grant creation. I think it might have been Eric Holscher, I think. Because yeah. We formed the group. We didn't actually get a proposal put together. 

There was a board election, and one of the new board members basically said, “I'm going to make this happen. What do you need?” I'm pretty sure it was Eric, but I'd have to look up records to be completely sure. (NOTE FROM NICK: I've checked the timeline here: The initial grant submission was drafted in July 2016 just after the WG was formed, but not actually completed and submitted at that point. Then in June 2017, Eric got involved and got things to the point of actually submitting the proposal in August 2017.)

All this was around the time when Sumana started getting involved as well. She was initially involved on a volunteer basis but also put in a bid on the actual project management side of the contract. (Corrects captioner spelling of Sumana’s name)

MEL: Another question. You're talking about the grant process in getting the PyPI migration. Is it appropriate to talk about the old PyPI, the legacy one and the new one as two separate projects or do you consider them to be two versions of the same thing? 

NICK: Software-wise, they're definitely two separate projects. It was just that as Donald was writing the new one he knew he was going to need a migration plan, so he wrote the new one to talk to the existing one's database. You kind of had this three-piece setup where you had a common backend SQL database and two servers talking to it. They were designed so they would happily interoperate with each other, and any changes one would make the other one would see. They're definitely two separate projects, but they were just closely related projects. 

MEL: Okay. If you think back to the time the grant was being written and figuring out who would be coming on board the grant to make that final migration process happen, going back to what you said earlier about your criteria for being well-maintained and being sustainable, how would PyPI, I guess both the legacy one and the new one that Donald had been making, how would that fit against your criteria? 

NICK: So, one of the biggest things was on the sustainability front, the PSF taking straight up responsibility for this as a service that the PSF provides and will make sure is functional. That's kind of the sustainability backing there, coming from the PSF. 

A lot of the actual work is still very volunteer driven, and so, there's -- it's not like the PSF is in a position to say we have this person working full time on making PyPI better. It is still grant driven, but at the same time, we have partial contributions from folks' employers to say this person has a certain amount of time to work on PyPI community stuff. At the moment, there's a reasonable amount of that going on, so there's still possible improvements to be made, but it is in a lot better place than a lot of projects and services. 

Another person I want to mention that got involved I think working directly with Donald on the front-end design stuff he was doing with warehouse, the new PyPI, and that was Nicole Harris, who got involved on the design side. Just actually putting some UX design work in place for the front-end part of PyPI. So not the [automation] API design, the actual web interface itself that people interact with in a browser. Again, she was participating on a volunteer basis which limited the amount of time that she could put into it for usability studies and that sort of stuff. 

Then that became the core of what let the packaging working group submit a credible Mozilla grant proposal, which was -- it was a bid that included the engineering work based primarily on input from Donald aided by Sumana and just going through with it to say, hey, what are the actual blockers, what is the stuff that has to be done before you can turn the old one off. 

Sorry. Two sets of things. What is the stuff that has to be done before we can make pypi.python.org resolve to the new one, and then what's the additional work that has to be done before you turn the old one off completely. 

That was the thing of Donald had the vague idea in his head of what those two lists consisted of, but it was Sumana who drove the process in saying, “this is what's missing.” Then Nicole had the list of, “this is the actual work that needs to be done to finish out the web interface.” Pretty sure it was Eric, as I said, who drove the, okay, let's actually get this grant proposal written and submitted and then Sumana did quite a bit on that front as well. 

In that case of the initial grant, it was the case of the working team -- it was the people who wanted to work on it, but needed to eat, that had a strong hand in the actual design of the proposal, with the PSF then putting in the oversight to say, “Okay, yes.” I think it was Dan Callahan who was the champion on the Mozilla side. 

Yeah. Then that grant was approved. There was a bit of editing as to a few things getting taken out because Mozilla going, “That particular thing is not within the scope of what Mozilla will fund.” There was a little bit of that on the edges, but the core of the proposal was like, “Yeah, that fits in with what the foundation grants are for.”

The process has changed a bit since that first proposal because again this is just growing organizational maturity on the part of the PSF, which is essentially the -- after the funding is secured, the PSF will actually put out a request for proposals to make the thing. 

There's that side of the process that's become a bit more open. We just had to do it differently on the first one because it was -- to make a credible proposal to Mozilla, we had to have a very concrete idea of how we were going to spend the money, which meant having the contractors lined up before the grant went in, rather than finding them afterwards. 

After having that first grant done, you get a better idea of what things cost, how much money you need, even if you don't have specific line items for each of the items that you want. 

The other thing there was having that understanding of, yes, you need to budget for project management. Yes, you need to budget for UX work, and you need to budget for the underlying engineering work to actually make the service go. 

MEL: I think that might actually make a good point to pause for this round, I’m looking at the time. Then we'll resume in the second round. 

One thing that is going to happen in the second round of interviews is that people start seeing bits and pieces of each other’s [interviews]. Is there anything you're particularly curious about, knowing I'm going to be talking with other folks that were involved in the migration to warehouse, and also knowing I'm going to be talking to folks that were not and were watching from the outside and were unaware of some things happening from the outside. Is there anything you're curious about that I make sure to pull in next time we talk? 

NICK: What I would be kind of curious about is what were people doing at that 2013-2014 point where a lot of the stuff that kind of culminated in the new PyPI in 2018 -- what were they doing at that starting point? Why did they get involved? 

Because I know why I got involved, because I was working for Red Hat at the time. The packaging to Linux packages story was just, like, oh, God, we have to be able to do better than we're doing right now. I was working for one of the platform providers and going, we've got to be able to do better than this. 

MEL: Okay. Anything else? That's for the folks that were also involved in the warehouse migration. Anything about the users that were not? 

NICK: Also with folks on the PSF side. Particularly if you talk to Ewa. 

MEL: Okay. 

NICK: That's been an interesting journey on that front from event coordination to executive director of a software nonprofit. 

MEL: Yeah. I don't think I'm going to get a chance to talk with her for this project, or at least the initial part of the project, but we've got some people who may have been on the PSF board at the time or otherwise very involved with things. I don't think anyone [talking with us about this project] has gone back as far as 2013 yet [when telling the PyPI story]. 

NICK: It was all very -- yeah, it was all the prior work to create -- to get to a point where the PSF was a credible grant recipient. That's been a lot of work by a lot of people. It was one of those things where often you get asked, oh, why do we need that. Because you're asking people to give you money to spend. You need to be a responsible steward of those funds. 

MEL: Cool. Okay. To wrap up here, I'll clean up the transcript a little bit and then send it to you over email with the licensing bit. Once we get more people's first round interviews done, I'll have Heather reach out to you again about scheduling. 

NICK: Okay, cool. 

MEL: This has been fantastic. I had no idea of the earlier backstory, so thank you so much.

NICK: Okay, cool. 

MEL: All right. See you in a bit. 

NICK: See you next time. 

MEL: Yeah, bye.
