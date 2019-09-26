# Copyright transfer statement

MEL CHUA hereby irrevocably transfers and assigns to DONALD STUFFT in perpetuity, all right (whether now known or hereinafter invented), title, and interest, throughout the world, including any copyrights and renewals or extensions thereto, in the attached transcript of the interview recorded between us on AUGUST 7, 2019 in A LIVE-TRANSCRIBED ONLINE VIDEO CHAT.

# License

I, Donald Stufft, hereby release this work under the following open license: http://creativecommons.org/licenses/by/3.0. Anyone is free to share and remix the work as long as they cite it. I consent to the open publication of this work using my name.  

# BEGIN TRANSCRIPT

MEL: Okay. So is it okay to start the official recording mark here?

DONALD: Yep. Whenever you’re ready is fine.

MEL: Cool. So we’ll start saving the transcript at this point. And to start out with… Can you describe your involvement in PyPI? How would you characterize your position with respect to it?

DONALD: Currently or over time?

MEL: Both.

DONALD: So currently I’m effectively technical lead for PyPI, I guess, is how I would describe it. It’s Open Source, so we don’t have official titles or anything, but I’m at least one of the technical leads, if not the technical lead. And I’ve sort of evolved into that position over time, where originally I was just sort of this outsider, trying to contribute to it. And, you know, I got the Commit Bit set, because Richard got tired of me emailing him patches, and then he stepped back and I sort of started to take over at that point. It just kind of evolved from there.

MEL: And when was that transition? When did you get the Commit Bit, roughly?

DONALD: I could look it up, but I want to say probably around 2012, 2013.

MEL: That’s… That’s enough precision. And so for the past seven-ish years, six, seven years, you’ve been leading the technical development?

DONALD: Yes. And, like, when I originally got the Commit Bit, I wasn’t necessarily leading the technical development at that point. It just sort of evolved over time, to where I started taking on more ownership and getting involved more, and people started to trust my judgment more. And it just sort of… I sort of stepped into that role. Over that time period.

MEL: Okay. And I know with Open Source projects, there’s not necessarily a specific day of transition, but maybe what year or so would you consider yourself to -- in hindsight -- this is when I started acting pretty much as the technical lead, as opposed to one of many contributors to this?

DONALD: Probably… Around 2014, 2015?

MEL: Okay. So fairly early in the process, it seems like, then. And some time ago, too.

DONALD: Yeah. And part of that was because at the time, it was basically just me and Richard. And Richard was already wanting to step back. And most of the other people involved were sort of… Commenters, and not necessarily people who were working on actual code changes. So obviously we’re Open Source. Everything gets discussed out in the open. So they would comment on issues. Say how they thought it should be solved, et cetera, but very few of them were actually, you know, putting pen to paper and writing code. So I had a wide latitude, because I was the one actually implementing things.

MEL: Mm-hm. Yeah. The do-ocracy kind of thing.

DONALD: Yeah.

MEL: And… And this was not your day job?

DONALD: Not at that point.

MEL: Okay. And when did it become… Is it your day job now? I’m actually not sure what the situation is with you and PyPI and work.

DONALD: Yeah. So I get roughly two days a week dedicated to Python packaging. To spend on PyPI, pip, discussions, sort of… Amazon just sort of writes that time off, and says: This is Donald’s time to contribute to these Open Source projects.

MEL: Cool.

DONALD: Previously, before that, when I was at HP, I was full-time on Python packaging.

MEL: Okay. And then that would include the PyPI work as well?

DONALD: Yes. And in that time, I was… I mean, I wasn’t exclusively on PyPI, but the vast bulk of my time at HP was taken up by PyPI.

MEL: Okay. Do you have a sense of like -- at what point PyPI became part of something you did for work, as opposed to something you did on the side, outside it?

DONALD: Yeah. So I started working… I actually just pulled it up to refresh my memory. I started working at HP May of 2015. And that was when it became part of my day job.

