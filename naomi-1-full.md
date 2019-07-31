# Copyright transfer statement

MEL CHUA hereby irrevocably transfers and assigns to NAOMI CEDER in perpetuity, all right (whether now known or hereinafter invented), title, and interest, throughout the world, including any copyrights and renewals or extensions thereto, in the attached transcript of the interview recorded between us on JULY 29, 2019 in A LIVE-TRANSCRIBED ONLINE VIDEO CHAT.

# License

I, NAOMI CEDER, hereby release this work under the following open license:http://creativecommons.org/licenses/by/3.0. Anyone is free to share and remix the work as long as they cite it. I consent to the open publication of this work using my name.

# BEGIN TRANSCRIPT

MEL: Okay. And is it okay to start the official transcribing record now?

NAOMI: Fine by me.

MEL: Okay, cool. So everything before this point, the transcript will be deleted and not part of the official record. Okey-dokey. So I’ll start out with asking you how you would like to be introduced for the purpose of this project. And so I mentioned that we’re doing a radically transparent research process within the Open Source community. So transcripts are gonna be part of the project. Open under Creative Commons license, probably attribution sharealike (nb: error on interviewer’s part, suggested license is attribution/by, not attibution-sharealike/cc-by), so how would you like to introduce yourself for people who are reading this later on?

NAOMI: Naomi Ceder.

MEL: And how would you describe your relationship with the Python community? And as a user of PyPI, but also thinking beyond that? In the Python community?

NAOMI: Well… I am an event organizer. I’ve worked a lot on PyCon. I’m the chair of the Python Software Foundation Board of Directors. So that’s sort of my relation to the community. In terms of being a user of PyPI, I, like everyone else, I suppose, I use it almost without thinking about it. Both at work, where the team that I lead -- we use several packages off of PyPI, but then even when I’m teaching or working at something -- on something at home -- pip install whatever package you need is just something that I do without thinking about it.

MEL: And do you remember when you started using PyPI? For a lot of people, it’s like… Oh, that was some time ago.

NAOMI: It was some time ago. And since I do remember the times before we had pip and PyPI, I know that there was a time when I started using it. I don’t have any specific recollection, other than… Oh! This is convenient. And I think with pip coming out and being adopted… Yeah. I think that was when I did it.

MEL: So… Before we get into your view on PyPI stuff specifically, I want to ask a couple general questions about FOSS project maintenance. Because I know you have a lot of experience with that. So for you, what does it mean for a FOSS project to be well maintained and sustainable? So there are many possible answers to this question. I’m interested in how you would describe it.

NAOMI: Well… I think “well maintained” suggests that there is not only some activity going on in the project, so that if you go and look at the repository, you can see that there have been updates and bugfixes and things like that. 

And also that particularly major issues have been addressed as well. So there aren’t issues that have been pointed out, say, for the past three years, that have been just sort of left alone. So all of that goes into “well maintained”, at just a glance. 

It’s somewhat harder to know if the group of people doing that maintaining is… If they have, say, the same values or share the values of inclusion, or things like that. Those, I think, also kind of go into that decision. But as I say, quite often it’s hard to know where you are on that. When there are a handful of names, and you don’t know any of the names. But that would be something that I think I would be interested in knowing more about, if I had the option.

“Sustainable”... We worry a lot about sustainability these days, with good reason. I’m not… I’m not sure that there is a one size fits all answer to that, but I think you like to see various people taking on roles, and I think even though it is kind of something that has been commonly accepted, I think the pattern of having just one person who is making all of the decisions on maintaining a project is probably not as sustainable as, maybe, having a group of people who sort of work together. Because when everything rests upon one person, then if that one person, for whatever reason, isn’t really able to step up and do that, then things get pretty strange, I think. So that’s, I think, something that I look at. 

And then I realize there are certain projects where maybe the same person has done it for years and is happy and maybe will do it forever, but I think that’s the exception. So there’s that. 

And I think… I suppose it’s really to the amount of work that is going in. What the proportion is. If there are only a few maintainers, yet there seems to be a lot of activity, a lot of requests for features, things like that, I think that becomes hard to sustain as well. So I don’t have a good answer to that. But those are the things that I think about.

