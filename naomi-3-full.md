# Copyright transfer statement

MEL CHUA hereby irrevocably transfers and assigns to NAOMI CEDER in perpetuity, all right (whether now known or hereinafter invented), title, and interest, throughout the world, including any copyrights and renewals or extensions thereto, in the attached transcript of the interview recorded between us on OCTOBER 28, 2019 in A LIVE-TRANSCRIBED ONLINE VIDEO CHAT.

# License

I, Naomi Ceder, hereby release this work under the following open license: http://creativecommons.org/licenses/by/3.0. Anyone is free to share and remix the work as long as they cite it. I consent to the open publication of this work using my name.  

# BEGIN TRANSCRIPT

MEL: Yeah. So… Welcome to the third and final PyPI interview! Ready to start the transcript?

NAOMI: Sure!

MEL: Cool. So today -- the agenda for today is that we’re actually going to be showing you some of the very rough preliminary analysis that we’re doing.

NAOMI: Okay.

MEL: I’d love to get some of your reactions to that. And it’s very early stage. We haven’t figured out how to word all the things yet. So criticize away. Edit away. This is the… Here’s the strawman stage. 

And then after that, I’ve got some aggregated definitions of sustainability and being well maintained from everybody. So taking a look at that and seeing if we’re forgetting anything. 

And then the rest of the time will be yours to throw in anything else about Open Source digital infrastructure sustainability, that we haven’t yet looked at. 

So the preliminary analysis results are about five little bullet points. Do you want to take them all at once, or do them one at a time?

NAOMI: Oh, let’s do them one at a time.

MEL: Okay. Let me grab the first one. So as backstory for this, one of the distinctions we’re looking at is: What difference does it make that it’s infrastructure, as opposed to non-infrastructure software?

NAOMI: Okay.

MEL: And then the other thing we’re looking at is: What difference does it make that it’s FOSS as opposed to non-FOSS?

NAOMI: Got it.

MEL: And so actually, first, the infrastructure versus non-infrastructure bit… (pause) I’m gonna jump ahead to the FOSS versus non-FOSS bit. The infrastructure versus non-infrastructure was basically… Infrastructure can be this magical thing that you don’t think about. I think you brought up the plumbing analogy. It’s like your plumbing.

NAOMI: Right.

MEL: I don’t want to think about my plumbing!

NAOMI: Right, right.

MEL: So with that in mind, this is number one of five of what difference does it make that it’s FOSS. 

> _Source(s): notes-11-10-2019.md_
> 
> 1. Infrastructure is “magical plumbing.” FOSS infrastructure lets you look behind the curtain if you so choose; non-FOSS infrastructure likely does not.

MEL: There we go. 

NAOMI: Yeah, that makes sense.

MEL: It’s the most straightforward of the five. It’s like… Yes! The code is available. Because that’s one of the freedoms.

NAOMI: Right.

MEL: So the second one…

> _Source(s): notes-11-10-2019.md_
> 
> 2. Infrastructure requires technical effort for operations (as well as development). FOSS infrastructure may begin as a pet project and then “accidentally” go into production; non-FOSS infrastructure is more likely to be deliberately planned as a product launch.

NAOMI: I think that’s good. I don’t have anything more to say, but I think that’s a good summary of it.

MEL: Okay. That’s the third.

> _Source(s): notes-11-10-2019.md_
> 
> 3. Infrastructure requires development capacity (people-time). FOSS infrastructure is likely to have some or all of this development capacity come from self-directed volunteers, but that effort is also more likely to fade out during the “last mile.” Non-FOSS infrastructure is more likely to have its development resources known, managed, and allocated in advance.
 
NAOMI: Um… Mostly in agreement. I’m wondering about the phrase “the last mile”. I mean… When I hear “last mile”, I’m almost thinking it’s, like, specifically, say, from the bit that’s right before “the consumer of it” -- I’m just wondering if that’s what we really want to say there. That’s all. I mean… Since it seems to me that they can… (audio drop)

MEL: Can you say that last bit one more time?