MEL: Cool. Okay.

DONALD: My entire day job, at that point.

MEL: That’s really cool. And so before that, everything was outside work? On the side?

DONALD: Yes.

MEL: I’m just thinking about the timeline -- you sort of took on the technical lead role a year or two before you had it be a formal part of your day job.

DONALD: Yeah.

MEL: Okay. Cool.

DONALD: And part of taking on… I guess history-wise, part of taking on that technical lead role was also… I started effectively reimplementing PyPI. There was a lot of problems with the old codebase. So I started saying… Okay. We need to throw out this old one. Start over. And since I was the one at that point, again, doing the work, I was also the one making a lot of these decisions about what PyPI is going to look like into the future.

MEL: And (inaudible) was that the (inaudible) transition already?

DONALD: Yep.

MEL: Okay. So this is really helpful contextual historical background to have. I want to sidestep for a moment, and we’ll come back to the history in a bit. I want to sidestep for a moment and ask: When we use terms like “sustainable” or “well maintained” for an Open Source project, what do those words mean to you? Different people have different criteria for it, but if you were gonna make a checklist for: What does it mean for a project to be sustainable, if it has A, B, C, D, E, what would that list be?

DONALD: Yeah. So… I think part of being sustainable is being able to cover sort of any ongoing operating cost. Now, for a small client-side project or library or something, the operating cost could be super small. Maybe even just a server for a website or something like that. But a project like PyPI, operating costs could be fairly significant. Off the top of my head, I believe we’re over… A million-some dollars a year in, quote-unquote, “costs”. For hosting. Then you start adding in my time, Ernest’s time, Dustin’s time, et cetera. The actual -- again, quote-unquote “cost” of PyPI is quite high.

MEL: Yeah.

DONALD: We serve a significant amount of traffic. And that is difficult to do cheaply.

MEL: And would you include people time in the operating costs? If you’re writing PyPI’s budget, would you put you and Ernest in there?

DONALD: So I would call it operating cost. I’m not a business person to know this is CapEx or OpEx or whatever. I would consider people costs part of operating costs. And again, that’s sort of the “keep the lights on” kind of operating cost. 

So we get a security issue on PyPI, we have to respond to that. PyPI goes down. We have to respond to that. We don’t have an official Pager Duty, but the people with access to sort of best effort are on call for it. So yeah. We’re not gonna leave our daughter’s recital or anything to fix it, but we might choose not to go out to eat or something, if it’s down. 

And for smaller projects or client-side things, the sort of ongoing operational cost of people time is gonna be significantly less. Because you’re not operating a service. You’re publishing artifacts. But you can still have problems. Like… You might have a dependency that publishes a new version that then breaks… Whenever people install your project, it breaks things, and that’s sort of an operations issue at that point. And that can require time to sort of go in and fix it. You know, and that’s sort of the cost of just keeping the lights on, making sure everything is still functional for what it is today. 

And then, beyond that, you have sort of feature/enhancement work, which is sort of adding new features, you know, responding to changes in the ecosystem, bugfixes, et cetera, that are easier to cut out, and they’re easier to get volunteers to do. But they still also involve a lot of… Unfun, necessarily… I don’t want to say unfun. I’m not quite sure of the exact wording. But the sort of emotional labor to get across the finish line. You know, doing reviews and handholding people who might need help, and the sort of things where most programmers enjoy programming, but they might not enjoy these other things, and feel forced into doing them, I guess.

MEL: Mm-hm. What other things would you say make a project sustainable? Or criteria for -- is this sustainable? Yes/no. You’ve got operating cost…

DONALD: Yeah. So outside of all the financial costs of doing all this, another big part, I think, is sort of the bus factor problem. If you have people depending on a project, you want to know that -- if this person loses interest, or quote-unquote “gets hit by a bus”, or whatever, that it’s going to continue to be maintained and worked on into the future. 

