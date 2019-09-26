# Copyright transfer statement

MEL CHUA hereby irrevocably transfers and assigns to TERRI ODA in perpetuity, all right (whether now known or hereinafter invented), title, and interest, throughout the world, including any copyrights and renewals or extensions thereto, in the attached transcript of the interview recorded between us on AUGUST 21, 2019 in A LIVE-TRANSCRIBED PHONE CALL.

# License

I, Terri Oda, hereby release this work under the following open license: http://creativecommons.org/licenses/by/3.0. Anyone is free to share and remix the work as long as they cite it. I consent to the open publication of this work using my name. 

# BEGIN TRANSCRIPT

MEL: Okay. Is it okay to start the official transcript recording now?

TERRI: Yep.

MEL: All right. And that becomes our line [for when the transcript starts]. So… First of all, how would you describe your involvement with the Python community and your relationship with PyPI as a piece of Python infrastructure?

TERRI: So I’ve been involved with Python since I was a teenager. So about 20 years now. Mostly as a Mailman developer in most of that time. The biggest thing that I do now is the Google Summer of Code effort. So I manage the volunteer program that brings new university students in to get paid by Google and get mentored by various members of the community. 

So as far as PyPI goes, I mostly just use it. I actually this past week did my first release -- my other releases with Mailman I wasn't the one pressing the final upload button. But I did just do one for work with cve-bin-tool, which is my new project at Intel.

MEL: I lost the part about -- you first released to PyPI? There’s a couple of places that I don’t think [our transcriber] Mirabai heard.

TERRI: Yeah, just reading the transcript. My first release on my own was this week. With cve-bin-tool. I can’t remember what CVE stands for. Common vulnerabilities and… Something. You would think I would have it memorized. This is a tool that I did for work, for finding security vulnerabilities. And so I did my first software release there. It looks like I did another software release, but it was actually done by a colleague while I was on a plane to New Zealand. So this was the first one I actually did all by myself.

MEL: Okay. So your first release -- is that your first release using the new PyPI?

TERRI: Even with old PyPI, I didn’t usually do the final release myself. So this is my first time ever, really. On my own.

MEL: Wow, okay. And just for clarification -- the Google Summer of Code -- is that for Mailman specifically?

TERRI: I do it for all of Python now. We usually have about 100 mentors, and 25 projects. Mailman is often one of the sub projects, as was my Intel project this year.

MEL: Wow, okay. So starting a little bit more abstractly, to you… What does it mean for a FOSS project to be well maintained and sustainable? So if those two things overlap and mean the same thing together, or if they mean different things to you, I would be interested in what the difference is.

TERRI: So most of my day job is as a security researcher. So when we look at things being well maintained, we almost always mean: If someone finds a bug that has a security impact, is anyone upstream going to be able to fix it? So that could mean… Is anyone paying attention? Does anyone know the software well enough to do the fixes? 

Which is sometimes a problem. The project has been passed around a few times, somebody nobody knows it well enough to do anything with it, and in our case, we mostly want to know how long is it going to take. 

So if we find a security issue in something that we’re using and we report it to them, are we expecting a fix within a couple of weeks or whatever the usual amount of time is, or are we basically taking on the risk of maintenance? Are we going to have to fix it ourselves and provide that patch? 

Which is… Not that far off from what I would think of as well maintained, as just a regular developer. You know? Are bugs being fixed. Is someone still involved.

MEL: And so a question on that front -- expecting a fix, is there particular -- I mean, sooner is nice, but is it… “I want it done really quickly?” Or is it okay… Would a project still be well maintained if you knew, “Okay. That’s gonna get fixed by someone else. It’ll be done, it’ll be done well, but because of their planning process, they told us it won’t happen for… A few months?” Is that still well maintained?

TERRI: That can be good enough. It depends on what the issue is. So with the things that are actually exploitable and maybe a real product, we would need to fix sooner, but it could still be well maintained if we could work with someone and we could be able to say… Hey, we’ve got this patch. Could you test it for us, if we need to do it sooner ourselves?

MEL: Okay. Any other criteria for being well maintained?

TERRI: Um… As someone who just likes working with projects, I consider it well maintained if the community is pretty easy to work with. So if I report a bug, I don’t want to have a… Submit this matter to us, closed wontfix attitude either.

MEL: And “easy to work with”... What kinds of things are easy to work with? Technological level? Interface level? People/attitudes level? All of the above?

