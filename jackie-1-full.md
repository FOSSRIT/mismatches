# Copyright transfer statement

MEL CHUA hereby irrevocably transfers and assigns to JACKIE KAZIL  in perpetuity, all right (whether now known or hereinafter invented), title, and interest, throughout the world, including any copyrights and renewals or extensions thereto, in the attached transcript of the interview recorded between us on AUGUST 28, 2019 in A LIVE-TRANSCRIBED PHONE CALL.

# License

I, Jackie Kazil, hereby release this work under the following open license: http://creativecommons.org/licenses/by/3.0. Anyone is free to share and remix the work as long as they cite it. I consent to the open publication of this work using my name.

# BEGIN TRANSCRIPT

MEL: Okay. Are we ready to begin transcription? 

JACKIE: Yeah. 

MEL: Okeydoke. First question is, if you could introduce yourself a bit and talk about your relationship to PyPI. 

JACKIE: Sure. I am JACKIE Kazil. I'm a member of the Python community. I sit on the board of the Python foundation, but my primary relationship with PyPI has been as a member of the user community as someone who has published packages to PyPI. 

MEL: How long or how often do you use PyPI? 

JACKIE: I think I've been publishing the package I maintain since about 2014. I've used PyPI as a programmer pulling packages since 2007, but as a person who publishes, 2013 or '14. I'm not sure how quickly after we created the project we pushed it to PyPI.

Wasn't there another part of the question? Oh, how often. How often? As a project maintainer, I probably publish a release four times a year. 

MEL: Okay. You've been around for a while and using PyPI pretty regularly, pretty heavily for quite a few years now. 

JACKIE: I could probably have been publishing more often, but I guess you could say that. Yes. 

MEL: In the context of all the Python programmers everywhere, you're someone who uses PyPI quite a bit. 

JACKIE: Yeah. In comparison to programmers everywhere, yes. In comparison to another library such as Requests or Django, I would say no. 

MEL: Okay. Before we launch into the history story of PyPI, the part about that, I want to take a step back and ask - to you, what does it mean for an open-source project to be well-maintained and sustainable? Some people combine those into one definition. Some people separate them. What would your criteria be for what does it mean to be well-maintained and sustainable? 

JACKIE: Well-maintained and sustainable. Before I answer this question, let me add one bit of context about my background that I think is important to this. Last year, at Pycon, I ran the maintainer summit, and sustainability was one of the conversations that was had there. The words I use or the way I would choose to describe it was probably influenced by others in the room. If you asked me before then, I might have given you a different answer. 

MEL: That's one of the reasons I wanted to ask you to participate, because I know you had that summit.

JACKIE: So, well-maintained. You know, I'm going to kind of frame this in what I look for in a project when I choose to use it or not. 

Because when somebody chooses to use a project, depending on the context they're using it in, if it is just the throw-away, one-off thing they're doing, who really cares? If the project does what you need it to do and your thing that you're building has a short shelf life, I think it's less important that it meet some of these criteria. However, if you are building something that eventually is going to be -- that is moving toward a production system or a product or something that you want sustained over the long term, I think it is more important that an open-source project is maintained and sustainable.

Some of the things I look for are “is a project regularly updated?” Are there regular communications? When was the last commit made? 

How many PRs do they have in their backlog? And when was the last time they merged the PR? Because you can have a lot of PRs. To me, as long as there's a movement and a path forward, I think that is a healthy sign. 

What you don't want is a project with 20 PRs that has not merged anything recently because it is kind of like hit a dead end for whatever reason. The maintainers decide to abandon it. So, I think that is a really important aspect. 

I think a great example of this that I love to use when I talk about -- I used to give this talk, and I haven't given it in a while called -- what was it called? Something along the lines of "UX of Open Source," so creating a welcoming environment and listening to users on what your libraries do and how they work. 

One of the examples I pull is GitHub's library page that interacts with their APIs. 
If you go to that page online, there is a bunch of libraries listed for a bunch of different languages with no distinguishing factors. When I look at that page, I think in Python specifically there are between seven to nine libraries. If someone is trying to understand what is the best library for me to do X, Y, or Z in GitHub, on the command line, how do they know which one of these do they choose? That's basically what I use the signals for when I had to make that choice. 

It becomes really obvious whether or not a project is something you will want to use when you click through the links and you end up on the project repo page by looking at how often are the contributions, is there any movement in the tickets, when was the last PR, are there active PRs. 