And oftentimes, that just means you need to have more contributors, but then getting more contributors involves attracting more people, it adds more overhead to the project than the sort of one-off thing that I just kind of do a little on the side, kind of thing.

MEL: Okay. Any other sustainability criteria?

DONALD: Um… I mean, those are the big things that come to my mind.

MEL: Okay. And “sustainable” versus -- another term that’s come up a lot is to be “well maintained”. Are those two different concepts? Or are they…

DONALD: So I guess it depends on specifically what it means to be well maintained. If well maintained just means sort of… There’s people there to address issues, to make sure it’s keeping up with changes in the ecosystem, that sort of falls under sustainability, to me. 

If it’s getting down into more of… You know, are they following best practices? You know, are they doing the right things? And these are more fiddly opinion-based things. I wouldn’t personally lump that under sustainability, but I suppose those questions could have an effect on sustainability, because if your review process is just a complete bear and intimidating to get through, it might not be “well maintained”. You know, but then that’s going to then affect your ability to be sustainable, because it’s gonna require more effort to maintain and keep the project going. So it’s sort of a gray area, in there, I guess. Whether or not that’s overlapping or the same or what have you.

MEL: Yeah. I mean, they seem to be related in some way. And you described some of that possible relationship. And what would your criteria for “well maintained” be?

DONALD: So a well maintained project should generally be able to keep up and respond to incoming issues. At least on a triage level. 

They should be able to handle urgent issues in a relatively timely manner. You know, again, depending on how urgent they are, if you’re openSSL, and heartbleed hits the internet, you know, within a day, this little side project… You have a bug, it might crash things, in certain cases -- within a couple weeks, you know, sort of depending. 

And also just sort of keeping your processes, and your overall code structure, style, tooling, up to what a modern contributor would expect. This is a problem a lot of older projects have, where they set up… This is what our workflow is. This is our tooling and everything. And this is all modern today. And then ten years later, everyone has moved on to something different, and now there are fiddly things. They’re still using this. Why are you still using this? And nobody has put in the effort to update that to the sort of modern tooling, so then it becomes increasingly harder to attract contributors to that project.

MEL: Anything else on the “well maintained” checklist?

DONALD: No, I think that’s about it.

MEL: Okay. So kind of jumping back to the history part of this, thinking about PyPI as an Open Source infrastructure project, and in terms of how you would tell the story of its sustainability and its “well maintainedness”, over the years you’ve been involved -- what would that narrative be?

DONALD: Yeah. So when I first got involved in PyPI, there were two PyPI administrators. Richard and Martin. Martin had largely stepped back, though. And Richard was wanting to step back, and sort of felt guilty, and couldn’t. It was… The codebase itself was a mess. 

So the history of PyPI is that PyPI pre-dates every modern web framework in Python. So… It pre-dates WSGI. Sorry, I think it is a contemporary of WSGI. If I’m going back in my history. But… So PyPI originally was not a WSGI service. It has no web framework whatsoever. 

It just sort of is proof of concept that Richard wrote one evening. Or one weekend. That then eventually came on to be production for every Python programmer. 

But so… Basically nobody knows how to contribute to PyPI, until you spend a significant amount of time digging into PyPI’s codebase. And that codebase was not very good. Again, this pre-dates modern practices and thoughts on unit testing and code structure and what-not. So PyPI was roughly… The bulk of PyPI was contained in two files. Each of them were about 3,000 to 4,000 lines long. And it had almost no unit testing or testing whatsoever.

MEL: Oh god.

DONALD: And at some points in its time, you have to -- to run it locally, you had to actually comment out bulks of -- parts of the code to make it run locally. So at that time, this is where test PyPI came from. The way you worked on PyPI is you just sort of committed code. Pushed it to test PyPI, to see if it broke. And then if it didn’t, you would push it to PyPI and hope that PyPI and test PyPI’s production environments had not drifted enough apart that now it would now break in PyPI. Which did happen. Or just that the amount of traffic and varying traffic PyPI got was different, and would also break it. 

