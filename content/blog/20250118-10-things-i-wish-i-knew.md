---
title: 10 Things I wish I knew when I started Software Engineering.
description: A listicle of some generic software engineering advice
date: 2025-01-18
tags: advice
---
Full disclosure: this is not actually good advice that'd have helped me that much early in my career. But these kind of click bait titles seem to get people to take notice.

So, I've been doing this software thing for a little while now (13 years, I guess?). So with the awesome power of hindsight, let me give you some sagely advice in one of them listicles that the Google algorithm likes to rank high on the results page. This is some relatively generic advice I've picked up over the years, but I've found it to hold pretty true.

## 1. Just look at the damn answer
So when I started to learn Javascript, I tried to use working through the coding problems in [Eloquent Javascript](https://eloquentjavascript.net/) (it was the 3rd edition at the time) but I was a complete newbie. I didn't know browser APIs (I used jQuery that abstracted all that way from me at the time), let alone I just barely knew the syntax on how to write basic JS.

Anyway, at some point in time, I gave up and just looked at the answer and I was able to learn and level up much faster.

Same thing when I started leet coding. I was able to brute force with the best of them. But actually coming up with a solution that wouldn't stack overflow on the more complex problems. Forget about it.

So to learn those more advance concepts like sliding window, making a hashmap, or whatever. These things are not intuitive and it's not easy to recognize when you need them. So just look up the answer and come back tomorrow and see if you can't implement it from memory. And come back a week later and try it again. The only way to commit something to memory is through repetition. Practice makes perfect, so you might as well get in to the habit of doing this stuff over and over again.
## 2. Time box the pain
Going back to #1, I am not a genius. If something is hard for you now. Rage quit it and try something else, or just revisit a problem later.

As a real world example, [OMA3](https://oma3.vercel.app/) for a VERY long time had a 404 problem if you tried to refresh the site on anything other than the home page. I created [this discussion](https://github.com/vercel/next.js/discussions/21235) in 2021 and found the solution for it in 2024 while trying to fix an unrelated problem. I spent a large amount of time trying to solve this issue. I knew it was some kind of configuration issue, I assumed it was a problem on the vercel side, since it worked as intended locally. And it technically was. But trying to find which thing was causing it was not a trivial matter since my set up was a bit unconventional.

Going back to leetcode, if you can't solve a problem in 30 minutes, or you quite literally have no concept what to do. Just look up the answer. Ain't nobody going to hold it against a newbie not knowing the answer.

Learning from others is quite literally one of the most powerful tools humanity has. So take advantage of it. Ask for help from those who are more experienced than yourself. Look up solutions on how other's solved programming problems. Don't try and be original and novel.

> What has been will be again, what has been done will be done again; there is nothing new under the sun.
> --Batman (Probably)

This holds pretty true for programming too.

## 3. Ask for help
You need to struggle a bit on your own. At least do your due diligence and see if you can't find a solution from documentation or other resources. But at the same time, looking for a solution can be a endless rabbit hole that you think you're almost at the solution, a kind of gambler's fallacy.

So go back to #2, time box the pain. If you've wasted more then 2 hours on a problem, you're probably not finding the solution in the 3rd or 4th hour. So you might as well ask for help. If you're using asynchronous communication, fire off a message and go back to researching a solution while you wait for your colleague/mentor/maintainer/hivemind to get back to you.

Also, try to document a solution in a way that it can be found by others. You might be unwittingly helping future other people with the same problem. So other forums, like stackoverflow, github discussions/issues, or reddit is preferred something closed wall gardens like discord or slack. It is better to embarrass yourself in public to help a future stranger than it is to silo knowledge.

Death to the wall gardens! Long live the open (and indexable) open web!
## 4. Don't copy and paste
You find a solution, or following a tutorial. Don't copy and paste a solution. Type it out. Force yourself to build up the muscle memory and also forces you to _read_ the code (and hopefully understand it). It's slower and more annoying. But when learning you're not in a race to the end. It's a marathon of repetition to incorporate it in to the ol' grey matter.
## 5. Learn how to write tests first
Test driven development is the concept of writing a test before you write the implementation.

In theory you should already know what you need to happen. So you should be able to write a test that looks for what you expect to happen.

In reality, there is a somewhat nightmarish amount of complexity and things that can go wrong. But if you can learn the basics of how to write what you are expecting to happen first, then write the implementation you'll be able to take a lot of mental load off your mind. Also tests act as living documentation for a project. Assuming you have a CI/CD pipeline, it should run tests before deploying and notify you if a tests breaks (and also not deploy). If you need to onboard someone you can just tell them to look at the tests to figure out what the software does. It's a win/win situation.

Unless tests are flaky...that's a kind of special hell. Usually it's because you wrote the test wrong, and learning how to write tests right is sometimes a real pain in the ass. But it's still worth it for the long term benefits of testing.

Maybe I'll write another blog post going over my philosophy of testing and some examples.
## 6. Make a cool hobby app
Work, or at least my work, is often boring and not creative. It's not like it's not interesting, because in someways it is else I'd have a real hard time getting out of bed to make websites for people. But where I feel like I can really solve real interesting problems is in hobby apps. I also get to experiment with new technologies, try new programming patterns, play with new frameworks and libraries, experiment with best practices, and throw caution to the wind.

I've build and rebuild an app to create Shadowrun characters for basically my entire career. One of the [first version](https://github.com/HeyOmae/Omae) I did, back at the dawn of time, was make a character generator using jQuery. The [second one](https://github.com/dethstrobe/omae2), I attempted to build it with angularjs. The [actual second attempt (v2.1)](https://github.com/HeyOmae/Omae2.1) was built using React and Redux. And the [newest one](https://github.com/HeyOmae/OMA3) is built using NextJS.

Each time I take what I've learned and I try to experiment to try new things to learn more. Anyway, think of a problem and make an app to solve it. It's a great way to learn and do cool stuff.
## 7. Hard problems are just a lot of small problems
I am a huge advocate for Agile software development. A lot of people follow scrum methodology and do the scrum ceremonies. But that's not necessarily what makes agile processes work.

The point of agile methodologies is to break big problems into small problems and ship it and get feedback if you're even building the right thing. And if it looks good, then you [kaizen](https://en.wikipedia.org/wiki/Kaizen)!

Predicting the future is hard. So don't. Instead try and make small incremental changes that will hopefully get you where you want to go. But if you're wrong, you can pivot and hopefully not waste a lot of effort to make something worthwhile.
## 8. Software is made of softness
Don't over think a solution. Just get something working. If you get it wrong, guess what, you can change it and make it better later. Software is super easy to make changes. Because if it wasn't, we'd call it hardware engineering.

This also gets to another point, if it is hard to change something in software, refactor it to make it easier. It is definitely an art to make modular software, but try to keep it in mind and you'll make your life easier.

If you make your software modular you also make software easier to be discarded. Your code is trash, you just don't know it yet because you haven't learned a better way to do it. You're not at the pinnacle of your skill set, so you can always write better code. So try and make it easier on future you to be able to refactor, discard, or just swap out your current code.
## 9. Find a new job every 2 years
Jump ship early and often. Aim for a 20 to 30% raise every 2 years until you hit the market cap of your city, than move to a bigger city.

Being exposed to more technology, frameworks, programming patterns, learning new ways to work, learning from others, even teaching others. There are so many benefits to jumping ship and you hurt your own personal growth and hold back your salary by staying at your current company.
## 10. Communication is key. Talk to people early and often.
Get feedback early and often, and give feedback early and often.

Try to have quick and regular talks. I'm personally a huge fan of adhoc conversations, but as I have learned at a larger companies sometimes you just need to set up meetings. Meetings are evil by the way and should be avoided at all cost. But...if it's the only way to get to talk to some people, then you got to do what you got to do, and make a meeting and add it to people's calendar that you need to talk with.