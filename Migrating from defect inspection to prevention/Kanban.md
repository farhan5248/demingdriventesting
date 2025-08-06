---
title: Kanban
---

Only my team-leads and I used the Kanban board to manage the workload.
Setting WIP limits helped by reducing the time context switching from one feature to another every day or multiple times in a day. 
The challenge was that we had a system where half the time is spent fixing production issues. 
That means that we needed to get information from the business users and so we spent quite a bit of time waiting so then we had to increase those WIP limits. 
The scope of my system was the QA inspection process. 
Things like code coming in or information from business users about production issues were just seen as orders from customers or parts from upstream suppliers with a high degree of fluctuation.

When it came to the use of bins in Kanban, that's what a Git commit was for as it was important for managing inventory (branches).
Before the testers were working in the dev environment in small batches, they were working in larger batches which I saw as inventory such as:
1. Test cases waiting to be executed after the code was deployed to QA.
2. Executed test cases waiting to be automated after the tester does a sign-off.
3. Automated test cases waiting to be reviewed by the tester after all automation was completely run successfully by the automation developer.
4. Fixed bugs waiting to be re-tested after cycle 1 testing.

On the development side I'd say they had inventories of:
1. Code sitting on branches waiting to be deployed to QA.
2. Pull requests waiting to be merged.

The [coin flip game](https://www.leansimulations.org/2010/11/penny-game.html) demonstrates the benefit of using smaller batch sizes.
I demonstrated it for my team and told them we want [one piece flow](https://www.allaboutlean.com/one-piece-flow/) (in my mind trunk based development or continuous delivery) with as close to 0 but not 0 inventory.
Over months we kept reducing the size of batches and that reduced the size of inventories above.
1. Nothing was waiting to be executed because they were executed hourly or daily.
2. Nothing was waiting to be automated because that process was automated.
3. Nothing was waiting to be reviewed since the tester created their own automation.
4. Developers found and fixed bugs by running the tests so virtually no defects were found in QA waiting to be re-tested.

How small did the batches get when the tests were driving the development?
Imagine each batch of tests as necessary inputs for code to be created. 
I taught the testers to craft/amend their git commits and only when they had the next batch of tests, they would push it. 
Each commit had to keep a developer busy for roughly a day.
Before this, testers would save up a week's worth of work and then push it at the end.
Over time they slowly learnt to match the pace of the developers and commit often and early. 