So when I sort of stepped into the project, and got involved, I figured out how to -- you know, I figured out the whole mess of the codebase. And at that time, there were approximately two people on the planet who understood PyPI. Me and Richard. Three, I guess. If you count Martin. But he wasn’t involved, really, anymore. So there were two to three people on the planet who currently understood PyPI. 

And PyPI was growing. It was originally sort of this service. It ran on the same box that ran the normal Python.org, SVN, all of the Python.org services were just sort of on the same box. When we got some servers donated to us, I believe, is what happened… We put them into OSU/OSL, and we started putting services in there on VMs, so PyPI got its own service. It was still primarily running on this one server, but it was a dedicated server at this point. 

That’s when Ernest started contributing at that point. So he started digging into the codebase some, to sort of increase the number of people who understood it out more. But still relatively few number of people. Over that period of time, I experienced a number of people who seemed like they were excited to -- wanted to get involved. They would open up the repository, and I would never hear from them again. They would just get completely scared away.

MEL: And the difficulty of contributing -- was that because of what you mentioned earlier? That there was no web framework to it?

DONALD: Right.

MEL: No structure that people would already understand from previous projects?

DONALD: Right. (inaudible) support got bolted on to PyPI. But it was basically just this huge hackish codebase that evolved over -- I think the original PyPI got written in 2003. I started getting involved around 2011, 2012-ish era, so at that point, about ten years. And it just… Nobody knew how to work on it, because it was completely custom. 

So at that point, I was like… Okay. I’ve had exactly zero percent success getting anyone else helping to contribute. Besides Ernest, but Ernest was originally paid to help on some of this stuff, as a part-time, I believe, ops person, and then he transitioned to volunteer -- who was helping out. And then now he’s paid again. But so basically… No one was successfully converted from “Hey, I want to help!” To actual contributor. Richard stepped back, so it was just me, and PyPI was sort of steadily growing.

MEL: And this was 2014?

DONALD: Say it again, please?

MEL: That was 2014-ish?

DONALD: Yes. 2013, 2014-ish. Yeah. So roughly around that point, and if it’s important, I can find the exact timeline in my email somewhere… I essentially said… Okay. We need to do some heavy refactoring of PyPI to make it modern. 

I spent about a month trying to do that. And so I concluded that the codebase was just so bad that there was no salvaging it. Like, trying to do anything effectively was rewriting the whole thing anyways. And we had no unit tests. So any change we made broke things every time we deployed, basically. 

So I was like… Okay. We’re gonna start this over from scratch. Taking what we’ve learned here, and really focus on making it something that is significantly easier to both get new contributors on board -- because bringing in new blood, I believe is… I forget if I mentioned that. But it’s part of sustainability. Being able to attract new people. And making it easier to maintain. And sort of solving these best practices problems. And also just making it possible to run it locally, without commenting out code, would have been nice. 

You know, so that’s when I started Warehouse. And my memory is a little hazy. I think I started Warehouse before I was at HP, and it was a sort of side project that didn’t get a ton of attention, because I was doing it in my spare time. I went through several rewrites of Warehouse in that time period. 

As I was just playing with different frameworks, and trying to decide: What does the sort of technical overview of this thing look like? PyPI is weird. We have… At that point, a decade-old database that people had just sort of added things to at random. So things like the Django ORM wasn’t powerful enough to support our database. We just couldn’t use it. I think now it could. But… So trying to find a thing that actually worked for this gnarly old codebase. 

And then I started working at HP, where I dedicated time to work on it, and I got, you know, sort of the first 80% of the project written, to where it was done. It was hosting things. People could use it. And it was sort of deployed side by side. And then we got the Moz grant, which allowed us to hire Dustin Ingram, and Nicole [Harris]… Now my brain is refusing to remember her last name.

MEL: I can look it up.