NAOMI: It just seems to me that… That the resources can fade out at any point. And it’s kind of hard to generalize -- you know, it’s likely to be this phase or whatever in this. So that phrase strikes me as being maybe a little bit more specific. I don’t know. Just a thought.

MEL: Ah. Good point. So this one comes from… At least for PyPI, so we can’t really generalize to other projects yet… But this one comes from Donald and Ernest and Nick all saying something like: PyPI was at 90% done for a really long time. And it was almost --

NAOMI: Ah!

MEL: But it just wasn’t done.

NAOMI: Right, right, right. Yeah. I mean… I understand, then. Yeah. I don’t know if I would rephrase or not, maybe to… Before the project is completed or something like that. But I just… When I read it, I didn’t quite get what was intended. So that’s why I raised it.

MEL: I think they might be doing something outside my apartment right now. (chainsaw noise)

NAOMI: Ah.

MEL: If I can hear those noises, it means they’re loud.

NAOMI: I can just barely hear them.

MEL: Oh, that’s good. Yeah. And this is the kind of feedback that’s helpful, because… So “last mile” came from the upstream -- the PyPI developers, who were saying “last mile”, because I think that’s what happened with PyPI specifically. But you’re right. It doesn’t have to be the last mile. It could be at any point. Making a note of that. And this actually relates to the fourth one. So I’m just gonna put that in here. And discuss them together, maybe.

> _Source(s): notes-11-10-2019.md_
> 
> 4. Infrastructure requires bureaucratic/organizational work. FOSS infrastructure is likely to have this set up late, during the “last mile” or the “sticking point.” Non-FOSS infrastructure is more likely to have this infrastructure (legal, organizational, financial, managerial, marketing, etc.) be set up early.

NAOMI: Okay. I know what they’re thinking. I’m still not sure I’m entirely convinced. I think that they tend to have that bureaucratic organizational work done whenever it becomes absolutely necessary. And if that doesn’t happen, it doesn’t happen at all. If it happens earlier, it happens earlier. That would just be my take on that. Certainly in PyPI’s case, yes. I know what they mean.

MEL: And so… (audio drop) when you say (audio drop) when it becomes (audio drop) is that… [when you say that it only happens when it’s absolutely necessary, is that with open source projects specifically, or all software projects, corporate and non-FOSS included?]

NAOMI: Um… I wouldn’t say for Open Source… For Open Source stuff… Specifically… Yeah. Yeah.

NAOMI: What should I say?

MEL: Included…

NAOMI: It’s when it’s actually felt to be such a problem that we can’t make progress.

MIRABAI: (typing) My internet might be kind of wonky? I’m wondering if I should try to switch to hot spot? I’m on university Wi-Fi right now.

NAOMI: I’m not getting any audio right now either.

MIRABAI: (typing) Naomi seems pretty clear. Getting drops from Mel. But that might just be bad luck. Can try to switch to 4G if that would be helpful.

NAOMI: I’m getting good video from Mel, but not getting any audio.

MEL: (typing) Are you still not getting any audio from  - I am going to drop out of the call and then back in.

MIRABAI: (typing) Not hearing anything from Mel right now at all. Naomi is loud and clear.

MEL: Open Source cultural thing? Like the bound to which that statement (audio drop)

(Mel restarts her video conference connection)

MEL: Okay. Is this any better?

NAOMI: Much better for me.

MIRABAI: Me too!

MEL: Okay. Sweet. Yay! Sorry about that. So the question I was asking was: The statement you made earlier about this kind of organizational infrastructure tends to happen only when it’s absolutely necessary. What does that statement apply to? Open Source stuff? Is it software in general? Is it just PyPI?

NAOMI: I think I would say it’s particularly Open Source, and I think… Then I would say it’s absolutely true for PyPI.

MEL: (laughing) In contrast to non-Open Source stuff, how would that kind of thing happen?

NAOMI: Well, typically it goes along with the other things we’ve said about non-Open Source, where the resources and the planning is there in advance. And usually along with that goes that kind of organizational sort of… Structure around it. So that somebody who is authorizing those resources has probably -- not always -- but has probably set up some sort of structure of accountability for that.

