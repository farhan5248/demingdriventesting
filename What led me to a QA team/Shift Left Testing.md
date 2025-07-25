---
title: Shift Left Testing
---

The way I try to explain BDD is that it's like TDD but with the 3 amigos. 
For the next release we used Cucumber but since the QA team still preferred to do their own thing, only the BSA and developers used it. 
The developer was a new senior developer and the code for this feature had to be written in Java for the first time. 
From the start, we incrementally took the requirements and the corresponding test case from QA and converted them to feature files. 
Even though we used the QA test cases, this developer still had half a dozen defects. Why? 

One was a documentation one. The test case simply said "as documented". The developer read the referenced doc and implemented it that way. 
It turns out the documentation was wrong. What the tester thought was in the document and what they tested was different. 
Another defect was logged after the tester discussed a different interpretation with the BSA and she changed the requirements right then and there. 
The pattern here was that while the developer and BSA read the tester's test cases, the tester didn't read what we had in Cucumber. 
Again I thought of the project management tree swing. The tester was in a silo and we only got to know their precise expectation at the time they ran the tests.

The other source of defects was from the other developer. He was also senior but not new. The two developers worked closely together helping each other. 
The more experienced developer however could re-use code for his part which was quite small in comparison to the Java code. 
He had roughly ten times fewer test cases, but ten times more defects. 
I'll see this pattern again working with the COBOL developers; new junior developer with more tests producing virtually defect free code.

Overall there was much less re-work on both teams but the delay still existed. 
Yet again, it was the QA process to manually test everything first before running anything automated so we had to wait for weeks. 
Had the manual tester been part of 3 amigos exercise, not only would we have no defects and re-work but also no days/weeks long delays. 
It's around this time did I learn of the phrase shift left testing and [Dr Deming's quote of "You burn, I'll scrape"](https://deming.org/you-burn-ill-scrape/)

As a reminder, even though the architecture team was closely aligned with my dev team we weren't on the same team, we had different managers.
I concluded that the tester had to be part of the dev team or at least have leadership that was aligned with the development team. 