DONALD: To… Work as contractors, to have the sort of -- again -- dedicated time to work on this. And that’s sort of what made it possible. Well, and Sumana, to handle the project management stuff. That’s sort of what made it possible to get the second 80% done, and push it over the finish line to where we could actually deploy it, and redirect production traffic to it. 

And since then, we’ve gotten additional grants. And continued funding additional work on it, to add new features and stuff. And that’s sort of where we are today.

MEL: So going back a little bit to when you started thinking… Okay. We’ve got to do the rewrite. And you started Warehouse… And this was still a side project, spare time thing for you…

DONALD: Yep.

MEL: Was there anyone that you had to convince? Like… Oh, we need to do this. Or was it just picking stuff up and starting to make things happen?

DONALD: So my history with PyPI is a little weird. So my first actual involvement with… My first major involvement with packaging is me getting mad at PyPI and saying: I could do better! And setting up a competing service. So I’ve sort of been trying to rewrite PyPI from the get-go, in some fashion.

MEL: Do you remember what you were mad about?

DONALD: Sorry, say again?

MEL: Do you remember what you were mad about?

DONALD: Oh, it went down. I believe it was just downtime. And then I spent… I remember, because I joke about it, because it was Christmas Eve. I had bought a domain name and I hacked together a basic hosting service that would just sort of suck in everything from PyPI and rehost it. And be better in ways like… Hey, we have a valid HTTPS certificate. We have a web UI -- just Twitter Bootstrap’s framework, but it looked relatively modern, instead of old PyPI’s horribleness. And things of that nature. 

And then, in doing that, I started submitting patches to PyPI, because I had discovered things that just weren’t working. And then Richard sort of got tired of… And I didn’t want to learn Mercurial, which is what PyPI’s VCS was, so I would just literally send patches to Richard. And he got tired of me mailing him patches, and gave me Commit Bit. So it was sort of from before I was even a committer to PyPI, I was trying to replace it. 

But to answer your actual question of whether I had to convince someone, I mean, I talked to Richard, and he was on board. But there was no one who was really a decision maker, to say: Yes, we’re gonna do this. Or no, we’re not gonna do this. I just kind of said: I’m going to do this! And did it. And nobody stopped me.

MEL: Yeah. And I think that one of the reasons that we’re trying to look at this as a case study for Open Source digital infrastructure/sustainability is that in a corporate environment, that is not how that happens, typically.

DONALD: Right.

MEL: So the picking up and doing stuff, and then… You started the Warehouse rewrite. And then you got hired by HP, and this became part of your day job. And did you continue having that sort of autonomy? At any point, did people start saying: Well, now you have to do it this way…

DONALD: Nope. In fact, when I went to HP, I said: I work on these projects. Do you expect to have control over them? Because if you do, I’m not interested. And again, when I came to Amazon, same basic thing. 

You know, that was important to me. Was that any place I went would not expect to be able to exert undue influence over these community projects. I mean, that’s the way I view them. They belong to the community. They don’t belong to me. They don’t belong to my employer. They belong to the community. And I am -- and my employer -- is just contributing to them. 

Both places were extremely on board with my… Sort of gave me free rein over what I do with those projects and when, and obviously if there’s some specific problem they’re having, I’m happy to go through it and look at it closer, because they’re my employer, but I wouldn’t allow them to dictate: This is how it’s gonna be solved! Or even that it’s going to be solved. Because if I disagree that it’s a problem… They’re out of luck. 

So -- like at HP, I joke about it sometimes -- they essentially just sort of stuck me in a corner and left me alone. I was hired by what was officially the Open Stack team. Because Open Stack is written in Python. And with sort of the directive to just go make Python packaging awesome, because Open Stack cared a lot about Python packaging. But, like, my manager -- I told him what I was working on, but that was about it. I had zero oversight, whatsoever. Beyond just sort of telling my manager what I’ve been doing.

MEL: Cool. So this fits really well into what I know about Open Source culture and corporate culture and how people have made that work with jobs at companies that may not be exactly -- not Red Hat, for instance.