MEL: And this is actually one area that I wanted to ask you specifically for help kind of thinking about. Because… So when we were thinking about number 4, and a little bit of number 3 also, but mostly number 4, we were trying to find some way to articulate the work that goes into a project, that isn’t about technical progress. So that’s where the bureaucratic, organizational, financial, legal, project management, design -- that sort of thing -- 

and in your first interview, when we talked about sustainability and projects being well maintained, you brought up a lot of considerations that were not strictly technical. But also to me don’t seem to quite fall into what we’re talking about in number four. 

So you were talking about, like, are people thinking about being inclusive and reaching out to newcomers? Is there an onramp for people coming in? So where would you fit those kinds of things that you were talking about in the first interview, in relation to this?

NAOMI: That’s kind of a good question, I guess. We’re talking about… I guess I would say a couple different levels of… I don’t know if I would say “management”, or maybe it’s even more vague than that. The bureaucratic organizational stuff -- that’s very practical. Anybody with experience would recognize that as management-type stuff. The inclusion and making sure that things can get in -- that’s a little bit of a higher level thing. 

Where typically… Well, I think typically tech organizations in general have struggled with where to put that, honestly. Do you hand it over to whoever you think is marginalized? Because they should know what needs to be done? Do you have a department for it? You know. There are a lot of questions as to how you handle that. Because it’s kind of a higher level thing that is a little bit more vague, and it is harder to place. It kind of goes to the culture and the underlying philosophy that’s kind of behind the organization. And a lot of organizations really struggle with that. Because it is sort of a vague slippery topic.

MEL: Yeah. And I, for instance, could imagine a FOSS project where the developers that started it were very thoughtful about being inclusive and everything, but then just sort of ran out of steam or ran out of time and got stuck. And so it’s not like -- oh, no, clearly your problem isn’t inclusion.

NAOMI: Right.

MEL: Okay. So it does seem to potentially be a separate thing. And not just -- yep, let’s lump it in here. That’s obviously where it goes. But at the same time, some of this stuff can affect it. Like, good project management can do a thing like -- are new contributors able to come in… I’ll keep thinking on that. Another bit that came up related to, I think, mostly… I was gonna say 3, but I actually think it might be number 2. Did we skip 2? 2 and 3. 

So this is not actually in that list of 5 yet. When people were talking about the different ways that FOSS infrastructure projects get resourced, when talking about -- okay, we need these resources to persist, so that the project can be sustainable -- one of the things that came up was: Okay. We need people. We need people to have jobs and salaries so they can keep doing this work not in their spare time. 

And both Donald and Terri mostly were describing the hiring process for how people tend to become paid to work on Open Source things. And it’s very much a, you’re already doing it. As a side hobby passion. You’ve already been doing it unpaid and now we’re just gonna start paying you for it. Which on the one hand is great, but on the other hand, excludes a lot of people who can’t do that kind of thing as a hobby first.

NAOMI: Right.

MEL: And so structurally… How do we think about that in terms of: If we’re working on improving Open Source infrastructure sustainability, how do we make sure that that sustainability is something that more people are able to chip in on, not just the people who can afford to have a 20 hour a week hobby first?

NAOMI: Right. I mean, that’s… That’s an issue that I think is starting to come to the fore a little bit more. I mean, it also affects the way that people think about conference attendance, say. There are more and more conferences now that are trying to pay speakers. 

And that’s… On the one hand, I guess for somebody like me, who’s been around Open Source for a long time, that seems very strange, because we all were doing it for free. But on the other hand, it is a good point. Some people can’t afford -- even if they get a full scholarship to come to a conference, they still can’t afford to take four days off or something like that. 

And the first place I saw that done was years ago, the PyCon UK Education Track actually had a teachers’ track where they paid the schools for a substitute teacher, so that the people who were interested could be released on a school day, and come and teach. I was first associated with that in 2014. I believe they’re still doing something like that. 

So… Then it is kind of a reasonable thing to apply it to the same thing. How can you spend 20 hours a week, 30 hours a week, 40 hours a week immersed in a codebase, doing these things, if you have to worry about… Who knows. Say working two jobs and making sure that your kids are taken care of, or things like that. 

