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
Since the tests were driving the development, imagine each batch of tests as necessary inputs for code to be created. 
I taught the testers to craft/amend their git commits and only when they had the next batch of tests, they would push it. 
Each commit had to keep a developer busy for roughly a day.
Before this, testers would save up a week's worth of work and then push it at the end.
The thing to remember is the team learnt to use Git months before the developers got involved.
So to them, Git was like SharePoint or the shared drive, just another tool for back-up or access for the Jenkins servers to run the regression.