TERRI: Yeah, I guess all of the above. Having people that you can communicate with in some way, and you feel like… They’re taking your bug reports seriously, and actually working on things. Even if it’s not necessarily your things. They don’t have to agree with me, but I do like seeing that they’re still involved in seeing how the software is used.

MEL: Okay. And how about sustainable? What would your criteria for a project being sustainable be?

TERRI: So this is one that… We’ve occasionally wanted to define for security purposes. But I don’t know that it’s obvious. We use a lot of different metrics to look at projects, to get our own estimates on that. And I don’t think we’ve ever been able to prove that a project is gonna be around a year from now or two years from now. So… I don’t know. 

I know what I want it to look like. Which is that there would be a decent number of people involved, that people are good at communicating with each other, that people are comfortable stepping down, or passing on information if they need to. 

But sometimes projects just stop for other reasons. Someone gets a new job or someone gets sick, and I don’t know how predictable any of that is.

MEL: I mean, sometimes it’s not.

TERRI: Yeah, I guess the one that I hope would be the answer would be… Communication and ability for people to switch between jobs. But I don’t know if that’s true.

MEL: And this actually helps. So I’m asking this question of everyone, because one of the things that we were hypothesizing earlier in the study is that… If we’re talking about sustainability of digital infrastructure stuff, what people mean by “sustainability”, what people mean by “good maintainership” -- there’s gonna be a dozen different definitions out there. So what might these be?

TERRI: Yeah, and sustainability in terms of money as well.

MEL: Right.

TERRI: Or hardware. 

Or… Just volume of people. I mean, part of why we do Google Summer of Code is sustainability overall, where we have new people getting new skills in the Open Source design methodologies and bringing new blood into our projects. 

I have to say one of my former Summer of Code students now runs the Mailman project, so I feel like we’ve really succeeded in sustainability there at least.

MEL: That’s fantastic! And you were also talking about defining it for security purposes. Can you talk a little bit about why it’s hard to predict, if something is sustainable? That might also be really useful. 

TERRI: I think… I guess part of why it’s hard is that we don’t have really great data in that space. So when we’re talking about sustainability and security, often people look at… You know, how many CVEs were filed and how long they took to fix, but all of these things, when they get boiled down to something you can shove into machine learning -- of course, everybody wants to do -- most of them boil down to something that you can shove into machine learning -- you lose a lot of the information that’s relevant. 

This bug might have taken six months to fix because we needed to rearchitect the whole thing, but that didn’t mean no one was working on it. That doesn’t change how active the community was or anything else in there, or things like… How many commits there are. We look at a lot of projects that are actually in pretty good shape, it’s a stable library, and people are watching it, but nobody is committing anything, and so all of the numbers we have, like the number of commits and bugs filed, doesn’t show that picture. 

So… I don’t know. Maybe eventually someone will take a lot of time and look at all of the many things. When we stuck a lot of these things into machine learning to see whether we could get quick answers we only had so-so luck.  We used human-review our Open Source projects. We did this for two years. We reviewed… I don’t know how many projects. I think I reviewed 400 or 500, so it must have been 4,000 or 5,000, maybe. So we had a whole lot of data on that. And when we boiled it down to machine learning, it basically told us… Is someone still committing to this project? Yes/no. A lot of the other things that we thought were useful… The machine learning obviously didn’t think they were. Which is part of why I suspect we were losing the nuance and what we wanted to get out of that.

MEL: Yeah. That’s the reason why we’re doing this as a qualitative study in the first place. This isn’t a thing you can point programs at yet. We don’t know what it means ourselves.

TERRI: Yeah, and I wish I had the answer, because obviously when I’m integrating Python software into a new Intel project, I want to know whether it's sustainable. I’m basically committing myself to work with the community, potentially, for many years. So I want to know if they’re still gonna be around. 

And they, on the other hand, want to know if we’re still gonna be around, because as a corporation… You never know from outside when a project is gonna get canceled or someone you've been working with will change jobs.

MEL: So sliding over to PyPI, as a user of that piece of Python infrastructure, and basically what you said about what it means for something to be well maintained and sustainable, what are your thoughts on PyPI and how it fits this criteria?

TERRI: So I had honestly never thought about the sustainability of PyPI. It was magic that was just always there, until Donald Stufft was looking for a job and Barry was like… Hey, do you know he’s the only one doing pip? And I was like, “What?! Wait?! What?!!?” So I really hadn’t thought about it at all. It was… 

