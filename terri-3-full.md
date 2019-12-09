# Copyright transfer statement

I, MEL CHUA hereby irrevocably transfers and assigns to TERRI ODA in perpetuity, all right (whether now known or hereinafter invented), title, and interest, throughout the world, including any copyrights and renewals or extensions thereto, in the attached transcript of the interview recorded between us on OCTOBER 11, 2019 in A LIVE-TRANSCRIBED PHONE CALL.

# License

I, Terri Oda, hereby release this work under the following open license: http://creativecommons.org/licenses/by/3.0. Anyone is free to share and remix the work as long as they cite it. I consent to the open publication of this work using my name. 

# BEGIN TRANSCRIPT

MEL: That works. It's good. And we've got plenty of time. So, no rush. Shall we start the official transcript at this point?

TERRI: Yep.

MEL: Okay. So, PyPI interviews round three. So, there are three things that I wanted to show you today if we have the time. And one is actually -- this might take most of the time -- is the sort of first-round analysis that we have been starting to pull together. And we don't have all our data yet, obviously. But in starting to think about what this should look like, we're curious if you have any initial reaction. 

And the second and third thing here is an aggregate of what people said about what it means for an infrastructure project to be well-maintained, and then the third one is what people said about sustainability.

So, that's sort of the agenda for today. And so, to start out with a bit of our extremely early stage -- so, all the disclaimers of “words are hard.” Maybe these are not the right ones. I'm not sure. All that stuff. And as we were starting to look through what people said, one of the things that we were trying to differentiate is, okay. We were thinking about sustainability. What difference does it make that this is about infrastructure versus software in general?

And on that front, Jackie actually said something in her first interview that was a really good example of the difference. So, I'm actually going to put that right in here. So, the context for this was when I was asking Jackie about sustainability, she responded from a developer perspective going, “oh. I hadn't thought about that. And here is why.” And that leads, I think, to the distinction between infrastructure and general software. So, I'll give you a moment to look at that and respond to that for a bit.

> _Source(s): Jackie-1_
>
> JACKIE: As a user of other packages, I never really looked at sustainability because I always looked at it as, well, if this doesn't continue or this somehow fails, I can fork it. In the worst case, I can fork it and fix the things that I need to fix to make it work.

TERRI: I suppose that's true. I don't usually think of it that way because I have to think about it in terms of sustainability for the purposes of security. And if I fix something then I'm on the hook for all that. And I don't usually want to be. So, I usually don't [skip looking at sustainability] now. I guess I have historically. But I usually don't anymore.

MEL: Yeah.

TERRI: I guess I always could fork things, but it's very rare that I do, I guess, in practice.

MEL: And this actually -- this just sort of came up in a couple of the other interviews for the PyPI maintainers. The upstream. [The notion that] oh, yeah, one of these differences between maintaining infrastructure and maintaining non-infrastructure software is that if it's a library or something, maintaining it and updating it, there's still a responsibility there. But the users get to decide when to switch over. Whereas with infrastructure, we decide everyone is switching now.

TERRI: Yeah, whether they like it or not.

MEL: Right so, we went from, okay, cool the fact that infrastructure is important and leads to a couple of qualities that would be true. Whether this was open source or not. And then so, right knew we have five big thematic clusters. Would you like me to put all five of them at the same time? Each of them is one or two sentences. Or do you want to go one --

TERRI: Yeah, might as well put them all in, then.

MEL: Okay. Hang on one second. I'm gonna take it out of this, make it a numbered... Ah!

> _Source(s): notes-11-10-2019.md_
> 
> 1. Infrastructure is “magical plumbing.” FOSS infrastructure lets you look behind the curtain if you so choose; non-FOSS infrastructure likely does not.
> 
> 2. Infrastructure requires technical effort for operations (as well as development). FOSS infrastructure may begin as a pet project and then “accidentally” go into production; non-FOSS infrastructure is more likely to be deliberately planned as a product launch.
> 
> 3. Infrastructure requires development capacity (people-time). FOSS infrastructure is likely to have some or all of this development capacity come from self-directed volunteers, but that effort is also more likely to fade out during the “last mile.” Non-FOSS infrastructure is more likely to have its development resources known, managed, and allocated in advance.
> 
> 4. Infrastructure requires bureaucratic/organizational work. FOSS infrastructure is likely to have this set up late, during the “last mile” or the “sticking point.” Non-FOSS infrastructure is more likely to have this infrastructure (legal, organizational, financial, managerial, marketing, etc.) be set up early.
> 
> 5. Infrastructure user data and usage patterns are important for determining future resource needs. FOSS infrastructure maintainers are less likely than non-FOSS infrastructure ones to have complete and reliable access to that data because of intentional cultural choices to prioritize user freedom and access over it.

