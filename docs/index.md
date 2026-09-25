# When AI Writes the Code, What Counts as Contribution?

*An argument for evaluating engineering through outcomes, judgment, ownership, and the ability to make others more effective.*

**The central argument: Evaluate engineers by the useful results they help create, the decisions behind those results, and the capability they leave with the team, not by how much code or documentation they produce.**

If two engineers ship the same feature, but one produces ten times more code, who contributed more?

The code cannot answer that question by its volume alone. Neither can the number of pull requests, tickets, or documents attached to it. We need to understand what changed for users, which decisions mattered, and whether the team can safely operate and adapt what it shipped.

Generative AI makes an old measurement problem more urgent: how do we distinguish producing work from creating value?

My answer is not to replace code counts with spec counts. It is to make valuable judgment easier to examine, connect it to results, and recognize the work that improves a team's ability to deliver those results again.

## Table of contents

- [The problem existed before AI](#the-problem-existed-before-ai)
- [What activity measures can, and cannot, tell us](#what-activity-measures-can-and-cannot-tell-us)
- [A smaller implementation can represent a larger contribution](#a-smaller-implementation-can-represent-a-larger-contribution)
- [Four dimensions of contribution](#four-dimensions-of-contribution)
	- [1. Outcomes: what improved?](#1-outcomes-what-improved)
	- [2. Judgment: which decisions made the work better?](#2-judgment-which-decisions-made-the-work-better)
	- [3. Ownership: can we trust and maintain the result?](#3-ownership-can-we-trust-and-maintain-the-result)
	- [4. Team contribution: who became more effective?](#4-team-contribution-who-became-more-effective)
- [Make explanations useful, not ceremonial](#make-explanations-useful-not-ceremonial)
- [AI can write the explanation too, trust but verify](#ai-can-write-the-explanation-too-trust-but-verify)
- [Evidence over credential, but not without context](#evidence-over-credential-but-not-without-context)
- [A practical framework without a leaderboard](#a-practical-framework-without-a-leaderboard)
- [Safeguards against a new set of bad incentives](#safeguards-against-a-new-set-of-bad-incentives)
	- [Do not replace code volume with document volume](#do-not-replace-code-volume-with-document-volume)
	- [Separate a team's result from an individual's role](#separate-a-teams-result-from-an-individuals-role)
	- [Do not reward visibility alone](#do-not-reward-visibility-alone)
	- [Treat prevention claims carefully](#treat-prevention-claims-carefully)
	- [Account for opportunity and constraints](#account-for-opportunity-and-constraints)
	- [Allow useful failure and uncertainty](#allow-useful-failure-and-uncertainty)
	- [Keep the administrative cost low](#keep-the-administrative-cost-low)
- [What changes in a performance conversation?](#what-changes-in-a-performance-conversation)
- [Reward the contribution, not its packaging](#reward-the-contribution-not-its-packaging)

## The problem existed before AI

**Key takeaway: AI makes an existing measurement problem more urgent. Producing work quickly is valuable only when that work solves a worthwhile problem responsibly.**

Engineering activity and engineering contribution have never been the same thing. A large change can solve a small problem. A small change can remove a serious risk. A decision not to build can save more work than an impressive implementation creates.

AI does not invalidate a previously perfect measurement system. It gives us another reason to stop treating visible activity as a reliable account of individual value.

When an engineer uses AI to produce an implementation quickly, the hard questions remain. Was this the right problem? Were the requirements sound? Does the solution fit the surrounding system? Was it verified? Can someone maintain it after the original author moves on?

This is not an argument against speed. Delivering a useful, reliable result sooner is valuable. But speed needs a destination and a quality threshold. Producing the wrong thing faster is not the contribution we should reward.

Nor should this discussion begin with a threat about replacement. A useful contribution framework should help people understand expectations, improve their practice, and receive credit for valuable work. It should not turn AI adoption into a contest over who can generate the most output with the fewest colleagues.

## What activity measures can, and cannot, tell us

**Key takeaway: Activity metrics can help identify delays, bottlenecks, and repeated work, but they do not show the value an engineer created. Counting specifications instead of lines of code still measures the amount produced, not whether it solved a worthwhile problem.**

Lines of code, pull requests, tickets, story points, and hours describe aspects of activity. The mistake is treating them as interchangeable with contribution.

| Activity measure | What it does not establish |
|---|---|
| Lines of code | Whether the change was necessary, correct, or simpler than the alternatives |
| Pull requests merged | Whether the work improved a product or reduced a meaningful risk |
| Tickets closed | Whether the underlying problem was solved and stayed solved |
| Story points completed | Whether the result justified the effort or improved an outcome |
| Hours worked | Whether the time produced value, learning, or avoidable rework |
| Specs and research documents written | Whether the reasoning was accurate or changed a decision |

These measures need not disappear. A team can examine delivery patterns to ask where work waits, where tasks are too large, or where rework occurs. That is different from ranking individuals by their counts.

The distinction matters especially when we introduce new practices. If we stop counting pull requests and start counting specifications, we have changed the object, not the measurement problem.

**An artifact is evidence to examine, not a unit of contribution to accumulate.**

## A smaller implementation can represent a larger contribution

**Key takeaway: Credit the investigation and decisions that solve the problem, including the decision to build less. Neither a large nor a small deliverable proves value on its own.**

Consider an illustrative scenario, not an account of a particular employer or project.

A team is asked to reduce failures in a background processing service. One engineer proposes a replacement service and uses an AI assistant to produce much of the implementation. The work looks substantial: new components, tests, configuration, and documentation.

Another engineer first investigates the failures. They discover that the recurring problem involves duplicate messages and a missing idempotency check. They propose a smaller change, test the duplicate-message behavior, define a safe rollout, and explain which failure modes the change does not address.

Suppose the smaller change meets the agreed reliability goal without adding another service to operate. In that case, the valuable contribution is not the amount of code produced. It is the investigation, the decision to narrow the solution, and the verification that the smaller intervention worked.

The larger implementation was not necessarily careless. A replacement might have been justified by other requirements. That is precisely why contribution cannot be inferred from the size of either deliverable. We need the context, the reasoning, and the result.

The same test should apply to written work. A lengthy design document that changes nothing is not automatically more valuable than a short review that exposes a false assumption.

## Four dimensions of contribution

**Key takeaway: Examine contribution through four distinct questions: what improved, which decisions mattered, whether the result is dependable, and who became more effective. No single dimension tells the whole story.**

I propose four dimensions: outcomes, judgment, ownership, and team contribution. They are prompts for an evidence-based conversation, not a universal scoring formula.

### 1. Outcomes: what improved?

**Key takeaway: Connect the work to a worthwhile change and show the evidence. Separate observed results from expected benefits, and do not confuse an unsuccessful outcome with a poor decision.**

Start with the problem the work was meant to solve.

Did users complete a task more reliably? Did a recurring operational burden decrease? Did a team make a decision with less uncertainty? Did a necessary control become verifiable? Did an experiment provide enough evidence to stop an unpromising investment?

The point is not to force every change into a revenue figure. It is to explain the relationship between the work and a worthwhile result.

Before substantial work begins, agree on the intended outcome and what would count as credible evidence. After delivery, revisit that expectation. Distinguish what was observed from what is still a prediction.

Useful questions include:

- What problem did we agree to solve, and for whom?
- What changed relative to the starting point?
- What evidence supports that conclusion?
- Which costs or trade-offs accompanied the improvement?
- What remains unknown?

Not all outcomes arrive within a review period. Foundational work, maintenance, and research may need intermediate evidence. A migration rehearsal, a verified restore procedure, or a tested hypothesis can demonstrate progress without pretending the final benefit has already occurred.

Outcomes also need context. A sound experiment can produce a negative result. A good decision can encounter an external constraint. Evaluate the result and the quality of the decision separately rather than assuming one proves the other.

### 2. Judgment: which decisions made the work better?

**Key takeaway: Assess how an engineer tested assumptions, chose among alternatives, and handled uncertainty, not whether they personally typed every line or memorized every dependency.**

Judgment is visible in the choices that shape a result: defining the problem, testing assumptions, comparing alternatives, understanding dependencies, and deciding what not to build.

AI-assisted implementation does not remove the need for those choices. The proposed standard is not that an engineer must type every line. It is that they remain accountable for the decisions they accept and the claims they make about the result.

Useful evidence includes:

- An investigation that corrected the team's understanding of a failure.
- A review that identified a dependency before a risky change.
- A simpler design chosen after examining alternatives.
- A decision to stop work because the expected benefit no longer justified it.
- A test or experiment that challenged an attractive but unsupported assumption.

Research and specifications can make this reasoning visible. Their value depends on their accuracy and usefulness, not their length or format.

Understanding also has practical boundaries. No engineer can explain every detail of every dependency. The relevant question is whether they understand enough to make the change responsibly, identify where their knowledge ends, and obtain help when needed.

Comprehension is not a memory test. It is the ability to use evidence to reason about behavior, consequences, and uncertainty.

### 3. Ownership: can we trust and maintain the result?

**Key takeaway: Delivery includes verification, safe operation, and maintainability, not just merging code. Expect care proportional to the risk, and treat seeking help as part of responsible ownership.**

A contribution does not end when a change is merged.

Ownership means verifying the important claims, considering failure and recovery, checking the result after release, and leaving the work in a state the team can maintain.

This is where understanding becomes practical. Can the engineer investigate unexpected behavior? Can they connect a failure to a design assumption? Can another person identify how to deploy, observe, or reverse the change?

Evidence might include appropriate tests, a rollout plan, observed production behavior, corrected assumptions, or a useful handover. The exact evidence should follow the risk.

A small copy change does not need an architectural review. A change to payment processing or access control deserves more scrutiny. Requiring the same package for both would reward procedure rather than judgment.

Ownership should not mean solitary heroics. Asking for a specialist review or involving colleagues in diagnosis can be responsible behavior. The aim is dependable work, not an engineer who never needs help.

### 4. Team contribution: who became more effective?

**Key takeaway: Recognize work that helps others perform better. Judge reviews, mentoring, tools, and reusable assets by their usefulness to colleagues, not their visibility or quantity.**

Some of the most useful work changes what other people can do.

A careful review can improve a colleague's design. A clear explanation can make an unfamiliar system accessible. A maintained tool can remove repeated work. Pairing can help someone develop the judgment to handle the next problem independently.

This contribution should not be reduced to public visibility. The most vocal person is not necessarily the most helpful, and not every useful interaction produces a document.

Ask instead:

- Who used the work, and what did it help them do?
- Which dependency or uncertainty did it remove?
- Did a reusable tool reduce work after accounting for its maintenance cost?
- Can someone else now perform a task they previously could not?

Reusable assets deserve credit when reuse is justified. Not every novel problem needs a framework, template, or agent instruction. Sometimes the better contribution is a small, local solution that avoids imposing an abstraction on everyone else.

## Make explanations useful, not ceremonial

**Key takeaway: An explanation should help others understand the problem, the choices, the risks, and the learning. Use only as much documentation as the work needs, and keep it aligned with what actually happened.**

If judgment matters, we need a way to inspect it. An explanation delivered with meaningful work can help.

For a non-trivial change, four questions provide a useful starting point:

1. **What is this?** What problem does it solve, and what is outside its scope?
2. **Why this approach?** Which alternatives were considered, and which trade-offs mattered?
3. **What could fail?** Which assumptions, dependencies, and failure modes deserve attention?
4. **What did we learn?** What did investigation, testing, or operation reveal, and what remains unknown?

These answers can live in a pull request, a design note, an issue, an architectural decision record, or a more formal request for comments. A particular document type is not the point.

For a larger design, explaining the alternatives can be as useful as explaining the chosen solution. For a smaller change, a few precise sentences may be enough. Update the relevant explanation when implementation or verification changes the reasoning; do not preserve an outdated plan simply because it was approved first.

The questions also apply at different stages. Before implementation, distinguish findings from assumptions and open questions. After verification, record what the evidence actually showed. A promise to investigate is not yet a lesson learned.

**This is not a demand for more paperwork. Evidence should be proportional to the risk and complexity of the work.**

## AI can write the explanation too, trust but verify

**Key takeaway: A convincing explanation is not proof of understanding, regardless of who wrote it. Build trust by checking it against the implementation, tests, and practical use.**

A serious framework must face this objection directly: the code and its explanation can both be AI-assisted. A polished document does not, by itself, establish that a person understands the system.

Shipping the explanation beside the code makes the reasoning available for review. It does not make that reasoning true.

The test is whether the explanation matches the implementation, survives relevant questions, and helps someone act safely. Does a claimed guarantee have a corresponding verification? If an assumption changes, can the engineer explain the consequence? If the observed behavior contradicts the design, do they investigate and revise their understanding?

This is not an invitation to turn every review into an oral examination. Use the ordinary work of engineering: discuss a trade-off, inspect a test, walk through a failure mode, or ask a colleague to use the handover information.

An AI-assisted explanation can be useful. An entirely human-written explanation can be wrong. Authorship alone should settle neither question.

The artifact makes reasoning inspectable. Review, verification, and use provide reasons to trust it.

## Evidence over credential, but not without context

**Key takeaway: Examine concrete work and the person's role in it rather than relying on titles or tenure alone. Respect sustained experience and confidentiality; a public portfolio is not a requirement for proving capability.**

Degrees, titles, and years of experience describe parts of a person's background. They should not substitute for examining what someone can do in a particular context.

For contribution discussions, a concrete account is more useful than a label: this was the problem, these were the constraints, this was the person's role, these decisions mattered, and this is what happened.

That does not mean experience has become irrelevant or that a burst of visible output replaces sustained responsibility. Maintaining a system through changing requirements can demonstrate something that an initial delivery cannot.

Nor should this become a demand for public portfolios. Many engineers cannot share their work outside their employer. Internal evidence, a clear account of decisions, and appropriately anonymized examples can support a conversation without exposing confidential material.

The aim is to examine capability in context, not replace one status signal with another.

## A practical framework without a leaderboard

**Key takeaway: Use the framework to discuss patterns across representative work, with expectations matched to role and context. It is a guide for inquiry, not a numerical ranking or a verdict based on one task.**

The four dimensions can guide expectations at different levels without becoming a points system.

| Dimension | A reason to investigate | Evidence of dependable contribution | Evidence of broader contribution |
|---|---|---|---|
| Outcomes | Completion is reported without checking whether the problem was solved | The intended result is clear, and evidence and limitations are reported | The work improves an important result across a wider area or helps others select better priorities |
| Judgment | Important assumptions go untested, or choices cannot be explained | Alternatives, dependencies, and relevant risks inform the approach | Decisions reveal non-obvious risks, avoid unnecessary work, or improve others' plans |
| Ownership | Verification or follow-through is missing relative to the risk | The result is appropriately tested, observed, and maintainable | The work improves how the team verifies, operates, or recovers related systems |
| Team contribution | Avoidable knowledge gaps or dependencies remain unaddressed | Reviews, collaboration, and handovers help others work effectively | Colleagues gain lasting capability or repeated work becomes demonstrably easier |

A single observation is a prompt for inquiry, not a verdict. Someone may lack access, time, support, or a clear assignment. A junior engineer and a staff engineer should not face identical expectations of scope and independence.

Likewise, not every project needs to demonstrate all four dimensions equally. An incident response, an exploratory prototype, and a long-term infrastructure change have different purposes.

I would use this framework to examine representative work over time, rather than score every task or collapse the dimensions into a numerical ranking.

## Safeguards against a new set of bad incentives

**Key takeaway: Better categories do not automatically produce fair evaluation. Explicitly guard against paperwork quotas, credit capture, visibility bias, unsupported claims, and unequal opportunities.**

A framework can fail even when its categories sound sensible. These safeguards belong in the design, not in a footnote.

### Do not replace code volume with document volume

**Key takeaway: Reward what a document helped clarify or improve, not the fact that it was written.**

Ask what the explanation clarified or changed. Do not set quotas for specifications, research notes, or reusable assets.

### Separate a team's result from an individual's role

**Key takeaway: Recognize the shared outcome while identifying each person's actual contribution; do not give everyone, or just the presenter, credit for the whole result.**

Describe who investigated, implemented, reviewed, tested, operated, and enabled the work. Recognize shared results without assigning each contributor the entire outcome, or giving all credit to the person who presented it.

### Do not reward visibility alone

**Key takeaway: Look for valuable work beyond what is publicly presented, including maintenance, support, and careful review.**

Seek evidence from collaborators and from the work itself. Include maintenance, support, review, and quiet problem-solving, not just launches and presentations.

### Treat prevention claims carefully

**Key takeaway: Credit evidence-backed risk reduction without claiming certainty about incidents or costs that never occurred.**

We cannot observe an incident that never happened. Record the risk, the evidence that made it credible, and the action taken. A demonstrated failure in a test is stronger evidence than a claim to have prevented an unspecified future outage. Avoid invented savings or incident counts.

### Account for opportunity and constraints

**Key takeaway: Evaluate what people did with the opportunities and support available to them, not just how prominent their assignments were.**

People differ in project access, assignment scope, and available support. Evaluate decisions within those conditions rather than rewarding only people assigned prominent work.

### Allow useful failure and uncertainty

**Key takeaway: Credit sound experiments and honest learning even when an approach fails. Judge decisions using the information available at the time, not hindsight alone.**

An honest experiment that rules out an approach can contribute more than a confident success story with weak evidence. Distinguish reasonable decisions under uncertainty from careless execution.

### Keep the administrative cost low

**Key takeaway: Evaluate contribution using evidence from normal engineering work rather than creating a separate job of proving productivity.**

Use evidence already produced by useful engineering work wherever possible. If people spend more time assembling proof than improving the system, the framework needs adjustment.

## What changes in a performance conversation?

**Key takeaway: Replace activity totals with a few concrete accounts of the problem, the person's role, a consequential decision, and the evidence of its result. Test and refine the approach before using it for high-stakes decisions.**

The conversation should move from activity totals to a few concrete examples.

| Instead of asking only… | Ask… |
|---|---|
| How many pull requests did you merge? | Which changes solved an important problem, and what evidence shows that? |
| How many specifications did you write? | Which decision improved because you clarified the problem? |
| How fast did you deliver? | Did the result arrive when needed, with appropriate quality and follow-through? |
| How many tools or templates did you create? | What repeated work became easier, for whom, and at what maintenance cost? |
| How many incidents did you prevent? | Which credible risks did you identify, and how did that change the work? |
| What did you build yourself? | What was your role in the shared result, and whom did you help? |

An engineer should be able to bring a small set of examples: the problem, their role, a consequential decision, evidence of the result, and remaining uncertainty. Colleagues can add context that the individual might miss.

For a team trying this approach, I would start with a few completed pieces of work. Discuss where the framework reveals overlooked contribution and where it demands evidence the team does not yet collect. Adjust expectations before attaching high-stakes consequences to the exercise.

The framework should make conversations more accurate and useful, not merely more elaborate.

## Reward the contribution, not its packaging

**Key takeaway: The final test is what the work changed, not how impressive the deliverable looks. Reward useful outcomes, responsible judgment, dependable systems, and stronger teams.**

Engineering contribution can take the form of code, a decision, an investigation, a review, a useful explanation, or the removal of unnecessary work. None is valuable merely because it exists.

The question is what it changed.

Did someone solve a worthwhile problem? Did their judgment improve the approach? Can the team trust and maintain the result? Are other people now better equipped to do good work?

Those questions leave room for speed, technical depth, collaboration, and learning without pretending that one count can represent them all.

When AI helps produce the implementation, the standard should not become more output or more paperwork. It should become clearer evidence of responsible decisions and useful results.

**Measuring contribution correctly means rewarding the judgment and outcomes, not the output volume.**