DONALD: Right.

MEL: Can you talk a little bit about… If your employer -- why was this so important? What kind of impact would it have on PyPI’s sustainability as an Open Source project, if your employer were to say: No, no, we do want to have control over this as a product?

DONALD: I mean, I would not have gone to work there. And I wouldn’t have had that time available to me. In all likelihood, Warehouse probably would not have happened, or, like, it might just now be getting to the point where it was years ago. You know, depending on how much of my free time I was willing to dedicate to it. Like a lot of programmers, I tend to be somewhat obsessive about my work. My wife calls herself “an Open Source widow”. So, you know, it likely would have still gotten done. It would have taken longer. And it would have been at greater personal cost to, like, me and my family.

MEL: Mm-hm. And so the… I guess what I’m hearing here, in terms of the relationship between sustainability and day job is that… The particular arrangement you had with your day job, with the autonomy you had, with the freedom to participate in it, I want to use the phrase “as an Open Source project”, “as an Open Source contributor”... Let you move PyPI forward. The arrangement with your day job made PyPI more sustainable, because they basically gave you time for it?

DONALD: Right. Absolutely. Like I said, one of the things about -- what at least I consider a project sustainable -- is that they have head count, effectively. We’re Open Source. There’s no real head count. But they effectively have a head count to say: We’re going to make sure this thing still works tomorrow. We’re gonna add new features. We’re gonna keep up with the ecosystem changes. All these things. And by giving me 40 hours, paid, a week, I mean… Again, I obsess. It’s more than 40 hours.

So it was more than 40 hours. But by paying my bills, essentially, it allowed me to dedicate that time. I was then able to respond to security issues, respond to pressures that come from just PyPI growing. And work on these sort of green field, pie in the sky ideas for how to make PyPI more sustainable in the long run. 

Like, the whole Warehouse project was a non-trivial undertaking, to sort of… I don’t remember the traffic stats from the day we cut the switch, but we served one to two petabytes of traffic a month. So… 

And the history of PyPI is there was basically no documentation, or really designed API. The API that pip and everything uses is completely accidental. It’s twelve layers of hacks on top of each other that have just now been ingrained as… This is our API! It’s why we have a really weird one, where it’s like HTML pages and not JSON or XML. It’s just… You have to scrape with a parser that says HTML, because the history of how PyPI evolved, there was no API. And we just kind of added one without telling anyone. 

And so sort of going through and figuring out -- untangling -- what is an implement detail that we can change? What do we actually have to replicate over into this new thing? When there’s no documentation, no unit tests, no sort of expectation of what needs to and should work, other than the entire bulk of code that interacts with PyPI and what they expect? Which obviously -- we can check to make sure if pip and setuptools still work, but I have no idea what random projects have put in their own personal repositories, when you hit PyPI, and what corporate companies have done to hit PyPI, and what they expect or not. 

It’s a really silly example, but at one point, there was a compatibility hack in PyPI that would add commented-out HTML that was like an HTML table structure, because I believe it was… Setuptools had a regex that would look for the table structure to discover links, and we moved away from using tables, but it only used the table structure, so we would just put the table structure in there and comment it out in the HTML. So it did nothing to the browser. But it was enough to trick setuptools into thinking the API hadn’t changed.

MEL: I’m not super… I’ve been around software long enough that I’m not surprised, but I’m still like… Oh! Okay!

DONALD: Yes. The history of PyPI’s API is really interesting. Like, PyPI originally had no file upload, no API, no nothing. It was essentially links that were designed for humans to click on, that might be a file at the end, or might be another website that had the file on, and you were expected to just sort of manually click around and find the file you wanted and download it. 

And then setuptools came along and added easy install, when you wanted to download these things, so it just sort of automated scanning of the UI of PyPI. It wasn’t an API. Just the UI of PyPI, to discover any link it could, and see if it kind of looked like a file. Then it would then go fetch those pages. If they were HTML pages. And scan those, looking for files. And it would just do this with, again, the literal UI of PyPI. 

