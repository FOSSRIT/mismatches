# Copyright transfer statement

MEL CHUA hereby irrevocably transfers and assigns to NICK COGHLAN in perpetuity, all right (whether now known or hereinafter invented), title, and interest, throughout the world, including any copyrights and renewals or extensions thereto, in the attached transcript of the interview recorded between us on OCTOBER 24, 2019 in A LIVE-TRANSCRIBED ONLINE VIDEO CHAT.

#License

I, Nick Coghlan, hereby release this work under the following open license: http://creativecommons.org/licenses/by/3.0. Anyone is free to share and remix the work as long as they cite it. I consent to the open publication of this work using my name.

# BEGIN TRANSCRIPT 

NICK: Ready for transcript start. We'll see how the audio goes.

MEL: Okay. So, this is the third of three interviews and every time we chat, you tell me more stories I didn't know about. (laughter)

What I wanted to bring to you, this round, is some of the preliminary analysis we have across all the stories, actually, and see if -- what you think of some of it. Which could be -- 

NICK: Most of -- oh. 

MEL: So, this is not part of the analysis, it's a little bit of -- I want to walk you through a little bit about how we starting thinking about it. 

NICK: Yep. 

> _Source(s): Jackie-1_
>
> JACKIE: As a user of other packages, I never really looked at sustainability because I always looked at it as, well, if this doesn't continue or this somehow fails, I can fork it. In the worst case, I can fork it and fix the things that I need to fix to make it work.

MEL: And so, we're trying to make two types of distinctions here. One is, you know, we're looking at open source digital infrastructure. There's the -- what difference does it make in open source. Both legally and culturally. And then, what difference does it make that it is infrastructure as opposed to some other kind of software project. 

And, so, in terms of this in the Google Doc where she talks about infrastructure verses non-infrastructure software. 

NICK: Uh-huh. Yep. Yeah. I mean, to add to what Jackie says there, with the -- the idea of you can fork it and fix the things that you need to fix to make it work, it's almost always the case of -- you can usually find a workaround to avoid the bit that's broken while still using the stuff that's fine. 

And particularly, in Python, because Python allows monkey patching so heavily, I've literally had software that reached into bugs -- reached into other libraries, at startup, and replaced functions with fixed versions, when the application started. (laughter).

MEL: I had not thought about that implication. But, yeah, you're right. 

NICK: So, yeah, it's -- it is very much the case, especially in -- in languages like Python, like JavaScript, where you do get into that mindset of, hey, look, even if there is a bug, I have so many ways to work around it that -- (laughter). And, yeah, you get into this mind set of, "I'll deal with that if I need to. Otherwise, I'm sure they're fine."

MEL: Well, but with infrastructure. 

Infrastructure, you're forcing users deal with what your decisions are. They can't work around it and say, oh, I guess I'll patch my version of PyPI because they don't have one. 

NICK: Interestingly, you say that, but it's not actually quite true. And this is one of the things where, for a very, very long time, an answer to people having reliability issues with PyPI, with just, like, going, "well, hang on, what do you mean you're downloading dependencies live from PyPI into your continuous integration? Why aren't you running your own package server and selectively pulling stuff from PyPI into that?"

And, because that was the thing of, like, well, hey, you got to do due diligence and review anyway. So, the critical bit of infrastructure should be your packaging server, not the public one. 

And then, of course, the reality is relatively few organizations even run a caching proxy in front of PyPI. They can stream directly from the public service. (laughter). We wouldn't have the downloads we do if they didn't. 

MEL: I mean, I know that there are some places that have the internal repositories, but by and large and certainly for individuals, when they say, I think I'd like to write some thing in Python. They don't do that first by setting up their own -- 

NICK: Yeah, exactly. 

MEL: So, in thinking about, like, infrastructure, versus non-infrastructure software, there's a difference there. And it's a difference whether it's open source or closed source. 

NICK: Now that I think about it, the key thing that's there is that if it's a library, the skills needed to work around it are developer skills. If it's infrastructure, the skills to work around it are sysadmin skills because you have to run a service in front of it that decouples you from the reliability of the public thing. So, yeah. 

MEL: That's a good point that I don't think anyone has explicitly said yet, so thank you very much for doing that. 

So the next thing I want to show you. If there's a difference when it's infrastructure, what's the difference if it's open source or not? 

