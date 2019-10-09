# Copyright transfer statement

MEL CHUA hereby irrevocably transfers and assigns to JACKIE KAZIL in perpetuity, all right (whether now known or hereinafter invented), title, and interest, throughout the world, including any copyrights and renewals or extensions thereto, in the attached transcript of the interview recorded between us on OCTOBER 1, 2019 in A LIVE-TRANSCRIBED PHONE CALL.
 
# License

I, Jacqueline Kazil, hereby release this work under the following open license: http://creativecommons.org/licenses/by/3.0. Anyone is free to share and remix the work as long as they cite it. I consent to the open publication of this work using my name.  

# BEGIN TRANSCRIPT

MEL: When you're ready, we'll start the transcript recording at this point. And I'll just copy everything below this line. 

JACKIE: Sounds good. 

MEL: Okay. I'm going to be at a few second delays responding to you last time because I'm watching through captions instead of listening. 

JACKIE: Sure. 

MEL: You're on your phone right now. I did call your phone number. And this is the second of three rounds on PyPI. And what I did, as you know, I'm interviewing six people on this, and you're one of them. 

And so, at the end of last time, I asked you is there anything you'd like to hear from anyone else? And specifically, the three people in the interview who were involved directly in the PyPI development. And I've got some excerpts from them. And I wanted to show you -- what would be the best way for me to get you that information? 

So I can email you that. I can paraphrase it really quickly what they said. Or if you'd like, I can read a full quote to you out loud here. 

JACKIE: Yeah, I think paraphrase. I think paraphrase is fine. Because I feel like you probably digest a lot of information, and your paraphrasing would probably be better than the quote. 

MEL: Okay. Cool. And in that case, I'm going to ask Diane, who is our captioner today, to transcribe my paraphrasing of that. So we have that on record. Cool. 

So just to review what you're asked about. You asked about a couple of things. One was the story of the PyPI remake. How that happened, how people got hired. And the other thing asked was how did it start grant-wise? And the last thing you asked was technologically, what happens? 

JACKIE: Mm-hmm. 

MEL: We'll start with the first one, which is the story of the PyPI troubles that kicked off this whole thing. And so, the three people, since everyone has consented to public review of data, I can tell you the three people on the inside, the PyPI development team side, that are being interviewed for this. Donald Stufft, Nick Coghlan, and Ernest Durbin.

JACKIE: I know Ernest, what are the other two names? 

MEL: Donald Stufft -- 

JACKIE: Yeah, I know Donald and I know Ernest, I'm not as familiar with Nick. 

MEL: Okay. Nick is one of the Python core developers, and he's been involved for many, many years. He was one of the people that was working behind the scenes to get the grant up and going. 

JACKIE: Okay. 

MEL: So started out with Ernest talking about how PyPI started about 17 years ago. And started as someone's pet project. Richard's pet project. 

And then, Nick talked about how the PSF took that pet project, put it on a server and then suddenly people started using it. So it was not necessarily designed to be production. But it became production because, hey, it worked. 

JACKIE: Because that's what happens. 

MEL: Production happens, yes. And so, Donald jumped in at that point saying PyPI, because it's 17 years old, it predates every modern web framework possible. A concept which was thrown together one weekend and became production for every Python programmer somehow. 

JACKIE: Was it written in Python? 

MEL: I believe so. I can double check on that, but I'm pretty sure. And everything that they said matches with that.

JACKIE: That's okay. 

MEL: The web framework, there was specifically no web framework in Python, this was before the time where any of those things existed. And this proof of concept became production, accidentally. 

JACKIE: Okay. 

MEL: So Ernest also talked about, okay, we have outages. There were no tests of the service. There's like two working tests for it. There was no TLS for a long time. They were using SSH for uploads. And the best monitoring they had was, can I go to the website? Is the website working? That was monitoring. 

JACKIE: Awesome. 

MEL: Yeah. And there's no documentation. There's no design API, so this is, like, switching over to what Donald was talking about. 

Because it was written as a hack, it was written as "here's this website, it's HTML, you can read it and click around on it," and it wasn't designed for non-human interfaces.

The setuptools and easy_install stuff, setuptools happened and "oh, shoot, now we have things crawling around scraping the web interface, that's using a lot of resources, maybe we should come up with a way to have people do that some other way." Because the scrapers don't need to download the HTML for that.

