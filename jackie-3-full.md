# Copyright transfer statement

MEL CHUA hereby irrevocably transfers and assigns to JACKIE KAZIL in perpetuity, all right (whether now known or hereinafter invented), title, and interest, throughout the world, including any copyrights and renewals or extensions thereto, in the attached transcript of the interview recorded between us on OCTOBER 28, 2019 in A LIVE-TRANSCRIBED PHONE CALL.

# License

I, Jacqueline Kazil, hereby release this work under the following open license: http://creativecommons.org/licenses/by/3.0. Anyone is free to share and remix the work as long as they cite it. I consent to the open publication of this work using my name.  
  
# BEGIN TRANSCRIPT

MEL: Okay! And are you ready for the transcript part to start now?

JACKIE: Yes.

MEL: Okay. Cool. So what we’re gonna be doing today is a little bit of a wrapup. We’re gonna be circling around to some of the very, very early stage analysis we’ve been doing across all of the interviews. And I just wanted to get some initial reactions, because it’s super rough. I’m pretty sure we’re getting some things wrong. And so just getting your input on where we’re headed so far, and then after that, I’ve got some aggregated definitions of what everyone’s said, when we asked them what sustainability and what being well maintained meant to them. So that’s sort of the agenda for today, and the rest of the time will be for you to share any other thoughts or stories about PyPI, digital infrastructure, sustainability, anything else that you want.

JACKIE: Okay.

MEL: Any questions before we begin that?

JACKIE: No.

MEL: All right! So if you look at the very top of the Google Doc, you’ll see two sections, and one is a bit that you said. Infrastructure versus non-infrastructure software. And just kind of to give you an overview of what you’re looking at, two of the questions we’re asking as we’re looking through the data is: What difference does it make if a software project is infrastructure as opposed to not infrastructure. Maybe it’s a library. Maybe it’s an end user application. Or a database. Or something. 

And then after that, the second section was: What difference does it make whether infrastructure is Open Source or not Open Source. And for the latter one, we’re thinking not just in terms of licensing, but also in terms of culture that tends to come with Open Source projects or structures. So you could think of this as: Community versus corporate. Or grassroots versus organizational. There’s a lot of different ways to think about it. But this is… 

So first I wanted to check and see if you had any thoughts on infrastructure versus non-infrastructure software. We have that little bit from you up top. But the first question is: What difference does it make in thinking about sustainability whether a piece of software is infrastructure or not?

> _Source(s): Jackie-1_
>
> JACKIE: As a user of other packages, I never really looked at sustainability because I always looked at it as, well, if this doesn't continue or this somehow fails, I can fork it. In the worst case, I can fork it and fix the things that I need to fix to make it work.

JACKIE: Hm. I’m not sure that there’s any difference. I just think that people often don’t think about infrastructure as… People often don’t think about infrastructure as… I’m sorry. People often don’t… I’m speaking for people in general. I don’t often think about infrastructure when it comes to Open Source packaging versus non-infrastructure. But I don’t think they should be thought of differently.

MEL: Okay. Cool. And some of the things that other people have said about that -- since this is the last one and I won’t get a chance to fill you in otherwise, is --

(audio drop)

I think it was Ernest who talked about -- for infrastructure, you get to decide -- the maintainers get to decide whenever you want to switch it over, versus if it’s a library or something else, the users can decide whether they want to switch to a different version. So that was one of the differences that came up.

JACKIE: Can you say that again?

MEL: Yeah. That… So one of the things that another person brought up was that, for infrastructure, the maintainers decide when it’s time to switch, because it’s a service that’s being provided or an API that’s changing or what-not. Whereas if it’s a library, the maintainers can put a new version out there, but the users downstream still get to decide… Okay. I’m gonna switch my project over to this version now, versus later, versus never.

JACKIE: Oh, I see. So the users have control over… Had more control and autonomy over the world, as opposed to it being imposed upon them. Yeah, I can see that. That’s interesting. I didn’t think about it that way, but that’s an interesting point.

