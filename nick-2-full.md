# Copyright transfer statement

MEL CHUA hereby irrevocably transfers and assigns to NICK COGHLAN in perpetuity, all right (whether now known or hereinafter invented), title, and interest, throughout the world, including any copyrights and renewals or extensions thereto, in the attached transcript of the interview recorded between us on SEPTEMBER 26, 2019 in A LIVE-TRANSCRIBED ONLINE VIDEO CHAT.

# License

I, Nick Coghlan, hereby release this work under the following open license: http://creativecommons.org/licenses/by/3.0. Anyone is free to share and remix the work as long as they cite it. I consent to the open publication of this work using my name.

# BEGIN TRANSCRIPT 

MEL: Yeah. So, is it -- are you ready to start?

NICK: Yep.

MEL: We can make the official transcript start point and start rolling.

NICK: Could I get a link to the transcript again? That was handy last time.

MEL: This is a slightly different captioning setup. The captions are happening in a separate browser window. I'm going it send you two links. One is the captioning link. One second. 

I'm using your -- there we go. Come on, keyboard. Come on. Of course, my keyboard decides right now is the perfect time to -- fortunately, I have a backup keyboard. As one does. Please hold. I am going to switch keyboards.

Okay. I think we're back with audio and then I put two links inside the chat.

NICK: Yep. And I've connected to those. Cool.

MEL: Okay. Welcome. Okay. Yeah. We see you inside both of them. So, what I want to do today is, so, the first time that we talked, we heard the story of the PyPI migration with a lot of lovely historical details.

As you know, I have been interviewing other people about this also. Six of you in total. And everyone consented to open sharing of their data. Since that's part of this study. So, I can tell you who they are, you probably won't be surprised. 

I'm also interviewing Donald Stufft and Ernest Durbin. And there are three people who are super-active contributors to the community that were not part of the Warehouse migration, Terri Oda, Naomi Cedar, and Jackie Kazil. Kazil.

NICK: I'm not sure I know how to pronounce it either.

MEL: I will ask her. So, what I have for you to kind of go off of today is I took some bits from Jackie and Naomi and Terri's interviews and sort of synthesized them into four, like, mashups, so to speak.

NICK: Yep.

MEL: Each of them is around a different theme. And we have the whole hour to do this. And then we can, you know, go back and retell whatever parts of the story you'd like. To just sort of take a while to read each of them and then respond to them and see if you're surprised or anything or if it prompts any thoughts about the narrative on your end or sustainable open source infrastructure.

NICK: I will say, the transcripts from the first round of the meetings?

MEL: Yeah.

NICK: Yeah. I think that was -- I don't know -- (Nick's audio starts cutting out)

MEL: So, the audio -- the captioner says it is cutting out a little bit?

NICK: I'm cutting out. Huh. Oh! Okay. I know -- the background noise.

MEL: Oh, okay. I can also try to relocate away from some of the humans in this room.

NICK: Okay. Let's try this. Is that better?

MEL: Let's see what our captioner says. Is this better?

AMANDA (typed): Say a little bit more... Nick.

NICK: Okay. What I was trying to say before is that, yes. I actually did read the transcripts. With what I said, also -- [still hard to hear him] --

MEL: Amanda is saying it's still hard to hear you.

NICK: Let me try that. Hang on. Why does that still think -- go back. Okay. Is that actually switched to the speaker or the headset microphone?

AMANDA (typed): I think so.

NICK: I think it's still using the webcam's mic up here.

MEL: Okay. She thinks it's switching.

NICK: Okay. That's better now? Okay, cool?

Amanda: Yes! Thank you.

MEL: Okay. Cool.

NICK: When I plugged the headset in, it switched the speakers, not the microphone. Go figure.

MEL: All right. So, you were saying that you read the transcripts.

NICK: Yes. Yes. It was very interesting. But, yes. But also, looking at the way what was said there. And it actually did remind me of something. 

Which was one of the -- one of the actual roles of the transition, like, essentially we knew -- we knew that our communication channels didn't reach most of them. And so, that was the case. And so, we knew that any improvement that we made would be limited to work without the users changing anything. And not necessarily even with the most up to date tools. 

Actually, that's not quite true. Going back, this was kind of the previous generation of changes. The early 2010, 2013 time frame.