> _Source(s): notes-2019-10-11.md_
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

NICK: Just reading. So, this is actually one I've spent a bunch of time thinking about. And while I do think this is broadly true, I also think there's an aspect around who the FOSS contributors are. 

And, the PyPI story -- I was thinking about this. “No, no, I've told you all my stories.” It's like, no, I haven't. We have more. (laughter).

Before the fastly CDN came in, there was a previous effort to set up a mirroring structure for PyPI. I don't remember the PEP number at the moment, but if you look for it in the list, it'll come up. 

Now, this proposal was kind of based on similar systems that were in place for Linux distros and I think potentially for CPAN, the Perl Package Network.

The interesting thing was, that it just straight-up didn't work. Whereas those other mirroring systems have been working happily for decades, in some cases. 

And so, I was like, going, okay, what's different here? Why hasn't this worked when those other ones were able to be successful? 

And I think it relates a lot to community structure and that thing I was talking about earlier with whether your volunteers are mostly infrastructure people with system administrator skills or mostly developers with development skills. 

And, if you look at something like a Linux distro community and all that other sort of stuff, and even Perl, I think they skew far more heavily in the direction of infrastructure people, and in particular, university admins. 

When a lot of that infrastructure for Linux distros and Pearl was coming up, you had this combination of Linux system administrators, who had access to hardware and systems to let them run public internet services, and, B, a working environment that gave them relatively-broad authority to dedicate university resources to that purpose. 

Often, because the university, itself, needed them. And so basically, the university needs the capability and the university had no problem with making it publicly available, rather than restricting it to university staff.

And so, you were able to set up these mirror networks and quite often, anchored by either Linux vendor -- sorry, not Linux vendors. Sometimes Linux vendors. But by universities and by internet service providers. 

And this was a case of folks making those things -- needing to set up that infrastructure because they needed it, but also being in a situation where they could say, well, I'm just going to make this available to the world, at large, so anybody who needs it can access it if they're closer to me than they are to the original upload server. 

And so the thing, then, with when we were trying to set up the PyPI mirroring, is that it was now 10 to 15 years after a lot of these other systems had been put in place. And, I think we had a user base that was less sysadmin centric, proportionately, there were few people -- 

but I think, also, being 15 years later, I'm -- I think a lot of universities were just genuinely less free in the way the sysadmins manage their infrastructure. I've got a -- I suspect sysadmins today have a lot less freedom than the ones 20 years ago did to say, hey, we're going to devote university resources to this. 

And so, yeah, and so I think something -- and so even though we were trying something that had worked before, the situation around us had changed enough, since those other systems were set up, that it didn't work for us. 

And then, fortunately, Fastly was able to come in and say, hey, we're going to -- we're going to offer you this as -- essentially advertising and contributing back and things. 

So -- but, yeah. It was a huge boon and it worked where the mirroring-based approach hadn't. So... anyway. So, that’s story time for today. (laughter)

MEL: That's fascinating and I think one of the ways to check that hypothesis -- I'm not sure if my team will have the bandwidth to do this, but looking at other projects that were trying to do, the package distribution type thing, at the same time as PyPI, if they ran into similar, the same problems. 

NICK: Yeah. I think the big one to check would be Ruby Gems because NPM is a completely different case because it's a proprietary company. They pay their own bandwidth bill, they pay for their CDN. Whereas Ruby Gems, I think, is much closer to the PyPI case. I'm genuinely not sure how their mirroring works. 

MEL: I don't know, either. And I don't know how the timeline compares to -- from my perspective, it seems like they came up at the same time but I'm sure that's not true. That's just when I became aware of them. 

NICK: The languages, themselves, are both early to mid-90s, I think. So -- but, yeah, the distribution -- yeah. Ruby Gems, I've got a feeling, was around 2010-ish, maybe a bit earlier. But that might just have been when I became aware of it, not when it came into existence. 

MEL: So, when you look at the Google Docs with the FOSS versus non-FOSS, I think it's a subject that's a very rather -- when we say "FOSS," do we mean legally or do we mean culturally? I'm more thinking culturally. So, you could substitute in non-corporate or, you know, grassroots-driven perhaps. 

NICK: Yeah. 

MEL: But it's kind of great to look at. Taking number one, the difference between FOSS and non-FOSS infrastructure. How do you feel about that point? Does that seem -- 

