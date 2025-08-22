---
layout: page
title:  About
permalink: /about
---

# Why Deming Driven Testing

I came across the term Deming Driven Testing from [Mike Harris][11] which I like very much because it describes the approach I took accurately.

So why Deming and not Lean?

As I was searching for information on how to transform QA teams in 2018, a new buzzword emerged; Shift Left.
I researched where that term came from and came across Dr Deming's work and the [quote on scraping toast][12].
I also learnt about his 14 points and the need to cease dependency on inspection and the System of Profound knowledge.
The latter included the psychology of change which I found was essential in trying to solve what are socio-technical problems.
I like to take a first principles approach and so I concluded that what Dr Deming described made for a good foundation. 

Additionally as it is with other concepts, there seems to be multiple definitions on what it is.
I was concerned that if people on my team went Googling what Lean is, they'd get information that would discourage them from trying it out.
Some folks think Lean six-sigma is the same as Lean which is the same as TPS.
I admit that I think the latter two are the same and know nothing about the six-sigma one (I've so far found no use for it).
From the podcasts I listen to I hear consultants say similar things; folks think it doesn't apply because they don't make anything (my QA team didn't make software), or they don't make cars or they don't make the same thing over and over again.
My response is that lean is about the process. Even if you don't make cars, the same car or make anything at all, your process is not changing everytime you do the job. 
And so this aligns nicely with Statistical Process Control and the emphasis on process quality and inspecting products to find defects in the process rather than inspecting the product to ensure quality.

I should note that when it came to how to apply anything to do with psychology I had no idea of what to do at the time and found very little help from the software development world.
For that I relied on [Start with Why][10] by Simon Sinek.

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
The result was that almost all of that QA team's end-to-end tests were run as business component tests before the code was delivered to the QA environment.

# The Ubiquitous language

I've tried to document not just the process of transforming the team but the use of a specific concept; the ubiquitous language from Domain Driven Design.
This link to [Martin Fowler's bliki entry on ubiquitous language][4] describes the concept of ubiquitous language as a language that is used by both domain experts and developers. 
In my case, I considered the testers as the domain experts as did the developers. 
[In his conversation with Eric Evans, at around minute 5][5], Dave Farley explains how he uses the ubiquitous language to write tests. 
This is what my QA team did and what I've done to create the test code for the supporting code. 
The implementation of the ubiquitous language was a natural language DSL, and specifically an external one. 
The code generated was an internal DSL just to make it easier to map from that platform specific implementation back to the business scenario.

Regardless of whether the test was intended to be automated or not in the current process, everything was written in that natural language DSL. 
This way, we could decide later which to automate with minimal back and forth. 
If it wasn't going to be automated, was it a waste to put in extra detail just to run it manually?
No, because other non-SME could help execute the tests if we couldn't automate it to help reduce the toil or [overburden/muri][1] on a tester.
I will say that I started out with the intention to adopt a keyword driven test automation approach but that had its own issues, namely it devolving into a programming language.

Why a natural language, why not just teach them to write in a programming language?
Teaching that many people to code would be more challenging (details explained in the stories) but think of the ski slope analogy in Sooner Safer Happier about taking everyone to the top of the hill.
Instead, refining a language they already used to communicate with the BSA and developers [reused skills they already had][2] requiring less tweaking to how they work.
The one constraint that I added on their language was to do with [finite state machines as described by Bob Martin][6].
This was so that we could easily adopt model based testing and reap its benefits.
Also most tests were system or end-to-end tests covering multiple technologies (Java, GGS, COBOL, PLSQL, webMethods etc).
Which language should my entire team write it in?

Why use an IDE? If it's not code, why not Jira, Word, Google Docs, Excel, Confluence? 
In fact at first they were using Microsoft Word and Excel and then those files were parsed and converted to automation.
It was like coding with Microsoft Notepad and finding your errors at compile time instead of as you were typing.
When the team learned about jidoka and poka-yoke, we moved to Xtext which provides full Eclipse IDE support.
Being able to look up other scenarios or browse through all the steps one could take from a page like you would browse methods in a class through code completions or content assist helped.
You can read more about [language workbenches on Martin Fowler's site][7]

In addition to the usual benefits of using a language editor in an IDE the [Xtext framework][8] gave us an API to query all the test cases written by everyone in my team.
To be clear this is like the [Java Parser API][9] I use to generate Java code automatically.
Through this API, you could extract whichever data you wanted to transform it into whatever you wanted from all of the tests written by all of the testers in the entire team for every component they tested.
It also ensured that the language used to describe the business domain was mapped to the system that was being tested.

Finally, though I didn't think of it at the time, you can use specs written in this language as prompts to practice [specification by prompt][3] with Claude Code and have it write the bulk of the code.

[1]: /demingdriventesting/Migrating%20from%20defect%20inspection%20to%20prevention/Muri
[2]: /demingdriventesting/Communicating%20the%20strategy%20to%20QA/The%20Neo%20Nurture%20Incubator
[3]: /specificationbyprompt/index
[4]: https://martinfowler.com/bliki/UbiquitousLanguage.html
[5]: https://youtube.com/clip/UgkxwDpbV3Wzrdz0mNow9cglz9_KJuxLmj25?si=6Sx67uKN7UoKukVM
[6]: https://blog.cleancoder.com/uncle-bob/2018/06/06/PickledState.html
[7]: https://martinfowler.com/articles/languageWorkbench.html
[8]: https://eclipse.dev/Xtext/
[9]: https://javaparser.org/
[10]: https://simonsinek.com/books/start-with-why/
[11]: https://testandanalysis.home.blog/
[12]: https://deming.org/you-burn-ill-scrape/