Now, in the context of that, there is one exception, and that is a library that is well-established and maybe -- and I think it is a rarity, but maybe it doesn't need additions. Maybe it's just fine the way it is, and that library is set out to do something and it has done it. The only updates it really needs are updates in -- to update patches from others and dependencies. Those are the only exceptions I look for. 

Most often, you can tell if a library is well-established because it is well documented. It works well. There haven't been tickets filed with bugs. Often, a library like that has name recognition. I can't think of one off the top of my head.

As far as sustainable, sustainable can, mean a lot of things. I look at sustainability as a sort of artifact of people and an extension of their time. 

Are the people working on the project supporting it in the best way possible, and are they able to -- or are they also working on like 20 other projects? 

Are there new people onboarding? Are there entryways for people to onboard? 

In that context, going a little further -- and I don't think a lot of people go into this element often, but have they received any money or support for the project that they're working on? 

I think a lot of people who are doing the open-source work that they're doing end upburnouted. Much of that happens in silence. It is often unrecognized until it is too late. 
MEL: The aspect of sustainability is -- what does that mean to you as a developer if you're looking at sustainability, and you know burnout is a factor but also that it's hard to see, what does that mean for how you look?

JACKIE: Well, I guess if I'm a developer and I'm trying to determine if a project is sustainable or not, I don't really look at that aspect. However, as a developer the only projects I have turned down as far as a lack of sustainability has been projects that have had like one gatekeeper. 

That was one of the reasons why I started the project I did, was because there were a couple of other projects that I felt had potential to be what I wanted to build, but I didn't end up using those or trying to contribute back to those projects because they had one person, a single point of failure, with no clear pathway to engage the community.

In one case, I felt like the gatekeeper -- wanted to maintain their status as a single point of authority. 

MEL: (inaudible)

JACKIE: Can you repeat the question again? 

MEL: You're talking about these projects that you didn't engage with with because you saw that single point of failure. What kind of indicators would you use for that? What gave you the feeling that, "oh, I don't think they're interested in making this less bottlenecky?""

JACKIE: Yeah. Most of them were direct conversations with the maintainer. I reached out to the individuals, and it didn't feel like they wanted to move forward with it or they wanted to be in complete control. In some cases, forking the projects seemed like it wouldn’t go over well. 
In one case, the person put their copyright, I think, on every single file in the repository, which made it feel very uninviting. 

MEL: Oh, boy. 

JACKIE: Yeah. To me, it was like this work is always going to be their work, and it was going to be an uphill relationship. These were sort of red flags to me. That's a very, I think, unique case, but my sample size is small.

As a user of other packages, I never really looked at sustainability because I always looked at it as, well, if this doesn't continue or this somehow fails, I can fork it. In the worst case, I can fork it and fix the things that I need to fix to make it work. 

MEL: Is (inaudible) the development (inaudible)? 

JACKIE: I'm sorry. Can you repeat that again? 

MEL: In talking about being a user of the packages earlier, do you mean a user of the code in a development sense of "I'm writing code, what other code do I want to use for that," or does this also apply to applications that you don't plan on ever developing for, like a browser or something you're going to never see the code there?

JACKIE: Yeah. I would say both. I'm never worried about sustainability. Well, I'm going to take that back. If I look at a project and I see one person's involved, then I get worried about sustainability.

Obviously, a package has to start with one person. You know, somebody is going to make that first commit, and that is going to be the first person. And whether they are one person, whether that turns into two, three, whatever, like when I see one person, I might pause. 

If it is licensed in a way that I can take it and fork it, then I'm not worried about it. That is not the goal. That is a safety net. Part of this is about getting done what you need to get done [in development] and part of it is about the community and being a good steward. Of course, I would try to contribute back first and hope that whatever project I contributed to was accepted. But if it wasn't accepted, then I would just use my fork.

MEL: Okay. Are there any other factors or criteria you can think of for being sustainable or well-maintained? 

JACKIE: Yeah. I don't think I can think of any others at the moment. 

MEL: Okay. This is the first round of the PyPI interviews, let’s talk about -- looking back at PyPI being well-maintained or sustainable.

JACKIE: Uh-huh. 

MEL: You talked about things like projects being regularly updated, communicating, backlog, the environment. If new people are onboarding, if there are ways to onboard, if other people can work on it. 