And so Donald was telling a story of how, basically, the PyPI API started with, and was designed for, setuptools is a webscraper that's basically grabbing our HTML, let's start with that.

And they didn't document this, they didn't tell anyone, they were just like, you know, we'll make this thing now. And he described it as, like, 12 layers of hacks on top of each other. Now this is our API. 

And Donald had examples of specific things that were in the previous API because of the hacks upon hacks upon hacks. There's an HTML table somewhere in the API because setuptools has a regular expression that was looking for an HTML table that was there for, like, the first human readable version. 

JACKIE: (laughing) It's terrible. Amazing, but terrible. 

MEL: It's, yeah. And so, there was that. Unsurprisingly down the road, you've got these outages happening, the service was not designed for that. Was not designed for production, it was a hack. And they went, "we've got to fix this. We can't keep on having this thing go down because it goes down and people complain and it goes down and people complain."

At the same time, no one could contribute to PyPI code. The code base was, and this is Donald, again, he's explaining the code base did predate modern practices and things like unit testing and code structure. So PyPI code consisted of two files, each file was about 3,000 to 4,000 lines of code.

Unsurprisingly, nobody could read it. And Donald talked about how he, basically, he and Richard were the only two people that knew what was going on. And Richard basically quit, leaving Donald.

And Donald was like, "I need to get other people to help on this because I'm looking at what happened to Richard and I don't want that to happen to me. I don't want to burn out. I need to other people involved." And he tried, and went "this is completely unsuccessful, nobody is coming to join [the development team]."

And Ernest talked about that, also, how it was really difficult to play around with the code. It was difficult to run locally. 

And both Donald and Ernest were talking about, well, how do you make changes to PyPI? You have to comment out a bunch of things, try to get it to run locally. And if you could figure that out, then maybe you can make a change. And maybe if you make a change and it works locally, you would push to test PyPI, and if it didn't break, you push it to production PyPI and hope it was close enough that it wouldn't break. 

But, again, no unit tests, no nothing. I think Ernest said two tests for the entire thing ever. And so, like, you couldn't tell whether this was going to cause any problems. You cross your fingers, pray, send it out there. So the way you work on it is that you push, and see if it works. 

And at some point Donald went, "this is not working. We should just throw everything out, start over, use a modern web framework, make something that other people can read and contribute to. It's not worth trying to salvage. And maybe that will help us get new contributors on board and maybe people other than me will be able to help with this. And that will all be good."

They were talking more about that, and they were talking about the downtime and the outages. 

So that's sort of the prelude to what would issues that led up to PyPI getting rewritten to warehouse. And I'll pause and kind of let you respond to that to see how does this strike you? Anything surprising? Any of this new? 

JACKIE: Yeah. The severity of the, the severity of the issue. I think there's a little bit more of what was happening is a little bit more, things that were a little bit more severe than I thought they were. 

And maybe I knew that when we were talking about it more and I had just blocked it out. But it, um, I don't remember it being this bad. But I remember it being a lot of issues. 

MEL: Talking about when it started getting bad, everyone is mentioning, like, 2012, 2013, I don't know if that rings any bells for you and what you remember at the time? 

JACKIE: Yeah. So I've -- I think I really started getting active in the Python community around that time. So I wasn't engaged enough in the community at that time to probably have noticed. 
    
MEL: Oh, okay. In terms of being an active member of the Python community? Or in terms of being -- like, was there a period where you were a user of Python, developing Python, and using PyPI but not yet active in the community? 

JACKIE: Yes. Yeah. I was a Python developer using PyPI probably since about 2007. 

MEL: Okay. 

JACKIE: And I, but I wasn't aware of any issues. I'm not sure I even encountered an outage that affected me that I can remember in my history. 

But as a board member, I remember having, well, maybe, probably as a board member, but at some point when I became more active in the community, I remember having conversations about this being an issue that we needed to address. 

MEL: Okay. Yeah. And as a developer, one of the things we're starting to see as a common pattern is there was, oh, as an individual using this, I never noticed any outages, it's always worked for me. Even during the period where Ernest and Donald are going, "this is when [the service] went down a lot.""

JACKIE: Yeah. That's interesting. 

MEL: Do you have any thoughts as to why that might be? 

JACKIE: Repeat the question?

MEL: Do you have any thoughts as to why that might be? On the individual level of the PyPI users, as a developer using PyPI, people were saying "it was working fine, I didn't notice any downtime, didn't notice any outages, this didn't affect me," but at the same time the folks in upstream doing PyPI development were like, "yeah, this was bad, we were having outages a bunch, we had downtime inconsistently, people were complaining."

