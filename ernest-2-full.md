# Copyright transfer statement

MEL CHUA hereby irrevocably transfers and assigns to ERNEST W. DURBIN III  in perpetuity, all right (whether now known or hereinafter invented), title, and interest, throughout the world, including any copyrights and renewals or extensions thereto, in the attached transcript of the interview recorded between us on SEPTEMBER 25, 2019 in A LIVE-TRANSCRIBED ONLINE VIDEO CHAT.

# License

I, Ernest W. Durbin III, hereby release this work under the following open license: http://creativecommons.org/licenses/by/3.0. Anyone is free to share and remix the work as long as they cite it. I consent to the open publication of this work using my name.   

# BEGIN TRANSCRIPT

MEL: Okay. And are you okay to start the transcript recording now?

ERNEST: I am, thank you.

MEL: Sweet. So… Welcome to the PyPI interview round two. So as I mentioned last time, what we did for this round was to go and grab bits from other people’s interviews, from the first round interviews, and I’ll be showing you some things, and you’ll just have a chance to respond or comment or ask questions if you want to go back and forth with other people on them. 

So the three people you’ll be seeing transcript bits from today… You may already know or know of. And since everyone’s stuff is public and open license, or in the process of getting up… I can actually tell you who they are. And you’ll see their names there. So Naomi Ceder and Jackie… I’m not sure how to pronounce her last name. Kaz-il? And then Terri Oda. So three people.

ERNEST: Who was the last one?

MEL: Who have been really… Terri Oda? O-D-A?

ERNEST: Oh, okay.

MEL: So these are three people who have been involved on the board level, really deeply involved in the Python community for a long time, and also people who have not been involved with PyPI development ever, and so they would be considered really well informed in the Python community, as well as downstream users of PyPI as infrastructure and service. 

So how would you prefer seeing these excerpts? I can put them into the transcript and give you time to read them. I’ll show you chunks at a time. I can also read them out loud to you. What would be…

ERNEST: I think in the transcript and giving me a moment to read is probably best.

MEL: Okay. So I’m going to put chunks in here, in italics, and then whenever you’re ready to expound, just start talking.

ERNEST: Great.

MEL: So the first bits are those three people responding to what they said about things like… Does PyPI feel like a sustainable and well maintained project? So this is a bit of a long one. Kind of hilarious.

