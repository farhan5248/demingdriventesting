---
title: Standardized Work
---

Before changing anything by making it faster or eliminating it, we needed a standard. 
Standardising the work was an informal way of developing a Value Stream Map. 
I tried to gradually understand the whole system of work through informal conversations. 
Though there were standards, they were very loosely followed or there was almost a different way of working for each tester. 
I think this happened because everyone just got so busy that there wasn't enough time for coaching or peer-reviews etc.

As we made kaizens, we documented them as they became part of the new standard. 
First we documented the current conditions, then we improved upon it.
Then if someone else wanted to try the new improvement, they had to check if they were working according to the standard.
If they weren't they first had to change to the standard because typically that standard would have already been a better practice.
What I didn't do is blindly document everything or try to map everything.
Instead the documentation developed organically as we improved.

How much did we document, like to what level of detail?
There was enough detail such that individuals could follow the improvement journey of their peers at their own pace with minimal (not none) guidance. 
They also had to be short enough that one could make the change to their way of working whenever they had down time for an hour or so.
An example is a simple checklist of 10 steps to installing Eclipse. 
In addition to organically developing the VSM, another use for standardising the work was to compare improvements. 
The documentation also had to have enough information to compare improvements.
Each time someone wanted to change something, they needed to make a hypotheses that compared their idea to the standard. 
Without a standard, it would be like running a test without a baseline which they understood.

One standard that already existed was around how the COBOL testers wrote their test cases.
The idea was that if someone finished their work for the release earlier, they could help others who were falling behind.
This was made possible by having tests cases so clear and so void of assumed knowledge that code generation from it was trivial.
I gradually steered the rest of the team to adopt such a standard and that's how we got the grammar for the ubiquitous language.

# The Ubiquitous Language

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

> **Note:**  
> Most of the testers didn't write test cases in a way that another tester could understand and execute their tests.  
> One challenge in getting folks to adopt a standard that requires so much details is fear.  
> I think folks kept the test cases light on details to protect their job-security.  
> That is, if nobody can read their work, then nobody can replace them.  
> By showing the team that the test cases written in the DSL can be automatically converted into automation, I feel it helped reduce the resistance.  
> Even if they would lose their job as a result of sharing knowledge, at least they would learn Robot Framework with Python.