At some point, that was causing additional bandwidth, because it was downloading HTML that was like the login box and images and what-not. So they made what they called the “simple API”, which was just… We’ll take a list of links, because that’s what setuptools is looking for, and reproduce it into -- this other page that’s not meant for humans. It’s meant for setuptools, and then we can just change the URL that setuptools looks at, and it would just sort of work without having to change this deployed structure. Or this deployed client. And then that’s been hacked on over the years. So yeah. Our API essentially was defined by setuptools scraping a UI, designed, like, 15 years ago.

MEL: Wow. A little bit of a tangent from that. We were talking about how HP both gave you the ability to improve sustainability, but also giving you to the project improved its sustainability in the first place, because you’re a head count, in that sense.

DONALD: Yes.

MEL: And then you mentioned before, but at some point you went from HP to Amazon. So with that transition, how would you feel that affected the sustainability of PyPI as a project? Head count jumped from one place to the other…

DONALD: Yeah, I went from full-time to part-time on PyPI. So that obviously reduces the head count by half or something. It’s not half, but… Partial head count, essentially. And then I still work on it in my spare time and discuss things, and what-not. So on that level, that has hurt the sustainability. 

However… The good side of that is: Because of the work that went in, and the additional people we’ve brought on, the project is healthier now than it was back then, so that me changing my job did not… Like, I don’t want to say adversely affect it, because yes, it did technically adversely affect it, because there are less people on it, but the project was still able to move forward and continue to evolve, and continue to exist without any major issues. Even though I now had reduced time on the project.

MEL: And that’s a good sign of a really well maintained, healthy project, that it’s not just hanging on one person.

DONALD: Right. And one of the things that I… That has made me the happiest about the state of PyPI today is that there are major features added to PyPI that I know nothing about. I’ve touched them zero amount. I don’t know anything about them. There are parts of the codebase that I don’t know… That I don’t have in my head, because I’ve never looked at them. And, you know, that sounds weird. But the fact that other people are able to get in there and work on it and become experts on their own part of the codebase, and are able to implement these features without my fingers having to be in all those pies… Makes me feel like -- on the sustainable side of things -- that the sustainability goals of Warehouse were a success.

MEL: Yeah, and you were talking about the bus factor, as a sustainability criterion earlier.

DONALD: Right. If it were technically my job, you know, one of my goals was to reduce my job security. But with Open Source, it’s more like… Make me able to focus elsewhere, if I want to. Or continue to focus here, if that’s what I want to do. 

Like, one of the things that I’ve thought about when I was doing this, was -- Richard, way back when, basically, like, he didn’t want to work on PyPI anymore, but he felt guilty, like he had to continue to work on it, because he was the only one there doing things. And talking to him about that had struck me. That was one of the reasons why I started Warehouse. Was to make sure that wasn’t me, ten years later.

MEL: And do you feel like it’s on track for that to not be you, ten years from now?

DONALD: Yeah. I feel like if I stepped away now, the project would continue to run. I don’t plan on stepping away. I still enjoy it. But I feel like if I wanted to, I could. And I mean… I think any time you have someone step away from a project, who was heavily involved, there is some level of… Oh, now how do we handle this or this or that? Now that someone filling those shoes is gone. So I don’t want to say, like, oh, I could just disappear tomorrow and no one would notice. But it’s possible for me to transition away, if I wanted to. Which to me is a huge success.

MEL: Yeah, that is really big. Yeah. Did you always feel that way? At whatever point in time, were you like… Oh, shoot. If I get hit by a bus tomorrow, this project is screwed?

DONALD: Oh, absolutely. Like I said, there was a time where there was, like, charitably three people on the planet who understood PyPI’s codebase. And I was the only active person who… I was the only one active of those three. And we don’t have an SLA, but if PyPI goes down, people can’t work. People can’t deploy things. 