MEL: Okay.

NICK: At that stage. That's when we really, really needed people to actually change what they were doing and stop using easy_install and start using pip instead. It [easy_install] doesn't work the way pip does. The panel that we actually did at PyCon US 2013 was subtitled "./setup.py install must die."

So, it was... and that was actually a real genuine technical blocker to a lot of the improvements that we wanted to make. Like, that we just needed people to be using actual installer clients and not running setup.py scripts directly all the time. 

And that was -- that was something that actually happened in the previous iteration with the Fellowship of the Packaging and all those folks. And the original formation of the Python Packaging Authority was, it was to actually get using a proper installer on the client side. Because that's what then let us change the way it worked.

And just -- I think -- I think Donald gave the description of how PyPI's API evolved out of setuptools screenscraping things.

MEL: Yeah.

NICK: And so, well, it was also the thing of setuptools and easy_install, [they were designed as] plugin systems. And so, [their] defaults, [they’re] good for an application plugin system. And stopped making sense if you're building a Python environment to do web stuff or do data analysis or whatever. And so, anyway, so, pip's defaults were a lot more around [that kind of thing]. 

So, yeah, pretty much one of the design constraints from the Python packaging enhancement was to a greater or lesser degree, don't break existing things. Make it so that the only thing that would be [required is contacting publishers]-- at least with publishers, is that they were trying, Richard and/or Donald and/or Ernest, to do mass mails from PyPI itself. 

And so, there are a bunch of -- a bunch of points along the way where what they're actually doing was trying to make sure they had valid email addresses and files.
And that if anybody had ever published a package in Python, they were going through, trying to make sure that the email address that Python had for the person was valid. That if we genuinely needed to tell publishers something, we could reach them.

MEL: How were they doing this? Manually?

NICK: PyPI had the email addresses in it. They just weren't necessarily still valid. I don't know how that -- what the mass mailing actually runs through. I don't think it's direct to servers. I think it's a Mailchimp kind of thing. But yeah. 

It was -- it was -- that was actually one of the -- that was like a whole hidden infrastructure thing of just getting the mass mails to work and not getting thrown in people's -- not getting thrown in people's Spam buckets. 

So, yeah. That -- Ernest did a bunch of the work to get that to work probably. But, yeah, that's actually been an ongoing source of drama for all the PSF infrastructure. The bug tracker had a similar problem, like confirmation emails getting thrown in Spam. And people going, I can't sign up!

And so, yeah, I had forgotten all of that. That was something -- I think it was Ernest sorted out really early. But, yeah, that was just one of those things. 

Was figuring out, do we have a way to reach publishers and tell them, "hey, such and such a thing is changing."

I think one of the main cases where that came up was some of that link spidering Donald talked about with the way setuptools works, easy_install works. Essentially, we stopped supporting all that. 

We changed, PyPI changed, to say, no, all the actual files need to be on PyPI itself. More to the point, pip changed, so the default link spidering doesn't exist anymore. It expects to see the actual files on PyPI itself. And so, it became far more a package repository, not just a package index. 

It's -- so, that was one of those things. Like, we realized that our communication channels were poor. And we were only reaching a tiny fraction of the audience. 

And that even if -- even when we did reach publishers, the stuff we were contacting publishers about was only new releases. That it was -- that it was all the existing releases still had to work. And for download tools, all the existing working -- the tools still had to work. 

Well, to the -- almost all of them, anyway. There was a point where we turned off downloads over plain HTTP. That was a case if you want PyPI to keep working, you have to upgrade to a new version that will do the HTTPS downloads. But that went back a pretty long way.

But there was a -- there was a point where I think sufficiently old Pythons on Mac OSX just straight up stopped working. Because the Mac OSX web stack -- the network security stack was too old because of Apple's whole move away from OpenSSL and all those exciting times. But, yeah. 

So, the PSF actually had to do a blog post about that saying, hey, here is what you have to do if PyPI suddenly stops working on your Mac laptop.

MEL: Oh, wow. Back up a little bit. You mentioned that you realized that communication channels were poor. When was that and how -- when was that? Who realized it and how did that come to be realized?