MEL: Yeah. I mean, you know, with Python 2 being sunset right now, support stops, in theory. But people can still keep using it. Whereas… PyPI it’s like -- well, now everyone is on Warehouse.

JACKIE: Yeah.

MEL: So looking at the next bit on FOSS versus non-FOSS infrastructure, and just kind of maybe taking these one at a time… Just getting reactions to this… This is sort of what we’re playing with. It’s not complete. It’s not necessarily correct. Do you have any reaction to the first part?

JACKIE: I didn’t have a chance to read it. Oh, just number one?

MEL: Yeah, just number one.

> _Source(s): notes-11-10-2019.md_
> 
> 1. Infrastructure is “magical plumbing.” FOSS infrastructure lets you look behind the curtain if you so choose; non-FOSS infrastructure likely does not.

JACKIE: Okay. What do you mean by “magical plumbing”? 

MEL: That was a phrase that came up in one of the other interviews. So infrastructure as… It’s like plumbing. You don’t think about it if it’s just working. Or it’s magic. It just happens. And I don’t need to worry about how it happens. It’s a black box. When people were talking about infrastructure being that kind of thing, as opposed to maybe a tool or an application where I’m thinking very hard about how it works precisely all the time. But one of the differences between Open Source infrastructure and non-Open Source infrastructure is that if infrastructure is magic, then the Open Source thing lets you turn it into not magic. You can open up the black box. You can peek under the hood, so to speak.

JACKIE: Yeah. So I would say… Okay. Yeah. So I would say I agree with that statement. Although I would also add, though… FOSS infrastructure allows you to look behind the curtain if you so choose, but most people don’t choose.

MEL: Yeah. That’s a good point. How about the second one?

> _Source(s): notes-11-10-2019.md_
> 
> 2. Infrastructure requires technical effort for operations (as well as development). FOSS infrastructure may begin as a pet project and then “accidentally” go into production; non-FOSS infrastructure is more likely to be deliberately planned as a product launch.

JACKIE: Hm. I think you can have FOSS infrastructure that is deliberately planned. But it is more likely that a pet project becomes… I don’t know that I would say that a pet project… Accidentally goes into production. Because I think sometimes it’s pet projects… Become productionized. And there was no, like, smooth line between: This was pet project and this was production. It was just… Oh! Now there’s a bunch of people who are reliant on our pet project!

MEL: Okay.

JACKIE: And with the way you have it here, it’s like there is a pet project and there was a decision to put it in production, and I think with FOSS infrastructure, when that pet project goes into production, it is more the line between pet project and production… Is blurred. 

And I think… You know, the other thing I would add is: No one’s made a conscious decision to basically say pet project is now production. The other thing I would say, too, is: The FOSS infrastructure can be deliberately planned, but there needs to be some sort of structure impetus to… That has to precede that. 

So like the remake of PyPI was planned. But there was a whole bunch of stuff that had to precede that, and the raising of money and other things. And there was no accident there. So sometimes there are sort of these accidental things, but sometimes there can be conscious efforts. 

You know, and another example is… I don’t know if this is, like, a great one to one, but… The Python Software Foundation is pushing forward some educational initiatives, and one of those is a website of educational resources. And so you could say that is infrastructure for educators in Python. And in that particular case, that is coming out the door as more of a planned project. With some funding behind it. Not somebody’s sort of pet project that they thought would be cool.

MEL: Right. So this is one of the things that we’ve been trying to disentangle, in terms of… It’s a distinction between FOSS and non-FOSS, in terms of licensing. For this one, clearly not. 

But what makes projects more likely to be one or the other? Is it that there’s a large mature organization behind it? So in this case, the Python Software Foundation, even if it’s not a company, even if the stuff is still Open Source, it’s enough of a thing that it can say: We have resources. We have structure. We can do this forward planning. As opposed to an individual going… Yeah, this seems like fun!

JACKIE: Yeah. Yeah. I think I would look at it in sort of three different ways. I would split FOSS into two… So if you think about a community like Go, and I don’t know… Like the Golang community, I don’t know as much about that community, but I imagine that there isn’t, like, a PSF for Golang. And in that particular case, I also imagine that a lot of their… I believe that a pet project would come out of that community more likely than a community like the Python community, where you would have more established… Not just more established, but more of an infrastructure to be able to do stuff in. With respect to groups who recognize… Groups and individuals who can sort of go after money and so on and so forth.

