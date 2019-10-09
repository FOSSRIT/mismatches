# Copyright transfer statement

MEL CHUA hereby irrevocably transfers and assigns to TERRI ODA in perpetuity, all right (whether now known or hereinafter invented), title, and interest, throughout the world, including any copyrights and renewals or extensions thereto, in the attached transcript of the interview recorded between us on SEPTEMBER 25, 2019 in A LIVE-TRANSCRIBED PHONE CALL.

# License

I, Terri Oda, hereby release this work under the following open license: http://creativecommons.org/licenses/by/3.0. Anyone is free to share and remix the work as long as they cite it. I consent to the open publication of this work using my name. 

# BEGIN TRANSCRIPT 

MEL: That’s good. So… New transcript start line is now. PyPI interview round two. And so this is the one for… I show you a bunch of excerpts from interviews… In this case, it’s gonna be the three participants we have who were part of the Warehouse migration. And because we’re doing open science, yay, I can tell you their names and you will probably recognize all of them. We have Nick Coghlan, we have Donald Stufft, and we have Ernest Durbin III. And I will spell Nick’s name. (edits transcript to correct spelling) There we go. 

So… The first bit I have -- and this is a little bit of a remix. So you’ll see the interviews interspersed, as if it were a dialogue, because these are bits and pieces of them telling the same story together, more or less.

TERRI: Mm-hm.

MEL: And the first… Bunch of excerpts I have is… PyPI problems. So I’ll paste it in here, in italics, and then when you’ve read it and you’re ready, just go ahead and start responding with whatever comes to mind.

> _Source(s): Ernest-1, Nick-1, Donald-1_
> 
> ERNEST: So PyPI is, as a service, something like 17 years old.
> 
> ...[it was] effectively a pet project at the time. It was… Hey, can we do this? And then they went for it, right?
> 
> NICK: [The first PyPI developers] ran up the proof of concept. The PSF put it on a server and said, here's this thing. Then people started putting more and more projects on it. Then it was like, oh, well, people are actually using this thing for real. (Laughter) I guess we better keep it working…
> 
> ERNEST: ...over time, PyPI grew sort of... Exponentially.
> 
> DONALD: PyPI pre-dates every modern web framework in Python. So… It pre-dates WSGI... 
> 
> ERNEST: ...there weren’t any of the fancy modern day web frameworks.
> 
> DONALD: It has no web framework whatsoever. It just sort of is proof of concept that Richard wrote one evening. Or one weekend. That then eventually came on to be production for every Python programmer.
> 
> ERNEST: There were a lot of regular outages. There were sort of… It was common, I guess, for changes to go out that broke things unexpectedly. There were, like, two working tests for the service.
> 
> ...It had features like SSH for uploads to bypass the fact that, you know, it didn’t have TLS for a really long time.
> 
> ...Sort of the best monitoring that it had was: Is PyPI working or not? Like, can I get to it? And so over time…
> 
> MEL: Literally can you go to the web page and see it?
> 
> ERNEST: Yeah, effectively. 

TERRI: Well, two tests is better than a number of other services. That sounds like a lot of other software projects I’ve been involved with and many software projects I even see at work sometimes. [Edit note: these are not final production-ready versions at work!]

MEL: Yeah. So this is fascinating. Because in your first interview, you used the word “magic” and “magical” when talking about PyPI. Like… It works! I think it’s good!

TERRI: That’s how people treat all of the projects I’ve seen… I’ve seen this happen a bazillion times, and often when we go back to review a project that we’re gonna use they’re like… Okay. What state is it in? How is it before we use it? 

Everyone tells us it’s magical and we go and look and there was one that had one test for an entire subsystem, and the test was: Does it compile or not? And then it always returned True. And we had an entire thing built on this thing!

MEL: Oh my gosh.

TERRI: So yeah. I don’t see conflict between it being a strange, organically grown Open Source thing that eventually got stable enough for people to trust it and the fact that I’m calling it magical. That happens to me all the time. 

I mean, to be fair, I feel the same way about Mailman, we -- I’ve been through the organic process of what works and what doesn’t, and people still just sort of assume it’s magic and are very disappointed if it turns out it’s not.

MEL: That’s a challenge with infrastructure work in particular. It’s like… It’s even more magic than your usual magic.

TERRI: Yeah. I mean, maybe the magical part is that it’s just, like, grown. It’s a spontaneous emission of software!

MEL: Yeah. Something like that. So, I mean, looking at this, anything that’s surprising? Anything that, you know, when you’re talking about… How do you feel about PyPI and sustainability? You and actually all of the other downstream folks we interviewed, which was Naomi Ceder and Jackie… Kazil? (Tries multiple pronunciations of Jackie’s last name) Jackie?

TERRI: Yeah, I know Jackie.

MEL: Okay, yeah. So all three of you went… “I think it’s pretty good?” Question mark. More or less. In contrast to Donald, Ernest, and Nick, going… “Well, there were the trouble times.”

TERRI: Yeah. That’s fair, though. I love that it pre-dates all the web frameworks. I had a conversation with someone just last week about doing things before we had calendar functions. And Go actually has the same problem, where their calendar functions are relatively new, and it sounded very familiar to 1995 PHP or whatever it was. Maybe it was Perl I was using at that point! 

I wonder… I wonder now that I’m thinking about it… How many functions had to be grown because of PyPI and other software that was used, because in some ways, growing it organically is… At least you know what you want when you want it. You don’t have to guess in advance. You just sort of… Add in the bits you need when they happen. 

I guess that’s sort of how Agile is supposed to work sometimes. I don’t know that I’ve ever seen it work quite the way that Open Source does. 

