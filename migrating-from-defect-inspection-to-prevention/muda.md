---
title: Muda - Waste
---
<a href="https://learning.oreilly.com/library/view/implementing-lean-software/0321437381/" target="_blank">
    <img src="{{ site.baseurl }}/assets/images/implementinglean.jpeg" alt="Implementing Lean Software Development" title="Implementing Lean Software Development" style="display: block;" />
</a>

When I joined the QA team, I had introduced the term shift left. By the time I left the team, I grew to hate the mere mention of it :P. 
My dislike came from all the misinterpretations of it. 
At the time I traced it all the way back to Dr Deming and it's how I came across his work.
Specifically it was the quote about burning and scraping toast.

Given the circumstances of why I joined the QA team, I assumed testers would be defensive and claim their work couldn't be automated.
I had taken care to communicate in advance of speaking to them individually that it's not individual efficiency but team efficiency that we're trying to improve. 
I used a Netflix documentary on coaches to help with this, the coach said he coaches teams, not individual players.
I wanted to communicate to my QA team why we had to focus on optimizing globally and not locally and the importance of quality being built-in since it can't be inspected in. 
That is, I wanted them to understand how their test data injected earlier in the process makes the developers lives easier and that the cost of delayed feedback such as test automation isn't as effective and creates waste.

Initially, the global system was the QA team only and later I included a dev team.
I did this because motivating them to make their lives harder for another team's life to be easier might have been a harder sell.
To do so I first showed them how the very process of QA could be improved. 

This is the list of wastes from the point of view of my QA team:
1. Transport: Manual tester to test automation developer.
2. Inventory: Unexecuted tests or unvalidated automation tests.
3. Waiting: Waiting for test automation to be created or run, waiting for devs to fix bugs.
4. Motion: Unnecessary clicking like with doc to dnp which I wrapped with maven.
5. Overproduction: Unnecessary test cases to meet a metric of x test cases for y days of coding.
6. Overprocessing: Unnecessary steps in the test case or over complicated test setups or doing e2e testing when a unit test is good enough.
7. Defects: Test case writing defects. The system was complex and difficult to understand in its entirety.
8. Skills: Testers who were able to learn to code but whose time was wasted doing manual testing.

The more waste was reduced, the more free time people had to try new things or help others.
This meant more kaizens and even more capacity for an individual or capacity for the team.

As an example, I showed them how time and effort is wasted between the manual tester and test automator when making Selenium tests.
Then I demonstrated how that waste can be reduced and eventually prevented by working in small batches through Jidoka and Poka-Yoke using an IDE or Maven.
First came Jidoka, the custom Maven plug-in worked as a sort of automated test suite that would validate their work similar to how their test cases in turn would validate the developers work. 
The more frequently they ran the plug-in, the earlier they would catch their mistakes and save more time and therefore reduce wasted efforts.
Then came Poka-Yoke by introducing preventative approaches through Xtext. They started to see the value of tests driving the development.
Instead of typing and then checking for mistakes, the IDE would give them feedback as they typed and that prevented the need to run a program to test for issues in the work.