NICK: Oh. I think we've just kind of always known. Like, I mean, back when this started, there was a -- like literally the only communication channels were the dev channels plus the mass emails from PyPI to folks with registered accounts. Like, there was no announcement mailing list. And even when there was one, it's the case of how do you announce the announcement mailing list?

And so, that was -- that was a matter of talking a bit to the PSF and that was specifically one of the things Sumana looked at as part of the original grant and as part of some of the follow-up funding that the PSF provided. But ultimately it just became one of those things. 

Like a lot of stuff -- a lot of stuff in open source. And we do it in Python core development as well. You just kind of assume that most of your users aren't gonna know what's going on. And so, if you suddenly break stuff on them, you better have a darn good reason.

And, honestly, that was, frankly, the biggest delay in the -- biggest delay in the -- from where Donald got Warehouse to the point of, "it's up and running. But off to the side and you have to opt into using it.” To, "it is PyPI." Was actually -- was actually that thing of making the transition seamless.

Like, a rough transition could have been done at any time. You just turned off the old server and say this is the new one over here. But the problem is that if you did that, a lot of the users of the old server would be just completely lost. And go, what the...? 

And so, that was -- so, I talked about when the Fastly CDN came in. Like that just pretty transparently dropped in in front.

But like one of the things that broke initially was the PyPI download stats went away. And we're just -- we're just like, "oh, nobody actually uses those for anything. They're kind of nonsense anyway. That's okay. We can just break them and nobody will notice.” It's like, people noticed.

MEL: And what happened?

NICK: So, I'm not sure if they ever came back on the main website or not. But the big thing that happened was Google offered BigQuery access. And so, Donald wrote this thing called Linehaul that basically takes all of PyPI's download data and shoves it over into a public BigQuery table. And so, shoves an anonymized version of it so the full IP addresses aren't there. But the fact that this download happened from this kind of client at this time actually goes into a BigQuery database. We've got some information up on packaging.python.org on how to access the BigQuery data and go get your download stats out and all that sort of stuff.

And so, yeah. So, there's a fair bit out there, if Python publishers want to, they can do their own analysis of what the actual PyPI download stats are like for their project. 

And there's some examples of how projects can use that to say, “h, well. How many of my users are still using such and such a version? Will anybody care if I drop support for it in my next release?” And that's -- so, that's like actually kind of one of our main bits of information of levels of adoption of Python 2.7 versus all the various versions of Python 3 that are supported.

Like, we know that -- we know that continuous integration systems mess up PyPI's numbers in various ways. But at the same time, it still gives you a flavor of at least what are people testing against? What are they downloading on? And so, there's still room for a lot of interpretation around what the numbers mean. But, there's a lot of interesting data in that BigQuery database as well.

And this is one of those things, like, you want to talk about an invisible infrastructure, that's all completely invisible. 

And there's all this weird stuff around user agents in the data as well. Like, because in a lot of cases even though it's pip that's doing the download, there's some other application in the front that's actually acting as a frontend driver for pip and getting -- so, pip's going the work and it's what's talking to PyPI. But there's some work going on to try and get information about, ”Is this pip being run directly by a user? Or is this pip with some other tool in front of it acting as a wrapper?” and trying to get information on what download clients people are actually using that way.

So, yeah. And while also at the same time trying to make sure that you don't cross over that line into getting intrusive as to fingerprinting systems and that sort of stuff. 

But, yeah. It does keep track of some stuff around what versions are being used of various components. 

So, but anyway, yeah. So, that was the case of, like, going behind the CDN, losing the download numbers. Because most downloads weren't hitting the server anymore. And, yeah. So, that was one of the first transitions we were able to do. 

And the vast majority of users never noticed because all the same URLs worked. And it was just hitting a CDN instead of the backend.

But the thing was, that was -- and so, that mostly dealt with the download side. And that then kind of made changing the download side after that was relatively straightforward because the download side, you're talking to the CDN. It's just a matter of changing what the CDN is backed by. 

So, that was kind of the final flip of, well, if you hit the simple API, go -- it'll go to the -- it'll go to the real app, not -- it'll go to the Warehouse app, not the old one. 

Download -- uploads were a lot more challenging. Because uploads you really are talking directly from the client to the backend. Like CDN doesn’t really help. Because you need to do interactive stuff.