But what do they say? The scratching the itch method of software requirements gathering. I need this right now. So I’m making it. And no concept of what else is going in there.

MEL: Yeah. So I mean, this is really amazing, to see… Not just the contrast between the upstream answers and what you and Jackie and Naomi said, but also the contrast between… Maybe not the contrast. The first time we talk, and you’re going… “Yeah. PyPI seems pretty good. I feel like it’s had uptime, whenever I wanted to use it.” And then now you’re looking at Donald and Ernest and Nick talking and you’re like… “Oh, well, yeah. Okay!”

TERRI: The funny thing to me is that it doesn’t make it feel any less like it’s good. It just took a long time to get there. Maybe that makes it better, if it has to take a long time to get there!

MEL: Huh. So… I’m trying to figure out how to frame this and understand this. And I’m not surprised at it, because I think I had the same reaction myself for projects that I used, but as an engineer, I know how some of that sausage gets made, and it’s kind of ugly, sometimes. Messy. How do you reconcile the Donald-Ernest-Nick stories of… “Oh, man. And things were going down. And it was not good.” Where sort of your experience of… Probably around the same time, going… “Yes. This works for me!”?

TERRI: I’m not even sure I was using it in… Whatever year they said that was. 20 years ago now? I’ll scroll back up. Yeah. 17 years ago. I’m not sure I was even using it in the beginning. I may not have started using it until it was stable enough. I don’t know.

MEL: Hm. Well, even… So scrolling up a little bit, Ernest said -- something like 17 years old, and then Donald… I’m gonna see if I can pull up his interview to have in a different tab… He had… This is the wonder of having all the transcripts and searchable text on your computer. 

So Donald got involved around 2012, 2013. Which I’m pretty sure is after you had started using it for quite some time.

TERRI: Yeah, definitely. I mean, I was developing software in Python starting around ‘98. So I don’t know when I first would have used the whole PyPI service. But probably… A couple of years after that. So I guess that probably is around the same time. You’re right. Maybe I never noticed it was down. I had a dial-up modem then.

MEL: Hm. Oh, wow. Yeah. That would probably… I’m also looking at what Ernest said, as I pull up his transcript. And he said… Let me copy it to you. Because I can do that. Let’s see.

> _Source(s): Ernest-1_
> 
> ERNEST: And so somewhere around 2012 or 2013, PyPI was starting to really show its age as a service.
MEL: So Ernest put that date 2012-2013. And then I’m looking… Okay. I have one. This is Ernest again.

> _Source(s): Ernest-1_
> 
> ERNEST: I guess if we were on a scale of one to ten, I think when it first showed up on the scene, it was probably somewhere in the five and six range. It was a small service. It wasn’t doing a whole lot. I mean, at that point, it didn’t even actually host packages. It was literally just an index.
> 
> And so it probably started as a five or six, and slowly, over nearly ten years, sort of degraded to like a one or a two, if that. On maintainability.
> 
> And then slowly sort of crept… It begrudgingly climbed back up to like a three or a four, maybe. Just as we sort of kept PyPI -- the initial implementation -- on life support, effectively, awaiting Warehouse.
> 
> And then when Warehouse deployed, I would say it rose to what I would consider a nine or a ten. You know, basically with the deployment of that service and the turning off of the old servers.
TERRI: On life support, yeah.

MEL: And if I sort of do the math a little bit here, he said: Started ‘05-’06, over several years degraded to a 1 or a 2 [out of 10 in terms of sustainability]. If it’s about 17 years old, which matches up with everyone’s timelines, starting around 2002-ish, then ten years after that would be… 2012. Would be when it degraded a lot.

TERRI: Yeah.

MEL: To what Ernest is calling a 1 or 2. Badness. And that is also around the same time Donald got involved, and Donald started out with… “I got involved because there was a bunch of downtime and I was mad.”

TERRI: Yep, scratching that itch. It’s funny. I don’t even remember there being downtime. And I definitely would have been using it around then. I was in the middle of writing my thesis. But I was… I was definitely… I was definitely involved in the wider Python community, I think. In fact, that’s probably around… What, ten years ago? That’s around when I was first doing Google Summer of Code, and I was working in Python even when I wasn’t working for the Python Software Foundation. 

So… I’m actually sort of surprised. So even though it was apparently an unmaintainable mess and was going down, I wasn’t seeing it often enough to remember it. 

And equally, like, I was bringing in Summer of Code students, who usually find everything. They encounter every horrible bug, because honestly, a lot of our bugs are kind of the broken stairs. Everyone knows how to go around them, and you bring in a bunch of students and they step on the broken stairs. 

I couldn’t even remember the students complaining about that. I remember my early students having trouble with their own internet connectivity. Maybe that was masking it. 

No, to be honest, I guess I was maybe lucky? Maybe the team that was propping it up did it fast enough that I was busy doing exams at the time they were doing it or something? Yeah. That’s kind of funny. 

MEL: Yeah, I’m also surprised. I’m like… Oh, jeez. How could this have worked out? This is I think a bit more for amusement than anything else. This is Donald’s description of him getting involved in 2013, because he was mad about downtime. At the exact same time period you’re describing.

TERRI: Yeah. Well, clearly Donald got involved faster than I noticed. He is the hero of the story. Which actually is… Probably true. Certainly before I even met Donald, that was how people described him, as the hero who saved PyPI.

MEL: Yeah, okay. So this is the origin story of Donald, the Hero of PyPI.