MEL: So this actually ties to the fourth point. So I’ll hold on that and get to that. Let’s look at the third one. The infrastructure requires development capacity, people-time one.

> _Source(s): notes-11-10-2019.md_
> 
> 3. Infrastructure requires development capacity (people-time). FOSS infrastructure is likely to have some or all of this development capacity come from self-directed volunteers, but that effort is also more likely to fade out during the “last mile.” Non-FOSS infrastructure is more likely to have its development resources known, managed, and allocated in advance.

JACKIE: Mm-hm.

MEL: Any… thoughts or comments or edits to that one? Any reaction to the third one?

JACKIE: Yeah. I would say… I would say that… It’s probably accurate. I think some of my problem with this, and the same as with two, is that you, in this, are drawing a very distinct line between FOSS and non-FOSS, and it sounds to me like FOSS in this particular case -- FOSS is completely unfunded. And you can’t have cases where FOSS is funded. And that’s where some of these statements fall apart.

MEL: Right. So that’s in the really early stage stuff. So that kind of subtlety of phrasing is something we’re trying to figure out how to get into more of an expansion. Because we certainly don’t want to essentialize and say: All FOSS projects are like this. Because they’re not. But are there cultural tendencies or organizational system patterns that we would tend to see in FOSS projects more than non-FOSS projects? That might be a better way of phrasing it. So how would you change the phrasing on that?

JACKIE: I think I would say… FOSS projects without large… I would make the definition of FOSS projects something that is without large amounts of money behind it. And when I say “large”, I mean… A couple thousand dollars to pay for infrastructure -- that’s not large. When I talk about large, I mean enough money to pay for people’s time. 

MEL: Okay. So in the territory of being able to have at least one full-time salaried person devoted to it?

JACKIE: Yeah. I would say for some amount of time period… I think three months… I would say six months. Because I think it changes the dynamic, when you have those salaried people. Or contracted people. On a FOSS project.

MEL: Right.

JACKIE: And it changes also what gets delivered. I couldn’t tell you exactly what’s the magic number. You know, I would probably cop out and say something like… For some significant… Salaried or contract… Full-time, paid individual. Whether that’s salary or contract. For some relevant time period where they’re able to make an impact, because of the money that they’re receiving, and they’re able to work on the project some more hours than they would have, had they been volunteer.

MEL: So… Poking at that slightly, actually, so Google Summer of Code pays students, who are typically quite new to the project, for three months of full-time work. Would that be enough of a resource to push an Open Source project that otherwise wouldn’t have that kind of resource over the line for you? Or does it need to be, like, a more experienced, seasoned person?

JACKIE: Um… I think it could. I think it depends on that person’s -- that individual’s relationship to the project before Google Summer of Code. And how much onboarding they’re gonna need. Because then that requires volunteers to assist them. Which kind of neutralizes the money that they’re receiving.

MEL: (laughing) True. And then in terms of… Even for FOSS projects that have that sort of larger organizational resource capacity, so for instance Python -- it’s Open Source. You’ve got the PSF. There are people who are paid to do PSF stuff full-time now. But the infrastructure sustainability of Python stuff is still… It’s by no means guaranteed. Like, if everyone stopped donating everything to the PSF right now, we would still kind of be in trouble in a year or sooner. So how do we think about… What kind of considerations do organizations like the PSF, projects like Python, have that -- and maybe we might not be thinking about it as much, or it might not be as widespread knowledge.

JACKIE: I’m going back to the transcript for a second, to reread your question.

MEL: It wasn’t a very clear question. The question would be something like: The PSF has resources, and has employees. But there’s still… Sustainability is still not a guarantee. And so as someone who’s quite deeply involved with the PSF, what kind of things would, in your opinion, make Python infrastructure more sustainable? What kinds of things would enable you to just not think about that anymore and say: Okay, actually, that’s just gonna be fine? That might not currently be known or happening?