MEL: Yeah. And one of the reasons that we’re asking everyone this question -- because when we started doing this research project, we were looking and we realized that there’s not actually a common definition of what does it mean for a project to be sustainable. And we talk about it a lot. And people say oh, it’s important, but we don’t necessarily know what that means. And we don’t mean the same thing by it, also. Because your [definition of] well maintained and sustainable may be different from somebody else’s.

NAOMI: Absolutely.

MEL: So if you were going to go back and turn those into a checklist -- I’m reading the transcript and seeing a couple of things that you suggested. So for “well maintained”, you mentioned having activity in the project. And is there activity, but also a recentness of activity?

NAOMI: Yes. Yeah. I mean, there are various things that maybe fill a niche that I happen to, like, need to use. And some of those, the activity has pretty much stopped or become very sporadic. You know, two, three, four years ago. Which means that then there are issues that have come up. 

So this is -- I guess this is the countercase, not so well maintained. You go, you discover an issue, and maybe it’s… Oh, let’s say handling Unicode or something like that. And the issue -- you go to the project that you’re using, that you’re relying on. There have been maybe a little bit of activity around the edges, but in essence, development stopped years ago. And there are comments maybe on the discussion session about this problem. There is even a request to fix it. There’s a ticket open, that’s been open for four years, to fix your problem. And at that point… It’s not well maintained. 

And if you really want the fix, then… Okay. You can fix it yourself. And that’s fine. You can even put in a pull request, although that usually involves more work. So if I’m doing this in the course of my day-to-day work, I am sort of stuck, then. I hate to do my own sort of fork and my own private thing for work. But I also hate to spend a couple days of work time getting ready to submit something when I have no indication at all that anybody is even going to look at it and merge it. So yeah. Then you’re stuck. I mean, that’s the countercase. So the opposite of that is what I’m looking for.

MEL: And when you’re looking at activity and trying to figure out… Okay. Is this something I can rely on someone else to pick up on, or something I might be stuck with doing on my own… I was just wondering -- which of these, to you, is more well maintained? A project that is -- every two months, there’s an update, but that seems pretty regular, or [a project where] the most recent thing was two days ago, but then before that was five weeks, and there seems to be this random pattern?

NAOMI: Well, I think that… That kind of depends upon the number of people. And even the maturity of the project. So I’m not so bothered about either of those things. 

I think what bothers me more is that when it seems that things kind of grind to a halt, and then there isn’t any sign of responsiveness from the people who would have the authority to do that. So there are open issues that have no comment on them. There’s maybe a pull request sitting there, that’s been there for a few years, and there’s no response. Or things like that. I mean, it’s that kind of thing that I look at, in terms of whether or not you could expect -- 

I mean, I don’t necessarily believe that somebody needs to stay on a two-month release schedule, if in fact they have a mature product. And they haven’t had any bugs. Why would they do that? But still, you want to have some sign that people are actually reading their mail and responding.

MEL: Okay. Yeah. And you used the word “responsiveness” there. That’s something that we’ve seen in a bunch of places. So looking at some of the other things that you mentioned… Then major issues being addressed, instead of being left alone. And one other aspect -- you talked about “well maintained”. You talked about the people who were involved and the values that they have. And the values of being inclusive and so forth. Could you talk a little bit more about what you mean by that, and how does that fit into being well maintained?

NAOMI: Well, I mean, I suppose, strictly speaking, it doesn’t necessarily have anything to do with the code. But it has to do with the organization, with the group that is doing the maintaining. And I think that if the group is not run in such a way that it is open to input, then I have a couple of problems with that. 

One of them, of course, is that just in a very simple-minded way, if they’re not -- if they’re behaving in such a way that they shut out classes of people, let’s say… I guess I could allude to, like, say the Linux kernel, or things like that. But there are other things, where the environment was such that people were discouraged from contributing. I think on a practical basis, fewer minds willing to contribute is counterproductive. 

And then I think also, just with all of the work and involvement I’ve had, I don’t know if it’s necessarily a maintenance issue, but in terms of: Do I want to use and sort of support a project that doesn’t include everybody? I mean… No. Not really.