> _Source(s): notes-11-10-2019.md_
> 
> 1. Infrastructure is “magical plumbing.” FOSS infrastructure lets you look behind the curtain if you so choose; non-FOSS infrastructure likely does not.

NICK: I think that's very true, because even -- like, even if -- even though we don't let you look at all the operational secrets of PyPI itself, you can go look and say, oh, here is the Warehouse project. Here are the scripts and the infrastructure we to actually run it. You can't go look at the Fastly CDN code, but you can look at our integration scripts. You can go look at the -- what's it called? The name -- linehaul, the project that scrapes the Fastly logs and pushes the data over to BigQuery for all the downloading information. 

So, yeah, it is the case of, no, you can't log in and access the servers. Yes, you can go look at all the code that runs on those servers. 

MEL: So, looking at the second one -- the first one is probably the most clear difference between FOSS and non-FOSS. 

Looking at the second one, we're starting to make stronger claims -- not claims, hypotheses. If any of them, you're like, no, I think that's bullshit or the wording's wrong, that's exactly why I'm putting these out and going please fix them. (laughter)

> _Source(s): notes-11-10-2019.md_
> 
> 2. Infrastructure requires technical effort for operations (as well as development). FOSS infrastructure may begin as a pet project and then “accidentally” go into production; non-FOSS infrastructure is more likely to be deliberately planned as a product launch.

NICK: Um -- I think point two is kind of true. 

I think point two is true if we're talking from the point of view of outside the organization providing the service. I think it can happen, rarely, but it can, where companies can build internal infrastructure because they need it. And, then -- and then essentially, the deliberate planning into a product launch phase comes after the -- so, it's the case of they built it because they needed it and then they go, ah, we can totally use this. 

And then they go, hey, this is actually a business opportunity. It's sufficiently well-aligned for us to be the right people to pursue it and so they reshape it into a product launch.

Most famously, Amazon Web Services. So, there's -- so there's a myth -- there's a myth that says, ah, that AWS was Amazon selling spare capacity on their own internal infrastructure. That part is a myth. The part that's not a myth is that AWS was born out of Amazon looking at their own infrastructure going, hey, we can sell this. And so AWS was conceived as a deliberate product launch. But the inspiration for that product launch was the way Amazon.com was operating. 

MEL: Yeah. So, the distinction that happens with PyPI that did not happen with AWS. Amazon did not wake up one day and say, oh, my God, this AWS we started as a thing for us, suddenly other people are using it! Lots of them! For production! That didn't happen. 

NICK: No, that's right. That's the -- what does happen, though, is inside a company, you can set up a service for say, your team or whatever, and then you're using it happily and then if you're not actively monitoring it, it might go down and some production system can be relying on what is under your desk. The difference is, you don't see that from the outside world. 

But, yeah -- but -- and that gets back to that first point, which is that inside a corporation, all of that stuff happens inside the firewall. People assume it's happening, but don't see the messy details. And so -- so, yeah. 

MEL: How about the third one? 

> _Source(s): notes-11-10-2019.md_
> 
> 3. Infrastructure requires development capacity (people-time). FOSS infrastructure is likely to have some or all of this development capacity come from self-directed volunteers, but that effort is also more likely to fade out during the “last mile.” Non-FOSS infrastructure is more likely to have its development resources known, managed, and allocated in advance.

NICK: If we're talking about the cases where the non-FOSS infrastructure is actually a commercial service, yeah. I'd agree. Commercial service or fully-structured -- organizationally-run thing with budgets and known resources and, yeah. 

So, yeah, it's -- the distinction there's not necessarily FOSS versus non-FOSS. I think it's more when people talk about community-run versus organization-run.

So, if you look at something like the OpenStack Foundation, for example, or even the Linux Foundation, for that matter, the OpenStack Foundation has a lot of money. They run and so they provide a lot of the infrastructure for OpenStack, as a project. So that is all completely FOSS. But, a heck of a lot of it is run by people who are being paid by either the OpenStack Foundation or OpenStack vendors and so, yeah, there's a lot of -- yeah. 

MEL: So, that actually relates nicely to some of the things that -- the stories you were telling me earlier. Some of the stories that I think you've been telling me are PSF, becoming more of that organization and saying, hey, now we have money, we're going to hire Ernest and we're going to have people paid to do this.