So I haven’t heard many people seriously saying we should be paying Open Source contributors. I haven’t really heard that. But if you think through the implications, that kind of is what we would be coming to, I think. You know? 

I think there are things that do it in a somewhat different way. I guess there’s a stipend associated with things like Outreachy and stuff like that. But that’s not really meant to be a model that’s applied to everyone. It’s meant to be specifically an onramp that people will presumably get past fairly quickly. So yeah. It does kind of follow from that discussion.

MEL: Yeah. So it’s one of the things that we’re kind of coming up with, in the data. These… I want to use the phrase “inadvertent tensions” that come from Open Source culture and Open Source principles. That we were like… Freedom is great! And then down the line, we’re like… Wait. Why are these all the same kind of people?

NAOMI: (laughing) Exactly.

MEL: Okay. And then let me find the fifth one. Because it was a similar kind of inadvertent tension from a FOSS cultural principle.

> _Source(s): notes-11-10-2019.md_
> 
> 5. Infrastructure user data and usage patterns are important for determining future resource needs. FOSS infrastructure maintainers are less likely than non-FOSS infrastructure ones to have complete and reliable access to that data because of intentional cultural choices to prioritize user freedom and access over it. 
 
NAOMI: Okay. That is an interesting point. Yeah, I agree. That is another tension that arises from the way that we’ve always thought about Open Source. 

MEL: And it was interesting to see it come up in the interviews, because when I was talking with the PyPI developers and maintainers, they were talking about how difficult it was to plan and to figure out what APIs can we break, because we don’t know if anyone is using this, or why it came to be in the first place. If we change this, how is our userbase going to shift or how is this going to scale in the future? And we don’t have that kind of information. 

And then when I was talking with Jackie especially, and a little bit Terri also, they’re like -- it’s fantastic that you don’t keep that data! I’m so happy you don’t. Like… Well, you can’t have both.

NAOMI: Right. Yeah. That is an excellent point. I think even in a wider range of things, I think that is… An issue we are likely to be grappling with more. As we start thinking about some of these things, and sort of fighting these sorts of dilemmas. Yeah.

MEL: So to be fair, Ernest on the infrastructure side also talked about not wanting to keep the logs. Not wanting to keep the data. So it wasn’t like… Maintainers versus users. Or upstream versus downstream.

NAOMI: Right.

MEL: It was… Right. Because one of our cultural values is this privacy and this individual choice and this freedom thing, the trade-off is… We don’t have these logs.

NAOMI: Well, and that, of course, kind of skates over a question. We don’t want to keep the logs, because the way that our logging is typically written, it contains things like IP addresses, and maybe things like that. There’s nothing saying we couldn’t have a mechanism that would just log “this service was hit at this time”. “This service was hit within this time period”, even. So that that data could be gathered. But none of the out of the box logging would be probably likely to do that in a very easy way. So there may be some room in between that we’re just not conditioned to think about.

MEL: Well, with someone -- I don’t recall who, but someone was talking about -- well, we could implement this stuff, but also the larger problem is that no one’s actually… I don’t think it was quite as strong a statement as “no one would look at it; no one would care about this stuff”. 

NAOMI: Right.

MEL: And they made the analogy of  -- if this was corporate, they would want to know those numbers for a potential market share, and so forth, and there’s a whole department dedicated towards -- is this product feasible, even, as a product. Whereas with something like PyPI, no one is looking at it and going: Well, we could make $30 million more dollars if…

NAOMI: True, but… I guess from my perspective, in thinking about the PSF, and resources, and planning, and trying to marshal the needed resources and all of that, I think even without all of those dollar motives, there would be good reasons to know how many people are using this or that service. What we might need to expand. How we could go to possible sponsors and donors and say: This thing is being used a lot. Please help us do more! 

So yeah, I guess I would say I don’t buy that one particularly. I think people would look. I think actually at the PSF board level, we’ve kind of asked questions like that occasionally, and been disappointed when we were told… No, no way to know. So yes, I think that there’s plenty of room for an interest in that.

MEL: So poking at that a bit, then, at the board level, if you would like these metrics and it would be useful on an organizational level, are there people who could do that? Are there people who -- so basically what’s stopping you from having that? Is it… Oh, no one’s interested? Should we hire a consultant to do that?