MEL: And I think that this is -- I’m really glad that you mentioned this, because like I said, it’s not the code. But when you think about sustainability of Open Source projects, we’re not only talking about sustainability of the code. We’re also talking about the sustainability of the people who make the code.

NAOMI: Right.

MEL: So yeah. There’s the community aspect of that. And so sustainability -- you talked about various people taking on roles. And is that, like, new people coming in and starting up? Or is that roles rotating among members?

NAOMI: Well, I think both. I think that it’s something that in some cases is hard to tell. But I think it is a good sign, if you can see that somebody who comes in with a good idea is welcomed to do more as they feel they can do more. Rather than sort of a gatekeeper type approach. You must be this tall in order to commit to this project, or whatever it might be. So yeah. 

That’s something that is sometimes hard to see. But I think there are a number of ways that you can kind of get a handle on this. In looking at the people who are contributing, as much as you can tell -- do they come from different places? Different countries? Different continents? Are they wrestling with a language barrier? I mean, I think that’s probably a good sign. If they’re wrestle with a language barrier. Because they’re then open to a lot of things. I mean, again, gender. All sorts of things like that. 

You can look at -- if any of those people are welcome to come in and contribute, then I think that’s a good sign. It’s something -- having been involved in Open Source for a long time, it’s something that I think the successful communities do. And that is… Somebody bright will appear on the scene, and amazingly, like it seems like -- in months, they’re already contributing at the highest level. I think probably amongst old timers, there’s a little bit this sort of “get off of my lawn” kind of resentment of people moving in that fast. I’ve seen that too. But I think that having a community that is that open to a bright newcomer is a good sign. A sign of health. A sign of development in that community. 

So it’s fine if you have the same bunch of people rotating, so they don’t get burned out. That’s certainly not a bad thing. But having somebody say: Hey, you know, I really love this, and I can do this thing and this thing and this thing, and then they do, that’s an interesting phenomenon as well.

MEL: Cool. So this part might be a little trickier. So now talking of PyPI, and by the way -- one of the things that we’re looking at is: Infrastructure that people use and take for granted. All the criteria that you were just talking about, about being well maintained and being sustainable -- how possible is it for us even to answer them? 

So if at any point any of the answers to these questions are… You know, I have no idea… That’s actually really good for us to know, because then it also becomes -- okay. And how should we be able to find out, as well? 

So for PyPI, just off the top of your head, first without looking or doing anything, what would you say is the status of PyPI, in terms of being well maintained and being sustainable? As an Open Source project?

NAOMI: Um… So… I think I would say that… PyPI is well maintained. And is sustainable. Maybe neither one of those as much as we’d like. But I think both of those are true. In that if there are issues that you have with PyPI, there is somebody who will respond. 

I think that in terms of their openness to contributions, I think that’s also there. I don’t know that from having checked closely, but I kind of assume that, knowing the people who would be making those determinations. So I believe that’s the case. 

I certainly think it would be nice maybe to have more people involved in the maintenance of that project. I think one wrinkle on that is that of course the PSF is actually paying one of the people who works on maintaining it now. As part of his role with the PSF. And that’s something that I think in my previous answers, I was assuming that everybody was unpaid. So that is is an additional factor that I think maybe gives some more sustainability there, in that it’s not outside of someone’s day job. It is someone’s day job, partly, to make sure that the infrastructure is working, and things like that. 

But historically, I think it’s been… It’s maybe not had as many people involved in the nuts and bolts of it. But I certainly know that several people have been involved one way or another, in helping out. So yeah.

MEL: Have you ever needed to interact with PyPI maintainers upstream? Filing a bug report or anything like that?

NAOMI: I don’t think I ever have, no. Through my role with… As part of the PSF? I have sort of seen those interactions sometimes go on.

MEL: And I’m looking through the definitions and making sure we’re not missing anything. So we talked a bit about activity. Do you have a sense of what kind of development activity is going on in PyPI, as a software project? From the development side, with the PSF?

NAOMI: So… I don’t have a specific sense. But I know that we’ve done things like… There’s been work on the user side of things. Two-factor authentication coming in, and things like that. Yeah.

