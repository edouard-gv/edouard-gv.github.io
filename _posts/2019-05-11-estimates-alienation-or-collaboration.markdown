---
layout: post
title:  "Estimates: alienation or collaboration?"
date:   2019-05-11 17:19:52 +0100
categories: agilite
---
[(Aller à la version française)]({% post_url 2019-05-11-les-estimations-alienation-ou-collaboration %})


**During a BBL at my client’s, graciously facilitated at the last minute by Chloé Mahalin from Itametis, we took the opportunity to deepen our understanding of the #NoEstimates approach and its challenges. In the exchange that followed, we more generally explored good use cases for estimates, and what makes an estimate reliable.**

**Personally, I had a political epiphany: I discovered that estimates do not necessarily trap us into a Hegelian master-slave relationship. On the contrary, they can trigger a conversation which helps everyone better understand expectations and their implications, and, ultimately, builds trust.**


Context
-------

<a name="_ednref1"></a>What are estimates? What is being estimated? During the discussion, the word “estimate” was thrown around, often without specifying what was being estimated. In our context (a large corporation’s IT department), estimates generally involve some form of the three standard project management measures: lead time/planning, costs/resources, and perimeter (the “Iron Triangle” [\[i\]](#_edn1)). First reminder from Chloé: one cannot estimate one of the indicators without defining or estimating the two others. The next time I will be asked a shipping date, I should verify that resources and perimeter are well defined.

As we talked, I felt the need to look further: is it relevant to estimate pure output? Wouldn’t it be better to estimate what is actually delivered to the end user? Or even the value brought to the team? To help answer these questions, I will walk you through what Chloé presented to us, the conversations that followed and the thoughts that popped into my head.

Conditions for reliable estimates, and their consequences
---------------------------------------------------------

Three general conditions are necessary for an estimate to be reliable.

<a name="_ednref2"></a>First, it should be based on past similar tasks – real ones, not our idea of the task. There is a significant difference between the time we effectively work on a task and the lead time, as the first does not take into account queue time or interruptions (which often come from the organization itself, like helping a colleague, and which Henri Kniberg proposes to resolve with the concept of “ideal man-day” [\[ii\]](#_edn2)).

In other words, we can only estimate equivalent experiences. In order for the estimate to be reliable, we try to make sure that past and present conditions remain similar. Thus, _believing the estimate prevents us from innovating and experimenting_.

Secondly, the perimeter should not fluctuate with time. From the outset, it must cover everything that is required for the product to work. This means making many assumptions – on deliverables, on their ability to satisfy the user, on how they will be used. And violating these assumptions would impact the whole system and lead to difficult choices.

Thus, we can only estimate if we are confident about the perimeter. As a result, _believing the estimate ultimately prevents the product from meeting the user’s needs_.

Thirdly, an estimate is only reliable if its context doesn’t change. The past must be similar to the present, with a similar team and technologies. Thus, one can only provide estimates with known technology and unchanged teams, limiting the unexpected. _Believing the estimate limits organizational and architectural continuous improvement._

<a name="_ednref3"></a>I began to see a pattern emerge: estimates only limit those who believe them. This could be a first insight into the CHAOS Report figures, which state that only 30% of IT projects cost as planned in the original estimate (a figure that is also up to personal belief – I haven’t found sound methodology to back it up [\[iii\]](#_edn3)).

The goals of estimates
----------------------

After this harsh judgment was presented, the audience maintained that estimates remain, nevertheless, necessary. Or, to phrase things like in the previous paragraph, that people need estimates they can trust. Several good reasons for this were mentioned around the table: simple, reliable estimates are a way to a) select partners and contractors on a cost basis; b) manage risks or even delegate risk management to third parties; c) arbitrate perimeters (on a ROI basis); and d) strengthen commitment.

However, because the conditions for a reliable estimate are rarely met, the audience suggested a few alternatives to attain these goals without using estimates.

Concerning the need for strategic decisions, such as risk management, understanding what can and cannot be done, making the right compromises such as striking the right balance between ambitions and available funding, the following solutions were suggested:

*   Do not gamble everything at the beginning. Invest a small amount that you can stand to lose with no regrets, and see how things go. For instance, before committing your entire budget to a supplier, ask to see what they can do with 5% of the budget (and later check that they did not overspend).
*   Have several suppliers work at the same time on small iterations, selecting (and paying) them at the end of the iteration, just like in Pop Idols or SuperStar.
*   Focus more on the impact of the product than on the deliverable itself.It is also said that estimates promote deeper commitment from both parties, even without a formal contract. The following points were raised against this argument:
*   <a name="_ednref4"></a>In addition, this approach should remove the cognitive bias known as the sunk cost fallacy, when the buyer has already paid so much money that they continue to fund the project even when it is no longer profitable [\[iv\]](#_edn4). At the BBL, someone gave the example of staying in your Uber despite being stuck in a traffic jam that makes your ride cost far more than initially estimated.

*   Short feedback loops produce stronger commitment than long term goals do
*   Human-sized estimates also generate better commitment.
*   One last point: estimates establish a dialogue between those who know what the needs are, and those who know how to meet them (and ultimately all the parties involved in a product). So in this case, there is no need to believe the estimate: it becomes an object of discussion and understanding, rather than a target to be met.

What about #NoEstimates?
------------------------

The starting point of this BBL was to talk about the #NoEstimates approach within Agile methodologies. This approach is applicable in particular to the various estimation exercises that we do as a team in Scrum ceremonies (Sprint planning, grooming sessions, with or without Planning Poker). Notice that the goals of these ceremonies are the ones mentioned above: giving the Product Owner an idea of what could be available in two weeks, understanding what each requirement really entails, commit the team, and, most importantly for me, having a discussion to align everybody on the same goals.

In this situation, I understand that #NoEstimates says that one should commit, for a sprint, on a number of user stories, and track this indicator in the burning chart, rather than estimating stories in story points (or worse, in hours or workdays) and using this as a progress indicator. It means that when the stories are presented, one should only distinguish those for which size is 1 from those over 1. Those over 1 must be sliced in order to have only size 1 stories. Ultimately, it boils down to measuring outcome rather than output. We change our own relationship to the burn-down chart when we look at it this way: we measure what the user sees, not how complex it is to implement a story, much less the time needed to do so. What we are doing has a purpose, we are creating real value! If you wish, then, you could improve the continuous flow of production, helping you shift from Scrum to Scrumban, which is closer to the paradigm of continuous delivery.

[![](https://pbs.twimg.com/media/D2CdGxbWsAAaXSP?format=jpg&name=small)_#noEstimates planning poker cards prototype, from Constantin Guay_](https://x.com/cog_g/status/1108058635077341185)

Indeed, this very much resonates with my personal experience: without knowing anything of the #NoEstimates theory, I had already noticed that when my team was mature enough, all the US were of 1, 2 or 3 story points – rarely 5. Over 5, we tried to slice it. And we knew that ultimately, some 1s were 3s and 3s were 1s. Thus the only benefit I found in the Planning Poker exercise was the discussions it triggered, both among the technical team and between it and the Product Owner. Ultimately, reaching a consensus on the estimate was pointless. I am not even talking about cases where the estimate stems less from personal conviction than from the position of someone within the group, for example when he or she adopts a rebellious or on the contrary a submissive stance.

In addition to the above, for a sprint estimate to be reliable, it should at least meet the following conditions:

1.  All stories should be the same size (#NoEstimates)
2.  For every story, one should have the same level of confidence in one’s ability to implement them (hence the notion of spike)
3.  All stories should have the same expected quality
4.  No story has to be thrown away (no “nearly done” stories)
5.  All stories should be sliced as much as possible. Anyway, a bigger story will be more expensive in the whole flow (merging, testing…)

There is nothing new under the sun: we must learn to slice stories intelligently! Teams must agree on the biggest size of a story, for example establishing that any story “should be tested by the end of the day”.

A typical example, when you have to implement ten simple and similar rules, is to put the first two in a story, including the factorization aspects, and the other eight in a second story.

In these conditions, #NoEstimates makes estimating sprints simpler and faster. And more generally, #NoEstimates works better with a team that is already accustomed to working together (for instance after several sprints), that is used to discussions on estimates, and that has built trust, both within the team but also with people on the outside, who will thus not ask for precise estimates either.

(And for those who prefer Kanban, slicing into small stories is essential for maintaining a continuous flow. This does not have to prevent the team from retrospectively estimating stories in order to gather improvement indicators.)

Back to our original question – what are we estimating?
-------------------------------------------------------

What are we trying to tackle when we estimate and plan? Why are we still basing decisions on unreliable estimates? I think that the underlying question is this: who is doing the estimate, and for whom?

Everything starts as a discussion between two parties which each have their area of expertise: those who formulate a need, and those who can meet it. But soon, a third group crashes the party: those who verify, or those who manage. Are the terms of the contract being upheld? Aren’t the costs slipping?

Therefore, why is it the third party that asks for estimates, and not the client itself?

I am confident I already know part of the answer: on the one hand Agility reduces the need for contracts and control, and attempts to produce maximal outcome for minimal output; on the other hand, estimates give us better control and reduce our fear of change.

And this is my conclusion, which I hope to remember all my life: most of the time, estimates are associated with a power relationship. They transform the relationship into a dominating or even an alienating one, considerably reducing freedom. The situation is Hegelian: one could say, by providing you an estimate I recognize myself as your slave. Who has never felt that knot in their stomach when asked over and over to recommit to a date given at the beginning? Sometimes this works the other way around: I recognize myself as your slave by believing your estimate. If the quote is the target, then the game will be to promise the moon in order to win the proposal.

Hence, to me #NoEstimates is a way to emancipate both parties, the sponsor and the producer.

<a name="_ednref5"></a>By extension, in large companies, estimates fuel the power play that allows a minority of people to organize control, for instance when risk management is shifted to employees who are forced to commit to deadlines, or, on the contrary, when an employee includes the deadlines as part of negotiations on unrelated matters [\[v\]](#_edn5).

On the contrary, estimates should raise discussions, creating a partnership based on the confidence they build. In this case, why not keep doing Planning Poker to get people to talk to each other, then discard the estimate as soon as everybody is clear on what has to get done? But in order for this to happen, power relationships should be reduced within the team (and the velocity in story points should not be shared with other parties that have a power relationship with the team).

There are other ways to emancipate ourselves from estimates. We already talked about measuring client value delivery (how it makes the client happier) rather than output or time spent: focus on use value instead of exchange value (man-days).

Another possibility is to focus on the problems that cause delays, instead of including these causes in the estimates – in other words, trying to solve the problems rather than optimizing the estimation process.

All this made me curious to learn more about “beyond budgeting” concepts.

Now more than ever, I am convinced that many truly agile practices encourage emancipation between developers and users, putting purpose back into our jobs and making us happier to get up in the morning!

Édouard Gomez-Vaëz, _in partnership with Chloé Mahalin, ITAMETIS_

* * *

<a name="_edn1"></a>[\[i\]](#_ednref1) Quick reminder on the iron triangle: if a perimeter and a deadline are already set, in order to estimate the resources needed to stay within those constraints, one must identify all the components of the future output and design the plan (aka roadmap). To do this, before starting off, all risks and uncertainties must be identified to ensure that the three golden variables remain the same throughout the project. Such is the promise of the standard project management methodology. In any case, none of the three dimensions can be estimated without the two others.

<a name="_edn2"></a>[\[ii\]](#_ednref2) See “Scrum and XP from the Trenches”

<a name="_edn3"></a>[\[iii\]](#_ednref3) Out of intellectual honesty, I should also mention methodologies that were not addressed during the BBL, and that go around these limitations. These approaches are much more complex. For instance, one is based on the pre-estimated cost of architectural bricks: by drawing the boxes, the idea is to ignore the cost of developing inside the box/team, and instead focus on the interfaces between the boxes/teams, accounting for the distance between them. However, this approach freezes the architecture from the outset, goes against emerging design and prevents the architecture from adapting to user satisfaction. It adds a specific constraint to project management.

Another methodology consists in distributing slack time at the end of a project without telling the teams, in order to reduce the bias that says that any time assigned to a task will be consumed by this task.

Nevertheless, to be relevant, these methodologies require expertise and come at a cost. Therefore, the first approach is mostly used in environments where innovation is not so important, and the second in strongly industrialized environments, such as aeronautical engineering, if I remember correctly.

<a name="_edn4"></a>[\[iv\]](#_ednref4) The Concorde airplane project is often given as a typical example of the sunk cost fallacy.

<a name="_edn5"></a>[\[v\]](#_ednref5) From our perspective, this aspect is reinforced by task specialization (Taylorism). In this context, the hierarchy, rather than peers, exercises control. Entire parts of the company are dedicated to managing the minority of people who actually fulfil contracts. Management is in pieces, and control can only be exerted through metrics and indicators, by measuring performance on the basis of compliance with a plan, rather than innovation. It follows that an estimates are just another metric which, by their usage, serve to legitimate strategic decisions made by experts of risk, budget, cost or human management. This is not the subject of this article, but it is one of our strong opinions.