TERRI: Sorry, I'm laughing at number two, the assertion that non free and open source software is better deliberately planned as a product launch. I wish I believed that. [I don’t believe that non-free software is better planned than free software.] 

But I do work in an open source section of a corporate environment. So, maybe my experience is a little different than average. [But I see both non-free and free software projects struggling with the same “now this is production” type problems.]

MEL: That is true. And also, I put “more likely,” not “definitely will be.”

TERRI: Yeah.

MEL: I worked for Red Hat. Which is technically corporate but it’s an open source company. So, I'm like, yeah, corporate is -- wait, kind of.

TERRI: All right. So, number two aside. I definitely agree with number one. That you have -- you have a great many larger opportunities to work behind the curtain. 

I think that is part of why the others seem to be true, though. So, like the assertion that non-free and open source infrastructure is more likely to be deliberately planned with a product launch. I work in an open source part of a larger corporation and I have not seen that be true in practice. So, I don't see that our open source parts are more likely to be deliberately planned than our non-open source parts.

MEL: Can you elaborate on that a little bit?

TERRI: I'm not sure if I can, really. Because some of that's probably considered proprietary information. 

But because I often get pulled into things later on when we're at the point of, “this is going to be real infrastructure that we need out. Can you do some checks to see whether it's okay [in terms of computer security] before it goes out?” 

And obviously, I do this mostly for open source infrastructure. My mandate is the open source side, but when I ask around [for best practices], I hear just as many stories about the demo that became a live product for non open source as I do for open source.
 
I think it's just not known that it's happening. I think people -- I mean, I wouldn't say they cover it up. But you have a nice slick marketing plan to go on top of the demo. And we never talk about the weird decisions in the beginning. Unless you're talking to your security person whereupon when somebody says, “why is it designed like this?” Everyone will always admit, well, it was just a demo.

And so, I think the magical curtain there is maybe hiding the fact that this pretty much is just a thing that happens with software. 

Often you don't realize you need infrastructure until you're halfway through building it and then you grab a server and do something quick. And, yeah. I think that just happens with software. 

I don't think it's really true that we planned it better on the non-open source side of the house. I could be wrong, though. As I said, I obviously do work on the open source side of the house. 

So, I'm seeing something that even though we're inside a corporate culture that has, for example, number four, we definitely have all of the bureaucratic and organizational work set up in advance. And that, I think, is not a function of being open source versus non.
 
In fact, the legal infrastructure for open source is particularly good because we have to deal with licenses. So, we have our lawyers who specialize in that and procedures for making sure that we make good decisions about licenses very early. So, that exists. But that exists because we're a company that can be sued. I don't think it's because there were non-open source people involved in the original decisions. That's part of the corporate culture. 

Maybe we're making a false equivalence between non-free and open source software and software that is backed by corporations.

MEL: Yeah, this is a really open conversation because that sort of ambiguity -- not ambiguity -- but the overlaps. It's not clear, not that everything is either type A or type B, but really the situation is that it’s a lot of mixed subtypes.

TERRI: Yeah.

MEL: So, yeah, that helps me think about how we might be rephrasing it to be more -- more specific and more accurate. Because, yeah -- I think the --

TERRI: Yeah, maybe we can say it's the difference between community and corporate projects in that respect. Like, I would agree that community projects are less likely to have legal infrastructure financial stuff set up in advance. But --

MEL: Okay, yeah.

TERRI: It doesn't matter whether you're open source or not. It just matters whether you have other legal frameworks to work around, I guess. 

So, community versus -- even a decent number of community projects have legal in their organizational infrastructure, though. Varying amounts of it. I would definitely say that my corporate projects have more of that.

