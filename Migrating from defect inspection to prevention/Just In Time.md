---
title: Just in Time - Pull Systems
---

My entire QA team worked in a waterfall project, all the code was written before any tests were executed. 
In some cases, you'd have 3 months of test case planning followed by 3 months of test case execution.
When I felt we had made it easy enough for developers to run the QA tests earlier, I explained what just-in-time manufacturing was and the waste of inventory. 
It was now time to work with our upstream parts suppliers, AKA the COBOL dev team but the roles would be reversed.

When the requirements document was ready, the developers would do their initial analysis while my testers created some key test cases as they'd call it. 
Then with this lead of a few days of tests for developers to run, they'd replenish one bin per day. 
Developers then could keep doing a fetch and only merge with the next git commit and work on those tests. 
I think some developers just did a pull but that was ok since there would only be 1 git commit added each day. 
Why did I care about this? Well, what I didn't want to have is failing tests all the time. 
I was aiming for Continuous Delivery and Trunk Based development. 
I wanted the developer and tester to learn to synchronise (reduce variation/fluctuation). 

Our goals was to not have huge inventories of:
1. Test cases that weren't executed yet. The COBOL testers needed hundreds of new test cases for each feature, all with their own head hurting math equations. 
Just as we don't have to have long lived branches with tonnes of git commits, I didn't want the testers making huge inventories of tests.
The bigger the inventory of tests, the higher the probability they would need to be re-worked or skipped altogether. 
I used to see the test execution phase as the test re-planning phase as testers went through re-doing all the math, it was just a waste of time.
2. Executed test cases and their code not deployed to production just waiting in QA. 
The obvious problem with this situation was when the dreaded high severity high impact bug that puts the whole release on hold. 
The idea was that if we sign-off on something, we should be able to promote it.

To avoid this we'd work towards the following:
1. Only write enough test cases to drive the development in the developer's local dev environment. 
That had to be balanced with the developer should never write code that waits too long to have tests run against it. 
This is to prevent testing in medium batches after coding and actually work towards red green refactor. 
We don't want an inventory of untested code building because then we'd be waiting for the developer to redo the work and we'd find ourselves ahead again. 
If the tester was ahead, they'd work on improvements to make the next cycle quicker or go help someone else. 
What would happen if the tester was too far ahead? Then until we got to the end we'd never see all the test suites pass every day.
I don't think this would be great for TBD, your pipeline would never complete successfully. 
2. The code should only be deployed to QA just in time for a regression to finish before the deploy into the customer facing environment. 
This is to avoid dumping a whole bunch of code into QA and then face the pressure of having to sign-off on everything before it can leave the environment. 
There were times where the project managers and development managers would downgrade defect severities just to get the sign-off and promote buggy code into production.