JACKIE: Yeah. Well. I would say developers are more actively using the API, the API is the experience the consumer could have had, maybe only one part of the API was down. Maybe the experience for consumers was untouched.

Also, the outages, I think I would need a lot more context around, sort of, the details of the outages to be able to explain that. Otherwise, I'd be giving you a bunch of hypotheticals. 

MEL: Yeah, I mean, the best guess we have right now is that the infrastructure folks, they literally saw all of the outages. But if you were just a user, and you only happen to touch it when it wasn't out, you would never have seen that pop up. 

JACKIE: Yeah, I would also say to anyone who is probably a more active user is probably more closely tied in the community with the folks who are working on PyPI, and people who are less connected are the ones that are not having their voices heard.

So it's not that maybe, maybe they were experiencing outages, but they weren't, that information wasn't given back to PyPI. 

And in the same way, people well-connected to the community would be able to express their opinion. 

MEL: Interesting. Okay. And is there anything so far that makes you think differently about infrastructure, sustainability or, like, open source dynamics with maintenance and sustainability? 

JACKIE: Nothing, it doesn't make me change in my opinions, the opinions that I've already formed. 

MEL: Okay. So the next thing that you asked me about was the story of the grant behind the scenes, how that happens. Ready for me to try to summarize that bit? 

JACKIE: Yeah. 

MEL: Okay. So a lot of this is from Nick. But starts out with, Ernest had a nice phrasing here where warehouse as rewrite was something that had "been in flight for a long time." And Donald talked about how he got it started and most of the way there. But it "never got over the finish line," is the phrase they used. Started off with development going absolutely fine, and then it became a last-mile problem. 

And so, Nick went way, way back in history. And said, "on the PSF level, there's a grant before the Mozilla grant for Warehouse that you need to know about."" Which was the grant to refresh the Python.org website. 

And what the PSF learned from that grant was that, one, project management is actually important and the thing we need to do. Because the Python.org website grant did not have project management. And that was one of the reasons why it had a lot of challenges in terms of getting completed.

The other thing that the PSF had to learn the hard way on the Python.org grant was the, this is not a word that Nick used, but I'm going to call it "organizational infrastructure." That the PSF was not equipped to handle grants that required any kind of larger organizational infrastructure on the PSF side. 

Because at the time, the PSF was all volunteer. And so any people being hired, any people being contracted for any kind of work couldn't be under the PSF, they had to be under somewhere else. But the grant that was giving them money, there were things being written which were clearly structured around, okay, the client needs to have the capacity to have full-time this, full-time that, full-time the other. Needing to hire people. And that's something they couldn't do. 

And so that affected the bids that the PSF could accept for the website work. There were some proposals that organizationally were a better fit for the PSF stucture at the time, but the pre-work and the preparation for the actual work being done on the website was not as strong [as the one that was accepted].

And so, because of that grant -- the next thing that came around for a grant discussion was, okay, now let's work on PyPI, let's get a grant for that. The PSF went, okay. Because of our prior experiences, the website refresh being so painful because of our organizational infrastructure or lack thereof, we're going to do it differently this time.

We're going to try to build up this organizational capacity, hire a project manager for the grant, we're going to not make the mistake we did last time of, well, we have one community member on the grant who has been good about their involvement. So we're going to assume that will make everything okay. And then, life happened and it didn't. So we need, we need to find a way to mitigate that. 

Because otherwise, there would have not been an incentive to put that sort of work into PSF's organizational structure up front.

So that, that is the backstory from the PSF side, and then the PyPI need came up and they realized, okay, we need resources for that. 

It is kind of technologically there. Donald has effectively written most of Warehouse. But it's the last switching over of the service, what do we need to make that happen? So the difference between writing the software for the new service and then switching people over to the new service, the second part, that was the hard part, not the how do we implement the new features part? 

JACKIE: So switching people over was the hard part? 

MEL: Yeah, I think it was Nick who was talking about how, it's not a technical problem, it was a marketing problem, it was a communications problem. Because the challenge is, we had to switch the service over, how do we tell people to prepare for it? That we're going to switch the service over. And so our old API, how do we figure out which things people are using still? What do we need to support? What can we break? If we're breaking it, how do we tell people we're breaking it? That was the tricky part.

