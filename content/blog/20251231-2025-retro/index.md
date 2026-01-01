---
title: "2025 Retrospective"
description: "What a wild ride this year has been."
date: 2025-12-31
tags: [tech industry]
---
![Hypocritical AI generated slop hero image.](./hero.jpg)
Figured New Years Eve is a good time to stop and reflect on how this year has been for me.

## In the Beginning
Back at the dawn of time, in January 2025, I was working in New York City at a little known company called _Google_. Maybe you've heard of them.

I also got married. That was fun. Things were going well.

### At the Googles
I wasn't happy with my work at Google. And I quite dreaded my work there. It felt meaningless and that no matter if I advocated for a better way to do things, no one cared.

## Mysterious ER Visit
I woke up in the middle of one random night in February with odd stomach pain. I got the IBS, so I figured it was just something up with a thing I ate for dinner. I went over to the bathroom to do my business and empty the ol' pipes. After a few moments I felt absolutely terrible and knew something was wrong.

I went over to my wife to ask her for help (she's a doctor). I blacked out and collapsed in our bed. My wife said I was out for only about 3 seconds. My stomach felt horrible. She ran off to the ER (living in NYC we were only a few blocks away from a hospital) and grabbed a wheelchair and she wheeled me all the way back to the ER.

I hung out in the ER for a few hours but then I started to get itchy all over my body. I started to develop hives, and I started to swell up. I was having an anaphylactic shock. The doctors hit me with an EpiPen gave me some antihistamine and something for my stomach.

They kept me around for a few hours under observation, and released me at about 7am. I went home, called in sick to work, and went to bed.

The doctor thought it was probably _exercise-induced anaphylaxis_. I did eat dinner at the GOOG, then hit the company gym to exercise the evening I had my ER visit. So that seems logical. But I've literally never had this happen before, or again. And no idea what food triggered it, as I was eating pretty boring stuff.

Though, later in the year, around August, I did also have the worse IBS flare up I've ever experienced. And it lasted for 3 months. It was a horrible nightmare and doctors basically did nothing, but at least did recommend peppermint to help relax the stomach.

My PCP wouldn't see me for 3 months and wouldn't give me a referral to the specialist until I've been seen by him. And since it took so long to see my primary doctor by that time I was feeling better. But then I had another flair up and it would take another 3 months before I could see a gastroenterologist! What if I have a colon tumor or a cyst or something? Why does it take so long to see a damn doctor! What am I even paying medical insurance for?

But man, the medical system sucks in America.

## Becoming a landlord

I bought a condo sometime ago. I have to move out for a bit so I rented it out to a friend. Then around April they had to move out after losing their job. And so, I had to actually find new renters.

And boy, what a huge pain in the ass that was. I cleaned up the place, and had to deal with old furniture my friend left behind and I hired cleaners, handyman to repair a few things, and painters to paint the place. After that I put it up on online for rent. I wasted 2 weekends showing it to people with no bites. I finally gave up and hired a agent to find me a renter and she was able to find someone in one single weekend. Moral of the story; leave it up to professionals.

## Leaving the Goog
On my birthday Google gave me the gift of severance. I made a post about [my time and leaving](../20250522-google.md). It's apparently pretty popular.

This was kind of a blessing because I really hated my time at Google.

Don't get me wrong. There are up sides to working at Google like working with some of the nicest people around that are also super smart. And the benefits are literally the industry best, even if they were starting to claw them back during my time there. (They closed a bunch of micro kitchens and reduced dinner time)

But I don't want to make this yet another Google post. So let's move on to the next problem.

## Divorce
My wonderful wife did not appreciate my post complaining about my former employer and thought I shot myself in the foot and that I'd be unhireable. She thought I'd be too much of a financial burden.

We went to counseling, and I told her that I understood her opinion, but she could not understand mine.

I didn't look at my criticism of Google as a red flag, but as a filter.

We had fundamentally different risk tolerances and views on career stability–neither wrong or right–just incompatible at that moment in our lives.

## Job hunt and pivot.

Originally, I started to interview at startups and other tech companies in NYC, but once my wife made it clear she wanted to divorce, I decided that I didn't want to swap one big tech master for another, so I decided I'd try and work for myself.

So July, I started to work on an idea I had to make a new and hopefully better RSS feed. I personally loved Google Reader and once Google killed that (before I even work there), I was disappointed at the least. There are perfectly good alternatives, (check out [Old Reader](https://www.theoldreader.com/en/)) but I wanted a centralized place for all my feeds, not just RSS.

So my original idea for a product was called Barefeed, and it was going to take open source feeds and make a single timeline in chronological order (revolutionary idea, I'm sure) in one place. Taking not just RSS, but also Mastodon and Bluesky, and if I could get away with it, Twitter and Facebook (probably not though, wall gardens don't like to share). And since it was built on RSS, it'd work with reddit and youtube that already support RSS. A one stop shop to get all your news and updates.

Anyway, while working on it, I started to write unit tests for it and then I was reminded of why I love test driven development (TDD). A friend of mine once told me, what makes it great is that tests act as living documentation. So then I thought to myself, what if we literally turned tests into human readable documentation for non-technical stakeholders?

## Test2Doc

And so I started to experiment with this idea. Could it work? Could we build documentation from tests?

First, it needs to be built from the highest level of abstraction possible. So I needed a reliable e2e testing library. I don't know if you know this. All e2e testing libraries kind of suck. But playwright did show promise and (relatively speaking) was pretty new.

I'm also a huge fan of Kent C. Dodds, and his approach to testing of [testing like your users](https://kentcdodds.com/blog/avoid-the-test-user#the-test-user).

So I needed the testing library to support:

- `.getByRole` to query the DOM similar to a user and/or screen reader.
- Taking screenshots.
- Output markdown (which Playwright does not natively do, but I could make it do so)

Anyway, I could have also gone with Cypress, but I'd never used Playwright before, and thought it'd be a good opportunity to learn it. Also, turns out that Playwright is growing faster and has over taken Cypress, but I didn't know that at the time.

So now that I picked my testing library, what should I pick for documentation?

I wanted it to be open source and support markdown. So I went with Docusaurus.

I tinkered with it and built a reporter and it showed a great deal of promise.

I also bought test2doc.com and released a marketing site to see if I could gauge interest by getting people to sign up for a newsletter. You can see the initial version [here](https://85f99ac2.test2doc.pages.dev/).

0 conversions.

It made some sense to me. The call to action is buried at the bottom of the site. You need to read the site. Who has time for that? And this is a problem that people don't even know they're having, or think there is not a solution for.

Anyway, I wasn't disheartened and on June 6, I released [v0.0.1](https://www.npmjs.com/package/@test2doc/playwright/v/0.0.1) of test2doc.

From there I'd release new versions as soon as I got a new feature working. So sometimes I'd release multiple versions a day, other times new features would take a few days to develop. But progress was fast.

Anyway, August rolled around. I filed for divorce with my wife and I moved back to Denver to live with my folks and reduce cost of living as much as possible. I'd take a small portion of my personal funds and bootstrap a startup around software testing and documentation.

So I founded Null Sweat, LLC. And you might have noticed my [ranty posts](../20250823-tech-co-op/index.md) about co-ops. And I do plan on converting to a co-op once I've been proven profitable and hired 10 employees. Currently, I'm an employee of one, and my lawyer said I can't have a co-op with one person in it. (Ridiculous, I know...)

Test2doc is solving a problem, that I've been annoyed with for years. So naturally, it'd hockey stick.

It didn't.

Turns out developers don't get testing, and QA doesn't want to write documentation.

So I figured, people just need to learn the benefits. So I started to work on a tutorial.

[Amy Dutton](https://selfteach.me/) built an amazing tutorial for RedwoodSDK that built a nontrivial webapp that is used to manage job seeking applications. It was honestly, amazing. But sadly, as the RedwoodSDK team moved from v0 to v1 they introduced a number of breaking changes that made Amy's tutorial obsolete.

I dogfooded test2doc on her tutorial. And since I am assuming people just need a guide to help learn TDD, I decided to rewrite the tutorial for the current RWSDK v1-beta. This does mean, they could introduce breaking changes at any time, and I'll need to rewrite my tutorial. But I still like RWSDK, and I think this is an amazing real world product and use case to showcase the power of TDD and test2doc.

I also figured, I'm not completely writing from scratch, so this'll go fast. Anyway, I just released [part 7 of the tutorial](https://www.test2doc.com/docs/tutorial-7) and there are still 2 more parts to write. I've been writing this tutorial for almost 3 months now. I've been working on the tutorial more than I've been working on my reporter.

While working on the tutorial, I already made 2 new packages to help with testing passkeys. 

- [playwright-passkey](https://www.npmjs.com/package/@test2doc/playwright-passkey): that helps add a passkey to chrome and helps with triggering validation that requires the passkey prompt.
- [playwright-passkey-gen](https://www.npmjs.com/package/@test2doc/playwright-passkey-gen): actually generates a passkey so you can test with it.

I launched these back in November.

So that brings us to now-ish where I'm still writing the tutorial. I'm hoping to be done in 2 weeks or so.

## What's next?

I could focus on cold out reach again to find clients to do consulting for. But it seems like such a huge time sink. I've only fired off 20 cold emails, but man it's like pulling teeth. I research who might need my services. Find out a bit about them. Tailor an email that'll hopefully catch their eye. And then hear nothing back. Not to be overly defeatist, I don't really want to do that.

My current plan is that to prove test2doc's value, I think I need to use test2doc to pass an SOC1 and 2 audit. If I can do that, I can prove the value of test2doc.

So I'm going to try and build a bank. If I can pass the audit, I've just proven that test2doc solves the hardest problem there is in documentation. If it can work for my online bank, it can work anywhere and for any industry.

Also, I think I might be able to build an open source white label banking solution. Some banking software is so janky. I'm thinking going with a Redhat business model. Open source the software and sell the support.

Anyway, stay tuned to see what 2026 brings. Wish me luck. And stay classy (or functional, I'm not here to judge you).