MEL: Well, one aspect of the legal infrastructure which is probably not clear in the current phrasing actually was something that Nick brought up in that it's not just licensing. But, for instance, if five or ten years ago, if a bunch of people said, I've got money. I would like to give that money to Python packaging. The PSF at that time didn't have time to say, why, yes. We will take money from random people at different countries in the world and we will have a way to funnel that to other people in other countries. Legally.

TERRI: Yep. Yeah. We had that problem with the Free Software Foundation. Mailman had a fairly large donation and had no idea how to manage it because it went into one giant bank account. And figuring out how to get money out of the giant bank account was really hard.

MEL: So, lots of stuff like that. Things like, oh, jeez. You're in Australia, your donation is not tax deductible. Because we’re a US nonprofit.

TERRI: Yeah, and I mean, naming and stuff too. So, for a lot of, I guess, for mostly number four, and a little bit with some of others is -- 

I lost my train of thought completely. I shouldn't have tried to read and speak at the same time. 

I guess we have actually kind of ridiculously complicated. We have been trying to document what it takes to release software at work. And there are different procedures for each part of the process. So, there's procedures for the licenses, there's procedures for naming, there's procedures for marketing, there's procedures for security. There's procedures for quality.

And all of those exist whether we do open source or not. And, yet, even though all of those exist, that doesn't stop us from having the same problems that you see -- that you see in number two and number five. 

So, like, even though we have this fairly elaborate set of procedures we use for building software, it is often true that infrastructure stuff -- or even smaller software projects -- are just, “hey, I built a thing to do this need. I want to give it to people. Now what?”

And so, even though we have all of these procedures and they're already there, we don't always know that we're gonna need them until we do. So, it's just like -- 

MEL: But once you need them, they’re already there.

TERRI: Yeah. They're already there once we get there. And they're a source of great frustration right now for a lot of people because it's a lot of procedures. And you think, oh, well, I just made this little Docker file that runs this other thing. Why do I need to go through all of these things again? And sometimes you do and sometimes you don't.

And so, we hit that a lot. so, I guess what I'm saying is that even though it's already there, I'm not sure that always helps. I guess. 

And -- I'm not sure that it's true that we know data and usage patterns for a lot of our early infrastructure projects. 

There are some things where if we're trying to set up a server that's -- that's handling existing tests, we know a decent amount of throughput and what.
 
But I said that it's often the case that we put out a demo and we have no idea if anyone's going to use it. And sometimes that demo requires some level of infrastructure. And we just don't know, basically until you're on the stage exactly what the numbers are going to be. We can estimate. 

But I'm not sure we're really estimating that much better than an open source project would. I guess the difference is really that we try, maybe?

MEL: It's not just looking forward. But also looking back -- so, maybe you don't have a way to predict it any better. But if two months into one of your services, I said, hey, so, in the two months that you have been up and running, what's happened? Who has been using it? What are the various statistics on traffic or whatnot? 

I guess one of the things I'm claiming as a -- let's test this and see if it works [idea] -- and, again, it might not be an open source versus non-open source. It might be a corporate-backed versus more of a grassroots organizational thing. 

But the non-open source and/or more corporate or structured group would be, why, yes. We have server logs. We kept track of them. We have survey data. And here it is. And nicely structured. Some versions of that. Here's a format you can use. And an open source project or a less corporate-backed project or whatnot might be like, do people use those things that sorts of thing.

TERRI: So, I suspect you're probably right in general. But I know that here specifically our privacy rules actually stop us from holding a lot of data. So, it is not abnormal for us to discover that we don't have the data because we have been vigorously purging server logs and whatever for anything that we don't need. Because of our privacy compliance choices. 

I don't think that's true at other companies. If you're a company that makes money off that data, then you probably do have it. Or if you're a smaller company that doesn't know if you're gonna make money off that data, you're maybe more likely to have it. But, yeah, we drop a lot of that stuff on the floor for privacy reasons. 

And I guess that proves the point, right? That there's an intentional cultural choice here to not keep user data. In this case, because we're a large company that could quickly become a surveillance point. And because we've made decisions to not be a surveillance point. Then we have to dump it all the time. So, that no one has it. Including us. 

