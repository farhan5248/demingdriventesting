---
title: Geordi La Forge
---

# Code Generation Adoption

When I decided to go to the QA team it's not just because of the lead time problem. 
There was another reason, code generation. 
As I mentioned, we had to rewrite the system and it was going to take a long time.
So I thought of generating the code automatically from UML models.
I'd automatically convert the webMethods flow language into a model and then forward engineer it into Java.
The flow language was quite simple so this was easy to do. 

The challenge was convincing other developers to work with code-generation instead of manually translating all the code. 
When I told the developers I could generate code 7 or 15 years ago, they'd resist and say it's not possible and it's better to do it all manually. 
I think this is because of scarcity mindset; I was taking something away from them.
They think that that's how they make their living, and if they can't create code, then they're out of a job because there's no other work.
However if I go to the QA team who don't code, and I tell them I can automate code creation, they were more receptive to it.
That's because they're not losing anything, they're actually gaining something; test automation. 

# Deterministic vs Non-Deterministic Approaches

For 15 years, ever since I graduated from university, I've been trying to automate the creation of code. 
It's been through uml and graph models and templates, including Excel.
I've realized that for some things like test automation or very thin layers of code like docker or AWS configuration, you can use traditional deterministic approaches. 
For the main code itself, tor practical reasons, I couldn't. 
1. It's hard to come up with all the patterns. You would almost need a program that recognizes patterns and then can dynamically figure out what needs to be replaced just by teaching it aA few patterns, which is basically what AI does nowadays. At the time it seemed impossible and even if I were to make a little program to do that, the amount of time it would outweigh any benefits. 
2. Even if I used tools like UML code generators, the feedback came too late.
You can't exactly debug a uml model, so you're constantly having this irritatingly long delay between changing something and getting feedback. 
As a TDD practitioner, I couldn't see the value in waiting that long for feedback. 
I concluded that the only useful UML model is an auto-generated one derived from text files like code or DSL.

It's desirable to reduce variation in any process and so the more deterministic the better but there are challenges with doing that past a certain point.
Now we have AI, which is a pattern recognition tool that I can actually run in my IDE to create the main code.
What I'm experimenting with is how to give small enough test specifications to drive the development of a coding agent. This involves
1. Dividing up the problem into small steps by using very small tests, think edges in a graph model.
2. Using traditional code generation to ensure I have test automation that I know works.
3. Running really small models that understand Java code well enough to use previous combinations of test scenarios and git commits of code changes which passed the tests to guide it.

# I Never Saw Geordi La Forge Write Code

Why have I been looking at code generation for 15 years? 
Well, I grew up watching Star Trek and Geordi used to solve engineering problems. 
I never saw him sitting there coding for hours and days.
For me, programming is a means to an end.
If I can remove coding from the process so I have more time to do think deeply about the problem or getting faster feedback, then I'm all for it.

Do I think automating the coding away will kill jobs? No, because there's tonnes of legacy software and technical debt that needs to be addressed.
Those are problems that I don't think an AI can solve and are the ones I think people should work on.

# Do you need the QA team?

Before 2022, I would have said no because the tester is already creating the test data. 
There's no resistance to trying out the code generation in a QA team.
So getting it to work there first before applying it to a dev team would be the path of least resistance.
If you're in a dev team though, trying to get a whole other team (QA in this case) to cooperate is challenging as I had experienced. 

Nowadays if you invest a little bit of time converting the QA teams's tests yourself, combined with code generation techniques, I think you can actually save quite a bit of time.
It might even render the need for inspection at the end useless and help convince the QA team to change such that acceptance tests are the [new programming language][1]

[1]: https://medium.com/@gergelygrcs/specification-as-a-prompt-how-ai-is-turning-specifications-more-important-than-code-0137366ae211