JACKIE: Sure. So… The vast majority of the Python Software Foundation’s budget comes and is reliant upon PyCon. And PyCon is… There are extra ways to get a little extra money here, a little extra money there. From the way things are packaged for sponsors or marketed. But PyCon is a sort of limited resource.

MEL: Yeah.

JACKIE: And it’s never-ending. We have gotten a couple of grants in the past, and I think that is the particular way to go. With respect to continually funding. But while PyCon is a major source of revenue to the PSF… It is going to get money from these other pots that I mentioned. Like grants. Becomes a little bit more risky and a little bit more unsustainable. But that is sort of the nature of non-profits. That money is not guaranteed. 

And so I think the other way of going about it is to sort of allow somebody to take control of the infrastructure as their project. Sort of like a private company or something like that. But then it becomes… The project then inherently becomes less FOSS. 

And if you get a company sponsor to basically… Let’s say we got a large Silicon Valley company to fund, you know, a couple of head count for infrastructure, but the PSF still ran infrastructure, that has the same uncertainty as large grants that you might get from other foundations. Or from the government. It’s all dependent on… You have a promise for a certain amount of time. But there’s never… There’s always the risk that things can change, or the money runs out after that time.

MEL: Right. And backing up a bit, when you talked about the PSF getting a lot of revenue from PyCon, is that from mostly ticket sales?

JACKIE: I’d have to go back to the budget. But it’s ticket sales and sponsors.

MEL: Okay. And sponsors. And then in terms of sustainability, just thinking about -- ongoing resourcing seems to be a thing that comes up for a lot of people in these interviews. If we were to say something like: Well, if someone stepped up and said we can run twice the number of PyCon events, regionally, and that would have more money… Is that a thing that would be scalable? Or is it like… No. We’ve maxed out on PyCon revenue. We need to find some other way to get money, whether it’s grants or something else.

JACKIE: So we defer all of the regional events to regional groups. And all of the events worldwide to the local Pythonista population. I don’t know quite how to word that. 

So we will manage -- the Python Software Foundation will manage the trademark of PyCon. But we only take revenue if they’re selling something that uses the trademark. For example, if somebody was selling T-shirts. And using the logo. Then we might take a percentage of the revenue. 

But the sort of… The way we run PyCons right now, we do not sort of -- we do not run the regional PyCons, like PyTennessee, PyOhio. PyTexas, PyCascades. All of those are run individually by the local Python groups.

MEL: Okay. So in terms of… As a source of revenue and resources, PyCon as the PSF is currently set up isn’t something that could really scale more, unless that structure changes pretty drastically, it sounds like?

JACKIE: Yeah. So yeah. It would be either us filling in spaces where those events didn’t happen, and then the question is: If they didn’t happen already, why haven’t they happened? And/or… Trying to do some inappropriate takeover of the regional PyCon -- like, local PyCons.

MEL: And drawing that out a little bit, why would that be inappropriate? To take over the regional ones?

JACKIE: I would say it’s inappropriate because there was never any conversation about it. And a lot of the people who have started them, locally, they’ve put a lot of time and effort into the events that they’ve created, and without a discussion, it would feel like a hostile takeover. 

And some of them… Some of them I don’t think… We own the trademark to PyCon and Python. So some of them I don’t think we could legally take over anyway. But I’m not a lawyer. It would kind of, I feel like, leave a bad taste in people’s mouths to now say: We’re gonna now host an event in this place. 

However, you could also say, too, it could be something to explore -- and you could say: Well, people are… People suffer a lot of burnout. And maybe some of the people… The volunteers. Volunteers suffer a lot of burnout. And maybe the volunteers who are running some of these events are getting tired, and they would welcome a takeover. 

But I think a lot of the local events are also… While PyCon is, in comparison to a lot of conferences, it’s pretty accessible, financially, it is not about… It’s not a $1,000, $3,000 conference. The local PyCons are even more accessible. And I think part of that is also about the fact that they don’t have the infrastructure around the PSF to support. 