> _Source(s): Donald-1_
> 
> DONALD: My first major involvement with packaging is me getting mad at PyPI and saying: I could do better! And setting up a competing service. So I’ve sort of been trying to rewrite PyPI from the get-go, in some fashion.
> 
> MEL: Do you remember what you were mad about?
> 
> DONALD: Oh, it went down. I believe it was just downtime. And then I spent… I remember, because I joke about it, because it was Christmas Eve. I had bought a domain name and I hacked together a basic hosting service that would just sort of suck in everything from PyPI and rehost it. And be better...

TERRI: We can make it a Hero’s Journey. Now I kind of want to write a children’s book. That would be a great children’s book. Donald, the Hero Who Saved Python.

MEL: I think that would actually be a hilarious product of this particular research project. I think I have to actually write a formal report and stuff.

TERRI: Yeah, this will be the remix of all the transcripts. Will be the Hero’s Story. I’ll be selling it at next PyCon. I’ll test it on my kid. Though if it doesn’t involve dogs, he’s not gonna be interested. To be fair… I’m gonna say there’s a whole… There’s a whole niche market for nerd-related kid’s books. We own several now. 

My husband came home from a conference with Kubernetes for Babies, which is actually great, because I didn’t know the basics of Kubernetes, and having it explained as a picture book was awesome! At the time. And I think that was when I was pregnant. I don’t think we even had a kid yet. 

But the best one I have is one called Goodnight, Server Room, which is adorable. If you ever need to buy a gift for nerd parents. That’s the best of the nerd bunch. But yeah. We have a few now. So clearly I need a Python one! I don’t know of any Python ones yet.

MEL: Yeah. In all seriousness, I wonder if this might solve one of the other problems that came up in all the first round interviews, which is… Getting information to people is hard. Because there’s a lot of it, and most of it’s boring, so we ignore it.

TERRI: That is definitely true. My earliest involvement in Python was actually writing the documentation for mailman, because I was tired of explaining to people on the Linuxchix lists  how mailman worked, and if no one else was gonna write the documentation, well, I guess I will. My first couple of commits were very heavy on the documentation. I maintained that for quite a number of years until I found someone else who is now maintaining most of it. So clearly I should go into children’s books. You know. From mailman documentation.

MEL: Yeah.

TERRI: People are always surprised that it had been around for so long and we hadn’t had up to date documentation for 2.1 until it had been out for several years before I came along. It was like… Hey, we need some updates!

MEL: Dang.

TERRI: That used to be… In fact, I still sometimes get emails about that. 

But it was one of the best negotiations at my university. So one of my profs… This is completely unrelated to Python, but related to how Open Source works, one of my profs taught me early on that knowing a bit of information and connecting people was very essential to getting anything done at the university. 

And so one day he traded the knowledge that I had written all the mailman documentation in exchange for… I forget what from the IT team in my department. And I became fast friends with them, because I could answer all of their mailman questions. It was actually pretty good. But I was like… I’m going between being really mad at you and realizing the value of my knowing that I could just walk down the hall and ask the person who wrote the documentation what it meant! 

Mailman is still very popular among universities, because the documentation is relatively easy for them to customize for their mailing lists. And it was designed that way on purpose, because I worked with them on it!

MEL: Wow. I did not know that little bit of history.

TERRI: Yeah, completely unrelated to Python, but definitely a sign of how personal connections sometimes make a bigger difference than anything we did technically.

MEL: So we’ve got a little bit of a choose your own adventure. I have a couple of excerpt types I can put on to you. Based on a couple things you mentioned in your last interview. So I’ll let you pick. 

So option number one is… The way that employment plays into the PyPI story. And sustainability. 

Option number two is: Here’s an example of a technical detail that we fixed in the migration to Warehouse. Kind of ridiculous. 

Option number three is: Let’s talk about making it easier for people to contribute. That’s a really important factor. 

Option number four is: Actually PSF stuff behind the scenes of getting ready to have a grant of this magnitude, and have money to fund an effort of this magnitude and manage it. 

And so I think I’ll start with… Those four options. Any of those seem particularly compelling to you?

TERRI: I want to know about all of them. Let’s start with… Let’s see. Option two. The technical details. Now I’m curious.

MEL: Okay. One moment. And this is mostly Donald. Actually, this is all Donald.

> _Source(s): Donald-1_
> 
> DONALD: And the history of PyPI is there was basically no documentation, or really designed API. 
> 
> ...Like, PyPI originally had no file upload, no API, no nothing. It was essentially links that were designed for humans to click on, that might be a file at the end, or might be another website that had the file on, and you were expected to just sort of manually click around and find the file you wanted and download it. 
> 
> And then setuptools came along and added easy install, when you wanted to download these things, so it just sort of automated scanning of the UI of PyPI... to discover any link it could, and see if it kind of looked like a file... And it would just do this with, again, the literal UI of PyPI. 
> 
> At some point, that was causing additional bandwidth, because it was downloading HTML that was like the login box and images and what-not...
> 
> So they made what they called the “simple API”, which was just… We’ll take a list of links, because that’s what setuptools is looking for, and reproduce it into -- this other page that’s not meant for humans. It’s meant for setuptools... So yeah. Our API essentially was defined by setuptools scraping a UI, designed, like, 15 years ago.
> 
> ...It’s why we have a really weird one, where it’s like HTML pages and not JSON or XML. It’s just... You have to scrape with a parser that says HTML, because the history of how PyPI evolved, there was no API. And we just kind of added one without telling anyone.
> 
> ...The API that pip and everything uses is completely accidental. It’s twelve layers of hacks on top of each other that have just now been ingrained as… This is our API! 
> 
> It’s a really silly example, but at one point, there was a compatibility hack in PyPI that would add commented-out HTML that was like an HTML table structure, because... Setuptools had a regex that would look for the table structure to discover links, and we moved away from using tables, but it only used the table structure, so we would just put the table structure in there and comment it out in the HTML. So it did nothing to the browser. But it was enough to trick setuptools into thinking the API hadn’t changed.
> 
> And so sort of going through and figuring out -- untangling -- what is an implement[ation] detail that we can change? What do we actually have to replicate over into this new thing? When there’s no documentation, no unit tests, no sort of expectation of what needs to and should work, other than the entire bulk of code that interacts with PyPI and what they expect?
> 
> Which obviously -- we can check to make sure if pip and setuptools still work, but I have no idea what random projects have put in their own personal repositories, when you hit PyPI, and what corporate companies have done to hit PyPI, and what they expect or not. 
 