MEL: And then… I think you mentioned for well maintained and sustainability… So responsiveness to issues. In terms of PyPI as an upstream -- having values of being inclusive and welcoming new people, do you have a sense of that, there?

NAOMI: I mean, at least officially, as something sponsored by the PSF, of course, it operates under the PSF’s code of conduct. And expectations and things like that. You know, more specific than that, I don’t have a real sense of that, going back and forth.

MEL: And… I am not sure how I want to phrase this question, but… Is there more you would like to know? PyPI as a really important piece of infrastructure for the Python community, as this developmental upstream that we just all take for granted, it’s just there --

NAOMI: Mm-hm?

MEL: Is there more visibility that you would like to have into any of these things, the health status of any of these indicators? Or is it like… It’s okay that I don’t know these things? Because I don’t need to know them?

NAOMI: I think… In general, it’s probably… It’s probably okay. I’m not sure that I would expect to have a lot more visibility. I mean, I think -- I guess let me say that I think the reason that I don’t have that visibility is that I haven’t looked. As opposed to it being not discoverable. So I don’t know that I have anything there. 

MEL: And before you got involved with the board, before you got involved with Python at a governance level, how much visibility did you have into issues like that? Like, the legal consideration stuff. We can’t say this. We can’t guarantee that. That would actually be a terrible idea, for legal reasons?

NAOMI: Right. Not very much, I think, actually. I think in the past it was… It was much harder to get that kind of visibility.

MEL: So… Okay. So… what would it mean for PyPI to do better -- or a common example is -- what would it look like if PyPI became quote-unquote “more sustainable”? Or more well maintained? Or more visible at already being sustainable and well maintained?

NAOMI: That’s a good question. I think… It would certainly be good if there were more people involved in PyPI. I think… I think in general, it is well maintained. 

I think that it’s hard to say what it would be that would make it more visible, I guess. As being that. It’s not something that a lot of people really care to spend a lot of time on. If it works, great. And if not, then it’s a problem. 

But in many cases, I guess my sense is that a lot of people don’t really, really want to know the details too much. I mean, it’s sort of like a lot of utilities. I really don’t care about the details of my plumbing. I just care if it works or not. So yeah. I’m not sure what the answer to that would be.

MEL: So now it’s the history/storytime section of this interview. So fairly recently, I want to say… PyPI, in the past, say, two years, has had some pretty substantial development and a fair amount of changes going on. And there’s a lot that’s been going on, both from a development perspective, but also from an organizational structure and… Do these words mean anything fron your perspective? (Naomi nods) 

And the arc of that story -- so first of all, what I’m referring to -- and I’m being very vague here, intentionally, because I want to let you use the words that you have for this. Instead of naming it for you. But sort of… In the past two years, PyPI has done… Stuff. (Naomi nodding on the video) Okay. Cool. And from your perspective, what would the story be of the past two years of “PyPI… Stuff happened!”

NAOMI: (laughing)

MEL: Tell me everything. Everything you know.

NAOMI: Well, I mean, part of it is that… Yeah, I guess it would be over the past two years. Part of the stuff that happened was that we managed to get a fair amount of grant money to supply work on the infrastructure, and working on PyPI in general. 

And that meant, for one thing, we could employ not just a person to work on PyPI full-time, which we did for a while, until we hired them as our infrastructure director for the PSF, but also that we could hire someone to do project management for all of that. So there was a substantial amount of money. And that was put together in ways to actually speed up and improve that development. So that’s why we managed to do a number of things. 

You know, the interface has been new and improved. Various other things, including the two-factor authentication, all of those things have been done to improve both the reliability, in terms of just how those things work behind the scenes, and how they look to the users up front. 

You want exact details of what they did? Again, that wasn’t my department. But that’s the high level view.

MEL: And so… In terms of exact details, I’m curious about: What did you find out, and where did you find it out from? And in what capacity? If it’s like… This is something I only learned about because I’m on the board. Or this is something that I and every other developer I know of became aware of at the same time?