NICK: Yeah, and it becomes the case of, you're not relying on people volunteering their evenings and weekends. You're going, no, no, no, this is your job. This is what we pay you to do in business hours. Your evening hours and weekends can go back to being yours. So, yeah. Yes, very much that. 

MEL: This is -- so this is a very leading question. (laughter)

Is that the only way that this can happen? Is that sort of inevitable that if we want to have that kind of infrastructure, then, well of course you've got to have an organization -- you have to have something with resources, to allocate them?

NICK: Yeah. My answer kind of boils down to humans gonna human. (laughter) So -- so, it's -- so, it's -- it's the case of, we still live in the world we live in and so, if we want to be able to devote people’s times to things, they still need to pay for food. They still need to pay for somewhere to live. 

And, the two main organizing structures, the world currently offers for that kind of thing, three, I guess, but -- is corporations, nonprofit organizations and governments. 

The idea of having governments run key open source infrastructure is not a popular one for all sorts of reasons. So, that pretty much gets you back to corporations and non-profits. (laughter)

So -- and, yeah, and then -- and then that structure -- I personally genuinely like the structure of, you have solid core nonprofit organization that is a true nonprofit to protect the interest of the volunteers. 

And then around that, you have an ecosystem of corporations that are monetizing what's there to be monetized and then feeding that back as a supply chain management activity. 

There are lots of folks who have serious problems with that style of organizing. I have problems with trade associations that call themselves foundations. 

But, the -- but at the same time, that is a -- it is a case of that basic model of having the core -- the core community-run setup that is there in the interest of the volunteers and nonprofit contributors and then the corporate world around that is not bad. 

And also gives you that point of actually being able to communicate effectively with governments and potentially get them to give you some money, so... 

MEL: There was a thought that came to my head and it dropped right out. Skipping on to number four, then. If it comes back, I'll let you know. 

NICK: I just did think of one thing, which is folks tend to have lots and lots of objections to government control. Many fewer objections to government money. (laughter)

MEL: Okay. So, point four? 

> _Source(s): notes-11-10-2019.md_
> 
> 4. Infrastructure requires bureaucratic/organizational work. FOSS infrastructure is likely to have this set up late, during the “last mile” or the “sticking point.” Non-FOSS infrastructure is more likely to have this infrastructure (legal, organizational, financial, managerial, marketing, etc.) be set up early.

NICK: Um -- yeah. Yeah. So, I'd agree with that. Yeah, in the non-FOSS case, it's -- yeah. Either set up early, using the infrastructure of an existing organization. But, yeah. Yeah, I'd agree with that. 

MEL: And I think that this is another place for the distinction between FOSS -- FOSS or is it, like -- organization --

NICK: Yeah. Again, this is one where I think the distinction may be less FOSS versus non-FOSS and more commercial versus non-commercial. 

Because again, if you look at something like the Linux Foundation or the Open Stack Foundation, they're actually trade associations and they just call themselves foundations, is that they're -- well, so, Linux Foundation is one that was bolted on later. 

But if you look at Open Stack Foundation, so, yeah, that came out of RackSpace and initially borrowing their legal and organizational structure and then RackSpace set up the foundation around it. Even though Open Stack is FOSS, in the process of making it open source, RackSpace actively sought to put a lot of that supporting infrastructure in place as quickly as they could, so...

MEL: Yeah, there's actually a diagram behind point four that I didn't have a way to put into the transcript, but it was -- if you imagine a graph, like, on one -- on the X-axis, it's time. On the y-axis, it's percent of project done.

And the narrative that you and Ernest and Donald told was -- some version of, well, it started and then things got defaulted and it was 90% done and then it stayed at 90% done for a really, really, really long time. 

NICK: Yeah, that's pretty much true. 

MEL: A long time of 90% done, and then we got it to done. And getting into the story of, okay, what the heck was happening during the long stretch of 90%. It's not that nothing was happening. It's that a bunch of that -- from a feature implementation or deployment implementation, nothing was happening because other stuff was happening.

That's the, oh, shoot, we need project management, let's get a grant to hire a project manager. And we should get some UX designer in here, let's get someone contracted. And so the bureaucratic infrastructure was being caught up, sort of. 