NAOMI: I would say that it’s not something that we have viewed as vital. And we do have… I think we’re pretty cognizant that we have limited resources. 

So that’s again a difference between that and perhaps a non-FOSS environment, where perhaps there would be… If you really wanted a particular bit of information that wasn’t being collected, if you could get to the right senior manager or vice-president or whatever and convince them, then they would make it happen. We don’t feel that we want to do that kind of direction and divert those resources to do that, when there are so many other things that need to be done.

MEL: Mmm.

NAOMI: That doesn’t mean we wouldn’t like to have them. But it’s just that we wouldn’t prioritize it to that point.

MEL: That’s fair. If it didn’t necessarily cost the PSF money, there’s that old grant tradition of… Gee, I wonder if there’s a student thesis project that would be -- oh, can we find an MBA student who likes Python?

NAOMI: It’s a possibility. I mean, those things, I think, end up… Even when you’re doing something like that to save effort, they take a lot of effort. 

And also, I think it’s kind of verging on… Perhaps involving the PSF board more in micromanagement. So we ask the questions. We can kind of try to point things in a particular direction. But I think the way that we’re evolving our board to be more for oversight… You know, I don’t think suddenly just stepping in and directing the staff -- you should do this thing! Is the way we would want to go.

MEL: Maybe this is another board perspective question. If not the board, then where would it be appropriate for that kind of push? If these sorts of metrics… Or data would be useful. So whose place is it to do that? It’s not the board, but if some external… If Google or someone came on and said: You know, we rely a lot on Python. And we’re not sure this is gonna be around. So we’re going to commission some of our employees to run this internal research project and then give you the results. I don’t know if that would be stepping out of line. Or…

NAOMI: Well, I think that that’s the sort of thing where the Executive Director and the people that we have working on either planning infrastructure and/or marketing… Those would be the people that would be interested. And I think it would sort of fall to them. It might still be the case… We’ve not evolved to the point where the board would be completely divorced from this. But I would think that the board shouldn’t be, like, the sole driver of that.

MEL: And the reason this is coming to mind is: There’s the larger question of… So this research project is being funded by the Ford and Sloan Foundations. And one of the questions that they’re kind of implicitly asking is: Hey, we and lots of companies and other foundations and people with money would really, really like Open Source infrastructure to continue to be around, because it’s so important to so much of society now. And we’ve got, like, money and people and resources and stuff. But we don’t know what to do with them to help out most.

NAOMI: Ah. Mm-hm.

MEL: And if this is the kind of thing where… People who are not part of that Open Source community can actually be more helpful from the outside, that would be something that’s better done as an… External group comes in and does it, as opposed to give money to the PSF to do it.

NAOMI: Um… I think that… Would be very situational. Really depending on where they find themselves in relationship to what that particular problem might be. I don’t know. It certainly could be -- depending on the situation, it could be something that just might be helpful to just have done. Yeah. 

At this point, I think we have certain things that we get from Google Analytics logs and things like that. But that’s really, I think, pretty much all that we get. So if someone were to come in and say: I can give you all of this information about the usage of your resources, without doing things that will make your community upset… Then that, I believe, should be interesting. Yes.

MEL: Yeah. And I know we can’t, like, actually make specific statements or claims or plans on this right now. But just thinking about… Noting this as an area for potential exploration of what might… What might entities outside a project community be more able to do. 

NAOMI: Right. 

MEL: When we think about what role -- if someone from outside says: I want to make sure Python is still around! We have the version of: Great! Donate to the PSF.

NAOMI: That’s one thing, yeah.

MEL: Great! Get involved in your local Python meetup, conference, community, hire programmers, whatever. But then there’s also the version of: It’s fantastic if you’re not the PSF. And therefore here’s what you can do.

NAOMI: Right.

MEL: Anything else kind of in this area? I also want to show you the definitions people came up with. Just want to make sure we…

NAOMI: No, I think that’s fine.

MEL: Okay. So… These bits are sort of the aggregate definitions of what people said for… I’m gonna do well maintained first and we’ll talk about that and then I’ll show you sustainability.