So, like, for example PyOhio tickets are free. And a lot of the others are maybe a couple hundred bucks at most. And so would an entity like the PSF be able to maintain that type of accessibility and culture on a local level? I don’t know. Certainly… 

Is it NumFocus Foundation that does PyData? I’m drawing a blank now. I’m looking it up right now. Yeah. So there are the PyData conferences all around the world, that the NumFocus Foundation does. And they certainly -- each one has to have so much return for them to be able to justify -- because they have them all over the place. 

So the model that you’re talking about sounds like that model. I mean, it’s certainly possible. It’s just not something that the PSF has ever talked about, to my knowledge. And there would have to be a lot of discussions… 

But it could also bring a Python conference to a place that hasn’t had one in a while, or that has never had one. For example, Washington, D.C., you expect to be a large city -- would have a Python conference. The local community has talked about it quite a bit, but the volunteers haven’t gotten together to actually do it in a while.

MEL: Huh. I didn’t realize DC hadn’t had one. And thanks for unpacking this a bit. Because I was thinking about sustainability and resources. And if you think about non-FOSS infrastructure, corporate infrastructure, if I’m thinking about like AWS, say, and I think about… What’s the revenue model for AWS? It’s… Selling the service. It’s not like… Oh, yes, Amazon gets most of that revenue from having AWS conferences.

JACKIE: Yeah. Yeah. Yeah. Yeah. They sell the infrastructure itself. But also, the conferences… Like, the AWS conference… I don’t know how much their tickets are. Do you know how much a ticket for that it?

MEL: I think they’re pretty absurdly expensive. I can look that up right now.

JACKIE: I think so too. And they’re, like, sold out. And so… I know it’s like a very limited… Okay. Full conference package is $1800.

MEL: Yeah, I just saw that.

JACKIE: Yeah. And it doesn’t look like they’re sold out, but I think they do sell out. But I think it’s also like… Somewhere between 50,000 to 60,000 or 65,000 people attended last year. Where PyCon is under 3,500. Above 3,000. So from AWS, just the tickets alone -- this doesn’t include sponsors -- that is… Uh… That’s $90 million.

MEL: Yeah.

JACKIE: So one of the things we’ve also talked about too -- and we’ve gone back and forth on this -- because we always sell out PyCon -- has been making PyCon bigger. Which means more ticket sales. But then also more features and also you get to raise the sponsorship packages. 

And I think the reason why we haven’t done it bigger -- well, there’s a couple reasons. One has been -- well, the main one has been… We do not want to take away from the local PyCons. And when I say local, I also mean internationally. Like, PyCaribbean. It’s funny. I’d love to list them off, but I completely just blanked on all the conferences. You know. PyPB. PyCon Iran. I didn’t even know Iran had one. PyCon Namibia. They just had a PyCon Africa. 

So we don’t want to take away from those by becoming bigger and bigger and bigger. And we want to encourage people to go to those smaller ones. And in some cases, equally sized. I say smaller, but equally sized. I think PyCon APAC might be of equal size to PyCon. And we want to encourage not just the individuals regionally who live in those places, but leaders from the Python community, to also go to conferences in other places. So this is… PyCon should be considered more like PyCon US. Not PyCon, period.

MEL: Mm-hm. And what you just described is a kind of… A value and a prioritization that I find it hard to imagine a corporate infrastructure provider thinking about that. Oh, let’s not increase our revenue here. Let’s not go here. Because we want these other things which bring us no income at all to be more successful.

JACKIE: Yeah.

MEL: Cool. So… Maybe take a look at number four and we can come back to this one if you want to. There’s a lot of interesting stuff here. Thank you.

JACKIE: Yeah, no problem.

> _Source(s): notes-11-10-2019.md_
> 
> 4. Infrastructure requires bureaucratic/organizational work. FOSS infrastructure is likely to have this set up late, during the “last mile” or the “sticking point.” Non-FOSS infrastructure is more likely to have this infrastructure (legal, organizational, financial, managerial, marketing, etc.) be set up early.

JACKIE: Yeah, I agree. I mean, I think some of it also depends on experience. Well, I’ll say… Okay. Some of it would depend on the experience of the individuals. Working on the project. And what they’ve done before. 