But warehouse was sitting out there, people could use it as an alpha, so to speak. But official PyPI didn't switch over, they couldn't figure out how to get people to switch over and what needed to happen for that. 

JACKIE: Interesting. 

MEL: Any particular things with that that you were surprised by, have comments on? 

JACKIE: Um, other than sometimes it's, sometimes we think that, you know, the technical part is going to be the hard part, when it's the people and culture. That becomes the hard part. 

MEL: Mm-hmm. 

JACKIE: I'm not surprised that's the case. But, yeah. I'm not surprised that's the case. I just, I probably would've, I might have overlooked it as well. 

MEL: Yeah, and it's, like, one of those things that in the interviews, when people go, "oh, yeah, of course that's how software's made." You know, we know that this is how it works. We don't remember it, sometimes. 

JACKIE: Yeah. Exactly . Sometimes, it's easy just to want to, it's easy to think that you've covered everything and then you realize you haven't talked to the users enough and the impact that's going to have. 

MEL: Yeah. And that's the, on that front, Ernest talking about the fact that PyPI is free. Like, there's no subscription, there's nothing, they want to provide it to the community. And so a tradeoff for that, they don't have contact information. They don't have usage statistics. They don't know, they don't have, like, a tightly bounded way of keeping track of people. 
    
JACKIE: Yeah. 

MEL: So Ernest was joking, you know, the best user data we got was from the outages because then suddenly people would come out of the woodwork and because what they were doing with it. It was stuff we didn't imagine and didn't know we needed to support.

So maybe, and then, we tried everything, asking people to please give us information. But they don't unless there's an outage, and then they give us information but they're angry.

Maybe if we want user data, we should intentionally take PyPI down and then we'll get information. But that seems like a bad solution. This is Ernest sort of thinking out loud of the tradeoff of that. 

Because this applies not only to PyPI as infrastructure, but also any infrastructure from an open source perspective that that really values things, like, people should be able to use it. They shouldn't need to sign up, they shouldn't need to pay.

The tradeoff being, okay, great, we don't have control of who is using it and we don't know anything about how they're using it. 

JACKIE: Yeah. Exactly. But I will say one of the things I do like is the privacy behind not having that information. But I think that's just me. That's just me as an individual. 

MEL: Mm-hmm. 

JACKIE: While (inaudible), I think you can still find -- if you shake the bushes or whatever and, you know, you go out and into the community, you can find the feedback you need to find. There'll always be edge cases. 

But from a privacy perspective, it's nice to know that we don't keep that data. And we don't, because then it also makes us liable for the power that the data holds. So usage patterns, for example, could tell you maybe the type of company, what type of work a particular company is doing. And it could also tell you what type of -- what direction the company might be investing in.

So, you know, the example was let's say there's, you know, company that exists out there and, you know, their IP address is downloading whatever library. And they decide to do a heavy investment in ML and AI, and it's not something that's traditionally in their domain, and they start downloading a bunch of stuff from PyPI in those spaces. That would be the kind of thing that would be included in such, or could be included in such a data set, which could be a business liability. 

And so, it's nice I'm kind of happy we don't, we don't collect that information, because then it provides us with less liability and makes the, makes it so there isn't like a central repository, basically sketching out what activities people might be doing.

MEL: So the tradeoff of that is -- and I can totally see how that could be a positive thing and influence whether people are willing to use -- whether people and companies are willing to use PyPI as a service. 

The tradeoff to that from the infrastructure side is the ability to plan for future usage and how much -- in production, what kind of changes can we make? Not just from a technical perspective, but from resources what need to be committed to continue that technical work to just sustain that infrastructure. Do we need to ask for more server donations? Do we need more CDN capacity? The flip side that comes up in other interviews.

JACKIE: Got it. 

MEL: And I don't know how much that sort of, you have an interesting perspective as someone who is both on the individual user's side but also a high-level view of Python culturally and organizationally. Are these kind of tradeoffs things that you see people talking about, either sort of on the ground, developer to developer? Or do those conversations happen on the board? Or have you seen...

JACKIE: Yeah. To be explicit, when you say these types of tradeoffs, can you enumerate what the tradeoffs are? 

MEL: Yes. For instance, we don't collect user data. As an intentional design decision. But on the pro side, this is what you said about, okay, there's privacy, and organizations PSF won't be liable for having that kind of data. On the business side, the businesses know that the people are not collecting that kind of information. So they may not be able to predict they're going in one direction or the other. On individual developer side, oh, I can sign up, it's free, I don't have to ask my boss for money, that's great.