And since then I know that a lot of work has been done, and I talked to Sumana a little bit about the project, when she was first setting it up. But again, I mostly don’t think about it, because it’s magic that just works for me.

MEL: So this has been a classic [story of] -- “Ah! This is when I found out it isn’t magic.” Because a lot of times, for infrastructure, it is assumed that thus shall it be forever. But, for instance, did you know that PyPI doesn’t have an SLA?

TERRI: Yeah, I did know that one. Again, because of talking with someone at Pycon.

MEL: When did you find that out?

TERRI: Um… I can’t remember. It must have been two PyCons ago? I forget when it came up. I think someone from Facebook was complaining that that was the case.

MEL: Wow, okay. And so what kinds of things… What kinds of external signals did PyPI give here that made you feel like… “Yeah, I think I can depend on this. It’s fine. It’s good. It looks sustainable.”

TERRI: Mostly that I had been using it for about 20 years, and it had never been a problem. Which is very different than many other [programs] that I’ve been using for years. I’ve had more trouble with Gmail than I’ve had with PyPI. Maybe because I use PyPI less frequently than some other services. But as I said, it’s been kind of magical.

MEL: So sustainable also in terms of well maintained… Is that something that you’ve thought about before?

TERRI: Only since I started hearing that people were looking for jobs. But I think because I work with the PSF -- I know there aren’t many paid employees, so I’m not surprised to learn that that’s the case. I knew a lot of this was being done by volunteers. 

Certainly I get a huge number of questions, because I do Google Summer of Code, assuming that I work for the Python Software Foundation. But I’ve never worked for the Python Software Foundation. 

It’s always fun for me, because sometimes I can’t even remember who I’m supposed to contact who actually works for the Foundation who can accept money, for example, as we just changed the accounting. So…

MEL: Yeah. I think one of the things that’s interesting specifically about FOSS infrastructure -- because if it was infrastructure that was being maintained by a company, as a service that costs [money], it would be very different. Who is an employee, who’s not -- that’s not a question.

TERRI: Yeah, certainly for the services that we hire for other things, that’s all part of our standard contract and procedures.

MEL: Right. So… The process is gonna be, in subsequent interviews, but just to begin it now, what happens in the next couple of interviews is we’re doing the first round and asking the same questions to all the participants. Some who were involved in PyPI development, some like yourself who are users of PyPI, and then we’re gonna start bringing snippets of the interviews to each other. So you get to see what other people said sustainability means to them, and you get to see other people talk about… “Here is what I think about PyPI at this point.” And you get to see their stories. 

So from your perspective… And I’m wording this in a deliberately vague way… In the past two years, PyPI has done a lot of... stuff. In part to make itself more well-maintained and sustainable. And some people call that PyPI and Warehouse… Those two words appear in that story. First of all, does this sound familiar? Does that reference something that… Do you know what I’m talking about?

TERRI: Yeah. I knew that there was an effort going on -- I’m still disappointed it’s not called The Cheese Shop, by the way. Showing my age there, I think, probably.

MEL: And also that… Yeah.

TERRI: It wasn’t a good name, but it was a cute name.

MEL: It’s adorable. And it might introduce more people to British humor. So… If you were to tell that story, how would you tell it? The PyPI-Warehouse thing. Once upon a time… What happened?

TERRI: Uh… I’m not even sure I really know. Once upon a time, people noticed that PyPI was… I don’t want to say not being maintained, but needed help being maintained. Needed help for the future. And went to put together a project to make sure that happened. They got funding from… I think it was Mozilla’s organization. And did something. I actually have no idea what happened in there. Except that there was a whole lot of infrastructure work. I know… I heard bits and pieces of stuff about the packages. But I don’t know what parts were in the Warehouse work at all.

MEL: This is great. People tell this story in very different ways. And one common bit is there’s a lot of the story that everybody doesn’t know. So you said people noticed that PyPI needed help. Do you recall who were the people? And how they noticed that?

TERRI: The first person I talked to it about was Sumana. So… I’m gonna… I’m not sure I can pronounce her last name. Harihareswara?

MEL: I pronounce her first name SUM-ana, and Harihareswara…

TERRI: And I’ve had her pronounce it for me, and I always forget. I don’t… I think we’ve interacted in person significantly less than we’ve interacted over IRC. We worked with her on Mailman on some project management stuff.

MEL: Ah.