But I’ll also say… With FOSS, with FOSS -- well, with non-FOSS, those resources often already exist. And because they’re building a product, they want to protect that product. And sell that product. With non-FOSS, that is not necessarily the goal from the very beginning. And I can see it being set up late, because if you have limited resources to do limited things, well, then, the most important thing should be to build the actual thing. Not…

MEL: Right.

JACKIE: Not try to figure out how to market something that doesn’t exist.

MEL: Mmm. And one of the… I wish I could show you this graph. But I don’t have a way to give you the picture here. But where number four comes from is: We were going at this on a whiteboard, and the three upstream folks -- so Donald, Nick, and Ernest -- when they were talking about the PyPI code progress over time, the feature implementation progress, it was like this graph that started at zero and then just kind of steadily went up, and then at 90%, it just stalled and it stayed at 90% done for a really, really, really long time. And then the Mozilla grant happened and it got to completion. 

But during that 90% long flatline period, what was happening in the background was everything that wasn’t code, basically. It was like… Oh, shoot. We need money. Let’s write a grant. Oh, shoot. We need project management. Let’s get Sumana. Oh, shoot. We need design. Let’s get Nicole. So all of the not technical pieces -- to massively oversimplify there -- but the organizational, bureaucratic, legal, financial, project management stuff happened during that flatline.

JACKIE: Yeah. I think, though, you need to figure out… With FOSS, you need to actually figure out if you actually have something. As where, with non-FOSS, companies can brand and pitch and sell something that is a half-baked idea. And then it sort of reinvents itself as users provide feedback. But with FOSS, you don’t sort of… You have less of that. 

I think there are pluses and minuses to both. Not just with non-FOSS… Not just with non-FOSS infrastructure, but with, you know, non-FOSS technical projects in general. I’ve seen individuals who will go out and write the story of the whole project, and tell you the most awesome thing about the awesome things that are being built, and how they will solve all the problems, and this is before you have any sort of chance of… This is before one line of code has been written. They’ve already written the marketing story in a blog post on how it’s so awesome. 

That’s how a lot of -- let’s be honest -- that’s how a lot of startups get started. You know? Let me tell you about this awesome thing. That’s coming. That doesn’t exist. And then they go out and sell that thing. They sell that story to people. And then people buy into it. You know, the same thing is like the Kickstarter mile. When we tell you -- give me money and let me tell you about this awesome thing that will happen. 

But I think FOSS is focused on making that thing actually happen before they go out and tell the story of the thing. Because why tell… I think that mentality is: Why tell the story if there’s nothing that exists? I’m here to help people. I have nothing to gain from telling them a story about something that doesn’t exist.

MEL: That’s fascinating. So how do you think the Mozilla grant sort of flipped that around? Because when the PSF wrote up the Mozilla grant proposal, it was: Hey, it would be awesome if Warehouse was done. It’s not. So give us money so we can finish Warehouse. It’s the opposite of what you’ve been describing.

JACKIE: Yeah, because they already had PyPI as the preceding story.

MEL: Oh, okay.

JACKIE: And so there was already like… So I think that fits under what you describe more. In that that’s more the bureaucratic organizational -- let’s put more structure around this and more money, because our thing became a success and we don’t have that.

MEL: Okay. Yeah. That fits with other patterns. Thinking about… When people apply for resources for Open Source stuff, there’s obviously: Show us the prototype. Do you have a link to the code? Do at least you have examples of other stuff you’ve written that’s related? Yeah.

JACKIE: Yeah.

MEL: Okay. And then real quick, looking at the fifth bit…

> _Source(s): notes-11-10-2019.md_
> 
> 5. Infrastructure user data and usage patterns are important for determining future resource needs. FOSS infrastructure maintainers are less likely than non-FOSS infrastructure ones to have complete and reliable access to that data because of intentional cultural choices to prioritize user freedom and access over it.

MEL: This is something we’ve talked about a little bit before.  

JACKIE: Can you describe that a little bit more than the words that are there?

