
**Title: Fake It 'Til You Make It: Mocking Reality So Your Tests Can Run**

Audience: R/Python data scientists who now write tests because they've drifted into building packages and tools. They know what a unit test is. Most have never intentionally mocked anything, and some think testing in isolation is cheating and/or excessive.

One big idea: Mocking is lying to your code, on purpose, to control the ecosystem it lives in. It matters because the code that touches that ecosystem is usually the riskiest and the least tested.

---

Hook/Intro
I want to tell everyone about how lying made me a better developer. This happened when I was working on code I couldn't test. I was building a feature for Posit’s Python package Pointblank, everything was going great, and then I needed to test console messages that only appear depending on whether a package is installed on a user’s computer. Something I had no control over or could possibly know as a developer. At first, I did what most of us do…ignored it and didn’t test it. I'm betting most people in the room have dealt with something similar, where you see something and you’re like… “nah, no thank you”. Thankfully working with posit supergeniuses, was able to see an example of mocking in it’s simplest form.

Context/setup
Lying to your tests is good, actually. This is where I state the big idea and take the misconceptions head-on,  that mocking is cheating, that it's too much overhead, or that it's a niche trick that’s overhyped. I found out the hard way it's not a “Python” thing or an “R” thing; it's a fundamental idea about control in software/engineering 101.

Ch 1. - Why lie?
Here, we’ll talk about things in the wild that most of us see or deal with in our day-to-day work usually like APIs, databases, time (-.-), randomness, environment variables, file systems, cloud services, the list could go on but we’ll cull it. The main point here is that these are the exact “everyday” places our code is most likely to break and least likely to be tested fully to completion (This “completion” refers to the percentage of test code coverage a software has, not a niche concept for those doing this work).

Ch 2. - How to lie
The only section with code, walked through statically with no live demos. R and Python examples alternating? (Not sure if it matters or if one example could be R and another Python)... I'm using interactivity to highlight lines step by step against two questions:

1. what's the thing we need to lie about? And
2. where do we need to lie about it?

The goal is for people to see the pattern thematically, not to memorize (thinking a qr code to example scripts/repository should be used for those that want it)

Ch 3. - When you shouldn't lie

Overmocking and the overhead it buys you. Although mocking is simple, it can be as complex as your brain will allow you to make it.

The rule I want people to leave with: lie about the world your code lives in, never about the thing you're testing.

Still am thinking through a good example for this one, but whatever example it is, it'll show a scenario where mocking really… really wasn't needed lol.

May make the point that mocking isn't always the answer because sometimes there's a lighter-weight way to control the world your code runs in, instead.

The withr package in R is an example that could be used (withr borrows from the idea of mocking, but isn't exactly mocking. It lets you temporarily control the environment your code runs in things like environment variables and options and then puts everything back when the test is done.) - If i do mention, it would be quick, want to see where I am on time when I start getting this together.

Close/CTA
The mental model shift: "So instead of losing sleep over how to make your tests reach the real world, just ask yourself what part of the real world you should fake." Next time they meet an API, a timestamp, or a random seed, the question changes from how do I make my test hit production? to what should I fake?

**