TERRI: Before she got involved with the greater Python effort.

MEL: How did you come to talk with Sumana about this?

TERRI: She showed up at my table at the PyCon sprints and said: Hey, you know, after all that work I spent working with you guys to try to make it easier to do stuff for Mailman, I realized we’ve got other stuff… Other infrastructure in Python that needed work. So I’m working on this project. And I wanted to tell you about it. And then we promptly got interrupted by… I forget what. Something completely interfered with our conversation and I never heard the end of her story. So that was as much as I heard, until I think the next year, when people were talking about how great the work -- the work was done in the Keynote, I think.

MEL: And this was at PyCon? In person?

TERRI: Yeah. The initial conversation was at PyCon in person. I don’t know who interrupted us. Probably my toddler.

MEL: Oh yeah, that happens. And do you remember any messages or emails or conversations on IRC or wherever about any of this?

TERRI: I definitely talked to Kushal about part of it. He kept me informed about something. In the giant pile of security and encryption-related conversations. I’m not sure when that was. I think he just mentioned it. He was really excited about it. A couple of times. And that things were going on. But usually we were busy talking about his other projects. So that hasn’t been much. I don’t know that I talked to anyone else about it, necessarily. I think that they might be the only two, other than actually talking about it in the keynotes later.

MEL: So when the Mozilla grant was referenced, work on the Mozilla grant happened somehow. By people.

TERRI: Yeah. As far as I know! I guess I did see some tweets about the Mozilla grant when it was granted. So I saw some tweets from Mozilla folk and probably from a few Python folk as well.

MEL: Okay. So that kind of informal network of individuals…

TERRI: Yeah. I probably would have gotten all of that out of the Python-development list, or the Python-members list, or any of those, if I were consistent about reading them, but again, I have a toddler. So all of my mailing lists are basically on the floor unless someone tells me I need to go read them right now.

MEL: Yeah. And I think that’s also an important point. Because other people have talked about… Oh, we sent out this announcement! And everybody is on it. Except not everybody is actually on it, and even people who are on it may or may not read it, because life.

TERRI: Yeah. I mean, it’s sort of silly. I should probably set up my email filters so that the announcements make it through. But all of my Python stuff gets moved into a folder so I can deal with it when I’ve got time to deal with it, and the biggest discovery of having a toddler is that our laptops have touch screens, and toddlers love touch screens, so I basically can’t use the computer until he’s asleep, and when he’s asleep, I need to be asleep. So I switched it to do all of my GSOC mentoring and all the work I do for Python -- I just use a phone. So again, I’m not so much for reading my mailing lists anymore. That’s on me, not Python people having them available. They’re all there. They’re on my phone, even. I just never see them. 

MEL: This is good. Because the actual lives of people who deal with Open Source infrastructure… Sometimes they have toddlers.

TERRI: Yeah, I’ve got to say, I’m very impressed at how much I can do with my phone, but there’s still only so much time in the day.

MEL: Yeah. So with the Python… PyPI-Warehouse project, as that was going on, as that was coming to the end of the -- again, I’m being very vague, because I’m trying to not give you too much to override the way you’re gonna tell the story -- did you experience any of it impacting the way you used PyPI? The way you understood PyPI? What changed for you as a result of the PyPI-Warehouse thing?

TERRI: I’m not sure that anything did, in the end. It’s still magical. I think… I’m assuming that all of the documents that I just read to do my release are probably new. They were certainly very up to date and easy to read. So I assume some of that happened in there. But as I said, I’m not sure I ever read all of the original documents, because I was always assisting in the process in PyPI. So maybe they’ve always been perfectly up to date. But I just assumed that was part of the work that had been done.

MEL: To some extent, that’s the ideal. It’s there, it works, I can understand the documentation.

TERRI: Yeah. I could understand everything. There were recent examples up. Just Googling to see exactly how do I put the command line entry in. Do I put it in a separate thing, or is it a different way -- that sort of thing. All pretty easy to find. And done recently enough that I could find it, anyway.

MEL: Okay. And because of what you just said… Is there anything that you would like PyPI to do or say or make visible about itself, about its well maintainedness and/or sustainability, that would make your life easier or make you less stressed out about it? Is it okay that the story you’re telling about PyPI-Warehouse is essentially… “Yeah, I heard there was a thing that happened. Okay. I’m not sure that affected me.”