TERRI: (laughing) That’s amazing. I love the HTML table. Oh my goodness.

MEL: Yeah. When Donald was telling the story, in the back of my mind, I’m going… Yes. This is in fact a software project. That’s what happens.

TERRI: Yep. It’s actually funny nowadays, because we have all of these systems, and people often are like… Well, why don’t you just use JSON? And the answer is almost always… Because it didn’t exist when we started.

MEL: So this excerpt from Donald -- this story -- is, one, hilarious. But again, with that, he’s sort of pulling aside the curtain of: Yeah, PyPI. Kind of hacky.

TERRI: Yeah. I had not realized that setuptools and PyPI were not exactly designed together. That it was… Setuptools was like… Hey, I can just automate this thing so you don’t have to click links by yourself. That’s kind of amazing. I had always assumed that setuptools had been designed to line up with something in PyPI. 

It was designed to line up with something. Just not… Not directly. Just scraping. Web scraping is great. 

To be fair, a lot of Python is very web scraping-y. I was so excited last year when they told us that we finally reached the point where we got as many data science projects -- data science Pythonistas as we had web Pythonistas. Wow. We’ve made the next step in our evolution. We might not… You know, die if everyone decides they want to have apps forever now. 

And I say that snarkily. I work on W3C committees. I know we have a bazillion HTML5 apps under the hood. But I do less web scraping than I think I used to. 

My whole thesis was in the end… Wound up… Utterly relied on Beautiful Soup, which is another project that I know is one person, and I don’t know what we’ll ever do if he decides he doesn’t want to maintain it. There are so many things dependent on that code.

MEL: So with any of this… Does this prompt any thoughts or reflections on Open Source infrastructure sustainability? With the story that Donald is telling here, or… Beautiful Soup is another example of… Yeah. I know that guy, in fact.

TERRI: Yep. So… One of the things I was doing for work that I mentioned last time was reviewing a whole log of Open Source projects. And the number of times that people would say… Hey, I’m using Beautiful Soup or I’m using xemacs was one… And they would be like… Yeah, this is well maintained. It’s super professional. It’s totally fine. We’ll be able to use it no problem. 

And I was like… I know the dude who maintains it! He does it in his spare time. And he’s a nice dude, but he has a day job. 

The one that’s been going around… I don’t know if you’ve seen… There’s a story about Curl, which has been maintained by one guy for 20 years, and apparently, he got a request to go and visit a company site, and they were not really interested in paying for that. 

So… I think that happens a lot in Open Source. I mean, that’s part of why we’re having all these conversations about licensing and whatever the name of that… The JavaScript library that was showing ads on the command line… So that people would know that they actually needed money. And it’s horrible, because I made the mistake of reading some of the comments, and everyone was completely appalled. But how else are you going to know? I know from watching these things, that no one does! 

And we were talking… I forget who I was talking to. But the point at which we started to realize that maybe we should give some money to the openSSL community, that it was also a side project.

MEL: Yeah.

TERRI: So I guess… Going back to Donald’s story… I mean, none of it is surprising, and yet somehow it just… Software keeps on. It’s kind of astounding, really. Where, like, the dubious backends of evolution, where you wouldn’t think that just random chance would just get you what you want, but somehow it does!

MEL: Yeah. So…

TERRI: I guess we always want to believe we have careful design when we have an organically grown… What do they call the… The design pattern? Oh, the Ball of Mud design pattern. Where we just sort of slap some mud on the side of the thing and it all stays together. As long as people keep slapping mud on the side, it’s fine.

MEL: And maybe it’s this mental pattern of… We’re gonna assume that this is beautifully designed, as long as there isn’t something that whacks us upside the head and forces us to think otherwise. We’re just gonna keep assuming. For you, it was… Oh, every time I want to use it, it’s there. Therefore, everything must be beautiful.

TERRI: Yeah. And I don’t know… Maybe it’s just our inability to have really complex mental models for software we don’t have to care that much about. You only have to build a mental model of it if you have to maintain it yourself or design it yourself, and otherwise it’s easier to assume everything is beautiful, like we saw in college. 

Maybe they should just teach us that all software is terrible right from the get-go. Screw this requirements gathering and all of these fancy Agile processes, and just teach us that no matter what you do, it’s just a bunch of patches strung together that sometimes work, and if you’re lucky, people will keep contributing, and if you’re unlucky, they will go and get new jobs. 

It does speak a lot to… You know, having corporate support and employment. Maybe we should go to the employment section. That might be the next one to move on to. Whatever that one was. Option one.

MEL: Yeah. So I pulled this one for you, because you mentioned that one of the first things you found out about PyPI other than… “I assumed it was magic…” Was when you went… “Oh, jeez. Donald is doing this as a side thing?” And so here we go.