And that was one of the big things in the Warehouse migration. Like, originally to use the new upload server, you had to go in and change -- explicitly change your PyPI config. 

And now, a bunch of people did that because uploads to the new one were much more reliable. Whereas the old one could kind of do weirdly inconsistent things where an upload would partially work. And it was just, yeah, not pretty.

And so, that was a lot of what the Mozilla grant actually went to cover was figuring out the migration strategies for a bunch of those pieces and doing the migrations in such a way that for the vast majority of users, they just wake up one day and they were now using the new PyPI and had no idea.

MEL: Yeah. I think that actually is a good segue into, I wanted to see if you had any responses to some of the things that other people said in their interviews? Earlier you read more of the transcripts. So, you can point to anything else. But I pulled a couple pieces that I thought might be particularly interesting to look at in the remaining time we have. Again, we don't need to stick to those if there's parts of the transcript online that really grabbed you. 

On the first page [of the prompt document], Jackie and Naomi and Terri talk about how this is how we perceive PyPI now, as an open source product that's pretty sustainable. It matches a lot with what you have been describing of that seamlessness of experience, 

Terri uses the word "magical" a bunch of times. Naomi [says] "I don't need to know." I'll give you a minute to just read that page and any responses you have to any of that.

> _Sources: Jackie-1, Naomi-1, Terri-1_
>
> JACKIE: [PyPI now] feels like a well-maintained project. I've never went and looked at the signals [of sustainability and well-maintainedness] that I would for a library that I was using for development, because I view PyPI as a service more than a library in itself that I would use.
>
> NAOMI: ...my sense is that a lot of people don’t really, really want to know the details too much. I mean, it’s sort of like a lot of utilities. I really don’t care about the details of my plumbing. I just care if it works or not.
> 
> JACKIE: Yeah, I think people need to know about obviously if there's changes to the API.
> 
> TERRI: So I had honestly never thought about the sustainability of PyPI. It was magic that was just always there, until Donald Stufft was looking for a job and Barry was like… Hey, do you know he’s the only one doing pip? And I was like, “What?! Wait?! What?!!?” So I really hadn’t thought about it at all.
> 
> NAOMI: I would say that... PyPI is well maintained. And is sustainable. Maybe neither one of those as much as we’d like. But I think both of those are true.  In that if there are issues that you have with PyPI, there is somebody who will respond.
> 
> TERRI: ...[I wasn't thinking about it because] I had been using it for about 20 years, and it had never been a problem... Maybe because I use PyPI less frequently than some other services. But as I said, it’s been kind of magical... I would guess that most people just assume it’s magical and sustained and great...
> 
> ...It’s still magical. I think... I’m assuming that all of the documents that I just read to do my [first] release [on PyPI] are probably new. They were certainly very up to date and easy to read... maybe they’ve always been perfectly up to date. But I just assumed that was part of the work that had been done.
> 
> NAOMI: I think that in terms of their openness to contributions, I think that’s also there. I don’t know that from having checked closely, but I kind of assume that, knowing the people who would be making those determinations. So I believe that’s the case.

NICK: Yeah. So, the one -- the one Terri mentioned about the point where Donald stopped working for HP. So, that was a case where HP was going through a bunch of problems. And it was actually one of the interesting things where they had been doing a bunch of quite interesting stuff around OpenStack. 

And one of the things they had been trying to do was actually invest in the infrastructure side of the OpenStack stuff and just build up some of the core capabilities of related parts of the Python ecosystem.

And so, that was -- it was a case where, unfortunately, for other unrelated reasons, not related to that engineering work, essentially HP decided to get out of the OpenStack business. 

And so, there were a bunch of people doing a bunch of stuff -- not just in Python packaging, but also in Python testing tools and various other parts -- where it was just basically HP went, "we're not doing this anymore." And so, the investments they had been making basically went away. 

And so, Donald was one of the ones who actually, when that happened, just did a blog post saying, "hey. I was getting paid to do PyPI and Python packaging full-time by HP. HP aren't doing that anymore. Does anyone want to talk to me?"

And so, that was -- that was actually a real eye-opener for a lot of people. So, Terri mentioned that it was a surprise to her. But, yeah. It was -- it was -- I was working at Red Hat at the time. It was a surprise to a lot of the Red Hatters, they're like going, "wait, what?"

And so, yeah. So, that was the case of people -- and while -- and that basically contributed to Donald being able to get his eventual position at AWS with the part-time work on PyPI. 

And -- but -- even beyond that -- it brought a whole bunch of attention from a whole bunch of people to go, "oh! Wait. We have been neglecting this. We haven't been paying attention. And we should really be doing more of what HP has been doing." 

HP spread it. They had been looking to the long-term sustainability of what we were doing. And we were, "hey, we need to make sure this is something we handle." 

It's unfortunate other business reasons didn't work out. But, yeah. So, it's like, open source investment is not a magic bullet that's gonna solve your business model problems. 

But it is the case of that these larger companies with longer time horizons and wanting to know, “Hey, is this stuff still gonna be around in five years or ten years?” It's kind of like, it's a form of supply management at these big companies. Where it's like, well, yeah. These communities will be around in five to ten years time. If you invest in making sure that they're still around in five to ten years' time. So yeah.

MEL: Terri had a bit -- a part on the third page of the Google Doc.

NICK: Oh, there's more pages.

MEL: How do you find out that the project needs help.

NICK: Oh, yeah.

MEL: She's working at Intel, which is huge. And then I was asking her, so, how have you signaled? How would you have known that this is a thing that you might want to talk with your company about?

> _Source: Terri-1_
> 
> TERRI: Well, I’ve got to say… I feel kind of weird, working for a large corporation, that we don’t give a whole lot of money to these things. And I suspect maybe if more of my corporation knew that Python needed help, they would actually step up. 
> 
> ...I certainly don’t want to make things harder to use in order for people to realize that there was a lot of effort going on behind the scenes. But it was kind of funny that every time I talk about Python, everyone was like… Oh yeah. It’s fine. That’s it.
> 
> MEL: And what kinds of signals would have clued you or your company in to the… Oh, hey. We should maybe support Python more?
> 
> TERRI: I have no idea. I mean, obviously I should have had all of those signals, and I’m not reading them. So I have no idea what would work in the wider Python community.

NICK: So, this is one of the things where I talked a lot last time about the maturation of the PSF as an organization and how important that is. 

And like one of the things that -- one of the managers at Red Hat was like, "at the end of the day, the business model has to work." And so, that was like when you're a corporate -- corporate contributor of open source, it doesn't matter how -- it doesn't matter how generous you are to the open source community if you fail as a business. Then all of your generosity goes away. 

And we saw that with HP. Like, HP didn't fail as a business. But their OpenStack business did fail. And so, all the community investment driven from their OpenStack involvement went away.

And so, and Terri mentioned that as well. That like corporate projects. You never know when a corporate project is gonna get canceled. And these people you have been collaborating with go, "well, I'm not working on that anymore. So, see ya!" 

And so, but you look at -- you look at what a lot of organizations are doing and this is one of the requests we get quite a bit about in relation to the Python package index. And people are like, hey, I can't sell the return on investment of, ”Hey, we need to make sure the PyPI is still around when we need it.” 

But I could say, sell, “I want to buy private repositories” or “I want to buy something else”. And Dustin Ingram's written a couple of things about this where, like, what would happen if you tried to run PyPI as a business rather than as a service run by a nonprofit foundation? And the short answer is we don't think it would work which is why we haven't tried it. 

But the long answer is that, you have to think about it in terms of how do -- how do potential providers of funds think about allocating those funds? 

And if you just sit around and wait for people to drop money on you out of the goodness of their hearts, well, you're not going to get a lot of money.

But it's also a matter of, like, going, saying -- Tim O'Reilly has this saying, create more value than you capture. For a long time I've mentally added a second paragraph to that: Which is, create more value than you capture. But capture enough value to thrive.

And a lot of open source projects, they're very good at the first half of the sentence. And not so good at the second half. 

And the second half, because the second half is not a development thing. The second half is essentially it's a sales activity. Where sales and market research [come in]. 

Like, for example, one of the feedbacks -- one of the bits of feedback that we get with -- from a lot of commercial users is they say, look. I can't do donations. Like, the corporate process for doing a donation is just not something they can do. 

But if there was some kind of service that they could sign up to for $10 or $15 a month, then there's an awful lot of corporate users where that spending limit is on their corporate credit card. Like, that is within the realm of services that they can just say, this is something I pay for on a corporate credit card and the company will sign off on it. So long as it is for a genuine service that provides them with something that they wouldn't get otherwise.

And this is something where as a public interest charity, you have to be careful -- sorry, public interest charity registered in the US, but other countries have similar rules. The PSF needs to be careful not to do stuff that will make the IRS unhappy. 

But it is, at the same time, a very, very consistent piece of feedback. 

This is where you go look at Mozilla, for example. Mozilla is actually in two major pieces where there's the Mozilla Foundation. The registered public interest charity that kind of drives the mission of Mozilla and what it does. But then you've also got Mozilla Corporation where most of Mozilla's employees work. And the thing about Mozilla Corporation, because it's an ordinary for-profit corporation that pays taxes like a regular for profit corporation, even though they're owned by a charity, they don't have the same rules around what they can and can't do. And so, they're able to just essentially go after those regular -- those payment for services rendered-type setups. This then lets them get that operating money, a lot of it from search -- default search providers -- and those various contracts. 

But it is that thing of, the stuff you want -- the stuff you want to give away is not the stuff that you want to get paid for. Well, you might want to get paid for it. But you're probably not going to because you're giving it away.

And it's -- it's this whole side of it is, Jackie talked about this a bit in her interview from the point of view of being able to go for larger foundational grants and that sort of stuff. 

But there's also a whole other side it which is that Mozilla-style pairing of a public interest charity with a wholly-owned commercial subsidiary gives you a lot more funding options. And you set up the ownership structure in such a way that the commercial side is still very much driven by the mission of the charity side.

But, yeah. It's a case where in a lot of ways in this regard the open source world is still relatively immature. And that we're only just now starting to look like, “Oh, we have a lot to learn from public interest charities that have been around a lot longer than we have and have been doing this stuff for a much longer time.”

MEL: And do you think that these legal and like business economic infrastructures, is it that they're out there and the public interest charities have them and what we need to do is copy and adapt and tweak a little bit? Or is there some -- or does open source need a different kind of legal structure that maybe doesn't exist yet? Or a different kind of economic structure? How much is it the pieces are out there, but we're just not using them yet? And how much of it is actually the existing stuff doesn't work and we need to figure out what would?

NICK: I think it's a combination of the two. 

So, like the -- like one of the big ones is if you want to run an actual public interest charity in a global way, that's still really hard. 

So, like the PSF, for example, yes. It's a public interest charity. But it's a public interest charity only in the US. So, if you're -- so, like, for instance, if I donate to the PSF, I don't get any tax benefits from that because they're not an Australian charity. 

And so, it is still very much a case of there are a lot of barriers to effectively running public interest stuff that's global. As something like Python is. 

And the PSF is actively trying to structure a lot of things to get that global inclusivity. Like the grants committee, for example, specifically tries to include people from -- I think it was -- I think we defined six different regions when that working group was being set up. And the aim of that grant -- that committee is to try to have at least one person on the committee from each region all the time.
So, if someone steps down, you try and replace them from that same region. 

Because that was -- that was an ongoing problem in the PSF was you're just like, going, just not having the understanding of different parts of the world. And what was normal in different places. Could create quite interesting questions. 

Now, trying to understand what's normal across an entire continent is still not easy. But it's slightly easier than trying to understand what's normal across the entire world.

MEL: You got to start somewhere.

NICK: That's right. So, yeah. So, I think -- I think -- I do think it's a combination of the two. 

So, like at the -- at that kind of big level, engaging with large corporations, engaging with governments, engaging with the UN. You're pretty much gonna end up with something that looks like a lot of the other NGOs that are out there already. So, oh. Non-government organization. For the transcript.

The -- at the smaller end, though, there's a lot of really interesting stuff around the notion of can we use online tools to create new forms of organization that allow funding to flow in quite interesting ways? 

And so, Open Collective is one of the better known -- Open Collective? I think it's called Open Collective [Ed: yes, it is - http://opencollective.com]. That what they do is they try to provide fully- transparent accounting for funds that are donated to a group. And so, basically you just put the funding in and then -- and it essentially creates a bucket of money. And people can see just all the records for what went in, what went out. And what the different things were. So, that's quite interesting.

MEL: So, one question I have is back to something you were saying at the beginning. So, right now we have been talking about like legal structures around -- that would enable larger finance deals sort of on the backend of companies being able to get money to the PSF and people that were keeping up infrastructure things in wheelhouse and PyPI. 

And at the beginning you were also talking about -- one of the things that really strikes me is in both of your interviews, you haven't talked very much about the technical problems. You've mostly talked about it as like an everything else problem. Today you started out by saying what was sort of a marketing and sales problem and getting people to switching over to the communications, and now you're like, well, there's the business and finance and legal aspect of this in getting money in.

NICK: Yep.

MEL: Do you see those two particular things being connected? The marketing communication, the awareness and the user end of like an individual developer going, oh, shoot. I've got to switch this over. And then on the -- on a different scale, like that person's company being able to throw however many thousands of dollars they want at PyPI in some way. Do you see those two things as connected?

NICK: I do. In a complicated way. So, there's -- there's an interesting thing in -- just in tech communities in general. We honestly -- we like talking to other techies. Because it's easy. 

That means you can focus on the technical stuff. And not worry about who is getting paid by who, who is delivering value. Is what you're getting worth what you're paying for it? You just want to be able to knuckle down and go, we have an interesting problem to solve here. Let's solve it. 

But the reality is that large organizations where the -- well, all organizations, honestly, whether for profit or charitable or governments or whatever, they only have so much money to spend. 

And they're gonna -- they're gonna choose to spend it in the way they think will do good. Or they'll choose to spend it the same way they spent it last year. These are the two main ways budgeting works. 

And so, a lot of the time we fall into the trap of trying to engage with the world the way we wish it was rather than the way it actually is. And then we get frustrated when that doesn't work. 

And so, yeah. So, I think for me, specifically, yeah, it has been the case of, the stuff I have been involved in as far as packaging is concerned has been the non-technical stuff. 

I think -- I think I maybe made my first actual code contribution to pip this year. 

So, yeah. It was -- it was very much the case of being in that position of going to people, like, ”What has the potential to get in your way?” Or just seeing myself, ”This has the potential to get in your way. So, I'll make sure it doesn't.” 

It was quite interesting to read Donald's stuff, [where he was] going, "huh. Nobody ever got in my way." Mission accomplished, then.

MEL: Yeah, it was -- and that is -- it's also been, I'm hoping the second round interviews going out soon. Just waiting on people for open-licensing them. It's been really interesting to see people's reactions to some much Donald's excerpts. Because between you, Ernest and Donald, it's interesting to see the context. You're talking about the business side, the legal side. Ernest is very much coming from like, I am an infrastructure person perspective.

NICK: Yes.

MEL: And then Donald is the one telling the stories about, yeah, this basically started out as a tool that scraped the web interface. It's three completely different scales of telling the story.

NICK: Yep. Yeah. It is -- yeah. It's very much -- and I mean, that's where if you cover more along these lines, I would love to hear -- I would love to hear more about what it looked like from Sumana's point of view and from Nicole's point of view. 

And I think Dustin was one of the main contractors in the Mozilla grant. And so, yeah. And so, he's kind of gone on from that to be one of the main folks in the Python Packaging Authority. And I think that -- and I think that was the sequence there. That he was brought on board as the contractor -- no, hang on.
He was... yeah. I'm not sure exactly how that worked. But certainly it was the Mozilla grant where Dustin really got involved and active and then that continued after the grant finished. So, but yeah. It's -- it's --

MEL: There's a lot.

NICK: Yeah. There's a lot. And, I mean, you see in my interviews, I keep going on and rambling on about all this stuff around PSF and open source funding in general.

MEL: This is great. This is all information that we didn't have before that hasn't been put down, hasn't been tied together. And -- yeah? Sorry. Go ahead.

NICK: I was going to say, it was also interesting seeing some of the more recent board members going that they didn't know necessarily a lot about what was going on. 

And I think that also says a fair bit about the -- that in a lot of cases with the working group system within the PSF, that, yeah. Once the working group is started and knows what it's doing, there doesn't need to be a lot of hands on involvement from the board of the day. That as long as the working group is there and it's functioning, operating reasonably well, they get the month -- I think it's a report every other month from the different working groups.

But, yeah. It's like, they don't need to -- they don't need -- they're actually being able to get into that oversight role that is a sign of a healthy nonprofit that the staff are handling most of the day-to-day stuff. The volunteers in the individual working groups are able to get on and do their thing. And then the board is more about where the organization [is going]. 

The stuff -- the stuff Jackie was talking about and going, like, how do you grow the annual budget? Like, and actually make it like -- because it becomes that interesting thing of, there's an opportunity for a positive snowball effect. 

And we've seen this with the Mozilla grant. Like, once you start getting successfully executed grants under your belt, then potential funders go, “Ah. Yes. We can trust you. If we give you money, we can trust you to manage it well. Therefore, we're more willing to give you money.” And then you do it again and they go, ”Ah. That was more money well spent. What else would you like to do?”

MEL: Right.

NICK: And even if specific funders go, “Well, we've already given you enough money, we're not give you anymore, we want to help fund other people.” But at the same time, there's still then more funding opportunities that when you put your proposals into them, you now have a longer essentially resume as an organization where you can say, ”This is -- this is our evidence that we have the ability to deliver.” 

And for a long time, the PSF essentially didn't have that resume. They couldn't point back to successful project and say, “Here is stuff we have delivered successfully”.

Whereas now, particularly through the PyPI projects, it's been the case of, ”Yes, if given funding, we can turn it into improvements”. And so, yeah. And, yeah. And, yeah. 

It's been that thing of -- for a lot of the time it was a case of, we're going, ah -- we were going, yes, in theory money should be able to help. But we're not sure how. 

Whereas if the people are willing to do what HP did and essentially donate people's time, that was a lot easier to use. Because you didn't have to figure out “Who are we gonna pay? How much are we gonna pay them and what are we going to ask them to do? What does success look like?” 

If people are donating time, those questions are between them and their employer and the community doesn't need to worry about it so much.

MEL: So, I'm looking at the time. This has been fantastic. This is a lot of -- every time -- you put so much historical detail in your transcripts that afterwards as I'm reading through them I have to constantly do Google searches and be like, "I did not know that existed. What is that you're talking about?" This is fantastic. 

I'm hoping in the report when we synthesize this we can link out to some of the resources you mentioned as well. I have the goal of adding them in the first one.

NICK: When I mentioned Open Collective, there's another mob in New Zealand that I've forgotten the name of. The structure is amazing. I'm going to look them up. Try to look them up, because when I don't remember their name. It makes it difficult.

[Ed: Nick later wrote that, courtesy of Aurynn Shaw as per the tweet at https://twitter.com/ncoghlan_dev/status/1177362449462251520, he rediscovered this group: https://enspiral.com/]

Yeah, so. Yeah. Anyway. Thank you. 

So, I assume we'll do the edit the transcript again and clarify stuff?

MEL: Yep. Same as last time. 

And then since the third time is going to be the last time we talk about this, is there anything in particular that you want to make sure we do? Or anything to keep an eye out in other interviews? Anything like that?

NICK: I'm curious about what perspectives -- so, now that we all know who the six interviewees were, what perspectives other people think are missing. So, like I mean, the big ones for me would be Sumana, Nicole, Dustin and Eva. But, yeah. The -- but, yeah. What other people think. Or perspectives that might be interesting. Oh! Dan Callahan from the Mozilla side. He was the champion from the Mozilla grant.
Yeah. So...

MEL: Yeah. And this is --

NICK: Anyway.

MEL: On our side, that's something that my co-PI, Steve, is coming tomorrow and we're going to to talk about that. We only have funding for six interview participants. But like you said, there's a few really obvious people, if we got to do another round of this. I would also love to have the other people funded by the Moz grant, and Dan on the Moz side. So, we're thinking about this. If there's something we can do about that. Right now we got those six people. But because the research is open science, open data, we can go out and say, "hey! Dan! We're making this thing. If you want to take a look at it. You can. We don't have the resources to formally interview you," but yeah.

NICK: Yeah, exactly. So, yeah. Anyway. Thank you. I'll chat you next time.

MEL: Okay. Thanks, Nick! Bye!

NICK: See ya.
