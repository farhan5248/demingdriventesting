---
layout: page
title:  About
permalink: /about/
---

# Why Deming Driven Testing

I came across the term Deming Driven Testing from [Mike Harris](https://testandanalysis.home.blog/) which I like very much because it describes the approach I took accurately.

So why Deming and not Lean?

As I was searching for information on how to transform QA teams, a new buzzword emerged; Shift Left.
I researched where that term came from and came across Dr Deming's work and the [quote on scraping toast](https://deming.org/you-burn-ill-scrape/).
I also learnt about his 14 points and the need to cease dependency on inspection and the System of Profound knowledge.
The latter included the psychology of change which I found was essential in trying to solve what are socio-technical problems.
I like to take a first principles approach and so I concluded that what Dr Deming described made for a good foundation. 

I should note that when it came to how to apply anything to do with psychology I had no idea of what to do at the time.
For that I relied on [Start with Why](https://simonsinek.com/books/start-with-why/) by Simon Sinek.
The approach he described in [this presentation](https://www.youtube.com/watch?v=N9d0NqSztWA&t=188s) is basically how I moved the team forward. 

# The direction of challenge

Keeping the improvement kata in mind, the direction of challenge is to gradually provide feedback earlier by having the QA tests run earlier.
To make it concrete, the QA testers needed to write their test cases in the ubiquitous language described in DDD by Eric Evans using an IDE.

This link to [Martin Fowler's bliki entry on Ubiquitous Language](https://martinfowler.com/bliki/UbiquitousLanguage.html) describes the concept of Ubiquitous Language as a language that is used by both domain experts and developers. 
In my case, I considered the testers as the domain experts as did the developers. 
[In his conversation with Eric Evans, at around minute 5](https://youtube.com/clip/UgkxwDpbV3Wzrdz0mNow9cglz9_KJuxLmj25?si=6Sx67uKN7UoKukVM), Dave Farley explains how he uses the ubiquitous language to write tests. 
This is what my QA team did and what I've done to create the test code for the supporting code. 

Regardless of whether the test was intended to be automated or not in the current process, everything was written in that language.
I won't go into the details of how we arrived at the conclusion that it was the goal over 3 years here, that's covered in the stories.
I will say that I started out with the intention to adopt a keyword driven test automation approach but that had its own issues, namely it devolving into a programming language.

Why the Ubiquitous language, why not just teach them to write the Java/Python code?
Teaching that many people to code would be more challenging (details explained in the stories) but think of the ski slope analogy in Sooner Safer Happier about taking everyone to the top of the hill.
Instead, refining a language they already used to communicate with the BSA and developers required less tweaking to how they work.

Why use an IDE? Why not Jira, Word, Google Docs, Excel, Confluence? 
In fact at first they were using Microsoft Word and Excel and then those files were parsed and converted to automation it was like coding with Microsoft Notepad and finding your errors at compile time instead of as you were typing.
In addition to the usual benefits of using a language editor in an IDE the [Xtext framework](https://eclipse.dev/Xtext/) gave us an API to query all the test cases written by everyone in my team.

To be clear this is like the [Java Parser API](https://javaparser.org/) I use to generate Java code automatically.
Through this API, you could extract whichever data you wanted to transform it into whatever you wanted from all of the tests written by all of the testers in the entire team for every component they tested.
It also ensured that the language used to describe the business domain was mapped to the system that was being tested.

# The approach

I applied the following to the process of inspection carried out by the QA team:

1. Toyota Production System concepts (Jidoka, Kaizen, Poka-Yoke)
2. Dr Deming's System of Profound Knowledge
3. Improvement Kata by Mike Rother
4. Lean Software Development by Tom and Mary Poppendieck

At first the process of inspecting for defects became more efficient. 
The testers were generating test automation and running it progressively earlier.
That is, first the automated tests were made by a test automation developer and run at the end of the first manual cycle of testing but later it was the manual testers generating the automation and running it themselves during that cycle.

Eventually in the case of one team, the testers were running their automated tests alongside developers in lower environments so that quality was built-in. 
The result was that almost all of that QA team's end-to-end tests were run as component tests before the code was delivered to the QA environment and was virtually defect-free.

I should add that the integration process was weak and we wound up implementing the [Test Hourglass anti-pattern](https://testing.googleblog.com/2020/11/fixing-test-hourglass.html) but at least the last phase was done in a week or so, down from months

If you're wondering which tools were used by the testers, they were:

1. Eclipse
2. Eclipse Modelling Framework (UML)
3. Eclipse Xtext
4. Java Universal Graph Library
5. PlantUML
6. D3.js
7. GraphWalker
8. Cucumber
9. Java
10. SoapUI
11. Groovy
12. Robot Framework
13. Python
14. PyCharm
15. Jenkins
16. Maven