> _Source(s): Donald-1_
> 
> DONALD: Yeah, I went from full-time to part-time on PyPI. So that obviously reduces the head count by half or something...
> 
> We’re Open Source. There’s no real head count. But they effectively have a head count to say: We’re going to make sure this thing still works tomorrow. We’re gonna add new features. We’re gonna keep up with the ecosystem changes. All these things. 
> 
> ....by paying my bills, essentially, it allowed me to dedicate that time. I was then able to respond to security issues, respond to pressures that come from just PyPI growing. And work on these sort of green field, pie in the sky ideas for how to make PyPI more sustainable in the long run.
> 
> MEL: [Asks about Donald’s arrangement with his employer regarding PyPI work]
> 
> DONALD: ...when I went to HP, I said: I work on these projects. Do you expect to have control over them? Because if you do, I’m not interested. And again, when I came to Amazon, same basic thing. 
> 
> You know, that was important to me. Was that any place I went would not expect to be able to exert undue influence over these community projects. I mean, that’s the way I view them. They belong to the community. They don’t belong to me. They don’t belong to my employer. They belong to the community. And I am -- and my employer -- is just contributing to them. 
> 
> MEL: [What if your employer didn't support this kind of arrangement?]
> 
> DONALD: ...I wouldn’t have had that time available to me. In all likelihood, Warehouse probably would not have happened, or, like, it might just now be getting to the point where it was years ago. You know, depending on how much of my free time I was willing to dedicate to it... And it would have been at greater personal cost to, like, me and my family. 

TERRI: Oh, that sounds familiar. Not that I know this story. But the thing of -- every time you go to a new job, giving them a list and having them clear them with the lawyers and everything. 

A large portion of the reason that I took the job at Intel is I gave them my list of things and they said… Yes, we just need to decide which one of these we need to pay you for and which ones just need to be filed. 

And everywhere else would take months for the lawyers to get back to me, because they had no idea what to do with them. And most of them came back and said… No, you have to drop all of these. 

I had one offer of employment -- with a company that later became very Open Source friendly, but wasn’t known for it at the time -- and they told me that I had to quit doing Google Summer of Code. Which is just mentoring. I’m not even writing any code. I’m just talking to people. And they wanted me to quit a month from the end and just abandon it for someone else to do. At that point, it was probably still around 100 mentors and 30 or 40 students counting on me to finish it out. And their lawyers thought that was fine. They were completely shocked when I turned down the job.

MEL: Yeah. Wow. So…

TERRI: It’s always funny to me when… I talk to students all the time. They often ask about interviewing, and they’re like… Well, what do you do if you get an offer and they only give you a week to respond? And I’m like… That’s never been an issue for me, because it takes months for their lawyers to get back to me, so I’ve never only had a week to respond. Just work on a lot of Open Source projects and you can gum up the entire system, where they have you over a barrel. 

I’m not the best at giving employment advice, clearly. Well, maybe I am. Depends on what you care about in life. If you care about Open Source projects, knowing the team you’re gonna work with is hard.

MEL: And I think one of the interesting bits about this particular research project is that one of the audiences is gonna be people who… Corporations or foundations or large institutions with money… That care about Open Source, because their services run on it now. But don’t know quite what to do to support people that work on these projects. They go… Oh, this means paying people. And it’s a different kind of interface and culture than they might be used to.

TERRI: I know. We try to hire as many of the people as we can ourselves, so that we can have bigger influence in the direction and, again, make sure things are working. 

But I know a lot of companies that just sort of throw some money at the Linux Foundation or whatever, and hope that magic happens. And I guess it must happen well enough that they feel comfortable with that. Because a lot of them have been doing it for years. 

We always joked a bit about some of these foundations just being money laundering for paying Open Source people that you couldn’t afford to hire yourself, either because of culture fit problems or they didn’t want to work for you or they didn’t want to live in the US or whatever. We often joke about a lot of our big foundations as money laundering for companies who want to support Open Source but couldn’t do it directly.

MEL: There’s some truth to that, though. We have different kinds of systems, different kinds of cultures. And how do you bridge that sort of interface mismatch? Sometimes it’s throw money at a foundation. They’ll be that bridge.

TERRI: Yeah. And sometimes it just frees people to do development without feeling quite beholden to a bunch of corporations. 

It’s super helpful, sometimes. I definitely know plenty of people who have worked for the various foundations, and the intellectual freedom and not having to worry about the next reorg deciding that their Open Source project would be dead… Is definitely a benefit to that. 

That’s one of the unfortunate side effects of being in a corporation. The Open Source projects I work on here are great. But if I leave or if someone gets reorged, or if they decide they want to productize something, they could go away, and I don’t have the same control I have over my personal ones. 

Thankfully, I do work at a corporation that lets me do both. So I basically let them know when I’m starting a new Open Source project and give them first dibs if they want to have an opinion about that. And then go do my thing if I want to go do my thing.

MEL: I’m getting over a bit of a cold on this end. So one thing I also wanted to show you… This is a little bit of a different… (coughing) Excuse me. Jeez. I’m gonna drink some water. 

So this is… Maybe interesting from a board perspective. This one is from Nick, and this is the backstory of… If I had to give it a name, I would call it something like: How the PSF became ready to write the Mozilla grant. So a kind of behind the scenes.

TERRI: That one doesn’t seem nearly as likely to be a children’s book. Although maybe it should be. We can teach children about getting funding! 

> _Source(s): Nick-1_
> 
> NICK: ...the whole other side of what brought us to the Mozilla grant in finally making the warehouse migration is the PSF side of the story.
> 
> There was a project to do a refresh of the Python.org web presence... The PSF put out a request for proposals...
> 
> There was one where essentially the quality of the prework that had gone in was spectacular, but the operational proposal for actually getting the job done we didn't think would fit in with the PSF's nature as an all-volunteer organization. It was clearly structured around working with a full-time project manager on the client side...
> 
> Then there was another -- the winning bid was one where the pre-work wasn't as strong but the operational proposal was a lot better... However, that was a project where the management on the PSF side was completely volunteer run. And so, when we're reviewing the bids, one of our comments was [that] the weak link here is not the contractor. It's management on the PSF side because this is a big project. It's a complicated project. Trying to do it with all-volunteer management is going to be tough.
>
> Now, one of the mitigating factors was the winning bidder had a very well-known profile community member working for them... [but then] The project lead on the PSF side had life happen. It was a case of -- so essentially, that project stalled for a long time... it was not a smooth journey.
> 
> I think that was one of the factors that led to when the Mozilla grant for PyPI was sent, the grant said “we will pay a professional project manager to actually be part of this process and actually be the PSF's ongoing management”.
> 
> ...The process has changed a bit since that first proposal because again this is just growing organizational maturity on the part of the PSF, which is essentially the -- after the funding is secured, the PSF will actually put out a request for proposals to make the thing. There's that side of the process that's become a bit more open. We just had to do it differently on the first one because it was -- to make a credible proposal to Mozilla, we had to have a very concrete idea of how we were going to spend the money, which meant having the contractors lined up before the grant went in, rather than finding them afterwards. After having that first grant done, you get a better idea of what things cost... 
> 
> The other thing there was having that understanding of, yes, you need to budget for project management. Yes, you need to budget for UX work, and you need to budget for the underlying engineering work to actually make the service go.

All right. So that’s a story I hadn’t heard. That’s not too surprising. I know the PSF didn’t have a whole lot of management. I know from Sumana that project management was definitely a gap there. But I love that it had to be included. And we had to realize that it needed to be included before we could make it happen.

MEL: I’m throwing a lot of information at you right now, but there are a lot of complex angles on this thing we’re talking about. PyPI as an Open Source digital infrastructure, sustainability, case study. There’s the technical side -- we have Donald’s story of -- look, a table. We have to leave it in! The organizational side, which is… The Nick bit just now. 

So do any of these things, thinking back to… When you’re talking about, in the first interview, what does sustainability mean to you, what does maintainership and being well maintained mean to you… Do any of these prompt thoughts about digital infrastructure sustainability and how we might understand it or what the gaps in our understanding or awareness might be, or what we might do?

TERRI: This actually reminds me of when we were looking to maintain LinuxChix’s infrastructure. And we had a bunch of people offering servers, but trying to get an appropriate number of sysadmins was surprisingly hard for an organization that you think would have a significant number of people who were sysadmins already.

MEL: I’m wondering… I might have been on the mailing list at that time. I might have been an undergrad. I remember that vaguely.

TERRI: I was an undergrad and eventually I became one of them for a while. But for LinuxChix, it was hard… I think for the same reason it’s hard for us to get mentors for core Python. The people who had the ability and could wrangle getting the hardware into a data center where they had access to it and everything… Didn’t have the time! 

I mean, in the end, what happened is we got hardware donated and time donated, and hosting donated, all from separate entities. 

And the only person… We did have one person who offered to do it all. But no one felt comfortable having a single person maintain it all. Even though she was very capable and she could have done it. But they wanted to make sure that we continued to have a collective, because that was how it was structured. 

It’s kind of funny, now that we’ve just been talking about how many things really do just have a single person, that we were concerned about that. But yeah, we were.

MEL: I think this might be a good segue… Go ahead?

TERRI: It was a lot of different pieces to make that happen. I had forgotten about how difficult that was.

MEL: And I think it also says something about the different kinds of stories… How does Open Source infrastructure work? So the story you just told is a little bit more of an implementation one. But some of the same issues popping up -- you’re talking about the bottleneck of one person, how do we coordinate resources, even on a much, much smaller scale. LinuxChix is not PyPI, by multiple orders of magnitude. And yet… Same themes.

TERRI: Yeah. And one of the things about Open Source has always been that it’s pretty good at attracting programmers. You know. We could attract a wider range of them. We could attract a more diverse set. 

But it’s not really great at attracting project managers, for example. And part of that is because nobody wants to be told what to do with their spare time. So it’s really hard. I mean, what do they say? Herding cats. It’s probably even more true in Open Source than in general software. But that’s got to be an incredibly thankless job, to try to wrangle people. 

So instead we put the project management part of the job on someone who’s originally there to do technical stuff. And is doing architecture and project management. So they get all the kudos from the community but then they also have all these other jobs to try and get things done. 

I mean… I was talking about that with another team here. About an Open Source software release, and not knowing when it was gonna happen, and you know, that we had to be comfortable with that. 

And I was reminded that Python as a whole has one of the stronger sets of release cadences. Not Python itself, but because of the sprints at PyCon, almost all the projects that are gonna do a release are gonna be really tempted to do it in the week after PyCon. After the sprints. When they’ve just fixed all their bugs and brought in new contributors and everyone’s got energy. 

I think maybe the sprints at PyCon are addressing some gaps we would otherwise have in management and figuring out timing and figuring out deployment and figuring out… You know, interoperability between things. Just because everyone is sort of… Well, not everyone. But a large number of people are available in a set of 20 rooms for a couple of days.

MEL: Huh. So you’re not the first person to bring up project management as a gap. And a gap that contributes to sustainability or lack thereof. But PyCon is a forcing function. That’s something I haven’t really thought about before.

TERRI: Yeah. It’s sort of unique among the different programming language communities I’m in. A pretty decent number of people stay for the sprints, and I went to PyCon the first year, just for the sprints. I didn’t even get to go to the conference because I didn’t realize I needed to sign up so early. 

And the second year, I also forgot I was supposed to sign up so early, but when I asked to be put on the waiting list, I first got an email saying… “There is no waiting list.” And then I got an email saying… “Oh, we know who you are. It’s okay. I reserved a spot. Go register.” That was pretty funny to me. I had no idea that the person in question knew who I was, and would think I was important enough to want me there. But that was nice of them.

MEL: There was one last set of excerpts I did want to show you. And it might be a nice wrap-up to this. And this is… Talking about the Warehouse rewrite as the… “Gee, we’re having problems getting new contributors to this. Maybe that will fix that.”

> _Source(s): Donald-1, Ernest-1_
>
> DONALD: Basically nobody knows how to contribute to PyPI, until you spend a significant amount of time digging into PyPI’s codebase. And that codebase was not very good. Again, this pre-dates modern practices and thoughts on unit testing and code structure and what-not. So PyPI was roughly… The bulk of PyPI was contained in two files. Each of them were about 3,000 to 4,000 lines long.
> 
> ...there were approximately two people on the planet who understood PyPI['s codebase at the time]. Me and Richard [Jones]. 
> 
> ...I was like… Okay. I’ve had exactly zero percent success getting anyone else helping to contribute. Besides Ernest [Durbin], but Ernest was originally paid to help on some of this stuff... No one was successfully converted from “Hey, I want to help!” To actual contributor.
> 
> ERNEST: ....there wasn’t a good open door that any developer could sort of walk in and do anything with PyPI. It was very difficult to run locally, to sort of make changes and play around. 
> 
> DONALD: ...you had to actually comment out bulks of -- parts of the code to make it run locally...
> 
> ERNEST: ...since there weren’t tests, it was really hard to verify that you hadn’t completely screwed up some other feature that you didn’t realize.
> 
> DONALD: ...we had no unit tests... The way you worked on PyPI is you just sort of committed code. Pushed it to test PyPI, to see if it broke. And then if it didn’t, you would push it to PyPI and hope... 
> 
> ....I concluded that the codebase was just so bad that there was no salvaging it. Like, trying to do anything effectively was rewriting the whole thing anyways.
> 
> So I was like… Okay. We’re gonna start this over from scratch. Taking what we’ve learned here, and really focus on making it something that is significantly easier to both get new contributors on board...

TERRI: That sounds somewhat familiar! That’s part of why mailman underwent a rewrite. Explaining the weird mental model you needed… In order to contribute to it -- it was a bit of a problem. That’s why Barry said “okay, we’re done.”

MEL: And also… In a way, that ties into… What did you call it? The mud ball architecture?

TERRI: Yeah, the mud ball architecture. Although I can’t say that mailman is entirely a success story there, because we have this thing that’s completely rewritten, but everybody wants to use the old version, because it looks the same way as it did in the 90s and they know how to use it. I probably need to write some more documentation. It worked in the 90s.

MEL: There we go.

TERRI: We’re actually taking part in the Google Summer of Docs, with mailman. I haven’t been super involved. It’s someone else who’s doing that. So maybe that is going to be a path to a different type of sustainability in Open Source, is bringing in paid document writers for the first time this year.

MEL: Huh!

TERRI: That’s kind of why I got so into doing Google Summer of Code. It gave me a cadence for… All right. I’m going to have a hundred people come and try to use this code and ask me questions about it. Now is the time to update all my docs, triage my bug queue, do all of the project management stuff that I do for mailman, basically. You know. Fixing things. 

Finding a bunch of easy bugs for people to start on. So they could feel like they’ve done something right from the beginning. Finding -- updating the setup stuff, because mailman is multiple services now, so it’s actually a real pain to get it started. 

And it used to be that I would do that just before PyCon. Because we would get new contributors there. 

I would do it just before Google Summer of Code would start. Which was really only a couple of months before PyCon. So they sort of blurred into one single thing. 

And then I would do it again just before Grace Hopper. Because I used to do a hackathon at Grace Hopper for that. Which used to be… The first year… I think it was ten of us in a conference room. And now it’s well over 200 people, and I’m no longer involved. 

But it was sort of an excuse to get… We thought… Hey, this conference is full of young women, many of whom have never contributed to Open Source but would probably be game for it, if they had an intro. And that’s what we did. We built a day where they would get an intro. And they would get those key couple of commits to say… Look! I’m an Open Source contributor now! 

I have to say that first commit can be a huge hurdle. My first commit for mailman was an image. Barry wanted a save icon. I was like… Okay. I can draw a 16x16 pixel image. I have no artistic skill in that direction, but I can handle that. 

By the time I was done, this was again back in the 90s, when most people had contributor licensing agreements, by the time I was done signing all the necessary paperwork with the Free Software Foundation and getting a thank you letter in the mail signed by Stallman, which was cooler then, because I didn’t know anything about him… By the time I had done all that, I was like… Well, I guess I’d better contribute something else, because that was a lot of work for 16 pixels by 16 pixels! 

That’s when I started on the documentation. And once I was doing the documentation, I was like… Well, this thing is terrible to document because it’s stupid. Why don’t I just fix the code? 

And so in my experience, that first commit, that getting over the hurdle and doing all the necessary to be a contributor, was the slippery slope into Open Source. So I always… I try to give that option to a bunch of other people. 

Hopefully it’s not quite as slippery a slope for some of… I’m now working in Open Source. I do security for Open Source. I talk about Open Source non-stop. 

But, I mean… Setting it up so that it’s easy for other people to get in is… Has been a large portion of my social Open Source contributions, I guess. My non-code and documentation and stuff. But I guess even when it is code and documentation. The goal is often a social one, for a couple of times a year. 

And I say all this, but I got lazy and just contributed to someone else’s project at PyCon this year. It was a completely different experience. It was very fun. I was like… Wait. You mean I could go to a hackathon and not spend a month preparing beforehand? This is amazing!

MEL: Yeah, that’s a weird experience! I made that transition myself, and it’s actually quite lovely.

TERRI: Yeah. It’s really quite fun. To be fair, it’s fun doing the prep the other way too. Because then I’ve got all these things, and I’ve got these great shiny new bugs that I’ve fixed and made easy for you to do, and then I get to see people actually fix them and actually work with them, and actually read the documentation, and give me immediate feedback. 

So it turns what could otherwise be a very solo pursuit into something where I have immediate gratification from actual humans who enjoy or don’t enjoy and can help me fix the things that I’m doing. 

So… I wouldn’t say I like one more than the other, although I will say that not doing all that with a toddler was a great idea this year. It was really convenient.

MEL: Yeah. Well, we’re at the end of our time for today. I know this was a lot of information dump. Do you have any other thoughts or burning statements or questions around any of the things that you’ve seen today? Any of the things we’ve talked about? Anything else around Open Source and digital infrastructure and sustainability thereof?

TERRI: I probably have a bazillion things that I’m gonna be thinking about all day. I guess I want to say that it’s kind of just nice to know that this sort of has a happy ending at the end. 

Because certainly seeing the path it takes to get there… That was never really guaranteed, I guess. 

I mean, I guess it still isn’t. There’s still work going on. I saw the call go out for the code signing stuff and I’ve had a lot of discussions with people about that one. But I’ll bet you’d have a very different study if we looked at a project that didn’t pull itself together somehow.

MEL: Yeah. One of the reasons we picked PyPI as a case study is so we could go… “Well, that worked out!”

TERRI: Somehow! It worked out but it was never guaranteed to work out. That makes it an especially interesting story. Again, children’s novel.

MEL: And I mean, also, this may end up happening, because I draw comics and stuff. So who knows! 

So… We’ll do the thing around a transcript approval and open licensing that we did last time, and then for the third and last interview in the series, it’ll be a little bit less of an information dump and we’ll come back and just have more time to talk about sustainability and infrastructure. I think looping back into the definitions that other people put in. 

And is there anything else that you’d like to make sure that we touch on for the last conversation?

TERRI: Not off the top of my head. Although I did learn the easiest way to get me to verify the transcript was to put it on my work calendar and set myself an hour to do it. So I’ll try to do that again and get it back to you a lot faster this time.

MEL: That works! Okay. And then separately from this… I’ll put this at the end of the transcript, because it’s a happy thing. You mentioned a happy ending. I have some bits from the upstream devs, talking about… And this is what the happy ending meant for us. So I’ll put that out there, and then I guess that will be the closer for this. And then you’ll get an email with “please approve this transcript” soon.

TERRI: Great. I’ve got a block of time on Friday already for you. So hopefully that will work out.

MEL: Awesome. Thank you. I will try to clean it up before then.

TERRI: And if not, I’ll find time next week.

MEL: Yep. I’ll put this in here. This will be the end of the transcript. You can respond. We can pick up there at the start of the third interview and go… So what was that like?

TERRI: Sounds great.

MEL: Thank you so much. I’ll do this and then end the call.

> _Source(s): Donald-1, Ernest-1_
> 
> DONALD: ...one of the things that I… That has made me the happiest about the state of PyPI today is that there are major features added to PyPI that I know nothing about. I’ve touched them zero amount. I don’t know anything about them. 
> 
> ...And, you know, that sounds weird. But the fact that other people are able to get in there and work on it and become experts on their own part of the codebase, and are able to implement these features without my fingers having to be in all those pies… Makes me feel like -- on the sustainable side of things -- that the sustainability goals of Warehouse were a success.
> 
> ...Because of the work that went in [for Warehouse], and the additional people we’ve brought on, the project is healthier now than it was back then, so that me changing my job [and going to half-time on PyPI] did not... Like, I don’t want to say adversely affect it, because yes, it did technically adversely affect it, because there are less people on it, but the project was still able to move forward and continue to evolve, and continue to exist without any major issues. Even though I now had reduced time on the project.
> 
> ERNEST: And so the current picture for the project is that it... ranks pretty high on maintainability from a development perspective.
> 
> There is extensive test coverage.
> 
> There is good documentation for a lot of the common operations a developer has to undertake.
> 
> There’s a very big issue tracker. It’s well classified...
> 
> There are... good automated tests. And good specifications for what the service is supposed to do.
> 
> So with that, it provides the ability for nearly anyone who has the basic skills to contribute to the project...
> 
> Also, we have a continuous deployment pipeline that gets changes out to production on a very regular basis. I think we’re well over 1200 deployments since PyPI launched two years ago, or more. I can’t remember at this point. We passed the 1,000 deployment mark, I think, a little bit after it had been deployed for a year.
> 
> So it’s reliable, it has good metrics as a service, which helps for maintainability as well, from an infrastructure administration, sysadmin-type perspective. And so we’re able to keep tabs on it really well.
> 
> ...And then, you know, I think generally it was sort of a morale boost, I think, for both the people working on the service and for the community as a whole. You know, there was a lot of excitement around the new PyPI, et cetera. Which I think was beneficial. Right? It’s just positive. It was a nice injection of happiness and excitement into the community...
> 
> ...Because I think there was always a lot of excitement at the opportunity to contribute to PyPI. But it wasn’t necessarily something you could just do. Right? You couldn’t take your skills and apply them immediately. There was a lot of… There were barriers that didn’t need to exist and shouldn’t have existed to that... [The rewrite] built on new excitement and it enabled a lot of existing excitement, if that makes sense.

MEL (typed): Thanks, Terri!
