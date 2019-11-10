# Explanation

This is an exercise we did during our analysis retreat based on the game "Snake Oil" (https://boardgamegeek.com/boardgame/113289/snake-oil) where players have to make up products based on cards they have in their hands. Similarly, we tried to come up with (preliminary) answers to our research questions based on the materials and insights we had generated during the retreat.

Shauna

# 1.  What implicit/explicit contracts/expectations do people have about FOSS digital infrastructure?

Implicit, downstream:

* that is "just works" like #magic without having to think about it (no obligation to keep up/not bothered by updates)
* that if you *do* want to understand it you can because it is #transparent
* that if you have problems with it, the people who work on it can and will help you solve your problems
* that the needs of the project are primarily technical and therefore the primary way you could give back to the project is through engineering
* that the creators of the project will not make major changes that affect me without warning me
* I deserve access to this infrastructure without payment or other contribution to the project

Implicit, upstream:

* that if something goes wrong with the project, it's my responsibility to fix it (#burnout #emotions)
* that because I'm working on it, I decide what happens with it (#doocracy #authority)
* that, at the same time, I shouldn't decide to do something that will disrupt the experience of users
* that if I'm scarce on resources, I should prioritize engineering over community, financial, legal, etc. (or, less consciously, this is what I know how to do so I will focus on it.)
* users shouldn't have to pay or otherwise contribute to the project in order to use it

Explicit: [skipping for now, don't have a lot of insight into common types of FOSS legal contracts]

# 1a.  What are the tensions in expectations?

* Downstreamers expect infrastructure to "just work" but when upstreamers can't fix problems they can't ask for help from downstreamers without violating that expectation.  Often, because communication between upstream and downstream has assumed no communication it's very hard to open lines of communication.

* Upstreamers often focus on engineering needs and because it's a doocracy, they have the implicit authority to determine what gets asked for/worked on.  Downstreamers/outsiders may be able to contribute vital non-engineering things but won't because upstreamers don't ask them or create space for them to do so.

* Some downstreamers expect help and problem-solving from upstreamers beyond what the upstreamers can provide, which leads to anger from downstreamers and guilt from upstreamers.  Because of the shared belief that downstreamers don't owe anything to the project, it's easy for demands from downstream to overwhelm capacity of upstream to handle them.

# 2.  What are conceptions of a well-maintained/sustainable FDI?

Well-maintained projects have: responsive maintainers (meets downstream expectation about getting help); high bus factor (eases impact of upstream expectation that if something goes wrong it's my responsibility fo fix it); diverse community (avoids downstream expectation that only technical contributions are needed; avoids upstream expectation that maintainers should focus on engineering because a diverse group will have diverse skills to contribute).

# 3.  How does PyPI illustrate #1 and #2?

In interviews, people talked about not realizing PyPI was having difficulties.  PyPI maintainers more or less met the downstream expectation that it "just works".

Interviewees talked about governance (Nick), project management (Sumana), design (Nicole), and other non-engineering ways of contributing to the project and how that made them more well-maintained and sustainable.

Sumana

_On implicit and explicit contracts/expectations:_

* If there is a specific person or organization who has earned #trust and whose support of the infrastructure is considered #magic, they need to speak up about #burnout or other problems before other people/organizations will step up to help. Help is pull, not push.
* It is natural and #evolution for people to #burnout, for #authority to fall via #doocracy to certain #contribtypes, for #speedexpectations to be variable in the absence of #contracts, and for users to only be able to expect the kinds of work and progress that #selfdirected #motivation from certain #contribtypes (per usual #whatisfoss fossroles) will drive.
* We have #emotions around what we expect, and we want to protect ourselves from others' #emotions, serving our duty but not being overwhelmed with their perceptions of their needs/desires, to prevent #burnout.

_On conceptions of well-maintained and sustainable FOSS digital infrastructure:_

* The #speedexpectations are met, not just when/if the user assessing sustainability/maintainedness needs something, but in the recent past, when the user uses #transparency and #tooling such as GitHub to check on recent commits and bug replies.
* There exist #contracts -- explicit financial ones to ensure labor for upkeep -- or the implicit contract of #magic in that it works reliably and thus creates expectations of reliability.
* Even without #personalconnections, the infrastructure does what you need it to do.
* #Corpdirection is not a driver of the product direction.

_On how PyPI illustrates those:_

* The #financialinfrastructure of the PSF and the #contracts started with the Mozilla award influenced people's perception of the maintainability and sustainability of PyPI.
* While #selfdirected #doocracy #motivation #whatisfoss labor led to the creation and initial work on Warehouse, and while sponsors gave PyPI in-kind donations, the donation of money via the MOSS award #contracts #financialinfrastructure is what made the phase change possible to increase PyPI's #busfactor.
* Our #personalconnections to Donald, et alia affect, even determine, the #linesofcommunication that cause us to understand whether PyPI's #busfactor is adequate. (Tension: deep focus versus broad awareness.)

Mel

# SJ

1.Contracts/Expectations
#speedexpectations, #communitymanagement,#linesofcommunications,#trust,#fossroles,#contribtypes, #tooling
In infrastructure there's an expectation of rapid turnaround of issues and little or no downtime.  Within a theoretical well-managed community this is facilitated by clearly defined roles, contribution/contributor type, trust and clear lines of communication.  A less well managed community might result in things falling to a small group or a single point of failure #busfactor #authority #do-ocracy. Depending on the project good tooling and piplines may be able to be developed to support this.  Corporate support of an unrestricted gift can be usefull here, whether that gift is of an internal employees time or cash to an external foundation to support sustainability
1a.Tensions
How much of the mainteneance and upgrading is organic/structured, do the contributions and the contributors end up bing long term /short term, how much of the transparencyinherent in the community becomes an obligation to stay on top of things and how does it end up as a do-ocracy vs. and inclusive community of contributors?
What are a conceptions of a well maintained and sustainable FOSS program.  See #1 really.
How do the narratives collected aroundPyPI illustrate this?  The shows an effort to move from one that was initially not well maintained and sustainable to one that is moving closer to meeting the conceptions and expectations of a well maintained and sustainable project, due, in part to some forms of #corpsupport.