If you think about PyPI as a project itself, how would you describe it from your perspective in terms of, like if you were going to draw a graph of PyPI being well-maintained and sustainable over time? What would that look like and why? 

JACKIE: Just so I understand, for PyPI itself? 

MEL: Uh-huh. 

JACKIE: Okay. As far as it being a well-maintained project, I believe with the recent update -- when did it get its facelift? Like the last year or two? 

MEL: Uh-huh. 

JACKIE: I believe with that and some of the changes to the way the API worked it feels like a well-maintained project. 

I've never went and looked at the signals that I would for a library that I was using for development, because I view PyPI as a service more than a library in itself that I would use.

The maintainability part -- I see some of the maintainability stuff with respect to my role on the Python Software Foundation. 

As far as sustainability, I was a little bit more worried, a few years ago. A few more years ago, PyPI started out as a volunteer effort. No one was getting paid. Then people started to get paid. I feel a lot better about the direction now. 

The PSF is also talking about going after larger grants to sponsor various efforts. Part of that process is getting a financial committee infrastructure in place and an audit process in place because to apply for larger grants, you need to have the ability to show people your financials and do that a very organized and quick way. 

I can see a lot of hope for the future in the continued sustainability and maintainability, but ultimately projects like PyPI start as a side project. Then they continue to a point where at some point PyPI became a critical part of the ecosystem. It needed to move from people volunteering to maintain it to people getting paid to maintain it for the health of the community as a whole. 

Just to pull back a little bit, that doesn't mean people can't still volunteer and contribute. A lot of people still do that, but it is a different sort of level of responsibility and expectation. 

MEL: If you were going to sort of tell the story of PyPI from your perspective, just take the last two or three years maybe of let's revamp PyPI, going to Warehouse, how would you tell that story? 

JACKIE: Yeah. I don't keep as much -- I don't know that I could tell that story without doing a lot of research first. 

MEL: That's okay. 

JACKIE: If I was having a cup of coffee with a friend and they asked me what happened to PyPI, I would probably say something like the following, knowing that it might be full of errors. 

I know that there was an upgrade to the infrastructure, and there was the upgrade to the front end, which the front end made it more inviting and usable. 

I know that there was a firm that was hired to help with that. It's my understanding we have one internal staffer as well as a contracting firm, and then the contracting firm also subcontracted. It was a combined effort of the contractor, the staffer -- or a couple of staffers, but one main engineer internally, so it was a combination of all these people working together to be able to do it. But I could have a lot of that wrong. I'm not sure exactly. I'm not sure exactly where the work was divided. 

MEL: Yeah. This is really helpful actually. Even just at PyCon, when I was talking about PyPI, a lot of the response was, "oh, yeah, I heard something was going on there, but I never really thought about it." I think that's important. 

It shows, well, there's the question of how much do the people even need to know about this sort of thing. Because one of the benefits of having something be infrastructure is it is something you don't have to think about.

JACKIE: Yeah, I think people need to know about obviously if there's changes to the API. I don't know who created it, but there was the library called Twine, and there was a push or movement to use Twine over the previous method. I forgot what that was now, but part of that was because the previous method exposed -- I believe exposed a password or something on the command line or in transit. The new method encrypted it. 

MEL: Okay. 

JACKIE: That particular element is very important for people to know because you want them to move over as quick as possible. 

MEL: Yes. 

JACKIE: I think I discovered that accidentally. Then when I discovered it, I was like, how long has this thing been around and why didn't I know about it. 

One of the things that should be clarified is -- this is a misnomer. Like myself, just because somebody sits on the board of the Python Software Foundation, doesn't mean they know all the things that are happening. When I say that, they don't know everything about Python. They don't know everything that's happening in every corner, so there are still surprises like this. 

MEL: Yeah. 

JACKIE: There was -- I think a great example is when people make the assumption that I am a Python expert because I sit on the board. I'm very flattered. 
I think there's a lot that I know, but to put me -- to say that I have the same knowledge as some of the core Python developers, I would say that I can have the same knowledge if I choose to pursue to have that knowledge, but I do not. And I think some people make a lot of assumptions about the level of knowledge that board members have. 

MEL: Yeah. All three people interviewing are people who have been involved in the Python community for a long time. They have sat on the board, held other leadership positions, that kind of thing. And even those people can't keep up, no one can keep up with all this information. So the question becomes, what are the right things to communicate to who, because the situation can't be "everyone has to get more information all the time."