I’ve joked before that I’ve never officially been on call for PyPI, but I’ve been de facto on call for a decade now, because as soon as PyPI goes down, every public communication mechanism I have, people start pinging me on. People I don’t even know. Just because my name has now been associated with PyPI for so long that people have figured out who I am. And they just start pinging me. Like, one time I remember PyPI went down, somebody looked up my cell phone number off of like Whois records or something, and started texting me on my cell phone, telling may PyPI was down. So I have to get pretty far out in the sticks before I’m not effectively on call for PyPI. 

And part of the way we structured Warehouse, too, was to reduce that operational burden, to make it as possible to run a service as massive as PyPI is with what is a pretty skeleton crew. We have no full-time operations person on PyPI. I’m part-time on “packaging”, which means if an operations thing happens, I can spend paid time on it. And Ernest works at the PSF, but he’s not dedicated to PyPI. He has a lot of things he does. So he has paid time, but again, not dedicated to operating PyPI. And that’s, like, it. And as far as any sort of paid time to make sure PyPI is running in five minutes from now… Or responding to issues, or, like, S3 died or whatever.

MEL: So if before, you were going off to… If I disappear, this is really bad, now it’s like… I think I could transition out, and it would be okay. When did that start changing?

DONALD: Um… So… Probably it started changing I want to say around the time we got the MOSS grant. Having other people who had paid time -- even though theirs was contract-based, while mine was salaried. So theirs was more finite, in terms of when it ended. 

Although every single one of those people stayed on and continued to work on things after the contract ended. So they ended up volunteering. 

But at that point, once there were people who were dedicated to working on this thing, I had given them Commit Bit, so I said: You’re a part owner of this now. Do good things! That’s when I started to feel like… Okay. Maybe I can, like, not touch things and it’ll be okay. And sort of over time, as the other people involved have sort of become leaders in the project, in their own right, it feels like someone would fill in those shoes, if I did step back.

MEL: I think this might actually be a good point for us to wrap up. And append this to next time, if there is a next time. This is awesome, all this history and insight. 

So what’s gonna happen is we’ll do three interviews in total. But for the second and third one, one of the things that I’m gonna do is bring back bits from the stories that other people are telling about… Here’s PyPI’s story from my perspective. And we have people both involved in the MOSS grant stuff, but also people who are outside users of PyPI, the service, who talked to me about the development and what their impressions were and how much they knew about the stuff that was happening. So given that, is there anything that you’re curious about, or anything that you want me to pay attention to asking people or pulling in for you, for next time?

DONALD: I mean, nothing comes to mind. If I think of something, I’m happy to reach out. And if there’s anything you guys want to know for clarification, or whatever, you can reach out to me any time as well. One side effect of being around packaging for as long as I have is I’ve become sort of a keeper of the lore. So, you know, there’s a lot of things that historywise… That exist in my head and I probably should write down at some point. Because I think it’s interesting. But, you know, is it necessarily relevant to actually maintaining or running of the service today?

MEL: Yeah. Any of that lore, any of those things that you want to make sure we capture, just -- and I want to make sure that I tell this story -- and then you can make sure to get that here. Cool. That’s all I have. Once we get the rest of the interviews going, then I’ll approach you again about scheduling the second round. That’ll be in about a month or so.

DONALD: Okay. Sounds good!

MEL: Thanks again. This was fantastic.

DONALD: No problem!

MEL: So I’m gonna email you the transcript in a bit, and then when you’re ready, I’ll put instructions in the email, but just basically email back and say: Now I think it’s ready to be under a Creative Commons license, and we’ll take it from there.

DONALD: Okay. Sounds good.

MEL: All right, cool. Have a fantastic afternoon.

DONALD: Yep. You too.

MEL: Bye!

DONALD: Bye. 

MEL: Thanks, Mirabai!

MIRABAI: My pleasure, as always! See you!