But on the con side, on the infrastructure side, now they don't know who is using that, how it's being used. How to predict what kind of people will be using it for what and when. And how to plan for what they can do with the service based on the usage pattern they're seeing. They can't get in touch with all of the users saying, hey, we're planning on making this change, please let us know if it's going to break something for you. They don't have the contact information, don't have the user information. 

JACKIE: Sure. 

MEL: From a resource perspective, how much money do we need? How much server capacity do we need? It's unknown. 

JACKIE: Sure. You know, I think, as far as conversations about this, I'm not sure that those, I don't want to say those conversations have never existed. I just can't think of one that has happened recently.

We do have conversations where we talk about privacy at times, or reliability. We have an attorney that is on the board and the PSF. So we, we have the ability to talk about these things. 

With respect to having people connect, I could see, I could see a world where maybe you make it optional. 

The, I think the issue becomes -- I think part of it is that you want to make sure you don't, you respect sort of every population's need for support. But at the same time, you don't overengineer a system. 

A large company, for example, is going to have an internal repository. And so they're not going to do all of the downloads. They're going to, you know, update it every so often. But from the perspective, the side of the company, they're not going to be downloading from PyPI as much as you would think they might be. Because a larger company has more risk and more liability, they're more likely to do internal software scans and have other checks inside the company.

A smaller -- an individual will probably go unnoticed. But a smaller company would, the smaller company is one that might be less tied to the community but needing to keep...

You know what, I'm talking, I'm trying to think out loud. And I would be more worried about the individual doing development, needing to keep updated on stuff. And so for that reason, I might say, as an individual, I'm willing to give you my information. And you can collect usage staff on me. But I would also, from a company policy perspective, I would prefer that not be the default. 

MEL: Okay. 

JACKIE: But I could see how that would be helpful. 

MEL: Yeah. I don't know if there were discussions that happened among the folks working on the infrastructure side. I can take that back and see and ask what they think about this. 

There's another thing that Nick mentioned about the behind the scenes on the grant side that you might be interested in. It was echoing something that you brought up, of "okay, this was a good, early grant to prove that hey the PSF has the organizational maturity. We can handle these grants, you should give us more of them, you should give us more stuff."

And Nick was talking about how, because it was sort of the first round of the PSF going through this sort of grant, with project management and the organizational infrastructure they trying to get up for this -- they did a couple of things that would not be the place in subsequent grants.
 
And in particular, the people who were contracted to work on the Mozilla grant were contracted, like, during the time the grant proposal was being written. 

Which is in contrast to what he said, that in the future it should be that the PSF gets the grants, [and says] "We want this work done, we have the money for it. Hey, open call for proposals. People in the Python community, send us your proposals for how you would do this. And then we'll pick the winning proposal." 

Which is what happened before the Mozilla grant, but pre-PSF organizational maturity. So to go back to that sort of openness again.

But what happened with this round instead was, because they were figuring out the organizational details internally, because it was, you know, "this is the first big grant we're trying to do this way, it's really important that we get this right and we have this down solid so that we can prove that the PSF can handle this," every person that was hired and paid with the Mozilla money was written into the grant as the grant was being written.

So it was not a transparent process. It was not an open process, from that perspective. When Mozilla said, yes, we're going to give you the money, they specifically said, yes, we're going to give you the money and you're going to hire Donald and you're going to hire Ernest and Sumana, you're going to hire Dustin, Nicole, I think I'm forgetting one other person.

So, again, in between, as an open source project, a project doing open source, we want to have that transparency, want to give people an opportunity to pitch in on this. But right now, because this has to get done, because we don't really have experience doing this, we've got to nail this stuff down beforehand. And that means it's less open to people participating. 

I thought that was an interesting note. And I wanted to toss that out to see if that's something you had seen or heard of. And what you thought about it. 

JACKIE: Yeah. So I didn't know about that in particular. I will say that from what I've seen of contracts in the past, especially from what I've seen of contracts in the past, especially of, like, I would call it, not corporate, but entities that are supposed to be more neutral, especially the government, that it is very easy to slip into a pattern of who you know. Or sort of give some preferential treatment, even if it's accidental. 