MEL: So… Yeah. So one of the things that a lot of people  -- both upstream and downstream PyPI folks  -- were talking about was: It’s challenging to work on and think about PyPI and how to resource PyPI, because we don’t have a lot of information about who’s using it, what they’re using it for, and therefore how do we predict what’s gonna happen in the future? If we keep on going the way we are. And/or if we make certain changes. 

So that story is like… You know, so we had this version, this component of the API, and if we turned it off or we broke it or we added stuff to it, we don’t know how many people that’s going to affect, because we don’t actually know how many people are using that or what they’re using it for or why this happened in the first place. 

As opposed to more productized, corporate, non-culturally FOSS things, where it would be like: Ah, we’re adding this. 30,000 people are paying for it. They’re using it for this kind of thing. And so this lack of data makes it difficult for us to do some kinds of forward planning, but also on the flip side also the description of: We don’t collect or store this data. Or we actually actively get rid of this data. And that is a feature, not a bug. That’s a deliberate cultural choice, because we want to make this available to more people, because we don’t want to do things that would restrict people from being comfortable to do things. Or being allowed to do things. We will value privacy. And sort of individual decision making. As part of this culture. And therefore the consequence is that we don’t have this data, but okay.

JACKIE: Yeah. I mean… I think that’s pretty accurate. From my very small sample size of information… Of projects that I know.

MEL: Any other thoughts on that note or on any of those five points?

JACKIE: Nope.

MEL: Okay. So… Just two last things to show you. One is, real quick, in the first interview, I asked everybody to explain sustainability and being well maintained. And so just to give you a chance to see a summary of what everyone’s said. See if you have any reactions or additions or comments on it.

JACKIE: Okay. 

MEL: I’ll put that at the end of the transcript. There you go. So I’ll give you a moment to look at that.

> Well-maintained
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

> Sustainability
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

JACKIE: Okay. Okay.

MEL: Any thoughts or responses or reactions or edits?

JACKIE: No. That sounds like a pretty good summary. There’s things in there that I probably wouldn’t have thought of. But I certainly agree with.

MEL: Okay. And then the last thing is… Is there anything else that you want to make sure we get on record about PyPI, Python, the PSF, and infrastructure sustainability?

JACKIE: No.

MEL: And is there anything about the experience of doing these interviews -- I know the scheduling has been a little bit challenging. So thank you for working with us on that. How has the experience of participating in this been? And in case we end up doing this with more people or different project communities or something, is there anything you would like us to know about what it’s like to be part of this kind of interview?

JACKIE: Sure. No, this was actually pretty great. And while the scheduling was difficult, I think more for me, I think it was… It was fine. I wouldn’t change anything. And I appreciate you all being flexible when I had to change it up a little bit.

MEL: Yeah. I hope you’re feeling better now.

JACKIE: Yeah.

MEL: You definitely sound much better.

JACKIE: You know, it’s funny. I feel like I’m still in this… I’ve been sick on top of sick. Like… I have a toddler. And it’s back to school season. So…

MEL: Yeah, yeah.

JACKIE: What she gets, I get. And so I appreciate the flexibility. Because… You know, it’s that time of year for us in this family. And just… Yeah. I’ll spare you the details. But it is… Definitely fun times.

MEL: Well, I’m glad you could participate in this. And thank you. It’s been really great to get especially your insights about the board and all that sort of stuff behind the scenes, what you’re thinking about there. That’s been particularly helpful.

JACKIE: Great.

MEL: So what’s gonna happen from now on is: I’ll send you a transcript link with the copyright thing. You know that routine. 

And then in early November, actually, two weeks from now, we’re going to be having a deep dive and actually Shauna is gonna come and Sumana is gonna come, and they and I and Steve are going to go in this and do lots of analysis. So we’ll keep you updated with what we’re finding. No obligation to read or to participate, but just so that you have visibility in what’s going on, in case you want to use it. 

And then around that time we’ll also be getting in touch about sending out the stipends. Just a little bit of a thank you for your time thing. Definitely not anywhere near what your time is worth. But a token of gratitude for participating.

JACKIE: Yeah, thank you.

MEL: And I think that’s it.