So, I don't know. I... I guess that really proves it. The intentional cultural choices to prioritize user freedom and user data access. And maybe we should add privacy to that list. Definitely makes infrastructure projects harder.

MEL: Yeah. And this is a good discussion to have. Because one of the things that I think the current, you know -- doesn't do very well. I'm trying to stay away from essentializing this and saying open source does this. Non-open projects do it like this. That's not the case. Open source projects are really ones that use this license.

TERRI: There's percent chances.

MEL: Right. And so, we can't essentialize. But there's something we can say about tendencies or some open source projects have this kind of culture which leads to the following. Or because of these choices that these other factors come into play, that's a bit of what I'm wrestling with.

TERRI: Yeah. I think all of these things are probably generally true except I'm not sure I agree on number two. I think it's just hidden that this happens everywhere.

MEL: But that's a good point. Even if it doesn't happen, it seems like that, you know, it could seem like from the outside that's what's happening. Because there is the curtain. The curtain being closed versus the curtain being open. You can -- you're able to pretend more that -- like, oh, well --

TERRI: Yeah. It's worth noting that all of these things we're saying that non-free and open source projects have are what would be more ideal, right? So, it would be nice if we had infrastructure deliberately planned. It would be nice if we had better knowledge of resources. It would be nice if we had infrastructure for bureaucratic and other organizational work. And the only one that maybe isn't the nice thing is it would be nice if we had the data which, as I said, for privacy reasons sometimes it's nice if you don't have the data.

So, I wonder if the fact that we're getting this impression is partially just because people want to present themselves in the best light? Being a little bit less transparent makes it a easier to do that.

MEL: I don't think I have a way to put this in the document right now. But there was a diagram that got drawn on a whiteboard during the analysis for this. And like a story pattern that -- last time [in your second interview] we talked about the children's book version. But --

TERRI: Yep.

MEL: But the story pattern, we heard across multiple interviews of PyPI in this case, but I don't think necessarily unique to PyPI. So, if it was a graph of time on the X axis and then progress towards completion on the Y axis. It was -- it starts steadily rising. Things are going well and then at like the 90% mark, they stall. Stall. Stall. 

And one of the things that happens during that stall sort of behind the scenes is it's just flatlining for some time on that last mile, and this is where some of the stories, especially with what some of the upstream folks were talking about. 

They went, oh, shoot. We need money. Oh, yeah. Okay. Can someone write the Mozilla grant proposal? Yeah, we need to hire people. Wait, what do we do? 

So, that flat line, that stall is the point where it's -- which number is it? Number four. The bureaucratic and organizational work or the infrastructure for that stuff suddenly kind of gets shoved in at the back end of realizing, oh, we need a project manager. Okay. Who can be a project manager?

TERRI: Yep.

MEL: Whereas for corporate projects, not necessarily open projects, but for corporate projects, you don't get the project manager involved when the development is 90% done. I think. You don't start drawing up budgets when the product is almost ready to launch. 

So, I mean, not necessarily they would be there from day one. They do start a side project, things start with demos. But the point at which that sort of organizational infrastructure would appear in a project would be earlier than it seemed to be happening in the PyPI story.

So, that is one of the things that we thought we were seeing. So, I want to kind of cross-check that with you and see how that felt.

TERRI: So, when I see a project stall internally, and they always do stall around the same 90% point, is when there's any kind of friction. And so, in our case sometimes the friction isn't the lack of procedure, but the existence of procedure. 

So, we have an inordinate number of projects in my group that are almost ready to be open sourced. Small security projects we're talking about here. Are almost ready to be open sourced, but we're waiting on naming approval or we're waiting on -- usually license compliance we're pretty good at. But we're waiting on something in the bureaucracy. 

And it's sort of -- for some of them, I mean, again, because these are the smaller projects that I'm looking at because we have been looking at what the procedures look like. I've had a couple that when they get to the security point, that's the point at which they realize they could use a project manager. 

So, yeah. I don't know if that's the fact that I work in an open source department where people are allowed to just sort of start whatever and scratch an itch that's -- so, we work really very much like an open source department until you have to release. 

But, yeah. I guess -- I think the pain points are different. But I think that getting to 90% and not quite finishing the last mile is a thing that happens everywhere.

