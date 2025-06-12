---
title: "A Better Way to Work: eXtreme Programming!!! 🚨🔊 *DJ airhorn sounds* It's in the mix!"
description: How and why to use Extreme Programming
date: 2025-05-28
tags: [agile, pair programming, extreme programming, testing]
---
![Just a typical pair programming session.](./xp-hero.png)
Once upon a time, billions of years ago, at the dawn of time, which was about the midpoint of my career, I worked at a company that was trying to experiment with their software practices. I was asked to join an experimental team trying a new software methodology called **Extreme Programming**. I was very skeptical (dare I say, extremely skeptical?) of it, but I'm down for trying new things so I can talk about what works and doesn't. But it turns out, though, it was literally the most effective I'd ever been in my entire career. And I've literally been chasing after this ever since.

So allow me to explain to you how to program to the extreme and why you should start to practice it.

## The Basics of XP
So let me talk to you about Extreme Programming (aka XP). The most obvious thing is when you talk about XP, it should probably be accompanied with [an airhorn sound](https://youtu.be/UaUa_0qPPgc?si=qD5_Mk0tAcmKEUjS) for maximum enjoyment. (Please don't actually buy an airhorn or play that sound effect all the time. This is meant to be a joke. So please laugh and move on to the more important paragraphs.)

At its core, XP's most important and notable processes, compared to other Agile methodologies, are its strict enforcement of **pair programming** and **test driven development** (aka **TDD**). The reason it's called **extreme** programming is because these two practices are very intense when done for an entire working day. But it can also be extremely rewarding, productive, and helps share the mental load of the problem you're trying to solve.

### Pair Programming
So, as the name implies, you have two engineers write the code together.

A common criticism is that some engineers feel that this slows them down. But what they don't realize is how much this will save them later, as they are no longer a knowledge silo on a particular implementation, and their solution can often be made either more optimally or at least more maintainable with a second pair of eyes on it.

Pair programming isn't for everyone, but for people that enjoy collaborating on solutions, discussing trade-offs in real time, and don't enjoy waiting around to get feedback, it is invaluable. It's basically real-time code review *and* a continuous learning experience, ensuring higher code quality and shared understanding.

### Test Driven Development
When you practice TDD, you write the test first. You have a function call, or an API endpoint, or a user interface. You call, click, or execute that code and expect to see a return value, a UI interface change, or a side effect. Because you've written the test first, it fails. With a failing test you now write the implementation to make it pass. You do this a few times and make a few more test cases. As you implement, or possibly as the code gets hard to maintain, you'll refactor your implementation with better abstractions while also ensuring that the previous tests still pass. This is called [**Red, Green, Refactor**](https://medium.com/news-uk-technology/is-the-red-green-refactor-cycle-of-test-driven-development-good-9e2b1b52d721).

* **Red** is the failing test.
* **Green** is when you make the test pass.
* **Refactor** is whenever you rewrite the code because you've decided that there are enough use cases to come up with a better abstraction to handle the implementation.

### TDD with Pair Programming
TDD and Pairing go extremely well together when using a pairing technique called [**Ping Pong**](https://labspractices.com/learningpaths/application-development/pair-programming/#tdd-ping-pong). The idea is that you'll be swapping driving roles regularly. One pair will drive and write a failing test; then the second pair will drive and write the implementation to make the test pass. From there, instead of giving the first pair the driving seat, the second pair will write the next test or extend the current test so that there is a new assertion to implement against. Then the first pair takes the driver's seat again and writes the implementation.

It basically goes back and forth like this until the task is done. All the while refactoring the code as needed when, say, an abstraction is needed to handle repetitive use cases.

There are a few other ways to pair program, but I think I like Ping Pong the best as it gives a pretty well-structured way to swap the driver role. Maybe I'll go over other ways to pair program in another post someday and their pros and cons. But for the most part, just go with Ping Pong. It's easier.

## Feedback Loops
So, the reason XP is focused on Pair Programming and TDD, is because it creates tight feedback loops. The process is really all about having constant and steady feedback. Not just on writing code (which we get with tests and collaborating with our peers), but also with continuously releasing software, iterating on software, reviewing what needs to get done, discussing what should be done, reprioritizing what should be worked on, and reviewing how the process is going.

Let's talk about the feedback loop from smallest to largest.

* TDD (minutes) - write test and make test pass
* Ticket (hours/days) - Get a user story to implement
* Pair (day) - Assign pairs to implement tickets
* Iterations (week) - Period of time to do work and review how things are going.
* Project (months) - The product that is being built
* Organizational Learning (quarters) - Swapping engineers between projects to prevent knowledge silos and propagate emerging best practices
* Strategic Adaptation (years) - A bit outside of the scope of this post, but reevaluating company priorities based on market/industry/societal changes.

We've already covered TDD and Pairing a bit. So, let's talk about just how we do that with...

### Iteration
We can also call them **Sprints** or whatever. The point is that it is an arbitrary amount of time in which to do work and review how the processes are going.

Most places will do 2-week sprints, and I've heard of places having 1-week or even 3-month sprints. I cannot possibly fathom how anything longer than 2 weeks could possibly be a good process to encourage feedback. But I've personally found 1 week iterations work ideally. It also works well to set up recurring meetings to improve the process and ensure the next week can attempt to change practices and test implementation to see how it’s going.

The Iteration week will consist of three meetings: **Iteration Planning**, **Retrospective** (these two meetings act as bookends, starting and ending the Iteration), and **Stand-ups** which happen daily to ensure regular team alignment and setting up pairs for the day.

#### Iteration Planning
Also known as a *pointing party*. Traditionally, this meeting is meant to scope out work for the next iteration (for the next week, not the current week). However, since priorities change, sometimes the point of this meeting is to scope out work for this iteration. But this should be uncommon (though it does happen more often than I'd like).

##### Scoping
When we say scoping out work, it refers to understanding how much effort goes into completing the work for a ticket. To keep this as simple as possible, to avoid analysis paralysis and creating too much cognitive overhead, we use a very simple heuristic to size a ticket: we try to measure how complex the user story is.

How to measure complexity is also extremely difficult, so we try to make it even easier. We reduce the measure of complexity to 3 points, following a very simple model of T-shirt sizes: 1 (small), 2 (medium), 3 (large).

When something is 1-point, it is of small complexity. Meaning the requirements are clear-cut and there is no ambiguity in how to implement the code.

2-points is a medium amount of complexity. It might mean there might be some unknowns like relying on some dependencies outside of the team’s control, but for the most part the tasks to complete the ticket are pretty well understood. An example of a medium level of complexity is having dependencies on a library or another team's code, but we are pretty confident we should have good documentation on how to integrate with said dependency.

3-points is a large amount of complexity. There are many unknowns. We don't even know if there are APIs or libraries we can use as dependencies to solve our problem. Worse, we might not even know how to solve the problem or understand the problem space enough to even solve it.

So the rule of thumb is, we only work on 1-point tickets. We take on 2-point tickets, because sometimes we just need to implement something with a few unknowns, but it should still not be extremely high risk. And if a ticket is 3-points, that's extremely high risk and we need to have many questions answered, so we should create a spike ticket to scope out work that needs to be done to create a 1- or 2-point ticket based off of the things we do know about the 3-point ticket.

There is nothing over 3-points. Work only gets done if it is a 1- or 2-point ticket.

0-Point tickets are tickets that don't bring value to the users, but they usually brings value to the dev team. Like say improving tooling or looking at de-scoping a 3-point ticket.

#### Retrospective
In my humble and biased opinion, this is probably the most important meeting. This isn't a meeting to complain for no reason. This is a meeting to understand pain points and how to mitigate or even eliminate them. The point isn't to blame anyone for pain points. The point of no-blame retrospectives is to understand and brainstorm as a team on how we can avoid these situations in the future. If the process of XP or Agile is the problem, this is the meeting to voice it and address the current process's shortcomings.

Creating a list of pain points to address them makes the team feel heard. Knowing that pain will be lessened will allow the team to go faster and give everyone more agency to be the change they want to see in the work environment. This is meant to be a psychologically safe space where team members can be open, honest, and candid.

If, purely hypothetically, the situation is caused by a person, then it should not be thought of as an attack on that person, but instead a reflection of behavior or a disagreement in a decision. It should not be a personal attack on an individual. Though I have never seen anyone bring up a person in a negative light in a retro, there should be some room for safety to bring up disagreements between individuals. But the point of the no-blame part is to ensure we're focused on the situation and how we can resolve that. If someone has written bad code, it doesn't matter who it was; it's more that we are now in a situation where we need to deal with code that is hard to work with. We all write bad code, at some point in time. So don't hate the player, hate the game.

There are many ways to run a retro, but my personal favorite is [the Mad Sad Glad retrospective](https://miro.com/templates/mad-sad-glad-retrospective/). Though we called it "Happy, Meh, and Sad," the concept is literally exactly the same.

We want to have an open forum to allow team members to help shape the process. We give props to people that we're having a great time working with. Talk about if a piece of code is problematic to work with, or if processes aren't working for a particular team member. This allows us to identify pain points so that we can create action items to resolve them next iteration.

An action item is a task that was identified during the retro that needs to be done to remove pain points. Action items are usually assigned to a person, like an engineer or the product manager, which will attempt to be resolved. If it is an engineer, they pair on resolving it during normal work hours. Examples of Action Items: investigate a flaky test (does not necessarily need to fix it yet), refactor a particularly problematic part of the codebase (depending on how problematic, this might get turned into some 0-point tickets), look into automating very repetitive tasks, or improve build and test times. These things are annoying for the team to deal with but technically don't bring user value to the product. So, while they're usually not worth capturing in tickets, they will still make the team's quality of life improve and are worth looking into.

If action items are not completed by the next retro, we need to reevaluate if it's worth keeping or if we need to prioritize it more or escalate its results.

Likewise, if we see the same action items appearing in retrospectives time and time again, we need to do something to address the issues. It can be extremely emotionally draining and will foster resentment and learned helplessness if nothing can be done. And I have yet to see pain points that cannot at least be mitigated to a slight annoyance.

#### Stand-ups
We start the day with a stand up. This is a simple meeting where team members report what they did last working day. Since pairing is encouraged, after one pair gives their status update, the other pair will say their status is covered, or add details the other pair may have left out.

The real point of this meeting is to bring up any blockers that are preventing work. The hope is that someone may know how to unblock the work, or it can be looked into by a team member or a pair.

This meeting should be quick and short. It should be time-boxed to 15 minutes. Any longer, and more in-depth discussion can be taken offline to be handled later.

After standup, pairs are assigned. Pivotal Labs created this simple web app called [Parrit](https://parrit.io/home/login), which can be used to assign pairs to ensure team members are working with a new team member every day. Highly recommend it; it's awesome and simple.

If the pairs from the previous day did not complete their ticket, one of them carries the ticket to the new day, gives context to the new pair, and works with the new pair to finish the ticket. Sometimes, some tickets will take multiple days to complete (though this should be very rare). By constantly swapping out who carries the ticket forward, it spreads knowledge to the team, allows others to bring their perspective to possibly solve a novel or tricky problem, and reduces burnout on particularly difficult problems.

## The Life and Times of a Ticket
What is a ticket exactly? It's a user story. The Product Manager has identified a feature or user need that needs to be addressed. They should have come up with this user story based on feedback from stakeholders and users.

A ticket needs to clearly define what needs to be implemented and be testable.

So, after a PM has identified a feature that needs to be implemented, they need to scope it down to a story that can be implemented without too much ambiguity. Then they write out the user story and put it in the backlog where it'll sit until Iteration Planning.

### Iteration Planning (from the perspective of a ticket)
At the iteration planning meeting the PM presents the ticket to engineers. The engineering team will discuss if they understand the ticket well enough, as well as its complexity, while attempting to avoid implementation details (a herculean effort from the eng team, I can assure you). To prevent discussions from going on too long, we try to time-box discussion to about 2 or 3 minutes, 5 tops, as we have many other tickets to go through.

After the PM describes the features, engineers can ask some clarifying questions, but usually we go straight into pointing. Building on our previous understanding of 1, 2, or 3 points, engineers all at once show (with fingers, playing cards, signs, or a piece of paper) what number they pointed to the ticket. If everyone agrees, that's the point for that ticket and we move on. Else, engineers discuss why they picked that number. Some engineers can reevaluate their stance and agree to change their points to match their colleagues, or else whatever the majority agrees on is the number the ticket is pointed to.

If a ticket is given 3 points, meaning there is a lot of complexity and unknowns, the PM may create a 0-point spike ticket to investigate, remove ambiguity, or find more ways to break the ticket down. After the spike ticket is completed, the engineers on the ticket talk with the PM about what they discovered and their suggestions for smaller tickets, which will be presented at a later Iteration Planning for pointing by the whole team.

If, hypothetically, a ticket is found to be pointed wrong later, this should be brought up in the retrospective. The team will learn and calibrate accordingly to make more informed decisions on sizing.

### Work
Pointed tickets are raised to the top of the backlog and are placed in the order of priority that the PM decides.

When engineers need new work, they grab the first ticket off the top of the backlog and start to work on it. They'll pair up, write tests for it and ping pong back and forth until they believe they've finished the work. They merge the code into the main branch (no need for code review as the pair should have been live code reviewing), which should automatically get deployed to the development environment.

The ticket is then moved into review and is assigned to the PM.

### Validation
When the PM has time, they take a look at what tickets need to be reviewed. And go to the development environment to validate that the ticket was implemented within their specification. This traditionally involves a UI, but occasionally might require them to make API requests (perhaps using [Postman](https://www.postman.com/)) to an endpoint and validating that a piece of data was added to a database. PMs should be slightly technical. We're not talking about PMs needing to know how to code (though that can be extremely helpful) or how to make complex join queries in SQL, but they should know how to do at least the basics and have access to do so.

After the PM reviews the implementation, they either move the ticket to completion (as their requirements were met) or, if something was missed, hand it back to the engineers and talk with them about what was missing. Another possibility is that the ticket was completed to specification, but the PM discovers missing functionality or, after interacting with it, realizes the feature is not ideal. If that's the case, the PM generates more tickets to implement ways to improve the feature or to remove the feature.

Validation is an extremely important step as it'll be the first bit of feedback to know if we are building the right thing. Without this feedback loop, we're just doing waterfall and will be surprised when the product launches and no one is interested in it. This gives us the perfect time to pivot early to save the product or know we're building the correct thing and should continue.

## Project
Let's move one more feedback loop higher than Iterations is the Project. The Project is what we are building. In theory, you've already identified a problem space to scope the project to and explore solutions. If not, that technically can be a project in itself—scoping out problem spaces to explore for a company—which sounds a bit too meta, so we won't be covering that here.

Don't get bogged down in details. Analysis paralysis is a real problem, so to avoid it, you just need enough information to get started. As development happens, the problem space will be explored and solutions refined.

At this point it's worth keeping in mind some [Lean software development](https://en.wikipedia.org/wiki/Lean_software_development#Lean_principles) principles. (All the principles are worth keeping in mind for each of the loops.)

*Decide as late as possible* (I've also heard this phrased as 'delay choices to the last responsible moment). This is to say, don't get bogged down in implementation details. As an example, whether to go with SQL or NoSQL for a database isn't important; what is important is the outcome of the solution.

*Amplify learning* (I've also heard this phrased as 'fail fast'). Assume that all our solutions are wrong (to avoid analysis paralysis), and we should just pick one that's good enough to learn from, to make a more informed decision next time around. This also leans into *'deliver as fast as possible'* so that we can facilitate learning quickly and pivot to the correct solution quicker.

### Project Kickoff
So, let's say we have our problem space. What we need is a kickoff meeting so all the members of the team can brainstorm solutions. This allows everyone to be on the same page with the same context, as well as allowing team members to have ownership of the solution and helping with self-organization.

The Product Manager should have a good idea of the problem space. In the kickoff meeting, they explain the problem to the engineers and designers (if there are other team members like Program Managers [not to be confused with Product Managers], Scrum Masters, or Agile Coaches, they should also be included) on the team.

After the problem space is explored, there is a short questions-and-answer section to help elaborate on and remove some ambiguity if possible. Solutioning should be avoided at this point, because it will be happening in a moment.

After that wraps up, we move on to brainstorming. This is the part where everyone starts to come up with different solutions to the problem space. The ideas need to be movable, so note cards or sticky notes make the most sense. If you're doing this practice online, having virtual equivalents in a Figma jam board or slide deck can also work.

After this, the notes are gathered, and we discuss the solutions on each note to help give everyone context and possibly refine the idea a bit (don’t spend too much time on refining). As discussions happen, some ideas may sound similar and they can be grouped together.

#### Initial Prioritization
Now that we have all our ideas, it's time to prioritize them using a variant of [the Eisenhower Matrix](https://www.youtube.com/watch?v=tT89OZ7TNwc), a [Difficulty Impact Matrix](https://www.timetrackapp.com/en/blog/difficulty-impact-matrix/).

First, we're only going to focus on understanding each solution's impact relative to other solutions. A solution is represented by either a note or a collection of notes. We grab one solution at a time and ask how it compares to the solutions we've already looked at. We place the solution between other solutions, or at the top if we all agree it will be very impactful to implement, or at the bottom if it sounds less impactful.

Once we place all the solutions relative to each other in terms of impact, we then start at the top and decide how difficult it is to implement. If it is easy, we move it on the left side of the axis, representing difficulty. If it's hard to implement, we move it to the right side of the axis.

Once each task has been measured for impact and difficulty, now we have our priority. Solutions that are easy and high-impact are prioritized for the backlog first. Solutions that are easy but impactful will go next in the backlog, as quick wins should always be prioritized. Work that is difficult but impactful is next in priority. And solutions that are hard and low-impact are removed.

Both difficult/impactful and low-impact/easy-implementable features may be deprioritized altogether still, but they're left in the backlog just in case engineers run out of work.

From here the PM now has an idea of what user stories need to be generated to populate the backlog.

## Organizational Learning
Best practices are always evolving. Employees are always learning better ways to do things, and these should be propagated through the organization. New processes are made; old ones discarded. How we envision a framework or core technologies being used may differ from real-world usage. Or there may be gaps in solutions that no one working close to the metal has realized exist.

> In theory there is no difference between theory and practice; in practice there is. --(wrongfully attributed to) Yogi Berra

The best way to propagate learnings is by collaboration and doing. No one reads docs (not literally no one, but it's hard to find time), and docs become stale and can't keep up with new ideas being added and old ones being discarded. So, rather than doing so, we attempt to allow best practices to evolve and ebb and flow through constant team member rotations.

Take a pair of engineers off one team and put them on another, replacing them with another pair of engineers from yet another team. This allows ideas to propagate between teams. It also exposes team members to new problems, helping to train them on how to solve new and novel problems, or help solve old problems in novel ways that the current team may not have thought of before.

Because of XP's practice around pairing, a team's velocity is barely impacted when onboarding new members.

Some people may feel this is dehumanizing, treating engineers as literally interchangeable cogs in the machine. But in reality, this is a benefit. Working in the same problem space can be quite boring. As well as developing a more generalist skill set helps engineers tackle any problem, making them more valuable and easier to adapt to new problems.

The obvious benefit to the organization is that institutional knowledge is spread out more, and the [bus factor](https://deviq.com/terms/bus-factor) is incredibly high. The organization can operate extremely consistently.

## Strategic Adaptation
I don't have a good framework for this. But at this stage, leadership should be attempting to find problem spaces to facilitate the entire fly wheel of feedback loops.

## Critique
Naturally people will be critical of XP. It's a paradigm that is easy to be skeptical about. So let me attempt to rebut a few common criticisms of XP.

### Brooks's Law
> "Adding manpower to a late software project makes it later"

As Brooks points out, adding more people to a project can delay it, as it requires more time to onboard new members, more meetings to coordinate members, and more chances for misunderstandings leading to mistakes.

XP is quite literally a response to Brooks's Law. By pairing, onboarding new team members does not hurt the overall productivity of the team. Because feedback is tight with pairing and regular ceremonies, coordination and alignment are naturally built into the process. And with regular validation from the PM and stakeholders, misunderstandings can be caught sooner and fixed.

On top of this, other benefits are that we raise the bus factor and reduce knowledge silos. So if a team member leaves, it does not hurt the team's velocity, as all team members should have a pretty good idea of how the entire system works.

So, yes, we are not necessarily going faster with XP, but our release cadence is more stable, and code confidence is higher.

### Jonathan Blow's Hot Take
[src](https://youtu.be/21JlBOxgGwY?si=ffomQ1XTpQIBMSuN&t=30)

> This whole thing about TDD about writing the tests before you write the code is nonsense because you don't exactly know what you're building yet if you're doing anything interesting so you can't write the tests yet, right?

[src](https://youtu.be/21JlBOxgGwY?si=ffomQ1XTpQIBMSuN&t=57)

> If you're doing TDD, you're writing tests for a design that you know is going to rot very early. Like that's not good

I completely disagree with Blow, but I can see where he comes from. Blow is an artist and an auteur. Blow's code is his paintbrush. He doesn't even know exactly what he wants to paint until he discovers it while doing so. Likewise, video games are extremely complicated, near-infinite state machines that are near impossible to unit test. So it’s hard to test when you have a near-infinite number of inputs.

So now for the rebuttal: we don't normally build interesting things as software engineers. We have a very finite state machine. For the most part, we know what input we need to take and what output we need to give to the user to know they've succeeded at inputting data. This is knowable, and we actually want our code to be this level of boring and be this predictable.

As for the code rot: if you are making changes to code and need to rewrite tests every time, you're probably testing implementation details. And this is a big no-no in TDD. You don't want your tests to be brittle; otherwise, they're useless and you might as well not have tests. Tests are meant to give you confidence when you refactor, ensuring you don't break functionality or introduce a regression. A test that always breaks when making changes is testing nothing, so delete it.

[src](https://youtu.be/21JlBOxgGwY?si=ffomQ1XTpQIBMSuN&t=11)

> The amount of test code that you end up writing for an actual program, in a lot of these setups, is about the same as the program. And in some companies, it's actually ten times as much

[src](https://youtu.be/21JlBOxgGwY?si=sQ6pXQsecqjLsazB&t=269)

> You have huge amounts of test code that makes it hard to change anything, so you're not agile anymore

[src](https://youtu.be/21JlBOxgGwY?si=0cs4_v0EXOyqfjc8&t=276)

> You can't refactor easily because you have a huge number of tests to change now. That keeps you stuck

Sometimes you do need to write more tests to ensure you cover more use cases.

But we should also attempt to test from the highest level of abstraction. It's less meaningful to write unit tests unless something is just hard to test. The reason for this is that the smallest unit should theoretically also be covered by high-level integration tests. Blow even agrees with this. And the point is that everything between the input and output should be a black box that we don't care about. This allows for much less brittle tests and more confidence when refactoring.

### Too Expensive
You might think that XP is expensive because you're having two engineers write code at once. That's twice the salary for each line of code. But it turns out that it ends up being only about 15% more expensive. [src](https://www.ayeconference.com/laurie/Papers/XPSardinia.PDF)

On top of that, the other benefits—of being more focused on a task, increasing the bus factor (we all like to go on vacation from time to time), overall enjoyment while working, and better code quality—are substantial. So, for 15% extra cost for code, that's a huge benefit.

## Why not Zoidberg?
I've scattered the why to practice extreme programming through out this massive blog post. So let's attempt to summarize them all here, so you can have an easier time advocating the whys in this easy to read numbered list (your doctor won't believe number {randomNum()}).

1. Higher code quality and fewer bugs
2. Reduced knowledge silos and increase bus factor
3. Levels up developers faster
4. Increased developer engagement & morale
5. Reduced onboarding times
6. Stronger product-engineering alignment
7. Reduced rework and waste
8. More stable processes
9. More predictable releases
10. Living documentation as tests

## Conclusions
These are the practices I remember learning from Extreme Programming. It was literally the most productive I've ever been as a software engineer. XP isn't just a methodology, it's a philosophy of continuous improvement through tight feedback loops.

Whether you adopt all the practices or just a few, the faster you can learn and adapt, the better software you'll build. When you implement everything together, it is pure gold. But even if you can't get everything, be the change you want to see in your company. Start small, maybe a pilot team to try out pair programming and TDD. Even adopting one practice can give you a taste of those transformative feedback loops. The goal isn't perfection; it's progress toward a better way of building software.