---
layout: page
title:  About
permalink: /about/
---

# Why Deming Driven Testing

I came across the term Deming Driven Testing from [Mike Harris](https://testandanalysis.home.blog/) which I like very much because it describes the approach I took accurately.

So why Deming and not Lean?

As I was searching for information on how to transform QA teams in 2018, a new buzzword emerged; Shift Left.
I researched where that term came from and came across Dr Deming's work and the [quote on scraping toast](https://deming.org/you-burn-ill-scrape/).
I also learnt about his 14 points and the need to cease dependency on inspection and the System of Profound knowledge.
The latter included the psychology of change which I found was essential in trying to solve what are socio-technical problems.
I like to take a first principles approach and so I concluded that what Dr Deming described made for a good foundation. 

Additionally Lean sadly seems to be misunderstood.
I was concerned that if people on my team went Googling what Lean is, they'd get information that would discourage them from trying it out.
Some folks think Lean six-sigma is the same as Lean which is the same as TPS.
I admit that I think the latter two are the same and know nothing about the six-sigma one (I've so far found no use for it).
From the podcasts I listen to I hear consultants say the same thing; folks think it doesn't apply because they don't make anything (my QA team didn't make software), or they don't make cars or they don't make the same thing over and over again.
My response is that lean is about the process. Even if you don't make cars, the same car or make anything at all, your process is not changing everytime you do the job. 
And so this aligns nicely with Statistical Process Control and the emphasis on process quality and inspecting products to find defects in the process rather than inspecting the product to ensure quality.

I should note that when it came to how to apply anything to do with psychology I had no idea of what to do at the time and found very little help from the software development world.
For that I relied on [Start with Why](https://simonsinek.com/books/start-with-why/) by Simon Sinek.

# The Approach

I applied the following to the process of inspection carried out by the QA team:

1. Toyota Production System concepts (Jidoka, Kaizen, Poka-Yoke)
2. Dr Deming's System of Profound Knowledge
3. Improvement Kata by Mike Rother
4. Lean Software Development by Tom and Mary Poppendieck

Keeping the improvement kata in mind, the direction of challenge is to gradually provide feedback earlier by having the QA tests run earlier reducing the need for mass inspection.
To make it concrete, the QA testers needed to write their test cases in the ubiquitous language described in DDD by Eric Evans using an IDE.

At first the process of inspecting for defects became more efficient. 
The testers were generating test automation and running it progressively earlier.
Eventually in the case of one team, the testers were running their automated tests alongside developers in lower environments so that quality was built-in. 
The result was that almost all of that QA team's end-to-end tests were run as business component tests before the code was delivered to the QA environment and was virtually defect-free.

I should add that the integration process was weak and we wound up implementing the [Test Hourglass anti-pattern](https://testing.googleblog.com/2020/11/fixing-test-hourglass.html) but at least the last phase was done in a week or so, down from months