And maybe it's a -- maybe it's just the way software is. Because it's really easy to get to an 80 or 90% solution for a lot of the problems we do. I mean, that's -- one of the things I have had to review a lot is parsers. It's easy to write a parser that looks a the 80% of things. But it's hard to write a parser that parses 100% and is safe. And we see a lot of solutions that it’s, “hope we can fix this at the end,” and nobody ever did.

MEL: This I think begs the question --

TERRI: I guess, I guess -- I mean, I guess really here, the interesting part is that infrastructure has a pain point that's different than software. Like, at software, the pain point seems to be the point at which your beautiful, elegant solution was no longer elegant and there's a bunch of bugs you need to do. Or there's a rewrite or there's, you know, a bad assumption you made in some data structure and you would have to refactor a bunch of stuff. Whereas for infrastructure, it's more likely to get to the point where, oh, crap, we've got too many users. Oh, crap, we need money.

Like, I guess I feel like the problem is the same, but the point at which we stopped -- and the point at which we stop is maybe even the same. But the reasons are a little different. 

I don't know. I guess that we could equally have said, you know, PyPI stopped at the point where it probably needed a refactor and yet we're doing the weird thing with the table scraping and stuff. And maybe... maybe they’re interrelated more than they're not.

MEL: And it's also relative to, is it in response to users' demands or load? Or is it because these features aren't present? But why do we need the features, right? Because we have more users now. So, they're not independent of each other.

TERRI: Yeah. And users are doing it differently than what was expected. The setuptools are making use of what was there to do the downloads instead of being pre-planned.

MEL: Right. But also to kind of go back to Jackie's statement in the beginning. One of the differences between infrastructure and non-infrastructure software is with infrastructure, you're the one that's flipping the switch for users. With non-infrastructure, maybe need a new version that has the patch in it. But if you get it out tomorrow, some users will switch over tomorrow. Some users will switch over next week, some users three years from now when they look back. Some users will never switch.

TERRI: Yeah, I guess when infrastructure fails, we all fail together. When software fails, we don't have to.

MEL: Yeah. It's a blessing and a curse both. This is really helpful, by the way. I appreciate you poking holes in all of this and going, huh, that's not actually -- because it's been a little bit too nice and neat. And this is my answer. Now I get to go back and go, ah! We need to redo the analysis.

TERRI: Well, like I said, I don't think the analysis was wrong. I just think some of it is people projecting wishful thinking on places they can't see.

MEL: But, yeah --

TERRI: I want to believe everyone plans these things. But I think -- I mean, there's a reason we have agile now. It's because we realized that nobody is actually good at setting requirements all at once in the beginning.

MEL: Yep.

TERRI: And I don't think that's -- yeah. And there's a reason we have 500 different flavors of agile is because none of them actually work every time for every team for every project.

MEL: So, it's kind of an engineering thing. We like to, you know, try to solve problems once and for all. But that's -- that's not how problem solving generally works. Like problems don't get solved that way.

TERRI: Well, and we saw that even with -- we saw it even with PyPI, right? All of us who worked in the trenches thought, it's magical! It just works, right? We assumed that everything was planned and beautiful because we didn't look under the hood. 

And so, maybe that's true everywhere. If you don't look under the hood, you just sort of assume that it's gonna be done the right way and maybe nobody ever does it the right way.

MEL: So, I want to make sure you get to see the last to things also. And they are sort of aggregates of what people said were their personal definitions of being well-maintained and being sustainable. So, I'm going to put the well-maintained list into the document right now.

TERRI: Awesome.

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

MEL: I forgot to number this also. There we go.

TERRI: I'm torn between hoping that we all have the same definitions and hoping that we all have completely different ones. Did I lose the document? There it is. Oh, this is such a great list. I love it.

MEL: Anything missing? Anything strike you?

TERRI: I really wanted to think of one missing thing, there could be ten. That's a terrible reason [to think of one more thing].

MEL: Any -- any thoughts or edits or recommendations or things that you notice about this list? And then I'll show you the sustainable one.

TERRI: The thing that I notice about this is a lot of it is about communication that makes changes. So, you know, there are people to communicate to, is pretty much what's happening in number one. Those people are listening. 