NAOMI: Well, that’s a little bit tricky to say. I know that all of these things were published. I know that they were all published, though, because I was part of the board, and that automatically meant I had an interest in looking at the announcements and things like that. 

So on the other hand, I do remember sometimes only shortly after I knew that… You know, seeing emails announcing this to the PSF Community Mailing List, or seeing tweets about that, or seeing, you know, PSF blog posts about that. 

I think honestly, if I were not on the board, I would not have known about the PSF blog posts. I think that’s something that is sad but probably true. 

But PSF Community Mailing Lists and things like that. So I knew about those things from a user perspective. 

However, I would also say that unless you are in some sense -- have a reason to pay attention, I think a lot of times people I’ve talked to, that I know had access to some of those same channels, had no idea that this happened. Came in on the PSF community list and they glanced at it and put it in the trash and that was it, and it didn’t stick, or whatever that might be.

MEL: And if you were going to make a list of: Here are the things, here are the places where stuff was published -- you said Community Mailing List. Is that a specific mailing list? Or a number of --

NAOMI: I mean, there is a specific -- we have various mailing lists, and I think it went out probably to a number of them, but there is a PSF-community list, that everybody who signs up as a member -- that’s even the free membership. All you need to do is fill out the form at psf.org -- they are added to that list. Now, that doesn’t necessarily mean that people read that list. But they are added to it. Yeah. That’s the specific one I’m talking about.

MEL: And do you have any sense of how many Python developers are on that list? So anyone can sign up for it, but do you have a sense of… Like, as a board member, whether most Python developers are on there, or are there a couple who don’t even know it exists?

NAOMI: Well, so we’re now talking about there being millions of Python developers in the world. I think that the subscription to PSF-community is probably more on the order of maybe… 10,000 or 20,000. Something like that. So I think there is quite a gap there. And I think even the PSF Twitter account, if you pay attention to that, has maybe tens of thousands, but nowhere near the level of the people in the community.

MEL: Okay. So you said mailing list, Twitter, the PSF blog. Are there any other public outlets you can remember?

NAOMI: Those would be the only ones that come to mind for me right now.

MEL: Okay. And then… What do you remember, again, from any perspective, about the beginning of that project? So you got grant money. It got put towards PyPI. But do you know anything about why PyPI, why that particular time, what was the motivation behind it?

NAOMI: I think there was… There was a certain amount of work that needed to be done. I think part of it was infrastructure migration. Part of it was migrating to a new version of the underlying software. Beyond that, I’m not sure I remember a whole lot of the specifics of this need. But I think those were the two things that come to mind.

MEL: Okay. This is very helpful. And in any of that story you just told, are there any parts that you would call out specifically as “I knew this because I was a board member”, versus “I knew this because… If I was not a board member, I would have found this out already”? 

NAOMI: I think the main thing that I knew because I was a board member was the existence of the grants, which is something that… You know, I would have become aware of much later. But it would have been as the thing was finishing, whereas I knew about the grants as they were being applied for. And as the project was starting. So I think in that sense, there would be that kind of difference.

MEL: Okay. So this is the fun part. I’m gonna be interviewing six people total for this project. Three downstreams, and three people who were hired by the grants to do work for this project. So thinking about the stories you told, here’s what I know about PyPI to date, and knowing that I’m gonna be talking with a bunch of other people through this and getting their versions, what things would you like to know? Like, I actually wonder how this started or what is the backstory behind that decision for that one?

NAOMI: I guess I would be interested, maybe, in knowing a bit more about the issues that they were specifically trying to address. And maybe within a little bit more detail. Not just saying… For example, we don’t have enough capacity. But we were having this problem because of overcapacity, X times a week. Or something like that. 

And if I would have wanted to bother people, I’m sure I could have found out in my position. But it’s something that I didn’t pursue. 

So I think things like that, and then I think the flip side of it is… You know, what level of success have they had, then, in specifically addressing those particular things? So, you know, now we can do all of this, zero latency, and whatever. That sort of thing. 

So I would just be interested maybe in a little bit more specifics in that. And I guess I would also be interested in whether or not or how or anything that they’ve considered in terms of some of the things we talked about, in terms of attracting more people to work on this, and maybe an even more inclusive and diverse bunch of people. 