NAOMI: Okay.

MEL: There you go.


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

NAOMI: Okay. I mean, this certainly seems to cover everything that I can remember talking about. And then some, I guess, a couple of aspects that are more specific to software practices, yeah. 

MEL: Is there anything here in terms of wording that you might want to tweak? Or things that… Are we missing anything?

NAOMI: I can’t think of anything we’re missing. And I don’t see anything in the wording that is ambiguous or would cause me to want to change anything. No, it looks fine.

MEL: Okay. And this is just sort of a rough check for everyone of whether we’ve covered everything obvious. So here’s sustainability.

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
> 1. There are new people onboarding.
> 1. There are clear entry points for new contributors so they know how to get started.
> 1. Maintainers are not burning out in silence or unexpectedly decreasing their contributions for some other reason (moving, new child, new job, health, etc.)
> 1. Contributions are not bottlenecked at one person, a single point of failure, with no clear pathway to engage the community otherwise.
> 1. Various people taking on roles, not just one person.
> 1. Sustainability is hard to define with numerical metrics; you can try to count how many PRs there are, or average time for an issue to get fixed, but there are always more complicated reasons than that.

NAOMI: These are fine. My reaction in reading them is that they’re maybe not quite as refined yet as the first set. There are some things that look to be kind of repetitive, and where one or two things might kind of go together. 

I don’t disagree with any of those things, certainly. And I think that onboarding and entry points and whatever are mentioned two or three times, and resources are mentioned a couple different ways, where maybe they go together. Things like that. But otherwise, I think that’s more just a matter of kind of boiling them down a little bit. 

I’m in agreement with them. I don’t see anything missing.

MEL: Yeah, it’s interesting that you noted that. That “not quite as refined”-ness. So I totally agree. You’re not the first person who’s noticed that. And there’s a quality of… Yes. More of this needs to be refined for it to be at the level of clarity that the “being well maintained” thing looks like. 

But there’s also… This was an interesting discussion with… I think it was Ernest. And to make both of these sets… I did basically the same amount of editing. So I went through and just grabbed portions of people’s transcripts and then put them in a list. And the second one, the sustainable list, was much harder to find, much harder to work with, much fuzzier in terms of phrasing.

NAOMI: Yeah.

MEL: And so when Ernest looked at a slightly earlier version of this list, but almost identical to what you’re seeing with just a few wording changes, he commented that… That matched his experience with talking about projects being well maintained, versus being sustainable. But in the Open Source software world, we kind of have a notion that’s more developed of what being well maintained looks like. But the conversation of sustainability was newer. And less figured out.

NAOMI: I would agree. That makes sense.

MEL: And yeah. So that seems to be reflected in the list and in the wording and the phrasing. If that makes sense, do you have any thoughts on why that might be? Why would one of these concepts be more well developed than the other?

NAOMI: Well… I think… I don’t think it’s surprising that we have that kind of discrepancy, because… I think maybe being well maintained is… I wouldn’t say necessarily an easier topic, but it’s a topic that is more familiar to people from an engineering background.

MEL: Oh, how?

NAOMI: Well, what should I say? It kind of falls in line with a lot of things that tend to go along with “best practices”. So really, we’ve been talking about how to make code well maintained. For -- who knows. At least 30 years. Probably more than that. And so this notion of thinking about things like that -- you know, we must do this, so that when we come back, we can have an easier time of updating it, doing whatever we need to do. That’s very common. That predates the FOSS world, certainly, by a long way. 

And sustainability is much more a problem that comes with FOSS maturing and taking the dominant… I think we can say… Dominant role that it has in the world today. And that’s a fairly new thing. 

And it’s, again, when we’re talking about a non-FOSS project that has the resources laid out, has a command structure, has all of those things given, they don’t think about sustainability in that way. And in that kind of environment, no one asks you: Will this be sustainable? It will be sustainable as long as it’s worth it. Then we’ll pull the plug. That’s the way people tend to think of it. So that’s why I’m not surprised.

MEL: Huh. And so sustainability… I don’t know if we have an analog for non-FOSS but also non-software things. So is the sort of sustainability that FOSS projects have to think about nowadays a different way of thinking about sustainability than technical people have had to consider it in the past?