NICK: Yep. I think that's definitely true. I think the other -- I think the other thing that's interesting is that I'm not sure it's true, that the -- I'm not sure it's true that the commercial projects actually get to 100% done sooner. It's just that they all have commercial incentives that say, yes, we know we're only at 90%, we're launching anyway. 

Whereas in an open source context or a non-commercial context, you don't have that pressure to say, no, no, no, we have to launch by May, dammit! Whether we're ready or not, we're launching in May. You don't have anyone telling you, you shall launch by this particular date. So, if you don't think it's ready, you just don't flip the switch. 

And so -- but that, then, where, in this case, it was the -- the external impetus from the board side where Eric was going, hey, look! You've had this almost ready for years. What do you actually need to get it over the line? (laughter)

MEL: So, poking at that slightly actually, it depends on the way that open source project does its release management.  I actually don't know if that's different with infrastructure versus non-infrastructure. But like, every six months, like clockwork -- Fedora Linux releases another version regardless of whether they're ready or not. Or, well, the features that are ready are in, and the features that aren't ready don't get in.

NICK: Yes. 

MEL: The feature-based release cycles, yeah, they can get put off, go on forever. But I don't actually know if infrastructure projects are more likely to have feature-based rather than time-base. 

NICK: I mean, even in time-based releases, you can still hit that kind of ultimatum. One of the very earliest projects I worked on in the C Python codebase was -- I'm trying to remember who it was. I think it -- maybe Jeremy Hylton? Anyway. Someone had been working on -- someone had been working on an AST-based compiler for C Python and around the 2.5 time frame, Guido [van Rossum] said, look, finish it or we're giving up on it. We're not just going to have this branch sitting around indefinitely. And so, we finished it. 

So, there were a few of us that got involved and said, okay, what's the blockers? Let's sort all those out, get it merged and make it the compiler. 

And -- but again, it was that case of needing someone to say, no, no, no, you have a deadline now. If it's not done by then, it's not getting done. And so, yeah, sometimes you do need that external impetus to say, okay, we're actually going to do this thing. 

MEL: And in the case of PyPI, we were talking about Eric doing that poking of, "hey, what do you need?" How much of that was -- what kinds of things were influencing him saying that? Was it him going, "I am personally being affected by these outages, this is terrible"? Or, "people have been complaining to us? Lots of them?"

NICK: I honestly don't know. But, I mean, I think -- Eric's -- Eric's just a wonderful human being. But, I mean, he created Read The Docs. 

So, I think -- so, I think one of the things Eva did change on the PSF side is when new board members came in, she did more actively encourage them to say, well, okay, what are you going to try and get done? Like, what do you want to be different after your time on the board? So, I think that may have been part of it, that Eric went, well, I want to get this PyPI thing sorted. 

So -- but, yeah, I suspect he may also have just seen that it had just stalled from time and energy-type things and so -- that he knew some of this stuff was going on and just wanted to know, well, look, what is -- what is actually blocking further progress? So...but, yeah, that would be a great question to ask Eric. (laughter)

MEL: You're right. It would. I need to make sure he sees this portion of the transcript.

How about number five? 

> _Source(s): notes-11-10-2019.md_
> 
> 5. Infrastructure user data and usage patterns are important for determining future resource needs. FOSS infrastructure maintainers are less likely than non-FOSS infrastructure ones to have complete and reliable access to that data because of intentional cultural choices to prioritize user freedom and access over it.

NICK: Um -- I think that's true. Yeah. Yeah. Basically, I think it's true. I don't -- I don't think it's -- I think it's not just the thing about prioritizing user freedom. Although it is, that's definitely part of it. 

I think it's also the case of ultimately when it comes to getting things done, FOSS communities are very much about the situation of what can we get contributors to put their energy behind? And I've yet to -- I've yet to meet a volunteer that got excited by t”The spreadsheet data says this…” (laughter)

And it's like -- so, the -- so mainly, the -- mainly the -- where I've seen data actually used, in open source projects, is where people going, we want to do this thing, so I want to drop support for this version or I want to do XYZ. 

Then they will go look at the data to say, does the data tell me that doing what I want to do would be an astonishingly bad idea? 

And then -- and then if the data says no, then they might -- if the data says, yes, that would be an astonishingly bad idea, then they reconsider and go, okay, fine, I won't do that thing yet.(laughter) I'll do it later, when the data says it's okay. 