Again, I could go bother people and find this out, but I chose not to do that. But I would be curious about that.

MEL: Yeah. And there’s a difference between “if you theoretically had the ability to access that information somehow,” and then if you actually had the time and bandwidth...

NAOMI: Right.

MEL: Completely different.

NAOMI: Mm-hm.

MEL: And that’s one of the reasons why we have this project in the first place. Yeah. People have no time. And so what’s gonna happen in the next two interviews -- is that I’ll come back for the second interview after I’ve interviewed a number of other participants, and bring back bits and pieces about what they said about this. Their version. And hopefully their answers to some of the questions you’ve been asking. Of the three interviews for this project, the first one is probably the most boring interview.

NAOMI: Well, yeah, no.

MEL: So I have one last question for you today. Which is: The things you’ve talked about -- and there’s two parts to this -- one is talking about what you think of when you think of what it means for a project to be well maintained and sustainable. And the second one is: How is PyPI doing on this front? Both in general and in the context of the last two years. Do you think that other people would largely say the same thing as you’ve said? Or what kinds of different perspectives would you find? How representative do you feel your answers are, of Python Community members?

NAOMI: I don’t have a good sense of that, to be honest. I think that… In terms of PyPI doing what it does, I think in general there probably would be… I think… I would be surprised if my opinion were that different. From other people’s. 

I think that there are a lot of people who would hope that the Python packaging system in general could somehow be improved. But that’s not really PyPI’s problem, exactly. So… 

And I know that people in corporate environments then have different sets of concerns than what ordinary users do. So I think you’d get very different opinions, if you, say, ask people at a big corporation what they thought of PyPI. They may not even be using it -- running their own version, so that they could have a curated set of packages. I know places that do that. So I really don’t have much sense beyond that.

MEL: And so would you consider yourself to be at a big corporation using Python in that way? Or a small… How would you characterize your development?

NAOMI: Yeah, professionally, I work at a medium sized company. And our involvement with Python is just my team. So we’re actually fairly small, in terms of what we do with Python.

MEL: And about how many people in your team do you have, using Python?

NAOMI: About seven.

MEL: So very small.

NAOMI: Right. Right.

MEL: And so you’re mostly using the Python infrastructure directly, instead of having your own internal stack?

NAOMI: That’s right.

MEL: Okay, cool. That’s good, to have the context. Cool. So that is… That’s all the questions that I have for today. And like I said, the second and third interviews are more fun, because you can do “oh, look at what this person said!”

NAOMI: Yeah, that sounds good.

MEL: Is there anything else that I should have asked about, that I forgot to ask about? Anything else about PyPI or your involvement with Python or sustainability that you feel is important?

NAOMI: I can’t think of anything right now, no.

MEL: Okay. So just to give you an idea of what comes next, so we have the transcript pretty much ready to go right now. Thank you, Mirabai. You’re awesome. So what’s gonna happen is I am going to put a little -- after we’ve been talking -- I’m gonna put a copy of that transcript in. So when we have a conversation like this, it’s unclear who holds the copyright.

NAOMI: Oh!

MEL: But it’s definitely some combination of the two of us. So I’ll put a little statement in there, saying that I transfer all my copyright rights to you. And so you’re the sole holder of copyright of the transcript. And that means you would be the only person who can assign a license to it. And that’s for protection of participants and everything, but also just to make the licensing really clean. And so you have an opportunity to look through this. And let me know if there’s anything you want to change or edit or take out, before we stick a creative commons on it, and then I can stick it up in the repository as part of the public dataset. Is there anything you can think of right now that you might want to look at?

NAOMI: I don’t think so. I mean…

MEL: Okay. So I’ll send your transcript in a little bit with that copyright statement and instructions on how to send me back the transcript with this statement at the top and everything is good to go… And then we’ll get it up on GitHub and yours will be the first public transcript, and after we get a couple of the other interviews up, I or Heather will reach out to you again about scheduling another one, and we’ll do this again, but with more interesting prompts.

NAOMI: Sounds good!

MEL: Any other questions? Or is that good?

NAOMI: I don’t think so. It’s been fun.