And all those people involved, from my knowledge are great people who do great work. But that doesn't address the inclusion problem with that. And, you know, makes for a less competitive environment. So, yeah, I didn't, I didn't -- I wasn't particularly aware of how that contract was structured or how the grant was applied for.

The other thing I will say is that sometimes having well-established people with track records on a grant request can help give it weight. It's not just me and my colleague applying for a grant, it's ten people and we're ready to go and we have a plan. 

MEL: Yeah. 

JACKIE: There is some weight to that. And these ten people that are ready to go are well-experienced and they're people you can count on as opposed to, and this is the plan. As opposed to we don't know who we're going to hire. 

It presents a better picture to the person you're applying, applying to the grant. Presents a better picture to the grantor. 

So, yeah, I'm not sure. Yes, there is a, seems like there's a lack of. A little bit lack of transparency, but I don't think it was maliciously done. 

MEL: Yeah. 

JACKIE: I think it's one of those things that in the future you do a retro and then, you identify, like, in this case, it's been identified this doesn't work or, you know, it's problematic for XYZ reasons, and then, you adjust in the future. 

MEL: That's one of the things that a lot of the upstream infrastructure folks were talking about. The capacity building problem of the same people doing the same work over and over. Needing new blood. 

JACKIE: Yeah. So this is kind of what happens. This is kind of what I've seen with government contracts in the past. And if somebody provides a service, you know, and you can bid a service out and you can ask for XYZ to be included in the service and that service has been provided to you with XYZ in the past by, you know, some provider, then it's almost like it is greenlighting or it's almost like, you know, laying the -- laying the red carpet out for that. For that individual that automatically wins. 
    
MEL: And so, one of the things I think you talked about and then all of the other PyPI users also talked about was the importance of getting new people involved, the importance of not just allowing the same people over and over, again. So, how can we think about balancing that need with the, wanting to go "we have experienced people on this grant." It just looks better because they have experience. 


JACKIE: Mm-hmm. Yeah. Well, I think I'd probably split it 50/50. I think there is a, I think, you know, I think with any software development team, it's important to have a mix of individuals because it pollinates new ideas, new ways of thinking, and it's, it's a good thing to be able to say, okay, you know, these are two people who have worked with in the past. And these two people are new. 

So there's some sort of known quantity. You can count on those two people pushing things forward. And then, you can also open the doorway for new individuals to establish themselves. 

MEL: Mm-hmm. So that's actually related to another bit from some of the other interviewers that I'm going to try to summarize right now. Which is the, this is not something you asked about. But it came up a few times of the nature of people working on PyPI and other infrastructure.

But not, and so, how do those people get paid for that work if at all? Because, so right now, as you probably now the PSF doesn't have multiple people, it has Ernest, and he has part of his time on PyPI. And so, it can't all be on Ernest. PSF pays one person.

There's the version that Donald has, which is Donald is employed by another company and that other company lets him use some of his time to work on PyPI. 

And there's the other version of, there's a bunch of people who are just doing this as volunteer fun time for whatever reasons they personally have.

And the balance of what predictable, what's sustainable? What does this mean for people? And what does this mean for who is able to contribute in what way? 

Donald was talking about how if his employer didn't give him the time and the job to do it, he'd probably still do it, it would just be slower. 

JACKIE: Mm-hmm. Yeah. I think that's one of the -- one of the issues I have with the projects I maintain is, you know, given the proper time and space, it would move along a lot more quickly.

You know, I think ultimately one of the things we're doing with the PSF, we're doing work with our financials to be able to submit the larger grants, to be able to support one of those things, and with one of those things being development. 

But going after significant money to be able to, you know, because it's, developers are not, if you're truly paying a developer what they're worth, it's not, their salaries are not insignificant.

Because, you know, ultimately, there are a lot of, a lot of companies and a lot of people dependent on a lot of the, you know, things out there, whether it be core, or whether it be something as an extension. And volunteers, volunteer teams is not sustainable. 

And, you know, some companies give time and space. But that still, you know, that's still a difficult proposition. And, you know, can be, can be shaky at times, as well. 

So yeah, do I believe open source contributors should get paid? I feel that by paying people to take some of their time that they would normally be making money to support themselves with is a very viable option. 

Should everyone get paid? That is the question, or where that line is. Obviously people who are getting paid are going to be doing more work and making more contributions and the people who aren't getting paid are going to be making less. And so, I think because they're doing it in their, they're doing it in their spare time and they can only do so much.