I've yet to see anybody go -- so, I've definitely seen people use data in the negative sense of, do not do that thing, it would be a bad idea.

I have yet to see anybody go, hey, we have the data that says this, okay, based on that data, I'm going to go do this thing. 

Because that's -- that's kind of mixing in the intrinsics rewards versus extrinsic rewards. 

If you've got a relatively -- if you've got a bucket of money and you're trying to figure out how to spend it, then that's when you start doing the, well, I'm going to use the data to tell me what I should be spending my bucket of money on. 

If you're going to -- if you've got volunteers, they're going to have their own intrinsic motivations of what they want to work on and it becomes the case of, okay, let's channel that energy in productive directions. And so, yeah, it's a lot -- it's a different way of using the data. 

So, I think -- I think it's the case -- I think the fifth point is right, as far as it goes. 

But I think there's also a thing of the different communities using data differently, which is the volunteer-driven communities, it's very much about you use the data to tell you when something would be an astonishingly bad idea and it's used in the sense of "don't do that." 

Whereas in a payment-driven system, it's more likely used in the sense of, can we define from the data what we should be doing? So...

MEL: Okay. Yeah. Anything else on those five points?  I promised I'd show you the definitions of what other people said about sustainability and being well-maintained.  And then give you a chance to say anything else you have before we run out of time.

> _Source(s): notes-11-10-2019.md_
> 
> Well-maintained
>
> 1. There are people there to triage and address issues that come up in a timely manner.
> 1. There are people to make sure a project is keeping up with changes in the ecosystem (ex: maintaining compatibility when dependencies are updated, etc.)
> 1. The project is following best practices regarding software development (tools, code style, tests, etc.)
> 1. The project cares about backwards compatibility.
> 1. The review process is clear. New changes can be evaluated effectively and merged if appropriate, and standards/expectations are clear to contributors.
> 1. The review process is pleasant; maintainers are friendly when contacted.
> 1. The project values inclusion and is visibly trying to be welcoming to a wide variety of contributors.
> 1. The project is regularly updated and has activity happening, AND this activity is fully and easily visible to outsiders.
>
> Sustainable
> 
> 1. There are resources (donated services or money to pay directly) for ongoing operating costs, including computing resources, people for operations, people for development, and people for “management.”
> 1. Will the resources needed for the project continue to be provided in the future?
> 1. The “bus factor” is high.
> 1. Sustainability relies on maintainability; what is the overhead to the project continuing to exist in the world?
> 1. Continued improvement of maintainabilty; keeping a project “up to date”
> 1. Computing resources, either donated or via the fiscal means to afford them
> 1. Interest in its existence from users (“existence sustainability”)
> 1. Sustainability is a sort of artifact of people and an extension of their time; do people have enough time to dedicate to this, or are they spread too thin?
> 1. There are new people onboarding.
> 1. There are clear entry points for new contributors so they know how to get started.
> 1. Maintainers are not burning out in silence or unexpectedly decreasing their contributions for some other reason (moving, new child, new job, health, etc.)
> 1. Contributions are not bottlenecked at one person, a single point of failure, with no clear pathway to engage the community otherwise.
> 1. Various people taking on roles, not just one person.
> 1. Sustainability is hard to define with numerical metrics; you can try to count how many PRs there are, or average time for an issue to get fixed, but there are always more complicated reasons than that. 

NICK: Yep. Oh, next page. 

There seems to be a duplicate in the sustainability ones. Ah, yeah, computing resources. There's one and six. 

MEL: Yeah, there's some overlap. These aren't, like, finalized. They're more like -- 

NICK: Okay, great. Oh, right. Aggregated. 

Yeah, I'd possibly move -- personally, I would probably move some of the stuff in "well maintained" into "sustainable." In particular, points five to seven. Because of the review process and the inclusion. 

MEL: Okay. 

NICK: I think -- five and six probably qualify as being under "well maintained" because it's a case of if you need a bug fixed or if you're trying to contribute a bug fixed, getting your own bugs fixed is part of being well-maintained. 

I guess it's more seven that the inclusivity is -- again, it probably falls under both because -- because again, it falls into that thing of well-maintained relates to "can you get your bugs fixed?" And if the project maintainers are assholes to certain kind of contributors, then for those contributors, it's not well-maintained for them because they can't get their bugs fixed. That actually is a sensible entry. 

