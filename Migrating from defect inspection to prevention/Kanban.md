---
title: Kanban
---

Explain how git was used as the kanban system.
Each git commit was a box.
Add Ryan's kanban video to explain it.
Describe WIP limits
> Setting WIP limits helped by reducing the time context switching from one feature to another every day or multiple times in a day.  
> The challenge was that we had a system where half the time is spent fixing production issues.  
> That means that we needed to get information from the business users and so we spent quite a bit of time waiting so then we had to increase those WIP limits.   
> The scope of my system was the QA inspection process and things like code coming in or information from business users about production issues were just seeing as orders from customers with a high degree of fluctuation.


> Since the tests were driving the development, imagine each batch of tests as requisitions for code to be created.  
> They needed enough to keep the developer busy but don't need to create millions of extra test cases if the developer will never get to them.  
> Just as we don't have to have long lived branches with tonnes of git commits, I didn't want the testers make huge inventories of tests.
> The bigger the inventory of tests, the higher the probability they would need to be re-worked or skipped altogether.

> I taught the testers to amend their git commits and only when they had the next batch of tests, they would push it.  
> This is why my testers had to get a head start.  
> The developers would do their initial analysis while my testers created some key test cases as they'd call it.  
> Then with this lead of a few days of tests for developers to run, they'd replenish one per day.  
> Developers then could keep doing a fetch and only merge with the next git commit and work on those tests.  
> I think some developers just did a pull but that was ok since there would only be 1 git commit added each day.  

> Why did I care about this? Well, what I didn't want to have is failing tests all the time.  
> I was aiming for Continuous Delivery and Trunk Based development
> Let's say the tester is always ahead, then you'd never see all the test suites pass.  
> This isn't great for TBD, your pipeline would never complete successfully.  
> I wanted the developer and tester to learn to synchronise (reduce variation/fluctuation)