And I think, I think that's fine to have sort of have two classes. And if an unpaid person wanted to become a paid person. You know, if more of those exist, it would be possible in the future, but yes, I do believe that is a way to make things more sustainable.

One of the bigger questions, though, is not only, like, we can go after grants but not only going after grants, but having larger companies that might have the ability to help sustain the community understand the value of open source contributions. And if they don't give, if they don't have someone on their staff they're carving out time to make contributions to back to open source, that they maybe pay into a system that they're highly benefitting from. 

MEL: And a few other people said they would like to see companies do that. And the question I was going to ask is related to that, which is, when you talk about paying contributors and paying people to work on open source, there's a lot of different kinds of work that goes into open source, development stuff, infrastructure work, there's marketing work, design and testing, there's project management. Do you see if the balance or resources we're getting should be distributed more to these areas that we need? Is the money being directed, and is the paid work being directed into the most needed types of paid work? And what would those types be?

JACKIE: Sure. So I don't think -- I don't think I have enough information to be able to say, you know, we really need more infrastructure or more X, Y or Z. And so, I think that would require a little bit more research because I suspect with different projects, it means different things.

So, for example, like if you, also, I would also say that for different projects it means different things. It also, I would say, is different for different projects at different points in time. It might mean different things early on and later on. 

And so, like right now for the project I manage, I do, I'm doing a lot more administrative and product management, which I wasn't expecting to do. Which, you know, we need, to be able to merge stuff and get things through. But if I had money for that project, I might hire someone to do that even though I'm currently doing it so I can then do some more of the engineering stuff. 

MEL: Right. 

JACKIE: At the same time, though, that role is being fulfilled. Somebody else might take that money and use it to push some of their bug fixes through or something like that. I think it depends on the project. And I can't make any generalizations. 

MEL: Yeah. Okay. One of the commonalities coming up across this project is a lot of times I'll ask questions of participants and they'll say, "I don't know." And the I don't know is also really useful to us. So the "I don't know" or "I'm not sure I should be the person answering that question."

JACKIE: Yeah. 

MEL: I think you brought this up in the first interview, also, that concept of, you are a board member, therefore, you know everything there is to know about what's happening with Python's organizational level, a technical level and all of the things, that no one actually can do that.

JACKIE: Yeah. Exactly. 

MEL: Okay. So I'm looking at the time and we should be wrapping up soon. Anything from today? I know today was a pretty big information dump. The third one will be more back to you talking, and less me going, "here's what people said."

Anything from today that you have comments on? Or was surprising? Anything else you want to make sure we touch on? 

JACKIE: No, nothing that I haven't covered already. One of the things you asked me I don't think I answered was "what should companies give?" Didn't you ask me that? 

MEL: Yeah, yeah!

JACKIE: Yeah. And so this, you know, I was talking to a friend of mine over at Google. And she, her name's Amanda. She had been, she had come up with this idea of, basically, mathematically calculating the economic value of open source to a company. 

So therefore, you can then say well, this project is, you know, having contributions on this project is worth X dollars to us per year. So let's put that money into the community. And, you know, I don't know what X dollars is. But I'm going to make up numbers. Whether that's $100,000, $200,000, $1 million, 10 million, whatever that is. 

But the idea is when you have a large company, whether it be Google or whether you have, you know, a large company like the one I work for at Capital One, or someone else -- there is economic value in investing in the open source community to making sure there's a healthy and sustainable community. Because ultimately, companies are using open source and saving a lot of money because they're not having to rebuild all of these things. It's kind of like a two-way street. 

MEL: And that's sort of, have you heard of Tidelift? 

JACKIE: Yes, I have heard of that. 

MEL: It sounds like thier model of -- how do we let people contribute back to infrastructure and these systems they're going to benefit from? 

JACKIE: Mm-hmm. 

MEL: All right. So thank you. This is really helpful. So what's going to happen is the usual, transcript will get cleaned up, you'll get an email saying "look this over."" And the third time we talk -- Heather will talk to you about scheduling -- we're going to come back around to the definitions that everyone put up for what sustainability means, about what being well-maintained means, and how that fits into the PyPI story everyone has been telling. And so that would be the last interview. Any questions or comments?

JACKIE: No. This all sounds good. 

MEL: Okay. Thank you so much, again, Jackie. 

JACKIE: Thank you. 

MEL: I'll be seeing you on the third one. 

JACKIE: Have a good day. 

MEL: Bye.