Yeah, those three, in particular, also heavily influence sustainability, which I think -- yeah, the point of four, that sustainability relies on maintainability, if the maintainability is poor, that's going to then lead to users abandoning it because it's like, "maintenance is terrible. I don't want to use this anymore. I'm going to find something else." And if you get too much of that happening, people see decay, which can essentially turn into a death spiral. I mean, who uses XFree86 anymore, for example?  (laughter) [Ed: the XFree86 project was forked around 2003 over governance and maintenance issues, and became x.org]

So...

MEL: It's interesting to see who put what things in "well maintained" versus "sustainable." There's a relationship between these two concepts, but what falls on which side of the line is not a consensus by any means. 

NICK: So, yeah, it's the case of -- I think there can definitely be projects that are incredibly well-maintained for now, but they're very much single-person projects and it's just that that person cares a lot about the thing, understands it really well, keeps it working and for the vast majority of users, they never need to report bugs because it doesn't break, so the -- whether essentially points five, six and seven never come up. 

And then the other one is, as far as point eight goes, so, I maintain contextlib2, on PyPI, for the Python library stuff, and essentially it went two years without a release, but that was because we went two years without changing contextlib in the library, so there was nothing to backport and so, yeah, and so -- and I don’t think I would claim it's well-maintained. It gets touched occasionally. (laughter)

But -- but, yeah, it's -- but, yeah, it was a case of in the -- in the well-maintained thing, there's -- yeah. Essentially, there are -- there are projects where you just never have reason to engage with them enough to find out the answers to these questions because you just install them and they just work. 

And sometimes, it can be that the reason they install and work is because they're maintained by somebody who's super focused, super into it and making sure it all works and is a pleasure to use. 

But, it may not be sustainable because they're the only one, if anything happens to them, the projects kind of stop. 

So, yeah... oh, there's more. I missed that. I went over to the next page. Yeah. Yeah. And that's the -- 12 and 13, and that last point I was talking about, the -- that it's -- yeah. 

MEL: So, that's sort of the very, very early stage analysis. I wanted to let you have the last couple of minutes to talk about whatever else you wanted to make sure we knew about or that was brought up in the PyPI study, about PyPI, or something you think we should know or infrastructure sustainability and open source, in general. 

NICK: No, no, I think I've told you all my rambling stories, well, related to this anyway. (laughter)

Yep. Yeah, I'm just interested in what the timeline is for -- for the further analysis and publishing the study and that sort of information. 

MEL: Yeah. So, we're finishing up -- we've got two more interviews to do and then we'll have all of the data, so it will all be on GitHub.

And then in early November, myself and the other members of the analysis team, which includes Sumana, she's coming, and Shauna, who did the maintainers summit with Jackie at PyCon. Diving into the data over a long weekend and sorting out -- they've got context that I don't, being more involved in PyPI and Python. Making sure we're reading it together and making links the right documents and stuff. 

And also, thinking about in what form would this be most useful to the Python community. What kinds of write-ups would specifically be useful. 

NICK: Yep. 

MEL: Then we'll be taking the rest of November and December to just start writing out and sending out things, so you'll start seeing, like, "We think we found this! Maybe that!"

And then we'll see if there's interest in anything else, what comes next from there.

NICK: Cool! 

MEL: Oh, one thing that I did want to ask is, in terms of your experience with these interviews, what has this been like, is there anything we should know or improve or change in case we do end up having more bandwidth and do this again later with more PyPI people, more Python people, or maybe other open source communities?

NICK: Oh, so, the one thing -- the one point where I was genuinely confused was between the first two interviews, where I wasn't sure whether I was supposed to go read the other transcripts or not, or whether I needed to go read the other transcripts. And, yeah, I like the system where you provide the snippets that you want us to react to and that sort of thing. 

So, yeah. So, that was a lot clearer between the second two sets of interviews, knowing that the information you wanted feedback on would be provided during the later interviews. 

MEL: Got it. Thanks for that. I can be a lot clearer about that next time around. It's all public, so you can [read the transcripts if you want]. But that's a lot of information, so we're not going to expect you to. 

NICK: Yes, that's right. (laughter)

MEL: Cool. Definitely making a note of that for next time. Anything else? 

NICK: No. Thank you for doing this. This is a really interesting project. I look forward to seeing what comes out of it.