NAOMI: Well… I think so. If it’s… Again, given the fact that we don’t have some of these mechanisms for saying whether or not something is, quote, “worth it” or not. And as we pointed out, in some cases we don’t even ask the question, because we don’t collect things like that. Then… You know, you have to think of different ways of making sure that it’s worth it, so that those resources are there. Yeah. 

So I think it is really an issue that is much more something you get with FOSS than you would with other projects. Other projects… If there is a return on investment in someone’s judgment… Whether they’re right or wrong… Then the project gets its resources and continues. If not, not. And nobody feels very sad about that. Oh, we killed that project. In the corporate world, projects get killed all the time. And people just go on.

MEL: Might there be an analog to maybe things outside of software, that aren’t necessarily profit-oriented? So sustainability of government systems. Like public libraries. Or…

NAOMI: Somewhat. Although there’s still that kind of… I don’t know. Command and control there. I mean, non-profits -- if you read about the struggles that non-profit organizations have to keep going -- I think that might be a rough analog to what goes on in Open Source as well. Are we serving enough people? Are we serving the right people? Are we serving the people that our funders think are the right people? And of course, very low financial rewards. Very demanding work. So there’s a similar problem with burnout in lots of non-profits. That isn’t that different from what you see in certain Open Source projects as well. So I think maybe that’s sort of an analog.

MEL: Yeah. So that’s the stuff that I had to show you today. Any other thoughts on any of this? This is the last time that we’ll…

NAOMI: Um… I don’t think of anything, really. This has been kind of a fascinating study. So I’m looking forward to… I guess to seeing the whole thing wrapped up with a bow or whatever it is. But yeah… And I am delighted to have been able to have been a part of it, too. So yeah, I don’t have anything more to add, I don’t think.

MEL: Okay. And it’s been absolutely fascinating to get your perspective as well. As a board member, and someone who’s been deeply involved for such a long time. The last thing before… (audio drop) we (audio drop) close out… What has it been like to participate in this process for you? Sorry, Mirabai is saying my audio is out again. What has it been like to be part of this study?

NAOMI: Um… I think it’s been really interesting to get the reactions from other people as part of the cycle, as we’ve iterated through the series of three interviews. I’ve found that to be kind of enjoyable, just seeing that, while we were looking at the thing from different views, we all were seeing the same thing. You know? It wasn’t that our perspectives were so different that it’s like… Oh, we’re not even talking about the same thing. No, we were all seeing the same thing. Just from kind of different perspectives. So I thought that was really a fascinating part of the process. And I enjoyed being able to talk and think about some of these things.

MEL: And is there anything about the process that you would want to change? Or add or tweak? In case we end up doing this with more people or different communities, down the line? Because it seems like a helpful way to look at Open Source projects, particularly.

NAOMI: Yeah. At this point, I can’t think of anything, particularly. I think this was interesting. Probably not something that will scale tremendously, I suppose. But I thought that this kind of conversational approach was really much more interesting than just a bunch of surveys or something like that. I don’t think that would have been very interesting.

MEL: Okay! Well, thank you so much, Naomi.

NAOMI: My pleasure!

MEL: So the usual open licensing transcripts thing is going to happen. And then in two weeks, in November, myself and (audio drop) Sumana and Shauna and my co-PI, Steve, are gonna sit down with everybody (audio drop) transcripts and do the big analysis.

NAOMI: Okay.

MEL: So we’ll send you updates on that. No obligations (audio drop) so that you (audio drop) can continue to peek in. What’s going on. And then (inaudible) thank you (inaudible) stipend (inaudible) not about work (inaudible) PyCon.

NAOMI: Okay. 

MEL: (typing) Short version:
Should catch up about not work at some point!
Will be probably almost certainly going to pycon this summer, so maybe see you there?

NAOMI: Excellent. Yes… Well… We’ll definitely try to set some time aside to catch up there. I would love that.

MEL: (typing) Will see you around next summer then! Thanks! 

NAOMI: You’re welcome! It’s been a pleasure.

MEL: Bye!