> _Source(s): Jackie-1, Naomi-1, Terri-1_
>
> JACKIE: [PyPI now] feels like a well-maintained project. I've never went and looked at the signals [of sustainability and well-maintainedness] that I would for a library that I was using for development, because I view PyPI as a service more than a library in itself that I would use.
> 
> NAOMI: ...my sense is that a lot of people don’t really, really want to know the details too much. I mean, it’s sort of like a lot of utilities. I really don’t care about the details of my plumbing. I just care if it works or not.
> 
> JACKIE: Yeah, I think people need to know about obviously if there's changes to the API.
> 
> TERRI: So I had honestly never thought about the sustainability of PyPI. It was magic that was just always there, until Donald Stufft was looking for a job and Barry was like… Hey, do you know he’s the only one doing pip? And I was like, “What?! Wait?! What?!!?” So I really hadn’t thought about it at all.
> 
> NAOMI: I would say that... PyPI is well maintained. And is sustainable. Maybe neither one of those as much as we’d like. But I think both of those are true.  In that if there are issues that you have with PyPI, there is somebody who will respond.
> 
> TERRI: ...[I wasn't thinking about it because] I had been using it for about 20 years, and it had never been a problem... Maybe because I use PyPI less frequently than some other services. But as I said, it’s been kind of magical... I would guess that most people just assume it’s magical and sustained and great...
> 
> ...It’s still magical. I think... I’m assuming that all of the documents that I just read to do my [first] release [on PyPI] are probably new. They were certainly very up to date and easy to read... maybe they’ve always been perfectly up to date. But I just assumed that was part of the work that had been done.
> 
> NAOMI: I think that in terms of their openness to contributions, I think that’s also there. I don’t know that from having checked closely, but I kind of assume that, knowing the people who would be making those determinations. So I believe that’s the case.
 
ERNEST: Cool. Yeah. It seems like this is fairly in line. Naomi brings up a really good point around… Most people just don’t worry about it. As long as the service keeps working, they’re happy. I was really pleased to read some of the feedback around just assuming that the docs had always been like they are. 

And again, I think Naomi points out… The openness to new contributions. And that’s again something… It’s great to hear that other people recognize that it’s happening. And can see it. And yeah. All of these quotes seem up to date with what I consider the current state of things as well.

MEL: So one of the interesting things for me in reading through and pulling these together is… At least when I was reading them, I got the sense of people saying… Yeah, I think it’s good. I think. I haven’t really thought about it much, but I think so.

ERNEST: Sure. Yeah. And that’s why I think… I was happy to see Naomi point out a couple specifics around… “Well, why would you want to know the details, necessarily?”

But yeah. I mean… Still, I remember back previous to… The current iteration and current deployment of PyPI, and even earlier than that, you know, when PyPI was down regularly, people seemed to care a lot more. And it brought a lot more attention to it, and people tweeted about it and sent emails and had nasty discussions on mailing lists. 

And then as the availability of the service improved and the quality of the service improved, it did. It sort of faded back in the background. 

So I think people probably think about the sustainability of PyPI less today than they necessarily would have when it was crashing every couple days. Right?

MEL: Well… So I wasn’t going to pull this quote this early, but… Terri said something… Interesting. Related to that. So the bit from Terri… There’s a bit from Terri that you just saw up there, that was about… I don’t know. “It seems to always have worked for me.” And she used the word “magical” repeatedly. And didn’t notice that… it had been crashing.

ERNEST: Yeah. That would have been… The darkest days were in, like, 2011 and 2012-ish. Was when the growth was sort of outpacing the service. And then there was this initial bit of work. To make the service more robust. But fairly stable thereafter. Still had regular sort of incidents. 

And then over the past two years, it’s improved to the point where we generally don’t have user-reported outages like… Ever, really. There’s been one or two incidents that were a database migration taking a little bit longer than anticipated, so people couldn’t log in and change something. 

But uploads and downloads continued to work. And, you know, that’s what most people care about, with PyPI. 

But I mean… I do want to go on record saying that it isn’t magic. There are no magicians involved. You know, it’s just… It’s just software.

MEL: Yeah. So I think this is… There’s a part from Terri I wanted to put in, since you just reminded me of it. And so the context for this is… Terri is talking about… “You know, I didn’t realize that PyPI needed help. That things were going on behind the scenes. Because it seemed to work magically and perfectly to me.” And then she said this.

> _Source(s): Terri-1_
> 
> TERRI: Well, I’ve got to say… I feel kind of weird, working for a large corporation, that we don’t give a whole lot of money to these things. And I suspect maybe if more of my corporation knew that Python needed help, they would actually step up. 
> 
> ...I certainly don’t want to make things harder to use in order for people to realize that there was a lot of effort going on behind the scenes. But it was kind of funny that every time I talk about Python, everyone was like… Oh yeah. It’s fine. That’s it.
> 
> MEL: And what kinds of signals would have clued you or your company in to the… Oh, hey. We should maybe support Python more?
> 
> TERRI: I have no idea. I mean, obviously I should have had all of those signals, and I’m not reading them. So I have no idea what would work in the wider Python community.
 
ERNEST: Yeah. Funding from companies is something that… All things considered, fairly few and far between. The Python Software Foundation itself collects sponsorship from some of the big name companies. It’s significant, but perhaps not necessarily proportional to the success they’ve seen. With Python or just with… From the community. From the infrastructure. 

So it is an interesting problem, where the funding that we have found corporately for PyPI -- the biggest chunk came from the Mozilla Foundation. So that’s a non-profit. Not Mozilla itself. 

You know, there’s a grant from Facebook that’s sort of actually… Work starting soon. We’re in the RFP process for it now. And then there’s the OTF-funded work that we’re actually wrapping up right now. So between those, two out of the three of those are non-profit arms of other entities. That we applied for and received funding. 

And the largest corporate -- direct corporate funding of PyPI work -- came from Facebook, and that was specifically championed by an individual working at Facebook. So it is difficult. We’re not… 

It’s actually directly in the footer of the website to support -- you know, “Interested in supporting PyPI? Here’s how.”

And the majority of the small recurring donations we get are from individuals. Very few from companies. 

And so… I think it’s -- Terri makes a good point. It’s not clear what signals need to be made or who they need to be made to, in order to better… In order to make it better understood, precisely how helpful this funding could be. 

We’ve been really happy with the Mozilla-funded work… I’m sorry. And the OTF-funded work. Publicizing that as it was happening and publicizing the results did actually introduce more interest in funding more work. Right? 

So it’s been productive from the aspect of people… Just by telling stories, saying: Hey, this happened. Here are the results. It draws people’s eyes, and then sort of… They say… Well, how do we help too? So that has been the only successful signal, I think. 

As far as corporations or companies or private -- reaching out and saying we’d really like to participate. That I’m aware of. Other campaigns we’ve done -- we had a header on the website for a while, et cetera. Didn’t draw nearly the same sort of response.

MEL: Hm. So one of the questions I have -- from your perspective on the infrastructure end -- I know last time we were talking about the in-kind -- the resource donations that you’d gotten from the CDN, from Fastly, from Amazon. 

And how… I just want to think about how to phrase this question. If there were lots of small donors, would that be a better situation? Because right now, it’s like… If one of these pulls out, well, that’s a huge chunk. But on the other hand, if you have a lot of small companies saying: I can offer you this tiny bit of resources… 

And then there’s in-kind versus… Here’s some cash. And that’s different also. 

What are the trade-offs when you’re thinking about it from infrastructure sustainability between different kind of portfolios of support?

ERNEST: Yeah. I think I follow what you’re saying. So… The biggest trade-off would be from just the management perspective, right? So there’s really only one person, me, consistently looking out for all of the in-kind infrastructure stuff. 

And so if we have a bunch of companies providing small bits of service, it would be overhead of sort of -- managing that would probably be much, much harder. Right? 

So right now we have a fairly small list of names that we know we need to keep in contact with, and renew, and whatever, or know that it could potentially go away. So if we had a lot of small companies offering small services, it would probably just be harder to manage. 

Versus… If we had… Depending on how it came in, either large companies just providing recurring amounts of cash to run the service… Versus a large number of small companies or individuals providing cash to run the service, then there would be some clear issues with… 

If it was one giant donor and then a handful of small donors, that one giant donor going away would be a really big deal. But that’s sort of the same boat we’re in right now, with the in-kind donations of services that are very large. 

So I think the trade-offs generally become the overhead and the planning. It’s easier to plan just from a fiscal perspective if you have a bunch of small donors on a recurring basis, versus an in-kind donation perspective, it’s better to have a handful of them. 

So it’s my overhead and time in managing all of that, and making decisions on how to move forward and what services we do use or don’t. 

Part of me thinks that the best possible outcome would be a healthy mix. A handful of reliable infrastructure in-kind donations of service, combined with a decent underbed of recurrent funding that could either be sort of… Sequestered away as the reserve fund, or to fund specific things that we need, that we can’t necessarily get donations for.

MEL: And with that mix of funding and in-kind donations, I don’t know if that would make sense -- like, for instance, with the CDN, if you somehow needed more capacity than Fastly could provide as an in-kind donation, and said something like… “Well, we’ll give you X as a donation, but anything more than this, you would have to figure out a way to pay for…” And then you’re like… “Well, okay. We’ve got a bunch of donations from other people, cash. Here you go.” Would that be easy to work out? Hard to work out?

ERNEST: I’m not sure, from an accounting perspective. But assuming from an accounting perspective that would be okay… I think it would be reasonable. 

I mean, if the packaging working group is collecting funding to operate PyPI and we have overages to pay for, that would be the funding that the PSF would tap into, to pay -- to operate the services. So I think it would be feasible. It wouldn’t be optimal, clearly.

MEL: Yeah. And why would it not be optimal? If you could unpack that a bit?

ERNEST: Again, overhead. There’s limited resources and staff from an accounting perspective. And so just… The overhead of managing those sorts of small caveats and… Invoices and payment of invoices and all of that… You know, it adds up to be costly in time.

MEL: And how much of your time right now do you figure you spend in managing those sorts of donated -- infrastructure donor relationships, versus working on the infrastructure itself?

ERNEST: Yeah. It’s… I mean, probably somewhere between, you know, 10% and 15% of my time. It’s not a constant thing. You know, there’ll be things that are lapsing or things we need to coordinate. 

Overseeing it -- sometimes we have to just keep check. We do have a cap on what service might be providing, and sometimes you just have to look at that and make sure we’re not edging towards that, and if we are, make other plans or reach back out and ask for more. 

And then there’s the… Not complexity, but there’s the process of… We’ve done a lot of work to sort of formalize these relationships. In the past, a lot of them were informal to the point where, you know, they were not necessarily unreliable, but it would become difficult to extend or renew or contact someone if we have a problem. So that involves sponsor coordinators and accountants and things like that. And even the General Counsel, to review an agreement. So there’s a decent amount of overhead to it. 

I think my estimate probably is a little high. Might be closer to 5% to 10%. But you know, overall, it is a significant and sort of recurring but not necessarily constant amount of work.

MEL: And does that need to be done by you? I guess I mean… You, Ernest, specifically. But also someone who has all this infrastructure knowledge and that leadership role there?

ERNEST: So I mean it just sort of defaults to me. Because the agreements for these are now… You know, agreements between the in-kind sponsors and the PSF. And so if a volunteer says… Hey, I would really like to use X and here’s an introduction to that person. Then generally I would pick up on it. 

It wouldn’t be impossible for a volunteer to work with the sponsorship team and stuff to get this stuff through. It just sort of defaults to me, because I’m available and it’s something that is to fulfill the PSF mission. In regard to the community infrastructure that we provide. Right?

MEL: Yeah. Okay. So here’s the next bit. So when I asked you and Nick and Donald what the story of the PyPI-Warehouse migration was, you had fairly long detailed versions of it. For obvious reasons. When I asked Terri and Naomi and Jackie what the PyPI-Warehouse story was, I’m gonna put all three of them in the transcript right now. And I think they might all fit on one page.

> _Source(s): Terri-1, Naomi-1, Jackie-1_
> 
> TERRI: Once upon a time, people noticed that PyPI was… I don’t want to say not being maintained, but needed help being maintained. Needed help for the future. And went to put together a project to make sure that happened. They got funding from… I think it was Mozilla’s organization. And did something. I actually have no idea what happened in there. Except that there was a whole lot of infrastructure work. I know… I heard bits and pieces of stuff about the packages. But I don’t know what parts were in the Warehouse work at all.
> 
> NAOMI: [The Mozilla grant] meant, for one thing, we could employ not just a person to work on PyPI full-time... until we hired them as our infrastructure director for the PSF, but also that we could hire someone to do project management for all of that. So there was a substantial amount of money. And that was put together in ways to actually speed up and improve that development...
> 
> You know, the interface has been new and improved. Various other things, including the two-factor authentication, all of those things have been done to improve both the reliability, in terms of just how those things work behind the scenes, and how they look to the users up front.
> 
> JACKIE: I don't know that I could tell that story without doing a lot of research first... I know that there was an upgrade to the infrastructure, and there was the upgrade to the front end, which the front end made it more inviting and usable. 
> 
> I know that there was a firm that was hired to help with that. It's my understanding we have one internal staffer as well as a contracting firm, and then the contracting firm also subcontracted. It was a combined effort of the contractor, the staffer -- or a couple of staffers, but one main engineer internally, so it was a combination of all these people working together to be able to do it. But I could have a lot of that wrong. I'm not sure exactly. I'm not sure exactly where the work was divided.
 
ERNEST: Still waiting for it to come through in the doc.

MEL: Do you see it yet?

ERNEST: Yep. Yeah. I mean, for many people in the community, I’m assuming that their story for this was: One day, PyPI changed how it looked. 

And so for folks who are even remotely tapped into the ongoing… What’s going on… It seems reasonable. The responses that came in. 

You know, Naomi being chair of the board, it makes sense why Naomi had a slightly deeper insight as far as who was paid and how. 

I would say Terri’s response is probably the most akin to what I would expect to have heard from a general community member. And so it’s both… I guess a positive and somewhat, you know, a little bit of a bummer that people don’t have a better understanding of the story. 

We did do a lot of blog posts and tweeting and the user experience person for the project did outreach directly to users. And so, like, there’s a lot going on, and a lot of buzz and chatter. 

But that still doesn’t change the fact that for 90% or more of people that use PyPI, they generally go there to search for a package, and then install it with pip, and never really do anything else with it. And so their interest in the ongoings of a project like this are probably fairly low. 

And so about the only exposure they might have to that is when the UI changed, they might have been like… Well… How did this happen?! But yeah. Those responses are fairly in line with what I would have expected. Yeah.

MEL: So I think I want to leap back to this in a little bit. But… I also asked them… And so for the record, all of them had some kind of… Yeah, I don’t really know. This is just a story I’m sort of making up. So when you check with the people that are actually involved in this, I would like to know what the real story was. So they’re starting to see that. But there was definitely that like… “I’m not actually sure”… Quality to that storytelling. Here are some bits that people said about -- how did they find out.

I split this into two to keep it from being too long, so this is round one of two. 

> _Source(s): Jackie-1, Terri-1_
> 
> JACKIE: there's no news publication that is necessarily good at capturing all the things Python. The PSF blog makes really great -- publishes a lot of things. Somebody might write a blog post, but there's no one necessarily looking at all the releases of everything to try to report on all the things. 
> 
> I would probably say the best way information gets passed along is somebody who is influential and knows about a project, like a go-to person for a project publishes something on Twitter that gets passed around. 
> 
> TERRI: I guess I did see some tweets about the Mozilla grant when it was granted. So I saw some tweets from Mozilla folk and probably from a few Python folk as well... 
> 
> JACKIE: And also let's be honest. With our email boxes, how many times have you lost an email, especially with high volume email lists, because Gmail or something else just decides to put it somewhere, and you didn't even know? 
> 
> TERRI: I probably would have gotten all of that out of the Python-development list, or the Python-members list, or any of those, if I were consistent about reading them, but again, I have a toddler. So all of my mailing lists are basically on the floor unless someone tells me I need to go read them right now.... That’s on me, not Python people having them available. They’re all there. They’re on my phone, even. I just never see them. 
 
ERNEST: All right. Reading. Again, this tends to make sense with my understanding of the way people hear about things. Twitter is brought up. And mailing lists are brought up. And the PSF blog is brought up. And those are the major outlets for the way these things are announced and communicated. 

Right now. The PSF has a newsletter specifically that did include some of the Mozilla information in it. And Jackie hits on a really good point. There’s not a news outlet that is watching this stuff and summarizing it for easy consumption. 

We’re never gonna have one of those little push notifications. Have you ever gotten the news push notifications on your phone about something going on in the world? There’s never gonna be something about PyPI, I assume, in one of those push notifications. 

And so the chances of, like, people seeing it… You know, in passing really does boil down to: Twitter or other social media. But primarily Twitter. And then… I mean, the mailing lists are… Mailing lists, our discussion forums, are difficult to keep up with as well. So it is a difficult way to… There’s no silver bullet for how to get everyone who might want to know… To get it in front of them. And actually have them read it. So yeah. That all tracks, basically.

MEL: And I guess… So one of the things I come back to here, thinking about this, is… Is this a problem? You know, because at the very beginning, Naomi’s quote about… It’s like the plumbing. I don’t have to care. I don’t need to know.

ERNEST: Yeah. I think that’s a consistent issue. Nearly every maintainer of Open Source infrastructure that I’ve ever had the chance to speak with… It is very much the same basic thing. It’s like… People do not care as long as it’s working. And when it’s broken, people get really mad. 

And it is almost a perfect equivalency for, like, your electricity utility. I actually had a power outage the other day that was, like, three days long. Right? It went off Friday afternoon. It came back Sunday night. So it was frustrating, but, like, I let it roll off my shoulders, because I was like… There was a giant storm. And, like, what do you do? 

But for other people, it is mission-critical. Right? If you have certain medical devices, or any other thing going on in your home that requires electricity. Or if you’d made a large investment in frozen food, your power going out for multiple days is a huge problem. And similarly, there are power outages that happen regularly, that I don’t even notice. The only way that I know they’ve happened is like… Oh, the clock on my microwave is blinking or something. 

So it’s very similar in infrastructure in that perspective. In that small blips… Nobody really minds them. And sometimes they don’t even notice that they’ve occurred. And the larger outages tend to be stuff that some people can just sort of… Eh, understand and move on with their life. 

But other people have either built deployment pipelines around it, or testing suites that require PyPI. Et cetera. And so when things get… When things break a pretty significant amount of time, they really notice. And it’s painful for them. But the other 99% of the time or more, they just don’t care. 

And so… In a way, and this is something I’ve jokingly said, and I think I truly do mean it… In a way, it was somewhat nice back in the day, when we had regular-ish outages. Because it gave us a chance to talk to people who were relying on it. Without, you know, without having to figure out who to talk to. And what use cases there are. So I’m not sure. 

You know, there’s just no… There’s no way to really get people’s attention of the sort of… Any of these issues, without interfering with the work they’re trying to accomplish. 

Right? So if PyPI had, you know, recurring outages intentionally, to get people’s attention, we could probably do that. But it wouldn’t necessarily be in the best service of our community. 

So there was… I can’t recall it now. But there was a tweet… I don’t remember what the impetus for it was either. But there was a Twitter thread about, like, just turning all the things off. To get people’s attention. And I tweeted back and I was like… Hey, I think it would be a good idea. But I’m definitely not going to do that by fiat. We would have to, like, organize this some way, and have communications around it.

But, you know, it’s fun to joke about. But occasionally, I do think more deeply about… It is really one of the only ways we’ve ever even discovered use cases of PyPI that we didn’t know about before. Is when we go to turn off a feature or turn off some aspect or deprecate something on PyPI. 

There was, for instance, one page that was, like, a user interface page, that had the same exact information that the symbol index provides and the other APIs provide, but had one difference. And that was that it also included the latest version number, right there, right next to it. 

And so as we were migrating to Warehouse, we turned that page off, because it was very expensive to render, and we weren’t planning to implement a new one. 

And when we turned it off, you know, I think it was a few… About a month or so or more, before we launched Warehouse. It broke a very prominent IDE. Right? 

And so that day, we got a ton of signal about… Why doesn’t this part of this IDE work anymore, for installing pip packages? And the answer was… Oh, well, we turned that page off. And so… But we had no idea it was being used in that way. 

So it’s very similar. We don’t get a great chance to communicate with people who rely on this, before something breaks or goes away. And that’s frustrating. Because as much as we might try to promote and say… Hey, tell us about how you’re using PyPI… We get almost no feedback. 

You know, I think the UX… The person who’s done most of the user experience for PyPI has done lots of interviews for different features and different things, and has still maybe only talked to 30 or 40 users. Right?

That’s a significantly smaller number than the number of actual users there are. 

MEL: Yeah. As you’re talking, as you’re telling this story, I’m thinking a bit about… When Donald had his first interview, actually, he was talking about… One, having to clean up the APIs and make it clearer -- what are we supporting? What are we providing? Why are we providing it? And documenting that, instead of having it be ad hoc. 

But he also talked about: How do you make a change to PyPI? You make a change and you try it in test PyPI, and then you push it to production if that works, and you kind of hope it doesn’t break something. And you’ve almost noted the parallel, but instead of technology breaking, it’s people going “Oh my gosh, it doesn’t work.” It’s the communication streams.

ERNEST: Sure. And that is basically -- I mean, the workflow of how do you make a change… Push to test PyPI and wait. It’s actually outdated. Now we don’t use test PyPI for the same reasons anymore. Because we have better tests. We can ship things more confidently. 

But as far as making an actual change to the service, we could announce it for… We can scream our heads off, practically, and whenever we ship it, we’ll have more people contact us to say: “You broke me!” Than probably actually read any of those announcements. And so it is. It’s… Yeah. It’s sort of unknowable.

MEL: Yeah. I’m also thinking about the recent sunsetting of Python 2, which is… I don’t know how many years in advance. Announced everywhere.

ERNEST: Well, I mean, it was even delayed. It was scheduled for… I don’t remember exactly when. But I think it was maybe two or three years ago, and it was extended, and now we’re reaching the extension date of, like, January 1st, 2020, and suddenly it’s become a much bigger deal. 

And again, I don’t know… I’m not involved in that, luckily. But I know it is gonna be really painful for a lot of organizations. So it’s unfortunate, but again, there’s no… Yeah. 

I don’t know the answers to these questions. I don’t know the answers to how you actually get people to understand the gravity of a change or even just read that a change is going to happen. Without doing… 

We could email every user on PyPI every time we make a change. But… A bunch of people would probably just unsubscribe. And not ever want to hear from that again. And move on with their lives, and then it would break and they would get mad. And so… And we probably couldn’t actually email everyone. That would be kind of expensive. But… Yeah. I don’t know.

MEL: So if you could magically get any information you wanted from PyPI users… There’s a lot of them. So all the information would probably be overwhelming to read… What would the most important bits be? Who would you want to hear from and what would you want to hear from them about? And either how often or what should trigger that notification to you?

ERNEST: Okay. So me specifically… I would love to know what people are using XML RPC API for. It’s been around for a long time. And it still sees… Probably it’s the majority of the backend traffic that PyPI itself actually sees, and it’s something that’s very… It’s not problematic, necessarily. But we require a lot of resources to support it. So I would really like better use case understandings for that. 

Because we don’t have any insight into it. Because it’s an anonymous API, and it doesn’t provide us really any information about the user, except for a user agent string. 

And so I think that’s probably the biggest one, would be: The people who are programmatically interacting with PyPI, what they’re using it for, what their expectations are, and how we could better support them, without having to maintain a legacy-expensive API. 

As far as frequency goes… I think it’s difficult. Because some parts of PyPI are unlikely to ever change. Right? Like, the interface for downloading and installing PyPI, the simple interface, we’ll likely maintain that as long as… There’s a PEP that defines that behavior. So we have to maintain that until the pep changes. And so if there’s never a proposal to change the PEP, or to deprecate it, we don’t… We just have to adhere to that contract, effectively. 

So it’s really all of the ad hoc uses of PyPI that are the most interesting. And require us to do the most tiptoeing around deprecating or replacing something. 

And so the cadence for that feedback… I think it would always be welcome. 

But realistically, it would be triggered by knowing we want to make a change. And having some way to communicate with people. Hey, we’re thinking about making this change. Can you provide feedback? 

And the current issue we have with that has been the latency. Sometimes a project -- or there might be a desire to do something with some expediency, and the feedback doesn’t necessarily come in at a pace that supports that. 

So it’s generally difficult to engage with people who aren’t part of the core Python community, if you will. Big users. Or… I don’t know exactly. But people who are sort of closer. We can get feedback from rather quickly. But they don’t represent, you know, the entire user base. In the way that we would need, in order to make some of these changes.

MEL: And two things… I’m curious if two things that may or may not make a difference… So that challenge you’re talking about, in terms of being able to get user feedback… Do you think that this is different between infrastructure and then projects that are not infrastructure? So like how Jackie went -- oh, well, if I’m using it as a library as a developer, I’ll check this out, but for infrastructure, no?

ERNEST: Um… Well, yeah, I think it is. There’s a major benefit for a library. In that libraries can deprecate features in a more gradual way. 

Like, we don’t necessarily have the same ability with PyPI. We can add headers to responses. We could, you know, but we can’t inject a message into these XML RPC responses, just as an example, specifically, because that would almost assuredly break them just as badly as turning it off. 

Whereas in a library, you can add deprecation warnings. You can even go so far as to just remove a feature outright, in a release, and if that causes someone a problem, they just downgrade and come to your issue tracker and discuss it. Right? 

So we did something similar when we deprecated TLS 1.0. Some time back. So we were gonna be turning off a specific protocol for TLS. 

And as we led up to that change, we had, like, rolling periods where we would turn it off for it… I think it was the first five minutes of an hour, once a week, or something. And then we’d slowly ramp that up, until I think it was the first five minutes of every hour. And that gave people a chance to see what was going on, but it still caused them a dramatic amount of pain. 

And so we don’t have, like, we don’t have necessarily what we need to do that for any given feature on PyPI. But it’s sort of the closest we could come to that gradual deprecation. Would just be breaking it in a consistent, reliable manner. So the people could either program around it, or change their cron job time, or whatever they needed to do, where they can escape it, until they figure out what to do next. 

And so we’ve discussed trying that with some other features, but have never actually done it. But it’s the closest we get to a library. 

All of this sort of gets back to the part where… You know… I think libraries have a slight advantage, in that, again, people can just pin to a specific release, and then have a discussion in the issue tracker and stuff, and then when they’re ready, upgrade. Versus running a service that’s sort of inverse. We can have lots of discussions and try to reach out to people, and then when we’re ready, we can deploy it. But that doesn’t necessarily line up with everyone else’s timelines. 

And so from a library maintenance perspective, I think there’s… It’s a little bit easier. I don’t think it’s easy. Maintaining Open Source software is always painful, practically, it seems. But there’s an advantage, where, again, your users can move at the speed that they desire, within reason. Whereas running a service… Your users have to be up to date with the current state of the service.

MEL: Yeah. And then the other thing I’m curious if you feel there’s a difference between… Infrastructure that’s Open Source and infrastructure that’s not. So if this was a corporate paid thing…

ERNEST: Oh, sure. So I mean, if people paid for PyPI, I’m sure we would do things differently. Right? If everyone had a billing plan to download or upload or whatever, we would have to… Respond differently to some of these things. You know, it’s sort of just logical, right? 

But it would also mean that we have a formal relationship with them too. Like, right now, we have… They agree to our terms of service and they sign up. And that’s sort of that. 

If people were paying us, we would have a formal relationship with them, where it would just be… It would probably be more direct to just… You know, we would also probably know who to contact specifically to ask like… Hey, is this something you use? Or how do you use it?

I’ve worked for companies… I don’t think I’ve ever worked for a company necessarily that has as many end users as PyPI does. So the scale is much larger too. Because it’s free, there’s a much larger pool of people who would be relying on the service. And the expectation from us to them and them to us is different than in a corporate or not Open Source infrastructure thing. So… Huh. Um… Yeah. I’ve never gotten a good chance to speak with, in depth, anyone who maintains, like, a for-profit package repository. I mean, there are a number of them out there. You know, but I would be interested to hear their feedback on that. I mean, as far as I’m concerned, none of the…

(captioner connection dropped)

...specifically around the APIs. They generally implement the simple index, and then, you know, user access control for uploading packages and downloading packages. That’s generally sort of the scope that they covered. And then we have all the other various… Like the JSON API, the XML RPC API, and the web interface that people rely on now. So it would be interesting to hear, though, how they approach it differently. But the biggest thing would probably just be service level agreements.

MEL: Yeah. We had a bit of a connection drop earlier. What were you saying between… It’s in the transcript. But… You talked about being interested to hear their feedback on… And then we dropped.

ERNEST: Yeah. During the connection drop… I was just saying that I don’t think any of the for-profit package repository hosting companies have the same number of interfaces that PyPI does. And so I don’t think they have to worry as much about deprecating any Python or PyPI-specific things the same way that we do. You know, I doubt any of them implement the XML RPC API. I doubt any of them implement the JSON API. They mostly tend to just implement the simple API.

(connection dropped again)

MEL: Um… Waiting for captions to catch up. Okay. Cool. So… Coming to the end of the time for the second interview. This has been fascinating. This is fantastic. Thank you so much. Does this prompt any new or different thoughts about sustainability of infrastructure and Open Source and PyPI?

ERNEST: It definitely puts a fairly fine point on the communication aspects of all of this. Right? It’s something that is hard to get right, and hard to stay on top of, but yeah. I mean, the bidirectional communication between users and the people who work on and run the service is hard. And I’d really be interested to hear, honestly, if any of the other interviews have perspectives on that, that can help us improve it. You know, again, not only is it sort of crucial and hard. It’s also time intensive, to stay on top of...

(connection dropped)

That’s probably the big…

(connection dropped)

(Mel wraps up interview, thanks Ernest, jokes about infrastructure issues happpening at the end of each of our interviews)