TERRI: Well, I’ve got to say… I feel kind of weird, working for a large corporation, that we don’t give a whole lot of money to these things. And I suspect maybe if more of my corporation knew that Python needed help, they would actually step up. But I say that, and we didn’t sponsor PyCon this year, so I don’t know. Maybe that’s just wishful thinking on my part. 

MEL: And what kind --

TERRI: I certainly don’t want to make things harder to use in order for people to realize that there was a lot of effort going on behind the scenes. But it was kind of funny that every time I talk about Python, everyone was like… Oh yeah. It’s fine. That’s it. The only complaint I hear internally about PyPI is around finding of packages. That not all the packages were code signed, so it made it a little harder for us to do our internal validation checks on all the things that we used. And that’s… As far as I know, it’s changing. It’s available. And we could be using it. We’re just not yet.

MEL: And what kinds of signals would have clued you or your company in to the… Oh, hey. We should maybe support Python more?

TERRI: I have no idea. I mean, obviously I should have had all of those signals, and I’m not reading them. So I have no idea what would work in the wider Python community.

MEL: Well, some things other projects do… Like Wikipedia has those banner ads. If everyone reading Wikipedia gave this much…

TERRI: Yeah, and I assume that worked to some extent, but I hear more people complain about them than I ever hear about people giving money.

MEL: Yeah, okay. Heh. So this is a really fascinating storytelling session, and I think you’ll see why when I bring you some of the PyPI insider maintainer/developer stuff next time, and I think that they’re also gonna find this absolutely fascinating.

TERRI: Yeah. I feel bad that I’m not more informed. But I’m definitely not.

MEL: Well… I think one of the things we’re looking for here is… You know, not necessarily how do we make people informed, but one of the questions is: Do people even need to be informed? Is this okay, even? Because everyone has information overload all the time already.

TERRI: Yeah, to be fair, I mean… I knew when someone needed a job, and I knew a little bit here and there, when maybe we could have applied some pressure, and that was about it. So I guess those are probably the most important times to know what they wanted help with. Sort of looking for new maintainership at PyCon. So I got that notice at least.

MEL: And so the last question here: From your perspective in this story, how do you think it would compare to some random Python developer, who also used PyPI?

TERRI: I would guess that most people just assume it’s magical and sustained and great. So obviously somewhat biased in that respect. The only people I ever hear worrying that PyPI is not going to do what they need are people who want full code signing on every single thing that their product imports, and that’s a different problem, I think.

MEL: Mm-hm. And… That’s good to have also, because one of the reasons we picked our downstream narrators for this project really carefully -- all of you are heavily involved in the Python community, so if any of you would know about these things and how to navigate them, you folks would definitely be on that list. So… All right. So that is basically the first round of what’s sustainability, what’s well maintainedness, what is PyPI’s story from your perspective. So anything in the comments or questions that you want to say on the record before we wrap this up, and I’ll tell you what’s gonna happen next?

TERRI: No, that’s good.

MEL: Okay. And thank you again for putting up with my schedule…

TERRI: Yeah, as I said, my whole life is on toddler time. So I wasn’t concerned. I just got some extra knitting done in a conference room.

MEL: So what’s gonna happen is that I’m gonna look through your transcript, make sure everything is good, take out the part before we said we would start the transcript, and I’ll email it back to you with a copyright assignment form, which gives you the entire copyright -- this is -- I can get into it sometime if you want, but if you are the sole owner of the copyright, sole holder of the copyright, you are the only person who can decide when to put a license on it, so when you look through it and go… Okay, this is great, I’m happy to just go up on GitHub with my name on it, you stick a Creative Commons license on it, I’ll send you the text for that, and stick it on GitHub and that’s it.

TERRI: Sounds good.

MEL: So I’ll go do that now. Thank you so much. This is fantastic. Also hilarious.

TERRI: Yeah, probably very different answers than you get from the people who knew what was going on.

MEL: Yes and no! It’s interesting to see the hypotheses of what other people were thinking during this entire time.

TERRI: Yeah. I look forward to hearing some more in the next interviews.

MEL: Okay. Thank you so much, Terri. I will be in touch about the transcript, and then once I finish the last couple of interviews, Heather will be in touch about scheduling.

TERRI: Thank you for inviting me to be part of this. This is gonna be really interesting. And good luck with the rest of your day. I hope it’s a lot quieter.

MEL: Yeah, I’m gonna do this and then I’m going to go to the hospital. It’ll be fun. All right. Thank you. All right. Bye.