Best practices is a little bit less so, and backwards compatibility. But the review process is a collaborative thing is basically what we're looking for. Again, the process is pleasant. It feels collaborative. That people are trying to communicate outside of their -- their little existing niche, getting a wider variety of contributors. 

So, I think a lot of that is -- instead of striking, I guess, that only a couple of these things are technical issues, right? Like backwards compatibility is a technical issue. And I guess we can talk about the -- maybe whether updated means releases or not. But like, backwards compatibility is the only one that's not humans talking to other humans. Backwards compatibility and best practices, I guess. Which, you know, software is for humans. So, that makes sense.

MEL: Yeah, it is. Sometimes we don't emphasize that enough. I'm going to send you the sustainability one. Also make this a numbered list. There we go.

> _Source(s): notes-11-10-2019.md_
> 
> 1. There are resources (donated services or money to pay directly) for ongoing operating costs, including computing resources, people for operations, people for development, and people for “management.”
> 1. Resources needed for the project will continue to be provided in the future.
> 1. The “bus factor” is high (i.e. many people would have to vanish before there were problems.)
> 1. Sustainability relies on maintainability; what is the overhead to the project continuing to exist in the world?
> 1. Continued improvement of maintainabilty; keeping a project “up to date”
> 1. Computing resources, either donated or via the fiscal means to afford them
> 1. Interest in its existence from users (“existence sustainability”)
> 1. Sustainability is a sort of artifact of people and an extension of their time; do people have enough time to dedicate to this, or are they spread too thin?
> 1. There are new people onboarding.
> 1. There are entryways for people to onboard.
> 1. Maintainers are not burning out in silence. (Terri's note, added later: not just about burnout; might be about communicating handoff responsibilities)
> 1. Contributions are not bottlenecked at one person, a single point of failure, with no clear pathway to engage the community otherwise.
> 1. Various people taking on roles, not just one person.
> 1. Sustainability is hard to define with numerical metrics; you can try to count how many PRs there are, or average time for an issue to get fixed, but there are always more complicated reasons than that. 

TERRI: Ah, the bus factor is in there. Oh, I like number 14. That is -- that is definitely true.

MEL: That's --

TERRI: [At work] we have tried so many metrics to estimate sustainability out of GitHub repos. And, yeah. [The result was that none of the metrics we tried really gave clear predictions.] We don't know. [That was] an unsurprising, but disappointing answer, I guess? If that makes sense? We wanted it to be a thing that you could get out of the data. But...

MEL: And anything that you would want to change or edit or feel is missing from this list? There's some overlapping phrasing. Some, you know, different angles of the same thing. For instance, for me, number three, the bus factor, and number 13, taking on roles. They're very similar.

TERRI: Yeah. That is definitely pretty similar. The thing that I don't see is like there's -- I guess it depends on how you consider resources. Like, there's number 11 is maintainers not burning out themselves. But it doesn't have to be "Burning out," right? It could equally be someone got a new job and needs to let someone know. Like, it doesn’t have to be a burning out problem.

MEL: Okay.

TERRI: Or someone got a new job or has a new kid and maybe just doesn't realize that they needed help. So, I'm not sure I would say that burning out is the only issue there.

MEL: Maintainers are unexpectedly decreasing their contributions?

TERRI: Yeah, well, just time and effort, resources. Don't have to be about burnout I guess is really the only thing I would add.

MEL: Okay. I'm going to make a note of that in here.

TERRI: Yeah, I'm not even sure if it's just true of maintainers. Maybe it's more -- like when you say resources -- number two, resources for the project will continue to be provided in the future. 

If you're talking about human resources, that would mean that there will be someone who steps in if you get sick as opposed -- or get a new job or start a new project or whatever. I don't think all the reasons for -- for the human resources to decrease are necessarily bad things. It's just life. Life happens a lot.

MEL: Okay.

TERRI: So, maybe -- I mean, number 12 talks about not having things bottlenecked. But maybe -- maybe something about people communicating handoff responsibilities as needed.

MEL: Hm. Okay.

TERRI: I feel like that sort of is captured in a lot of the other ones. But it's not explicit that it doesn't have to be a burn out situation.

MEL: I'm taking notes on that. It's in the transcript. But I also want to make sure that gets into the list. So next time we sit down with the analysis part -- cool. One of the other --

TERRI: Because, I mean, the biggest maintainer change for Mailman was not about someone burning out. It was about Barry deciding to do some new things. So, and he just made sure we knew at the right time. And that's what made it so sustainable. He could have just taken on a new job or, you know, not mentioned that he was looking -- when he was looking for a new job or that sort of thing.

And similarly, like because -- because the core group knows each other well enough, I usually know [when people have time]. You know, I know when I'm gonna be able to get help from Steven and when he's got grad students finishing their thesis and is never going to be able to answer my question. 

So, some of that is just core team communication includes the soft skills part of things. I don't even know how you would say that. But for us, a lot of the maintainability is just in the quiet -- a quiet head's up, hey, I'm buying a new house or whatever. Can you keep an eye on these bugs for the next, you know, foreseeable future or the next month or whatever?

MEL: That's sustainability or being well-maintained? Or both.

TERRI: I guess both. I mean, sustainability is being able to do that hand-off regularly. And obviously. And I think that's -- that's really in number 12, right? Like that wouldn't work if we hadn't been careful to not bottleneck things. But it also wouldn't work if we didn't communicate when a bottleneck might happen otherwise. And, yeah, probably well-maintained again is -- well-maintained really covers a lot more of the communication stuff.

MEL: And there are other things that I noticed between those two lists that well-maintained, people seemed like, oh, well, this and that and the other. And I have kind of a list. And then sustainability was a little more like, um. Here are some things. But I'm not --

TERRI: Here's some thoughts. And then maybe well-maintained and sustainable are subsets, you know? It can't be sustainable without also being well-maintained probably is true.

MEL: Yeah. So, number five was interesting. That was an explicit statement of relationship of sustainability means continuing to keep a project well-maintained.

TERRI: Yeah.

MEL: I'm looking at the time. We're kind of coming to the end of it. This is what I wanted to show you. That was all I had. Anything about digital infrastructure, sustainability, that you think is important to share for this that we haven't talked about?

TERRI: Just pulling all those together. It seems like knowing what's going on is one of our bigger gaps. So, back up into it. We, you know, magical plumbing section there. We don't always have the data to plan what we're doing. And we don't always know what we're doing in advance. And, like... I guess there's a lot of related issues in there. 

But I'm wondering if maybe the final sustainability isn't necessarily about knowing any that have stuff in advance. But in communicating it when it matters. And being able to get the resources when they matter.

MEL: Yeah. Because I remember in the first interview we did, you talked about how keeping up with all the information was a challenge. Trying to work that up against what you said there. You know, knowing what's going on. Or having that not be the gap. But at the same time, not just overwhelming people with information that they're not going to actually read.

TERRI: Yeah, we've seen this a lot in open source in general. That, like, we discover -- discover? Suddenly the world knows that open SSL is two people who aren't being paid for it. Suddenly the world knows that PyPI was one guy who needs a new job. 

I'm not so sure we ever could seed the information where everyone would know this all the time continually the way like, as I said -- one of the ways that maintenance of sustainability works for Mailman is there's maybe a dozen people involved. And we know each other well enough to sort of keep a bunch of these things in the back of your mind. But I'm not sure that's possible or desirable at a bigger level. 

And maybe we just need to find a way to make sure that people know what they need to know when they can help. And maybe we should stop being surprised that that's the only time we know. Like, you know? 

If everyone ignores anything that isn't a call to action, then everywhere is just going to push call to action after call to action. 

And maybe we just shouldn't be surprised that that's happening. We've got our terrible, you know, engagement algorithm of the modern political and social scenes. And that's the way it is.

MEL: Yeah.

TERRI: I don't know if I feel comfortable with that. I feel like it would be nice if we had big overlapping groups of friends that could spot things before it becomes a, oh, crap, we all need to band together to solve our infrastructure problem before everything falls over and our language is dead. 

But maybe in practice -- maybe in practice that's just -- that's what sustainability means. Is somebody knows in time to put out the call when we need to put out the call and there's enough people ready to answer when this happens.

MEL: That's kind of like, why do we have fire stations or fire departments? Fires happen. But now we have trucks.

TERRI: Yep. (laughs) 

MEL: Okay. Anything else you can think of?

TERRI: No, I'm thinking about this implication for security and it doesn't look good for my job.

MEL: Cool. One last question from my side. What has participating in this research project been like for you as an experience? And especially if there's anything that we should keep in mind if we do this with other open source projects for people in the future? So, what has it been like to participate in this?

TERRI: Well, I have to say that this is actually been a boost for me professionally. Because I had people come up and ask me about the state of where has -- and about the state of code signing and a bunch of stuff that we had talked about in the course of the three interviews. Coincidentally. 

So, the fact that I could answer that we had, you know, this hardware and this grant open and, you know, all of these things. Actually, really great for me. Because it makes Python look super-organized. 

So, I actually gave my coworkers who asked these questions the impression that the Python Software Foundation is like totally on the ball in its plan for all the infrastructure and of having more information. So, that was actually kind of cool. I don't -- I don't know that's a thing you can plan for. But it was pretty cool for me that having a little bit more information about what was going on. 

And I would say that thinking about maintainability and sustainability and communication and all that have stuff is always good for my job because the ties between security and maintenance and sustainability are very, very tight and people want to rely on metrics for security that don't include any of this. 

So, I think having -- like having these lists that we just talked about. So, the next time someone says, well, I want to know if this is gonna be secure in 18 months I can say, well, look, here's a list of what other people think sustainability and maintenance is. None of this is stuff we're going to get out of our GitHub metrics or the CBE database.

So, you know, I think it sort of helps drive home the challenges that we have in this attempt to make software more data-driven when some of this is data that you can say with privacy and stuff, some of this is data we wouldn't to want to gather. I don't want everyone to know when I'm going to be bad at fixing bugs. I needed friends in the community to know. But I didn't need the entire Internet to be privy to, you know, the details of what date was defending my thesis, for example. Whereas I totally gave Florian the heads up on that stuff when we were maintaining Postorius together.

So, yeah. I think it's forced me to think about it in deeper ways. And it's given me a toolbox of other people's opinions that sort of agree with my own. I think we are all headed in the same direction. But look at it from perspectives that I just don't, right? I look at everything through a security lens lately.

MEL: Right. It's quite a few things. So, that's fair.

TERRI: Yeah. So, it taught me things and taught me things in an incredibly timely manner.

MEL: I'm glad that was, you know, the side effects weren’t planned on our part. But I'm glad it was helpful. And this has been really helpful talking with you getting your stories and your opinions and poking at the preliminary analysis. Thank you so much for participating in this.

TERRI: Yeah. This has been really interesting. And really fun, actually. I -- I now do want the children's book of how it got to be PyPI. I wouldn't have heard all of those stories otherwise.

MEL: Yeah. Well, we'll keep working on it and finishing up the last round of interviews and then we'll be getting together in November to do an analysis deep dive. So, I'll make sure to send people a summary of what's going on so if you're interested you can keep track. 

And also we have a small honorarium to thank you and the other people who participated. So, once we figure that out with the accounting people at our university, we --

TERRI: Yeah.

MEL: We will probably reach out and say, hi. We have money for you.

TERRI: That's fine. Yeah. I -- I look forward to seeing your final results. And I hope you can get some interesting papers out of this. Because I think this is -- I don't know what conference you take this stuff to. But I have seen people ask about this sort of information before and there's not a lot of academic resources. So, I hope this is going to be something people see.

MEL: Me too. And if you have any -- if ideas come to mind of where to send that to you, let me know because I'm also looking around my field and going, actually, I don't know if this goes here. So, but, you know, we'll do the analysis first and then see what happens.

TERRI: Yeah, no, that's -- I mean, I know we want it in the security conference if you gave it a security spin. There's got to be like software maintenance conferences closer to what you're already looking at.

MEL: Yeah. I might ask Jackie about that. I think that might be more -- but we'll see. Okay.

TERRI: Yeah, really cool. Thank you for including me in this. I'm glad I was able to participate.

MEL: Me too. All right. Thank you, Terri. Have a wonderful weekend.

TERRI: All right, bye, bye.

MEL: Bye.
