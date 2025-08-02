---
title: Standard Work
---

I aimed to standardize the work for these reasons
1. Create a value stream map through the organic evolution of the documentation.
2. Use as a baseline for Kaizens.
3. Stabilize the system of work by reducing the overburden through the adoption of standards.

Standardising the work was an informal way of developing a Value Stream Map. 
I tried to gradually understand the whole system of work through informal conversations. 
First we documented the current conditions, then we improved upon it.
Then if someone else wanted to try an improvement, they had to check if they were working according to the standard.
If they weren't they first had to change to the standard because typically that standard would have already been a better practice.
What I didn't do is blindly document everything or try to map everything because what people say is the process and what actually is often turn out to be two different things.

In addition to organically developing the VSM, another use for standardising the work was to compare improvements. 
The documentation also had to have enough information to compare improvements.
Each time someone wanted to change something, they needed to make a hypotheses that compared their idea to the standard. 
Without a standard, it would be like running a test without a baseline which they understood.

Though there were standards, they were very loosely followed or there was almost a different way of working for each tester. 
I think this happened because everyone just got so busy that there wasn't enough time for coaching or peer-reviews etc.
One challenge in getting folks to adopt a standard that requires so much details is fear.  
I think folks kept the test cases light on details to protect their job-security.  
That is, if nobody can read their work, then nobody can replace them.  
By showing the team that the test cases written in the DSL can be automatically converted into automation, I feel it helped reduce the resistance because they learnt new skills.
With the exception of the COBOL testers most of the testers didn't write test cases in a way that another tester could understand and execute their tests.  
In the COBOL testing team, if someone finished their work for the release earlier, they could help others who were falling behind.
Understanding the tests would make it easier for the testers to practice pairing, teaming, mobbing or swarming and therefore reduce the overburden.

# Operational Definitions

How much did we document, like to what level of detail?
There was enough detail such that individuals could follow the improvement journey of their peers at their own pace with minimal (not none) guidance. 
They also had to be short enough that one could make the change to their way of working whenever they had down time for an hour or so.
An example is a simple checklist of 10 steps to installing Eclipse. 

More recently I learnt about [operational definitions](https://deming.org/data-is-important-and-you-must-confirm-what-the-data-actually-says/) and their impact on variation. 
The analogy that was given to me was if you tell someone to test something which requires measuring, whether you use a micrometer or caliper will produce different results.
Reflecting on that I'd say one goal of the documentation was to prevent problems and therefore reduce variation in our processes.
So we started with light documentation and then only updated it when we found another source of variation could be prevented.

These are some examples
1. Install Eclipse. In the beginning, that was the step, but in the end, we had to specify the version and package type as well. If we didn't specify either then, later when someone needed to use an EMF feature, they'd try and install the plug-ins but often get them wrong so we specified the package. Similar for the version, there were little issues folks would run into and then work around it, which would create overburden. To me these things were perceived as special cause variation, but really there was a common cause for all the incompatibility issues we ran into. Because we hadn't defined the step of setting up the testers laptop, it actually got in the way of us properly measuring the impact of code generation on test execution.
2. Test it. How two testers interpreted a test step and therefore passed or failed a test also varied around coverage and retesting. Because of time constraints mainly, they didn't test beyond the original failing test when a bug was fixed or either they had breadth but not depth of coverage or vice versa. By specifying that they use the [ubiquitous language](/demingdriventesting/about) to write a test automated test execution could be leveraged earlier and more frequently. Also the DSL ensured we'd work towards a graph model and model based testing which would slowly allow us to choose graph traversal algorithms to select tests coverage.
3. Mock it. If you just mock someone else's code, then you might discover you're not on the same page as them when you do integration tests. 
Better is to have them make the mock and give it to you as a promise of functionality.
Even that might not be good enough if they don't test against the mock to make sure they'e keeping that promise.
So instead of telling someone to mock something, I think I'd say, use a mock made by the service provider which they test as part of their build process.
Here, the impact of not specifying how to mock resulted in data that would indicate that earlier testing yields little to no improvement because you still wind up with integration testing issues.


