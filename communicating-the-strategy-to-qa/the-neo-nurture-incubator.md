---
title: The Neo Nurture Incubator
---

<a href="https://www.designthatmatters.org/past-projects" target="_blank">
  <img src="{{ site.baseurl }}/assets/images/neonurture.jpg" alt="NeoNurture" title="NeoNurture" style="width:50%; display: block;" />
</a>

Grasp the current condition. I had to start with the skills people already had and come up with creative ways to build on that. 
The state of things was such that nobody had time to learn any other skills. 

I took inspiration from the [NeoNurture Incubator][1]. Long story short, when it broke down, nobody could fix it because they didn't have the skills. 
So the designers made an incubator that looked it was made out of car parts. 
Why? Because the folks in that country were very good at fixing their cars and keeping them running for years. 
After the design change, anytime the part that looked like a headlight broke, they could walk out onto the street and ask someone to come in and fix it. 
Basically they made the problem look like another problem which folks knew how to solve.

The COBOL testing team had a Java SWING program (somebatchtool.jar) that converted Microsoft Word documents into text files. 
These text files were either CPHA3 claim requests or upload files with data about new certificate holders and drugs etc. 
Instead of trying to get folks to use Cucumber and teach them about Gherkin and stories etc, I worked with Word and somebatchtool.jar. 
I asked them what problems they ran into and kept fixing those by wrapping the entire process within a custom Maven plug-in.
Then I showed this way of working to the non-COBOL testers and defined it as the standard that we'd work towards.
This was almost like keyword driven testing but closer to the [Ubiquitous language in Domain Driven Design][2].

The other testing team, a UAT team also tried to adopt Robot Framework for their testers but failed.
The path they took was to get a capable technical resource to automate the tests and make a library of keywords that could be used.
The problem was that the testers didn't recognise those keywords, they were like functions in a program.
It would be like asking a tester to write their tests in another language, like Latin.

Another smaller testing team did a demo, the lady presenting was a master of all her tools, my team was impressed.
The tester there I believe learnt everything herself and used those tools to make her life easier.
Her tests were run by the developers too.
Like my team, she defined the language, not someone else.

## Understanding Test Types Through Team History

An interesting question arose during the transformation: were the tests my team wrote unit tests or acceptance tests? 

The approach was originally developed by the system's developers before there ever was a QA team. When the first QA analyst was hired more than a decade ago, she simply continued their methodology. My team inherited this same approach another decade later.

So are these unit tests because developers created the process, or acceptance tests because the QA team executes them? According to [Ian Cooper's presentation on TDD][3], they're unit tests - tests that verify a unit of behavior rather than a unit of code structure.

This historical perspective reinforces the neo-nurture approach: rather than forcing teams to abandon working practices, we built on the solid foundation that had evolved organically over decades. The QA team was already writing behavioral specifications in clear language - we just needed to enhance the tooling and process around it.

[1]: https://www.youtube.com/watch?v=0af00UcTO-c
[2]: /specificationbyprompt/walkthrough-of-tools/ubiquitous-language
[3]: https://www.youtube.com/watch?v=EZ05e7EMOLM