JACKIE: Another part of my background is that I studied journalism. Early in my career, I worked at The Washington Post and other news media outlets. If you think about it from a journalistic lens, part of it is editing that information.

Right now, when I publish information about a project, I discuss this thing. Here's something cool I found. Here's the release, and here's what the release contains. Because there's a minimal amount of information and the project is so niche, all of those things, I assume, are interesting to the people who are receiving them.

However, when you have a very complicated project with releases that are happening more often, it's like a minor release is less important and less interesting than a major release. Or if you have a minor release that let's say fixes a security vulnerability, there's nothing in the sea of information that is highlighting that. With respect to that, there's nothing highlighting it. 

That's kind of like what a news outlet would do in the world of information when it comes to news. They would sort of curate that, but there's no news publication that is necessarily good at capturing all the things Python. 

The PSF blog makes really great -- publishes a lot of things. Somebody might write a blog post, but there's no one necessarily looking at all the releases of everything to try to report on all the things. 

There were a couple of publications that do a good job. I can dig those out of my email if you wanted me to. I can't think of the names off the top of my head right now, but there's a really good curation of information happening. 

I would probably say the best way information gets passed along is somebody who is influential and knows about a project, like a go-to person for a project publishes something on Twitter that gets passed around. 

MEL: That is one way of doing things. It's maybe not the most systematic way ever, but it's one way.

JACKIE: Exactly. Yeah, exactly. You could say, okay, pull in PyPI data. Let's pull in the most influential projects or whatever it is, whatever metric. Maybe all the projects. I don't know. Then let's go mash those up with some GitHub and Twitter accounts. 

Then let's look for signals of people publishing information about their projects, because that's where they're going to go there's a security vulnerability. "You need to update this right now."

And I think some of the email lists that might exist with the project as well can sometimes be overwhelming and easy to ignore because there's a lot of conversations or mixup on how do you know, especially with highly active projects, what is important to filter.

And also let's be honest. With our email boxes, how many times have you lost an email, especially with high volume email lists, because Gmail or something else just decides to put it somewhere, and you didn't even know? 

MEL: With that in mind, is there anything that you wish you knew about PyPI? To give you a little bit of a preview of what's going to happen in the subsequent interviews, we are finishing out the first round interviews with everybody. And everybody's stuff is going to be open licensed and up on github -- when we come back for the second round, I'm going to bring bits of the interviews to each other. 

I'll probably come and bring you some of the things from people that were developing PyPI, what their insider backstory was and their thoughts on, "oh, my God, this is not sustainable and how do we fix this." Then I'll bring your stories over to them and say, hey, this is what it looked like from the outside and see how people respond to that.

Are there any particular things that you'd like to find out when I go looking for parts of stories to bring to you or things you're curious about that I can ask other people in subsequent interviews? 

JACKIE: Yeah. I think one of the things I would be interested in understanding or learning about is the story of the PyPI remake, the specific story. Not just my "I'm going to make up something but I really don't know anything" story. What was the impetus for that, and how we went about hiring the contractor and the role that everyone involved played? I want to hear the real story. Not the one I made up. 
(Laughter). 

MEL: When you were talking earlier, you mentioned being aware that there was some kind of grant going on. Do you want it to go back further? What are the bound to your story so I can go look for that? 

JACKIE: Yeah. Oh, yeah. There was a grant. No, I remember the grant. I know about the grants. It's more like -- I guess I want to answer -- maybe I know this, but I am just not aware that I know this. 

How did that all get started, especially with the grants, because we're looking into other grants, so how did that come into existence? Who was involved, and how did that sort of shake out? 

Because I know there isn't like a six-person team of people or an eight-person team of people working on PyPI. It is very slimmed down. And so, to do such a large effort you need to bring on extra people. At least for temporary relief. 

The other thing I would be interested in knowing is technologically how that happened. I'm just interested in how they made that transition. I think it was Sumana who did the actual -- did a lot of the communications around the switch being flipped on, the transition, but I don't know -- I'm really wondering what did they actually do technologically to do that and how did they set that up, because that might be into far in the weeds. 

MEL: Okay. Yeah, I can definitely ask about that and look for that in the transcripts.

You were asking about how did the grant come into existence. You mean the financial or logistical parts or how did people come to say, "this is a project we should work on, this is the problem we should solve?

JACKIE: Yeah, I think it is both of those that I'm interested in. 

MEL: Okay. Cool. Yeah, you had mentioned the PSF is looking at more infrastructure for grants and finance stuff. 

JACKIE: Yeah. When I talk about PSF being interested in more infrastructure for grants and projects, right now we provide a lot of grants to people around the world for conferences and workshops. We did a recent initiative where we provided a couple of grants or were in the process of providing a couple of grants that are larger than our workshops and conferences grants for advancing education in Python.

But with respect to what I was talking about, one of the things that we're in the process of pushing for are grants that are things that we apply for maybe in the half million, million to be able to advance some part of Python with a larger amount of money. And so, what those grants are, how much those are for, and what those are applied to are all being discussed, but I would love to learn a little bit about the back story of the grants that supported PyPI because that might be able to help us with the (phone signal breaking up). 

MEL: Grants as a thing that the Python Software Foundation gets, not just gives out. 

JACKIE: Yeah. This would be like the Python Software Foundation applying for grants from another foundation or from another source and then using that money to basically push some element of the Python ecosystem forward. 

MEL: Cool. Do you know if the PyPI grant had anything to do with the PSF going we should do this again and be better at it? Was that an influence on that? 

JACKIE: Well, I was one of the people -- I don't know if I was the person, but I was pushing for us to go after larger pots of money because we had never thought about it before. Our budget is about 3 million right now, and I thought, well, you know, what would we do, as a board, if we had another million dollars dropped in our laps? How could we help Python? 

If we don't come up with any great ideas that are worth pursuing, then we shouldn't pursue going to get a million dollars, but immediately, when you start putting it that way, people are like, oh, well, you could do X, Y, or Z. I'm hesitant in naming specific things because I don't want people to get excited if they're reading this.

Immediately, people are like, oh, if we had a million dollars, we could do this and this and this, and wouldn't that be great? Suddenly, there's a whole list of things you could be doing.

Then there's the question of you have to start somewhere. You can't have a $3 million budget and then go ask somebody for $10 million. You have a $3 million budget. You ask people for a couple hundred thousand. Then you grow that a little bit. Then maybe you push to a million. 

I don't know that the PyPI grant was independent of this or did not have any influence, but what I saw was -- I sit on the board of another organization in Washington, D.C. called Byte Back, B-Y-T-E B-A-C-K. 

Byte Back teaches digital literacy. Often to underrepresented populations. The first thing they do on the lowest level, when you come in the door, is they give you a task. Can you send an email with an attachment? Then they test you up to see the classes they offer would have the most impact and help in your life to put you into a living wage job. 

In one period, our executive director at Byte Back got a lot of extra funding from people who wanted to support the mission and the organization, and it was something like 100 grants here. 

They had a similar size budget. Somewhere at the time it was almost identical to the PSF. It was about 2, $2.5 million. 100,000 here. 300,000 here.

One of the grants was like 950,000 Canadian dollars, so it wasn't $950,000 American dollars. It wasn't quite a million, but there were all these extra pockets of money. 

Then we started saying, because people wanted to support the mission, what can we do? We were like in this amazing position. As a result, especially because of the support with that 900 and change Canadian dollars, which was provided by TD Bank, they made it possible for us to expand the services that we offer and develop more. 

Then you can start seeing big idea stuff. Like what can you do if you have the money? Once you get those ideas (phone audio breaking up), there's money out there. We just need a story to tell and a plan to put it towards so that people can trust what is happening with -- we're actually doing due diligence about -- sorry. We're actually providing and doing due diligence with respect to our financials, with respect to how we use the money and being responsible to the community. 

MEL: Cool. Okay. I think that gives me a lot to go into the second interviews with. 
Thank you. This is super helpful. 

JACKIE: I'm glad.

MEL: Do you have any other comments or questions or things you want to say about PyPI before we wrap up? 

JACKIE: Nope. 

MEL: Next round, I will bring back to you some of the things other people said about the back story that you want about how it came together. Then you can take a look at it, and then we'll go from there. The second round will be sometime next month. 

JACKIE: Awesome. 

MEL: I'll put it in a Google Doc, clean it up, and Heather or I will send it back to you later tonight, you can look it over, edit or take out whatever you want, open license it, that'll be it. 

JACKIE: Okay. Sounds good. 

MEL: All right. Thank you so much. 

JACKIE: Have a good day. Bye. 

MEL: You too.
